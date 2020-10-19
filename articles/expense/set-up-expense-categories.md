---
title: ตั้งค่าประเภทค่าใช้จ่าย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีตั้งค่าประเภทค่าใช้จ่ายและประเภทที่ใช้ร่วมกันสำหรับรายงานค่าใช้จ่าย
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896709"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="65132-103">ตั้งค่าประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="65132-103">Set up expense categories</span></span>

<span data-ttu-id="65132-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="65132-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="65132-105">เมื่อพนักงานสร้างรายงานค่าใช้จ่าย ค่าใช้จ่ายแต่ละรายการที่พวกเขาบันทึกจะต้องเชื่อมโยงกับประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="65132-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="65132-106">ประเภทค่าใช้จ่ายมาจากประเภทที่ใช้ร่วมกัน ซึ่งสามารถใช้ร่วมกันระหว่างนิติบุคคลในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="65132-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="65132-107">ขึ้นอยู่กับว่าองค์กรของคุณกำหนดไว้อย่างไร ประเภทค่าใช้จ่ายเหล่านี้ยังสามารถใช้ร่วมกันในพื้นที่อื่นๆ ด้วย</span><span class="sxs-lookup"><span data-stu-id="65132-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="65132-108">ตามข้อกำหนดขององค์กรของคุณและคำแนะนำจากทีมการนำไปใช้งาน คุณต้องกำหนดว่าประเภทที่ใช้ในการจัดการค่าใช้จ่ายจะใช้เฉพาะในการจัดการค่าใช้จ่ายหรือควรใช้ร่วมกันในด้านอื่นๆ ด้วย</span><span class="sxs-lookup"><span data-stu-id="65132-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="65132-109">ประเภทเหล่านี้สามารถใช้ร่วมกันระหว่างการจัดการและการบัญชีโครงการ และการจัดการค่าใช้จ่าย หรือระหว่างการจัดการและการบัญชีโครงการและการผลิต</span><span class="sxs-lookup"><span data-stu-id="65132-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="65132-110">อย่างไรก็ตาม ไม่สามารถใช้ร่วมกันระหว่างการจัดการค่าใช้จ่ายและการผลิตได้</span><span class="sxs-lookup"><span data-stu-id="65132-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="65132-111">ก่อนที่คุณจะเริ่มกระบวนการตั้งค่า คุณต้องตัดสินใจต่อไปนี้สำหรับค่าใช้จ่ายแต่ละประเภท:</span><span class="sxs-lookup"><span data-stu-id="65132-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="65132-112">ประเภทค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="65132-112">What is the expense category?</span></span> <span data-ttu-id="65132-113">ตัวอย่างได้แก่ ประเภทสำหรับเที่ยวบิน โรงแรม หรือระยะไมล์</span><span class="sxs-lookup"><span data-stu-id="65132-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="65132-114">ประเภทค่าใช้จ่ายสามารถใช้ในการจัดการและการบัญชีโครงการได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="65132-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="65132-115">หากสามารถใช้ได้ คุณต้องตัดสินใจเกี่ยวกับเรื่องต่อไปนี้ด้วย</span><span class="sxs-lookup"><span data-stu-id="65132-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="65132-116">บัญชีต้นทุนใดที่จะใช้สำหรับค่าใช้จ่ายต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="65132-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="65132-117">ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="65132-117">Cost</span></span>
        - <span data-ttu-id="65132-118">การจัดสรรเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="65132-118">Payroll allocation</span></span>
        - <span data-ttu-id="65132-119">WIP-มูลค่าต้นทุน</span><span class="sxs-lookup"><span data-stu-id="65132-119">WIP-cost value</span></span>
        - <span data-ttu-id="65132-120">ต้นทุน-สินค้า</span><span class="sxs-lookup"><span data-stu-id="65132-120">Cost-item</span></span>
        - <span data-ttu-id="65132-121">WIP-มูลค่าต้นทุน-สินค้า</span><span class="sxs-lookup"><span data-stu-id="65132-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="65132-122">ขาดทุนสะสม</span><span class="sxs-lookup"><span data-stu-id="65132-122">Accrued loss</span></span>
        - <span data-ttu-id="65132-123">WIP-ขาดทุนสะสม</span><span class="sxs-lookup"><span data-stu-id="65132-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="65132-124">บัญชีรายได้ใดที่จะใช้สำหรับแหล่งรายได้ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="65132-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="65132-125">รายได้ที่ออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="65132-125">Invoiced revenue</span></span>
        - <span data-ttu-id="65132-126">มูลค่าการขายของรายได้ค้างรับ</span><span class="sxs-lookup"><span data-stu-id="65132-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="65132-127">WIP-มูลค่าการขาย</span><span class="sxs-lookup"><span data-stu-id="65132-127">WIP-sales value</span></span>
        - <span data-ttu-id="65132-128">รายได้ค้างรับ-การผลิต</span><span class="sxs-lookup"><span data-stu-id="65132-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="65132-129">WIP-การผลิต</span><span class="sxs-lookup"><span data-stu-id="65132-129">WIP-production</span></span>
        - <span data-ttu-id="65132-130">รายได้ค้างรับ-กำไร</span><span class="sxs-lookup"><span data-stu-id="65132-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="65132-131">WIP-กำไร</span><span class="sxs-lookup"><span data-stu-id="65132-131">WIP-profit</span></span>
        - <span data-ttu-id="65132-132">รายได้ค้างรับ-การสมัครใช้งาน</span><span class="sxs-lookup"><span data-stu-id="65132-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="65132-133">WIP-การสมัครใช้งาน</span><span class="sxs-lookup"><span data-stu-id="65132-133">WIP-subscription</span></span>

- <span data-ttu-id="65132-134">ชนิดค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="65132-134">What is the expense type?</span></span>
- <span data-ttu-id="65132-135">วิธีการชำระเงินเริ่มต้นสำหรับประเภทค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="65132-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="65132-136">ค่าใช้จ่ายในประเภทค่าใช้จ่ายต้องแยกรายการหรือไม่</span><span class="sxs-lookup"><span data-stu-id="65132-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="65132-137">บัญชีเริ่มต้นหลักสำหรับประเภทค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="65132-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="65132-138">กลุ่มภาษีขายสินค้าเริ่มต้นสำหรับประเภทค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="65132-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="65132-139">สามารถใช้วิธีการชำระเงินเพิ่มเติมสำหรับประเภทค่าใช้จ่ายได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="65132-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="65132-140">ถ้าเป็นเช่นนั้น คืออะไรบ้าง</span><span class="sxs-lookup"><span data-stu-id="65132-140">If so, what are they?</span></span>
- <span data-ttu-id="65132-141">มีประเภทย่อยในประเภทค่าใช้จ่ายนี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="65132-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="65132-142">หากมีประเภทย่อย คุณต้องตัดสินใจเกี่ยวกับเรื่องต่อไปนี้ด้วย</span><span class="sxs-lookup"><span data-stu-id="65132-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="65132-143">ประเภทย่อยใดๆ ไม่รวมอยู่ในการขอคืนภาษีหรือไม่</span><span class="sxs-lookup"><span data-stu-id="65132-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="65132-144">กลุ่มภาษีขายสินค้าของประเภทย่อยคืออะไร</span><span class="sxs-lookup"><span data-stu-id="65132-144">What is the item sales tax group of the subcategories?</span></span>
