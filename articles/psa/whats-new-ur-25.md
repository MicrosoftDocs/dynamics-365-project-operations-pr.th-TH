---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 25 V3
description: บทความนี้แสดงรายการคุณลักษณะและการแก้ไขที่มีอยู่ในการปรับปรุง Project Service Automation รุ่น 25, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 2330c7dc5d2dfb148d5c7fb9a5ce643fded84dde
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922567"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 25 V3

[!include [banner](../includes/psa-now-project-operations.md)]

เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365 รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชัน เพื่อติดตั้งการปรับปรุง สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง ปรับปรุง หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)

บทความนี้แสดงรายการคุณลักษณะและการแก้ไขที่เป็นของใหม่หรือมีการเปลี่ยนแปลงสำหรับ Project Service Automation V3 การปรับปรุงรุ่น 25 เวอร์ชันนี้มีหมายเลขรุ่นของ V3.10.43.76 และโดยทั่วไปจะสามารถใช้งานผ่านการปรับปรุงตัวเองในเดือนตุลาคม 2020

## <a name="update-release-25"></a>รุ่นการปรับปรุง 25

### <a name="bug-fixes"></a>แก้ไขข้อบกพร่อง

**เวลาและค่าใช้จ่าย**

ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:

- แผนภูมิรายการเวลาแสดงข้อมูลเพิ่มเติมตามช่วงเวลาที่ดึงข้อมูลมากเกินไป

**การจัดการทรัพยากร**

ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:

- เพิ่มรหัส Package Deployer เพื่อข้ามการนำเข้าโปรแกรมแก้ไข Universal Resource Scheduling หากมีโปรแกรมแก้ไขรุ่นที่สูงกว่าอยู่แล้ว

**การจัดการโครงการ**

ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:

- แก้ไขความคลาดเคลื่อนในการปัดเศษและอัตราแลกเปลี่ยนทำให้ต้นทุนตามแผนไม่ถูกต้องในตารางการติดตามโครงการ
- รองรับความสามารถในการแสดงกริดปฏิกิริยาสองรายการขึ้นไปในฟอร์ม **โครงการ**
- มีการตรวจสอบความถูกต้องเพื่อระบุความสามารถในการมอบหมายงานหลังจากวันที่สิ้นสุดของปฏิทิน ซึ่งส่งผลให้การกำหนดทรัพยากรล้มเหลว
- ปรับปรุงการจัดการข้อผิดพลาดเพื่อแก้ไขข้อยกเว้นการอ้างอิง Null ที่สร้างขึ้นจากสิ่งต่อไปนี้:

    - ปลั๊กอิน **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** เมื่องานโครงการถูกสร้างขึ้นโดยไม่มีโครงการที่เกี่ยวข้อง
    - ปลั๊กอิน **PreProjectTeamMemberCreate**
    - ปลั๊กอิน **PostProjectTeamMemberDelete**
    - ปลั๊กอิน **PreValidateProjectTaskDelete**

**Sales**

ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:

- การจัดการข้อผิดพลาดที่ปรับปรุงเพื่อแก้ไขข้อยกเว้นการอ้างอิง Null สร้างขึ้นจาก **คัดลอกโครงการ: ประมาณการการจัดการแหล่งข้อมูล HelperResource**
- **ไม่พร้อมที่จะออกใบแจ้งหนี้** บน **รายการคงค้างของการเรียกเก็บเงินเวลาและวัสดุ** ไม่ล้างสถานะการเรียกเก็บเงิน
- ปุ่มแก้ไขป้ายกำกับ **ราคา** ผิดบนแท็บ **ราคาตามบทบาท** และ **รายการแค็ตตาล็อก**


[!INCLUDE[footer-include](../includes/footer-banner.md)]
