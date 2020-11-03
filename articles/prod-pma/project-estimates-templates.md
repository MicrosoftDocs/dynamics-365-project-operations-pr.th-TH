---
title: ซิงโครไนซ์การประมาณการโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations
description: หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้เพื่อซิงโครไนซ์การประมาณชั่วโมงโครงการและค่าใช้จ่ายโครงการโดยตรงจาก Microsoft Dynamics 365 Project Service Automation ไปยัง Dynamics 365 Finance
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086060"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>ซิงโครไนซ์การประมาณการโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้เพื่อซิงโครไนซ์การประมาณชั่วโมงโครงการและค่าใช้จ่ายโครงการโดยตรงจาก Dynamics 365 Project Service Automation ไปยัง Dynamics 365 Finance

> [!NOTE]
> - การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประมาณชั่วโมง การประมาณค่าใช้จ่าย และการล็อกฟังก์ชัน จะพร้อมใช้งานในเวอร์ชัน 8.0
> - การรวมจริงพร้อมใช้งานในเวอร์ชัน 8.0.1 หรือใหม่กว่า

## <a name="data-flow-for-project-service-automation-to-finance"></a>โฟลว์ข้อมูลสำหรับ Project Service Automation กับ Finance

โซลูชันการรวม Project Service Automation กับ Finance ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนซ์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance แม่แบบการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ของข้อมูลเกี่ยวกับการประมาณชั่วโมงโครงการและค่าใช้จ่ายโครงการจาก Project Service Automation ไปยัง Finance

ภาพประกอบต่อไปนี้แสดงวิธีซิงโครไนซ์ข้อมูลระหว่าง Project Service Automation และ Finance

