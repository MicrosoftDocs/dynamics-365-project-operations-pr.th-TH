---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 40 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่มีอยู่ใน Microsoft Dynamics 365 Project Service Automation รุ่นการปรับปรุง 40, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 25f375ce648eb7d233f6433739832caee351830d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588667"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 40 V3

[!include [banner](../includes/psa-now-project-operations.md)]

เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอป Microsoft Dynamics 365 Project Service Automation รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน เข้ากันได้กับ Dynamics 365 9.x หากต้องการปรับปรุงเป็นรุ่นนี้ ให้ไปที่หน้าศูนย์การจัดการสำหรับโซลูชันออนไลน์ของ Dynamics 365 และติดตั้งการปรับปรุง สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง ปรับปรุง หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)

หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation รุ่นการปรับปรุง 40 V3 รุ่นนี้มีหมายเลขรุ่น V3.10.61.61 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตด้วยตนเองในเดือนกุมภาพันธ์ 2022

## <a name="update-release-40"></a>รุ่นการปรับปรุง 40

### <a name="features"></a>คุณลักษณะ
ระยะที่ 1 ของการปรับรุ่นจาก Project Service Automation เป็น Project Operations - Lite ออกใช้ในเดือนกุมภาพันธ์ 2022 กับลูกค้าทุกคน หากต้องการตรวจสอบการมีสิทธิ์ ดูที่ [ปรับรุ่นจาก Project Service Automation เป็น Project Operations](upgrade-project-operations-non-stocked.md) หากแอปพลิเคชันไม่ปรากฏในอินสแตนซ์ของคุณในศูนย์จัดการ Power Platform ติดต่อฝ่ายสนับสนุนและขอให้เปิดใช้งานเวอร์ชันทดสอบสำหรับสภาพแวดล้อมของคุณ คำขอของคุณต้องมีรายการรหัสสภาพแวดล้อมที่ต้องการเปิดใช้งานเวอร์ชันทดสอบ

### <a name="bug-fixes"></a>แก้ไขข้อบกพร่อง

ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว

**เวลาและค่าใช้จ่าย**
- รายการบันทึกหายไปเมื่อรายการเวลาถูกปฏิเสธหรือถูกยกเลิก 

**การขาย**

- เมื่อคุณปรับปรุงประมาณการต้นทุนหรือการขายโดยใช้ปลั๊กอินสำเร็จรูป คุณจะได้รับอนุญาตให้ส่งเพย์โหลด JSON ที่ไม่ถูกต้องนอกส่วนติดต่อผู้ใช้
- เมื่อคุณปรับปรุงรายการใบเสนอราคาโดยใช้มุมมองด่วน คุณจะเปิดใช้งานใบเสนอราคาได้
