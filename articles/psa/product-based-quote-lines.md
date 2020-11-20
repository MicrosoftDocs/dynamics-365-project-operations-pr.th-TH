---
title: รายการเสนอราคาตามผลิตภัณฑ์
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับรายการเสนอราคาตามผลิตภัณฑ์
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9c3b2b35abe894e79d6f55a7ddd6e5c64d0f12f2
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123240"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="0a11f-103">รายการเสนอราคาตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0a11f-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="0a11f-104">คุณจะสามารถสร้างรายการเสนอราคาตามผลิตภัณฑ์ได้ใน Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0a11f-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="0a11f-105">รายการเสนอราคาตามผลิตภัณฑ์สามารถเป็นรายการที่ "เขียนเพิ่ม" หรือเป็นรายการจากแคตาล็อกสินค้าก็ได้</span><span class="sxs-lookup"><span data-stu-id="0a11f-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="0a11f-106">แค็ตตาล็อกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0a11f-106">Product catalog</span></span>

<span data-ttu-id="0a11f-107">สินค้าในแคตาล็อกสินค้า Dynamics 365 product มีหน่วยเริ่มต้นและกลุ่มของหน่วย</span><span class="sxs-lookup"><span data-stu-id="0a11f-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="0a11f-108">ถ้าผลิตภัณฑ์หลายชนิดใช้ชุดของคุณลักษณะร่วมกัน คุณจะสามารถสร้างตระกูลผลิตภัณฑ์ที่มีลักษณะเหล่านั้นได้</span><span class="sxs-lookup"><span data-stu-id="0a11f-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="0a11f-109">ผลิตภัณฑ์ทั้งหมดในหนึ่งตระกูลผลิตภัณฑ์จะใช้ชุดของคุณลักษณะของผลิตภัณฑ์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="0a11f-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="0a11f-110">ตัวอย่างเช่น บริษัทขายใบอนุญาตการสมัครสมาชิกให้กับซอฟต์แวร์ที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="0a11f-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="0a11f-111">ซอฟต์แวร์ที่สมัครสมาชิกทั้งหมดจะมีสองคุณลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0a11f-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="0a11f-112">จำนวนของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="0a11f-112">Number of users</span></span> 
- <span data-ttu-id="0a11f-113">ระยะเวลาการสมัครสมาชิก (เป็นเดือน)</span><span class="sxs-lookup"><span data-stu-id="0a11f-113">Subscription duration (in months)</span></span>

