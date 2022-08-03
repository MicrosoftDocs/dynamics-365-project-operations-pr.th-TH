---
title: รายการใบแจ้งหนี้ของผู้จัดจำหน่ายสำหรับประเภทค่าใช้จ่าย
description: บทความนี้อธิบายวิธีการบันทึกรายการใบแจ้งหนี้ของผู้จัดจำหน่ายสำหรับประเภทค่าใช้จ่าย
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ffad20b53344221ead9b6850ecdc1efd48d5b13
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925925"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>รายการใบแจ้งหนี้ของผู้จัดจำหน่ายสำหรับประเภทค่าใช้จ่าย

[!include [banner](../../includes/dataverse-preview.md)]

_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

ใบแจ้งหนี้ของผู้จัดจำหน่ายใน Microsoft Dynamics 365 Project Operations สามารถมีรายการใบแจ้งหนี้ของผู้จัดจำหน่ายสำหรับประเภทค่าใช้จ่ายได้ ผู้จัดการโครงการสามารถใช้รายการใบแจ้งหนี้ของผู้จัดจำหน่ายสำหรับประเภทค่าใช้จ่ายเพื่อบันทึกต้นทุนของบริการที่จัดซื้อเป็นประเภทค่าใช้จ่าย

รายการใบแจ้งหนี้ของผู้จัดจำหน่ายสำหรับประเภทค่าใช้จ่ายอาจหรืออาจไม่อ้างอิงรายการสัญญารับเหมารายย่อยสำหรับประเภทค่าใช้จ่าย ถ้ารายการใบแจ้งหนี้ของผู้จัดจำหน่ายสำหรับประเภทค่าใช้จ่ายอ้างอิงถึงสัญญารับเหมารายย่อย ผู้จัดการโครงการจะสามารถจับคู่และตรวจสอบค่าใช้จ่ายที่ออกใบแจ้งหนี้โดยรายการใบแจ้งหนี้ของผู้จัดจำหน่ายกับค่าใช้จ่ายที่บันทึกไว้ในประเภทค่าใช้จ่ายเหล่านี้ และได้รับการอนุมัติโดยผู้จัดการโครงการในโครงการ

ตารางต่อไปนี้แสดงข้อมูลเกี่ยวกับฟิลด์ในรายการใบแจ้งหนี้ของผู้จัดจำหน่ายสำหรับประเภทค่าใช้จ่าย

