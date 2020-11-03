---
title: กำหนดค่าการจัดการค่าใช้จ่าย
description: บทความนี้อธิบายถึงข้อควรพิจารณาและการตัดสินใจที่คุณต้องทำในระหว่างกระบวนการวางแผนก่อนที่คุณจะกำหนดค่าการจัดการค่าใช้จ่ายใน Microsoft Dynamics 365 Finance
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2291515cc154fb5b34ca5802135791958bea1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086080"
---
# <a name="configure-expense-management"></a><span data-ttu-id="25487-103">กำหนดค่าการจัดการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="25487-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25487-104">หัวข้อนี้อธิบายถึงข้อควรพิจารณาและการตัดสินใจที่คุณต้องทำในระหว่างกระบวนการวางแผนก่อนที่คุณจะกำหนดค่าการจัดการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="25487-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="25487-105">ในการจัดการค่าใช้จ่าย คุณสามารถจัดเก็บข้อมูลเกี่ยวกับวิธีการชำระเงิน ใบเบิกค่าเดินทาง รายงานค่าใช้จ่าย นโยบาย และอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="25487-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="25487-106">เนื่องจากการตัดสินใจหลายอย่างที่คุณทำเมื่อคุณวางแผนการกำหนดค่าสำหรับการจัดการค่าใช้จ่ายนั้น ขึ้นอยู่กับลำดับชั้นและโครงสร้างทางการเงินขององค์กรของคุณ คุณจึงต้องอ้างถึงเอกสารการวางแผนสำหรับพื้นที่เหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="25487-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="25487-107">ค่าใช้จ่ายระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="25487-107">Intercompany expenses</span></span>

<span data-ttu-id="25487-108">เมื่อคุณเปิดใช้งานค่าใช้จ่ายระหว่างบริษัท คุณอนุญาตให้นิติบุคคลและพนักงานต้องเสียค่าใช้จ่ายในนามของนิติบุคคลอื่น และเรียกเก็บเงินจากนิติบุคคลของการจ้างงานภายในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="25487-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="25487-109">ตัวอย่างเช่น พนักงานในนิติบุคคล A ดำเนินโครงการสำหรับนิติบุคคล B และโครงการต้องเสียค่าใช้จ่ายที่เกี่ยวข้องกับการเดินทาง</span><span class="sxs-lookup"><span data-stu-id="25487-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="25487-110">หากเปิดใช้งานค่าใช้จ่ายระหว่างบริษัท พนักงานสามารถยื่นรายงานค่าใช้จ่ายที่จะโพสต์รายการค่าใช้จ่ายไปยังนิติบุคคล B จากนั้นค่าใช้จ่ายจะต้องจ่ายโดยนิติบุคคล A หากองค์กรของคุณไม่ได้มีหลายนิติบุคคล คุณไม่ต้องเปิดใช้งานค่าใช้จ่ายระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="25487-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="25487-111">**การตัดสินใจ:** คุณต้องการเปิดใช้งานค่าใช้จ่ายระหว่างบริษัทหรือไม่</span><span class="sxs-lookup"><span data-stu-id="25487-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="25487-112">การจัดการทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="25487-112">Financial management</span></span>

<span data-ttu-id="25487-113">การจัดการค่าใช้จ่ายถูกรวมเข้ากับการจัดการทางการเงินขององค์กรของคุณอย่างแน่นหนา</span><span class="sxs-lookup"><span data-stu-id="25487-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="25487-114">การกำหนดค่าจำนวนมากของคุณสำหรับการจัดการค่าใช้จ่ายจะขึ้นอยู่กับการตัดสินใจที่คุณได้ทำเกี่ยวกับการเงินขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="25487-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="25487-115">ส่วนต่อไปนี้อธิบายถึงพื้นที่ต่างๆ ที่ต้องมีการวางแผนและการตัดสินใจ โดยพิจารณาจากการตัดสินใจทางการเงินขององค์กรและคำแนะนำจากทีมผู้นำของคุณ</span><span class="sxs-lookup"><span data-stu-id="25487-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="25487-116">เบี้ยเลี้ยง</span><span class="sxs-lookup"><span data-stu-id="25487-116">Per diems</span></span>

