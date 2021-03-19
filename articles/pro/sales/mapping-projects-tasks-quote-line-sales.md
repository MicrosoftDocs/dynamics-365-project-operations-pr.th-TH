---
title: แม็ปโครงการและงานกับรายการใบเสนอราคาตามโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการแม็ปโครงการและงานกับรายการงานตามโครงการ
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d714304f408050babae1a6ba74268979e0b6ea4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272771"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="0e778-103">แม็ปโครงการและงานกับรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e778-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="0e778-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="0e778-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0e778-105">ในรายการใบเสนอราคาตามโครงการ คุณสามารถแม็ปงานเฉพาะของโครงการที่เชื่อมโยงกับรายการใบเสนอราคาได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="0e778-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="0e778-106">เมื่อคุณแม็ปงานกับรายการใบเสนอราคา รายการต่อไปนี้ที่คุณกำหนดไว้ในรายการใบเสนอราคาจะใช้กับงานเหล่านั้นเท่านั้น:</span><span class="sxs-lookup"><span data-stu-id="0e778-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="0e778-107">วิธีการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="0e778-107">Billing method</span></span>
- <span data-ttu-id="0e778-108">ตัวเลือกการคิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="0e778-108">Chargeability options</span></span>
- <span data-ttu-id="0e778-109">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="0e778-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="0e778-110">ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0e778-110">Customers</span></span>

<span data-ttu-id="0e778-111">ตัวอย่างเช่น คุณอาจมีโครงการที่ระยะหนึ่งเป็นราคาคงที่ และระยะอื่นๆ ทั้งหมดเป็นเวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="0e778-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="0e778-112">ในกรณีนี้ คุณสามารถเชื่อมโยงระบะแรกและงานย่อยทั้งหมดเข้ากับรายการใบเสนอราคาสำหรับระยะนั้นด้วยวิธีการเรียกเก็บเงินแบบราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="0e778-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="0e778-113">จากนั้นคุณสามารถเชื่อมโยงระยะอื่นๆ ทั้งหมดกับรายการใบเสนอราคาตามเวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="0e778-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="0e778-114">เชื่อมโยงงานกับรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e778-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="0e778-115">คุณสามารถเชื่อมโยงงานกับรายการใบเสนอราคาจากตำแหน่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0e778-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="0e778-116">เพจ **โครงการ** > แท็บ **การเรียกเก็บเงินของงาน** (เหมาะสมที่สุด)</span><span class="sxs-lookup"><span data-stu-id="0e778-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="0e778-117">เพจ **รายการใบเสนอราคา** > แท็บ **งานที่คิดค่าธรมเนียม**</span><span class="sxs-lookup"><span data-stu-id="0e778-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="0e778-118">จากเพจโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e778-118">From the Project page</span></span>

