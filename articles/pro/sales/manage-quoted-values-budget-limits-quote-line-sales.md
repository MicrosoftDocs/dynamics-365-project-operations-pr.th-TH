---
title: ภาพรวมรายการใบเสนอราคาตามโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการใช้รายการใบเสนอราคาตามโครงการสำหรับงานโครงการ
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cfe98fc89130c93dd0a36af8583881fdcb4550c0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858721"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="5e396-103">ภาพรวมรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="5e396-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="5e396-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว, Project Operations สำหรับสถานการณ์ตามทรัพยากร/สินค้าที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="5e396-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5e396-105">รายการใบเสนอราคาตามโครงการได้รับการออกแบบมาเพื่อช่วยในการประเมินงานโครงการสำหรับการมีส่วนร่วม</span><span class="sxs-lookup"><span data-stu-id="5e396-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="5e396-106">โครงสร้างของรายการใบเสนอราคาตามโครงการมีการขยายสำหรับการประมาณการโครงการด้วยแนวคิดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5e396-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="5e396-107">วิธีการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="5e396-107">Billing Method</span></span>
- <span data-ttu-id="5e396-108">การแม็ปโครงการและงาน</span><span class="sxs-lookup"><span data-stu-id="5e396-108">Project and Task Mapping</span></span>
- <span data-ttu-id="5e396-109">คลาสธุรกรรมที่รวมไว้</span><span class="sxs-lookup"><span data-stu-id="5e396-109">Included Transaction classes</span></span>
- <span data-ttu-id="5e396-110">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="5e396-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="5e396-111">การตั้งค่าการคิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="5e396-111">Chargeability setup</span></span>
- <span data-ttu-id="5e396-112">การประมาณการโดยใช้รายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="5e396-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="5e396-113">ลูกค้าในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="5e396-113">Quote line Customers</span></span>

