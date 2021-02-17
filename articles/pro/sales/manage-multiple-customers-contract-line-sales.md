---
title: จัดการลูกค้าหลายรายในรายละเอียดการให้บริการตามสัญญาตามโครงการ - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการจัดการลูกค้าหลายรายในรายละเอียดการให้บริการตามสัญญาตามโครงการ
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f28e7d1363647621f7bd23504aa6d4ea3fc95fc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181681"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a><span data-ttu-id="52d77-103">จัดการลูกค้าหลายรายในรายละเอียดการให้บริการตามสัญญาตามโครงการ - Lite</span><span class="sxs-lookup"><span data-stu-id="52d77-103">Manage multiple customers on project-based contract lines - lite</span></span>

<span data-ttu-id="52d77-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="52d77-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="52d77-105">รายละเอียดการให้บริการตามสัญญาตามโครงการสามารถรวมรายชื่อลูกค้าที่ต้องรับผิดชอบในการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="52d77-105">Project-based contract lines can include a list of customers that are responsible for payment.</span></span> <span data-ttu-id="52d77-106">รายชื่อลูกค้าในรายละเอียดการให้บริการตามสัญญาตามโครงการอาจเหมือนกับรายชื่อลูกค้าในสัญญา แต่ไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="52d77-106">This list of customers on the project-based contract line can be same as the list of customers on the contract but that isn't required.</span></span> <span data-ttu-id="52d77-107">เมื่อได้รับใบเสนอราคาโครงการและมีการสร้างสัญญาโครงการ รายชื่อลูกค้าในรายการใบเสนอราคาจะถูกคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="52d77-107">When a project quote is won, and a project contract is created, the customer list on the quote line is copied to the corresponding contract line.</span></span> <span data-ttu-id="52d77-108">ลูกค้าในใบเสนอราคาจะถูกคัดลอกไปยังสัญญา</span><span class="sxs-lookup"><span data-stu-id="52d77-108">Customers on the quote are copied to the contract.</span></span>

<span data-ttu-id="52d77-109">เมื่อมีการออกใบแจ้งหนี้สัญญาโครงการ รายชื่อลูกค้าในรายละเอียดการให้บริการตามสัญญาตามโครงการจะมีลำดับความสำคัญเหนือรายชื่อลูกค้าในสัญญา</span><span class="sxs-lookup"><span data-stu-id="52d77-109">When the project contract is invoiced, the customer list on project-based contract line takes priority over the customer list on the contract.</span></span> <span data-ttu-id="52d77-110">รายชื่อลูกค้าในสัญญาโครงการใช้เพื่อเริ่มต้นรายละเอียดการให้บริการตามสัญญาใหม่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="52d77-110">The customer list on the project contract is only used to default new contract lines.</span></span>

<span data-ttu-id="52d77-111">ลูกค้าตามสัญญาทั้งหมดในแท็บ **ลูกค้า** ของค่าเริ่มต้นสัญญาโครงการเป็นลูกค้าตามรายละเอียดการให้บริการตามสัญญาในรายละเอียดการให้บริการตามสัญญาใหม่ที่สร้างขึ้นสำหรับสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="52d77-111">All contract customers on the **Customers** tab of the project contract default as contract line customers on any new contract lines created for the project contract.</span></span> <span data-ttu-id="52d77-112">รายละเอียดการให้บริการตามสัญญาที่มีอยู่จะไม่สืบทอดเรกคอร์ดลูกค้าตามสัญญาใหม่ที่สร้างขึ้นหลังจากนั้น</span><span class="sxs-lookup"><span data-stu-id="52d77-112">Any existing contract lines will not inherit the new contract customer records created after them.</span></span>

## <a name="create-update-or-delete-a-contract-line-customer-record"></a><span data-ttu-id="52d77-113">สร้าง อัปเดต หรือลบเรกคอร์ดลูกค้าตามรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="52d77-113">Create, update, or delete a contract line customer record</span></span>

