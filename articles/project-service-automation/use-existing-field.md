---
title: ใช้ฟิลด์ที่มีอยู่ใน Project Service เป็นมิติการกำหนดราคา
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการใช้ฟิลด์ Project Service ที่มีอยู่เป็นมิติการกำหนดราคา
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: ed86e0c4-b2ea-4b3b-b9e3-cbfb3b512591
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: b280e2aeecc9d63fb65b77fad809edff817aff65
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756432"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>ใช้ฟิลด์ที่มีอยู่ใน Project Service เป็นมิติการกำหนดราคา

Project Service Automation (PSA) มีฟิลด์หลายฟิลด์บนเอนทิตี **ข้อมูลจริง** ที่สามารถใช้เป็นมิติการกำหนดราคาสำหรับการกำหนดราคาตามทรัพยากรในองค์กรโครงการ ตัวอย่างเช่น ฟิลด์ทั่วไปหนึ่งฟิลด์เป็น **ทรัพยากรที่สามารถจองได้** บริษัทที่ขนาดเล็กกว่าที่มีทรัพยากรที่เรียกเก็บเงินได้น้อยกว่า 20-30 รายการ อาจพบว่าการมีอัตราค่าใช้จ่ายและราคาต้นทุนซึ่งเฉพาะเจาะจงสำหรับทรัพยากรแต่ละรายการ เป็นวิธีการที่ง่ายกว่า อย่างไรก็ตาม เนื่องจากพนักงานที่เรียกเก็บเงินได้เติบโตขึ้น นี่อาจกลายเป็นความไม่เป็นจริงในการรักษา เมื่อต้นทุนทรัพยากรและอัตราเรียกเก็บเงินเริ่มที่จะแตกต่างกันเนื่องจากทรัพยากรได้รับการเลื่อนระดับ ได้รับประสบการณ์มากขึ้น หรือได้รับชุดทักษะที่แตกต่างกัน เนื่องจากวิธีการนี้ยังคงใช้งานได้สำหรับบริษัทที่มีขนาดหนึ่งๆ ให้ดูที่หัวข้อ [ใช้ทรัพยากรที่สามารถจองได้เป็นมิติการกำหนดราคา](bookable-resource-pricing-dimension.md) เพื่อทำความเข้าใจว่าสามารถใช้ฟิลด์ Project Service ที่มีอยู่เป็นมิติการกำหนดราคาได้อย่างไร

อีกตัวอย่างหนึ่งคือ ประเภทของธุรกรรม ลูกค้าและตัวใช้งานได้ใช้ประเภทธุรกรรมใน PSA เพื่อจัดประเภทงาน และใช้ฟิลด์นี้ในการกำหนดราคาและต้นทุนตามประเภทของงาน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ใช้ประเภทธุรกรรมเป็นมิติการกำหนดราคา](transaction-category-pricing-dimension.md)