<span data-ttu-id="0e778-119">เพจ **โครงการ** มอบประสบการณ์ที่ดีที่สุดสำหรับการเชื่อมโยงงานกับรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="0e778-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="0e778-120">คุณสามารถใช้เพจนี้เพื่อเลือกหลายๆ งานและเชื่อมโยงงานทั้งหมด รวมทั้งงานรองกับรายการใบเสนอราคาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0e778-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="0e778-121">บนแท็บ **ทั่วไป** ของรายการใบเสนอราคาตามโครงการ ตรวจสอบว่าฟิลด์ **โครงการ** มีการกรอกข้อมูลแล้ว</span><span class="sxs-lookup"><span data-stu-id="0e778-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="0e778-122">ในฟิลด์ **งานที่รวมไว้** ให้เลือก **งานที่เลือกเท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="0e778-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="0e778-123">บันทึกรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e778-123">Save the project-based quote line.</span></span> <span data-ttu-id="0e778-124">เมื่อฟอร์มรีเฟรช แท็บ **งานที่คิดค่าธรมเนียม** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="0e778-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="0e778-125">บนแท็บ **ทั่วไป** เลือกลิงก์สำหรับโครงการจากฟิลด์ **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="0e778-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="0e778-126">บนเพจ **โครงการ** เลือกแท็บ **การเรียกเก็บเงินงาน**</span><span class="sxs-lookup"><span data-stu-id="0e778-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="0e778-127">ในตารางที่สองซึ่งใช้กับการตั้งค่าการเรียกเก็บเงินเฉพาะงาน ให้เลือกงานอย่างน้อยหนึ่งงาน จากนั้นเลือก **เชื่อมโยงรายการใบเสนอราคา**</span><span class="sxs-lookup"><span data-stu-id="0e778-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="0e778-128">ในเพจกล่องโต้ตอบที่ปรากฏขึ้น ให้เลือกรายการใบเสนอราคาที่แสดงรายการใบเสนอราคาตามโครงการบนใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="0e778-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="0e778-129">ในฟิลด์ **ชนิดการเรียกเก็บเงิน** ระบุว่างานเหล่านี้มีการคิดค่าธรรมเนียมหรือไม่คิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="0e778-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="0e778-130">เลือกกล่องกาเครื่องหมายเพื่อระบุว่าการเชื่อมโยงควรรวมงานย่อยของงานที่เลือกไว้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e778-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="0e778-131">การทำเครื่องหมายในกล่องนี้จะเชื่อมโยงงานย่อยของงานที่เลือกเข้ากับรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="0e778-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="0e778-132">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="0e778-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="0e778-133">จากเพจรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="0e778-133">From the Quote line page</span></span>

<span data-ttu-id="0e778-134">คุณสามารถเชื่อมโยงงานโครงการกับรายการใบเสนอราคาจากแท็บ **งานที่คิดค่าธรรมเนียม** บนเพจ **รายการใบเสนอราคา**</span><span class="sxs-lookup"><span data-stu-id="0e778-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="0e778-135">สถานที่ที่เหมาะสมที่สุดในการเชื่อมโยงงานโครงการกับรายการใบเสนอราคาคือบนแท็บ **การเรียกเก็บเงินของงาน** บนเพจ **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="0e778-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="0e778-136">หากคุณเชื่อมโยงงานจากแท็บ **งานที่คิดค่าธรรมเนียม** บนเพจ **รายการใบเสนอราคา** คุณต้องเชื่อมโยงแต่ละโครงการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="0e778-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="0e778-137">บนแท็บ **ทั่วไป** ของรายการใบเสนอราคาตามโครงการ ตรวจสอบว่ามีการเลือกโครงการในฟิลด์ **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="0e778-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="0e778-138">ในฟิลด์ **งานที่รวมไว้** ให้เลือก **งานที่เลือกเท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="0e778-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="0e778-139">บันทึกรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e778-139">Save the project-based quote line.</span></span> <span data-ttu-id="0e778-140">เมื่อฟอร์มรีเฟรช แท็บ **งานที่คิดค่าธรมเนียม** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="0e778-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="0e778-141">บนแท็บ **งานที่คิดค่าธรรมเนียม** เลือก **เพิ่มงานรายการใบเสนอราคา**</span><span class="sxs-lookup"><span data-stu-id="0e778-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="0e778-142">บนเพจ **งานรายการใบเสนอราคา** ในฟิลด์ **งาน** เลือกงานและในฟิลด์ **ชนิดการเรียกเก็บเงิน** ให้เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0e778-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="0e778-143">ปิดเพจ</span><span class="sxs-lookup"><span data-stu-id="0e778-143">Close the page.</span></span> <span data-ttu-id="0e778-144">ขณะนี้งานที่เลือกเชื่อมโยงกับรายการใบเสนอราคาแล้ว</span><span class="sxs-lookup"><span data-stu-id="0e778-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="0e778-145">ยกเลิกการเชื่อมโยงงานจากรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e778-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="0e778-146">จากเพจโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e778-146">From the Project page</span></span>

