---
title: การแก้ไขเป็นกลุ่มของข้อมูลจริงที่สร้างขึ้นโดยเวลาที่ได้รับอนุมัติและรายการค่าใช้จ่าย
description: หัวข้อนี้อธิบายวิธีที่ผู้ดูแลระบบสามารถทำการแก้ไขเดียวหรือเป็นกลุ่มสำหรับรายการเวลาหรือค่าใช้จ่ายที่ได้รับอนุมัติก่อนหน้านี้ หากการเรียกเก็บเงินไม่สมบูรณ์
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 17d6648840e27a4e573985af2cdd74c4adf878e1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290922"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="a07eb-103">การแก้ไขเป็นกลุ่มของข้อมูลจริงที่สร้างขึ้นโดยเวลาที่ได้รับอนุมัติและรายการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a07eb-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a07eb-104">บางครั้ง อาจมีการป้อนเวลาหรือค่าใช้จ่ายอย่างไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a07eb-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="a07eb-105">ตัวอย่างเช่น ที่ปรึกษาอาจเลือกวันที่ที่ไม่ถูกต้อง เมื่อสร้างรายการเวลา หรือพวกเขาอาจสลับเปลี่ยนตัวเลขเมื่อป้อนค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a07eb-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="a07eb-106">หากที่ปรึกษาไม่สามารถปรับปรุงรายการที่ส่งได้ ผู้ดูแลระบบสามารถแก้ไขรายการสำหรับโครงการได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="a07eb-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="a07eb-107">หากต้องการทำกระบวนงานในหัวข้อนี้ให้เสร็จสมบูรณ์ คุณจะต้องมีสิทธิ์ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="a07eb-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="a07eb-108">แก้ไขรายการเวลาที่อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="a07eb-108">Correct approved time entries</span></span>     

<span data-ttu-id="a07eb-109">ทำขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์เพื่อแก้ไขรายการเวลาเดียวหรือหลายรายการสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="a07eb-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="a07eb-110">ในพื้นที่ **การขาย** เลือก **ธุรกรรม** แล้วเลือก **เวลาที่อนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="a07eb-110">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="a07eb-111">ในรายการ **เวลาที่อนุมัติ** ค้นหาและเลือกรายการเวลาที่อนุมัติอย่างน้อยหนึ่งรายการเพื่อแก้ไข</span><span class="sxs-lookup"><span data-stu-id="a07eb-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="a07eb-112">คุณสามารถใช้ตัวกรองเพื่อค้นหารายการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="a07eb-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="a07eb-113">ตัวอย่างเช่น คุณอาจกรองรหัสโครงการ และเลือกรายการเวลาที่อนุมัติทั้งหมดด้วยรหัสโครงการนั้น</span><span class="sxs-lookup"><span data-stu-id="a07eb-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="a07eb-114">เลือก **แก้ไขรายการ**</span><span class="sxs-lookup"><span data-stu-id="a07eb-114">Select **Correct entries**.</span></span> <span data-ttu-id="a07eb-115">สมุดรายวันการแก้ไขใหม่จะถูกสร้างขึ้นโดยอัตโนมัติด้วยชนิดที่กำหนด **การแก้ไขเวลา**</span><span class="sxs-lookup"><span data-stu-id="a07eb-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="a07eb-116">รายการที่คุณเลือกจะถูกเพิ่มลงในสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="a07eb-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="a07eb-117">บนหน้า **สมุดรายวันใหม่** ป้อน **คำอธิบาย** สำหรับสมุดรายวันการแก้ไขของคุณ แล้วเลือกแท็บ **การแก้ไขรายการเวลา**</span><span class="sxs-lookup"><span data-stu-id="a07eb-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="a07eb-118">ในส่วน **ค่าใหม่สำหรับรายการเวลา** ให้ปรับปรุงฟิลด์ด้วยข้อมูลที่ถูกต้องตามที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="a07eb-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="a07eb-119">ตัวอย่างเช่น คุณสามารถเปลี่ยนโครงการที่กำหนดหรือทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="a07eb-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="a07eb-120">เลือก **แสดงตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="a07eb-120">Select **Preview**.</span></span> <span data-ttu-id="a07eb-121">ในกล่องโต้ตอบ ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a07eb-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="a07eb-122">บนแท็บ **รายการสมุดรายวัน** คุณสามารถดูรายการของข้อมูลจริงดั้งเดิมที่เกี่ยวข้องกับรายการเวลาที่เลือกซึ่งได้รับการกลับรายการและรายการที่สอดคล้องที่แก้ไขแล้วซึ่งถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a07eb-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="a07eb-123">หากจำเป็นต้องทำการแก้ไขเพิ่มเติม ให้ทำซ้ำขั้นตอนที่ 5 และ 6</span><span class="sxs-lookup"><span data-stu-id="a07eb-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="a07eb-124">ค่าจริงที่แก้ไขแล้วทั้งหมดจะมีค่าเดียวกับที่คุณเลือกในส่วน **ค่าใหม่สำหรับรายการเวลา**</span><span class="sxs-lookup"><span data-stu-id="a07eb-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="a07eb-125">หากการแก้ไขปรากฏตามที่คาดหมาย ให้เลือก **ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="a07eb-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="a07eb-126">ในกล่องโต้ตอบ ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a07eb-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="a07eb-127">กลับไปที่พื้นที่ **การขาย** เลือก **โครงการ** และจากนั้น เปิดโครงการที่คุณเพิ่งปรับปรุงรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="a07eb-127">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="a07eb-128">บนหน้า **โครงการ** บนแท็บ **ข้อมูลจริง** ดูการเปลี่ยนแปลงที่คุณทำ</span><span class="sxs-lookup"><span data-stu-id="a07eb-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="a07eb-129">ถ้ามองไม่เห็นแท็บ **ข้อมูลจริง** ให้เลือก **ที่เกี่ยวข้อง** > **ข้อมูลจริง**</span><span class="sxs-lookup"><span data-stu-id="a07eb-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="a07eb-130">ในรายการ **มุมมองที่เกี่ยวข้องจริง** คุณจะเห็นว่ารายการเวลาดั้งเดิมที่ถูกกลับรายการนั้นยังคงอยู่ในรายการ เช่นเดียวกับรายการเวลาที่แก้ไขที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="a07eb-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="a07eb-131">ตัวอย่างเช่น ในกราฟิกต่อไปนี้ มีรายการสองรายการที่มีปริมาณเป็น 8.00 ซึ่งมีเดบิตที่แสดงรายการในคอลัมน์จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="a07eb-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="a07eb-132">นอกจากนี้ ยังมีรายการสองรายการที่มีปริมาณเป็น -8.00 ซึ่งแสดงจำนวนที่มีการให้สินเชื่อในคอลัมน์จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="a07eb-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="a07eb-133">การแก้ไขเหล่านี้ทำให้ปริมาณเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="a07eb-133">These corrections bring the quantity to zero.</span></span>

