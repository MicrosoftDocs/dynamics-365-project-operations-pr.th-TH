---
title: ภารวมของรายละเอียดการให้บริการตามสัญญาตามโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการทำงานกับรายละเอียดการให้บริการตามสัญญาตามโครงการ
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858181"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="f1881-103">ภารวมของรายละเอียดการให้บริการตามสัญญาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="f1881-103">Project-based contract lines overview</span></span>

<span data-ttu-id="f1881-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="f1881-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f1881-105">รายละเอียดการให้บริการตามสัญญาตามโครงการใน Dynamics 365 Project Operations ออกแบบมาเพื่อเก็บค่าการประมาณการและข้อตกลงการเรียกเก็บเงินสำหรับองค์ประกอบเฉพาะของงานโครงการในการมีส่วนร่วม</span><span class="sxs-lookup"><span data-stu-id="f1881-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="f1881-106">โครงสร้างของรายละเอียดการให้บริการตามสัญญาตามโครงการจะขยายสำหรับการประมาณการโครงการและสถานการณ์การเรียกเก็บเงินด้วยแนวคิดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f1881-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="f1881-107">วิธีการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="f1881-107">Billing method</span></span>
- <span data-ttu-id="f1881-108">การแม็ปโครงการและงาน</span><span class="sxs-lookup"><span data-stu-id="f1881-108">Project and task mapping</span></span>
- <span data-ttu-id="f1881-109">คลาสธุรกรรมที่รวมไว้</span><span class="sxs-lookup"><span data-stu-id="f1881-109">Included transaction classes</span></span>
- <span data-ttu-id="f1881-110">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="f1881-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="f1881-111">การตั้งค่าการคิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="f1881-111">Chargeability setup</span></span>
- <span data-ttu-id="f1881-112">ประมาณการโดยใช้รายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="f1881-112">Estimates using contract line details</span></span>
- <span data-ttu-id="f1881-113">ลูกค้าในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="f1881-113">Contract line customers</span></span>

