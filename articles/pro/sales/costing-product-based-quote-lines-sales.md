---
title: รายการใบเสนอราคาตามผลิตภัณฑ์ที่มีต้นทุน
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการใช้ราคาต้นทุนกับรายการใบเสนอราคาตามผลิตภัณฑ์
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906358"
---
# <a name="costing-product-based-quote-lines"></a>รายการใบเสนอราคาตามผลิตภัณฑ์ที่มีต้นทุน

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_


รายการใบเสนอราคาตามผลิตภัณฑ์ใน Dynamics 365 Project Operations ยังมีฟิลด์ **ราคาต้นทุน** ด้วย ฟิลด์นี้ใช้เพื่อติดตามราคาต้นทุนของผลิตภัณฑ์ในรายการใบเสนอราคาและสำหรับการคำนวณผลกำไรขั้นปลาย

เมื่อมีการสร้างรายการใบเสนอราคาตามผลิตภัณฑ์สำหรับผลิตภัณฑ์ในแค็ตตาล็อก ต้นทุนของรายการใบเสนอราคาตามผลิตภัณฑ์จะเริ่มต้นจากฟิลด์ **ต้นทุนมาตรฐาน** ในแค็ตตาล็อกผลิตภัณฑ์ ฟิลด์ต้นทุนมาตรฐานในแค็ตตาล็อกผลิตภัณฑ์จะตั้งค่าในสกุลเงินฐานขององค์กร ต้นทุนต่อหน่วยเริ่มต้นในรายการใบเสนอราคาตามผลิตภัณฑ์จะมีการแปลงเป็นสกุลเงินการขายในใบเสนอราคา

## <a name="unit-cost-on-a-product-based-quote-line"></a>ต้นทุนต่อหน่วยในรายการใบเสนอราคาตามผลิตภัณฑ์

จุดประสงค์ของการมีต้นทุนต่อหน่วยในรายการใบเสนอราคาตามผลิตภัณฑ์คือการสามารถมีต้นทุนที่แตกต่างกันสำหรับผลิตภัณฑ์ในการขายแต่ละครั้ง ลักษณะดังกล่าวไม่ใช่สถานการณ์ทั่วไป แต่ในบางครั้งซัพพลายเออร์อาจให้ส่วนลดต้นทุนของผลิตภัณฑ์ได้ ขึ้นอยู่กับลูกค้าในการขายขั้นสุดท้าย

ตัวอย่างเช่น:

Fabrikam Robotics กำลังติดตั้งแขนหุ่นยนต์ที่สายการประกอบของ A Datum Corporation Fabrikam ให้บริการติดตั้ง แต่แขนหุ่นยนต์ได้รับการจัดหาจาก Trey หากการติดตั้งแขนหุ่นยนต์ที่ A Datum Corporation เป็นการเปิดแนวทางอุตสาหกรรมใหม่สำหรับแขนหุ่นยนต์ของ Trey บริษัท Trey สามารถให้ส่วนลดพิเศษสำหรับข้อตกลงนี้แก่ Fabrikam ได้

ในกรณีนี้ Fabrikam จะสร้างใบเสนอราคาตามผลิตภัณฑ์สำหรับแขนหุ่นยนต์ และป้อนต้นทุนต่อหน่วยแบบพิเศษสำหรับใบเสนอราคานี้ ต้นทุนนี้แตกต่างจากต้นทุนมาตรฐานของแขนหุ่นยนต์ Trey
