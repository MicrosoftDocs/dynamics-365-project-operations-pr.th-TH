---
title: ใช้ฟิลด์ที่มีอยู่ใน Project Service เป็นมิติการกำหนดราคา
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการใช้ฟิลด์ Project Service ที่มีอยู่เป็นมิติการกำหนดราคา
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bc3a1df7669dac43b45d781448ed5c795a65be4
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144204"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="8477a-103">ใช้ฟิลด์ที่มีอยู่ใน Project Service เป็นมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="8477a-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8477a-104">Project Service Automation (PSA) มีฟิลด์หลายฟิลด์บนเอนทิตี **ข้อมูลจริง** ที่สามารถใช้เป็นมิติการกำหนดราคาสำหรับการกำหนดราคาตามทรัพยากรในองค์กรโครงการ</span><span class="sxs-lookup"><span data-stu-id="8477a-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="8477a-105">ตัวอย่างเช่น ฟิลด์ทั่วไปหนึ่งฟิลด์เป็น **ทรัพยากรที่สามารถจองได้**</span><span class="sxs-lookup"><span data-stu-id="8477a-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="8477a-106">บริษัทที่ขนาดเล็กกว่าที่มีทรัพยากรที่เรียกเก็บเงินได้น้อยกว่า 20-30 รายการ อาจพบว่าการมีอัตราค่าใช้จ่ายและราคาต้นทุนซึ่งเฉพาะเจาะจงสำหรับทรัพยากรแต่ละรายการ เป็นวิธีการที่ง่ายกว่า</span><span class="sxs-lookup"><span data-stu-id="8477a-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="8477a-107">อย่างไรก็ตาม เนื่องจากพนักงานที่เรียกเก็บเงินได้เติบโตขึ้น อัตราเฉพาะอาจกลายเป็นความไม่เป็นจริงในการรักษา เมื่อต้นทุนทรัพยากรและอัตราเรียกเก็บเงินเริ่มที่จะแตกต่างกันเนื่องจากทรัพยากรได้รับการเลื่อนระดับ ได้รับประสบการณ์มากขึ้น หรือได้รับชุดทักษะที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="8477a-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="8477a-108">เนื่องจากวิธีการนี้ยังคงใช้งานได้สำหรับบริษัทที่มีขนาดหนึ่งๆ โปรดดู [ใช้ทรัพยากรที่สามารถจองได้เป็นมิติการกำหนดราคา](bookable-resource-pricing-dimension.md) เพื่อทำความเข้าใจว่าสามารถใช้ฟิลด์ Project Service ที่มีอยู่เป็นมิติการกำหนดราคาได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="8477a-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="8477a-109">อีกตัวอย่างหนึ่งคือ ประเภทของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="8477a-109">Another example is that of transaction category.</span></span> <span data-ttu-id="8477a-110">ลูกค้าและตัวใช้งานได้ใช้ประเภทธุรกรรมใน PSA เพื่อจัดประเภทงาน และใช้ฟิลด์นี้ในการกำหนดราคาและต้นทุนตามประเภทของงาน</span><span class="sxs-lookup"><span data-stu-id="8477a-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="8477a-111">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ใช้ประเภทธุรกรรมเป็นมิติการกำหนดราคา](transaction-category-pricing-dimension.md)</span><span class="sxs-lookup"><span data-stu-id="8477a-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
