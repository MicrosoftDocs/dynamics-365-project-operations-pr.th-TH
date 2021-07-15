---
title: ภารวมของรายละเอียดการให้บริการตามสัญญาตามโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการทำงานกับรายละเอียดการให้บริการตามสัญญาตามโครงการ
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369939"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="ed99f-103">ภารวมของรายละเอียดการให้บริการตามสัญญาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="ed99f-103">Project-based contract lines overview</span></span>

<span data-ttu-id="ed99f-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="ed99f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ed99f-105">รายละเอียดการให้บริการตามสัญญาตามโครงการใน Dynamics 365 Project Operations ออกแบบมาเพื่อเก็บค่าการประมาณการและข้อตกลงการเรียกเก็บเงินสำหรับองค์ประกอบเฉพาะของงานโครงการในการมีส่วนร่วม</span><span class="sxs-lookup"><span data-stu-id="ed99f-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="ed99f-106">โครงสร้างของรายละเอียดการให้บริการตามสัญญาตามโครงการจะขยายสำหรับการประมาณการโครงการและสถานการณ์การเรียกเก็บเงินด้วยแนวคิดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ed99f-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="ed99f-107">วิธีการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="ed99f-107">Billing method</span></span>
- <span data-ttu-id="ed99f-108">การแม็ปโครงการและงาน</span><span class="sxs-lookup"><span data-stu-id="ed99f-108">Project and task mapping</span></span>
- <span data-ttu-id="ed99f-109">คลาสธุรกรรมที่รวมไว้</span><span class="sxs-lookup"><span data-stu-id="ed99f-109">Included transaction classes</span></span>
- <span data-ttu-id="ed99f-110">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="ed99f-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="ed99f-111">การตั้งค่าการคิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="ed99f-111">Chargeability setup</span></span>
- <span data-ttu-id="ed99f-112">ประมาณการโดยใช้รายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="ed99f-112">Estimates using contract line details</span></span>
- <span data-ttu-id="ed99f-113">ลูกค้าในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="ed99f-113">Contract line customers</span></span>

