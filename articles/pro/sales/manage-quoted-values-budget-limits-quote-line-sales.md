---
title: รายการใบเสนอราคาตามโครงการ (Pro)
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการใช้รายการใบเสนอราคาตามโครงการสำหรับงานโครงการ (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085862"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="feaa4-104">รายการใบเสนอราคาตามโครงการ (Pro)</span><span class="sxs-lookup"><span data-stu-id="feaa4-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="feaa4-105">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="feaa4-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="feaa4-106">รายการใบเสนอราคาตามโครงการได้รับการออกแบบมาเพื่อช่วยในการประเมินงานโครงการสำหรับการมีส่วนร่วม</span><span class="sxs-lookup"><span data-stu-id="feaa4-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="feaa4-107">โครงสร้างของรายการใบเสนอราคาตามโครงการมีการขยายสำหรับการประมาณการโครงการด้วยแนวคิดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="feaa4-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="feaa4-108">วิธีการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="feaa4-108">Billing Method</span></span>
- <span data-ttu-id="feaa4-109">การแม็ปโครงการและงาน</span><span class="sxs-lookup"><span data-stu-id="feaa4-109">Project and Task Mapping</span></span>
- <span data-ttu-id="feaa4-110">คลาสธุรกรรมที่รวมไว้</span><span class="sxs-lookup"><span data-stu-id="feaa4-110">Included Transaction classes</span></span>
- <span data-ttu-id="feaa4-111">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="feaa4-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="feaa4-112">การตั้งค่าการคิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="feaa4-112">Chargeability setup</span></span>
- <span data-ttu-id="feaa4-113">การประมาณการโดยใช้รายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="feaa4-114">ลูกค้าในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-114">Quote line Customers</span></span>

<span data-ttu-id="feaa4-115">ตารางต่อไปนี้ให้ข้อมูลเกี่ยวกับฟิลด์บนแท็บ **ทั่วไป** ของรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="feaa4-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="feaa4-116">ฟิลด์เหล่านี้ช่วยตั้งค่าพื้นฐานสำหรับการประมาณการค่าเบื้องต้นอย่างละเอียดสำหรับงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="feaa4-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="feaa4-117">**ฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="feaa4-117">**Field**</span></span> | <span data-ttu-id="feaa4-118">**ความเกี่ยวข้อง วัตถุประสงค์ และคำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="feaa4-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="feaa4-119">**ผลกระทบขั้นปลาย**</span><span class="sxs-lookup"><span data-stu-id="feaa4-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="feaa4-120">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="feaa4-120">Name</span></span> | <span data-ttu-id="feaa4-121">ชื่อของรายการใบเสนอราคาที่จะช่วยคุณระบุส่วนประกอบที่ไม่ต่อเนื่องของใบเสนอราคาที่กำลังประมาณการ</span><span class="sxs-lookup"><span data-stu-id="feaa4-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="feaa4-122">คัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="feaa4-123">วิธีการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="feaa4-123">Billing Method</span></span> | <span data-ttu-id="feaa4-124">ในใบเสนอราคาที่สร้างขึ้นจากโอกาสทางการขาย ค่านี้จะมีการคัดลอกจากฟิลด์ที่เกี่ยวข้องในรายการโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="feaa4-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="feaa4-125">ฟิลด์นี้ประกอบด้วยรูปแบบการทำสัญญาหลักสองแบบที่สนับสนุนโดย Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="feaa4-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="feaa4-126">- ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="feaa4-126">- Fixed price</span></span></br><span data-ttu-id="feaa4-127">- เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="feaa4-127">- Time and material.</span></span>| <span data-ttu-id="feaa4-128">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="feaa4-129">Project</span><span class="sxs-lookup"><span data-stu-id="feaa4-129">Project</span></span> | <span data-ttu-id="feaa4-130">ใช้ฟิลด์ที่ไม่บังคับนี้เพื่อระบุโครงการที่จะใช้เพื่อส่งมอบงานในการมีส่วนร่วมนี้</span><span class="sxs-lookup"><span data-stu-id="feaa4-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="feaa4-131">เมื่อโครงการถูกแม็ปกับรายการใบเสนอราคา จะช่วยในการตั้งค่างานที่คิดค่าธรมเนียมและยังนำการประมาณราคาตามโครงการไปใช้กับรายการใบเสนอราคาเป็นรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="feaa4-132">เมื่อไม่ได้แม็ปโครงการกับรายการใบเสนอราคาตามโครงการ ควรสร้างการประมาณด้วยตนเองโดยการสร้างรายละเอียดรายการใบเสนอราคาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="feaa4-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="feaa4-133">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="feaa4-134">งานที่รวมไว้</span><span class="sxs-lookup"><span data-stu-id="feaa4-134">Included Tasks</span></span> | <span data-ttu-id="feaa4-135">ระบุว่ารายการใบเสนอราคานี้มีการใช้สำหรับงานโครงการทั้งหมดหรือบางส่วนสำหรับโครงการที่เลือก</span><span class="sxs-lookup"><span data-stu-id="feaa4-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="feaa4-136">ฟิลด์นี้มีค่าที่เป็นไปได้ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="feaa4-136">This field has the following possible values:</span></span></br><span data-ttu-id="feaa4-137">- งานโครงการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="feaa4-137">- All project tasks</span></span></br><span data-ttu-id="feaa4-138">- งานโครงการที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="feaa4-138">- Selected project tasks only</span></span></br><span data-ttu-id="feaa4-139">ค่าว่างในฟิลด์นี้เทียบเท่ากับตัวเลือก **งานโครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="feaa4-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="feaa4-140">เมื่อมีการเลือก **งานโครงการที่เลือกเท่านั้น** จากนั้นในเพจโครงการ แท็บ **การตั้งค่าการเรียกเก็บเงินงาน** ช่วยให้คุณสามารถเลือกงานเฉพาะเพื่อเชื่อมโยงกับรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="feaa4-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="feaa4-141">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="feaa4-142">รวมเวลา</span><span class="sxs-lookup"><span data-stu-id="feaa4-142">Include Time</span></span> | <span data-ttu-id="feaa4-143">ค่าสถานะ **ใช่**/**ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานในโครงการที่เลือกจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="feaa4-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="feaa4-144">ค่า **ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="feaa4-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="feaa4-145">ค่า **ใช่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="feaa4-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="feaa4-146">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="feaa4-147">รวมค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="feaa4-147">Include Expense</span></span> | <span data-ttu-id="feaa4-148">ค่าสถานะ **ใช่**/**ไม่** ระบุว่าต้นทุนค่าใช้จ่ายในโครงการที่เลือกจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="feaa4-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="feaa4-149">ค่า **ไม่** ระบุว่าต้นทุนค่าใช้จ่ายจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="feaa4-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="feaa4-150">ค่า **ใช่** ระบุว่าต้นทุนค่าใช้จ่ายจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="feaa4-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="feaa4-151">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="feaa4-152">รวมค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="feaa4-152">Include Fee</span></span> | <span data-ttu-id="feaa4-153">ค่าสถานะ **ใช่**/**ไม่** ระบุว่าค่าธรรมเนียมในโครงการที่เลือกจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="feaa4-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="feaa4-154">ค่า **ไม่** ระบุว่าต้นทุนค่าธรรมเนียมจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="feaa4-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="feaa4-155">ค่า **ใช่** ระบุว่าต้นทุนค่าธรรมเนียมจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="feaa4-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="feaa4-156">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="feaa4-157">จำนวนเงินตามใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-157">Quoted Amount</span></span> | <span data-ttu-id="feaa4-158">นี่คือจำนวนเงินที่จะเสนอให้กับลูกค้าสำหรับงานทั้งหมดที่คาดการณ์ไว้ในรายการใบเสนอราคาตามโครงการนี้</span><span class="sxs-lookup"><span data-stu-id="feaa4-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="feaa4-159">ในใบเสนอราคาที่สร้างขึ้นจากโอกาสทางการขาย ค่านี้จะมีการคัดลอกจากฟิลด์ **งบประมาณของลูกค้า** ในรายการโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="feaa4-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="feaa4-160">เมื่อรายการใบเสนอราคาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและมีการสรุปจากจำนวนเงินในรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="feaa4-161">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="feaa4-162">ภาษีที่ประเมิน</span><span class="sxs-lookup"><span data-stu-id="feaa4-162">Estimated Tax</span></span> | <span data-ttu-id="feaa4-163">นี่คือฟิลด์ที่แก้ไขได้สำหรับผู้ใช้ในการเพิ่มจำนวนภาษีโดยประมาณในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="feaa4-164">เมื่อรายการใบเสนอราคาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและมีการสรุปจากจำนวนเงินภาษีในรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="feaa4-165">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="feaa4-166">จำนวนเงินตามใบเสนอราคาหลังหักภาษี</span><span class="sxs-lookup"><span data-stu-id="feaa4-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="feaa4-167">ฟิลด์นี้คือจำนวนเงินของรายการใบเสนอราคาหลังหักภาษีและเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="feaa4-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="feaa4-168">จำนวนเงินในฟิลด์นี้มีการคำนวณเป็น *จำนวนเงินที่เสนอราคา + ภาษี*</span><span class="sxs-lookup"><span data-stu-id="feaa4-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="feaa4-169">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="feaa4-170">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="feaa4-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="feaa4-171">ฟิลด์นี้สามารถแก้ไขได้และพร้อมใช้งานในรายการใบเสนอราคาตามโครงการที่มีวิธีการเรียกเก็บเงินสำหรับ **เวลาและวัสดุ**</span><span class="sxs-lookup"><span data-stu-id="feaa4-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="feaa4-172">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="feaa4-173">งบประมาณของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="feaa4-173">Customer Budget</span></span> | <span data-ttu-id="feaa4-174">ฟิลด์นี้สามารถแก้ไขได้และมีการคัดลอกจากฟิลด์ที่สัมพันธ์กันในรายการโอกาสทางการขายหากมีการสร้างใบเสนอราคาจากโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="feaa4-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="feaa4-175">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="feaa4-176">กฎการตรวจสอบความถูกต้องสำหรับฟิลด์บนแท็บ ทั่วไป ของรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="feaa4-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="feaa4-177">**กฎข้อที่ 1** : ถ้าฟิลด์ **งานที่รวมไว้** ว่างเปล่าหรือหากตั้งค่าเป็น **งานโครงการทั้งหมด** โครงการจะรวมอยู่ในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="feaa4-177">**Rule 1** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project is included in the quote line.</span></span>

<span data-ttu-id="feaa4-178">**กฎข้อที่ 2** : ถ้าฟิลด์ **งานที่รวมไว้** ว่างเปล่าหรือหากตั้งค่าเป็น **งานโครงการทั้งหมด** โครงการและคลาสธุรกรรมบางรายการสามารถรวมอยู่ในรายการใบเสนอราคาตามโครงการของใบเสนอราคาเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="feaa4-178">**Rule 2** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="feaa4-179">**กฎข้อที่ 3** : ถ้าฟิลด์ **งานที่รวมไว้** ตั้งค่าเป็น **งานโครงการที่เลือกเท่านั้น** โครงการและคลาสธุรกรรมบางรายการสามารถรวมอยู่ในรายการใบเสนอราคาตามโครงการของใบเสนอราคาหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="feaa4-179">**Rule 3** : If the **Included Tasks** field is set to **Selected project tasks only** , a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="feaa4-180">**กฎข้อที่ 4** : หากโอกาสทางการขายมีใบเสนอราคาหลายใบ สามารถมีรายการใบเสนอราคาจากใบเสนอราคาที่ต่างกันซึ่งการอ้างอิงโครงการเดียวกันทั้งหมดและมีคลาสธุรกรรมเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="feaa4-180">**Rule 4** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="feaa4-181">**กฎข้อที่ 5** : หากใบเสนอราคาไม่ได้อยู่ในโอกาสทางการขายเดียวกัน ก็จะไม่สามารถรวมโครงการและคลาสธุรกรรมเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="feaa4-181">**Rule 5** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="feaa4-182">
                    <strong>โอกาสทางการขาย</strong>
                </span><span class="sxs-lookup"><span data-stu-id="feaa4-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="feaa4-183">
                    <strong>ใบเสนอราคา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="feaa4-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="feaa4-184">
                    <strong>รายการใบเสนอราคา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="feaa4-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="feaa4-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="feaa4-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="feaa4-186">
                    <strong>งานที่รวมไว้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="feaa4-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="feaa4-187">
                    <strong>รวมเวลา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="feaa4-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="feaa4-188">
                    <strong>รวมค่าใช้จ่าย</strong>
                </span><span class="sxs-lookup"><span data-stu-id="feaa4-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="feaa4-189">
                    <strong>รวม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="feaa4-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="feaa4-190">
                    <strong>ค่าธรรมเนียม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="feaa4-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="feaa4-191">
                    <strong>ถูกต้อง/ไม่ถูกต้อง</strong>
                </span><span class="sxs-lookup"><span data-stu-id="feaa4-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="feaa4-192">
                    <strong>เหตุผล</strong>
                </span><span class="sxs-lookup"><span data-stu-id="feaa4-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="feaa4-193">O1</span><span class="sxs-lookup"><span data-stu-id="feaa4-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="feaa4-194">Q1</span><span class="sxs-lookup"><span data-stu-id="feaa4-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-195">QL1</span><span class="sxs-lookup"><span data-stu-id="feaa4-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-196">ร1</span><span class="sxs-lookup"><span data-stu-id="feaa4-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="feaa4-197">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="feaa4-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-198">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-199">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-200">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="feaa4-201">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="feaa4-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="feaa4-202">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="feaa4-202">Violation of Rule #2.</span></span> <span data-ttu-id="feaa4-203">เวลา ค่าใช้จ่าย และค่าธรรมเนียมของโครงการ P1 รวมอยู่ในรายการใบเสนอราคา QL1 และ QL2</span><span class="sxs-lookup"><span data-stu-id="feaa4-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="feaa4-204">O1</span><span class="sxs-lookup"><span data-stu-id="feaa4-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="feaa4-205">Q1</span><span class="sxs-lookup"><span data-stu-id="feaa4-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-206">QL2</span><span class="sxs-lookup"><span data-stu-id="feaa4-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-207">ร1</span><span class="sxs-lookup"><span data-stu-id="feaa4-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="feaa4-208">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="feaa4-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-209">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-210">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-211">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-211">Yes</span></span> </p>
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
<span data-ttu-id="feaa4-212">O1</span><span class="sxs-lookup"><span data-stu-id="feaa4-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="feaa4-213">Q1</span><span class="sxs-lookup"><span data-stu-id="feaa4-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-214">QL1</span><span class="sxs-lookup"><span data-stu-id="feaa4-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-215">ร1</span><span class="sxs-lookup"><span data-stu-id="feaa4-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="feaa4-216">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="feaa4-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-217">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-218">No</span><span class="sxs-lookup"><span data-stu-id="feaa4-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-219">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="feaa4-220">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="feaa4-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="feaa4-221">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="feaa4-221">Violation of Rule #2.</span></span> <span data-ttu-id="feaa4-222">เวลาและค่าธรรมเนียมของโครงการ P1 รวมอยู่ในรายการใบเสนอราคา QL1 และ QL2</span><span class="sxs-lookup"><span data-stu-id="feaa4-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="feaa4-223">O1</span><span class="sxs-lookup"><span data-stu-id="feaa4-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="feaa4-224">Q1</span><span class="sxs-lookup"><span data-stu-id="feaa4-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-225">QL2</span><span class="sxs-lookup"><span data-stu-id="feaa4-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-226">ร1</span><span class="sxs-lookup"><span data-stu-id="feaa4-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="feaa4-227">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="feaa4-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-228">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-229">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-230">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-230">Yes</span></span> </p>
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
<span data-ttu-id="feaa4-231">O1</span><span class="sxs-lookup"><span data-stu-id="feaa4-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="feaa4-232">Q1</span><span class="sxs-lookup"><span data-stu-id="feaa4-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-233">QL1</span><span class="sxs-lookup"><span data-stu-id="feaa4-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-234">ร1</span><span class="sxs-lookup"><span data-stu-id="feaa4-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="feaa4-235">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="feaa4-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-236">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-237">No</span><span class="sxs-lookup"><span data-stu-id="feaa4-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-238">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="feaa4-239">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="feaa4-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="feaa4-240">เวลาและค่าธรรมเนียมของโครงการ P1 รวมอยู่ใน QL1</span><span class="sxs-lookup"><span data-stu-id="feaa4-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="feaa4-241">ค่าใช้จ่ายในโครงการ P1 รวมอยู่ใน QL2</span><span class="sxs-lookup"><span data-stu-id="feaa4-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="feaa4-242">ไม่มีการทับซ้อนกันในสิ่งที่รวมอยู่ในแต่ละรายการใบเสนอราคา และจะถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="feaa4-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="feaa4-243">O1</span><span class="sxs-lookup"><span data-stu-id="feaa4-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="feaa4-244">Q1</span><span class="sxs-lookup"><span data-stu-id="feaa4-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-245">QL2</span><span class="sxs-lookup"><span data-stu-id="feaa4-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-246">ร1</span><span class="sxs-lookup"><span data-stu-id="feaa4-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="feaa4-247">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="feaa4-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-248">No</span><span class="sxs-lookup"><span data-stu-id="feaa4-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-249">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-250">No</span><span class="sxs-lookup"><span data-stu-id="feaa4-250">No</span></span> </p>
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
<span data-ttu-id="feaa4-251">O1</span><span class="sxs-lookup"><span data-stu-id="feaa4-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="feaa4-252">Q1</span><span class="sxs-lookup"><span data-stu-id="feaa4-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-253">QL1</span><span class="sxs-lookup"><span data-stu-id="feaa4-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-254">ร1</span><span class="sxs-lookup"><span data-stu-id="feaa4-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="feaa4-255">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="feaa4-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-256">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-257">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-258">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="feaa4-259">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="feaa4-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="feaa4-260">การละเมิดกฎ #2 ข้างต้น</span><span class="sxs-lookup"><span data-stu-id="feaa4-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="feaa4-261">Q1 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="feaa4-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="feaa4-262">QL2 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับโครงการ P1 ทั้งหมดและทับซ้อนกับสิ่งที่รวมอยู่ใน Q1</span><span class="sxs-lookup"><span data-stu-id="feaa4-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="feaa4-263">O1</span><span class="sxs-lookup"><span data-stu-id="feaa4-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="feaa4-264">Q1</span><span class="sxs-lookup"><span data-stu-id="feaa4-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-265">QL2</span><span class="sxs-lookup"><span data-stu-id="feaa4-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-266">ร1</span><span class="sxs-lookup"><span data-stu-id="feaa4-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="feaa4-267">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="feaa4-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-268">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-269">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-270">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-270">Yes</span></span> </p>
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
<span data-ttu-id="feaa4-271">O1</span><span class="sxs-lookup"><span data-stu-id="feaa4-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="feaa4-272">Q1</span><span class="sxs-lookup"><span data-stu-id="feaa4-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-273">QL1</span><span class="sxs-lookup"><span data-stu-id="feaa4-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-274">ร1</span><span class="sxs-lookup"><span data-stu-id="feaa4-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="feaa4-275">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="feaa4-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-276">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-277">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-278">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="feaa4-279">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="feaa4-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="feaa4-280">ตามกฎ #3 ข้างต้น</span><span class="sxs-lookup"><span data-stu-id="feaa4-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="feaa4-281">Q1 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="feaa4-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="feaa4-282">QL2 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="feaa4-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="feaa4-283">การตรวจสอบความถูกต้องเพิ่มเติมเพียงอย่างเดียวคือชุดย่อยของงานบน QL1 ซึ่งแตกต่างจากชุดย่อยของงานบน QL2</span><span class="sxs-lookup"><span data-stu-id="feaa4-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="feaa4-284">เพื่อให้แน่ใจว่าไม่มีการทับซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="feaa4-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="feaa4-285">ระบบดำเนินการนี้ทำได้เมื่อเกี่ยวข้องกับงาน</span><span class="sxs-lookup"><span data-stu-id="feaa4-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="feaa4-286">O1</span><span class="sxs-lookup"><span data-stu-id="feaa4-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="feaa4-287">Q1</span><span class="sxs-lookup"><span data-stu-id="feaa4-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-288">QL2</span><span class="sxs-lookup"><span data-stu-id="feaa4-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-289">ร1</span><span class="sxs-lookup"><span data-stu-id="feaa4-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="feaa4-290">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="feaa4-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-291">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-292">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-293">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-293">Yes</span></span> </p>
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
<span data-ttu-id="feaa4-294">O1</span><span class="sxs-lookup"><span data-stu-id="feaa4-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="feaa4-295">Q1</span><span class="sxs-lookup"><span data-stu-id="feaa4-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-296">QL1</span><span class="sxs-lookup"><span data-stu-id="feaa4-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-297">ร1</span><span class="sxs-lookup"><span data-stu-id="feaa4-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="feaa4-298">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="feaa4-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-299">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-300">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-301">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="feaa4-302">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="feaa4-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="feaa4-303">ตามกฎ #5, Q1 และ Q2 เป็นใบเสนอราคาสองรายการในโอกาสทางการขายเดียวกัน ดังนั้นทั้งคู่จึงสามารถประมาณการสำหรับส่วนประกอบเดียวกันของโครงการได้</span><span class="sxs-lookup"><span data-stu-id="feaa4-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="feaa4-304">O1</span><span class="sxs-lookup"><span data-stu-id="feaa4-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="feaa4-305">Q2</span><span class="sxs-lookup"><span data-stu-id="feaa4-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-306">QL1</span><span class="sxs-lookup"><span data-stu-id="feaa4-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-307">ร1</span><span class="sxs-lookup"><span data-stu-id="feaa4-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="feaa4-308">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="feaa4-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-309">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-310">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-311">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-311">Yes</span></span> </p>
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
<span data-ttu-id="feaa4-312">O1</span><span class="sxs-lookup"><span data-stu-id="feaa4-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="feaa4-313">Q1</span><span class="sxs-lookup"><span data-stu-id="feaa4-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-314">QL1</span><span class="sxs-lookup"><span data-stu-id="feaa4-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-315">ร1</span><span class="sxs-lookup"><span data-stu-id="feaa4-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="feaa4-316">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="feaa4-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-317">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-318">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-319">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="feaa4-320">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="feaa4-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="feaa4-321">ตามกฎ #4, Q1 และ Q2 เป็นใบเสนอราคาสองรายการในโอกาสทางการขายที่ต่างกัน ดังนั้นทั้งคู่จึงสามารถประมาณการสำหรับส่วนประกอบเดียวกันของโครงการเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="feaa4-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="feaa4-322">O2</span><span class="sxs-lookup"><span data-stu-id="feaa4-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="feaa4-323">Q1</span><span class="sxs-lookup"><span data-stu-id="feaa4-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-324">QL1</span><span class="sxs-lookup"><span data-stu-id="feaa4-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-325">ร1</span><span class="sxs-lookup"><span data-stu-id="feaa4-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="feaa4-326">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="feaa4-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-327">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="feaa4-328">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="feaa4-329">มี</span><span class="sxs-lookup"><span data-stu-id="feaa4-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="feaa4-330">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="feaa4-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

