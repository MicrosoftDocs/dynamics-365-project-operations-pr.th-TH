---
title: สร้างฟิลด์และเอนทิตีแบบกำหนดเองเป็นมิติการกำหนดราคา
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีสร้างชุดตัวเลือกหรือเอนทิตีแบบกำหนดเอง
author: rumant
manager: AnnBe
ms.date: 11/18/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275651"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="fb634-103">สร้างฟิลด์และเอนทิตีแบบกำหนดเองเป็นมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="fb634-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="fb634-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="fb634-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fb634-105">ทำตามขั้นตอนต่อไปนี้เมื่อคุณต้องการสร้างชุดตัวเลือกหรือเอนทิตีแบบกำหนดสำหรับใช้เป็นมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="fb634-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="fb634-106">สำหรับข้อมูลเพิ่มเติม ให้ดู [ภาพรวมของมิติการกำหนดราคา](pricing-dimensions-overview.md)</span><span class="sxs-lookup"><span data-stu-id="fb634-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="fb634-107">เราขอแนะนำให้คุณทำการเปลี่ยนแปลงมิติการกำหนดราคาแบบกำหนดเองทั้งหมดในโซลูชันแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="fb634-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="fb634-108">แนวทางปฏิบัติที่ดีที่สุดที่สำคัญนี้ให้ความยืดหยุ่นในอนาคตเพื่ออัปเดตหรือลบการเปลี่ยนแปลงตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="fb634-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="fb634-109">นอกจากนี้ยังช่วยในการนำงานของคุณกลับมาใช้ใหม่และทำให้ง่ายต่อการพอร์ตการเปลี่ยนแปลงเหล่านี้ไปยังอินสแตนซ์อื่น หลังจากที่คุณทำการเปลี่ยนแปลงที่จำเป็นทั้งหมดแล้ว ให้ส่งออกโซลูชันนี้เป็น **โซลูชันที่มีการจัดการ** และนำเข้าในอินสแตนซ์อื่นๆ เพื่อใช้การตั้งค่าการกำหนดราคาของคุณซ้ำ</span><span class="sxs-lookup"><span data-stu-id="fb634-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="fb634-110">สร้างฟิลด์ที่กำหนดเองและชุดตัวเลือกในโซลูชันมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="fb634-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="fb634-111">มิติการกำหนดราคาอาจเป็นชุดตัวเลือกหรือเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="fb634-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="fb634-112">ทั้งสองต้องถูกสร้างขึ้นในโซลูชันการกำหนดราคาของคุณ</span><span class="sxs-lookup"><span data-stu-id="fb634-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="fb634-113">ขั้นตอนในกระบวนงานนี้อธิบายวิธีการสร้างมิติตามเอนทิตีและมิติตามชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="fb634-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="fb634-114">มิติตามเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="fb634-114">Entity-based dimensions</span></span>
<span data-ttu-id="fb634-115">ในการสร้างมิติตามเอนทิตี ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="fb634-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="fb634-116">ไปที่ **การตั้งค่า** > **โซลูชัน** แล้วดับเบิลคลิก **มิติการกำหนดราคาของ \<your organization name>**</span><span class="sxs-lookup"><span data-stu-id="fb634-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="fb634-117">ใน Solution Explorer ในบานหน้าต่างการนำทางด้านซ้าย เลือก **เอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="fb634-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="fb634-118">เลือก **สร้าง** เพื่อสร้างเอนทิตีใหม่ที่เรียกว่า **ชื่อมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="fb634-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="fb634-119">ป้อนข้อมูลที่จำเป็นให้ครบ จากนั้นเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fb634-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![คำนิยามเอนทิตีชื่อมาตรฐาน](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="fb634-121">มิติตามชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="fb634-121">Option set-based dimensions</span></span> 
<span data-ttu-id="fb634-122">คุณสามารถสร้างสองมิติตามชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="fb634-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="fb634-123">ใช้ **สถานที่ทำงานของทรัพยากร** เพื่อติดตามราคาของสถานที่ทำงานของ **หน้าแรก** และงาน **นอกสถานที่**</span><span class="sxs-lookup"><span data-stu-id="fb634-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="fb634-124">ใช้ **ชั่วโมงการทำงานของทรัพยากร** ด้วยค่า **ปกติ** และ **ล่วงเวลา** เพื่อใช้มาร์กอัปเมื่องานเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fb634-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="fb634-125">กราฟิกต่อไปนี้ให้มุมมองของ มิติของ **สถานที่ทำงานของทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="fb634-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![มิติการกำหนดราคาตามชุดตัวเลือกที่เรียกว่า สถานที่ทำงานของทรัพยากร](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="fb634-127">กราฟิกต่อไปนี้ให้มุมมองของมิติของ **ชั่วโมงการทำงานของทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="fb634-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![มิติการกำหนดราคาตามชุดตัวเลือกที่เรียกว่า ชั่วโมงทำงานของทรัพยากร](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="fb634-129">ไปที่ **การตั้งค่า** > **โซลูชัน** และดับเบิลคลิก **มิติการกำหนดราคาของ \<your organization name>**</span><span class="sxs-lookup"><span data-stu-id="fb634-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="fb634-130">ใน Solution Explorer ในบานหน้าต่างการนำทางด้านซ้าย เลือก **ชุดตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="fb634-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="fb634-131">เลือก **สร้าง** เพื่อสร้างชุดตัวเลือกใหม่ ป้อนข้อมูลที่จำเป็นให้ครบ และจากนั้นเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fb634-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="fb634-132">สร้างข้อมูลสำหรับมิติตามเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="fb634-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="fb634-133">คุณสามารถสร้างข้อมูลสำหรับมิติตามเอนทิตี้ด้วยตนเอง หรือโดยใช้การนำเข้าหรือเรียกใช้บริการ Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="fb634-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="fb634-134">ใช้ขั้นตอนในกระบวนงานนี้สร้างสองชื่อมาตรฐาน ได้แก่ **วิศวกรระบบ** และ **วิศวกรระบบอาวุโส** จากมิติตามเอนทิตี **ชื่อมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="fb634-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="fb634-135">ถ้าข้อมูลที่คุณต้องการสร้างมีขนาดเล็ก ดังในตัวอย่างต่อไปนี้ คุณสามารถใช้ฟอร์มมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="fb634-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="fb634-136">เลือก **การค้นหาขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="fb634-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="fb634-137">เลือกเอนทิตี **ชื่อมาตรฐาน** จากนั้นเลือก **ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="fb634-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="fb634-138">แถวทั้งหมดในเอนทิตี **ชื่อมาตรฐาน** จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="fb634-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="fb634-139">เลือก **ใหม่** จากนั้นในฟิลด์ **ชื่อ** ให้ป้อน "วิศวกรระบบ" แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fb634-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="fb634-140">ปิดเพจ</span><span class="sxs-lookup"><span data-stu-id="fb634-140">Close the page.</span></span> 
5. <span data-ttu-id="fb634-141">ทำซ้ำขั้นตอนที่ 1-3 เพื่อสร้างชื่อมาตรฐานอื่นสำหรับ "Senior Systems Engineer"</span><span class="sxs-lookup"><span data-stu-id="fb634-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![ข้อมูลตัวอย่างสำหรับเอนทิตีชื่อมาตรฐาน](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]