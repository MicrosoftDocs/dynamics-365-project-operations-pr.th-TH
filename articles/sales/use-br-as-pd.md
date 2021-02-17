---
title: ใช้ทรัพยากรที่สามารถจองได้เป็นมิติการกำหนดราคา
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ทรัพยากรที่จองได้เป็นมิติการกำหนดราคา
author: Rumant
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b0c5cb85f7c43f7b2fd9c367d7f7ac9c3250e0a1
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643106"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a><span data-ttu-id="bc9fb-103">ใช้ทรัพยากรที่สามารถจองได้เป็นมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="bc9fb-103">Use a bookable resource as a pricing dimension</span></span>

 <span data-ttu-id="bc9fb-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="bc9fb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

<span data-ttu-id="bc9fb-105">หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ทรัพยากรที่จองได้เป็นมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="bc9fb-105">This topic provides information about how to use a bookable resource as a pricing dimension.</span></span> <span data-ttu-id="bc9fb-106">หากกลยุทธ์การกำหนดราคาของคุณตั้งค่าเพื่อให้ทรัพยากรที่สามารถจองได้แต่ละรายการต้องมีราคาหรืออัตราต้นทุนที่เฉพาะเจาะจง ให้ใช้ทรัพยากรที่สามารถจองได้เป็นมิติข้อมูลการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="bc9fb-106">If your pricing strategy is set up so that each bookable resource must have a specific price or cost rate, use a bookable resource as a pricing dimension.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bc9fb-107">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="bc9fb-107">Prerequisites</span></span>
<span data-ttu-id="bc9fb-108">ก่อนที่คุณจะทำตามขั้นตอนในหัวข้อนี้ คุณต้องมีโซลูชันมิติการกำหนดราคาใหม่สำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="bc9fb-108">Before you complete the procedures in this topic, you must have a new pricing dimension solution for your organization.</span></span> <span data-ttu-id="bc9fb-109">หากคุณยังไม่ได้สร้าง ดูที่ [สร้างฟิลด์และเอนทิตีแบบกำหนดเอง](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md)</span><span class="sxs-lookup"><span data-stu-id="bc9fb-109">If you haven't already created one, see [Create custom fields and entities](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).</span></span>

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a><span data-ttu-id="bc9fb-110">เพิ่มฟิลด์ทรัพยากรที่สามารถจองได้ในฟอร์มและมุมมอง</span><span class="sxs-lookup"><span data-stu-id="bc9fb-110">Add the Bookable Resource field to forms and views</span></span>
<span data-ttu-id="bc9fb-111">เพื่อให้ฟิลด์ **ทรัพยากรที่สามารถจองได้** มองเห็นได้ในโซลูชันมิติการกำหนดราคา คุณต้องเพิ่มฟิลด์ลงในฟอร์มและมุมมองทั้งหมดเป็นเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="bc9fb-111">To make the **Bookable Resource** field visible in the pricing dimension solution, you need to add the field to all the forms and views as an entity.</span></span>

<span data-ttu-id="bc9fb-112">ตารางต่อไปนี้แสดงรายการฟอร์มและมุมมองแบบสำเร็จรูปทั้งหมด ตามเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="bc9fb-112">The following table lists all of the out-of-the box forms and views, by entity.</span></span> <span data-ttu-id="bc9fb-113">คุณจะต้องเพิ่มฟิลด์ใหม่ลงในฟอร์มหรือมุมมองเพิ่มเติมในเอนทิตีที่กำหนดเองของคุณ</span><span class="sxs-lookup"><span data-stu-id="bc9fb-113">You will also need to add the new field to any additional forms or views in your customized entities.</span></span>

