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
ms.openlocfilehash: 2f95228cd765d9f220aa4b143412b237ec609eb89fd9aeb786818af828dd3229
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001949"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a>ฟิลด์ Project Operations เป็นมิติการกำหนดราคา

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

เอนทิตี **ค่าจริง** มีหลายฟิลด์ที่สามารถใช้เป็นมิติการกำหนดราคาสำหรับการกำหนดราคาตามทรัพยากร ตัวอย่างเช่น ฟิลด์ทั่วไปหนึ่งฟิลด์เป็น **ทรัพยากรที่สามารถจองได้** บริษัทที่ขนาดเล็กกว่าที่มีทรัพยากรที่เรียกเก็บเงินได้น้อยกว่า 20-30 รายการ อาจพบว่าการมีอัตราค่าใช้จ่ายและราคาต้นทุนซึ่งเฉพาะเจาะจงสำหรับทรัพยากรแต่ละรายการ เป็นวิธีการที่ง่ายกว่า อย่างไรก็ตาม ขณะที่พนักงานที่เรียกเก็บเงินได้เพิ่มขึ้น อัตราเฉพาะทรัพยากรอาจไม่สมจริงหากจะมีการคงไว้ ต้นทุนทรัพยากรและอัตราการเรียกเก็บเงินเริ่มแตกต่างกันไปเมื่อทรัพยากรได้รับการเลื่อนตำแหน่ง มีประสบการณ์มากขึ้น หรือมีชุดทักษะที่แตกต่างออกไป 

อีกตัวอย่างหนึ่งคือ ประเภทของธุรกรรม ลูกค้าและตัวใช้งานได้ใช้ประเภทธุรกรรมเพื่อจัดประเภทงาน และใช้ฟิลด์นี้ในการกำหนดราคาและต้นทุนตามประเภทของงาน


[!INCLUDE[footer-include](../includes/footer-banner.md)]