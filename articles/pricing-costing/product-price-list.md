---
title: รายการราคาของผลิตภัณฑ์
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับรายการราคาในการกำหนดราคาของแค็ตตาล็อกที่ใช้สำหรับใบเสนอราคาและสัญญาของโครงการ
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877514"
---
# <a name="product-price-lists"></a><span data-ttu-id="b497f-103">รายการราคาของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b497f-103">Product price lists</span></span>

<span data-ttu-id="b497f-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="b497f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="b497f-105">ใน Project Operations **รายการราคาของผลิตภัณฑ์** และเอนทิตีรายการในรายการราคาที่เกี่ยวข้องรองรับฟังก์ชันการทำงานการกำหนดราคาผลิตภัณฑ์ในรายการใบเสนอราคาและรายละเอียดการให้บริการตามสัญญาตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="b497f-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="b497f-106">สำหรับผลิตภัณฑ์ที่ใช้ในโครงการ จะมีการใช้เรกคอร์ดรายการในรายการราคาสำหรับรายการราคาของโครงการ</span><span class="sxs-lookup"><span data-stu-id="b497f-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="b497f-107">สินค้าจะต้องถูกกำหนดเพื่อให้กำหนดต้นทุนเริ่มต้นและรายการราคาในแคตาล็อกสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="b497f-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="b497f-108">ใช้รายการราคา ต้นทุนพื้นฐาน และต้นทุนปัจจุบันในการกำหนดค่าเริ่มต้นของต้นทุนและรายการราคา</span><span class="sxs-lookup"><span data-stu-id="b497f-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="b497f-109">รายการราคาเริ่มต้นจะถูกใช้ในรายการเสนอราคาและรายการสัญญาโครงการเมื่อระบบไม่สามารถค้นหารายการราคาสำหรับสินค้าในรายการราคาสินค้าสำหรับการเสนอราคาหรือสัญญาโครงการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b497f-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="b497f-110">ราคาต้นทุนของรายการผลิตภัณฑ์ในแคตาล็อกสามาถเปลี่ยนแปลงในระหว่างการเสนอราคาได้</span><span class="sxs-lookup"><span data-stu-id="b497f-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="b497f-111">ความสามารถนี้มีความสำคัญ เพราะถ้าคุณไม่สามารถติดตามต้นทุนได้อย่างถูกต้อง คุณจะไม่สามารถกำหนดกำไรจากการดำเนินการตามข้อตกลงของโครงการได้</span><span class="sxs-lookup"><span data-stu-id="b497f-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="b497f-112">ในบื้องต้น ต้นทุนพื้นฐานของสินค้าจะถูกใช้เป็นราคาต้นทุน</span><span class="sxs-lookup"><span data-stu-id="b497f-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="b497f-113">อย่างไรก็ตาม ราคาต้นทุนเริ่มต้นจะถูกอัพเดตบนรายการเสนอราคาถ้าเกิดความแตกต่างของราคาต้นทุนในการเสนอราคานั้น ๆ</span><span class="sxs-lookup"><span data-stu-id="b497f-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="b497f-114">รายการในรายการราคา</span><span class="sxs-lookup"><span data-stu-id="b497f-114">Price list items</span></span>

