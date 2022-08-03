---
title: มีอะไรใหม่ในเดือนพฤษภาคม 2022 - Project Operations สำหรับสถานการณ์ตามทรัพยากร/ไม่ได้เก็บในคลัง
description: บทความนี้ให้ข้อมูลเกี่ยวกับการปรับปรุงคุณภาพที่มีอยู่ในรุ่นเดือนพฤษภาคม 2022 ของ Microsoft Dynamics 365 Project Operations สำหรับสถานการณ์ตามทรัพยากร/ไม่ได้เก็บในคลัง
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921417"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>มีอะไรใหม่ในเดือนพฤษภาคม 2022 - Project Operations สำหรับสถานการณ์ตามทรัพยากร/ไม่ได้เก็บในคลัง

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ทรัพยากร/ไม่ได้เก็บในคลัง_

บทความนี้ใช้กับส่วนประกอบและเวอร์ชันของ Microsoft Dynamics 365 Project Operations ต่อไปนี้:

- Project Operations ในสภาพแวดล้อม Dataverse เวอร์ชัน 4.42.0.70
- การจัดการโครงการและการบัญชีในสภาพแวดล้อม Dynamics 365 Finance เวอร์ชัน 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>การปรับปรุงแผนที่การรวมแบบสองทิศทางของ Project Operations

ไม่มีการปรับปรุงสำหรับแผนที่การรวมแบบสองทิศทางของ Project Operations ในรุ่นนี้ สำหรับรายการปัจจุบันและรุ่นของแผนที่การรวมแบบสองทิศทางของ Project Operations โปรดดูที่ [รุ่นของแผนที่การรวมแบบสองทิศทางของ Project Operations](../environment/resource-dual-write-maps.md)

เรียกใช้แผนที่รุ่นล่าสุดในสภาพแวดล้อมของคุณเสมอ และเปิดใช้งานแผนที่ตารางที่เกี่ยวข้องทั้งหมดเมื่อคุณปรับปรุงโซลูชัน Project Operations Dataverse และรุ่นโซลูชัน Finance ของคุณ คุณลักษณะและความสามารถบางอย่างอาจทำงานไม่ถูกต้องหากไม่มีการเปิดใช้งานแผนผังเวอร์ชันล่าสุด คุณสามารถดูแผนที่เวอร์ชันที่ใช้งานได้ในคอลัมน์ **เวอร์ชัน** บนหน้า **การรวมแบบสองทิศทาง** หากต้องการเปิดใช้งานแผนที่เวอร์ชันใหม่ได้ ให้เลือก **เวอร์ชันแผนที่ของตาราง** เลือกเวอร์ชันล่าสุด และจากนั้น บันทึกเวอร์ชันที่เลือก หากคุณปรับแต่งแผนผังตารางสำเร็จรูป ให้ใช้การเปลี่ยนแปลงอีกครั้ง สำหรับข้อมูลเพิ่มเติม โปรดดู [การจัดการวงจรชีวิตของแอปพลิเคชัน](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

หากคุณประสบปัญหาเมื่อคุณเริ่มต้นแผนผัง ให้ทำตามคำแนะนำในส่วน [ปัญหาคอลัมน์ตารางในแผนผังหายไป](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) ของคู่มือการแก้ไขปัญหาการรวมแบบสองทิศทาง

## <a name="quality-updates"></a>การปรับปรุงคุณภาพ
### <a name="project-operations-on-dataverse"></a>Project Operations บน Dataverse

| พื้นที่คุณลักษณะ | หมายเลขอ้างอิง | การปรับปรุงคุณภาพ |
| --- | --- | --- |
| การจัดการทรัพยากร | 2634019 | ปรับปรุงข้อความแสดงข้อผิดพลาดสำหรับการตรวจสอบธุรกิจเมื่อเพิ่มสมาชิกทีมทั่วไปเป็นทรัพยากร |
| การวางแผนและการติดตามโครงการ | 2648515 | การปรับปรุงที่จำกัดของ **ownerid**, **state** และ **status** ในเอนทิตีการจัดกำหนดการ |
| การเรียกเก็บเงินและการกำหนดราคา | 2653167 | ตัวคั่นทศนิยมกริด **ประมาณการ** ต้องเป็นไปตามการตั้งค่ารูปแบบใน **ตัวเลือกส่วนบุคคล** |
| การเรียกเก็บเงินและการกำหนดราคา| 2662251 | ค่าในฟิลด์ **หน่วยที่แก้ไข** และ **กลุ่มของหน่วยนับ** เป็นค่าเริ่มต้นเมื่อสร้างเรกคอร์ดในประมาณการวัสดุ |
| การเรียกเก็บเงินและการกำหนดราคา| 2571408 | การขายจริงที่ยังไม่ได้เรียกเก็บเงินจะถูกประทับตราด้วยรหัสใบแจ้งหนี้ชั่วคราวเมื่อสร้างใบแจ้งหนี้ฉบับร่าง |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>การจัดการโครงการและการบัญชีใน Dynamics 365 Finance

สำหรับข้อมูลเกี่ยวกับการแก้ไขจุดบกพร่องที่รวมอยู่ในการปรับปรุงนี้ ให้ลงชื่อเข้าใช้ Microsoft Dynamics Lifecycle Services (LCS) และดู [บทความ KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864)