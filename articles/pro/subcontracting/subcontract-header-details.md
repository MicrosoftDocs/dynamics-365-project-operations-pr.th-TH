---
title: รายละเอียดส่วนหัวสำหรับการรับเหมารายย่อย
description: หัวข้อนี้อธิบายฟังก์ชันการทำงานที่มีให้ในส่วนหัวการรับเหมารายย่อยใน Project Operations
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee863d31b45e7de962488fe804202ddfe580eb04
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501349"
---
# <a name="header-details-for-subcontracts"></a>รายละเอียดส่วนหัวสำหรับการรับเหมารายย่อย

[!include [banner](../../includes/dataverse-preview.md)]

_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

หัวข้อนี้อธิบายฟังก์ชันการทำงานที่มีให้ในส่วนหัวการรับเหมารายย่อยใน Dynamics 365 Project Operations

ขณะที่ผู้จัดการโครงการวางแผนและดำเนินโครงการ พวกเขาอาจจ้างผู้รับเหมารายย่อยและซื้อผลิตภัณฑ์และบริการจากผู้จัดจำหน่าย เมื่อผู้จัดการโครงการต้องการซื้อผลิตภัณฑ์หรือบริการ พวกเขาสามารถสร้างการรับเหมารายย่อยใน Project Operations

เพื่อสร้างการรับเหมารายย่อย ให้ทำตามขั้นตอนต่อไปนี้