|   <span data-ttu-id="bc9fb-114">Entity</span><span class="sxs-lookup"><span data-stu-id="bc9fb-114">Entity</span></span>        | <span data-ttu-id="bc9fb-115">ฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="bc9fb-115">Forms</span></span>   |<span data-ttu-id="bc9fb-116">มุมมอง</span><span class="sxs-lookup"><span data-stu-id="bc9fb-116">Views</span></span>        |
| ------------------------------|---------------------------------|----------------------------------|
|  <span data-ttu-id="bc9fb-117">ราคาตามบทบาท</span><span class="sxs-lookup"><span data-stu-id="bc9fb-117">Role Price</span></span>| <span data-ttu-id="bc9fb-118">ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bc9fb-118">Information</span></span> | <span data-ttu-id="bc9fb-119">- ราคาของประเภททรัพยากรที่ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bc9fb-119">- Active Resource Category Prices</span></span><br> <span data-ttu-id="bc9fb-120">- ราคาประเภททรัพยากรร่วม</span><span class="sxs-lookup"><span data-stu-id="bc9fb-120">- Resource Category Price Associated</span></span> |
|  <span data-ttu-id="bc9fb-121">ส่วนเพิ่มราคาของราคาตามบทบาท</span><span class="sxs-lookup"><span data-stu-id="bc9fb-121">Role Price Markup</span></span>| <span data-ttu-id="bc9fb-122">ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bc9fb-122">Information</span></span>| <span data-ttu-id="bc9fb-123">- ส่วนเพิ่มราคาของราคาตามบทบาทที่ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bc9fb-123">- Active Role Price Markup</span></span><br><span data-ttu-id="bc9fb-124">- ส่วนเพิ่มราคาสำหรับราคาตามบทบาทร่วม</span><span class="sxs-lookup"><span data-stu-id="bc9fb-124">- Role Price Markup Associated</span></span> |
|  <span data-ttu-id="bc9fb-125">รายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="bc9fb-125">Quote line detail</span></span>| <span data-ttu-id="bc9fb-126">- ข้อมูลโครงการ</span><span class="sxs-lookup"><span data-stu-id="bc9fb-126">- Project Information</span></span><br><span data-ttu-id="bc9fb-127">- การสร้างโครงการแบบด่วน</span><span class="sxs-lookup"><span data-stu-id="bc9fb-127">- Project Quick Create</span></span>| <span data-ttu-id="bc9fb-128">- รายละเอียดรายการใบเสนอราคาที่ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bc9fb-128">- Active Quote Line Detail</span></span><br><span data-ttu-id="bc9fb-129">- รายละเอียดรายการใบเสนอราคาแบบรวม</span><span class="sxs-lookup"><span data-stu-id="bc9fb-129">- Combined Quote Line Details</span></span><br><span data-ttu-id="bc9fb-130">- รายละเอียดบรรทัดใบเสนอราคาร่วม</span><span class="sxs-lookup"><span data-stu-id="bc9fb-130">- Quote Line Detail Associated</span></span> |
|  <span data-ttu-id="bc9fb-131">รายการรายละเอียดการให้บริการตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="bc9fb-131">Project Contract line detail</span></span>| <span data-ttu-id="bc9fb-132">- ข้อมูลโครงการ</span><span class="sxs-lookup"><span data-stu-id="bc9fb-132">- Project Information</span></span><br><span data-ttu-id="bc9fb-133">- การสร้างโครงการแบบด่วน</span><span class="sxs-lookup"><span data-stu-id="bc9fb-133">- Project Quick Create</span></span>| <span data-ttu-id="bc9fb-134">- รายละเอียดที่เป็นรายละเอียดการให้บริการตามสัญญาของโครงการแบบรวม</span><span class="sxs-lookup"><span data-stu-id="bc9fb-134">- Combined Contract Line Details</span></span><br><span data-ttu-id="bc9fb-135">- รายละเอียดที่เป็นรายละเอียดการให้บริการตามสัญญาของโครงการที่ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bc9fb-135">- Active Contract Line Details</span></span><br><span data-ttu-id="bc9fb-136">- รายละเอียดที่เป็นรายละเอียดการให้บริการตามสัญญาร่วม</span><span class="sxs-lookup"><span data-stu-id="bc9fb-136">- Contract Line Detail Associated</span></span> |
|  <span data-ttu-id="bc9fb-137">งานโครงการ</span><span class="sxs-lookup"><span data-stu-id="bc9fb-137">Project Task</span></span>| <span data-ttu-id="bc9fb-138">- ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bc9fb-138">- Information</span></span><br><span data-ttu-id="bc9fb-139">- ฟอร์มใหม่</span><span class="sxs-lookup"><span data-stu-id="bc9fb-139">- New Form</span></span>| &nbsp; |
|  <span data-ttu-id="bc9fb-140">สมาชิกของทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="bc9fb-140">Project Team Member</span></span>| <span data-ttu-id="bc9fb-141">- ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bc9fb-141">- Information</span></span><br><span data-ttu-id="bc9fb-142">- ฟอร์มใหม่</span><span class="sxs-lookup"><span data-stu-id="bc9fb-142">- New Form</span></span>| <span data-ttu-id="bc9fb-143">- สมาชิกทีมโครงการที่ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bc9fb-143">- Active Project Team Members</span></span><br><span data-ttu-id="bc9fb-144">- สมาชิกของทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="bc9fb-144">- Project Team Members</span></span><br><span data-ttu-id="bc9fb-145">- สมาชิกทีมโครงการที่เชื่อมโยงแล้ว</span><span class="sxs-lookup"><span data-stu-id="bc9fb-145">- Project Team members Associated</span></span> |
|  <span data-ttu-id="bc9fb-146">รายการเวลา</span><span class="sxs-lookup"><span data-stu-id="bc9fb-146">Time Entry</span></span>| <span data-ttu-id="bc9fb-147">- ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bc9fb-147">- Information</span></span><br><span data-ttu-id="bc9fb-148">- สร้างรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="bc9fb-148">- Create Time Entry</span></span>| <span data-ttu-id="bc9fb-149">- รายการเวลาของฉันตามวันที่</span><span class="sxs-lookup"><span data-stu-id="bc9fb-149">- My Time Entries By Date</span></span><br><span data-ttu-id="bc9fb-150">- รายการเวลาของฉันสำหรับสัปดาห์นี้</span><span class="sxs-lookup"><span data-stu-id="bc9fb-150">- My Time Entries for this Week</span></span><br><span data-ttu-id="bc9fb-151">- รายการเวลาสำหรับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="bc9fb-151">- Time Entries for Approval</span></span>|
|  <span data-ttu-id="bc9fb-152">รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="bc9fb-152">Journal Line</span></span>| <span data-ttu-id="bc9fb-153">- ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bc9fb-153">- Information</span></span><br><span data-ttu-id="bc9fb-154">- การสร้างด่วน</span><span class="sxs-lookup"><span data-stu-id="bc9fb-154">- Quick Create</span></span>| <span data-ttu-id="bc9fb-155">- รายการสมุดรายวันที่ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bc9fb-155">- Active Journal Lines</span></span><br><span data-ttu-id="bc9fb-156">- บรรทัดสมุดรายวันร่วม</span><span class="sxs-lookup"><span data-stu-id="bc9fb-156">- Journal Line Associated</span></span> |
|  <span data-ttu-id="bc9fb-157">รายละเอียดรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="bc9fb-157">Invoice Line Detail</span></span>| <span data-ttu-id="bc9fb-158">- ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bc9fb-158">- Information</span></span><br><span data-ttu-id="bc9fb-159">- การสร้างด่วน</span><span class="sxs-lookup"><span data-stu-id="bc9fb-159">- Quick Create</span></span>| <span data-ttu-id="bc9fb-160">- รายละเอียดรายการใบแจ้งหนี้ที่ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bc9fb-160">- Active Invoice Line Details</span></span><br><span data-ttu-id="bc9fb-161">- ธุรกรรมใบแจ้งหนี้ที่คิดค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="bc9fb-161">- Chargeable Invoice Transactions</span></span><br><span data-ttu-id="bc9fb-162">- ธุรกรรมใบแจ้งหนี้ส่วนเสริม</span><span class="sxs-lookup"><span data-stu-id="bc9fb-162">- Complimentary Invoice Transactions</span></span><br><span data-ttu-id="bc9fb-163">- รายละเอียดบรรทัดใบแจ้งหนี้ร่วม</span><span class="sxs-lookup"><span data-stu-id="bc9fb-163">- Invoice Line Detail Associated</span></span> <br><span data-ttu-id="bc9fb-164">- ธุรกรรมใบแจ้งหนี้ที่คิดค่าธรรมเนียมไม่ได้</span><span class="sxs-lookup"><span data-stu-id="bc9fb-164">- Non-Chargeable Invoice Transactions</span></span>|
|  <span data-ttu-id="bc9fb-165">เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="bc9fb-165">Actual</span></span>| <span data-ttu-id="bc9fb-166">- ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bc9fb-166">- Information</span></span><br><span data-ttu-id="bc9fb-167">- ข้อมูลจริงที่ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bc9fb-167">- Active Actuals</span></span>| <span data-ttu-id="bc9fb-168">ข้อมูลจริงร่วม</span><span class="sxs-lookup"><span data-stu-id="bc9fb-168">Actual Associated</span></span> |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a><span data-ttu-id="bc9fb-169">ตั้งค่าทรัพยากรที่สามารถจองได้เป็นมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="bc9fb-169">Set up a bookable resource as a pricing dimension</span></span>
<span data-ttu-id="bc9fb-170">หากต้องการตั้งค่าทรัพยากรที่สามารถจองได้เป็นมิติการกำหนดราคา ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bc9fb-170">To set up a bookable resource as a pricing dimension, follow these steps:</span></span>

