---
title: ภาพรวมการรับรู้รายได้
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการรับรู้รายได้ใน Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013779"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="cfb50-103">ภาพรวมการรับรู้รายได้</span><span class="sxs-lookup"><span data-stu-id="cfb50-103">Revenue recognition overview</span></span>

<span data-ttu-id="cfb50-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="cfb50-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cfb50-105">ใน Dynamics 365 Project Operations หลักการรับรู้รายได้จะแตกต่างกันไปตามวิธีการเรียกเก็บเงินที่เลือกสำหรับโครงการหรือบางส่วนของโครงการ</span><span class="sxs-lookup"><span data-stu-id="cfb50-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="cfb50-106">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการรับรู้รายได้ใน Project Operations.</span><span class="sxs-lookup"><span data-stu-id="cfb50-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="cfb50-107">ธุรกรรมพิจารณาโดยใช้วิธีการเรียกเก็บเงินสำหรับเวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="cfb50-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="cfb50-108">การรับรู้ต้นทุนและรายได้เชื่อมโยงกัน</span><span class="sxs-lookup"><span data-stu-id="cfb50-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="cfb50-109">ต้นทุนธุรกรรมและยอดขายที่ยังไม่เรียกเก็บจะลงรายการบัญชีโดยใช้ [สมุดรายวันการรวม Project Operations](../project-accounting/project-operations-integration-journal.md)</span><span class="sxs-lookup"><span data-stu-id="cfb50-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="cfb50-110">ต้นทุนโครงการและโปรไฟล์รายได้กำหนดว่าธุรกรรมการขายที่ไม่ได้เรียกเก็บเงินถูกลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไปหรือไม่</span><span class="sxs-lookup"><span data-stu-id="cfb50-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="cfb50-111">ถ้า **สะสมรายได้** ถูกเลือก ระบบจะใช้บัญชี **มูลค่าการขาย WIP** และ **มูลค่าการขายรายได้ค้างรับ** ระหว่างการโพสต์</span><span class="sxs-lookup"><span data-stu-id="cfb50-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="cfb50-112">ต่อไปนี้คือตัวอย่างของวิธีนี้</span><span class="sxs-lookup"><span data-stu-id="cfb50-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="cfb50-113">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="cfb50-113">Transaction type</span></span> | <span data-ttu-id="cfb50-114">เดบิต/เครดิต</span><span class="sxs-lookup"><span data-stu-id="cfb50-114">Debit/Credit</span></span> | <span data-ttu-id="cfb50-115">จำนวน</span><span class="sxs-lookup"><span data-stu-id="cfb50-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="cfb50-116">มูลค่าการขาย WIP</span><span class="sxs-lookup"><span data-stu-id="cfb50-116">WIP Sales value</span></span> | <span data-ttu-id="cfb50-117">เดบิต</span><span class="sxs-lookup"><span data-stu-id="cfb50-117">Debit</span></span> | <span data-ttu-id="cfb50-118">100</span><span class="sxs-lookup"><span data-stu-id="cfb50-118">100</span></span> |
  | <span data-ttu-id="cfb50-119">มูลค่าการขายของรายได้ค้างรับ</span><span class="sxs-lookup"><span data-stu-id="cfb50-119">Accrued revenue sales value</span></span> | <span data-ttu-id="cfb50-120">เครดิต</span><span class="sxs-lookup"><span data-stu-id="cfb50-120">Credit</span></span> | <span data-ttu-id="cfb50-121">100</span><span class="sxs-lookup"><span data-stu-id="cfb50-121">100</span></span> |

- <span data-ttu-id="cfb50-122">รายได้รับรู้ได้ระหว่างการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="cfb50-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="cfb50-123">ระบบใช้บัญชี **รายได้ที่ออกใบแจ้งหนี้** ระหว่างการโพสต์</span><span class="sxs-lookup"><span data-stu-id="cfb50-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="cfb50-124">ต่อไปนี้คือตัวอย่างของวิธีนี้</span><span class="sxs-lookup"><span data-stu-id="cfb50-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="cfb50-125">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="cfb50-125">Transaction type</span></span> | <span data-ttu-id="cfb50-126">เดบิต/เครดิต</span><span class="sxs-lookup"><span data-stu-id="cfb50-126">Debit/Credit</span></span> | <span data-ttu-id="cfb50-127">จำนวน</span><span class="sxs-lookup"><span data-stu-id="cfb50-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="cfb50-128">ยอดเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cfb50-128">Customer balance</span></span> | <span data-ttu-id="cfb50-129">เดบิต</span><span class="sxs-lookup"><span data-stu-id="cfb50-129">Debit</span></span> | <span data-ttu-id="cfb50-130">120</span><span class="sxs-lookup"><span data-stu-id="cfb50-130">120</span></span> |
  | <span data-ttu-id="cfb50-131">ภาษีขายที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="cfb50-131">Sales tax payable</span></span> | <span data-ttu-id="cfb50-132">เครดิต</span><span class="sxs-lookup"><span data-stu-id="cfb50-132">Credit</span></span> | <span data-ttu-id="cfb50-133">20</span><span class="sxs-lookup"><span data-stu-id="cfb50-133">20</span></span> |
  | <span data-ttu-id="cfb50-134">รายได้ที่ออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="cfb50-134">Invoiced Revenue</span></span> | <span data-ttu-id="cfb50-135">เครดิต</span><span class="sxs-lookup"><span data-stu-id="cfb50-135">Credit</span></span> | <span data-ttu-id="cfb50-136">100</span><span class="sxs-lookup"><span data-stu-id="cfb50-136">100</span></span> |

