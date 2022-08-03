---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 37 V3
description: บทความนี้แสดงรายการคุณลักษณะและการแก้ไขที่มีอยู่ในการปรับปรุง Microsoft Dynamics 365 Project Service Automation รุ่น 37, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: bdbb125b4f41bb9970f5bd8a01cf0bb863c34738
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922521"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 37 V3

[!include [banner](../includes/psa-now-project-operations.md)]

เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอป Microsoft Dynamics 365 Project Service Automation รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน เข้ากันได้กับ Dynamics 365 9.x หากต้องการปรับปรุงเป็นรุ่นนี้ ให้ไปที่หน้าศูนย์การจัดการสำหรับโซลูชันออนไลน์ของ Dynamics 365 และติดตั้งการปรับปรุง สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง ปรับปรุง หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)

บทความนี้แสดงรายการคุณลักษณะและการแก้ไขที่เป็นของใหม่หรือมีการเปลี่ยนแปลงสำหรับการปรับปรุง Project Service Automation รุ่น 37, V3 รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.58.120 และโดยทั่วไปจะพร้อมใช้งานผ่านการปรับปรุงด้วยตนเองในเดือนพฤศจิกายน 2021

## <a name="update-release-37"></a>รุ่นการปรับปรุง 37

### <a name="bug-fixes"></a>แก้ไขข้อบกพร่อง

ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว

**เวลาและค่าใช้จ่าย**
- ผู้ใช้ไม่สามารถลบรายการเวลาด้วยการล้างเซลล์
- มุมมอง **การอนุมัติที่ล้มเหลวของฉัน** มีเฉพาะการอนุมัติโครงการที่มีสถานะ **ส่งแล้ว** เท่านั้น

**การจัดการโครงการ**
- ผู้ใช้ได้รับข้อผิดพลาดเป็นข้อยกเว้นการอ้างอิงเป็นไม่มีค่าเมื่อเปิดโครงการใน Add-in เดสก์ท็อปของ Microsoft หากชื่อตำแหน่งของสมาชิกในทีมโครงการถูกเว้นว่างไว้
- ไม่มีปุ่ม **บันทึก** ในเพจ **งานโครงการ** เพื่อให้ผู้ใช้ไม่สามารถบันทึกการเปลี่ยนแปลงไปยังเรกคอร์ดงานได้
- ผู้ใช้ไม่สามารถลบโครงการที่มีงานที่เกี่ยวข้องกับใบเสนอราคาที่มีสถานะเป็น **ชนะ**

**การขาย**
- ฟิลด์ **สกุลเงิน** ในเพจ **โครงการ** ได้รับการปรับปรุงให้ตรงกับสกุลเงินของเทมเพลตที่ใช้
- มีการคำนวณต้นทุนไม่ถูกต้องในงานที่มีหลายสกุลเงิน