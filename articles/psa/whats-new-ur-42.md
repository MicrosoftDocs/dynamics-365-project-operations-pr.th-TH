---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 42 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่มีอยู่ใน Microsoft Dynamics 365 Project Service Automation รุ่นการปรับปรุง 42, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589219"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 42 V3

[!include [banner](../includes/psa-now-project-operations.md)]

เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอป Microsoft Dynamics 365 Project Service Automation รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน เข้ากันได้กับ Dynamics 365 9.x หากต้องการปรับปรุงเป็นรุ่นนี้ ให้ไปที่หน้าศูนย์การจัดการสำหรับโซลูชันออนไลน์ของ Dynamics 365 และติดตั้งการปรับปรุง สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง ปรับปรุง หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)

หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation รุ่นการปรับปรุง 42 V3 เวอร์ชันนี้มีหมายเลขรุ่น V3.10.73.61 และจะพร้อมให้ปรับปรุงด้วยตนเองโดยทั่วไปในเดือนเมษายน 2022

## <a name="update-release-42"></a>รุ่นการปรับปรุง 42

### <a name="bug-fixes"></a>แก้ไขข้อบกพร่อง

ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว

**เวลาและค่าใช้จ่าย**

- เมื่อใบบันทึกเวลาถูกปฏิเสธ ผู้ใช้ที่ปฏิเสธจะถูกระบุอย่างไม่ถูกต้องว่าเป็น **ระบบ**
- เมื่อนำเข้ารายการเวลา ไม่มีค่าของ **ประเภททรัพยากร**
- ผู้อนุมัติโครงการสามารถอนุมัติโครงการที่ส่งเมื่อไม่ได้ตั้งค่าสิทธิ์เป็น **สามารถอนุมัติ** โดยเฉพาะ

**การขาย**

- เมื่อข้อมูลจริงถูกบันทึกบนงานที่ไม่ใช่ระดับราก ต้นทุนจริงจะถูกรวมอย่างไม่ถูกต้อง
