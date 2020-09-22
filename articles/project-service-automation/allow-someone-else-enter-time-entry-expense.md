---
title: อนุญาตให้บุคคลอื่นป้อนรายการเวลาหรือค่าใช้จ่ายของคุณ
description: อนุญาตให้บุคคลอื่นป้อนรายการเวลาหรือค่าใช้จ่ายของคุณใน Project Service
author: revathiMuthiah
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 7/31/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 553cb9e3-8294-4469-b9f5-f0ef2d51f1f0
ms.author: revathim
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: dce23a1de2d56bcb6b20ec095b971cb23951c45c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756446"
---
# <a name="allow-someone-else-to-enter-your-time-entry-or-expense-project-service"></a><span data-ttu-id="84de4-103">อนุญาตให้บุคคลอื่นป้อนรายการเวลาหรือค่าใช้จ่ายของคุณ (Project Service)</span><span class="sxs-lookup"><span data-stu-id="84de4-103">Allow someone else to enter your time entry or expense (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="84de4-104">ตั้งค่าผู้รับมอบสิทธิ์ เพื่อให้ผู้อื่นทำรายการเวลาหรือค่าใช้จ่ายในนามของคุณใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ได้</span><span class="sxs-lookup"><span data-stu-id="84de4-104">Set up a delegate to let someone else make time or expense entries on your behalf in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  
  
## <a name="create-a-delegate"></a><span data-ttu-id="84de4-105">สร้างผู้รับมอบสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="84de4-105">Create a delegate</span></span>  
  
1.  <span data-ttu-id="84de4-106">จากเมนูหลัก คลิก **Project Service** > **ผู้รับมอบสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="84de4-106">From the main menu, click **Project Service** > **Delegations**.</span></span>  
  
2.  <span data-ttu-id="84de4-107">บนแถบคำสั่ง คลิก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="84de4-107">On the command bar, click **New**.</span></span>  
  
3. <span data-ttu-id="84de4-108">**ชื่อ**: ป้อนชื่อสำหรับเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="84de4-108">**Name**: Enter a name for the record.</span></span>  
  
4. <span data-ttu-id="84de4-109">**ชนิด**: เลือกว่าผู้รับมอบสิทธิ์สามารถป้อนรายการเวลา หรือค่าใช้จ่ายได้ ในนามของคุณ</span><span class="sxs-lookup"><span data-stu-id="84de4-109">**Type**: Select whether the delegate can enter time or expense entries on your behalf.</span></span>  
  
5. <span data-ttu-id="84de4-110">**ผู้รับมอบสิทธิ์**: เลือกชื่อของบุคคลที่คุณต้องการให้เป็นผู้รับมอบสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="84de4-110">**Delegate**: Select the name of the person you want to be the delegate.</span></span>  
  
6. <span data-ttu-id="84de4-111">**วันที่เริ่มต้นและวันที่สิ้นสุด**: เลือกวันที่ที่การมอบหมายเริ่มต้น และสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="84de4-111">**Start and end dates**: Choose dates when delegation starts and ends.</span></span>  
  
7.  <span data-ttu-id="84de4-112">เมื่อคุณทำเสร็จแล้ว คลิก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="84de4-112">When you're done, click **Save & Close**.</span></span>  
  
## <a name="turn-off-delegation"></a><span data-ttu-id="84de4-113">ปิดการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="84de4-113">Turn off delegation</span></span>  
  
1.  <span data-ttu-id="84de4-114">จากเมนูหลัก คลิก **Project Service** > **ผู้รับมอบสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="84de4-114">From the main menu, click **Project Service** > **Delegations**.</span></span>  
  
2.  <span data-ttu-id="84de4-115">เลือกเรกคอร์ดการมอบหมายที่คุณต้องการปิด</span><span class="sxs-lookup"><span data-stu-id="84de4-115">Select the delegation record you want to turn off.</span></span>  
  
3.  <span data-ttu-id="84de4-116">บนแถบคำสั่ง คลิก **ปิดการใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="84de4-116">On the command bar, click **Deactivate**.</span></span>  
  
4.  <span data-ttu-id="84de4-117">ในกล่องโต้ตอบ **ยืนยันการปิดใช้งาน** คลิก **ปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="84de4-117">On the **Confirm Deactivation** dialog box, click **Deactivate**.</span></span>  
  
## <a name="enter-time-for-someone-else"></a><span data-ttu-id="84de4-118">ป้อนเวลาให้บุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="84de4-118">Enter time for someone else</span></span>  
  
1.  <span data-ttu-id="84de4-119">จากเมนูหลัก คลิก **Project Service** > **รายการเวลา**</span><span class="sxs-lookup"><span data-stu-id="84de4-119">From the main menu, click **Project Service** > **Time Entries**.</span></span>  
  