1. ในบานหน้าต่างนำทาง เลือก **การรับเหมารายย่อย** และบนเพจ **การรับเหมาราย่อย** เลือก **ใหม่**
2. ป้อนข้อมูลที่จำเป็นให้ครบ จากนั้นเลือก **บันทึก**

    ตารางต่อไปนี้แสดงข้อมูลเกี่ยวกับฟิลด์ในเพจ **ส่วนหัวการรับเหมารายย่อย**

    | ฟิลด์ | รายละเอียด |ผลของฟังก์ชัน |
    |---|------|---| 
    | ชื่อ | ชื่อของการรับเหมารายย่อย | ในรายการแบบหล่นลงของการรับเหมารายย่อยทั้งหมด ชื่อของการรับเหมารายย่อยจะแสดงอยู่ในคอลัมน์แรกเพื่อช่วยคุณระบุการรับเหมารายย่อย | 
    | รายละเอียด | คำอธิบายสั้นๆ เกี่ยวกับบริการและผลิตภัณฑ์ที่กำลังจะซื้อในการรับเหมารายย่อย | ไม่มี |
    | ผู้จัดจำหน่าย | ชื่อบริษัทที่จะซื้อผลิตภัณฑ์และบริการ เรกคอร์ดบัญชีนี้มีชนิดความสัมพันธ์เป็น **ผู้จัดจำหน่าย** หรือ **ผู้จัดหา** | โดยอิงตามผู้จัดจำหน่ายที่เลือก จะมีการป้อนค่าเริ่มต้นโดยอัตโนมัติสำหรับฟิลด์ต่อไปนี้:<br/> **• สกุลเงิน** </br> **• รายการราคา** </br> **• เงื่อนไขการชำระเงิน**</br> **• ที่อยู่การชำระเงิน**</br> **• ที่อยู่สำหรับเรียกเก็บเงิน**</br> **• ชื่อผู้ถูกเรียกเก็บเงิน** </br>**• ผู้จัดการบัญชีผู้จัดจำหน่าย**|
    | วันที่ของการรับเหมารายย่อย | วันที่สร้างการรับเหมารายย่อย | วันที่ของการรับเหมารายย่อยจะใช้เพื่อเลือกรายการราคาซื้อที่ถูกต้องจากรายการราคาที่แนบกับผู้จัดจำหน่ายที่เกี่ยวข้องหรือจากพารามิเตอร์โครงการ |
    | คำอธิบายรายการของสถานะ | สถานะของการรับเหมารายย่อย | สถานะจะกำหนดว่าการรับเหมารายย่อยอยู่ที่ส่วนใดในกระบวนการทางธุรกิจและจะสามารถแก้ไขได้หรือไม่ <br/>ค่ารวมถึง:<br>• **แบบร่าง**: การรับเหมารายย่อยสามารถแก้ไขได้ คุณแก้ไขได้เฉพาะการรับเหมารายย่อยที่มีสถานะ **แบบร่าง**<br/>• **ยืนยันแล้ว**: การเจรจากับผู้จัดจำหน่ายเสร็จสมบูรณ์และการรับเหมารายย่อยงได้รับอนุมัติให้ส่งมอบ <br/>• **ปิดแล้ว**: การส่งมอบในการรับเหมารายย่อยเสร็จสมบูรณ์<br/>• **ถูกยกเลิก**: การรับเหมารายย่อยถูกยกเลิกและไม่มีการวางแผนการส่งมอบ  | 
    | สกุลเงิน | สกุลเงินที่ซื้อผลิตภัณฑ์และบริการ จะมีการป้อนค่าเริ่มต้นโดยอัตโนมัติจากบัญชีผู้จัดจำหน่าย แต่สามารถเปลี่ยนแปลงได้ | สกุลเงินของการรับเหมารายย่อยจะใช้เพื่อเลือกรายการราคาซื้อจากรายการราคาที่แนบกับผู้จัดจำหน่ายที่เกี่ยวข้องหรือจากพารามิเตอร์โครงการ รายการราคาในสกุลเงินอื่นไม่สามารถเชื่อมโยงกับการรับเหมารายย่อยได้ ต้นทุนของเวลา ค่าใช้จ่าย และวัสดุที่ทรัพยากรของผู้จัดจำหน่ายส่งมอบจากการรับเหมารายย่อยนี้จะมีการบันทึกในสกุลเงินนี้ในโครงการ หลังจากบันทึกเรกคอร์ดการรับเหมารายย่อยแล้ว สกุลเงินในการรับเหมารายย่อยจะไม่สามารถเปลี่ยนแปลงได้|
    | หน่วยที่ทำสัญญา | แผนกของบริษัทที่ทำสัญญาซื้อหรือทำสัญญารับเหมารายย่อยกับผู้จัดจำหน่าย | ไม่มี |
    | เงื่อนไขการชำระเงิน | เงื่อนไขการชำระเงินในใบแจ้งหนี้ของผู้จัดจำหน่ายที่ออกให้ในการรับเหมารายย่อยนี้ จะมีการป้อนค่าเริ่มต้นโดยอัตโนมัติจากเรกคอร์ดบัญชีผู้จัดจำหน่าย | เงื่อนไขการชำระเงินจากการรับเหมารายย่อยจะมีการคัดลอกไปยังใบแจ้งหนี้ของผู้จัดจำหน่ายทั้งหมดที่เกี่ยวข้องกับการรับเหมารายย่อยนี้ คุณสามารถปรับปรุงเงื่อนไขการชำระเงินได้หากการรับเหมารายย่อยมีสถานะเป็น **แบบร่าง** | 
    | ที่อยู่การชำระเงิน | ที่อยู่ของผู้จัดจำหน่ายที่ต้องส่งการชำระเงินไปให้ จะมีการป้อนค่าเริ่มต้นโดยอัตโนมัติจากเรกคอร์ดบัญชีผู้จัดจำหน่าย | ที่อยู่การชำระเงินจากการรับเหมารายย่อยจะมีการคัดลอกเป็นที่อยู่การชำระเงินไปยังใบแจ้งหนี้ของผู้จัดจำหน่ายทั้งหมดที่สร้างขึ้นสำหรับการรับเหมารายย่อยนี้ คุณสามารถปรับปรุงที่อยู่การชำระเงินได้หากการรับเหมารายย่อยมีสถานะเป็น **แบบร่าง**|
    | ชื่อผู้ถูกเรียกเก็บเงิน | ชื่อบุคคลหรือแผนกในบริษัทของผู้จัดจำหน่ายที่จะส่งใบแจ้งหนี้ จะมีการป้อนค่าเริ่มต้นโดยอัตโนมัติจากเรกคอร์ดบัญชีผู้จัดจำหน่าย | ค่า **ชื่อผู้ถูกเรียกเก็บเงิน** จากการรับเหมารายย่อยจะมีการคัดลอกไปยังใบแจ้งหนี้ของผู้จัดจำหน่ายทั้งหมดที่เกี่ยวข้องกับการรับเหมารายย่อยนี้ คุณสามารถปรับปรุงฟิลด์นี้ได้หากการรับเหมารายย่อยมีสถานะเป็น **แบบร่าง**|
    | ที่อยู่สำหรับเรียกเก็บเงิน | ที่อยู่ที่ใช้ในใบแจ้งหนี้จากผู้จัดจำหน่าย จะมีการป้อนค่าเริ่มต้นโดยอัตโนมัติจากเรกคอร์ดบัญชีผู้จัดจำหน่าย | ที่อยู่นี้เป็นที่อยู่ "ใบแจ้งหนี้จาก" ในใบแจ้งหนี้ของผู้จัดจำหน่ายที่สร้างขึ้นสำหรับการรับเหมารายย่อยนี้ |
    | ผลรวมย่อย | หากการรับเหมารายย่อยไม่มีรายการ ให้ป้อนยอดรวมย่อยของใบสั่งก่อนหักภาษี ถ้าการรับเหมารายย่อยมีรายการ ฟิลด์นี้เป็นแบบอ่านอย่างเดียว จำนวนเงินที่แสดงคือยอดรวมย่อยจากทุกรายการในการรับเหมารายย่อย | ไม่มี |
    | ภาษีรวม | หากการรับเหมารายย่อยไม่มีรายการ ให้ป้อนยอดรวมภาษีในการรับเหมารายย่อยนี้ ถ้าการรับเหมารายย่อยมีรายการ ฟิลด์นี้เป็นแบบอ่านอย่างเดียว จำนวนเงินที่แสดงคือผลรวมของจำนวนเงินภาษีจากทุกรายการในการรับเหมารายย่อย | ไม่มี |
    | จำนวนรวม | ฟิลด์ที่มีการคำนวณนี้แสดงจำนวนเงินรวมของการรับเหมารายย่อยหลังรวมภาษีแล้ว | ไม่มี |
    | วันที่ที่ยืนยัน | วันที่ที่ยืนยันการรับเหมารายย่อย | ไม่มี |
    | ขอโดย | โดยค่าเริ่มต้น ฟิลด์นี้มีการกำหนดเป็นชื่อผู้ใช้ที่สร้างการรับเหมารายย่อย อย่างไรก็ตาม ผู้สร้างการรับเหมารายย่อยสามารถเปลี่ยนค่าเพื่อระบุบุคคลที่พวกเขากำลังสร้างการรับเหมารายย่อยในนามได้ | ไม่มี |
    | ผู้จัดการบัญชีผู้จัดจำหน่าย | ชื่อของผู้ติดต่อหลักของบัญชีผู้จัดจำหน่าย จะมีการป้อนค่าเริ่มต้นโดยอัตโนมัติจากเรกคอร์ดบัญชีผู้จัดจำหน่าย คุณสามารถเลือกผู้ติดต่ออื่นเป็นผู้จัดการบัญชีผู้จัดจำหน่ายของการรับเหมารายย่อยได้ | คุณสามารถตั้งค่าการแจ้งเตือนทางอีเมลเพื่อแจ้งผู้ติดต่อเมื่อมีการเปลี่ยนแปลงกับการรับเหมารายย่อย ซึ่งเป็นผลมาจากการเจรจาต่อรองราคาได้ |