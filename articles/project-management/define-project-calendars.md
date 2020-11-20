---
title: กำหนดปฏิทินโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการใช้ปฏิทินโครงการเพื่อติดตามกำหนดการของโครงการ
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 442a901af8754fa0335bbf43f4ac8c73b11f9499
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131681"
---
# <a name="define-project-calendars"></a><span data-ttu-id="f7e0d-103">กำหนดปฏิทินโครงการ</span><span class="sxs-lookup"><span data-stu-id="f7e0d-103">Define project calendars</span></span>

<span data-ttu-id="f7e0d-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="f7e0d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f7e0d-105">เมื่อต้องการสร้างหมายกำหนดการให้บริการโครงการ สร้างแม่แบบปฏิทินโครงการที่กำหนดจำนวนของชั่วโมงการทำงานต่อวัน และระยะเวลาที่ปิดดำเนินการใดๆ</span><span class="sxs-lookup"><span data-stu-id="f7e0d-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="f7e0d-106">เมื่อต้องการสร้างแม่แบบปฏิทินโครงการ คุณเชื่อมโยงแม่แบบงานกับฟิลด์ **แม่แบบปฏิทิน** สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="f7e0d-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="f7e0d-107">ทำตามขั้นตอนเหล่านี้เพื่อสร้างแม่แบบงาน</span><span class="sxs-lookup"><span data-stu-id="f7e0d-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="f7e0d-108">ในบานหน้าต่างการนำทางด้านซ้าย เลือก **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="f7e0d-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="f7e0d-109">บนเพจรายการ **ทรัพยากร** ให้เปิดเรกคอร์ดผู้ใช้ แล้วเลือก **แสดงชั่วโมงทำงาน**</span><span class="sxs-lookup"><span data-stu-id="f7e0d-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="f7e0d-110">ตรวจสอบให้แน่ใจว่าคุณอนุญาตป๊อปอัพในเพจเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="f7e0d-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="f7e0d-111">ซึ่งจะช่วยให้คุณเห็นชั่วโมงทำงานที่ตั้งค่าไว้สำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="f7e0d-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="f7e0d-112">บนแท็บ **มุมมองรายเดือน** ให้เลือก **ตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="f7e0d-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="f7e0d-113">รายการของสามตัวเลือกจะปรากฏขึ้น:</span><span class="sxs-lookup"><span data-stu-id="f7e0d-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="f7e0d-114">หมายกำหนดการให้บริการรายสัปดาห์ใหม่</span><span class="sxs-lookup"><span data-stu-id="f7e0d-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="f7e0d-115">กำหนดการทำงานสำหรับหนึ่งวัน</span><span class="sxs-lookup"><span data-stu-id="f7e0d-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="f7e0d-116">Time Off</span><span class="sxs-lookup"><span data-stu-id="f7e0d-116">Time Off</span></span>

4. <span data-ttu-id="f7e0d-117">เลือก **หมายกำหนดการให้บริการรายสัปดาห์ใหม่** และจากนั้นตั้งค่าตัวเลือกสำหรับหมายกำหนดการให้บริการทรัพยากรนี้</span><span class="sxs-lookup"><span data-stu-id="f7e0d-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="f7e0d-118">คุณสามารถตั้งค่าหมายกำหนดการให้บริการรายสัปดาห์ที่เป็นกิจวัตร พารามิเตอร์ชั่วโมงประจำวัน ระยะเวลาที่ปิดดำเนินการ และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="f7e0d-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="f7e0d-119">ตั้งค่าช่วงวันที่ เลือก **บันทึก** และจากนั้นเลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="f7e0d-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="f7e0d-120">กลับไปที่หน้ารายการ **ทรัพยากร** และเลือกทรัพยากรที่คุณตั้งค่าชั่วโมงทำงานให้</span><span class="sxs-lookup"><span data-stu-id="f7e0d-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="f7e0d-121">เลือก **ตั้งค่าปฏิทินเป็น** เพื่อตั้งค่าแม่แบบงาน</span><span class="sxs-lookup"><span data-stu-id="f7e0d-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="f7e0d-122">ในกล่องโต้ตอบ **แม่แบบงาน** ป้อนชื่อสำหรับแม่แบบงาน และจากนั้นเลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="f7e0d-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="f7e0d-123">ขณะนี้คุณสามารถเชื่อมโยงแม่แบบงานกับแม่แบบปฏิทินโครงการได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="f7e0d-123">You can now associate the work template with a project calendar template.</span></span>
