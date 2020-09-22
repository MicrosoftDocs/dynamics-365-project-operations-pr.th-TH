---
title: รับสินค้าในใบสั่งซื้อจากความต้องการสินค้า
description: หัวข้อนี้อธิบายวิธีการรับสินค้าในใบสั่งซื้อจากความต้องการสินค้า
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756361"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="c2902-103">รับสินค้าในใบสั่งซื้อจากความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="c2902-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c2902-104">หัวข้อนี้อธิบายวิธีการรับสินค้าในใบสั่งซื้อจากความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="c2902-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="c2902-105">ด้วยการใช้ความต้องการสินค้าแทนธุรกรรมสินค้า คุณสามารถวางแผนการจัดส่งก่อนที่สินค้าจะถูกใช้จริง สร้างใบสั่งซื้อ รวมสินค้าในกรอบเวลาของข้อตกลงทางการค้า และรวมความต้องการสินค้าในการวางแผนการผลิต</span><span class="sxs-lookup"><span data-stu-id="c2902-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="c2902-106">งานนี้ใช้ชุดข้อมูล USSI</span><span class="sxs-lookup"><span data-stu-id="c2902-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="c2902-107">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > โครงการ > โครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="c2902-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="c2902-108">ในรายการ ให้เลือกลิงค์ในแถวที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c2902-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="c2902-109">ในบานหน้าต่างการดำเนินการ เลือก **วางแผน**</span><span class="sxs-lookup"><span data-stu-id="c2902-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="c2902-110">เลือก **ความต้องการสินค้า**</span><span class="sxs-lookup"><span data-stu-id="c2902-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="c2902-111">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c2902-111">Select **New**.</span></span>
6. <span data-ttu-id="c2902-112">ในแถวใหม่ ให้ป้อนหรือเลือกค่าในฟิลด์ **หมายเลขสินค้า**</span><span class="sxs-lookup"><span data-stu-id="c2902-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="c2902-113">ในฟิลด์ **ปริมาณ** ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c2902-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="c2902-114">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c2902-114">Select **Save**.</span></span>
9. <span data-ttu-id="c2902-115">ในบานหน้าต่างการดำเนินการ เลือก **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="c2902-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="c2902-116">เลือก **ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="c2902-116">Select **Functions**.</span></span>
11. <span data-ttu-id="c2902-117">เลือก **สร้างใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="c2902-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="c2902-118">เลือกกล่องกาเครื่องหมาย **รวมทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="c2902-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="c2902-119">ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c2902-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="c2902-120">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c2902-120">Select **OK**.</span></span>
15. <span data-ttu-id="c2902-121">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="c2902-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="c2902-122">ในรายการ ให้เลือกลิงค์ในแถวที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c2902-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="c2902-123">ในบานหน้าต่างการดำเนินการ เลือก **ซื้อ**</span><span class="sxs-lookup"><span data-stu-id="c2902-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="c2902-124">เลือก **ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="c2902-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="c2902-125">ในบานหน้าต่างการดำเนินการ เลือก **รับ**</span><span class="sxs-lookup"><span data-stu-id="c2902-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="c2902-126">เลือก **ใบรับสินค้า**</span><span class="sxs-lookup"><span data-stu-id="c2902-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="c2902-127">ใน **ใบรับสินค้า** พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c2902-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="c2902-128">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c2902-128">Select **OK**.</span></span>

