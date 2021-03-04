---
title: การวิเคราะห์ใบเสนอราคาโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการวิเคราะห์ใบเสนอราคาโครงการ
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 361a940261811467c46222c3d58c9504434ec882
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145246"
---
# <a name="analysis-of-project-quotes"></a>การวิเคราะห์ใบเสนอราคาโครงการ

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation วิเคราะห์ใบเสนอราคาโครงการเพื่อประเมินผลกำไร นอกจากนี้ยังวิเคราะห์ว่าใบเสนอราคาสอดคล้องกับความคาดหวังของลูกค้ามากน้อยแค่ไหน เกี่ยวกับวันที่จัดส่งหรือวันที่เสร็จสมบูรณ์ และเกี่ยวกับงบประมาณ.

## <a name="profitability-analysis"></a>การวิเคราะห์ความสามารถในการทำกำไร

Project Service Automation วิเคราะห์การทำกำไรโดยใช้กำไรขั้นต้นและกำไรขั้นต้นที่ปรับปรุง

- กำไรขั้นต้นจะถูกคำนวณโดยใช้สูตรต่อไปนี้:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- กำไรขั้นต้นที่ปรับปรุงจะถูกคำนวณโดยใช้สูตรต่อไปนี้:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

ถ้าค่าสำหรับกำไรขั้นต้นและกำไรขั้นต้นที่ปรับปรุงแตกต่างกันไปตามระยะขอบกว้าง การทำงานจำนวนมากในใบเสนอราคาจะถูกจัดประเภทเป็นไม่คิดค่าธรรมเนียม

## <a name="analysis-of-customer-expectations"></a>การวิเคราะห์ความคาดหมายของลูกค้า

คุณสามารถวิเคราะห์ใบเสนอราคาและสร้างแผนภูมิสำหรับความคาดหมายของลูกค้าเกี่ยวกับกำหนดการและงบประมาณ ถ้าคุณป้อนค่าสำหรับฟิลด์ต่อไปนี้:

- ฟิลด์ **วันที่จัดส่งที่ร้องขอ** บนส่วนหัวของใบเสนอราคา
- ฟิลด์ **งบประมาณลูกค้า** สำหรับแต่ละบรรทัดใบเสนอราคา (สำหรับบรรทัดตามโครงการและบรรทัดตามผลิตภัณฑ์)

การวิเคราะห์ความคาดหมายของลูกค้าเกี่ยวกับกำหนดการจะทำโดยการเปรียบเทียบวันที่สิ้นสุดของรายละเอียดบรรทัดใบเสนอราคากับวันที่จัดส่งที่ร้องขอในบรรทัดใบเสนอราคาทั้งหมดในใบเสนอราคา

การวิเคราะห์ความคาดหมายของลูกค้าเกี่ยวกับงบประมาณจะทำโดยการเปรียบเทียบผลรวมของงบประมาณลูกค้ากับยอดเงินที่เสนอในบรรทัดใบเสนอราคาทั้งหมด


[!INCLUDE[footer-include](../includes/footer-banner.md)]