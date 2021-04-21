---
title: กำหนดค่าส่วนประกอบที่คิดค่าธรรมเนียมได้ของรายการใบเสนอราคา
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการตั้งค่าส่วนประกอบที่คิดค่าธรรมเนียมได้และไม่ได้ในรายการใบเสนอราคาตามโครงการ
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858316"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="fb1a9-103">กำหนดค่าส่วนประกอบที่เรียกเก็บเงินของรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="fb1a9-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="fb1a9-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว, Project Operations สำหรับสถานการณ์ตามทรัพยากร/สินค้าที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="fb1a9-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fb1a9-105">รายการใบเสนอราคาตามโครงการมีแนวคิดส่วนประกอบ *รวม* และส่วนประกอบ *คิดค่าธรรมเนียมได้*</span><span class="sxs-lookup"><span data-stu-id="fb1a9-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="fb1a9-106">ส่วนประกอบที่รวมอยู่ภายใต้:</span><span class="sxs-lookup"><span data-stu-id="fb1a9-106">Included components are subject to:</span></span>

  - <span data-ttu-id="fb1a9-107">วิธีการเรียกเก็บเงินและการแยกลูกค้า</span><span class="sxs-lookup"><span data-stu-id="fb1a9-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="fb1a9-108">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="fb1a9-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="fb1a9-109">การตั้งค่าความถี่ของใบแจ้งหนี้ที่กำหนดไว้ในรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="fb1a9-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="fb1a9-110">ชุดย่อยของส่วนประกอบที่รวมอยู่สามารถทำเครื่องหมายเป็นคิดค่าธรรมเนียมได้โดยใช้ฟิลด์ **ชนิดการเรียกเก็บเงิน**</span><span class="sxs-lookup"><span data-stu-id="fb1a9-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="fb1a9-111">ฟิลด์ **ชนิดการเรียกเก็บเงิน** คือชุดตัวเลือกที่อนุญาตให้ใช้ค่าต่อไปนี้ในบริบทของรายการใบเสนอราคา:</span><span class="sxs-lookup"><span data-stu-id="fb1a9-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="fb1a9-112">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-112">Chargeable</span></span>
  - <span data-ttu-id="fb1a9-113">คิดค่าธรรมเนียมไม่ได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-113">Non-chargeable</span></span>

