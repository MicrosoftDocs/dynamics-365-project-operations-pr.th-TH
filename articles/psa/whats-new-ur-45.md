---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 45 V3
description: บทความนี้แสดงรายการคุณลักษณะและการแก้ไขที่มีอยู่ในการปรับปรุง Microsoft Dynamics 365 Project Service Automation รุ่น 45, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169168"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 45 V3

[!include [banner](../includes/psa-now-project-operations.md)]

เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอป Microsoft Dynamics 365 Project Service Automation รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน เข้ากันได้กับ Dynamics 365 9.x หากต้องการปรับปรุงเป็นรุ่นนี้ ให้ไปที่หน้าศูนย์การจัดการสำหรับโซลูชันออนไลน์ของ Dynamics 365 และติดตั้งการปรับปรุง สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง ปรับปรุง หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)

บทความนี้แสดงรายการคุณลักษณะและการแก้ไขที่เป็นของใหม่หรือมีการเปลี่ยนแปลงสำหรับการปรับปรุง Project Service Automation รุ่น 45, V3 รุ่นนี้มีหมายเลขการสร้างเป็น V3.10.76.168 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตตนเองในเดือนกรกฎาคม 2022

## <a name="update-release-45"></a>รุ่นการปรับปรุง 45

### <a name="bug-fixes"></a>แก้ไขข้อบกพร่อง

ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว

**การขาย**

- ผู้ใช้ไม่สามารถสร้างใบแจ้งหนี้ได้หลังจากที่พยายามสร้างใบแจ้งหนี้โดยไม่มีการขายที่ยังไม่ได้เรียกเก็บเงิน หากพวกเขากำลังดูอินสแตนซ์ของหน้าเดียวกันของหน้าและไม่ได้รีเฟรชหน้า

**เวลาและค่าใช้จ่าย**

- เมื่อเปิดใช้งานการอนุมัติแบบใหม่และได้อนุมัติการอนุมัติโครงการที่เรียกคืน ลำดับขั้นของเรกคอร์ดจะถูกปรับปรุงเป็น **อนุมัติคำขอการเรียกคืนแล้ว** อย่างไม่ถูกต้อง
- เมื่อเปิดใช้งานการอนุมัติแบบใหม่และโฟลว์ระบบคลาวด์เป็นไม่ใช้งาน กระบวนการอนุมัติจะไม่สำเร็จ และผู้ใช้ที่ส่งหรืออนุมัติจะไม่ได้รับแจ้ง
