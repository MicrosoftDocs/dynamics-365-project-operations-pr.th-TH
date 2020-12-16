---
title: ซิงโครไนซ์สัญญาโครงการและโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations
description: หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้เพื่อซิงโครไนซ์สัญญาโครงการและโครงการโดยตรงจาก Microsoft Dynamics 365 Project Service Automation ไปยัง Dynamics 365 Finance
author: Yowelle
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0b3bc159fff25c4f6e5b1ed1b2eabbba675fb0f5
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642656"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>ซิงโครไนซ์สัญญาโครงการและโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้เพื่อซิงโครไนซ์สัญญาโครงการและโครงการโดยตรงจาก Dynamics 365 Project Service Automation ไปยัง Dynamics 365 Finance

> [!NOTE] 
> หากคุณใช้ Enterprise edition รุ่น 7.3.0 คุณต้องติดตั้ง KB 4074835

## <a name="data-flow-for-project-service-automation-to-finance"></a>โฟลว์ข้อมูลสำหรับ Project Service Automation กับ Finance

> [!NOTE]
> ก่อนที่คุณจะสามารถใช้โซลูชันการรวม Project Service Automation กับ Finance คุณควรทำความคุ้นเคยกับคุณลักษณะการรวมข้อมูล Dynamics 365

โซลูชันการรวม Project Service Automation กับ Finance ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนซ์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance แม่แบบการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ข้อมูลเกี่ยวกับสัญญาโครงการ โครงการ รายละเอียดการให้บริการตามสัญญา และเป้าหมายรายละเอียดการให้บริการตามสัญญาจาก Project Service Automation ไปยัง Finance

ภาพประกอบต่อไปนี้แสดงวิธีซิงโครไนซ์ข้อมูลระหว่าง Project Service Automation และ Finance

