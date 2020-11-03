---
title: กำหนดการใบแจ้งหนี้ในรายการใบเสนอราคาตามโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการสร้างกำหนดการใบแจ้งหนี้และหลักเป้าหมายสำหรับรายการใบเสนอราคา
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3ead79371c5ebf5801123e47dc0d24e35ae51e58
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085865"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>กำหนดการใบแจ้งหนี้ในรายการใบเสนอราคาตามโครงการ

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

รายการใบเสนอราคาตามโครงการให้ความสามารถในการแสดงกำหนดการใบแจ้งหนี้ ซึ่งเป็นทางเลือกในระหว่างขั้นตอนการเสนอราคาเนื่องจากแอปพลิเคชันไม่รองรับการออกใบแจ้งหนี้ของโครงการเมื่อผูกกับรายการใบเสนอราคา การออกใบแจ้งหนี้สามารถทำได้หลังจากชนะการเสนอราคาแล้วเท่านั้น ผลกระทบขั้นปลายเพียงอย่างเดียวของการสร้างกำหนดการใบแจ้งหนี้ระหว่างขั้นตอนการเสนอราคาคือ กำหนดการใบแจ้งหนี้นี้จะถูกคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาของโครงการ หากคุณไม่ได้สร้างกำหนดการใบแจ้งหนี้ในระหว่างขั้นตอนการเสนอราคา คุณจะสามารถทำได้โดยใช้รายการรายละเอียดการให้บริการตามสัญญาของโครงการ

โดยรวมแล้ว จุดประสงค์ของกำหนดการใบแจ้งหนี้คือเพื่อให้สามารถสร้างใบแจ้งหนี้ฉบับร่างสำหรับรายละเอียดการให้บริการตามสัญญาของโครงการโดยอัตโนมัติ 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>สร้างกำหนดการใบแจ้งหนี้สำหรับเวลาและวัสดุสำหรับรายการใบเสนอราคาตามโครงการ

เมื่อวิธีการเรียกเก็บเงินสำหรับรายการใบเสนอราคาตามโครงการคือเวลาและวัสดุ ระบบจะสร้างกำหนดการใบแจ้งหนี้ตามวันที่ หากต้องการสร้างกำหนดการใบแจ้งหนี้ตามวันที่โดยอัตโนมัติ ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **การตั้งค่า** > **ความถี่ของใบแจ้งหนี้** และตั้งค่าความถี่ของใบแจ้งหนี้
2. บนเพจ **ใบเสนอราคา** ให้เปิดใบเสนอราคาของโครงการและบนแท็บ **สรุป** ให้กำหนดวันที่ส่งมอบที่ร้องขอ
3. เปิดรายการใบเสนอราคาสำหรับเวลาและวัสดุที่คุณต้องการสร้างกำหนดการใบแจ้งหนี้ตามวันที่ 
4. บนแท็บ **กำหนดการใบแจ้งหนี้** ให้เลือกค่าในฟิลด์ **การเริ่มต้นการเรียกเก็บเงิน** และ **ความถี่ของใบแจ้งหนี้** 
5. ในตารางย่อย ให้เลือก **สร้างกำหนดการใบแจ้งหนี้**
6. แอปพลิเคชันสร้างกำหนดการใบแจ้งหนี้ที่มีการตั้งค่าฟิลด์ **วันที่เรียกใช้ใบแจ้งหนี้** , **วันที่ตัดธุรกรรม** และ **การสถานะการเรียกใช้** ด้วยวิธีต่อไปนี้:

    - **วันที่เรียกใช้ใบแจ้งหนี้** มีการตั้งค่าเป็นวันที่ที่กำหนดตามความถี่ของใบแจ้งหนี้
    - **วันที่ตัดธุรกรรม** มีการตั้งค่าเป็นวันก่อนหน้า **วันที่เรียกใช้ใบแจ้งหนี้**
    - **สถานะการเรียกใช้** จะตั้งค่าโดยอัตโนมัติเป็น **ไม่ทำงาน** เมื่องานการสร้างใบแจ้งหนี้อัตโนมัติทำงานในวันที่เรียกใช้ใบแจ้งหนี้ที่กำหนด งานจะปรับปรุงฟิลด์นี้เป็น **เรียกใช้สำเร็จ** หรือ **เรียกใช้ล้มเหลว**

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>สร้างกำหนดการใบแจ้งหนี้ที่มีราคาคงที่สำหรับรายการใบเสนอราคาตามโครงการ

เมื่อรายการใบเสนอราคาตามโครงการมีวิธีการเรียกเก็บเงิน **แบบคงที่** ระบบจะสร้างกำหนดการใบแจ้งหนี้ตามหลักเป้าหมาย ทำตามขั้นตอนต่อไปนี้เพื่อสร้างกำหนดการนี้โดยอัตโนมัติสำหรับชุดหลักเป้าหมายคงที่ซึ่งมีการกระจายเท่าๆ กันสำหรับช่วงเวลาปฏิทิน