<span data-ttu-id="25487-117">คุณต้องกำหนดค่าเบี้ยเลี้ยงต่อวันของพนักงานที่องค์กรของคุณจัดหาให้</span><span class="sxs-lookup"><span data-stu-id="25487-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="25487-118">เนื่องจากโดยทั่วไปแล้วค่าเบี้ยเลี้ยงต่อวันจะใช้เพื่อครอบคลุมค่าใช้จ่ายต่างๆ เช่น ค่าอาหาร ค่าที่พัก และค่าใช้จ่ายอื่น ๆ คุณสามารถสร้างกฎสำหรับค่าเบี้ยเลี้ยงต่อวันที่องค์กรของคุณเสนอได้</span><span class="sxs-lookup"><span data-stu-id="25487-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="25487-119">ค่าเบี้ยเลี้ยงต่อวันอาจขึ้นอยู่กับช่วงเวลาของปี สถานที่เดินทาง หรือทั้งสองอย่าง</span><span class="sxs-lookup"><span data-stu-id="25487-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="25487-120">เมื่อคุณกำหนดกฎค่าเบี้ยเลี้ยงต่อวัน คุณสามารถระบุว่าเปอร์เซ็นต์ของอัตราค่าเบี้ยเลี้ยงต่อวันจะถูกระงับหากผู้ปฏิบัติงานได้รับอาหารหรือบริการฟรี</span><span class="sxs-lookup"><span data-stu-id="25487-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="25487-121">คุณยังสามารถกำหนดระดับอัตราค่าเบี้ยเลี้ยงต่อวันเพื่อกำหนดจำนวนชั่วโมงขั้นต่ำและสูงสุดที่อัตราค่าเบี้ยเลี้ยงต่อวันสามารถใช้กับการเดินทางของผู้ปฏิบัติงานได้</span><span class="sxs-lookup"><span data-stu-id="25487-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="25487-122">**การตัดสินใจ:**</span><span class="sxs-lookup"><span data-stu-id="25487-122">**Decisions:**</span></span>