<span data-ttu-id="5e396-114">ตารางต่อไปนี้ให้ข้อมูลเกี่ยวกับฟิลด์บนแท็บ **ทั่วไป** ของรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="5e396-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="5e396-115">ฟิลด์เหล่านี้ช่วยตั้งค่าพื้นฐานสำหรับการประมาณการค่าเบื้องต้นอย่างละเอียดสำหรับงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="5e396-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="5e396-116">**ฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="5e396-116">**Field**</span></span> | <span data-ttu-id="5e396-117">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="5e396-117">**Description**</span></span> | <span data-ttu-id="5e396-118">**ผลกระทบขั้นปลาย**</span><span class="sxs-lookup"><span data-stu-id="5e396-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5e396-119">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="5e396-119">Name</span></span> | <span data-ttu-id="5e396-120">ชื่อของรายการใบเสนอราคาที่ช่วยให้คุณระบุส่วนประกอบที่ไม่ต่อเนื่องของใบเสนอราคาที่กำลังประเมินได้</span><span class="sxs-lookup"><span data-stu-id="5e396-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="5e396-121">คัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="5e396-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5e396-122">วิธีการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="5e396-122">Billing Method</span></span> | <span data-ttu-id="5e396-123">ในใบเสนอราคาที่สร้างขึ้นจากโอกาสทางการขาย ค่านี้จะมีการคัดลอกจากฟิลด์ที่เกี่ยวข้องในรายการโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="5e396-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="5e396-124">ฟิลด์นี้ประกอบด้วยรูปแบบการทำสัญญาหลักสองแบบที่รองรับโดย Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="5e396-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="5e396-125">- ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="5e396-125">- Fixed price</span></span></br><span data-ttu-id="5e396-126">- เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="5e396-126">- Time and material.</span></span>| <span data-ttu-id="5e396-127">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="5e396-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5e396-128">Project</span><span class="sxs-lookup"><span data-stu-id="5e396-128">Project</span></span> | <span data-ttu-id="5e396-129">ใช้ฟิลด์ที่ไม่บังคับนี้เพื่อระบุโครงการที่จะใช้เพื่อส่งมอบงานในการมีส่วนร่วมนี้</span><span class="sxs-lookup"><span data-stu-id="5e396-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="5e396-130">เมื่อโครงการถูกแม็ปกับรายการใบเสนอราคา จะช่วยในการตั้งค่างานที่คิดค่าธรมเนียมและยังนำการประมาณราคาตามโครงการไปใช้กับรายการใบเสนอราคาเป็นรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="5e396-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="5e396-131">เมื่อไม่ได้แม็ปโครงการกับรายการใบเสนอราคาตามโครงการ ควรสร้างการประมาณด้วยตนเองโดยการสร้างรายละเอียดรายการใบเสนอราคาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="5e396-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="5e396-132">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="5e396-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="5e396-133">งานที่รวมไว้</span><span class="sxs-lookup"><span data-stu-id="5e396-133">Included Tasks</span></span> | <span data-ttu-id="5e396-134">ระบุว่ารายการใบเสนอราคานี้มีการใช้สำหรับงานโครงการทั้งหมดหรือบางส่วนสำหรับโครงการที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5e396-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="5e396-135">ฟิลด์นี้มีค่าที่เป็นไปได้ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5e396-135">This field has the following possible values:</span></span></br><span data-ttu-id="5e396-136">- งานโครงการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5e396-136">- All project tasks</span></span></br><span data-ttu-id="5e396-137">- งานโครงการที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5e396-137">- Selected project tasks only</span></span></br><span data-ttu-id="5e396-138">ค่าว่างในฟิลด์นี้เทียบเท่ากับตัวเลือก **งานโครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="5e396-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="5e396-139">เมื่อมีการเลือก **งานโครงการที่เลือกเท่านั้น** ในเพจโครงการ แท็บ **การตั้งค่าการเรียกเก็บเงินของงาน** ช่วยให้คุณสามารถเลือกงานเฉพาะเพื่อเชื่อมโยงกับรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="5e396-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="5e396-140">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="5e396-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5e396-141">รวมเวลา</span><span class="sxs-lookup"><span data-stu-id="5e396-141">Include Time</span></span> | <span data-ttu-id="5e396-142">ค่า **ใช่**/**ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานในโครงการที่เลือกจะรวมอยู่ในประมาณการของรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="5e396-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5e396-143">ค่า **ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="5e396-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5e396-144">ค่า **ใช่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="5e396-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5e396-145">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="5e396-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5e396-146">รวมค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="5e396-146">Include Expense</span></span> | <span data-ttu-id="5e396-147">ค่า **ใช่**/**ไม่** ระบุว่าต้นทุนค่าใช้จ่ายในโครงการที่เลือกจะรวมอยู่ในประมาณการของรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="5e396-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5e396-148">ค่า **ไม่** ระบุว่าต้นทุนค่าใช้จ่ายจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="5e396-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5e396-149">ค่า **ใช่** ระบุว่าต้นทุนค่าใช้จ่ายจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="5e396-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5e396-150">ค่านี้จะมีการคัดลอกผ่านไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="5e396-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5e396-151">รวมวัสดุ</span><span class="sxs-lookup"><span data-stu-id="5e396-151">Include Material</span></span> | <span data-ttu-id="5e396-152">ค่า **ใช่**/**ไม่** ระบุว่าต้นทุนวัสดุในโครงการที่เลือกจะรวมอยู่ในประมาณการของรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="5e396-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5e396-153">ค่า **ไม่** ระบุว่าต้นทุนวัสดุจะไม่รวมอยู่ในประมาณการของรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="5e396-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5e396-154">ค่า **ใช่** ระบุว่าต้นทุนวัสดุจะรวมอยู่ในประมาณการของรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="5e396-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5e396-155">ค่านี้จะมีการคัดลอกผ่านไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="5e396-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5e396-156">รวมค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="5e396-156">Include Fee</span></span> | <span data-ttu-id="5e396-157">ค่า **ใช่**/**ไม่** ระบุว่าต้นทุนค่าธรรมเนียมในโครงการที่เลือกจะรวมอยู่ในประมาณการของรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="5e396-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5e396-158">ค่า **ไม่** ระบุว่าค่าธรรมเนียมจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="5e396-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5e396-159">ค่า **ใช่** ระบุว่าค่าธรรมเนียมจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="5e396-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5e396-160">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="5e396-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5e396-161">จำนวนเงินตามใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="5e396-161">Quoted Amount</span></span> | <span data-ttu-id="5e396-162">นี่คือจำนวนเงินที่จะเสนอให้กับลูกค้าสำหรับงานทั้งหมดที่คาดการณ์ไว้ในรายการใบเสนอราคาตามโครงการนี้</span><span class="sxs-lookup"><span data-stu-id="5e396-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="5e396-163">ในใบเสนอราคาที่สร้างขึ้นจากโอกาสทางการขาย ค่านี้จะมีการคัดลอกจากฟิลด์ **งบประมาณของลูกค้า** ในรายการโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="5e396-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="5e396-164">เมื่อรายการใบเสนอราคาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและมีการสรุปจากจำนวนเงินในรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="5e396-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="5e396-165">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="5e396-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5e396-166">ภาษีที่ประเมิน</span><span class="sxs-lookup"><span data-stu-id="5e396-166">Estimated Tax</span></span> | <span data-ttu-id="5e396-167">นี่คือฟิลด์ที่แก้ไขได้สำหรับผู้ใช้ในการเพิ่มจำนวนภาษีโดยประมาณในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="5e396-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="5e396-168">เมื่อรายการใบเสนอราคาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและมีการสรุปจากจำนวนเงินภาษีในรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="5e396-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="5e396-169">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="5e396-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5e396-170">จำนวนเงินตามใบเสนอราคาหลังหักภาษี</span><span class="sxs-lookup"><span data-stu-id="5e396-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="5e396-171">ฟิลด์นี้คือจำนวนเงินของรายการใบเสนอราคาหลังหักภาษีและเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="5e396-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="5e396-172">จำนวนเงินในฟิลด์นี้มีการคำนวณเป็น *จำนวนเงินที่เสนอราคา + ภาษี*</span><span class="sxs-lookup"><span data-stu-id="5e396-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="5e396-173">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="5e396-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5e396-174">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="5e396-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="5e396-175">ฟิลด์นี้สามารถแก้ไขได้และพร้อมใช้งานในรายการใบเสนอราคาตามโครงการที่มีวิธีการเรียกเก็บเงินสำหรับ **เวลาและวัสดุ**</span><span class="sxs-lookup"><span data-stu-id="5e396-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="5e396-176">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="5e396-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5e396-177">งบประมาณของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="5e396-177">Customer Budget</span></span> | <span data-ttu-id="5e396-178">ฟิลด์นี้สามารถแก้ไขได้และมีการคัดลอกจากฟิลด์ที่สัมพันธ์กันในรายการโอกาสทางการขายหากมีการสร้างใบเสนอราคาจากโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="5e396-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="5e396-179">ค่านี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อใบเสนอราคาชนะ</span><span class="sxs-lookup"><span data-stu-id="5e396-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="5e396-180">กฎการตรวจสอบความถูกต้องสำหรับฟิลด์บนแท็บ ทั่วไป ของรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="5e396-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="5e396-181">**กฎข้อที่ 1**: ถ้าฟิลด์ **งานที่รวมไว้** ว่างเปล่าหรือหากตั้งค่าเป็น **งานโครงการทั้งหมด** โครงการจะรวมอยู่ในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="5e396-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="5e396-182">**กฎข้อที่ 2**: ถ้าฟิลด์ **งานที่รวมไว้** ว่างเปล่าหรือหากตั้งค่าเป็น **งานโครงการทั้งหมด** โครงการและคลาสธุรกรรมบางรายการสามารถรวมอยู่ในรายการใบเสนอราคาตามโครงการของใบเสนอราคาเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5e396-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="5e396-183">**กฎข้อที่ 3**: ถ้าฟิลด์ **งานที่รวมไว้** ตั้งค่าเป็น **งานโครงการที่เลือกเท่านั้น** โครงการและคลาสธุรกรรมบางรายการสามารถรวมอยู่ในรายการใบเสนอราคาตามโครงการของใบเสนอราคาหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="5e396-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="5e396-184">**กฎข้อที่ 4**: หากโอกาสทางการขายมีใบเสนอราคาหลายใบ สามารถมีรายการใบเสนอราคาจากใบเสนอราคาที่ต่างกันซึ่งการอ้างอิงโครงการเดียวกันทั้งหมดและมีคลาสธุรกรรมเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="5e396-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="5e396-185">**กฎข้อที่ 5**: หากใบเสนอราคาไม่ได้อยู่ในโอกาสทางการขายเดียวกัน ก็จะไม่สามารถรวมโครงการและคลาสธุรกรรมเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="5e396-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="5e396-186">
                    <strong>โอกาสทางการขาย</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5e396-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="5e396-187">
                    <strong>ใบเสนอราคา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5e396-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="5e396-188">
                    <strong>รายการใบเสนอราคา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5e396-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="5e396-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5e396-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="5e396-190">
                    <strong>งานที่รวมไว้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5e396-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="5e396-191">
                    <strong>รวมเวลา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5e396-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="5e396-192">
                    <strong>รวมค่าใช้จ่าย</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5e396-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="5e396-193">
                    <strong>รวมวัสดุ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5e396-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="5e396-194">
                    <strong>รวม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5e396-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="5e396-195">
                    <strong>ค่าธรรมเนียม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5e396-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="5e396-196">
                    <strong>ถูกต้อง/ไม่ถูกต้อง</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5e396-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="5e396-197">
                    <strong>เหตุผล</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5e396-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5e396-198">O1</span><span class="sxs-lookup"><span data-stu-id="5e396-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5e396-199">Q1</span><span class="sxs-lookup"><span data-stu-id="5e396-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5e396-200">QL1</span><span class="sxs-lookup"><span data-stu-id="5e396-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-201">P1</span><span class="sxs-lookup"><span data-stu-id="5e396-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5e396-202">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="5e396-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5e396-203">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5e396-204">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5e396-205">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-206">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5e396-207">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5e396-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5e396-208">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="5e396-208">Violation of Rule #2.</span></span> <span data-ttu-id="5e396-209">เวลา ค่าใช้จ่าย และค่าธรรมเนียมของโครงการ P1 รวมอยู่ในรายการใบเสนอราคา QL1 และ QL2</span><span class="sxs-lookup"><span data-stu-id="5e396-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5e396-210">O1</span><span class="sxs-lookup"><span data-stu-id="5e396-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5e396-211">Q1</span><span class="sxs-lookup"><span data-stu-id="5e396-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5e396-212">QL2</span><span class="sxs-lookup"><span data-stu-id="5e396-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-213">P1</span><span class="sxs-lookup"><span data-stu-id="5e396-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5e396-214">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="5e396-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5e396-215">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5e396-216">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5e396-217">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-218">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-218">Yes</span></span> </p>
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
<span data-ttu-id="5e396-219">O1</span><span class="sxs-lookup"><span data-stu-id="5e396-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5e396-220">Q1</span><span class="sxs-lookup"><span data-stu-id="5e396-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5e396-221">QL1</span><span class="sxs-lookup"><span data-stu-id="5e396-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-222">P1</span><span class="sxs-lookup"><span data-stu-id="5e396-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5e396-223">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="5e396-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5e396-224">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5e396-225">ไม่</span><span class="sxs-lookup"><span data-stu-id="5e396-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5e396-226">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-227">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5e396-228">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5e396-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5e396-229">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="5e396-229">Violation of Rule #2.</span></span> <span data-ttu-id="5e396-230">เวลา วัสดุ และค่าธรรมเนียมของโครงการ P1 รวมอยู่ในรายการใบเสนอราคา QL1 และ QL2</span><span class="sxs-lookup"><span data-stu-id="5e396-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5e396-231">O1</span><span class="sxs-lookup"><span data-stu-id="5e396-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5e396-232">Q1</span><span class="sxs-lookup"><span data-stu-id="5e396-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5e396-233">QL2</span><span class="sxs-lookup"><span data-stu-id="5e396-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-234">P1</span><span class="sxs-lookup"><span data-stu-id="5e396-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5e396-235">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="5e396-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5e396-236">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5e396-237">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5e396-238">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-239">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-239">Yes</span></span> </p>
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
<span data-ttu-id="5e396-240">O1</span><span class="sxs-lookup"><span data-stu-id="5e396-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5e396-241">Q1</span><span class="sxs-lookup"><span data-stu-id="5e396-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5e396-242">QL1</span><span class="sxs-lookup"><span data-stu-id="5e396-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-243">P1</span><span class="sxs-lookup"><span data-stu-id="5e396-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5e396-244">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="5e396-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5e396-245">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5e396-246">ไม่</span><span class="sxs-lookup"><span data-stu-id="5e396-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5e396-247">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-248">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5e396-249">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5e396-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5e396-250">เวลา วัสดุ และค่าธรรมเนียมของโครงการ P1 รวมอยู่ใน QL1</span><span class="sxs-lookup"><span data-stu-id="5e396-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="5e396-251">ค่าใช้จ่ายในโครงการ P1 รวมอยู่ใน QL2</span><span class="sxs-lookup"><span data-stu-id="5e396-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="5e396-252">ไม่มีการทับซ้อนกันในสิ่งที่รวมอยู่ในรายการใบเสนอราคาแต่ละรายการ ดังนั้นจึงถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5e396-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5e396-253">O1</span><span class="sxs-lookup"><span data-stu-id="5e396-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5e396-254">Q1</span><span class="sxs-lookup"><span data-stu-id="5e396-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5e396-255">QL2</span><span class="sxs-lookup"><span data-stu-id="5e396-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-256">P1</span><span class="sxs-lookup"><span data-stu-id="5e396-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5e396-257">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="5e396-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5e396-258">ไม่</span><span class="sxs-lookup"><span data-stu-id="5e396-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5e396-259">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5e396-260">ไม่</span><span class="sxs-lookup"><span data-stu-id="5e396-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-261">ไม่</span><span class="sxs-lookup"><span data-stu-id="5e396-261">No</span></span> </p>
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
<span data-ttu-id="5e396-262">O1</span><span class="sxs-lookup"><span data-stu-id="5e396-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5e396-263">Q1</span><span class="sxs-lookup"><span data-stu-id="5e396-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5e396-264">QL1</span><span class="sxs-lookup"><span data-stu-id="5e396-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-265">P1</span><span class="sxs-lookup"><span data-stu-id="5e396-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5e396-266">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5e396-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5e396-267">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5e396-268">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5e396-269">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-270">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5e396-271">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5e396-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5e396-272">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="5e396-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="5e396-273">Q1 รวมเวลา วัสดุ ค่าใช้จ่าย และค่าธรรมเนียมสำหรับชุดงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="5e396-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="5e396-274">QL2 รวมเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับโครงการ P1 ทั้งหมด ดังนั้นจึงทับซ้อนกับสิ่งที่รวมอยู่ใน Q1</span><span class="sxs-lookup"><span data-stu-id="5e396-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5e396-275">O1</span><span class="sxs-lookup"><span data-stu-id="5e396-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5e396-276">Q1</span><span class="sxs-lookup"><span data-stu-id="5e396-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5e396-277">QL2</span><span class="sxs-lookup"><span data-stu-id="5e396-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-278">P1</span><span class="sxs-lookup"><span data-stu-id="5e396-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5e396-279">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="5e396-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5e396-280">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5e396-281">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5e396-282">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-283">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-283">Yes</span></span> </p>
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
<span data-ttu-id="5e396-284">O1</span><span class="sxs-lookup"><span data-stu-id="5e396-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5e396-285">Q1</span><span class="sxs-lookup"><span data-stu-id="5e396-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5e396-286">QL1</span><span class="sxs-lookup"><span data-stu-id="5e396-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-287">P1</span><span class="sxs-lookup"><span data-stu-id="5e396-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5e396-288">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5e396-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5e396-289">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5e396-290">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5e396-291">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-292">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5e396-293">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5e396-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5e396-294">ตามกฎ #3</span><span class="sxs-lookup"><span data-stu-id="5e396-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="5e396-295">Q1 รวมเวลา วัสดุ ค่าใช้จ่าย และค่าธรรมเนียมสำหรับชุดงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="5e396-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="5e396-296">QL2 รวมเวลา วัสดุ ค่าใช้จ่าย และค่าธรรมเนียมสำหรับชุดงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="5e396-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="5e396-297">การตรวจสอบความถูกต้องเพิ่มเติมเพียงอย่างเดียวคือชุดงานย่อยใน QL1 ซึ่งแตกต่างจากชุดงานย่อยใน QL2 เพื่อให้แน่ใจว่าไม่มีการทับซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="5e396-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="5e396-298">ระบบดำเนินการนี้ทำได้เมื่อเกี่ยวข้องกับงาน</span><span class="sxs-lookup"><span data-stu-id="5e396-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5e396-299">O1</span><span class="sxs-lookup"><span data-stu-id="5e396-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5e396-300">Q1</span><span class="sxs-lookup"><span data-stu-id="5e396-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5e396-301">QL2</span><span class="sxs-lookup"><span data-stu-id="5e396-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-302">P1</span><span class="sxs-lookup"><span data-stu-id="5e396-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5e396-303">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5e396-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5e396-304">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5e396-305">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5e396-306">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-307">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-307">Yes</span></span> </p>
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
<span data-ttu-id="5e396-308">O1</span><span class="sxs-lookup"><span data-stu-id="5e396-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5e396-309">Q1</span><span class="sxs-lookup"><span data-stu-id="5e396-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5e396-310">QL1</span><span class="sxs-lookup"><span data-stu-id="5e396-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-311">P1</span><span class="sxs-lookup"><span data-stu-id="5e396-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5e396-312">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="5e396-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5e396-313">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5e396-314">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5e396-315">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-316">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5e396-317">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5e396-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5e396-318">ตามกฎ #5, Q1 และ Q2 เป็นใบเสนอราคาสองรายการในโอกาสทางการขายเดียวกัน ดังนั้นทั้งคู่จึงสามารถประมาณการองค์ประกอบเดียวกันของโครงการได้</span><span class="sxs-lookup"><span data-stu-id="5e396-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5e396-319">O1</span><span class="sxs-lookup"><span data-stu-id="5e396-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5e396-320">Q2</span><span class="sxs-lookup"><span data-stu-id="5e396-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5e396-321">QL1</span><span class="sxs-lookup"><span data-stu-id="5e396-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-322">P1</span><span class="sxs-lookup"><span data-stu-id="5e396-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5e396-323">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="5e396-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5e396-324">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5e396-325">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5e396-326">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-327">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-327">Yes</span></span> </p>
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
<span data-ttu-id="5e396-328">O1</span><span class="sxs-lookup"><span data-stu-id="5e396-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5e396-329">Q1</span><span class="sxs-lookup"><span data-stu-id="5e396-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5e396-330">QL1</span><span class="sxs-lookup"><span data-stu-id="5e396-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-331">P1</span><span class="sxs-lookup"><span data-stu-id="5e396-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5e396-332">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="5e396-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5e396-333">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5e396-334">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5e396-335">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-336">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5e396-337">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5e396-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5e396-338">ตามกฎ #4, Q1 และ Q2 เป็นใบเสนอราคาสองรายการในโอกาสทางการขายที่ต่างกัน ดังนั้นทั้งคู่จึงไม่สามารถประมาณการองค์ประกอบเดียวกันของโครงการเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="5e396-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="5e396-339">O2</span><span class="sxs-lookup"><span data-stu-id="5e396-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="5e396-340">Q1</span><span class="sxs-lookup"><span data-stu-id="5e396-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="5e396-341">QL1</span><span class="sxs-lookup"><span data-stu-id="5e396-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-342">P1</span><span class="sxs-lookup"><span data-stu-id="5e396-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="5e396-343">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="5e396-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="5e396-344">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="5e396-345">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="5e396-346">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5e396-347">ใช่</span><span class="sxs-lookup"><span data-stu-id="5e396-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
