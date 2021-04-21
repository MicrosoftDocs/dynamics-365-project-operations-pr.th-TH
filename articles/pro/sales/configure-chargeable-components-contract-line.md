---
title: กำหนดค่าส่วนประกอบที่คิดค่าบริการของรายละเอียดการให้บริการตามสัญญาตามโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการเพิ่มส่วนประกอบคิดค่าธรรมเนียมได้ลงในรายละเอียดการให้บริการตามสัญญาใน Project Operations
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858496"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="44642-103">กำหนดค่าส่วนประกอบที่คิดค่าบริการของรายละเอียดการให้บริการตามสัญญาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="44642-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="44642-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว, Project Operations สำหรับสถานการณ์ตามทรัพยากร/สินค้าที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="44642-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="44642-105">รายละเอียดการให้บริการตามสัญญาตามโครงการมีส่วนประกอบ *รวม* และส่วนประกอบ *คิดค่าธรรมเนียมได้*</span><span class="sxs-lookup"><span data-stu-id="44642-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="44642-106">ส่วนประกอบที่รวมเป็นส่วนประกอบที่อยู่ภายใต้:</span><span class="sxs-lookup"><span data-stu-id="44642-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="44642-107">วิธีการเรียกเก็บเงินและการแยกลูกค้า</span><span class="sxs-lookup"><span data-stu-id="44642-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="44642-108">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="44642-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="44642-109">การตั้งค่าความถี่ของใบแจ้งหนี้ที่กำหนดไว้ในรายละเอียดการให้บริการตามสัญญาของโครงการ</span><span class="sxs-lookup"><span data-stu-id="44642-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="44642-110">ชุดย่อยของส่วนประกอบที่รวมอยู่สามารถทำเครื่องหมายเป็นคิดค่าธรรมเนียมได้โดยใช้ฟิลด์ **ชนิดการเรียกเก็บเงิน**</span><span class="sxs-lookup"><span data-stu-id="44642-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="44642-111">ฟิลด์ **ชนิดการเรียกเก็บเงิน** คือชุดตัวเลือกที่อนุญาตให้ใช้ค่าต่อไปนี้ในบริบทของรายละเอียดการให้บริการตามสัญญา:</span><span class="sxs-lookup"><span data-stu-id="44642-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="44642-112">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-112">Chargeable</span></span>
  - <span data-ttu-id="44642-113">คิดค่าธรรมเนียมไม่ได้</span><span class="sxs-lookup"><span data-stu-id="44642-113">Non-chargeable</span></span>

