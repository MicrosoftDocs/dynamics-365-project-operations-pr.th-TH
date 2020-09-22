---
title: ลำดับขั้นของโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับลำดับขั้นของโครงการ
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756400"
---
# <a name="project-stages"></a><span data-ttu-id="dfee9-103">ลำดับขั้นของโครงการ</span><span class="sxs-lookup"><span data-stu-id="dfee9-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="dfee9-104">ขั้นตอนของโครงการจะถูกปรับปรุงเพื่อสะท้อนให้เห็นถึงสถานะของโครงการขณะดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="dfee9-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="dfee9-105">โฟลว์กระบวนการธุรกิจค่าเริ่มต้นปรับปรุงบางขั้นตอนของโครงการโดยอัตโนมัติ ในขณะที่อื่นๆ ได้รับการปรับปรุงโดยผู้จัดการโครงการเอง</span><span class="sxs-lookup"><span data-stu-id="dfee9-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="dfee9-106">ขั้นตอนต่อไปนี้ถูกกำหนดใน BPF เริ่มต้น:</span><span class="sxs-lookup"><span data-stu-id="dfee9-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="dfee9-107">สร้าง</span><span class="sxs-lookup"><span data-stu-id="dfee9-107">New</span></span>
- <span data-ttu-id="dfee9-108">ใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="dfee9-108">Quote</span></span>
- <span data-ttu-id="dfee9-109">แผน</span><span class="sxs-lookup"><span data-stu-id="dfee9-109">Plan</span></span>
- <span data-ttu-id="dfee9-110">นำเสนอ</span><span class="sxs-lookup"><span data-stu-id="dfee9-110">Deliver</span></span>
- <span data-ttu-id="dfee9-111">ทำให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="dfee9-111">Complete</span></span>
- <span data-ttu-id="dfee9-112">ปิด</span><span class="sxs-lookup"><span data-stu-id="dfee9-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="dfee9-113">สร้าง</span><span class="sxs-lookup"><span data-stu-id="dfee9-113">New</span></span>

<span data-ttu-id="dfee9-114">เมื่อคุณสร้างโครงการ ลำดับขั้นของโครงการจะถูกตั้งค่าเป็น **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="dfee9-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="dfee9-115">ถ้าโครงการถูกสร้างจากแม่แบบ อาจมีข้อมูลหมายกำหนดการให้บริการ การประเมินและทีมงาน</span><span class="sxs-lookup"><span data-stu-id="dfee9-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="dfee9-116">มิฉะนั้น จะเป็นเพียงโครงร่างของโครงการ และต้องป้อนส่วนประกอบที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="dfee9-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="dfee9-117">ใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="dfee9-117">Quote</span></span>

<span data-ttu-id="dfee9-118">เมื่อคุณเชื่อมโยงโครงการกับใบเสนอราคา หรือเมื่อคุณสร้างโครงการจากใบเสนอราคา ลำดับขั้นของโครงการถูกตั้งค่าเป็น **ใบเสนอราคา**และการประเมินวันเริ่มต้นและสิ้นสุดจะถูกอัพเดต</span><span class="sxs-lookup"><span data-stu-id="dfee9-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="dfee9-119">เมื่อโครงการอยู่ในลำดับขั้น **ใบเสนอราคา** แท็บ **การขาย** บนหน้า **เอนทิตีโครงการ** จะแสดงรายละเอียดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="dfee9-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="dfee9-120">แผน</span><span class="sxs-lookup"><span data-stu-id="dfee9-120">Plan</span></span>

<span data-ttu-id="dfee9-121">เมื่อคุณชนะใบเสนอราคาที่เกี่ยวข้องกับโครงการ และโครงการถูกย้ายไปที่ขั้นตอน **สัญญา** ลำดับขั้นโครงการถูกปรับปรุงตาม **แผน**</span><span class="sxs-lookup"><span data-stu-id="dfee9-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="dfee9-122">เมื่อโครงการอยู่ในลำดับขั้น **แผน** หน้า **เอนทิตีโครงการ** จะแสดงรายละเอียดสัญญา</span><span class="sxs-lookup"><span data-stu-id="dfee9-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="dfee9-123">นำเสนอ</span><span class="sxs-lookup"><span data-stu-id="dfee9-123">Deliver</span></span>

<span data-ttu-id="dfee9-124">เมื่อแผนโครงการเสร็จสมบูรณ์ และคุณพร้อมที่จะเริ่มต้นโครงการ ผู้จัดการโครงการควรปรับปรุงขั้นตอนโครงการเป็น **นำเสนอ** เพื่อแสดงว่าโครงการได้เริ่มต้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="dfee9-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="dfee9-125">ทำให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="dfee9-125">Complete</span></span> 

<span data-ttu-id="dfee9-126">เมื่องานสำหรับโครงการเสร็จสมบูรณ์แล้ว ผู้จัดการโครงการจะสามารถปรับปรุงขั้นตอนเป็น **เสร็จสมบูรณ์** ได้</span><span class="sxs-lookup"><span data-stu-id="dfee9-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="dfee9-127">โดยการปรับปรุงขั้นตอนโครงการเป็น **เสร็จสมบูรณ์** ผู้จัดการโครงการระบุว่างานเป็น 100 เปอร์เซ็นต์เสร็จสมบูรณ์ แต่ว่าโครงการจะถูกเปิดไว้ เพื่อให้สามารถบันทึกเวลาที่ค้างอยู่หรือรายการค่าใช้จ่ายใดๆ ได้</span><span class="sxs-lookup"><span data-stu-id="dfee9-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="dfee9-128">ปิด</span><span class="sxs-lookup"><span data-stu-id="dfee9-128">Close</span></span>

<span data-ttu-id="dfee9-129">เมื่อธุรกรรมทั้งหมดถูกบันทึกสำหรับโครงการแล้ว ผู้จัดการโครงการจะสามารถปรับปรุงขั้นตอนเป็น **ปิด** ได้</span><span class="sxs-lookup"><span data-stu-id="dfee9-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="dfee9-130">ในจุดนั้น ไม่มีธุรกรรมใดที่สามารถบันทึก และโครงการจะถูกตั้งค่าเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="dfee9-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
