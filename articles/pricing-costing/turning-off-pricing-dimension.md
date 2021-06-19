---
title: การปิดมิติการกำหนดราคา
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการปิดมิติการกำหนดราคา
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 7b7c1d1b3363c0d158fcf6fda532822354b852a3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004554"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="4d7ef-103">การปิดมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="4d7ef-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="4d7ef-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="4d7ef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4d7ef-105">คุณอาจต้องตรวจสอบและอัปเดกลยุทธ์การกำหนดราคาของคุณทุกสองสามปี</span><span class="sxs-lookup"><span data-stu-id="4d7ef-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="4d7ef-106">การอัปเดตใดๆที่คุณทำอาจต้องการให้คุณปิดมิติการกำหนดราคาที่มีอยู่และสร้างรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="4d7ef-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="4d7ef-107">ตัวอย่างเช่น คุณอาจจะมีการกำหนดราคาก่อนหน้านี้โดย **บทบาท** แต่ตอนนี้คุณได้ตัดสินใจที่จะให้ราคาตาม **ประสบการณ์การทำงาน**</span><span class="sxs-lookup"><span data-stu-id="4d7ef-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="4d7ef-108">การทำเช่นนี้อาจทำให้คุณจำเป็นต้องปิด **บทบาท** เป็นมิติการกำหนดราคาและสร้าง **ประสบการณ์การทำงาน** เป็นมิติการกำหนดราคาใหม่</span><span class="sxs-lookup"><span data-stu-id="4d7ef-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="4d7ef-109">การปิดมิติการกำหนดราคา โดยไม่คำนึงถึงว่าจะเป็นแบบสำเร็จรูปหรือกำหนดเอง สามารถทำได้โดยการตั้งค่าที่ฟิลด์ **สามารถใช้งานได้กับต้นทุน** และ **สามารถใช้งานได้กับการขาย** ของมิติการกำหนดราคาเป็น **ไม่ใช่**</span><span class="sxs-lookup"><span data-stu-id="4d7ef-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="4d7ef-110">อย่างไรก็ตาม เมื่อคุณทำเช่นนี้ คุณอาจได้รับข้อความแสดงข้อผิดพลาด **ไม่สามารถปรับปรุงหรือลบมิติการกำหนดราคาได้หากมีเรกคอร์ดราคาที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="4d7ef-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![ข้อผิดพลาดของกระบวนการทางธุรกิจมีแนวโน้มเมื่อปิดมิติการกำหนดราคา](media/Business-Process-Error.png)

<span data-ttu-id="4d7ef-112">ข้อความข้อผิดพลาดนี้บ่งชี้ว่ามีเรกคอร์ดราคาที่ตั้งค่าไว้ก่อนหน้านี้สำหรับมิติที่ถูกปิด</span><span class="sxs-lookup"><span data-stu-id="4d7ef-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="4d7ef-113">เรกคอร์ด **ราคาตามบทบาท** และ **ส่วนเพิ่มราคาของราคาตามบทบาท** ทั้งหมดที่อ้างอิงถึงมิติต้องถูกลบก่อนที่การบังคับใช้ของมิติสามารถตั้งค่าเป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="4d7ef-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="4d7ef-114">กฎนี้ใช้ได้กับทั้งมิติการกำหนดราคาแบบสำเร็จรูปและมิติการกำหนดราคาที่กำหนดเองที่คุณอาจสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="4d7ef-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="4d7ef-115">เหตุผลสำหรับการตรวจสอบความถูกต้องนี้เป็นเพราะเรกคอร์ด **ราคาตามบทบาท** แต่ละเรกคอร์ดต้องมีชุดรวมของมิติที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="4d7ef-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="4d7ef-116">ตัวอย่างเช่น ในรายการราคาที่เรียกว่า **อัตราต้นทุน US 2018** คุณมีแถว **ราคาตามบทบาท** ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4d7ef-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="4d7ef-117">ชื่อมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="4d7ef-117">Standard Title</span></span>         | <span data-ttu-id="4d7ef-118">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="4d7ef-118">Org Unit</span></span>    |<span data-ttu-id="4d7ef-119">หน่วย</span><span class="sxs-lookup"><span data-stu-id="4d7ef-119">Unit</span></span>   |<span data-ttu-id="4d7ef-120">ราคา</span><span class="sxs-lookup"><span data-stu-id="4d7ef-120">Price</span></span>  |<span data-ttu-id="4d7ef-121">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="4d7ef-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="4d7ef-122">วิศวกรระบบ</span><span class="sxs-lookup"><span data-stu-id="4d7ef-122">Systems Engineer</span></span>|<span data-ttu-id="4d7ef-123">Contoso US</span><span class="sxs-lookup"><span data-stu-id="4d7ef-123">Contoso US</span></span>|<span data-ttu-id="4d7ef-124">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="4d7ef-124">Hour</span></span>| <span data-ttu-id="4d7ef-125">100</span><span class="sxs-lookup"><span data-stu-id="4d7ef-125">100</span></span>|<span data-ttu-id="4d7ef-126">USD</span><span class="sxs-lookup"><span data-stu-id="4d7ef-126">USD</span></span>|
| <span data-ttu-id="4d7ef-127">วิศวกรระบบรุ่นพี่</span><span class="sxs-lookup"><span data-stu-id="4d7ef-127">Senior Systems Engineer</span></span>|<span data-ttu-id="4d7ef-128">Contoso US</span><span class="sxs-lookup"><span data-stu-id="4d7ef-128">Contoso US</span></span>|<span data-ttu-id="4d7ef-129">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="4d7ef-129">Hour</span></span>| <span data-ttu-id="4d7ef-130">150</span><span class="sxs-lookup"><span data-stu-id="4d7ef-130">150</span></span>| <span data-ttu-id="4d7ef-131">USD</span><span class="sxs-lookup"><span data-stu-id="4d7ef-131">USD</span></span>|


<span data-ttu-id="4d7ef-132">เมื่อคุณปิด **ชื่อมาตรฐาน** เป็นมิติการกำหนดราคา และกลไกจัดการการกำหนดราคาจะค้นหาราคา โดยจะใช้ค่า **หน่วยขององค์กร** จากบริบทการป้อนข้อมูลเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4d7ef-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="4d7ef-133">ถ้า **หน่วยองค์กร** ของบริบทการป้อนข้อมูลคือ "Contoso US" ผลลัพธ์จะไม่สามารถระบุได้เนื่องจากทั้งสองแถวจะตรงกัน</span><span class="sxs-lookup"><span data-stu-id="4d7ef-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="4d7ef-134">เพื่อหลีกเลี่ยงสถานการณ์นี้ เมื่อคุณสร้างเรกคอร์ด **ราคาตามบทบาท** ระบบจะตรวจสอบว่าการรวมกันของมิติไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="4d7ef-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="4d7ef-135">ถ้ามิติถูกปิดหลังจากเรกคอร์ด **ราคาตามบทบาท** ถูกสร้าง ข้อจำกัดนี้สามารถถูกละเมิดได้</span><span class="sxs-lookup"><span data-stu-id="4d7ef-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="4d7ef-136">ดังนั้น ก่อนที่คุณจะปิดมิติ คุณลบแถว **ราคาตามบทบาท** และ **ส่วนเพิ่มราคาของราคาตามบทบาท** ทั้งหมดที่มีค่ามิตินำเข้าข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4d7ef-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]