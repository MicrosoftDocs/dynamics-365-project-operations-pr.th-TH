---
title: การจัดการหน่วยที่ซับซ้อน เช่น ต่อผู้ใช้ ต่อเดือน สำหรับใบเสนอราคาตามผลิตภัณฑ์ - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการจัดการหน่วยที่ซับซ้อนสำหรับรายการใบเสนอราคาตามผลิตภัณฑ์
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2ee46da2f663ef4f5f8fc7f9f89b6fcfd09a1798
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175599"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a><span data-ttu-id="c2c76-103">การจัดการหน่วยที่ซับซ้อน เช่น ต่อผู้ใช้ ต่อเดือน สำหรับใบเสนอราคาตามผลิตภัณฑ์ - Lite</span><span class="sxs-lookup"><span data-stu-id="c2c76-103">Managing complex units such as per-user, per-month for product-based quote lines - lite</span></span>

<span data-ttu-id="c2c76-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="c2c76-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c2c76-105">Dynamics 365 Project Operations จะใช้ปัจจัยปริมาณในการสนับสนุนยอดขายของผลิตภัณฑ์ตามการสม้ครสมาชิก</span><span class="sxs-lookup"><span data-stu-id="c2c76-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="c2c76-106">สำหรับผลิตภัณฑ์ตามการสมัครใช้งาน ปริมาณในใบเสนอราคาหรือรายการสัญญาโครงการจะแสดงเป็นจำนวนเดือนของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c2c76-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="c2c76-107">โดยทั่วไป ราคาของการสมัครใช้งานซอฟต์แวร์จะถูกเก็บไว้ในแคตาล็อกในรูปแบบราคาต่อเดือนต่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c2c76-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="c2c76-108">ระหว่างกระบวนการขาย ราคาในรายการเสนอราคาจะอยู่ในรูปแบบราคาต่อผู้ใช้ ต่อเดือน ที่จะได้รับการต่อรองและให้ส่วนลดโดยตัวแทนผู้ขายฝ่าย IT</span><span class="sxs-lookup"><span data-stu-id="c2c76-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="c2c76-109">ในแต่ละข้อตกลงจะมีจำนวนผู้ใช้ที่แตกต่างกันและจำนวนของเดือนของการสมัครใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c2c76-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="c2c76-110">ปริมาณที่ใช้ในการคำนวณรายการใบเสนอราคาเป็นผลิตภัณฑ์ของจำนวนผู้ใช้และจำนวนเดือนของการสมัครใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c2c76-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="c2c76-111">เพื่อสนับสนุนการขายชนิดนี้ Project Operations จะแนะนำคอนเซปต์ของปัจจัยปริมาณ</span><span class="sxs-lookup"><span data-stu-id="c2c76-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="c2c76-112">ปัจจับปริมาณขึ้นอยู่กับคุณลักษณะผลิตภัณฑ์ใน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c2c76-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="c2c76-113">เมื่อคุณตั้งค่าคอนฟิกของคุณสมบัติเฉพาะของผลิตภัณฑ์ Project Operations จะช่วยให้คุณตั้งค่าสถานะชุดย่อย หรือคุณสมบัติทั้งหมด เป็นปัจจัยปริมาณ</span><span class="sxs-lookup"><span data-stu-id="c2c76-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="c2c76-114">Project Operations จะตรวจสอบว่าเฉพาะคุณสมบัติตัวเลขหรือคุณสมบัติผลิตภัณฑ์เท่านั้นที่มีการตั้งค่าสถานะชนิดข้อมูลแบบตัวเลขเป็นปัจจัยปริมาณ</span><span class="sxs-lookup"><span data-stu-id="c2c76-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="c2c76-115">เมื่อคุณเพิ่มผลิตภัณฑ์ที่มีปัจจัยปริมาณลงในรายการใบเสนอราคา ฟิลด์ **ปริมาณ** จะกลายเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="c2c76-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="c2c76-116">หลังจากคุณป้อนค่าคุณสมบัติผลิตภัณฑ์ที่เป็นปัจจัยผลิตภัณฑ์ Project Operations จะคำนวณปริมาณของรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="c2c76-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="c2c76-117">ตัวอย่างเช่น Dynamics 365 Sales อาจมีคุณสมบัติดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c2c76-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="c2c76-118">**จำนวนของผู้ใช้**: จำนวนผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c2c76-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="c2c76-119">**จำนวนของเดือน**: จำนวนเดือนที่สมัครใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c2c76-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="c2c76-120">**Product SKU**</span><span class="sxs-lookup"><span data-stu-id="c2c76-120">**Product SKU**</span></span>

<span data-ttu-id="c2c76-121">คุณสามารถตั้งค่าคุณสมบัติ **จำนวนของผู้ใช้** และ **จำนวนของเดือน** เป็นปัจจัยปริมาณโดยการแก้ไขคุณสมบัติของรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="c2c76-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="c2c76-122">หากต้องการสร้างปัจจัยด้านปริมาณจากคุณสมบัติของผลิตภัณฑ์ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="c2c76-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="c2c76-123">ในบานหน้าต่างนำทางด้านซ้ายของ Project Operations ไปที่ **การขาย** > **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="c2c76-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="c2c76-124">เปิดผลิตภัณฑ์ที่คุณต้องการกำหนดค่าปัจจัยด้านปริมาณ</span><span class="sxs-lookup"><span data-stu-id="c2c76-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="c2c76-125">ตรวจสอบให้แน่ใจว่าผลิตภัณฑ์มีคุณสมบัติที่กำหนดค่าไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c2c76-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="c2c76-126">บนเพจ **ข้อมูลโครงการ** สำหรับผลิตภัณฑ์ เลือกแท็บ **ปัจจัยด้านปริมาณ**</span><span class="sxs-lookup"><span data-stu-id="c2c76-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="c2c76-127">ในตารางย่อย เลือก **+ การคำนวณฟิลด์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c2c76-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="c2c76-128">ป้อนชื่อของปัจจัยด้านปริมาณและเลือกค่าคุณสมบัติที่แม็ปกับการคำนวณฟิลด์</span><span class="sxs-lookup"><span data-stu-id="c2c76-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="c2c76-129">บันทึกและปิดฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="c2c76-129">Save and close the form.</span></span> <span data-ttu-id="c2c76-130">ทำซ้ำขั้นตอนเหล่านี้สำหรับคุณสมบัติทั้งหมดที่จะใช้ในการคำนวณปริมาณสำหรับรายการใบเสนอราคาตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c2c76-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="c2c76-131">เมื่อคุณสร้างรายการใบเสนอราคาตามผลิตภัณฑ์สำหรับผลิตภัณฑ์ ปริมาณของรายการใบเสนอราคาจะถูกล็อกไว้</span><span class="sxs-lookup"><span data-stu-id="c2c76-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="c2c76-132">ปริมาณจะมีการคำนวณเป็นผลิตภัณฑ์ที่มีค่าคุณสมบัติที่คุณป้อนสำหรับรายการใบเสนอราคานั้น</span><span class="sxs-lookup"><span data-stu-id="c2c76-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>