<span data-ttu-id="52d77-114">คุณสามารถสร้าง อัปเดต หรือลบลูกค้าตามรายละเอียดการให้บริการตามสัญญาจากแท็บลูกค้าตามรายละเอียดการให้บริการตามสัญญาในหน้ารายละเอียดการให้บริการตามสัญญาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="52d77-114">You can create, update, or delete a contract line customer from the Contract Line Customers tab on the Project-based Contract Line page.</span></span> <span data-ttu-id="52d77-115">เมื่อมีการเพิ่มลูกค้าใหม่ในรายละเอียดการให้บริการตามสัญญาตามโครงการ พวกเขาจะถูกเพิ่มในสัญญา โดยรวมในฐานะลูกค้าตามสัญญาโดยมีเปอร์เซ็นต์การแบ่งการเรียกเก็บเงินเริ่มต้นเป็นศูนย์เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="52d77-115">When a new customer is added on the project-based contract line, they are also added on the overall contract as a contract customer with a default billing split percentage of zero percent.</span></span> <span data-ttu-id="52d77-116">เปอร์เซ็นต์การแบ่งการเรียกเก็บเงินในสัญญาโดยรวมจะถูกคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาใหม่และไปยังสัญญาโครงการสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="52d77-116">The billing split percentage on the overall contract is copied to new contract lines and to the eventual project contract.</span></span> <span data-ttu-id="52d77-117">อย่างไรก็ตามเมื่อออกใบแจ้งหนี้จากสัญญา จะเป็นเปอร์เซ็นต์การแบ่งการเรียกเก็บเงินที่ระดับรายละเอียดการให้บริการตามสัญญาที่ใช้ ไม่ใช่เปอร์เซ็นต์การแยกการเรียกเก็บเงินที่ระดับสัญญาโดยรวม</span><span class="sxs-lookup"><span data-stu-id="52d77-117">However, when invoicing from the contract, it's the billing split percentage at the contract line level that is used and not the billing split percentage at the overall contract level.</span></span>

<span data-ttu-id="52d77-118">ด้านล่างนี้คือฟิลด์ในเรกคอร์ดลูกค้ารายละเอียดการให้บริการ **ตามสัญญา** ของรายละเอียดการให้บริการตามสัญญาตามโครงการเพื่อให้ทราบเมื่อคุณทำงาน:</span><span class="sxs-lookup"><span data-stu-id="52d77-118">Below are the fields on the **Contract** line customer record of a project-based contract line to keep in mind as you are working with it:</span></span>