![รายการมุมมองที่เชื่อมโยงตามจริง](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="a07eb-135">แก้ไขรายการค่าใช้จ่ายที่อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="a07eb-135">Correct approved expense entries</span></span>

<span data-ttu-id="a07eb-136">ทำขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์ เพื่อแก้ไขรายการค่าใช้จ่ายอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="a07eb-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="a07eb-137">ในพื้นที่ **การขาย** ในบานหน้าต่างนำทางด้านซ้าย ภายใต้ **ธุรกรรม** เลือก **ค่าใช้จ่ายที่อนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="a07eb-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="a07eb-138">ในรายการ **ค่าใช้จ่ายที่อนุมัติ** ให้เลือกโครงการที่คุณต้องการแก้ไข แล้วเลือก **แก้ไขรายการ**</span><span class="sxs-lookup"><span data-stu-id="a07eb-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="a07eb-139">สมุดรายวันการแก้ไขใหม่จะถูกสร้างขึ้นโดยอัตโนมัติด้วยชนิดที่กำหนดของ **การแก้ไขค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="a07eb-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="a07eb-140">บนหน้า **สมุดรายวันใหม่** ป้อน **คำอธิบาย** สำหรับการแก้ไข และบนแท็บ **การแก้ไขค่าใช้จ่าย** ในส่วน **ค่าใหม่สำหรับค่าใช้จ่าย** ให้เลือกฟิลด์ข้อมูลที่คุณต้องการแก้ไขสำหรับรายการค่าใช้จ่ายที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a07eb-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="a07eb-141">ตัวอย่างเช่น คุณสามารถกำหนดค่าใช้จ่ายให้กับ **โครงการ** อื่น หรือแก้ไข **ประเภทค่าใช้จ่าย** **วันที่ของค่าใช้จ่าย** หรือ **ทรัพยากรที่สามารถจองได้**</span><span class="sxs-lookup"><span data-stu-id="a07eb-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="a07eb-142">เลือก **แสดงตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="a07eb-142">Select **Preview**.</span></span> <span data-ttu-id="a07eb-143">ในกล่องโต้ตอบ ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a07eb-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="a07eb-144">ตรวจสอบการแก้ไขบนแท็บ **รายการสมุดรายวัน** คุณสามารถดูรายการของข้อมูลจริงดั้งเดิมที่เกี่ยวข้องกับรายการค่าใช้จ่ายที่เลือกซึ่งได้รับการกลับรายการและรายการที่สอดคล้องกันซึ่งแก้ไขแล้วซึ่งถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a07eb-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="a07eb-145">หากค่าที่แก้ไขเป็นตามที่คาดหมาย ให้เลือก **ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="a07eb-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="a07eb-146">ในกล่องโต้ตอบ ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a07eb-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="a07eb-147">หากค่าไม่แสดงตามที่คาดไว้ ให้เลือก **ยกเลิก** เพื่อกลับไปที่รายการ **ค่าใช้จ่ายที่อนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="a07eb-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="a07eb-148">ทำซ้ำขั้นตอนที่ 2 ถึง 5</span><span class="sxs-lookup"><span data-stu-id="a07eb-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="a07eb-149">ค่าจริงที่แก้ไขแล้วจะมีค่าเดียวกับที่คุณเลือกในส่วน **ค่าใหม่สำหรับค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="a07eb-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="a07eb-150">หลังจากที่คุณยืนยันสมุดรายวันการแก้ไข ให้นำทางกลับไปที่โครงการหรือโครงการที่คุณปรับปรุง เพื่อดูการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="a07eb-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="a07eb-151">ในหน้าโครงการ บนแท็บ **ข้อมูลจริง** ตรวจสอบ **มุมมองที่เกี่ยวข้องจริง**</span><span class="sxs-lookup"><span data-stu-id="a07eb-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="a07eb-152">รายการต้นฉบับและรายการที่แก้ไขจะแสดงรายการ</span><span class="sxs-lookup"><span data-stu-id="a07eb-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="a07eb-153">ภาพต่อไปนี้แสดงจำนวนรายการค่าใช้จ่ายดั้งเดิมและจำนวนรายการค่าใช้จ่ายที่แก้ไขแล้วซึ่งสอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="a07eb-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![ค่าใช้จ่ายตามจริง](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]