---
title: ภาพรวมของ Project Service Automation
description: หัวข้อนี้แสดงข้อมูลทั่วไปเกี่ยวกับโซลูชันการรวม Dynamics 365 Project Service Automation กับ Dynamics 365 Finance
author: ruhercul
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b8588e664f140ca1b0dd740d27fe6a5137da595
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685585"
---
# <a name="project-service-automation-overview"></a>ภาพรวมของ Project Service Automation

[!include[banner](../includes/banner.md)]


โซลูชันการรวม Project Service Automation กับ Finance ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Dynamics 365 Finance กับ Dynamics 365 Project Service Automation ผ่าน Common Data Service แม่แบบการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ของโครงการ สัญญาโครงการ รายละเอียดการให้บริการตามสัญญาโครงการ เหตุการณ์สำคัญของรายละเอียดการให้บริการตามสัญญาโครงการ งานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประมาณการชั่วโมง และการประมาณการค่าใช้จ่าย จาก Project Service Automation ไปยัง Finance

> [!NOTE]
> - หากคุณใช้เวอร์ชัน 7.3.0 คุณต้องติดตั้ง KB 4074835 จากนั้น คุณจะสามารถรวมโครงการราคาคงที่
> - หากคุณใช้เวอร์ชัน 7.3.0 และคุณนำธุรกรรมค่าธรรมเนียมมาจาก Project Service Automation คุณต้องติดตั้ง KB 4345320 เพื่อรวมค่าธรรมเนียมเหล่านั้นในใบแจ้งหนี้โครงการ
> - หากคุณใช้เวอร์ชัน 8.0 คุณจะสามารถใช้การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประมาณชั่วโมง การประมาณค่าใช้จ่าย และการล็อกฟังก์ชัน
> - หากคุณใช้เวอร์ชัน 8.0.1 หรือใหม่กว่า คุณจะสามารถซิงโครไนซ์ข้อมูลจริงได้

ก่อนที่คุณจะสามารถรวม Project Service Automation Finance คุณต้องตั้งค่าคอนฟิกพารามิเตอร์การรวม Project Service Automation สำหรับข้อมูลเพิ่มเติม ดู [พารามิเตอร์การรวม Project Service Automation](PSA-parameters.md)

โซลูชันการรวมนี้เปิดใช้งานการซิงโครไนซ์โดยตรงในสถานการณ์ต่อไปนี้:

- รักษาสัญญาโครงการใน Project Service Automation และซิงโครไนซ์โดยตรงจาก Project Service Automation ไปยัง Finance
- สร้างโครงการใน Project Service Automation และซิงโครไนซ์โดยตรงจาก Project Service Automation ไปยัง Finance
- รักษารายละเอียดการให้บริการตามสัญญาโครงการใน Project Service Automation และซิงโครไนซ์โดยตรงจาก Project Service Automation ไปยัง Finance
- รักษาเหตุการณ์สำคัญของรายละเอียดการให้บริการตามสัญญาโครงการใน Project Service Automation และซิงโครไนซ์โดยตรงจาก Project Service Automation ไปยัง Finance
- รักษางานใน Project Service Automation และซิงโครไนซ์โดยตรงจาก Project Service Automation ไปยัง Finance
- รักษาประเภทธุรกรรมค่าใช้จ่ายใน Finance และซิงโครไนซ์โดยตรงจาก Finance ไปยัง Project Service Automation
- สร้างการประมาณชั่วโมงของโครงการใน Project Service Automation และซิงโครไนซ์โดยตรงจาก Project Service Automation ไปยัง Finance
- สร้างการประมาณค่าใช้จ่ายของโครงการใน Project Service Automation และซิงโครไนซ์โดยตรงจาก Project Service Automation ไปยัง Finance
- สร้างเวลาโครงการ ค่าใช้จ่าย และค่าธรรมเนียมที่เกิดขึ้นจริงใน Project Service Automation และสร้างธุรกรรมโครงการในสมุดรายวันการรวม Project Service Automation เพื่อให้สามารถลงรายการบัญชีใน Finance

## <a name="data-synchronization"></a>การซิงโครไนซ์ข้อมูล

ภาพประกอบต่อไปนี้แสดงวิธีซิงโครไนซ์ข้อมูลโดยเป็นส่วนหนึ่งของการรวมระหว่าง Project Service Automation และ Finance

> [!NOTE]
> ขณะนี้แม่แบบพร้อมใช้งานบางรายการเท่านั้น แม่แบบจะถูกนำออกใช้ เมื่อเสร็จสมบูรณ์

[![การรวม Project Service Automation กับ Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>ข้อกำหนดของระบบสำหรับ Finance

ในการใช้โซลูชันการรวม Project Service Automation กับ Finance คุณต้องติดตั้ง Enterprise edition 7.3 ที่มีการปรับปรุง Platform 12 หรือใหม่กว่า

## <a name="system-requirements-for-project-service-automation"></a>ข้อกำหนดของระบบสำหรับ Project Service Automation

ในการใช้โซลูชันการรวม Project Service Automation กับ Finance คุณต้องติดตั้งส่วนประกอบต่อไปนี้:

- Dynamics 365 Project Service Automationรุ่น 9.0.0.0 หรือรุ่นที่ใหม่กว่า
- โซลูชัน Prospect to cash สำหรับ Dynamics 365 Sales รุ่น 1.14.0.0 (v14) หรือใหม่กว่า
- โซลูชัน Project Service Automation to Finance สำหรับ Dynamics 365 Project Service Automation รุ่น 1.0.0.0 หรือใหม่กว่า

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>ติดตั้งโซลูชันการรวม Project Service Automation กับ Finance ในอินสแตนซ์ Project Service Automation ของคุณ

ดาวน์โหลดโซลูชันการรวม Project Service Automation กับ Finance จาก [ศูนย์ดาวน์โหลด Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) และปฏิบัติตามคำแนะนำที่มาพร้อมกับโซลูชัน


[!INCLUDE[footer-include](../includes/footer-banner.md)]