---
title: มีอะไรใหม่เดือนธันวาคม 2021 - Project Operations สำหรับสถานการณ์ทรัพยากร/ไม่ได้เก็บในคลัง
description: บทความนี้ให้ข้อมูลเกี่ยวกับการปรับปรุงคุณภาพที่มีอยู่ใน Project Operations ประจำเดือนธันวาคม 2021 สำหรับสถานการณ์ตามทรัพยากร/ไม่ได้เก็บในคลัง
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 79ae9f49a4291d162a8a9bb6eb9a22d615773f6e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910883"
---
# <a name="whats-new-december-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>มีอะไรใหม่เดือนธันวาคม 2021 - Project Operations สำหรับสถานการณ์ทรัพยากร/ไม่ได้เก็บในคลัง

*นำไปใช้กับ: Project Operations สำหรับสถานการณ์ทรัพยากร/ไม่ได้เก็บในคลัง*

บทความนี้ใช้กับส่วนประกอบและเวอร์ชันของ Microsoft Dynamics 365 Project Operations ต่อไปนี้:

- Project Operations ในสภาพแวดล้อม Dataverse เวอร์ชัน 4.27.0.195, 4.27.0.242, 4.27.0.244
- การจัดการโครงการและการบัญชีในสภาพแวดล้อม Dynamics 365 Finance เวอร์ชัน 10.0.23

## <a name="features-included-in-this-release"></a>คุณลักษณะที่รวมอยู่ในรุ่นนี้:

- ปรับปรุงการแก้ไขปัญหาสำหรับผู้ดูแลระบบ เมื่อผู้ใช้ไม่สามารถเปิดโครงการได้ ผู้ดูแลระบบสามารถตรวจสอบข้อผิดพลาดที่ไม่เกี่ยวข้องกับสิทธิ์การใช้งานซึ่งเกิดขึ้นจาก Project for the Web ใน [บันทึกการจัดกำหนดการโครงการ](../project-management/schedule-api-logs.md)
- [ใช้รายการตรวจสอบงานใน Microsoft Project for the Web](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) ใน Microsoft Project for the Web คุณสามารถเพิ่มรายการตรวจสอบในงานเพื่อติดตามรายการเฉพาะได้

## <a name="project-operations-dual-write-maps-updates"></a>การปรับปรุงแผนที่การรวมแบบสองทิศทางของ Project Operations

ไม่มีการปรับปรุงสำหรับแผนที่การรวมแบบสองทิศทางของ Project Operations ในรุ่นนี้ สำหรับรายการปัจจุบันและรุ่นของแผนที่การรวมแบบสองทิศทางของ Project Operations โปรดดูที่ [รุ่นของแผนที่การรวมแบบสองทิศทางของ Project Operations](../environment/resource-dual-write-maps.md)

