---
title: จัดกำหนดการทรัพยากรสำหรับโครงการ
description: วิธีการจัดกำหนดการทรัพยากรสำหรับโครงการใน Project Service
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: c67633960bb448d2190ec1bfde4e964f4fcb7969
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008514"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="bb92f-103">จัดกำหนดการทรัพยากรสำหรับโครงการ (Project Service)</span><span class="sxs-lookup"><span data-stu-id="bb92f-103">Schedule resources for a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="bb92f-104">คุณสามารถตรวจสอบความพร้อมใช้งานของทรัพยากรเพื่อดูมุมมองโดยรวมของวิธีการจองทรัพยากรของคุณคือ หรือคุณสามารถกรองมุมมองตามทักษะ ทีม ที่ตั้ง และตัวเลือกอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="bb92f-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="bb92f-105">บอร์ดกำหนดการแสดงรายการของทรัพยากรและความพร้อม</span><span class="sxs-lookup"><span data-stu-id="bb92f-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="bb92f-106">เลือกโหมดมุมมองเพื่อแสดงความพร้อมใช้งานตาม **ชั่วโมง** **วัน** **สัปดาห์** หรือ **เดือน**</span><span class="sxs-lookup"><span data-stu-id="bb92f-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="bb92f-107">ก่อนที่คุณจะใช้ตารางกำหนดการ สิ่งสำคัญคือการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="bb92f-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="bb92f-108">สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่าคอนฟิกบอร์ดกำหนดการ (Field Service หรือ Project Service Automation)](/dynamics365/field-service/configure-schedule-board)</span><span class="sxs-lookup"><span data-stu-id="bb92f-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="bb92f-109">ถ้าคุณกำลังใช้รุ่นที่เก่ากว่า สำหรับความพร้อมใช้งานของทรัพยากร โปรดดู [ดูความพร้อมใช้งานของทรัพยากร](../psa/view-resource-availability.md)</span><span class="sxs-lookup"><span data-stu-id="bb92f-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="bb92f-110">เมื่อต้องการใช้ฟังก์ชันการจองของตารางกำหนดการ พิกัดทางภูมิศาสตร์ และบริการตำแหน่งที่ตั้ง คุณจะต้องเปิดบนแผนผัง</span><span class="sxs-lookup"><span data-stu-id="bb92f-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="bb92f-111">บนเมนูหลัก เลือก **การจัดกำหนดการทรัพยากร** > **การจัดการ**</span><span class="sxs-lookup"><span data-stu-id="bb92f-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="bb92f-112">คลิก **พารามิเตอร์การจัดกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="bb92f-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="bb92f-113">เปิดเรกคอร์ดและเลื่อนลงไปที่ส่วน **Resource Scheduling Optimization**</span><span class="sxs-lookup"><span data-stu-id="bb92f-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="bb92f-114">ในฟิลด์ **เชื่อมต่อกับแผนผัง** เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="bb92f-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="bb92f-115">ยอมรับข้อกำหนด และบันทึกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="bb92f-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="bb92f-116">บนเมนูหลัก เลือก **Project Service** > **บอร์ดกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="bb92f-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="bb92f-117">จากที่นี่ มีวิธีหลายวิธีในการจัดกำหนดการความต้องการในการจองด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="bb92f-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="bb92f-118">เลือกวิธีการที่เหมาะสมสำหรับคุณ</span><span class="sxs-lookup"><span data-stu-id="bb92f-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="bb92f-119">ค้นหาทรัพยากรที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bb92f-119">Find available resources</span></span>

1.  <span data-ttu-id="bb92f-120">จากรายการ **ความต้องการในการจอง** คลิกขวาที่การจองที่ไม่ได้จัดกำหนดการ และเลือกรายการใดรายการหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bb92f-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="bb92f-121">เลือก **ค้นหาความพร้อมใช้งาน - ทรัพยากรปัจจุบัน** เพื่อค้นหาทรัพยากรที่พร้อมใช้งานจากรายการบนตารางกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="bb92f-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="bb92f-122">เลือก **ค้นหาความพร้อมใช้งาน - ทรัพยากรทั้งหมด** เพื่อค้นหาทรัพยากรที่พร้อมใช้งานจากทรัพยากรในระบบ</span><span class="sxs-lookup"><span data-stu-id="bb92f-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="bb92f-123">เมื่อคุณทำเช่นนี้ ตัวกรองที่จะแสดงตัวเลือกสำหรับความต้องการในการจองที่ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="bb92f-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="bb92f-124">เมื่อคุณเห็นช่องที่พร้อมใช้งาน คลิกขวาที่ช่องเวลาบนบอร์ดกำหนดการ และเลือก **จองที่นี่**</span><span class="sxs-lookup"><span data-stu-id="bb92f-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="bb92f-125">หรือลากแล้วปล่อยความต้องการในการจอง ไปที่ช่องเวลาที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bb92f-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="bb92f-126">จองทรัพยากรโดยใช้มุมมองรายวัน และค้นหาผู้ที่ไม่ได้จอง</span><span class="sxs-lookup"><span data-stu-id="bb92f-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="bb92f-127">บนบอร์ดกำหนดการ เลือก **โหมดมุมมอง** และเลือก **วัน**</span><span class="sxs-lookup"><span data-stu-id="bb92f-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="bb92f-128">ฟิลด์นี้แสดงมุมมองกริดของจำนวนชั่วโมงที่ทรัพยากรถูกจองสำหรับแต่ละวัน และวันที่ไม่ถูกจอง</span><span class="sxs-lookup"><span data-stu-id="bb92f-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="bb92f-129">คลิกที่ชื่อของทรัพยากรที่คุณต้องการจอง และจากนั้น เลือก **จอง**</span><span class="sxs-lookup"><span data-stu-id="bb92f-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="bb92f-130">ในกล่องโต้ตอบ **การจองทรัพยากร (สร้าง)** เลือกโครงการที่คุณต้องการจองทรัพยากร รวมทั้งวิธีการจอง และเวลาเริ่มต้นและเวลาสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="bb92f-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="bb92f-131">เมื่อคุณทำเสร็จแล้ว เลือก **จอง**</span><span class="sxs-lookup"><span data-stu-id="bb92f-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="bb92f-132">ดูไปยังบอร์ดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="bb92f-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="bb92f-133">เลือกความต้องการในการจองที่ไม่ได้จัดกำหนดจากรายการด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="bb92f-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="bb92f-134">ลากความต้องการในการจองไปที่ทรัพยากรที่พร้อมใช้งาน/ช่องเวลาในตารางกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="bb92f-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="bb92f-135">เมื่อคุณทำเสร็จแล้ว เลือก **จอง**</span><span class="sxs-lookup"><span data-stu-id="bb92f-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="bb92f-136">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="bb92f-136">Additional resources</span></span>  
 [<span data-ttu-id="bb92f-137">คู่มือของผู้จัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="bb92f-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]