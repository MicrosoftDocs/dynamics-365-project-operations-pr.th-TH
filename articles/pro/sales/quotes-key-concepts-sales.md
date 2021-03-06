---
title: แนวคิดหลักของใบเสนอราคาโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการใช้ใบเสนอราคาโครงการใน Project Operations
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 64d2fd9bab9452d71e8cd194fbab70edadf00b93
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896304"
---
# <a name="project-quote-key-concepts"></a>แนวคิดหลักของใบเสนอราคาโครงการ

_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_


ต่อไปนี้เป็นแนวคิดหลักที่ควรทราบก่อนที่คุณจะเริ่มใช้ใบเสนอราคาโครงการใน Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>หน่วยที่ทำสัญญา

หน่วยที่ทำสัญญาหมายถึงส่วนงานหรือฝ่ายปฏิบัติการที่เป็นเจ้าของการส่งมอบโครงการ คุณสามารถตั้งค่าต้นทุนทรัพยากรสำหรับหน่วยที่ทำสัญญาแต่ละหน่วย เมื่อคุณระบุต้นทุนทรัพยากรสำหรับทรัพยากรในหน่วยที่ทำสัญญา คุณจะสามารถตั้งค่าอัตราต้นทุนที่แตกต่างกันสำหรับทรัพยากรที่หน่วยที่ทำสัญญานี้ยืมมาหรือส่วนงานหรือฝ่ายปฏิบัติการอื่นๆ ภายในองค์กร ข้อมูลเหล่านี้เรียกว่าราคาโอน การยืมทรัพยากร หรือราคาแลกเปลี่ยน เมื่อคุณตั้งค่าต้นทุนในการยืมทรัพยากรจากส่วนงานอื่นๆ คุณยังสามารถเลือกที่จะตั้งค่าอัตราต้นทุนเหล่านั้นในสกุลเงินของส่วนงานที่ให้ยืมได้

## <a name="cost-currency"></a>สกุลเงินต้นทุน

สกุลเงินต้นทุนใน Project Operations คือสกุลเงินที่รายงานต้นทุน สกุลเงินนี้ได้มาจากสกุลเงินที่แนบมากับฟิลด์ **หน่วยที่ทำสัญญา** ในใบเสนอราคา สัญญา และโครงการ คุณสามารถบันทึกต้นทุนในสกุลเงินใดก็ได้กับโครงการ อย่างไรก็ตาม มีการแปลงสกุลเงินจากต้นทุนในสกุลเงินที่บันทึกเป็นสกุลเงินต้นทุนของโครงการ

เนื่องจากอัตราแลกเปลี่ยนในแพลตฟอร์ม CDS ไม่สามารถเป็นวันที่ที่มีผลบังคับใช้ ผลรวมบนหน้าจอของต้นทุนอาจเปลี่ยนแปลงเมื่อเวลาผ่านไป หากคุณปรับปรุงอัตราแลกเปลี่ยนสกุลเงิน อย่างไรก็ตาม ค่าใช้จ่ายที่บันทึกไว้ในฐานข้อมูลจะไม่เปลี่ยนแปลง เนื่องจากจำนวนเงินจะถูกเก็บไว้ในสกุลเงินที่เกิดขึ้น

## <a name="sales-currency"></a>สกุลเงินการขาย

สกุลเงินการขายใน Project Operations คือสกุลเงินที่ใช้บันทึกและแสดงจำนวนเงินการขายโดยประมาณและตามจริง นอกจากนี้ ยังเป็นสกุลเงินที่ลูกค้าจะได้รับการออกใบแจ้งหนี้สำหรับข้อตกลงด้วย ในใบเสนอราคาโครงการ สกุลเงินการขายเป็นค่าเริ่มต้นจากเรกคอร์ดลูกค้าหรือบัญชี และสามารถเปลี่ยนแปลงได้เมื่อสร้างใบเสนอราคา หลังจากบันทึกใบเสนอราคาแล้ว จะไม่สามารถเปลี่ยนแปลงสกุลเงินการขายได้ รายการราคาของผลิตภัณฑ์และโครงการเป็นค่าเริ่มต้นในสกุลเงินการขายของใบเสนอราคา

