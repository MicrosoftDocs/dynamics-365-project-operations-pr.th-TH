---
title: มอบหมายทรัพยากรให้กับงาน
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการมอบหมายทรัพยากรให้กับงาน
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: a348130ee5760196b2f008ea811e7a81758dd73e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993259"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="b07b6-103">มอบหมายทรัพยากรให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="b07b6-103">Assign a resource to a task</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b07b6-104">มีวิธีสามวิธีในการมอบหมายทรัพยากรให้กับงานใน Microsoft Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b07b6-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="b07b6-105">จองทรัพยากรในฐานะสมาชิกทีม และจากนั้นมอบหมายทรัพยากรให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="b07b6-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="b07b6-106">คุณสามารถเพิ่มทรัพยากรลงในทีมโครงการได้ และจากนั้น มอบหมายทรัพยากรให้กับงานในกำหนดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="b07b6-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="b07b6-107">บนแท็บ **สมาชิกทีม** เพิ่มสมาชิกทีมใหม่โดยการเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="b07b6-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="b07b6-108">เปิดแผง **การสร้างสมาชิกทีมด่วน** ที่ซึ่งคุณสามารถเลือกชื่อทรัพยากรที่จองได้และตั้งค่าบทบาทได้</span><span class="sxs-lookup"><span data-stu-id="b07b6-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="b07b6-109">เลือกหนึ่งในวิธีการจัดสรรต่อไปนี้สำหรับการจองทรัพยากร:</span><span class="sxs-lookup"><span data-stu-id="b07b6-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="b07b6-110">**กำลังการผลิตแบบเต็ม** จองกำลังการผลิตแบบเต็มของทรัพยากร สำหรับวันที่เริ่มต้นและวันที่สิ้นสุดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="b07b6-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="b07b6-111">**กำลังการผลิตเป็นเปอร์เซ็นต์** จองทรัพยากรสำหรับเปอร์เซ็นต์ของกำลังการผลิตของทรัพยากร สำหรับวันที่เริ่มต้นและวันที่สิ้นสุดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="b07b6-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="b07b6-112">**ตามชั่วโมง การกระจายแบบเท่า ๆ กัน** จองทรัพยากรสำหรับจำนวนของชั่วโมงที่ระบุ กระจายชั่วโมงเท่า ๆ กัน ในแต่ละวัน ในช่วงวันเริ่มต้นถึงวันสิ้นสุดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="b07b6-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="b07b6-113">**ตามชั่วโมง เน้นช่วงต้น** จองทรัพยากรสำหรับจำนวนของชั่วโมงที่ระบุ ซึ่งกระจายเท่าๆ กันต่อวัน ผ่านวันที่เริ่มต้นและวันที่สิ้นสุดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="b07b6-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="b07b6-114">**ไม่มี** เพิ่มทรัพยากรลงในกลุ่มคน แต่จะไม่สร้างการจองใดๆ ที่ซึมซับกำลังการผลิตของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="b07b6-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="b07b6-115">บนกริด **กำหนดการ** สำหรับงาน เลือกไอคอน **ทรัพยากร** ในเซลล์ทรัพยากร และจากนั้นข้างล่าง **สมาชิกทีม** เลือกสมาชิกทีมที่คุณเพิ่งเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b07b6-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="b07b6-116">บนแท็บ **สมาชิกทีม** และแท็บ **การกระทบยอด** ทรัพยากรจะแสดงชั่วโมงที่ถูกจอง และถูกมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="b07b6-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="b07b6-117">ชั่วโมงเหล่านั้นควรจะเหมือนกัน แต่ไม่จำเป็น เพราะการจอง และการมอบหมายไม่ถูกเชื่อมโยงอย่างแน่นหนา</span><span class="sxs-lookup"><span data-stu-id="b07b6-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="b07b6-118">แท็บ **การกระทบยอด** ให้คุณทราบรายละเอียด เมื่อรายการเหล่านั้นแตกต่างกัน เช่น เมื่อคุณมอบหมายชั่วโมงให้ทรัพยากรมากกว่าที่คุณได้จองไว้</span><span class="sxs-lookup"><span data-stu-id="b07b6-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="b07b6-119">ถ้าต้องการ คุณสามารถงแก้ไขข้อมูลด้วยการขยายจองทรัพยากร หรือเปลี่ยนการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="b07b6-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="b07b6-120">สร้างสมาชิกทีมทั่วไปผ่านการมอบหมายงาน</span><span class="sxs-lookup"><span data-stu-id="b07b6-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="b07b6-121">เมื่อคุณสร้างสมาชิกทีมทั่วไปผ่านการมอบหมายงาน คุณสร้างตัวยึดหรือทรัพยากรทั่วไปที่อธิบายคุณลักษณะของทรัพยากรที่ระบุชื่อ ที่คุณต้องการทำงานในตอนท้ายสุด</span><span class="sxs-lookup"><span data-stu-id="b07b6-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="b07b6-122">จากนั้น คุณสร้างความต้องการ (หรือส่งการร้องขอโดยใช้ความต้องการ) ที่ใช้ในการค้นหา และจองทรัพยากรที่ระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="b07b6-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="b07b6-123">บนกริด **กำหนดการ** สำหรับงาน เลือกไอคอน **ทรัพยากร** ในเซลล์ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="b07b6-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="b07b6-124">พิมพ์ชื่อที่จะใช้เป็นชื่อของทรัพยากรตัวยึด</span><span class="sxs-lookup"><span data-stu-id="b07b6-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="b07b6-125">ตัวอย่างเช่น Program Manager</span><span class="sxs-lookup"><span data-stu-id="b07b6-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="b07b6-126">เลือก **สร้าง** และในฟิลด์ **การสร้างสมาชิกทีมโครงการแบบด่วน** กำหนดบทบาทสำหรับทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="b07b6-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="b07b6-127">คุณสามารถมอบหมายงานให้กับทรัพยากรตัวยึดนี้ต่อไปได้ โดยการเลือกทรัพยากรใน **ตัวเลือกทรัพยากร** สำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="b07b6-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="b07b6-128">มีการแสดงไว้ภายใต้ **สมาชิกทีม**</span><span class="sxs-lookup"><span data-stu-id="b07b6-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="b07b6-129">เมื่อคุณเสร็จสิ้นการมอบหมายทรัพยากรทั่วไป เลือกทรัพยากรทั่วไปบนแท็บ **ทีม** และเลือก **สร้างความต้องการ** เพื่อสร้างความต้องการทรัพยากรสำหรับทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="b07b6-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="b07b6-130">เลือก **จอง** สำหรับทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="b07b6-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="b07b6-131">จากนั้น คุณสามารถใช้ตารางกำหนดการเพื่อค้นหา และจองทรัพยากรจริงได้</span><span class="sxs-lookup"><span data-stu-id="b07b6-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="b07b6-132">นอกจากนี้ คุณยังสามารถส่งความต้องการสำหรับการบรรลุเป้าหมายโดยผู้จัดการทรัพยากรได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="b07b6-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="b07b6-133">เมื่อทรัพยากรทั่วไปถูกทำให้สมบูรณ์ด้วยทรัพยากรที่มีชื่อ ทรัพยากรทั่วไปจะถูกเอาออกจากกลุ่มคน และการมอบหมายงานสำหรับทรัพยากรทั่วไปถูกมอบหมายให้กับทรัพยากรที่มีชื่อ ที่ตอบสนองความต้องการทางทรัพยากรของทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="b07b6-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="b07b6-134">การมอบหมายทรัพยากรที่ระบุชื่อจากรายการของทรัพยากรที่จองได้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b07b6-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="b07b6-135">คุณสามารถใช้กล่องค้นหาใน **ตัวเลือกทรัพยากร** เพื่อค้นหาทรัพยากรที่สามารถจองได้ทั้งหมดใน และมอบหมายให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="b07b6-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="b07b6-136">ทรัพยากรที่ถูกมอบหมายด้วยวิธีนี้ จะถูกเพิ่มเข้าไปในทีมโดยไม่ต้องทำการจองใด ๆ</span><span class="sxs-lookup"><span data-stu-id="b07b6-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="b07b6-137">คล้ายกับการเพิ่มสมาชิกในทีมและเลือก "ไม่มี" เป็นวิธีการจัดสรร</span><span class="sxs-lookup"><span data-stu-id="b07b6-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="b07b6-138">ทรัพยากรนั้นถูกแสดงเป็นทรัพยากรที่มีการมอบหมายเท่านั้นและการจองที่ขาดในแท็บ **ทีม** และแท็บ **การกระทบยอด**</span><span class="sxs-lookup"><span data-stu-id="b07b6-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="b07b6-139">จองรายการเหล่านี้ ถ้าคุณต้องการใช้ความพร้อมใช้งานของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="b07b6-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="b07b6-140">บนกริด **กำหนดการ** สำหรับงาน เลือกไอคอน **ทรัพยากร** ในเซลล์ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="b07b6-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="b07b6-141">เริ่มต้นการพิมพ์ชื่อ</span><span class="sxs-lookup"><span data-stu-id="b07b6-141">Start typing a name.</span></span> <span data-ttu-id="b07b6-142">ผลลัพธ์การค้นหาสำหรับชื่อที่แสดงใน **ตัวเลือกทรัพยากร** ภายใต้ **ทรัพยากรอื่น ๆ**</span><span class="sxs-lookup"><span data-stu-id="b07b6-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="b07b6-143">เลือกทรัพยากรที่คุณต้องการมอบหมายให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="b07b6-143">Select the resource that you want to assign to the task.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]