---
title: รายการโอกาสทางการขายตามโครงการ (Pro)
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับรายการโอกาสทางการขายตามโครงการ (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a688b9bed5a38e7b5947cbcee1e3cb8ab211e98
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085857"
---
# <a name="project-based-opportunity-lines-pro"></a>รายการโอกาสทางการขายตามโครงการ (Pro)

_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

รายการโอกาสทางการขายตามโครงการจะใช้ได้เฉพาะในโอกาสทางการขายตามโครงการเท่านั้น เรกคอร์ดโอกาสทางการขายตามโครงการมีการตั้งค่าฟิลด์ **ชนิด** เป็น **ตามงาน**

รายการโอกาสทางการขายตามโครงการคือการแสดงรายการที่จะส่งมอบให้กับลูกค้าโดยใช้โครงการ อย่างไรก็ตาม ไม่สามารถผูกโครงการกับรายการโอกาสทางการขายตามโครงการได้ โครงการสามารถผูกกับการแสดงรายการจากลำดับขั้น **ใบเสนอราคา** เป็นต้นไป เนื่องจากโดยทั่วไปแล้วโอกาสทางการขายอยู่ในลำดับขั้นเริ่มต้นของวงจรข้อตกลง การกำหนดจำนวนโครงการที่จะใช้ในการส่งมอบงานให้กับลูกค้าเป็นการตัดสินใจที่เกิดขึ้นในระยะการขายในภายหลัง คุณสามารถใช้ระยะโอกาสทางการขายในการระบุส่วนประกอบการส่งมอบแบบแยกสำหรับลูกค้า การตัดสินใจเกี่ยวกับจำนวนโครงการจริงที่ใช้ในการส่งมอบส่วนประกอบเหล่านี้สามารถส่งออกไปได้จนกว่าจะทราบข้อมูลเพิ่มเติมเกี่ยวกับงานนั้น

ด้านล่างนี้คือฟิลด์ในรายการโอกาสทางการขายตามโครงการ:

| **ฟิลด์** | **ตำแหน่งที่ตั้ง** | **ความเกี่ยวข้อง วัตถุประสงค์ และคำแนะนำ** | **ผลกระทบขั้นปลาย** |
| --- | --- | --- | --- |
| ชนิดผลิตภัณฑ์ | แท็บทั่วไป (ถูกซ่อนไว้) | คุณสามารถเลือกตัวเลือกใดตัวเลือกหนึ่งต่อไปนี้:</br>- บริการตามโครงการ (สามารถใช้ได้เฉพาะเมื่อติดตั้ง Dynamics 365 Project Operations เท่านั้น)</br>- ผลิตภัณฑ์ (สามารถใช้ได้เฉพาะเมื่อติดตั้ง Project Operations และ Dynamics 365 Sales เท่านั้น) | ค่าของฟิลด์นี้มีการตั้งค่าเป็น **บริการตามโครงการ** เมื่อคุณสร้างรายการโอกาสทางการขายตามโครงการจากตารางรายการตามโครงการในโอกาสทางการขาย <br> หากคุณเปลี่ยนแปลงหรือแทนที่่ค่านี้ ฟังก์ชันการทำงานของโครงการจะไม่ถูกเปิดใช้งานสำหรับการแสดงรายการตามโครงการของคุณ |
| โอกาสทางการขาย | แท็บทั่วไป | ฟิลด์นี้เป็นแบบอ่านอย่างเดียวและอ้างอิงถึงเรกคอร์ดโอกาสทางการขายหลักที่มีการแสดงรายการนี้อยู่ | ไม่มีผลกระทบขั้นปลายจากฟิลด์นี้ |
| ชื่อ | แท็บทั่วไป | นี่คือฟิลด์ข้อความที่แก้ไขได้ซึ่งสามารถใช้เพื่อระบุข้อมูลเฉพาะสั้นๆ ให้กับการแสดงรายการ | ค่านี้จะมีการส่งไปยังรายการใบเสนอราคาเมื่อคุณสร้างใบเสนอราคาจากโอกาสทางการขายนี้ |
| งบประมาณของลูกค้า | แท็บทั่วไป | ฟิลด์สกุลเงินที่แก้ไขได้นี้สามารถใช้เพื่อติดตามจำนวนเงินที่ลูกค้ายินดีจ่ายสำหรับการแสดงรายการนี้ | ค่านี้จะมีการส่งไปยังฟิลด์ที่สัมพันธ์กันในรายการใบเสนอราคาเมื่อคุณสร้างใบเสนอราคาจากโอกาสทางการขายนี้ |
| วิธีการเรียกเก็บเงิน | แท็บทั่วไป | ฟิลด์ที่แก้ไขได้นี้มีค่าต่อไปนี้:</br>- เวลาและวัสดุ</br>- ราคาคงที่ | ค่านี้จะมีการส่งไปยังฟิลด์ที่สัมพันธ์กันในรายการใบเสนอราคาเมื่อคุณสร้างใบเสนอราคาจากโอกาสทางการขายนี้ หลังจากสร้างรายการใบเสนอราคาแล้ว ฟิลด์นี้จะถูกล็อกและไม่สามารถเปลี่ยนแปลงได้ กำหนดค่าฟิลด์นี้ให้ถูกต้องที่สุด หากคุณต้องการเปลี่ยนค่าของฟิลด์นี้ในรายการใบเสนอราคา ให้ลบและสร้างรายการใบเสนอราคาใหม่ |