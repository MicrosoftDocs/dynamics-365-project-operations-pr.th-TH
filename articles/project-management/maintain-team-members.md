---
title: ดูแลสมาชิกในทีม
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการจองทรัพยากรที่มีชื่อให้กับทีมโครงการและการมอบหมายงาน
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085798"
---
# <a name="maintain-team-members"></a>ดูแลสมาชิกในทีม

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

คุณสามารถเพิ่มทรัพยากรที่มีชื่อให้กับทีมโครงการของคุณโดยการจองโดยตรงไปยังทีม

1. ใน Dynamics 365 Project Operations ไปที่ **โครงการ** และเลือกเปิดโครงการที่คุณกำลังทำการจอง
2. บนเพจ **โครงการ** บนแท็บ **ทีม** ให้เลือก **สร้าง** 
3. ในกล่องโต้ตอบ **สร้างสมาชิกทีมโครงการด่วน** ให้เลือกทรัพยากรที่จองได้ ฟิลด์ **บทบาท** จะเติมข้อมูลด้วยบทบาทเริ่มต้นของทรัพยากรถ้ามีการกำหนดไว้ คุณสามารถเปลี่ยนบทบาท 
4. เลือกวันที่เริ่มต้นและวันที่สิ้นสุดที่จะต้องใช้ทรัพยากรและเลือกวิธีการจัดสรรของความสามารถรองรับของทรัพยากร 
5. ในฟิลด์ **ผู้อนุมัติโครงการ** เลือก **ใช่** หากคุณต้องการให้สมาชิกทีมเป็นผู้อนุมัติโครงการ สมาชิกทีมจะสามารถอนุมัติรายการเวลาและค่าใช้จ่ายที่ส่งมาสำหรับโครงการนี้ 
6. เลือก **บันทึก**

ขณะนี้คุณสามารถกำหนดทรัพยากรที่จองให้กับงานในโครงการได้แล้ว บนเพจ **โครงการ** บนแท็บ **กำหนดการ** ให้มอบหมายงานให้กับทรัพยากรใหม่ ตัวเลือกทรัพยากรที่ถูกเปิดใช้จากฟิลด์ **ทรัพยากร** ในกริดงานจะแสดงสมาชิกในทีมที่คุณสามารถเลือกได้


ใน Project Operations การจองทรัพยากรและการมอบหมายงานไม่ได้เชื่อมโยงกันอย่างแน่นหนา เมื่อคุณใช้ตัวเลือกทรัพยากรในกำหนดการ คุณสามารถกำหนดงานให้กับสมาชิกในทีมด้วยชั่วโมงที่มากกว่าที่ครอบคลุมการจองของพวกเขาในโครงการ

ความแตกต่างระหว่างการจองสมาชิกทีมและการมอบหมายงานแสดงอยู่ในแท็บ **ทีม** และ **การกระทบยอดทรัพยากร** คุณยังสามารถกระทบยอดความแตกต่างระหว่างการจองและการมอบหมายทรัพยากรในระดับที่ละเอียดมากขึ้นได้

ใช้ตัวเลือกทรัพยากรบนแท็บ **กำหนดการ** เพื่อค้นหาและเลือกทรัพยากรที่สามารถจองได้ที่ยังไม่ได้เป็นส่วนหนึ่งของทีมโครงการ ทรัพยากรนี้จะแสดงในตัวเลือกทรัพยากรเป็น **ทรัพยากรอื่นๆ**

เมื่อคุณทำการเลือก ทรัพยากรจะถูกเพิ่มไปยังทีมโครงการและกำหนดให้กับงาน แต่จะไม่มีการสร้างการจอง

คุณสามารถใช้การขยายความสามารถในการจองของแท็บ **การกระทบยอด** หรือ **ตารางกำหนดการ** เพื่อจองความสามารถรองรับของทรัพยากรให้โครงการ

หลังจากที่สมาชิกทีมในโครงการของคุณมีการจองแล้ว คุณสามารถใช้ **รักษาการจอง** หรือ **ตารางกำหนดการ** เพื่อจัดการการจองของพวกเขาโดยตรง