<span data-ttu-id="0a11f-114">ทางที่ดีที่สุดในการรักษาขนิดของแคตาล็อกนี้คือการสร้างตระกูลผลิตภัณฑ์ที่มีชื่อว่า **Subscription Software** และมีคุณลักษณะ **Number of users** และ **Subscription duration**</span><span class="sxs-lookup"><span data-stu-id="0a11f-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="0a11f-115">จากนั้นคุณจะสามารถเพิ่มผลิตภัณฑ์แต่ละตัว เช่น **Dynamics 365 Sales** หรือ **Dynamics 365 Field Service** ไปยังตระกูลผลิตภัณฑ์ **Subscription Software**</span><span class="sxs-lookup"><span data-stu-id="0a11f-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="0a11f-116">เพิ่มรายการแคตาล็อกสินค้าลงในการเสนอราคาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0a11f-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="0a11f-117">การเสนอราคาโครงการและหน้าสัญญาโครงการจะมีส่วนของรายการสินค้าอยู่สองส่วน คือ รายการตามโครงการ และรายการตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0a11f-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="0a11f-118">สำหรับรายการตามผลิตภัณฑ์ สามารถใช้ Dynamics 365 เพื่อเพิ่มรายการจากแคตาล็อกสินค้าในการเสนอราคาได้</span><span class="sxs-lookup"><span data-stu-id="0a11f-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="0a11f-119">รายการแบบดร็อปดาวน์บนรายการเสนอราคาหรือรายการสัญญาโครงการประกอบด้วยสินค้าทั้งหมดและหน่วยในรายการราคาสินค้าที่แนบกับใบเสนอราคาหรือสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="0a11f-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="0a11f-120">คุณสามารถเพิ่มผลิตภัณฑ์ที่ไม่ได้เป็นส่วนหนึ่งของรายการราคาสินค้าของการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="0a11f-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="0a11f-121">นอกจากนี้ คุณยังสามารถเลือกผลิตภัณฑ์จากรายการสินค้าอื่น หรือคุณสามารถเลือกผลิตภัณฑ์โดยตรงจากแคตาล็อกสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="0a11f-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="0a11f-122">เมื่อคุณเลือกสินค้าจากแคตาล็อกสินค้าโดยตรง รายการราคาเริ่มต้นของผลิตภัณฑ์นั้นจะถูกใช้เป็นราคาขายของสินค้า</span><span class="sxs-lookup"><span data-stu-id="0a11f-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="0a11f-123">ถ้ารายการราคาเริ่มต้นยังไม่ได้รับการตั้งค่า ราคาจะถูกตั้งค่าเป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="0a11f-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="0a11f-124">ถ้ารายการเสนอราคาเป็นไปตามแคาล็อกสินค้า คุณจะสามารถกำหนดราคาขายได้โดยตรงบนรายการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="0a11f-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="0a11f-125">โปรดทราบว่ารายการเสนอราคาใน Dynamics 365 มีฟิลด์ **Pricing**</span><span class="sxs-lookup"><span data-stu-id="0a11f-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="0a11f-126">จะมีสองค่า</span><span class="sxs-lookup"><span data-stu-id="0a11f-126">Two values are available:</span></span>

- <span data-ttu-id="0a11f-127">การกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="0a11f-127">Override pricing</span></span>  
- <span data-ttu-id="0a11f-128">ใช้ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="0a11f-128">Use default</span></span>

