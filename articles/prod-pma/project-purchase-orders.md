---
title: ใบสั่งซื้อสำหรับโครงการ
description: บทความนี้อธิบายถึงวิธีการต่างๆ ที่คุณสามารถใช้เพื่อสร้างใบสั่งซื้อสำหรับโครงการ วิธีที่คุณใช้ขึ้นอยู่กับวัตถุประสงค์ของใบสั่งซื้อ และเมื่อมีการใช้สินค้าที่ซื้อและมีการเรียกเก็บเงินในโครงการ
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3f5d196e0d7db4a6d8c4cfe834a335f4ef737c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289212"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="0062e-104">ใบสั่งซื้อสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="0062e-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0062e-105">บทความนี้อธิบายถึงวิธีการต่างๆ ที่คุณสามารถใช้เพื่อสร้างใบสั่งซื้อสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="0062e-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="0062e-106">วิธีที่คุณใช้ขึ้นอยู่กับวัตถุประสงค์ของใบสั่งซื้อ และเมื่อมีการใช้สินค้าที่ซื้อและมีการเรียกเก็บเงินในโครงการ</span><span class="sxs-lookup"><span data-stu-id="0062e-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="0062e-107">วิธีการสร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="0062e-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="0062e-108">คุณสามารถใช้วิธีใดวิธีหนึ่งต่อไปนี้เพื่อสร้างใบสั่งซื้อในการจัดการโครงการและการบัญชี</span><span class="sxs-lookup"><span data-stu-id="0062e-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="0062e-109">วัตถุประสงค์ของใบสั่งซื้อจะกำหนดเมื่อมีการใช้ใบสั่งซื้อ และเมื่อมีการเรียกเก็บเงินสินค้าในโครงการด้วย</span><span class="sxs-lookup"><span data-stu-id="0062e-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0062e-110">วิธีการ</span><span class="sxs-lookup"><span data-stu-id="0062e-110">Method</span></span></th>
<th><span data-ttu-id="0062e-111">วัตถุประสงค์</span><span class="sxs-lookup"><span data-stu-id="0062e-111">Purpose</span></span></th>
<th><span data-ttu-id="0062e-112">การใช้สินค้า</span><span class="sxs-lookup"><span data-stu-id="0062e-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0062e-113">สร้างใบสั่งซื้อโดยตรงจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="0062e-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="0062e-114">ใช้วิธีนี้เพื่อซื้อสินค้าจากผู้จัดจำหน่ายภายนอกเพื่อใช้ในโครงการ</span><span class="sxs-lookup"><span data-stu-id="0062e-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="0062e-115">คุณสามารถสร้างใบสั่งซื้อได้สองวิธี:</span><span class="sxs-lookup"><span data-stu-id="0062e-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="0062e-116">จากตัวโครงการเอง</span><span class="sxs-lookup"><span data-stu-id="0062e-116">From the project itself.</span></span> <span data-ttu-id="0062e-117">ในกรณีนี้โครงการถูกกำหนดไว้แล้วสำหรับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="0062e-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="0062e-118">โดยไปที่ใบสั่งซื้อโครงการ</span><span class="sxs-lookup"><span data-stu-id="0062e-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="0062e-119">คุณต้องเลือกทั้งผู้จัดจำหน่ายและโครงการเพื่อสร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="0062e-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="0062e-120">สินค้าจะถูกใช้เมื่อมีการปรับปรุงใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="0062e-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0062e-121">สร้างใบสั่งซื้อโดยตรงจากใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0062e-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="0062e-122">ใช้วิธีนี้ซื้อสินค้าเมื่อคุณสร้างใบสั่งขายจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="0062e-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="0062e-123">สินค้าจะถูกใช้เมื่อมีการออกใบแจ้งหนี้ใบสั่งขายให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0062e-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0062e-124">สร้างใบสั่งซื้อจากความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="0062e-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="0062e-125">ใช้วิธีนี้ซื้อสินค้าเมื่อคุณสร้างความต้องการสินค้าจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="0062e-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="0062e-126">สินค้าจะถูกใช้เมื่อมีการอัปเดตบันทึกการจัดส่งความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="0062e-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="0062e-127">เมื่อคุณอัปเดตใบแจ้งหนี้ของผู้จัดจำหน่ายหรือบันทึกการจัดส่ง คุณจะได้รับพร้อมต์ให้อัปเดตบันทึกการจัดส่งตามความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="0062e-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="0062e-128">สำหรับข้อมูลเพิ่มเติม โปรดดู [รับสินค้าตามใบสั่งซื้อจากความต้องการสินค้า](tasks/receive-items-purchase-order-item-requirement.md)</span><span class="sxs-lookup"><span data-stu-id="0062e-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]