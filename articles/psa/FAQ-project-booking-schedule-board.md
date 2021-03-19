---
title: สร้างการจองโครงการจากตารางกำหนดการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการสร้างการจองโครงการจากตารางกำหนดการ
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 5d815210ee78f3c728c0722e03bab2f790c953ee
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286136"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="4decb-103">สร้างการจองโครงการจากตารางกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="4decb-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4decb-104">คุณสามารถจองทรัพยากรไปยังโครงการได้โดยตรงบนแท็บ **ทีม** ของโครงการ หรือโดยการสร้างความต้องการทรัพยากรจากการมอบหมายสมาชิกทีมทั่วไป และจากนั้น ดำเนินการตามความต้องการที่สร้างขึ้นด้วยสมาชิกทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="4decb-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="4decb-105">คุณยังสามารถจองทรัพยากรไปยังโครงการได้โดยตรงจากตารางกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="4decb-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="4decb-106">มีสามวิธีในการที่จะจัดการสิ่งนี้ คือ</span><span class="sxs-lookup"><span data-stu-id="4decb-106">There are three ways to do this:</span></span>

- <span data-ttu-id="4decb-107">**จองจากความต้องการทรัพยากรที่สร้างขึ้น:** คุณสามารถสร้างความต้องการทรัพยากรหลังจากที่คุณสร้างทรัพยากรทั่วไป และมอบหมายงานภายในโครงการ</span><span class="sxs-lookup"><span data-stu-id="4decb-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="4decb-108">**จองจากความต้องการหลัก:** ความต้องการหลักแสดงขึ้นบนตารางกำหนดการบนแท็บ **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="4decb-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="4decb-109">**จองจากความต้องการทรัพยากรใหม่:** คุณสามารถสร้างความต้องการทรัพยากรตั้งแต่เริ่มและเชื่อมโยงเข้ากับโครงการได้</span><span class="sxs-lookup"><span data-stu-id="4decb-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="4decb-110">บนตารางกำหนดการ ความต้องการทางทรัพยากรจะแสดงขึ้นมาบนแท็บ **ความต้องการที่เปิดอยู่**</span><span class="sxs-lookup"><span data-stu-id="4decb-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="4decb-111">จองจากความต้องการทางทรัพยากรที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="4decb-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="4decb-112">คุณสามารถสร้างทรัพยากรทั่วไป และมอบหมายให้กับหนึ่งงานหรือหลายงานภายในโครงการได้</span><span class="sxs-lookup"><span data-stu-id="4decb-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="4decb-113">จากนั้น คุณสามารถสร้างความต้องการทรัพยากรจากสมาชิกทีมทั่วไป</span><span class="sxs-lookup"><span data-stu-id="4decb-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="4decb-114">บนตารางกำหนดการ ทรัพยากรนี้จะแสดงบนแท็บ **ความต้องการที่เปิดอยู่** คุณอาจต้องการใช้ตัวกรองคอลัมน์ในกริด ถ้าคุณมีความต้องการที่เปิดอยู่หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="4decb-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="4decb-115">![เปิดแท็บความต้องการบนตารางกำหนดการ](media/FAQ-Project-Booking-Schedule-Board-1.png "ภาพหน้าจอของตารางการจองและการกำหนด")</span><span class="sxs-lookup"><span data-stu-id="4decb-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="4decb-116">เลือกความต้องการ</span><span class="sxs-lookup"><span data-stu-id="4decb-116">Select the requirement.</span></span> <span data-ttu-id="4decb-117">แท็บ **ค้นหาความพร้อมให้บริการ** จะปรากฏขึ้นที่ด้านบนของแถวที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="4decb-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="4decb-118">เมื่อคุณเลือกแท็บนั้น โหมดตัวช่วยจัดกำหนดการของตารางกำหนดการ เปิดและกรองทรัพยากรที่พร้อมใช้งานที่ตรงกับความต้องการทางทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4decb-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="4decb-119">หลังจากนั้น คุณสามารถจองทรัพยากรได้</span><span class="sxs-lookup"><span data-stu-id="4decb-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="4decb-120">คุณยังสามารถลากแล้วปล่อยแถวที่ถูกเลือกจากด้านล่างของตารางกำหนดการ ไปยังเซลล์ทรัพยากรในกริดข้างต้นได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="4decb-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="4decb-121">เมื่อคุณปล่อยลง จะเปิดแผง **สร้างการจองทรัพยากร** ทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="4decb-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="4decb-122">การเลือก **จอง** จะจองทรัพยากรลงในทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="4decb-122">Selecting **Book** books the resource onto the project team.</span></span>

