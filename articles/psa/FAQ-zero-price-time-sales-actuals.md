---
title: ทำไมราคาที่กำหนดค่าเริ่มต้นเป็นศูนย์ในการขายจริงในเวลา?
description: การแก้ปัญหาว่าทำไมราคากำหนดค่าเริ่มต้นเป็น 0 ในการขายจริงในเวลา
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 5f72e0db94392a35fee9fdcf2c4adb8a08feef13
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146236"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a><span data-ttu-id="2a31c-103">ทำไมราคาที่กำหนดค่าเริ่มต้นเป็นศูนย์ในการขายจริงในเวลา?</span><span class="sxs-lookup"><span data-stu-id="2a31c-103">Why is price defaulting to zero on time sales actuals?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2a31c-104">คำถามที่ถามบ่อยนี้ใช้กับรายการจริง ซึ่งคลาสธุรกรรมถูกกำหนดเป็นเวลา และชนิดของธุรกรรมเป็นยอดขายที่ยังไม่ได้เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="2a31c-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Unbilled Sales.</span></span> <span data-ttu-id="2a31c-105">การตรวจสอบสามรายการต่อไปนี้จะช่วยคุณในการแก้ปัญหาสาเหตุที่ราคา (อัตราที่เรียกเก็บเงิน) กำหนดค่าเริ่มต้นเป็น 0 ในการขายจริงในเวลา</span><span class="sxs-lookup"><span data-stu-id="2a31c-105">The following three checks will help you troubleshoot why price (bill rate) is defaulting to 0 on time sales actuals.</span></span>

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a><span data-ttu-id="2a31c-106">การตรวจสอบ 1: ระบุราคาตลาดของการขายสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="2a31c-106">Check 1: Identify the sales price list for the project</span></span>

<span data-ttu-id="2a31c-107">ค้นหาโครงการจากฟิลด์โครงการของมูลค่าที่แท้จริง และจากนั้น ไปที่หน้าโครงการ</span><span class="sxs-lookup"><span data-stu-id="2a31c-107">Find the project from the project field of the actual and go to the project page.</span></span> <span data-ttu-id="2a31c-108">จากนั้น ไปที่แท็บการขาย และกริดรายละเอียดการให้บริการตามสัญญาโครงการ คลิกที่ลิงค์ในฟิลด์สัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="2a31c-108">Then go to the Sales tab and on Project Contract lines grid, click on the link in the Project Contract field.</span></span> <span data-ttu-id="2a31c-109">หน้าสัญญาโครงการจะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="2a31c-109">The project Contract page will open.</span></span> <span data-ttu-id="2a31c-110">บนหน้าสัญญาโครงการ ไปยังแท็บโครงการราคาตลาดที่กาเครื่องหมาย ตรวจสอบว่ามีราคาตลาดอย่างน้อยหนึ่งรายการที่แนบมาที่นี่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="2a31c-110">On the Project Contract page, go to the Project Price Lists tab. Check if there is at least one price list attached here.</span></span> <span data-ttu-id="2a31c-111">ถ้าไม่มีราคาตลาดแนบอยู่ในกริดราคาตลาดของโครงการของสัญญาโครงการที่คุณได้แยกปัญหา</span><span class="sxs-lookup"><span data-stu-id="2a31c-111">If there is no price list attached in the Project Price Lists grid of the Project Contract you have isolated the problem.</span></span> <span data-ttu-id="2a31c-112">แนบราคาตลาดในกริดราคาตลาดของโครงการ</span><span class="sxs-lookup"><span data-stu-id="2a31c-112">Attach a price list to the Project Price lists grid.</span></span> <span data-ttu-id="2a31c-113">ราคาตลาดที่ได้รับอนุญาตให้ถูกแนบที่นี่ ควรมีฟิลด์บริบทในการตั้งค่าการขาย และฟิลด์สกุลเงินในราคาตลาดควรตรงกับฟิลด์สกุลเงินในสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="2a31c-113">The price lists allowed to be attached here should have the context field set to Sales and the currency field on the price list should match the currency field on the Project Contract.</span></span> <span data-ttu-id="2a31c-114">หลังจากที่คุณเสร็จสิ้นการทำการแก้ไขที่จำเป็น สร้างการป้อนข้อมูลเวลาใหม่ อนุมัติ และตรวจสอบว่าการขายจริงที่ยังไม่ได้เรียกเก็บเงินแสดงราคาที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="2a31c-114">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span> 

