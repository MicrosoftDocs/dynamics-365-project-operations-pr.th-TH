---
title: การตั้งค่าสัญญาโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับฟิลด์ที่ส่งผลกระทบต่อรายละเอียดการให้บริการตามสัญญาและข้อมูลเกี่ยวกับสัญญาที่สรุปไว้ในรายการทั้งหมด
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f29e396f8d30a5c5648b5c9937f1f20fbf72e89
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181165"
---
# <a name="project-contract-settings"></a><span data-ttu-id="86e64-103">การตั้งค่าสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-103">Project contract settings</span></span>

<span data-ttu-id="86e64-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="86e64-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="86e64-105">หัวข้อนี้ให้ข้อมูลเกี่ยวกับฟิลด์ที่ใช้กับสัญญาโครงการทั้งหมดรวมถึงการตั้งค่าที่มีผลต่อรายละเอียดการให้บริการตามสัญญาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="86e64-105">This topic provides information about fields that apply to the entire project contract including settings that impact all contract lines.</span></span> <span data-ttu-id="86e64-106">ข้อมูลเกี่ยวกับสัญญาที่สรุปไว้ในรายการทั้งหมดเพื่อขับเคลื่อน KPI ของสัญญาโครงการจะรวมอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="86e64-106">Information about the contract that is summarized across all the line items to drive KPIs of the project contract is also included.</span></span>

<span data-ttu-id="86e64-107">ตารางต่อไปนี้แสดงฟิลด์บนสัญญาโครงการที่ไม่ซ้ำกันสำหรับ Dynamics 365 Project Operations หรือมีการเปลี่ยนแปลงที่สำคัญบางอย่างในลักษณะการทำงานจากใบสั่งขายใน Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="86e64-107">The following table lists the fields on a project contract that are unique to Dynamics 365 Project Operations or have some important changes in behavior from sales orders in Dynamics 365 Sales.</span></span>

