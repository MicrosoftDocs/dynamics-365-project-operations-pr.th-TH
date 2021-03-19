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
ms.openlocfilehash: 27847575e2d6ec9af77d24f756b13d3aeb0efea7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286946"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="fed5b-103">พัฒนาแม่แบบโครงการด้วย คัดลอกโครงการ</span><span class="sxs-lookup"><span data-stu-id="fed5b-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="fed5b-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="fed5b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="fed5b-105">Dynamics 365 Project Operations สนับสนุนความสามารถในการคัดลอกโครงการและเปลี่ยนการมอบหมายกลับไปยังทรัพยากรทั่วไปที่แสดงถึงบทบาท</span><span class="sxs-lookup"><span data-stu-id="fed5b-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="fed5b-106">ลูกค้าสามารถใช้ฟังก์ชันนี้เพื่อสร้างแม่แบบโครงการพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="fed5b-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="fed5b-107">เมื่อคุณเลือก **คัดลอกโครงการ** สถานะของโครงการเป้าหมายจะได้รับการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="fed5b-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="fed5b-108">ใช้ **คำอธิบายรายการของสถานะ** เพื่อพิจารณาว่าการคัดลอกเสร็จสมบูรณ์เมื่อใด</span><span class="sxs-lookup"><span data-stu-id="fed5b-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="fed5b-109">กำลังเลือก **คัดลอกโครงการ** นอกจากนี้ยังอัปเดตวันที่เริ่มต้นของโครงการเป็นวันที่เริ่มต้นปัจจุบันหากไม่พบวันที่เป้าหมายในเอนทิตีโครงการเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="fed5b-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="fed5b-110">การดำเนินการ คัดลอกโครงการ แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="fed5b-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="fed5b-111">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="fed5b-111">Name</span></span> 

<span data-ttu-id="fed5b-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="fed5b-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="fed5b-113">พารามิเตอร์อินพุต</span><span class="sxs-lookup"><span data-stu-id="fed5b-113">Input parameters</span></span>
<span data-ttu-id="fed5b-114">มีพารามิเตอร์ข้อมูลป้อนเข้าสามรายการ:</span><span class="sxs-lookup"><span data-stu-id="fed5b-114">There are three input parameters:</span></span>

| <span data-ttu-id="fed5b-115">พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="fed5b-115">Parameter</span></span>          | <span data-ttu-id="fed5b-116">พิมพ์ข้อความ</span><span class="sxs-lookup"><span data-stu-id="fed5b-116">Type</span></span>   | <span data-ttu-id="fed5b-117">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="fed5b-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="fed5b-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="fed5b-118">ProjectCopyOption</span></span>  | <span data-ttu-id="fed5b-119">String</span><span class="sxs-lookup"><span data-stu-id="fed5b-119">String</span></span> | <span data-ttu-id="fed5b-120">**{"removeNamedResources":true}** หรือ **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="fed5b-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="fed5b-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="fed5b-121">SourceProject</span></span>      | <span data-ttu-id="fed5b-122">การอ้างอิงเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="fed5b-122">Entity Reference</span></span> | <span data-ttu-id="fed5b-123">โครงการต้นทาง</span><span class="sxs-lookup"><span data-stu-id="fed5b-123">Source Project</span></span> |
| <span data-ttu-id="fed5b-124">เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="fed5b-124">Target</span></span>             | <span data-ttu-id="fed5b-125">การอ้างอิงเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="fed5b-125">Entity Reference</span></span> | <span data-ttu-id="fed5b-126">โครงการเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="fed5b-126">Target Project</span></span> |


- <span data-ttu-id="fed5b-127">**{"clearTeamsAndAssignments":true}**: เป็นลักษณะการทำงานเริ่มต้นสำหรับโครงการสำหรับเว็บและจะลบการมอบหมายงานและสมาชิกในทีมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fed5b-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="fed5b-128">**{"removeNamedResources":true}** ลักษณะการทำงานเริ่มต้นสำหรับ Project Operations และจะเปลี่ยนการมอบหมายกลับเป็นทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="fed5b-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="fed5b-129">สำหรับค่าเริ่มต้นบนการดำเนินการ ดูที่ [ใช้การดำเนินการ API เว็บ](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="fed5b-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="fed5b-130">ระบุช่องที่จะคัดลอก</span><span class="sxs-lookup"><span data-stu-id="fed5b-130">Specify fields to copy</span></span> 
<span data-ttu-id="fed5b-131">เมื่อมีการเรียกการดำเนินการ **คัดลอกโครงการ** จะดูมุมมองโครงการ **คัดลอกคอลัมน์โครงการ** เพื่อกำหนดฟิลด์ที่จะคัดลอกเมื่อโครงการถูกคัดลอก</span><span class="sxs-lookup"><span data-stu-id="fed5b-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="fed5b-132">ตัว อย่าง เช่น</span><span class="sxs-lookup"><span data-stu-id="fed5b-132">Example</span></span>
<span data-ttu-id="fed5b-133">ตัวอย่างต่อไปนี้แสดงวิธีการเรียกการดำเนินการที่กำหนดเอง **CopyProject** ด้วยชุดพารามิเตอร์ **removeNamedResources**</span><span class="sxs-lookup"><span data-stu-id="fed5b-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
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