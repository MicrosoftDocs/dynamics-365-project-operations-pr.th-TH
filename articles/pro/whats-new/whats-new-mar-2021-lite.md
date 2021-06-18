---
title: มีอะไรใหม่ในเดือนมีนาคม 2021 - การปรับใช้งาน Project Operations แบบ Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการอัปเดตคุณภาพที่มีอยู่ใน Project Operations รุ่นเดือนมีนาคม 2021 สำหรับการปรับใช้งาน Project Operations แบบ Lite
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: efddb96b2cb428b9dc0488c32eb5670d01322bcb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993889"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="5ff89-103">มีอะไรใหม่ในเดือนมีนาคม 2021 - การปรับใช้งาน Project Operations แบบ Lite</span><span class="sxs-lookup"><span data-stu-id="5ff89-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="5ff89-104">_นำไปใช้กับ: การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="5ff89-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="5ff89-105">หัวข้อนี้ใช้กับส่วนประกอบและรุ่นของ Dynamics 365 Project Operations ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5ff89-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="5ff89-106">Project Operations บนสภาพแวดล้อม Dataverse รุ่น 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="5ff89-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="5ff89-107">การปรับปรุงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="5ff89-107">Quality updates</span></span>

| <span data-ttu-id="5ff89-108">**พื้นที่คุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="5ff89-108">**Feature area**</span></span> | <span data-ttu-id="5ff89-109">**หมายเลขอ้างอิง**</span><span class="sxs-lookup"><span data-stu-id="5ff89-109">**Reference number**</span></span> | <span data-ttu-id="5ff89-110">**การปรับปรุงคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="5ff89-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5ff89-111">การเรียกเก็บเงินและการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="5ff89-111">Billing and pricing</span></span> | <span data-ttu-id="5ff89-112">2133873</span><span class="sxs-lookup"><span data-stu-id="5ff89-112">2133873</span></span> | <span data-ttu-id="5ff89-113">แก้ไขการแสดงผลของสัญลักษณ์สกุลเงิน **ราคาขายต่อหน่วย** ในตาราง **ประมาณการค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="5ff89-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="5ff89-114">การเรียกเก็บเงินและการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="5ff89-114">Billing and pricing</span></span> | <span data-ttu-id="5ff89-115">2174616</span><span class="sxs-lookup"><span data-stu-id="5ff89-115">2174616</span></span> | <span data-ttu-id="5ff89-116">เมื่อได้รับใบเสนอราคา รายการราคาที่กำหนดเองของสัญญาจะอ้างอิงตามรายละเอียดการให้บริการตามสัญญาที่คัดลอกมาจากใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="5ff89-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="5ff89-117">การจัดการโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="5ff89-117">Opportunity Management</span></span> | <span data-ttu-id="5ff89-118">2167475</span><span class="sxs-lookup"><span data-stu-id="5ff89-118">2167475</span></span> | <span data-ttu-id="5ff89-119">จำนวนเงินภาษีคงที่ในใบแจ้งหนี้การแก้ไขที่มาจากรายการข้อมูลจริงที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="5ff89-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="5ff89-120">การจัดการโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="5ff89-120">Opportunity Management</span></span> | <span data-ttu-id="5ff89-121">2176285</span><span class="sxs-lookup"><span data-stu-id="5ff89-121">2176285</span></span> | <span data-ttu-id="5ff89-122">ต้องไม่คัดลอกจำนวนเงินภาษีจากรายละเอียดรายการสัญญาการขาย/ใบเสนอราคาไปยังรายละเอียดรายการสัญญาต้นทุน/ใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="5ff89-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="5ff89-123">การจัดการโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="5ff89-123">Opportunity Management</span></span> | <span data-ttu-id="5ff89-124">2188079</span><span class="sxs-lookup"><span data-stu-id="5ff89-124">2188079</span></span> | <span data-ttu-id="5ff89-125">ต้องไม่สร้างกฎแบ่งการเรียกเก็บเงินสำหรับสัญญาที่ไม่อิงตามงาน</span><span class="sxs-lookup"><span data-stu-id="5ff89-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="5ff89-126">การวางแผนและการติดตาม</span><span class="sxs-lookup"><span data-stu-id="5ff89-126">Planning and Tracking</span></span> | <span data-ttu-id="5ff89-127">2138853</span><span class="sxs-lookup"><span data-stu-id="5ff89-127">2138853</span></span> | <span data-ttu-id="5ff89-128">ปรับปรุงฟังก์ชันการคัดลอกโครงการเพื่อให้แน่ใจว่ารายการประมาณการค่าใช้จ่ายที่อ้างอิงงานได้รับการคัดลอกไปยังโครงการปลายทาง</span><span class="sxs-lookup"><span data-stu-id="5ff89-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="5ff89-129">การวางแผนและการติดตาม</span><span class="sxs-lookup"><span data-stu-id="5ff89-129">Planning and Tracking</span></span> | <span data-ttu-id="5ff89-130">2173259</span><span class="sxs-lookup"><span data-stu-id="5ff89-130">2173259</span></span> | <span data-ttu-id="5ff89-131">ปรับปรุงฟังก์ชันการคัดลอกโครงการเพื่อให้แน่ใจว่าจะไม่แสดงข้อความแสดงข้อผิดพลาด **กำลังคัดลอก WBS** ในบางสถานการณ์</span><span class="sxs-lookup"><span data-stu-id="5ff89-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="5ff89-132">เวลาและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="5ff89-132">Time and Expense</span></span> | <span data-ttu-id="5ff89-133">2148910</span><span class="sxs-lookup"><span data-stu-id="5ff89-133">2148910</span></span> | <span data-ttu-id="5ff89-134">แก้ไขปัญหาการแสดงผลของเพจ **แก้ไขรายการ** ในตาราง **รายการเวลา**</span><span class="sxs-lookup"><span data-stu-id="5ff89-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="5ff89-135">เวลาและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="5ff89-135">Time and Expense</span></span> | <span data-ttu-id="5ff89-136">2159798</span><span class="sxs-lookup"><span data-stu-id="5ff89-136">2159798</span></span> | <span data-ttu-id="5ff89-137">การควบคุมที่รัดกุมขึ้นเพื่อให้แน่ใจว่าไม่สามารถแก้ไขรายการค่าใช้จ่ายที่ได้รับอนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="5ff89-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


