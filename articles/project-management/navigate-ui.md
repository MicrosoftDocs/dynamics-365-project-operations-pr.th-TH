---
title: การนำทางอินเทอร์เฟซผู้ใช้
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการจัดการทรัพยากรในการดำเนินการ Dynamics 365 Project
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 02dda534dcab4e8fee0a96a7e09759c32a669be5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286766"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="73b70-103">การนำทางอินเทอร์เฟซผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="73b70-103">Navigating the user interface</span></span>

<span data-ttu-id="73b70-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="73b70-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="73b70-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="73b70-105">Overview</span></span>

<span data-ttu-id="73b70-106">ฟอร์มโครงการหลักแบ่งออกเป็นหลายแท็บ</span><span class="sxs-lookup"><span data-stu-id="73b70-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="73b70-107">แต่ละแท็บแสดงถึงระดับรายละเอียดที่แตกต่างกันภายในโครงการ</span><span class="sxs-lookup"><span data-stu-id="73b70-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="73b70-108">**สรุป**: ให้คำอธิบายของโครงการและรวมทั้งผลการดำเนินงานตามแผนและโครงการจริง</span><span class="sxs-lookup"><span data-stu-id="73b70-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![แท็บสรุปและฟิลด์](media/navigation7.png)

- <span data-ttu-id="73b70-110">**งาน**: ให้รายละเอียดเกี่ยวกับโครงสร้างการแบ่งงานที่แสดงโดยมุมมองกริด มุมมองตาราง และแกนต์</span><span class="sxs-lookup"><span data-stu-id="73b70-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![แท็บงานและฟิลด์](media/navigation8.png)

- <span data-ttu-id="73b70-112">**ทีม**: ให้รายละเอียดเกี่ยวกับผู้เข้าร่วมโครงการ</span><span class="sxs-lookup"><span data-stu-id="73b70-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="73b70-113">กำลังคนที่ได้รับมอบหมายของสมาชิกทีมแต่ละคนยังสรุปไว้ในมุมมองนี้ด้วย</span><span class="sxs-lookup"><span data-stu-id="73b70-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![แท็บทีมและฟิลด์](media/navigation9.png)

- <span data-ttu-id="73b70-115">**การมอบหมายทรัพยากร**: ให้มุมมองตามระยะเวลาของกำลังคนของทรัพยากรแต่ละรายในโครงการ</span><span class="sxs-lookup"><span data-stu-id="73b70-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![แท็บการมอบหมายทรัพยากรและฟิลด์](media/navigation10.png)

- <span data-ttu-id="73b70-117">**การกระทบยอดทรัพยากร**: ให้มุมมองตามระยะเวลาของความแตกต่างระหว่างการมอบหมายของทรัพยากรที่ระบุชื่อแต่ละรายและการจอง</span><span class="sxs-lookup"><span data-stu-id="73b70-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![แท็บการกระทบยอดทรัพยากรและฟิลด์](media/navigation11.png)

- <span data-ttu-id="73b70-119">**ประมาณการ**: ให้มุมมองตามระยะเวลาของประมาณการต้นทุนและยอดขายของโครงการ</span><span class="sxs-lookup"><span data-stu-id="73b70-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![แท็บประมาณการและฟิลด์](media/navigation12.png)

- <span data-ttu-id="73b70-121">**การติดตาม**: ให้มุมมองที่แสดงความคืบหน้าของงานในโครงสร้างการแบ่งงานสำหรับกำลังคน ต้นทุน และยอดขาย</span><span class="sxs-lookup"><span data-stu-id="73b70-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![แท็บการติดตามและฟิลด์](media/navigation13.png)

