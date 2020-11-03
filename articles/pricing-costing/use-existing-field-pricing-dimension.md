---
title: ฟิลด์ Project Operations เป็นมิติการกำหนดราคา
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการใช้ฟิลด์เป็นมิติการกำหนดราคาใน Dynamics 365 Project Operations
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 56ff45169058d96d7ef81a710de309eec698a75f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085995"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a>ฟิลด์ Project Operations เป็นมิติการกำหนดราคา

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

เอนทิตี **ค่าจริง** มีหลายฟิลด์ที่สามารถใช้เป็นมิติการกำหนดราคาสำหรับการกำหนดราคาตามทรัพยากร ตัวอย่างเช่น ฟิลด์ทั่วไปหนึ่งฟิลด์เป็น **ทรัพยากรที่สามารถจองได้** บริษัทที่ขนาดเล็กกว่าที่มีทรัพยากรที่เรียกเก็บเงินได้น้อยกว่า 20-30 รายการ อาจพบว่าการมีอัตราค่าใช้จ่ายและราคาต้นทุนซึ่งเฉพาะเจาะจงสำหรับทรัพยากรแต่ละรายการ เป็นวิธีการที่ง่ายกว่า อย่างไรก็ตาม ขณะที่พนักงานที่เรียกเก็บเงินได้เพิ่มขึ้น อัตราเฉพาะทรัพยากรอาจไม่สมจริงหากจะมีการคงไว้ ต้นทุนทรัพยากรและอัตราการเรียกเก็บเงินเริ่มแตกต่างกันไปเมื่อทรัพยากรได้รับการเลื่อนตำแหน่ง มีประสบการณ์มากขึ้น หรือมีชุดทักษะที่แตกต่างออกไป 

อีกตัวอย่างหนึ่งคือ ประเภทของธุรกรรม ลูกค้าและตัวใช้งานได้ใช้ประเภทธุรกรรมเพื่อจัดประเภทงาน และใช้ฟิลด์นี้ในการกำหนดราคาและต้นทุนตามประเภทของงาน
