---
title: การเสนอราคา การกำหนดราคา และการเรียกเก็บเงินขั้นสูง
description: หัวข้อนี้จะแสดงข้อมูลเกี่ยวกับการเสนอราคา การเรียกเก็บเงิน และการกำหนดราคาใน Project Service Automation
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
ms.openlocfilehash: c4674aba1d152289c78a202f9da1f710e28f9960
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275246"
---
# <a name="advanced-quoting-pricing-and-billing-guide"></a><span data-ttu-id="c0d5c-103">คู่มือการเสนอราคาขั้นสูง การกำหนดราคา และการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="c0d5c-103">Advanced quoting, pricing, and billing guide</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c0d5c-104">ความสามารถในการค้นหาทรัพยากรที่ถูกต้องในเวลาที่เหมาะสม จองทรัพยากรเหล่านั้นในโครงการ และเก็บทรัพยากรที่ใช้ ช่วยให้องค์กรบรรลุเป้าหมายรายได้และเป้าหมายความพึงพอใจของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c0d5c-104">The ability to find the right resources at the right time, book those resources on projects, and keep resources utilized helps organizations meet revenue targets and customer satisfaction goals.</span></span> 

<span data-ttu-id="c0d5c-105">การเชื่อมโยง PDF ที่ก่อนหน้านี้ในหัวข้อนี้ได้ถูกเอาออกและมีการย้ายเนื้อหาไปยังหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c0d5c-105">The PDF link that was previously in this topic has been removed and the content has been moved to the following topics:</span></span>

- [<span data-ttu-id="c0d5c-106">การเสนอราคา การกำหนดราคา และการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="c0d5c-106">Quoting, pricing, and billing</span></span>](../quote-bill-price.md)
- [<span data-ttu-id="c0d5c-107">กระบวนการขาย</span><span class="sxs-lookup"><span data-stu-id="c0d5c-107">Sales processes</span></span>](../basic-sales-process.md)
- [<span data-ttu-id="c0d5c-108">ใบเสนอราคาและบรรทัดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="c0d5c-108">Quotes and quote lines</span></span>](../basic-quote-lines.md)
- [<span data-ttu-id="c0d5c-109">บรรทัดใบเสนอราคาตามโผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0d5c-109">Product-based quote lines</span></span>](../product-based-quote-lines.md)
- [<span data-ttu-id="c0d5c-110">การกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="c0d5c-110">Pricing</span></span>](../basic-pricing.md)
- [<span data-ttu-id="c0d5c-111">การกำหนดราคาแค็ตตาล็อกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0d5c-111">Product catalog pricing</span></span>](../product-catalog-pricing.md)
- [<span data-ttu-id="c0d5c-112">ธุรกรรมทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="c0d5c-112">Business transactions</span></span>](../basic-business-transactions.md)
- [<span data-ttu-id="c0d5c-113">การประมาณการ</span><span class="sxs-lookup"><span data-stu-id="c0d5c-113">Estimates</span></span>](../estimates.md)
- [<span data-ttu-id="c0d5c-114">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="c0d5c-114">Actuals</span></span>](../actuals.md)
- [<span data-ttu-id="c0d5c-115">การวิเคราะห์ใบเสนอราคาโครงการ</span><span class="sxs-lookup"><span data-stu-id="c0d5c-115">Analyzing project quotes</span></span>](../basic-analyzing-quotes.md)
- [<span data-ttu-id="c0d5c-116">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="c0d5c-116">Organizational units</span></span>](../advanced-organizational.md)
- [<span data-ttu-id="c0d5c-117">กลุ่มหน่วยและหน่วย</span><span class="sxs-lookup"><span data-stu-id="c0d5c-117">Unit groups and units</span></span>](../advanced-units.md)
- [<span data-ttu-id="c0d5c-118">สถานการณ์สกุลเงินที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="c0d5c-118">Multi-currency scenarios</span></span>](../advanced-currency.md)
- [<span data-ttu-id="c0d5c-119">ค่าจริงของการบันทึก</span><span class="sxs-lookup"><span data-stu-id="c0d5c-119">Recording actuals</span></span>](../advanced-actuals.md)

> [!NOTE]
> <span data-ttu-id="c0d5c-120">หัวข้อนี้จะถูกเอาออกในการปรับปรุงเอกสารในอนาคต</span><span class="sxs-lookup"><span data-stu-id="c0d5c-120">This topic will be removed in a future documentation update.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]