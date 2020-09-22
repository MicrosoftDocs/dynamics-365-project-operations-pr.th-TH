---
title: มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Project Service Automation รุ่น 3.x เวฟ 1 2020
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับสิ่งใหม่และสิ่งที่เปลี่ยนแปลงใน Project Service Automation รุ่น 3 เวฟ 1 2020
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756421"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Project Service Automation รุ่น 3 เวฟ 1 2020
หัวข้อเน้นข้อควรพิจารณาในการปรับรุ่นของคีย์เมื่อย้ายไปยังรุ่นล่าสุดของ Project Service Automation (PSA) รุ่น 3.x เวฟ 1 2020

## <a name="time-entry"></a>รายการเวลา
ประสบการณ์รายการเวลาได้รับการขยายเพื่อมอบความสามารถในการขยายเวลาเข้าสู่สถานการณ์ลูกค้ามากขึ้น ซึ่งรวมถึงความสามารถในการเพิ่มประเภทรายการ ซึ่งตอนนี้กระตุ้นให้เกิดพฤติกรรมที่เฉพาะเจาะจง ขึ้นอยู่กับชื่อ Schema **การตั้งค่ารายการเวลา** แสดงเป็น **แหล่งเวลา**

### <a name="upgrade-consideration"></a>ข้อควรพิจารณาในการปรับรุ่น
เพื่อรองรับฟังก์ชันนี้ บทบาทภายใน PSA ได้รับการปรับปรุงเพื่อรวมสิทธิการใช้งานใหม่ๆ สิทธิ์การใช้งานเหล่านี้ให้สิทธิ์การอ่านเพื่อเข้าถึงเอนทิตีใหม่ **การตั้งค่ารายการเวลา**

ผู้ใช้ที่ต้องการความสามารถในการบันทึกเวลาควรได้รับบทบาทผู้ใช้ **ผู้ใช้รายการเวลา** นอกเหนือจากบทบาทที่มีอยู่ บทบาทนี้รวมถึงฟังก์ชันใหม่และช่วยให้มั่นใจได้ว่ารายการเวลาจะทำงานต่อ

### <a name="currently-extended-time-entry-changes"></a>การเปลี่ยนแปลงรายการเวลาที่นานขึ้นในปัจจุบัน
เพื่อลดผลกระทบต่อผู้ใช้งานปัจจุบันของรายการเวลา การเปลี่ยนแปลงบทบาทนี้เป็นข้อกำหนดหลักเพียงอย่างเดียวที่จำเป็นในการใช้ประโยชน์จากรายการเวลาต่อไป หากคุณสร้างมุมมองที่กำหนดเองหรือประสบการณ์รายการเวลาแยกกันคุณต้องตั้งค่าฟิลด์ **การตั้งค่ารายการเวลา** เป็นค่า PSA ที่ถูกต้อง
