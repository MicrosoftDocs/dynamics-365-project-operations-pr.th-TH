---
title: คู่มือพื้นฐานของการเสนอราคา การกำหนดราคา และการเรียกเก็บเงิน
description: หัวข้อนี้ขะแสดงการเชื่อมโยงไปยังข้อมูลเกี่ยวกับการเสนอราคา การกำหนดราคา และการเรียกเก็บเงินขั้นพื้นฐานใน Project Service Automation
author: kfend
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 2/14/2019
ms.topic: article
ms.author: kfend
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: eb90c1ac2880dc07414276618a8259d17932b4a0
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132581"
---
# <a name="basic-guide-to-quoting-pricing-and-billing"></a><span data-ttu-id="c55c1-103">คู่มือพื้นฐานของการเสนอราคา การกำหนดราคา และการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="c55c1-103">Basic guide to quoting, pricing and billing</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c55c1-104">ความสามารถในการค้นหาทรัพยากรที่ถูกต้องในเวลาที่เหมาะสม จองทรัพยากรเหล่านั้นในโครงการ และเก็บทรัพยากรที่ใช้ ช่วยให้องค์กรบรรลุเป้าหมายรายได้และเป้าหมายความพึงพอใจของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c55c1-104">The ability to find the right resources at the right time, book those resources on projects, and keep resources utilized helps organizations meet revenue targets and customer satisfaction goals.</span></span> 

<span data-ttu-id="c55c1-105">การเชื่อมโยง PDF ที่ก่อนหน้านี้ในหัวข้อนี้ได้ถูกเอาออกและมีการย้ายเนื้อหาไปยังหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c55c1-105">The PDF link that was previously in this topic has been removed and the content has been moved to the following topics:</span></span>

- [<span data-ttu-id="c55c1-106">การเสนอราคา การกำหนดราคา และการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="c55c1-106">Quoting, pricing, and billing</span></span>](../quote-bill-price.md)
- [<span data-ttu-id="c55c1-107">กระบวนการขาย</span><span class="sxs-lookup"><span data-stu-id="c55c1-107">Sales processes</span></span>](../basic-sales-process.md)
- [<span data-ttu-id="c55c1-108">ใบเสนอราคาและบรรทัดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="c55c1-108">Quotes and quote lines</span></span>](../basic-quote-lines.md)
- [<span data-ttu-id="c55c1-109">บรรทัดใบเสนอราคาตามโผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c55c1-109">Product-based quote lines</span></span>](../product-based-quote-lines.md)
- [<span data-ttu-id="c55c1-110">การกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="c55c1-110">Pricing</span></span>](../basic-pricing.md)
- [<span data-ttu-id="c55c1-111">การกำหนดราคาแค็ตตาล็อกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c55c1-111">Product catalog pricing</span></span>](../product-catalog-pricing.md)
- [<span data-ttu-id="c55c1-112">ธุรกรรมทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="c55c1-112">Business transactions</span></span>](../basic-business-transactions.md)
- [<span data-ttu-id="c55c1-113">การประมาณการ</span><span class="sxs-lookup"><span data-stu-id="c55c1-113">Estimates</span></span>](../estimates.md)
- [<span data-ttu-id="c55c1-114">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="c55c1-114">Actuals</span></span>](../actuals.md)
- [<span data-ttu-id="c55c1-115">การวิเคราะห์ใบเสนอราคาโครงการ</span><span class="sxs-lookup"><span data-stu-id="c55c1-115">Analyzing project quotes</span></span>](../basic-analyzing-quotes.md)
- [<span data-ttu-id="c55c1-116">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="c55c1-116">Organizational units</span></span>](../advanced-organizational.md)
- [<span data-ttu-id="c55c1-117">กลุ่มหน่วยและหน่วย</span><span class="sxs-lookup"><span data-stu-id="c55c1-117">Unit groups and units</span></span>](../advanced-units.md)
- [<span data-ttu-id="c55c1-118">สถานการณ์สกุลเงินที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="c55c1-118">Multi-currency scenarios</span></span>](../advanced-currency.md)
- [<span data-ttu-id="c55c1-119">ค่าจริงของการบันทึก</span><span class="sxs-lookup"><span data-stu-id="c55c1-119">Recording actuals</span></span>](../advanced-actuals.md)

> [!NOTE]
> <span data-ttu-id="c55c1-120">หัวข้อนี้จะถูกเอาออกในการปรับปรุงเอกสารในอนาคต</span><span class="sxs-lookup"><span data-stu-id="c55c1-120">This topic will be removed in a future documentation update.</span></span> 
