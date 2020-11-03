---
title: กำหนดการค่าใช้จ่ายของการสอบถาม Federal Awards
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับกำหนดการค่าใช้จ่ายของการสอบถาม Federal Awards
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085916"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="4d259-103">กำหนดการค่าใช้จ่ายของการสอบถาม Federal Awards</span><span class="sxs-lookup"><span data-stu-id="4d259-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d259-104">ตามที่สำนักงานการจัดการและงบประมาณ Circular A-133 หน่วยงานที่ได้รับเงินของรัฐบาลกลางจะต้องปฏิบัติตามข้อกำหนดการตรวจสอบ ซึ่งเรียกอีกอย่างว่า การตรวจสอบเพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="4d259-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="4d259-105">กระบวนการตรวจสอบใช้เพื่อรายงานเกี่ยวกับรายรับและรายจ่ายของเงินช่วยเหลือของรัฐบาลกลางเป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="4d259-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="4d259-106">ส่วนหนึ่งของรายงานการตรวจสอบฉบับเดียวรวมถึงกำหนดการค่าใช้จ่ายของ Federal Awards (SEFA)</span><span class="sxs-lookup"><span data-stu-id="4d259-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="4d259-107">กำหนดการค่าใช้จ่ายของการสอบถาม Federal Awards รวมถึงแคตตาล็อกชื่อและหมายเลขของ Federal Domestic Assistance (CFDA) หมายเลขทุน ปีที่ให้ทุน ชื่อหน่วยงานของรัฐบาลกลางที่จัดหาเงินทุน และชื่อของเอนทิตีแบบพาส-ทรู</span><span class="sxs-lookup"><span data-stu-id="4d259-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="4d259-108">การสอบถามเป็นช่วงเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="4d259-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="4d259-109">โดยปกติแล้ว ช่วงเวลาดังกล่าวจะเหมือนกับรอบระยะเวลางบการเงิน ซึ่งก็คือ ปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="4d259-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="4d259-110">การสอบถามรวมถึงทุนที่มีวันที่การประมาณการในช่วงวันที่ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4d259-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="4d259-111">คอลัมน์ **หน่วยงานผู้ให้เงินช่วยเหลือ** ของการสอบถามจะแสดงลูกค้าที่ให้เงินช่วยเหลือ เงินช่วยเหลือแบบพาส-ทรู หรือหน่วยงานผู้ให้เงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="4d259-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="4d259-112">สำหรับเงินช่วยเหลือแบบพาส-ทรู คอลัมน์ **หน่วยงานแบบพาส-ทรู** แสดงลูกค้าที่ให้เงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="4d259-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="4d259-113">หากเงินช่วยเหลือไม่ใช่แบบพาส-ทรู คอลัมน์ **หน่วยงานแบบพาส-ทรู** จะว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="4d259-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="4d259-114">ตั้งค่ากลุ่ม CFDA</span><span class="sxs-lookup"><span data-stu-id="4d259-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="4d259-115">คุณต้องตั้งค่ากลุ่ม CFDA ที่สามารถเชื่อมโยงกับหมายเลข CFDA ในการสอบถามกำหนดการค่าใช้จ่ายของแบบสอบถาม Federal Awards</span><span class="sxs-lookup"><span data-stu-id="4d259-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="4d259-116">ไปที่ **การจัดการโครงการและการบัญชี \> การตั้งค่า \> เงินช่วยเหลือ \> แคตตาล็อกของกลุ่มความช่วยเหลือภายในประเทศของรัฐบาลกลาง**</span><span class="sxs-lookup"><span data-stu-id="4d259-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="4d259-117">เลือก **สร้าง** เพื่อสร้างกลุ่ม CFDA</span><span class="sxs-lookup"><span data-stu-id="4d259-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="4d259-118">ป้อนชื่อกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="4d259-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="4d259-119">เลือก **บันทึก** เพื่อบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="4d259-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="4d259-120">ตั้งค่าหมายเลข CFDA</span><span class="sxs-lookup"><span data-stu-id="4d259-120">Set up CFDA numbers</span></span>