- <span data-ttu-id="25487-123">กฎค่าเบี้ยเลี้ยงต่อวันเริ่มต้นสำหรับวันแรกและวันสุดท้าย:</span><span class="sxs-lookup"><span data-stu-id="25487-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="25487-124">จำนวนชั่วโมงขั้นต่ำที่พนักงานสามารถอ้างสิทธิ์ได้ในหนึ่งวันและยังคงได้รับค่าเบี้ยเลี้ยงต่อวันคือเท่าใด</span><span class="sxs-lookup"><span data-stu-id="25487-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="25487-125">มีการลดให้การสนับสนุนค่าอาหารสำหรับวันแรกและวันสุดท้ายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="25487-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="25487-126">ถ้ามีการลดลง เปอร์เซ็นต์ของการลดคือเท่าใด</span><span class="sxs-lookup"><span data-stu-id="25487-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="25487-127">มีการลดให้การสนับสนุนค่าโรงแรมสำหรับวันแรกและวันสุดท้ายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="25487-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="25487-128">ถ้ามีการลดลง เปอร์เซ็นต์ของการลดคือเท่าใด</span><span class="sxs-lookup"><span data-stu-id="25487-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="25487-129">มีการลดให้การสนับสนุนค่าใช้จ่ายอื่นๆ ที่เกิดขึ้นในวันแรกและวันสุดท้ายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="25487-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="25487-130">ถ้ามีการลดลง เปอร์เซ็นต์ของการลดคือเท่าใด</span><span class="sxs-lookup"><span data-stu-id="25487-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="25487-131">กฎค่าเบี้ยเลี้ยงต่อวันเริ่มต้น:</span><span class="sxs-lookup"><span data-stu-id="25487-131">Default per diem rules:</span></span>

    - <span data-ttu-id="25487-132">มีการลดเปอร์เซ็นต์ของค่าเบี้ยเลี้ยงต่อวันสำหรับอาหารแต่ละมื้อหรือไม่ถ้าหาก ตัวอย่างเช่นอาหารนั้นฟรี</span><span class="sxs-lookup"><span data-stu-id="25487-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="25487-133">ถ้ามีการลดลง เปอร์เซ็นต์ของการลดสำหรับอาหารแต่ละมื้อคือเท่าใด</span><span class="sxs-lookup"><span data-stu-id="25487-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="25487-134">การลดมื้ออาหารคำนวณต่อวัน ต่อเที่ยว หรือตามจำนวนมื้อต่อวัน</span><span class="sxs-lookup"><span data-stu-id="25487-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="25487-135">จำนวนค่าเบี้ยเลี้ยงต่อวันควรปัดตามปกติหรือปัดขึ้น</span><span class="sxs-lookup"><span data-stu-id="25487-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="25487-136">ค่าเบี้ยเลี้ยงต่อวันคำนวณตามระยะเวลา 24 ชั่วโมง หรือในวันตามปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="25487-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="25487-137">กฎค่าเบี้ยเลี้ยงต่อวันที่ขึ้นอยู่กับสถานที่:</span><span class="sxs-lookup"><span data-stu-id="25487-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="25487-138">อัตราค่าเบี้ยเลี้ยงต่อวันแตกต่างกันไปตามสถานที่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="25487-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="25487-139">รวมสถานที่ใดบ้าง</span><span class="sxs-lookup"><span data-stu-id="25487-139">What locations are included?</span></span>
    - <span data-ttu-id="25487-140">หากอัตราค่าเบี้ยเลี้ยงต่อวันแตกต่างกันไปตามสถานที่ตั้ง สำหรับแต่ละสถานที่ จะมีการระบุจำนวนเปอร์เซ็นต์ใดสำหรับค่าใช้จ่ายประเภทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="25487-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="25487-141">ค่าอาหาร</span><span class="sxs-lookup"><span data-stu-id="25487-141">Meals</span></span>
        - <span data-ttu-id="25487-142">โรงแรม</span><span class="sxs-lookup"><span data-stu-id="25487-142">Hotel</span></span>
        - <span data-ttu-id="25487-143">ค่าใช้จ่ายอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="25487-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="25487-144">สมุดรายวันและบัญชีการจัดการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="25487-144">Expense management journals and accounts</span></span>

<span data-ttu-id="25487-145">การจัดการค่าใช้จ่ายต้องการให้คุณใช้สมุดรายวันและบัญชีหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="25487-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="25487-146">ตัวอย่างเช่น คุณต้องตัดสินใจว่าจะใช้บัญชีเดียวกันสำหรับการเบิกเงินสดล่วงหน้าและข้อพิพาทเกี่ยวกับบัตรเครดิตหรือไม่</span><span class="sxs-lookup"><span data-stu-id="25487-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="25487-147">**การตัดสินใจ:**</span><span class="sxs-lookup"><span data-stu-id="25487-147">**Decisions:**</span></span>

- <span data-ttu-id="25487-148">สมุดรายวันบัญชีแยกประเภทใดที่ได้รับการอนุมัติรายงานค่าใช้จ่ายที่โพสต์รายการไป</span><span class="sxs-lookup"><span data-stu-id="25487-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="25487-149">บัญชีใดใช้สำหรับการเบิกเงินสดล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="25487-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="25487-150">ควรโพสต์เงินสดล่วงหน้าทันทีหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="25487-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="25487-151">วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="25487-151">Payment methods</span></span>

<span data-ttu-id="25487-152">เมื่อคุณอนุญาตให้พนักงานออกค่าใช้จ่ายในนามของธุรกิจ คุณต้องกำหนดวิธีการชำระเงินที่พนักงานได้รับอนุญาตให้ใช้</span><span class="sxs-lookup"><span data-stu-id="25487-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="25487-153">ตัวอย่างเช่น คุณอาจอนุญาตให้พนักงานใช้เงินสดหรือบัตรเครดิตขององค์กร</span><span class="sxs-lookup"><span data-stu-id="25487-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="25487-154">คุณอาจอนุญาตให้พนักงานใช้บัตรเครดิตส่วนบุคคล แล้วคืนเงินให้พนักงาน</span><span class="sxs-lookup"><span data-stu-id="25487-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="25487-155">คุณต้องตัดสินใจต่อไปนี้สำหรับวิธีการชำระเงินแต่ละวิธีที่คุณอนุญาต</span><span class="sxs-lookup"><span data-stu-id="25487-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="25487-156">**การตัดสินใจ:**</span><span class="sxs-lookup"><span data-stu-id="25487-156">**Decisions:**</span></span>

