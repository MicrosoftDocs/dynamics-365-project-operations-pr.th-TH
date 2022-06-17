---
title: การเปลี่ยนแปลงคุณลักษณะจาก Project Service Automation เป็น Project Operations
description: บทความนี้ให้ภาพรวมของการเปลี่ยนแปลงคุณลักษณะจาก Project Service Automation เป็น Dynamics 365 Project Operations
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 8a6030faf777051ea1003679589af4bdf97322ab
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925373"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>การเปลี่ยนแปลงคุณลักษณะจาก Project Service Automation เป็น Project Operations

การปรับรุ่นจาก Dynamics 365 Project Service Automation เป็น Dynamics 365 Project Operations Lite จะมีการนำเสนอในสามระยะ บทความนี้ให้ข้อมูลเกี่ยวกับการเปลี่ยนแปลงที่สำคัญที่คุณจะได้เห็นเมื่อการปรับรุ่นเสร็จสมบูรณ์

| การจัดส่งการปรับรุ่น | ระยะที่ 1 <br>(มกราคม 2022) | ระยะที่ 2 <br>(เวฟเมษายน 2022) | ระยะที่ 3  |
|------------------|------------------------|---------------------------|---------------------------|
| ไม่มีการขึ้นต่อกันของโครงสร้างการแบ่งงาน (WBS) สำหรับโครงการ | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS มีการรวมอยู่ในขีดจำกัดที่รองรับในปัจจุบันของ Project Operations | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS อยู่นอกขีดจำกัดที่รองรับในปัจจุบันของ Project Operations รวมถึงการรองรับสำหรับ Project Desktop Client | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>การจัดการโครงการ

การเปลี่ยนแปลงที่สำคัญที่สุดในด้านประสบการณ์ของผู้ใช้จะอยู่ในส่วนการวางแผนโครงการ Project Operations นำประสบการณ์ใหม่ที่ทันสมัยมาใช้ในการจัดการโครงสร้างการแบ่งงาน (WBS) โดยใช้ประโยชน์จากความสามารถในการจัดกำหนดการโดย [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5)

## <a name="differences-in-the-scheduling-experience"></a>ความแตกต่างในประสบการณ์การจัดกำหนดการ

ตารางต่อไปนี้สรุปความแตกต่างของการจัดกำหนดการระหว่าง Project Service Automation และ Project Operations