<span data-ttu-id="f1881-114">ตารางต่อไปนี้มีฟิลด์ในแท็บ **ทั่วไป** ของรายละเอียดการให้บริการตามสัญญาตามโครงการที่ช่วยตั้งค่าพื้นฐานสำหรับรายละเอียด การประมาณการพื้นฐาน และการเตรียมการเรียกเก็บเงินสำหรับงานตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="f1881-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="f1881-115">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="f1881-115">Field</span></span> | <span data-ttu-id="f1881-116">รายละเอียด</span><span class="sxs-lookup"><span data-stu-id="f1881-116">Description</span></span> | <span data-ttu-id="f1881-117">ผลกระทบขั้นปลาย</span><span class="sxs-lookup"><span data-stu-id="f1881-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f1881-118">**ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="f1881-118">**Name**</span></span> | <span data-ttu-id="f1881-119">ชื่อของรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="f1881-119">Name of the contract line.</span></span> <span data-ttu-id="f1881-120">ซึ่งระบุส่วนประกอบที่ไม่ต่อเนื่องของสัญญาที่อยู่ระหว่างการประมาณ</span><span class="sxs-lookup"><span data-stu-id="f1881-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="f1881-121">สำหรับสัญญาโครงการที่สร้างจากใบเสนอราคา ค่านี้จะถูกคัดลอกจากค่าที่สอดคล้องกันของรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="f1881-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="f1881-122">ชื่อนี้ถูกคัดลอกไปยังรายการใบแจ้งหนี้โครงการที่สร้างขึ้นจากรายละเอียดการให้บริการตามสัญญานี้เมื่อสร้างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="f1881-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="f1881-123">**วิธีการเรียกเก็บเงิน**</span><span class="sxs-lookup"><span data-stu-id="f1881-123">**Billing Method**</span></span> | <span data-ttu-id="f1881-124">บนสัญญาโครงการที่สร้างจากใบเสนอราคา ค่านี้จะถูกคัดลอกจากฟิลด์ที่สอดคล้องกันบนรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="f1881-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="f1881-125">นี่คือชุดตัวเลือกที่แสดงถึงรูปแบบการทำสัญญาหลักสองแบบที่สนับสนุนโดย Project Operations:</span><span class="sxs-lookup"><span data-stu-id="f1881-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="f1881-126">- **ราคาคงที่**</span><span class="sxs-lookup"><span data-stu-id="f1881-126">- **Fixed Price**</span></span></br><span data-ttu-id="f1881-127">- **เวลาและวัสดุ**</span><span class="sxs-lookup"><span data-stu-id="f1881-127">- **Time and Material**</span></span> | <span data-ttu-id="f1881-128">ตามวิธีการเรียกเก็บเงินของรายละเอียดการให้บริการตามสัญญาที่อ้างอิง ธุรกรรมจริงจะได้รับการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="f1881-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="f1881-129">หากรายละเอียดการให้บริการตามสัญญาที่อ้างอิงตามจริงมีวิธีการเรียกเก็บเงินตามเวลาและวัสดุ ระบบจะสร้างเรกคอร์ดต้นทุนและยอดขายที่ยังไม่เรียกเก็บ</span><span class="sxs-lookup"><span data-stu-id="f1881-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="f1881-130">หากรายละเอียดการให้บริการตามสัญญาที่อ้างอิงตามจริงมีวิธีการเรียกเก็บเงินแบบราคาคงที่ ระบบจะสร้างเฉพาะต้นทุนจริงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f1881-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="f1881-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="f1881-131">**Project**</span></span> | <span data-ttu-id="f1881-132">ใช้ฟิลด์นี้เพื่อระบุโครงการที่จะใช้ในการส่งมอบงานในการมีส่วนร่วมนี้</span><span class="sxs-lookup"><span data-stu-id="f1881-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="f1881-133">ค่านี้จะใช้ร่วมกับ **งานที่รวมไว้** และ **คลาสธุรกรรมที่รวม** เพื่อแก้ไขการอ้างอิงรายละเอียดการให้บริการตามสัญญาในเรกคอร์ดรายการข้อมูลจริงหรือประมาณการ</span><span class="sxs-lookup"><span data-stu-id="f1881-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="f1881-134">**งานที่รวมไว้**</span><span class="sxs-lookup"><span data-stu-id="f1881-134">**Included Tasks**</span></span> | <span data-ttu-id="f1881-135">ระบุว่ารายละเอียดการให้บริการตามสัญญานี้รวมงานโครงการทั้งหมดสำหรับโครงการที่เลือกหรือเฉพาะบางส่วนของงานหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f1881-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="f1881-136">นี่เป็นชุดตัวเลือกที่มีค่าที่เป็นไปได้ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f1881-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="f1881-137">- **งานโครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="f1881-137">- **All Project Tasks**</span></span></br><span data-ttu-id="f1881-138">- **งานโครงการที่เลือกเท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="f1881-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="f1881-139">ค่าว่างในฟิลด์นี้เท่ากับการเลือก **งานโครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="f1881-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="f1881-140">ถ้า **งานที่เลือกเท่านั้น** ถูกเลือก คุณสามารถเลือกงานเฉพาะและเชื่อมโยงกับรายละเอียดการให้บริการตามสัญญานี้ในแท็บ **การตั้งค่าการเรียกเก็บเงินงาน** บนหน้า **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="f1881-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="f1881-141">ค่านี้ใช้ร่วมกับ **โครงการ** และคลาส **รวมธุรกรรม** เพื่อแก้ไขการอ้างอิงรายการสัญญาในเรกคอร์ดรายการจริงหรือรายการโดยประมาณ</span><span class="sxs-lookup"><span data-stu-id="f1881-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="f1881-142">**รวมเวลา**</span><span class="sxs-lookup"><span data-stu-id="f1881-142">**Include Time**</span></span> | <span data-ttu-id="f1881-143">ค่า **ใช่**/**ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานในโครงการที่เลือกจะรวมอยู่ในรายละเอียดการให้บริการตามสัญญานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="f1881-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="f1881-144">ค่า **ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานจะไม่รวมอยู่ในรายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="f1881-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="f1881-145">ค่า **ใช่** บ่งชี้ว่ารวม</span><span class="sxs-lookup"><span data-stu-id="f1881-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="f1881-146">ค่านี้ใช้ร่วมกับโครงการเพื่อแก้ไขการอ้างอิงรายละเอียดการให้บริการตามสัญญาในเรกคอร์ดข้อมูลจริงหรือประมาณการ</span><span class="sxs-lookup"><span data-stu-id="f1881-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="f1881-147">**รวมค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="f1881-147">**Include Expense**</span></span> | <span data-ttu-id="f1881-148">ค่า **ใช่**/**ไม่** ระบุว่าต้นทุนค่าใช้จ่ายในโครงการที่เลือกจะรวมอยู่ในรายละเอียดการให้บริการตามสัญญานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="f1881-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="f1881-149">ค่า **ไม่** ระบุว่าต้นทุนค่าใช้จ่ายจะไม่รวมอยู่ในรายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="f1881-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="f1881-150">ค่า **ใช่** บ่งชี้ว่ารวม</span><span class="sxs-lookup"><span data-stu-id="f1881-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="f1881-151">ค่านี้ใช้ร่วมกับโครงการเพื่อแก้ไขการอ้างอิงรายละเอียดการให้บริการตามสัญญาในเรกคอร์ดข้อมูลจริงหรือประมาณการ</span><span class="sxs-lookup"><span data-stu-id="f1881-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="f1881-152">**รวมวัสดุ**</span><span class="sxs-lookup"><span data-stu-id="f1881-152">**Include Materials**</span></span> | <span data-ttu-id="f1881-153">ค่า **ใช่**/**ไม่** ระบุว่าต้นทุนวัสดุในโครงการที่เลือกจะรวมอยู่ในรายละเอียดการให้บริการตามสัญญานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="f1881-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="f1881-154">ค่า **ไม่** ระบุว่าต้นทุนวัสดุจะไม่รวมอยู่ในรายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="f1881-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="f1881-155">ค่า **ใช่** บ่งชี้ว่ารวม</span><span class="sxs-lookup"><span data-stu-id="f1881-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="f1881-156">ค่านี้ใช้ร่วมกับโครงการเพื่อแก้ไขการอ้างอิงรายละเอียดการให้บริการตามสัญญาในเรกคอร์ดข้อมูลจริงหรือประมาณการ</span><span class="sxs-lookup"><span data-stu-id="f1881-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="f1881-157">**รวมค่าธรรมเนียม**</span><span class="sxs-lookup"><span data-stu-id="f1881-157">**Include Fee**</span></span> | <span data-ttu-id="f1881-158">ค่า **ใช่**/**ไม่** ระบุว่าต้นทุนค่าธรรมเนียมในโครงการที่เลือกจะรวมอยู่ในรายละเอียดการให้บริการตามสัญญานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="f1881-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="f1881-159">ค่า **ไม่** ระบุว่าค่าธรรมเนียมจะไม่รวมอยู่ในรายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="f1881-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="f1881-160">ค่า **ใช่** บ่งชี้ว่ารวม</span><span class="sxs-lookup"><span data-stu-id="f1881-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="f1881-161">ค่านี้ใช้ร่วมกับโครงการเพื่อแก้ไขการอ้างอิงรายละเอียดการให้บริการตามสัญญาในเรกคอร์ดข้อมูลจริงหรือประมาณการ</span><span class="sxs-lookup"><span data-stu-id="f1881-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="f1881-162">**จำนวนเงินตามสัญญา**</span><span class="sxs-lookup"><span data-stu-id="f1881-162">**Contracted Amount**</span></span> | <span data-ttu-id="f1881-163">ในรายละเอียดการให้บริการตามสัญญาราคาคงที่ จำนวนนี้คือมูลค่าที่ตกลงกันซึ่งจะออกใบแจ้งหนี้ให้กับลูกค้าสำหรับส่วนประกอบงานทั้งหมดที่เกี่ยวข้องกับรายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="f1881-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="f1881-164">ในรายละเอียดการให้บริการตามสัญญาเวลาและวัสดุ จำนวนนี้คือค่าประมาณที่จะออกใบแจ้งหนี้ให้กับลูกค้าสำหรับส่วนประกอบงานทั้งหมดที่เกี่ยวข้องกับรายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="f1881-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="f1881-165">บนสัญญาโครงการที่สร้างจากใบเสนอราคา ค่านี้จะถูกคัดลอกจากฟิลด์ที่สอดคล้องกันบนรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="f1881-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="f1881-166">เมื่อรายละเอียดการให้บริการตามสัญญาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและสรุปจากจำนวนเงินในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="f1881-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="f1881-167">เมื่อรายละเอียดการให้บริการตามสัญญามีรายละเอียดของรายการ ค่านี้สามารถแก้ไขได้โดยการเปลี่ยนจำนวนเงินในรายละเอียดรายการ</span><span class="sxs-lookup"><span data-stu-id="f1881-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="f1881-168">ในบรายละเอียดการให้บริการตามสัญญาราคาคงที่ ค่านี้จะใช้เพื่อสร้างจำนวนเงินก่อนหักภาษีสำหรับเหตุการณ์การเรียกเก็บเงินตามงวด</span><span class="sxs-lookup"><span data-stu-id="f1881-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="f1881-169">**ภาษีที่ประเมิน**</span><span class="sxs-lookup"><span data-stu-id="f1881-169">**Estimated Tax**</span></span> | <span data-ttu-id="f1881-170">ผู้ใช้สามารถแก้ไขฟิลด์นี้เพื่อป้อนจำนวนภาษีโดยประมาณในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="f1881-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="f1881-171">เมื่อรายละเอียดการให้บริการตามสัญญาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและสรุปจากจำนวนเงินภาษีในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="f1881-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="f1881-172">เมื่อรายละเอียดการให้บริการตามสัญญามีรายละเอียดของรายการ ค่านี้สามารถแก้ไขได้โดยการเปลี่ยนจำนวนเงินภาษีในรายละเอียดรายการ</span><span class="sxs-lookup"><span data-stu-id="f1881-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="f1881-173">ในบรายละเอียดการให้บริการตามสัญญาราคาคงที่ ค่านี้จะใช้เพื่อสร้างภาษีสำหรับเหตุการณ์การเรียกเก็บเงินตามงวด</span><span class="sxs-lookup"><span data-stu-id="f1881-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="f1881-174">**จำนวนเงินตามสัญญาหลังหักภาษี**</span><span class="sxs-lookup"><span data-stu-id="f1881-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="f1881-175">จำนวนเงินตามรายละเอียดการให้บริการตามสัญญาหลังหักภาษี</span><span class="sxs-lookup"><span data-stu-id="f1881-175">The contract line amount after tax.</span></span> <span data-ttu-id="f1881-176">ฟิลด์นี้เป็นแบบอ่านอย่างเดียวและคำนวณเป็น **จำนวนเงินตามสัญญา + ภาษี**</span><span class="sxs-lookup"><span data-stu-id="f1881-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="f1881-177">ในบรายละเอียดการให้บริการตามสัญญาราคาคงที่ ค่านี้จะใช้เพื่อสร้างเหตุการณ์การเรียกเก็บเงินตามงวด</span><span class="sxs-lookup"><span data-stu-id="f1881-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="f1881-178">**วงเงินที่ต้องไม่เกิน**</span><span class="sxs-lookup"><span data-stu-id="f1881-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="f1881-179">ผู้ใช้สามารถแก้ไขฟิลด์นี้และใช้ได้เฉพาะในรายละเอียดการให้บริการตามสัญญาตามโครงการที่มีวิธีการเรียกเก็บเงินตั้งค่าเป็นเวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="f1881-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="f1881-180">ผู้ใช้สามารถแก้ไขฟิลด์นี้</span><span class="sxs-lookup"><span data-stu-id="f1881-180">The user can edit this field.</span></span> <span data-ttu-id="f1881-181">เมื่อบ้อมูลจริงสำหรับเวลาหรือวัสดุอ้างถึงรายละเอียดการให้บริการตามสัญญาสำหรับเวลาและวัสดุ จำนวนเงินตามจริงจะถูกประเมินเทียบกับไม่เกินขีดจำกัด ในรายละเอียดการให้บริการตามสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="f1881-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="f1881-182">การประเมินนี้จะเสร็จสมบูรณ์หลังจากที่มีการคำนวณยอดเงินที่รับผิดชอบอและยืนยันแล้ว</span><span class="sxs-lookup"><span data-stu-id="f1881-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="f1881-183">**งบประมาณของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="f1881-183">**Customer Budget**</span></span> | <span data-ttu-id="f1881-184">ค่านี้สามารถแก้ไขได้และถูกคัดลอกจากฟิลด์ที่สอดคล้องกันบนรายการใบเสนอราคา หากสัญญาสร้างจากใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="f1881-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="f1881-185">ฟิลด์นี้ใช้สำหรับข้อมูลเท่านั้นและไม่มีความสำคัญดาวน์สตรีม</span><span class="sxs-lookup"><span data-stu-id="f1881-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="f1881-186">กฎการตรวจสอบความถูกต้องสำหรับตัวเลือกบนแท็บทั่วไปของรายละเอียดการให้บริการตามสัญญาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="f1881-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="f1881-187">กฎข้อที่ 1: หากฟิลด์ **รวมงาน** ว่างหรือตั้งค่าเป็น **งานโครงการทั้งหมด** งานทั้งหมดของโครงการจะรวมอยู่ในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="f1881-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="f1881-188">กฎข้อ 2: เมื่อฟิลด์ **รวมงาน** ว่างเปล่าหรือตั้งค่าเป็น **งานโครงการทั้งหมด** โครงการและคลาสธุรกรรมบางรายการสามารถรวมอยู่ในรายละเอียดการให้บริการตามสัญญาตามโครงการของสัญญาได้เพียงรายการเดียว</span><span class="sxs-lookup"><span data-stu-id="f1881-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="f1881-189">กฎข้อ 3: เมื่อฟิลด์ **รวมงาน** ตั้งค่าเป็น **งานโครงการที่เลือกเท่านั้น** โครงการและคลาสธุรกรรมบางรายการสามารถรวมอยู่ในรายละเอียดการให้บริการตามสัญญาตามโครงการของสัญญาได้หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="f1881-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="f1881-190">
                    <strong>สัญญา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f1881-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f1881-191">
                    <strong>รายละเอียดการให้บริการตามสัญญา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f1881-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="f1881-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f1881-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="f1881-193">
                    <strong>งานที่รวมไว้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f1881-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="f1881-194">
                    <strong>รวมเวลา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f1881-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="f1881-195">
                    <strong>รวมค่าใช้จ่าย</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f1881-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="f1881-196">
                    <strong>รวมวัสดุ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f1881-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="f1881-197">
                    <strong>รวม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f1881-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="f1881-198">
                    <strong>ค่าธรรมเนียม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f1881-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="f1881-199">
                    <strong>ถูกต้อง/ไม่ถูกต้อง</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f1881-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="f1881-200">
                    <strong>เหตุผล</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f1881-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f1881-201">C1</span><span class="sxs-lookup"><span data-stu-id="f1881-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f1881-202">CL1</span><span class="sxs-lookup"><span data-stu-id="f1881-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-203">P1</span><span class="sxs-lookup"><span data-stu-id="f1881-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="f1881-204">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="f1881-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-205">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-206">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-207">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-208">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f1881-209">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f1881-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f1881-210">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="f1881-210">Violation of Rule #2.</span></span> <span data-ttu-id="f1881-211">เวลา ค่าใช้จ่าย วัสดุ และค่าธรรมเนียมของโครงการ P1 จะรวมอยู่ในทั้งรายละเอียดการให้บริการตามสัญญา CL1 และ CL2</span><span class="sxs-lookup"><span data-stu-id="f1881-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f1881-212">C1</span><span class="sxs-lookup"><span data-stu-id="f1881-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f1881-213">CL2</span><span class="sxs-lookup"><span data-stu-id="f1881-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-214">P1</span><span class="sxs-lookup"><span data-stu-id="f1881-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="f1881-215">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="f1881-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-216">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-217">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-218">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-219">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-219">Yes</span></span> </p>
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
<span data-ttu-id="f1881-220">C1</span><span class="sxs-lookup"><span data-stu-id="f1881-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f1881-221">CL1</span><span class="sxs-lookup"><span data-stu-id="f1881-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-222">P1</span><span class="sxs-lookup"><span data-stu-id="f1881-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="f1881-223">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="f1881-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-224">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-225">ไม่</span><span class="sxs-lookup"><span data-stu-id="f1881-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-226">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-227">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f1881-228">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f1881-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f1881-229">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="f1881-229">Violation of Rule #2.</span></span> <span data-ttu-id="f1881-230">เวลา วัสดุ และค่าธรรมเนียมของโครงการ P1 จะรวมอยู่ในทั้งรายละเอียดการให้บริการตามสัญญา CL1 และ CL2</span><span class="sxs-lookup"><span data-stu-id="f1881-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f1881-231">C1</span><span class="sxs-lookup"><span data-stu-id="f1881-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f1881-232">CL2</span><span class="sxs-lookup"><span data-stu-id="f1881-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-233">P1</span><span class="sxs-lookup"><span data-stu-id="f1881-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="f1881-234">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="f1881-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-235">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-236">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-237">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-238">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-238">Yes</span></span> </p>
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
<span data-ttu-id="f1881-239">C1</span><span class="sxs-lookup"><span data-stu-id="f1881-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f1881-240">CL1</span><span class="sxs-lookup"><span data-stu-id="f1881-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-241">P1</span><span class="sxs-lookup"><span data-stu-id="f1881-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="f1881-242">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="f1881-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-243">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-244">ไม่</span><span class="sxs-lookup"><span data-stu-id="f1881-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-245">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-246">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f1881-247">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f1881-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f1881-248">เวลา วัสดุ และค่าธรรมเนียมของโครงการ P1 รวมอยู่ใน CL1</span><span class="sxs-lookup"><span data-stu-id="f1881-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="f1881-249">ค่าใช้จ่ายในโครงการ P1 รวมอยู่ใน CL2</span><span class="sxs-lookup"><span data-stu-id="f1881-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="f1881-250">ไม่มีการทับซ้อนกันในสิ่งที่รวมอยู่ในรายละเอียดการให้บริการตามสัญญาแต่ละรายการ ดังนั้นจึงถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f1881-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f1881-251">C1</span><span class="sxs-lookup"><span data-stu-id="f1881-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f1881-252">CL2</span><span class="sxs-lookup"><span data-stu-id="f1881-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-253">P1</span><span class="sxs-lookup"><span data-stu-id="f1881-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="f1881-254">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="f1881-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-255">ไม่</span><span class="sxs-lookup"><span data-stu-id="f1881-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-256">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-257">ไม่</span><span class="sxs-lookup"><span data-stu-id="f1881-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-258">ไม่</span><span class="sxs-lookup"><span data-stu-id="f1881-258">No</span></span> </p>
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
<span data-ttu-id="f1881-259">C1</span><span class="sxs-lookup"><span data-stu-id="f1881-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f1881-260">CL1</span><span class="sxs-lookup"><span data-stu-id="f1881-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-261">P1</span><span class="sxs-lookup"><span data-stu-id="f1881-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="f1881-262">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f1881-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-263">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-264">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-265">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-266">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f1881-267">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f1881-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f1881-268">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="f1881-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="f1881-269">C1 รวมเวลา วัสดุ ค่าใช้จ่าย และค่าธรรมเนียมสำหรับชุดงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="f1881-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="f1881-270">CL2 รวมเวลา วัสดุ ค่าใช้จ่าย และค่าธรรมเนียมสำหรับโครงการ P1 ทั้งหมด ดังนั้นจึงทับซ้อนกับสิ่งที่รวมอยู่ใน C1</span><span class="sxs-lookup"><span data-stu-id="f1881-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f1881-271">C1</span><span class="sxs-lookup"><span data-stu-id="f1881-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f1881-272">CL2</span><span class="sxs-lookup"><span data-stu-id="f1881-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-273">P1</span><span class="sxs-lookup"><span data-stu-id="f1881-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="f1881-274">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="f1881-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-275">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-276">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-277">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-278">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-278">Yes</span></span> </p>
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
<span data-ttu-id="f1881-279">C1</span><span class="sxs-lookup"><span data-stu-id="f1881-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f1881-280">CL1</span><span class="sxs-lookup"><span data-stu-id="f1881-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-281">P1</span><span class="sxs-lookup"><span data-stu-id="f1881-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="f1881-282">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f1881-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-283">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-284">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-285">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-286">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f1881-287">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f1881-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f1881-288">ตามกฎ #3</span><span class="sxs-lookup"><span data-stu-id="f1881-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="f1881-289">C1 รวมเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับชุดงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="f1881-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="f1881-290">CL2 รวมเวลา ค่าใช้จ่าย วัสดุ และค่าธรรมเนียมสำหรับชุดงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="f1881-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="f1881-291">การตรวจสอบความถูกต้องเพิ่มเติมเพียงอย่างเดียวคือชุดงานย่อยใน CL1 นั้นแตกต่างจากชุดงานย่อยใน CL2 เพื่อให้แน่ใจว่าไม่มีการทับซ้อนกันที่นั่น</span><span class="sxs-lookup"><span data-stu-id="f1881-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="f1881-292">ระบบดำเนินการนี้ทำได้เมื่อเกี่ยวข้องกับงาน</span><span class="sxs-lookup"><span data-stu-id="f1881-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="f1881-293">C1</span><span class="sxs-lookup"><span data-stu-id="f1881-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f1881-294">CL2</span><span class="sxs-lookup"><span data-stu-id="f1881-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-295">P1</span><span class="sxs-lookup"><span data-stu-id="f1881-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="f1881-296">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f1881-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-297">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f1881-298">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-299">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f1881-300">ใช่</span><span class="sxs-lookup"><span data-stu-id="f1881-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
