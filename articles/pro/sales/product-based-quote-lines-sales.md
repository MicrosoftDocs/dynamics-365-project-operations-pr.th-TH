---
title: ภาพรวมรายการใบเสนอราคาตามผลิตภัณฑ์ - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการทำงานกับรายการใบเสนอราคาตามผลิตภัณฑ์
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178211"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="5751f-103">ภาพรวมรายการใบเสนอราคาตามผลิตภัณฑ์ - Lite</span><span class="sxs-lookup"><span data-stu-id="5751f-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="5751f-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="5751f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5751f-105">คุณจะสามารถสร้างรายการเสนอราคาตามผลิตภัณฑ์ได้ใน Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="5751f-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="5751f-106">รายการเสนอราคาตามผลิตภัณฑ์สามารถเพิ่มได้ด้วยตนเอง หรือเป็นรายการจากแคตาล็อกสินค้าก็ได้</span><span class="sxs-lookup"><span data-stu-id="5751f-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="5751f-107">แค็ตตาล็อกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5751f-107">Product catalog</span></span>

<span data-ttu-id="5751f-108">สินค้าแต่ละรายการในแคตาล็อกสินค้ามีหน่วยเริ่มต้นและกลุ่มของหน่วย</span><span class="sxs-lookup"><span data-stu-id="5751f-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="5751f-109">ถ้าผลิตภัณฑ์หลายชนิดใช้ชุดของคุณลักษณะร่วมกัน คุณจะสามารถสร้างตระกูลผลิตภัณฑ์ที่มีลักษณะเหล่านั้นร่วมกันได้</span><span class="sxs-lookup"><span data-stu-id="5751f-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="5751f-110">ตัวอย่างเช่น บริษัทขายใบอนุญาตการสมัครสมาชิกให้กับซอฟต์แวร์ประเภทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="5751f-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="5751f-111">ซอฟต์แวร์ที่สมัครสมาชิกทั้งหมดจะมีสองคุณลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5751f-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="5751f-112">จำนวนผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="5751f-112">Number of users</span></span>
- <span data-ttu-id="5751f-113">ระยะเวลาการสมัครสมาชิกถูกวัดเป็นเดือน</span><span class="sxs-lookup"><span data-stu-id="5751f-113">A subscription duration measured in months</span></span>

<span data-ttu-id="5751f-114">ในการรักษาขนิดของแคตาล็อกนี้ สร้างตระกูลผลิตภัณฑ์ที่มีชื่อว่า **ซอฟต์แวร์การบอกรับเป็นสมาชิก** และเพิ่มจำนวนผู้ใช้และระยะเวลาการสมัครสมาชิกเป็นแอตทริบิวต์</span><span class="sxs-lookup"><span data-stu-id="5751f-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="5751f-115">จากนั้น คุณสามารถเพิ่มผลิตภัณฑ์แต่ละรายการลงในตระกูลผลิตภัณฑ์ **ซอฟต์แวร์การบอกรับเป็นสมาชิก**</span><span class="sxs-lookup"><span data-stu-id="5751f-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="5751f-116">เพิ่มรายการแคตาล็อกสินค้าลงในการเสนอราคาโครงการ</span><span class="sxs-lookup"><span data-stu-id="5751f-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="5751f-117">หน้า **ใบเสนอราคาโครงการ** และ **สัญญาโครงการ** จะมีส่วนของรายการตามโครงการ และรายการตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5751f-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="5751f-118">สำหรับรายการตามผลิตภัณฑ์ รายการแบบดร็อปดาวน์บนรายการเสนอราคาหรือรายการสัญญาโครงการประกอบด้วยสินค้าทั้งหมดและหน่วยในรายการราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="5751f-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="5751f-119">คุณสามารถเพิ่มผลิตภัณฑ์ที่ไม่ได้เป็นส่วนหนึ่งของราคาตลาดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5751f-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="5751f-120">นอกจากนี้ คุณยังสามารถเลือกผลิตภัณฑ์จากรายการสินค้าอื่น หรือโดยตรงจากแคตาล็อกสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="5751f-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="5751f-121">เมื่อคุณเลือกสินค้าจากแคตาล็อกสินค้าโดยตรง รายการราคาเริ่มต้นของผลิตภัณฑ์นั้นจะถูกใช้เป็นราคาขายของสินค้า</span><span class="sxs-lookup"><span data-stu-id="5751f-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="5751f-122">ถ้ารายการราคาเริ่มต้นยังไม่ได้รับการตั้งค่า ราคาจะถูกตั้งค่าเป็นศูนย์ (0)</span><span class="sxs-lookup"><span data-stu-id="5751f-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="5751f-123">เมื่อรายการเสนอราคาเป็นไปตามแคาล็อกสินค้า คุณจะสามารถกำหนดราคาขายได้โดยตรงบนรายการเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="5751f-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="5751f-124">รายการใบเสนอราคาในฟิลด์ **การกำหนดราคา** มีค่าที่ใช้ได้สองค่า:</span><span class="sxs-lookup"><span data-stu-id="5751f-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="5751f-125">**ราคาที่ใช้แทน**</span><span class="sxs-lookup"><span data-stu-id="5751f-125">**Override Pricing**</span></span>
- <span data-ttu-id="5751f-126">**ใช้ค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="5751f-126">**Use Default**</span></span>

<span data-ttu-id="5751f-127">หากคุณเลือก **การกำหนดราคาที่ใช้แทน** ราคาเริ่มต้นไม่ได้กำหนด</span><span class="sxs-lookup"><span data-stu-id="5751f-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="5751f-128">คุณต้องป้อนราคาสำหรับผลิตภัณฑ์ในรายการเสนอราคาแทน</span><span class="sxs-lookup"><span data-stu-id="5751f-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="5751f-129">หากคุณเลือก **ใช้ค่าเริ่มต้น** ราคาขายเริ่มต้นจะถูกใช้ และฟิลด์จะถูกล็อกเพื่อแก้ไข</span><span class="sxs-lookup"><span data-stu-id="5751f-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="5751f-130">ราคาขายเริ่มต้นจะถูกป้อนเข้าไปในรายการตามผลิตภัณฑ์บนใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="5751f-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="5751f-131">ฟิลด์ **ราคา** จะถูกตั้งค่าใน **ราคาที่ใช้แทน** ทำให้คุณสามารถแก้ไขราคาเริ่มต้นในรายการเสนอราคาได้</span><span class="sxs-lookup"><span data-stu-id="5751f-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="5751f-132">นี่คือการแทนที่เฉพาะ Project Operations สำหรับลักษณะการทำงานของรายการตามผลิตภัณฑ์ใน Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="5751f-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>
