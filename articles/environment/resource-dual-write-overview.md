---
title: การรวมแบบสองทิศทางของ Project Operations
description: หัวข้อนี้ให้ภาพรวมของการรวมแบบสองทิศทางของ Project Operations
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: b65c40e8aaa9524c1c634738dadd23f21e86e2ec095c47bc849467c8806addbc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007934"
---
# <a name="project-operations-dual-write-integration-overview"></a>ภาพรวมการรวมแบบสองทิศทางของ Project Operations

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_

Project Operations ใช้ [ความสามารถในการรวมแบบสองทิศทาง](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) เพื่อซิงโครไนซ์ข้อมูลระหว่าง Microsoft Dataverse และ Dynamics 365 Finance

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
