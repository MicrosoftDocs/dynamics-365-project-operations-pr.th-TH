---
title: โอนงบประมาณโครงการเมื้อสิ้นปีบัญชี
description: บทความนี้ให้ข้อมูลเบื้องต้นเกี่ยวกับวิธีการโอนจำนวนงบประมาณที่เหลือไปยังปีต่อ ๆ ไปและสร้างรายละเอียดการลงทะเบียนงบประมาณ
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: be3dc039b92e88cac6f6b3b7f72bc32ecf587539
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008064"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="d3234-103">โอนงบประมาณโครงการเมื้อสิ้นปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="d3234-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3234-104">เมื่อทำงานในโครงการหลายปี คุณอาจมีงบประมาณเหลือเมื่อสิ้นสุดปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="d3234-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="d3234-105">คุณสามารถโอนยอดงบประมาณที่เหลือไปยังปีในอนาคต และสร้างรายละเอียดการลงทะเบียนงบประมาณสำหรับยอดเงินในบัญชีแยกประเภททั่วไปที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="d3234-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="d3234-106">ก่อนที่คุณจะยกยอดจำนวนเงินที่เหลือ โปรดตรวจสอบและวิเคราะห์จำนวนงบประมาณที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="d3234-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="d3234-107">ตรวจสอบและวิเคราะห์จำนวนงบประมาณที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="d3234-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="d3234-108">ทำตามขั้นตอนต่อไปนี้เพื่อตรวจสอบยอดงบประมาณสิ้นปีสำหรับโครงการ แต่ไม่ยกยอดเงินไปข้างหน้า</span><span class="sxs-lookup"><span data-stu-id="d3234-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="d3234-109">ไปที่ **การจัดการโครงการและการบัญชี** > **เป็นระยะ** > **งบประมาณ** > **ยกยอดงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="d3234-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="d3234-110">บนหน้า **กระบวนการยกยอดงบประมาณโครงการ** บนแท็บ **ตัวเลือกสิ้นปี** ตรวจสอบว่า **ดำเนินการยกยอดงบประมาณโครงการที่เหลือ** ไม่ได้เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d3234-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="d3234-111">บนแท็บ **พารามิเตอร์** ในฟิลด์ **ปีบัญชีโครงการ** เลือกปีบัญชีที่คุณต้องการดูจำนวนงบประมาณที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="d3234-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="d3234-112">ในฟิลด์ **ปีบัญชีที่กำลังเปิด** เลือกปีบัญชีที่คุณต้องการดูจำนวนงบประมาณที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="d3234-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="d3234-113">ในฟิลด์ **จากแบบจำลองการคาดการณ์** ให้เลือก **งบประมาณที่เหลือ**</span><span class="sxs-lookup"><span data-stu-id="d3234-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="d3234-114">หากต้องการรวมโครงการที่ตรงตามเกณฑ์ที่คุณเลือกและไม่มีงบประมาณเหลือ ให้เลือก **แสดงศูนย์ที่เหลือ**</span><span class="sxs-lookup"><span data-stu-id="d3234-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="d3234-115">บนแท็บ **เลือกงบประมาณ** เลือก **ดึงงบประมาณทั้งหมด** เพื่อโหลดงบประมาณทั้งหมดที่ตรงกับเกณฑ์ที่คุณเลือก จากนั้นเลือก **ดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="d3234-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="d3234-116">ในการออกแบบแบบสอบถามฐานข้อมูลที่โหลดชุดงบประมาณที่ต้องการลงในบานหน้าต่าง ให้เลือก **ดึงงบประมาณที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="d3234-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="d3234-117">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรายการเฉพาะในบานหน้าต่าง ให้เลือกรายการ จากนั้นเลือก **ดูรายละเอียดงบประมาณ** หรือ **ดูบัญชี**</span><span class="sxs-lookup"><span data-stu-id="d3234-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="d3234-118">ยกยอดงบประมาณที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="d3234-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="d3234-119">เมื่อคุณประมวลผลจำนวนเงินงบประมาณที่เหลือ คุณสามารถสร้างธุรกรรมในบัญชีแยกประเภทสำหรับยอดเงินที่คุณกำลังดำเนินการต่อไป</span><span class="sxs-lookup"><span data-stu-id="d3234-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="d3234-120">ในการสร้างธุรกรรมบัญชีแยกประเภททั่วไป ให้ทำตามขั้นตอนในส่วน [ดำเนินการยกยอดงบประมาณและสร้างธุรกรรมบัญชีแยกประเภททั่วไป](#carry-forward)</span><span class="sxs-lookup"><span data-stu-id="d3234-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="d3234-121">จำนวนงบประมาณที่ยกยอดมาจะถูกโอนไปยังแบบจำลองการคาดการณ์ที่เลือกไว้ในหน้า **แบบจำลองการคาดการณ์** เป็นแบบจำลองการคาดการณ์ยกยอดไป</span><span class="sxs-lookup"><span data-stu-id="d3234-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a> <span data-ttu-id="d3234-122">ดำเนินการยกยอดงบประมาณและสร้างธุรกรรมบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="d3234-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="d3234-123">เลือก **การจัดการโครงการและการบัญชี** > **เป็นระยะ** > **งบประมาณ** > **ยกยอดงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="d3234-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="d3234-124">บนหน้า **ดำเนินการยกยอดงบประมาณโครงการ** ให้เลือก **สิ้นปี** แล้วเปิดใช้งาน **ดำเนินการยกยอดงบประมาณโครงการที่เหลือ** และ **สร้างรายการลงทะเบียนงบประมาณในบัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="d3234-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="d3234-125">บนแท็บ **พารามิเตอร์** ในกลุ่มฟิลด์ **พารามิเตอร์โครงการ** เลือกรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d3234-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="d3234-126">**ปีบัญชีโครงการ**: เลือกงช่วงเริ่มต้นปีบัญชีที่คุณต้องการดูจำนวนงบประมาณที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="d3234-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="d3234-127">**กำไรและขาดทุน**: สร้างธุรกรรมกำไรและขาดทุนในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="d3234-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="d3234-128">**WIP**: สร้างธุรกรรมกำลังดำเนินการงาน (WIP) ในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="d3234-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="d3234-129">**บัญชีเงินเดือน**: สร้างธุรกรรมการจัดสรรบัญชีเงินเดือนในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="d3234-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="d3234-130">ในกลุ่มฟิลด์ **บัญชีแยกประเภททั่วไป** กรอกข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d3234-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="d3234-131">ในฟิลด์ **ปีบัญชีที่กำลังเปิด** เลือกปีบัญชีที่คุณต้องการโอนจำนวนงบประมาณที่เหลือไปยังโครงการ</span><span class="sxs-lookup"><span data-stu-id="d3234-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="d3234-132">ค่าเริ่มต้นคือหนึ่งปีหลังจากค่าในฟิลด์ **ปีงบประมาณโครงการ**</span><span class="sxs-lookup"><span data-stu-id="d3234-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="d3234-133">ในฟิลด์ **ระยะเวลายกยอดไป** เลือกช่วงเวลาที่คุณต้องการสร้างรายละเอียดการลงทะเบียนงบประมาณในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="d3234-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="d3234-134">โดยปกติจะเป็นช่วงแรกในการเปิดปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="d3234-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="d3234-135">ในกลุ่มฟิลด์ **คัดลอกจาก/ไปยัง** กรอกข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d3234-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="d3234-136">ในฟิลด์ **จากแบบจำลองการคาดการณ์** เลือกแบบจำลองการคาดการณ์งบประมาณโครงการที่เชื่อมโยงกับจำนวนงบประมาณที่เหลือที่คุณต้องการโอนสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="d3234-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="d3234-137">ในฟิลด์ **ไปยังแบบจำลองการคาดการณ์** เลือกแบบจำลองงบประมาณบัญชีแยกประเภททั่วไปที่เชื่อมโยงกับจำนวนงบประมาณที่คุณต้องการโอนไปยังบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="d3234-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="d3234-138">เลือก **โอนสกุลเงินการขาย** เพื่อใช้สกุลเงินการขายของโครงการสำหรับธุรกรรมบัญชีแยกประเภททั่วไปที่สร้างขึ้นเมื่อคุณโอนยอดงบประมาณสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="d3234-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="d3234-139">เมื่อไม่ได้เลือกตัวเลือก ธุรกรรมจะใช้สกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="d3234-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="d3234-140">เลือก **แสดงศูนย์ที่เหลือ** เพื่อรวมโครงการที่ไม่มีจำนวนงบประมาณเหลือ แต่ตรงตามเกณฑ์อื่น ๆ ที่คุณเลือกในโครงการที่แสดงในบานหน้าต่างด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="d3234-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="d3234-141">บนแท็บ **เลือกงบประมาณ** เลือก **ดึงงบประมาณทั้งหมด** เพื่อโหลดงบประมาณทั้งหมดที่ตรงกับเกณฑ์ที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="d3234-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="d3234-142">ถ้าคุณต้องการออกแบบแบบสอบถามฐานข้อมูลที่โหลดชุดงบประมาณโครงการที่ต้องการลงในบานหน้าต่าง ให้เลือก **ดึงงบประมาณที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="d3234-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="d3234-143">สำหรับแต่ละโครงการที่คุณต้องการดำเนินการ ให้เลือกตัวเลือกที่จุดเริ่มต้นของรายการสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="d3234-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="d3234-144">ในการเลือกโครงการทั้งหมดหรือเกือบทั้งหมด ให้เลือกเครื่องหมายถูกที่มุมบนซ้าย</span><span class="sxs-lookup"><span data-stu-id="d3234-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="d3234-145">หากต้องการยกเว้นการประมวลผลโครงการใด ๆ ให้ล้างเครื่องหมายถูกสำหรับโครงการนั้น</span><span class="sxs-lookup"><span data-stu-id="d3234-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="d3234-146">เมื่อต้องการโอนยอดงบประมาณที่เหลือสำหรับโครงการที่เลือกไปยังปีบัญชีที่เลือกและสร้างรายละเอียดการลงทะเบียนงบประมาณในบัญชีแยกประเภททั่วไป ให้เลือก **ดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="d3234-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="d3234-147">ดำเนินการยกยอดงบประมาณโดยไม่ต้องสร้างธุรกรรมบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="d3234-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="d3234-148">ไปที่ **การจัดการโครงการและการบัญชี** > **เป็นระยะ** > **งบประมาณ** > **ยกยอดงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="d3234-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="d3234-149">บนหน้า **กระบวนการยกยอดงบประมาณโครงการ** ในฟิลด์ **ตัวเลือกสิ้นปี** ให้เลือก **ดำเนินการยกยอดงบประมาณโครงการที่เหลือ**</span><span class="sxs-lookup"><span data-stu-id="d3234-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="d3234-150">ในกลุ่ม **พารามิเตอร์** ในฟิลด์ **ปีบัญชีโครงการ** เลือกปีบัญชีที่คุณต้องการดูจำนวนงบประมาณที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="d3234-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="d3234-151">ในกลุ่ม **คัดลอกจาก/ไปยัง** กรอกข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d3234-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="d3234-152">ในฟิลด์ **จากแบบจำลองการคาดการณ์** เลือกแบบจำลองการคาดการณ์งบประมาณโครงการที่เชื่อมโยงกับจำนวนงบประมาณที่เหลือที่คุณต้องการโอนสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="d3234-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="d3234-153">ให้เลือก **แสดงศูนย์ที่เหลือ** เพื่อรวมโครงการที่ไม่มีงบประมาณเหลือ แต่ตรงตามเกณฑ์ที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="d3234-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="d3234-154">ในกลุ่ม **เลือกงบประมาณ** เลือก **ดึงงบประมาณทั้งหมด** เพื่อโหลดงบประมาณทั้งหมดที่ตรงกับเกณฑ์ที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="d3234-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="d3234-155">ในการออกแบบแบบสอบถามฐานข้อมูลที่โหลดชุดงบประมาณโครงการที่ต้องการลงในบานหน้าต่าง ให้เลือก **ดึงงบประมาณที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="d3234-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="d3234-156">สำหรับแต่ละโครงการที่คุณต้องการดำเนินการ ให้เลือกตัวเลือกที่จุดเริ่มต้นของรายการสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="d3234-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="d3234-157">เลือก **ดำเนินการ** เพื่อโอนจำนวนงบประมาณที่เหลือสำหรับโครงการที่เลือกไปยังปีบัญชีที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d3234-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]