<span data-ttu-id="0a11f-129">ถ้าคุณกำหนดค่าฟิลด์ลงใน **Override pricing**, Dynamics 365 จะไม่กำหนดราคาเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="0a11f-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="0a11f-130">คุณต้องป้อนราคาสำหรับผลิตภัณฑ์ในรายการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="0a11f-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="0a11f-131">ถ้าคุณกำหนดฟิลด์นี้ลงใน **Use default** Dynamics 365 จะใช้ราคาขายเริ่มต้นและล็อคฟิลด์เพื่อป้องกันการแก้ไขข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0a11f-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="0a11f-132">หลังจากคุณติดตั้ง PSA ราคาขายเริ่มต้นจะถูกป้อนเข้าไปในรายการตามผลิตภัณฑ์บนใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="0a11f-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="0a11f-133">ฟิลด์ **Pricing** จะถูกตั้งค่าใน **Override pricing** ทำให้คุณสามารถแก้ไขราคาเริ่มต้นในรายการเสนอราคาได้</span><span class="sxs-lookup"><span data-stu-id="0a11f-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![การตั้งค่าการกำหนดราคา](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="0a11f-135">ปัจจัยปริมาณสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0a11f-135">Quantity factors for products</span></span>

<span data-ttu-id="0a11f-136">PSA จะใช้ปัจจัยปริมาณในการสนับสนุนยอดขายของผลิตภัณฑ์ตามการสม้ครสมาชิก</span><span class="sxs-lookup"><span data-stu-id="0a11f-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="0a11f-137">สำหรับผลิตภัณฑ์ตามการสมัครสมาชิก ปริมาณในใบเสนอราคาหรือรายการสัญญาโครงการจะแสดงเป็นจำนวนเดือนของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="0a11f-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="0a11f-138">โดยทั่วไป ราคาของการสมัครสมาชิกซอฟต์แวร์จะถูกเก็บไว้ในแคตาล็อกในรูปแบบราคาต่อเดือนต่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="0a11f-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="0a11f-139">อย่างไรก็ตาม คุณสามารถใช้คำอธิบายของเวลาอื่นแทนได้</span><span class="sxs-lookup"><span data-stu-id="0a11f-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="0a11f-140">ระหว่างกระบวนการขาย ราคาในรายการเสนอราคาจะอยู่ในรูปแบบราคาต่อผู้ใช้ ต่อเดือน ที่จะได้รับการต่อรองและให้ส่วนลดโดยตัวแทนผู้ขายฝ่าย IT</span><span class="sxs-lookup"><span data-stu-id="0a11f-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="0a11f-141">ในแต่ละข้อตกลงจะมีจำนวนผู้ใช้ที่แตกต่างกันและจำนวนของเดือนของการสมัครสมาชิก</span><span class="sxs-lookup"><span data-stu-id="0a11f-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="0a11f-142">ปริมาณที่ใช้ในการคำนวณจำนวนของรายการเสนอราคาเป็นผลิตภัณฑ์ของจำนวนผู้ใช้และจำนวนเดือนของการสมัครสมาชิก</span><span class="sxs-lookup"><span data-stu-id="0a11f-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="0a11f-143">เพื่อสนับสนุนการขายชนิดนี้ PSA จะแนะนำคอนเซปต์ของปัจจัยปริมาณ</span><span class="sxs-lookup"><span data-stu-id="0a11f-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="0a11f-144">ปัจจับปริมาณขึ้นอยู่กับคุณลักษณะผลิตภัณฑ์ใน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="0a11f-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="0a11f-145">เมื่อคุณตั้งค่าคอนฟิกของคุณสมบัติเฉพาะของผลิตภัณฑ์ PSA จะช่วยให้คุณตั้งค่าสถานะส่วนย่อยของคุณสมบัตินั้น หรือคุณสมบัติทั้งหมด เป็นปัจจัยปริมาณ</span><span class="sxs-lookup"><span data-stu-id="0a11f-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="0a11f-146">PSA ทำให้คุณลักษณะทางตัวเลขนั้นมีผลสมบูรณ์ หรือคุณสมบัติผลิตภัณฑ์ที่มีชนิดข้อมูลแบบตัวเลขถูกตั้งค่าเป็นปัจจัยปริมาณ</span><span class="sxs-lookup"><span data-stu-id="0a11f-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="0a11f-147">เมื่อมีการเพิ่มผลิตภัณฑ์ที่ปัจจัยผลิตภัณฑ์ถูกกำหนดค่าในรายการใบเสนอราคา ฟิลด์ **Quantity** ในรายการเสนอราคาจะกลายเป็นฟิลด์ที่อ่านได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0a11f-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="0a11f-148">หลังจากคุณป้อนค่าคุณสมบัติผลิตภัณฑ์ที่เป็นปัจจัยผลิตภัณฑ์ PSA จะคำนวณปริมาณของรายการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="0a11f-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="0a11f-149">ตัวอย่างเช่น Dynamics 365 อาจมีคุณสมบัติดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0a11f-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="0a11f-150">**No of users** - จำนวนผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="0a11f-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="0a11f-151">**No of Months** - จำนวนเดือนที่สมัครสมาชิก</span><span class="sxs-lookup"><span data-stu-id="0a11f-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="0a11f-152">**Product SKU**</span><span class="sxs-lookup"><span data-stu-id="0a11f-152">**Product SKU**</span></span> 

<span data-ttu-id="0a11f-153">คุณสมบัติ **No of Users** และ **No of Months** สามารถถูกตั้งค้่เป็นปัจจัยปริมาณโดยการแก้ไขคุณสมบัติของรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="0a11f-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![การตั้งค่าจำนวนของผู้ใช้และจำนวนเดือนเป็นปัจจัยปริมาณ](media/basic-guide-11.png)
 