<span data-ttu-id="4d259-121">คุณต้องตั้งค่าหมายเลข CFDA ที่สามารถเพิ่มกับเงินช่วยเหลือและรวมในการสอบถามกำหนดการค่าใช้จ่ายของแบบสอบถาม Federal Awards</span><span class="sxs-lookup"><span data-stu-id="4d259-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="4d259-122">ไปที่ **การจัดการโครงการและการบัญชี \> การตั้งค่า \> เงินช่วยเหลือ \> แคตตาล็อกของหมายเลขความช่วยเหลือภายในประเทศของรัฐบาลกลาง**</span><span class="sxs-lookup"><span data-stu-id="4d259-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="4d259-123">เลือก **สร้าง** เพื่อสร้างหมายเลข CFDA</span><span class="sxs-lookup"><span data-stu-id="4d259-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="4d259-124">ในคอลัมน์ **หมายเลข** ให้ใส่หมายเลข CFDA</span><span class="sxs-lookup"><span data-stu-id="4d259-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="4d259-125">กดคีย์ **แท็บ**</span><span class="sxs-lookup"><span data-stu-id="4d259-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="4d259-126">ในคอลัมน์ **รายละเอียด** ให้ใส่ชื่อเรื่อง CFDA</span><span class="sxs-lookup"><span data-stu-id="4d259-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="4d259-127">กดคีย์ **แท็บ**</span><span class="sxs-lookup"><span data-stu-id="4d259-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="4d259-128">ไม่บังคับ: ในฟิลด์ **กลุ่มโปรแกรม** เพิ่มกลุ่ม CFDA ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="4d259-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="4d259-129">เลือก **บันทึก** เพื่อบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="4d259-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="4d259-130">ตั้งค่าเงินช่วยเหลือเพื่อรายงานกำหนดการค่าใช้จ่ายของการสอบถาม Federal Awards</span><span class="sxs-lookup"><span data-stu-id="4d259-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="4d259-131">ไปที่ **การจัดการโครงการและการบัญชี \> เงินช่วยเหลือ \> เงินช่วยเหลือ** และเลือกเงินช่วยเหลือที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="4d259-131">Go to **Project management and accounting \> Grants \> Grants** , and select an existing grant.</span></span>
2. <span data-ttu-id="4d259-132">บนแท็บด่วน **การตั้งค่า** ในฟิลด์ **แคตตาล็อกของความช่วยเหลือภายในประเทศของรัฐบาลกลาง** กำหนดหมายเลข CFDA</span><span class="sxs-lookup"><span data-stu-id="4d259-132">On the **Setup** FastTab, in the  **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="4d259-133">หมายเลข CFDA ในเงินช่วยเหลือจะกำหนดกลุ่ม CFDA สำหรับการรายงาน</span><span class="sxs-lookup"><span data-stu-id="4d259-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="4d259-134">บนแท็บด่วน **ข้อมูลติดต่อ** ให้ป้อนข้อมูลผู้ให้เงินช่วยเหลือ โดยทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="4d259-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="4d259-135">ในฟิลด์ **ลูกค้าที่ให้เงินช่วยเหลือ** ป้อนลูกค้าที่รับผิดชอบเงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="4d259-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="4d259-136">สำหรับเงินช่วยเหลือที่มีอยู่ อาจมีการป้อนข้อมูลนี้ไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="4d259-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="4d259-137">ระบุว่าลูกค้าที่ให้เงินช่วยเหลือเป็นผู้ให้ทุนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4d259-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="4d259-138">หากลูกค้าที่ให้เงินช่วยเหลือเป็นผู้ให้ทุน ให้ล้างกล่องกาเครื่องหมาย **แบบพาส-ทรู**</span><span class="sxs-lookup"><span data-stu-id="4d259-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="4d259-139">หากลูกค้ารายอื่นเป็นผู้ให้ทุน และลูกค้าที่ให้เงินช่วยเหลือเป็นผู้รับผิดชอบในการใช้จ่ายและติดตามเงิน ให้เลือกกล่องกาเครื่องหมาย **แบบพาส-ทรู**</span><span class="sxs-lookup"><span data-stu-id="4d259-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="4d259-140">หากคุณเลือกกล่องกาเครื่องหมาย **แบบพาส-ทรู** ในขั้นตอนก่อนหน้า ในฟิลด์ **หน่วยงานผู้ให้เงินช่วยเหลือ** ป้อนลูกค้าที่ให้เงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="4d259-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="4d259-141">หน่วยงานผู้ให้เงินช่วยเหลือและลูกค้าที่ให้เงินช่วยเหลือไม่สามารถเป็นลูกค้ารายเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="4d259-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="4d259-142">นี่คือตัวอย่างของการให้เงินช่วยเหลือแบบพาสทรู:</span><span class="sxs-lookup"><span data-stu-id="4d259-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="4d259-143">รัฐบาลกลางให้ทุนโครงการโครงสร้างพื้นฐานสำหรับรัฐ</span><span class="sxs-lookup"><span data-stu-id="4d259-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="4d259-144">รัฐบาลกลางให้เงินแก่รัฐเพื่อใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="4d259-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="4d259-145">ในกรณีนี้ รัฐบาลกลางเป็นหน่วยงานผู้ให้เงินช่วยเหลือ และรัฐเป็นลูกค้าผู้ให้เงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="4d259-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="4d259-146">เมื่อคุณเปิดคุณสมบัติครั้งแรก หมายเลข CFDA เริ่มต้นจะถูกป้อนโดยใช้ตัวเลขที่มีอยู่ในการให้เงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="4d259-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="4d259-147">ยกเว้นเงินช่วยเหลือจากการรายงาน SEFA ตามประเภทเงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="4d259-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="4d259-148">ไปที่ **การจัดการโครงการและการบัญชี \> การตั้งค่า \> เงินช่วยเหลือ \> ชนิดเงินช่วยเหลือ**</span><span class="sxs-lookup"><span data-stu-id="4d259-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="4d259-149">บนแท็บด่วน **ข้อมูลเริ่มต้น** เลือกกล่องกาเครื่องหมาย **ไม่รวมในกำหนดการค่าใช้จ่ายของ Federal Awards**</span><span class="sxs-lookup"><span data-stu-id="4d259-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="4d259-150">เลือก **บันทึก** เพื่อบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="4d259-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="4d259-151">เรียกใช้งานกำหนดการค่าใช้จ่ายของการสอบถาม Federal Awards</span><span class="sxs-lookup"><span data-stu-id="4d259-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="4d259-152">ไปที่ **การจัดการโครงการและการบัญชี \> สอบถามข้อมูลและรายงาน \> การสอบถามเงินช่วยเหลือ \> กำหนดการค่าใช้จ่ายของ Federal Awards**</span><span class="sxs-lookup"><span data-stu-id="4d259-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="4d259-153">ในส่วน **พารามิเตอร์** ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="4d259-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="4d259-154">ในฟิลด์ **ช่วงวันที่** เลือกรหัสสำหรับช่วงวันที่</span><span class="sxs-lookup"><span data-stu-id="4d259-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="4d259-155">หรืออีกวิธีหนึ่ง ในฟิลด์ **จากวันที่** และ **จนถึงวันที่** กำหนดช่วงวันที่</span><span class="sxs-lookup"><span data-stu-id="4d259-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="4d259-156">ทางเลือก: หากต้องการรวมเฉพาะธุรกรรมที่เรียกเก็บเงินเป็นรายได้ในการสอบถาม ให้ตั้งค่าตัวเลือก **รวมเฉพาะรายได้ที่เรียกเก็บเงิน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="4d259-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="4d259-157">คอลัมน์</span><span class="sxs-lookup"><span data-stu-id="4d259-157">Columns</span></span>

