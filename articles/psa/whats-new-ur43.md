---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 43 V3
description: บทความนี้แสดงรายการคุณลักษณะและการแก้ไขที่มีอยู่ในการปรับปรุง Microsoft Dynamics 365 Project Service Automation รุ่น 43, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.openlocfilehash: b12cfda08f1ea1fc441782003130be445a437f7c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915345"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 43 V3

[!include [banner](../includes/psa-now-project-operations.md)]

เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอป Microsoft Dynamics 365 Project Service Automation รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน นเข้ากันได้กับ Dynamics 365 9.x หากต้องการปรับปรุงเป็นรุ่นนี้ ให้ไปที่หน้าศูนย์การจัดการสำหรับโซลูชันออนไลน์ของ Dynamics 365 และติดตั้งการปรับปรุง สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง ปรับปรุง หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)

บทความนี้แสดงรายการคุณลักษณะและการแก้ไขที่เป็นของใหม่หรือมีการเปลี่ยนแปลงสำหรับการปรับปรุง Project Service Automation รุ่น 43, V3 เวอร์ชันนี้มีหมายเลขรุ่น V3.10.74.200 และจะพร้อมให้ปรับปรุงด้วยตนเองโดยทั่วไปในเดือนพฤษภาคม 2022

## <a name="update-release-43"></a>รุ่นการปรับปรุง 43

### <a name="bug-fixes"></a>แก้ไขข้อบกพร่อง

ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว


**เวลาและค่าใช้จ่าย**

- เมื่อนำเข้ารายการเวลาจากการจองหรือการกำหนดทรัพยากร การอ้างอิงไปยังทรัพยากรที่สามารถจองได้ที่เกี่ยวข้องจะไม่ถูกรักษาไว้
- เมื่อขยายกริดรายการเวลาเป็นแบบเต็มหน้าจอ การนำทางในตารางด้วยปุ่มแท็บจะไม่ทำงาน
- เมื่อส่งรายการเวลาที่สร้างโดยผู้ใช้รายอื่น ฟิลด์ **ส่งโดย** จะถูกเติมข้อมูลอย่างไม่ถูกต้องด้วยผู้ใช้ที่สร้างใบบันทึกเวลา