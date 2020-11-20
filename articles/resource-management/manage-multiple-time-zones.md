---
title: จัดการโซนเวลาต่างๆ
description: เมื่อสร้างโครงการ โซนเวลาจะขึ้นอยู่กับโซนเวลาที่กำหนดไว้ในแม่แบบชั่วโมงการทำงานที่ใช้
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 278b226c88c2f441262eb5be0504f34a1964848c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119846"
---
# <a name="manage-time-zones"></a><span data-ttu-id="df872-103">จัดการโซนเวลาต่างๆ</span><span class="sxs-lookup"><span data-stu-id="df872-103">Manage time zones</span></span>

<span data-ttu-id="df872-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="df872-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="df872-105">โครงการ</span><span class="sxs-lookup"><span data-stu-id="df872-105">Projects</span></span>

<span data-ttu-id="df872-106">เมื่อสร้างโครงการ โซนเวลาจะขึ้นอยู่กับโซนเวลาที่กำหนดไว้ในแม่แบบชั่วโมงการทำงานที่ใช้</span><span class="sxs-lookup"><span data-stu-id="df872-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="df872-107">ใน **โครงการ** วันที่จะสัมพันธ์กับโซนเวลาของผู้ใช้ที่เข้าสู่ระบบในแต่ละแท็บเสมอ ยกเว้นแท็บ **งาน** เมื่อคุณดูโครงสร้างการแบ่งงาน วันที่จะแสดงในเขตเวลาของโครงการเสมอ</span><span class="sxs-lookup"><span data-stu-id="df872-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="df872-108">งาน</span><span class="sxs-lookup"><span data-stu-id="df872-108">Tasks</span></span>

<span data-ttu-id="df872-109">เมื่อมีการสร้างงาน เวลาเริ่มต้น เวลาสิ้นสุด และชั่วโมง/วันจะมีการควบคุมโดยชั่วโมงการทำงานของโครงการ</span><span class="sxs-lookup"><span data-stu-id="df872-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="df872-110">ตัวอย่างเช่น ถ้ามีการสร้างงานด้วยโครงการที่มีโซนเวลา -8 PST และมีเวลาทำงานต่อไปนี้: 9.00 - 17.00 น. วันจันทร์ถึงวันศุกร์ งานใดๆ ที่สร้างขึ้นโดยไม่มีการมอบหมายจะใช้เวลาเริ่มต้นและเวลาสิ้นสุดของปฏิทินโครงการ</span><span class="sxs-lookup"><span data-stu-id="df872-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="df872-111">จัดการทรัพยากรด้วยโซนเวลา</span><span class="sxs-lookup"><span data-stu-id="df872-111">Manage resources with time zones</span></span>