- <span data-ttu-id="25487-157">วิธีการชำระเงินใดที่ได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="25487-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="25487-158">ใครเป็นเจ้าของค่าใช้จ่ายวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="25487-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="25487-159">มีชนิดบัญชีออฟเซ็ตหรือไม่</span><span class="sxs-lookup"><span data-stu-id="25487-159">Is there an offset account type?</span></span> <span data-ttu-id="25487-160">ถ้ามีชนิดบัญชีออฟเซ็ต คืออะไร</span><span class="sxs-lookup"><span data-stu-id="25487-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="25487-161">ถ้ามีชนิดบัญชีออฟเซ็ต บัญชีคืออะไร</span><span class="sxs-lookup"><span data-stu-id="25487-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="25487-162">หากวิธีการชำระเงินเป็นบัตรเครดิต ควรใช้วิธีการชำระเงินกับธุรกรรมที่นำเข้าเท่านั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="25487-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="25487-163">ประเภทของค่าใช้จ่ายและประเภทที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="25487-163">Expense categories and shared categories</span></span>

<span data-ttu-id="25487-164">เมื่อพนักงานสร้างรายงานค่าใช้จ่าย ค่าใช้จ่ายแต่ละรายการที่พวกเขาบันทึกจะต้องเชื่อมโยงกับประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="25487-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="25487-165">ประเภทค่าใช้จ่ายมาจากประเภทที่ใช้ร่วมกัน ซึ่งสามารถใช้ร่วมกันระหว่างนิติบุคคลในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="25487-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="25487-166">นอกจากนี้ยังสามารถแชร์หมวดหมู่เหล่านี้ได้ในการจัดการโครงการและการบัญชี ทั้งนี้ขึ้นอยู่กับวิธีการกำหนดขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="25487-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="25487-167">ตามข้อกำหนดขององค์กรของคุณและคำแนะนำจากทีมการนำไปใช้งาน กำหนดว่าประเภทที่ใช้ในการจัดการค่าใช้จ่ายจะใช้เฉพาะในการจัดการค่าใช้จ่าย หรือว่าพวกเขาควรใช้ร่วมกันระหว่างการจัดการและการบัญชีโครงการ และการจัดการค่าใช้จ่ายด้วย</span><span class="sxs-lookup"><span data-stu-id="25487-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="25487-168">โปรดทราบว่าประเภทเหล่านี้สามารถใช้ร่วมกันระหว่างโครงการและค่าใช้จ่าย หรือโครงการและการผลิต แต่ไม่ใช่ระหว่างค่าใช้จ่ายและการผลิต</span><span class="sxs-lookup"><span data-stu-id="25487-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="25487-169">คุณต้องตัดสินใจต่อไปนี้สำหรับค่าใช้จ่ายแต่ละประเภท</span><span class="sxs-lookup"><span data-stu-id="25487-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="25487-170">**การตัดสินใจ:**</span><span class="sxs-lookup"><span data-stu-id="25487-170">**Decisions:**</span></span>

