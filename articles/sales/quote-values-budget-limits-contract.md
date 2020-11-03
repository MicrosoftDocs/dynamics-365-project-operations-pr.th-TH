---
title: ข้อมูลสรุปเกี่ยวกับใบเสนอราคาโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับข้อมูลและการตั้งค่าที่ใช้กับและส่งผลกระทบต่อใบเสนอราคาโครงการ
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6dde5305f179e9a4454bf97c44f1ebdf9986dd43
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085778"
---
# <a name="summary-information-on-a-project-quote"></a>ข้อมูลสรุปเกี่ยวกับใบเสนอราคาโครงการ

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_


บทความนี้อธิบายข้อมูลที่ใช้กับใบเสนอราคาโครงการ ซึ่งรวมถึงการตั้งค่าที่ส่งผลต่อรายการใบเสนอราคาทั้งหมดและข้อมูลเกี่ยวกับใบเสนอราคาที่สรุปในการแสดงรายการทั้งหมดเพื่อส่งเสริม KPI ของใบเสนอราคาโครงการ

ตารางต่อไปนี้แสดงฟิลด์ข้อมูลสรุปในใบเสนอราคาโครงการที่ไม่ซ้ำกันสำหรับ Dynamics 365 Project Operations หรือมีการเปลี่ยนแปลงที่สำคัญบางอย่างในลักษณะการทำงานจากใบเสนอราคาของ Dynamics 365 Sales

| **ฟิลด์** | **ตำแหน่งที่ตั้ง** | **ความเกี่ยวข้อง วัตถุประสงค์ และคำแนะนำ** | **ผลกระทบขั้นปลาย** |
| --- | --- | --- | --- |
| ประเภท | แท็บสรุป (ซ่อนไว้) | ฟิลด์ชุดตัวเลือกนี้มีตัวเลือกดังต่อไปนี้:</br>- ตามงาน (ใช้ได้เฉพาะเมื่อติดตั้ง Project Operations)</br>- ตามสินค้า (สามารถใช้ได้เฉพาะเมื่อติดตั้ง Project Operations และ Sales เท่านั้น)</br>- ตามการบำรุงรักษาบริการ (สามารถใช้งานได้เมื่อติดตั้ง Dynamics 365 Field Service) | เมื่อคุณใช้แอปพลิเคชัน Project Operations ค่าของฟิลด์นี้จะตั้งค่าเป็น **ตามงาน** โดยอัตโนมัติ การดำเนินการนี้จัดประเภทใบเสนอราคาเป็นใบเสนอราคาตามโครงการ ใบเสนอราคาควรอิงตามโครงการเพื่อเปิดใช้งานส่วนขยายและฟังก์ชันเฉพาะโครงการทั้งหมด |
| บริษัทที่เป็นเจ้าของ | สรุป | นิติบุคคลที่จะพิจารณาต้นทุนและรายได้ที่เกิดขึ้นจากโครงการนี้หรือโครงการที่เกี่ยวข้องกับใบเสนอราคานี้ เมื่อมีการสร้างใบเสนอราคาจากโอกาสทางการขาย ระบบจะคัดลอกฟิลด์นี้จากฟิลด์ที่เกี่ยวข้องในโอกาสทางการขาย | บริษัทที่เป็นเจ้าของเทียบเท่ากับแนวคิดของนิติบุคคลในโมดูล **การจัดการและการบัญชีโครงการ** ของ Project Operations ต้นทุนและรายได้ทั้งหมดที่เกิดขึ้นจากโครงการนี้จะรวมอยู่ในบัญชีแยกประเภททั่วไปของบริษัทที่เป็นเจ้าของ |
| ผู้ที่มีโอกาสเป็นลูกค้า | แท็บสรุปข้อมูล | การอ้างอิงถึงเรกคอร์ดบริษัทหรือบัญชีของลูกค้า ลูกค้าที่ถูกต้องที่จะอ้างอิงในใบเสนอราคาโครงการต้องได้รับการตั้งค่าเป็นลูกค้าในบริษัทที่เป็นเจ้าของใบเสนอราคา บริษัทที่เป็นเจ้าของแสดงรายการของนิติบุคคลและมีการตั้งค่าในโมดูล **การจัดการและการบัญชีโครงการ** ของ Project Operations เมื่อมีการสร้างใบเสนอราคาจากโอกาสทางการขาย ระบบจะคัดลอกฟิลด์นี้จากฟิลด์ที่เกี่ยวข้องในโอกาสทางการขาย | สกุลเงินในใบเสนอราคาโครงการมีการตั้งค่าเริ่มต้นตามสกุลเงินของลูกค้า อย่างไรก็ตาม รายการนี้สามารถเปลี่ยนแปลงก่อนบันทึกใบเสนอราคา |
| ผู้จัดการลูกค้าองค์กร | แท็บสรุปข้อมูล | ชื่อของผู้จัดการลูกค้าองค์กรสำหรับข้อตกลงนี้ เมื่อมีการสร้างใบเสนอราคาจากโอกาสทางการขาย ระบบจะคัดลอกฟิลด์นี้จากฟิลด์ที่เกี่ยวข้องในโอกาสทางการขาย | ผู้จัดการลูกค้าองค์กรมีหน้าที่จัดการความสัมพันธ์กับลูกค้าจนโครงการนี้เสร็จสมบูรณ์ ตามเรกคอร์ดทรัพยากรที่สามารถจองได้ที่ผูกกับผู้จัดการลูกค้าองค์กร หน่วยที่ทำสัญญาจะมีการกำหนดเป็นค่าเริ่มต้นในใบเสนอราคาโครงการ|
| หน่วยตามสัญญา | แท็บสรุปข้อมูล | หน่วยองค์กรที่รับผิดชอบการส่งมอบโครงการที่เกี่ยวข้องกับใบเสนอราคานี้ เมื่อมีการสร้างใบเสนอราคาจากโอกาสทางการขาย ระบบจะคัดลอกฟิลด์นี้จากฟิลด์ที่เกี่ยวข้องในโอกาสทางการขาย | หน่วยที่ทำสัญญาคือแผนกของบริษัทที่จะดำเนินโครงการหลังจากปิดข้อเสนอ ทุกหน่วยที่ทำสัญญามีสกุลเงิน และสกุลเงินนี้ใช้เพื่อรายงานต้นทุนโดยประมาณและต้นทุนจริงที่เกิดขึ้นระหว่างการดำเนินโครงการ |
| รายการราคาผลิตภัณฑ์ | แท็บสรุปข้อมูล | นี่คือรายการราคาที่ใช้เป็นราคาเริ่มต้นในรายการใบเสนอราคาตามผลิตภัณฑ์ รายการของตัวเลือกสำหรับฟิลด์นี้จะแสดงรายการของรายการราคาที่สกุลเงินของรายการราคาตรงกับสกุลเงินในใบเสนอราคา เมื่อมีการสร้างใบเสนอราคาจากโอกาสทางการขาย ระบบจะคัดลอกฟิลด์นี้จากฟิลด์ที่เกี่ยวข้องในโอกาสทางการขาย ฟิลด์นี้ในโอกาสทางการเป็นค่าเริ่มต้นจากเรกคอร์ดบัญชี แต่สามารถเปลี่ยนแปลงได้ | เมื่อชนะการเสนอราคา ค่าฟิลด์นี้จะมีการคัดลอกไปยังสัญญาโครงการที่สร้างขึ้น |
| สกุลเงิน | แท็บสรุปข้อมูล | ตัวเลือกนี้ระบุสกุลเงินที่จะใช้ในการรายงานมูลค่าของข้อตกลงนี้ นอกจากนี้ ยังเป็นสกุลเงินที่ลูกค้าจะได้รับการออกใบแจ้งหนี้หากชนะข้อตกลง เมื่อมีการสร้างใบเสนอราคาจากโอกาสทางการขาย ระบบจะคัดลอกฟิลด์นี้จากฟิลด์ที่เกี่ยวข้องในโอกาสทางการขาย ฟิลด์นี้ในโอกาสทางการเป็นค่าเริ่มต้นจากเรกคอร์ดบัญชี แต่ผู้ใช้สามารถเปลี่ยนแปลงได้  | หลังจากบันทึกใบเสนอราคาแล้ว ฟิลด์นี้จะไม่สามารถแก้ไขได้อีกต่อไป ค่านี้ใช้เป็นค่าเริ่มต้นรายการราคาของผลิตภัณฑ์และโครงการในใบเสนอราคา สกุลเงินในใบเสนอราคาใช้จับคู่สกุลเงินในรายการราคา |
| วงเงินที่ต้องไม่เกิน | แท็บสรุปข้อมูล | ตัวเลือกนี้แสดงขอบเขตที่เจรจาไว้สำหรับมูลค่าสุดท้ายที่ลูกค้าตกลงสำหรับข้อตกลงนี้ | ขอบเขตนี้ได้รับการประเมินในระหว่างการดำเนินการและใช้ได้กับการแสดงรายการและโครงการทั้งหมดที่เกี่ยวข้องกับข้อตกลงนี้ |
| วันที่ส่งมอบที่ร้องขอ | แท็บสรุปข้อมูล | เมื่อมีการสร้างใบเสนอราคาจากโอกาสทางการขาย ระบบจะคัดลอกฟิลด์นี้จากฟิลด์ที่เกี่ยวข้องในโอกาสทางการขาย | วันที่นี้ใช้เป็นวันที่สิ้นสุดในการสร้างกำหนดการใบแจ้งหนี้ |

