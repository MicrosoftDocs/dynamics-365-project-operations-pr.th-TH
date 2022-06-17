---
title: การรวม Project Operations ด้วยการรวมแบบสองทิศทาง
description: บทความนี้แสดงภาพรวมของการรวม Project Operations ด้วยการรวมแบบสองทิศทาง
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927995"
---
# <a name="project-operations-dual-write-integration-overview"></a>ภาพรวมของการรวม Project Operations ด้วยการรวมแบบสองทิศทาง

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/ไม่ได้เก็บในคลัง_

Project Operations ใช้ [ความสามารถของการรวมแบบสองทิศทาง](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) เพื่อซิงโครไนซ์ข้อมูลใน Microsoft Dataverse และ Dynamics 365 Finance

ภาพประกอบต่อไปนี้แสดงให้เห็นวิธีการที่ข้อมูลถูกซิงโครไนซ์เป็นส่วนหนึ่งของการรวมระหว่าง Dataverse และ Finance

![ภาพรวมโฟลว์ข้อมูลของ Project Operations](./media/ProjectOperationsFlows.jpg)

Project Operations ใน Dataverse มีอินเทอร์เฟซผู้ใช้ที่ทันสมัย (UI) และความสามารถในการเพิ่มที่ไม่มีรหัส/ที่เขียนโค้ดเล็กน้อยอย่างง่าย โดยใช้ความสามารถ Power Platform ผู้จัดการโครงการ ผู้จัดการทรัพยากร สมาชิกในกลุ่มคนของโครงการ และบุคลากรส่วนหน้าอื่นๆ ดำเนินกิจกรรมของพวกเขาใน Project Operations ใน Dataverse

Project Operations ใน Finance ให้การสนับสนุนการบัญชีโครงการและการรับรู้รายได้ Project Operations เชื่อมต่อกับกรอบงานทางการเงินใน Finance สำหรับการคำนวณภาษีขาย อัตราแลกเปลี่ยนสกุลเงิน การรายงานมิติทางการเงิน และอื่นๆ ประสบการณ์ของนักบัญชีโครงการส่วนใหญ่อยู่ใน Finance

การรวม Project Operations ประกอบด้วยการรวมองค์ประกอบต่อไปนี้:


- [การตั้งค่าและการรวมข้อมูลการตั้งค่าคอนฟิกของ Project Operations](resource-dual-write-setup-integration.md) 
- [การประมาณการและข้อมูลจริงของโครงการ](resource-dual-write-estimates-actuals.md)
- [ใบแจ้งหนี้ของโครงการ](resource-dual-write-project-invoice.md)
- [การจัดการค่าใช้จ่าย](resource-dual-write-expense.md)
- [ใบแจ้งหนี้ของผู้จัดจำหน่าย](resource-dual-write-vendor-invoice.md)
