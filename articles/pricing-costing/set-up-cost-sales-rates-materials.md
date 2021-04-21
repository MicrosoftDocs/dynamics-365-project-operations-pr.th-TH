---
title: ตั้งค่าอัตราต้นทุนและการขายสำหรับวัสดุ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีตั้งค่าอัตราต้นทุนและการขายสำหรับวัสดุที่ใช้ในโครงการ
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 05abefcec5c64632d00e2317107fe7a84ded4908
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877810"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a><span data-ttu-id="bbb8f-103">ตั้งค่าอัตราต้นทุนและการขายสำหรับวัสดุ</span><span class="sxs-lookup"><span data-stu-id="bbb8f-103">Set up cost and sales rates for materials</span></span>

<span data-ttu-id="bbb8f-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="bbb8f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bbb8f-105">คุณสามารถตั้งค่าราคาต้นทุนและราคาขายสำหรับผลิตภัณฑ์ใน Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="bbb8f-105">You can set up cost and sales prices for products in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="bbb8f-106">ราคาต้นทุนและราคาขายสำหรับผลิตภัณฑ์สามารถระบุได้ในสกุลเงินเดียวเท่านั้น ซึ่งต้องเป็นสกุลเงินในส่วนหัวของรายการราคา</span><span class="sxs-lookup"><span data-stu-id="bbb8f-106">Cost and sales prices for products can only be listed in one currency, which must be the currency on the price list header.</span></span>

<span data-ttu-id="bbb8f-107">ในการตั้งค่าอัตราต้นทุนและอัตราการขายสำหรับผลิตภัณฑ์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="bbb8f-107">To set up cost and sales rates for products, complete the following steps.</span></span> 

1. <span data-ttu-id="bbb8f-108">ไปที่ **การขาย** > **ลูกค้า** > **รายการราคา** และเลือก **ใหม่** เพื่อสร้างรายการราคาใหม่</span><span class="sxs-lookup"><span data-stu-id="bbb8f-108">Go to **Sales** > **Customers** > **Price Lists** and select **New** to create a new price list.</span></span> 
2. <span data-ttu-id="bbb8f-109">ใน **รายการในรายการราคา** บนเมนูตารางย่อย เลือก **รายการในรายการราคาใหม่**</span><span class="sxs-lookup"><span data-stu-id="bbb8f-109">On the **Price list items**, on the subgrid menu, select **New price list item**.</span></span> 
3. <span data-ttu-id="bbb8f-110">บนเพจ **สร้างด่วน** ให้ป้อนผลิตภัณฑ์และหน่วยที่คุณกำลังสร้างราคาใหม่</span><span class="sxs-lookup"><span data-stu-id="bbb8f-110">On the **Quick Create** page, enter the product and unit that you are creating the new price for.</span></span>

<span data-ttu-id="bbb8f-111">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีกำหนดราคาสำหรับสินค้าในแค็ตตาล็อก โปรดดู [ตั้งค่าการกำหนดราคาสำหรับผลิตภัณฑ์](https://docs.microsoft.com/dynamics365/sales-enterprise/create-price-lists-price-list-items-define-pricing-products) และ [หลักของทศนิยมในสกุลเงินและการกำหนดราคา](https://docs.microsoft.com/dynamics365/sales-enterprise/decimal-precision-currency-pricing)</span><span class="sxs-lookup"><span data-stu-id="bbb8f-111">For more information about how to define prices for catalog items, see [Setup pricing for products](https://docs.microsoft.com/dynamics365/sales-enterprise/create-price-lists-price-list-items-define-pricing-products) and [Decimal precision in currency and pricing](https://docs.microsoft.com/dynamics365/sales-enterprise/decimal-precision-currency-pricing).</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
