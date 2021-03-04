---
title: ฉันจะมอบหมายทรัพยากรที่สามารถจองได้ให้กับงานในแอปเว็บได้อย่างไร
description: ภาพรวมของวิธีการที่คุณสามารถมอบหมายทรัพยากรที่สามารถจองได้
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 27a93c41243f300cadb632c697672180e5a3817b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146596"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="478e4-103">ฉันจะมอบหมายทรัพยากรที่สามารถจองได้ให้กับงานในแอพเว็บ (แอพ Project Service v2.x) ได้อย่างไร?</span><span class="sxs-lookup"><span data-stu-id="478e4-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="478e4-104">มีวิธีสองวิธีในการมอบหมายทรัพยากรให้กับงานใน Project Service</span><span class="sxs-lookup"><span data-stu-id="478e4-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="478e4-105">คุณสามารถจองทรัพยากรในฐานะสมาชิกในทีมได้ และมอบหมายให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="478e4-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="478e4-106">หรือ คุณสามารถสร้างสมาชิกในทีมทั่วไปผ่านการมอบหมายบทบาทในงาน สร้างทีม และจากนั้น เติมเต็มความต้องการสำรองด้วยทรัพยากรที่มีชื่อ</span><span class="sxs-lookup"><span data-stu-id="478e4-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="478e4-107">หมายเหตุว่า ถ้าคุณต้องการมอบหมายทรัพยากรที่สามารถจองได้ให้กับงาน สมาชิกทีมทรัพยากรที่สามารถจองได้ต้องมีการจองที่พร้อมใช้งานที่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="478e4-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="478e4-108">สถานะของการจองต้องเป็น ยอมรับชนิดการจองแบบตายตัว และสถานะยอมรับแล้ว</span><span class="sxs-lookup"><span data-stu-id="478e4-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="478e4-109">ถ้าไม่มีการจองสำหรับทรัพยากรเพียงพอสำหรับ Project Service จะลบการมอบหมาย และแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="478e4-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="478e4-110">*ไม่สามารถมอบหมายทรัพยากรให้กับงานได้ - ทรัพยากรต่อไปนี้ไม่มีชั่วโมงที่เพียงพอที่จองให้กับโครงการ*</span><span class="sxs-lookup"><span data-stu-id="478e4-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="478e4-111">จองทรัพยากรในฐานะสมาชิกในทีม และจากนั้น มอบหมายทรัพยากรให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="478e4-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="478e4-112">ด้วยวิธีนี้ คุณจะเพิ่มทรัพยากรลงในทีมโครงการ และจากนั้น มอบหมายงานให้กับทรัพยากรในการจัดกำหนดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="478e4-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="478e4-113">นี่คือวิธีที่คุณดำเนินการสิ่งนี้:</span><span class="sxs-lookup"><span data-stu-id="478e4-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="478e4-114">บนกริดสมาชิกทีม เพิ่มสมาชิกทีมใหม่โดยการเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="478e4-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="478e4-115">บนหน้าจอสร้างทีมสมาชิกด่วน เลือกชื่อทรัพยากรที่สามารถจองได้และตั้งค่าบทบาท</span><span class="sxs-lookup"><span data-stu-id="478e4-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="478e4-116">เลือกวันที่ **เริ่มต้น** และ **สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="478e4-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="478e4-117">![ภาพหน้าจอของการเพิ่มสมาชิกในทีม](media/FAQ-Resources-to-Tasks2-1.png "ภาพหน้าจอของการเพิ่มสมาชิกในทีม")</span><span class="sxs-lookup"><span data-stu-id="478e4-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="478e4-118">เลือกหนึ่งในวิธีการปันส่วนต่อไปนี้สำหรับการจองทรัพยากร:</span><span class="sxs-lookup"><span data-stu-id="478e4-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="478e4-119">**กำลังการผลิตแบบเต็ม** จองกำลังการผลิตแบบเต็มของทรัพยากร สำหรับวันที่เริ่มต้นและวันที่สิ้นสุดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="478e4-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="478e4-120">**กำลังการผลิตเป็นเปอร์เซ็นต์** จองทรัพยากรสำหรับเปอร์เซ็นต์ของกำลังการผลิตของทรัพยากร สำหรับวันที่เริ่มต้นและวันที่สิ้นสุดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="478e4-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="478e4-121">**ตามชั่วโมง การกระจายแบบเท่าๆ กัน** จองทรัพยากรสำหรับจำนวนของชั่วโมงที่ระบุ ซึ่งกระจายเท่าๆ กันต่อวัน ผ่านวันที่เริ่มต้นและวันที่สิ้นสุดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="478e4-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="478e4-122">**ตามชั่วโมง เน้นช่วงต้น** จองทรัพยากรสำหรับจำนวนของชั่วโมงที่ระบุ ซึ่งกระจายเท่าๆ กันต่อวัน ผ่านวันที่เริ่มต้นและวันที่สิ้นสุดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="478e4-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="478e4-123">อย่าเลือก **ไม่มี** เนื่องจากจะเพิ่มทรัพยากรลงในกลุ่มคน แต่จะไม่สร้างการจองใดๆ ที่ซึมซับกำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="478e4-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="478e4-124">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="478e4-124">Select **Save**.</span></span>

    <span data-ttu-id="478e4-125">หมายเหตุว่า ชั่วโมงของการจองที่ต้องเพียงพอที่จะครอบคลุมชั่วโมงความพยายาม และช่วงวันที่ของงานที่คุณมอบหมายทรัพยากรนี้ให้</span><span class="sxs-lookup"><span data-stu-id="478e4-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="478e4-126">ถ้ารายการเหล่านั้นไม่ได้อยู่ในแนวเดียวกัน คุณไม่สามารถมอบหมายทรัพยากรไปยังงานได้</span><span class="sxs-lookup"><span data-stu-id="478e4-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="478e4-127">ในโครงสร้างการแบ่งงาน (WBS) สำหรับงาน คลิกบนรายการแบบหล่นลงของเซลล์ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="478e4-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="478e4-128">จากนั้น:</span><span class="sxs-lookup"><span data-stu-id="478e4-128">Then:</span></span> 

    1. <span data-ttu-id="478e4-129">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="478e4-129">Select **Add**.</span></span>
    2. <span data-ttu-id="478e4-130">เลือกรายการแบบหล่นลงภายใต้ **ทรัพยากร** และเลือกสมาชิกของกลุ่มคนที่คุณได้เพิ่มไว้ข้างต้น</span><span class="sxs-lookup"><span data-stu-id="478e4-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="478e4-131">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="478e4-131">Select **OK**.</span></span> <span data-ttu-id="478e4-132">ขณะนี้ สมาชิกของทีมได้รับการมอบหมายให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="478e4-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="478e4-133">![ภาพหน้าจอของการเพิ่มทรัพยากรด้วย WBS](media/FAQ-Resources-to-Tasks2-2.png "ภาพหน้าจอของการเพิ่มทรัพยากรด้วย WBS")</span><span class="sxs-lookup"><span data-stu-id="478e4-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="478e4-134">บนกริดสมาชิกกลุ่มคน คุณจะเห็นการรวมของชั่วโมงที่ได้รับมอบหมายของทรัพยากรภายใต้ชั่วโมงที่ได้รับมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="478e4-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="478e4-135">ซึ่งจะน้อยกว่าหรือเท่ากับชั่วโมงที่จองสำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="478e4-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="478e4-136">![ภาพหน้าจอของชั่วโมงที่กำหนดสำหรับทรัพยากร](media/FAQ-Resources-to-Tasks2-3.png "ภาพหน้าจอของชั่วโมงที่กำหนดสำหรับทรัพยากร")</span><span class="sxs-lookup"><span data-stu-id="478e4-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="478e4-137">ถ้างานคุณกำลังพยายามที่จะมอบหมายให้กับทรัพยากร เริ่มต้นหลังจากวันที่สิ้นสุดของการจองทรัพยากร ทรัพยากรจะไม่ปรากฏในรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="478e4-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="478e4-138">หมายเหตุว่า คุณสามารถมอบหมายทรัพยากรให้กับจำนวนชั่วโมงมากกว่าชั่วโมงที่จองของพวกเขา ทรัพยากรมีกำลังการผลิตที่ไม่ได้มอบหมายที่เหลือบางรายการ</span><span class="sxs-lookup"><span data-stu-id="478e4-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="478e4-139">ในกรณีนี้ ทรัพยากรจะถูกมอบหมายเพียงบางส่วนให้กับการจองของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="478e4-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="478e4-140">คุณสามารถดูชั่วโมงงานที่ไม่ถูกมอบหมายงานที่เหลือเหล่านี้ ด้วยการเพิ่มคอลัมจำนวนชั่วโมงที่ยังไม่ได้จัดเตรียมพนักงานไปยังโครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="478e4-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="478e4-141">ถ้ามีการกำหนดทรัพยากรให้กับชั่วโมงที่จองของพวกเขา (ชั่วโมงที่จองของพวกเขาเท่ากับชั่วโมงที่ได้รับมอบหมายของพวกเขา) คุณจะเห็นข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามที่จะมอบหมายงานเพิ่มเติมให้พวกเขา:</span><span class="sxs-lookup"><span data-stu-id="478e4-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="478e4-142">*ไม่สามารถมอบหมายทรัพยากรให้กับงานได้ - ทรัพยากรต่อไปนี้ไม่มีชั่วโมงที่เพียงพอที่จองให้กับโครงการ*</span><span class="sxs-lookup"><span data-stu-id="478e4-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="478e4-143">นอกจากนี้ สมาชิกกลุ่มคนของผู้จัดการโครงการเริ่มต้นที่จะถูกเพิ่มให้กับกลุ่มคนเมื่อคุณสร้างโครงการ โครงการจะถูกเพิ่มโดยไม่มีการจองใดๆ และไม่สามารถถูกมอบหมายให้แก่งานใดๆ ได้</span><span class="sxs-lookup"><span data-stu-id="478e4-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="478e4-144">รายการเหล่านั้นจะไม่แสดงขึ้นในรายการแบบหล่นลงทรัพยากรสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="478e4-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="478e4-145">ถ้าคุณต้องการมอบหมายทรัพยากรนี้ คุณจำเป็นต้องลบออกจากกลุ่มคน แล้วเพิ่มใหม่อีกครั้งโดยใช้วิธีการปันส่วนอื่นที่ไม่ใช่ ไม่มี</span><span class="sxs-lookup"><span data-stu-id="478e4-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="478e4-146">เหตุผลที่พวกเขาถูกเพิ่มไปยังทีมเมื่อมีการสร้างโครงการคือ เพื่อให้โครงการมีผู้อนุมัติโครงการอย่างน้อยหนึ่งคนโดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="478e4-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="478e4-147">สร้างสมาชิกกลุ่มคนทั่วไปผ่านการมอบหมายบทบาทในงาน</span><span class="sxs-lookup"><span data-stu-id="478e4-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="478e4-148">วิธีการนี้ช่วยให้แน่ใจว่า ทรัพยากรมีการจองเพียงพอสำหรับสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="478e4-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="478e4-149">อันดับแรก คุณสร้างตัวยึดหรือทรัพยากรทั่วไปที่อธิบายลักษณะของทรัพยากรที่มีชื่อที่คุณต้องการทำงานในตอนท้าย โดยการสร้างกลุ่มคน หลังจากที่มอบหมายบทบาทให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="478e4-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="478e4-150">นี่คือวิธีที่คุณดำเนินการสิ่งนี้:</span><span class="sxs-lookup"><span data-stu-id="478e4-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="478e4-151">ในโครงสร้างการแบ่งงาน เลือกงาน</span><span class="sxs-lookup"><span data-stu-id="478e4-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="478e4-152">เลือกไอคอนในรายการแบบหล่นลง **บทบาทที่ได้รับมอบหมาย** ในเซลล์ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="478e4-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="478e4-153">เลือกรายการแบบหล่นลง **บทบาท** และเลือกบทบาทสำหรับทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="478e4-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="478e4-154">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="478e4-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="478e4-155">![ภาพหน้าจอของการใช้ WBS เพื่อเพิ่มทรัพยากร](media/FAQ-Resources-to-Tasks2-4.png "ภาพหน้าจอของการใช้ WBS เพื่อเพิ่มทรัพยากร")</span><span class="sxs-lookup"><span data-stu-id="478e4-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="478e4-156">หลังจากที่คุณเสร็จสิ้นการมอบหมายบทบาทให้กับงานใน WBS เลือก **สร้างกลุ่มคนในโครงการ**</span><span class="sxs-lookup"><span data-stu-id="478e4-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="478e4-157">Project Service สร้างจำนวนต่ำสุดของสมาชิกในกลุ่มคนทั่วไปตามบทบาท หน่วยองค์กรการจัดหาทรัพยากร และปฏิทินโครงการ โดยการรวมการมอบหมายงาน</span><span class="sxs-lookup"><span data-stu-id="478e4-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="478e4-158">![ภาพหน้าจอของการสร้างทีมโครงการ](media/FAQ-Resources-to-Tasks2-5.png "ภาพหน้าจอของการสร้างทีมโครงการ")</span><span class="sxs-lookup"><span data-stu-id="478e4-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="478e4-159">บนกริดสมาชิกของกลุ่มคน คุณจะเห็นทรัพยากรของชนิดทรัพยากรทั่วไปที่มีชื่อบทบาทและตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="478e4-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="478e4-160">ถ้าทรัพยากรสองรายการจำเป็นสำหรับบทบาทเพื่อทำให้งานเสร็จสมบูรณ์ คุณลักษณะสร้างกลุ่มคนจะสร้างสมาชิกในกลุ่มคนสองราย และใช้ชื่อตำแหน่งเพื่อใช้แยกออกจากกัน</span><span class="sxs-lookup"><span data-stu-id="478e4-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="478e4-161">![ภาพหน้าจอของการเพิ่มทรัพยากรทั่วไปสองรายการ](media/FAQ-Resources-to-Tasks2-6.png "ภาพหน้าจอของการเพิ่มทรัพยากรทั่วไปสองรายการ")</span><span class="sxs-lookup"><span data-stu-id="478e4-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="478e4-162">คุณสามารถเปิดความต้องการทรัพยากรสำรองสำหรับสมาชิกกลุ่มคนทั่วไปได้ โดยการเลือกการเชื่อมโยงภายใต้ความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="478e4-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="478e4-163">![ภาพหน้าจอของการเปิดความต้องการทรัพยากรสำรอง](media/FAQ-Resources-to-Tasks2-7.png "ภาพหน้าจอของการเปิดความต้องการทรัพยากรสำรอง")</span><span class="sxs-lookup"><span data-stu-id="478e4-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="478e4-164">เลือก **จอง** สำหรับทรัพยากรทั่วไป และจากนั้น คุณสามารถใช้บอร์ดกำหนดการเพื่อค้นหาและจองทรัพยากรจริงได้</span><span class="sxs-lookup"><span data-stu-id="478e4-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="478e4-165">นอกจากนี้ คุณยังสามารถส่งความต้องการสำหรับการบรรลุเป้าหมายโดยผู้จัดการทรัพยากร โดยการเลือก **ส่งการร้องขอ** ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="478e4-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="478e4-166">เมื่อทรัพยากรทั่วไปถูกทำให้สมบูรณ์ด้วยทรัพยากรที่มีชื่อ ทรัพยากรทั่วไปจะถูกเอาออกจากกลุ่มคน และการมอบหมายงานสำหรับทรัพยากรทั่วไปถูกมอบหมายให้กับทรัพยากรที่มีชื่อ ที่ตอบสนองความต้องการทางทรัพยากรของทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="478e4-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