[![โฟลว์ข้อมูลสำหรับการรวม Project Service Automation กับ Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>แม่แบบและงาน

ในการเข้าถึงแม่แบบที่พร้อมใช้งาน ในศูนย์การจัดการ Microsoft Power Apps เลือก **โครงการ** และจากนั้น ที่มุมขวาบน ให้เลือก **โครงการใหม่** เพื่อเลือกแม่แบบสาธารณะ

แม่แบบและงานพื้นฐานต่อไปนี้ถูกใช้เพื่อซิงโครไนซ์การประมาณค่าใช้จ่ายสัญญาโครงการและโครงการจาก Project Service Automation ไปยัง Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>รวมกับ Dynamics 365 Project Service Automation v2.x
- **ชื่อของแม่แบบในการรวมข้อมูล:** โครงการและสัญญา (PSA ไปยัง Fin และ Ops)
- **ชื่อของงานในโครงการ:**

    - โครงการทำสัญญา PSA ไปยัง Fin และ Ops
    - โครงการ PSA ไปยัง Fin และ Ops
    - รายละเอียดการให้บริการตามสัญญาของโครงการ PSA ไปยัง Fin และ Ops
    - เป้าหมายรายละเอียดการให้บริการตามสัญญาของโครงการ PSA ไปยัง Fin และ Ops
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>รวมกับ Dynamics 365 Project Service Automation v3.x
มีการเปลี่ยนแปลง Schema ใน Project Service Automation ที่ส่งผลกระทบต่อแม่แบบเป้าหมายรายละเอียดการให้บริการตามสัญญาของโครงการและการใช้แม่แบบเวอร์ชัน v2 จึงจำเป็นต้องรวม Project Service Automation v3.x เข้ากับ Dynamics 365

- **ชื่อของแม่แบบในการรวมข้อมูล:** โครงการและสัญญา (PSA 3.x ไปยัง Fin และ Ops) - v2
- **ชื่อของงานในโครงการ:**

    - โครงการทำสัญญา PSA ไปยัง Fin และ Ops
    - โครงการ PSA ไปยัง Fin และ Ops
    - รายละเอียดการให้บริการตามสัญญาของโครงการ PSA ไปยัง Fin และ Ops
    - เป้าหมายรายละเอียดการให้บริการตามสัญญาของโครงการ PSA ไปยัง Fin และ Ops

ก่อนที่จะเกิดการซิงโครไนซ์สัญญาโครงการและโครงการ คุณต้องซิงโครไนซ์บัญชี

## <a name="entity-set"></a>ชุดเอนทิตี

| Project Service Automation       | Finance                                                |
|----------------------------------|--------------------------------------------------------|
| ใบสั่ง                           | เอนทิตีการรวมสำหรับสัญญาโครงการ                |
| โครงการ                         | เอนทิตีการรวมสำหรับโครงการ                         |
| รายการในใบสั่ง                      | เอนทิตีการรวมสำหรับรายละเอียดการให้บริการตามสัญญาของโครงการ           |
| เป้าหมายรายละเอียดการให้บริการตามสัญญาของโครงการ | เอนทิตีการรวมสำหรับเป้าหมายของรายละเอียดการให้บริการตามสัญญาของโครงการ |

## <a name="entity-flow"></a>โฟลว์เอนทิตี

สัญญาโครงการได้รับการจัดการใน Project Service Automation และมีการซิงโครไนซ์กับ Finance เป็นสัญญาของโครงการ ในฐานะส่วนหนึ่งของแม่แบบการรวม คุณสามารถตั้งค่าแหล่งการรวมใน Finance สำหรับสัญญาโครงการ

โครงการเวลาและวัสดุและโครงการราคาคงที่ได้รับการจัดการใน Project Service Automation และมีการซิงโครไนซ์กับ Finance เป็นโครงการ ในฐานะส่วนหนึ่งของการรวมแม่แบบ คุณสามารถตั้งค่าแหล่งการรวมใน Finance สำหรับโครงการ

รายละเอียดการให้บริการตามสัญญาของโครงการได้รับการจัดการใน Project Service Automation และมีการซิงโครไนซ์กับ Finance เป็นกฎการเรียกเก็บเงินของสัญญา หากวิธีการเรียกเก็บเงินแตกต่างจากประเภทโครงการเริ่มต้น การซิงโครไนซ์จะอัปเดตประเภทโครงการสำหรับโครงการรายละเอียดการให้บริการตามสัญญาและกลุ่มโครงการ

เป้าหมายของรายละเอียดการให้บริการตามสัญญาของโครงการได้รับการจัดการใน Project Service Automation และมีการซิงโครไนซ์กับ Finance เป็นเป้าหมายกฎการเรียกเก็บเงินของสัญญา

## <a name="project-service-automation-to-finance-integration-solution"></a>การรวม Project Service Automation กับโซลูชันการรวม

ฟิลด์ **รหัสสัญญาโครงการ** มีอยู่ในหน้า **สัญญาโครงการ** ฟิลด์นี้เป็นคีย์ที่เป็นธรรมชาติและไม่ซ้ำในการสนับสนุนการรวม

เมื่อมีการสร้างสัญญาโครงการใหม่ ถ้าค่า **รหัสสัญญาโครงการ** ไม่มีอยู่ ค่านี้สร้างขึ้นโดยอัตโนมัติโดยใช้ลำดับตัวเลข ค่าประกอบด้วย **ORD** ตามด้วยลำดับตัวเลขที่เพิ่มขึ้นแล้วต่อท้ายด้วยอักขระหกตัว นี่เป็นตัวอย่าง: **ORD-01022-Z4M9Q0**

ฟิลด์ **ตัวเลขโครงการ** มีอยู่ในหน้า **โครงการ** ฟิลด์นี้เป็นคีย์ที่เป็นธรรมชาติและไม่ซ้ำในการสนับสนุนการรวม

เมื่อมีการสร้างสัญญาโครงการใหม่ ถ้าค่า **ตัวเลขโครงการ** ไม่มีอยู่ ค่านี้สร้างขึ้นโดยอัตโนมัติโดยใช้ลำดับตัวเลข ค่าประกอบด้วย **PRJ** ตามด้วยลำดับตัวเลขที่เพิ่มขึ้นแล้วต่อท้ายด้วยอักขระหกตัว นี่เป็นตัวอย่าง: **PRJ-01049-CCNID0**

เมื่อใช้โซลูชันการรวม Project Service Automation กับ Finance สคริปต์อัปเกรดจะตั้งค่าฟิลด์ **รหัสสัญญาโครงการ** สำหรับสัญญาโครงการที่มีอยู่และฟิลด์ **หมายเลขโครงการ** สำหรับโครงการที่มีอยู่ใน Project Service Automation

## <a name="prerequisites-and-mapping-setup"></a>ข้อกำหนดเบื้องต้นและการตั้งค่าการแม็ป

- ก่อนที่จะเกิดการซิงโครไนซ์สัญญาโครงการและโครงการ คุณต้องซิงโครไนซ์บัญชี
- ในชุดการเชื่อมต่อของคุณ เพิ่มการแม็ปฟิลด์คีย์การรวมสำหรับ **msdyn\_organizationalunits** ไปยัง **msdyn\_name \[ชื่อ\]** ก่อนอื่นคุณอาจต้องเพิ่มโครงการลงในชุดการเชื่อมต่อ สำหรับข้อมูลเพิ่มเติม โปรดดู [รวมข้อมูลลงใน Common Data Service สำหรับแอป](https://docs.microsoft.com/powerapps/administrator/data-integrator)
- ในชุดการเชื่อมต่อของคุณ เพิ่มการแม็ปฟิลด์คีย์การรวมสำหรับ **msdyn\_projects** ไปยัง **msdynce\_projectnumber \[หมายเลขโครงการ\]** ก่อนอื่นคุณอาจต้องเพิ่มโครงการลงในชุดการเชื่อมต่อ สำหรับข้อมูลเพิ่มเติม โปรดดู [รวมข้อมูลลงใน Common Data Service สำหรับแอป](https://docs.microsoft.com/powerapps/administrator/data-integrator)
- **SourceDataID** สำหรับสัญญาโครงการและโครงการสามารถอัปเดตเป็นค่าอื่นหรือลบออกจากการแม็ป ค่าแม่แบบเริ่มต้นคือ **Project Service Automation**
- การแม็ป **เงื่อนไขการชำระเงิน** ต้องอัปเดตเพื่อให้แสดงเงื่อนไขการชำระเงินที่ถูกต้องใน Finance คุณยังสามารถลบการแม็ปออกจากงานโครงการได้ แม็ปค่าเริ่มต้นมีค่าเริ่มต้นสำหรับข้อมูลสาธิต ตารางต่อไปนี้แสดงค่าใน Project Service Automation

    | Value | รายละเอียด   |
    |-------|---------------|
    | 1     | 30 วันสุทธิ        |
    | 2     | 2% 10, 30 วันสุทธิ |
    | 3     | 45 วันสุทธิ        |
    | 4     | 60 วันสุทธิ        |

## <a name="power-query"></a>Power Query

คุณต้องใช้ Microsoft Power Query สำหรับ Excel เพื่อกรองข้อมูล หากตรงตามเงื่อนไขต่อไปนี้:

- คุณมีใบสั่งขายใน Dynamics 365 Sales
- คุณมีหน่วยขององค์กรหลายหน่วยใน Project Service Automation และหน่วยขององค์กรเหล่านี้จะถูกแม็ปกับนิติบุคคลหลายแห่งใน Finance

หากคุณต้องใช้ Power Query ให้ปฏิบัติตามแนวทางเหล่านี้:

- แม่แบบโครงการและสัญญา (PSA กับ Fin and Ops) มีตัวกรองเริ่มต้นที่รวมเฉพาะใบสั่งขายของประเภท **รายการงาน (msdyn\_ordertype = 192350001)** ตัวกรองนี้ช่วยรับประกันว่าไม่ได้สร้างสัญญาโครงการสำหรับใบสั่งขายใน Finance หากคุณสร้างแม่แบบของคุณเอง คุณต้องเพิ่มตัวกรองนี้
- คุณต้องสร้างตัวกรอง Power Query ที่มีเฉพาะองค์กรที่ทำสัญญาเท่านั้นที่ควรซิงโครไนซ์กับนิติบุคคลของชุดการเชื่อมต่อการรวม ตัวอย่างเช่น สัญญาโครงการที่คุณมีกับหน่วยองค์กรตามสัญญาของ Contoso US ควรซิงโครไนซ์กับนิติบุคคล USSI แต่สัญญาโครงการที่คุณมีกับหน่วยองค์กรตามสัญญาของ Contoso Global ควรซิงโครไนซ์กับนิติบุคคลของ USMF หากคุณไม่เพิ่มตัวกรองนี้ในการแม็ปงานของคุณ สัญญาโครงการทั้งหมดจะซิงโครไนซ์กับนิติบุคคลที่กำหนดไว้สำหรับชุดการเชื่อมต่อ โดยไม่คำนึงถึงหน่วยขององค์กรตามสัญญา

## <a name="template-mapping-in-data-integration"></a>การแม็ปแม่แบบในการรวมข้อมูล

> [!NOTE] 
> ฟิลด์ **การอ้างอิงของลูกค้า** **ที่อยู่เมือง** **รหัสภูมิภาคในประเทศ** **คำอธิบายที่อยู่** **ที่อยู่บรรทัดที่ 1** **ที่อยู่บรรทัดที่ 2** **รัฐที่อยู่** และ **รหัสไปรษณีย์ตามที่อยู่** ไม่รวมอยู่ในการแม็ปเริ่มต้นสำหรับสัญญาโครงการ คุณสามารถเพิ่มการแม็ปได้ หากคุณต้องการให้ซิงโครไนซ์ข้อมูลนี้สำหรับสัญญาโครงการ
>
> ฟิลด์ **คำอธิบาย** **รหัสหลัก** **กลุ่มโครงการ** **หมายเลขส่วนตัวของผู้จัดการโครงการ** และ **ประเภทโครงการ** ไม่รวมอยู่ในการแม็ปเริ่มต้นสำหรับโครงการ คุณสามารถเพิ่มการแม็ปได้หากคุณต้องการให้ซิงโครไนซ์ข้อมูลนี้สำหรับโครงการ

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานแม่แบบในการรวมข้อมูล การแม็ปแสดงข้อมูลฟิลด์ที่จะซิงโครไนซ์จาก Project Service Automation ไปยัง Finance

[![การแม็ปแม่แบบสัญญาโครงการ](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![การแม็ปแม่แบบโครงการ](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![การแม็ปแม่แบบรายละเอียดการให้บริการตามสัญญาโครงการ](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![การแม็ปแม่แบบเหตุการณ์สำคัญรายละเอียดการให้บริการตามสัญญาโครงการ](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>การแม็ปเป้าหมายรายละเอียดการให้บริการตามสัญญาโครงการในโครงการและสัญญา (PSA 3.x ถึง Dynamics) - แม่แบบ v2:

[![การแม็ปเหตุการณ์สำคัญรายละเอียดการให้บริการตามสัญญาโครงการพร้อมแม่แบบรุ่นสอง](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