<span data-ttu-id="2a31c-115">ถ้าคุณมีราคาตลาดอย่างน้อยหนึ่งรายการที่แนบในกริดราคาตลาดของโครงการของสัญญาโครงการ ดำเนินการเช็คอินถัดไปในเอกสาร</span><span class="sxs-lookup"><span data-stu-id="2a31c-115">If you have one or more price lists attached in the Project Price Lists grid of the Project Contract, proceed to the next check in the document.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a><span data-ttu-id="2a31c-116">การตรวจสอบ 2: ราคาตลาดดๆ ที่ระบุข้างต้นถูกต้องสำหรับวันที่เฉพาะเจาะจงของการขายเวลาที่เกิดขึ้นจริงหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="2a31c-116">Check 2: Are any of the price lists identified above valid for the specific date of the time sales actual?</span></span>

<span data-ttu-id="2a31c-117">สำหรับ Project Service เพื่อพิจารณาราคาตลาดสำหรับราคาที่ตั้งค่าเริ่มต้น ราคาตลาดที่ควรจะใช้สำหรับวันที่ในการขายจริงในเวลา</span><span class="sxs-lookup"><span data-stu-id="2a31c-117">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time sales actual.</span></span> <span data-ttu-id="2a31c-118">ตรวจสอบรายการต่อไปนี้เพื่อดูว่า ราคาตลาดที่ระบุไว้ข้างต้นสามารถใช้ได้หรือไม่:</span><span class="sxs-lookup"><span data-stu-id="2a31c-118">Check the following to see if the price list(s) identified above are applicable:</span></span>
- <span data-ttu-id="2a31c-119">ตรวจสอบว่า วันที่เริ่มและสิ้นสุดบนแท็บทั่วไปสำหรับราคาตลาดที่แนบไม่ว่างเปล่าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2a31c-119">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="2a31c-120">ถ้าวันที่เริ่มต้นและสิ้นสุดในราคาตลาดที่ระบุไว้ข้างต้นคือ ว่างเปล่า คุณแยกปัญหาต่างหาก</span><span class="sxs-lookup"><span data-stu-id="2a31c-120">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="2a31c-121">ทำบันทึกย่อของฟิลด์วันที่เริ่มต้นของการขายจริงในเวลาของคุณ และตรวจสอบว่าราคาตลาดใดๆ ที่ระบุสามารถใช้ได้สำหรับวันนั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2a31c-121">Make a note of the start date field on your time sales actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="2a31c-122">ตัวอย่างเช่น วันที่ของการขายจริงในเวลาควรอยู่ภายในวันที่เริ่มต้นและวันที่สิ้นสุดในราคาตลาด</span><span class="sxs-lookup"><span data-stu-id="2a31c-122">For example, the date of the time sales actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="2a31c-123">ถ้าไม่มีราคาตลาดที่ครอบคลุมวันที่นั้นในการขายจริงในเวลา คุณได้แยกปัญหา</span><span class="sxs-lookup"><span data-stu-id="2a31c-123">If there is no price list that covers that date on the time sales actual, you have isolated the problem.</span></span> <span data-ttu-id="2a31c-124">ปรับเปลี่ยนวันที่เริ่มและสิ้นสุดของราคาตลาดเพื่อให้แน่ใจว่า ราคาตลาดครอบคลุมวันที่ของการขายจริงในเวลา</span><span class="sxs-lookup"><span data-stu-id="2a31c-124">Modify the start and end dates of the price list to ensure that the price list covers the date of the time sales actual.</span></span> 
    - <span data-ttu-id="2a31c-125">ถ้ามีราคาตลาดมากกว่าหนึ่งรายการที่ครอบคลุมวันที่ในการขายจริงในเวลา คุณได้แยกปัญหา</span><span class="sxs-lookup"><span data-stu-id="2a31c-125">If there is more than one price list that covers the date on the time sales actual, you have isolated the problem.</span></span> <span data-ttu-id="2a31c-126">คุณสามารถแก้ไขปัญหานี้ได้โดยการแก้ไขวันที่เริ่มต้นและสิ้นสุดของราคาตลาด เพื่อให้มีราคาตลาดเดียวเท่านั้นที่ครอบคลุมวันที่ของการขายจริงในเวลา</span><span class="sxs-lookup"><span data-stu-id="2a31c-126">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time sales actual.</span></span> 
    - <span data-ttu-id="2a31c-127">ถ้ามีราคาตลาดเดียวเท่านั้นที่ครอบคลุมวันที่ของการขายจริงในเวลา ไปที่การตรวจสอบ 3</span><span class="sxs-lookup"><span data-stu-id="2a31c-127">If there is only one price list that covers that date of the time sales actual, go to Check 3.</span></span>
