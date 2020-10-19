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
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908673"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="6370e-104">รายการใบเสนอราคาตามโครงการ (Pro)</span><span class="sxs-lookup"><span data-stu-id="6370e-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="6370e-105">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="6370e-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6370e-106">รายการใบเสนอราคาตามโครงการได้รับการออกแบบมาเพื่อช่วยในการประเมินงานโครงการสำหรับการมีส่วนร่วม</span><span class="sxs-lookup"><span data-stu-id="6370e-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="6370e-107">โครงสร้างของรายการใบเสนอราคาตามโครงการมีการขยายสำหรับการประมาณการโครงการด้วยแนวคิดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6370e-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="6370e-108">วิธีการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="6370e-108">Billing Method</span></span>
- <span data-ttu-id="6370e-109">การแม็ปโครงการและงาน</span><span class="sxs-lookup"><span data-stu-id="6370e-109">Project and Task Mapping</span></span>
- <span data-ttu-id="6370e-110">คลาสธุรกรรมที่รวมไว้</span><span class="sxs-lookup"><span data-stu-id="6370e-110">Included Transaction classes</span></span>
- <span data-ttu-id="6370e-111">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="6370e-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="6370e-112">การตั้งค่าการคิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="6370e-112">Chargeability setup</span></span>
- <span data-ttu-id="6370e-113">การประมาณการโดยใช้รายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="6370e-114">ลูกค้าในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-114">Quote line Customers</span></span>

