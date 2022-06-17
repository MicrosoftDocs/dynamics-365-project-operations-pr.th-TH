---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 28 V3
description: บทความนี้แสดงรายการคุณลักษณะและการแก้ไขที่มีอยู่ในการปรับปรุง Project Service Automation รุ่น 28, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 56a87bce55c560e541e20709b10d38b9512ffcee
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930617"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 28 V3

[!include [banner](../includes/psa-now-project-operations.md)]

เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365 รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชัน เพื่อติดตั้งการปรับปรุง สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง ปรับปรุง หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)

บทความนี้แสดงรายการคุณลักษณะและการแก้ไขที่เป็นของใหม่หรือมีการเปลี่ยนแปลงสำหรับ Project Service Automation V3 การปรับปรุงรุ่น 28 เวอร์ชันนี้มีหมายเลขรุ่นของ V3.10.46.32 และโดยทั่วไปจะสามารถใช้งานผ่านการปรับปรุงตัวเองในเดือนมกราคม 2021

## <a name="update-release-28"></a>รุ่นการปรับปรุง 28

### <a name="bug-fixes"></a>แก้ไขข้อบกพร่อง

**เวลาและค่าใช้จ่าย**

ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:

- ผู้ใช้สามารถใช้ **การแก้ไขจำนวนมาก** เพื่ออัปเดตรายการเวลาที่ได้รับการอนุมัติและส่ง

**การจัดการโครงการ**

ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:

- ในกรณีที่งาน GUID ถูกตีความเป็นตัวเลข งานจะไม่สามารถเปิดเพื่อแก้ไขโดยใช้ **การแก้ไขงาน** ใน Ribbon บนหน้า **โครงสร้างการแบ่งงาน**

**Sales**

ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:

- ข้อยกเว้นการอ้างอิงว่างถูกสร้างขึ้นเมื่อมีการเรียกใช้ปลั๊กอิน **GetEstimatesForProject**
- **ทำเครื่องหมายพร้อมออกใบแจ้งหนี้** บนตารางเหตุการณ์สำคัญจะอัปเดตแอตทริบิวต์เพียงบางส่วนเท่านั้น ยกเว้นแอตทริบิวต์ **InvoiceStatus** ซึ่งได้รับการอัปเดต



[!INCLUDE[footer-include](../includes/footer-banner.md)]
