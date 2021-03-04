---
title: รายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์ที่มีต้นทุน - Lite
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการสร้าง
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764482"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="83476-103">รายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์ที่มีต้นทุน - Lite</span><span class="sxs-lookup"><span data-stu-id="83476-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="83476-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="83476-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="83476-105">รายละเอียดการให้บริการตามสัญญาที่อิงตามผลิตภัณฑ์ใน Dynamics 365 Project Operations รวมฟิลด์ **ราคาต้นทุน** ซึ่งเก็บราคาต้นทุนของผลิตภัณฑ์สำหรับการคำนวณความสามารถในการทำกำไรปลายน้ำ</span><span class="sxs-lookup"><span data-stu-id="83476-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="83476-106">เมื่อมีการสร้างรายละเอียดการให้บริการตามสัญญาที่อิงตามผลิตภัณฑ์สำหรับผลิตภัณฑ์แค็ตตาล็อก ต้นทุนของรายการจะเริ่มต้นจากฟิลด์ **ต้นทุนมาตรฐาน** ในแค็ตตาล็อกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="83476-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="83476-107">ฟิลด์ **ต้นทุนมาตรฐาน** ในแค็ตตาล็อกผลิตภัณฑ์ จะตั้งค่าในสกุลเงินฐานขององค์กร</span><span class="sxs-lookup"><span data-stu-id="83476-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="83476-108">เมื่อต้นทุนต่อหน่วยเป็นค่าเริ่มต้นในรายละเอียดการให้บริการตามสัญญา จะถูกแปลงเป็นสกุลเงินการขายในสัญญา</span><span class="sxs-lookup"><span data-stu-id="83476-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="83476-109">ต้นทุนต่อหน่วยในรายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="83476-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="83476-110">การมีต้นทุนต่อหน่วยในรายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์ช่วยให้มีต้นทุนที่แตกต่างกันสำหรับแต่ละหน่วยการขาย</span><span class="sxs-lookup"><span data-stu-id="83476-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="83476-111">แม้ว่าจะไม่จำเป็นเสมอไป แต่ก็มีบางสถานการณ์ที่ผู้จัดหาอาจจะลดต้นทุนของผลิตภัณฑ์ให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="83476-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="83476-112">พิจารณาสถานการณ์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="83476-112">Consider the following scenario:</span></span>

<span data-ttu-id="83476-113">Fabrikam Robotics กำลังติดตั้งแขนหุ่นยนต์ที่สายการประกอบของ Adatum Corporation</span><span class="sxs-lookup"><span data-stu-id="83476-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="83476-114">Fabrikam ให้บริการติดตั้ง แต่แขนหุ่นยนต์มาจาก Trey Research</span><span class="sxs-lookup"><span data-stu-id="83476-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="83476-115">หากการติดตั้งแขนหุ่นยนต์ที่ Adatum Corporation เป็นการเปิดแนวทางอุตสาหกรรมใหม่สำหรับแขนหุ่นยนต์ของ Trey Research พวกเขาสามารถให้ส่วนลดพิเศษสำหรับข้อตกลงนี้แก่ Fabrikam ได้</span><span class="sxs-lookup"><span data-stu-id="83476-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="83476-116">ในกรณีนี้ Fabrikam จะสร้างรายละเอียดการให้บริการตามสัญญาตามผลิตภัณฑ์สำหรับ Robotic Arms</span><span class="sxs-lookup"><span data-stu-id="83476-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="83476-117">มีการป้อนต้นทุนต่อหน่วยสำหรับสัญญานี้</span><span class="sxs-lookup"><span data-stu-id="83476-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="83476-118">ต้นทุนแตกต่างจากต้นทุนของแขนหุ่นยนต์จาก Trey Research</span><span class="sxs-lookup"><span data-stu-id="83476-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>