- <span data-ttu-id="25487-171">ประเภทค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="25487-171">What is the expense category?</span></span> <span data-ttu-id="25487-172">ตัวอย่างได้แก่ ประเภทสำหรับเที่ยวบิน โรงแรม หรือระยะไมล์</span><span class="sxs-lookup"><span data-stu-id="25487-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="25487-173">ประเภทค่าใช้จ่ายสามารถใช้ในการจัดการและการบัญชีโครงการได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="25487-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="25487-174">ชนิดค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="25487-174">What is the expense type?</span></span>
- <span data-ttu-id="25487-175">วิธีการชำระเงินเริ่มต้นสำหรับประเภทค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="25487-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="25487-176">ค่าใช้จ่ายในประเภทค่าใช้จ่ายต้องแยกรายการหรือไม่</span><span class="sxs-lookup"><span data-stu-id="25487-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="25487-177">บัญชีเริ่มต้นหลักสำหรับประเภทค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="25487-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="25487-178">กลุ่มภาษีขายสินค้าเริ่มต้นสำหรับประเภทค่าใช้จ่ายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="25487-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="25487-179">สามารถใช้วิธีการชำระเงินเพิ่มเติมสำหรับประเภทค่าใช้จ่ายได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="25487-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="25487-180">หากอนุญาตวิธีการชำระเงินเพิ่มเติม มีอะไรบ้าง</span><span class="sxs-lookup"><span data-stu-id="25487-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="25487-181">มีประเภทย่อยในประเภทค่าใช้จ่ายนี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="25487-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="25487-182">หากมีประเภทย่อย คุณต้องตัดสินใจเกี่ยวกับเรื่องต่อไปนี้ด้วย</span><span class="sxs-lookup"><span data-stu-id="25487-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="25487-183">ประเภทย่อยใดๆ ไม่รวมอยู่ในการขอคืนภาษีหรือไม่</span><span class="sxs-lookup"><span data-stu-id="25487-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="25487-184">กลุ่มภาษีขายสินค้าของประเภทย่อยคืออะไร</span><span class="sxs-lookup"><span data-stu-id="25487-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="25487-185">หากยังใช้ประเภทค่าใช้จ่ายในการจัดการโครงการและการบัญชีด้วย ให้ตอบคำถามที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="25487-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="25487-186">มิฉะนั้น ไปยังส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="25487-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="25487-187">บัญชีต้นทุนใดที่จะใช้สำหรับค่าใช้จ่ายต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="25487-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="25487-188">ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="25487-188">Cost</span></span>
    - <span data-ttu-id="25487-189">การจัดสรรเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="25487-189">Payroll allocation</span></span>
    - <span data-ttu-id="25487-190">WIP-มูลค่าต้นทุน</span><span class="sxs-lookup"><span data-stu-id="25487-190">WIP-cost value</span></span>
    - <span data-ttu-id="25487-191">ต้นทุน-สินค้า</span><span class="sxs-lookup"><span data-stu-id="25487-191">Cost-item</span></span>
    - <span data-ttu-id="25487-192">WIP-มูลค่าต้นทุน-สินค้า</span><span class="sxs-lookup"><span data-stu-id="25487-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="25487-193">ขาดทุนสะสม</span><span class="sxs-lookup"><span data-stu-id="25487-193">Accrued loss</span></span>
    - <span data-ttu-id="25487-194">WIP-ขาดทุนสะสม</span><span class="sxs-lookup"><span data-stu-id="25487-194">WIP-accrued loss</span></span>

- <span data-ttu-id="25487-195">บัญชีรายได้ใดที่จะใช้สำหรับต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="25487-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="25487-196">รายได้ที่ออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="25487-196">Invoiced revenue</span></span>
    - <span data-ttu-id="25487-197">มูลค่าการขายของรายได้ค้างรับ</span><span class="sxs-lookup"><span data-stu-id="25487-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="25487-198">WIP-มูลค่าการขาย</span><span class="sxs-lookup"><span data-stu-id="25487-198">WIP-sales value</span></span>
    - <span data-ttu-id="25487-199">รายได้ค้างรับ-การผลิต</span><span class="sxs-lookup"><span data-stu-id="25487-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="25487-200">WIP-การผลิต</span><span class="sxs-lookup"><span data-stu-id="25487-200">WIP-production</span></span>
    - <span data-ttu-id="25487-201">รายได้ค้างรับ-กำไร</span><span class="sxs-lookup"><span data-stu-id="25487-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="25487-202">WIP-กำไร</span><span class="sxs-lookup"><span data-stu-id="25487-202">WIP-profit</span></span>
    - <span data-ttu-id="25487-203">รายได้ค้างรับ-การสมัครใช้งาน</span><span class="sxs-lookup"><span data-stu-id="25487-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="25487-204">WIP-การสมัครใช้งาน</span><span class="sxs-lookup"><span data-stu-id="25487-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="25487-205">ภาษี</span><span class="sxs-lookup"><span data-stu-id="25487-205">Taxes</span></span>