<span data-ttu-id="44642-114">ส่วนประกอบที่สามารถคิดค่าธรรมเนียมได้สามารถกำหนดได้ตามงาน บทบาท และประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="44642-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="44642-115">การคิดค่าธรรมเนียมถูกกำหนดไว้ในงานสำหรับรายละเอียดการให้บริการตามสัญญาโครงการและใช้กับคลาสธุรกรรมทั้งหมดที่รวมอยู่ในรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="44642-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="44642-116">ถ้าฟิลด์ **รวมงาน** บนรายละเอียดการให้บริการตามสัญญาว่างเปล่า หรือถูกตั้งค่าเป็น **ทั้งโครงการ** แท็บ **งานที่คิดค่าธรรมเนียมได้** จะไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="44642-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="44642-117">การคิดค่าธรรมเนียมที่กำหนดไว้สำหรับรายละเอียดการให้บริการตามสัญญาของโครงการจะใช้กับคลาสธุรกรรม **เวลา** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="44642-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="44642-118">ถ้าฟิลด์ **รวมเวลา** บนรายละเอียดการให้บริการตามสัญญาตั้งค่าเป็น **ไม่** แท็บ **บทบาทที่คิดค่าธรรมเนียมได้** จะไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="44642-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="44642-119">การคิดค่าธรรมเนียมที่กำหนดไว้บนประเภทธุรกรรมสำหรับรายละเอียดการให้บริการตามสัญญาของโครงการจะใช้กับคลาสธุรกรรม **ค่าใช้จ่าย** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="44642-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="44642-120">ถ้าฟิลด์ **รวมค่าใช้จ่าย** ตั้งค่าเป็น **ไม่** แท็บ **ประเภทที่คิดค่าธรรมเนียมได้** จะไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="44642-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="44642-121">อัปเดตงานโครงการเป็นแบบคิดค่าธรรมเนียมได้หรือคิดค่าธรรมเนียมไม่ได้</span><span class="sxs-lookup"><span data-stu-id="44642-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="44642-122">งานโครงการสามารถคิดค่าธรรมเนียมได้หรือคิดค่าธรรมเนียมไม่ได้ในรายละเอียดการให้บริการตามสัญญาเฉพาะ ซึ่งทำให้การตั้งค่าต่อไปนี้เป็นไปได้:</span><span class="sxs-lookup"><span data-stu-id="44642-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="44642-123">หากรายละเอียดการให้บริการตามสัญญามี **เวลา** และงานบางอย่าง **T1** จะเกี่ยวข้องกับโดยเป็นแบบคิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="44642-124">หากมีรายละเอียดการให้บริการตามสัญญาซึ่งรวมถึง **ค่าใช้จ่าย** คุณสามารถเชื่อมโยงงาน T1 บนรายละเอียดการให้บริการตามสัญญาเป็นแบบไม่คิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="44642-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="44642-125">ผลที่ได้คือเวลาทั้งหมดที่บันทึกไว้ในงานนั้นสามารถคิดค่าธรรมเนียมได้และค่าใช้จ่ายทั้งหมดจะไม่สามารถคิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="44642-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="44642-126">ชนิดการเรียกเก็บเงินของงานสามารถกำหนดค่าได้ในแท็บ **งานที่สามารถคิดค่าธรรมเนียมได้** ของรายละเอียดการให้บริการตามสัญญาโดยการอัปเดตฟิลด์ **ชนิดการเรียกเก็บเงิน** บนตารางย่อยงานในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="44642-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="44642-127">หรือคุณสามารถอัปเดตฟิลด์ **ชนิดการเรียกเก็บเงิน** บนตารางย่อยของการตั้งค่าการเรียกเก็บเงินงานของโครงการที่แสดงรายละเอียดการให้บริการตามสัญญาที่เกี่ยวข้องกับงาน</span><span class="sxs-lookup"><span data-stu-id="44642-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="44642-128">อัปเดตบทบาทเป็นแบบคิดค่าธรรมเนียมได้หรือคิดค่าธรรมเนียมไม่ได้</span><span class="sxs-lookup"><span data-stu-id="44642-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="44642-129">บทบาทสามารถเป็นแบบคิดค่าธรรมเนียมได้หรือคิดค่าธรรมเนียมไม่ได้ในรายละเอียดการให้บริการตามสัญญาเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="44642-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="44642-130">ชนิดการเรียกเก็บเงินของบทบาทสามารถกำหนดค่าได้ในแท็บ **บทบาทที่คิดค่าธรรมเนียมได้** ของรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="44642-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="44642-131">ในการดำเนินการนี้ ให้อัปเดตฟิลด์ **ชนิดการเรียกเก็บเงิน** บนตารางย่อย **บทบาทที่คิดค่าธรรมเนียมได้**</span><span class="sxs-lookup"><span data-stu-id="44642-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="44642-132">อัปเดตประเภทธุรกรรมเป็นแบบคิดค่าธรรมเนียมได้หรือคิดค่าธรรมเนียมไม่ได้</span><span class="sxs-lookup"><span data-stu-id="44642-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="44642-133">ประเภทธุรกรรมสามารถเป็นแบบคิดค่าธรรมเนียมได้หรือคิดค่าธรรมเนียมไม่ได้ในรายละเอียดการให้บริการตามสัญญาเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="44642-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="44642-134">ชนิดการเรียกเก็บเงินของธุรกรรมสามารถกำหนดค่าได้ในแท็บ **ประเภทที่คิดค่าธรรมเนียมได้** ของรายละเอียดการให้บริการตามสัญญาของโครงการ</span><span class="sxs-lookup"><span data-stu-id="44642-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="44642-135">ในการดำเนินการนี้ ให้อัปเดตฟิลด์ **ชนิดการเรียกเก็บเงิน** บนตารางย่อย **ประเภทที่คิดค่าธรรมเนียมได้**</span><span class="sxs-lookup"><span data-stu-id="44642-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="44642-136">แก้ไขการคิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="44642-136">Resolve chargeability</span></span>

