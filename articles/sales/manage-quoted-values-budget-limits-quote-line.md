---
title: รายการใบเสนอราคาตามโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการใช้รายการใบเสนอราคาตามโครงการสำหรับงานโครงการ
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906363"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="96fea-103">รายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="96fea-103">Project-based quote lines</span></span>

<span data-ttu-id="96fea-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="96fea-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="96fea-105">รายการใบเสนอราคาตามโครงการได้รับการออกแบบมาเพื่อช่วยในการประเมินงานโครงการสำหรับการมีส่วนร่วม</span><span class="sxs-lookup"><span data-stu-id="96fea-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="96fea-106">โครงสร้างของรายการใบเสนอราคาตามโครงการมีการขยายสำหรับการประมาณการโครงการด้วยแนวคิดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="96fea-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="96fea-107">วิธีการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="96fea-107">Billing Method</span></span>
- <span data-ttu-id="96fea-108">การแม็ปโครงการ</span><span class="sxs-lookup"><span data-stu-id="96fea-108">Project Mapping</span></span>
- <span data-ttu-id="96fea-109">คลาสธุรกรรมที่รวมไว้</span><span class="sxs-lookup"><span data-stu-id="96fea-109">Included Transaction classes</span></span>
- <span data-ttu-id="96fea-110">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="96fea-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="96fea-111">การตั้งค่าการคิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="96fea-111">Chargeability setup</span></span>
- <span data-ttu-id="96fea-112">การประมาณการโดยใช้รายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="96fea-113">ลูกค้าในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-113">Quote line Customers</span></span>

