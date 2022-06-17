---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 41 V3
description: บทความนี้แสดงรายการคุณลักษณะและการแก้ไขที่มีอยู่ในการปรับปรุง Microsoft Dynamics 365 Project Service Automation รุ่น 41, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930571"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 41 V3

[!include [banner](../includes/psa-now-project-operations.md)]

เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอป Microsoft Dynamics 365 Project Service Automation รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน เข้ากันได้กับ Dynamics 365 9.x หากต้องการปรับปรุงเป็นรุ่นนี้ ให้ไปที่หน้าศูนย์การจัดการสำหรับโซลูชันออนไลน์ของ Dynamics 365 และติดตั้งการปรับปรุง สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง ปรับปรุง หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)

บทความนี้แสดงรายการคุณลักษณะและการแก้ไขที่เป็นของใหม่หรือมีการเปลี่ยนแปลงสำหรับการปรับปรุง Project Service Automation รุ่น 41, V3 รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.62.162 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตด้วยตนเองในเดือนมีนาคม 2022

## <a name="update-release-41"></a>รุ่นการปรับปรุง 41

### <a name="bug-fixes"></a>แก้ไขข้อบกพร่อง

ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว

**การจัดการโครงการ**
- เมื่อคุณพยายามสร้างโครงการจากเทมเพลตที่ยึดตามโครงการที่สร้างจาก Add-in สำหรับเดสก์ท็อป ข้อผิดพลาดต่อไปนี้จะแสดงขึ้น "การตรวจสอบความถูกต้องของฟิลด์งานที่วางแผนไว้ของการกำหนดทรัพยากร: วันที่สิ้นสุดของการแบ่งเวลาการกำหนดทรัพยากรแต่ละรายการต้องไม่เร็วกว่าวันที่เริ่มต้น"

**เวลาและค่าใช้จ่าย**
- เมื่อคุณพยายามลบรายการเวลา ข้อความแสดงข้อผิดพลาดต่อไปนี้จะปรากฏขึ้น "เกิดข้อผิดพลาดที่ไม่คาดคิดจากรหัส ISV"

**การขาย**
- เมื่อคุณสร้างใบแจ้งหนี้สำหรับหลักเป้าหมายราคาคงที่ จะไม่มีการกรอกข้อมูลในฟิลด์ **คำอธิบาย** และ **คำอธิบายภายนอก** 
