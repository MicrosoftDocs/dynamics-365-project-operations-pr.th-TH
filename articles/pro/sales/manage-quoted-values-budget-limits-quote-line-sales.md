---
title: ภาพรวมรายการใบเสนอราคาตามโครงการ - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการใช้รายการใบเสนอราคาตามโครงการสำหรับงานโครงการ (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181115"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="88571-104">ภาพรวมรายการใบเสนอราคาตามโครงการ - Lite</span><span class="sxs-lookup"><span data-stu-id="88571-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="88571-105">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="88571-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="88571-106">รายการใบเสนอราคาตามโครงการได้รับการออกแบบมาเพื่อช่วยในการประเมินงานโครงการสำหรับการมีส่วนร่วม</span><span class="sxs-lookup"><span data-stu-id="88571-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="88571-107">โครงสร้างของรายการใบเสนอราคาตามโครงการมีการขยายสำหรับการประมาณการโครงการด้วยแนวคิดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88571-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="88571-108">วิธีการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="88571-108">Billing Method</span></span>
- <span data-ttu-id="88571-109">การแม็ปโครงการและงาน</span><span class="sxs-lookup"><span data-stu-id="88571-109">Project and Task Mapping</span></span>
- <span data-ttu-id="88571-110">คลาสธุรกรรมที่รวมไว้</span><span class="sxs-lookup"><span data-stu-id="88571-110">Included Transaction classes</span></span>
- <span data-ttu-id="88571-111">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="88571-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="88571-112">การตั้งค่าการคิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="88571-112">Chargeability setup</span></span>
- <span data-ttu-id="88571-113">การประมาณการโดยใช้รายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="88571-114">ลูกค้าในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-114">Quote line Customers</span></span>

<span data-ttu-id="88571-115">ตารางต่อไปนี้ให้ข้อมูลเกี่ยวกับฟิลด์บนแท็บ **ทั่วไป** ของรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="88571-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="88571-116">ฟิลด์เหล่านี้ช่วยตั้งค่าพื้นฐานสำหรับการประมาณการค่าเบื้องต้นอย่างละเอียดสำหรับงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="88571-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="88571-117">**ฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="88571-117">**Field**</span></span> | <span data-ttu-id="88571-118">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="88571-118">**Description**</span></span> | <span data-ttu-id="88571-119">**ผลกระทบขั้นปลาย**</span><span class="sxs-lookup"><span data-stu-id="88571-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="88571-120">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="88571-120">Name</span></span> | <span data-ttu-id="88571-121">ชื่อของรายการใบเสนอราคาที่จะช่วยคุณระบุส่วนประกอบที่ไม่ต่อเนื่องของใบเสนอราคาที่กำลังประมาณการ</span><span class="sxs-lookup"><span data-stu-id="88571-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="88571-122">คัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="88571-123">วิธีการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="88571-123">Billing Method</span></span> | <span data-ttu-id="88571-124">ในใบเสนอราคาที่สร้างขึ้นจากโอกาสทางการขาย ค่านี้จะมีการคัดลอกจากฟิลด์ที่เกี่ยวข้องในรายการโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="88571-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="88571-125">ฟิลด์นี้ประกอบด้วยรูปแบบการทำสัญญาหลักสองแบบที่สนับสนุนโดย Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="88571-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="88571-126">- ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="88571-126">- Fixed price</span></span></br><span data-ttu-id="88571-127">- เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="88571-127">- Time and material.</span></span>| <span data-ttu-id="88571-128">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="88571-129">Project</span><span class="sxs-lookup"><span data-stu-id="88571-129">Project</span></span> | <span data-ttu-id="88571-130">ใช้ฟิลด์ที่ไม่บังคับนี้เพื่อระบุโครงการที่จะใช้เพื่อส่งมอบงานในการมีส่วนร่วมนี้</span><span class="sxs-lookup"><span data-stu-id="88571-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="88571-131">เมื่อโครงการถูกแม็ปกับรายการใบเสนอราคา จะช่วยในการตั้งค่างานที่คิดค่าธรมเนียมและยังนำการประมาณราคาตามโครงการไปใช้กับรายการใบเสนอราคาเป็นรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="88571-132">เมื่อไม่ได้แม็ปโครงการกับรายการใบเสนอราคาตามโครงการ ควรสร้างการประมาณด้วยตนเองโดยการสร้างรายละเอียดรายการใบเสนอราคาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="88571-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="88571-133">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="88571-134">งานที่รวมไว้</span><span class="sxs-lookup"><span data-stu-id="88571-134">Included Tasks</span></span> | <span data-ttu-id="88571-135">ระบุว่ารายการใบเสนอราคานี้มีการใช้สำหรับงานโครงการทั้งหมดหรือบางส่วนสำหรับโครงการที่เลือก</span><span class="sxs-lookup"><span data-stu-id="88571-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="88571-136">ฟิลด์นี้มีค่าที่เป็นไปได้ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88571-136">This field has the following possible values:</span></span></br><span data-ttu-id="88571-137">- งานโครงการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="88571-137">- All project tasks</span></span></br><span data-ttu-id="88571-138">- งานโครงการที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="88571-138">- Selected project tasks only</span></span></br><span data-ttu-id="88571-139">ค่าว่างในฟิลด์นี้เทียบเท่ากับตัวเลือก **งานโครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="88571-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="88571-140">เมื่อมีการเลือก **งานโครงการที่เลือกเท่านั้น** จากนั้นในเพจโครงการ แท็บ **การตั้งค่าการเรียกเก็บเงินงาน** ช่วยให้คุณสามารถเลือกงานเฉพาะเพื่อเชื่อมโยงกับรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="88571-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="88571-141">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="88571-142">รวมเวลา</span><span class="sxs-lookup"><span data-stu-id="88571-142">Include Time</span></span> | <span data-ttu-id="88571-143">ค่าสถานะ **ใช่**/**ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานในโครงการที่เลือกจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="88571-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="88571-144">ค่า **ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="88571-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="88571-145">ค่า **ใช่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="88571-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="88571-146">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="88571-147">รวมค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="88571-147">Include Expense</span></span> | <span data-ttu-id="88571-148">ค่าสถานะ **ใช่**/**ไม่** ระบุว่าต้นทุนค่าใช้จ่ายในโครงการที่เลือกจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="88571-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="88571-149">ค่า **ไม่** ระบุว่าต้นทุนค่าใช้จ่ายจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="88571-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="88571-150">ค่า **ใช่** ระบุว่าต้นทุนค่าใช้จ่ายจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="88571-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="88571-151">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="88571-152">รวมค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="88571-152">Include Fee</span></span> | <span data-ttu-id="88571-153">ค่าสถานะ **ใช่**/**ไม่** ระบุว่าค่าธรรมเนียมในโครงการที่เลือกจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="88571-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="88571-154">ค่า **ไม่** ระบุว่าต้นทุนค่าธรรมเนียมจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="88571-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="88571-155">ค่า **ใช่** ระบุว่าต้นทุนค่าธรรมเนียมจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="88571-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="88571-156">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="88571-157">จำนวนเงินตามใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-157">Quoted Amount</span></span> | <span data-ttu-id="88571-158">นี่คือจำนวนเงินที่จะเสนอให้กับลูกค้าสำหรับงานทั้งหมดที่คาดการณ์ไว้ในรายการใบเสนอราคาตามโครงการนี้</span><span class="sxs-lookup"><span data-stu-id="88571-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="88571-159">ในใบเสนอราคาที่สร้างขึ้นจากโอกาสทางการขาย ค่านี้จะมีการคัดลอกจากฟิลด์ **งบประมาณของลูกค้า** ในรายการโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="88571-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="88571-160">เมื่อรายการใบเสนอราคาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและมีการสรุปจากจำนวนเงินในรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="88571-161">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="88571-162">ภาษีที่ประเมิน</span><span class="sxs-lookup"><span data-stu-id="88571-162">Estimated Tax</span></span> | <span data-ttu-id="88571-163">นี่คือฟิลด์ที่แก้ไขได้สำหรับผู้ใช้ในการเพิ่มจำนวนภาษีโดยประมาณในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="88571-164">เมื่อรายการใบเสนอราคาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและมีการสรุปจากจำนวนเงินภาษีในรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="88571-165">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="88571-166">จำนวนเงินตามใบเสนอราคาหลังหักภาษี</span><span class="sxs-lookup"><span data-stu-id="88571-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="88571-167">ฟิลด์นี้คือจำนวนเงินของรายการใบเสนอราคาหลังหักภาษีและเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="88571-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="88571-168">จำนวนเงินในฟิลด์นี้มีการคำนวณเป็น *จำนวนเงินที่เสนอราคา + ภาษี*</span><span class="sxs-lookup"><span data-stu-id="88571-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="88571-169">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="88571-170">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="88571-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="88571-171">ฟิลด์นี้สามารถแก้ไขได้และพร้อมใช้งานในรายการใบเสนอราคาตามโครงการที่มีวิธีการเรียกเก็บเงินสำหรับ **เวลาและวัสดุ**</span><span class="sxs-lookup"><span data-stu-id="88571-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="88571-172">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="88571-173">งบประมาณของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="88571-173">Customer Budget</span></span> | <span data-ttu-id="88571-174">ฟิลด์นี้สามารถแก้ไขได้และมีการคัดลอกจากฟิลด์ที่สัมพันธ์กันในรายการโอกาสทางการขายหากมีการสร้างใบเสนอราคาจากโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="88571-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="88571-175">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="88571-176">กฎการตรวจสอบความถูกต้องสำหรับฟิลด์บนแท็บ ทั่วไป ของรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="88571-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="88571-177">**กฎข้อที่ 1**: ถ้าฟิลด์ **งานที่รวมไว้** ว่างเปล่าหรือหากตั้งค่าเป็น **งานโครงการทั้งหมด** โครงการจะรวมอยู่ในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="88571-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="88571-178">**กฎข้อที่ 2**: ถ้าฟิลด์ **งานที่รวมไว้** ว่างเปล่าหรือหากตั้งค่าเป็น **งานโครงการทั้งหมด** โครงการและคลาสธุรกรรมบางรายการสามารถรวมอยู่ในรายการใบเสนอราคาตามโครงการของใบเสนอราคาเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="88571-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="88571-179">**กฎข้อที่ 3**: ถ้าฟิลด์ **งานที่รวมไว้** ตั้งค่าเป็น **งานโครงการที่เลือกเท่านั้น** โครงการและคลาสธุรกรรมบางรายการสามารถรวมอยู่ในรายการใบเสนอราคาตามโครงการของใบเสนอราคาหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="88571-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="88571-180">**กฎข้อที่ 4**: หากโอกาสทางการขายมีใบเสนอราคาหลายใบ สามารถมีรายการใบเสนอราคาจากใบเสนอราคาที่ต่างกันซึ่งการอ้างอิงโครงการเดียวกันทั้งหมดและมีคลาสธุรกรรมเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="88571-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="88571-181">**กฎข้อที่ 5**: หากใบเสนอราคาไม่ได้อยู่ในโอกาสทางการขายเดียวกัน ก็จะไม่สามารถรวมโครงการและคลาสธุรกรรมเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="88571-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="88571-182">
                    <strong>โอกาสทางการขาย</strong>
                </span><span class="sxs-lookup"><span data-stu-id="88571-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="88571-183">
                    <strong>ใบเสนอราคา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="88571-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="88571-184">
                    <strong>รายการใบเสนอราคา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="88571-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="88571-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="88571-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="88571-186">
                    <strong>งานที่รวมไว้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="88571-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="88571-187">
                    <strong>รวมเวลา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="88571-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="88571-188">
                    <strong>รวมค่าใช้จ่าย</strong>
                </span><span class="sxs-lookup"><span data-stu-id="88571-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="88571-189">
                    <strong>รวม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="88571-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="88571-190">
                    <strong>ค่าธรรมเนียม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="88571-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="88571-191">
                    <strong>ถูกต้อง/ไม่ถูกต้อง</strong>
                </span><span class="sxs-lookup"><span data-stu-id="88571-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="88571-192">
                    <strong>เหตุผล</strong>
                </span><span class="sxs-lookup"><span data-stu-id="88571-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="88571-193">O1</span><span class="sxs-lookup"><span data-stu-id="88571-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="88571-194">Q1</span><span class="sxs-lookup"><span data-stu-id="88571-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-195">QL1</span><span class="sxs-lookup"><span data-stu-id="88571-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-196">ร1</span><span class="sxs-lookup"><span data-stu-id="88571-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="88571-197">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="88571-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-198">มี</span><span class="sxs-lookup"><span data-stu-id="88571-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-199">มี</span><span class="sxs-lookup"><span data-stu-id="88571-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-200">มี</span><span class="sxs-lookup"><span data-stu-id="88571-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88571-201">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="88571-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88571-202">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="88571-202">Violation of Rule #2.</span></span> <span data-ttu-id="88571-203">เวลา ค่าใช้จ่าย และค่าธรรมเนียมของโครงการ P1 รวมอยู่ในรายการใบเสนอราคา QL1 และ QL2</span><span class="sxs-lookup"><span data-stu-id="88571-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="88571-204">O1</span><span class="sxs-lookup"><span data-stu-id="88571-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="88571-205">Q1</span><span class="sxs-lookup"><span data-stu-id="88571-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-206">QL2</span><span class="sxs-lookup"><span data-stu-id="88571-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-207">ร1</span><span class="sxs-lookup"><span data-stu-id="88571-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="88571-208">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="88571-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-209">มี</span><span class="sxs-lookup"><span data-stu-id="88571-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-210">มี</span><span class="sxs-lookup"><span data-stu-id="88571-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-211">มี</span><span class="sxs-lookup"><span data-stu-id="88571-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="88571-212">O1</span><span class="sxs-lookup"><span data-stu-id="88571-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="88571-213">Q1</span><span class="sxs-lookup"><span data-stu-id="88571-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-214">QL1</span><span class="sxs-lookup"><span data-stu-id="88571-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-215">ร1</span><span class="sxs-lookup"><span data-stu-id="88571-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="88571-216">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="88571-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-217">มี</span><span class="sxs-lookup"><span data-stu-id="88571-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-218">No</span><span class="sxs-lookup"><span data-stu-id="88571-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-219">มี</span><span class="sxs-lookup"><span data-stu-id="88571-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88571-220">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="88571-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88571-221">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="88571-221">Violation of Rule #2.</span></span> <span data-ttu-id="88571-222">เวลาและค่าธรรมเนียมของโครงการ P1 รวมอยู่ในรายการใบเสนอราคา QL1 และ QL2</span><span class="sxs-lookup"><span data-stu-id="88571-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="88571-223">O1</span><span class="sxs-lookup"><span data-stu-id="88571-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="88571-224">Q1</span><span class="sxs-lookup"><span data-stu-id="88571-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-225">QL2</span><span class="sxs-lookup"><span data-stu-id="88571-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-226">ร1</span><span class="sxs-lookup"><span data-stu-id="88571-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="88571-227">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="88571-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-228">มี</span><span class="sxs-lookup"><span data-stu-id="88571-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-229">มี</span><span class="sxs-lookup"><span data-stu-id="88571-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-230">มี</span><span class="sxs-lookup"><span data-stu-id="88571-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="88571-231">O1</span><span class="sxs-lookup"><span data-stu-id="88571-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="88571-232">Q1</span><span class="sxs-lookup"><span data-stu-id="88571-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-233">QL1</span><span class="sxs-lookup"><span data-stu-id="88571-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-234">ร1</span><span class="sxs-lookup"><span data-stu-id="88571-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="88571-235">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="88571-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-236">มี</span><span class="sxs-lookup"><span data-stu-id="88571-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-237">No</span><span class="sxs-lookup"><span data-stu-id="88571-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-238">มี</span><span class="sxs-lookup"><span data-stu-id="88571-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88571-239">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="88571-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="88571-240">เวลาและค่าธรรมเนียมของโครงการ P1 รวมอยู่ใน QL1</span><span class="sxs-lookup"><span data-stu-id="88571-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="88571-241">ค่าใช้จ่ายในโครงการ P1 รวมอยู่ใน QL2</span><span class="sxs-lookup"><span data-stu-id="88571-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="88571-242">ไม่มีการทับซ้อนกันในสิ่งที่รวมอยู่ในแต่ละรายการใบเสนอราคา และจะถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="88571-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="88571-243">O1</span><span class="sxs-lookup"><span data-stu-id="88571-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="88571-244">Q1</span><span class="sxs-lookup"><span data-stu-id="88571-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-245">QL2</span><span class="sxs-lookup"><span data-stu-id="88571-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-246">ร1</span><span class="sxs-lookup"><span data-stu-id="88571-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="88571-247">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="88571-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-248">No</span><span class="sxs-lookup"><span data-stu-id="88571-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-249">มี</span><span class="sxs-lookup"><span data-stu-id="88571-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-250">No</span><span class="sxs-lookup"><span data-stu-id="88571-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="88571-251">O1</span><span class="sxs-lookup"><span data-stu-id="88571-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="88571-252">Q1</span><span class="sxs-lookup"><span data-stu-id="88571-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-253">QL1</span><span class="sxs-lookup"><span data-stu-id="88571-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-254">ร1</span><span class="sxs-lookup"><span data-stu-id="88571-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="88571-255">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="88571-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-256">มี</span><span class="sxs-lookup"><span data-stu-id="88571-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-257">มี</span><span class="sxs-lookup"><span data-stu-id="88571-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-258">มี</span><span class="sxs-lookup"><span data-stu-id="88571-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88571-259">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="88571-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88571-260">การละเมิดกฎ #2 ข้างต้น</span><span class="sxs-lookup"><span data-stu-id="88571-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="88571-261">Q1 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="88571-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="88571-262">QL2 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับโครงการ P1 ทั้งหมดและทับซ้อนกับสิ่งที่รวมอยู่ใน Q1</span><span class="sxs-lookup"><span data-stu-id="88571-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="88571-263">O1</span><span class="sxs-lookup"><span data-stu-id="88571-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="88571-264">Q1</span><span class="sxs-lookup"><span data-stu-id="88571-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-265">QL2</span><span class="sxs-lookup"><span data-stu-id="88571-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-266">ร1</span><span class="sxs-lookup"><span data-stu-id="88571-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="88571-267">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="88571-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-268">มี</span><span class="sxs-lookup"><span data-stu-id="88571-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-269">มี</span><span class="sxs-lookup"><span data-stu-id="88571-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-270">มี</span><span class="sxs-lookup"><span data-stu-id="88571-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="88571-271">O1</span><span class="sxs-lookup"><span data-stu-id="88571-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="88571-272">Q1</span><span class="sxs-lookup"><span data-stu-id="88571-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-273">QL1</span><span class="sxs-lookup"><span data-stu-id="88571-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-274">ร1</span><span class="sxs-lookup"><span data-stu-id="88571-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="88571-275">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="88571-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-276">มี</span><span class="sxs-lookup"><span data-stu-id="88571-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-277">มี</span><span class="sxs-lookup"><span data-stu-id="88571-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-278">มี</span><span class="sxs-lookup"><span data-stu-id="88571-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88571-279">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="88571-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88571-280">ตามกฎ #3 ข้างต้น</span><span class="sxs-lookup"><span data-stu-id="88571-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="88571-281">Q1 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="88571-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="88571-282">QL2 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="88571-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="88571-283">การตรวจสอบความถูกต้องเพิ่มเติมเพียงอย่างเดียวคือชุดย่อยของงานบน QL1 ซึ่งแตกต่างจากชุดย่อยของงานบน QL2</span><span class="sxs-lookup"><span data-stu-id="88571-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="88571-284">เพื่อให้แน่ใจว่าไม่มีการทับซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="88571-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="88571-285">ระบบดำเนินการนี้ทำได้เมื่อเกี่ยวข้องกับงาน</span><span class="sxs-lookup"><span data-stu-id="88571-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="88571-286">O1</span><span class="sxs-lookup"><span data-stu-id="88571-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="88571-287">Q1</span><span class="sxs-lookup"><span data-stu-id="88571-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-288">QL2</span><span class="sxs-lookup"><span data-stu-id="88571-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-289">ร1</span><span class="sxs-lookup"><span data-stu-id="88571-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="88571-290">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="88571-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-291">มี</span><span class="sxs-lookup"><span data-stu-id="88571-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-292">มี</span><span class="sxs-lookup"><span data-stu-id="88571-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-293">มี</span><span class="sxs-lookup"><span data-stu-id="88571-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="88571-294">O1</span><span class="sxs-lookup"><span data-stu-id="88571-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="88571-295">Q1</span><span class="sxs-lookup"><span data-stu-id="88571-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-296">QL1</span><span class="sxs-lookup"><span data-stu-id="88571-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-297">ร1</span><span class="sxs-lookup"><span data-stu-id="88571-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="88571-298">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="88571-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-299">มี</span><span class="sxs-lookup"><span data-stu-id="88571-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-300">มี</span><span class="sxs-lookup"><span data-stu-id="88571-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-301">มี</span><span class="sxs-lookup"><span data-stu-id="88571-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="88571-302">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="88571-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88571-303">ตามกฎ #5, Q1 และ Q2 เป็นใบเสนอราคาสองรายการในโอกาสทางการขายเดียวกัน ดังนั้นทั้งคู่จึงสามารถประมาณการสำหรับส่วนประกอบเดียวกันของโครงการได้</span><span class="sxs-lookup"><span data-stu-id="88571-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="88571-304">O1</span><span class="sxs-lookup"><span data-stu-id="88571-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="88571-305">Q2</span><span class="sxs-lookup"><span data-stu-id="88571-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-306">QL1</span><span class="sxs-lookup"><span data-stu-id="88571-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-307">ร1</span><span class="sxs-lookup"><span data-stu-id="88571-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="88571-308">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="88571-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-309">มี</span><span class="sxs-lookup"><span data-stu-id="88571-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-310">มี</span><span class="sxs-lookup"><span data-stu-id="88571-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-311">มี</span><span class="sxs-lookup"><span data-stu-id="88571-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="88571-312">O1</span><span class="sxs-lookup"><span data-stu-id="88571-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="88571-313">Q1</span><span class="sxs-lookup"><span data-stu-id="88571-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-314">QL1</span><span class="sxs-lookup"><span data-stu-id="88571-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-315">ร1</span><span class="sxs-lookup"><span data-stu-id="88571-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="88571-316">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="88571-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-317">มี</span><span class="sxs-lookup"><span data-stu-id="88571-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-318">มี</span><span class="sxs-lookup"><span data-stu-id="88571-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-319">มี</span><span class="sxs-lookup"><span data-stu-id="88571-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="88571-320">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="88571-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="88571-321">ตามกฎ #4, Q1 และ Q2 เป็นใบเสนอราคาสองรายการในโอกาสทางการขายที่ต่างกัน ดังนั้นทั้งคู่จึงสามารถประมาณการสำหรับส่วนประกอบเดียวกันของโครงการเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="88571-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="88571-322">O2</span><span class="sxs-lookup"><span data-stu-id="88571-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="88571-323">Q1</span><span class="sxs-lookup"><span data-stu-id="88571-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-324">QL1</span><span class="sxs-lookup"><span data-stu-id="88571-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-325">ร1</span><span class="sxs-lookup"><span data-stu-id="88571-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="88571-326">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="88571-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-327">มี</span><span class="sxs-lookup"><span data-stu-id="88571-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="88571-328">มี</span><span class="sxs-lookup"><span data-stu-id="88571-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="88571-329">มี</span><span class="sxs-lookup"><span data-stu-id="88571-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="88571-330">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="88571-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