1. <span data-ttu-id="bc9fb-171">ไปที่ **การตั้งค่า** > **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="bc9fb-171">Go to **Settings** > **Parameters**.</span></span> 
2. <span data-ttu-id="bc9fb-172">บนเพจ **พารามิเตอร์** บนแท็บ **มิติการกำหนดราคาตามจำนวนเงิน** ตรวจสอบให้แน่ใจว่ากริดแสดงเรกคอร์ดในเอนทิตี **มิติการกำหนดราคา**</span><span class="sxs-lookup"><span data-stu-id="bc9fb-172">On the **Parameter** page, on the **Amount-Based Pricing Dimensions** tab, verify that the grid shows the records in the **Pricing Dimensions** entity.</span></span> 
2. <span data-ttu-id="bc9fb-173">เพิ่ม **ทรัพยากรที่สามารถจองได้** ไปยังรายการของมิติการกำหนดราคาเป็น **msdyn_bookableresource**</span><span class="sxs-lookup"><span data-stu-id="bc9fb-173">Add **Bookable Resource** to this list of pricing dimensions as **msdyn_bookableresource**.</span></span> 
3. <span data-ttu-id="bc9fb-174">ใน **ใช้ได้กับต้นทุน** และ **ใช้ได้กับการขาย** เลือกค่า</span><span class="sxs-lookup"><span data-stu-id="bc9fb-174">In **Applicable to cost** and **Applicable to sales**, select a value.</span></span>
4. <span data-ttu-id="bc9fb-175">ใน **ชนิดมิติ** ให้เลือก **ตามจำนวนเงิน**</span><span class="sxs-lookup"><span data-stu-id="bc9fb-175">In **Dimension Type**, select **Amount-based**.</span></span> 
5. <span data-ttu-id="bc9fb-176">เลือกต้นทุนและระดับความสำคัญของการขายสำหรับทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="bc9fb-176">Select the cost and sales priority for the bookable resource.</span></span> <span data-ttu-id="bc9fb-177">โดยทั่วไป ทรัพยากรที่สามารถจองได้จะมีลำดับความสำคัญสูงสุดเมื่อรวมเป็นมิติข้อมูลการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="bc9fb-177">Typically, a bookable resource has the highest priority when included as a pricing dimension.</span></span> <span data-ttu-id="bc9fb-178">ตั้งค่าลำดับความสำคัญเป็น **1** (หรือ **0** ขึ้นอยู่กับว่าคุณนับลำดับความสำคัญอย่างไร) เพื่อให้แน่ใจลักษณะการทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="bc9fb-178">Set the priority to **1** (or **0** depending on how you count the priority) to ensure this behavior.</span></span>

