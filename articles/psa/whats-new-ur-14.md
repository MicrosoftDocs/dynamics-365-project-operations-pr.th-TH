---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 14 V3
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับสิ่งใหม่ในรุ่นการปรับปรุง Project Service Automation 14 V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e19c8ffe7d92ab7ec9eb46aff8f944c62b0bb4bc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281006"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation รุ่นการปรับปรุง 14 V3

[!include [banner](../includes/psa-now-project-operations.md)]

เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Dynamics 365 Project Service Automation (PSA) รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x หากต้องการอัปเดตเป็นรุ่นนี้ ให้ไปที่ศูนย์ผู้ดูแลระบบสำหรับ Dynamics 365 ออนไลน์ และไปที่หน้าโซลูชันเพื่อติดตั้งการอัปเดต สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)

หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่เป็นของใหม่หรือที่เปลี่ยนแปลงสำหรับ PSA V3, รุ่นการปรับปรุง 14 รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.4.21 และพร้อมใช้งานตามกำหนดการต่อไปนี้:

- **ความพร้อมใช้งานทั่วไป (อัปเดตด้วยตนเอง):** มกราคม 2020
- **อัปเดตอัตโนมัติ:** กุมภาพันธ์ 2020

## <a name="update-release-14"></a>รุ่นการปรับปรุง 14

### <a name="enhancements"></a>การปรับปรุง

- Sales

     - ค่าฟิลด์ที่กำหนดเองจาก **รายละเอียดบรรทัดใบเสนอราคา** ถูกคัดลอกไปยัง **รายละเอียดบรรทัดสัญญาโครงการ** เมื่อมีการปรับปรุงใบเสนอราคาเป็น **ปิดในสถานะชนะ**
     - โครงการที่ได้รับการยืนยันสามารถถูก **ปิดในสถานะแพ้**

- การจัดการทรัพยากร

     - เมื่อขยายการจอง ผู้ใช้จะได้รับแจ้งพร้อมกล่องโต้ตอบการยืนยันเพื่อสรุปผลการจองและให้ลิงก์ไปยังการรักษาการจอง


### <a name="bug-fixes"></a>การแก้ไขข้อผิดพลาด

- เวลาและค่าใช้จ่าย

     - แก้ไข: ปรับปรุงประสบการณ์ผู้ใช้เมื่อผู้ใช้ไม่ได้เลือกรายการใดๆ ที่จะแก้ไข

- การจัดการทรัพยากร

     - แก้ไข: จองทรัพยากรหลายครั้งทำให้มีชื่อของทรัพยากรที่จองได้มากเกินไป

- Sales

     - แก้ไข: ราคาขายทั้งหมดจะไม่ถูกคำนวณจนกว่าผู้ใช้จะป้อนราคาต้นทุนสำหรับการประมาณการค่าใช้จ่ายในโครงการ
     - แก้ไข: การปิดใบเสนอราคาเป็น **ชนะ** ล้มเหลวหากสัญญาโครงการที่เกี่ยวข้องไม่ได้อยู่ในสถานะ **ร่าง**



[!INCLUDE[footer-include](../includes/footer-banner.md)]