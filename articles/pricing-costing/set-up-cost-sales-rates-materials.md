---
title: ตั้งค่าอัตราต้นทุนและการขายสำหรับวัสดุ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีตั้งค่าอัตราต้นทุนและการขายสำหรับวัสดุที่ใช้ในโครงการ
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3deea480222af00ee49a34bd49c7c951937323f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004779"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a><span data-ttu-id="697bc-103">ตั้งค่าอัตราต้นทุนและการขายสำหรับวัสดุ</span><span class="sxs-lookup"><span data-stu-id="697bc-103">Set up cost and sales rates for materials</span></span>

<span data-ttu-id="697bc-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="697bc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="697bc-105">คุณสามารถตั้งค่าราคาต้นทุนและราคาขายสำหรับผลิตภัณฑ์ใน Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="697bc-105">You can set up cost and sales prices for products in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="697bc-106">ราคาต้นทุนและราคาขายสำหรับผลิตภัณฑ์สามารถระบุได้ในสกุลเงินเดียวเท่านั้น ซึ่งต้องเป็นสกุลเงินในส่วนหัวของรายการราคา</span><span class="sxs-lookup"><span data-stu-id="697bc-106">Cost and sales prices for products can only be listed in one currency, which must be the currency on the price list header.</span></span>

<span data-ttu-id="697bc-107">ในการตั้งค่าอัตราต้นทุนและอัตราการขายสำหรับผลิตภัณฑ์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="697bc-107">To set up cost and sales rates for products, complete the following steps.</span></span> 

1. <span data-ttu-id="697bc-108">ไปที่ **การขาย** > **ลูกค้า** > **รายการราคา** และเลือก **ใหม่** เพื่อสร้างรายการราคาใหม่</span><span class="sxs-lookup"><span data-stu-id="697bc-108">Go to **Sales** > **Customers** > **Price Lists** and select **New** to create a new price list.</span></span> 
2. <span data-ttu-id="697bc-109">ใน **รายการในรายการราคา** บนเมนูตารางย่อย เลือก **รายการในรายการราคาใหม่**</span><span class="sxs-lookup"><span data-stu-id="697bc-109">On the **Price list items**, on the subgrid menu, select **New price list item**.</span></span> 
3. <span data-ttu-id="697bc-110">บนเพจ **สร้างด่วน** ให้ป้อนผลิตภัณฑ์และหน่วยที่คุณกำลังสร้างราคาใหม่</span><span class="sxs-lookup"><span data-stu-id="697bc-110">On the **Quick Create** page, enter the product and unit that you are creating the new price for.</span></span>

<span data-ttu-id="697bc-111">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีกำหนดราคาสำหรับสินค้าในแค็ตตาล็อก โปรดดู [ตั้งค่าการกำหนดราคาสำหรับผลิตภัณฑ์](/dynamics365/sales-enterprise/create-price-lists-price-list-items-define-pricing-products.md) และ [หลักของทศนิยมในสกุลเงินและการกำหนดราคา](/dynamics365/sales-enterprise/decimal-precision-currency-pricing.md)</span><span class="sxs-lookup"><span data-stu-id="697bc-111">For more information about how to define prices for catalog items, see [Setup pricing for products](/dynamics365/sales-enterprise/create-price-lists-price-list-items-define-pricing-products.md) and [Decimal precision in currency and pricing](/dynamics365/sales-enterprise/decimal-precision-currency-pricing.md).</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