[![โฟลว์ข้อมูลสำหรับการรวม Project Service Automation กับ Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>การประมาณการชั่วโมงโครงการ

### <a name="template-and-tasks"></a>แม่แบบและงาน

ในการเข้าถึงแม่แบบที่พร้อมใช้งาน ในศูนย์การจัดการ Microsoft Power Apps เลือก **โครงการ** และจากนั้น ที่มุมขวาบน ให้เลือก **โครงการใหม่** เพื่อเลือกแม่แบบสาธารณะ

แม่แบบและงานพื้นฐานต่อไปนี้ถูกใช้เพื่อซิงโครไนซ์การประมาณชั่วโมงโครงการจาก Project Service Automation ไปยัง Finance:

- **ชื่อของแม่แบบในการรวมข้อมูล:** การประมาณชั่วโมงโครงการ (PSA ไปยัง Fin และ Ops)
- **ชื่อของงานในโครงการ:**

    - ความสัมพันธ์ของธุรกรรม
    - การประเมินค่าใช้จ่าย

### <a name="entity-set"></a>ชุดเอนทิตี

| Project Service Automation | Finance                                       |
|----------------------------|-----------------------------------------------|
| งานโครงการ              | เอนทิตีการรวมสำหรับการประมาณชั่วโมงของโครงการ |

### <a name="entity-flow"></a>โฟลว์เอนทิตี

การประมาณชั่วโมงโครงการได้รับการจัดการใน Project Service Automation และมีการซิงโครไนซ์กับ Finance เป็นการคาดการณ์ชั่วโมงของโครงการ

### <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่จะซิงโครไนซ์การประมาณชั่วโมงของโครงการได้ คุณต้องซิงโครไนซ์โครงการ งานโครงการ และประเภทธุรกรรมค่าใช้จ่ายโครงการ

### <a name="power-query"></a>Power Query

ในแม่แบบประมาณการชั่วโมงของโครงการ คุณต้องใช้ Microsoft Power Query สำหรับ Excel เพื่อทำงานเหล่านี้ให้เสร็จสิ้น:

- ตั้งค่ารหัสแบบจำลองการคาดการณ์เริ่มต้นที่จะใช้เมื่อการรวมสร้างการคาดการณ์รายชั่วโมงใหม่
- กรองเรกคอร์ดเฉพาะทรัพยากรในงานที่จะทำให้การรวมเข้ากับการคาดการณ์ชั่วโมงล้มเหลว
- กรองแถวหมวดหมู่ธุรกรรมที่ว่างเปล่าออก ความล้มเหลวในการทำงานนี้ให้เสร็จสมบูรณ์อาจส่งผลให้การคาดการณ์ชั่วโมงไม่ถูกต้อง

#### <a name="set-the-default-forecast-model-id"></a>ตั้งค่ารหัสแบบจำลองการคาดการณ์เริ่มต้น

หากต้องการอัปเดตรหัสแบบจำลองการคาดการณ์เริ่มต้นในแม่แบบ ให้คลิกลูกศร **แม็ป** เพื่อเปิดการแม็ป จากนั้นเลือกลิงก์ **การสืบค้นและการกรองขั้นสูง**

- หากคุณกำลังใช้แม่แบบการประมาณการชั่วโมงโครงการเริ่มต้น (PSA ไปยัง Fin และ Ops) ให้เลือก **แทรกเงื่อนไข** ในรายการ **ขั้นตอนที่ใช้** ในรายการ **ฟังก์ชัน** ให้แทนที่ **O\_การคาดการณ์** ด้วยชื่อของรหัสแบบจำลองการคาดการณ์ที่ควรใช้กับการรวม แม่แบบเริ่มต้นมีรหัสแบบจำลองการคาดการณ์จากข้อมูลสาธิต
- หากคุณกำลังสร้างแม่แบบใหม่ คุณต้องเพิ่มคอลัมน์นี้ ใน Power Query ให้เลือก **เพิ่มคอลัมน์เงื่อนไข** และป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **ModelID** ป้อนเงื่อนไขสำหรับคอลัมน์โดย ที่ถ้างานโครงการไม่ว่าง แล้ว \<enter the forecast model ID\>; อื่นว่าง

#### <a name="filter-out-resource-specific-records"></a>กรองเรกคอร์ดเฉพาะทรัพยากรออก

แม่แบบการประมาณชั่วโมงของโครงการ (PSA ไปยัง Fin และ Ops) มีตัวกรองเริ่มต้นที่ลบเรกคอร์ดเฉพาะทรัพยากรใดๆ หากคุณสร้างแม่แบบของคุณเอง คุณต้องเพิ่มตัวกรองนี้ เลือกลิงก์ **การสืบค้นและการกรองขั้นสูง** เพื่อกรองคอลัมน์ **msdyn\_islinetask** เพื่อรวมเรกคอร์ด **เท็จ** เท่านั้น

#### <a name="filter-out-empty-transaction-category-rows"></a>กรองแถวหมวดหมู่ธุรกรรมที่ว่างเปล่าออก

คุณต้องเพิ่มตัวกรองเพื่อลบแถวที่มีหมวดหมู่ธุรกรรมว่าง จำเป็นต้องมีงานนี้ ไม่ว่าคุณจะใช้แม่แบบเริ่มต้นหรือสร้างแม่แบบของคุณเอง ตัวกรองนี้จะลบแถวสรุปใดๆ ออกจาก Project Service Automation ที่อาจทำให้การคาดการณ์ชั่วโมงใน Finance ไม่ถูกต้อง เลือกลิงก์ **การสืบค้นและการกรองขั้นสูง** เพื่อกรองเรกคอร์ด null ในคอลัมน์ **msdyn\_ประเภทธุรกรรม\_มูลค่า**

### <a name="template-mapping-in-data-integration"></a>การแม็ปแม่แบบในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานแม่แบบในการรวมข้อมูล การแม็ปแสดงข้อมูลฟิลด์ที่จะซิงโครไนซ์จาก Project Service Automation ไปยัง Finance

[![การแม็ปงานแม่แบบในการรวมข้อมูล](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>การประมาณการค่าใช้จ่ายโครงการ

### <a name="template-and-tasks"></a>แม่แบบและงาน

แม่แบบและงานพื้นฐานต่อไปนี้ถูกใช้เพื่อซิงโครไนซ์การประมาณค่าใช้จ่ายโครงการจาก Project Service Automation ไปยัง Finance:

- **ชื่อของแม่แบบในการรวมข้อมูล:** การประมาณค่าใช้จ่ายโครงการ (PSA ไปยัง Fin และ Ops)
- **ชื่อของงานในโครงการ:**

    - ความสัมพันธ์ของธุรกรรม 
    - การประเมินค่าใช้จ่าย

### <a name="entity-set"></a>ชุดเอนทิตี

| Project Service Automation | Finance                                                  |
|----------------------------|----------------------------------------------------------|
| การเชื่อมต่อธุรกรรม    | เอนทิตีการรวมสำหรับความสัมพันธ์ธุรกรรมโครงการ |
| บรรทัดการประมาณการ             | เอนทิตีการรวมสำหรับการประมาณค่าใช้จ่ายของโครงการ         |

### <a name="entity-flow"></a>โฟลว์เอนทิตี

การประมาณค่าใช้จ่ายโครงการได้รับการจัดการใน Project Service Automation และมีการซิงโครไนซ์กับ Finance เป็นการคาดการณ์ค่าใช้จ่ายของโครงการ

### <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่จะซิงโครไนซ์การประมาณค่าใช้จ่ายของโครงการได้ คุณต้องซิงโครไนซ์โครงการ งานโครงการ และประเภทธุรกรรมค่าใช้จ่ายโครงการ

### <a name="power-query"></a>Power Query

ในแม่แบบประมาณการค่าใช้จ่ายของโครงการ คุณต้องใช้ Power Query เพื่อทำงานต่อไปนี้ให้เสร็จสิ้น:

- กรองเพื่อรวมเฉพาะเรกคอร์ดรายการประมาณการค่าใช้จ่าย
- ตั้งค่ารหัสแบบจำลองการคาดการณ์เริ่มต้นที่จะใช้เมื่อการรวมสร้างการคาดการณ์รายชั่วโมงใหม่
- เปลี่ยนประเภทการเรียกเก็บเงิน
- เปลี่ยนประเภทธุรกรรม

#### <a name="filter-to-include-only-expense-estimate-lines"></a>กรองเพื่อรวมเฉพาะรายการประมาณการค่าใช้จ่าย

แม่แบบประมาณการค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin และ Ops) มีตัวกรองเริ่มต้นที่รวมเฉพาะรายการค่าใช้จ่ายในการรวม หากคุณสร้างแม่แบบของคุณเอง คุณต้องเพิ่มตัวกรองนี้ เลือกงาน **ความสัมพันธ์ของธุรกรรม** แล้วคลิกลูกศร **แม็ป** เพื่อเปิดการแม็ป เลือกลิงก์ **การสืบค้นและการกรองขั้นสูง** กรองคอลัมน์ **msdyn\_transactiontype1** เพื่อให้รวมเฉพาะ **msdyn\_estimateline**

#### <a name="set-the-default-forecast-model-id"></a>ตั้งค่ารหัสแบบจำลองการคาดการณ์เริ่มต้น

หากต้องการอัปเดตรหัสแบบจำลองการคาดการณ์เริ่มต้นในแม่แบบ ให้เลือกงาน **ประมาณการค่าใช้จ่าย** จากนั้นคลิกลูกศร **แม็ป** เพื่อเปิดการแม็ป เลือกลิงก์ **การสืบค้นและการกรองขั้นสูง**

- หากคุณกำลังใช้แม่แบบการประมาณการค่าใช้จ่ายโครงการเริ่มต้น (PSA ไปยัง Fin และ Ops) ใน Power Query ให้เลือก **แทรกเงื่อนไข** จากส่วน **ขั้นตอนที่ใช้** ในรายการ **ฟังก์ชัน** ให้แทนที่ **O\_การคาดการณ์** ด้วยชื่อของรหัสแบบจำลองการคาดการณ์ที่ควรใช้กับการรวม แม่แบบเริ่มต้นมีรหัสแบบจำลองการคาดการณ์จากข้อมูลสาธิต
- หากคุณกำลังสร้างแม่แบบใหม่ คุณต้องเพิ่มคอลัมน์นี้ ใน Power Query ให้เลือก **เพิ่มคอลัมน์เงื่อนไข** และป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **ModelID** ป้อนเงื่อนไขสำหรับคอลัมน์โดย ที่ถ้ารหัสรายการประมาณการไม่ว่าง แล้ว \<enter the forecast model ID\>; อื่นว่าง

#### <a name="transform-the-billing-types"></a>เปลี่ยนประเภทการเรียกเก็บเงิน

แม่แบบการประมาณการค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin และ Ops) ประกอบด้วยคอลัมน์เงื่อนไขที่ใช้ในการแปลงประเภทการเรียกเก็บเงินที่ได้รับจาก Project Service Automation ระหว่างการรวม หากคุณสร้างแม่แบบของคุณเอง คุณต้องเพิ่มคอลัมน์เงื่อนไขนี้ เลือกลิงก์ **การสืบค้นและการกรองขั้นสูง** จากนั้นเลือก **เพิ่มคอลัมน์เงื่อนไข** ป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **BillingType** จากนั้นใส่เงื่อนไขต่อไปนี้:

ถ้า **msdyn\_billingtype** = 192350000 ดังนั้น **ไม่คิดค่าบริการ**  
หรือถ้า **msdyn\_billingtype** = 192350001 ดังนั้น **คิดค่าบริการ**  
หรือถ้า **msdyn\_billingtype** = 192350002 ดังนั้น **ส่วนเสริม**  
หรือ **ไม่พร้อมใช้งาน**

#### <a name="transform-the-transaction-types"></a>เปลี่ยนประเภทธุรกรรม

แม่แบบการประมาณการค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin และ Ops) ประกอบด้วยคอลัมน์เงื่อนไขที่ใช้ในการแปลงประเภทธุรกรรมที่ได้รับจาก Project Service Automation ระหว่างการรวม หากคุณสร้างแม่แบบของคุณเอง คุณต้องเพิ่มคอลัมน์เงื่อนไขนี้ เลือกลิงก์ **การสืบค้นและการกรองขั้นสูง** จากนั้นเลือก **เพิ่มคอลัมน์เงื่อนไข** ป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **TransactionType** จากนั้นใส่เงื่อนไขต่อไปนี้:

ถ้า **msdyn\_transactiontypecode** = 192350000 แล้ว **ค่าใช้จ่าย**  
หรือถ้า **msdyn\_transactiontypecode** = 192350005 ดังนั้น **ยอดขาย**  
หรือ **null**

### <a name="template-mapping-in-data-integration"></a>การแม็ปแม่แบบในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานแม่แบบในการรวมข้อมูล การแม็ปแสดงข้อมูลฟิลด์ที่จะซิงโครไนซ์จาก Project Service Automation ไปยัง Finance

[![การแม็ปแม่แบบของธุรกรรมประมาณการค่าใช้จ่าย](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![การแม็ปแม่แบบของประมาณการค่าใช้จ่าย](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)