---
title: แม่แบบโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้แม่แบบโครงการสำหรับการตั้งค่าโครงการด่วน
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f0161bf9-af4c-4a21-b767-ac20a8e30688
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5a3112c2eef9525946314bdb587c44904557fa52
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756399"
---
# <a name="project-templates"></a><span data-ttu-id="71d6c-103">แม่แบบโครงการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="71d6c-104">แม่แบบโครงการคือกรอบงานที่กำหนดไว้ล่วงหน้า ซึ่งจะช่วยให้คุณสามารถเริ่มโครงการได้อย่างรวดเร็วและง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="71d6c-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="71d6c-105">คุณสามารถใช้แม่แบบที่กำหนดไว้ล่วงหน้า เพื่อสร้างโครงการใหม่ได้ด้วยคลิกเดียว</span><span class="sxs-lookup"><span data-stu-id="71d6c-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="71d6c-106">สำหรับโครงการ คุณต้องกำหนดข้อกำหนดเบื้องต้นสำหรับแม่แบบโครงการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="71d6c-107">คุณต้องกำหนดปฏิทินโครงการสำหรับแต่ละแม่แบบโครงการ และบทบาท และรายการราคาต้องถูกกำหนดไว้ล่วงหน้าในองค์กร เพื่อให้ส่วนประกอบของแม่แบบมีข้อมูลที่เป็นประโยชน์</span><span class="sxs-lookup"><span data-stu-id="71d6c-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="71d6c-108">แม่แบบโครงการประกอบด้วยส่วนประกอบสามอย่าง ได้แก่ หมายกำหนดการให้บริการ การประมาณการโครงการ และสมาชิกในทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="71d6c-109">กำหนดการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-109">Schedule</span></span>

<span data-ttu-id="71d6c-110">หมายกำหนดการให้บริการในแม่แบบโครงการมีชุดขององค์ประกอบเดียวกันเป็นหมายกำหนดการให้บริการในโครงการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="71d6c-111">คุณสามารถสร้างลำดับชั้นงาน เชื่อมโยงบทบาทกับงาน กำหนดแอททริบิวต์หมายกำหนดการให้บริการ และตั้งค่าภาวะการขึ้นต่อกัน</span><span class="sxs-lookup"><span data-stu-id="71d6c-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="71d6c-112">หมายกำหนดการให้บริการในแม่แบบโครงการยังสนับสนุนโหมดงานสำหรับแต่ละงาน</span><span class="sxs-lookup"><span data-stu-id="71d6c-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="71d6c-113">ดังนั้น จึงสนับสนุนกลไกการจัดการหมายกำหนดการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="71d6c-114">คุณต้องเชื่อมโยงปฏิทินโครงการกับโครงการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="71d6c-115">เมื่อคุณสร้างหมายกำหนดการให้บริการงาน ไม่มีความแตกต่างใดๆ ระหว่างแม่แบบโครงการและโครงการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="71d6c-116">การประมาณการโครงการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-116">Project estimates</span></span>

<span data-ttu-id="71d6c-117">การประมาณการโครงการในแม่แบบโครงการทำงานในลักษณะเดียวกับการประมาณการโครงการในโครงการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="71d6c-118">อย่างไรก็ตาม ต้นทุนและราคาตลาดจะถูกดึงมาจากรายการต้นทุนเริ่มต้นและราคาตลาดที่กำหนดไว้ในพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="71d6c-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="71d6c-119">การสร้างโครงการจากแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="71d6c-119">Creating a project from a template</span></span>
 
<span data-ttu-id="71d6c-120">มีหลายวิธีในการสร้างโครงการจากแม่แบบโครงการ:</span><span class="sxs-lookup"><span data-stu-id="71d6c-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="71d6c-121">เมื่อคุณสร้างโครงการจากใบเสนอราคา คุณสามารถเลือกแม่แบบโครงการในกล่องโตอบ **การสร้างด่วน: โครงการ**</span><span class="sxs-lookup"><span data-stu-id="71d6c-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![สร้างด่วน: กล่องโต้ตอบโครงการ](media/project-11.png)