| ฟิลด์ | Description | ผลของฟังก์ชัน |
| --- | --- | --- |
| Name | ชื่อของรายการใบแจ้งหนี้ของผู้จัดจำหน่ายเพื่อช่วยระบุตัวตน | ชื่อนี้จะแสดงเป็นคอลัมน์แรกในการค้นหาทั้งหมดที่อิงตามใบแจ้งหนี้ของผู้จัดจำหน่าย |
| Description | คำอธิบายสั้นๆ เกี่ยวกับบริการที่กำลังออกใบแจ้งหนี้โดยผู้จัดจำหน่ายในรายการใบแจ้งหนี้ของผู้จัดจำหน่าย | None |
| สัญญารับเหมารายย่อย | สัญญารับเหมารายย่อยที่เริ่มสั่งบริการตั้งแต่แรก | เมื่อมีการเลือกสัญญารับเหมารายย่อยสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย รายการทั้งหมดในใบแจ้งหนี้ของผู้จัดจำหน่ายจะได้รับมาจากการเลือกนั้น ใบแจ้งหนี้ของผู้จัดจำหน่ายไม่สามารถมีรายการใบแจ้งหนี้ของผู้จัดจำหน่ายที่อ้างอิงถึงสัญญารับเหมารายย่อยที่แตกต่างกัน |
| รายการสัญญารับเหมารายย่อย | รายการสัญญารับเหมารายย่อยที่มีการสั่งบริการ รายการของรายการสัญญารับเหมารายย่อยที่สามารถเลือกได้จำกัดเฉพาะรายการในสัญญารับเหมารายย่อยที่เลือก | เมื่อมีการเลือกรายการสัญญารับเหมารายย่อยในรายการใบแจ้งหนี้ของผู้จัดจำหน่ายสำหรับประเภทค่าใช้จ่าย ค่าเริ่มต้นสำหรับฟิลด์ **โครงการ**, **งาน** และ **ประเภทธุรกรรม** จะถูกป้อนจากฟิลด์ที่เกี่ยวข้องในรายการสัญญารับเหมารายย่อย หากรายการสัญญารับเหมารายย่อยที่เลือกมีค่าในฟิลด์ **โครงการ**, **งานโครงการ** และ **ประเภทธุรกรรม** ค่าของฟิลด์ที่สอดคล้องกันในรายการใบแจ้งหนี้ของผู้จัดจำหน่ายไม่สามารถแตกต่างจากค่าเหล่านั้นได้ |
| วันที่ของธุรกรรม | วันที่ที่ต้นทุนจริงของรายการใบแจ้งหนี้ของผู้จัดจำหน่ายจะถูกบันทึกในโครงการ |None |
| ประเภทธุรกรรม | เลือก **ค่าใช้จ่าย** เพื่อบันทึกใบแจ้งหนี้ของผู้จัดจำหน่ายสำหรับประเภทค่าใช้จ่าย | ค่าของ **ค่าใช้จ่าย** ระบุว่ามีการใช้รายการใบแจ้งหนี้ของผู้จัดจำหน่ายเพื่อบันทึกยอดเงินในใบแจ้งหนี้สำหรับบริการที่จัดซื้อเป็นประเภทค่าใช้จ่าย |
| Project | ชื่อของโครงการที่มีการใช้บริการที่กำลังออกใบแจ้งหนี้ | ฟิลด์นี้จำเป็นต้องระบุและต้องไม่เว้นว่าง |
| งาน | ชื่อของงานโครงการที่มีการใช้บริการที่กำลังออกใบแจ้งหนี้ ฟิลด์นี้จะพร้อมใช้งานก็ต่อเมื่อเลือกโครงการ การเลือกงานโครงการเป็นทางเลือก | ถ้าฟิลด์นี้เว้นว่างไว้ ผู้จัดการโครงการสามารถจับคู่รายการใบแจ้งหนี้ของผู้จัดจำหน่ายกับค่าใช้จ่ายที่บันทึกไว้ในงานใดๆ ของโครงการ ถ้ารายการใบแจ้งหนี้ของผู้จัดจำหน่ายไม่ได้อ้างอิงถึงรายการสัญญารับเหมารายย่อย และฟิลด์นี้เว้นว่างไว้ ต้นทุนจริงที่สร้างขึ้นโดยรายการใบแจ้งหนี้ของผู้จัดจำหน่ายจะไม่ถูกเชื่อมโยงกับการขายจริงที่ยังไม่ได้เรียกเก็บเงินใดๆ ในกรณีนี้ หากมีการตั้งค่าการเรียกเก็บเงินตามงาน ต้นทุนอาจไม่สามารถออกใบแจ้งหนี้ให้กับลูกค้าปลายทางได้ |
| ประเภทธุรกรรม | ประเภทธุรกรรมที่กำลังออกใบแจ้งหนี้ คุณต้องสร้างประเภทค่าใช้จ่ายที่สอดคล้องกันสำหรับประเภทธุรกรรมที่เลือก | ชุดข้อมูลรวมของค่า **ประเภทธุรกรรม** และ **หน่วย** จะใช้เป็นค่าเริ่มต้นหรือค่าที่คำนวณสำหรับฟิลด์ **ราคาต่อหน่วย** ของรายการใบแจ้งหนี้ของผู้จัดจำหน่าย |
| ปริมาณ | ป้อนปริมาณที่ออกใบแจ้งหนี้โดยผู้จัดจำหน่ายในรายการใบแจ้งหนี้ |None|
| กลุ่มของหน่วยนับ | มีการป้อนค่าเริ่มต้นตามกลุ่มของหน่วยนับของประเภทธุรกรรมที่เลือก | None |
| หน่วย | ค่าเริ่มต้นคือหน่วยพื้นฐานของกลุ่มของหน่วยนับที่เลือก คุณสามารถเปลี่ยนค่านี้เพื่อยอมรับหน่วยใดๆ ในกลุ่มของหน่วยนับ | ชุดข้อมูลรวมของค่า **ประเภทธุรกรรม** และ **หน่วย** จะใช้เป็นค่าเริ่มต้นหรือค่าที่คำนวณสำหรับฟิลด์ **ราคาต่อหน่วย** ของรายการใบแจ้งหนี้ของผู้จัดจำหน่าย |
| ราคาต่อหน่วย | ราคาต่อหน่วยเริ่มต้นใช้ชุดรวมของค่า **ประเภทธุรกรรม** และ **หน่วย** จากรายการราคาโครงการที่ใช้กับวันที่ทำธุรกรรมของรายการใบแจ้งหนี้ของผู้จัดจำหน่าย | ถ้ามีการตั้งค่าราคาสำหรับรายการราคาโครงการที่เกี่ยวข้องในหน่วยที่แตกต่างจากหน่วยในรายการใบแจ้งหนี้ของผู้จัดจำหน่าย ระบบจะใช้การแปลงหน่วยเพื่อคำนวณราคาต่อหน่วย |
| ผลรวมย่อย | ฟิลด์แบบอ่านอย่างเดียวนี้มีการคำนวณเป็น *ปริมาณ* &times; *ราคาต่อหน่วย*  หากป้อนค่าทั้งในฟิลด์ **ปริมาณ** และฟิลด์ **ราคาต่อหน่วย** หากฟิลด์ใดฟิลด์หนึ่งหรือทั้งคู่ว่างเปล่า คุณสามารถป้อนค่าในฟิลด์นี้ได้| None |
| ภาษีขาย | ป้อนจำนวนเงินภาษีขาย | None |
| จำนวนรวม | ยอดเงินรวมของรายการใบแจ้งหนี้ของผู้จัดจำหน่าย รวมภาษี ฟิลด์นี้คำนวณเป็น *ผลรวมย่อย* + *ภาษีขาย* | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]