ด้านล่างนี้คือแท็บและ KPI ที่มีอยู่ในใบเสนอราคาโครงการที่เป็นลักษณะเฉพาะของ Project Operations หรือมีการเปลี่ยนแปลงที่สำคัญบางอย่างในลักษณะการทำงานจากใบเสนอราคาของ Sales:

| **ฟิลด์** | **ตำแหน่งที่ตั้ง** | **ความเกี่ยวข้อง วัตถุประสงค์ และคำแนะนำ** |
| --- | --- | --- |
| การวิเคราะห์ความสามารถในการทำกำไร | แท็บบนใบเสนอราคา | ตารางจะแสดงเมตริกต่อไปนี้:</br>- ต้นทุนทั้งหมดที่คิดค่าธรรมเนียม</br></br>- ต้นทุนทั้งหมดที่ไม่คิดค่าธรรมเนียม</br>- ยอดรวมรายได้</br>- ยอดรวมรายได้ (ฐาน)</br>- กำไรขั้นต้น</br>- กำไรขั้นต้นที่ปรับปรุง|
| การเปรียบเทียบกับความคาดหมายของลูุกค้า | แท็บบนใบเสนอราคา | ตารางนี้จะแสดงเมตริกต่อไปนี้:</br>- การเสร็จสมบูรณ์โดยประมาณ</br>- การเสร็จสมบูรณ์ที่ต้องการ</br>- งบประมาณของลูกค้า</br>- มูลค่าที่เสนอราคา |
| การวิเคราะห์ใบเสนอราคา | แท็บบนใบเสนอราคา | แท็บนี้สรุป KPI อันดับต้นๆ ต่อไปนี้สำหรับใบเสนอราคาโครงการ</br>- การเปรียบเทียบกับความคาดหวังของลูกค้าสำหรับงบประมาณและกำหนดการ</br>- กำไรขั้นต้น</br>- กำไรขั้นต้นที่ปรับปรุง |