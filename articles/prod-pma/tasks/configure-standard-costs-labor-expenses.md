---
title: กำหนดค่าต้นทุนมาตรฐานสำหรับแรงงานและค่าใช้จ่าย
description: หัวข้อนี้จะอธิบายวิธีตั้งค่าต้นทุนมาตรฐานสำหรับแรงงานและค่าใช้จ่ายสำหรับโครงการ
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085989"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="6e84c-103">กำหนดค่าต้นทุนมาตรฐานสำหรับแรงงานและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="6e84c-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6e84c-104">หัวข้อนี้จะอธิบายวิธีตั้งค่าต้นทุนมาตรฐานสำหรับแรงงานและค่าใช้จ่ายสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="6e84c-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="6e84c-105">งานนี้ใช้ชุดข้อมูล USSI</span><span class="sxs-lookup"><span data-stu-id="6e84c-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="6e84c-106">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > การตั้งค่า > ราคา > ราคาต้นทุน (ชั่วโมง)**</span><span class="sxs-lookup"><span data-stu-id="6e84c-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="6e84c-107">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6e84c-107">Select **New**.</span></span>
3. <span data-ttu-id="6e84c-108">ในฟิลด์ **วันที่มีผล** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="6e84c-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="6e84c-109">ในฟิลด์ **ราคาต้นทุน** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6e84c-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="6e84c-110">คุณสามารถกำหนดราคาต้นทุนมาตรฐานสำหรับประเภทโครงการ หรือตั้งราคาต้นทุนตามหมายเลขผู้ปฏิบัติงาน หมายเลขโครงการ ประเภท วันที่ หรือชุดค่าผสมเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="6e84c-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="6e84c-111">ราคาต้นทุนที่ใช้เป็นราคาต้นทุนที่มีรายละเอียดระดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="6e84c-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="6e84c-112">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6e84c-112">Select **Save**.</span></span>
6. <span data-ttu-id="6e84c-113">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > การตั้งค่า > ราคา > ราคาขาย (ชั่วโมง)**</span><span class="sxs-lookup"><span data-stu-id="6e84c-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="6e84c-114">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6e84c-114">Select **New**.</span></span>
8. <span data-ttu-id="6e84c-115">ในฟิลด์ **วันที่มีผล** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="6e84c-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="6e84c-116">ในฟิลด์ **ใช้ได้สำหรับ** ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="6e84c-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="6e84c-117">ในฟิลด์ **ราคา** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6e84c-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="6e84c-118">คุณสามารถกำหนดราคาขายมาตรฐานสำหรับธุรกรรมรายชั่วโมงหรือสำหรับประเภทโครงการ</span><span class="sxs-lookup"><span data-stu-id="6e84c-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="6e84c-119">คุณยังสามารถตั้งราคาขายตามหมายเลขผู้ปฏิบัติงาน หมายเลขโครงการ ประเภท วันที่ทำธุรกรรม หรือชุดค่าผสมเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="6e84c-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="6e84c-120">ราคาขายจริง ซึ่งใช้เมื่อผู้ปฏิบัติงานป้อนธุรกรรมในสมุดรายวันชั่วโมง คือราคาขายที่มีรายละเอียดระดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="6e84c-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="6e84c-121">ตัวอย่างเช่น หากมีการตั้งค่าทั้งราคาขายทั่วไปและราคาขายเฉพาะ ผู้ปฏิบัติงานระบบจะใช้ราคาขายเฉพาะผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="6e84c-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="6e84c-122">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6e84c-122">Select **Save**.</span></span>
12. <span data-ttu-id="6e84c-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e84c-123">Close the page.</span></span>
13. <span data-ttu-id="6e84c-124">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > การตั้งค่า > ราคา > ราคาต้นทุน (ค่าใช้จ่าย)**</span><span class="sxs-lookup"><span data-stu-id="6e84c-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="6e84c-125">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6e84c-125">Select **New**.</span></span>
15. <span data-ttu-id="6e84c-126">ในฟิลด์ **วันที่มีผล** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="6e84c-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="6e84c-127">ในฟิลด์ **ราคาต้นทุน** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6e84c-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="6e84c-128">สามารถกรอกข้อมูลได้หลายฟิลด์ แต่เป็นจำนวนขั้นต่ำที่จำเป็นในการบันทึกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="6e84c-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="6e84c-129">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6e84c-129">Select **Save**.</span></span>
18. <span data-ttu-id="6e84c-130">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > การตั้งค่า > ราคา > ราคาขาย (ค่าใช้จ่าย)**</span><span class="sxs-lookup"><span data-stu-id="6e84c-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="6e84c-131">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6e84c-131">Select **New**.</span></span>
20. <span data-ttu-id="6e84c-132">ในฟิลด์ **วันที่มีผล** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="6e84c-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="6e84c-133">ในฟิลด์ **ใช้ได้สำหรับ** ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="6e84c-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="6e84c-134">ในฟิลด์ **ราคา** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6e84c-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="6e84c-135">ราคาขายจริง ซึ่งใช้เมื่อผู้ปฏิบัติงานป้อนธุรกรรมในสมุดรายวันค่าใช้จ่าย คือราคาขายที่มีรายละเอียดระดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="6e84c-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="6e84c-136">ตัวอย่างเช่น หากมีการตั้งค่าทั้งราคาขายทั่วไปและราคาขายเฉพาะผู้ปฏิบัติงาน ระบบจะใช้ราคาขายเฉพาะผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="6e84c-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="6e84c-137">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6e84c-137">Select **Save**.</span></span>

