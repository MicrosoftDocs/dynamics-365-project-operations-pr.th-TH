---
title: รายละเอียดส่วนหัวสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย
description: บทความนี้อธิบายฟังก์ชันการทำงานที่มีให้ในส่วนหัวสำหรับใบแจ้งหนี้ของผู้จัดจำหน่ายใน Microsoft Dynamics 365 Project Operations
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 95f84f2d2a357abbd8d507705412a0434b44f658
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929881"
---
# <a name="header-details-for-vendor-invoices"></a>รายละเอียดส่วนหัวสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย

[!include [banner](../../includes/dataverse-preview.md)]

_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

บทความนี้อธิบายฟังก์ชันการทำงานที่มีให้ในส่วนหัวสำหรับใบแจ้งหนี้ของผู้จัดจำหน่ายใน Microsoft Dynamics 365 Project Operations

เนื่องจากผู้จัดการโครงการวางแผนและดำเนินโครงการ พวกเขาอาจจ้างผู้รับเหมารายย่อยและซื้อผลิตภัณฑ์และบริการจากผู้จัดจำหน่าย ในระหว่างการดำเนินโครงการ ต้นทุนจะเกิดขึ้นจากประเภทการบริการ วัสดุ และค่าใช้จ่ายที่จัดหาจากสัญญารับเหมารายย่อยกับผู้จัดจำหน่าย ผู้จัดจำหน่ายออกใบแจ้งหนี้ค่าใช้จ่ายเหล่านี้ให้กับโครงการโดยการสร้างใบแจ้งหนี้ของผู้จัดจำหน่าย

ตารางต่อไปนี้แสดงข้อมูลเกี่ยวกับฟิลด์ในส่วนหัวของใบแจ้งหนี้ของผู้จัดจำหน่ายใน Project Operations

