---
title: การประมวลผลใบเสร็จรับเงินค่าใช้จ่าย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการประมวลผลการรู้จำอักขระด้วยแสง (OCR) สำหรับใบเสร็จรับเงิน คุณลักษณะนี้ออกแบบมาเพื่อปรับปรุงประสบการณ์ของผู้ใช้เมื่อสร้างรายงานค่าใช้จ่ายใน Microsoft Dynamics 365 Finance
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 64901610144f9dfe274bd4c2294ab32659743a1a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960315"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="d6e83-104">การประมวลผลใบเสร็จรับเงินค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d6e83-104">Expense receipt processing</span></span>

<span data-ttu-id="d6e83-105">รายการค่าใช้จ่ายได้รับการปรับปรุงโดยการใช้การประมวลผลการรู้จำอักขระด้วยแสง (OCR) สำหรับใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="d6e83-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="d6e83-106">คุณลักษณะนี้ออกแบบมาเพื่อปรับปรุงประสบการณ์ของผู้ใช้เมื่อสร้างรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d6e83-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="d6e83-107">คุณลักษณะสำคัญ</span><span class="sxs-lookup"><span data-stu-id="d6e83-107">Key features</span></span>

- <span data-ttu-id="d6e83-108">ระบบจะแยกชื่อผู้ขาย วันที่ และจำนวนเงินทั้งหมดออกจากใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="d6e83-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="d6e83-109">คุณลักษณะพยายามจับคู่ใบเสร็จที่ไม่ได้แนบกับธุรกรรมค่าใช้จ่ายที่ไม่ได้แนบมา</span><span class="sxs-lookup"><span data-stu-id="d6e83-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="d6e83-110">ผู้ใช้สามารถสร้างธุรกรรมค่าใช้จ่ายที่ป้อนด้วยตนเองจากใบเสร็จรับเงินได้</span><span class="sxs-lookup"><span data-stu-id="d6e83-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="d6e83-111">ตัวอย่างการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d6e83-111">Usage examples</span></span>

<span data-ttu-id="d6e83-112">หากต้องการแนบใบเสร็จรับเงินที่มีธุรกรรมบัตรเครดิตโดยอัตโนมัติเมื่อสร้างรายงานค่าใช้จ่าย ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d6e83-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="d6e83-113">เปิดพื้นที่ทำงาน **การจัดการค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="d6e83-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="d6e83-114">บนแท็บ **ใบเสร็จรับเงิน** ตรวจสอบว่ามีใบเสร็จรับเงินที่ไม่ได้แนบอยู่</span><span class="sxs-lookup"><span data-stu-id="d6e83-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="d6e83-115">คุณยังสามารถอัปโหลดใบเสร็จรับเงินในแท็บ **รายรับ**</span><span class="sxs-lookup"><span data-stu-id="d6e83-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="d6e83-116">บนแท็บ **ค่าใช้จ่าย** ตรวจสอบว่ามีใบเสร็จรับเงินที่ไม่ได้แนบอยู่</span><span class="sxs-lookup"><span data-stu-id="d6e83-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="d6e83-117">โดยปกติ ผู้ดดูแลระบบค่าใช้จ่ายจะนำเข้าค่าใช้จ่ายเหล่านี้จากผู้ให้บริการบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="d6e83-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="d6e83-118">เลือก **รายงานค่าใช้จ่ายใหม่**</span><span class="sxs-lookup"><span data-stu-id="d6e83-118">Select **New expense report**.</span></span> <span data-ttu-id="d6e83-119">สังเกตว่าคุณสามารถรวมค่าใช้จ่ายและใบเสร็จรับเงินได้เช่นกันเดียวกับเมื่อคุณสร้างรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d6e83-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="d6e83-120">หากคุณเพิ่มทั้งค่าใช้จ่ายและใบเสร็จรับเงิน การจับคู่ใบเสร็จรับเงินกับค่าใช้จ่ายโดยอัตโนมัติจะถูกทริกเกอร์</span><span class="sxs-lookup"><span data-stu-id="d6e83-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="d6e83-121">หากต้องการสร้างค่าใช้จ่าย หรือจับคู่ค่าใช้จ่ายจากใบเสร็จรับเงิน ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d6e83-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="d6e83-122">ในรายงานค่าใช้จ่าย บนแท็บ **ใบเสร็จรับเงิน** ให้แนบใบเสร็จรับเงินโดยการเลือก **เพิ่มใบเสร็จรับเงิน**</span><span class="sxs-lookup"><span data-stu-id="d6e83-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="d6e83-123">ใต้ภาพใบเสร็จรับเงินที่อัปโหลด โปรดสังเกตตัวเลือก **สร้าง** และ **จับคู่**</span><span class="sxs-lookup"><span data-stu-id="d6e83-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="d6e83-124">เลือก **สร้าง** เพื่อสร้างธุรกรรมค่าใช้จ่ายที่ป้อนด้วยตนเองและกรอกค่าที่ดึงออกมาจากใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="d6e83-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="d6e83-125">หากคุณเลือก **จับคู่** ระบบจะพยายามจับคู่ค่าใช้จ่ายที่มีอยู่กับใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="d6e83-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="d6e83-126">การติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="d6e83-126">Installation</span></span>