|  การจัดตารางเวลา     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| เทมเพลตโครงการ - ความสามารถในการกำหนดและใช้เทมเพลตโครงการเมื่อมีการสร้างโครงการ  |  &nbsp;    | :heavy_check_mark: |
| การรวมโครงสร้างการแบ่งงานโครงการ (WBS) กับไคลเอ็นต์เดสก์ท็อป   |    &nbsp;  | :heavy_check_mark: |
| ข้อจำกัด - เริ่มไม่เร็วกว่า สิ้นสุดไม่ช้ากว่า  | :heavy_check_mark: |   &nbsp;  |
| หลักเป้าหมาย - งานที่มีระยะเวลาเป็นศูนย์   | :heavy_check_mark:  |  &nbsp;  |
| งานที่ขับเคลื่อนด้วยทรัพยากรจะคำนึงถึงความพร้อมให้บริการของทรัพยากรที่ได้รับมอบหมาย   | :heavy_check_mark: |  &nbsp;    |
| การแก้ไขตามช่วงเวลา - แก้ไขแผนและทำงานแบบวันต่อวัน   |   &nbsp;  | :heavy_check_mark: |
| การจัดกำหนดการอัตโนมัติ/ด้วยตนเอง - ใช้โปรแกรมการจัดกำหนดการโครงการเพื่อจัดกำหนดการงานโดยอัตโนมัติหรือด้วยตนเอง |  &nbsp; | :heavy_check_mark:  |
| แก้ไขโครงการขนาดใหญ่ได้โดยตรงในส่วนติดต่อผู้ใช้: ไม่มีการจำกัดขนาดของแผนงานที่สามารถแก้ไขได้  | จำกัด 500 งาน  | :heavy_check_mark:       |
| เปอร์เซ็นต์ที่เสร็จสมบูรณ์ - ทำเครื่องหมายความคืบหน้าของงาน   | :heavy_check_mark:  |  &nbsp;  |
| [โหมดกำหนดการโครงการ](../project-management/scheduling-modes.md) - กำหนดโครงการเป็นหน่วยคงที่ ความพยายามคงที่ หรือระยะเวลาคงที่ | :heavy_check_mark: | &nbsp; |
| ไทม์ไลน์ - สร้างและปรับแต่งมุมมองไทม์ไลน์เพื่อแสดงภาพรายละเอียดกำหนดการและสื่อสารกับผู้เกี่ยวข้อง | :heavy_check_mark:  | &nbsp; |
| งานที่ขับเคลื่อนด้วยความพยายาม - การรองรับโปรแกรมการจัดกำหนดการสำหรับการจัดกำหนดการงานตามที่ขับเคลื่อนด้วยความพยายาม  | :heavy_check_mark:  | &nbsp; |
| กล่องโต้ตอบ **ข้อมูลงาน** - บันทึกรายละเอียดงานโดยใช้กล่องโต้ตอบ | :heavy_check_mark:  |  &nbsp;  |
| ลากแล้วปล่อย - งานแบบเลือกหลายรายการและแก้ไขตำแหน่งบน WBS | :heavy_check_mark: | &nbsp;  |
| มุมมองถาวรที่ยืดหยุ่น - กำหนดมุมมองที่ละเอียดยิ่งขึ้นของแอตทริบิวต์งาน   | :heavy_check_mark:  | &nbsp; |
| เรียงลำดับและกรอง WBS  | :heavy_check_mark:  | &nbsp; |
| มุมมองกระดานสำหรับการส่งมอบโครงการที่ไม่ใช่แผนภูมิน้ำตก  | :heavy_check_mark:   | &nbsp; |
| มุมมองไทม์ไลน์ - แผนภูมิแกนต์แบบโต้ตอบที่ใช้เพื่อแสดงภาพและแก้ไข WBS   | :heavy_check_mark:  | &nbsp; |
| แป้นพิมพ์ลัด - ใช้แป้นพิมพ์ลัดสำหรับการทำงานทั่วไป เช่น เยื้องหรือแทรก  | :heavy_check_mark:  |  &nbsp; |
| เลิกทำหลายระดับ - ดำเนินการวิเคราะห์แบบ what-if เพื่อทำความเข้าใจผลกระทบของการเปลี่ยนแปลงอย่างเต็มที่โดยการย้อนกลับและนำชุดปฏิบัติการทั้งหมดมาใช้ใหม่ | :heavy_check_mark: | &nbsp; |
| ตัด/คัดลอก/วาง - ทำงานร่วมกันในการพัฒนากำหนดการโดยการคัดลอกและวางรายละเอียดกำหนดการระหว่างแอปพลิเคชัน  | :heavy_check_mark: | &nbsp; |
| รายการตรวจสอบงาน - เพิ่มรายการตรวจสอบได้ถึง 20 รายการในงาน   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>การวางแผนโครงการ

หน้า **โครงการ** ใน Project Operations มีความแตกต่างอย่างมีนัยสำคัญเมื่อเทียบกับหน้า **โครงการ** ใน Project Service Automation

การดำเนินการต่อไปนี้ถูกลบออกจากหน้า **โครงการ** ที่เป็นส่วนหนึ่งของการปรับรุ่นระยะ 1:

  - **เปิดใน MS Project**
  - **สร้างแม่แบบ**
  - **ยกเลิกการเชื่อมโยง MS Project**

หน้า **โครงการ** ใน Project Operations มีแท็บใหม่ดังต่อไปนี้

- **ประมาณการวัสดุ**
- **การตั้งค่าการเรียกเก็บเงินของงาน**

แท็บ **สถานะ** มีการเอาออกและฟิลด์ **สถานะ** อยู่บนแท็บ **สรุป** พร้อมโหมดการจัดกำหนดการของโครงการ

   ![การปรับปรุงหน้าโครงการ](media/projectform.png)

