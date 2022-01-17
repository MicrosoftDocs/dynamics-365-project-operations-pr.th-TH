---
title: การรับเหมารายย่อยในรุ่นการเข้าใช้ล่วงหน้าเดือนตุลาคม 2021
description: หัวข้อนี้ให้ภาพรวมของความสามารถด้านการรับเหมารายย่อยใน Project Operations ซึ่งเป็นส่วนหนึ่งของรุ่นทดลองใช้รุ่นการเข้าใช้ล่วงหน้าเดือนตุลาคม 2021
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383718"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>การรับเหมารายย่อยในรุ่นการเข้าใช้ล่วงหน้าเดือนตุลาคม 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

หัวข้อนี้ให้ภาพรวมของความสามารถด้านการรับเหมารายย่อยใน Dynamics 365 Project Operations ซึ่งเป็นส่วนหนึ่งของการทดลองใช้รุ่นการเข้าใช้ล่วงหน้าเดือนตุลาคม 2021 ชุดคุณลักษณะนี้ไม่พร้อมสำหรับสภาพแวดล้อมการทำงานจริงหรือสภาพแวดล้อมที่ใช้งานอยู่ ดังนั้นคุณลักษณะเหล่านี้จะยังคงอยู่ในรุ่นการเข้าใช้ล่วงหน้าจนกว่าจะมีการเปิดตัวชุดคุณลักษณะทั้งหมด เราขอแนะนำให้คุณอย่าใช้ชุดคุณลักษณะการรับเหมารายย่อยสำหรับสถานการณ์การทำงานจริงที่ใช้งานอยู่จนกว่าแบนเนอร์รุ่นพรีวิวจะถูกเอาออก 

รายการต่อไปนี้เป็นรายละเอียดของสิ่งที่มีอยู่ในตอนนี้ในรุ่นการเข้าใช้ล่วงหน้าเดือนตุลาคม 2021:

1. ผู้จัดการโครงการสร้างการรับเหมารายย่อยกับผู้จัดจำหน่าย ตามค่าเริ่มต้น รายการราคาที่ถูกแนบกับเรกคอร์ดผู้จัดจำหน่ายจะถูกใช้สำหรับการรับเหมารายย่อย บัญชีผู้จัดจำหน่ายมีชนิดความสัมพันธ์เป็น **ผู้จัดจำหน่าย** หรือ **ผู้จัดหา**

2. ผู้จัดการโครงการสามารถลงรายการการซื้อทั้งหมดเป็นสินค้าในรายการในการรับเหมารายย่อย การรับเหมารายย่อยใช้สำหรับเวลา ค่าใช้จ่าย หรือผลิตภัณฑ์ก็ได้ คลาสธุรกรรมรายการของการรับเหมารายย่อยจะกำหนดว่ารายการนั้นมีไว้สำหรับอะไร

3. ผู้จัดการบัญชีผู้จัดจำหน่ายและผู้จัดการโครงการสามารถทำซ้ำผ่านการรับเหมารายย่อยได้ สามารถปรับการกำหนดราคาได้ในรายการราคาการซื้อที่ถูกแนบกับการรับเหมารายย่อย

4. ณ จุดนี้ หรือภายหลังในกระบวนการ ถ้ารายการของการรับเหมารายย่อยใช้สำหรับเวลา ผู้จัดการบัญชีผู้จัดจำหน่ายจะเชื่อมโยงผู้ติดต่อของผู้จัดจำหน่ายกับแต่ละรายการของการรับเหมารายย่อย การเชื่อมโยงนี้ให้ข้อมูลแก่ผู้จัดการโครงการที่ทำงานเกี่ยวกับการรับเหมารายย่อย เมื่อผู้ติดต่อของผู้จัดจำหน่ายเชื่อมโยงกับรายการของการรับเหมารายย่อย ระบบจะสร้างทรัพยากรที่สามารถจองได้โดยอัตโนมัติจากผู้ติดต่อ หากไม่มีทรัพยากรที่สามารถจองได้อยู่

5. วิธีการเรียกเก็บเงินในแต่ละรายการของการรับเหมารายย่อยสามารถเป็น **ราคาคงที่** หรือ **เวลาและวัสดุ** สำหรับรายการของการรับเหมารายย่อยที่มีราคาคงที่ สามารถตั้งค่ากำหนดการใบแจ้งหนี้ตามหลักเป้าหมายได้

ขั้นตอนที่เหลือในโฟลว์กระบวนการธุรกิจสำหรับการรับเหมารายย่อยที่ระบุไว้ในภาพรวมยังไม่สามารถใช้ได้ในขณะนี้ เมื่อมีการเพิ่มฟังก์ชันการทำงานใหม่ หัวข้อนี้จะได้รับการอัปเดต 

ภาพประกอบต่อไปนี้แสดงถึงรุ่นการเข้าใช้ล่วงหน้าของการรับเหมารายย่อยซึ่งตรงกันข้ามกับกระบวนการทางธุรกิจแบบครบวงจร

![โฟลว์กระบวนการการรับเหมารายย่อย](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>รุ่นการเข้าใช้ล่วงหน้าของการรับเหมารายย่อยอิงตามปริมาณและตามงาน
ในรุ่นการเข้าใช้ล่วงหน้าเดือนตุลาคม 2021 รองรับเฉพาะรายการรับเหมารายย่อยตามปริมาณเท่านั้น ซึ่งหมายความว่ารายการรับเหมารายย่อยสามารถใช้ซื้อเวลา ค่าใช้จ่าย หรือวัสดุจากผู้จัดจำหน่ายได้ แต่ไม่สามารถใช้กับงานทั้งหมดได้ นอกจากนี้ยังหมายความว่าปริมาณที่ซื้อ (หน่วยของเวลา ค่าใช้จ่าย หรือปริมาณของวัสดุ) ในรายการรับเหมารายย่อยสามารถใช้กับโครงการใดๆ ในระบบได้



[!INCLUDE[footer-include](../../includes/footer-banner.md)]