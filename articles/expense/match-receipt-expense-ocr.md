---
title: จับคู่ใบเสร็จกับค่าใช้จ่ายโดยใช้ OCR
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการประมวลผลการรู้จำอักขระด้วยแสง (OCR) สำหรับใบเสร็จรับเงิน
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 62d6316c9602089518a94267d8ef2b7fb8d59cd0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085897"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="669d4-103">จับคู่ใบเสร็จกับค่าใช้จ่ายโดยใช้ OCR</span><span class="sxs-lookup"><span data-stu-id="669d4-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="669d4-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="669d4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="669d4-105">รายการค่าใช้จ่ายได้รับการปรับปรุงโดยการใช้การประมวลผลการรู้จำอักขระด้วยแสง (OCR) สำหรับใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="669d4-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="669d4-106">ฟังก์ชันนี้ออกแบบมาเพื่อปรับปรุงประสบการณ์ของผู้ใช้เมื่อสร้างรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="669d4-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="669d4-107">คุณลักษณะสำคัญ</span><span class="sxs-lookup"><span data-stu-id="669d4-107">Key features</span></span>

- <span data-ttu-id="669d4-108">ระบบจะแยกชื่อผู้ขาย วันที่ และจำนวนเงินทั้งหมดออกจากใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="669d4-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="669d4-109">ระบบจะพยายามจับคู่ใบเสร็จที่ไม่ได้แนบกับธุรกรรมค่าใช้จ่ายที่ไม่ได้แนบมา</span><span class="sxs-lookup"><span data-stu-id="669d4-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="669d4-110">คุณสามารถสร้างธุรกรรมค่าใช้จ่ายที่ป้อนด้วยตนเองจากใบเสร็จรับเงินได้</span><span class="sxs-lookup"><span data-stu-id="669d4-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="669d4-111">แนบใบเสร็จรับเงินกับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="669d4-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="669d4-112">หากต้องการแนบใบเสร็จรับเงินที่มีธุรกรรมบัตรเครดิตโดยอัตโนมัติเมื่อสร้างรายงานค่าใช้จ่าย ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="669d4-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="669d4-113">เปิดพื้นที่ทำงาน **การจัดการค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="669d4-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="669d4-114">บนแท็บ **ใบเสร็จรับเงิน** ตรวจสอบว่ามีใบเสร็จรับเงินที่ไม่ได้แนบอยู่</span><span class="sxs-lookup"><span data-stu-id="669d4-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="669d4-115">คุณยังสามารถอัปโหลดใบเสร็จรับเงินในแท็บ **รายรับ**</span><span class="sxs-lookup"><span data-stu-id="669d4-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="669d4-116">บนแท็บ **ค่าใช้จ่าย** ตรวจสอบว่ามีใบเสร็จรับเงินที่ไม่ได้แนบอยู่</span><span class="sxs-lookup"><span data-stu-id="669d4-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="669d4-117">โดยปกติ ผู้ดดูแลระบบค่าใช้จ่ายจะนำเข้าค่าใช้จ่ายเหล่านี้จากผู้ให้บริการบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="669d4-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="669d4-118">เลือก **รายงานค่าใช้จ่ายใหม่**</span><span class="sxs-lookup"><span data-stu-id="669d4-118">Select **New expense report**.</span></span> <span data-ttu-id="669d4-119">สังเกตว่าคุณสามารถรวมค่าใช้จ่ายและใบเสร็จรับเงินได้เช่นกันเดียวกับเมื่อคุณสร้างรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="669d4-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="669d4-120">หากคุณเพิ่มทั้งค่าใช้จ่ายและใบเสร็จรับเงิน การจับคู่ใบเสร็จรับเงินกับค่าใช้จ่ายโดยอัตโนมัติจะถูกทริกเกอร์</span><span class="sxs-lookup"><span data-stu-id="669d4-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="669d4-121">สร้างหรือจับคู่ใบเสร็จรับเงินกับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="669d4-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="669d4-122">หากต้องการสร้างค่าใช้จ่าย หรือจับคู่ค่าใช้จ่ายจากใบเสร็จรับเงิน ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="669d4-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="669d4-123">ในรายงานค่าใช้จ่าย บนแท็บ **ใบเสร็จรับเงิน** ให้แนบใบเสร็จรับเงินโดยการเลือก **เพิ่มใบเสร็จรับเงิน**</span><span class="sxs-lookup"><span data-stu-id="669d4-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="669d4-124">ใต้ภาพใบเสร็จรับเงินที่อัปโหลด โปรดสังเกตตัวเลือก **สร้าง** และ **จับคู่**</span><span class="sxs-lookup"><span data-stu-id="669d4-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="669d4-125">เลือก **สร้าง** เพื่อสร้างธุรกรรมค่าใช้จ่ายที่ป้อนด้วยตนเองและกรอกค่าที่ดึงออกมาจากใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="669d4-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="669d4-126">หากคุณเลือก **จับคู่** ระบบจะพยายามจับคู่ค่าใช้จ่ายที่มีอยู่กับใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="669d4-126">If you select **Match** , the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="669d4-127">การติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="669d4-127">Installation</span></span>

