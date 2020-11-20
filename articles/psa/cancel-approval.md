---
title: ยกเลิกรายการเวลาและค่าใช้จ่ายที่อนุมัติก่อนหน้านี้
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการยกเลิกธุรกรรมเวลาและค่าใช้จ่ายของโครงการที่ได้รับอนุมัติ
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 84fc057599dd98162320d6104ed4a7612e894ecb
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123356"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="16ef0-103">ยกเลิกรายการเวลาหรือค่าใช้จ่ายที่อนุมัติก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="16ef0-103">Cancel previously approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="16ef0-104">ในเวอร์ชันล่าสุดของผู้อนุมัติ Dynamics 365 Project Service Automation สามารถยกเลิกรายการเวลาหรือค่าใช้จ่ายที่พวกเขาได้รับอนุมัติก่อนหน้านี้ได้</span><span class="sxs-lookup"><span data-stu-id="16ef0-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="16ef0-105">ยกเลิกรายการเวลาหรือค่าใช้จ่ายที่อนุมัติก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="16ef0-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="16ef0-106">ทำตามขั้นตอนเหล่านี้เพื่อยกเลิกรายการเวลาหรือค่าใช้จ่ายที่คุณได้อนุมัติไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="16ef0-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="16ef0-107">ไปที่ **โครงการ** \> **การทำงานของฉัน** \> **การอนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="16ef0-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="16ef0-108">ในหน้ารายการ **การอนุมัติ** ให้เปลี่ยนมุมมองเป็น **เป็นการอนุมัติที่ผ่านมาของฉัน**</span><span class="sxs-lookup"><span data-stu-id="16ef0-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="16ef0-109">รายการของรายการเวลาและค่าใช้จ่ายที่คุณอนุมัติก่อนหน้านี้จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="16ef0-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="16ef0-110">เลือกอย่างน้อยหนึ่งรายการแล้วเลือก **ยกเลิกการอนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="16ef0-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="16ef0-111">คุณได้รับข้อความเตือน</span><span class="sxs-lookup"><span data-stu-id="16ef0-111">You receive a warning message.</span></span>
4. <span data-ttu-id="16ef0-112">เลือก **ตกลง** เพื่อยกเลิกการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="16ef0-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="16ef0-113">ทำความเข้าใจผลกระทบของการยกเลิกการอนุมัติรายการเวลาหรือค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="16ef0-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="16ef0-114">เมื่อมีการยกเลิกการอนุมัติ จะมีผลกระทบต่อทั้งการดำเนินงานและการเงิน</span><span class="sxs-lookup"><span data-stu-id="16ef0-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="16ef0-115">ผลกระทบต่อการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="16ef0-115">Operational impact</span></span>

