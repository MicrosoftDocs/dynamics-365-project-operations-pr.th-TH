---
title: มีอะไรใหม่ในเดือนสิงหาคม 2022 - Project Operations สำหรับสถานการณ์ทรัพยากร/ไม่ได้เก็บในคลัง
description: บทความนี้ให้ข้อมูลเกี่ยวกับการปรับปรุงคุณภาพที่มีอยู่ในรุ่นเดือนสิงหาคม 2022 ของ Microsoft Dynamics 365 Project Operations สำหรับสถานการณ์ตามทรัพยากร/ไม่ได้เก็บในคลัง
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403880"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>มีอะไรใหม่ในเดือนสิงหาคม 2022 - Project Operations สำหรับสถานการณ์ทรัพยากร/ไม่ได้เก็บในคลัง

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/ไม่ได้เก็บในคลัง_

บทความนี้ใช้กับส่วนประกอบและเวอร์ชันของ Microsoft Dynamics 365 Project Operations ต่อไปนี้:

- Project Operations ในสภาพแวดล้อม Dataverse เวอร์ชัน 4.45.0.53
- การจัดการโครงการและการบัญชีในสภาพแวดล้อม Dynamics 365 Finance เวอร์ชัน 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>การปรับปรุงแผนที่การรวมแบบสองทิศทางของ Project Operations

ไม่มีการปรับปรุงสำหรับแผนที่การรวมแบบสองทิศทางของ Project Operations ในรุ่นนี้ สำหรับรายการปัจจุบันและรุ่นของแผนที่การรวมแบบสองทิศทางของ Project Operations โปรดดูที่ [รุ่นของแผนที่การรวมแบบสองทิศทางของ Project Operations](../environment/resource-dual-write-maps.md)

เรียกใช้แผนที่รุ่นล่าสุดในสภาพแวดล้อมของคุณเสมอ และเปิดใช้งานแผนที่ตารางที่เกี่ยวข้องทั้งหมดเมื่อคุณปรับปรุงโซลูชัน Project Operations Dataverse และรุ่นโซลูชัน Finance ของคุณ คุณลักษณะและความสามารถบางอย่างอาจทำงานไม่ถูกต้องหากไม่มีการเปิดใช้งานแผนผังเวอร์ชันล่าสุด คุณสามารถดูแผนที่เวอร์ชันที่ใช้งานได้ในคอลัมน์ **เวอร์ชัน** บนหน้า **การรวมแบบสองทิศทาง** หากต้องการเปิดใช้งานแผนที่เวอร์ชันใหม่ได้ ให้เลือก **เวอร์ชันแผนที่ของตาราง** เลือกเวอร์ชันล่าสุด และจากนั้น บันทึกเวอร์ชันที่เลือก หากคุณปรับแต่งแผนผังตารางสำเร็จรูป ให้ใช้การเปลี่ยนแปลงอีกครั้ง สำหรับข้อมูลเพิ่มเติม โปรดดู [การจัดการวงจรชีวิตของแอปพลิเคชัน](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

หากคุณประสบปัญหาเมื่อคุณเริ่มต้นแผนผัง ให้ทำตามคำแนะนำในส่วน [ปัญหาคอลัมน์ตารางในแผนผังหายไป](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) ของคู่มือการแก้ไขปัญหาการรวมแบบสองทิศทาง

## <a name="quality-updates"></a>การปรับปรุงคุณภาพ

### <a name="project-operations-on-dataverse"></a>Project Operations บน Dataverse

| พื้นที่คุณลักษณะ | หมายเลขอ้างอิง | การปรับปรุงคุณภาพ |
| --- | --- | --- |
|   การจัดการโอกาสทางการขาย | 2762089 | เกิดข้อผิดพลาดในการจัดการขณะปิดสัญญาเป็นแพ้หากการบันทึกอัตโนมัติในองค์กรถูกปิดใช้งาน|
|การวางแผนและการติดตามโครงการ | 2767841 | การตรวจวัดระยะไกลอัปเดตเอนทิตีโครงการ สร้างหรืออัปเดตสถานการณ์|
|การเรียกเก็บเงินและการกำหนดราคา | 2771072 | การจัดการข้อยกเว้นการอ้างอิงเป็นโมฆะในขณะที่ชนะการเสนอราคา|
|การเรียกเก็บเงินและการกำหนดราคา | 2844181 |ล้มเหลวในการรับรหัสความสัมพันธ์ และการบล็อกการสร้างใบแจ้งหนี้|
|การเรียกเก็บเงินและการกำหนดราคา | 2852836 | ค่าจริงระหว่างบริษัทที่ขาดหายไปสำหรับค่าใช้จ่ายระหว่างบริษัทที่สร้างและอนุมัติใน CE|


### <a name="project-management-and-accounting-in-finance"></a>ภาพรวมการจัดการโครงการและการบัญชีใน Finance

สำหรับข้อมูลเกี่ยวกับการแก้ไขจุดบกพร่องที่รวมอยู่ในการปรับปรุงนี้ ให้ลงชื่อเข้าใช้ Microsoft Dynamics Lifecycle Services (LCS) และดู [บทความ KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438)
