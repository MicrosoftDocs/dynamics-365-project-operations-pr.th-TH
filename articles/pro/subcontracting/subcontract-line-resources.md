---
title: ทรัพยากรของรายการรับเหมารายย่อย
description: หัวข้อนี้อธิบายวิธีระบุทรัพยากรเฉพาะที่ผู้จัดจำหน่ายจัดเตรียมไว้สำหรับรายการรับเหมารายย่อยเฉพาะในช่วงเวลาหนึ่ง
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4a929b985a51ab49d3e34ce4a5c277af4c05c216
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558480"
---
# <a name="subcontract-line-resources"></a>ทรัพยากรของรายการรับเหมารายย่อย

[!include [banner](../../includes/dataverse-preview.md)]

_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

ใน Dynamics 365 Project Operations ผู้จัดจำหน่ายสามารถระบุทรัพยากรที่จะใช้เพื่อจัดหากำลังการผลิตของทรัพยากรที่ซื้อในรายการรับเหมารายย่อยสำหรับเวลา

## <a name="create-subcontract-line-resources"></a>สร้างทรัพยากรของรายการรับเหมารายย่อย

เพื่อสร้างทรัพยากรของรายการรับเหมารายย่อย ให้ทำตามขั้นตอนต่อไปนี้

1. ในบานหน้าต่างนำทาง เลือก **การรับเหมารายย่อย** และเปิดการรับเหมารายย่อยที่คุณต้องการทำงานด้วย
2. เปิดรายการรับเหมารายย่อยสำหรับเวลาที่คุณต้องการระบุทรัพยากรของผู้จัดจำหน่าย
3. บนแท็บ **ทรัพยากรของรายการรับเหมารายย่อย** ในตารางย่อย เลือก **+ ทรัพยากรของรายการรับเหมารายย่อยใหม่**
4. บนเพจ **ทรัพยากรในรายการรับเหมารายย่อยใหม่** ให้ป้อนข้อมูลที่ต้องการ แล้วเลือก **บันทึกและปิด**

ตารางต่อไปนี้อธิบายฟิลด์ในทรัพยากรของรายการรับเหมารายย่อย

| ฟิลด์ | รายละเอียด | ผลของฟังก์ชัน |
| ----- | ----------- | ----------------- |
| ทรัพยากรที่สามารถจองได้ | เลือกทรัพยากรที่สามารถจองได้ของชนิด **ผู้ปฏิบัติงานแบบสัญญาจ้าง** ที่คุณต้องการใช้เป็นทรัพยากรในรายการรับเหมารายย่อย| ถ้าคุณยังไม่ได้สร้างทรัพยากรที่สามารถจองได้สำหรับผู้ปฏิบัติงานแบบสัญญาจ้าง ให้ปล่อยฟิลด์นี้ว่างไว้ ทรัพยากรที่สามารถจองได้จะสร้างขึ้นเมื่อคุณบันทึกเรกคอร์ด  |
| ผู้ติดต่อ | คุณสามารถสร้างทรัพยากรในรายการรับเหมารายย่อยของคุณจากผู้ติดต่อที่มีอยู่ ใช้การค้นหาเพื่อดูรายชื่อผู้ติดต่อที่ใช้งานอยู่ในระบบ เลือกผู้ติดต่อสำหรับผู้จัดจำหน่ายของการรับเหมารายย่อยนี้ ถ้าผู้ติดต่อที่คุณเลือกไม่ใช่ผู้ติดต่อที่ถูกต้องสำหรับผู้จัดจำหน่ายในการรับเหมารายย่อย เรกคอร์ดทรัพยากรของรายการรับเหมารายย่อยจะไม่ถูกบันทึก| หากไม่มีทรัพยากรที่สามารถจองได้สำหรับผู้ติดต่อที่เลือก ระบบจะสร้างทรัพยากรที่สามารถจองได้สำหรับผู้ติดต่อที่เลือกก่อนที่จะสร้างทรัพยากรของรายการรับเหมารายย่อย |
| ผู้ใช้ | คุณสามารถสร้างทรัพยากรในรายการรับเหมารายย่อยโดยการเลือกผู้ใช้ที่ใช้งานอยู่ ใช้การค้นหาเพื่อดูรายชื่อผู้ใช้ที่ใช้งานอยู่ในระบบ| หากไม่มีทรัพยากรที่สามารถจองได้สำหรับผู้ใช้ที่เลือก ระบบจะสร้างทรัพยากรที่สามารถจองได้สำหรับผู้ใช้ที่เลือกก่อนที่จะสร้างทรัพยากรของรายการรับเหมารายย่อย |
| วันที่เริ่มต้น | วันที่ที่การมอบหมายงานสำหรับผู้ปฏิบัติงานของการรับเหมารายย่อยจะเริ่มต้น| หากทรัพยากรนี้ถูกจองไว้สำหรับช่วงเวลาที่อยู่ก่อนช่วงวันที่นี้ จะปรากฏคำเตือน |
| วันที่สิ้นสุด | วันที่ที่การมอบหมายงานสำหรับผู้ปฏิบัติงานของการรับเหมารายย่อยเสร็จสิ้น| หากทรัพยากรนี้ถูกจองไว้สำหรับช่วงเวลาที่อยู่หลังช่วงวันที่นี้ จะปรากฏคำเตือน |
| ความพยายาม | จำนวนชั่วโมงความพยายามทั้งหมดที่ผู้ปฏิบัติงานแบบสัญญาจ้างจะใช้ในรายการรับเหมารายย่อยนี้| ถ้าทรัพยากรนี้ถูกจองเกินความพยายามที่จัดสรรในการรับเหมารายย่อยนี้ จะปรากฏคำเตือน |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]