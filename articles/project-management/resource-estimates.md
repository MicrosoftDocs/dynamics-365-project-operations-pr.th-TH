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
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286541"
---
# <a name="resource-estimates"></a><span data-ttu-id="5c74f-103">การประมาณการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="5c74f-103">Resource estimates</span></span>

<span data-ttu-id="5c74f-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="5c74f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5c74f-105">ประมาณการทรัพยากรมาจากกำลังคนตามระยะเวลาที่กำหนดไว้ในโครงสร้างการแบ่งงานพร้อมกับมิติการกำหนดราคาที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="5c74f-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="5c74f-106">โดยปกติ การคำนวณคือ **อัตรา/ชม. สำหรับแต่ละบทบาท x ชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="5c74f-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="5c74f-107">กำลังคนตามระยะเวลาสำหรับแต่ละทรัพยากรจะมีการเก็บไว้ในเรกคอร์ดการมอบหมายทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="5c74f-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="5c74f-108">การกำหนดราคาจะมีการเก็บไว้ในรายการราคาที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="5c74f-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="5c74f-109">การแปลงหน่วยใช้ตามรายการราคาที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="5c74f-109">Unit conversion is applied based on the applicable price list.</span></span>

![ประมาณการทรัพยากร](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="5c74f-111">ราคาต้นทุนและสกุลเงินต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5c74f-111">Default cost price and cost currency</span></span>

<span data-ttu-id="5c74f-112">ราคาต้นทุนเป็นเริ่มต้นจากหน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="5c74f-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="5c74f-113">อัตราการเรียกเก็บค่าใช้จ่ายและสกุลเงินการขายเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5c74f-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="5c74f-114">ราคาขายจะใช้หนึ่งครั้งต่อข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="5c74f-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="5c74f-115">ลำดับชั้นสำหรับรายการราคาขายที่เป็นค่าเริ่มต้นเป็นดังนี้:</span><span class="sxs-lookup"><span data-stu-id="5c74f-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="5c74f-116">องค์กร</span><span class="sxs-lookup"><span data-stu-id="5c74f-116">Organization</span></span>
2. <span data-ttu-id="5c74f-117">ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="5c74f-117">Customer</span></span>
3. <span data-ttu-id="5c74f-118">ใบเสนอราคา/สัญญา</span><span class="sxs-lookup"><span data-stu-id="5c74f-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]