<span data-ttu-id="b497f-115">คุณสามารถเพิ่มผลิตภัณฑ์จากแคตาล็อกผลิตภัณฑ์ไปยังรายการราคาที่แตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="b497f-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="b497f-116">รายการราคาของผลิตภัณฑ์มักจะอ้างอิงถึงหน่วยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b497f-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="b497f-117">การกำหนดราคาของสินค้าในรายการราคาสามารถกำหนดค่าเป็นจำนวนสกุลเงินได้</span><span class="sxs-lookup"><span data-stu-id="b497f-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="b497f-118">เพื่อเป็นทางเลือก สามารถกำหนดค่าเป็นฟังก์ชั่นของรายการราคา ต้นทุนปัจจุบัน หรือต้นทุนพื้นฐานได้</span><span class="sxs-lookup"><span data-stu-id="b497f-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="b497f-119">ฟังก์ชันการทำงานการกำหนดราคารองรับตัวเลือกการปัดเศษต่างๆ เมือมีการกำหนดค่าราคาผลิตภัณฑ์เป็นฟังก์ชันของราคาในรายการ ต้นทุนมาตรฐาน หรือต้นทุนปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b497f-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="b497f-120">นอกจากนี้ ข้อดีของวิธีการกำหนดราคาที่มีหลากหลายและตัวเลือกการปัดเศษ จะทำให้คุณสามารถเชื่อมต่อรายการส่วนลดเข้ากับรายการราคาได้</span><span class="sxs-lookup"><span data-stu-id="b497f-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="b497f-121">การกำหนดค่าเริ่มต้นของรายการราคาผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b497f-121">Default product price list</span></span>
<span data-ttu-id="b497f-122">บันทึกของลูกค้าแต่ละรายจะอยู่ในฟิลด์ **Default Price List** ที่คุณสามารถกำหนดรายการราคาที่ตรงกันกับสกุลเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b497f-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="b497f-123">ค่าเริ่มต้นจะไม่ถูกป้อนลงไปในฟิลด์นี้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b497f-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="b497f-124">เมื่อมีข้อมูลข้อตกลงในการกำหนดราคาเองกับลูกค้าเฉพาะราย คุณจะสามารถใช้ฟิลด์นี้ในการเชื่อมรายการราคาเข้ากับลูกค้ารายนั้น ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="b497f-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="b497f-125">รายละเอียดของโอกาส การเสนอราคา และสัญญาโครงการ จะใช้คำสั่งตามนี้ในการป้อนรายการราคาเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b497f-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="b497f-126">คำสั่งเดียวกันจะถูกนำไปใข้ในรายการราคาของโครงการ</span><span class="sxs-lookup"><span data-stu-id="b497f-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="b497f-127">ใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="b497f-127">Quote</span></span>
2.  <span data-ttu-id="b497f-128">โอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="b497f-128">Opportunity</span></span>
3.  <span data-ttu-id="b497f-129">ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b497f-129">Customer</span></span>
4.  <span data-ttu-id="b497f-130">การตั้งค่าส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="b497f-130">Global settings</span></span> 

<span data-ttu-id="b497f-131">โดยค่าเริ่มต้น ฟิลด์ **Product** ในรายการเสนอราคาจะจัดเรียงสินค้าที่มีอยู่ในรายการราคาสินค้าของการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="b497f-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="b497f-132">ถ้าผลิตภัณฑ์ถูกระงับ หรือเป็นผลิตภัณฑ์ฉบับร่าง ผลิตภัณฑ์นั้นจะไม่ปรากฎในรายการสินค้าหรือแม้แต่ในรายการราคา</span><span class="sxs-lookup"><span data-stu-id="b497f-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="b497f-133">รายการแคตาล็อกของผลิตภัณฑ์จะถูกเพิ่มเป็นรายการแจ้งหนี้ในใบแจ้งหนี้ใบแรกที่ถูกสร้างขึ้นมาสำหรับสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="b497f-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="b497f-134">ในร่างใบแจ้งหนี้ รายการหนี้สินนั้นสามารถลบออกได้</span><span class="sxs-lookup"><span data-stu-id="b497f-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="b497f-135">ในกรณีนี้ รายการจะปรากฎบนใบแจ้งหนี้ในภายหลัง จนกว่าจะมีการออกใบแจ้งหนี้ หรือจนกว่าใบแจ้งหนี้นั้นจะถูกส่งไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b497f-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="b497f-136">คุณไม่สามารถแจ้งหนี้ในปริมาณเพียงบางส่วนของรายการแจ้งหนี้ของสินค้า</span><span class="sxs-lookup"><span data-stu-id="b497f-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="b497f-137">เมื่อการแจ้งหนี้ของรายการสินค้าจากสัญญาโครงการได้รับการยืนยัน ใบแจ้งหนี้ฉบับจริงจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="b497f-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="b497f-138">อย่างไรก็ตาม ใบแจ้งหนี้ฉบับจริงจะไม่เชื่อมต่อกับรายละเอียดของโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="b497f-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="b497f-139">ในทางตรงกันข้าม รายการสัญญาโครงการตามผลิตภัณฑ์จะเป็นอิสระจากการใช้งานตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="b497f-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
