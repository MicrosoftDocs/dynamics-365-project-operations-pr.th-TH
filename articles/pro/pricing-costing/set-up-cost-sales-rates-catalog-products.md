---
title: ตั้งค่าต้นทุนและอัตราการขายสำหรับผลิตภัณฑ์แค็ตตาล็อก
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีตั้งค่าต้นทุนและอัตราการขายสำหรับสินค้าในแค็ตตาล็อกผลิตภัณฑ์
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085999"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a><span data-ttu-id="b16c6-103">ตั้งค่าต้นทุนและอัตราการขายสำหรับผลิตภัณฑ์แค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="b16c6-103">Set up cost and sales rates for catalog products</span></span>

<span data-ttu-id="b16c6-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="b16c6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b16c6-105">การตั้งค่าการกำหนดราคาสำหรับรายการแค็ตตาล็อกผลิตภัณฑ์ใน Dynamics 365 Project Operations จะเหมือนกับใน Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="b16c6-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="b16c6-106">เนื่องจากผลิตภัณฑ์ไม่สามารถประมาณหรือใช้กับโครงการใน Project Operations จึงไม่จำเป็นต้องตั้งราคาแค็ตตาล็อกผลิตภัณฑ์ในราคาตลาดของโครงการสำหรับใบเสนอราคาและสัญญา</span><span class="sxs-lookup"><span data-stu-id="b16c6-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="b16c6-107">ราคาแค็ตตาล็อกผลิตภัณฑ์ควรตั้งค่าไว้ในฟิลด์ **ราคาผลิตภัณฑ์** ของใบเสนอราคา สัญญา หรือบัญชี</span><span class="sxs-lookup"><span data-stu-id="b16c6-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="b16c6-108">อย่าตั้งค่าราคาแค็ตตาล็อกผลิตภัณฑ์ในราคาตลาดของโครงการสำหรับเอนทิตีเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="b16c6-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="b16c6-109">ราคาตลาดของโครงการเป็นเอกสิทธิ์ของ Project Operations</span><span class="sxs-lookup"><span data-stu-id="b16c6-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="b16c6-110">มีตรรกะทางธุรกิจเฉพาะแอปพลิเคชันที่คัดลอกราคาตลาดจากใบเสนอราคาไปยังสัญญา</span><span class="sxs-lookup"><span data-stu-id="b16c6-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="b16c6-111">ผลลัพธ์เป็นราคาตลาดของโครงการแบบเฉพาะสัญญา</span><span class="sxs-lookup"><span data-stu-id="b16c6-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="b16c6-112">การดำเนินการคัดลอกอาจทำให้กระบวนการชนะของใบเสนอราคาล่าช้า หากราคาตลาดของโครงการในใบเสนอราคามีขนาดใหญ่เกินไป</span><span class="sxs-lookup"><span data-stu-id="b16c6-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="b16c6-113">ไม่ได้คัดลอกราคาตลาดของผลิตภัณฑ์เพื่อสร้างราคาตลาดที่กำหนดเองในสัญญา</span><span class="sxs-lookup"><span data-stu-id="b16c6-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="b16c6-114">นี่หมายความว่าราคาตลาดของผลิตภัณฑ์จะไม่ส่งผลกระทบต่อประสิทธิภาพของกระบวนการชนะของใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="b16c6-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