แท็บ **กำหนดการ** ถูกเปลี่ยนชื่อเป็นแท็บ **งาน** และนำเสนอประสบการณ์การวางแผนโครงการใหม่ด้วย Project for the Web

   ![แท็บงานโครงการใหม่](media/tasktab.png)

## <a name="scheduling-modes"></a>โหมดการจัดกำหนดการ

Project Operations ได้แนะนำคุณลักษณะใหม่ คือ [โหมดการจัดกำหนดการ](../project-management/scheduling-modes.md) โครงการ Project Service Automation ที่มีอยู่ทั้งหมดจะมีค่าเริ่มต้นเป็น **ระยะเวลาคงที่** ใน Project Operations อย่างไรก็ตาม คุณสามารถจัดการค่าเริ่มต้นสำหรับโครงการใหม่ได้โดยไปที่ **การตั้งค่า** > **พารามิเตอร์** > **พารามิเตอร์** > **โหมดกำหนดการ**

   ![การตั้งค่าพารามิเตอร์โครงการสำหรับโหมดกำหนดการ](media/projectparameter.png)

## <a name="project-planning-limits"></a>ขีดจำกัดการวางแผนโครงการ

Project Operations อาศัย Project for the Web สำหรับการดำเนินการจัดกำหนดการโครงการทั้งหมด Project for the Web จัดการโครงสร้างการแบ่งงานโดยใช้ขีดจำกัดในตารางต่อไปนี้

| **ฟิลด์**                                          | **ขีดจำกัด**             |
|----------------------------------------------------|-----------------------|
| งานรวมสูงสุดสำหรับโครงการ                  | 500                   |
| ระยะเวลารวมสูงสุดสำหรับโครงการ               | 3650 วัน (10 ปี)  |
| ทรัพยากรรวมสูงสุดสำหรับโครงการ              | 300                   |
| การเชื่อมโยงรวมสูงสุด (งานที่ตามมาเท่านั้น) สำหรับโครงการ | 600                   |
| ฟิลด์ที่กำหนดเองรวมสูงสุดสำหรับโครงการ          | 10                    |
| ระดับของลำดับชั้นสูงสุด                            | 10 ระดับ             |
| การเชื่อมโยงสูงสุด (งานที่ตามมา + งานที่เกิดขึ้นก่อนหน้า)            | 20                    |
| ระยะเวลาสูงสุดของงานปลายสุด                      | 1250 วัน             |
| ระยะเวลาสูงสุดของงานสรุป                 | 3650 วัน (10 ปี)  |
| ทรัพยากรสูงสุดที่กำหนดให้กับงาน               | ทรัพยากร 20 รายการ          |
| ช่วงวันที่ที่รองรับสำหรับงาน                    | 1/1/2000 - 12/31/2149 |
| รายการตรวจสอบ                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>การขยายและการพัฒนาการวางแผนโครงการ

หลังจากที่คุณปรับรุ่นเป็น Project Operations คุณต้องใช้ API การจัดกำหนดการโครงการเพื่อดำเนินการสร้าง ปรับปรุง และลบในเอนทิตีต่อไปนี้:

|   ชื่อเอนทิตี           |   ชื่อตรรกะของเอนทิตี       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| งานโครงการ            | msdyn_projecttask           |
| การขึ้นต่อกันของงานโครงการ | msdyn_projecttaskdependency |
| การมอบหมายทรัพยากร     | msdyn_resourceassignment    |
| บักเก็ตโครงการ          | msdyn_projectbucket         |
| สมาชิกของทีมโครงการ     | msdyn_projectteam           |

หากคุณมีการปรับแต่งที่เกี่ยวข้องกับเอนทิตีเหล่านี้ โปรดดู [ใช้ API กำหนดการโครงการเพื่อดำเนินการกับเอนทิตีการจัดกำหนดการ](../project-management/schedule-api-preview.md) เพื่อเป็นแนวทางในการนำไปปฏิบัติ

## <a name="data-model-changes"></a>การเปลี่ยนแปลงรูปแบบข้อมูล