<span data-ttu-id="ed99f-114">ตารางต่อไปนี้มีฟิลด์ในแท็บ **ทั่วไป** ของรายละเอียดการให้บริการตามสัญญาตามโครงการที่ช่วยตั้งค่าพื้นฐานสำหรับรายละเอียด การประมาณการพื้นฐาน และการเตรียมการเรียกเก็บเงินสำหรับงานตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="ed99f-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="ed99f-115">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="ed99f-115">Field</span></span> | <span data-ttu-id="ed99f-116">รายละเอียด</span><span class="sxs-lookup"><span data-stu-id="ed99f-116">Description</span></span> | <span data-ttu-id="ed99f-117">ผลกระทบขั้นปลาย</span><span class="sxs-lookup"><span data-stu-id="ed99f-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ed99f-118">**ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="ed99f-118">**Name**</span></span> | <span data-ttu-id="ed99f-119">ชื่อของรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="ed99f-119">Name of the contract line.</span></span> <span data-ttu-id="ed99f-120">ซึ่งระบุส่วนประกอบที่ไม่ต่อเนื่องของสัญญาที่อยู่ระหว่างการประมาณ</span><span class="sxs-lookup"><span data-stu-id="ed99f-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="ed99f-121">สำหรับสัญญาโครงการที่สร้างจากใบเสนอราคา ค่านี้จะถูกคัดลอกจากค่าที่สอดคล้องกันของรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="ed99f-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="ed99f-122">ชื่อนี้ถูกคัดลอกไปยังรายการใบแจ้งหนี้โครงการที่สร้างขึ้นจากรายละเอียดการให้บริการตามสัญญานี้เมื่อสร้างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ed99f-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="ed99f-123">**วิธีการเรียกเก็บเงิน**</span><span class="sxs-lookup"><span data-stu-id="ed99f-123">**Billing Method**</span></span> | <span data-ttu-id="ed99f-124">บนสัญญาโครงการที่สร้างจากใบเสนอราคา ค่านี้จะถูกคัดลอกจากฟิลด์ที่สอดคล้องกันบนรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="ed99f-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="ed99f-125">นี่คือชุดตัวเลือกที่แสดงถึงรูปแบบการทำสัญญาหลักสองแบบที่สนับสนุนโดย Project Operations:</span><span class="sxs-lookup"><span data-stu-id="ed99f-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="ed99f-126">- **ราคาคงที่**</span><span class="sxs-lookup"><span data-stu-id="ed99f-126">- **Fixed Price**</span></span></br><span data-ttu-id="ed99f-127">- **เวลาและวัสดุ**</span><span class="sxs-lookup"><span data-stu-id="ed99f-127">- **Time and Material**</span></span> | <span data-ttu-id="ed99f-128">ตามวิธีการเรียกเก็บเงินของรายละเอียดการให้บริการตามสัญญาที่อ้างอิง ธุรกรรมจริงจะได้รับการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="ed99f-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="ed99f-129">หากรายละเอียดการให้บริการตามสัญญาที่อ้างอิงตามจริงมีวิธีการเรียกเก็บเงินตามเวลาและวัสดุ ระบบจะสร้างเรกคอร์ดต้นทุนและยอดขายที่ยังไม่เรียกเก็บ</span><span class="sxs-lookup"><span data-stu-id="ed99f-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="ed99f-130">หากรายละเอียดการให้บริการตามสัญญาที่อ้างอิงตามจริงมีวิธีการเรียกเก็บเงินแบบราคาคงที่ ระบบจะสร้างเฉพาะต้นทุนจริงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ed99f-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="ed99f-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="ed99f-131">**Project**</span></span> | <span data-ttu-id="ed99f-132">ใช้ฟิลด์นี้เพื่อระบุโครงการที่จะใช้ในการส่งมอบงานในการมีส่วนร่วมนี้</span><span class="sxs-lookup"><span data-stu-id="ed99f-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="ed99f-133">ค่านี้จะใช้ร่วมกับ **งานที่รวมไว้** และ **คลาสธุรกรรมที่รวม** เพื่อแก้ไขการอ้างอิงรายละเอียดการให้บริการตามสัญญาในเรกคอร์ดรายการข้อมูลจริงหรือประมาณการ</span><span class="sxs-lookup"><span data-stu-id="ed99f-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="ed99f-134">**งานที่รวมไว้**</span><span class="sxs-lookup"><span data-stu-id="ed99f-134">**Included Tasks**</span></span> | <span data-ttu-id="ed99f-135">ระบุว่ารายละเอียดการให้บริการตามสัญญานี้รวมงานโครงการทั้งหมดสำหรับโครงการที่เลือกหรือเฉพาะบางส่วนของงานหรือไม่</span><span class="sxs-lookup"><span data-stu-id="ed99f-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="ed99f-136">นี่เป็นชุดตัวเลือกที่มีค่าที่เป็นไปได้ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ed99f-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="ed99f-137">- **งานโครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="ed99f-137">- **All Project Tasks**</span></span></br><span data-ttu-id="ed99f-138">- **งานโครงการที่เลือกเท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="ed99f-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="ed99f-139">ค่าว่างในฟิลด์นี้เท่ากับการเลือก **งานโครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="ed99f-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="ed99f-140">ถ้า **งานที่เลือกเท่านั้น** ถูกเลือก คุณสามารถเลือกงานเฉพาะและเชื่อมโยงกับรายละเอียดการให้บริการตามสัญญานี้ในแท็บ **การตั้งค่าการเรียกเก็บเงินงาน** บนหน้า **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="ed99f-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="ed99f-141">ค่านี้ใช้ร่วมกับ **โครงการ** และคลาส **รวมธุรกรรม** เพื่อแก้ไขการอ้างอิงรายการสัญญาในเรกคอร์ดรายการจริงหรือรายการโดยประมาณ</span><span class="sxs-lookup"><span data-stu-id="ed99f-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="ed99f-142">**รวมเวลา**</span><span class="sxs-lookup"><span data-stu-id="ed99f-142">**Include Time**</span></span> | <span data-ttu-id="ed99f-143">ค่า **ใช่**/**ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานในโครงการที่เลือกจะรวมอยู่ในรายละเอียดการให้บริการตามสัญญานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="ed99f-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="ed99f-144">ค่า **ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานจะไม่รวมอยู่ในรายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="ed99f-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="ed99f-145">ค่า **ใช่** บ่งชี้ว่ารวม</span><span class="sxs-lookup"><span data-stu-id="ed99f-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="ed99f-146">ค่านี้ใช้ร่วมกับโครงการเพื่อแก้ไขการอ้างอิงรายละเอียดการให้บริการตามสัญญาในเรกคอร์ดข้อมูลจริงหรือประมาณการ</span><span class="sxs-lookup"><span data-stu-id="ed99f-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="ed99f-147">**รวมค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="ed99f-147">**Include Expense**</span></span> | <span data-ttu-id="ed99f-148">ค่า **ใช่**/**ไม่** ระบุว่าต้นทุนค่าใช้จ่ายในโครงการที่เลือกจะรวมอยู่ในรายละเอียดการให้บริการตามสัญญานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="ed99f-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="ed99f-149">ค่า **ไม่** ระบุว่าต้นทุนค่าใช้จ่ายจะไม่รวมอยู่ในรายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="ed99f-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="ed99f-150">ค่า **ใช่** บ่งชี้ว่ารวม</span><span class="sxs-lookup"><span data-stu-id="ed99f-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="ed99f-151">ค่านี้ใช้ร่วมกับโครงการเพื่อแก้ไขการอ้างอิงรายละเอียดการให้บริการตามสัญญาในเรกคอร์ดข้อมูลจริงหรือประมาณการ</span><span class="sxs-lookup"><span data-stu-id="ed99f-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="ed99f-152">**รวมวัสดุ**</span><span class="sxs-lookup"><span data-stu-id="ed99f-152">**Include Materials**</span></span> | <span data-ttu-id="ed99f-153">ค่า **ใช่**/**ไม่** ระบุว่าต้นทุนวัสดุในโครงการที่เลือกจะรวมอยู่ในรายละเอียดการให้บริการตามสัญญานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="ed99f-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="ed99f-154">ค่า **ไม่** ระบุว่าต้นทุนวัสดุจะไม่รวมอยู่ในรายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="ed99f-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="ed99f-155">ค่า **ใช่** บ่งชี้ว่ารวม</span><span class="sxs-lookup"><span data-stu-id="ed99f-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="ed99f-156">ค่านี้ใช้ร่วมกับโครงการเพื่อแก้ไขการอ้างอิงรายละเอียดการให้บริการตามสัญญาในเรกคอร์ดข้อมูลจริงหรือประมาณการ</span><span class="sxs-lookup"><span data-stu-id="ed99f-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="ed99f-157">**รวมค่าธรรมเนียม**</span><span class="sxs-lookup"><span data-stu-id="ed99f-157">**Include Fee**</span></span> | <span data-ttu-id="ed99f-158">ค่า **ใช่**/**ไม่** ระบุว่าต้นทุนค่าธรรมเนียมในโครงการที่เลือกจะรวมอยู่ในรายละเอียดการให้บริการตามสัญญานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="ed99f-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="ed99f-159">ค่า **ไม่** ระบุว่าค่าธรรมเนียมจะไม่รวมอยู่ในรายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="ed99f-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="ed99f-160">ค่า **ใช่** บ่งชี้ว่ารวม</span><span class="sxs-lookup"><span data-stu-id="ed99f-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="ed99f-161">ค่านี้ใช้ร่วมกับโครงการเพื่อแก้ไขการอ้างอิงรายละเอียดการให้บริการตามสัญญาในเรกคอร์ดข้อมูลจริงหรือประมาณการ</span><span class="sxs-lookup"><span data-stu-id="ed99f-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="ed99f-162">**จำนวนเงินตามสัญญา**</span><span class="sxs-lookup"><span data-stu-id="ed99f-162">**Contracted Amount**</span></span> | <span data-ttu-id="ed99f-163">ในรายละเอียดการให้บริการตามสัญญาราคาคงที่ จำนวนนี้คือมูลค่าที่ตกลงกันซึ่งจะออกใบแจ้งหนี้ให้กับลูกค้าสำหรับส่วนประกอบงานทั้งหมดที่เกี่ยวข้องกับรายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="ed99f-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="ed99f-164">ในรายละเอียดการให้บริการตามสัญญาเวลาและวัสดุ จำนวนนี้คือค่าประมาณที่จะออกใบแจ้งหนี้ให้กับลูกค้าสำหรับส่วนประกอบงานทั้งหมดที่เกี่ยวข้องกับรายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="ed99f-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="ed99f-165">บนสัญญาโครงการที่สร้างจากใบเสนอราคา ค่านี้จะถูกคัดลอกจากฟิลด์ที่สอดคล้องกันบนรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="ed99f-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="ed99f-166">เมื่อรายละเอียดการให้บริการตามสัญญาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและสรุปจากจำนวนเงินในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="ed99f-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="ed99f-167">เมื่อรายละเอียดการให้บริการตามสัญญามีรายละเอียดของรายการ ค่านี้สามารถแก้ไขได้โดยการเปลี่ยนจำนวนเงินในรายละเอียดรายการ</span><span class="sxs-lookup"><span data-stu-id="ed99f-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="ed99f-168">ในบรายละเอียดการให้บริการตามสัญญาราคาคงที่ ค่านี้จะใช้เพื่อสร้างจำนวนเงินก่อนหักภาษีสำหรับเหตุการณ์การเรียกเก็บเงินตามงวด</span><span class="sxs-lookup"><span data-stu-id="ed99f-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="ed99f-169">**ภาษีที่ประเมิน**</span><span class="sxs-lookup"><span data-stu-id="ed99f-169">**Estimated Tax**</span></span> | <span data-ttu-id="ed99f-170">ผู้ใช้สามารถแก้ไขฟิลด์นี้เพื่อป้อนจำนวนภาษีโดยประมาณในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="ed99f-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="ed99f-171">เมื่อรายละเอียดการให้บริการตามสัญญาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและสรุปจากจำนวนเงินภาษีในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="ed99f-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="ed99f-172">เมื่อรายละเอียดการให้บริการตามสัญญามีรายละเอียดของรายการ ค่านี้สามารถแก้ไขได้โดยการเปลี่ยนจำนวนเงินภาษีในรายละเอียดรายการ</span><span class="sxs-lookup"><span data-stu-id="ed99f-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="ed99f-173">ในบรายละเอียดการให้บริการตามสัญญาราคาคงที่ ค่านี้จะใช้เพื่อสร้างภาษีสำหรับเหตุการณ์การเรียกเก็บเงินตามงวด</span><span class="sxs-lookup"><span data-stu-id="ed99f-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="ed99f-174">**จำนวนเงินตามสัญญาหลังหักภาษี**</span><span class="sxs-lookup"><span data-stu-id="ed99f-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="ed99f-175">จำนวนเงินตามรายละเอียดการให้บริการตามสัญญาหลังหักภาษี</span><span class="sxs-lookup"><span data-stu-id="ed99f-175">The contract line amount after tax.</span></span> <span data-ttu-id="ed99f-176">ฟิลด์นี้เป็นแบบอ่านอย่างเดียวและคำนวณเป็น **จำนวนเงินตามสัญญา + ภาษี**</span><span class="sxs-lookup"><span data-stu-id="ed99f-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="ed99f-177">ในบรายละเอียดการให้บริการตามสัญญาราคาคงที่ ค่านี้จะใช้เพื่อสร้างเหตุการณ์การเรียกเก็บเงินตามงวด</span><span class="sxs-lookup"><span data-stu-id="ed99f-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="ed99f-178">**วงเงินที่ต้องไม่เกิน**</span><span class="sxs-lookup"><span data-stu-id="ed99f-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="ed99f-179">ผู้ใช้สามารถแก้ไขฟิลด์นี้และใช้ได้เฉพาะในรายละเอียดการให้บริการตามสัญญาตามโครงการที่มีวิธีการเรียกเก็บเงินตั้งค่าเป็นเวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="ed99f-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="ed99f-180">ผู้ใช้สามารถแก้ไขฟิลด์นี้</span><span class="sxs-lookup"><span data-stu-id="ed99f-180">The user can edit this field.</span></span> <span data-ttu-id="ed99f-181">เมื่อบ้อมูลจริงสำหรับเวลาหรือวัสดุอ้างถึงรายละเอียดการให้บริการตามสัญญาสำหรับเวลาและวัสดุ จำนวนเงินตามจริงจะถูกประเมินเทียบกับไม่เกินขีดจำกัด ในรายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="ed99f-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="ed99f-182">การประเมินนี้จะเสร็จสมบูรณ์หลังจากที่มีการคำนวณยอดเงินที่รับผิดชอบอและยืนยันแล้ว</span><span class="sxs-lookup"><span data-stu-id="ed99f-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="ed99f-183">**งบประมาณของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="ed99f-183">**Customer Budget**</span></span> | <span data-ttu-id="ed99f-184">ค่านี้สามารถแก้ไขได้และถูกคัดลอกจากฟิลด์ที่สอดคล้องกันบนรายการใบเสนอราคา หากสัญญาสร้างจากใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="ed99f-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="ed99f-185">ฟิลด์นี้ใช้สำหรับข้อมูลเท่านั้นและไม่มีความสำคัญดาวน์สตรีม</span><span class="sxs-lookup"><span data-stu-id="ed99f-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="ed99f-186">กฎการตรวจสอบความถูกต้องสำหรับตัวเลือกบนแท็บทั่วไปของรายละเอียดการให้บริการตามสัญญาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="ed99f-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="ed99f-187">กฎข้อที่ 1: หากฟิลด์ **รวมงาน** ว่างหรือตั้งค่าเป็น **งานโครงการทั้งหมด** งานทั้งหมดของโครงการจะรวมอยู่ในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="ed99f-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="ed99f-188">กฎข้อ 2: เมื่อฟิลด์ **รวมงาน** ว่างเปล่าหรือตั้งค่าเป็น **งานโครงการทั้งหมด** โครงการและคลาสธุรกรรมบางรายการสามารถรวมอยู่ในรายละเอียดการให้บริการตามสัญญาตามโครงการของสัญญาได้เพียงรายการเดียว</span><span class="sxs-lookup"><span data-stu-id="ed99f-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="ed99f-189">กฎข้อ 3: เมื่อฟิลด์ **รวมงาน** ตั้งค่าเป็น **งานโครงการที่เลือกเท่านั้น** โครงการและคลาสธุรกรรมบางรายการสามารถรวมอยู่ในรายละเอียดการให้บริการตามสัญญาตามโครงการของสัญญาได้หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="ed99f-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="ed99f-190">
                    <strong>สัญญา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ed99f-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ed99f-191">
                    <strong>รายละเอียดการให้บริการตามสัญญา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ed99f-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ed99f-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ed99f-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="ed99f-193">
                    <strong>งานที่รวมไว้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ed99f-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="ed99f-194">
                    <strong>รวมเวลา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ed99f-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="ed99f-195">
                    <strong>รวมค่าใช้จ่าย</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ed99f-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ed99f-196">
                    <strong>รวมวัสดุ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ed99f-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ed99f-197">
                    <strong>รวม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ed99f-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="ed99f-198">
                    <strong>ค่าธรรมเนียม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ed99f-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="ed99f-199">
                    <strong>ถูกต้อง/ไม่ถูกต้อง</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ed99f-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="ed99f-200">
                    <strong>เหตุผล</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ed99f-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ed99f-201">C1</span><span class="sxs-lookup"><span data-stu-id="ed99f-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ed99f-202">CL1</span><span class="sxs-lookup"><span data-stu-id="ed99f-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-203">P1</span><span class="sxs-lookup"><span data-stu-id="ed99f-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ed99f-204">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="ed99f-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-205">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-206">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-207">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-208">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ed99f-209">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="ed99f-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ed99f-210">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="ed99f-210">Violation of Rule #2.</span></span> <span data-ttu-id="ed99f-211">เวลา ค่าใช้จ่าย วัสดุ และค่าธรรมเนียมของโครงการ P1 จะรวมอยู่ในทั้งรายละเอียดการให้บริการตามสัญญา CL1 และ CL2</span><span class="sxs-lookup"><span data-stu-id="ed99f-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ed99f-212">C1</span><span class="sxs-lookup"><span data-stu-id="ed99f-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ed99f-213">CL2</span><span class="sxs-lookup"><span data-stu-id="ed99f-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-214">P1</span><span class="sxs-lookup"><span data-stu-id="ed99f-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ed99f-215">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="ed99f-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-216">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-217">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-218">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-219">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ed99f-220">C1</span><span class="sxs-lookup"><span data-stu-id="ed99f-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ed99f-221">CL1</span><span class="sxs-lookup"><span data-stu-id="ed99f-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-222">P1</span><span class="sxs-lookup"><span data-stu-id="ed99f-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ed99f-223">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="ed99f-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-224">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-225">ไม่</span><span class="sxs-lookup"><span data-stu-id="ed99f-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-226">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-227">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ed99f-228">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="ed99f-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ed99f-229">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="ed99f-229">Violation of Rule #2.</span></span> <span data-ttu-id="ed99f-230">เวลา วัสดุ และค่าธรรมเนียมของโครงการ P1 จะรวมอยู่ในทั้งรายละเอียดการให้บริการตามสัญญา CL1 และ CL2</span><span class="sxs-lookup"><span data-stu-id="ed99f-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ed99f-231">C1</span><span class="sxs-lookup"><span data-stu-id="ed99f-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ed99f-232">CL2</span><span class="sxs-lookup"><span data-stu-id="ed99f-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-233">P1</span><span class="sxs-lookup"><span data-stu-id="ed99f-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ed99f-234">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="ed99f-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-235">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-236">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-237">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-238">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ed99f-239">C1</span><span class="sxs-lookup"><span data-stu-id="ed99f-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ed99f-240">CL1</span><span class="sxs-lookup"><span data-stu-id="ed99f-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-241">P1</span><span class="sxs-lookup"><span data-stu-id="ed99f-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ed99f-242">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="ed99f-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-243">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-244">ไม่</span><span class="sxs-lookup"><span data-stu-id="ed99f-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-245">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-246">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ed99f-247">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="ed99f-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ed99f-248">เวลา วัสดุ และค่าธรรมเนียมของโครงการ P1 รวมอยู่ใน CL1</span><span class="sxs-lookup"><span data-stu-id="ed99f-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="ed99f-249">ค่าใช้จ่ายในโครงการ P1 รวมอยู่ใน CL2</span><span class="sxs-lookup"><span data-stu-id="ed99f-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="ed99f-250">ไม่มีการทับซ้อนกันในสิ่งที่รวมอยู่ในรายละเอียดการให้บริการตามสัญญาแต่ละรายการ ดังนั้นจึงถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="ed99f-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ed99f-251">C1</span><span class="sxs-lookup"><span data-stu-id="ed99f-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ed99f-252">CL2</span><span class="sxs-lookup"><span data-stu-id="ed99f-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-253">P1</span><span class="sxs-lookup"><span data-stu-id="ed99f-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ed99f-254">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="ed99f-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-255">ไม่</span><span class="sxs-lookup"><span data-stu-id="ed99f-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-256">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-257">ไม่</span><span class="sxs-lookup"><span data-stu-id="ed99f-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-258">ไม่</span><span class="sxs-lookup"><span data-stu-id="ed99f-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ed99f-259">C1</span><span class="sxs-lookup"><span data-stu-id="ed99f-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ed99f-260">CL1</span><span class="sxs-lookup"><span data-stu-id="ed99f-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-261">P1</span><span class="sxs-lookup"><span data-stu-id="ed99f-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ed99f-262">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ed99f-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-263">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-264">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-265">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-266">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ed99f-267">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="ed99f-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ed99f-268">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="ed99f-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="ed99f-269">C1 รวมเวลา วัสดุ ค่าใช้จ่าย และค่าธรรมเนียมสำหรับชุดงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="ed99f-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="ed99f-270">CL2 รวมเวลา วัสดุ ค่าใช้จ่าย และค่าธรรมเนียมสำหรับโครงการ P1 ทั้งหมด ดังนั้นจึงทับซ้อนกับสิ่งที่รวมอยู่ใน C1</span><span class="sxs-lookup"><span data-stu-id="ed99f-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ed99f-271">C1</span><span class="sxs-lookup"><span data-stu-id="ed99f-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ed99f-272">CL2</span><span class="sxs-lookup"><span data-stu-id="ed99f-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-273">P1</span><span class="sxs-lookup"><span data-stu-id="ed99f-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ed99f-274">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="ed99f-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-275">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-276">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-277">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-278">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ed99f-279">C1</span><span class="sxs-lookup"><span data-stu-id="ed99f-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ed99f-280">CL1</span><span class="sxs-lookup"><span data-stu-id="ed99f-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-281">P1</span><span class="sxs-lookup"><span data-stu-id="ed99f-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ed99f-282">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ed99f-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-283">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-284">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-285">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-286">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ed99f-287">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="ed99f-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ed99f-288">ตามกฎ #3</span><span class="sxs-lookup"><span data-stu-id="ed99f-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="ed99f-289">C1 รวมเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับชุดงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="ed99f-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="ed99f-290">CL2 รวมเวลา ค่าใช้จ่าย วัสดุ และค่าธรรมเนียมสำหรับชุดงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="ed99f-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="ed99f-291">การตรวจสอบความถูกต้องเพิ่มเติมเพียงอย่างเดียวคือชุดงานย่อยใน CL1 นั้นแตกต่างจากชุดงานย่อยใน CL2 เพื่อให้แน่ใจว่าไม่มีการทับซ้อนกันที่นั่น</span><span class="sxs-lookup"><span data-stu-id="ed99f-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="ed99f-292">ระบบดำเนินการนี้ทำได้เมื่อเกี่ยวข้องกับงาน</span><span class="sxs-lookup"><span data-stu-id="ed99f-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ed99f-293">C1</span><span class="sxs-lookup"><span data-stu-id="ed99f-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ed99f-294">CL2</span><span class="sxs-lookup"><span data-stu-id="ed99f-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-295">P1</span><span class="sxs-lookup"><span data-stu-id="ed99f-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ed99f-296">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ed99f-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-297">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ed99f-298">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-299">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ed99f-300">ใช่</span><span class="sxs-lookup"><span data-stu-id="ed99f-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