<span data-ttu-id="44642-137">ประมาณการหรือข้อมูลจริงที่สร้างขึ้นสำหรับเวลาจะถือว่าสามารถคิดค่าธรรมเนียมได้ก็ต่อเมื่อ:</span><span class="sxs-lookup"><span data-stu-id="44642-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="44642-138">**เวลา** รวมอยู่ในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="44642-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="44642-139">**บทบาท** ได้รับการกำหนดค่าให้คิดค่าธรรมเนียมได้ในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="44642-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="44642-140">**งานที่รวมไว้** ตั้งค่าเป็น **งานที่เลือก** ในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="44642-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="44642-141">หากสามสิ่งเหล่านี้เป็นจริง จะมีการกำหนดค่างานเป็นแบบคิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="44642-142">ประมาณการหรือข้อมูลจริงที่สร้างขึ้นสำหรับค่าใช้จ่ายจะถือว่าสามารถคิดค่าธรรมเนียมได้ก็ต่อเมื่อ:</span><span class="sxs-lookup"><span data-stu-id="44642-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="44642-143">**ค่าใช้จ่าย** รวมอยู่ในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="44642-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="44642-144">**ประเภทธุรกรรม** ได้รับการกำหนดค่าให้คิดค่าธรรมเนียมได้ในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="44642-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="44642-145">**งานที่รวมไว้** ตั้งค่าเป็น **งานที่เลือก** ในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="44642-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="44642-146">หากสามสิ่งเหล่านี้เป็นจริง จะมีการกำหนดค่า **งาน** เป็นแบบคิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="44642-147">ประมาณการหรือข้อมูลจริงที่สร้างขึ้นสำหรับวัสดุจะถือว่าสามารถคิดค่าธรรมเนียมได้ก็ต่อเมื่อ:</span><span class="sxs-lookup"><span data-stu-id="44642-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="44642-148">**วัสดุ** รวมอยู่ในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="44642-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="44642-149">**งานที่รวมไว้** ตั้งค่าเป็น **งานที่เลือก** ในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="44642-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="44642-150">หากสองสิ่งเหล่านี้เป็นจริง จะมีการกำหนดค่า **งาน** เป็นแบบคิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="44642-151">
                    <strong>รวมเวลา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="44642-152">
                    <strong>รวมค่าใช้จ่าย</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="44642-153">
                    <strong>รวมวัสดุ</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="44642-154">
                    <strong>งานที่รวมไว้</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="44642-155">
                    <strong>บทบาท</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="44642-156">
                    <strong>ประเภท</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="44642-157">
                    <strong>งาน</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="44642-158">
                    <strong>ผลกระทบของการคิดค่าธรรมเนียม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-159">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="44642-160">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="44642-161">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="44642-162">ทั้งโครงการ</span><span class="sxs-lookup"><span data-stu-id="44642-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="44642-163">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-164">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="44642-165">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="44642-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="44642-166">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>คิดค่าธรรมเนียมได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-167">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: <strong>คิดค่าธรรมเนียมได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-168">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: <strong>คิดค่าธรรมเนียมได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-169">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="44642-170">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="44642-171">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="44642-172">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="44642-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="44642-173">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-174">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="44642-175">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="44642-176">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>คิดค่าธรรมเนียมได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-177">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: <strong>คิดค่าธรรมเนียมได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-178">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: <strong>คิดค่าธรรมเนียมได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-179">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="44642-180">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="44642-181">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="44642-182">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="44642-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="44642-183">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-184">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="44642-185">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="44642-186">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-187">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="44642-188">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-189">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="44642-190">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="44642-191">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="44642-192">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="44642-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="44642-193">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-194">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="44642-195">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="44642-196">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-197">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-198">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-199">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="44642-200">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="44642-201">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="44642-202">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="44642-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="44642-203">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-204">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="44642-205">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="44642-206">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-207">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-208">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-209">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="44642-210">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="44642-211">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="44642-212">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="44642-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="44642-213">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="44642-214">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="44642-215">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="44642-216">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-217">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-218">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="44642-219">
                    <strong>ไม่</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="44642-220">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="44642-221">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="44642-222">ทั้งโครงการ</span><span class="sxs-lookup"><span data-stu-id="44642-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="44642-223">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="44642-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="44642-224">
                    <strong>คิดค่าธรรมเนียมได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="44642-225">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="44642-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="44642-226">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>ไม่พร้อมใช้งาน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-227">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="44642-228">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="44642-229">
                    <strong>ไม่</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="44642-230">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="44642-231">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="44642-232">ทั้งโครงการ</span><span class="sxs-lookup"><span data-stu-id="44642-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="44642-233">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="44642-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="44642-234">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="44642-235">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="44642-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="44642-236">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>ไม่พร้อมใช้งาน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-237">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-238">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-239">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="44642-240">
                    <strong>ไม่</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="44642-241">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="44642-242">ทั้งโครงการ</span><span class="sxs-lookup"><span data-stu-id="44642-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="44642-243">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-244">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="44642-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="44642-245">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="44642-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="44642-246">การเรียกเก็บเงินสำหรับเวลาจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="44642-247">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง:<strong> ไม่พร้อมใช้งาน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-248">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-249">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="44642-250">
                    <strong>ไม่</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="44642-251">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="44642-252">ทั้งโครงการ</span><span class="sxs-lookup"><span data-stu-id="44642-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="44642-253">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-254">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="44642-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="44642-255">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="44642-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="44642-256">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-257">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง:<strong> ไม่พร้อมใช้งาน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-258">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-259">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="44642-260">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="44642-261">
                    <strong>ไม่</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="44642-262">ทั้งโครงการ</span><span class="sxs-lookup"><span data-stu-id="44642-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="44642-263">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-264">คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="44642-265">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="44642-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="44642-266">การเรียกเก็บเงินสำหรับเวลาจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="44642-267">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง: คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="44642-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="44642-268">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง: <strong>ไม่พร้อมใช้งาน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="44642-269">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="44642-270">ใช่</span><span class="sxs-lookup"><span data-stu-id="44642-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="44642-271">
                    <strong>ไม่</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="44642-272">ทั้งโครงการ</span><span class="sxs-lookup"><span data-stu-id="44642-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="44642-273">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="44642-274">
                    <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="44642-275">ไม่สามารถตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="44642-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="44642-276">การเรียกเก็บเงินสำหรับเวลาจริง: <strong>คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-277">ชนิดการเรียกเก็บเงินสำหรับค่าใช้จ่ายจริง:<strong> คิดค่าธรรมเนียมไม่ได้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="44642-278">ชนิดการเรียกเก็บเงินสำหรับวัสดุจริง:<strong> ไม่พร้อมใช้งาน</strong>
                </span><span class="sxs-lookup"><span data-stu-id="44642-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
