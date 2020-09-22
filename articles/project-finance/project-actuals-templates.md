---
title: ซิงโครไนซ์ข้อมูลจริงของโครงการโดยตรงจาก Project Service Automation ไปยังสมุดรายวันการรวมโครงการเพื่อลงรายการบัญชีใน Finance and Operations
description: หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้เพื่อซิงโครไนซ์ค่าจริงของโครงการโดยตรงจาก Microsoft Dynamics 365 Project Service Automation ไปยัง Finance and Operations
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 02ae4986-8e7b-4abe-97d3-cff0904d84de
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7e5aff102226e5eac2ba3de17407eaa4461cd1ac
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756452"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>ซิงโครไนซ์ข้อมูลจริงของโครงการโดยตรงจาก Project Service Automation ไปยังสมุดรายวันการรวมโครงการเพื่อลงรายการบัญชีใน Finance and Operations

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้เพื่อซิงโครไนซ์ค่าจริงของโครงการโดยตรงจาก Dynamics 365 Project Service Automation ไปยัง Dynamics 365 Finance

แม่แบบซิงโครไนซ์ธุรกรรมจาก Project Service Automation ไปยังตารางการจัดเตรียมใน Finance หลังจากการซิงโครไนซ์เสร็จสิ้น คุณ **ต้อง** นำเข้าข้อมูลจากตารางการจัดเตรียมลงในสมุดรายวันการรวม

> [!NOTE]
> - การรวมค่าจริงโครงการพร้อมใช้งานตั้งแต่เวอร์ชัน 8.0.1
> - หากคุณใช้ Enterprise Edition 7.3.0 หลังจากที่คุณติดตั้ง KB 4132657 และ KB 4132660 คุณจะสามารถใช้แม่แบบเพื่อรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประมาณชั่วโมง การประมาณค่าใช้จ่ายและข้อมูลจริง และเพื่อตั้งค่าคอนฟิกการล็อกฟังก์ชัน หากคุณต้องรีเซ็ตการกระจายการลงบัญชี เราขอแนะนำให้คุณติดตั้ง KB 4131710 ด้วย
> - หากคุณใช้เวอร์ชัน 7.3.0 และคุณนำธุรกรรมค่าธรรมเนียมมาจาก Project Service Automation คุณต้องติดตั้ง KB 4345320 เพื่อรวมค่าธรรมเนียมเหล่านั้นในใบแจ้งหนี้โครงการ
> - ถ้าคุณกำลังป้อนยอดภาษีขายตรงเวลาหรือธุรกรรมค่าใช้จ่ายใน Project Service Automation คุณต้องติดตั้ง Project Service Automation รุ่นอัปเดต 7 มิฉะนั้นภาษีจะไม่เชื่อมโยงกับเวลาที่เกี่ยวข้องหรือค่าใช้จ่ายที่เกิดขึ้นจริงและจะไม่ซิงโครไนซ์กับ Finance สำหรับข้อมูลเพิ่มเติม โปรดติดต่อทีมสนับสนุน

## <a name="data-flow-for-project-service-automation-to-finance"></a>โฟลว์ข้อมูลสำหรับ Project Service Automation กับ Finance

โซลูชันการรวม Project Service Automation กับ Finance ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนซ์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance แม่แบบการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ของข้อมูลเกี่ยวกับค่าจริงของโครงการจาก Project Service Automation ไปยัง Finance

ภาพประกอบต่อไปนี้แสดงวิธีซิงโครไนซ์ข้อมูลระหว่าง Project Service Automation และ Finance

