---
title: ปิดมิติการกำหนดราคา
description: หัวข้อนี้แสดงวิธีการตั้งค่ามิติการกำหนดราคาในโซลูชัน Project Service
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da8615fa147838d9088c639039d5a2534e662e82
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014319"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="59134-103">ปิดมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="59134-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="59134-104">คุณอาจต้องตรวจสอบและอัปเดกลยุทธ์การกำหนดราคาของคุณทุกสองสามปี</span><span class="sxs-lookup"><span data-stu-id="59134-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="59134-105">การอัปเดตใดๆที่คุณทำอาจต้องการให้คุณปิดมิติการกำหนดราคาที่มีอยู่และสร้างรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="59134-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="59134-106">ตัวอย่างเช่น คุณอาจจะมีการกำหนดราคาก่อนหน้านี้โดย **บทบาท** แต่ตอนนี้คุณได้ตัดสินใจที่จะให้ราคาตาม **ประสบการณ์การทำงาน**</span><span class="sxs-lookup"><span data-stu-id="59134-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="59134-107">การทำเช่นนี้อาจทำให้คุณจำเป็นต้องปิด **บทบาท** เป็นมิติการกำหนดราคาและสร้าง **ประสบการณ์การทำงาน** เป็นมิติการกำหนดราคาใหม่</span><span class="sxs-lookup"><span data-stu-id="59134-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="59134-108">การปิดมิติการกำหนดราคา โดยไม่คำนึงถึงว่าจะเป็นแบบสำเร็จรูปหรือกำหนดเอง สามารถทำได้โดยการตั้งค่าที่ฟิลด์ **สามารถใช้งานได้กับต้นทุน** และ **สามารถใช้งานได้กับการขาย** ของมิติการกำหนดราคาเป็น **ไม่ใช่**</span><span class="sxs-lookup"><span data-stu-id="59134-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="59134-109">อย่างไรก็ตาม เมื่อคุณทำเช่นนี้ คุณอาจได้รับข้อความข้อผิดพลาดต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="59134-109">However, when you do this, you might receive the following error message.</span></span>

![ข้อผิดพลาดของกระบวนการทางธุรกิจมีแนวโน้มเมื่อปิดมิติการกำหนดราคา](media/Business-Process-Error.png)


<span data-ttu-id="59134-111">ข้อความข้อผิดพลาดนี้บ่งชี้ว่ามีเรกคอร์ดราคาที่ตั้งค่าไว้ก่อนหน้านี้สำหรับมิติที่ถูกปิด</span><span class="sxs-lookup"><span data-stu-id="59134-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="59134-112">เรกคอร์ด **ราคาตามบทบาท** และ **ส่วนเพิ่มราคาของราคาตามบทบาท** ทั้งหมดที่อ้างอิงถึงมิติต้องถูกลบก่อนที่การบังคับใช้ของมิติสามารถตั้งค่าเป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="59134-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="59134-113">กฎนี้ใช้ได้กับทั้งมิติการกำหนดราคาแบบสำเร็จรูปและมิติการกำหนดราคาที่กำหนดเองที่คุณอาจสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="59134-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="59134-114">เหตุผลสำหรับการตรวจสอบความถูกต้องนี้เป็นเพราะ Project Service มีข้อจำกัดที่แต่ละเรกคอร์ด **ราคาตามบทบาท** ต้องมีการรวมกันของมิติที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="59134-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="59134-115">ตัวอย่างเช่น ในรายการราคาที่เรียกว่า **อัตราต้นทุน US 2018** คุณมีแถว **ราคาตามบทบาท** ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="59134-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="59134-116">ชื่อมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="59134-116">Standard Title</span></span>         | <span data-ttu-id="59134-117">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="59134-117">Org Unit</span></span>    |<span data-ttu-id="59134-118">หน่วย</span><span class="sxs-lookup"><span data-stu-id="59134-118">Unit</span></span>   |<span data-ttu-id="59134-119">ราคา</span><span class="sxs-lookup"><span data-stu-id="59134-119">Price</span></span>  |<span data-ttu-id="59134-120">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="59134-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="59134-121">วิศวกรระบบ</span><span class="sxs-lookup"><span data-stu-id="59134-121">Systems Engineer</span></span>|<span data-ttu-id="59134-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="59134-122">Contoso US</span></span>|<span data-ttu-id="59134-123">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="59134-123">Hour</span></span>| <span data-ttu-id="59134-124">100</span><span class="sxs-lookup"><span data-stu-id="59134-124">100</span></span>|<span data-ttu-id="59134-125">USD</span><span class="sxs-lookup"><span data-stu-id="59134-125">USD</span></span>|
| <span data-ttu-id="59134-126">วิศวกรระบบรุ่นพี่</span><span class="sxs-lookup"><span data-stu-id="59134-126">Senior Systems Engineer</span></span>|<span data-ttu-id="59134-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="59134-127">Contoso US</span></span>|<span data-ttu-id="59134-128">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="59134-128">Hour</span></span>| <span data-ttu-id="59134-129">150</span><span class="sxs-lookup"><span data-stu-id="59134-129">150</span></span>| <span data-ttu-id="59134-130">USD</span><span class="sxs-lookup"><span data-stu-id="59134-130">USD</span></span>|


<span data-ttu-id="59134-131">เมื่อคุณปิด **ชื่อมาตรฐาน** เป็นมิติการกำหนดราคา และกลไกจัดการการกำหนดราคา Project Service ค้นหาราคา จะใช้ค่า **หน่วยขององค์กร** จากบริบทการป้อนข้อมูลเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="59134-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="59134-132">ถ้า **หน่วยองค์กร** ของบริบทการป้อนข้อมูลคือ "Contoso US" ผลลัพธ์จะไม่สามารถระบุได้เนื่องจากทั้งสองแถวจะตรงกัน</span><span class="sxs-lookup"><span data-stu-id="59134-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="59134-133">เพื่อหลีกเลี่ยงสถานการณ์นี้ เมื่อคุณสร้างเรกคอร์ด **ราคาตามบทบาท** Project Service จะตรวจสอบว่าการรวมกันของมิติไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="59134-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="59134-134">ถ้ามิติถูกปิดหลังจากเรกคอร์ด **ราคาตามบทบาท** ถูกสร้าง ข้อจำกัดนี้สามารถถูกละเมิดได้</span><span class="sxs-lookup"><span data-stu-id="59134-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="59134-135">ดังนั้น ก่อนที่คุณจะปิดมิติ คุณลบแถว **ราคาตามบทบาท** และ **ส่วนเพิ่มราคาของราคาตามบทบาท** ทั้งหมดที่มีค่ามิตินำเข้าข้อมูล</span><span class="sxs-lookup"><span data-stu-id="59134-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]