<span data-ttu-id="16ef0-116">ในด้านการดำเนินงาน เมื่อยกเลิกการอนุมัติ สถานะของเรกคอร์ดจะถูกตั้งค่าใหม่เป็น **แบบร่าง** และการอนุมัติจะไม่ปรากฏในมุมมอง **การอนุมัติที่ผ่านมาของฉัน** อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="16ef0-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="16ef0-117">การอนุมัติที่ยกเลิกจะปรากฏในมุมมอง **รายการเวลาสำหรับการอนุมัติ** หรือมุมมอง **รายการค่าใช้จ่ายสำหรับการอนุมัติ** โดยขึ้นอยู่กับว่าเป็นรายการเวลาหรือรายการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="16ef0-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="16ef0-118">นอกจากนี้สถานะของรายการเวลาหรือค่าใช้จ่ายที่เกี่ยวข้องจะเปลี่ยนเป็น **ส่ง** เพื่อให้รายการที่เกี่ยวข้องสอดคล้องกับการอนุมัติที่มีสถานะของ **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="16ef0-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="16ef0-119">ในฐานะผู้อนุมัติ คุณสามารถแก้ไขฟิลด์บางส่วนของการอนุมัติที่มีสถานะเป็น **แบบร่าง** ได้</span><span class="sxs-lookup"><span data-stu-id="16ef0-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="16ef0-120">ฟิลด์เหล่านี้รวมถึง **ชนิดของการเรียกเก็บเงิน** และ **ชั่วโมงที่เรียกเก็บเงินได้สำหรับรายการเวลา**</span><span class="sxs-lookup"><span data-stu-id="16ef0-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="16ef0-121">หลังจากที่คุณทำการเปลี่ยนแปลงแล้ว คุณสามารถอนุมัติเรกคอร์ดอีกครั้งได้</span><span class="sxs-lookup"><span data-stu-id="16ef0-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="16ef0-122">อีกทางหนึ่งคือคุณสามารถปฏิเสธรายการได้</span><span class="sxs-lookup"><span data-stu-id="16ef0-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="16ef0-123">ถ้าคุณปฏิเสธการอนุมัติรายการเวลา สถานะของรายการจะถูกเปลี่ยนเป็น **ถูกส่งคืน**</span><span class="sxs-lookup"><span data-stu-id="16ef0-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="16ef0-124">ถ้าคุณปฏิเสธการอนุมัติรายการค่าใช้จ่าย สถานะของรายการจะถูกเปลี่ยนเป็น **ถูกปฏิเสธ**</span><span class="sxs-lookup"><span data-stu-id="16ef0-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="16ef0-125">โดยฟังก์ชันการทำงาน ทั้งรายการที่ส่งคืนและถูกปฏิเสธจะทำหน้าที่เหมือนกับรายการที่มีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="16ef0-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="16ef0-126">สมาชิกในทีมโครงการสามารถทำการเปลี่ยนแปลงใดๆ ที่จำเป็นในรายการแล้วส่งอีกครั้งเพื่ออนุมัติหรือลบรายการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="16ef0-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="16ef0-127">ผลกระทบทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="16ef0-127">Financial impact</span></span>

<span data-ttu-id="16ef0-128">โครงการจะได้รับผลกระทบทางการเงินด้วยเมื่อมีการยกเลิกการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="16ef0-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="16ef0-129">อันดับแรก จะมีการปรับปรุงค่าจริงที่สอดคล้องกันสำหรับต้นทุนและการขายในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="16ef0-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="16ef0-130">สถานะการปรับปรุงถูกตั้งค่าเป็น **ปรับปรุงแล้ว**</span><span class="sxs-lookup"><span data-stu-id="16ef0-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="16ef0-131">สถานะการเรียกเก็บเงินถูกตั้งค่าเป็น **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="16ef0-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="16ef0-132">ถัดไป รายการการกลับรายการจะถูกสร้างขึ้นในตารางจริง</span><span class="sxs-lookup"><span data-stu-id="16ef0-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="16ef0-133">ถ้าต้องการสร้างรายการการกลับรายการ ระบบจะคัดลอกค่าของฟิลด์จากต้นฉบับที่เกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="16ef0-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="16ef0-134">ค่าเดียวที่ไม่ได้คัดลอกมาคือค่าปริมาณ</span><span class="sxs-lookup"><span data-stu-id="16ef0-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="16ef0-135">ค่าเหล่านี้จะถูกกลับรายการแทน</span><span class="sxs-lookup"><span data-stu-id="16ef0-135">These values are reversed instead.</span></span> <span data-ttu-id="16ef0-136">ค่าจริงที่กลับรายการจะถูกสร้างสำหรับทั้งค่า **ต้นทุน** และ **ยอดขายที่ยังไม่ได้เรียกเก็บเงิน** จริง</span><span class="sxs-lookup"><span data-stu-id="16ef0-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="16ef0-137">ฟิลด์ **สถานะการปรับปรุง** ในค่าจริงที่กลับรายการถูกตั้งค่าเป็น **ไม่สามารถปรับเปลี่ยนได้** และสถานะการเรียกเก็บเงินถูกตั้งค่าเป็น **ยกเลิกแล้ว**</span><span class="sxs-lookup"><span data-stu-id="16ef0-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="16ef0-138">หลังจากทำการเปลี่ยนแปลงเหล่านี้ ยอดเงินที่ถูกบันทึกเป็นใช้ไปในโครงการและรายการคงค้างของรายได้ในโครงการจะมีบัญชีสำหรับยอดเงินที่แสดงค่าจริงเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="16ef0-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
