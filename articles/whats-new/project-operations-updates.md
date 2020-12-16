---
title: การปรับปรุง Project Operations
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับรุ่นที่นำออกใช้ของ Dynamics 365 Project Operations
author: sigitac
manager: Annbe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: acafb97b2bb20deaf12db12cd9238cf5ad0817a9
ms.sourcegitcommit: 87dd3b9bb23384e4d0c3208f0341a3de295eefc8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689433"
---
# <a name="project-operations-updates"></a>การปรับปรุง Project Operations

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว และProject Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ตามการผลิต_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="project-operations-components"></a>ส่วนประกอบ Project Operations

Dynamics 365 Project Operations ประกอบด้วยสององค์ประกอบ:

- Project Operations บนสภาพแวดล้อม Common Data Service (CDS)ครอบคลุมถึงความสามารถตั้งแต่โอกาสทางการขายไปจนถึงการออกใบแจ้งหนี้ชั่วคราว CDS ถูกใช้ในการปรับใช้งานแบบ Lite และการปรับใช้สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลังของ Project Operations
- การจัดการโครงการและการบัญชีในสภาพแวดล้อม Dynamics 365 Finance ครอบคลุมถึงความสามารถในการจัดการค่าใช้จ่าย การบัญชีโครงการ และการรับรู้รายได้ สภาพแวดล้อมแอป Finance and Operations ใช้ใน Project Operations สำหรับสถานการณ์ตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก และ Project Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ตามการผลิต

## <a name="project-operations-latest-version"></a>Project Operations รุ่นล่าสุด

| การดำเนินงานโครงการบนสภาพแวดล้อม CDS | การจัดการโครงการและการบัญชีในสภาพแวดล้อมแอป Finance and Operations |
| --- | --- |
| 4.5.0.134 | 10.0.15 |

บันทึกย่อ Project Operations ประจำรุ่นธนวาคม 2020 สำหรับ [ทรัพยากร/ที่ไม่เก็บในคลัง](whats-new-dec-2020-resource-based.md)

## <a name="release-schedule-for-project-operations-on-cds-environment"></a>กำหนดการเผยแพร่สำหรับ Project Operations บนสภาพแวดล้อม CDS

การอัปเดตสำหรับ Project Operations บนสภาพแวดล้อม CDS มีให้บริการทุกเดือน 

| สถานี   | ขอบเขต        | รุ่นปัจจุบัน | รุ่นถัดไป | พร้อมใช้งานโดยทั่วไป |
|-----------|---------------|-----------------|--------------|---------------------|
| สถานี 2 |   &nbsp;      |    &nbsp;       | &nbsp;       |      &nbsp;         |
|   &nbsp;  | อเมริกาใต้ |  4.5.0.134       | TBD     | 08 ม.ค. 21           |
|    &nbsp; | แคนาดา        |  4.5.0.134       | TBD     | 08 ม.ค. 21          |
|   &nbsp;  | อินเดีย         |  4.5.0.134       | TBD     | 08 ม.ค. 21           |
| สถานี 3  |      &nbsp;   |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | ญี่ปุ่น         |  4.5.0.134       | TBD     | 15 ม.ค. 21           |
|   &nbsp;  | เอเชียแปซิฟิก  |  4.5.0.134       | TBD     | 15 ม.ค. 21           |
|   &nbsp;  | สหราชอาณาจักร |  4.5.0.134       | TBD     | 15 ม.ค. 21           |
|   &nbsp;  | โอเชียเนีย       |  4.5.0.134       | TBD     | 15 ม.ค. 21           |
| สถานี 4 |     &nbsp;    |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | ยุโรป        |  4.4.0.70       | 4.5.0.134     | 11 ธ.ค. 20           |
| สถานี 5 |     &nbsp;    |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | อเมริกาเหนือ |  4.4.0.70       | 4.5.0.134     | 18 ธ.ค. 20           |

## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a>กำหนดการเผยแพร่สำหรับการจัดการโครงการและการบัญชีในสภาพแวดล้อมของแอป Finance and Operations

การอัปเดตสำหรับการจัดการโครงการและการบัญชีมีการเผยแพร่แปดครั้งต่อปี

| การเผยแพร่ที่สนับสนุน | พร้อมใช้งานโดยทั่วไป (อัปเดตด้วยตนเอง) |
| --- | --- |
| 10.0.15 | 4 ธันวาคม 2020 |
| 10.0.14 | 23 ตุลาคม 2020 |

วันที่วางจำหน่ายเป้าหมายอาจเปลี่ยนแปลงได้ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การปรับปรุงความพร้อมใช้งานการให้บริการ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=/dynamics365/finance/toc.json)

| วันที่นำออกใช้เป้าหมาย | พร้อมใช้งานโดยทั่วไป (อัปเดตด้วยตนเอง) |
| --- | --- |
| 10.0.16 | 22 มกราคม 2021 |
| 10.0.17 | 1 กุมภาพันธ์ 2021 |