เรียกใช้แผนที่รุ่นล่าสุดในสภาพแวดล้อมของคุณเสมอ และเปิดใช้งานแผนที่ตารางที่เกี่ยวข้องทั้งหมดเมื่อคุณปรับปรุงโซลูชัน Project Operations Dataverse และรุ่นโซลูชัน Finance ของคุณ คุณลักษณะและความสามารถบางอย่างอาจทำงานไม่ถูกต้องหากไม่มีการเปิดใช้งานแผนผังเวอร์ชันล่าสุด คุณสามารถดูแผนที่เวอร์ชันที่ใช้งานได้ในคอลัมน์ **เวอร์ชัน** บนหน้า **การรวมแบบสองทิศทาง** หากต้องการเปิดใช้งานแผนที่เวอร์ชันใหม่ได้ ให้เลือก **เวอร์ชันแผนที่ของตาราง** เลือกเวอร์ชันล่าสุด และจากนั้น บันทึกเวอร์ชันที่เลือก หากคุณปรับแต่งแผนผังตารางสำเร็จรูป ให้ใช้การเปลี่ยนแปลงอีกครั้ง สำหรับข้อมูลเพิ่มเติม โปรดดู [การจัดการวงจรชีวิตของแอปพลิเคชัน](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

หากคุณประสบปัญหาเมื่อคุณเริ่มต้นแผนผัง ให้ทำตามคำแนะนำในส่วน [ปัญหาคอลัมน์ตารางในแผนผังหายไป](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) ของคู่มือการแก้ไขปัญหาการรวมแบบสองทิศทาง

## <a name="quality-updates"></a>การปรับปรุงคุณภาพ

### <a name="project-operations-on-dataverse"></a>Project Operations บน Dataverse

| **พื้นที่คุณลักษณะ** | **หมายเลขอ้างอิง** | **การปรับปรุงคุณภาพ** |
| --- | --- | --- |
| การวางแผนและการติดตาม | 2392596 | ตอนนี้ API กำหนดการให้คุณสามารถปรับปรุงฟิลด์ **ความพยายามที่เหลืออยู่**, **ความพยายามที่เสร็จสิ้น** และ **% ที่สมบูรณ์** ได้แล้ว |
| การวางแผนและการติดตาม | 2478497 | ฟิลด์ **หมายเลขกิจกรรม** และ **รหัสงาน** สำหรับ API กำหนดการสามารถเว้นว่างไว้ได้เนื่องจากระบบจะเติมข้อมูลโดยใช้การกำหนดหมายเลขอัตโนมัติ|
| เวลาและค่าใช้จ่าย | 2468135 | จำนวนครั้งของการขออนุมัติใหม่จะลดลงจากห้าเป็นสามครั้ง |
| เวลาและค่าใช้จ่าย | 2468188 | แก้ไขปัญหาข้อความบันทึกเกินความยาวสูงสุดในแอตทริบิวต์ **notetext** ของเอนทิตี **คำอธิบายประกอบ** |
| การเรียกเก็บเงินและการกำหนดราคา | 2488698 | ปรับปรุงข้อความแสดงข้อผิดพลาดที่เกิดขึ้นเมื่อการตั้งค่าสภาพแวดล้อมไม่มีเรกคอร์ดเอนทิตีบัญชีแยกประเภทที่เติมข้อมูลจาก Finance |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>การจัดการโครงการและการบัญชีใน Dynamics 365 Finance

| **พื้นที่คุณลักษณะ** | **หมายเลขอ้างอิง** | **การปรับปรุงคุณภาพ** |
| --- | --- | --- |
| การจัดการและการบัญชีโครงการ | [587187](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D587187&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225501421%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=qpKECMgKZe9sHGVZUhBxs%2F4ou3fXIiFFg2amMTJ6t9U%3D&amp;reserved=0) | บัญชีรายได้ระหว่างบริษัทจะมีการพิจารณาเฉพาะ **ทั้งหมด - ทุกรายการ** โดยไม่รวมกลุ่มภาษีขาย |
| การจัดการและการบัญชีโครงการ | [599568](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D599568&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225600986%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=IudfEjWmkNeiTsWmR%2Fu2oR0CnnCkffAshvqZJuF76q8%3D&amp;reserved=0) | ค่าประมาณการแบบเส้นตรงคำนวณอย่างไม่ถูกต้อง |
| การจัดการและการบัญชีโครงการ | [602728](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D602728&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227094434%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=Q2%2BveFHlGrzg4QHtqcgeqjyZSQkmpr%2Fku7oObKHMB9g%3D&amp;reserved=0) | ปัญหาการลงรายการบัญชีกับรายได้ที่ออกใบแจ้งหนี้ของโครงการในกรณีค่าธรรมเนียมล่วงหน้าที่ทำให้ธุรกรรมในใบสำคัญไม่สอดคล้องกัน |
| การจัดการและการบัญชีโครงการ | [610906](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D610906&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227134259%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=xDBnz10T71GmOZt78ooFK3SYvmTLoC5fj1OftYNYDpY%3D&amp;reserved=0) | การปรับปรุงประสิทธิภาพสำหรับการรวมกับข้อมูลจริงของ Project Operations |
| การจัดการและการบัญชีโครงการ | [618670](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D618670&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227203949%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=PqvHsTGLcQ3bYbUlzYABYhl7J9v2zbnjcOgm%2FTvXB20%3D&amp;reserved=0) | ผู้ใช้ไม่สามารถออกใบแจ้งหนี้ได้หากลงรายการบัญชีธุรกรรมต้นทุนชั่วโมงด้วย **ห้ามใช้บัญชีแยกประเภท** หรือ **ไม่มีบัญชีแยกประเภท** |
| การจัดการและการบัญชีโครงการ | [623818](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D623818&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227303517%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=LAfdEiuKG8DoGk8O48MRLuaKYDINhCyMAtrlpGvVAw0%3D&amp;reserved=0) | ชุดงานล้มเหลวถ้าลงรายการบัญชีสมุดรายวันรายการใดรายการหนึ่งล้มเหลวและไม่มีการประมวลผลสมุดรายวันที่เหลือ  |
| การเดินทางและค่าใช้จ่าย | [575378](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D575378&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225451644%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=3tW0ngQqcz8pdNFY8FVuFlsgv3l73HMgeQTLbzIAAOg%3D&amp;reserved=0) | สถานะการอนุมัติสำหรับค่าใช้จ่ายที่ไม่ได้แนบสามารถเปลี่ยนแปลงได้ |
| การเดินทางและค่าใช้จ่าย | [592997](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D592997&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225521336%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=0leQsokHcl2NLqePFXC6%2BuH1V5UNRWUIPx0wTUaB4vg%3D&amp;reserved=0) | รายงานค่าใช้จ่ายที่ส่งไปยังเวิร์กโฟลว์ช่วยให้คุณสามารถสร้างรายการค่าใช้จ่ายใหม่ได้ |
| การเดินทางและค่าใช้จ่าย | [594853](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D594853&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225541248%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=5PINC45EBeV8PC0Cvtt0QPPJn0VYQ%2FRCjBmlEsZJCq4%3D&amp;reserved=0) | คุณสามารถรีเซ็ตรายการค่าใช้จ่ายที่ยังไม่ได้ลงรายการบัญชีในรายงานค่าใช้จ่ายได้ |
| การเดินทางและค่าใช้จ่าย | [599821](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D599821&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225610944%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=eb2CAb8L9IUDxDoukDcZQxNyI3TNQtFO%2FcjycucNj44%3D&amp;reserved=0) | ถ้ามีค่าใช้จ่ายที่ไม่ได้แนบซึ่งเจ้าของค่าใช้จ่ายเป็นพนักงาน คุณจะไม่สามารถเปิดใช้งานคุณลักษณะการเบิกเงินสดล่วงหน้าสำหรับค่าใช้จ่ายได้ |
| การเดินทางและค่าใช้จ่าย | [601446](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D601446&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225650767%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=Z4CBMqrmYtlIEBWxzMEBf%2BXu5dlst7NnKcQ62yoV%2BWM%3D&amp;reserved=0) | หากคำขอเดินทางตั้งค่าเป็นไม่มีค่า **IsPreAuthorized** ไม่ควรเปิดใช้งานในส่วนหัวของค่าใช้จ่าย |
| การเดินทางและค่าใช้จ่าย | [601753](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D601753&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225660718%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=PVwbDhH5uqGJJZTNLddsHYlHsCknK%2FC%2FY%2Btg6fu8heo%3D&amp;reserved=0) | ฟิลด์ **เรียกเก็บเงินได้** ใน **การจัดการค่าใช้จ่าย** จะถูกล้างเมื่อมีการบันทึกค่าใช้จ่าย |
| การเดินทางและค่าใช้จ่าย | [602009](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D602009&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225680636%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=t3m29Vkxx8g96CvaDz%2FRzuciP2doP2xejomPl440wNs%3D&amp;reserved=0) | เมื่อคุณลบการแสดงรายการที่มีประเภทย่อยที่เลือก **ยกเว้นจากการเก็บภาษี** ไว้ ตัวเลื่อน **รวมภาษี** จะเลื่อนไปที่ **ไม่** สำหรับรายงานค่าใช้จ่าย |
| การเดินทางและค่าใช้จ่าย | [607516](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D607516&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225849894%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=%2BceTskfUl1kTe2XHk6QSYu9UN%2FE%2F9nP2gv20kVweURA%3D&amp;reserved=0) |เหตุการณ์ทางการบัญชีว่างเปล่าและสถานะทางการบัญชีไม่ถูกต้อง |
| การเดินทางและค่าใช้จ่าย | [617801](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D617801&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919226337756%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=L69x65xY6LQDS1u2sUbVX5QKEYgbDh6lld2Pm%2BSsUyI%3D&amp;reserved=0) | เวิร์กโฟลว์ประเมินรายงานค่าใช้จ่ายอย่างไม่ถูกต้องเมื่อมีการแบ่งค่าใช้จ่ายในธุรกรรมบัตรเครดิต |
| การเดินทางและค่าใช้จ่าย | [575295](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D575295&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227074518%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=FyrzO1Yx%2BWLfw5arIrFiW07QZC%2F%2BpUk3ekx3g66X8bE%3D&amp;reserved=0) | ยอดเงินในสกุลเงินการรายงานที่ไม่ถูกต้องในธุรกรรมธนาคารของผู้จัดจำหน่ายถูกลงรายการบัญชีในรอบระยะเวลาที่ปิดจากรายงานค่าใช้จ่าย |
| การเดินทางและค่าใช้จ่าย | [610910](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D610910&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227134259%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=P6wVchjx9GcH7nZ07yg3%2FuEFht6Df7Ew5Z4hSL%2BQ8oY%3D&amp;reserved=0) | ในคุณลักษณะรายงานค่าใช้จ่ายที่ออกแบบใหม่ วิธีการชำระเงินเริ่มต้นจะได้รับการเติมข้อมูลรายการค่าใช้จ่าย แม้ว่าวิธีการชำระเงินจะเปลี่ยนไปเมื่อมีการสร้างค่าใช้จ่าย |
| การเดินทางและค่าใช้จ่าย | [617146](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D617146&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227193996%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=134C%2BXGuzA8GmM7ZjWYaiYQfNqnV9a1mEKuzrh0hzpw%3D&amp;reserved=0) | คุณไม่สามารถส่งรายงานค่าใช้จ่ายได้หากเปิดใช้งานนโยบายการรับสินค้า |
| การเดินทางและค่าใช้จ่าย | [619783](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D619783&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227243778%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=pV1rLgOniDy3hXMHAtXeD9o4ZPTmyhZHd7O7zCUpLLs%3D&amp;reserved=0) | ข้อผิดพลาดต่อไปนี้จะเกิดขึ้นเมื่อคุณส่งรายงานค่าใช้จ่าย **การติดตามสแต็ก: บริษัทไม่มีอยู่** |
| การเดินทางและค่าใช้จ่าย | [620773](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D620773&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227253737%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=%2B5ZZAsXV%2FM29%2Byg6JoGzwJFRa1Fi4NDj4BB38ZeYTH0%3D&amp;reserved=0) | เมื่อมีรายการค่าใช้จ่ายระหว่างบริษัท การกระจายไม่ปรับปรุงนิติบุคคลเมื่อมีการเพิ่มธุรกรรมที่ไม่ได้แนบอีกครั้งในรายงานค่าใช้จ่าย |
| การเดินทางและค่าใช้จ่าย | [621967](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D621967&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227273644%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=RdiupzmL8Dp8nqQIHu9rGMTdJ%2FVVhqN5EIP5uFYS2W4%3D&amp;reserved=0) | ราคาขายและยอดเงินในสกุลเงินการรายงานภายใต้ธุรกรรมของผู้จัดจำหน่ายมีการคำนวณอย่างไม่ถูกต้องในรายงานค่าใช้จ่ายที่เกี่ยวข้องกับโครงการ และสร้างขึ้นในสกุลเงินต่างประเทศโดยใช้ธุรกรรมบัตรเครดิตที่นำเข้า |