<span data-ttu-id="d6e83-127">คุณลักษณะนี้ทำงานร่วมกับคุณลักษณะ **รายงานค่าใช้จ่ายที่สมมติขึ้น** ที่จะช่วยลดความซับซ้อนของประสบการณ์ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d6e83-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="d6e83-128">คุณลักษณะนี้ใช้ได้เฉพาะกับสภาพแวดล้อมระดับ 2+ ซึ่ง ได้แก่ Sandbox และการใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="d6e83-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="d6e83-129">หากต้องการใช้ความสามารถของค่าใช้จ่ายขั้นสูงเหล่านี้ ให้ติดตั้ง Add-in ของ บริการจัดการค่าใช้จ่ายสำหรับ Microsoft Dynamics 365 Finance และเปิดคุณลักษณะในอินสแตนซ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d6e83-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="d6e83-130">คุณสามารถเข้าถึง Add-in จากโครงการของคุณใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="d6e83-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="d6e83-131">ลงชื่อเข้าใช้ LCS และเปิดสภาพแวดล้อมที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d6e83-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="d6e83-132">ไปที่ **รายละเอียดทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="d6e83-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="d6e83-133">เลือก **รักษา** หรือเลื่อนลงไปที่แท็บด่วน **Add-in ของสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="d6e83-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="d6e83-134">เลือก **ติดตั้ง Add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="d6e83-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="d6e83-135">เลือก **บริการจัดการค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="d6e83-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="d6e83-136">ปฏิบัติตามคู่มือการติดตั้ง และยอมรับข้อกำหนดและเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="d6e83-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="d6e83-137">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="d6e83-137">Select **Install**.</span></span>

