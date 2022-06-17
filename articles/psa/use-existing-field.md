---
title: ใช้ฟิลด์ที่มีอยู่ใน Project Service เป็นมิติการกำหนดราคา
description: บทความนี้ให้ข้อมูลเกี่ยวกับการใช้ฟิลด์ Project Service ที่มีอยู่เป็นมิติการกำหนดราคา
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: abc3a3a2b61ea6f8dd34d82bf91546f8f7552a61
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925235"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>ใช้ฟิลด์ที่มีอยู่ใน Project Service เป็นมิติการกำหนดราคา

[!include [banner](../includes/psa-now-project-operations.md)]

Project Service Automation (PSA) มีฟิลด์หลายฟิลด์บนเอนทิตี **ข้อมูลจริง** ที่สามารถใช้เป็นมิติการกำหนดราคาสำหรับการกำหนดราคาตามทรัพยากรในองค์กรโครงการ ตัวอย่างเช่น ฟิลด์ทั่วไปหนึ่งฟิลด์เป็น **ทรัพยากรที่สามารถจองได้** บริษัทที่ขนาดเล็กกว่าที่มีทรัพยากรที่เรียกเก็บเงินได้น้อยกว่า 20-30 รายการ อาจพบว่าการมีอัตราค่าใช้จ่ายและราคาต้นทุนซึ่งเฉพาะเจาะจงสำหรับทรัพยากรแต่ละรายการ เป็นวิธีการที่ง่ายกว่า อย่างไรก็ตาม เนื่องจากพนักงานที่เรียกเก็บเงินได้เติบโตขึ้น อัตราเฉพาะอาจกลายเป็นความไม่เป็นจริงในการรักษา เมื่อต้นทุนทรัพยากรและอัตราเรียกเก็บเงินเริ่มที่จะแตกต่างกันเนื่องจากทรัพยากรได้รับการเลื่อนระดับ ได้รับประสบการณ์มากขึ้น หรือได้รับชุดทักษะที่แตกต่างกัน เนื่องจากวิธีการนี้ยังคงใช้งานได้สำหรับบริษัทที่มีขนาดหนึ่งๆ โปรดดู [ใช้ทรัพยากรที่สามารถจองได้เป็นมิติการกำหนดราคา](bookable-resource-pricing-dimension.md) เพื่อทำความเข้าใจว่าสามารถใช้ฟิลด์ Project Service ที่มีอยู่เป็นมิติการกำหนดราคาได้อย่างไร

อีกตัวอย่างหนึ่งคือ ประเภทของธุรกรรม ลูกค้าและตัวใช้งานได้ใช้ประเภทธุรกรรมใน PSA เพื่อจัดประเภทงาน และใช้ฟิลด์นี้ในการกำหนดราคาและต้นทุนตามประเภทของงาน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ใช้ประเภทธุรกรรมเป็นมิติการกำหนดราคา](transaction-category-pricing-dimension.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