## <a name="set-up-pricing-dimension-field-names"></a><span data-ttu-id="bc9fb-179">ตั้งค่าชื่อฟิลด์มิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="bc9fb-179">Set up pricing dimension field names</span></span>

<span data-ttu-id="bc9fb-180">เมื่อชื่อฟิลด์ของมิติการกำหนดราคาในตาราง **ราคาตามบทบาท** แตกต่างจากชื่อฟิลด์ในเอนทิตีอื่นๆ ที่ใช้การกำหนดค่าเริ่มต้นของราคา มิติการกำหนดราคาจะต้องทราบถึงชื่อที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="bc9fb-180">When the field name of a pricing dimension in the **Role Price** table is different from the field name in any of the other entities where the default price is used, the pricing dimension record must be notified of the different names.</span></span>  

<span data-ttu-id="bc9fb-181">สำหรับทรัพยากรที่สามารถจองได้ เอนทิตี **สมาชิกของทีมโครงการ** จะมีชื่อฟิลด์ที่แตกต่างเล็กน้อยจากสิ่งที่ถูกเรียกบนเอนทิตี **ราคาตามบทบาท** :</span><span class="sxs-lookup"><span data-stu-id="bc9fb-181">For a bookable resource, the **Project Team Members** entity has a slightly different field name from what it is called on the **Role Price** entity:</span></span> 

 - <span data-ttu-id="bc9fb-182">เอนทิตี **สมาชิกในทีมโครงการ** = **msdyn_bookableresourceid**</span><span class="sxs-lookup"><span data-stu-id="bc9fb-182">**Project Team Members** entity = **msdyn_bookableresourceid**</span></span>
 - <span data-ttu-id="bc9fb-183">เอนทิตี **ราคาตามบทบาท** = **msdyn_bookableresource**</span><span class="sxs-lookup"><span data-stu-id="bc9fb-183">**Role Price** entity = **msdyn_bookableresource**</span></span>

