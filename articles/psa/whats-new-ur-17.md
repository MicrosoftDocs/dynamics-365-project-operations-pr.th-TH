---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 17 V3
description: บทความนี้แสดงรายการคุณลักษณะและการแก้ไขที่มีอยู่ในการปรับปรุง Project Service Automation รุ่น 17, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: c8486ef689f0d8ab014c2248fc6e5d0fddc937e7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915713"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation รุ่นการปรับปรุง 17 V3

[!include [banner](../includes/psa-now-project-operations.md)]

เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365 รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน  รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชันเพื่อติดตั้งการปรับปรุง สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง ปรับปรุง หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)

บทความนี้แสดงรายการคุณลักษณะและการแก้ไขที่เป็นของใหม่หรือมีการเปลี่ยนแปลงสำหรับ PSA V3 การปรับปรุงรุ่น 17 รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.6.34 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตด้วยตนเองในเดือนมีนาคม 2020


## <a name="update-release-17"></a>รุ่นการปรับปรุง 17

### <a name="bug-fixes"></a>การแก้ไขข้อผิดพลาด

**ทั่วไป**

- แก้ไขแล้ว: ปรับปรุง Project Service Automation เพื่อบังคับใช้สิทธิ์การใช้งานของ Team Member (Project Resource Hub จะรวมข้อมูลเมตาของแผน Team Member Service 3.x)
 
**เวลาและค่าใช้จ่าย**

- แก้ไขแล้ว: เป็นไปไม่ได้ที่จะเปลี่ยนการประมาณการค่าใช้จ่ายจากราคาที่ไม่เป็นศูนย์เป็นศูนย์ (0) การเปลี่ยนแปลงจะถูกละเว้น

**การจัดการโครงการ**

- แก้ไขแล้ว: การตรวจสอบค่า Null ถูกเพิ่มในชื่อตำแหน่งของสมาชิกกลุ่มคน
- แก้ไขแล้ว: ฟิลด์ **msdyn_userresourceid** บนเอนทิตี **msdyn_resourceassignment** ถูกเลิกใช้แล้ว
- แก้ไขแล้ว: ในขณะนี้การอัปเกรดจาก 2.x เป็น 3.x จัดการกับเส้นชั้นของความพยายามที่ว่างเปล่าในการมอบหมายงาน

**Sales**

- แก้ไขแล้ว: **Invoice.PreValidateInvoiceUpdate** ตอนนี้จัดการสถานการณ์จำลองของการมอบหมายเจ้าของเรกคอร์ดใหม่อย่างเหมาะสมอีกครั้ง
- แก้ไขแล้ว: เมื่อคลาสธุรกรรมคือ **เวลา** **UnitGroup** เป็นแบบไม่สามารถแก้ไขได้สำหรับเอนทิตีทั้งหมด ซึ่งรวมถึง **QuoteLineDetails** **JournalLine** **InvoiceLineDetail** และ **ContractLineDetails** อย่างไรก็ตาม **หน่วย** เป็นแบบไม่สามารถแก้ไขได้ เฉพาะสำหรับ **JournalLine** และ **InvoiceLineDetails**




[!INCLUDE[footer-include](../includes/footer-banner.md)]
