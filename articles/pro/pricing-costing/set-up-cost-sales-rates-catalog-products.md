---
title: ตั้งค่าอัตราต้นทุนและการขายสำหรับผลิตภัณฑ์ในแค็ตตาล็อก - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีตั้งค่าต้นทุนและอัตราการขายสำหรับสินค้าในแค็ตตาล็อกผลิตภัณฑ์
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0941c549cc38f0938a5819e8cb6ca9912f14790
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274481"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="1f1b6-103">ตั้งค่าอัตราต้นทุนและการขายสำหรับผลิตภัณฑ์ในแค็ตตาล็อก - Lite</span><span class="sxs-lookup"><span data-stu-id="1f1b6-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="1f1b6-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="1f1b6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="1f1b6-105">การตั้งราคาสำหรับรายการแค็ตตาล็อกสินค้าใน Dynamics 365 Project Operations เหมือนกับใน Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="1f1b6-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="1f1b6-106">ใน Project Operations ไม่สามารถประมาณหรือใช้ผลิตภัณฑ์ในโครงการได้ ดังนั้นจึงไม่จำเป็นต้องกำหนดราคาแค็ตตาล็อกผลิตภัณฑ์ในรายการราคาโครงการสำหรับใบเสนอราคาและสัญญา</span><span class="sxs-lookup"><span data-stu-id="1f1b6-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="1f1b6-107">ใช้ฟิลด์ **ราคาผลิตภัณฑ์** ของใบเสนอราคา สัญญา หรือบัญชีเพื่อกำหนดราคาแค็ตตาล็อกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="1f1b6-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="1f1b6-108">อย่าตั้งราคาแค็ตตาล็อกผลิตภัณฑ์ในรายการราคาโครงการ</span><span class="sxs-lookup"><span data-stu-id="1f1b6-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="1f1b6-109">รายการราคาของโครงการเป็นเอกสิทธิ์ของ Project Operations</span><span class="sxs-lookup"><span data-stu-id="1f1b6-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="1f1b6-110">ตรรกะทางธุรกิจเฉพาะโปรแกรมประยุกต์คัดลอกรายการราคาจากใบเสนอราคาเป็นสัญญา</span><span class="sxs-lookup"><span data-stu-id="1f1b6-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="1f1b6-111">ผลลัพธ์เป็นรายการราคาของโครงการแบบเฉพาะสัญญา</span><span class="sxs-lookup"><span data-stu-id="1f1b6-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="1f1b6-112">การดำเนินการคัดลอกอาจทำให้กระบวนการชนะของใบเสนอราคาล่าช้า หากรายการราคาของโครงการในใบเสนอราคามีขนาดใหญ่เกินไป</span><span class="sxs-lookup"><span data-stu-id="1f1b6-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="1f1b6-113">ไม่ได้คัดลอกรายการราคาของผลิตภัณฑ์เพื่อสร้างรายการราคาที่กำหนดเองในสัญญา</span><span class="sxs-lookup"><span data-stu-id="1f1b6-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="1f1b6-114">เนื่องจากไม่มีการคัดลอกที่เกี่ยวข้อง ประสิทธิภาพของกระบวนการเสนอราคาจึงไม่ได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="1f1b6-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]