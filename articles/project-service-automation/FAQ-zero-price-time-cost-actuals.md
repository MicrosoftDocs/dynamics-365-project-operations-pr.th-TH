---
title: ทำไมราคาที่กำหนดค่าเริ่มต้นเป็นศูนย์ในต้นทุนเวลาจริง?
description: การแก้ปัญหาว่าทำไมราคากำหนดค่าเริ่มต้นเป็น 0 ในต้นทุนจริงในเวลา
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: 597d75b7-fadf-4947-8d52-95425ff90324
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 448c6c0569a40e1d7cb133561435811ecedb4356
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756530"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="65581-103">ทำไมราคาที่กำหนดค่าเริ่มต้นเป็นศูนย์ในต้นทุนเวลาจริง?</span><span class="sxs-lookup"><span data-stu-id="65581-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="65581-104">คำถามที่ถามบ่อยนี้ใช้กับรายการจริง ที่ซึ่งคลาสธุรกรรมถูกกำหนดเป็นเวลา และชนิดของธุรกรรมเป็นต้นทุน</span><span class="sxs-lookup"><span data-stu-id="65581-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="65581-105">การตรวจสอบสามรายการต่อไปนี้จะช่วยคุณในการแก้ปัญหาสาเหตุที่ราคากำหนดค่าเริ่มต้นเป็น 0 ในต้นทุนจริงในเวลา</span><span class="sxs-lookup"><span data-stu-id="65581-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="65581-106">การตรวจสอบ 1: ระบุราคาต้นทุนสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="65581-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="65581-107">ค้นหาโครงการจากฟิลด์โครงการของมูลค่าที่แท้จริง และจากนั้น ไปที่หน้าโครงการ</span><span class="sxs-lookup"><span data-stu-id="65581-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="65581-108">คลิกที่การเชื่อมโยงฝ่ายทำสัญญาในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="65581-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="65581-109">บนหน้าหน่วยตามสัญญา ตรวจสอบว่า หน่วยตามสัญญามีราคาตลาดในกริดรายการราคาต้นทุนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="65581-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="65581-110">ถ้ามีราคาตลาดมากกว่าหนึ่งรายการ คุณได้แยกปัญหาต่างหาก</span><span class="sxs-lookup"><span data-stu-id="65581-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="65581-111">Project Service สนับสนุนเฉพาะราคาตลาดหนึ่งรายการต่อหน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="65581-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="65581-112">เอาราคาตลาดทั้งหมดออกจากเอนทิตีนี้ จนกระทั่งมีราคาตลาดหนึ่งรายการเท่านั้นที่แนบในกริดรายการราคาต้นทุนของหน่วยงาน</span><span class="sxs-lookup"><span data-stu-id="65581-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="65581-113">ถ้าไม่มีราคาตลาดที่แนบกับหน่วยงาน ทำบันทึกย่อของสกุลเงินของหน่วยงาน</span><span class="sxs-lookup"><span data-stu-id="65581-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="65581-114">ไปที่ Project Service และจากนั้นพารามิเตอร์ และเปิดแท็บราคาตลาด ตรวจสอบว่ามีราคาตลาดใดๆ ที่มีบริบทที่ตั้งค่าเป็นต้นทุนและสกุลเงินที่สอดคล้องกับสกุลเงินของหน่วยงาน</span><span class="sxs-lookup"><span data-stu-id="65581-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="65581-115">ถ้าไม่มีราคาตลาดที่ตรงกับเกณฑ์นั้น คุณแยกปัญหาต่างหาก</span><span class="sxs-lookup"><span data-stu-id="65581-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="65581-116">ตรวจสอบว่ามีราคาตลาดอย่างน้อยหนึ่งราคา ที่มีบริบทถูกตั้งค่าเป็นต้นทุน และที่สกุลเงินที่ตรงกับสกุลเงินของหน่วยงาน</span><span class="sxs-lookup"><span data-stu-id="65581-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="65581-117">ถ้ามีราคาตลาดมากกว่าหนึ่งรายการที่ตรงกับเงื่อนไขนั้น อ่านเอกสารนี้เพื่อทำการตรวจสอบเพิ่มเติมต่อไป</span><span class="sxs-lookup"><span data-stu-id="65581-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="65581-118">การตรวจสอบ 2: ราคาตลาดดๆ ที่ระบุข้างต้นถูกต้องสำหรับวันที่เฉพาะเจาะจงของของต้นทุนจริงในเวลา?</span><span class="sxs-lookup"><span data-stu-id="65581-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="65581-119">สำหรับ Project Service เพื่อพิจารณาราคาตลาดสำหรับราคาที่ตั้งค่าเริ่มต้น ราคาตลาดนั้นควรจะใช้สำหรับวันที่ในต้นทุนจริงในเวลา</span><span class="sxs-lookup"><span data-stu-id="65581-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="65581-120">ตรวจสอบรายการต่อไปนี้เพื่อดูว่า ราคาตลาดที่ระบุไว้ข้างต้นสามารถใช้ได้หรือไม่:</span><span class="sxs-lookup"><span data-stu-id="65581-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="65581-121">ตรวจสอบว่า วันที่เริ่มและสิ้นสุดบนแท็บทั่วไปสำหรับราคาตลาดที่แนบไม่ว่างเปล่าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="65581-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="65581-122">ถ้าวันที่เริ่มต้นและสิ้นสุดในราคาตลาดที่ระบุไว้ข้างต้นคือ ว่างเปล่า คุณแยกปัญหาต่างหาก</span><span class="sxs-lookup"><span data-stu-id="65581-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="65581-123">ทำบันทึกย่อของฟิลด์วันที่เริ่มต้นของต้นทุนจริงในเวลาของคุณ และตรวจสอบว่าราคาตลาดใดๆ ที่ระบุสามารถใช้ได้สำหรับวันนั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="65581-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="65581-124">ตัวอย่างเช่น วันที่ของการต้นทุนจริงในเวลาควรอยู่ภายในวันที่เริ่มต้นและวันที่สิ้นสุดในราคาตลาด</span><span class="sxs-lookup"><span data-stu-id="65581-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="65581-125">ถ้าไม่มีราคาตลาดที่ครอบคลุมวันที่นั้นในต้นทุนจริงในเวลา คุณได้แยกปัญหา</span><span class="sxs-lookup"><span data-stu-id="65581-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="65581-126">ปรับเปลี่ยนวันที่เริ่มและสิ้นสุดของราคาตลาดเพื่อให้แน่ใจว่า ราคาตลาดครอบคลุมวันที่ของการต้นทุนจริงในเวลา</span><span class="sxs-lookup"><span data-stu-id="65581-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="65581-127">ถ้ามีราคาตลาดมากกว่าหนึ่งรายการที่ครอบคลุมวันที่ในต้นทุนจริงในเวลา คุณได้แยกปัญหา</span><span class="sxs-lookup"><span data-stu-id="65581-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="65581-128">คุณสามารถแก้ไขปัญหานี้ได้โดยการแก้ไขวันที่เริ่มต้นและสิ้นสุดของราคาตลาด เพื่อให้มีราคาตลาดเดียวเท่านั้นที่ครอบคลุมวันที่ของต้นทุนจริงในเวลา</span><span class="sxs-lookup"><span data-stu-id="65581-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="65581-129">ถ้ามีราคาตลาดเดียวเท่านั้นที่ครอบคลุมวันที่ของต้นทุนจริงในเวลา ย้ายไปยังการตรวจสอบถัดไปในเอกสาร</span><span class="sxs-lookup"><span data-stu-id="65581-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="65581-130">หลังจากที่คุณเสร็จสิ้นการทำการแก้ไขที่จำเป็น สร้างการป้อนข้อมูลเวลาใหม่ อนุมัติ และตรวจสอบว่า ต้นทุนจริงในเวลาแสดงราคาที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="65581-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="65581-131">การตรวจสอบ 3: มีราคาในราคาตลาดสำหรับมิติการกำหนดราคาในต้นทุนจริงในเวลาหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="65581-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="65581-132">ถ้าคุณได้ดำเนินการตรวจสอบ 1 และการตรวจสอบ 2 เสร็จสิ้นแล้ว ขณะนี้ คุณควรมีราคาตลาดราคาเดียวเท่านั้นที่เกี่ยวข้องสำหรับวันที่ของต้นทุนจริงในเวลา</span><span class="sxs-lookup"><span data-stu-id="65581-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="65581-133">เปิดราคาตลาดนี้ และไปยังแท็บราคาบทบาท ต้องแน่ใจว่ามีแถวในกริดสำหรับมิติการกำหนดราคาในต้นทุนจริงในเวลา</span><span class="sxs-lookup"><span data-stu-id="65581-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="65581-134">ถ้าไม่มีไม่มีแถวในกริดราคาบทบาทสำหรับมิติการกำหนดราคาในต้นทุนจริงในเวลา จากนั้นคุณแยกปัญหาต่างหาก</span><span class="sxs-lookup"><span data-stu-id="65581-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="65581-135">สร้างแถวในกริดราคาบทบาทสำหรับมิติการกำหนดราคาในต้นทุนจริงในเวลาของคุณ</span><span class="sxs-lookup"><span data-stu-id="65581-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="65581-136">หลังจากที่เสร็จสิ้น สร้างการป้อนข้อมูลเวลาใหม่ อนุมัติ และตรวจสอบว่าต้นทุนจริงในเวลาแสดงราคาที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="65581-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="65581-137">ถ้าคุณยังคงไม่เห็นราคาถูกต้องในต้นทุนจริงในเวลาของคุณ หลังจากที่คุณได้ดำเนินการตรวจสอบสามรายการข้างต้น โปรดเข้าสู่ระบบตั๋วที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="65581-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



