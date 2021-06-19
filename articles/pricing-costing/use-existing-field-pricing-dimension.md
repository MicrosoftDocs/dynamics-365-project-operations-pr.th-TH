---
title: ฟิลด์ Project Operations เป็นมิติการกำหนดราคา
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการใช้ฟิลด์เป็นมิติการกำหนดราคาใน Dynamics 365 Project Operations
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a29460b2a9dc9a9755e7e28a6cd9712c6b06e8c6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004509"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="eced3-103">ฟิลด์ Project Operations เป็นมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="eced3-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="eced3-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="eced3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="eced3-105">เอนทิตี **ค่าจริง** มีหลายฟิลด์ที่สามารถใช้เป็นมิติการกำหนดราคาสำหรับการกำหนดราคาตามทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="eced3-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="eced3-106">ตัวอย่างเช่น ฟิลด์ทั่วไปหนึ่งฟิลด์เป็น **ทรัพยากรที่สามารถจองได้**</span><span class="sxs-lookup"><span data-stu-id="eced3-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="eced3-107">บริษัทที่ขนาดเล็กกว่าที่มีทรัพยากรที่เรียกเก็บเงินได้น้อยกว่า 20-30 รายการ อาจพบว่าการมีอัตราค่าใช้จ่ายและราคาต้นทุนซึ่งเฉพาะเจาะจงสำหรับทรัพยากรแต่ละรายการ เป็นวิธีการที่ง่ายกว่า</span><span class="sxs-lookup"><span data-stu-id="eced3-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="eced3-108">อย่างไรก็ตาม ขณะที่พนักงานที่เรียกเก็บเงินได้เพิ่มขึ้น อัตราเฉพาะทรัพยากรอาจไม่สมจริงหากจะมีการคงไว้</span><span class="sxs-lookup"><span data-stu-id="eced3-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="eced3-109">ต้นทุนทรัพยากรและอัตราการเรียกเก็บเงินเริ่มแตกต่างกันไปเมื่อทรัพยากรได้รับการเลื่อนตำแหน่ง มีประสบการณ์มากขึ้น หรือมีชุดทักษะที่แตกต่างออกไป</span><span class="sxs-lookup"><span data-stu-id="eced3-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="eced3-110">อีกตัวอย่างหนึ่งคือ ประเภทของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="eced3-110">Another example is that of transaction category.</span></span> <span data-ttu-id="eced3-111">ลูกค้าและตัวใช้งานได้ใช้ประเภทธุรกรรมเพื่อจัดประเภทงาน และใช้ฟิลด์นี้ในการกำหนดราคาและต้นทุนตามประเภทของงาน</span><span class="sxs-lookup"><span data-stu-id="eced3-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]