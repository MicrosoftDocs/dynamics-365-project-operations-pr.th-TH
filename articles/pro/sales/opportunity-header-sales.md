---
title: ส่วนหัวของโอกาสทางการขาย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับข้อมูลโดยรวมเกี่ยวกับข้อตกลงตามโครงการและรายการโอกาสทางการขายตามโครงการ
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f08de54767f49c308d0ccc7f2e1c6ef880b7f99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085860"
---
# <a name="opportunity-header"></a>ส่วนหัวของโอกาสทางการขาย

_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

ส่วนหัวของโอกาสทางการขายจะรวบรวมข้อมูลโดยรวมเกี่ยวกับข้อตกลงตามโครงการที่ใช้กับทุกรายการในโอกาสทางการขายตามโครงการ

โอกาสทางการขายตามโครงการใน Dynamics 365 Project Operations เป็นส่วนขยายของโอกาสทางการขายใน Dynamics 365 Sales ส่วนขยายเหล่านี้มีฟังก์ชันเพิ่มเติมที่เฉพาะเจาะจงและจำเป็นสำหรับโอกาสทางการขายตามโครงการ ส่วนขยายเหล่านี้สามารถรวมฟิลด์ใหม่และการดำเนินการของ Ribbon ที่มีอยู่ในโอกาสทางการขายตามโครงการ คุณอาจพบฟิลด์ ฟังก์ชันการทำงาน และตรรกะเริ่มต้นบางส่วนที่มีอยู่ใน Sales ไม่สามารถใช้งานใน Project Operations

ตารางต่อไปนี้มีฟิลด์ในโอกาสทางการขายตามโครงการที่ไม่ซ้ำกันกับ Project Operations หรือมีการเปลี่ยนแปลงที่สำคัญบางอย่างกับลักษณะการทำงานจากโอกาสทางการขายใน Sales

| **ฟิลด์** | **ตำแหน่งที่ตั้ง** | **ความเกี่ยวข้อง วัตถุประสงค์ และคำแนะนำ** | **ผลกระทบขั้นปลาย** |
| --- | --- | --- | --- |
| ประเภท | แท็บทั่วไป (ถูกซ่อนไว้) | ฟิลด์ชุดตัวเลือกนี้มีตัวเลือกดังต่อไปนี้:</br>- ตามงาน (ใช้ได้เฉพาะกับ Project Operations)</br>- ตามสินค้า (สามารถใช้ได้เฉพาะเมื่อติดตั้ง Project Operations และ Sales เท่านั้น)</br>- ตามการบำรุงรักษาบริการ (สามารถใช้งานเมื่อติดตั้ง Field Service) | เมื่อคุณใช้ Project Operations ค่าฟิลด์นี้จะตั้งค่าเป็น **ตามงาน** โดยอัตโนมัติ ซึ่งจะจัดประเภทของโอกาสทางการขายเป็นแบบตามโครงการ โอกาสทางการขายควรเป็นไปตามโครงการเพื่อเปิดใช้งานส่วนขยายและฟังก์ชันการทำงานเฉพาะโครงการทั้งหมดในกระบวนการขายขั้นปลายสำหรับข้อเสนอนี้ |
| ติดต่อ | แท็บทั่วไป | การอ้างอิงถึงผู้ติดต่อหลักของลูกค้าสำหรับข้อตกลงนี้ | |
| บัญชี | แท็บทั่วไป | การอ้างอิงถึงเรกคอร์ดบริษัทหรือบัญชีของลูกค้า | |
| ผู้จัดการลูกค้าองค์กร | แท็บทั่วไป | ชื่อของผู้จัดการบัญชีสำหรับโอกาสทางการขายตามโครงการนี้ | ผู้จัดการลูกค้าองค์กรมีหน้าที่จัดการความสัมพันธ์กับลูกค้าจนโครงการนี้เสร็จสมบูรณ์ ตามเรกคอร์ดทรัพยากรที่สามารถจองได้ที่เชื่อมโยงกับผู้จัดการบัญชี หน่วยที่ทำสัญญาจะมีการกำหนดเป็นค่าเริ่มต้น |
| หน่วยตามสัญญา | แท็บทั่วไป | หน่วยองค์กรที่รับผิดชอบการส่งมอบโครงการที่เกี่ยวข้องกับข้อตกลงนี้ | หน่วยที่ทำสัญญาคือแผนกของบริษัทที่จะดำเนินโครงการหลังจากปิดข้อตกลง ทุกหน่วยที่ทำสัญญามีสกุลเงิน และสกุลเงินนี้ใช้เพื่อรายงานต้นทุนโดยประมาณและต้นทุนจริงที่เกิดขึ้นระหว่างโครงการ |

สำหรับฟิลด์และส่วนอื่นๆ ทั้งหมดในแท็บ **สรุป** ของโอกาสทางการขาย ดูที่ [สร้างหรือแก้ไขโอกาสทางการขาย (การขายและฮับการขาย)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)