1. ไปที่ **การตั้งค่า** > **ความถี่ของใบแจ้งหนี้** และตั้งค่าความถี่ของใบแจ้งหนี้
2. บนเพจ **ใบเสนอราคา** ให้เปิดใบเสนอราคาของโครงการและบนแท็บ **สรุป** ให้กำหนดวันที่ส่งมอบที่ร้องขอ
3. เปิดรายการใบเสนอราคาที่มีราคาคงที่ที่คุณต้องการเพื่อสร้างกำหนดการหลักเป้าหมาย 
4. บนแท็บ **กำหนดการใบแจ้งหนี้** ให้เลือกค่าในฟิลด์ **การเริ่มต้นการเรียกเก็บเงิน** และ **ความถี่ของใบแจ้งหนี้** 
5. ในตารางย่อย ให้เลือก **สร้างหลักเป้าหมายเป็นระยะ**
6. แอปพลิเคชันสร้างกำหนดการใบแจ้งหนี้โดยมีชื่อหลักเป้าหมาย วันที่ และจำนวนเงิน

    - ชื่อหลักเป้าหมายมีการตั้งค่าเป็นวันที่ที่กำหนดตามความถี่ของใบแจ้งหนี้
    - วันที่ของหลักเป้าหมายมีการตั้งค่าเป็นวันที่ที่กำหนดตามความถี่ของใบแจ้งหนี้
    - จำนวนเงินของหลักเป้าหมายคำนวณโดยการหารจำนวนเงินของใบเสนอราคาในรายการใบเสนอราคาตามโครงการด้วยจำนวนของหลักเป้าหมายที่กำหนดโดยความถี่และการเริ่มต้นการเรียกเก็บเงินและวันที่ส่งมอบที่ร้องขอ
    - หากรายการใบเสนอราคามีจำนวนเงินภาษีโดยประมาณ ค่านี้จะแบ่งระหว่างแต่ละหลักเป้าหมายเท่าๆ กันเมื่อสร้างหลักเป้าหมายเป็นระยะ

### <a name="manually-create-milestones"></a>สร้างหลักเป้าหมายด้วยตนเอง

นอกจากนี้ คุณยังสามารถสร้างหลักเป้าหมายของราคาคงที่ได้ด้วยตนเองเมื่อไม่มีการแบ่งเป็นระยะได้ด้วย หากต้องการสร้างหลักเป้าหมายด้วยตนเอง:

เปิดรายการใบเสนอราคาที่มีราคาคงที่ที่คุณต้องการเพื่อสร้างหลักเป้าหมาย บนแท็บ **กำหนดการใบแจ้งหนี้** บนตารางย่อย เลือก **+ สร้างหลักเป้าหมายของรายการใบเสนอราคาใหม่** และป้อนข้อมูลที่จำเป็นตามตารางต่อไปนี้

| **ฟิลด์** | **ตำแหน่งที่ตั้ง** | **ความเกี่ยวข้อง วัตถุประสงค์ และคำแนะนำ** | **ผลกระทบขั้นปลาย** |
| --- | --- | --- | --- |
| ชื่อหลักเป้าหมาย | การสร้างด่วน | ชื่อของหลักเป้าหมาย | รายการนี้จะเผยแพร่เป็นหลักเป้าหมายในรายละเอียดการให้บริการตามสัญญาโครงการและไปยังใบแจ้งหนี้ |
| งานโครงการ | การสร้างด่วน | หากหลักเป้าหมายเชื่อมโยงกับงานโครงการ คุณสามารถใช้การอ้างอิงนี้เพื่อเพิ่มตรรกะที่กำหนดเองเพื่อตั้งค่าสถานะหลักเป้าหมายตามสถานะของงาน | แอปพลิเคชันนี้ไม่มีผลกระทบขั้นปลายของการอ้างอิงถึงงานนี้ |
| วันที่ของหลักเป้าหมาย | การสร้างด่วน | ตั้งค่าวันที่ที่กระบวนการสร้างใบแจ้งหนี้อัตโนมัติควรมองหาสถานะของหลักเป้าหมายนี้เพื่อใช้ในการออกใบแจ้งหนี้ | รายการนี้จะเผยแพร่เป็นหลักเป้าหมายในรายละเอียดการให้บริการตามสัญญาโครงการและไปยังใบแจ้งหนี้ |
| สถานะใบแจ้งหนี้ | การสร้างด่วน | เมื่อสร้างหลักเป้าหมาย สถานะนี้จะถูกตั้งค่าเป็น **ไม่พร้อมสำหรับการออกใบแจ้งหนี้** เสมอ | รายการนี้จะเผยแพร่เป็นหลักเป้าหมายในรายละเอียดการให้บริการตามสัญญาโครงการและไปยังใบแจ้งหนี้ |
| จำนวนเงินในบรรทัด | การสร้างด่วน | จำนวนเงินหรือมูลค่าของหลักเป้าหมายที่จะออกใบแจ้งหนี้ให้กับลูกค้า | รายการนี้จะเผยแพร่เป็นหลักเป้าหมายในรายละเอียดการให้บริการตามสัญญาโครงการและไปยังใบแจ้งหนี้ |
| ภาษี | การสร้างด่วน | จำนวนเงินภาษีที่จะนำไปใช้กับหลักเป้าหมาย | รายการนี้จะเผยแพร่เป็นหลักเป้าหมายในรายละเอียดการให้บริการตามสัญญาโครงการและไปยังใบแจ้งหนี้ |