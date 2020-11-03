---
title: ใช้ข้อมูลสาธิตของ Project Operations กับสภาพแวดล้อมที่โฮสต์บนระบบคลาวด์ของ Finance
description: หัวข้อนี้อธิบายถึงวิธีการใช้ข้อมูลสาธิตจาก Project Operations กับภาพแวดล้อมที่โฮสต์บนระบบคลาวด์ของ Dynamics 365 Finance
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1a94862d5a024eb1630f33c0c96699e8b4b49bf2
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949115"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a>ใช้ข้อมูลสาธิตของ Project Operations กับสภาพแวดล้อมที่โฮสต์บนระบบคลาวด์ของ Finance

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_

>[สำคัญ] หัวข้อนี้ใช้ได้เฉพาะ Microsoft Dynamics 365 Finance เวอร์ชัน 10.0.13 เท่านั้นและสามารถทำได้บนสภาพแวดล้อมที่โฮสต์บนระบบคลาวด์เท่านั้น ทำตามขั้นตอนในหัวข้อนี้ **ก่อน** คุณจึงจะสามารถใช้การปรับปรุงคุณภาพกับสภาพแวดล้อมได้

1. ในโครงการ LCS ของคุณ ให้เปิดเพจ **รายละเอียดสภาพแวดล้อม** สังเกตว่ามีรายละเอียดที่จำเป็นในการเชื่อมต่อกับสภาพแวดล้อมโดยใช้โพรโทคอลการใช้เดสก์ท็อประยะไกล (RDP)

![ รายละเอียดสภาพแวดล้อม](./media/1EnvironmentDetails.png)

ข้อมูลประจำตัวที่ไฮไลต์ชุดแรกคือข้อมูลประจำตัวของบัญชีภายในเครื่องและมีไฮเปอร์ลิงก์ไปยังการเชื่อมต่อเดสก์ท็อประยะไกล ข้อมูลประจำตัวงรวมถึงชื่อผู้ใช้และรหัสผ่านของผู้ดูแลระบบสภาพแวดล้อม ข้อมูลประจำตัวชุดที่สองใช้เพื่อเข้าสู่ระบบ SQL Server ในสภาพแวดล้อมนี้

2. เชื่อมต่อกับสภาพแวดล้อมจากระบะไกลโดยใช้ไฮเปอร์ลิงก์ใน **บัญชีภายในเครื่อง** และใช้ **ข้อมูลประจำตัวบัญชีภายในเครื่อง** เพื่อรับรองความถูกต้อง
3. ไปที่ **บริการข้อมูลอินเทอร์เน็ต** > **แอปพลิเคชันพูล** > **AOSService** และหยุดบริการ คุณกำลังหยุดบริการในตอนนี้เพื่อให้คุณสามารถแทนที่ฐานข้อมูล SQL ต่อไปได้

![หยุด AOS](./media/2StopAOS.png)

4. ไปที่ **บริการ** และหยุดสองรายการต่อไปนี้:

- Microsoft Dynamics 365 Unified Operations: บริการจัดการชุดงาน
- Microsoft Dynamics 365 Unified Operations: กรอบงานการนำเข้าส่งออกข้อมูล

![หยุดบริการ](./media/3StopServices.png)

5. เปิด Microsoft SQL Server Management Studio. เข้าสู่ระบบด้วยข้อมูลประจำตัวของ SQL Server และใช้ผู้ใช้ axdbadmin และรหัสผ่านจากเพจ **รายละเอียดสภาพแวดล้อม** ของ LCS

![SQL Server Management Studio](./media/4SSMS.png)

6. ใน Object Explorer, **ฐานข้อมูล** และค้นหา **AXDB** คุณจะแทนที่ฐานข้อมูลด้วยฐานข้อมูลใหม่ที่อยู่ใน [ศูนย์ดาวน์โหลด](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip) 
7. คัดลอกไฟล์ zip ไปยัง VM ที่คุณเข้าถึงระยะไกลและแยกเนื้อหา zip
8. ใน SQL Server Management Studio คลิกขวา **AxDB** แล้วเลือก **งาน** > **คืนค่า** > **ฐานข้อมูล**

![คืนค่าฐานข้อมูล](./media/5RestoreDatabase.png)

9. เลือก **อุปกรณ์ต้นทาง** และไปที่ไฟล์ที่แยกจาก zip ที่คุณคัดลอก

![อุปกรณ์ต้นทาง](./media/6SourceDevice.png)

10. เลือก **ตัวเลือก** แล้วเลือก **เขียนทับฐานข้อมูลที่มีอยู่** และ **ปิดการเชื่อมต่อไปยังฐานข้อมูลปลายทางที่มีอยู่** 
11. เลือก **ตกลง**

![คืนค่าการตั้งค่า](./media/7RestoreSetting.png)

คุณจะได้รับการยืนยันว่าการคืนค่า AXDB สำเร็จแล้ว หลังจากที่คุณได้รับการยืนยันนี้ คุณสามารถปิด SQL Services Management Studio

12. กลับไปที่ **บริการข้อมูลอินเทอร์เน็ต** > **แอปพลิเคชันพูล** > **AOSService** และเริ่มต้น AOSService
13. ไปที่ **บริการ** และเริ่มบริการสองอย่างที่คุณหยุดไว้ก่อนหน้านี้

14. ค้นหาเครื่องมือ AdminUserProvisioning บน VM นี้ ดูที่ K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe
15. เรียกใช้ไฟล์ .ext โดยใช้ที่อยู่ผู้ใช้ของคุณในฟิลด์ **ที่อยู่อีเมล** 
16. เลือก **ส่ง**

![การจัดเตรียมผู้ใช้ที่เป็นผู้ดูแลระบบ](./media/8AdminUserProvisioning.png)

การดำเนินการนี้ใช้เวลาสองถึงสามนาที คุณควรได้รับข้อความยืนยันว่าปรับปรุงผู้ใช้ที่เป็นผู้ดูแลระบบเรียบร้อยแล้ว

17. สุดท้ายเรียกใช้พร้อมท์รับคำสั่งเป็นผู้ดูแลระบบและดำเนินการ iisreset

![ตั้งค่า IIS ใหม่](./media/9IISReset.png)

18. ปิดเซสชันเดสก์ท็อประยะไกลและใช้เพจ **รายละเอียดสภาพแวดล้อม** ของ LCS เพื่อเข้าสู่สภาพแวดล้อมในการยืนยันว่าทำงานได้ตามที่คาดไว้

![Finance and Operations](./media/10FinanceAndOperations.png)