---
title: จองทรัพยากรที่มีชื่อว่าสามารถจองได้ให้ทีมโครงการและมอบหมายงาน
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการจองทรัพยากรที่มีชื่อให้กับทีมโครงการและการมอบหมายงาน
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: e0f3957936e699fb2a9f570b9789924c55e12cc2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009369"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="e8b52-103">จองทรัพยากรที่มีชื่อว่าสามารถจองได้ให้ทีมโครงการและมอบหมายงาน</span><span class="sxs-lookup"><span data-stu-id="e8b52-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e8b52-104">คุณสามารถเพิ่มทรัพยากรที่มีชื่อให้กับทีมโครงการของคุณโดยการจองโดยตรงไปยังทีม</span><span class="sxs-lookup"><span data-stu-id="e8b52-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="e8b52-105">เมื่อต้องการดำเนินการนี้ ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e8b52-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="e8b52-106">ใน Project Service Automation ไปที่ **โครงการ** และเลือกเปิดโครงการที่คุณกำลังทำการจอง</span><span class="sxs-lookup"><span data-stu-id="e8b52-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="e8b52-107">บนหน้า **โครงการ** บนแท็บ **ทีม** ให้คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="e8b52-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![การเพิ่มสมาชิกในทีมจากแท็บทีม](media/RM-how-to-1.png)

3. <span data-ttu-id="e8b52-109">ในกล่องโต้ตอบ **สร้างสมาชิกทีมโครงการด่วน** ให้เลือกทรัพยากรที่จองได้</span><span class="sxs-lookup"><span data-stu-id="e8b52-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="e8b52-110">ฟิลด์ **บทบาท** จะเติมข้อมูลด้วยบทบาทเริ่มต้นของทรัพยากรถ้ามีการกำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="e8b52-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="e8b52-111">หากจำเป็น คุณสามารถเปลี่ยนแปลงบทบาทดังกล่าวได้</span><span class="sxs-lookup"><span data-stu-id="e8b52-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="e8b52-112">เลือกวันที่เริ่มต้นและวันที่สิ้นสุดที่จะต้องใช้ทรัพยากรและเลือกวิธีการจัดสรรของกำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="e8b52-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="e8b52-113">ถ้าคุณต้องการให้สมาชิกในทีมเป็นผู้อนุมัติโครงการ ให้เลือก **ใช่** ในฟิลด์ **ผู้อนุมัติโครงการ**</span><span class="sxs-lookup"><span data-stu-id="e8b52-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="e8b52-114">นี่จะหมายความว่าสมาชิกในทีมสามารถอนุมัติรายการเวลาและค่าใช้จ่ายที่ส่งมาสำหรับโครงการนี้</span><span class="sxs-lookup"><span data-stu-id="e8b52-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="e8b52-115">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="e8b52-115">Click **Save**.</span></span>

![การเพิ่มสมาชิกในทีมในฟอร์มการสร้างด่วน](media/RM-how-to-2.png)


<span data-ttu-id="e8b52-117">ขณะนี้คุณสามารถกำหนดทรัพยากรที่จองให้กับงานในโครงการได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="e8b52-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="e8b52-118">บนหน้า **โครงการ** ให้คลิกแท็บ **กำหนดการ** เพื่อมอบหมายงานให้กับทรัพยากรใหม่</span><span class="sxs-lookup"><span data-stu-id="e8b52-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="e8b52-119">ตัวเลือกทรัพยากรที่ถูกเปิดใช้จากฟิลด์ **ทรัพยากร** ในกริดงานจะแสดงสมาชิกในทีมที่คุณสามารถเลือกได้</span><span class="sxs-lookup"><span data-stu-id="e8b52-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![การกำหนดสมาชิกในทีมให้กับงานบนแท็บกำหนดการ](media/RM-how-to-3.png)

<span data-ttu-id="e8b52-121">ในรุ่นที่3 สำหรับ Project Service Automation (PSA) การจองทรัพยากรและการกำหนดงานจะไม่เชื่อมโยงกันอย่างแน่นหนา</span><span class="sxs-lookup"><span data-stu-id="e8b52-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="e8b52-122">นั่นหมายความว่าเมื่อคุณใช้ตัวเลือกทรัพยากรในกำหนดการ คุณสามารถกำหนดงานให้กับสมาชิกในทีมด้วยชั่วโมงที่มากกว่าที่ครอบคลุมการจองของพวกเขาในโครงการ</span><span class="sxs-lookup"><span data-stu-id="e8b52-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="e8b52-123">คุณสามารถดูความแตกต่างระหว่างการจองของสมาชิกในทีมและการมอบหมายบนแท็บ **ทีม** หรือบนแท็บ **การกระทบยอดทรัพยากร** นอกจากนี้คุณยังสามารถตรวจสอบความแตกต่างระหว่างการจองและการมอบหมายงานสำหรับทรัพยากรในระดับที่มีรายละเอียดมากขึ้นให้ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="e8b52-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![แท็บการกระทบยอดทรัพยากร](media/RM-how-to-4.png)

<span data-ttu-id="e8b52-125">คุณยังสามารถใช้ตัวเลือกทรัพยากรบนแท็บ **กำหนดการ** เพื่อค้นหาและเลือกทรัพยากรที่สามารถจองได้ที่ยังไม่ได้เป็นส่วนหนึ่งของทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="e8b52-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="e8b52-126">สิ่งเหล่านี้จะแสดงในตัวเลือกทรัพยากรเป็น **ทรัพยากรอื่นๆ**</span><span class="sxs-lookup"><span data-stu-id="e8b52-126">These are shown in the resource picker as **Other Resources**.</span></span>

![การกำหนดทรัพยากรที่ไม่ใช่สมาชิกให้กับงาน](media/RM-how-to-5.png)

<span data-ttu-id="e8b52-128">เมื่อคุณทำเช่นนี้ ทรัพยากรจะถูกเพิ่มไปยังทีมโครงการและกำหนดให้กับงาน แต่จะไม่มีการสร้างการจอง</span><span class="sxs-lookup"><span data-stu-id="e8b52-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![สมาชิกทีมที่ได้รับมอบหมายงานและไม่มีการจอง](media/RM-how-to-6.png)

<span data-ttu-id="e8b52-130">คุณสามารถใช้การขยายความสามารถในการจองของแท็บ **การกระทบยอด** หรือ **ตารางกำหนดการ** เพื่อจองกำลังการผลิตของทรัพยากรให้โครงการ</span><span class="sxs-lookup"><span data-stu-id="e8b52-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![การขยายการจองสำหรับสมาชิกในทีมบนแท็บการกระทบยอดทรัพยากร](media/RM-how-to-7.png)

<span data-ttu-id="e8b52-132">หลังจากที่สมาชิกในทีมในโครงการของคุณมีการจองแล้ว คุณสามารถใช้การรักษาการจองหรือใช้ตารางกำหนดการเพื่อจัดการการจองของพวกเขาโดยตรง</span><span class="sxs-lookup"><span data-stu-id="e8b52-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]