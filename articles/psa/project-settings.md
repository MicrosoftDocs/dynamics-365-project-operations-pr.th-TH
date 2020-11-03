---
title: การตั้งค่าโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการตั้งค่าการจัดการของโครงการ
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: c9b8659f3b7ee81d2e21ef52743debd521fa9bb9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086095"
---
# <a name="project-settings"></a><span data-ttu-id="7662d-103">การตั้งค่าโครงการ</span><span class="sxs-lookup"><span data-stu-id="7662d-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7662d-104">ใช้การตั้งค่าต่อไปนี้ เพื่อเข้าถึงคุณลักษณะการวางแผนโครงการ</span><span class="sxs-lookup"><span data-stu-id="7662d-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="7662d-105">เท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="7662d-105">Work template</span></span>

<span data-ttu-id="7662d-106">เมื่อต้องการสร้างหมายกำหนดการให้บริการโครงการ สร้างแม่แบบปฏิทินโครงการที่กำหนดจำนวนของชั่วโมงการทำงานต่อวัน และระยะเวลาที่ปิดดำเนินการใดๆ</span><span class="sxs-lookup"><span data-stu-id="7662d-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="7662d-107">เมื่อต้องการสร้างแม่แบบปฏิทินโครงการ คุณเชื่อมโยงแม่แบบงานกับฟิลด์ **แม่แบบปฏิทิน** สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="7662d-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="7662d-108">ทำตามขั้นตอนเหล่านี้เพื่อสร้างแม่แบบงาน</span><span class="sxs-lookup"><span data-stu-id="7662d-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="7662d-109">ใน PSA ในบานหน้าต่างนำทางด้านซ้าย ให้คลิก **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="7662d-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="7662d-110">บนเพจรายการ **ทรัพยากร** ให้เปิดเรกคอร์ดผู้ใช้ แล้วเลือก **แสดงชั่วโมงทำงาน**</span><span class="sxs-lookup"><span data-stu-id="7662d-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="7662d-111">ตรวจสอบให้แน่ใจว่าคุณอนุญาตป๊อปอัพในเพจเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="7662d-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="7662d-112">ซึ่งจะช่วยให้คุณเห็นชั่วโมงทำงานที่ตั้งค่าไว้สำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7662d-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="7662d-113">บนแท็บ **มุมมองรายเดือน** ให้คลิก **ตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="7662d-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="7662d-114">รายการของสามตัวเลือกจะปรากฏขึ้น:</span><span class="sxs-lookup"><span data-stu-id="7662d-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="7662d-115">หมายกำหนดการให้บริการรายสัปดาห์ใหม่</span><span class="sxs-lookup"><span data-stu-id="7662d-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="7662d-116">กำหนดการทำงานสำหรับหนึ่งวัน</span><span class="sxs-lookup"><span data-stu-id="7662d-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="7662d-117">Time Off</span><span class="sxs-lookup"><span data-stu-id="7662d-117">Time Off</span></span>

> ![ตั้งค่าตัวเลือก](media/project-13.png)

4. <span data-ttu-id="7662d-119">เลือก **หมายกำหนดการให้บริการรายสัปดาห์ใหม่** และจากนั้นตั้งค่าตัวเลือกสำหรับหมายกำหนดการให้บริการทรัพยากรนี้</span><span class="sxs-lookup"><span data-stu-id="7662d-119">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="7662d-120">คุณสามารถตั้งค่าหมายกำหนดการให้บริการรายสัปดาห์ที่เกิดซ้ำ พารามิเตอร์ชั่วโมงประจำวัน ระยะเวลาที่ปิดดำเนินการ และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="7662d-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="7662d-121">ตั้งค่าช่วงวันที่ เลือก **บันทึก** และจากนั้นคลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="7662d-121">Set the date range, select **Save** , and then click **Close**.</span></span> 
6. <span data-ttu-id="7662d-122">กลับไปที่หน้ารายการ **ทรัพยากร** และเลือกทรัพยากรที่คุณตั้งค่าชั่วโมงทำงานให้</span><span class="sxs-lookup"><span data-stu-id="7662d-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="7662d-123">เลือก **ตั้งค่าปฏิทินเป็น** เพื่อตั้งค่าแม่แบบงาน</span><span class="sxs-lookup"><span data-stu-id="7662d-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="7662d-124">ในกล่องโต้ตอบ **แม่แบบงาน** ป้อนชื่อสำหรับแม่แบบงาน และจากนั้นเลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="7662d-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="7662d-125">ขณะนี้คุณสามารถเชื่อมโยงแม่แบบงานกับแม่แบบปฏิทินโครงการได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="7662d-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="7662d-126">บทบาทของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7662d-126">Resource roles</span></span>

<span data-ttu-id="7662d-127">คำว่า *บทบาทของทรัพยากร* หมายถึงชุดของทักษะ ความสามารถ และใบรับรองที่บุคคลต้องมีเพื่อดำเนินการชุดของงานที่เฉพาะเจาะจงในโครงการ</span><span class="sxs-lookup"><span data-stu-id="7662d-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="7662d-128">PSA ช่วยให้คุณคิดต้นทุนและเรียกเก็บเงินเวลาของทรัพยากรตามบทบาทที่เชื่อมโยงกับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7662d-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="7662d-129">ทุกองค์กรต้องตั้งค่าบทบาทเหล่านี้ โดยใช้การนำทางด้านซ้ายบนเมนู **Project Service**</span><span class="sxs-lookup"><span data-stu-id="7662d-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="7662d-130">ทุกองค์กรต้องตั้งค่าบทบาทเหล่านี้บนเพจ **ประเภททรัพยากรที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="7662d-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="7662d-131">เมื่อต้องการเปิดเพจนี้ ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **บทบาทของทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="7662d-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="7662d-132">ราคาตลาด</span><span class="sxs-lookup"><span data-stu-id="7662d-132">Price lists</span></span>

<span data-ttu-id="7662d-133">ราคาตลาดช่วยให้คุณตั้งค่าต้นทุนและราคาขายสำหรับบทบาทของทรัพยากร ประเภทค่าใช้จ่าย ผลิตภัณฑ์ และองค์ประกอบอื่นๆ ในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="7662d-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="7662d-134">ก่อนตั้งค่าการประมาณการด้านการเงินสำหรับงานที่จะต้องส่งสำหรับโครงการ คุณควรสร้างต้นทุนสำรองและราคาตลาดในการขาย</span><span class="sxs-lookup"><span data-stu-id="7662d-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="7662d-135">ในส่วนพารามิเตอร์ คุณควรตั้งค่าต้นทุนและรายการราคาตลาดของการขายเริ่มต้นที่ใช้กับโครงการทั้งหมดที่สร้างขึ้นในองค์กรด้วย</span><span class="sxs-lookup"><span data-stu-id="7662d-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="7662d-136">ในหน้า **พารามิเตอร์โครงการที่ใช้งานอยู่** โปรดตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าต้นทุนและรายการราคาตลาดของการขายเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7662d-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