[![โฟลว์ข้อมูลสำหรับการรวม Project Service Automation กับ Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>ค่าจริงของโครงการจาก Project Service Automation

### <a name="template-and-tasks"></a>แม่แบบและงาน

ในการเข้าถึงแม่แบบที่พร้อมใช้งาน ในศูนย์การจัดการ Microsoft Power Apps เลือก **โครงการ** และจากนั้น ที่มุมขวาบน ให้เลือก **โครงการใหม่** เพื่อเลือกแม่แบบสาธารณะ

แม่แบบและงานพื้นฐานต่อไปนี้ถูกใช้เพื่อซิงโครไนซ์ค่าจริงของโครงการจาก Project Service Automation ไปยัง Finance:

- **ชื่อของแม่แบบในการรวมข้อมูล:** ค่าจริงของโครงการ (PSA ไปยัง Fin และ Ops)
- **ชื่อของงานในโครงการ:**

    - ข้อมูลจริง
    - การเชื่อมต่อธุรกรรม

### <a name="entity-set"></a>ชุดเอนทิตี

| Project Service Automation | Finance                                   |
|----------------------------|----------------------------------------------------------|
| ข้อมูลจริง                    | เอนทิตีการรวมสำหรับค่าจริงของโครงการ                   |
| การเชื่อมต่อธุรกรรม    | เอนทิตีการรวมสำหรับความสัมพันธ์ธุรกรรมโครงการ |

### <a name="entity-flow"></a>โฟลว์เอนทิตี

ค่าจริงของโครงการได้รับการจัดการใน Project Service Automation และมีการซิงโครไนซ์กับสมุดรายวันการรวมโครงการใน Finance การบัญชีจะถูกนำไปใช้ตามมิติทางการเงินเริ่มต้นและการตั้งค่าการลงรายการบัญชี

### <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่การซิงโครไนซ์ของค่าจริงจะเกิดขึ้น คุณต้องกำหนดค่าพารามิเตอร์การรวม Project Service Automation และซิงโครไนซ์โครงการ งานโครงการ และประเภทธุรกรรมค่าใช้จ่ายของโครงการ

### <a name="power-query"></a>Power Query

ในแม่แบบค่าจริงของโครงการ คุณต้องใช้ Microsoft Power Query สำหรับ Excel เพื่อทำงานเหล่านี้ให้เสร็จสิ้น:

- แปลงชนิดธุรกรรมใน Project Service Automation เป็นชนิดธุรกรรมที่ถูกต้องใน Finance การเปลี่ยนแปลงนี้ได้กำหนดไว้แล้วในแม่แบบ Project actuals (PSA ไปยัง Fin and Ops)
- แปลงชนิดการเรียกเก็บเงินใน Project Service Automation เป็นชนิดการเรียกเก็บเงินที่ถูกต้องใน Finance การเปลี่ยนแปลงนี้ได้กำหนดไว้แล้วในแม่แบบ Project actuals (PSA ไปยัง Fin and Ops) จากนั้นประเภทการเรียกเก็บเงินจะถูกจับคู่กับคุณสมบัติรายการ ตามการกำหนดค่าบนหน้า **พารามิเตอร์การรวม Project Service Automation**
- กรองหน่วยขององค์กรทรัพยากรเฉพาะที่ต้องซิงโครไนซ์กับแม่แบบนี้
- ถ้าค่าจริงของเวลาระหว่างบริษัทหรือค่าใช้จ่ายระหว่างบริษัทจะซิงโครไนซ์กับ Finance คุณต้องเปลี่ยนหน่วยขององค์กรตามสัญญาเป็นนิติบุคคลที่ถูกต้องใน Finance ในแม่แบบค่าจริงของโครงการ (PSA ไปยัง Fin และ Ops) คอลัมน์เงื่อนไขจะถูกกำหนดตามข้อมูลสาธิต คุณต้องอัปเดตคอลัมน์เงื่อนไขสุดท้ายที่แทรกเป็นนิติบุคคลที่ถูกต้อง มิฉะนั้นข้อผิดพลาดในการรวมอาจเกิดขึ้นหรืออาจมีการนำเข้าธุรกรรมตามจริงที่ไม่ถูกต้องไปยัง Finance
- ถ้าค่าจริงของเวลาระหว่างบริษัทหรือค่าใช้จ่ายระหว่างบริษัทจะไม่ซิงโครไนซ์กับ Finance คุณต้องลบคอลัมน์เงื่อนไขสุดท้ายที่แทรกออกจากแม่แบบของคุณ มิฉะนั้นข้อผิดพลาดในการรวมอาจเกิดขึ้นหรืออาจมีการนำเข้าธุรกรรมตามจริงที่ไม่ถูกต้องไปยัง Finance

#### <a name="contract-organizational-unit"></a>หน่วยองค์กรตามสัญญา
หากต้องการอัปเดตคอลัมน์เงื่อนไขสุดท้ายที่แทรกในแม่แบบ ให้คลิกลูกศร **แม็ป** เพื่อเปิดการแม็ป เลือกลิงก์ **การสืบค้นและการกรองขั้นสูง** เพื่อเปิด Power Query

- หากคุณกำลังใช้แม่แบบค่าจริงของโครงการเริ่มต้น (PSA ไปยัง Fin และ Ops) ใน Power Query ให้เลือก **แทรกเงื่อนไข** สุดท้ายจากส่วน **ขั้นตอนที่ใช้** ในรายการ **ฟังก์ชัน** ให้แทนที่ **USSI** ด้วยชื่อของนิติบุคคลที่ควรใช้กับการรวม เพิ่มเงื่อนไขเพิ่มเติมในรายการ **ฟังก์ชัน** ตามที่คุณต้องการและอัปเดตเงื่อนไข **อื่น** จาก **USMF** ไปเป็นนิติบุคคลที่ถูกต้อง
- หากคุณกำลังสร้างแม่แบบใหม่ คุณต้องเพิ่มคอลัมน์เพื่อรองรับเวลาและค่าใช้จ่ายระหว่างบริษัท เลือก **เพิ่มคอลัมน์เงื่อนไข**และป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **LegalEntity** ป้อนเงื่อนไขสำหรับคอลัมน์โดยที่ถ้า **msdyn\_contractorganizationalunitid.msdyn\_name** คือ \<หน่วยองค์กร\> ดังนั้น \<ป้อนนิติบุคคล\> รายการอื่นว่าง

### <a name="template-mapping-in-data-integration"></a>การแม็ปแม่แบบในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานแม่แบบในการรวมข้อมูล การแม็ปแสดงข้อมูลฟิลด์ที่จะซิงโครไนซ์จาก Project Service Automation ไปยัง Finance

[![การแม็ปแม่แบบ](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![การแม็ปแม่แบบ](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>นำเข้าจากตารางการจัดเตรียมหลังจากการรวมจาก Project Service Automation

ต้องเรียกใช้กระบวนการนำเข้าจากตารางการจัดเตรียมหลังจากการซิงโครไนซ์ของค่าจริงจาก Project Service Automation ไปยัง Finance กระบวนการนี้จะนำเข้าธุรกรรมโครงการจากตารางการจัดเตรียมลงในสมุดรายวันการรวม Project Service Automation ซึ่งการบัญชีจะถูกนำไปใช้และสามารถลงรายการบัญชีธุรกรรมที่นำเข้าได้ เราขอแนะนำให้คุณเรียกใช้กระบวนการนี้ในโหมดชุดงาน เพราะสามารถเลือกที่จะตั้งค่าให้ทำงานเป็นชุดที่เกิดซ้ำได้

## <a name="update-actuals-from-finance"></a>อัปเดตข้อมูลจริงจาก Finance

### <a name="template-and-tasks"></a>แม่แบบและงาน

แม่แบบและงานพื้นฐานต่อไปนี้ใช้เพื่อซิงโครไนซ์หมายเลขใบสำคัญและภาษีขายสำหรับธุรกรรมโครงการที่ลงรายการบัญชีจาก Finance ไปยัง Project Service Automation:

- **ชื่อของแม่แบบในการรวมข้อมูล:** การอัปเดตค่าจริงของโครงการ (Fin Ops ไปยัง PSA)
- **ชื่อของงานในโครงการ:**

    - ข้อมูลจริง 
    - การเชื่อมต่อธุรกรรม

### <a name="entity-set"></a>ชุดเอนทิตี

| Finance                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| เอนทิตีการรวมสำหรับค่าจริงของโครงการ                   | ข้อมูลจริง                    |
| เอนทิตีการรวมสำหรับความสัมพันธ์ธุรกรรมโครงการ | การเชื่อมต่อธุรกรรม    |

### <a name="entity-flow"></a>โฟลว์เอนทิตี

ค่าจริงของโครงการได้รับการจัดการใน Project Service Automation และมีการซิงโครไนซ์กับสมุดรายวันการรวมโครงการใน Finance หลังจากลงรายการบัญชีจริงใน Finance แล้วจะมีการอัปเดตใน Project Service Automation ด้วยหมายเลขใบสำคัญจาก Finance ถ้ามีการเพิ่มภาษีขายใน Finance ค่าจริงใหม่ของภาษีจะถูกสร้างขึ้นใน Project Service Automation

### <a name="power-query"></a>Power Query

ในแม่แบบการอัปเดตค่าจริงของโครงการ คุณต้องใช้ Power Query เพื่อทำงานเหล่านี้ให้เสร็จสิ้น:

- แปลงชนิดธุรกรรมใน Finance เป็นชนิดธุรกรรมที่ถูกต้องใน Project Service Automation การเปลี่ยนแปลงนี้ได้กำหนดไว้แล้วในการอัปเดตค่าจริงของแม่แบบโครงการ (Fin Ops ไปยัง PSA)
- แปลงชนิดการเรียกเก็บเงินใน Finance เป็นชนิดการเรียกเก็บเงินที่ถูกต้องใน Project Service Automation การเปลี่ยนแปลงนี้ได้กำหนดไว้แล้วในการอัปเดตค่าจริงของแม่แบบโครงการ (Fin Ops ไปยัง PSA)

### <a name="template-mapping-in-data-integration"></a>การแม็ปแม่แบบในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานแม่แบบในการรวมข้อมูล การแม็ปแสดงข้อมูลฟิลด์ที่จะซิงโครไนซ์จาก Finance ไปยัง Project Service Automation

[![การแม็ปแม่แบบ](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![การแม็ปแม่แบบ](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
