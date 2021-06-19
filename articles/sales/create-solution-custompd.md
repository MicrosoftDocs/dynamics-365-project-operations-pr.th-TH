---
title: สร้างโซลูชันสำหรับมิติการกำหนดราคาที่กำหนดเอง
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการสร้างโซลูชันสำหรับมิติการกำหนดราคาแบบกำหนดเอง
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010359"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="d124b-103">สร้างโซลูชันสำหรับมิติการกำหนดราคาที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="d124b-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="d124b-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="d124b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="d124b-105">การเปลี่ยนแปลงมิติการกำหนดราคาที่กำหนดเองทั้งหมดควรอยู่ในโซลูชันที่แยกกัน</span><span class="sxs-lookup"><span data-stu-id="d124b-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="d124b-106">หลักปฏิบัติที่สำคัญที่สุดนี้ให้ความยืดหยุ่นสำหรับการปรับปรุง หรือลบการเปลี่ยนแปลงตามความจำเป็น ช่วยให้มีการใช้นำงานของคุณกลับมาใช้อีกครััง และทำให้การส่งการเปลี่ยนแปลงไปยังอินสแตนซ์อื่นเป็นไปได้ง่ายกว่าเดิม</span><span class="sxs-lookup"><span data-stu-id="d124b-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="d124b-107">หลังจากที่คุณได้ทำการเปลี่ยนแปลงที่จำเป็นแล้ว ส่งออกโซลูชันนี้เป็นโซลูชัน **ที่ถูกจัดการแล้ว** และจากนั้นนำเข้าไปยังอินสแตนซ์อื่น ๆ เพื่อนำมาใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="d124b-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="d124b-108">สร้างโซลูชันสำหรับมิติการกำหนดราคาที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="d124b-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="d124b-109">เลือก **การตั้งค่า** > **โซลูชัน** แล้วเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="d124b-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="d124b-110">ตั้งชื่อโซลูชัน *มิติการกำหนดราคา <your organization name>*</span><span class="sxs-lookup"><span data-stu-id="d124b-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="d124b-111">ป้อนข้อมูลที่จำเป็นให้ครบ จากนั้นเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d124b-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![การสร้างโซลูชันสำหรับมิติการกำหนดราคาที่กำหนดเอง](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="d124b-113">เพิ่มเอนทิตีที่จำเป็นทั้งหมด และส่วนประกอบที่เกี่ยวข้องกับโซลูชันมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="d124b-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="d124b-114">เพิ่มเอนทิตี Project Service ต่อไปนี้ในโซลูชันการกำหนดราคาของคุณเพื่อทำการเปลี่ยนแปลง Schema ที่สำคัญในโซลูชันการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="d124b-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="d124b-115">หลังจากที่คุณทำตามขั้นตอนนี้เรียบร้อยแล้ว เอนทิตีจะรับรู้มิติการกำหนดราคาใหม่</span><span class="sxs-lookup"><span data-stu-id="d124b-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="d124b-116">เลือก **การตั้งค่า** > **โซลูชัน** จากนั้นคลิกสองครั้งที่ **<*ชื่อองค์กรของคุณ*> มิติการกำหนดราคา**</span><span class="sxs-lookup"><span data-stu-id="d124b-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="d124b-117">ใน Solution Explorer บนบานหน้าต่างการนำทางด้านซ้าย เลือก **เพิ่มสิ่งที่มีอยู่** > **เอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="d124b-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="d124b-118">ในกล่องโต้ตอบ **ส่วนประกอบโซลูชัน** เลือกเอนทิตีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d124b-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="d124b-119">**เกิดขึ้นจริง**</span><span class="sxs-lookup"><span data-stu-id="d124b-119">**Actual**</span></span>
   - <span data-ttu-id="d124b-120">**ทรัพยากรที่สามารถจองได้**</span><span class="sxs-lookup"><span data-stu-id="d124b-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="d124b-121">**บรรทัดการประมาณการ**</span><span class="sxs-lookup"><span data-stu-id="d124b-121">**Estimate Line**</span></span>
   - <span data-ttu-id="d124b-122">**งานโครงการ**</span><span class="sxs-lookup"><span data-stu-id="d124b-122">**Project Task**</span></span>
   - <span data-ttu-id="d124b-123">**รายละเอียดรายการใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="d124b-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="d124b-124">**รายการสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="d124b-124">**Journal Line**</span></span>
   - <span data-ttu-id="d124b-125">**รายการรายละเอียดการให้บริการตามสัญญาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="d124b-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="d124b-126">**สมาชิกของทีมโครงการ**</span><span class="sxs-lookup"><span data-stu-id="d124b-126">**Project Team Member**</span></span>
   - <span data-ttu-id="d124b-127">**รายละเอียดรายการใบเสนอราคา**</span><span class="sxs-lookup"><span data-stu-id="d124b-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="d124b-128">**ส่วนเพิ่มราคาของราคาตามบทบาท**</span><span class="sxs-lookup"><span data-stu-id="d124b-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="d124b-129">**ราคาตามบทบาท**</span><span class="sxs-lookup"><span data-stu-id="d124b-129">**Role Price**</span></span>
   - <span data-ttu-id="d124b-130">**รายการเวลา**</span><span class="sxs-lookup"><span data-stu-id="d124b-130">**Time Entry**</span></span>
 
   ![เพิ่มโซลูชันมิติการกำหนดราคาแบบกำหนดเองของเอนทิตีที่มีอยู่](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="d124b-132">สำหรับแต่ละเอนทิตี ตรวจสอบส่วนประกอบที่เพิ่มและรายการสุดท้ายของสินทรัพย์เอนทิตีสำหรับแต่ละเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="d124b-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="d124b-133">รวมฟอร์มและมุมมองทั้งหมดสำหรับแต่ละเอนทิตีที่ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="d124b-133">Include all forms and views for each of the selected entities.</span></span>

  ![เพิ่มเอนทิตี](./media/solution-component-selection.png)


5.  <span data-ttu-id="d124b-135">เมื่อได้รับแจ้งให้รวมเอนทิตีที่เกี่ยวข้องสำหรับเอนทิตีที่เลือก ให้เลือก **ไม่ ไม่รวมส่วนประกอบที่ต้องใช้**</span><span class="sxs-lookup"><span data-stu-id="d124b-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![รวมถึงเอนทิตีที่ขึ้นต่อกัน](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]