| <span data-ttu-id="52d77-119">เขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="52d77-119">Field</span></span> | <span data-ttu-id="52d77-120">สถานที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="52d77-120">Location</span></span> | <span data-ttu-id="52d77-121">รายละเอียด</span><span class="sxs-lookup"><span data-stu-id="52d77-121">Description</span></span> | <span data-ttu-id="52d77-122">ผลกระทบขั้นปลาย</span><span class="sxs-lookup"><span data-stu-id="52d77-122">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="52d77-123">**ลูกค้าองค์กร**</span><span class="sxs-lookup"><span data-stu-id="52d77-123">**Account**</span></span> | <span data-ttu-id="52d77-124">ตารางที่สามารถแก้ไขได้ในแท็บ **ลูกค้าตามสัญญา** และฟอร์ม **หลัก** และ **สร้างด่วน** สำหรับลูกค้าที่ทำสัญญา</span><span class="sxs-lookup"><span data-stu-id="52d77-124">Editable grid on the **Contract Customers** tab and the **Main** and **Quick Create** forms for a contract customer.</span></span> | <span data-ttu-id="52d77-125">ลูกค้าองค์กรที่ใช้งานอยู่ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="52d77-125">All active accounts.</span></span> <span data-ttu-id="52d77-126">ฟิลด์นี้ถูกล็อกหลังจากสร้างเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="52d77-126">This field is locked after the record is created.</span></span> <span data-ttu-id="52d77-127">หากต้องการอัปเดตฟิลด์ ให้ลบเรกคอร์ด และสร้างเรกคอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="52d77-127">To update the field, delete the record, and create a new record.</span></span> <span data-ttu-id="52d77-128">หากคุณบันทึกยอดจริง คุณจะไม่สามารถลบเรกคอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="52d77-128">If you have recorded any actuals, you can't delete the record.</span></span> <span data-ttu-id="52d77-129">อย่างไรก็ตาม คุณสามารถทำเครื่องหมายเปอร์เซ็นต์การแบ่งการเรียกเก็บเงินเป็นศูนย์สำหรับบัญชีนั้นได้</span><span class="sxs-lookup"><span data-stu-id="52d77-129">However, you can mark the billing split percentage as zero for that account.</span></span> <span data-ttu-id="52d77-130">เมื่อเรกคอร์ดถูกทำเครื่องหมายเป็นศูนย์ ต้นทุนและรายได้ในอนาคตที่เกิดขึ้นจริงหรือแบ่งให้กับลูกค้ารายนี้จะได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="52d77-130">When the record is marked as zero, any future cost and revenue actuals that are attributed or split to this customer are impacted.</span></span> | <span data-ttu-id="52d77-131">เมื่อคุณเลือกบัญชีจากรายการหลักของบัญชี เพื่อเพิ่มและบันทึก ลูกค้ารายละเอียดการให้บริการตามสัญญาจะถูกเพิ่มเป็นลูกค้าตามสัญญาด้วย</span><span class="sxs-lookup"><span data-stu-id="52d77-131">When you pick an account from the master list of accounts to add and save them, the contract line customer is also added as a contract customer.</span></span> <span data-ttu-id="52d77-132">ลูกค้าตามรายละเอียดการให้บริการตามสัญญาจะใช้เมื่อสร้างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="52d77-132">Contract line customers are used when invoices are generated.</span></span> |
| <span data-ttu-id="52d77-133">**เปอร์เซ็นต์การแยกการเรียกเก็บเงิน**</span><span class="sxs-lookup"><span data-stu-id="52d77-133">**Billing Split Percent**</span></span> | <span data-ttu-id="52d77-134">ตารางที่สามารถแก้ไขได้ในแท็บ **ลูกค้าตามสัญญา** และฟอร์ม **หลัก** และ **สร้างด่วน** สำหรับลูกค้าที่ทำสัญญา</span><span class="sxs-lookup"><span data-stu-id="52d77-134">Editable grid on the **Contract Customers** tab and the **Main** and **Quick Create** forms for a contract customer.</span></span> | <span data-ttu-id="52d77-135">ฟิลด์นี้แสดงเปอร์เซ็นต์ของธุรกรรมการขายที่ยังไม่เรียกเก็บเงินแต่ละรายการที่เกิดจากลูกค้ารายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="52d77-135">This field represents the percentage of each unbilled sales transaction that will be attributed to this contract line customer.</span></span> | <span data-ttu-id="52d77-136">ลูกค้าตามรายละเอียดการให้บริการตามสัญญาและเปอร์เซ็นต์การแยกการเรียกเก็บเงินจะถูกใช้เมื่อมีการสร้างยอดจริงหลังจากการอนุมัติและเมื่อสร้างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="52d77-136">Contract line customers and billing split percentages are used when actuals are created after approval and when the invoice is generated.</span></span> |
| <span data-ttu-id="52d77-137">**วงเงินที่ต้องไม่เกิน**</span><span class="sxs-lookup"><span data-stu-id="52d77-137">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="52d77-138">ตารางที่สามารถแก้ไขได้ในแท็บ **ลูกค้าตามสัญญา** และฟอร์ม **หลัก** และ **สร้างด่วน** สำหรับลูกค้าที่ทำสัญญา</span><span class="sxs-lookup"><span data-stu-id="52d77-138">Editable grid on the **Contract Customers** tab and the **Main** and **Quick Create** forms for a contract customer.</span></span> | <span data-ttu-id="52d77-139">ระบุว่ามีขีดจำกัดหรือขีดจำกัดที่เจรจาไว้สำหรับจำนวนเงินโดยรวมที่จะออกใบแจ้งหนี้ให้กับลูกค้าสำหรับรายละเอียดการให้บริการตามสัญญานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="52d77-139">Indicates if there is a negotiated limit or cap to the overall amount that will be invoiced to this customer for the contract line.</span></span> | <span data-ttu-id="52d77-140">ขีดจำกัดไม่เกินสำหรับลูกค้ารายละเอียดการให้บริการตามสัญญาจะถูกใช้เมื่อมีการสร้างยอดจริงและสร้างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="52d77-140">The not-to-exceed limit for the contract line customer is used when actuals are created and the invoices are generated.</span></span> |
| <span data-ttu-id="52d77-141">**การปัดเศษ**</span><span class="sxs-lookup"><span data-stu-id="52d77-141">**Is Rounding**</span></span> | <span data-ttu-id="52d77-142">ตารางที่สามารถแก้ไขได้ในแท็บ **ลูกค้าตามสัญญา** และฟอร์ม **หลัก** และ **สร้างด่วน** สำหรับลูกค้ารายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="52d77-142">Editable grid on **Contract Customers** tab and **Main** and **Quick Create** forms for a contract line customer.</span></span> | <span data-ttu-id="52d77-143">ฟิลด์นี้ระบุว่าลูกค้ารายนี้เป็นลูกค้าการปัดเศษเริ่มต้นสำหรับรายละเอียดการให้บริการตามสัญญาตามโครงการนี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="52d77-143">This field indicates if this customer is a default rounding customer for this project-based contract line.</span></span> | <span data-ttu-id="52d77-144">เมื่อคุณสร้างจริงตามเปอร์เซ็นต์การแบ่งการเรียกเก็บเงิน อาจมีความแตกต่างในการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="52d77-144">When you generate an actual according to the billing split percentage, there may be some rounding differences.</span></span> <span data-ttu-id="52d77-145">ลูกค้ารายนี้เกิดจากความแตกต่างของการปัดเศษในกรณีนี้</span><span class="sxs-lookup"><span data-stu-id="52d77-145">This customer is attributed the rounding differences in this case.</span></span> |

