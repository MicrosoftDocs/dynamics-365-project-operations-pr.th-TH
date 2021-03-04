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
ms.openlocfilehash: ef2698b52bd5a89a10ff0be6aff3d98e6917e95c
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149206"
---
# <a name="advanced-quoting-pricing-and-billing-guide"></a><span data-ttu-id="9abe3-103">คู่มือการเสนอราคาขั้นสูง การกำหนดราคา และการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="9abe3-103">Advanced quoting, pricing, and billing guide</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9abe3-104">ความสามารถในการค้นหาทรัพยากรที่ถูกต้องในเวลาที่เหมาะสม จองทรัพยากรเหล่านั้นในโครงการ และเก็บทรัพยากรที่ใช้ ช่วยให้องค์กรบรรลุเป้าหมายรายได้และเป้าหมายความพึงพอใจของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9abe3-104">The ability to find the right resources at the right time, book those resources on projects, and keep resources utilized helps organizations meet revenue targets and customer satisfaction goals.</span></span> 

<span data-ttu-id="9abe3-105">การเชื่อมโยง PDF ที่ก่อนหน้านี้ในหัวข้อนี้ได้ถูกเอาออกและมีการย้ายเนื้อหาไปยังหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9abe3-105">The PDF link that was previously in this topic has been removed and the content has been moved to the following topics:</span></span>

- [<span data-ttu-id="9abe3-106">การเสนอราคา การกำหนดราคา และการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="9abe3-106">Quoting, pricing, and billing</span></span>](../quote-bill-price.md)
- [<span data-ttu-id="9abe3-107">กระบวนการขาย</span><span class="sxs-lookup"><span data-stu-id="9abe3-107">Sales processes</span></span>](../basic-sales-process.md)
- [<span data-ttu-id="9abe3-108">ใบเสนอราคาและบรรทัดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="9abe3-108">Quotes and quote lines</span></span>](../basic-quote-lines.md)
- [<span data-ttu-id="9abe3-109">บรรทัดใบเสนอราคาตามโผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9abe3-109">Product-based quote lines</span></span>](../product-based-quote-lines.md)
- [<span data-ttu-id="9abe3-110">การกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="9abe3-110">Pricing</span></span>](../basic-pricing.md)
- [<span data-ttu-id="9abe3-111">การกำหนดราคาแค็ตตาล็อกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9abe3-111">Product catalog pricing</span></span>](../product-catalog-pricing.md)
- [<span data-ttu-id="9abe3-112">ธุรกรรมทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="9abe3-112">Business transactions</span></span>](../basic-business-transactions.md)
- [<span data-ttu-id="9abe3-113">การประมาณการ</span><span class="sxs-lookup"><span data-stu-id="9abe3-113">Estimates</span></span>](../estimates.md)
- [<span data-ttu-id="9abe3-114">ตามจริง</span><span class="sxs-lookup"><span data-stu-id="9abe3-114">Actuals</span></span>](../actuals.md)
- [<span data-ttu-id="9abe3-115">การวิเคราะห์ใบเสนอราคาโครงการ</span><span class="sxs-lookup"><span data-stu-id="9abe3-115">Analyzing project quotes</span></span>](../basic-analyzing-quotes.md)
- [<span data-ttu-id="9abe3-116">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="9abe3-116">Organizational units</span></span>](../advanced-organizational.md)
- [<span data-ttu-id="9abe3-117">กลุ่มหน่วยและหน่วย</span><span class="sxs-lookup"><span data-stu-id="9abe3-117">Unit groups and units</span></span>](../advanced-units.md)
- [<span data-ttu-id="9abe3-118">สถานการณ์สกุลเงินที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="9abe3-118">Multi-currency scenarios</span></span>](../advanced-currency.md)
- [<span data-ttu-id="9abe3-119">ค่าจริงของการบันทึก</span><span class="sxs-lookup"><span data-stu-id="9abe3-119">Recording actuals</span></span>](../advanced-actuals.md)

> [!NOTE]
> <span data-ttu-id="9abe3-120">หัวข้อนี้จะถูกเอาออกในการปรับปรุงเอกสารในอนาคต</span><span class="sxs-lookup"><span data-stu-id="9abe3-120">This topic will be removed in a future documentation update.</span></span> 