![สร้างแผงการจองทรัพยากร](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="4decb-124">จองจากความต้องการหลัก</span><span class="sxs-lookup"><span data-stu-id="4decb-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="4decb-125">การสร้างโครงการใน Project Service จะสร้างความต้องการทางทรัพยากรที่เรียกว่า ความต้องการหลัก โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="4decb-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="4decb-126">นี่คือความต้องการที่ว่างเปล่าที่ใช้เพื่อจองทรัพยากรอย่างรวดเร็วด้วยตารางกำหนดการ โดยไม่มีการสร้างความต้องการ หรือการสร้างตั้งแต่ต้น</span><span class="sxs-lookup"><span data-stu-id="4decb-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="4decb-127">เนื่องจากความต้องการว่างเปล่า คุณจะจำเป็นต้องระบุวันที่รวมทั้งวิธีการจัดสรรและชั่วโมง ถ้าใช้ได้</span><span class="sxs-lookup"><span data-stu-id="4decb-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="4decb-128">เพื่อจองทรัพยากรที่มีความต้องการหลัก บนตารางกำหนดการ เลือกแท็บ **โครงการ** คุณอาจต้องการใช้ตัวกรองคอลัมน์ในคอลัมน์ **โครงการ** ถ้าคุณมีหลายโครงการ</span><span class="sxs-lookup"><span data-stu-id="4decb-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="4decb-129">![ตัวกรองคอลัมน์บนตารางกำหนดการ](media/FAQ-Project-Booking-Schedule-Board-2.png "ภาพหน้าจอของตารางการจองและการกำหนด")</span><span class="sxs-lookup"><span data-stu-id="4decb-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="4decb-130">เลือกความต้องการที่มีชื่อโครงการเป็นชื่อของตนเอง และมีระยะเวลาเป็นศูนย์ (0) เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4decb-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="4decb-131">เลือกแท็บ **ค้นหาความพร้อมใช้งาน** ที่ปรากฏขึ้นในแถว</span><span class="sxs-lookup"><span data-stu-id="4decb-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="4decb-132">สิ่งนี้จะใส่ตารางกำหนดการในโหมดตัวช่วยจัดกำหนดการ และแสดงทรัพยากรที่สามารถจองได้ไปยังโครงการ</span><span class="sxs-lookup"><span data-stu-id="4decb-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="4decb-133">เนื่องจาก **ความต้องการหลัก** เป็นความต้องการที่ว่างเปล่าที่มีระยะเวลาศูนย์ (0) คุณจำเป็นต้องตั้งค่าระยะเวลาในแผง **สร้างการจองทรัพยากร** เมื่อมีการเลือกและการจองทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4decb-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="4decb-134">คุณยังสามารถเลือก **ความต้องการหลักของโครงการ** ที่ด้านล่างของตารางกำหนดการได้ และลากและปล่อยไว้บนทรัพยากรเพื่อทำการจอง</span><span class="sxs-lookup"><span data-stu-id="4decb-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="4decb-135">เนื่องจาก **ความต้องการหลัก** เป็นความต้องการที่ว่างเปล่าที่มีระยะเวลาเป็นศูนย์ (0) คุณจำเป็นต้องตั้งค่าระยะเวลาในแผง **สร้างการจองทรัพยากร** เมื่อมีการเลือกและการจองทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4decb-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="4decb-136">เมื่อคุณจองทรัพยากรผ่าน **ความต้องการหลัก** บนตารางกำหนดการ คุณเพิ่มมันไปยัวทีมโครงการโดยไม่มีการมอบหมายใด ๆ</span><span class="sxs-lookup"><span data-stu-id="4decb-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="4decb-137">จองจากความต้องการทางทรัพยากรใหม่</span><span class="sxs-lookup"><span data-stu-id="4decb-137">Book from a new resource requirement</span></span>
<span data-ttu-id="4decb-138">ทำขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์เพื่อจองทรัพยากรจากความต้องการทรัพยากรใหม่</span><span class="sxs-lookup"><span data-stu-id="4decb-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="4decb-139">ไปที่ **ความต้องการทรัพยากร** และเลือก **สร้าง** เพื่อสร้างความต้องการทรัพยากรใหม่</span><span class="sxs-lookup"><span data-stu-id="4decb-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="4decb-140">บนแท็บ **โครงการ** เลือกโครงการที่จะเชื่อมโยงความต้องการกับโครงการ</span><span class="sxs-lookup"><span data-stu-id="4decb-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="4decb-141">บนตารางกำหนดการ ความต้องการใหม่นี้แสดงเป็น **ความต้องการที่เปิดอยู่** ซึ่งคุณสามารถทำให้สำเร็จได้</span><span class="sxs-lookup"><span data-stu-id="4decb-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="4decb-142">จองทรัพยากรเพื่อเพิ่มรายการนั้นไปยังทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="4decb-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="4decb-143">เมื่อทรัพยากรถูกจองแล้ว คุณจำเป็นต้องมอบหมายงานด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="4decb-143">Now that the resource is booked, you must assign tasks manually.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]