| ฟิลด์ | Description | ผลของฟังก์ชัน |
| --- | --- | --- |
| Name | ชื่อของใบแจ้งหนี้ของผู้จัดจำหน่าย | ในรายการดรอปดาวน์ของใบแจ้งหนี้ของผู้จัดจำหน่ายทั้งหมด ชื่อของใบแจ้งหนี้ของผู้จัดจำหน่ายจะแสดงอยู่ในคอลัมน์แรกเพื่อช่วยคุณระบุใบแจ้งหนี้ของผู้จัดจำหน่าย โดยค่าเริ่มต้น เมื่อมีการสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายจากสัญญารับเหมารายย่อย ฟิลด์ **ชื่อ** ของใบแจ้งหนี้ของผู้จัดจำหน่ายถูกตั้งค่าเป็นค่าที่ประกอบด้วยชื่อของสัญญารับเหมาราย่อยพร้อมกับวันที่ปัจจุบัน |
| Description | คำอธิบายสั้นๆ เกี่ยวกับบริการและผลิตภัณฑ์ที่กำลังออกใบแจ้งหนี้ในใบแจ้งหนี้ของผู้จัดจำหน่าย | None |
| ผู้จัดจำหน่าย | ชื่อบริษัทที่ออกใบแจ้งหนี้สำหรับสินค้าและบริการ บริษัทนี้ควรเป็นเรกคอร์ดบัญชีที่มีชนิดความสัมพันธ์ **ผู้จัดจำหน่าย** หรือ **ผู้จัดหา** | <p>โดยอิงตามผู้จัดจำหน่ายที่เลือก จะมีการป้อนค่าเริ่มต้นโดยอัตโนมัติในฟิลด์ต่อไปนี้:</p><ul><li>สกุลเงิน</li><li>รายการราคา</li><li>เงื่อนไขการชำระเงิน</li><li>ที่อยู่การชำระเงิน</li></ul> |
| สัญญารับเหมารายย่อย | การอ้างอิงถึงสัญญารับเหมารายย่อยสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย | <p>โดยอิงตามสัญญารับเหมารายย่อยที่เลือก จะมีการป้อนค่าเริ่มต้นโดยอัตโนมัติในฟิลด์ต่อไปนี้:</p><ul><li>สกุลเงิน</li><li>รายการราคา</li><li>เงื่อนไขการชำระเงิน</li><li>ที่อยู่การชำระเงิน</li></ul><p>สัญญารับเหมารายย่อยที่เลือกในส่วนหัวของใบแจ้งหนี้ของผู้จัดจำหน่ายจะถูกป้อนตามค่าเริ่มต้นในรายการใบแจ้งหนี้ของผู้จัดจำหน่าย และไม่สามารถเปลี่ยนแปลงได้ที่นั่น</p> |
| วันที่ในใบแจ้งหนี้ | วันที่สำหรับต้นทุนจริงที่จะถูกสร้างขึ้นเมื่อใบแจ้งหนี้ของผู้จัดจำหน่ายได้รับการยืนยัน | วันที่ของใบแจ้งหนี้ยังใช้เพื่อเลือกรายการราคาซื้อที่ถูกต้องจากรายการราคาที่แนบกับผู้จัดจำหน่ายที่เกี่ยวข้องหรือจากพารามิเตอร์โครงการด้วย |
| เหตุผลของสถานะ | สถานะของใบแจ้งหนี้ของผู้จัดจำหน่าย | <p>สถานะจะกำหนดว่าใบแจ้งหนี้ของผู้จัดจำหน่ายอยู่ที่ส่วนใดในกระบวนการทางธุรกิจและจะสามารถแก้ไขได้หรือไม่ นี่คือค่าบางส่วนที่ใช้ได้:</p><ul><li>**แบบร่าง** – ใบแจ้งหนี้ของผู้จัดจำหน่ายสามารถแก้ไขได้</li><li>**ยืนยันแล้ว** – ใบแจ้งหนี้ของผู้จัดจำหน่ายได้รับการตรวจสอบและยืนยันแล้ว ไม่สามารถแก้ไขหรือลบใบแจ้งหนี้ของผู้จัดจำหน่ายที่อยู่ในสถานะนี้</li><li>**อยู่ระหว่างดำเนินการ** – กำลังตรวจสอบใบแจ้งหนี้ของผู้จัดจำหน่าย ไม่สามารถแก้ไขใบแจ้งหนี้ของผู้จัดจำหน่ายที่อยู่ในสถานะนี้ แต่สามารถลบได้</li><li>**ถูกยกเลิก** – ใบแจ้งหนี้ของผู้จัดจำหน่ายถูกยกเลิก ไม่สามารถแก้ไขหรือลบใบแจ้งหนี้ของผู้จัดจำหน่ายที่อยู่ในสถานะนี้</li></ul> |
| สกุลเงิน | สกุลเงินที่ผู้จัดจำหน่ายออกใบแจ้งหนี้สำหรับผลิตภัณฑ์และบริการในใบแจ้งหนี้ของผู้จัดจำหน่าย | ในใบแจ้งหนี้ของผู้จัดจำหน่ายที่อ้างอิงถึงสัญญารับเหมารายย่อย สกุลเงินของสัญญารับเหมารายย่อยจะถูกป้อนโดยค่าเริ่มต้นเป็นสกุลเงินของใบแจ้งหนี้ของผู้จัดจำหน่าย ในใบแจ้งหนี้ของผู้จัดจำหน่ายที่ไม่อ้างอิงสัญญารับเหมารายย่อย ค่าเริ่มต้นจะถูกป้อนจากเรกคอร์ดบัญชีผู้จัดจำหน่ายและสามารถเปลี่ยนแปลงได้ หลังจากบันทึกใบแจ้งหนี้ของผู้จัดจำหน่ายแล้ว สกุลเงินจะไม่สามารถแก้ไขได้อีกต่อไป |
| หน่วยที่ทำสัญญา | แผนกของบริษัทที่รับผิดชอบในการรับบริการและ/หรือสินค้าจากผู้จัดจำหน่าย | None |
| เงื่อนไขการชำระเงิน | เงื่อนไขการชำระเงินในใบแจ้งหนี้ของผู้จัดจำหน่ายที่ออกใบแจ้งหนี้ จะมีการป้อนค่าเริ่มต้นโดยอัตโนมัติจากเรกคอร์ดบัญชีผู้จัดจำหน่าย | เงื่อนไขการชำระเงินจากสัญญารับเหมารายย่อยจะมีการคัดลอกไปยังใบแจ้งหนี้ของผู้จัดจำหน่ายทั้งหมดที่เกี่ยวข้องกับสัญญารับเหมารายย่อย คุณสามารถปรับปรุงเงื่อนไขการชำระเงินได้หากใบแจ้งหนี้ของผู้จัดจำหน่ายมีสถานะเป็น **แบบร่าง** |
| ที่อยู่การชำระเงิน | ที่อยู่ของผู้จัดจำหน่ายที่ต้องส่งการชำระเงินไปให้ จะมีการป้อนค่าเริ่มต้นโดยอัตโนมัติจากเรกคอร์ดบัญชีผู้จัดจำหน่าย | ที่อยู่การชำระเงินจากสัญญารับเหมารายย่อยจะมีการคัดลอกเป็นที่อยู่การชำระเงินไปยังใบแจ้งหนี้ของผู้จัดจำหน่ายทั้งหมดที่สร้างขึ้นสำหรับสัญญารับเหมารายย่อยนั้น คุณสามารถปรับปรุงที่อยู่การชำระเงินได้หากใบแจ้งหนี้ของผู้จัดจำหน่ายมีสถานะเป็น **แบบร่าง** |
| ผลรวมย่อย | หากใบแจ้งหนี้ของผู้จัดจำหน่ายไม่มีรายการ ให้ป้อนยอดรวมย่อยของใบแจ้งหนี้ก่อนหักภาษี ถ้าใบแจ้งหนี้ของผู้จัดจำหน่ายมีรายการ ฟิลด์นี้จะเป็นแบบอ่านอย่างเดียว ในกรณีนี้ จำนวนเงินที่แสดงคือยอดรวมย่อยจากทุกรายการในใบแจ้งหนี้ของผู้จัดจำหน่าย | None |
| ภาษีรวม | หากใบแจ้งหนี้ของผู้จัดจำหน่ายไม่มีรายการ ให้ป้อนยอดรวมภาษีของสัญญารับเหมารายย่อย ถ้าใบแจ้งหนี้ของผู้จัดจำหน่ายมีรายการ ฟิลด์นี้จะเป็นแบบอ่านอย่างเดียว ในกรณีนี้ จำนวนเงินที่แสดงคือผลรวมของยอดเงินภาษีจากทุกรายการในใบแจ้งหนี้ของผู้จัดจำหน่าย | None |
| จำนวนรวม | ฟิลด์ที่มีการคำนวณนี้แสดงยอดเงินรวมของใบแจ้งหนี้ของผู้จัดจำหน่ายหลังจากรวมภาษีแล้ว | None |

> [!NOTE]
> ฟิลด์ต่อไปนี้ในใบแจ้งหนี้ของผู้จัดจำหน่ายไม่สามารถเปลี่ยนแปลงได้หลังจากที่บันทึกใบแจ้งหนี้ของผู้จัดจำหน่ายแล้ว: **ผู้จัดจำหน่าย**, **สัญญารับเหมารายย่อย**, **สกุลเงิน**, **หน่วยที่ทำสัญญา** และ **เงื่อนไขการชำระเงิน** หากจำเป็นต้องเปลี่ยนแปลงฟิลด์เหล่านี้ในใบแจ้งหนี้ของผู้จัดจำหน่าย คุณต้องลบใบแจ้งหนี้ของผู้จัดจำหน่ายและสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายใหม่

[!INCLUDE[footer-include](../../includes/footer-banner.md)]