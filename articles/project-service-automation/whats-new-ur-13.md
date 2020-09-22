---
title: มีอะไรใหม่ในรุ่นการปรับปรุง Project Service Automation 13 V3
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับสิ่งใหม่ในรุ่นการปรับปรุง Project Service Automation 13 V3
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756425"
---
# <a name="project-service-automation-v3-update-release-13"></a>Project Service Automation V3 รุ่นการปรับปรุง 13
เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Dynamics 365 Project Service Automation (PSA) รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x หากต้องการอัปเดตเป็นรุ่นนี้ ให้ไปที่ศูนย์ผู้ดูแลระบบสำหรับ Dynamics 365 ออนไลน์ และไปที่หน้าโซลูชันเพื่อติดตั้งการอัปเดต สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)

หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation V3 รุ่นการปรับปรุง 13 รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.3.18 และพร้อมใช้งานตามกำหนดการต่อไปนี้:

- **ความพร้อมใช้งานทั่วไป (อัปเดตด้วยตนเอง):** พฤศจิกายน 2019
- **การปรับปรุงอัตโนมัติ:** ธันวาคม 2019


## <a name="update-release-13"></a>รุ่นการปรับปรุง 13 

### <a name="bug-fixes"></a>การแก้ไขข้อผิดพลาด

- เวลาและค่าใช้จ่าย

     - แก้ไข: ฟังก์ชันการค้นหาในหน้า **การอนุมัติค่าใช้จ่าย** ไม่ทำงานเมื่อค้นหาตามจุดประสงค์ของค่าใช้จ่าย

- การจัดการทรัพยากร

     - แก้ไข: หมายเลขในการกระทบยอดได้รับการอัปเดตเพื่อให้มีความชอบธรรม
     - แก้ไข: ทรัพยากรที่มีชื่อไม่สามารถกำหนดให้กับงานผ่านแท็บ **จัดกำหนดการ**

- การจัดการโครงการ

     - แก้ไข: ข้อยกเว้นอ้างอิงเป็นศูนย์เมื่อการกำหนดสมาชิกทีมเมื่อ **TransactionType** ไม่มีข้อมูลการตั้งค่าสำหรับ **หน่วย** และ **DefaultGroup**

- Sales

     - แก้ไข: เร็กคอร์ดชนิดธุรกรรมที่ซ้ำกันส่งคืนข้อผิดพลาดเมื่อสร้างเรกคอร์ดราคาบทบาท
     - แก้ไข: ปุ่มพิเศษสำหรับ **โอกาสทางการขายใหม่** **ใบเสนอราคา** **บรรทัดในใบสั่ง** และ **เพิ่มผลิตภัณฑ์** สามารถมองเห็นได้ในคำสั่งสำหรับโอกาสทางการขาย การเสนอราคา ผลิตภัณฑ์ในใบสั่ง และกริดย่อยที่อิงตามโครงการ


