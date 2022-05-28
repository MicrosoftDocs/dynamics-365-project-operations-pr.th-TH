---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 39 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่มีอยู่ใน Microsoft Dynamics 365 Project Service Automation รุ่นการปรับปรุง 39, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: 1d198f9ad9144f5cc2f533fa9603e1f1a181c8b6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588759"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 39 V3

[!include [banner](../includes/psa-now-project-operations.md)]

เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอป Microsoft Dynamics 365 Project Service Automation รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน เข้ากันได้กับ Dynamics 365 9.x หากต้องการปรับปรุงเป็นรุ่นนี้ ให้ไปที่หน้าศูนย์การจัดการสำหรับโซลูชันออนไลน์ของ Dynamics 365 และติดตั้งการปรับปรุง สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง ปรับปรุง หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)

หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation รุ่นการปรับปรุง 39 V3 รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.60.170 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตด้วยตนเองในเดือนมกราคม 2022

## <a name="update-release-39"></a>รุ่นการปรับปรุง 39

### <a name="bug-fixes"></a>แก้ไขข้อบกพร่อง

ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว

**ทั่วไป**

- มีการปรับปรุงหลายอย่างในแผนผังเว็บไซต์สำหรับการแปลภาษาอาหรับ

**การจัดการโครงการ**

- มีข้อผิดพลาดเกิดขึ้นเมื่อคุณเปลี่ยนผู้จัดการโครงการในโครงการเป็นผู้ใช้ที่เป็นสมาชิกทีมในโครงการอยู่แล้ว

**การขาย**

- เจ้าของ **รายการราคาในสัญญาโครงการ** ไม่ถูกต้องเมื่อมีการสร้างรายการราคาโดยอัตโนมัติ 
- วันที่มีผลของรายการราคาจะไม่มีผลเมื่อมีการใช้รายการราคากับพารามิเตอร์โครงการ
- หน่วยที่ทำสัญญาอาจมีค่าเริ่มต้นที่ไม่ถูกต้องเมื่อแก้ไขใบเสนอราคาแยกกันสองรายการ
