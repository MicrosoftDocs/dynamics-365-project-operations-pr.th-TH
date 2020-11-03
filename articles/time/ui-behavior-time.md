---
title: ลักษณะการทำงานของ UI รายการเวลา
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับลักษณะการทำงานของ UI สำหรับรายการเวลา
author: stsporen
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 86f805cd33f81e70bf9ae3c1fb20a1c310473604
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085867"
---
# <a name="time-entry-ui-behavior"></a>ลักษณะการทำงานของ UI รายการเวลา

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_


ตาราง **รายการเวลารายสัปดาห์** เป็นตัวควบคุมแบบกำหนดเองที่มีสองส่วนหลัก **มิติ** และ **ระยะเวลา**

## <a name="dimensions"></a>มิติ
ส่วน **มิติ** แสดงมิติที่สามารถป้อนข้อมูลเวลา มิติต่อไปนี้ได้รับการสนับสนุนแบบสำเร็จรูป:

  - Project
  - งานโครงการ
  - บทบาท
  - ประเภท
  - สถานะรายการ

ส่วน **มิติ** ไม่อนุญาตให้มีการแก้ไขแบบอินไลน์ ส่วนนี้ได้รับการสนับสนุนโดยมุมมองที่เปิดใช้งานฟิลด์แบบกำหนดเองที่จะเพิ่มลงในกริดการป้อนข้อมูลเวลารายสัปดาห์

## <a name="duration"></a>ระยะเวลา
ส่วนระยะเวลาแสดงวันในสัปดาห์เป็นส่วนหัวของคอลัมน์ ส่วนนี้อนุญาตให้มีการแก้ไขแบบอินไลน์ หลังจากที่มีการสร้างแถวรายการเวลาที่มีมิติที่เหมาะสม ผู้ใช้สามารถป้อนระยะเวลาที่พวกเขาใช้ในมิติเหล่านั้นได้อย่างรวดเร็ว

## <a name="create-a-new-time-entry"></a>สร้างรายการเวลาใหม่

1. ในตารางรายการเวลา เลือก **ใหม่** 
2. ในกล่องโต้ตอบ **สร้างรายการเวลาด่วน** เลือกวันที่ของรายการเวลา
3. ป้อนข้อมูลสำหรับมิติ **โครงการ** , **งานโครงการ** , **บทบาท** และ **ระยะเวลา** ข้อมูลนี้ควรเพิ่มเป็นนาที ชั่วโมง หรือวันโดยการพิมพ์ **ชม.** , **นาที** หรือ **วัน** พร้อมกับตัวเลข 
4. ป้อนคำอธิบายสำหรับการป้อนข้อมูลและข้อคิดเห็นที่สามารถใช้ร่วมกันภายนอกสำหรับการป้อนข้อมูลเวลา 

เมื่อคุณบันทึกรายการข้อมูล ค่าที่ป้อนจะปรากฏในส่วน **มิติ** ข้อมูลที่ป้อนในฟิลด์ **ระยะเวลา** จะปรากฏขึ้นในวันที่ที่สร้างรายการเวลา

ฟิลด์การค้นหาได้รับการสนับสนุนโดยมุมมองของระบบ ตัวอย่างเช่น หลังจากที่ผู้ใช้ป้อนโครงการ ฟิลด์ **งานโครงการ** ถูกตั้งค่าเป็นมุมมอง **คัดลอก** ตามค่าเริ่มต้น ถ้าต้องการสร้างรายการเวลาสำหรับงานที่ไม่ได้กำหนดให้กับผู้ใช้ให้เลือก **เปลี่ยนมุมมอง** ในกล่องโต้ตอบการค้นหา แล้วเลือกมุมมอง **งานโครงการที่ใช้งานอยู่ทั้งหมด**

## <a name="edit-a-time-entry"></a>แก้ไขรายการเวลา 
รายละเอียดจากบางฟิลด์ในเพจรายการเวลา เช่น **คำอธิบาย** และ **ข้อคิดเห็นภายนอก** จะไม่แสดงในกริดรายการเวลารายสัปดาห์ แต่ ตัวบ่งชี้รูปสามเหลี่ยมขนาดเล็กจะปรากฏในเซลล์ **ระยะเวลา** ที่มีรายละเอียดเพิ่มเติมเหล่านี้ 

1. หากต้องการแก้ไขรายการเวลา ให้เลือกเซลล์ที่คุณต้องการปรับปรุงในรายการเวลา
2. เลือก **แก้ไขรายละเอียด** เพื่อปรับปรุงข้อมูลในบานหน้าต่าง **รูปแบบหลักของรายการเวลา** 

## <a name="copy-a-time-entry-row"></a>คัดลอกแถวของรายการเวลา
หลังจากที่มีการสร้างแถว คุณสามารถเลือก **คัดลอกแถว** เพื่อคัดลอกแถวทั้งหมดไปยังแถวใหม่ เมื่อแถวถูกคัดลอกด้วยวิธีนี้ มิติและระยะเวลาจะถูกคัดลอกด้วย นอกจากนี้ คุณยังสามารถเลือก **แก้ไขแถว** เพื่อปรับปรุงค่ามิติและระยะเวลาในส่วน **ระยะเวลา**

