---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 43 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่มีอยู่ใน Microsoft Dynamics 365 Project Service Automation รุ่นการปรับปรุง 43, V3
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
ms.openlocfilehash: fcf18a24b3bc354a16a415368063133743e79696
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710037"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 43 V3

[!include [banner](../includes/psa-now-project-operations.md)]

เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอป Microsoft Dynamics 365 Project Service Automation รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน นเข้ากันได้กับ Dynamics 365 9.x หากต้องการปรับปรุงเป็นรุ่นนี้ ให้ไปที่หน้าศูนย์การจัดการสำหรับโซลูชันออนไลน์ของ Dynamics 365 และติดตั้งการปรับปรุง สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง ปรับปรุง หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)

หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation รุ่นการปรับปรุง 43 V3 เวอร์ชันนี้มีหมายเลขรุ่น V3.10.74.200 และจะพร้อมให้ปรับปรุงด้วยตนเองโดยทั่วไปในเดือนพฤษภาคม 2022

## <a name="update-release-43"></a>รุ่นการปรับปรุง 43

### <a name="bug-fixes"></a>แก้ไขข้อบกพร่อง

ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว


**เวลาและค่าใช้จ่าย**

- เมื่อนำเข้ารายการเวลาจากการจองหรือการกำหนดทรัพยากร การอ้างอิงไปยังทรัพยากรที่สามารถจองได้ที่เกี่ยวข้องจะไม่ถูกรักษาไว้
- เมื่อขยายกริดรายการเวลาเป็นแบบเต็มหน้าจอ การนำทางในตารางด้วยปุ่มแท็บจะไม่ทำงาน
- เมื่อส่งรายการเวลาที่สร้างโดยผู้ใช้รายอื่น ฟิลด์ **ส่งโดย** จะถูกเติมข้อมูลอย่างไม่ถูกต้องด้วยผู้ใช้ที่สร้างใบบันทึกเวลา
