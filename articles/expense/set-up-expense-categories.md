---
title: ตั้งค่าประเภทค่าใช้จ่าย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีตั้งค่าประเภทค่าใช้จ่ายและประเภทที่ใช้ร่วมกันสำหรับรายงานค่าใช้จ่าย
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1589cf82626e744d35f31fef8e8437a5ad71360d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276146"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="649bc-103">ตั้งค่าประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="649bc-103">Set up expense categories</span></span>

<span data-ttu-id="649bc-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="649bc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="649bc-105">เมื่อพนักงานสร้างรายงานค่าใช้จ่าย ค่าใช้จ่ายแต่ละรายการที่พวกเขาบันทึกจะต้องเชื่อมโยงกับประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="649bc-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="649bc-106">ประเภทค่าใช้จ่ายมาจากประเภทที่ใช้ร่วมกัน ซึ่งสามารถใช้ร่วมกันระหว่างนิติบุคคลในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="649bc-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="649bc-107">ขึ้นอยู่กับว่าองค์กรของคุณกำหนดไว้อย่างไร ประเภทค่าใช้จ่ายเหล่านี้ยังสามารถใช้ร่วมกันในพื้นที่อื่นๆ ด้วย</span><span class="sxs-lookup"><span data-stu-id="649bc-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="649bc-108">ตามข้อกำหนดขององค์กรของคุณและคำแนะนำจากทีมการนำไปใช้งาน คุณต้องกำหนดว่าประเภทที่ใช้ในการจัดการค่าใช้จ่ายจะใช้เฉพาะในการจัดการค่าใช้จ่ายหรือควรใช้ร่วมกันในด้านอื่นๆ ด้วย</span><span class="sxs-lookup"><span data-stu-id="649bc-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="649bc-109">ประเภทเหล่านี้สามารถใช้ร่วมกันระหว่างการจัดการและการบัญชีโครงการ และการจัดการค่าใช้จ่าย หรือระหว่างการจัดการและการบัญชีโครงการและการผลิต</span><span class="sxs-lookup"><span data-stu-id="649bc-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="649bc-110">อย่างไรก็ตาม ไม่สามารถใช้ร่วมกันระหว่างการจัดการค่าใช้จ่ายและการผลิตได้</span><span class="sxs-lookup"><span data-stu-id="649bc-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="649bc-111">ก่อนที่คุณจะเริ่มกระบวนการตั้งค่า คุณต้องตัดสินใจต่อไปนี้สำหรับค่าใช้จ่ายแต่ละประเภท:</span><span class="sxs-lookup"><span data-stu-id="649bc-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="649bc-112">ประเภทค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="649bc-112">What is the expense category?</span></span> <span data-ttu-id="649bc-113">ตัวอย่างได้แก่ ประเภทสำหรับเที่ยวบิน โรงแรม หรือระยะไมล์</span><span class="sxs-lookup"><span data-stu-id="649bc-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="649bc-114">ประเภทค่าใช้จ่ายสามารถใช้ในการจัดการและการบัญชีโครงการได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="649bc-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="649bc-115">หากสามารถใช้ได้ คุณต้องตัดสินใจเกี่ยวกับเรื่องต่อไปนี้ด้วย</span><span class="sxs-lookup"><span data-stu-id="649bc-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="649bc-116">บัญชีต้นทุนใดที่จะใช้สำหรับค่าใช้จ่ายต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="649bc-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="649bc-117">ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="649bc-117">Cost</span></span>
        - <span data-ttu-id="649bc-118">การจัดสรรเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="649bc-118">Payroll allocation</span></span>
        - <span data-ttu-id="649bc-119">WIP-มูลค่าต้นทุน</span><span class="sxs-lookup"><span data-stu-id="649bc-119">WIP-cost value</span></span>
        - <span data-ttu-id="649bc-120">ต้นทุน-สินค้า</span><span class="sxs-lookup"><span data-stu-id="649bc-120">Cost-item</span></span>
        - <span data-ttu-id="649bc-121">WIP-มูลค่าต้นทุน-สินค้า</span><span class="sxs-lookup"><span data-stu-id="649bc-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="649bc-122">ขาดทุนสะสม</span><span class="sxs-lookup"><span data-stu-id="649bc-122">Accrued loss</span></span>
        - <span data-ttu-id="649bc-123">WIP-ขาดทุนสะสม</span><span class="sxs-lookup"><span data-stu-id="649bc-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="649bc-124">บัญชีรายได้ใดที่จะใช้สำหรับแหล่งรายได้ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="649bc-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="649bc-125">รายได้ที่ออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="649bc-125">Invoiced revenue</span></span>
        - <span data-ttu-id="649bc-126">มูลค่าการขายของรายได้ค้างรับ</span><span class="sxs-lookup"><span data-stu-id="649bc-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="649bc-127">WIP-มูลค่าการขาย</span><span class="sxs-lookup"><span data-stu-id="649bc-127">WIP-sales value</span></span>
        - <span data-ttu-id="649bc-128">รายได้ค้างรับ-การผลิต</span><span class="sxs-lookup"><span data-stu-id="649bc-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="649bc-129">WIP-การผลิต</span><span class="sxs-lookup"><span data-stu-id="649bc-129">WIP-production</span></span>
        - <span data-ttu-id="649bc-130">รายได้ค้างรับ-กำไร</span><span class="sxs-lookup"><span data-stu-id="649bc-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="649bc-131">WIP-กำไร</span><span class="sxs-lookup"><span data-stu-id="649bc-131">WIP-profit</span></span>
        - <span data-ttu-id="649bc-132">รายได้ค้างรับ-การสมัครใช้งาน</span><span class="sxs-lookup"><span data-stu-id="649bc-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="649bc-133">WIP-การสมัครใช้งาน</span><span class="sxs-lookup"><span data-stu-id="649bc-133">WIP-subscription</span></span>

- <span data-ttu-id="649bc-134">ชนิดค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="649bc-134">What is the expense type?</span></span>
- <span data-ttu-id="649bc-135">วิธีการชำระเงินเริ่มต้นสำหรับประเภทค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="649bc-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="649bc-136">ค่าใช้จ่ายในประเภทค่าใช้จ่ายต้องแยกรายการหรือไม่</span><span class="sxs-lookup"><span data-stu-id="649bc-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="649bc-137">บัญชีเริ่มต้นหลักสำหรับประเภทค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="649bc-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="649bc-138">กลุ่มภาษีขายสินค้าเริ่มต้นสำหรับประเภทค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="649bc-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="649bc-139">สามารถใช้วิธีการชำระเงินเพิ่มเติมสำหรับประเภทค่าใช้จ่ายได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="649bc-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="649bc-140">ถ้าเป็นเช่นนั้น คืออะไรบ้าง</span><span class="sxs-lookup"><span data-stu-id="649bc-140">If so, what are they?</span></span>
- <span data-ttu-id="649bc-141">มีประเภทย่อยในประเภทค่าใช้จ่ายนี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="649bc-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="649bc-142">หากมีประเภทย่อย คุณต้องตัดสินใจเกี่ยวกับเรื่องต่อไปนี้ด้วย</span><span class="sxs-lookup"><span data-stu-id="649bc-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="649bc-143">ประเภทย่อยใดๆ ไม่รวมอยู่ในการขอคืนภาษีหรือไม่</span><span class="sxs-lookup"><span data-stu-id="649bc-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="649bc-144">กลุ่มภาษีขายสินค้าของประเภทย่อยคืออะไร</span><span class="sxs-lookup"><span data-stu-id="649bc-144">What is the item sales tax group of the subcategories?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]