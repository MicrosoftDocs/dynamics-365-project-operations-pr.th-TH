---
title: ซิงโครไนซ์งานโครงการโดยตรงจาก Project Service Automation ถึง Finance and Operations
description: หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้เพื่อซิงโครไนซ์งานโครงการโดยตรงจาก Microsoft Dynamics 365 Project Service Automation ถึง Dynamics 365 Finance
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0383607a07def6c21562bf4b0893fe3ce3db6a04
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085914"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>ซิงโครไนซ์งานโครงการโดยตรงจาก Project Service Automation ถึง Finance and Operations

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้เพื่อซิงโครไนซ์งานโครงการโดยตรงจาก Dynamics 365 Project Service Automation ถึง Dynamics 365 Finance

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

## <a name="prerequisites-and-mapping-setup"></a>ข้อกำหนดเบื้องต้นและการตั้งค่าการแม็ป

ก่อนที่จะเกิดการซิงโครไนซ์งานโครงการ คุณต้องซิงโครไนซ์สัญญาโครงการและโครงการ

## <a name="power-query"></a>Power Query

คุณต้องใช้ Microsoft Power Query สำหรับ Excel เพื่อกรองข้อมูล หากตรงตามเงื่อนไขนี้:

- คุณมีเรกคอร์ดเฉพาะทรัพยากรในงานโครงการ

หากคุณต้องใช้ Power Query ให้ปฏิบัติตามแนวทางนี้:

- แม่แบบงานโครงการ (PSA ถึง Fin และ Ops) มีตัวกรองเริ่มต้นที่แยกเรกคอร์ดเฉพาะทรัพยากรออกจากงานโครงการ โดยตั้งค่าตัวกรองใน **IsLineTask** เป็น **เท็จ** หากคุณสร้างแม่แบบของคุณเอง คุณต้องเพิ่มตัวกรองนี้

## <a name="template-mapping-in-data-integration"></a>การแม็ปแม่แบบในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานแม่แบบในการรวมข้อมูล การแม็ปแสดงข้อมูลฟิลด์ที่จะซิงโครไนซ์จาก Project Service Automation ไปยัง Finance

[![การแม็ปแม่แบบ](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
