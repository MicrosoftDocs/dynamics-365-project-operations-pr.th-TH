---
title: รายการโอกาสทางการขายตามผลิตภัณฑ์ - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับข้อมูลเกี่ยวกับการแสดงรายการโอกาสทางการขายตามโครงการใน Project Operations
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7865da682ae607f017bf59ce1ae1addc9fefa60b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994519"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="3ab75-103">รายการโอกาสทางการขายตามผลิตภัณฑ์ - Lite</span><span class="sxs-lookup"><span data-stu-id="3ab75-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="3ab75-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="3ab75-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3ab75-105">รายการโอกาสทางการขายตามผลิตภัณฑ์คือการแสดงรายการในโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="3ab75-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="3ab75-106">สินค้าในรายการที่แตกต่างกันเหล่านี้อยู่ในใบแจ้งหนี้ในตอนท้ายที่ให้ไว้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3ab75-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="3ab75-107">ใบแจ้งหนี้ไม่รวมบริการเพิ่มเติมอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="3ab75-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="3ab75-108">การใช้จ่ายและการบริโภคที่เกี่ยวข้องจะไม่ติดตามงานของโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3ab75-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="3ab75-109">รายการตามผลิตภัณฑ์อาจเป็นสินค้าในแค็ตตาล็อกหรือผลิตภัณฑ์ที่เขียนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="3ab75-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="3ab75-110">ฟังก์ชันส่วนใหญ่ในรายการผลิตภัณฑ์ตามโอกาสทางการขายเป็นไปตามฟังก์ชันที่จัดเตรียมโดยแอปพลิเคชัน Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="3ab75-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="3ab75-111">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโอกาสทางการขายตามผลิตภัณฑ์ โปรดดู [เพิ่มผลิตภัณฑ์ในโอกาสทางการขาย](/dynamics365/sales-enterprise/add-products-opportunity)</span><span class="sxs-lookup"><span data-stu-id="3ab75-111">For more information about product-based opportunity lines, see [Add products to an opportunity](/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="3ab75-112">**งบประมาณของลูกค้า** เป็นแนวคิดที่เฉพาะเจาะจงสำหรับกลุ่มโอกาสทางการขายตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="3ab75-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="3ab75-113">ฟิลด์ **งบประมาณของลูกค้า** ติดตามจำนวนเงินที่ลูกค้ายินดีจ่ายสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="3ab75-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="3ab75-114">เมื่อสรุปวิธีการสร้างรายได้ของโอกาสทางการขายคือ **ระบบที่คำนวณ** ระบบจะสรุปมูลค่างบประมาณของลูกค้าในรายการโอกาสทางการขายเพื่อคำนวณรายได้โดยประมาณ</span><span class="sxs-lookup"><span data-stu-id="3ab75-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]