<span data-ttu-id="6370e-115">ตารางต่อไปนี้ให้ข้อมูลเกี่ยวกับฟิลด์บนแท็บ **ทั่วไป** ของรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="6370e-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="6370e-116">ฟิลด์เหล่านี้ช่วยตั้งค่าพื้นฐานสำหรับการประมาณการค่าเบื้องต้นอย่างละเอียดสำหรับงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="6370e-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="6370e-117">**ฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="6370e-117">**Field**</span></span> | <span data-ttu-id="6370e-118">**ความเกี่ยวข้อง วัตถุประสงค์ และคำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="6370e-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="6370e-119">**ผลกระทบขั้นปลาย**</span><span class="sxs-lookup"><span data-stu-id="6370e-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6370e-120">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="6370e-120">Name</span></span> | <span data-ttu-id="6370e-121">ชื่อของรายการใบเสนอราคาที่จะช่วยคุณระบุส่วนประกอบที่ไม่ต่อเนื่องของใบเสนอราคาที่กำลังประมาณการ</span><span class="sxs-lookup"><span data-stu-id="6370e-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="6370e-122">คัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6370e-123">วิธีการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="6370e-123">Billing Method</span></span> | <span data-ttu-id="6370e-124">ในใบเสนอราคาที่สร้างขึ้นจากโอกาสทางการขาย ค่านี้จะมีการคัดลอกจากฟิลด์ที่เกี่ยวข้องในรายการโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="6370e-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="6370e-125">ฟิลด์นี้ประกอบด้วยรูปแบบการทำสัญญาหลักสองแบบที่สนับสนุนโดย Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="6370e-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="6370e-126">- ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="6370e-126">- Fixed price</span></span></br><span data-ttu-id="6370e-127">- เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="6370e-127">- Time and material.</span></span>| <span data-ttu-id="6370e-128">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6370e-129">Project</span><span class="sxs-lookup"><span data-stu-id="6370e-129">Project</span></span> | <span data-ttu-id="6370e-130">ใช้ฟิลด์ที่ไม่บังคับนี้เพื่อระบุโครงการที่จะใช้เพื่อส่งมอบงานในการมีส่วนร่วมนี้</span><span class="sxs-lookup"><span data-stu-id="6370e-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="6370e-131">เมื่อโครงการถูกแม็ปกับรายการใบเสนอราคา จะช่วยในการตั้งค่างานที่คิดค่าธรมเนียมและยังนำการประมาณราคาตามโครงการไปใช้กับรายการใบเสนอราคาเป็นรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="6370e-132">เมื่อไม่ได้แม็ปโครงการกับรายการใบเสนอราคาตามโครงการ ควรสร้างการประมาณด้วยตนเองโดยการสร้างรายละเอียดรายการใบเสนอราคาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="6370e-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="6370e-133">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="6370e-134">งานที่รวมไว้</span><span class="sxs-lookup"><span data-stu-id="6370e-134">Included Tasks</span></span> | <span data-ttu-id="6370e-135">ระบุว่ารายการใบเสนอราคานี้มีการใช้สำหรับงานโครงการทั้งหมดหรือบางส่วนสำหรับโครงการที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6370e-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="6370e-136">ฟิลด์นี้มีค่าที่เป็นไปได้ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6370e-136">This field has the following possible values:</span></span></br><span data-ttu-id="6370e-137">- งานโครงการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6370e-137">- All project tasks</span></span></br><span data-ttu-id="6370e-138">- งานโครงการที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6370e-138">- Selected project tasks only</span></span></br><span data-ttu-id="6370e-139">ค่าว่างในฟิลด์นี้เทียบเท่ากับตัวเลือก **งานโครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="6370e-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="6370e-140">เมื่อมีการเลือก **งานโครงการที่เลือกเท่านั้น** จากนั้นในเพจโครงการ แท็บ **การตั้งค่าการเรียกเก็บเงินงาน** ช่วยให้คุณสามารถเลือกงานเฉพาะเพื่อเชื่อมโยงกับรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="6370e-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="6370e-141">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6370e-142">รวมเวลา</span><span class="sxs-lookup"><span data-stu-id="6370e-142">Include Time</span></span> | <span data-ttu-id="6370e-143">ค่าสถานะ **ใช่**/**ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานในโครงการที่เลือกจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="6370e-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6370e-144">ค่า **ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="6370e-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6370e-145">ค่า **ใช่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="6370e-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6370e-146">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6370e-147">รวมค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="6370e-147">Include Expense</span></span> | <span data-ttu-id="6370e-148">ค่าสถานะ **ใช่**/**ไม่** ระบุว่าต้นทุนค่าใช้จ่ายในโครงการที่เลือกจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="6370e-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6370e-149">ค่า **ไม่** ระบุว่าต้นทุนค่าใช้จ่ายจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="6370e-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6370e-150">ค่า **ใช่** ระบุว่าต้นทุนค่าใช้จ่ายจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="6370e-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6370e-151">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6370e-152">รวมค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="6370e-152">Include Fee</span></span> | <span data-ttu-id="6370e-153">ค่าสถานะ **ใช่**/**ไม่** ระบุว่าค่าธรรมเนียมในโครงการที่เลือกจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="6370e-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6370e-154">ค่า **ไม่** ระบุว่าต้นทุนค่าธรรมเนียมจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="6370e-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6370e-155">ค่า **ใช่** ระบุว่าต้นทุนค่าธรรมเนียมจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="6370e-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6370e-156">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6370e-157">จำนวนเงินตามใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-157">Quoted Amount</span></span> | <span data-ttu-id="6370e-158">นี่คือจำนวนเงินที่จะเสนอให้กับลูกค้าสำหรับงานทั้งหมดที่คาดการณ์ไว้ในรายการใบเสนอราคาตามโครงการนี้</span><span class="sxs-lookup"><span data-stu-id="6370e-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="6370e-159">ในใบเสนอราคาที่สร้างขึ้นจากโอกาสทางการขาย ค่านี้จะมีการคัดลอกจากฟิลด์ **งบประมาณของลูกค้า** ในรายการโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="6370e-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="6370e-160">เมื่อรายการใบเสนอราคาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและมีการสรุปจากจำนวนเงินในรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="6370e-161">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6370e-162">ภาษีที่ประเมิน</span><span class="sxs-lookup"><span data-stu-id="6370e-162">Estimated Tax</span></span> | <span data-ttu-id="6370e-163">นี่คือฟิลด์ที่แก้ไขได้สำหรับผู้ใช้ในการเพิ่มจำนวนภาษีโดยประมาณในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="6370e-164">เมื่อรายการใบเสนอราคาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและมีการสรุปจากจำนวนเงินภาษีในรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="6370e-165">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6370e-166">จำนวนเงินตามใบเสนอราคาหลังหักภาษี</span><span class="sxs-lookup"><span data-stu-id="6370e-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="6370e-167">ฟิลด์นี้คือจำนวนเงินของรายการใบเสนอราคาหลังหักภาษีและเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="6370e-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="6370e-168">จำนวนเงินในฟิลด์นี้มีการคำนวณเป็น *จำนวนเงินที่เสนอราคา + ภาษี*</span><span class="sxs-lookup"><span data-stu-id="6370e-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="6370e-169">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6370e-170">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="6370e-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="6370e-171">ฟิลด์นี้สามารถแก้ไขได้และพร้อมใช้งานในรายการใบเสนอราคาตามโครงการที่มีวิธีการเรียกเก็บเงินสำหรับ **เวลาและวัสดุ**</span><span class="sxs-lookup"><span data-stu-id="6370e-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="6370e-172">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6370e-173">งบประมาณของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6370e-173">Customer Budget</span></span> | <span data-ttu-id="6370e-174">ฟิลด์นี้สามารถแก้ไขได้และมีการคัดลอกจากฟิลด์ที่สัมพันธ์กันในรายการโอกาสทางการขายหากมีการสร้างใบเสนอราคาจากโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="6370e-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="6370e-175">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="6370e-176">กฎการตรวจสอบความถูกต้องสำหรับฟิลด์บนแท็บ ทั่วไป ของรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="6370e-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="6370e-177">**กฎข้อที่ 1**: ถ้าฟิลด์ **งานที่รวมไว้** ว่างเปล่าหรือหากตั้งค่าเป็น **งานโครงการทั้งหมด** โครงการจะรวมอยู่ในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6370e-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="6370e-178">**กฎข้อที่ 2**: ถ้าฟิลด์ **งานที่รวมไว้** ว่างเปล่าหรือหากตั้งค่าเป็น **งานโครงการทั้งหมด** โครงการและคลาสธุรกรรมบางรายการสามารถรวมอยู่ในรายการใบเสนอราคาตามโครงการของใบเสนอราคาเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6370e-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="6370e-179">**กฎข้อที่ 3**: ถ้าฟิลด์ **งานที่รวมไว้** ตั้งค่าเป็น **งานโครงการที่เลือกเท่านั้น** โครงการและคลาสธุรกรรมบางรายการสามารถรวมอยู่ในรายการใบเสนอราคาตามโครงการของใบเสนอราคาหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="6370e-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="6370e-180">**กฎข้อที่ 4**: หากโอกาสทางการขายมีใบเสนอราคาหลายใบ สามารถมีรายการใบเสนอราคาจากใบเสนอราคาที่ต่างกันซึ่งการอ้างอิงโครงการเดียวกันทั้งหมดและมีคลาสธุรกรรมเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="6370e-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="6370e-181">**กฎข้อที่ 5**: หากใบเสนอราคาไม่ได้อยู่ในโอกาสทางการขายเดียวกัน ก็จะไม่สามารถรวมโครงการและคลาสธุรกรรมเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="6370e-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="6370e-182">
                    <strong>โอกาสทางการขาย</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6370e-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="6370e-183">
                    <strong>ใบเสนอราคา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6370e-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6370e-184">
                    <strong>รายการใบเสนอราคา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6370e-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6370e-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6370e-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="6370e-186">
                    <strong>งานที่รวมไว้</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6370e-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="6370e-187">
                    <strong>รวมเวลา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6370e-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="6370e-188">
                    <strong>รวมค่าใช้จ่าย</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6370e-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6370e-189">
                    <strong>รวม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6370e-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="6370e-190">
                    <strong>ค่าธรรมเนียม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6370e-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="6370e-191">
                    <strong>ถูกต้อง/ไม่ถูกต้อง</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6370e-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="6370e-192">
                    <strong>เหตุผล</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6370e-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6370e-193">O1</span><span class="sxs-lookup"><span data-stu-id="6370e-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6370e-194">Q1</span><span class="sxs-lookup"><span data-stu-id="6370e-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-195">QL1</span><span class="sxs-lookup"><span data-stu-id="6370e-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-196">ร1</span><span class="sxs-lookup"><span data-stu-id="6370e-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6370e-197">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="6370e-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-198">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-199">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-200">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6370e-201">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6370e-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6370e-202">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="6370e-202">Violation of Rule #2.</span></span> <span data-ttu-id="6370e-203">เวลา ค่าใช้จ่าย และค่าธรรมเนียมของโครงการ P1 รวมอยู่ในรายการใบเสนอราคา QL1 และ QL2</span><span class="sxs-lookup"><span data-stu-id="6370e-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6370e-204">O1</span><span class="sxs-lookup"><span data-stu-id="6370e-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6370e-205">Q1</span><span class="sxs-lookup"><span data-stu-id="6370e-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-206">QL2</span><span class="sxs-lookup"><span data-stu-id="6370e-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-207">ร1</span><span class="sxs-lookup"><span data-stu-id="6370e-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6370e-208">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="6370e-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-209">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-210">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-211">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-211">Yes</span></span> </p>
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
<span data-ttu-id="6370e-212">O1</span><span class="sxs-lookup"><span data-stu-id="6370e-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6370e-213">Q1</span><span class="sxs-lookup"><span data-stu-id="6370e-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-214">QL1</span><span class="sxs-lookup"><span data-stu-id="6370e-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-215">ร1</span><span class="sxs-lookup"><span data-stu-id="6370e-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6370e-216">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="6370e-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-217">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-218">No</span><span class="sxs-lookup"><span data-stu-id="6370e-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-219">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6370e-220">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6370e-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6370e-221">การละเมิดกฎ #2</span><span class="sxs-lookup"><span data-stu-id="6370e-221">Violation of Rule #2.</span></span> <span data-ttu-id="6370e-222">เวลาและค่าธรรมเนียมของโครงการ P1 รวมอยู่ในรายการใบเสนอราคา QL1 และ QL2</span><span class="sxs-lookup"><span data-stu-id="6370e-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6370e-223">O1</span><span class="sxs-lookup"><span data-stu-id="6370e-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6370e-224">Q1</span><span class="sxs-lookup"><span data-stu-id="6370e-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-225">QL2</span><span class="sxs-lookup"><span data-stu-id="6370e-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-226">ร1</span><span class="sxs-lookup"><span data-stu-id="6370e-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6370e-227">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="6370e-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-228">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-229">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-230">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-230">Yes</span></span> </p>
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
<span data-ttu-id="6370e-231">O1</span><span class="sxs-lookup"><span data-stu-id="6370e-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6370e-232">Q1</span><span class="sxs-lookup"><span data-stu-id="6370e-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-233">QL1</span><span class="sxs-lookup"><span data-stu-id="6370e-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-234">ร1</span><span class="sxs-lookup"><span data-stu-id="6370e-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6370e-235">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="6370e-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-236">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-237">No</span><span class="sxs-lookup"><span data-stu-id="6370e-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-238">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6370e-239">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6370e-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="6370e-240">เวลาและค่าธรรมเนียมของโครงการ P1 รวมอยู่ใน QL1</span><span class="sxs-lookup"><span data-stu-id="6370e-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="6370e-241">ค่าใช้จ่ายในโครงการ P1 รวมอยู่ใน QL2</span><span class="sxs-lookup"><span data-stu-id="6370e-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="6370e-242">ไม่มีการทับซ้อนกันในสิ่งที่รวมอยู่ในแต่ละรายการใบเสนอราคา และจะถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6370e-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6370e-243">O1</span><span class="sxs-lookup"><span data-stu-id="6370e-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6370e-244">Q1</span><span class="sxs-lookup"><span data-stu-id="6370e-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-245">QL2</span><span class="sxs-lookup"><span data-stu-id="6370e-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-246">ร1</span><span class="sxs-lookup"><span data-stu-id="6370e-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6370e-247">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="6370e-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-248">No</span><span class="sxs-lookup"><span data-stu-id="6370e-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-249">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-250">No</span><span class="sxs-lookup"><span data-stu-id="6370e-250">No</span></span> </p>
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
<span data-ttu-id="6370e-251">O1</span><span class="sxs-lookup"><span data-stu-id="6370e-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6370e-252">Q1</span><span class="sxs-lookup"><span data-stu-id="6370e-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-253">QL1</span><span class="sxs-lookup"><span data-stu-id="6370e-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-254">ร1</span><span class="sxs-lookup"><span data-stu-id="6370e-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6370e-255">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6370e-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-256">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-257">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-258">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6370e-259">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6370e-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6370e-260">การละเมิดกฎ #2 ข้างต้น</span><span class="sxs-lookup"><span data-stu-id="6370e-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="6370e-261">Q1 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="6370e-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="6370e-262">QL2 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับโครงการ P1 ทั้งหมดและทับซ้อนกับสิ่งที่รวมอยู่ใน Q1</span><span class="sxs-lookup"><span data-stu-id="6370e-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6370e-263">O1</span><span class="sxs-lookup"><span data-stu-id="6370e-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6370e-264">Q1</span><span class="sxs-lookup"><span data-stu-id="6370e-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-265">QL2</span><span class="sxs-lookup"><span data-stu-id="6370e-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-266">ร1</span><span class="sxs-lookup"><span data-stu-id="6370e-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6370e-267">ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="6370e-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-268">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-269">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-270">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-270">Yes</span></span> </p>
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
<span data-ttu-id="6370e-271">O1</span><span class="sxs-lookup"><span data-stu-id="6370e-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6370e-272">Q1</span><span class="sxs-lookup"><span data-stu-id="6370e-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-273">QL1</span><span class="sxs-lookup"><span data-stu-id="6370e-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-274">ร1</span><span class="sxs-lookup"><span data-stu-id="6370e-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6370e-275">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6370e-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-276">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-277">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-278">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6370e-279">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6370e-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6370e-280">ตามกฎ #3 ข้างต้น</span><span class="sxs-lookup"><span data-stu-id="6370e-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="6370e-281">Q1 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="6370e-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="6370e-282">QL2 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับงานย่อยในโครงการ P1</span><span class="sxs-lookup"><span data-stu-id="6370e-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="6370e-283">การตรวจสอบความถูกต้องเพิ่มเติมเพียงอย่างเดียวคือชุดย่อยของงานบน QL1 ซึ่งแตกต่างจากชุดย่อยของงานบน QL2</span><span class="sxs-lookup"><span data-stu-id="6370e-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="6370e-284">เพื่อให้แน่ใจว่าไม่มีการทับซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="6370e-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="6370e-285">ระบบดำเนินการนี้ทำได้เมื่อเกี่ยวข้องกับงาน</span><span class="sxs-lookup"><span data-stu-id="6370e-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6370e-286">O1</span><span class="sxs-lookup"><span data-stu-id="6370e-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6370e-287">Q1</span><span class="sxs-lookup"><span data-stu-id="6370e-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-288">QL2</span><span class="sxs-lookup"><span data-stu-id="6370e-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-289">ร1</span><span class="sxs-lookup"><span data-stu-id="6370e-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6370e-290">งานที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6370e-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-291">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-292">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-293">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-293">Yes</span></span> </p>
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
<span data-ttu-id="6370e-294">O1</span><span class="sxs-lookup"><span data-stu-id="6370e-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6370e-295">Q1</span><span class="sxs-lookup"><span data-stu-id="6370e-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-296">QL1</span><span class="sxs-lookup"><span data-stu-id="6370e-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-297">ร1</span><span class="sxs-lookup"><span data-stu-id="6370e-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6370e-298">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="6370e-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-299">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-300">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-301">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6370e-302">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6370e-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6370e-303">ตามกฎ #5, Q1 และ Q2 เป็นใบเสนอราคาสองรายการในโอกาสทางการขายเดียวกัน ดังนั้นทั้งคู่จึงสามารถประมาณการสำหรับส่วนประกอบเดียวกันของโครงการได้</span><span class="sxs-lookup"><span data-stu-id="6370e-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6370e-304">O1</span><span class="sxs-lookup"><span data-stu-id="6370e-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6370e-305">Q2</span><span class="sxs-lookup"><span data-stu-id="6370e-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-306">QL1</span><span class="sxs-lookup"><span data-stu-id="6370e-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-307">ร1</span><span class="sxs-lookup"><span data-stu-id="6370e-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6370e-308">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="6370e-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-309">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-310">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-311">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-311">Yes</span></span> </p>
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
<span data-ttu-id="6370e-312">O1</span><span class="sxs-lookup"><span data-stu-id="6370e-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6370e-313">Q1</span><span class="sxs-lookup"><span data-stu-id="6370e-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-314">QL1</span><span class="sxs-lookup"><span data-stu-id="6370e-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-315">ร1</span><span class="sxs-lookup"><span data-stu-id="6370e-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6370e-316">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="6370e-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-317">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-318">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-319">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6370e-320">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6370e-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6370e-321">ตามกฎ #4, Q1 และ Q2 เป็นใบเสนอราคาสองรายการในโอกาสทางการขายที่ต่างกัน ดังนั้นทั้งคู่จึงสามารถประมาณการสำหรับส่วนประกอบเดียวกันของโครงการเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="6370e-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6370e-322">O2</span><span class="sxs-lookup"><span data-stu-id="6370e-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6370e-323">Q1</span><span class="sxs-lookup"><span data-stu-id="6370e-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-324">QL1</span><span class="sxs-lookup"><span data-stu-id="6370e-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-325">ร1</span><span class="sxs-lookup"><span data-stu-id="6370e-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6370e-326">งานโครงการทั้งหมดหรือว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="6370e-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-327">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6370e-328">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6370e-329">มี</span><span class="sxs-lookup"><span data-stu-id="6370e-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6370e-330">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6370e-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

