---
title: ภาพรวมการรับรู้รายได้
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการรับรู้รายได้ใน Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368049"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="ff61c-103">ภาพรวมการรับรู้รายได้</span><span class="sxs-lookup"><span data-stu-id="ff61c-103">Revenue recognition overview</span></span>

<span data-ttu-id="ff61c-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="ff61c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ff61c-105">ใน Dynamics 365 Project Operations หลักการรับรู้รายได้จะแตกต่างกันไปตามวิธีการเรียกเก็บเงินที่เลือกสำหรับโครงการหรือบางส่วนของโครงการ</span><span class="sxs-lookup"><span data-stu-id="ff61c-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="ff61c-106">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการรับรู้รายได้ใน Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ff61c-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="ff61c-107">ธุรกรรมพิจารณาโดยใช้วิธีการเรียกเก็บเงินสำหรับเวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="ff61c-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="ff61c-108">การรับรู้ต้นทุนและรายได้เชื่อมโยงกัน</span><span class="sxs-lookup"><span data-stu-id="ff61c-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="ff61c-109">ต้นทุนธุรกรรมและยอดขายที่ยังไม่เรียกเก็บจะลงรายการบัญชีโดยใช้ [สมุดรายวันการรวม Project Operations](../project-accounting/project-operations-integration-journal.md)</span><span class="sxs-lookup"><span data-stu-id="ff61c-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="ff61c-110">ต้นทุนโครงการและโปรไฟล์รายได้กำหนดว่าธุรกรรมการขายที่ไม่ได้เรียกเก็บเงินถูกลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไปหรือไม่</span><span class="sxs-lookup"><span data-stu-id="ff61c-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="ff61c-111">ถ้า **สะสมรายได้** ถูกเลือก ระบบจะใช้บัญชี **มูลค่าการขาย WIP** และ **มูลค่าการขายรายได้ค้างรับ** ระหว่างการโพสต์</span><span class="sxs-lookup"><span data-stu-id="ff61c-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="ff61c-112">ต่อไปนี้คือตัวอย่างของวิธีนี้</span><span class="sxs-lookup"><span data-stu-id="ff61c-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="ff61c-113">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ff61c-113">Transaction type</span></span> | <span data-ttu-id="ff61c-114">เดบิต/เครดิต</span><span class="sxs-lookup"><span data-stu-id="ff61c-114">Debit/Credit</span></span> | <span data-ttu-id="ff61c-115">จำนวน</span><span class="sxs-lookup"><span data-stu-id="ff61c-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="ff61c-116">มูลค่าการขาย WIP</span><span class="sxs-lookup"><span data-stu-id="ff61c-116">WIP Sales value</span></span> | <span data-ttu-id="ff61c-117">เดบิต</span><span class="sxs-lookup"><span data-stu-id="ff61c-117">Debit</span></span> | <span data-ttu-id="ff61c-118">100</span><span class="sxs-lookup"><span data-stu-id="ff61c-118">100</span></span> |
  | <span data-ttu-id="ff61c-119">มูลค่าการขายของรายได้ค้างรับ</span><span class="sxs-lookup"><span data-stu-id="ff61c-119">Accrued revenue sales value</span></span> | <span data-ttu-id="ff61c-120">เครดิต</span><span class="sxs-lookup"><span data-stu-id="ff61c-120">Credit</span></span> | <span data-ttu-id="ff61c-121">100</span><span class="sxs-lookup"><span data-stu-id="ff61c-121">100</span></span> |

- <span data-ttu-id="ff61c-122">รายได้รับรู้ได้ระหว่างการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ff61c-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="ff61c-123">ระบบใช้บัญชี **รายได้ที่ออกใบแจ้งหนี้** ระหว่างการโพสต์</span><span class="sxs-lookup"><span data-stu-id="ff61c-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="ff61c-124">ต่อไปนี้คือตัวอย่างของวิธีนี้</span><span class="sxs-lookup"><span data-stu-id="ff61c-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="ff61c-125">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ff61c-125">Transaction type</span></span> | <span data-ttu-id="ff61c-126">เดบิต/เครดิต</span><span class="sxs-lookup"><span data-stu-id="ff61c-126">Debit/Credit</span></span> | <span data-ttu-id="ff61c-127">จำนวน</span><span class="sxs-lookup"><span data-stu-id="ff61c-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="ff61c-128">ยอดเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="ff61c-128">Customer balance</span></span> | <span data-ttu-id="ff61c-129">เดบิต</span><span class="sxs-lookup"><span data-stu-id="ff61c-129">Debit</span></span> | <span data-ttu-id="ff61c-130">120</span><span class="sxs-lookup"><span data-stu-id="ff61c-130">120</span></span> |
  | <span data-ttu-id="ff61c-131">ภาษีขายที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="ff61c-131">Sales tax payable</span></span> | <span data-ttu-id="ff61c-132">เครดิต</span><span class="sxs-lookup"><span data-stu-id="ff61c-132">Credit</span></span> | <span data-ttu-id="ff61c-133">20</span><span class="sxs-lookup"><span data-stu-id="ff61c-133">20</span></span> |
  | <span data-ttu-id="ff61c-134">รายได้ที่ออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ff61c-134">Invoiced Revenue</span></span> | <span data-ttu-id="ff61c-135">เครดิต</span><span class="sxs-lookup"><span data-stu-id="ff61c-135">Credit</span></span> | <span data-ttu-id="ff61c-136">100</span><span class="sxs-lookup"><span data-stu-id="ff61c-136">100</span></span> |