- <span data-ttu-id="73b70-123">**ยอดขาย**: ให้ลิงก์ในรายละเอียดของใบเสนอราคาและสัญญาที่เกี่ยวข้องกับโครงการ</span><span class="sxs-lookup"><span data-stu-id="73b70-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="73b70-124">**ประมาณการค่าใช้จ่าย**: แสดงตารางที่กำหนดค่าใช้จ่ายโครงการตามประเภทค่าใช้จ่ายขององค์กร</span><span class="sxs-lookup"><span data-stu-id="73b70-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![แท็บประมาณการค่าใช้จ่ายและฟิลด์](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="73b70-126">ตัวควบคุมตาราง</span><span class="sxs-lookup"><span data-stu-id="73b70-126">Grid controls</span></span>

<span data-ttu-id="73b70-127">ต่อไปนี้เป็นภาพรวมคร่าวๆ ของตัวควบคุมทั่วไปที่พบในแท็บการวางแผนโครงการต่างๆ</span><span class="sxs-lookup"><span data-stu-id="73b70-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="73b70-128">รีเฟรช</span><span class="sxs-lookup"><span data-stu-id="73b70-128">Refresh</span></span>

<span data-ttu-id="73b70-129">**รีเฟรช**: ดึงข้อมูลล่าสุดจากเซิร์ฟเวอร์หากมีการเปลี่ยนแปลงเกิดขึ้นหลังจากโหลดตาราง</span><span class="sxs-lookup"><span data-stu-id="73b70-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![ปุ่มรีเฟรช](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="73b70-131">จัดกลุ่มตาม</span><span class="sxs-lookup"><span data-stu-id="73b70-131">Group by</span></span>

<span data-ttu-id="73b70-132">**จัดกลุ่มตาม** : ปรับปรุงการจัดกลุ่มของแถวในตารางเพื่อสะท้อนให้เห็นทรัพยากร บทบาท หรือประเภทตามความต้องการของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="73b70-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![ปุ่มจัดกลุ่มตาม](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="73b70-134">ก่อนหน้า/ถัดไป</span><span class="sxs-lookup"><span data-stu-id="73b70-134">Previous/Next</span></span>

<span data-ttu-id="73b70-135">**ก่อนหน้า**/**ถัดไป**: ปรับปรุงช่วงเวลาที่มองเห็นได้บนตารางแบบแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="73b70-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![ปุ่มก่อนหน้าและถัดไป](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="73b70-137">สเกลเวลา</span><span class="sxs-lookup"><span data-stu-id="73b70-137">Timescale</span></span>

<span data-ttu-id="73b70-138">**สเกลเวลา**: เปลี่ยนการรวมของข้อมูลที่แบ่งตามเวลาระหว่างวัน สัปดาห์ เดือน และปี</span><span class="sxs-lookup"><span data-stu-id="73b70-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![ปุ่มสเกลเวลา](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="73b70-140">ขยาย</span><span class="sxs-lookup"><span data-stu-id="73b70-140">Expand</span></span>

<span data-ttu-id="73b70-141">**ขยาย**: แสดงเส้นตารางที่มองเห็นเป็นแบบเต็มหน้าจอเพื่อเพิ่มความสามารถในการดูบทบาทเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="73b70-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![ปุ่ม ขยาย](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="73b70-143">ระยะเวลาตาม</span><span class="sxs-lookup"><span data-stu-id="73b70-143">Time-phase by</span></span>

<span data-ttu-id="73b70-144">**ระยะเวลาตาม**: ปรับปรุงการจัดกลุ่มของแถวในตารางเพื่อแสดงการประมาณการต้นทุนสำหรับประมาณการยอดขาย</span><span class="sxs-lookup"><span data-stu-id="73b70-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="73b70-145">ตัวควบคุมนี้ยังใช้กับสคริปต์ประมาณการและตารางการติดตามด้วย</span><span class="sxs-lookup"><span data-stu-id="73b70-145">This control also applies to the estimate script and the tracking grid.</span></span>

![ปุ่มระยะเวลาตาม](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="73b70-147">เพิ่มคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="73b70-147">Add column</span></span>

<span data-ttu-id="73b70-148">**เพิ่มคอลัมน์**: อนุญาตให้ผู้ใช้กำหนดคอลัมน์ที่มองเห็นได้ในตาราง</span><span class="sxs-lookup"><span data-stu-id="73b70-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="73b70-149">คุณสามารถเพิ่มได้เฉพาะคอลัมน์สำเร็จรูปในตารางในฟอร์ม **การวางแผนโครงการ** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="73b70-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![ปุ่มเพิ่มคอลัมน์](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]