ซึ่งแตกต่างจากต้นทุน มูลค่าการขายสามารถบันทึกได้ในสกุลเงินการขายเท่านั้น

## <a name="billing-method"></a>วิธีการเรียกเก็บเงิน

โดยทั่วไป โครงการจะมีรูปแบบการทำสัญญาแบบค่าธรรมเนียมคงที่และตามการใช้งาน ตัวเลือกนี้แสดงใน Project Operations เป็น **วิธีการเรียกเก็บเงิน** และมีสองค่าคือ เวลาและวัสดุ และราคาคงที่

- **เวลาและวัสดุ:** รูปแบบสัญญาตามการใช้งานซึ่งต้นทุนที่เกิดขึ้นแต่ละรายการได้รับการสนับสนุนจากรายได้ที่สอดคล้องกัน เมื่อคุณประมาณการหรือมีค่าใช้จ่ายเพิ่มขึ้น ยอดขายโดยประมาณและยอดขายจริงที่เกี่ยวข้องก็จะเพิ่มขึ้นเช่นกัน คุณสามารถระบุวงเงินที่ต้องไม่เกินสำหรับรายการใบเสนอราคาที่มีวิธีการเรียกเก็บเงินนี้ ซึ่งจะจำกัดรายได้จริง รายได้โดยประมาณจะไม่ได้รับผลกระทบจากวงเงินที่ต้องไม่เกิน
- **ราคาคงที่:** รูปแบบสัญญาแบบค่าธรรมเนียมคงที่ซึ่งระบุว่ามูลค่าการขายจะไม่ขึ้นอยู่กับต้นทุนที่เกิดขึ้น มูลค่าการขายเป็นแบบคงที่และไม่เปลี่ยนแปลงเมื่อคุณประมาณการหรือมีต้นทุนเพิ่มขึ้น

## <a name="project-price-lists"></a>ราคาตลาดของโครงการ

รายการราคาโครงการคือรายการราคาที่ใช้เป็นราคาเริ่มต้น ไม่ใช่อัตราต้นทุนสำหรับเวลา ค่าใช้จ่าย และส่วนประกอบอื่นๆ ที่เกี่ยวข้องกับโครงการ รายการราคาอาจมีได้หลายรายการและแต่ละรายการสามารถมีวันที่ที่มีผลบังคับใช้ของตนเองสำหรับใบเสนอราคาโครงการแต่ละใบ วันที่ที่มีผลบังคับใช้ที่ทับซ้อนกันของรายการราคาโครงการไม่รองรับใน Project Operations

## <a name="product-price-lists"></a>ราคาตลาดของผลิตภัณฑ์

รายการราคาผลิตภัณฑ์คือรายการราคาที่ใช้เป็นราคาเริ่มต้น ไม่ใช่อัตราต้นทุนสำหรับรายการตามผลิตภัณฑ์ในใบเสนอราคา มีรายการราคาผลิตภัณฑ์เพียงรายการเดียวต่อใบเสนอราคา

## <a name="transaction-classes"></a>คลาสธุรกรรม

Project Operations รองรับคลาสธุรกรรมสี่ประเภท:

- เวลา
- ค่าใช้จ่าย
- วัสดุ
- ค่าธรรมเนียม

ต้นทุนและมูลค่าการขายสามารถประมาณและเกิดขึ้นได้ในคลาสธุรกรรมเวลา ค่าใช้จ่าย และวัสดุ ค่าธรรมเนียมเป็นรายได้ประเภทเดียวของธุรกรรม

## <a name="work-entities-and-billing-entities"></a>เอนทิตีงานและเอนทิตีการเรียกเก็บเงิน

