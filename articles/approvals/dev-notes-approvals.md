---
title: หมายเหตุสำหรับนักพัฒนาสำหรับการอนุมัติ
description: หัวข้อนี้ให้ข้อมูลนักพัฒนาเพิ่มเติมเกี่ยวกับการทำงานกับการอนุมัติ
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483971"
---
# <a name="developer-notes-for-approvals"></a>หมายเหตุสำหรับนักพัฒนาสำหรับการอนุมัติ

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

Dynamics 365 Project Operations มีตรรกะการตรวจสอบความถูกต้องที่ช่วยให้แน่ใจว่าการเปลี่ยนแปลงเรกคอร์ดที่ถูกต้องผ่านขั้นตอนการอนุมัติ การเปลี่ยนเรกคอร์ดที่ถูกต้องทำให้แน่ใจว่า: 

  - แถวที่สนับสนุนทั้งหมดถูกสร้างขึ้นในตารางที่เกี่ยวข้อง เช่น สมุดรายวัน และข้อมูลจริง
  - ผู้อนุมัติถูกทำเครื่องหมายเป็น **ผู้อนุมัติโครงการ** ในโครงการก่อนดำเนินการต่อ
