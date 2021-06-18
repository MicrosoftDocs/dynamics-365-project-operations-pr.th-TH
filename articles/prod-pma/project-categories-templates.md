---
title: ซิงโครไนซ์ประเภทค่าใช้จ่ายโครงการระหว่าง Finance and Operations และ Project Service Automation
description: หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้เพื่อซิงโครไนซ์ประเภทค่าใช้จ่ายของโครงการระหว่าง Microsoft Dynamics 365 Finance และ Dynamics 365 Project Service Automation
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999874"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>ซิงโครไนซ์ประเภทค่าใช้จ่ายโครงการระหว่าง Finance and Operations และ Project Service Automation

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้เพื่อซิงโครไนซ์ประเภทค่าใช้จ่ายของโครงการระหว่าง Dynamics 365 Finance และ Dynamics 365 Project Service Automation

> [!NOTE]
> - การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประมาณชั่วโมง การประมาณค่าใช้จ่าย และการล็อกฟังก์ชัน จะพร้อมใช้งานในเวอร์ชัน 8.0
> - การรวมจริงพร้อมใช้งานในเวอร์ชัน 8.0.1 หรือใหม่กว่า
> - หากคุณใช้ Enterprise Edition 7.3.0 หลังจากที่คุณติดตั้ง KB 4132657 และ KB 4132660 คุณจะสามารถใช้แม่แบบเพื่อรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประมาณชั่วโมง การประมาณค่าใช้จ่ายและข้อมูลจริง และเพื่อตั้งค่าคอนฟิกการล็อกฟังก์ชัน หากคุณต้องรีเซ็ตการกระจายการลงบัญชี เราขอแนะนำให้คุณติดตั้ง KB 4131710 ด้วย

## <a name="data-flow-for-project-service-automation-and-finance"></a>โฟลว์ข้อมูลสำหรับ Project Service Automation และ Finance

โซลูชันการรวม Project Service Automation และ Finance ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนซ์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance แม่แบบการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ของข้อมูลเกี่ยวกับประเภทธุรกรรมค่าใช้จ่ายโครงการระหว่าง Project Service Automation และ Finance

ถ้าประเภทค่าใช้จ่ายของโครงการมีการต่อยอดใน Finance ขั้นตอนการรวมจะเริ่มจาก Finance ไปยัง Project Service Automation จากนั้นรหัสการรวมของประเภทค่าใช้จ่ายโครงการจะถูกอัปเดตผ่านการซิงโครไนซ์จาก Project Service Automation ไปยัง Finance

ถ้าประเภทค่าใช้จ่ายของโครงการมีการต่อยอดใน Project Service Automation โฟลว์การรวมจะเริ่มจาก Project Service Automation ไปยัง Finance ประเภทโครงการต้องได้รับการกำหนดค่าไว้แล้วใน Finance ก่อนการซิงโครไนซ์จาก Project Service Automation จากนั้นซิงโครไนซ์จาก Finance กลับไปยัง Project Service Automation จากนั้นจาก Project Service Automation ไปยัง Finance อีกครั้ง ด้วยวิธีนี้คุณช่วยรับประกันได้ว่าประเภทต่างๆ จะเชื่อมโยงกันและไม่มีการสร้างรายการซ้ำ

> [!NOTE]
> โดยทั่วไปแล้วประเภทค่าใช้จ่ายโครงการจะมีการต่อยอดในด้านการเงิน อย่างไรก็ตามหากไม่เป็นเช่นนั้นหรือหากมีการสร้างประเภทค่าใช้จ่ายใน Project Service Automation ก่อนอื่นคุณต้องซิงโครไนซ์โดยใช้แม่แบบประเภทธุรกรรมค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin และ Ops) จากนั้นซิงโครไนซ์โดยใช้แม่แบบประเภทธุรกรรมค่าใช้จ่ายโครงการ (Fin และ Ops ไปยัง PSA) จากนั้นคุณควรเรียกใช้การซิงโครไนซ์จาก Project Service Automation ไปยัง Finance อีกครั้ง
>
> ถ้าคุณซิงโครไนซ์ก่อนจาก Project Service Automation ต้องปฏิบัติตามข้อกำหนดต่อไปนี้ใน Finance ก่อนที่จะรันการซิงโครไนซ์:
>
> - ประเภทที่ใช้ร่วมกันที่ตรงกับประเภทโครงการที่ตั้งค่าใน Project Service Automation ต้องมีอยู่และต้องเปิดใช้งานสำหรับทั้ง **โครงการ** และ **ค่าใช้จ่าย**
> - สำหรับนิติบุคคลทางการเงินแต่ละรายที่ต้องรวมเข้าด้วยกัน ต้องมีประเภทโครงการต่อไปนี้:
>
>     - **ประเภทโครงการ** มีอยู่ 
>     - เปิดใช้งาน **ใช้ในค่าใช้จ่าย**
>     - เปิดใช้งาน **ใช้งานอยู่ในสมุดรายวัน**
>     - **ประเภทธุรกรรม** ถูกตั้งค่าเป็น **ค่าใช้จ่าย**

ภาพประกอบต่อไปนี้แสดงวิธีซิงโครไนซ์ข้อมูลระหว่าง Project Service Automation และ Finance

