---
title: จัดการหน่วยที่ซับซ้อนสำหรับรายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์ - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการสนับสนุนการขายผลิตภัณฑ์ตามการสมัครใช้งาน
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177399"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="d8e0b-103">จัดการหน่วยที่ซับซ้อนสำหรับรายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์ - Lite</span><span class="sxs-lookup"><span data-stu-id="d8e0b-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="d8e0b-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="d8e0b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d8e0b-105">Dynamics 365 Project Operations จะใช้ปัจจัยปริมาณในการสนับสนุนยอดขายของผลิตภัณฑ์ตามการสม้ครสมาชิก</span><span class="sxs-lookup"><span data-stu-id="d8e0b-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="d8e0b-106">สำหรับผลิตภัณฑ์ตามการสมัครสมาชิก ปริมาณในสัญญาหรือรายการสัญญาโครงการจะแสดงเป็นจำนวนเดือนของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="d8e0b-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="d8e0b-107">ราคาของการสมัครใช้งานซอฟต์แวร์จะถูกเก็บไว้ในแคตาล็อกในรูปแบบราคาต่อเดือน ต่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="d8e0b-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="d8e0b-108">ระหว่างกระบวนการขาย ราคาในรายละเอียดการให้บริการตามสัญญาจะอยู่ในรูปแบบราคาต่อผู้ใช้ ต่อเดือน ที่จะได้รับการต่อรองและให้ส่วนลดโดยตัวแทนผู้ขายฝ่าย</span><span class="sxs-lookup"><span data-stu-id="d8e0b-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="d8e0b-109">ในแต่ละข้อตกลงจะมีจำนวนผู้ใช้ที่แตกต่างกันและจำนวนของเดือนของการสมัครใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d8e0b-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="d8e0b-110">ปริมาณที่ใช้ในการคำนวณจำนวนของรายละเอียดการให้บริการตามสัญญาเป็นผลิตภัณฑ์ของจำนวนผู้ใช้และจำนวนเดือนของการสมัครสมาชิก</span><span class="sxs-lookup"><span data-stu-id="d8e0b-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="d8e0b-111">เพื่อสนับสนุนการขายชนิดนี้ Project Operations จะรองรับคอนเซปต์ของ *ปัจจัยปริมาณ*</span><span class="sxs-lookup"><span data-stu-id="d8e0b-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="d8e0b-112">ปัจจับปริมาณขึ้นอยู่กับแอตทริบิวต์ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="d8e0b-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="d8e0b-113">เมื่อคุณกำหนดค่าของคุณสมบัติเฉพาะของผลิตภัณฑ์ คุณสามารถตั้งค่าสถานะส่วนย่อยของคุณสมบัตินั้น หรือคุณสมบัติทั้งหมด เป็นปัจจัยปริมาณ</span><span class="sxs-lookup"><span data-stu-id="d8e0b-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="d8e0b-114">Project Operations จะตรวจสอบว่าเฉพาะคุณสมบัติตัวเลขหรือคุณสมบัติผลิตภัณฑ์เท่านั้นที่มีการตั้งค่าสถานะชนิดข้อมูลแบบตัวเลขเป็นปัจจัยปริมาณ</span><span class="sxs-lookup"><span data-stu-id="d8e0b-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="d8e0b-115">เมื่อมีการเพิ่มผลิตภัณฑ์ที่มีปัจจัยด้านปริมาณที่กำหนดค่าไว้ในรายละเอียดการให้บริการตามสัญญา ฟิลด์ **ปริมาณ** จะกลายเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="d8e0b-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="d8e0b-116">หลังจากคุณป้อนค่าคุณสมบัติผลิตภัณฑ์ที่เป็นปัจจัยผลิตภัณฑ์ Project Operations จะคำนวณปริมาณของรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="d8e0b-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="d8e0b-117">ตัวอย่างเช่น Dynamics 365 Sales อาจมีคุณสมบัติดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d8e0b-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="d8e0b-118">**จำนวนของผู้ใช้**: จำนวนผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="d8e0b-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="d8e0b-119">**จำนวนของเดือน**: จำนวนเดือนที่สมัครใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d8e0b-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="d8e0b-120">**SKU ของผลิตภัณฑ์**: หน่วยเก็บสต็อก (SKU) สำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="d8e0b-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="d8e0b-121">คุณสมบัติ **จำนวนของผู้ใช้** และ **จำนวนของเดือน** สามารถตั้งค่าเป็นปัจจัยปริมาณโดยการแก้ไขคุณสมบัติของรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="d8e0b-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="d8e0b-122">ในการสร้างปัจจัยด้านปริมาณจากคุณสมบัติของผลิตภัณฑ์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d8e0b-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="d8e0b-123">บน **Project Operations** เลือก **การขาย - ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="d8e0b-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="d8e0b-124">เปิดผลิตภัณฑ์ที่คุณต้องการตั้งค่าปัจจัยด้านปริมาณ</span><span class="sxs-lookup"><span data-stu-id="d8e0b-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="d8e0b-125">ตรวจสอบให้แน่ใจว่าผลิตภัณฑ์มีคุณสมบัติที่ตั้งค่าไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="d8e0b-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="d8e0b-126">บนหน้า **ข้อมูลโครงการ** เลือกแท็บ **ปัจจัยปริมาณ**</span><span class="sxs-lookup"><span data-stu-id="d8e0b-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="d8e0b-127">ในตารางย่อย เลือก **+ การคำนวณฟิลด์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="d8e0b-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="d8e0b-128">ป้อนชื่อของ **ปัจจัยด้านปริมาณ** และเลือกค่าคุณสมบัติที่แม็ปกับการคำนวณฟิลด์</span><span class="sxs-lookup"><span data-stu-id="d8e0b-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="d8e0b-129">บันทึกและปิดฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="d8e0b-129">Save and close the form.</span></span>
7. <span data-ttu-id="d8e0b-130">ทำซ้ำขั้นตอนที่ 2-6 สำหรับคุณสมบัติทั้งหมดที่รวมกันจะประกอบเป็นปริมาณสำหรับรายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="d8e0b-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="d8e0b-131">ด้วยการตั้งค่าปัจจัยด้านปริมาณ เมื่อผู้ใช้สร้างรายละเอียดการให้บริการตามสัญญาสำหรับผลิตภัณฑ์นี้ ปริมาณของรายละเอียดการให้บริการตามสัญญาจะถูกล็อก</span><span class="sxs-lookup"><span data-stu-id="d8e0b-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="d8e0b-132">จากนั้นปริมาณจะถูกคำนวณเป็นผลคูณของมูลค่าคุณสมบัติสำหรับรายละเอียดการให้บริการตามสัญญานั้น</span><span class="sxs-lookup"><span data-stu-id="d8e0b-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>
