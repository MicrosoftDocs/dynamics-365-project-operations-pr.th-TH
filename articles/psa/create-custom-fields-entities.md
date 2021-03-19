---
title: การสร้างฟิลด์และเอนทิตีแบบกำหนดเอง
description: หัวข้อนี้อธิบายถึงวิธีการสร้างชุดตัวเลือกและเอนทิตีในโซลูชันของคุณในแพลตฟอร์ม Power Apps
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c58745a46e84a40b90fbb3cbf89b10e293588fc3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290561"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="c42be-103">การสร้างฟิลด์และเอนทิตีแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="c42be-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c42be-104">ทำตามขั้นตอนต่อไปนี้ทุกครั้งที่คุณต้องการสร้างชุดตัวเลือกหรือเอนทิตีแบบกำหนดบนแพลตฟอร์ม Power Apps</span><span class="sxs-lookup"><span data-stu-id="c42be-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="c42be-105">ขั้นตอนในหัวข้อนี้ควรจะทำให้เสร็จโดยใช้ส่วนติดต่อเว็บของ Project Service Automation (PSA)</span><span class="sxs-lookup"><span data-stu-id="c42be-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c42be-106">เราขอแนะนำให้คุณทำการเปลี่ยนแปลงมิติการกำหนดราคาแบบกำหนดเองทั้งหมดในโซลูชันแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="c42be-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="c42be-107">หลักปฏิบัติที่สำคัญที่สุดนี้ให้ความยืดหยุ่นสำหรับการปรับปรุง หรือลบการเปลี่ยนแปลงตามความจำเป็นในอนาคต จะช่วยให้มีการใช้นำงานของคุณกลับมาใช้อีกครััง และทำให้การส่งการเปลี่ยนแปลงเหล่านี้ไปยังอินสแตนซ์อื่นเป็นไปได้ง่ายกว่าเดิม</span><span class="sxs-lookup"><span data-stu-id="c42be-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="c42be-108">หลังจากที่คุณได้ทำการเปลี่ยนแปลงที่จำเป็นทั้งหมดแล้ว ส่งออกโซลูชันนี้เป็น **โซลูชันที่ถูกจัดการแล้ว** และนำเข้าไปยังอินสแตนซ์อื่น ๆ เพื่อนำการตั้งค่าการกำหนดราคาของคุณมาใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="c42be-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="c42be-109">สร้างฟิลด์ที่กำหนดเองและชุดตัวเลือกในโซลูชันมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="c42be-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="c42be-110">มิติการกำหนดราคาอาจเป็นชุดตัวเลือกหรือเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="c42be-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="c42be-111">ทั้งสองต้องถูกสร้างขึ้นในโซลูชันการกำหนดราคาของคุณ</span><span class="sxs-lookup"><span data-stu-id="c42be-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="c42be-112">ขั้นตอนในกระบวนงานนี้อธิบายวิธีการสร้างมิติตามเอนทิตีและมิติตามชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c42be-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="c42be-113">มิติตามเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="c42be-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="c42be-114">ใน PSA คลิก **การตั้งค่า** > **แนวทางแก้ไข** แล้วดับเบิลคลิก **มิติการกำหนดราคาของ \<your organization name>**</span><span class="sxs-lookup"><span data-stu-id="c42be-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="c42be-115">ใน Solution Explorer บนบานหน้าต่างการนำทางด้านซ้าย เลือก **เอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="c42be-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="c42be-116">คลิก **สร้าง** เพื่อสร้างเอนทิตีใหม่ที่เรียกว่า **ชื่อมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="c42be-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="c42be-117">ป้อนข้อมูลที่จำเป็นให้ครบ จากนั้นคลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c42be-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![คำนิยามเอนทิตีชื่อมาตรฐาน](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="c42be-119">มิติตามชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c42be-119">Option set-based dimensions</span></span> 
<span data-ttu-id="c42be-120">คุณสามารถสร้างสองมิติตามชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c42be-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="c42be-121">ใช้ **สถานที่ทำงานของทรัพยากร** เพื่อติดตามราคาของงานทำที่ **บ้าน** และการทำงาน **นอกสถานที่** และใช้ **ชั่วโมงการทำงานของทรัพยากร** กับมูลค่า **ในเวลา** และ **ล่วงเวลา** เพื่อนำมาคิดราคาเพิ่มเมื่องานสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="c42be-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="c42be-122">ใน PSA คลิก **การตั้งค่า** > **แนวทางแก้ไข** แล้วดับเบิลคลิก **มิติการกำหนดราคาของ \<your organization name>**</span><span class="sxs-lookup"><span data-stu-id="c42be-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c42be-123">ใน Solution Explorer บนบานหน้าต่างการนำทางด้านซ้าย เลือก **ชุดตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="c42be-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="c42be-124">คลิก **สร้าง** เพื่อสร้างชุดตัวเลือกใหม่ ป้อนข้อมูลที่จำเป็นให้ครบ และจากนั้นคลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c42be-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="c42be-125">มิติการกำหนดราคาตามชุดตัวเลือกที่เรียกว่า สถานที่ทำงานของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c42be-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="c42be-126">มิติการกำหนดราคาตามชุดตัวเลือกที่เรียกว่า ชั่วโมงทำงานของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c42be-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="c42be-127">สร้างข้อมูลสำหรับมิติตามเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="c42be-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="c42be-128">คุณสามารถสร้างข้อมูลสำหรับมิติตามเอนทิตี้ด้วยตนเอง หรือโดยใช้การนำเข้าหรือเรียกใช้บริการ Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="c42be-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="c42be-129">ใช้ขั้นตอนในกระบวนงานนี้สร้างสองชื่อมาตรฐาน ได้แก่ **วิศวกรระบบ** และ **วิศวกรระบบอาวุโส** จากมิติตามเอนทิตี **ชื่อมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="c42be-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="c42be-130">ถ้าข้อมูลที่คุณต้องการสร้างมีขนาดเล็ก ดังในตัวอย่างต่อไปนี้ คุณสามารถใช้ฟอร์มมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="c42be-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="c42be-131">ใน PSA คลิก **การค้นหาขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="c42be-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="c42be-132">เลือกเอนทิตี **ชื่อมาตรฐาน** จากนั้นคลิก **ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="c42be-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="c42be-133">แถวทั้งหมดในเอนทิตี **ชื่อมาตรฐาน** จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="c42be-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="c42be-134">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c42be-134">Click **New**.</span></span> <span data-ttu-id="c42be-135">ในฟิลด์ **ชื่อ** ให้ป้อน "Systems Engineer" แล้วคลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c42be-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="c42be-136">ปิดฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="c42be-136">Close the form.</span></span> 
4. <span data-ttu-id="c42be-137">ทำซ้ำขั้นตอนที่ 1-3 เพื่อสร้างชื่อมาตรฐานอื่นสำหรับ "Senior Systems Engineer"</span><span class="sxs-lookup"><span data-stu-id="c42be-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="c42be-138">ข้อมูลตัวอย่างสำหรับเอนทิตีชื่อมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="c42be-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]