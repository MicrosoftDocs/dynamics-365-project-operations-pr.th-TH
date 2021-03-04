---
title: พัฒนาแม่แบบโครงการด้วย คัดลอกโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีสร้างแม่แบบโครงการโดยใช้การดำเนินการ คัดลอกโครงการ แบบกำหนดเอง
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 87696b41db20e9ec70270c850d9acfe05df8cd84
ms.sourcegitcommit: d5004acb6f1c257b30063c873896fdea92191e3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/22/2021
ms.locfileid: "5045032"
---
# <a name="develop-project-templates-with-copy-project"></a>พัฒนาแม่แบบโครงการด้วย คัดลอกโครงการ

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations สนับสนุนความสามารถในการคัดลอกโครงการและเปลี่ยนการมอบหมายกลับไปยังทรัพยากรทั่วไปที่แสดงถึงบทบาท ลูกค้าสามารถใช้ฟังก์ชันนี้เพื่อสร้างแม่แบบโครงการพื้นฐาน

เมื่อคุณเลือก **คัดลอกโครงการ** สถานะของโครงการเป้าหมายจะได้รับการอัปเดต ใช้ **คำอธิบายรายการของสถานะ** เพื่อพิจารณาว่าการคัดลอกเสร็จสมบูรณ์เมื่อใด กำลังเลือก **คัดลอกโครงการ** นอกจากนี้ยังอัปเดตวันที่เริ่มต้นของโครงการเป็นวันที่เริ่มต้นปัจจุบันหากไม่พบวันที่เป้าหมายในเอนทิตีโครงการเป้าหมาย

## <a name="copy-project-custom-action"></a>การดำเนินการ คัดลอกโครงการ แบบกำหนดเอง 

### <a name="name"></a>ชื่อ 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>พารามิเตอร์อินพุต
มีพารามิเตอร์ข้อมูลป้อนเข้าสามรายการ:

| พารามิเตอร์          | พิมพ์ข้อความ   | มูลค่า                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** หรือ **{"clearTeamsAndAssignments":true}** |
| SourceProject      | การอ้างอิงเอนทิตี | โครงการต้นทาง |
| เป้าหมาย             | การอ้างอิงเอนทิตี | โครงการเป้าหมาย |


- **{"clearTeamsAndAssignments":true}**: เป็นลักษณะการทำงานเริ่มต้นสำหรับโครงการสำหรับเว็บและจะลบการมอบหมายงานและสมาชิกในทีมทั้งหมด
- **{"removeNamedResources":true}** ลักษณะการทำงานเริ่มต้นสำหรับ Project Operations และจะเปลี่ยนการมอบหมายกลับเป็นทรัพยากรทั่วไป

สำหรับค่าเริ่มต้นบนการดำเนินการ ดูที่ [ใช้การดำเนินการ API เว็บ](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>ระบุช่องที่จะคัดลอก 
เมื่อมีการเรียกการดำเนินการ **คัดลอกโครงการ** จะดูมุมมองโครงการ **คัดลอกคอลัมน์โครงการ** เพื่อกำหนดฟิลด์ที่จะคัดลอกเมื่อโครงการถูกคัดลอก


### <a name="example"></a>ตัว อย่าง เช่น
ตัวอย่างต่อไปนี้แสดงวิธีการเรียกการดำเนินการที่กำหนดเอง **CopyProject** ด้วยชุดพารามิเตอร์ **removeNamedResources**
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

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
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]