- <span data-ttu-id="71d6c-123">เมื่อคุณสร้างโครงการโดยการเลือก **โครงการใหม่** หน้า **โครงการ** จะปรากฏขึ้นก่อนที่จะบันทึกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="71d6c-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="71d6c-124">ในฟิลด์ **เลือกแม่แบบ** ให้เลือกหนึ่งในแม่แบบโครงการที่กำหนดไว้ล่วงหน้าในองค์กร</span><span class="sxs-lookup"><span data-stu-id="71d6c-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="71d6c-125">ใช้ **สร้างโครงการจากแม่แบบ** ในหน้า **เอนทิตีแม่แบบ**</span><span class="sxs-lookup"><span data-stu-id="71d6c-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="71d6c-126">การคัดลอกองค์ประกอบของแม่แบบไปยังโครงการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-126">Copying components of template to project</span></span>

<span data-ttu-id="71d6c-127">เมื่อคุณคัดลอกส่วนประกอบของแม่แบบโครงการไปยังโครงการการ การแทนที่อาจเกิดขึ้นได้ขึ้นอยู่กับการตั้งค่าในโครงการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="71d6c-128">การคัดลอกหมายกำหนดการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-128">Copying the schedule</span></span>

<span data-ttu-id="71d6c-129">เมื่อคุณคัดลอกหมายกำหนดการให้บริการจากแม่แบบโครงการ ถ้าโครงการมีปฏิทินโครงการที่แตกต่างจากแม่แบบ ชั่วโมงทำงานจากปฏิทินโครงการจะถูกนำมาใช้กับกำหนดการของงาน</span><span class="sxs-lookup"><span data-stu-id="71d6c-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="71d6c-130">ในวิธีนี้ หมายกำหนดการให้บริการจะมีการปรับเปลี่ยนให้ตรงกับปฏิทินโครงการสำรอง</span><span class="sxs-lookup"><span data-stu-id="71d6c-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="71d6c-131">ในทำนองเดียวกัน งานแรกในหมายกำหนดการให้บริการใช้วันที่เริ่มต้นของโครงการ และหมายกำหนดการให้บริการของลำดับขึ้นที่เหลือจะถูกอัพเดตตามระยะเวลาและการอ้างอิงที่ระบุไว้ในโครงสร้างการแบ่งงานของแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="71d6c-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="71d6c-132">การคัดลอกการประมาณการโครงการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-132">Copying project estimates</span></span> 

<span data-ttu-id="71d6c-133">เมื่อคุณคัดลอกข้ามรายการการประเมินโครงการ จะมีการปรับปรุงราคาตลาด</span><span class="sxs-lookup"><span data-stu-id="71d6c-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="71d6c-134">สำหรับราคาตลาดต้นทุน การปรับปรุงเหล่านี้จะขึ้นอยู่กับหน่วยที่เป็นเจ้าของของโครงการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="71d6c-135">สำหรับราคาตลาดขายจะขึ้นอยู่กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="71d6c-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="71d6c-136">สำหรับโครงการที่เกี่ยวข้องกับเอนทิตีการขาย ต้นทุนต่อหน่วยและราคาตลาดจะถูกกำหนดโดยยึดตามราคาตลาดเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="71d6c-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="71d6c-137">การคัดลอกกลุ่มคนของโครงการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-137">Copying a project team</span></span>

<span data-ttu-id="71d6c-138">เมื่อมีการคัดลอกกลุ่มคนของโครงการจากแม่แบบโครงการไปยังโครงการ ทรัพยากรทั่วไปจะถูกคัดลอก พร้อมด้วยทักษะและประสิทธิภาพที่กำหนดไว้ในแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="71d6c-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="71d6c-139">การมอบหมายทรัพยากรทรัพยากรทั่วไปยังจะได้รับการดูแลรักษาตามที่อยู่ในแม่แบบโครงการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="71d6c-140">ทรัพยากรที่มีชื่อไม่ได้รับการสนับสนุนในแม่แบบโครงการ</span><span class="sxs-lookup"><span data-stu-id="71d6c-140">Named resources aren't supported in project templates.</span></span>
