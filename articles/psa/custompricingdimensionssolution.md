---
title: สร้างโซลูชันแบบกำหนดเองสำหรับมิติการกำหนดราคา
description: หัวข้อนี้อธิบายวิธีสร้างโซลูชันแบบกำหนดเองเมื่อสร้างมิติการกำหนดราคาที่กำหนดเอง
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
ms.openlocfilehash: 1d8117d6f6bcedc97264401fc941470f34efb1ae
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285011"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="d0ae7-103">สร้างโซลูชันแบบกำหนดเองสำหรับมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="d0ae7-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="d0ae7-104">การเปลี่ยนแปลงมิติการกำหนดราคาที่กำหนดเองทั้งหมดควรอยู่ในโซลูชันที่แยกกัน</span><span class="sxs-lookup"><span data-stu-id="d0ae7-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="d0ae7-105">หลักปฏิบัติที่สำคัญที่สุดนี้ให้ความยืดหยุ่นสำหรับการปรับปรุง หรือลบการเปลี่ยนแปลงตามความจำเป็นในอนาคต จะช่วยให้มีการใช้นำงานของคุณกลับมาใช้อีกครััง และทำให้การส่งการเปลี่ยนแปลงเหล่านี้ไปยังอินสแตนซ์อื่นเป็นไปได้ง่ายกว่าเดิม</span><span class="sxs-lookup"><span data-stu-id="d0ae7-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="d0ae7-106">หลังจากที่คุณทำการเปลี่ยนแปลงที่จำเป็นทั้งหมดแล้ว ส่งออกโซลูชันนี้เป็น **โซลูชันที่มีการจัดการ** และนำเข้าไปยังอินสแตนซ์อื่น ๆ เพื่อนำการตั้งค่าการกำหนดราคาของคุณมาใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="d0ae7-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="d0ae7-107">เลือก **การตั้งค่า** > **โซลูชัน** แล้วเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="d0ae7-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="d0ae7-108">ตั้งชื่อโซลูชันเป็น **มิติการกำหนดราคาของ \<your organization name>** ให้ป้อนข้อมูลจำเป็นที่เหลือ แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d0ae7-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![การสร้างโซลูชันแบบกำหนดเองสำหรับมิติการกำหนดราคา](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="d0ae7-110">เพิ่มเอนทิตีที่จำเป็นทั้งหมด และส่วนประกอบที่เกี่ยวข้องกับโซลูชันมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="d0ae7-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="d0ae7-111">คุณจะต้องเพิ่มเอนทิตี Project Service ต่อไปนี้ลงในโซลูชันการกำหนดราคาของคุณ</span><span class="sxs-lookup"><span data-stu-id="d0ae7-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="d0ae7-112">ทำตามขั้นตอนในกระบวนงานนี้เพื่อทำการเปลี่ยนแปลงแบบแผนที่สำคัญบางอย่างในโซลูชันการกำหนดราคา เพื่อให้เอนทิตีตระหนักถึงมิติการกำหนดราคาใหม่</span><span class="sxs-lookup"><span data-stu-id="d0ae7-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="d0ae7-113">เลือก **การตั้งค่า** > **โซลูชัน** แล้วดับเบิลคลิก **มิติการกำหนดราคาของ \<your organization name>**</span><span class="sxs-lookup"><span data-stu-id="d0ae7-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="d0ae7-114">ใน Solution Explorer บนบานหน้าต่างการนำทางด้านซ้าย เลือก **เพิ่มสิ่งที่มีอยู่** > **เอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="d0ae7-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="d0ae7-115">ในกล่องโต้ตอบ **ส่วนประกอบโซลูชัน** เลือกเอนทิตีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d0ae7-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="d0ae7-116">เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="d0ae7-116">Actual</span></span>
- <span data-ttu-id="d0ae7-117">ทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="d0ae7-117">Bookable Resource</span></span>
- <span data-ttu-id="d0ae7-118">บรรทัดการประมาณการ</span><span class="sxs-lookup"><span data-stu-id="d0ae7-118">Estimate Line</span></span>
- <span data-ttu-id="d0ae7-119">งานโครงการ</span><span class="sxs-lookup"><span data-stu-id="d0ae7-119">Project Task</span></span>
- <span data-ttu-id="d0ae7-120">รายละเอียดรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="d0ae7-120">Invoice Line Detail</span></span>
- <span data-ttu-id="d0ae7-121">รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="d0ae7-121">Journal Line</span></span>
- <span data-ttu-id="d0ae7-122">รายการรายละเอียดการให้บริการตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="d0ae7-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="d0ae7-123">สมาชิกของทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="d0ae7-123">Project Team Member</span></span>
- <span data-ttu-id="d0ae7-124">รายละเอียดรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="d0ae7-124">Quote Line Detail</span></span>
- <span data-ttu-id="d0ae7-125">ส่วนเพิ่มราคาของราคาตามบทบาท</span><span class="sxs-lookup"><span data-stu-id="d0ae7-125">Role Price Markup</span></span>
- <span data-ttu-id="d0ae7-126">ราคาตามบทบาท</span><span class="sxs-lookup"><span data-stu-id="d0ae7-126">Role Price</span></span> 
- <span data-ttu-id="d0ae7-127">รายการเวลา</span><span class="sxs-lookup"><span data-stu-id="d0ae7-127">Time Entry</span></span> 

> ![เพิ่มเอนทิตีที่มีอยู่ไปยังโซลูชันมิติการกำหนดราคา](media/Existing-entities-to-PD-solution.png)

> ![เลือกส่วนประกอบของโซลูชัน](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="d0ae7-130">ตรวจสอบให้แน่ใจว่าได้รวมฟอร์มและมุมมองทั้งหมดสำหรับแต่ละเอนทิตีที่ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="d0ae7-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="d0ae7-131">เมื่อถูกพร้อมท์ให้รวมเอนทิตีที่ไม่เป็นอิสระใด ๆ เข้ากับเอนทิตีที่เลือกไว้ เลือก **ไม่**</span><span class="sxs-lookup"><span data-stu-id="d0ae7-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![ไม่รวมถึงส่วนประกอบที่เกี่ยวข้องทั้งหมด](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]