<span data-ttu-id="2a31c-128">หลังจากที่คุณเสร็จสิ้นการทำการแก้ไขที่จำเป็น สร้างการป้อนข้อมูลเวลาใหม่ อนุมัติ และตรวจสอบว่าการขายจริงในเวลาแสดงราคาที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="2a31c-128">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time sales actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a><span data-ttu-id="2a31c-129">การตรวจสอบ 3: มีราคาในราคาตลาดสำหรับมิติการกำหนดราคาในการขายจริงในเวลาหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2a31c-129">Check 3: Is there a price in the price list for the pricing dimensions on the time sales actual?</span></span>

<span data-ttu-id="2a31c-130">ถ้าคุณได้ดำเนินการตรวจสอบ 1 และการตรวจสอบ 2 เสร็จสิ้นแล้ว ขณะนี้ คุณควรมีราคาตลาดเดียวเท่านั้นที่เกี่ยวข้องสำหรับวันที่ของการขายจริงในเวลา</span><span class="sxs-lookup"><span data-stu-id="2a31c-130">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time sales actual.</span></span> <span data-ttu-id="2a31c-131">เปิดราคาตลาดนี้ และนำทางไปยังแท็บราคาบทบาท ต้องแน่ใจว่ามีแถวในกริดสำหรับมิติการกำหนดราคาในการขายจริงในเวลา</span><span class="sxs-lookup"><span data-stu-id="2a31c-131">Open this Price List and navigate to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the Time sales actual.</span></span>

<span data-ttu-id="2a31c-132">ถ้าไม่มีแถวอยู่ในกริดราคาบทบาทสำหรับมิติการกำหนดราคาในการขายจริงในเวลา จากนั้น คุณได้แยกปัญหาต่างหาก</span><span class="sxs-lookup"><span data-stu-id="2a31c-132">If there is no row in the role price grid for the pricing dimensions on the time sales actual, then you have isolated the problem.</span></span> <span data-ttu-id="2a31c-133">สร้างแถวในกริดราคาบทบาทสำหรับมิติการกำหนดราคาในรายการจริงในเวลาของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a31c-133">Create a row in the Role prices grid for the pricing dimensions on your time sales actual.</span></span> <span data-ttu-id="2a31c-134">หลังจากที่เสร็จสิ้น สร้างการป้อนข้อมูลเวลาใหม่ อนุมัติ และตรวจสอบว่าการขายจริงในเวลาแสดงราคาที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="2a31c-134">Once this is done, recreate time entry, approve it, and verify that the time sales actual shows a valid price.</span></span>

<span data-ttu-id="2a31c-135">ถ้าคุณยังคงไม่เห็นราคาถูกต้องในการขายจริงในเวลาของคุณ หลังจากดำเนินการตรวจสอบสามรายการข้างต้น โปรดเข้าสู่ระบบตั๋วที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="2a31c-135">If you still don't see a valid price on your time sales actual after following the three checks above, please log a support ticket.</span></span> 

