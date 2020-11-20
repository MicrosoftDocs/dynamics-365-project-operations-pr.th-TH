---
title: ฟิลด์ Project Operations เป็นมิติการกำหนดราคา
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการใช้ฟิลด์เป็นมิติการกำหนดราคาใน Dynamics 365 Project Operations
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 59367b35f15f806b109f606e912edc487d9e7685
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119261"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="c567a-103">ฟิลด์ Project Operations เป็นมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="c567a-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="c567a-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="c567a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c567a-105">เอนทิตี **ค่าจริง** มีหลายฟิลด์ที่สามารถใช้เป็นมิติการกำหนดราคาสำหรับการกำหนดราคาตามทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c567a-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="c567a-106">ตัวอย่างเช่น ฟิลด์ทั่วไปหนึ่งฟิลด์เป็น **ทรัพยากรที่สามารถจองได้**</span><span class="sxs-lookup"><span data-stu-id="c567a-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="c567a-107">บริษัทที่ขนาดเล็กกว่าที่มีทรัพยากรที่เรียกเก็บเงินได้น้อยกว่า 20-30 รายการ อาจพบว่าการมีอัตราค่าใช้จ่ายและราคาต้นทุนซึ่งเฉพาะเจาะจงสำหรับทรัพยากรแต่ละรายการ เป็นวิธีการที่ง่ายกว่า</span><span class="sxs-lookup"><span data-stu-id="c567a-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="c567a-108">อย่างไรก็ตาม ขณะที่พนักงานที่เรียกเก็บเงินได้เพิ่มขึ้น อัตราเฉพาะทรัพยากรอาจไม่สมจริงหากจะมีการคงไว้</span><span class="sxs-lookup"><span data-stu-id="c567a-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="c567a-109">ต้นทุนทรัพยากรและอัตราการเรียกเก็บเงินเริ่มแตกต่างกันไปเมื่อทรัพยากรได้รับการเลื่อนตำแหน่ง มีประสบการณ์มากขึ้น หรือมีชุดทักษะที่แตกต่างออกไป</span><span class="sxs-lookup"><span data-stu-id="c567a-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="c567a-110">อีกตัวอย่างหนึ่งคือ ประเภทของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="c567a-110">Another example is that of transaction category.</span></span> <span data-ttu-id="c567a-111">ลูกค้าและตัวใช้งานได้ใช้ประเภทธุรกรรมเพื่อจัดประเภทงาน และใช้ฟิลด์นี้ในการกำหนดราคาและต้นทุนตามประเภทของงาน</span><span class="sxs-lookup"><span data-stu-id="c567a-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