## <a name="open-a-time-entry-behavior"></a>เปิดลักษณะรายการเวลา
ในการสนับสนุนรายการที่ดีที่สุดและรวดเร็วในฟิลด์ที่โดดเด่นที่สุด กริดรายการเวลารายสัปดาห์จะแสดงชุดย่อยของมิติข้อมูลและระยะเวลาที่เลือก หากต้องการดูรายละเอียดทั้งหมดของการป้อนข้อมูลครั้งเดียว ภายใต้ **แก้ไขรายการ** ให้เลือก **เปิด**

## <a name="submit-a-time-entry"></a>ส่งรายการเวลา
คุณสามารถส่งรายการเวลาเดียวหรือกลุ่มของรายการเวลาโดยการเลือกบล็อกของเซลล์หรือแถวรายการเวลาทั้งหมด และจากนั้นเลือก **ส่ง** รายการเวลาที่ส่งจะปรากฏเป็นรายการที่ค้างอยู่รอการอนุมัติในเพจ **การอนุมัติ** ของผู้อนุมัติ หลังจากที่ส่งรายการเวลาเสร็จเรียบร้อยแล้ว จะไม่สามารถแก้ไขได้

## <a name="recall-a-time-entry"></a>เรียกคืนรายการเวลา
คุณสามารถเรียกคืนรายการเวลาที่คุณส่งได้ คุณสามารถเรียกคืนการป้อนข้อมูลครั้งเดียว บล็อกของรายการเวลา หรือแถวของรายการเวลาทั้งหมด รายการเวลาที่เรียกคืนสามารถแก้ไขได้

## <a name="time-entry-status"></a>สถานะรายการเวลา

- **แบบร่าง** : รายการเวลาใหม่จะมีการกำหนดสถานะเป็น **แบบร่าง** โดยอัตโนมัติ สามารถลบได้เฉพาะรายการเวลาที่มีสถานะเป็น **ฉบับร่าง** เท่านั้น
- **ส่งแล้ว** : เมื่อมีการส่งรายการเวลา สถานะจะได้รับการปรับปรุงเป็น **ส่งแล้ว** 
- **อนุมัติแล้ว** : เมื่อการส่งรายการเวลาที่ส่งไปแล้วได้รับการอนุมัติ สถานะจะถูกปรับปรุงเป็น **อนุมัติแล้ว** 
- **ส่งคืนแล้ว** : ถ้ารายการเวลาถูกปฏิเสธ สถานะจะถูกปรับปรุงเป็น **ส่งคืนแล้ว** และรายการจะพร้อมใช้งานสำหรับการแก้ไขและการส่งใหม่ 

## <a name="view-rejection-comments"></a>ดูข้อคิดเห็นในการปฏิเสธ
เมื่อรายการเวลาได้รับการปฏิเสธโดยผู้อนุมัติ ผู้อนุมัติอาจเพิ่มข้อคิดเห็นเพื่อช่วยให้ทรัพยากรเข้าใจเหตุผลของการปฏิเสธ หากต้องการดูข้อคิดเห็นการปฏิเสธสำหรับรายการเวลา ให้เลือก **รายการที่เปิด** ข้อคิดเห็นการปฏิเสธจะแสดงในเส้นเวลา ผู้ใช้สามารถตอบกลับข้อคิดเห็นในการปฏิเสธก่อนที่จะส่งรายการอีกครั้ง

## <a name="copy-week"></a>คัดลอกสัปดาห์
หลังจากสร้างรายการเวลาสองสามรายการ ผู้ใช้สามารถสร้างรายการเวลาหลายรายการในเวลาเดียวกันได้

1. ในฟอร์ม **รายการเวลา** เลือก **คัดลอกสัปดาห์** เพื่อสร้างรายการเวลาเพิ่มเติมจำนวนมาก 
2. ในกล่องโต้ตอบ **คัดลอก** ในส่วน **รอบระยะเวลาเริ่มต้น** ใช้ฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** เพื่อกำหนดช่วงวันที่ที่จะคัดลอกรายการเวลา 
3. ในส่วน **รอบระยะเวลาสิ้นสุด** ในฟิลด์ **วันที่เริ่มต้น** ให้ระบุวันที่ที่ต้องการสร้างรายการเวลาให้ 
4. เลือก **คัดลอก** สำหรับวันที่ที่ระบุในรอบระยะเวลา **รอบระยะเวลาสิ้นสุด** สำเนาของรายการเวลาสำหรับวันที่สอดคล้องกันของสัปดาห์ใน **รอบระยะเวลาเริ่มต้น** จะถูกสร้าง ตัวอย่างเช่น รายการเวลาสำหรับวันจันทร์ของสัปดาห์ที่ผ่านมาจะถูกคัดลอกไปยังวันจันทร์ของสัปดาห์ที่ได้ระบุไว้ให้เป็น **รอบระยะเวลาสิ้นสุด**

## <a name="import"></a>นำเข้า
กระบวนการพื้นฐานเดียวกันจะใช้ในการนำเข้าจากการจองงาน มอบหมาย และการแลกเปลี่ยน คุณสามารถระบุช่วงวันที่ที่มีการนำเข้าการจอง และเลือกการจองอย่างชัดเจนที่ควรคัดลอกลงในรายการเวลาแบบร่าง 