<span data-ttu-id="bc9fb-184">เรกคอร์มิติการกำหนดราคาสำหรับ **msydn_bookableresource** ต้องตระหนักถึงความแตกต่างนี้</span><span class="sxs-lookup"><span data-stu-id="bc9fb-184">The pricing dimension record for **msydn_bookableresource** must be notified of this difference.</span></span>

1. <span data-ttu-id="bc9fb-185">ให้คลิกสองครั้งที่แถวในกริด **มิติการกำหนดราคา** เพื่อเปิดหน้าของมิติของ **msdyn_bookableresource**</span><span class="sxs-lookup"><span data-stu-id="bc9fb-185">Double-click the row in the **Pricing Dimensions** grid to open the dimension page of **msdyn_bookableresource**.</span></span>
2. <span data-ttu-id="bc9fb-186">บนหน้ามิติ บนแท็บ **ที่เกี่ยวข้อง** เลือก **ชื่อฟิลด์มิติการกำหนดราคา**</span><span class="sxs-lookup"><span data-stu-id="bc9fb-186">On dimension page, on the **Related** tab, select **Pricing Dimension Field Names**.</span></span>

  ![แท็บชื่อฟิลด์มิติการกำหนดราคา](media/PD-fieldname.png)

3. <span data-ttu-id="bc9fb-188">ในมุมมองร่วมที่เปิดขึ้น เลือก **เพิ่มชื่อฟิลด์มิติการกำหนดราคาใหม่**</span><span class="sxs-lookup"><span data-stu-id="bc9fb-188">In the associated view that opens, select **Add New Pricing Dimension Field Name**.</span></span>

  ![เพิ่มชื่อฟิลด์มิติการกำหนดราคาใหม่](media/Add-NewPD-fieldname.png)

  <span data-ttu-id="bc9fb-190">ซึ่งจะเป็นการเปิดหน้า **ชื่อฟิลด์มิติการกำหนดราคาใหม่** ขึ้นสำหรับ **msdyn_bookableresource**</span><span class="sxs-lookup"><span data-stu-id="bc9fb-190">This opens the **New Pricing dimension field name** page for **msdyn_bookableresource**.</span></span> 

4. <span data-ttu-id="bc9fb-191">บนหน้า **ชื่อฟิลด์มิติการกำหนดราคาใหม่** เพิ่ม **msdyn_projectteam** เป็น **ชื่อตรรกะของเอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="bc9fb-191">On the **New Pricing Dimension Field Name** page, add **msdyn_projectteam** to **Entity Locigal Name**.</span></span>
5. <span data-ttu-id="bc9fb-192">เพิ่ม **msdyn_bookableresourceid** เป็น **ชื่อฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="bc9fb-192">Add  **msdyn_bookableresourceid** to **Field Name**.</span></span>

 ![ฟอร์มชื่อฟิลด์มิติการกำหนดราคาใหม่](media/PD-fieldname-Added.png)