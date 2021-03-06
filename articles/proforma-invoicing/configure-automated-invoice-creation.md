---
title: กำหนดค่าการสร้างใบแจ้งหนี้อัตโนมัติ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีกำหนดค่าระบบเพื่อสร้างใบแจ้งหนี้โดยอัตโนมัติ
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898149"
---
# <a name="configure-automated-invoice-creation"></a>กำหนดค่าการสร้างใบแจ้งหนี้อัตโนมัติ

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

ทำตามขั้นตอนต่อไปนี้เพื่อกำหนดค่าใบแจ้งหนี้อัตโนมัติที่ใช้งานใน Project operations

1. ไปที่ **การตั้งค่า** \> **ชุดงาน**
2. สร้างชุดงาน และตั้งชื่อว่า **Project Operations สร้างใบแจ้งหนี้** ชื่อของชุดงานต้องมีคำว่า "สร้างใบแจ้งหนี้"
3. ในฟิลด์ **ชนิดงาน** ให้เลือก **ไม่มี** โดยค่าเริ่มต้น **ความถี่รายวัน** และตัวเลือก **เปิดใช้งาน** จะถูกตั้งค่าเป็น **ใช่**
4. เลือก **เรียกใช้เวิร์กโฟลว์** ในกล่องโต้ตอบ **การค้นหาเรกคอร์ด** คุณจะเห็นสามเวิร์กโฟลว์

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. เลือก **ProcessRunCaller** จากนั้นเลือก **เพิ่ม**
6. ในกล่องโต้ตอบถัดไป ให้เลือก **ตกลง** เวิร์กโฟลว์ **การพักเครื่อง** ตามด้วยเวิร์กโฟลว์ **กระบวนการ**

    นอกจากนี้คุณยังสามารถเลือก **ProcessRunner** ในขั้นตอนที่5 จากนั้น เมื่อคุณเลือก **ตกลง** เวิร์กโฟลว์ **กระบวนการ** ตามด้วยเวิร์กโฟลว์ **การพักเครื่อง**

เวิร์กโฟลว์ **ProcessRunCaller** และ **ProcessRunner** สร้างใบแจ้งหนี้ **ProcessRunCaller** เรียกใช้ **ProcessRunner** **ProcessRunner** เป็นเวิร์กโฟลว์ที่สร้างใบแจ้งหนี้อย่างแท้จริง รวมถึงรายละเอียดการให้บริการตามสัญญาทั้งหมดที่ต้องสร้างใบแจ้งหนี้ และจะมีการสร้างใบแจ้งหนี้สำหรับรายละเอียดเหล่านั้น ในการกำหนดรายละเอียดการให้บริการตามสัญญาที่ต้องสร้างใบแจ้งหนี้ งานจะดูที่วันที่เรียกใช้ใบแจ้งหนี้สำหรับรายละเอียดการให้บริการตามสัญญา ถ้ารายละเอียดการให้บริการตามสัญญาที่เป็นของสัญญาเดียวมีวันที่เรียกใช้ใบแจ้งหนี้เดียวกัน ธุรกรรมจะรวมอยู่ในใบแจ้งหนี้เดียวที่มีรายการใบแจ้งหนี้สองรายการ ถ้าไม่มีธุรกรรมที่จะสร้างใบแจ้งหนี้ งานจะข้ามการสร้างใบแจ้งหนี้

หลังจาก **ProcessRunner** เสร็จสิ้น จะเรียก **ProcessRunCaller** ให้เวลาสิ้นสุด และถูกปิด **ProcessRunCallerr** เริ่มต้นการจับเวลาที่ทำงานเป็นเวลา 24 ชั่วโมง ตั้งแต่เวลาสิ้นสุดที่ระบุ ในตอนท้ายของการจับเวลา **ProcessRunCaller** ถูกปิด

งานกระบวนการชุดงานสำหรับการสร้างใบแจ้งหนี้เป็นงานที่เกิดขึ้นเป็นประจำ ถ้ามีการเรียกใช้กระบวนการชุดงานนี้หลายครั้ง จะมีการสร้างหลายอินสแตนซ์ของงาน และทำให้เกิดข้อผิดพลาด ดังนั้น คุณควรเริ่มต้นกระบวนการชุดงานเพียงครั้งเดียว และคุณควรเริ่มต้นใหม่เฉพาะเมื่อหยุดทำงาน

> [!NOTE]
> การออกใบแจ้งหนี้แบบกลุ่มทำงานเฉพาะสำหรับรายละเอียดการให้บริการตามสัญญาโครงการที่กำหนดค่าโดยกำหนดการใบแจ้งหนี้ รายละเอียดการให้บริการตามสัญญาที่มีวิธีการเรียกเก็บเงินแบบราคาคงที่ ต้องมีการกำหนดค่าเหตุการณ์สำคัญ รายละเอียดการให้บริการตามสัญญาโครงการที่มีวิธีการเรียกเก็บเงินตามเวลาและวัสดุจะต้องมีการตั้งค่ากำหนดการใบแจ้งหนี้ตามวันที่ เช่นเดียวกับรายละเอียดการให้บริการตามสัญญาโครงการ     