<span data-ttu-id="df872-112">เพื่อผลลัพธ์ที่แม่นยำและคาดเดาได้เมื่อใช้ **ขยายเวลาการจอง** มีข้อกำหนดเบื้องต้นที่สำคัญสองประการที่ต้องปฏิบัติตาม:</span><span class="sxs-lookup"><span data-stu-id="df872-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="df872-113">ผู้ใช้ต้องกำหนดค่าโซนเวลาของอุปกรณ์ให้ตรงกับโซนเวลาที่กำหนดไว้ใน **การตั้งค่าส่วนบุคคล** ของระบบ</span><span class="sxs-lookup"><span data-stu-id="df872-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![การตั้งค่าโซนเวลาใน Windows 10](media/reconcile-assignments-03.png)

  ![การตั้งค่าโซนเวลาในการตั้งค่าส่วนบุคคล](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="df872-116">ทรัพยากรที่สามารถจองได้ต้องมีเวลาทำงานอย่างน้อยหนึ่งนาทีที่ทับซ้อนกับเส้นชั้นที่ใช้เพื่อกำหนดส่วนขยายที่ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="df872-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="df872-117">ตัวอย่างเช่น ทรัพยากรต่อไปนี้ซึ่งมีเวลาทำงานอยู่ระหว่าง 9.00 น. ถึง 19.00 น.</span><span class="sxs-lookup"><span data-stu-id="df872-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![การเปรียบเทียบเส้นชั้นของทรัพยากร](media/reconcile-assignments-05.png)

<span data-ttu-id="df872-119">ตารางต่อไปนี้แสดง:</span><span class="sxs-lookup"><span data-stu-id="df872-119">The following table shows:</span></span>

- <span data-ttu-id="df872-120">แม่แบบปฏิทินโครงการ</span><span class="sxs-lookup"><span data-stu-id="df872-120">A project calendar template</span></span>
- <span data-ttu-id="df872-121">ทรัพยากร A: ทรัพยากรนี้มีปฏิทินเดียวกันและอยู่ในโซนเวลาเดียวกันกับโครงการ</span><span class="sxs-lookup"><span data-stu-id="df872-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="df872-122">เวลาเริ่มต้นของการจองจะเป็น 9.00 น.</span><span class="sxs-lookup"><span data-stu-id="df872-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="df872-123">ทรัพยากร B: ทรัพยากรนี้อยู่ในโซนเวลาที่แตกต่างจากโครงการ และเริ่มเวลา 07:00 น. ในโซนเวลาของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="df872-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="df872-124">อย่างไรก็ตาม การจองจะเริ่มในเวลา 9.00 น. เนื่องจากเป็นเวลาเริ่มต้นที่เร็วที่สุดของเส้นชั้นการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="df872-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="df872-125">ทรัพยากร C และ D: ทรัพยากรอยู่ในโซนเวลาที่แตกต่างกัน ทั้งคู่แตกต่างกันและแตกต่างจากโครงการ และการจองของพวกเขาเริ่มต้นไม่เร็วกว่าเวลาเริ่มต้นที่มีอยู่ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="df872-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="df872-126">เอนทิตี</span><span class="sxs-lookup"><span data-stu-id="df872-126">Entity</span></span>  |<span data-ttu-id="df872-127">ปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="df872-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="df872-128">แม่แบบปฏิทินโครงการ</span><span class="sxs-lookup"><span data-stu-id="df872-128">Project calendar template</span></span>   | ![ปฏิทินโครงการ](media/reconcile-assignments-06.png) |
|<span data-ttu-id="df872-130">ทรัพยากร A</span><span class="sxs-lookup"><span data-stu-id="df872-130">Resource A</span></span>  | ![ปฏิทินทรัพยากร A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="df872-132">ทรัพยากร B</span><span class="sxs-lookup"><span data-stu-id="df872-132">Resource B</span></span>  |  ![ปฏิทินทรัพยากร B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="df872-134">ทรัพยากร C</span><span class="sxs-lookup"><span data-stu-id="df872-134">Resource C</span></span>  |  ![ปฏิทินทรัพยากร C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="df872-136">ทรัพยากร D</span><span class="sxs-lookup"><span data-stu-id="df872-136">Resource D</span></span>  | ![ปฏิทินทรัพยากร D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="df872-138">เมื่อคุณไปที่มุมมอง **การกระทบยอด** การมอบหมายทรัพยากรและการจองไมเพียงพอที่เกี่ยวข้องจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="df872-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![มุมมองการกระทบยอดก่อนการขยาย](media/reconcile-assignments-10.png)

<span data-ttu-id="df872-140">หลังจากใช้ฟังก์ชันขยายการจอง สำหรับทรัพยากรแต่ละรายแล้ว การจองจะมีการขยายสำหรับทรัพยากรแต่ละได้สำเร็จเนื่องจากชั่วโมงการทำงานของทรัพยากรแต่ละรายทับซ้อนกับลักษณะของการไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="df872-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![มุมมองการกระทบยอดหลังจากการขยายการจอง](media/reconcile-assignments-11.png) 

<span data-ttu-id="df872-142">โปรดสังเกตว่าการดูข้อมูลการจองอย่างละเอียดยิ่งขึ้นจะเห็นความแตกต่างในเวลาเริ่มต้นของการจอง</span><span class="sxs-lookup"><span data-stu-id="df872-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="df872-143">การจองเริ่มต้นไม่เร็วกว่าเวลาเริ่มต้นของลักษณะการมอบหมายและไม่เร็วกว่าเวลาเริ่มต้นที่มีอยู่ของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="df872-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![การจองทรัพยากรใหม่ในตารางกำหนดการ](media/reconcile-assignments-12.png)