- <span data-ttu-id="ff61c-137">หากรายได้ค้างรับเมื่อมีการลงรายการบัญชีการขายที่ยังไม่เรียกเก็บเงิน ระบบจะย้อนกลับรายได้ค้างรับที่เกิดขึ้นในการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ff61c-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="ff61c-138">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ff61c-138">Transaction type</span></span> | <span data-ttu-id="ff61c-139">เดบิต/เครดิต</span><span class="sxs-lookup"><span data-stu-id="ff61c-139">Debit/Credit</span></span> | <span data-ttu-id="ff61c-140">จำนวน</span><span class="sxs-lookup"><span data-stu-id="ff61c-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="ff61c-141">มูลค่าการขาย WIP</span><span class="sxs-lookup"><span data-stu-id="ff61c-141">WIP Sales value</span></span> | <span data-ttu-id="ff61c-142">เครดิต</span><span class="sxs-lookup"><span data-stu-id="ff61c-142">Credit</span></span> | <span data-ttu-id="ff61c-143">100</span><span class="sxs-lookup"><span data-stu-id="ff61c-143">100</span></span> |
  | <span data-ttu-id="ff61c-144">มูลค่าการขายของรายได้ค้างรับ</span><span class="sxs-lookup"><span data-stu-id="ff61c-144">Accrued revenue sales value</span></span> | <span data-ttu-id="ff61c-145">เดบิต</span><span class="sxs-lookup"><span data-stu-id="ff61c-145">Debit</span></span> | <span data-ttu-id="ff61c-146">100</span><span class="sxs-lookup"><span data-stu-id="ff61c-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="ff61c-147">ธุรกรรมพิจารณาโดยใช้วิธีการเรียกเก็บเงินแบบราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="ff61c-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="ff61c-148">การรับรู้ต้นทุนและรายได้แยกจากกัน</span><span class="sxs-lookup"><span data-stu-id="ff61c-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="ff61c-149">ต้นทุนธุรกรรมจะลงรายการบัญชีโดยใช้ [สมุดรายวันการรวม Project Operations](../project-accounting/project-operations-integration-journal.md)</span><span class="sxs-lookup"><span data-stu-id="ff61c-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="ff61c-150">ธุรกรรมการขายที่ยังไม่เรียกเก็บเงินไม่ได้สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="ff61c-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="ff61c-151">รายได้สามารถรับรู้ได้ระหว่างการออกใบแจ้งหนี้ หากต้นทุนโครงการและโปรไฟล์รายได้มี **หลักการที่ใช้ในการคำนวณความสำเร็จของโครงการ** ตั้งค่าเป็น **ไม่มี WIP**</span><span class="sxs-lookup"><span data-stu-id="ff61c-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="ff61c-152">ใช้วิธีนี้สำหรับโครงการระยะสั้นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ff61c-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="ff61c-153">รายได้สามารถรับรู้โดยใช้การประมาณการรายได้ราคาคงที่ โดยใช้วิธี **สัญญาที่เสร็จสมบูรณ์** หรือ **เปอร์เซ็นต์การรับรู้รายได้ที่เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="ff61c-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff61c-154">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ff61c-154">Additional resources</span></span>
[<span data-ttu-id="ff61c-155">บทความการกำหนดค่าการบัญชีสำหรับโครงการที่เรียกเก็บเงินได้</span><span class="sxs-lookup"><span data-stu-id="ff61c-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="ff61c-156">โครงการประมาณการรายได้สำหรับราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="ff61c-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="ff61c-157">จัดการประมาณการรายได้</span><span class="sxs-lookup"><span data-stu-id="ff61c-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="ff61c-158">ต้นทุนในการดำเนินการตามวิธีการ</span><span class="sxs-lookup"><span data-stu-id="ff61c-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]