<span data-ttu-id="4d259-158">กำหนดการของค่าใช้จ่ายในการสอบถาม Federal Awards ประกอบด้วยคอลัมน์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4d259-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="4d259-159">แค็ตตาล็อกชื่อกลุ่ม Federal Domestic Assistance</span><span class="sxs-lookup"><span data-stu-id="4d259-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="4d259-160">หน่วยงานผู้ให้เงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="4d259-160">Grantor agency</span></span>
- <span data-ttu-id="4d259-161">หน่วยงานแบบพาส-ทรู</span><span class="sxs-lookup"><span data-stu-id="4d259-161">Pass-through agency</span></span>
- <span data-ttu-id="4d259-162">ชื่อเงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="4d259-162">Grant name</span></span>
- <span data-ttu-id="4d259-163">รหัสเงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="4d259-163">Grant ID</span></span>
- <span data-ttu-id="4d259-164">รหัสแอปพลิเคชันเงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="4d259-164">Grant application ID</span></span>
- <span data-ttu-id="4d259-165">แค็ตตาล็อก Federal Domestic Assistance</span><span class="sxs-lookup"><span data-stu-id="4d259-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="4d259-166">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="4d259-166">Receipts</span></span>
- <span data-ttu-id="4d259-167">ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="4d259-167">Expenditures</span></span>
