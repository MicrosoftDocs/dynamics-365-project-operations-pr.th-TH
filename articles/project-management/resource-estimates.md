---
title: การประมาณการทรัพยากร
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการคำนวณประมาณการทรัพยากรใน Project Operations
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127405"
---
# <a name="resource-estimates"></a><span data-ttu-id="c8e85-103">การประมาณการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c8e85-103">Resource estimates</span></span>

<span data-ttu-id="c8e85-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="c8e85-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c8e85-105">ประมาณการทรัพยากรมาจากกำลังคนตามระยะเวลาที่กำหนดไว้ในโครงสร้างการแบ่งงานพร้อมกับมิติการกำหนดราคาที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c8e85-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="c8e85-106">โดยปกติ การคำนวณคือ **อัตรา/ชม. สำหรับแต่ละบทบาท x ชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="c8e85-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="c8e85-107">กำลังคนตามระยะเวลาสำหรับแต่ละทรัพยากรจะมีการเก็บไว้ในเรกคอร์ดการมอบหมายทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c8e85-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="c8e85-108">การกำหนดราคาจะมีการเก็บไว้ในรายการราคาที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="c8e85-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="c8e85-109">การแปลงหน่วยใช้ตามรายการราคาที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c8e85-109">Unit conversion is applied based on the applicable price list.</span></span>

![ประมาณการทรัพยากร](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="c8e85-111">ราคาต้นทุนและสกุลเงินต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c8e85-111">Default cost price and cost currency</span></span>

<span data-ttu-id="c8e85-112">ราคาต้นทุนเป็นเริ่มต้นจากหน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="c8e85-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="c8e85-113">อัตราการเรียกเก็บค่าใช้จ่ายและสกุลเงินการขายเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c8e85-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="c8e85-114">ราคาขายจะใช้หนึ่งครั้งต่อข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="c8e85-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="c8e85-115">ลำดับชั้นสำหรับรายการราคาขายที่เป็นค่าเริ่มต้นเป็นดังนี้:</span><span class="sxs-lookup"><span data-stu-id="c8e85-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="c8e85-116">องค์กร</span><span class="sxs-lookup"><span data-stu-id="c8e85-116">Organization</span></span>
2. <span data-ttu-id="c8e85-117">ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c8e85-117">Customer</span></span>
3. <span data-ttu-id="c8e85-118">ใบเสนอราคา/สัญญา</span><span class="sxs-lookup"><span data-stu-id="c8e85-118">Quote/contract</span></span>