## <a name="edit-billing-split-percentages"></a><span data-ttu-id="52d77-146">แก้ไขเปอร์เซ็นต์การแบ่งการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="52d77-146">Edit billing split percentages</span></span>

<span data-ttu-id="52d77-147">เปอร์เซ็นต์การแบ่งการเรียกเก็บเงินสามารถแก้ไขได้ในตาราง</span><span class="sxs-lookup"><span data-stu-id="52d77-147">Billing split percentages can be edited in the grid.</span></span> <span data-ttu-id="52d77-148">เมื่อเปอร์เซ็นต์การแบ่งการเรียกเก็บเงินไม่รวมถึง 100 เปอร์เซ็นต์ ข้อผิดพลาดจะเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="52d77-148">When the billing split percentages don't total 100 percent, an error will occur.</span></span> <span data-ttu-id="52d77-149">หลังจากคุณแก้ไขเปอร์เซ็นต์การแยกการเรียกเก็บเงินแล้ว ให้รีเฟรชหน้าเพื่อนำข้อผิดพลาดออก</span><span class="sxs-lookup"><span data-stu-id="52d77-149">After you edit the billing split percentages, refresh the page to remove the error.</span></span>

<span data-ttu-id="52d77-150">คุณยังสามารถเลือก **กระจายอย่างสม่ำเสมอ** ในตารางย่อยลูกค้ารายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="52d77-150">You can also select **Evenly Distribute** on the contract line customer subgrid.</span></span> <span data-ttu-id="52d77-151">การดำเนินการนี้จะจัดสรรการแบ่งการเรียกเก็บเงินให้กับลูกค้ารายละเอียดการให้บริการตามสัญญาทั้งหมดอย่างเท่าเทียมกัน</span><span class="sxs-lookup"><span data-stu-id="52d77-151">This action evenly allocates billing splits to all contract line customers.</span></span> <span data-ttu-id="52d77-152">หากมีปัจจัยการปัดเศษ จะถูกเพิ่มให้กับลูกค้าที่ปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="52d77-152">If there is any rounding factor, it will be added to the rounding customer.</span></span> <span data-ttu-id="52d77-153">ลูกค้ารายละเอียดการให้บริการตามสัญญารายหนึ่งจะถูกแท็กเป็นลูกค้า **การปัดเศษ** กับสถานะ **การปัดเศษ** ตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="52d77-153">One contract line customer is always tagged as the **Rounding** customer with the **Rounding** flag set to **Yes**.</span></span>