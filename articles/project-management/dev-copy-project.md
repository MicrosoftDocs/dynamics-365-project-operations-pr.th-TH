---
title: พัฒนาเทมเพลตโครงการด้วย คัดลอกโครงการ
description: บทความนี้ให้ข้อมูลเกี่ยวกับวิธีการสร้างและใช้เทมเพลตโครงการโดยใช้การดำเนินการที่กำหนดเองคัดลอกโครงการ
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923855"
---
# <a name="develop-project-templates-with-copy-project"></a>พัฒนาเทมเพลตโครงการด้วย คัดลอกโครงการ

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

Dynamics 365 Project Operations สนับสนุนความสามารถในการคัดลอกโครงการและเปลี่ยนการมอบหมายกลับไปยังทรัพยากรทั่วไปที่แสดงถึงบทบาท ลูกค้าสามารถใช้ฟังก์ชันนี้เพื่อสร้างเทมเพลตโครงการพื้นฐาน

เมื่อคุณเลือก **คัดลอกโครงการ** สถานะของโครงการเป้าหมายจะได้รับการอัปเดต ใช้ **คำอธิบายรายการของสถานะ** เพื่อพิจารณาว่าการคัดลอกเสร็จสมบูรณ์เมื่อใด กำลังเลือก **คัดลอกโครงการ** นอกจากนี้ยังอัปเดตวันที่เริ่มต้นของโครงการเป็นวันที่เริ่มต้นปัจจุบันหากไม่พบวันที่เป้าหมายในเอนทิตีโครงการเป้าหมาย

## <a name="copy-project-custom-action"></a>การดำเนินการ คัดลอกโครงการ แบบกำหนดเอง

### <a name="name"></a>Name 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>พารามิเตอร์อินพุต

มีพารามิเตอร์ข้อมูลป้อนเข้าสามรายการ:

- **ReplaceNamedResources** หรือ **ClearTeamsAndAssignments** – ตั้งค่าตัวเลือกเดียวเท่านั้น อย่าตั้งค่าทั้งคู่

    - **\{"ReplaceNamedResources":true\}** – ลักษณะการทำงานเริ่มต้นสำหรับ Project Operations ทรัพยากรที่ระบุชื่อถุกแทนที่ด้วยทรัพยากรทั่วไป
    - **\{"ClearTeamsAndAssignments":true\}** – ลักษณะการทำงานเริ่มต้นสำหรับ Project for the Web การมอบหมายและสมาชิกทีมทั้งหมดจะถูกลบออก

- **SourceProject** – การอ้างอิงเอนทิตีของโครงการต้นทางที่จะคัดลอก พารามิเตอร์ไม่สามารถเป็นไม่มีค่า
- **Target** – การอ้างอิงเอนทิตีของโครงการเป้าหมายในการคัดลอก พารามิเตอร์ไม่สามารถเป็นไม่มีค่า

ตารางต่อไปนี้แสดงสรุปข้อมูลของพารามิเตอร์สามรายการ

| พารามิเตอร์                | ขนิด             | มูลค่า                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **จริง** หรือ **เท็จ** |
| ClearTeamsAndAssignments | Boolean          | **จริง** หรือ **เท็จ** |
| SourceProject            | การอ้างอิงเอนทิตี | โครงการต้นทาง    |
| Target                   | การอ้างอิงเอนทิตี | โครงการเป้าหมาย    |

สำหรับค่าเริ่มต้นเกี่ยวกับการดำเนินการเพิ่มเติม ดูที่ [ใช้การดำเนินการ Web API](/powerapps/developer/common-data-service/webapi/use-web-api-actions)

### <a name="validations"></a>การตรวจสอบความถูกต้อง

การตรวจสอบความถูกต้องที่ดำเนินการมีดังต่อไปนี้

1. ไม่มีค่า จะตรวจสอบและเรียกค้นโครงการต้นทางและเป้าหมายเพื่อยืนยันการมีอยู่ของทั้งสองโครงการในองค์กร
2. ระบบจะตรวจสอบว่าโครงการเป้าหมายนั้นถูกต้องสำหรับการคัดลอกโดยตรวจสอบเงื่อนไขต่อไปนี้:

    - ไม่มีกิจกรรมก่อนหน้าในโครงการ (รวมถึงการเลือกแท็บ **งาน**) และโครงการจะถูกสร้างขึ้นใหม่
    - ไม่มีสำเนาก่อนหน้า ไม่มีการร้องขอการนำเข้าในโครงการนี้ และโครงการไม่มีสถานะ **ล้มเหลว**

3. การดำเนินการนี้ไม่ได้ถูกเรียกโดยใช้ HTTP

## <a name="specify-fields-to-copy"></a>ระบุช่องที่จะคัดลอก

เมื่อมีการเรียกการดำเนินการ **คัดลอกโครงการ** จะดูมุมมองโครงการ **คัดลอกคอลัมน์โครงการ** เพื่อกำหนดฟิลด์ที่จะคัดลอกเมื่อโครงการถูกคัดลอก

### <a name="example"></a>ตัวอย่างเช่น

ตัวอย่างต่อไปนี้แสดงวิธีการเรียกการดำเนินการที่กำหนดเอง **CopyProjectV3** ด้วยชุดพารามิเตอร์ **removeNamedResources**

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