| <span data-ttu-id="86e64-108">เขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="86e64-108">Field</span></span> | <span data-ttu-id="86e64-109">สถานที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="86e64-109">Location</span></span> | <span data-ttu-id="86e64-110">รายละเอียด</span><span class="sxs-lookup"><span data-stu-id="86e64-110">Description</span></span> | <span data-ttu-id="86e64-111">ผลกระทบขั้นปลาย</span><span class="sxs-lookup"><span data-stu-id="86e64-111">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="86e64-112">พิมพ์ข้อความ</span><span class="sxs-lookup"><span data-stu-id="86e64-112">Type</span></span> | <span data-ttu-id="86e64-113">แท็บ **สรุป** (ซ่อนไว้)</span><span class="sxs-lookup"><span data-stu-id="86e64-113">**Summary** tab (hidden)</span></span> | <span data-ttu-id="86e64-114">ฟิลด์ชุดตัวเลือกนี้มีตัวเลือกดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="86e64-114">This is an option set field with the following options:</span></span></br><span data-ttu-id="86e64-115">- **ตามงาน** (ใช้ได้เฉพาะเมื่อติดตั้ง Project Operations)</span><span class="sxs-lookup"><span data-stu-id="86e64-115">- **Work-based** (Available only when Project Operations is installed)</span></span></br><span data-ttu-id="86e64-116">- **ตามสินค้า** (สามารถใช้ได้เฉพาะเมื่อติดตั้ง Project Operations และ Sales เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="86e64-116">- **Item-based** (Available only when Project Operations and Sales are installed)</span></span></br><span data-ttu-id="86e64-117">- **ตามการบำรุงรักษาบริการ** (สามารถใช้งานได้เมื่อติดตั้ง Dynamics 365 Field Service)</span><span class="sxs-lookup"><span data-stu-id="86e64-117">- **Service Maintenance-based** (Available when Dynamics 365 Field Service is installed)</span></span> | <span data-ttu-id="86e64-118">ในการดำเนินงานโครงการ ค่าของฟิลด์นี้จะมีค่าเริ่มต้นเป็น **ตามงาน** และจัดประเภทสัญญาเป็นสัญญาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-118">In Project Operations, the value of this field defaults to **Work-based** and classifies the contract as a project-based contract.</span></span> <span data-ttu-id="86e64-119">สัญญาควรอิงตามโครงการเพื่อเปิดใช้งานส่วนขยายและฟังก์ชันเฉพาะโครงการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="86e64-119">A contract should be project-based to enable all project-specific extensions and functionality.</span></span> |
| <span data-ttu-id="86e64-120">บริษัทที่เป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="86e64-120">Owning Company</span></span> | <span data-ttu-id="86e64-121">แท็บ **สรุป**</span><span class="sxs-lookup"><span data-stu-id="86e64-121">**Summary** tab</span></span> | <span data-ttu-id="86e64-122">นิติบุคคลที่จะพิจารณาต้นทุนและรายได้ที่เกิดขึ้นจากโครงการที่เกี่ยวข้องกับสัญญาโครงการนี้</span><span class="sxs-lookup"><span data-stu-id="86e64-122">The legal entity that accounts for the costs and revenue that accrues from the projects associated with this project contract.</span></span> <span data-ttu-id="86e64-123">เมื่อมีการสร้างสัญญาจากใบเสนอราคา ระบบจะคัดลอกฟิลด์นี้จากฟิลด์ที่เกี่ยวข้องในเรกคอร์ดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="86e64-123">When a contract is created from a quote, this field is copied from the corresponding field on the quote record.</span></span> | <span data-ttu-id="86e64-124">บริษัทที่เป็นเจ้าของเทียบเท่ากับแนวคิดของนิติบุคคลในโมดูล **การจัดการและการบัญชีโครงการ** ของ Project Operations</span><span class="sxs-lookup"><span data-stu-id="86e64-124">The owning company equates the concept of legal entity in the **Project management and accounting** module of Project Operations.</span></span> <span data-ttu-id="86e64-125">ต้นทุนและรายได้ทั้งหมดที่เกิดขึ้นจากโครงการนี้จะรวมอยู่ในบัญชีแยกประเภททั่วไปของบริษัทที่เป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="86e64-125">All costs and revenue accrued from this project are accounted for in the General Ledger of the owning company.</span></span> |
| <span data-ttu-id="86e64-126">ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="86e64-126">Customer</span></span> | <span data-ttu-id="86e64-127">แท็บ **สรุป**</span><span class="sxs-lookup"><span data-stu-id="86e64-127">**Summary** tab</span></span> | <span data-ttu-id="86e64-128">การอ้างอิงถึงเรกคอร์ดบริษัทหรือบัญชีของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="86e64-128">A reference to the customer's company or account record.</span></span> <span data-ttu-id="86e64-129">เมื่อมีการสร้างสัญญาจากใบเสนอราคา ระบบจะคัดลอกฟิลด์นี้จากฟิลด์ที่เกี่ยวข้องในเรกคอร์ดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="86e64-129">When a contract is created from a quote, this field is copied from the corresponding field on the quote record.</span></span> | <span data-ttu-id="86e64-130">สกุลเงินในสัญญาโครงการมีการตั้งค่าเริ่มต้นตามสกุลเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="86e64-130">The currency on the project contract defaults based on the currency of the customer.</span></span> <span data-ttu-id="86e64-131">สกุลเงินสามารถเปลี่ยนแปลงก่อนบันทึกสัญญา</span><span class="sxs-lookup"><span data-stu-id="86e64-131">The currency can be changed before the contract is saved.</span></span> |
| <span data-ttu-id="86e64-132">ผู้จัดการลูกค้าองค์กร</span><span class="sxs-lookup"><span data-stu-id="86e64-132">Account Manager</span></span> | <span data-ttu-id="86e64-133">แท็บ **สรุป**</span><span class="sxs-lookup"><span data-stu-id="86e64-133">**Summary** tab</span></span> | <span data-ttu-id="86e64-134">ชื่อของผู้จัดการลูกค้าองค์กรสำหรับข้อตกลงนี้</span><span class="sxs-lookup"><span data-stu-id="86e64-134">The name of the Account Manager for this deal.</span></span> <span data-ttu-id="86e64-135">เมื่อมีการสร้างสัญญาจากใบเสนอราคา ระบบจะคัดลอกฟิลด์นี้จากฟิลด์ที่เกี่ยวข้องในเรกคอร์ดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="86e64-135">When a contract is created from a quote, this field is copied from the corresponding field on the quote record.</span></span> | <span data-ttu-id="86e64-136">ผู้จัดการลูกค้าองค์กรมีหน้าที่จัดการความสัมพันธ์กับลูกค้าจนโครงการนี้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="86e64-136">The Account Manager is responsible for managing the relationship with the customer through the completion of the project.</span></span> <span data-ttu-id="86e64-137">ตามเรกคอร์ดทรัพยากรที่สามารถจองได้ที่ผูกกับผู้จัดการลูกค้าองค์กร หน่วยที่ทำสัญญาจะมีการกำหนดเป็นค่าเริ่มต้นในสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-137">Based on the bookable resource record tied to the Account Manager, the contracting unit defaults on the project contract.</span></span> |
| <span data-ttu-id="86e64-138">หน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="86e64-138">Contracting Unit</span></span> | <span data-ttu-id="86e64-139">แท็บ **สรุป**</span><span class="sxs-lookup"><span data-stu-id="86e64-139">**Summary** tab</span></span> | <span data-ttu-id="86e64-140">หน่วยองค์กรที่รับผิดชอบการส่งมอบโครงการที่เกี่ยวข้องกับสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="86e64-140">The organization unit responsible for the delivery of the projects associated with this contract.</span></span> <span data-ttu-id="86e64-141">เมื่อมีการสร้างสัญญาจากใบเสนอราคา ระบบจะคัดลอกฟิลด์นี้จากฟิลด์ที่เกี่ยวข้องในเรกคอร์ดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="86e64-141">When a contract is created from a quote, this field is copied from the corresponding field on the quote record.</span></span> | <span data-ttu-id="86e64-142">หน่วยที่ทำสัญญาคือแผนกของบริษัทที่ดำเนินโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-142">The contracting unit is the division of the company that executes the projects.</span></span> <span data-ttu-id="86e64-143">ทุกหน่วยที่ทำสัญญามีสกุลเงิน และสกุลเงินนี้ใช้เพื่อรายงานต้นทุนโดยประมาณและต้นทุนจริงที่เกิดขึ้นระหว่างโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-143">Every contracting unit has a currency, and this currency is used to report estimated and actual costs incurred during the project.</span></span> |
| <span data-ttu-id="86e64-144">ราคาตลาดของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="86e64-144">Product Price List</span></span> | <span data-ttu-id="86e64-145">แท็บ **สรุป**</span><span class="sxs-lookup"><span data-stu-id="86e64-145">**Summary** tab</span></span> | <span data-ttu-id="86e64-146">นี่คือรายการราคาที่ใช้เป็นราคาเริ่มต้นในรายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="86e64-146">This price list is used to default prices on product-based contract lines.</span></span> <span data-ttu-id="86e64-147">รายการของตัวเลือกรแบบหล่นลงสำหรับฟิลด์นี้จะแสดงรายการของรายการราคาที่สกุลเงินของรายการราคาตรงกับสกุลเงินในสัญญา</span><span class="sxs-lookup"><span data-stu-id="86e64-147">The list of drop-down options for this field shows a list of price lists where the price list currency matches the currency on the contract.</span></span> <span data-ttu-id="86e64-148">เมื่อมีการสร้างสัญญาจากใบเสนอราคา ระบบจะคัดลอกฟิลด์นี้จากฟิลด์ที่เกี่ยวข้องในเรกคอร์ดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="86e64-148">When a contract is created from a quote, this field is copied from the corresponding field on the quote record.</span></span> <span data-ttu-id="86e64-149">ในสัญญาโครงการ ฟิลด์นี้เป็นค่าเริ่มต้นจากเรกคอร์ดบัญชี แต่สามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="86e64-149">On the project contract, this field is defaulted from the account record but can be changed.</span></span> | <span data-ttu-id="86e64-150">ไม่มีความเกี่ยวข้องขั้นปลายสำหรับฟิลด์นี้</span><span class="sxs-lookup"><span data-stu-id="86e64-150">There is no downstream relevance for this field.</span></span> |
| <span data-ttu-id="86e64-151">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="86e64-151">Currency</span></span> | <span data-ttu-id="86e64-152">แท็บ **สรุป**</span><span class="sxs-lookup"><span data-stu-id="86e64-152">**Summary** tab</span></span> | <span data-ttu-id="86e64-153">สกุลเงินที่ใช้ในการรายงานมูลค่าของดีลนี้และสกุลเงินที่ลูกค้าจะออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="86e64-153">The currency used to report the value of this deal and the currency in which the customer will be invoiced.</span></span> <span data-ttu-id="86e64-154">เมื่อมีการสร้างสัญญาจากใบเสนอราคา ระบบจะคัดลอกฟิลด์นี้จากฟิลด์ที่เกี่ยวข้องในเรกคอร์ดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="86e64-154">When a contract is created from a quote, this field is copied from the corresponding field on the quote record.</span></span> <span data-ttu-id="86e64-155">ในสัญญาโครงการ ฟิลด์นี้เป็นค่าเริ่มต้นจากเรกคอร์ดบัญชี แต่สามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="86e64-155">On the project contract, this field defaults from the account record but can be changed.</span></span> | <span data-ttu-id="86e64-156">หลังจากบันทึกสัญญาแล้ว ฟิลด์นี้จะไม่สามารถแก้ไขได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="86e64-156">After a contract is saved, this field is no longer editable.</span></span> <span data-ttu-id="86e64-157">ฟิลด์นี้ใช้เป้นค่าเริ่มต้นรายการราคาของผลิตภัณฑ์และโครงการในสัญญา</span><span class="sxs-lookup"><span data-stu-id="86e64-157">This field is used to default the product and project price lists on the contract.</span></span> <span data-ttu-id="86e64-158">สกุลเงินในสัญญาใช้จับคู่สกุลเงินในรายการราคา</span><span class="sxs-lookup"><span data-stu-id="86e64-158">The currency on the contract is used to match the currency on the price list.</span></span> |
| <span data-ttu-id="86e64-159">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="86e64-159">Not-to-Exceed Limit</span></span> | <span data-ttu-id="86e64-160">แท็บ **สรุป**</span><span class="sxs-lookup"><span data-stu-id="86e64-160">**Summary** tab</span></span> | <span data-ttu-id="86e64-161">ฟิลด์นี้แสดงค่าขีดบนที่เจรจาไว้สำหรับมูลค่าสุดท้ายที่ลูกค้าตกลงสำหรับข้อตกลงนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="86e64-161">This field indicates the negotiated cap on the final value that the customer has agreed to for this deal.</span></span> | <span data-ttu-id="86e64-162">ค่าขีดบนได้รับการประเมินในระหว่างการดำเนินการและใช้ได้กับสินค้าในรายการและโครงการทั้งหมดที่เกี่ยวข้องกับข้อตกลงนี้</span><span class="sxs-lookup"><span data-stu-id="86e64-162">The cap is evaluated during execution and is applicable across all line items and projects associated with this deal.</span></span> |
| <span data-ttu-id="86e64-163">วันที่ขอให้นำส่ง</span><span class="sxs-lookup"><span data-stu-id="86e64-163">Requested Delivery Date</span></span> | <span data-ttu-id="86e64-164">แท็บ **สรุป**</span><span class="sxs-lookup"><span data-stu-id="86e64-164">**Summary** tab</span></span> | <span data-ttu-id="86e64-165">เมื่อมีการสร้างสัญญาจากใบเสนอราคาโครงการ ระบบจะคัดลอกฟิลด์นี้จากฟิลด์ที่เกี่ยวข้องในใบเสนอราคาโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-165">When a contract is created from a project quote, this field is copied from the corresponding field on the project quote.</span></span> | <span data-ttu-id="86e64-166">วันที่นี้ใช้เป็นวันที่สิ้นสุดเพื่อสร้างกำหนดการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="86e64-166">This date is used as the end date to generate invoice schedules.</span></span> |

<span data-ttu-id="86e64-167">KPI ต่อไปนี้มีอยู่ในแท็บ **ประสิทธิภาพของสัญญา** ของสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-167">The following KPIs are available on the **Contract Performance** tab of a project contract.</span></span>

| <span data-ttu-id="86e64-168">เขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="86e64-168">Field</span></span> | <span data-ttu-id="86e64-169">สถานที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="86e64-169">Location</span></span> | <span data-ttu-id="86e64-170">รายละเอียด</span><span class="sxs-lookup"><span data-stu-id="86e64-170">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="86e64-171">ค่าสัญญา</span><span class="sxs-lookup"><span data-stu-id="86e64-171">Contract Value</span></span> | <span data-ttu-id="86e64-172">สัญญาโดยรวม</span><span class="sxs-lookup"><span data-stu-id="86e64-172">Overall contract</span></span> | <span data-ttu-id="86e64-173">มูลค่ารวมของสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-173">The total value of the Project contract.</span></span> |
| <span data-ttu-id="86e64-174">จำนวนเงินที่เรียกเก็บ</span><span class="sxs-lookup"><span data-stu-id="86e64-174">Billed Amount</span></span> | <span data-ttu-id="86e64-175">สัญญาโดยรวม</span><span class="sxs-lookup"><span data-stu-id="86e64-175">Overall contract</span></span> | <span data-ttu-id="86e64-176">ผลรวมของจำนวนเงินในใบแจ้งหนี้ทั้งหมดที่มีต่อสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="86e64-176">The sum of the amounts on all invoices against this contract.</span></span> |
| <span data-ttu-id="86e64-177">ต้นทุนที่เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="86e64-177">Cost Incurred</span></span> | <span data-ttu-id="86e64-178">สัญญาโดยรวม</span><span class="sxs-lookup"><span data-stu-id="86e64-178">Overall contract</span></span> | <span data-ttu-id="86e64-179">ผลรวมของต้นทุนจริงทั้งหมดที่บันทึกในโครงการทั้งหมดที่แมปกับสัญญา</span><span class="sxs-lookup"><span data-stu-id="86e64-179">The sum of all cost actuals logged on all projects that are mapped to the contract.</span></span> |
| <span data-ttu-id="86e64-180">กำไรขั้นต้น</span><span class="sxs-lookup"><span data-stu-id="86e64-180">Gross Margin</span></span> | <span data-ttu-id="86e64-181">สัญญาโดยรวม</span><span class="sxs-lookup"><span data-stu-id="86e64-181">Overall contract</span></span> | <span data-ttu-id="86e64-182">จำนวนเงินที่เรียกเก็บ - ค่าใช้จ่ายที่เกิดขึ้นจนถึงวันที่ / จำนวนเงินที่เรียกเก็บ</span><span class="sxs-lookup"><span data-stu-id="86e64-182">Billed amount - Cost incurred till date / Billed amount</span></span> |
| <span data-ttu-id="86e64-183">กำไรเบื้องต้นที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="86e64-183">Expected Margin</span></span> | <span data-ttu-id="86e64-184">สัญญาโดยรวม</span><span class="sxs-lookup"><span data-stu-id="86e64-184">Overall contract</span></span> | <span data-ttu-id="86e64-185">(มูลค่าสัญญา - ค่าใช้จ่ายโดยประมาณ) / มูลค่าสัญญาค่าใช้จ่ายโดยประมาณ = ผลรวมของต้นทุนโดยประมาณทั้งหมดของโครงการทั้งหมดที่เชื่อมโยงกับสัญญา</span><span class="sxs-lookup"><span data-stu-id="86e64-185">(Contract value - Estimated costs) / Contract valueEstimated costs = The sum of all estimated costs on all projects mapped to the contract.</span></span>|
| <span data-ttu-id="86e64-186">ค่าสัญญา</span><span class="sxs-lookup"><span data-stu-id="86e64-186">Contract Value</span></span> | <span data-ttu-id="86e64-187">บรรทัดตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-187">Project-based lines</span></span> | <span data-ttu-id="86e64-188">ค่าของรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="86e64-188">The value of the contract line.</span></span> |
| <span data-ttu-id="86e64-189">จำนวนเงินที่เรียกเก็บ</span><span class="sxs-lookup"><span data-stu-id="86e64-189">Billed amount</span></span> | <span data-ttu-id="86e64-190">บรรทัดตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-190">Project-based lines</span></span> | <span data-ttu-id="86e64-191">สำหรับรายละเอียดการให้บริการตามสัญญาราคาคงที่: ผลรวมของจำนวนเงินในเหตุการณ์สำคัญของการขายที่เรียกเก็บเงินทั้งหมดที่เกิดขึ้นจริงกับรายละเอียดการให้บริการตามสัญญานี้ในใบแจ้งหนี้ต่างๆ ที่สร้างขึ้นสำหรับสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="86e64-191">For fixed price contract line: The sum of the amounts on all billed sales milestone actuals against this contract line on various invoices created for this contract.</span></span> <span data-ttu-id="86e64-192">สำหรับรายละเอียดการให้บริการตามสัญญาเวลาและวัสดุ: ผลรวมของจำนวนเงินในยอดขายตามจริงที่เรียกเก็บและคิดค่าธรรมเนียมได้ทั้งหมดที่เกิดขึ้นกับรายละเอียดการให้บริการตามสัญญานี้ในใบแจ้งหนี้ต่างๆ ที่สร้างขึ้นสำหรับสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="86e64-192">For time and material contract line: The sum of the amounts on all chargeable billed sales actuals against this contract line on various invoices created for this contract.</span></span> |
| <span data-ttu-id="86e64-193">ต้นทุนที่เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="86e64-193">Cost Incurred</span></span> | <span data-ttu-id="86e64-194">บรรทัดตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-194">Project-based lines</span></span> | <span data-ttu-id="86e64-195">ผลรวมของต้นทุนจริงทั้งหมดที่บันทึกในโครงการทั้งหมดที่แมปกับรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="86e64-195">The sum of all cost actuals logged on all projects mapped to the contract line.</span></span> |
| <span data-ttu-id="86e64-196">กำไรขั้นต้น</span><span class="sxs-lookup"><span data-stu-id="86e64-196">Gross Margin</span></span> | <span data-ttu-id="86e64-197">บรรทัดตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-197">Project-based lines</span></span> | <span data-ttu-id="86e64-198">(จำนวนเงินที่เรียกเก็บ - ค่าใช้จ่ายที่เกิดขึ้นจนถึงวันที่) / จำนวนเงินที่เรียกเก็บ</span><span class="sxs-lookup"><span data-stu-id="86e64-198">(Billed amount - Cost incurred till date) / Billed amount</span></span> |
| <span data-ttu-id="86e64-199">กำไรเบื้องต้นที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="86e64-199">Expected Margin</span></span> | <span data-ttu-id="86e64-200">บรรทัดตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-200">Project-based lines</span></span> | <span data-ttu-id="86e64-201">(จำนวนเงินตามรายละเอียดการให้บริการตามสัญญาในสกุลเงินหลัก - ต้นทุนโดยประมาณสำหรับรายละเอียดการให้บริการตามสัญญาในสกุลเงินฐาน) / จำนวนเงินตามรายละเอียดการให้บริการตามสัญญาในสกุลเงินฐาน</span><span class="sxs-lookup"><span data-stu-id="86e64-201">(Contract line amount in base currency - Estimated costs for the contract line in base currency) / Contract line amount in base currency</span></span> |
| <span data-ttu-id="86e64-202">ต้นทุนที่เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="86e64-202">Cost Incurred</span></span> | <span data-ttu-id="86e64-203">รายละเอียดของรายการตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-203">Detail of a project-based line</span></span> | <span data-ttu-id="86e64-204">เวลา: ผลรวมของต้นทุนจริงในเวลาที่บันทึกไว้สำหรับบทบาทนี้ในโครงการที่แมปกับรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="86e64-204">Time: The sum of the amount on time cost actuals logged for this role on the project mapped to the contract line.</span></span> <span data-ttu-id="86e64-205">ค่าใช้จ่าย: ผลรวมของต้นทุนจริงในค่าใช้จ่ายทั้งหมดที่บันทึกไว้สำหรับประเภทนี้ในโครงการที่แมปกับรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="86e64-205">Expenses: The sum of the amount on all expense cost actuals logged for this category on the project mapped to the contract line.</span></span> |
| <span data-ttu-id="86e64-206">ปริมาณที่บันทึก</span><span class="sxs-lookup"><span data-stu-id="86e64-206">Logged Quantity</span></span> | <span data-ttu-id="86e64-207">รายละเอียดของรายการตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-207">Detail of a project-based line</span></span> | <span data-ttu-id="86e64-208">เวลา: ปริมาณของต้นทุนจริงในเวลาทั้งหมดสำหรับบทบาทนี้ในโครงการที่แมปกับรายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="86e64-208">Time: All of the time quantity on the time cost actuals for a role on the project that is mapped to this contract line.</span></span> <span data-ttu-id="86e64-209">ค่าใช้จ่าย: ปริมาณทั้งหมดสำหรับประเภทค่าใช้จ่ายนี้ในต้นทุนค่าใช้จ่ายจริงของโครงการที่แมปกับรายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="86e64-209">Expenses: All quantities for this expense category on the expense cost actuals on the project are mapped to this contract line.</span></span> |
| <span data-ttu-id="86e64-210">จำนวนเงินที่เรียกเก็บ</span><span class="sxs-lookup"><span data-stu-id="86e64-210">Billed Amount</span></span> | <span data-ttu-id="86e64-211">รายละเอียดของรายการตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-211">Detail of a project-based line</span></span> | <span data-ttu-id="86e64-212">สำหรับรายละเอียดการให้บริการตามสัญญาราคาคงที่ ฟิลด์นี้จะเว้นว่างไว้ในระดับรายละเอียด และจะแสดงที่ระดับรายละเอียดการให้บริการตามสัญญาเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="86e64-212">For a fixed price contract line, this field is left blank on the detail level and is only shown at the contract line level.</span></span> <span data-ttu-id="86e64-213">สำหรับรายละเอียดการให้บริการตามสัญญาเวลาและวัสดุ การคำนวณจะเสร็จสมบูรณ์ในระดับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="86e64-213">For a time and material contract line, calculations are completed at the details level.</span></span> <span data-ttu-id="86e64-214">รายละเอียดแสดงผลรวมของจำนวนเงินในรายการรายได้ที่เรียกเก็บเงินทั้งหมดเทียบกับรายละเอียดการให้บริการตามสัญญาที่เรียกเก็บได้</span><span class="sxs-lookup"><span data-stu-id="86e64-214">The details show the sum of the amount on all the billed revenue lines against this contract line that are chargeable.</span></span> |
| <span data-ttu-id="86e64-215">ปริมาณที่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="86e64-215">Billed Quantity</span></span> | <span data-ttu-id="86e64-216">รายละเอียดของรายการตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-216">Detail of a project-based line</span></span> | <span data-ttu-id="86e64-217">สำหรับรายละเอียดการให้บริการตามสัญญาราคาคงที่ ฟิลด์นี้จะเว้นว่างไว้ในระดับรายละเอียด และจะแสดงที่ระดับรายละเอียดการให้บริการตามสัญญาเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="86e64-217">For a fixed price contract line, this field is left blank on the detail level and is only shown at the contract line level.</span></span> <span data-ttu-id="86e64-218">สำหรับรายละเอียดการให้บริการตามสัญญาเวลาและวัสดุ การคำนวณจะเสร็จสมบูรณ์ในระดับรายละเอียดสำหรับเวลาและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="86e64-218">For a time and material contract line, calculations are completed at the details level for time and expenses.</span></span> <span data-ttu-id="86e64-219">เวลา: ผลรวมของชั่วโมงในรายการรายได้ที่เรียกเก็บเงินทั้งหมดสำหรับบทบาทนี้เทียบกับรายละเอียดการให้บริการตามสัญญาที่เรียกเก็บได้</span><span class="sxs-lookup"><span data-stu-id="86e64-219">Time: The sum of the hours on all the billed revenue lines for this role against this contract line that are chargeable.</span></span> <span data-ttu-id="86e64-220">ค่าใช้จ่าย: ปริมาณทั้งหมดสำหรับประเภทค่าใช้จ่ายนี้ในต้นทุนค่าใช้จ่ายจริงของโครงการที่แมปกับรายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="86e64-220">Expenses: All quantities for this expense category on the expense cost actuals on the project are mapped to this contract line.</span></span> |
| <span data-ttu-id="86e64-221">ค่าสัญญา</span><span class="sxs-lookup"><span data-stu-id="86e64-221">Contract Value</span></span> | <span data-ttu-id="86e64-222">บรรทัดตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="86e64-222">Product-based lines</span></span> | <span data-ttu-id="86e64-223">มูลค่าตามรายละเอียดการให้บริการตามสัญญาของรายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์นี้</span><span class="sxs-lookup"><span data-stu-id="86e64-223">The contract line value of this product-based contract line.</span></span> |
| <span data-ttu-id="86e64-224">จำนวนเงินที่เรียกเก็บ</span><span class="sxs-lookup"><span data-stu-id="86e64-224">Billed Amount</span></span> | <span data-ttu-id="86e64-225">บรรทัดตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="86e64-225">Product-based lines</span></span> | <span data-ttu-id="86e64-226">ผลรวมของยอดเงินในรายการใบแจ้งหนี้ทั้งหมดเทียบกับรายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์นี้ในใบแจ้งหนี้ต่างๆ ที่สร้างขึ้นสำหรับสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="86e64-226">The sum of the amounts on all invoice lines against this product-based contract line on various invoices that are created for this contract.</span></span> |
| <span data-ttu-id="86e64-227">ต้นทุนที่เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="86e64-227">Cost Incurred</span></span> | <span data-ttu-id="86e64-228">บรรทัดตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="86e64-228">Product-based lines</span></span> | <span data-ttu-id="86e64-229">ผลรวมของต้นทุนจริงทั้งหมดที่บันทึกสำหรับรายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="86e64-229">The sum of all cost actuals logged for the product-based contract line.</span></span> |
| <span data-ttu-id="86e64-230">กำไรขั้นต้น</span><span class="sxs-lookup"><span data-stu-id="86e64-230">Gross Margin</span></span> | <span data-ttu-id="86e64-231">บรรทัดตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="86e64-231">Project-based lines</span></span> | <span data-ttu-id="86e64-232">จำนวนเงินที่เรียกเก็บ - ค่าใช้จ่ายที่เกิดขึ้นจนถึงวันที่ / จำนวนเงินที่เรียกเก็บ</span><span class="sxs-lookup"><span data-stu-id="86e64-232">Billed amount - Cost incurred till date / Billed amount</span></span> |
| <span data-ttu-id="86e64-233">กำไรเบื้องต้นที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="86e64-233">Expected Margin</span></span> | <span data-ttu-id="86e64-234">บรรทัดตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="86e64-234">Product-based lines</span></span> | <span data-ttu-id="86e64-235">(มูลค่าตามรายละเอียดการให้บริการตามสัญญา - ต้นทุนโดยประมาณสำหรับรายละเอียดการให้บริการตามสัญญา) / มูลค่าตามรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="86e64-235">(Contract line value - Estimated costs for the contract line) / Contract line value</span></span> |