<span data-ttu-id="0e778-147">วิธีการนี้มอบประสบการณ์ที่ดีที่สุดสำหรับการยกเลิกการเชื่อมโยงงานจากรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="0e778-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="0e778-148">คุณสามารถเลือกหลายงานและยกเลิกการเชื่อมโยงงานทั้งหมด รวมทั้งงานรองจากรายการใบเสนอราคาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0e778-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="0e778-149">บนแท็บ **ทั่วไป** ของรายการใบเสนอราคาตามโครงการ ในฟิลด์ **โครงการ** ให้เลือกลิงก์โครงการ</span><span class="sxs-lookup"><span data-stu-id="0e778-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="0e778-150">บนเพจ **โครงการ** เลือกแท็บ **การเรียกเก็บเงินงาน**</span><span class="sxs-lookup"><span data-stu-id="0e778-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="0e778-151">ในตารางที่สองซึ่งใช้กับการตั้งค่าการเรียกเก็บเงินเฉพาะงาน ให้เลือกงานอย่างน้อยหนึ่งงาน จากนั้นเลือก **ยกเลิกการเชื่อมโยงรายการใบเสนอราคา**</span><span class="sxs-lookup"><span data-stu-id="0e778-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="0e778-152">ในเพจกล่องโต้ตอบที่ปรากฏขึ้น ให้เลือกรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="0e778-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="0e778-153">เลือกกล่องกาเครื่องหมายเพื่อระบุว่าการเชื่อมโยงควรเอาออกจากงานย่อยของงานที่เลือกไว้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0e778-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="0e778-154">การทำเครื่องหมายในกล่องนี้จะยกเลิกการเชื่อมโยงงานย่อยของงานที่เลือกจากรายการใบเสนอราคาด้วย</span><span class="sxs-lookup"><span data-stu-id="0e778-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="0e778-155">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0e778-155">Select **OK**.</span></span> <span data-ttu-id="0e778-156">ข้อความเตือนแจ้งให้คุณทราบว่าหากคุณเอาการเชื่อมโยงนี้ออก ข้อมูลจริงที่บันทึกไว้ก่อนหน้านี้ในงานอาจถูกย้อนกลับได้</span><span class="sxs-lookup"><span data-stu-id="0e778-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="0e778-157">เลือก **ตกลง** เพื่อดำเนินการต่อและเอาการเชื่อมโยงระหว่างงานและรายการใบเสนอราคาตามโครงการออก</span><span class="sxs-lookup"><span data-stu-id="0e778-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="0e778-158">จากเพจรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="0e778-158">From the Quote line page</span></span>

<span data-ttu-id="0e778-159">คุณสามารถเชื่อมโยงงานโครงการกับรายการใบเสนอราคาจากแท็บ **งานที่คิดค่าธรรมเนียม** บนเพจ **รายการใบเสนอราคา**</span><span class="sxs-lookup"><span data-stu-id="0e778-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="0e778-160">บนแท็บ **งานที่คิดค่าธรรมเนียม** เลือก **ลบงานรายการใบเสนอราคา**</span><span class="sxs-lookup"><span data-stu-id="0e778-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="0e778-161">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0e778-161">Select **OK**.</span></span> <span data-ttu-id="0e778-162">ข้อความเตือนแจ้งให้คุณทราบว่าหากคุณเอาการเชื่อมโยงนี้ออก ข้อมูลจริงที่บันทึกไว้ก่อนหน้านี้ในงานอาจถูกย้อนกลับได้</span><span class="sxs-lookup"><span data-stu-id="0e778-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="0e778-163">เลือก **ตกลง** เพื่อดำเนินการต่อและเอาการเชื่อมโยงระหว่างงานและรายการใบเสนอราคาตามโครงการออก</span><span class="sxs-lookup"><span data-stu-id="0e778-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="0e778-164">ขั้นตอนนี้ไม่ได้ลบงานออกจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e778-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="0e778-165">แต่จะเอาการเชื่อมโยงงานออกจากรายการใบเสนอราคาตามโครงการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0e778-165">It only removes the task association from the project-based quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]