[![โฟลว์ข้อมูลสำหรับการรวม Project Service Automation กับ Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>การซิงโครไนซ์ประเภทค่าใช้จ่ายโครงการจาก Finance ไปยัง Project Service Automation

### <a name="template-and-task"></a>แม่แบบและงาน

ในการเข้าถึงแม่แบบ ในศูนย์การจัดการ Microsoft Power Apps เลือก **โครงการ** และจากนั้น ที่มุมขวาบน ให้เลือก **โครงการใหม่** เพื่อเลือกแม่แบบสาธารณะ

แม่แบบและงานพื้นฐานต่อไปนี้ถูกใช้เพื่อซิงโครไนซ์ประเภทค่าใช้จ่ายโครงการจาก Finance ไปยัง Project Service Automation:

- **ชื่อของแม่แบบในการรวมข้อมูล:** ประเภทธุรกรรมค่าใช้จ่ายโครงการ (Fin และ Ops ไปยัง PSA)
- **ชื่อของงานในโครงการ:** ซิงค์ประเภทกับ PSA

### <a name="entity-set"></a>ชุดเอนทิตี

| Finance                           | Project Service Automation |
|-----------------------------------|----------------------------|
| เอนทิตีการรวมสำหรับประเภท | ประเภทธุรกรรม     |

### <a name="entity-flow"></a>โฟลว์เอนทิตี

ประเภทค่าใช้จ่ายโครงการได้รับการจัดการใน Finance และมีการซิงโครไนซ์กับ Project Service Automation เป็นประเภทค่าใช้จ่าย

### <a name="power-query"></a>Power Query

เมื่อคุณซิงโครไนซ์กับ Project Service Automation คุณต้องใช้ Microsoft Power Query สำหรับ Excel เพื่อตั้งค่าประเภทการเรียกเก็บเงินในประเภทธุรกรรม แม่แบบประเภทธุรกรรมค่าใช้จ่ายโครงการ (Fin และ Ops ไปยัง PSA) มีคอลัมน์และการแม็ปเริ่มต้น หากคุณสร้างแม่แบบของคุณเอง คุณต้องเพิ่มคอลัมน์เงื่อนไขใน Power Query ให้ทำตามขั้นตอนเหล่านี้

1. คลิกลูกศรเพื่อเปิดการแม็ปของงานประเภทค่าใช้จ่ายโครงการในแม่แบบประเภทธุรกรรมค่าใช้จ่ายโครงการ (Fin และ Ops ไปยัง PSA)
2. คลิกลิงก์ **การสืบค้นและการกรองขั้นสูง** เพื่อเปิด Power Query
2. เลือก **เพิ่มคอลัมน์เงื่อนไข**
3. ป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **BillingType**
4. ป้อนเงื่อนไขต่อไปนี้: **ถ้า CATEGORYID ไม่เท่ากับ null ดังนั้นเท่ากับ 19235001 มิฉะนั้นจะเป็น null**
5. คลิก **ตกลง** บนคอลัมน์
6. อย่าลืมแม็ปคอลัมน์ใหม่นี้ในหน้าการแม็ป

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานแม่แบบในการรวมข้อมูล การแม็ปแสดงข้อมูลฟิลด์ที่จะซิงโครไนซ์จาก Finance ไปยัง Project Service Automation

[![ซ์ประเภทค่าใช้จ่ายโครงการไปยังการแม็ปแม่แบบ Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>การซิงโครไนซ์ประเภทค่าใช้จ่ายโครงการจาก Project Service Automation ไปยัง Finance

### <a name="template-and-task"></a>แม่แบบและงาน

แม่แบบและงานพื้นฐานต่อไปนี้ถูกใช้เพื่อซิงโครไนซ์ประเภทค่าใช้จ่ายโครงการจาก Project Service Automation ไปยัง Finance:

- **ชื่อของแม่แบบในการรวมข้อมูล:** ประเภทธุรกรรมค่าใช้จ่ายโครงการ (PSA ไปยัง Fin และ Ops)
- **ชื่อของงานในโครงการ:** ซิงค์ประเภทกับ Fin Ops

### <a name="entity-set"></a>ชุดเอนทิตี

| Project Service Automation | Finance                           |
|----------------------------|-----------------------------------|
| ประเภทธุรกรรม     | เอนทิตีการรวมสำหรับประเภท |

### <a name="entity-flow"></a>โฟลว์เอนทิตี

ประเภทค่าใช้จ่ายโครงการได้รับการจัดการใน Finance และมีการซิงโครไนซ์กับ Project Service Automation เป็นประเภทค่าใช้จ่าย การซิงโครไนซ์กลับไปที่ Finance จะอัปเดตประเภทโครงการใน Finance ด้วยรหัสการรวมจาก Project Service Automation

### <a name="template-mapping-in-data-integration"></a>การแม็ปแม่แบบในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานแม่แบบในการรวมข้อมูล

> [!NOTE]
> การแม็ปแสดงข้อมูลฟิลด์ที่จะซิงโครไนซ์จาก Project Service Automation ไปยัง Finance

[![การแม็ปแม่แบบ Project Service Automation กับ Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]