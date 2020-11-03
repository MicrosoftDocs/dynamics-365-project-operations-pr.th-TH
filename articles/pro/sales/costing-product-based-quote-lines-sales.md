---
title: รายการใบเสนอราคาตามผลิตภัณฑ์ที่มีต้นทุน
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการใช้ราคาต้นทุนกับรายการใบเสนอราคาตามผลิตภัณฑ์
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085835"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="4244f-103">รายการใบเสนอราคาตามผลิตภัณฑ์ที่มีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="4244f-103">Costing product-based quote lines</span></span>

<span data-ttu-id="4244f-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="4244f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="4244f-105">รายการใบเสนอราคาตามผลิตภัณฑ์ใน Dynamics 365 Project Operations ยังมีฟิลด์ **ราคาต้นทุน** ด้วย</span><span class="sxs-lookup"><span data-stu-id="4244f-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="4244f-106">ฟิลด์นี้ใช้เพื่อติดตามราคาต้นทุนของผลิตภัณฑ์ในรายการใบเสนอราคาและสำหรับการคำนวณผลกำไรขั้นปลาย</span><span class="sxs-lookup"><span data-stu-id="4244f-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="4244f-107">เมื่อมีการสร้างรายการใบเสนอราคาตามผลิตภัณฑ์สำหรับผลิตภัณฑ์ในแค็ตตาล็อก ต้นทุนของรายการใบเสนอราคาตามผลิตภัณฑ์จะเริ่มต้นจากฟิลด์ **ต้นทุนมาตรฐาน** ในแค็ตตาล็อกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4244f-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="4244f-108">ฟิลด์ต้นทุนมาตรฐานในแค็ตตาล็อกผลิตภัณฑ์จะตั้งค่าในสกุลเงินฐานขององค์กร</span><span class="sxs-lookup"><span data-stu-id="4244f-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="4244f-109">ต้นทุนต่อหน่วยเริ่มต้นในรายการใบเสนอราคาตามผลิตภัณฑ์จะมีการแปลงเป็นสกุลเงินการขายในใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="4244f-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="4244f-110">ต้นทุนต่อหน่วยในรายการใบเสนอราคาตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4244f-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="4244f-111">จุดประสงค์ของการมีต้นทุนต่อหน่วยในรายการใบเสนอราคาตามผลิตภัณฑ์คือการสามารถมีต้นทุนที่แตกต่างกันสำหรับผลิตภัณฑ์ในการขายแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="4244f-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="4244f-112">ลักษณะดังกล่าวไม่ใช่สถานการณ์ทั่วไป แต่ในบางครั้งซัพพลายเออร์อาจให้ส่วนลดต้นทุนของผลิตภัณฑ์ได้ ขึ้นอยู่กับลูกค้าในการขายขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="4244f-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="4244f-113">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="4244f-113">For example:</span></span>

<span data-ttu-id="4244f-114">Fabrikam Robotics กำลังติดตั้งแขนหุ่นยนต์ที่สายการประกอบของ A Datum Corporation</span><span class="sxs-lookup"><span data-stu-id="4244f-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="4244f-115">Fabrikam ให้บริการติดตั้ง แต่แขนหุ่นยนต์ได้รับการจัดหาจาก Trey</span><span class="sxs-lookup"><span data-stu-id="4244f-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="4244f-116">หากการติดตั้งแขนหุ่นยนต์ที่ A Datum Corporation เป็นการเปิดแนวทางอุตสาหกรรมใหม่สำหรับแขนหุ่นยนต์ของ Trey บริษัท Trey สามารถให้ส่วนลดพิเศษสำหรับข้อตกลงนี้แก่ Fabrikam ได้</span><span class="sxs-lookup"><span data-stu-id="4244f-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="4244f-117">ในกรณีนี้ Fabrikam จะสร้างใบเสนอราคาตามผลิตภัณฑ์สำหรับแขนหุ่นยนต์ และป้อนต้นทุนต่อหน่วยแบบพิเศษสำหรับใบเสนอราคานี้</span><span class="sxs-lookup"><span data-stu-id="4244f-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="4244f-118">ต้นทุนนี้แตกต่างจากต้นทุนมาตรฐานของแขนหุ่นยนต์ Trey</span><span class="sxs-lookup"><span data-stu-id="4244f-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