<span data-ttu-id="fb1a9-114">ส่วนประกอบที่สามารถคิดค่าธรรมเนียมได้สามารถกำหนดได้ตามงาน บทบาท และประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="fb1a9-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="fb1a9-115">การคิดค่าธรรมเนียมถูกกำหนดไว้ในงานสำหรับรายการใบเสนอราคาและใช้กับคลาสธุรกรรมทั้งหมดที่รวมอยู่ในรายการนั้น</span><span class="sxs-lookup"><span data-stu-id="fb1a9-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="fb1a9-116">ถ้าฟิลด์ **รวมงาน** ถูกตั้งค่าเป็น **ทั้งโครงการ** หรือปล่อยว่าง **งานที่คิดค่าธรรมเนียมได้** จะไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="fb1a9-117">การคิดค่าธรรมเนียมที่กำหนดไว้สำหรับรายการใบเสนอราคาและจะใช้กับคลาสธุรกรรม **เวลา** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fb1a9-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="fb1a9-118">ถ้าฟิลด์ **รวมเวลา** ถูกตั้งค่าเป็น **ไม่** บนรายการใบเสนอราคาของโครงการ แท็บ **บทบาทที่คิดค่าธรรมเนียมได้** จะไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="fb1a9-119">การคิดค่าธรรมเนียมที่กำหนดไว้บนประเภทธุรกรรมสำหรับรายการใบเสนอราคาและจะใช้กับคลาสธุรกรรม **ค่าใช้จ่าย** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fb1a9-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="fb1a9-120">ถ้าฟิลด์ **รวมค่าใช้จ่าย** ถูกตั้งค่าเป็น **ไม่** บนรายการใบเสนอราคาของโครงการ แท็บ **ประเภทที่คิดค่าธรรมเนียมได้** จะไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="fb1a9-121">อัปเดตงานโครงการเป็นแบบคิดค่าธรรมเนียมได้หรือคิดค่าธรรมเนียมไม่ได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="fb1a9-122">งานโครงการสามารถคิดค่าธรรมเนียมได้หรือคิดค่าธรรมเนียมไม่ได้ในบริบทของรายการใบเสนอราคาตามโครงการเฉพาะ ซึ่งทำให้การตั้งค่าต่อไปนี้เป็นไปได้:</span><span class="sxs-lookup"><span data-stu-id="fb1a9-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="fb1a9-123">หากมีรายการใบเสนอราคาตามโครงการ **เวลา** และงาน **T1** งานนี้เชื่อมโยงกับรายการใบเสนอราคาที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="fb1a9-124">หากมีรายการใบเสนอราคาที่สองซึ่งรวมถึง **ค่าใช้จ่าย** คุณสามารถเชื่อมโยงงาน **T1** บนรายการใบเสนอราคาเป็นแบบไม่คิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="fb1a9-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="fb1a9-125">ผลที่ได้คือเวลาทั้งหมดที่บันทึกไว้ในงานนั้นสามารถคิดค่าธรรมเนียมได้และค่าใช้จ่ายทั้งหมดจะบันทึกบนงานเป็นไม่สามารถคิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="fb1a9-126">ชนิดการเรียกเก็บเงินของงานสามารถกำหนดค่าได้ในแท็บ **งานที่สามารถคิดค่าธรรมเนียมได้** ของรายการใบเสนอราคาตามโครงการโดยการอัปเดตฟิลด์ **ชนิดการเรียกเก็บเงิน** บนตารางย่อย **งานในรายการใบเสนอราคา**</span><span class="sxs-lookup"><span data-stu-id="fb1a9-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="fb1a9-127">หรือคุณสามารถอัปเดตชนิดการเรียกเก็บเงินสำหรับงานโครงการในฟิลด์ **ชนิดการเรียกเก็บเงิน** บนตารางย่อยในการตั้งค่าการเรียกเก็บเงินงานของโครงการที่แสดงรายการใบเสนอราคาที่เกี่ยวข้องกับงาน</span><span class="sxs-lookup"><span data-stu-id="fb1a9-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="fb1a9-128">อัปเดตบทบาทเป็นแบบคิดค่าธรรมเนียมได้หรือคิดค่าธรรมเนียมไม่ได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="fb1a9-129">บทบาทสามารถคิดค่าธรรมเนียมได้หรือไม่ได้ในบริบทของรายการใบเสนอราคาตามโครงการเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="fb1a9-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="fb1a9-130">ชนิดการเรียกเก็บเงินของบทบาทสามารถกำหนดค่าได้ในแท็บ **บทบาทที่สามารถคิดค่าธรรมเนียมได้** ของรายการใบเสนอราคาโดยการอัปเดตฟิลด์ **ชนิดการเรียกเก็บเงิน** บนตารางย่อย **บทบาทที่สามารถคิดค่าธรรมเนียมได้**</span><span class="sxs-lookup"><span data-stu-id="fb1a9-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="fb1a9-131">อัปเดตประเภทธุรกรรมเป็นแบบคิดค่าธรรมเนียมได้หรือคิดค่าธรรมเนียมไม่ได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="fb1a9-132">ประเภทธุรกรรมสามารถเป็นแบบคิดค่าธรรมเนียมได้หรือคิดค่าธรรมเนียมไม่ได้ในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="fb1a9-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="fb1a9-133">ชนิดการเรียกเก็บเงินของธุรกรรมสามารถกำหนดค่าได้ในแท็บ **ประเภทที่คิดค่าธรรมเนียมได้** ของรายการใบเสนอราคาโดยการอัปเดตฟิลด์ **ชนิดการเรียกเก็บเงิน** บนตารางย่อย **ประเภทที่คิดค่าธรรมเนียมได้**</span><span class="sxs-lookup"><span data-stu-id="fb1a9-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="fb1a9-134">แก้ไขการคิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="fb1a9-134">Resolve chargeability</span></span>
<span data-ttu-id="fb1a9-135">ประมาณการหรือข้อมูลจริงที่สร้างขึ้นสำหรับเวลาจะถือว่าสามารถคิดค่าธรรมเนียมได้ก็ต่อเมื่อ:</span><span class="sxs-lookup"><span data-stu-id="fb1a9-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="fb1a9-136">**เวลา** รวมอยู่ในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="fb1a9-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="fb1a9-137">**บทบาท** ได้รับการกำหนดค่าให้คิดค่าธรรมเนียมได้ในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="fb1a9-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="fb1a9-138">**งานที่รวมไว้** ตั้งค่าเป็น **งานที่เลือก** ในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="fb1a9-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="fb1a9-139">หากสามสิ่งเหล่านี้เป็นจริง จะมีการกำหนดค่า **งาน** เป็นแบบคิดค่าธรรมเนียมได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="fb1a9-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="fb1a9-140">ประมาณการหรือข้อมูลจริงที่สร้างขึ้นสำหรับค่าใช้จ่ายจะถือว่าสามารถคิดค่าธรรมเนียมได้ก็ต่อเมื่อ:</span><span class="sxs-lookup"><span data-stu-id="fb1a9-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="fb1a9-141">**ค่าใช้จ่าย** รวมอยู่ในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="fb1a9-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="fb1a9-142">**ประเภทธุรกรรม** ได้รับการกำหนดค่าให้คิดค่าธรรมเนียมได้ในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="fb1a9-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="fb1a9-143">**งานที่รวมไว้** ตั้งค่าเป็น **งานที่เลือก** ในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="fb1a9-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="fb1a9-144">หากสามสิ่งเหล่านี้เป็นจริง จะมีการกำหนดค่า **งาน** เป็นแบบคิดค่าธรรมเนียมได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="fb1a9-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="fb1a9-145">ประมาณการหรือข้อมูลจริงที่สร้างขึ้นสำหรับวัสดุจะถือว่าสามารถคิดค่าธรรมเนียมได้ก็ต่อเมื่อ:</span><span class="sxs-lookup"><span data-stu-id="fb1a9-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="fb1a9-146">**วัสดุ** รวมอยู่ในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="fb1a9-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="fb1a9-147">**งานที่รวมไว้** ตั้งค่าเป็น **งานที่เลือก** ในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="fb1a9-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="fb1a9-148">หากสองสิ่งเหล่านี้เป็นจริง ควรมีการกำหนดค่า **งาน** เป็นแบบคิดค่าธรรมเนียมได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="fb1a9-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="fb1a9-149">
                    <strong>รวมเวลา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="fb1a9-150">
                    <strong>รวมค่าใช้จ่าย</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="fb1a9-151">
                    <strong>รวมวัสดุ</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="fb1a9-152">
                    <strong>งานที่รวมไว้</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fb1a9-153">
                    <strong>บทบาท</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fb1a9-154">
                    <strong>ประเภท</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fb1a9-155">
                    <strong>งาน</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="fb1a9-156">
                    <strong>ผลกระทบของการคิดค่าธรรมเนียม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-157">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fb1a9-158">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fb1a9-159">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fb1a9-160">ทั้งโครงการ</span><span class="sxs-lookup"><span data-stu-id="fb1a9-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fb1a9-161">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-162">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fb1a9-163">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fb1a9-164">การเรียกเก็บเงินสำหรับเวลาจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fb1a9-165">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fb1a9-166">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-167">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fb1a9-168">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fb1a9-169">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fb1a9-170">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fb1a9-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fb1a9-171">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-172">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fb1a9-173">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fb1a9-174">การเรียกเก็บเงินสำหรับเวลาจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fb1a9-175">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fb1a9-176">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-177">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fb1a9-178">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fb1a9-179">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fb1a9-180">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fb1a9-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fb1a9-181">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-182">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fb1a9-183">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fb1a9-184">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fb1a9-185">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fb1a9-186">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-187">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fb1a9-188">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fb1a9-189">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fb1a9-190">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fb1a9-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fb1a9-191">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-192">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fb1a9-193">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fb1a9-194">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fb1a9-195">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fb1a9-196">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-197">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fb1a9-198">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fb1a9-199">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fb1a9-200">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fb1a9-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fb1a9-201">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-202">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fb1a9-203">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fb1a9-204">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fb1a9-205">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fb1a9-206">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-207">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fb1a9-208">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fb1a9-209">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fb1a9-210">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fb1a9-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fb1a9-211">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fb1a9-212">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fb1a9-213">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fb1a9-214">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fb1a9-215">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fb1a9-216">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="fb1a9-217">
                    <strong>ไม่</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fb1a9-218">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fb1a9-219">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fb1a9-220">ทั้งโครงการ</span><span class="sxs-lookup"><span data-stu-id="fb1a9-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fb1a9-221">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fb1a9-222">
                    <strong>คิดค่าธรรมเนียมได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fb1a9-223">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fb1a9-224">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>ไม่พร้อมใช้งาน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fb1a9-225">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fb1a9-226">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="fb1a9-227">
                    <strong>ไม่</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fb1a9-228">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fb1a9-229">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fb1a9-230">ทั้งโครงการ</span><span class="sxs-lookup"><span data-stu-id="fb1a9-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fb1a9-231">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fb1a9-232">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fb1a9-233">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fb1a9-234">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>ไม่พร้อมใช้งาน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fb1a9-235">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fb1a9-236">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-237">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="fb1a9-238">
                    <strong>ไม่</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fb1a9-239">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fb1a9-240">ทั้งโครงการ</span><span class="sxs-lookup"><span data-stu-id="fb1a9-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fb1a9-241">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-242">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fb1a9-243">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fb1a9-244">การเรียกเก็บเงินสำหรับเวลาจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fb1a9-245">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง:<strong> ไม่พร้อมใช้งาน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fb1a9-246">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-247">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="fb1a9-248">
                    <strong>ไม่</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fb1a9-249">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fb1a9-250">ทั้งโครงการ</span><span class="sxs-lookup"><span data-stu-id="fb1a9-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fb1a9-251">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-252">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fb1a9-253">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fb1a9-254">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="fb1a9-255">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง:<strong> ไม่พร้อมใช้งาน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fb1a9-256">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-257">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fb1a9-258">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="fb1a9-259">
                    <strong>ไม่</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fb1a9-260">ทั้งโครงการ</span><span class="sxs-lookup"><span data-stu-id="fb1a9-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fb1a9-261">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-262">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fb1a9-263">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fb1a9-264">การเรียกเก็บเงินสำหรับเวลาจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fb1a9-265">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fb1a9-266">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: <strong>ไม่พร้อมใช้งาน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fb1a9-267">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fb1a9-268">ใช่</span><span class="sxs-lookup"><span data-stu-id="fb1a9-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="fb1a9-269">
                    <strong>ไม่</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fb1a9-270">ทั้งโครงการ</span><span class="sxs-lookup"><span data-stu-id="fb1a9-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fb1a9-271">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fb1a9-272">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fb1a9-273">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="fb1a9-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fb1a9-274">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="fb1a9-275">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง:<strong> คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="fb1a9-276">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง:<strong> ไม่พร้อมใช้งาน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb1a9-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