2.  <span data-ttu-id="84de4-120">บนแถบคำสั่ง เลือกเมนูแบบหล่นลง **ชื่อทรัพยากร** และเลือกชื่อของบุคคลที่คุณกำลังป้อนเวลาให้</span><span class="sxs-lookup"><span data-stu-id="84de4-120">On the command bar, select the **RESOURCE NAME** drop-down menu, and select the name of the person who you’re entering time for.</span></span>  
  
3.  <span data-ttu-id="84de4-121">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="84de4-121">Click **OK**.</span></span>  
  
4.  <span data-ttu-id="84de4-122">นี่จะแสดงปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="84de4-122">This brings up the calendar.</span></span> <span data-ttu-id="84de4-123">เพื่อดูปฏิทินสำหรับสัปดาห์ก่อนหน้าหรือถัดไป คลิก **ก่อนหน้า** หรือ **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="84de4-123">To see the calendar for the previous or next week, click **Previous** or **Next**.</span></span> <span data-ttu-id="84de4-124">คลิก **วันนี้** เพื่อกลับไปในสัปดาห์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="84de4-124">Click **Today** to get back to the current week.</span></span>  
  
5.  <span data-ttu-id="84de4-125">เพื่อป้อนเวลาของคุณ คลิก **สร้าง** หรือคลิกสองครั้งในปฏิทิน ภายใต้วันที่คุณต้องการป้อนเวลา อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="84de4-125">To enter your time, either click **New** or double-click in the calendar under the day you want to enter time for.</span></span>  
  
6.  <span data-ttu-id="84de4-126">กรอกข้อมูลในฟิลด์ในฟอร์ม **รายการเวลา** และคลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="84de4-126">Fill in the fields in the **Time Entry** form and click **Save**.</span></span>  
  
7.  <span data-ttu-id="84de4-127">ป้อนเวลาต่อไปสำหรับสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="84de4-127">Continue entering time for the week.</span></span> <span data-ttu-id="84de4-128">เมื่อคุณทำเสร็จแล้ว และทุกอย่างถูกต้องดีแล้ว คลิก **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="84de4-128">When you’re done and everything looks correct, click **Submit**.</span></span>  
  
## <a name="enter-expenses-for-someone-else"></a><span data-ttu-id="84de4-129">ป้อนค่าใช้จ่ายให้บุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="84de4-129">Enter expenses for someone else</span></span>  
  
1.  <span data-ttu-id="84de4-130">จากเมนูหลัก คลิก **Project Service** > **ค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="84de4-130">From the main menu, click **Project Service** > **Expenses**.</span></span>  
  
2.  <span data-ttu-id="84de4-131">บนแถบคำสั่ง เลือกเมนูแบบหล่นลง **ชื่อทรัพยากร** และเลือกชื่อของบุคคลที่คุณกำลังป้อนค่าใช้จ่ายให้</span><span class="sxs-lookup"><span data-stu-id="84de4-131">On the command bar, select the **RESOURCE NAME** drop-down menu, and select the name of the person who you’re entering expenses for.</span></span>  
  
3.  <span data-ttu-id="84de4-132">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="84de4-132">Click **OK**.</span></span>  
  
4.  <span data-ttu-id="84de4-133">เพื่อดูปฏิทินสำหรับสัปดาห์ก่อนหน้าหรือถัดไป คลิก **ก่อนหน้า** หรือ **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="84de4-133">To see the calendar for the previous or next week, click **Previous** or **Next**.</span></span> <span data-ttu-id="84de4-134">คลิก **วันนี้** เพื่อกลับไปในสัปดาห์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="84de4-134">Click **Today** to get back to the current week.</span></span>  
  
5.  <span data-ttu-id="84de4-135">เมื่อต้องการป้อนค่าใช้จ่าย คลิก **ใหม่** หรือ</span><span class="sxs-lookup"><span data-stu-id="84de4-135">To enter an expense, either click **New**</span></span>  
  
6.  <span data-ttu-id="84de4-136">กรอกข้อมูลในฟิลด์ในฟอร์ม **ค่าใช้จ่ายใหม่**</span><span class="sxs-lookup"><span data-stu-id="84de4-136">Fill in the fields in the **New Expense** form.</span></span> <span data-ttu-id="84de4-137">คุณยังสามารถเพิ่มใบเสร็จรับเงินได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="84de4-137">You can also add receipts.</span></span>  
  
7.  <span data-ttu-id="84de4-138">เมื่อคุณทำเสร็จแล้ว คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="84de4-138">When you’re done, click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="84de4-139">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="84de4-139">See Also</span></span>  
 [<span data-ttu-id="84de4-140">เวลา ค่าใช้จ่าย และคำแนะนำในการทำงานร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="84de4-140">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)