<span data-ttu-id="96fea-114">ตารางต่อไปนี้ให้ข้อมูลเกี่ยวกับฟิลด์บนแท็บ **ทั่วไป** ของรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="96fea-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="96fea-115">ฟิลด์เหล่านี้ช่วยตั้งค่าพื้นฐานสำหรับการประมาณการค่าเบื้องต้นอย่างละเอียดสำหรับงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="96fea-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="96fea-116">**ฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="96fea-116">**Field**</span></span> | <span data-ttu-id="96fea-117">**ความเกี่ยวข้อง วัตถุประสงค์ และคำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="96fea-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="96fea-118">**ผลกระทบขั้นปลาย**</span><span class="sxs-lookup"><span data-stu-id="96fea-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="96fea-119">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="96fea-119">Name</span></span> | <span data-ttu-id="96fea-120">ชื่อของรายการใบเสนอราคาที่จะช่วยคุณระบุส่วนประกอบที่ไม่ต่อเนื่องของใบเสนอราคาที่กำลังประมาณการ</span><span class="sxs-lookup"><span data-stu-id="96fea-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="96fea-121">คัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96fea-122">วิธีการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="96fea-122">Billing Method</span></span> | <span data-ttu-id="96fea-123">ในใบเสนอราคาที่สร้างขึ้นจากโอกาสทางการขาย ค่านี้จะมีการคัดลอกจากฟิลด์ที่เกี่ยวข้องในรายการโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="96fea-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="96fea-124">ฟิลด์นี้ประกอบด้วยรูปแบบการทำสัญญาหลักสองแบบที่สนับสนุนโดย Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="96fea-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="96fea-125">- ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="96fea-125">- Fixed price</span></span></br><span data-ttu-id="96fea-126">- เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="96fea-126">- Time and material.</span></span>| <span data-ttu-id="96fea-127">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96fea-128">Project</span><span class="sxs-lookup"><span data-stu-id="96fea-128">Project</span></span> | <span data-ttu-id="96fea-129">ใช้ฟิลด์ที่ไม่บังคับนี้เพื่อระบุโครงการที่จะใช้เพื่อส่งมอบงานในการมีส่วนร่วมนี้</span><span class="sxs-lookup"><span data-stu-id="96fea-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="96fea-130">เมื่อโครงการถูกแม็ปกับรายการใบเสนอราคา จะช่วยในการตั้งค่างานที่คิดค่าธรมเนียมและยังนำการประมาณราคาตามโครงการไปใช้กับรายการใบเสนอราคาเป็นรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="96fea-131">เมื่อไม่ได้แม็ปโครงการกับรายการใบเสนอราคาตามโครงการ ควรสร้างการประมาณด้วยตนเองโดยการสร้างรายละเอียดรายการใบเสนอราคาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="96fea-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="96fea-132">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96fea-133">รวมเวลา</span><span class="sxs-lookup"><span data-stu-id="96fea-133">Include Time</span></span> | <span data-ttu-id="96fea-134">ค่าสถานะ **ใช่**/**ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานในโครงการที่เลือกจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="96fea-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="96fea-135">ค่า **ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="96fea-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="96fea-136">ค่า **ใช่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="96fea-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="96fea-137">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96fea-138">รวมค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="96fea-138">Include Expense</span></span> | <span data-ttu-id="96fea-139">ค่าสถานะ **ใช่**/**ไม่** ระบุว่าต้นทุนค่าใช้จ่ายในโครงการที่เลือกจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="96fea-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="96fea-140">ค่า **ไม่** ระบุว่าต้นทุนค่าใช้จ่ายจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="96fea-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="96fea-141">ค่า **ใช่** ระบุว่าต้นทุนค่าใช้จ่ายจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="96fea-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="96fea-142">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96fea-143">รวมค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="96fea-143">Include Fee</span></span> | <span data-ttu-id="96fea-144">ค่าสถานะ **ใช่**/**ไม่** ระบุว่าค่าธรรมเนียมในโครงการที่เลือกจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="96fea-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="96fea-145">ค่า **ไม่** ระบุว่าต้นทุนค่าธรรมเนียมจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="96fea-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="96fea-146">ค่า **ใช่** ระบุว่าต้นทุนค่าธรรมเนียมจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="96fea-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="96fea-147">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96fea-148">จำนวนเงินตามใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-148">Quoted Amount</span></span> | <span data-ttu-id="96fea-149">นี่คือจำนวนเงินที่จะเสนอให้กับลูกค้าสำหรับงานทั้งหมดที่คาดการณ์ไว้ในรายการใบเสนอราคาตามโครงการนี้</span><span class="sxs-lookup"><span data-stu-id="96fea-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="96fea-150">ในใบเสนอราคาที่สร้างขึ้นจากโอกาสทางการขาย ค่านี้จะมีการคัดลอกจากฟิลด์ **งบประมาณของลูกค้า** ในรายการโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="96fea-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="96fea-151">เมื่อรายการใบเสนอราคาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและมีการสรุปจากจำนวนเงินในรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="96fea-152">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96fea-153">ภาษีที่ประเมิน</span><span class="sxs-lookup"><span data-stu-id="96fea-153">Estimated Tax</span></span> | <span data-ttu-id="96fea-154">นี่คือฟิลด์ที่แก้ไขได้สำหรับผู้ใช้ในการเพิ่มจำนวนภาษีโดยประมาณในรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="96fea-155">เมื่อรายการใบเสนอราคาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและมีการสรุปจากจำนวนเงินภาษีในรายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="96fea-156">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96fea-157">จำนวนเงินตามใบเสนอราคาหลังหักภาษี</span><span class="sxs-lookup"><span data-stu-id="96fea-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="96fea-158">ฟิลด์นี้คือจำนวนเงินของรายการใบเสนอราคาหลังหักภาษีและเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="96fea-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="96fea-159">จำนวนเงินในฟิลด์นี้มีการคำนวณเป็น *จำนวนเงินที่เสนอราคา + ภาษี*</span><span class="sxs-lookup"><span data-stu-id="96fea-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="96fea-160">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96fea-161">วงเงินที่ต้องไม่เกิน</span><span class="sxs-lookup"><span data-stu-id="96fea-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="96fea-162">ฟิลด์นี้สามารถแก้ไขได้และพร้อมใช้งานในรายการใบเสนอราคาตามโครงการที่มีวิธีการเรียกเก็บเงินสำหรับ **เวลาและวัสดุ**</span><span class="sxs-lookup"><span data-stu-id="96fea-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="96fea-163">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96fea-164">งบประมาณของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="96fea-164">Customer Budget</span></span> | <span data-ttu-id="96fea-165">ฟิลด์นี้สามารถแก้ไขได้และมีการคัดลอกจากฟิลด์ที่สัมพันธ์กันในรายการโอกาสทางการขายหากมีการสร้างใบเสนอราคาจากโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="96fea-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="96fea-166">ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="96fea-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="96fea-167">กฎการตรวจสอบความถูกต้องสำหรับฟิลด์บนแท็บ ทั่วไป ของรายการใบเสนอราคาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="96fea-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="96fea-168">**กฎข้อที่ 1**: คลาสธุรกรรมบางอย่างในโครงการที่เลือกสามารถรวมอยู่ในรายการใบเสนอราคาตามโครงการของใบเสนอราคาเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="96fea-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="96fea-169">**กฎข้อที่ 2**: หากโอกาสทางการขายมีใบเสนอราคาหลายใบ สามารถมีรายการใบเสนอราคาจากใบเสนอราคาที่ต่างกันซึ่งการอ้างอิงโครงการเดียวกันทั้งหมดและมีคลาสธุรกรรมเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="96fea-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="96fea-170">**กฎข้อที่ 3**: หากใบเสนอราคาไม่ได้อยู่ในโอกาสทางการขายเดียวกัน ก็จะไม่สามารถรวมโครงการและคลาสธุรกรรมเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="96fea-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="96fea-171">
                    <strong>โอกาสทางการขาย</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96fea-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="96fea-172">
                    <strong>ใบเสนอราคา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96fea-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="96fea-173">
                    <strong>รายการใบเสนอราคา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96fea-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="96fea-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96fea-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="96fea-175">
                    <strong>รวมเวลา</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96fea-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="96fea-176">
                    <strong>รวมค่าใช้จ่าย</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96fea-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="96fea-177">
                    <strong>รวม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96fea-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="96fea-178">
                    <strong>ค่าธรรมเนียม</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96fea-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="96fea-179">
                    <strong>ถูกต้อง/ไม่ถูกต้อง</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96fea-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="96fea-180">
                    <strong>เหตุผล</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96fea-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="96fea-181">O1</span><span class="sxs-lookup"><span data-stu-id="96fea-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96fea-182">Q1</span><span class="sxs-lookup"><span data-stu-id="96fea-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-183">QL1</span><span class="sxs-lookup"><span data-stu-id="96fea-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-184">ร1</span><span class="sxs-lookup"><span data-stu-id="96fea-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-185">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-186">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-187">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96fea-188">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="96fea-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96fea-189">การละเมิดกฎ #1</span><span class="sxs-lookup"><span data-stu-id="96fea-189">Violation of Rule #1.</span></span> <span data-ttu-id="96fea-190">เวลา ค่าใช้จ่าย และค่าธรรมเนียมของโครงการ P1 รวมอยู่ในทั้งสองรายการใบเสนอราคา, QL1 และ QL2</span><span class="sxs-lookup"><span data-stu-id="96fea-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="96fea-191">O1</span><span class="sxs-lookup"><span data-stu-id="96fea-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96fea-192">Q1</span><span class="sxs-lookup"><span data-stu-id="96fea-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-193">QL2</span><span class="sxs-lookup"><span data-stu-id="96fea-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-194">ร1</span><span class="sxs-lookup"><span data-stu-id="96fea-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-195">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-196">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-197">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-197">Yes</span></span> </p>
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
<span data-ttu-id="96fea-198">O1</span><span class="sxs-lookup"><span data-stu-id="96fea-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96fea-199">Q1</span><span class="sxs-lookup"><span data-stu-id="96fea-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-200">QL1</span><span class="sxs-lookup"><span data-stu-id="96fea-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-201">ร1</span><span class="sxs-lookup"><span data-stu-id="96fea-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-202">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-203">No</span><span class="sxs-lookup"><span data-stu-id="96fea-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-204">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96fea-205">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="96fea-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96fea-206">การละเมิดกฎ #1</span><span class="sxs-lookup"><span data-stu-id="96fea-206">Violation of Rule #1.</span></span> <span data-ttu-id="96fea-207">เวลาและค่าธรรมเนียมของโครงการ P1 รวมอยู่ในทั้งสองรายการใบเสนอราคา, QL1 และ QL2</span><span class="sxs-lookup"><span data-stu-id="96fea-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="96fea-208">O1</span><span class="sxs-lookup"><span data-stu-id="96fea-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96fea-209">Q1</span><span class="sxs-lookup"><span data-stu-id="96fea-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-210">QL2</span><span class="sxs-lookup"><span data-stu-id="96fea-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-211">ร1</span><span class="sxs-lookup"><span data-stu-id="96fea-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-212">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-213">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-214">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-214">Yes</span></span> </p>
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
<span data-ttu-id="96fea-215">O1</span><span class="sxs-lookup"><span data-stu-id="96fea-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96fea-216">Q1</span><span class="sxs-lookup"><span data-stu-id="96fea-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-217">QL1</span><span class="sxs-lookup"><span data-stu-id="96fea-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-218">ร1</span><span class="sxs-lookup"><span data-stu-id="96fea-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-219">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-220">No</span><span class="sxs-lookup"><span data-stu-id="96fea-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-221">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96fea-222">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="96fea-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="96fea-223">เวลาและค่าธรรมเนียมของโครงการ P1 รวมอยู่ใน QL1</span><span class="sxs-lookup"><span data-stu-id="96fea-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="96fea-224">ค่าใช้จ่ายในโครงการ P1 รวมอยู่ใน QL2</span><span class="sxs-lookup"><span data-stu-id="96fea-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="96fea-225">ไม่มีการทับซ้อนกันในสิ่งที่รวมอยู่ในแต่ละรายการใบเสนอราคา จึงจะถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="96fea-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="96fea-226">O1</span><span class="sxs-lookup"><span data-stu-id="96fea-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96fea-227">Q1</span><span class="sxs-lookup"><span data-stu-id="96fea-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-228">QL2</span><span class="sxs-lookup"><span data-stu-id="96fea-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-229">ร1</span><span class="sxs-lookup"><span data-stu-id="96fea-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-230">No</span><span class="sxs-lookup"><span data-stu-id="96fea-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-231">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-232">No</span><span class="sxs-lookup"><span data-stu-id="96fea-232">No</span></span> </p>
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
<span data-ttu-id="96fea-233">O1</span><span class="sxs-lookup"><span data-stu-id="96fea-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96fea-234">Q1</span><span class="sxs-lookup"><span data-stu-id="96fea-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-235">QL1</span><span class="sxs-lookup"><span data-stu-id="96fea-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-236">ร1</span><span class="sxs-lookup"><span data-stu-id="96fea-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-237">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-238">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-239">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96fea-240">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="96fea-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96fea-241">การละเมิดกฎ #1 ข้างต้น</span><span class="sxs-lookup"><span data-stu-id="96fea-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="96fea-242">Q1 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับโครงการ P1 ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="96fea-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="96fea-243">QL2 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับโครงการ P1 ทั้งหมดและทับซ้อนกับสิ่งที่รวมอยู่ใน Q1</span><span class="sxs-lookup"><span data-stu-id="96fea-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="96fea-244">O1</span><span class="sxs-lookup"><span data-stu-id="96fea-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96fea-245">Q1</span><span class="sxs-lookup"><span data-stu-id="96fea-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-246">QL2</span><span class="sxs-lookup"><span data-stu-id="96fea-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-247">ร1</span><span class="sxs-lookup"><span data-stu-id="96fea-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-248">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-249">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-250">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-250">Yes</span></span> </p>
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
<span data-ttu-id="96fea-251">O1</span><span class="sxs-lookup"><span data-stu-id="96fea-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96fea-252">Q1</span><span class="sxs-lookup"><span data-stu-id="96fea-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-253">QL1</span><span class="sxs-lookup"><span data-stu-id="96fea-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-254">ร1</span><span class="sxs-lookup"><span data-stu-id="96fea-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-255">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-256">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-257">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="96fea-258">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="96fea-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96fea-259">ตามกฎ #2, Q1 และ Q2 เป็นใบเสนอราคาสองรายการในโอกาสทางการขายเดียวกัน ดังนั้นทั้งคู่จึงสามารถประมาณการสำหรับส่วนประกอบเดียวกันของโครงการได้</span><span class="sxs-lookup"><span data-stu-id="96fea-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="96fea-260">O1</span><span class="sxs-lookup"><span data-stu-id="96fea-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96fea-261">Q2</span><span class="sxs-lookup"><span data-stu-id="96fea-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-262">QL1 ใน Q2</span><span class="sxs-lookup"><span data-stu-id="96fea-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-263">ร1</span><span class="sxs-lookup"><span data-stu-id="96fea-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-264">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-265">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-266">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-266">Yes</span></span> </p>
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
<span data-ttu-id="96fea-267">O1</span><span class="sxs-lookup"><span data-stu-id="96fea-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96fea-268">Q1</span><span class="sxs-lookup"><span data-stu-id="96fea-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-269">QL1</span><span class="sxs-lookup"><span data-stu-id="96fea-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-270">ร1</span><span class="sxs-lookup"><span data-stu-id="96fea-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-271">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-272">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-273">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="96fea-274">ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="96fea-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96fea-275">ตามกฎ #3, Q1 และ Q2 เป็นใบเสนอราคาสองรายการในโอกาสทางการขายที่ต่างกัน ดังนั้นทั้งคู่จึงสามารถประมาณการสำหรับส่วนประกอบเดียวกันของโครงการเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="96fea-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="96fea-276">O2</span><span class="sxs-lookup"><span data-stu-id="96fea-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96fea-277">Q1</span><span class="sxs-lookup"><span data-stu-id="96fea-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-278">QL1</span><span class="sxs-lookup"><span data-stu-id="96fea-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-279">ร1</span><span class="sxs-lookup"><span data-stu-id="96fea-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-280">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="96fea-281">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="96fea-282">มี</span><span class="sxs-lookup"><span data-stu-id="96fea-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="96fea-283">ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="96fea-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

