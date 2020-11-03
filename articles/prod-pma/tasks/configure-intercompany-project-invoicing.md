---
title: กำหนดค่าการออกใบแจ้งหนี้โครงการระหว่างบริษัท
description: หัวข้อนี้แสดงวิธีตั้งค่าการออกใบแจ้งหนี้โครงการระหว่างสองบริษัทในองค์กรของคุณ
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085991"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="3c4cd-103">กำหนดค่าการออกใบแจ้งหนี้โครงการระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="3c4cd-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3c4cd-104">หัวข้อนี้แสดงวิธีตั้งค่าการออกใบแจ้งหนี้โครงการระหว่างสองบริษัทในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="3c4cd-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="3c4cd-105">งานนี้ใช้ชุดข้อมูล USSI</span><span class="sxs-lookup"><span data-stu-id="3c4cd-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="3c4cd-106">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > ผู้จัดจำหน่าย > ผู้จัดจำหน่ายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="3c4cd-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="3c4cd-107">ในรายการ **ผู้ขายทั้งหมด** ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="3c4cd-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="3c4cd-108">ในบานหน้าต่างการดำเนินการ เลือก **ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="3c4cd-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="3c4cd-109">เลือก **ระหว่างบริษัท**</span><span class="sxs-lookup"><span data-stu-id="3c4cd-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="3c4cd-110">ตั้งค่า **ใช้งานอยู่** เป็น **ใช่** เพื่อเปิดใช้งานการซื้อขายระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="3c4cd-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="3c4cd-111">ในฟิลด์ **บริษัทลูกค้า** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3c4cd-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="3c4cd-112">ในฟิลด์ **บัญชีของฉัน** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3c4cd-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="3c4cd-113">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3c4cd-113">Select **Save**.</span></span>
9. <span data-ttu-id="3c4cd-114">ปิดหน้าเพื่อกลับไปที่โฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="3c4cd-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="3c4cd-115">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > การตั้งค่า > พารามิเตอร์การจัดการโครงการและการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="3c4cd-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="3c4cd-116">เลือกแท็บ **ระหว่างบริษัท**</span><span class="sxs-lookup"><span data-stu-id="3c4cd-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="3c4cd-117">เลื่อนแถบเลื่อนไปที่ **ใช่** เพื่อเปิดใช้งานการจัดกำหนดการทรัพยากรระหว่างบริษัทและแผ่นเวลา</span><span class="sxs-lookup"><span data-stu-id="3c4cd-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="3c4cd-118">ในรายการ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3c4cd-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="3c4cd-119">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="3c4cd-119">Select **New**.</span></span>
15. <span data-ttu-id="3c4cd-120">ในฟิลด์ **นิติบุคคลที่ยืม** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3c4cd-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="3c4cd-121">เลือกกล่องกาเครื่องหมาย **สะสมรายได้**</span><span class="sxs-lookup"><span data-stu-id="3c4cd-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="3c4cd-122">ในฟิลด์ **ประเภทแผ่นเวลาเริ่มต้น** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3c4cd-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="3c4cd-123">ในฟิลด์ **ประเภทค่าใช้จ่ายเริ่มต้น** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3c4cd-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="3c4cd-124">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3c4cd-124">Select **Save**.</span></span>
20. <span data-ttu-id="3c4cd-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3c4cd-125">Close the page.</span></span>
21. <span data-ttu-id="3c4cd-126">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > การตั้งค่า > การลงรายการบัญชี > การตั้งค่าการลงรายการบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="3c4cd-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="3c4cd-127">ในฟิลด์ **ประเภทบัญชีแยกประเภท** เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="3c4cd-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="3c4cd-128">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="3c4cd-128">Select **New**.</span></span>
24. <span data-ttu-id="3c4cd-129">ในฟิลด์ **บัญชีหลัก** ของแถวใหม่ ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="3c4cd-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="3c4cd-130">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3c4cd-130">Select **Save**.</span></span>
26. <span data-ttu-id="3c4cd-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3c4cd-131">Close the page.</span></span>
27. <span data-ttu-id="3c4cd-132">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > การตั้งค่า > ราคา > โอนราคา**</span><span class="sxs-lookup"><span data-stu-id="3c4cd-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="3c4cd-133">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="3c4cd-133">Select **New**.</span></span>
29. <span data-ttu-id="3c4cd-134">ในฟิลด์ **วันที่มีผล** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="3c4cd-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="3c4cd-135">ในฟิลด์ **นิติบุคคลที่ยืม** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3c4cd-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="3c4cd-136">ในฟิลด์ **แบบจำลองราคาโอน** ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="3c4cd-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="3c4cd-137">ในฟิลด์ **ราคา** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="3c4cd-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="3c4cd-138">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3c4cd-138">Select **Save**.</span></span>

