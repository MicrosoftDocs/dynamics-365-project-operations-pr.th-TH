---
title: ภาพรวมรายการใบเสนอราคาตามโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการใช้รายการใบเสนอราคาตามโครงการสำหรับงานโครงการ
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369894"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="39f57-103">ภาพรวมรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="39f57-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="39f57-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว, Project Operations สำหรับสถานการณ์ตามทรัพยากร/สินค้าที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="39f57-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="39f57-105">รายการใบเสนอราคาตามโครงการได้รับการออกแบบมาเพื่อช่วยในการประเมินงานโครงการสำหรับการมีส่วนร่วม</span><span class="sxs-lookup"><span data-stu-id="39f57-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="39f57-106">โครงสร้างของรายการใบเสนอราคาตามโครงการมีการขยายสำหรับการประมาณการโครงการด้วยแนวคิดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="39f57-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="39f57-107">วิธีการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="39f57-107">Billing Method</span></span>
- <span data-ttu-id="39f57-108">การแม็ปโครงการและงาน</span><span class="sxs-lookup"><span data-stu-id="39f57-108">Project and Task Mapping</span></span>
- <span data-ttu-id="39f57-109">คลาสธุรกรรมที่รวมไว้</span><span class="sxs-lookup"><span data-stu-id="39f57-109">Included Transaction classes</span></span>
- <span data-ttu-id="39f57-110">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="39f57-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="39f57-111">การตั้งค่าการคิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="39f57-111">Chargeability setup</span></span>
- <span data-ttu-id="39f57-112">การประมาณการโดยใช้รายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="39f57-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="39f57-113">ลูกค้าในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="39f57-113">Quote line Customers</span></span>