<span data-ttu-id="669d4-128">หากต้องการใช้ความสามารถของค่าใช้จ่ายขั้นสูงเหล่านี้ ให้ติดตั้ง Add-in ของ บริการจัดการค่าใช้จ่ายสำหรับ Microsoft Dynamics 365 Finance และเปิดคุณลักษณะในอินสแตนซ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="669d4-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="669d4-129">คุณสามารถเข้าถึง Add-in จากโครงการของคุณใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="669d4-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="669d4-130">ลงชื่อเข้าใช้ LCS และเปิดสภาพแวดล้อมที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="669d4-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="669d4-131">ไปที่ **รายละเอียดทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="669d4-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="669d4-132">เลือก **รักษา** หรือเลื่อนลงไปที่แท็บด่วน **Add-in ของสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="669d4-132">Select **Maintain** , or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="669d4-133">เลือก **ติดตั้ง Add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="669d4-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="669d4-134">เลือก **บริการจัดการค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="669d4-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="669d4-135">ปฏิบัติตามคู่มือการติดตั้ง และยอมรับข้อกำหนดและเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="669d4-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="669d4-136">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="669d4-136">Select **Install**.</span></span>

<span data-ttu-id="669d4-137">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** เปิดคุณลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="669d4-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="669d4-138">รายงานค่าใช้จ่ายที่สมมติขึ้น</span><span class="sxs-lookup"><span data-stu-id="669d4-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="669d4-139">จับคู่อัตโนมัติและสร้างค่าใช้จ่ายจากใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="669d4-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="669d4-140">เมื่อคุณเปิดคุณลักษณะเหล่านี้ การดำเนินการต่อไปนี้จะเกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="669d4-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="669d4-141">พื้นที่ทำงาน **การจัดการค่าใช้จ่าย** ที่มีอยู่จะถูกแทนที่ด้วยพื้นที่ทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="669d4-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="669d4-142">ระบบจะเพิ่มรายการเมนูใหม่สำหรับการมองเห็นฟิลด์ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="669d4-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="669d4-143">คุณยังสามารถเปิดเพจ **รายงานค่าใช้จ่าย** ของเดิมได้โดยไปที่ **การจัดการค่าใช้จ่าย > ค่าใช้จ่ายของฉัน > รายงานค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="669d4-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="669d4-144">เวิร์กโฟลว์และการอนุมัติใดๆ ยังคงนำคุณไปยังเพจรายงานค่าใช้จ่ายที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="669d4-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="669d4-145">ใบเสร็จรับเงินจะได้รับการดำเนินการผ่าน Microsoft Azure Cognitive Services และเมตาดาต้าจะถูกแยกและเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="669d4-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="669d4-146">มีการเพิ่มตัวเลือกที่ช่วยให้คุณสามารถสร้างรายงานค่าใช้จ่ายที่มีใบเสร็จรับเงินที่ไม่ได้แนบที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="669d4-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="669d4-147">ตัวเลือกที่เพิ่มลงในรายงานค่าใช้จ่ายช่วยให้คุณสามารถสร้างรายการค่าใช้จ่ายจากใบเสร็จรับเงิน หรือพยายามจับคู่ใบเสร็จรับเงินที่มีอยู่กับรายการค่าใช้จ่ายที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="669d4-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="669d4-148">คำถามที่ถามบ่อย</span><span class="sxs-lookup"><span data-stu-id="669d4-148">Frequently asked questions</span></span>

<span data-ttu-id="669d4-149">**Microsoft ใช้ข้อมูลของฉันสำหรับแบบจำลองหรือไม่**</span><span class="sxs-lookup"><span data-stu-id="669d4-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="669d4-150">ไม่ Microsoft สร้างแบบจำลองการเรียนรู้ของเครื่องทั่วไปสำหรับบริการประมวลผลใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="669d4-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="669d4-151">แบบจำลองนี้ไม่ได้ขึ้นอยู่กับใบเสร็จรับเงินที่คุณอัปโหลด</span><span class="sxs-lookup"><span data-stu-id="669d4-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="669d4-152">**คุณลักษณะนี้มีให้บริการและประมวลผลที่ไหน**</span><span class="sxs-lookup"><span data-stu-id="669d4-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="669d4-153">ปัจจุบัน รองรับในสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="669d4-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="669d4-154">**ใบเสร็จรับเงินของฉันไปที่ไหน**</span><span class="sxs-lookup"><span data-stu-id="669d4-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="669d4-155">Finance จะติดต่อ Cognitive Services เพื่อดึงข้อมูลภาคสนาม</span><span class="sxs-lookup"><span data-stu-id="669d4-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="669d4-156">Cognitive Services จะเก็บสำเนาใบเสร็จรับเงินของคุณไว้เป็นเวลา 24 ชั่วโมงในขณะที่มีการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="669d4-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="669d4-157">หลังจากการประมวลผลเสร็จสิ้น Cognitive Services จะลบใบเสร็จรับเงินออก</span><span class="sxs-lookup"><span data-stu-id="669d4-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="669d4-158">ใบเสร็จรับเงินยังคงเก็บไว้ใน Finance</span><span class="sxs-lookup"><span data-stu-id="669d4-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="669d4-159">สำหรับข้อมูลเพิ่มเติม โปรดดู [เปิดใช้งานการทำความเข้าใจใบเสร็จรับเงินด้วยความสามารถใหม่ของตัวรู้จำฟอร์ม](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)</span><span class="sxs-lookup"><span data-stu-id="669d4-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
