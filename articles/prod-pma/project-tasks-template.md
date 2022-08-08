---
title: ซิงโครไนส์งานโครงการโดยตรงจาก Project Service Automation ไปยังการเงินและการดำเนินงาน
description: บทความนี้อธิบายเทมเพลตและงานพื้นฐานที่ใช้ซิงโครไนส์งานโครงการโดยตรงจาก Microsoft Dynamics 365 Project Service Automation ไปยัง Dynamics 365 Finance
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ed559fcd9e0e666f68e7d9f4f1fca91417fe4970
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028449"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>ซิงโครไนส์งานโครงการโดยตรงจาก Project Service Automation ไปยังการเงินและการดำเนินงาน

[!include[banner](../includes/banner.md)]

บทความนี้อธิบายเทมเพลตและงานพื้นฐานที่ใช้ซิงโครไนส์งานโครงการโดยตรงจาก Dynamics 365 Project Service Automation ไปยัง Dynamics 365 Finance

> [!NOTE]
> - การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประมาณชั่วโมง การประมาณค่าใช้จ่าย และการล็อกฟังก์ชัน จะพร้อมใช้งานในเวอร์ชัน 8.0
> - หากคุณใช้ Enterprise Edition 7.3.0 หลังจากที่คุณติดตั้ง KB 4132657 และ KB 4132660 คุณจะสามารถใช้แม่แบบเพื่อรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประมาณชั่วโมง การประมาณค่าใช้จ่ายและข้อมูลจริง และเพื่อตั้งค่าคอนฟิกการล็อกฟังก์ชัน หากคุณต้องรีเซ็ตการกระจายการลงบัญชี เราขอแนะนำให้คุณติดตั้ง KB 4131710 ด้วย
> - การรวมจริงพร้อมใช้งานในเวอร์ชัน 8.0.1 หรือใหม่กว่า

## <a name="data-flow-for-project-service-automation-to-finance"></a>โฟลว์ข้อมูลสำหรับ Project Service Automation กับ Finance

โซลูชันการรวม Project Service Automation กับ Finance ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนซ์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance แม่แบบการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ของข้อมูลเกี่ยวกับงานโครงการจาก Project Service Automation ไปยัง Finance

ภาพประกอบต่อไปนี้แสดงวิธีซิงโครไนซ์ข้อมูลระหว่าง Project Service Automation และ Finance

[![โฟลว์ข้อมูลสำหรับการรวม Project Service Automation กับ Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>แม่แบบและงาน

ในการเข้าถึงแม่แบบ ในศูนย์การจัดการ Microsoft Power Apps เลือก **โครงการ** และจากนั้น ที่มุมขวาบน ให้เลือก **โครงการใหม่** เพื่อเลือกแม่แบบสาธารณะ

แม่แบบและงานพื้นฐานต่อไปนี้ถูกใช้เพื่อซิงโครไนซ์งานโครงการจาก Project Service Automation ถึง Finance:

- **ชื่อของแม่แบบในการรวมข้อมูล:** งานโครงการ (PSA ถึง Fin และ Ops)
- **ชื่อของงานในโครงการ:** งานโครงการ

ก่อนที่จะเกิดการซิงโครไนซ์งานโครงการ คุณต้องซิงโครไนซ์สัญญาโครงการและโครงการ

## <a name="entity-set"></a>ชุดเอนทิตี

| Project Service Automation | Finance                             |
|----------------------------|-------------------------------------|
| งานโครงการ              | เอนทิตีการรวมสำหรับงานโครงการ |

## <a name="entity-flow"></a>โฟลว์เอนทิตี

งานโครงการได้รับการจัดการใน Project Service Automation และมีการซิงโครไนซ์กับ Finance เป็นกิจกรรมของโครงการ

## <a name="prerequisites-and-mapping-setup"></a>ข้อกำหนดเบื้องต้นและการตั้งค่าการแมป

ก่อนที่จะเกิดการซิงโครไนซ์งานโครงการ คุณต้องซิงโครไนซ์สัญญาโครงการและโครงการ

## <a name="power-query"></a>Power Query

คุณต้องใช้ Microsoft Power Query for Excel เพื่อกรองข้อมูล ถ้าเป็นไปตามเงื่อนไขนี้:

- คุณมีเรกคอร์ดเฉพาะทรัพยากรในงานโครงการ

ถ้าคุณต้องใช้ Power Query ให้ทำตามคำแนะนำนี้:

- แม่แบบงานโครงการ (PSA ถึง Fin และ Ops) มีตัวกรองเริ่มต้นที่แยกเรกคอร์ดเฉพาะทรัพยากรออกจากงานโครงการ โดยตั้งค่าตัวกรองใน **IsLineTask** เป็น **เท็จ** หากคุณสร้างแม่แบบของคุณเอง คุณต้องเพิ่มตัวกรองนี้

## <a name="template-mapping-in-data-integration"></a>การแมปแม่แบบในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแมปงานแม่แบบในการรวมข้อมูล การแมปแสดงข้อมูลฟิลด์ที่จะซิงโครไนซ์จาก Project Service Automation ไปยัง Finance

[![การแมปเทมเพลต](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]