<span data-ttu-id="25487-206">สำหรับภาษีที่เกี่ยวข้องกับค่าใช้จ่าย คุณต้องกำหนดสิ่งที่รวมหรือเปิดใช้งานในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="25487-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="25487-207">**การตัดสินใจ:**</span><span class="sxs-lookup"><span data-stu-id="25487-207">**Decisions:**</span></span>

- <span data-ttu-id="25487-208">ภาษีการขายรวมอยู่ในยอดค่าใช้จ่ายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="25487-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="25487-209">ควรเปิดใช้การกู้คืนภาษีสำหรับค่าใช้จ่ายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="25487-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="25487-210">เมื่อคุณวางแผนบัญชีแยกประเภททั่วไป หากคุณตัดสินใจที่จะใช้ภาษีการขายของสหรัฐอเมริกาและใช้กฎภาษี คุณจะไม่สามารถเปิดใช้งานการกู้คืนภาษีสำหรับค่าใช้จ่ายได้</span><span class="sxs-lookup"><span data-stu-id="25487-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="25487-211">(หากต้องการใช้ภาษีการขายของสหรัฐอเมริกาและใช้กฎภาษี ให้ตั้งค่าตัวเลือก **ใช้กฎภาษีการขาย** เป็น **ใช่** )</span><span class="sxs-lookup"><span data-stu-id="25487-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="25487-212">นโยบาย</span><span class="sxs-lookup"><span data-stu-id="25487-212">Policies</span></span>

<span data-ttu-id="25487-213">การสร้างนโยบายรายงานค่าใช้จ่าย คุณสามารถช่วยให้องค์กรของคุณประหยัดเวลาและค่าใช้จ่าย เมื่อพนักงานต้องเสียค่าใช้จ่ายในนามขององค์กร</span><span class="sxs-lookup"><span data-stu-id="25487-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="25487-214">นโยบายช่วยรับประกันว่าพนักงานจะอยู่ในงบประมาณ ให้ข้อมูลที่จำเป็นทั้งหมด และใช้จ่ายเงินตามที่ต้องการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="25487-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="25487-215">คุณต้องทำการตัดสินใจต่อไปนี้สำหรับนโยบายรายงานค่าใช้จ่ายและนโยบายการอนุมัติรายงานค่าใช้จ่ายแต่ละรายการที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="25487-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="25487-216">**การตัดสินใจ:**</span><span class="sxs-lookup"><span data-stu-id="25487-216">**Decisions:**</span></span>

- <span data-ttu-id="25487-217">นโยบายชื่ออะไร</span><span class="sxs-lookup"><span data-stu-id="25487-217">What is the name of the policy?</span></span>
- <span data-ttu-id="25487-218">นโยบายค่าใช้จ่ายมีไว้ทำอะไร</span><span class="sxs-lookup"><span data-stu-id="25487-218">What is the expense policy for?</span></span>
- <span data-ttu-id="25487-219">หากก่อนหน้านี้คุณตัดสินใจเปิดใช้ค่าใช้จ่ายระหว่างบริษัท นโยบายนี้จะนำไปใช้กับบริษัทใดในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="25487-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="25487-220">นโยบายนี้มีผลบังคับใช้เมื่อใด</span><span class="sxs-lookup"><span data-stu-id="25487-220">When does the policy become effective?</span></span>
- <span data-ttu-id="25487-221">นโยบายจะหมดอายุเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="25487-221">When does the policy expire?</span></span>
- <span data-ttu-id="25487-222">กฎของนโยบายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="25487-222">What is the policy rule?</span></span>
- <span data-ttu-id="25487-223">ผลลัพธ์ของกฎของนโยบายคืออะไร</span><span class="sxs-lookup"><span data-stu-id="25487-223">What is the outcome of the policy rule?</span></span>
