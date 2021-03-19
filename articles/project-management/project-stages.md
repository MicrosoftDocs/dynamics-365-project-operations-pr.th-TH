---
title: ลำดับขั้นของโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับขั้นตอนของโครงการที่มีอยู่ใน Microsoft Dynamics Project Operations
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a5c695e0cd39f8a222e719cc6c9ffe984fe80b07
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286811"
---
# <a name="project-stages"></a><span data-ttu-id="6cf10-103">ลำดับขั้นของโครงการ</span><span class="sxs-lookup"><span data-stu-id="6cf10-103">Project stages</span></span>

<span data-ttu-id="6cf10-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="6cf10-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6cf10-105">ขั้นตอนของโครงการจะถูกออกแบบเพื่อสะท้อนให้เห็นถึงสถานะของโครงการขณะดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="6cf10-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="6cf10-106">การปรับแต่งสามารถใช้เพื่ออัปเดตขั้นตอนโดยอัตโนมัติด้วยส่วนขยายโฟลว์กระบวนการทางธุรกิจ Power Automate หรือปลั๊กอิน</span><span class="sxs-lookup"><span data-stu-id="6cf10-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="6cf10-107">ขั้นตอนต่อไปนี้ถูกกำหนดในโฟลว์กระบวนการธุรกิจเริ่มต้น:</span><span class="sxs-lookup"><span data-stu-id="6cf10-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="6cf10-108">ใหม่</span><span class="sxs-lookup"><span data-stu-id="6cf10-108">New</span></span>
- <span data-ttu-id="6cf10-109">ใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6cf10-109">Quote</span></span>
- <span data-ttu-id="6cf10-110">แผน</span><span class="sxs-lookup"><span data-stu-id="6cf10-110">Plan</span></span>
- <span data-ttu-id="6cf10-111">ส่งมอบ</span><span class="sxs-lookup"><span data-stu-id="6cf10-111">Deliver</span></span>
- <span data-ttu-id="6cf10-112">ทำให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6cf10-112">Complete</span></span>
- <span data-ttu-id="6cf10-113">ปิด</span><span class="sxs-lookup"><span data-stu-id="6cf10-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="6cf10-114">ใหม่</span><span class="sxs-lookup"><span data-stu-id="6cf10-114">New</span></span>

<span data-ttu-id="6cf10-115">เมื่อคุณสร้างโครงการ ลำดับขั้นของโครงการจะถูกตั้งค่าเป็น **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6cf10-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="6cf10-116">ถ้าโครงการถูกสร้างจากแม่แบบ อาจมีข้อมูลหมายกำหนดการให้บริการ การประเมินและทีมงาน</span><span class="sxs-lookup"><span data-stu-id="6cf10-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="6cf10-117">มิฉะนั้น จะเป็นโครงร่างของโครงการ และต้องป้อนส่วนประกอบที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="6cf10-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="6cf10-118">ใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6cf10-118">Quote</span></span>

<span data-ttu-id="6cf10-119">เมื่อคุณเชื่อมโยงโครงการกับใบเสนอราคา หรือเมื่อคุณสร้างโครงการจากใบเสนอราคา ลำดับขั้นของโครงการถูกตั้งค่าเป็น **ใบเสนอราคา** และการประเมินวันเริ่มต้นและสิ้นสุดจะถูกอัพเดต</span><span class="sxs-lookup"><span data-stu-id="6cf10-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="6cf10-120">เมื่อโครงการอยู่ในลำดับขั้น **ใบเสนอราคา** แท็บ **การขาย** บนหน้า **เอนทิตีโครงการ** จะแสดงรายละเอียดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6cf10-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="6cf10-121">แผน</span><span class="sxs-lookup"><span data-stu-id="6cf10-121">Plan</span></span>

<span data-ttu-id="6cf10-122">เมื่อคุณชนะใบเสนอราคาที่เกี่ยวข้องกับโครงการ และโครงการถูกย้ายไปที่ขั้นตอน **สัญญา** ลำดับขั้นโครงการถูกปรับปรุงตาม **แผน**</span><span class="sxs-lookup"><span data-stu-id="6cf10-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="6cf10-123">เมื่อโครงการอยู่ในลำดับขั้น **แผน** หน้า **เอนทิตีโครงการ** จะแสดงรายละเอียดสัญญา</span><span class="sxs-lookup"><span data-stu-id="6cf10-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="6cf10-124">นำเสนอ</span><span class="sxs-lookup"><span data-stu-id="6cf10-124">Deliver</span></span>

<span data-ttu-id="6cf10-125">เมื่อแผนโครงการเสร็จสมบูรณ์ และคุณพร้อมที่จะเริ่มต้นโครงการ ผู้จัดการโครงการควรปรับปรุงขั้นตอนโครงการเป็น **นำเสนอ** เพื่อแสดงว่าโครงการได้เริ่มต้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="6cf10-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="6cf10-126">ทำให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6cf10-126">Complete</span></span> 

<span data-ttu-id="6cf10-127">เมื่องานสำหรับโครงการเสร็จสมบูรณ์แล้ว ผู้จัดการโครงการจะสามารถปรับปรุงขั้นตอนเป็น **เสร็จสมบูรณ์** ได้</span><span class="sxs-lookup"><span data-stu-id="6cf10-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="6cf10-128">โดยการปรับปรุงขั้นตอนโครงการเป็น **เสร็จสมบูรณ์** ผู้จัดการโครงการระบุว่างานเป็น 100 เปอร์เซ็นต์เสร็จสมบูรณ์ แต่ว่าโครงการจะถูกเปิดไว้ เพื่อให้สามารถบันทึกเวลาที่ค้างอยู่หรือรายการค่าใช้จ่ายใดๆ ได้</span><span class="sxs-lookup"><span data-stu-id="6cf10-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="6cf10-129">ปิด</span><span class="sxs-lookup"><span data-stu-id="6cf10-129">Close</span></span>

<span data-ttu-id="6cf10-130">เมื่อธุรกรรมทั้งหมดถูกบันทึกสำหรับโครงการแล้ว ผู้จัดการโครงการจะสามารถปรับปรุงขั้นตอนเป็น **ปิด** ได้</span><span class="sxs-lookup"><span data-stu-id="6cf10-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="6cf10-131">ในจุดนั้น ไม่มีธุรกรรมใดที่สามารถบันทึก และโครงการจะถูกตั้งค่าเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="6cf10-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]