ในส่วนของการปรับรุ่นระยะที่ 1 จะมีการเปลี่ยนแปลงกับรูปแบบข้อมูล การเปลี่ยนแปลงเหล่านี้เป็นการเปลี่ยนแปลงฟิลด์ในเอนทิตีที่มีอยู่เป็นหลัก ในระยะที่ 1 เอนทิตี **msydn_project** และ **msdyn_projectteam** เป็นการปรับโครงสร้างการปรับแต่ง 

> [!IMPORTANT]
> ส่วนนี้จะปรับปรุงด้วยเอนทิตีเพิ่มเติมเมื่อขั้นตอนการปรับรุ่นในอนาคตเสร็จสมบูรณ์

ฟิลด์ต่อไปนี้ถูกแทนที่ด้วยฟิลด์ใหม่

|   เอนทิตี          |   ชื่อตรรกะของเดิม   |   ชื่อตรรกะใหม่    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

โดยมีการเพิ่มฟิลด์ต่อไปนี้

|   เอนทิตี          |   ชื่อตรรกะ                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | แสดงผลรวมของค่าธรรมเนียมต่อยอดขายจริงในโครงการ สำหรับการใช้ใน Project Service Automation เท่านั้น |
| msdyn_project     | msdyn_actualmaterialcost                     | แสดงการรวมของต้นทุนวัสดุตามจริงในโครงการ สำหรับการใช้ใน Project Service Automation เท่านั้น |
| msdyn_project     | msdyn_actualmaterialsales                    | แสดงผลรวมของวัสดุต่อยอดขายจริงในโครงการ สำหรับการใช้ใน Project Service Automation เท่านั้น |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | รายละเอียดการให้บริการตามสัญญาที่เชื่อมโยงกับโครงการนี้ |
| msdyn_project     | msdyn_copyprojectcorrelationid               | นี่คือฟิลด์ระบบภายในที่ใช้สำหรับ **คัดลอกโครงการ** ที่เกี่ยวข้องกับตัวระบุสหสัมพันธ์ สำหรับการใช้ใน Project Service Automation เท่านั้น |
| msdyn_project     | msdyn_copyprojectsessionid                   | นี่คือฟิลด์ระบบภายในที่ใช้สำหรับ **คัดลอกโครงการ** ที่เกี่ยวข้องกับตัวระบุเซสชัน สำหรับการใช้ใน Project Service Automation เท่านั้น |
| msdyn_project     | msdyn_globalrevisiontoken                    | ซิงค์โทเค็นการแก้ไขส่วนกลางของ xRM ล่าสุดจากบริการจัดกำหนดการโครงการ |
| msdyn_project     | msdyn_msprojectdocument                      | เอกสาร Microsoft Project ที่เป็นของโครงการ |
| msdyn_project     | msdyn_plannedmaterialcost                    | การรวมของต้นทุนวัสดุตามแผนในโครงการ สำหรับการใช้ใน Project Service Automation เท่านั้น |
| msdyn_project     | msdyn_plannedmaterialsales                   | การรวมของการขายวัสดุตามแผนในโครงการ สำหรับการใช้ใน Project Service Automation เท่านั้น |
| msdyn_project     | msdyn_program                                | โปรแกรมที่โครงการนี้เกี่ยวข้อง |
| msdyn_project     | msdyn_quotelineproject                       | ใบเสนอราคาที่เชื่อมโยงกับโครงการนี้ |
| msdyn_project     | msdyn_replaylogheader                        | ส่วนหัวสำหรับบันทึกการเล่นซ้ำ |
| msdyn_project     | msdyn_schedulemode                           | โหมดการจัดกำหนดการเริ่มต้นที่ใช้สำหรับงานทั้งหมดในโครงการ  |
| msdyn_project     | msdyn_taskearlieststart                      | วันที่เริ่มต้นแรกสุดของงานใดๆ ในโครงการ  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | สมาชิกทีมในโครงการที่คัดลอกมาจากสมาชิกทีมในโครงการ |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | ระบุว่าต้องการสร้างความต้องการทรัพยากรสำหรับสมาชิกทีมทั่วไปที่สร้างขึ้นใหม่หรือไม่  |
| msdyn_projectteam | msdyn_deletestatus                           | สถานะการลบสมาชิกทีมเพื่อติดตามว่ามีคำขอลบที่ส่งไปยังบริการจัดกำหนดการโครงการหรือไม่ และมีการส่งการตอบกลับสำเร็จและอยู่ในช่วงเวลาที่ต้องการหรือไม่ |
| msdyn_projectteam | msdyn_effortcompleted                        | ติดตามความพยายามที่ดำเนินการของสมาชิกทีมสำหรับการมอบหมายงานของพวกเขา |
| msdyn_projectteam | msdyn_effortremaining                        | ติดตามความพยายามที่ยังไม่เสร็จสมบูรณ์ของสมาชิกทีมสำหรับการมอบหมายงานของพวกเขา |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | ช่วงเวลารอตั้งแต่เมื่อสมาชิกทีมส่งคำขอลบไปยังบริการจัดกำหนดการโครงการจนกว่าสมาชิกทีมจะถูกลบจริงบน Microsoft Dataverse|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | การประทับเวลาที่จะบันทึกเมื่อมีการส่งคำขอลบของสมาชิกทีมไปยังบริการจัดกำหนดการโครงการ |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | แสดงสมาชิกทีมในโครงการที่คัดลอกมาจากสมาชิกทีมในโครงการ  |