- <span data-ttu-id="cfb50-137">หากรายได้ค้างรับเมื่อมีการลงรายการบัญชีการขายที่ยังไม่เรียกเก็บเงิน ระบบจะย้อนกลับรายได้ค้างรับที่เกิดขึ้นในการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="cfb50-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="cfb50-138">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="cfb50-138">Transaction type</span></span> | <span data-ttu-id="cfb50-139">เดบิต/เครดิต</span><span class="sxs-lookup"><span data-stu-id="cfb50-139">Debit/Credit</span></span> | <span data-ttu-id="cfb50-140">จำนวน</span><span class="sxs-lookup"><span data-stu-id="cfb50-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="cfb50-141">มูลค่าการขาย WIP</span><span class="sxs-lookup"><span data-stu-id="cfb50-141">WIP Sales value</span></span> | <span data-ttu-id="cfb50-142">เครดิต</span><span class="sxs-lookup"><span data-stu-id="cfb50-142">Credit</span></span> | <span data-ttu-id="cfb50-143">100</span><span class="sxs-lookup"><span data-stu-id="cfb50-143">100</span></span> |
  | <span data-ttu-id="cfb50-144">มูลค่าการขายของรายได้ค้างรับ</span><span class="sxs-lookup"><span data-stu-id="cfb50-144">Accrued revenue sales value</span></span> | <span data-ttu-id="cfb50-145">เดบิต</span><span class="sxs-lookup"><span data-stu-id="cfb50-145">Debit</span></span> | <span data-ttu-id="cfb50-146">100</span><span class="sxs-lookup"><span data-stu-id="cfb50-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="cfb50-147">ธุรกรรมพิจารณาโดยใช้วิธีการเรียกเก็บเงินแบบราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="cfb50-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="cfb50-148">การรับรู้ต้นทุนและรายได้แยกจากกัน</span><span class="sxs-lookup"><span data-stu-id="cfb50-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="cfb50-149">ต้นทุนธุรกรรมจะลงรายการบัญชีโดยใช้ [สมุดรายวันการรวม Project Operations](../project-accounting/project-operations-integration-journal.md)</span><span class="sxs-lookup"><span data-stu-id="cfb50-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="cfb50-150">ธุรกรรมการขายที่ยังไม่เรียกเก็บเงินไม่ได้สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="cfb50-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="cfb50-151">รายได้สามารถรับรู้ได้ระหว่างการออกใบแจ้งหนี้ หากต้นทุนโครงการและโปรไฟล์รายได้มี **หลักการที่ใช้ในการคำนวณความสำเร็จของโครงการ** ตั้งค่าเป็น **ไม่มี WIP**</span><span class="sxs-lookup"><span data-stu-id="cfb50-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="cfb50-152">ใช้วิธีนี้สำหรับโครงการระยะสั้นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="cfb50-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="cfb50-153">รายได้สามารถรับรู้โดยใช้การประมาณการรายได้ราคาคงที่ โดยใช้วิธี **สัญญาที่เสร็จสมบูรณ์** หรือ **เปอร์เซ็นต์การรับรู้รายได้ที่เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="cfb50-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cfb50-154">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="cfb50-154">Additional resources</span></span>
[<span data-ttu-id="cfb50-155">บทความการกำหนดค่าการบัญชีสำหรับโครงการที่เรียกเก็บเงินได้</span><span class="sxs-lookup"><span data-stu-id="cfb50-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="cfb50-156">โครงการประมาณการรายได้สำหรับราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="cfb50-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="cfb50-157">จัดการประมาณการรายได้</span><span class="sxs-lookup"><span data-stu-id="cfb50-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="cfb50-158">ต้นทุนในการดำเนินการตามวิธีการ</span><span class="sxs-lookup"><span data-stu-id="cfb50-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]