<span data-ttu-id="d6e83-138">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** เปิดคุณลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d6e83-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="d6e83-139">รายงานค่าใช้จ่ายที่สมมติขึ้น</span><span class="sxs-lookup"><span data-stu-id="d6e83-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="d6e83-140">จับคู่อัตโนมัติและสร้างค่าใช้จ่ายจากใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="d6e83-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="d6e83-141">เมื่อคุณเปิดคุณลักษณะเหล่านี้ การดำเนินการต่อไปนี้จะเกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="d6e83-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="d6e83-142">พื้นที่ทำงาน **การจัดการค่าใช้จ่าย** ที่มีอยู่จะถูกแทนที่ด้วยพื้นที่ทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="d6e83-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="d6e83-143">ระบบจะเพิ่มรายการเมนูใหม่สำหรับการมองเห็นฟิลด์ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d6e83-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="d6e83-144">คุณยังสามารถเปิดเพจ **รายงานค่าใช้จ่าย** ของเดิมได้โดยไปที่ **การจัดการค่าใช้จ่าย > ค่าใช้จ่ายของฉัน > รายงานค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="d6e83-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="d6e83-145">เวิร์กโฟลว์และการอนุมัติใดๆ ยังคงนำคุณไปยังเพจรายงานค่าใช้จ่ายที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="d6e83-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="d6e83-146">ใบเสร็จรับเงินจะได้รับการดำเนินการผ่าน Microsoft Azure Cognitive Services และเมตาดาต้าจะถูกแยกและเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="d6e83-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="d6e83-147">มีการเพิ่มตัวเลือกที่ช่วยให้คุณสามารถสร้างรายงานค่าใช้จ่ายที่มีใบเสร็จรับเงินที่ไม่ได้แนบที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="d6e83-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="d6e83-148">ตัวเลือกที่เพิ่มลงในรายงานค่าใช้จ่ายช่วยให้คุณสามารถสร้างรายการค่าใช้จ่ายจากใบเสร็จรับเงิน หรือพยายามจับคู่ใบเสร็จรับเงินที่มีอยู่กับรายการค่าใช้จ่ายที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="d6e83-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="d6e83-149">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะที่สมมติขึ้นของรายงานค่าใช้จ่าย โปรดดู [รายงานค่าใช้จ่ายที่สมมติขึ้น](ExpenseWorkspaceNew.md)</span><span class="sxs-lookup"><span data-stu-id="d6e83-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="d6e83-150">คำถามที่ถามบ่อย</span><span class="sxs-lookup"><span data-stu-id="d6e83-150">Frequently asked questions</span></span>

<span data-ttu-id="d6e83-151">**Microsoft ใช้ข้อมูลของฉันสำหรับแบบจำลองหรือไม่**</span><span class="sxs-lookup"><span data-stu-id="d6e83-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="d6e83-152">ไม่ Microsoft สร้างแบบจำลองการเรียนรู้ของเครื่องทั่วไปสำหรับบริการประมวลผลใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="d6e83-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="d6e83-153">แบบจำลองนี้ไม่ได้ขึ้นอยู่กับใบเสร็จรับเงินที่คุณอัปโหลด</span><span class="sxs-lookup"><span data-stu-id="d6e83-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="d6e83-154">**คุณลักษณะนี้มีให้บริการและประมวลผลที่ไหน**</span><span class="sxs-lookup"><span data-stu-id="d6e83-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="d6e83-155">ปัจจุบัน รองรับในสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="d6e83-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="d6e83-156">**ใบเสร็จรับเงินของฉันไปที่ไหน**</span><span class="sxs-lookup"><span data-stu-id="d6e83-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="d6e83-157">Finance จะติดต่อ Cognitive Services เพื่อดึงข้อมูลภาคสนาม</span><span class="sxs-lookup"><span data-stu-id="d6e83-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="d6e83-158">Cognitive Services จะเก็บสำเนาใบเสร็จรับเงินของคุณไว้เป็นเวลา 24 ชั่วโมงในขณะที่มีการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="d6e83-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="d6e83-159">หลังจากการประมวลผลเสร็จสิ้น Cognitive Services จะลบใบเสร็จรับเงินออก</span><span class="sxs-lookup"><span data-stu-id="d6e83-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="d6e83-160">ใบเสร็จรับเงินยังคงเก็บไว้ใน Finance</span><span class="sxs-lookup"><span data-stu-id="d6e83-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="d6e83-161">สำหรับข้อมูลเพิ่มเติม โปรดดู [เปิดใช้งานการทำความเข้าใจใบเสร็จรับเงินด้วยความสามารถใหม่ของตัวรู้จำฟอร์ม](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)</span><span class="sxs-lookup"><span data-stu-id="d6e83-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
