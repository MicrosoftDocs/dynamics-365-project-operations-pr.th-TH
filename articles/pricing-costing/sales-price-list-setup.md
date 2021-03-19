---
title: ตั้งค่ารายการราคาสำหรับการขาย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับรายการราคาสำหรับการขายในการกำหนดราคาของโครงการ
author: rumant
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
ms.openlocfilehash: 05b1c13540e902975eee7379276cf394d9fc5743
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275471"
---
# <a name="set-up-a-sales-price-list"></a><span data-ttu-id="9dcfe-103">ตั้งค่ารายการราคาสำหรับการขาย</span><span class="sxs-lookup"><span data-stu-id="9dcfe-103">Set up a sales price list</span></span>

<span data-ttu-id="9dcfe-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="9dcfe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9dcfe-105">สำหรับใบเสนอราคาและสัญญาราคาโครงการ รายการราคาโครงการมีรูปแบบการแทนที่ราคาที่แตกต่างจากรายการราคาผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9dcfe-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="9dcfe-106">บนรายการใบเสนอราคาตามแค็ตตาล็อกผลิตภัณฑ์ คุณสามารถแทนที่ราคาให้กับบทบาทและประเภทโดยตรงบนรายการใบเสนอราคา เนื่องจากแต่ละรายการใบเสนอราคาชี้ไปที่สินค้าในแค็ตตาล็อกหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="9dcfe-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="9dcfe-107">อย่างไรก็ตามในรายการใบเสนอราคาตามโครงการ คุณไม่สามารถแทนที่ราคาให้กับบทบาทและประเภทโดยตรงบนรายการใบเสนอราคาได้</span><span class="sxs-lookup"><span data-stu-id="9dcfe-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="9dcfe-108">คุณสามารถใช้รายการราคาของโครงการเพื่อทำงานกับรูปแบบการแทนที่ที่แตกต่างกันสองรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="9dcfe-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="9dcfe-109">เราขอแนะนำให้คุณมีรายการราคาที่แยกต่างหากสำหรับทรัพยากรโครงการและสินค้าในแค็ตตาล็อกของคุณ เนื่องจากความแตกต่างของลักษณะการทำงานระหว่างสองอย่างนี้เมื่อคุณแทนที่การกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="9dcfe-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="9dcfe-110">แต่ละเอนทิตีต่อไปนี้สามารถมีราคาขายที่เกี่ยวข้องหนึ่งรายการขึ้นไปสำหรับการกำหนดราคาโครงการ:</span><span class="sxs-lookup"><span data-stu-id="9dcfe-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="9dcfe-111">ลูกค้า (บัญชี)</span><span class="sxs-lookup"><span data-stu-id="9dcfe-111">Customer (account)</span></span> 
- <span data-ttu-id="9dcfe-112">โอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="9dcfe-112">Opportunity</span></span> 
- <span data-ttu-id="9dcfe-113">ใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="9dcfe-113">Quote</span></span> 
- <span data-ttu-id="9dcfe-114">สัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="9dcfe-114">Project Contract</span></span>

<span data-ttu-id="9dcfe-115">การเชื่อมโยงของเอนทิตีเหล่านี้กับรายการราคาจะถูกระบุโดยรายการราคาของโครงการ</span><span class="sxs-lookup"><span data-stu-id="9dcfe-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="9dcfe-116">คุณสามารถเชื่อมโยงรายการราคาอย่างน้อยหนึ่งรายการกับเอนทิตีการขายของลูกค้า โอกาสทางการขาย ใบเสนอราคา และสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="9dcfe-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="9dcfe-117">รายการราคาเริ่มต้นของโครงการจะไม่ถูกป้อนโดยอัตโนมัติบนเรกคอร์ดลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9dcfe-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="9dcfe-118">อย่างไรก็ตามคุณสามารถแนบรายการราคาโครงการกับเรกคอร์ดลูกค้าได้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9dcfe-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="9dcfe-119">อย่างไรก็ตามคุณควรแนบรายการราคาโครงการด้วยตนเองเมื่อคุณมีข้อตกลงการกำหนดราคาแบบกำหนดเองกับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9dcfe-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="9dcfe-120">เมื่อรายการราคาของโครงการแนบอยู่กับเอนทิตีการขาย จะมีการตรวจสอบข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9dcfe-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="9dcfe-121">รายการราคาที่แสดงเป็นบริบทของ **การขาย**</span><span class="sxs-lookup"><span data-stu-id="9dcfe-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="9dcfe-122">สกุลเงินรายการราคาต้องตรงกับสกุลเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9dcfe-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="9dcfe-123">ในสัญญาโครงการ จะมีการใช้ลำดับความสำคัญต่อไปนี้ในการตั้งค่ารายการราคาของโครงการที่เกี่ยวข้องโดยอัตโนมัติ:</span><span class="sxs-lookup"><span data-stu-id="9dcfe-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="9dcfe-124">ใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="9dcfe-124">Quote</span></span>
2. <span data-ttu-id="9dcfe-125">โอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="9dcfe-125">Opportunity</span></span>
3. <span data-ttu-id="9dcfe-126">ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9dcfe-126">Customer</span></span> 
4. <span data-ttu-id="9dcfe-127">การตั้งค่าส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="9dcfe-127">Global settings</span></span> 

<span data-ttu-id="9dcfe-128">เมื่อรายการราคาของโครงการถูกป้อนโดยค่าเริ่มต้น ระบบจะตรวจสอบว่าสกุลเงินตรงกับสกุลเงินของลูกค้า และรายการราคาเริ่มต้นที่ได้ป้อนไว้มีบริบทของ **การขาย**</span><span class="sxs-lookup"><span data-stu-id="9dcfe-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="9dcfe-129">คุณสามารถเชื่อมโยงรายการราคาของหลายโครงการกับเอนทิตีลูกค้า โอกาสทางการขาย ใบเสนอราคา และสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="9dcfe-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="9dcfe-130">ความสามารถนี้สนับสนุนราคาเริ่มต้นเฉพาะวันที่สำหรับสัญญาโครงการที่ใช้เวลานาน ซึ่งคุณอาจต้องใช้รายการราคามากกว่าหนึ่งรายการสำหรับการปรับปรุงราคาที่เกิดขึ้นเนื่องจากภาวะเงินเฟ้อ</span><span class="sxs-lookup"><span data-stu-id="9dcfe-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="9dcfe-131">อย่างไรก็ตามถ้ารายการราคาที่คุณเชื่อมโยงกับเอนทิตีลูกค้า โอกาสทางการขาย การเสนอราคา หรือสัญญาโครงการ มีวันที่ทับซ้อนกัน ส่งผลให้ราคาเริ่มต้นอาจไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="9dcfe-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="9dcfe-132">ดังนั้นคุณควรตรวจสอบให้แน่ใจว่ารายการราคาของโครงการที่มีวันที่ทับซ้อนกันไม่ได้มีผลเชื่อมโยงกับเอนทิตีเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="9dcfe-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]