<span data-ttu-id="39f57-114">ตารางต่อไปนี้ให้ข้อมูลเกี่ยวกับฟิลด์บนแท็บ **ทั่วไป** ของรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="39f57-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="39f57-115">ฟิลด์เหล่านี้ช่วยตั้งค่าพื้นฐานสำหรับการประมาณการค่าเบื้องต้นอย่างละเอียดสำหรับงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="39f57-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="39f57-116">**ฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="39f57-116">**Field**</span></span> | <span data-ttu-id="39f57-117">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="39f57-117">**Description**</span></span> | <span data-ttu-id="39f57-118">**ผลกระทบขั้นปลาย**</span><span class="sxs-lookup"><span data-stu-id="39f57-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="39f57-119">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="39f57-119">Name</span></span> | <span data-ttu-id="39f57-120">ชื่อของรายการใบเสนอราคาที่ช่วยให้คุณระบุส่วนประกอบที่ไม่ต่อเนื่องของใบเสนอราคาที่กำลังประเมินได้</span><span class="sxs-lookup"><span data-stu-id="39f57-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="39f57-121">คัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="39f57-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="39f57-122">วิธีการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="39f57-122">Billing Method</span></span> | <span data-ttu-id="39f57-123">ในใบเสนอราคาที่สร้างขึ้นจากโอกาสทางการขาย ค่านี้จะมีการคัดลอกจากฟิลด์ที่เกี่ยวข้องในรายการโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="39f57-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="39f57-124">ฟิลด์นี้ประกอบด้วยรูปแบบการทำสัญญาหลักสองแบบที่รองรับโดย Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="39f57-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="39f57-125">- ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="39f57-125">- Fixed price</span></span></br><span data-ttu-id="39f57-126">- เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="39f57-126">- Time and material.</span></span>| <span data-ttu-id="39f57-127">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="39f57-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="39f57-128">Project</span><span class="sxs-lookup"><span data-stu-id="39f57-128">Project</span></span> | <span data-ttu-id="39f57-129">ใช้ฟิลด์ที่ไม่บังคับนี้เพื่อระบุโครงการที่จะใช้เพื่อส่งมอบงานในการมีส่วนร่วมนี้</span><span class="sxs-lookup"><span data-stu-id="39f57-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="39f57-130">เมื่อโครงการถูกแม็ปกับรายการใบเสนอราคา จะช่วยในการตั้งค่างานที่คิดค่าธรมเนียมและยังนำการประมาณราคาตามโครงการไปใช้กับรายการใบเสนอราคาเป็นรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="39f57-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="39f57-131">เมื่อไม่ได้แม็ปโครงการกับรายการใบเสนอราคาตามโครงการ ควรสร้างการประมาณด้วยตนเองโดยการสร้างรายละเอียดรายการใบเสนอราคาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="39f57-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="39f57-132">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="39f57-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="39f57-133">งานที่รวมไว้</span><span class="sxs-lookup"><span data-stu-id="39f57-133">Included Tasks</span></span> | <span data-ttu-id="39f57-134">ระบุว่ารายการใบเสนอราคานี้มีการใช้สำหรับงานโครงการทั้งหมดหรือบางส่วนสำหรับโครงการที่เลือก</span><span class="sxs-lookup"><span data-stu-id="39f57-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="39f57-135">ฟิลด์นี้มีค่าที่เป็นไปได้ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="39f57-135">This field has the following possible values:</span></span></br><span data-ttu-id="39f57-136">- งานโครงการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="39f57-136">- All project tasks</span></span></br><span data-ttu-id="39f57-137">- งานโครงการที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="39f57-137">- Selected project tasks only</span></span></br><span data-ttu-id="39f57-138">ค่าว่างในฟิลด์นี้เทียบเท่ากับตัวเลือก **งานโครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="39f57-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="39f57-139">เมื่อมีการเลือก **งานโครงการที่เลือกเท่านั้น** ในเพจโครงการ แท็บ **การตั้งค่าการเรียกเก็บเงินของงาน** ช่วยให้คุณสามารถเลือกงานเฉพาะเพื่อเชื่อมโยงกับรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="39f57-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="39f57-140">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="39f57-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="39f57-141">รวมเวลา</span><span class="sxs-lookup"><span data-stu-id="39f57-141">Include Time</span></span> | <span data-ttu-id="39f57-142">ค่า **ใช่**/**ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานในโครงการที่เลือกจะรวมอยู่ในประมาณการของรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="39f57-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="39f57-143">ค่า **ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="39f57-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="39f57-144">ค่า **ใช่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="39f57-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="39f57-145">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="39f57-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="39f57-146">รวมค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="39f57-146">Include Expense</span></span> | <span data-ttu-id="39f57-147">ค่า **ใช่**/**ไม่** ระบุว่าต้นทุนค่าใช้จ่ายในโครงการที่เลือกจะรวมอยู่ในประมาณการของรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="39f57-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="39f57-148">ค่า **ไม่** ระบุว่าต้นทุนค่าใช้จ่ายจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="39f57-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="39f57-149">ค่า **ใช่** ระบุว่าต้นทุนค่าใช้จ่ายจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="39f57-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="39f57-150">ค่านี้จะมีการคัดลอกผ่านไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="39f57-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="39f57-151">รวมวัสดุ</span><span class="sxs-lookup"><span data-stu-id="39f57-151">Include Material</span></span> | <span data-ttu-id="39f57-152">ค่า **ใช่**/**ไม่** ระบุว่าต้นทุนวัสดุในโครงการที่เลือกจะรวมอยู่ในประมาณการของรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="39f57-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="39f57-153">ค่า **ไม่** ระบุว่าต้นทุนวัสดุจะไม่รวมอยู่ในประมาณการของรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="39f57-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="39f57-154">ค่า **ใช่** ระบุว่าต้นทุนวัสดุจะรวมอยู่ในประมาณการของรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="39f57-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="39f57-155">ค่านี้จะมีการคัดลอกผ่านไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="39f57-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="39f57-156">รวมค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="39f57-156">Include Fee</span></span> | <span data-ttu-id="39f57-157">ค่า **ใช่**/**ไม่** ระบุว่าต้นทุนค่าธรรมเนียมในโครงการที่เลือกจะรวมอยู่ในประมาณการของรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="39f57-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="39f57-158">ค่า **ไม่** ระบุว่าค่าธรรมเนียมจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="39f57-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="39f57-159">ค่า **ใช่** ระบุว่าค่าธรรมเนียมจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="39f57-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="39f57-160">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="39f57-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="39f57-161">จำนวนเงินตามใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="39f57-161">Quoted Amount</span></span> | <span data-ttu-id="39f57-162">นี่คือจำนวนเงินที่จะเสนอให้กับลูกค้าสำหรับงานทั้งหมดที่คาดการณ์ไว้ในรายการใบเสนอราคาตามโครงการนี้</span><span class="sxs-lookup"><span data-stu-id="39f57-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="39f57-163">ในใบเสนอราคาที่สร้างขึ้นจากโอกาสทางการขาย ค่านี้จะมีการคัดลอกจากฟิลด์ **งบประมาณของลูกค้า** ในรายการโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="39f57-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="39f57-164">เมื่อรายการใบเสนอราคาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและมีการสรุปจากจำนวนเงินในรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="39f57-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="39f57-165">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="39f57-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="39f57-166">ภาษีที่ประเมิน</span><span class="sxs-lookup"><span data-stu-id="39f57-166">Estimated Tax</span></span> | <span data-ttu-id="39f57-167">นี่คือฟิลด์ที่แก้ไขได้สำหรับผู้ใช้ในการเพิ่มจำนวนภาษีโดยประมาณในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="39f57-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="39f57-168">เมื่อรายการใบเสนอราคาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและมีการสรุปจากจำนวนเงินภาษีในรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="39f57-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="39f57-169">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="39f57-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="39f57-170">จำนวนเงินตามใบเสนอราคาหลังหักภาษี</span><span class="sxs-lookup"><span data-stu-id="39f57-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="39f57-171">ฟิลด์นี้คือจำนวนเงินของรายการใบเสนอราคาหลังหักภาษีและเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="39f57-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="39f57-172">จำนวนเงินในฟิลด์นี้มีการคำนวณเป็น *จำนวนเงินที่เสนอราคา + ภาษี*</span><span class="sxs-lookup"><span data-stu-id="39f57-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="39f57-173">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="39f57-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="39f57-174">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="39f57-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="39f57-175">ฟิลด์นี้สามารถแก้ไขได้และพร้อมใช้งานในรายการใบเสนอราคาตามโครงการที่มีวิธีการเรียกเก็บเงินสำหรับ **เวลาและวัสดุ**</span><span class="sxs-lookup"><span data-stu-id="39f57-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="39f57-176">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="39f57-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="39f57-177">งบประมาณของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="39f57-177">Customer Budget</span></span> | <span data-ttu-id="39f57-178">ฟิลด์นี้สามารถแก้ไขได้และมีการคัดลอกจากฟิลด์ที่สัมพันธ์กันในรายการโอกาสทางการขายหากมีการสร้างใบเสนอราคาจากโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="39f57-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="39f57-179">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="39f57-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="39f57-180">กฎการตรวจสอบความถูกต้องสำหรับฟิลด์บนแท็บ ทั่วไป ของรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="39f57-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="39f57-181">**กฎข้อที่ 1**: ถ้าฟิลด์ **งานที่รวมไว้** ว่างเปล่าหรือหากตั้งค่าเป็น **งานโครงการทั้งหมด** โครงการจะรวมอยู่ในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="39f57-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="39f57-182">**กฎข้อที่ 2**: ถ้าฟิลด์ **งานที่รวมไว้** ว่างเปล่าหรือหากตั้งค่าเป็น **งานโครงการทั้งหมด** โครงการและคลาสธุรกรรมบางรายการสามารถรวมอยู่ในรายการใบเสนอราคาตามโครงการของใบเสนอราคาเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="39f57-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="39f57-183">**กฎข้อที่ 3**: ถ้าฟิลด์ **งานที่รวมไว้** ตั้งค่าเป็น **งานโครงการที่เลือกเท่านั้น** โครงการและคลาสธุรกรรมบางรายการสามารถรวมอยู่ในรายการใบเสนอราคาตามโครงการของใบเสนอราคาหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="39f57-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="39f57-184">**กฎข้อที่ 4**: หากโอกาสทางการขายมีใบเสนอราคาหลายใบ สามารถมีรายการใบเสนอราคาจากใบเสนอราคาที่ต่างกันซึ่งการอ้างอิงโครงการเดียวกันทั้งหมดและมีคลาสธุรกรรมเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="39f57-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="39f57-185">**กฎข้อที่ 5**: หากใบเสนอราคาไม่ได้อยู่ในโอกาสทางการขายเดียวกัน ก็จะไม่สามารถรวมโครงการและคลาสธุรกรรมเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="39f57-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="39f57-186">
                    <strong>โอกาสทางการขาย</strong>
                </span><span class="sxs-lookup"><span data-stu-id="39f57-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="39f57-187">
                    <strong>ใบเสนอราคา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="39f57-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="39f57-188">
                    <strong>รายการใบเสนอราคา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="39f57-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="39f57-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="39f57-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="39f57-190">
                    <strong>งานที่รวมไว้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="39f57-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="39f57-191">
                    <strong>รวมเวลา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="39f57-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="39f57-192">
                    <strong>รวมค่าใช้จ่าย</strong>
                </span><span class="sxs-lookup"><span data-stu-id="39f57-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="39f57-193">
                    <strong>รวมวัสดุ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="39f57-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="39f57-194">
                    <strong>รวม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="39f57-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="39f57-195">
                    <strong>ค่าธรรมเนียม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="39f57-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="39f57-196">
                    <strong>ถูกต้อง/ไม่ถูกต้อง</strong>
                </span><span class="sxs-lookup"><span data-stu-id="39f57-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="39f57-197">
                    <strong>เหตุผล</strong>
                </span><span class="sxs-lookup"><span data-stu-id="39f57-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="39f57-198">O1</span><span class="sxs-lookup"><span data-stu-id="39f57-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="39f57-199">Q1</span><span class="sxs-lookup"><span data-stu-id="39f57-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="39f57-200">QL1</span><span class="sxs-lookup"><span data-stu-id="39f57-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-201">P1</span><span class="sxs-lookup"><span data-stu-id="39f57-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="39f57-202">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="39f57-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="39f57-203">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="39f57-204">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="39f57-205">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-206">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="39f57-207">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="39f57-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="39f57-208">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="39f57-208">Violation of Rule #2.</span></span> <span data-ttu-id="39f57-209">เวลา ค่าใช้จ่าย และค่าธรรมเนียมของโครงการ P1 รวมอยู่ในรายการใบเสนอราคา QL1 และ QL2</span><span class="sxs-lookup"><span data-stu-id="39f57-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="39f57-210">O1</span><span class="sxs-lookup"><span data-stu-id="39f57-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="39f57-211">Q1</span><span class="sxs-lookup"><span data-stu-id="39f57-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="39f57-212">QL2</span><span class="sxs-lookup"><span data-stu-id="39f57-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-213">P1</span><span class="sxs-lookup"><span data-stu-id="39f57-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="39f57-214">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="39f57-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="39f57-215">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="39f57-216">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="39f57-217">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-218">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="39f57-219">O1</span><span class="sxs-lookup"><span data-stu-id="39f57-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="39f57-220">Q1</span><span class="sxs-lookup"><span data-stu-id="39f57-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="39f57-221">QL1</span><span class="sxs-lookup"><span data-stu-id="39f57-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-222">P1</span><span class="sxs-lookup"><span data-stu-id="39f57-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="39f57-223">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="39f57-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="39f57-224">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="39f57-225">ไม่</span><span class="sxs-lookup"><span data-stu-id="39f57-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="39f57-226">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-227">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="39f57-228">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="39f57-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="39f57-229">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="39f57-229">Violation of Rule #2.</span></span> <span data-ttu-id="39f57-230">เวลา วัสดุ และค่าธรรมเนียมของโครงการ P1 รวมอยู่ในรายการใบเสนอราคา QL1 และ QL2</span><span class="sxs-lookup"><span data-stu-id="39f57-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="39f57-231">O1</span><span class="sxs-lookup"><span data-stu-id="39f57-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="39f57-232">Q1</span><span class="sxs-lookup"><span data-stu-id="39f57-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="39f57-233">QL2</span><span class="sxs-lookup"><span data-stu-id="39f57-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-234">P1</span><span class="sxs-lookup"><span data-stu-id="39f57-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="39f57-235">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="39f57-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="39f57-236">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="39f57-237">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="39f57-238">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-239">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="39f57-240">O1</span><span class="sxs-lookup"><span data-stu-id="39f57-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="39f57-241">Q1</span><span class="sxs-lookup"><span data-stu-id="39f57-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="39f57-242">QL1</span><span class="sxs-lookup"><span data-stu-id="39f57-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-243">P1</span><span class="sxs-lookup"><span data-stu-id="39f57-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="39f57-244">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="39f57-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="39f57-245">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="39f57-246">ไม่</span><span class="sxs-lookup"><span data-stu-id="39f57-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="39f57-247">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-248">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="39f57-249">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="39f57-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="39f57-250">เวลา วัสดุ และค่าธรรมเนียมของโครงการ P1 รวมอยู่ใน QL1</span><span class="sxs-lookup"><span data-stu-id="39f57-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="39f57-251">ค่าใช้จ่ายในโครงการ P1 รวมอยู่ใน QL2</span><span class="sxs-lookup"><span data-stu-id="39f57-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="39f57-252">ไม่มีการทับซ้อนกันในสิ่งที่รวมอยู่ในรายการใบเสนอราคาแต่ละรายการ ดังนั้นจึงถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="39f57-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="39f57-253">O1</span><span class="sxs-lookup"><span data-stu-id="39f57-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="39f57-254">Q1</span><span class="sxs-lookup"><span data-stu-id="39f57-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="39f57-255">QL2</span><span class="sxs-lookup"><span data-stu-id="39f57-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-256">P1</span><span class="sxs-lookup"><span data-stu-id="39f57-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="39f57-257">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="39f57-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="39f57-258">ไม่</span><span class="sxs-lookup"><span data-stu-id="39f57-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="39f57-259">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="39f57-260">ไม่</span><span class="sxs-lookup"><span data-stu-id="39f57-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-261">ไม่</span><span class="sxs-lookup"><span data-stu-id="39f57-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="39f57-262">O1</span><span class="sxs-lookup"><span data-stu-id="39f57-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="39f57-263">Q1</span><span class="sxs-lookup"><span data-stu-id="39f57-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="39f57-264">QL1</span><span class="sxs-lookup"><span data-stu-id="39f57-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-265">P1</span><span class="sxs-lookup"><span data-stu-id="39f57-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="39f57-266">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="39f57-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="39f57-267">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="39f57-268">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="39f57-269">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-270">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="39f57-271">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="39f57-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="39f57-272">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="39f57-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="39f57-273">Q1 รวมเวลา วัสดุ ค่าใช้จ่าย และค่าธรรมเนียมสำหรับชุดงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="39f57-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="39f57-274">QL2 รวมเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับโครงการ P1 ทั้งหมด ดังนั้นจึงทับซ้อนกับสิ่งที่รวมอยู่ใน Q1</span><span class="sxs-lookup"><span data-stu-id="39f57-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="39f57-275">O1</span><span class="sxs-lookup"><span data-stu-id="39f57-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="39f57-276">Q1</span><span class="sxs-lookup"><span data-stu-id="39f57-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="39f57-277">QL2</span><span class="sxs-lookup"><span data-stu-id="39f57-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-278">P1</span><span class="sxs-lookup"><span data-stu-id="39f57-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="39f57-279">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="39f57-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="39f57-280">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="39f57-281">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="39f57-282">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-283">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="39f57-284">O1</span><span class="sxs-lookup"><span data-stu-id="39f57-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="39f57-285">Q1</span><span class="sxs-lookup"><span data-stu-id="39f57-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="39f57-286">QL1</span><span class="sxs-lookup"><span data-stu-id="39f57-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-287">P1</span><span class="sxs-lookup"><span data-stu-id="39f57-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="39f57-288">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="39f57-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="39f57-289">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="39f57-290">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="39f57-291">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-292">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="39f57-293">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="39f57-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="39f57-294">ตามกฎ #3</span><span class="sxs-lookup"><span data-stu-id="39f57-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="39f57-295">Q1 รวมเวลา วัสดุ ค่าใช้จ่าย และค่าธรรมเนียมสำหรับชุดงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="39f57-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="39f57-296">QL2 รวมเวลา วัสดุ ค่าใช้จ่าย และค่าธรรมเนียมสำหรับชุดงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="39f57-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="39f57-297">การตรวจสอบความถูกต้องเพิ่มเติมเพียงอย่างเดียวคือชุดงานย่อยใน QL1 ซึ่งแตกต่างจากชุดงานย่อยใน QL2 เพื่อให้แน่ใจว่าไม่มีการทับซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="39f57-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="39f57-298">ระบบดำเนินการนี้ทำได้เมื่อเกี่ยวข้องกับงาน</span><span class="sxs-lookup"><span data-stu-id="39f57-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="39f57-299">O1</span><span class="sxs-lookup"><span data-stu-id="39f57-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="39f57-300">Q1</span><span class="sxs-lookup"><span data-stu-id="39f57-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="39f57-301">QL2</span><span class="sxs-lookup"><span data-stu-id="39f57-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-302">P1</span><span class="sxs-lookup"><span data-stu-id="39f57-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="39f57-303">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="39f57-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="39f57-304">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="39f57-305">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="39f57-306">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-307">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="39f57-308">O1</span><span class="sxs-lookup"><span data-stu-id="39f57-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="39f57-309">Q1</span><span class="sxs-lookup"><span data-stu-id="39f57-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="39f57-310">QL1</span><span class="sxs-lookup"><span data-stu-id="39f57-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-311">P1</span><span class="sxs-lookup"><span data-stu-id="39f57-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="39f57-312">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="39f57-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="39f57-313">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="39f57-314">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="39f57-315">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-316">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="39f57-317">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="39f57-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="39f57-318">ตามกฎ #5, Q1 และ Q2 เป็นใบเสนอราคาสองรายการในโอกาสทางการขายเดียวกัน ดังนั้นทั้งคู่จึงสามารถประมาณการองค์ประกอบเดียวกันของโครงการได้</span><span class="sxs-lookup"><span data-stu-id="39f57-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="39f57-319">O1</span><span class="sxs-lookup"><span data-stu-id="39f57-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="39f57-320">Q2</span><span class="sxs-lookup"><span data-stu-id="39f57-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="39f57-321">QL1</span><span class="sxs-lookup"><span data-stu-id="39f57-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-322">P1</span><span class="sxs-lookup"><span data-stu-id="39f57-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="39f57-323">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="39f57-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="39f57-324">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="39f57-325">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="39f57-326">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-327">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="39f57-328">O1</span><span class="sxs-lookup"><span data-stu-id="39f57-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="39f57-329">Q1</span><span class="sxs-lookup"><span data-stu-id="39f57-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="39f57-330">QL1</span><span class="sxs-lookup"><span data-stu-id="39f57-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-331">P1</span><span class="sxs-lookup"><span data-stu-id="39f57-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="39f57-332">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="39f57-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="39f57-333">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="39f57-334">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="39f57-335">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-336">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="39f57-337">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="39f57-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="39f57-338">ตามกฎ #4, Q1 และ Q2 เป็นใบเสนอราคาสองรายการในโอกาสทางการขายที่ต่างกัน ดังนั้นทั้งคู่จึงไม่สามารถประมาณการองค์ประกอบเดียวกันของโครงการเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="39f57-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="39f57-339">O2</span><span class="sxs-lookup"><span data-stu-id="39f57-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="39f57-340">Q1</span><span class="sxs-lookup"><span data-stu-id="39f57-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="39f57-341">QL1</span><span class="sxs-lookup"><span data-stu-id="39f57-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-342">P1</span><span class="sxs-lookup"><span data-stu-id="39f57-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="39f57-343">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="39f57-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="39f57-344">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="39f57-345">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="39f57-346">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="39f57-347">ใช่</span><span class="sxs-lookup"><span data-stu-id="39f57-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