เอนทิตีที่แสดงถึงงาน ได้แก่ โครงการและงาน เอนทิตีที่แสดงถึงการเรียกเก็บเงิน ได้แก่ รายการใบเสนอราคา และรายละเอียดการให้บริการตามสัญญา คุณสามารถเชื่อมโยงเอนทิตีงานต่างๆ กับตัวเลือกการเรียกเก็บเงินได้โดยเชื่อมโยงกับใบเสนอราคาหรือรายละเอียดการให้บริการตามสัญญา

## <a name="multi-customer-deals"></a>ข้อตกลงที่มีลูกค้าหลายราย

ข้อตกลงที่มีลูกค้าหลายรายเกิดขึ้นเมื่อมีลูกค้ามากกว่าหนึ่งรายที่จะออกใบแจ้งหนี้ ตัวอย่างโดยทั่วไปได้แก่:

- **องค์กร OEM และคู่ค้า:** คู่ค้าและผู้ขายปลีกขายผลิตภัณฑ์ที่มีบริการเสริม โดยปกติจะเป็นสถานการณ์ที่เกิดระหว่างการทำข้อตกลงกับลูกค้าโดยเฉพาะ, OEM เสนอที่จะให้เงินทุนบางส่วนของโครงการ 

- **โครงการภาครัฐ:** หลายหน่วยงานของรัฐบาลท้องถิ่นตกลงที่จะให้ทุนแก่โครงการและได้รับการออกใบแจ้งหนี้ตามการแบ่งที่ตกลงกันไว้ก่อนหน้านี้ ตัวอย่างเช่น เขตการศึกษาและหน่วยงานของเมืองหรือรัฐบาลท้องถิ่นตกลงที่จะให้ทุนในการสร้างสระว่ายน้ำ

## <a name="invoice-schedules"></a>กำหนดการใบแจ้งหนี้

กำหนดการใบแจ้งหนี้เป็นข้อมูลเฉพาะสำหรับแต่ละรายการใบเสนอราคาและเป็นทางเลือก กำหนดการใบแจ้งหนี้มีการสร้างขึ้นตามวันที่เริ่มต้นและวันที่สิ้นสุดและความถี่ของใบแจ้งหนี้ กำหนดการใบแจ้งหนี้มีการใช้ในลำดับขั้นของสัญญาเมื่อมีการกำหนดค่ากระบวนการสร้างใบแจ้งหนี้อัตโนมัติ ในลำดับขั้นการเสนอราคา กำหนดการเป็นทางเลือก เมื่อกำหนดเวลาใบแจ้งหนี้มีการสร้างในลำดับขั้น **ใบเสนอราคา** กำหนดการจะถูกคัดลอกไปยังสัญญาโครงการที่สร้างขึ้นเมื่อชนะการเสนอราคาโครงการ

## <a name="changes-from-dynamics-365-sales-quote"></a>การเปลี่ยนแปลงจากใบเสนอราคาของ Dynamics 365 Sales:

ใบเสนอราคา Project Operations สร้างขึ้นจากใบเสนอราคาของ Dynamics 365 Sales อย่างไรก็ตาม มีความแตกต่างที่สำคัญบางประการในฟังก์ชันการทำงานที่คุณควรทราบ:

- การดำเนินการ **แก้ไข** และ **เปิดใช้งาน** ไม่รองรับ
- ใบเสนอราคา Project Operations มีสองประเภทที่แตกต่างกัน แบบหนึ่งใช้สำหรับโครงการและอีกแบบใช้สำหรับผลิตภัณฑ์
- ใบเสนอราคา Project Operations มีรูปแบบและองค์ประกอบ UI กฎธุรกิจ ตรรกะทางธุรกิจในปลั๊กอิน และสคริปต์ฝั่งไคลเอ็นต์ของตนเองที่แตกต่างจากใบเสนอราคาของ Sales

ด้วยเหตุผลเหล่านี้ จึงไม่แนะนำให้ใช้ใบเสนอราคาของ Sales และใบเสนอราคา Project Operations แทนกัน