## <a name="project-templates"></a>เทมเพลตโครงการ

Project Operations ไม่ได้ให้การสนับสนุนเทมเพลตโครงการ อย่างไรก็ตาม คุณสามารถทำซ้ำฟังก์ชันการทำงานหลักได้มากด้วยการใช้ [API การคัดลอกโครงการ](../project-management/dev-copy-project.md)

## <a name="desktop-add-in-support"></a>การรองรับโปรแกรมเสริมบนเดสก์ท็อป

การรองรับโปรแกรมเสริมบนเดสก์ท็อปของ Microsoft Project จะไม่สามารถใช้ได้ใน 2 ระยะแรกของการปรับรุ่น ในระยะที่ 3 ลูกค้าที่มีโครงการใหญ่กว่าขีดจำกัดที่สนับสนุนในปัจจุบันของ Project for the Web จะสามารถใช้โปรแกรมเสริมบนเดสก์ท็อปได้

## <a name="editing-resource-assignment-contours"></a>การแก้ไขโครงร่างการมอบหมายทรัพยากร

ความสามารถในการแก้ไขโครงร่างการมอบหมายทรัพยากรจะพร้อมใช้งานเมื่อระยะที่ 2 ของการปรับรุ่นพร้อมใช้งาน

## <a name="billing-and-pricing"></a>การเรียกเก็บเงินและการกำหนดราคา

มีการเพิ่มคุณลักษณะใหม่ต่อไปนี้ใน Project Operations คุณลักษณะเหล่านี้เป็นส่วนเสริมและไม่ส่งผลกระทบต่อรูปแบบข้อมูล Project Service Automation

- [การบันทึกการใช้วัสดุในโครงการและงานโครงการ](../material/material-usage-log.md)
- [การจัดการสัญญารับเหมารายย่อย](../pro/subcontracting/managing-subcontracts-overview.md)
- [สัญญาตามเงินทดรองและค่าธรรมเนียมล่วงหน้า](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [สถานะไม่เกินของสัญญาและการตรวจสอบความถูกต้อง](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [การเรียกเก็บเงินตามงาน](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>ส่วนประกอบที่ไม่สนับสนุน

ตารางต่อไปนี้บันทึกฟิลด์ที่ไม่สนับสนุนทั้งหมดซึ่งถูกย้ายไปยังโซลูชันส่วนประกอบที่ไม่สนับสนุนหลังการปรับรุ่น สำหรับข้อมูลเพิ่มเติมและลิงก์ไปยังโซลูชัน โปรดดู [ส่วนประกอบที่ไม่สนับสนุนของ Dynamics 365 Project Service Automation 3x ไปยัง Project Operations 4x](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution)

### <a name="invoicedetail"></a>invoicedetail

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| ฟิลด์                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

