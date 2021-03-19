---
title: ภารวมของรายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์ - Lite
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับรายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6e9ef33cc9c79f828e85733f4f5a199bce842700
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272681"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="bd164-103">ภารวมของรายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์ - Lite</span><span class="sxs-lookup"><span data-stu-id="bd164-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="bd164-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="bd164-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bd164-105">คุณสามารถสร้างรายละเอียดการให้บริการตามสัญญาแบบตามผลิตภัณฑ์ได้ใน Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="bd164-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="bd164-106">รายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์สามารถสร้างรายการด้วยตนเอง หรือเป็นรายการจากแคตาล็อกสินค้าก็ได้</span><span class="sxs-lookup"><span data-stu-id="bd164-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="bd164-107">แค็ตตาล็อกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bd164-107">Product catalog</span></span>

<span data-ttu-id="bd164-108">สินค้าในแค็ตตาล็อกผลิตภัณฑ์มีหน่วยเริ่มต้นและกลุ่มของหน่วย</span><span class="sxs-lookup"><span data-stu-id="bd164-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="bd164-109">ถ้าผลิตภัณฑ์หลายชนิดใช้ชุดของคุณลักษณะร่วมกัน คุณจะสามารถสร้างตระกูลผลิตภัณฑ์ที่มีลักษณะเหล่านั้นได้</span><span class="sxs-lookup"><span data-stu-id="bd164-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="bd164-110">ผลิตภัณฑ์ทั้งหมดในหนึ่งตระกูลผลิตภัณฑ์จะใช้ชุดของคุณลักษณะของผลิตภัณฑ์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="bd164-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="bd164-111">ตัวอย่างเช่น บริษัทขายใบอนุญาตการสมัครสมาชิกให้กับซอฟต์แวร์ประเภทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="bd164-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="bd164-112">ซอฟต์แวร์ที่สมัครสมาชิกทั้งหมดจะมีสองคุณลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bd164-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="bd164-113">จำนวนผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="bd164-113">Number of users</span></span>
- <span data-ttu-id="bd164-114">ระยะเวลาการสมัครสมาชิก (เป็นเดือน)</span><span class="sxs-lookup"><span data-stu-id="bd164-114">Subscription duration (in months)</span></span>

<span data-ttu-id="bd164-115">เพื่อรักษาแค็ตตาล็อกประเภทนี้ ให้สร้างตระกูลผลิตภัณฑ์ที่มีชื่อว่า **ซอฟต์แวร์การบอกรับเป็นสมาชิก**</span><span class="sxs-lookup"><span data-stu-id="bd164-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="bd164-116">เพิ่มแอตทริบิวต์ **จำนวนผู้ใช้** และ **ระยะเวลาการสมัครสมาชิก** ไปยังตระกูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bd164-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="bd164-117">จากนั้น เพิ่มผลิตภัณฑ์แต่ละรายการลงในตระกูลผลิตภัณฑ์ **ซอฟต์แวร์การบอกรับเป็นสมาชิก**</span><span class="sxs-lookup"><span data-stu-id="bd164-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="bd164-118">เพิ่มรายการแคตาล็อกสินค้าลงในสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="bd164-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="bd164-119">สัญญาโครงการและหน้าสัญญาโครงการจะมีส่วนของรายการสินค้าอยู่สองส่วน ตามโครงการ และตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bd164-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="bd164-120">รายการตามผลิตภัณฑ์รวมถึงผลิตภัณฑ์และหน่วยทั้งหมดในรายการราคาของผลิตภัณฑ์ในสัญญา</span><span class="sxs-lookup"><span data-stu-id="bd164-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="bd164-121">ผลิตภัณฑ์ที่ไม่ได้เป็นส่วนหนึ่งของรายการราคาสินค้าของสัญญาสามารถเพิ่มได้</span><span class="sxs-lookup"><span data-stu-id="bd164-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="bd164-122">คุณสามารถเลือกสินค้าจากรายการราคาอื่น ๆ หรือจากแคตตาล็อกผลิตภัณฑ์โดยตรง</span><span class="sxs-lookup"><span data-stu-id="bd164-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="bd164-123">เมื่อคุณเลือกสินค้าจากแคตาล็อกสินค้าโดยตรง รายการราคาเริ่มต้นของผลิตภัณฑ์นั้นจะถูกใช้เป็นราคาขายของสินค้า</span><span class="sxs-lookup"><span data-stu-id="bd164-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="bd164-124">ถ้ารายการราคาเริ่มต้นยังไม่ได้รับการตั้งค่า ราคาจะถูกตั้งค่าเป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="bd164-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="bd164-125">ถ้ารายละเอียดการให้บริการตามสัญญาเป็นไปตามแคตตาล็อกสินค้า คุณจะสามารถกำหนดราคาขายได้โดยตรงบนรายการ</span><span class="sxs-lookup"><span data-stu-id="bd164-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="bd164-126">รายละเอียดการให้บริการตามสัญญามีฟิลด์ **ราคา** ที่มีสองค่า:</span><span class="sxs-lookup"><span data-stu-id="bd164-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="bd164-127">**การกำหนดราคา**</span><span class="sxs-lookup"><span data-stu-id="bd164-127">**Override pricing**</span></span>
- <span data-ttu-id="bd164-128">**ใช้ค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="bd164-128">**Use default**</span></span>

<span data-ttu-id="bd164-129">ถ้าคุณกำหนดค่าฟิลด์ **ราคา** ไปที่ **การกำหนดราคา** ราคาเริ่มต้นจะไม่ถูกกำหนด</span><span class="sxs-lookup"><span data-stu-id="bd164-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="bd164-130">ป้อนราคาสำหรับผลิตภัณฑ์ในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="bd164-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="bd164-131">หากคุณตั้งค่าฟิลด์เป็น **ใช้ค่าเริ่มต้น** ราคาขายเริ่มต้นถูกใช้และไม่สามารถแก้ไขฟิลด์ได้</span><span class="sxs-lookup"><span data-stu-id="bd164-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="bd164-132">หลังจากคุณติดตั้ง Project Operations ราคาขายเริ่มต้นจะถูกป้อนเข้าไปในรายการตามผลิตภัณฑ์บนสัญญา</span><span class="sxs-lookup"><span data-stu-id="bd164-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="bd164-133">ฟิลด์ **Pricing** จะถูกตั้งค่าใน **Override pricing** ทำให้คุณสามารถแก้ไขราคาเริ่มต้นในรายละเอียดการให้บริการตามสัญญาได้</span><span class="sxs-lookup"><span data-stu-id="bd164-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="bd164-134">นี่คือการแทนที่เฉพาะ Project Operations สำหรับลักษณะการทำงานของรายการตามผลิตภัณฑ์ใน Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="bd164-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]