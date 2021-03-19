---
title: ฉันจะทำการจองทรัพยากร "แบบไม่ตายตัว" ในรุ่นแอพ 2.x ได้อย่างไร?
description: บทความนี้อธิบายถึงวิธีการจองสมาชิกในกลุ่มคนของโครงการแบบไม่ตายด้วยบ Project Service
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
ms.openlocfilehash: 18a1176c131e233f62f74dc0dd8a6aa3ee561da5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286046"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="55a11-103">ฉันจะทำการจองทรัพยากร "แบบไม่ตายตัว" ในแอพเว็บได้อย่างไร (แอพ Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="55a11-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="55a11-104">คุณสามารถจัดกำหนดการอย่างไม่แน่นอน หรือ "จองแบบไม่ตายตัว" ทรัพยากรลงในกลุ่มคนของโครงการ เพื่อแสดงแผนเพื่อให้คุณกำหนดทรัพยากรให้กับโครงการ</span><span class="sxs-lookup"><span data-stu-id="55a11-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="55a11-105">การจองแบบไม่ตายตัวไม่ใช้กำลังการผลิตที่พร้อมใช้งานของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="55a11-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="55a11-106">ไม่สามารถกำหนดสมาชิกของกลุ่มคนที่มีการจองแบบไม่ตายตัวไปที่งานโครงการได้</span><span class="sxs-lookup"><span data-stu-id="55a11-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="55a11-107">ทรัพยากรที่มีสถานะจองแบบตายตัวและยอมรับชนิดที่ยอมรับ สามารถกำหนดให้กับงาน (โดยใช้สมมติฐานว่ามีชั่วโมงจองแบบตายตัวเพียงพอเพื่อครอบคลุมความพยายามในการกำหนด)</span><span class="sxs-lookup"><span data-stu-id="55a11-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="55a11-108">สมาชิกในกลุ่มคนของโครงการแบบไม่ตายตัวแสดงขึ้นในกริดสมาชิกในกลุ่มคน ที่มีชั่วโมงที่มีการจองแบบไม่ตายตัวของพวกเขาที่แสดงในคอลัมน์แบบไม่ตายตัว</span><span class="sxs-lookup"><span data-stu-id="55a11-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="55a11-109">จะแสดงขึ้นบนบอร์ดกำหนดการด้วย</span><span class="sxs-lookup"><span data-stu-id="55a11-109">They also show up on the schedule board.</span></span> <span data-ttu-id="55a11-110">อีกครั้ง จะไม่แสดงปริมาณการใช้ใดๆ ของกำลังการผลิตเป็นการจองแบบไม่ตายตัว ไม่ใช้กำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="55a11-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="55a11-111">มีวิธีสามวิธีในการจองแบบไม่ตายตัวสมาชิกในกลุ่มคนบนโครงการที่มี Project Service รุ่น 2.x</span><span class="sxs-lookup"><span data-stu-id="55a11-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="55a11-112">คุณสามารถจองแบบไม่ตายตัวด้วยบอร์ดกำหนดการ ใช้คุณลักษณะการรักษาการจอง หรือด้วยการสร้างทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="55a11-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="55a11-113">วิธีการเหล่านี้ถูกอธิบายอยู่ด้านล่างนี้</span><span class="sxs-lookup"><span data-stu-id="55a11-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="55a11-114">จองแบบไม่ตายตัวด้วยบอร์ดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="55a11-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="55a11-115">เพื่อจองแบบไม่ตายตัวด้วยบอร์ดกำหนดการ ให้ทำตามกระบวนงานนี้:</span><span class="sxs-lookup"><span data-stu-id="55a11-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="55a11-116">เปิดบอร์ดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="55a11-116">Open the schedule board.</span></span>
2. <span data-ttu-id="55a11-117">เลือกแท็บโครงการที่แผงความต้องการการจองด้านล่างของบอร์ดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="55a11-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="55a11-118">ค้นหาโครงการคุณต้องการจองแบบไม่ตายตัวทรัพยากรในนั้น</span><span class="sxs-lookup"><span data-stu-id="55a11-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="55a11-119">ถ้าคุณมีโครงการหลายโครงการ คลิกบนส่วนหัวของคอลัมน์โครงการ และจากนั้น ใช้ตัวกรองเพื่อค้นหาโครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="55a11-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="55a11-120">คลิกบนโครงการ จากนั้นลากแล้วปล่อยไว้บนกริดเวลาของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="55a11-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="55a11-121">นี่จะเปิดแผงการสร้างการจองทรัพยากรทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="55a11-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="55a11-122">ปรับปรุงวันที่เริ่มต้นและสิ้นสุด เลือกสถานะการจองเป็นแบบชั่วคราว และตั้งค่าชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="55a11-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="55a11-123">คลิกจอง</span><span class="sxs-lookup"><span data-stu-id="55a11-123">Click Book.</span></span>
7. <span data-ttu-id="55a11-124">กลับไปในโครงการ ขณะนี้ ทรัพยากรจะแสดงเป็นสมาชิกในทีมที่มีชั่วโมงที่จองแบบไม่ตายตัวในคอลัมน์การจองแบบไม่ตายตัว</span><span class="sxs-lookup"><span data-stu-id="55a11-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="55a11-125">หมายเหตุว่า คุณไม่สามารถกำหนดรายการเหล่านั้นให้กับงานในโครงสร้างการแบ่งงาน (WBS) ได้ เนื่องจากทรัพยากรต้องถูกจองแบบตายตัวในกลุ่มคนที่จะถูกกำหนด</span><span class="sxs-lookup"><span data-stu-id="55a11-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="55a11-126">จองแบบไม่ตายตัวโดยใช้คุณลักษณะรักษาการจอง</span><span class="sxs-lookup"><span data-stu-id="55a11-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="55a11-127">เพื่อจองแบบไม่ตายตัวด้วยการรักษาการจอง ให้ทำตามกระบวนงานนี้:</span><span class="sxs-lookup"><span data-stu-id="55a11-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="55a11-128">จากกริดสมาชิกในกลุ่มคน คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="55a11-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="55a11-129">เลือกทรัพยากรที่สามารถจองได้ บทบาท เริ่มต้น/สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="55a11-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="55a11-130">เลือกวิธีการปันส่วนอื่นที่ไม่ใช่ ไม่มี:</span><span class="sxs-lookup"><span data-stu-id="55a11-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="55a11-131">กำลังการผลิตแบบเต็ม</span><span class="sxs-lookup"><span data-stu-id="55a11-131">Full Capacity</span></span>
- <span data-ttu-id="55a11-132">กำลังการผลิตเป็นเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="55a11-132">Percentage Capacity</span></span>
- <span data-ttu-id="55a11-133">ตามชั่วโมง กระจายแบบเท่าๆ กัน</span><span class="sxs-lookup"><span data-stu-id="55a11-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="55a11-134">ตามชั่วโมง เน้นช่วงต้น</span><span class="sxs-lookup"><span data-stu-id="55a11-134">By Hours Front Load</span></span>
4. <span data-ttu-id="55a11-135">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="55a11-135">Click Save.</span></span> <span data-ttu-id="55a11-136">คุณจะเห็นทรัพยากรบนกริดของกลุ่มคนและชั่วโมงของพวกเขาที่ถูกระบุเป็นตายตัว</span><span class="sxs-lookup"><span data-stu-id="55a11-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="55a11-137">รักษาการจองของทรัพยากร โดยการคลิกที่รักษาการจอง</span><span class="sxs-lookup"><span data-stu-id="55a11-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="55a11-138">เมื่อบอร์ดกำหนดการเปิดขึ้น ขยายทรัพยากรเพื่อแสดงการจองของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="55a11-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="55a11-139">คุณจะเห็นการจองที่ระบุเป็นตายตัว</span><span class="sxs-lookup"><span data-stu-id="55a11-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="55a11-140">คลิกขวาที่การจอง ภายใต้สถานะการเปลี่ยน เลือกการจองแบบไม่ตายตัว และจากนั้น ไม่ตายตัว</span><span class="sxs-lookup"><span data-stu-id="55a11-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="55a11-141">ขณะนี้ สถานะการจองเป็น ไม่ตายตัว</span><span class="sxs-lookup"><span data-stu-id="55a11-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="55a11-142">หลังจากปิดบอร์ดกำหนดการ คุณจะเห็นว่า ชั่วโมงสำหรับทรัพยากรมีการเปลี่ยนแปลงจากแบบตายตัวเป็นแบบไม่ตายตัวบนกริดสมาชิกในกลุ่มคน</span><span class="sxs-lookup"><span data-stu-id="55a11-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="55a11-143">หมายเหตุว่า ถ้าคุณจองทรัพยากรแบบตายตัวลงในกลุ่มคน และจากนั้น กำหนดงานให้พวกเขาใน WBS เมื่อคุณใช้รักษาการจองเพื่อเปลี่ยนสถานะของแบบตายตัวเป็นแบบไม่ตายตัว จะเอาการกำหนดจากงานสำหรับทรัพยากรนั้น เมื่อคุณสามารถกำหนดทรัพยากรที่จองแบบตายตัวเท่ากับงานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="55a11-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="55a11-144">จองแบบไม่ตายตัวโดยการสร้างทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="55a11-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="55a11-145">คุณสามารถสร้างการจองแบบไม่ตายตัวได้โดยการสร้างสมาชิกในกลุ่มคนของทรัพยากรทั่วไป ดำเนินการตามกับบอร์ดกำหนดการหรือการร้องขอทรัพยากร และเปลี่ยนแปลงชนิดในระหว่างการจอง</span><span class="sxs-lookup"><span data-stu-id="55a11-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="55a11-146">เพื่อทำสิ่งนี้ ใช้กระบวนงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="55a11-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="55a11-147">ในโครงการ WBS กำหนดบทบาทให้กับงานคุณต้องการสร้างสมาชิกในกลุ่มคนทั่วไปให้</span><span class="sxs-lookup"><span data-stu-id="55a11-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="55a11-148">คลิกสร้างกลุ่มคนในโครงการ</span><span class="sxs-lookup"><span data-stu-id="55a11-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="55a11-149">กริดสมาชิกในกลุ่มคนของโครงการ เลือกทรัพยากรทั่วไป แล้วคลิกจอง</span><span class="sxs-lookup"><span data-stu-id="55a11-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="55a11-150">บนบอร์ดกำหนดการ เลือกทรัพยากรที่คุณต้องการจอง</span><span class="sxs-lookup"><span data-stu-id="55a11-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="55a11-151">บนแผงสร้างการจองทรัพยากรของบอร์ดกำหนดการ เปลี่ยนสถานะจองเป็นแบบไม่ตายตัว</span><span class="sxs-lookup"><span data-stu-id="55a11-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="55a11-152">คลิกจอง หรือจองและจบการทำงาน</span><span class="sxs-lookup"><span data-stu-id="55a11-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="55a11-153">หลังจากปิดบอร์ดกำหนดการ คุณจะเห็นทรัพยากรที่เลือกถูกเพิ่มลงในกลุ่มคนที่มีชั่วโมงที่แบบไม่ตายตัว ตลอดจนชั่วโมงที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="55a11-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="55a11-154">นอกจากนี้ คุณจะเห็นว่า ทรัพยากรทั่วไปยังคงอยู่ในกลุ่มคนเป็นตัวบ่งชี้ที่งานกำหนดให้กับสมาชิกในกลุ่มคนที่จองแบบไม่ตายตัว</span><span class="sxs-lookup"><span data-stu-id="55a11-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="55a11-155">เมื่อคุณพร้อมที่จะเปลี่ยนแปลงทรัพยากรสมาชิกในกลุ่มคนที่จองแบบไม่ตายตัว เป็นในกลุ่มคนที่จองแบบตายตัว เพื่อให้คุณสามารถกำหนดรายการเหล่านั้นให้กับงานได้ ดำเนินการรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="55a11-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="55a11-156">เลือกทรัพยากร และคลิกรักษาการจอง</span><span class="sxs-lookup"><span data-stu-id="55a11-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="55a11-157">เมื่อบอร์ดกำหนดการเปิดขึ้น ขยายทรัพยากรเพื่อแสดงการจองของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="55a11-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="55a11-158">คุณจะเห็นการจองถูกทำเครื่องหมายเป็นแบบไม่ตายตัว</span><span class="sxs-lookup"><span data-stu-id="55a11-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="55a11-159">คลิกขวาที่การจอง ภายใต้สถานะการเปลี่ยน เลือกการจองแบบตายตัว และจากนั้น ตายตัว</span><span class="sxs-lookup"><span data-stu-id="55a11-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="55a11-160">ขณะนี้ สถานะการจองเป็น ตายตัว</span><span class="sxs-lookup"><span data-stu-id="55a11-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="55a11-161">หลังจากปิดบอร์ดกำหนดการ คุณจะเห็นว่า ชั่วโมงสำหรับทรัพยากรมีการเปลี่ยนแปลงจากแบบไม่ตายตัวเป็นแบบตายตัวบนกริดสมาชิกในกลุ่มคน</span><span class="sxs-lookup"><span data-stu-id="55a11-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="55a11-162">ตอนนี้ คุณอาจกำหนดทรัพยากรไปที่งาน (โดยมีการจัดตำแหน่งระหว่างชั่วโมงที่จองแบบตายตัวและจำนวนชั่วโมงความพยายามของงานสำหรับการมอบหมาย)</span><span class="sxs-lookup"><span data-stu-id="55a11-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="55a11-163">หมายเหตุว่า ถ้าคุณตามขั้นตอนการบรรลุทรัพยากรทั่วไปในรายการ #3 ข้างต้น เมื่อคุณเปลี่ยนสถานะของทรัพยากรที่สามารถจองได้ซึ่งจองแบบไม่ตายตัวเป็นแบบตายตัว สมาชิกในกลุ่มคนทั่วไปจะถูกเอาออกจากกลุ่มคน</span><span class="sxs-lookup"><span data-stu-id="55a11-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]