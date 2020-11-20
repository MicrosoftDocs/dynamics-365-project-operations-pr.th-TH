---
title: การปรับปรุง Project Operations
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับรุ่นที่นำออกใช้ของ Dynamics 365 Project Operations
author: sigitac
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2d1a6b411f17ddf1633443c2cf1526f3424efac6
ms.sourcegitcommit: 3a10fb3b7eaaa983e562ba9cda0576966e09421b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/07/2020
ms.locfileid: "4404129"
---
# <a name="project-operations-updates"></a>การปรับปรุง Project Operations

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว และProject Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ตามการผลิต_

## <a name="project-operations-components"></a>ส่วนประกอบ Project Operations

Dynamics 365 Project Operations ประกอบด้วยสองส่วนประกอบ:

- Project Operations บนสภาพแวดล้อม Common Data Service (CDS)ครอบคลุมถึงความสามารถตั้งแต่โอกาสทางการขายไปจนถึงการออกใบแจ้งหนี้ชั่วคราว CDS ถูกใช้ในการปรับใช้งานแบบ Lite และการปรับใช้สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลังของ Project Operations
- การจัดการโครงการและการบัญชีในสภาพแวดล้อม Dynamics 365 Finance ครอบคลุมถึงความสามารถในการจัดการค่าใช้จ่าย การบัญชีโครงการ และการรับรู้รายได้ สภาพแวดล้อมแอป Finance and Operations ใช้ใน Project Operations สำหรับสถานการณ์ตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก และ Project Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ตามการผลิต

## <a name="project-operations-latest-version"></a>Project Operations รุ่นล่าสุด

| การดำเนินงานโครงการบนสภาพแวดล้อม CDS | การจัดการโครงการและการบัญชีในสภาพแวดล้อมแอป Finance and Operations |
| --- | --- |
| 4.4.0.70 | 10.0.14 |

การดำเนินงานโครงการบันทึกย่อประจำรุ่นเดือนพฤศจิกายน 2020 สำหรับ [ทรัพยากร/ไม่มีในสต็อก](whats-new-nov-2020-resource-based.md) [สต็อก/การผลิต](../prod-pma/whats-new/whats-new-nov-2020-production-based.md) และ [การปรับใช้แบบ Lite](../pro/whats-new/whats-new-nov-2020-lite.md)

## <a name="release-schedule-for-project-operations-on-cds-environment"></a>กำหนดการเผยแพร่สำหรับ Project Operations บนสภาพแวดล้อม CDS

การอัปเดตสำหรับ Project Operations บนสภาพแวดล้อม CDS มีให้บริการทุกเดือน 

| สถานี   | ขอบเขต        | รุ่นปัจจุบัน | รุ่นถัดไป | พร้อมใช้งานโดยทั่วไป |
|-----------|---------------|-----------------|--------------|---------------------|
| สถานี 2 |   &nbsp;      |    &nbsp;       | &nbsp;       |      &nbsp;         |
|   &nbsp;  | อเมริกาใต้ |  4.4.0.70       | TBD     | 20 พ.ย. 20           |
|    &nbsp; | แคนาดา        |  4.4.0.70       | TBD     | 20 พ.ย. 20           |
|   &nbsp;  | อินเดีย         |  4.4.0.70       | TBD     | 20 พ.ย. 20           |
| สถานี 3  |      &nbsp;   |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | ญี่ปุ่น         |  4.4.0.70       | TBD     | 4 ธ.ค. 20           |
|   &nbsp;  | เอเชียแปซิฟิก  |  4.4.0.70       | TBD     | 4 ธ.ค. 20           |
|   &nbsp;  | สหราชอาณาจักร |  4.4.0.70       | TBD     | 4 ธ.ค. 20           |
|   &nbsp;  | โอเชียเนีย       |  4.4.0.70       | TBD     | 4 ธ.ค. 20           |
| สถานี 4 |     &nbsp;    |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | ยุโรป        |  4.4.0.70       | TBD     | 11 ธ.ค. 20           |
| สถานี 5 |     &nbsp;    |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | อเมริกาเหนือ | 4.3.0.61        | 4.4.0.70     | 15 พ.ย. 20           |

## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a>กำหนดการเผยแพร่สำหรับการจัดการโครงการและการบัญชีในสภาพแวดล้อมของแอป Finance and Operations

การอัปเดตสำหรับการจัดการโครงการและการบัญชีมีการเผยแพร่แปดครั้งต่อปี

| การเผยแพร่ที่สนับสนุน | พร้อมใช้งานโดยทั่วไป (อัปเดตด้วยตนเอง) |
| --- | --- |
| 10.0.14 | 23 ตุลาคม 2020 |
| 10.0.13 (พร้อมอัปเดตคุณภาพ ณ วันที่ 2 ตุลาคม 2020) | 18 กันยายน 2020 |

วันที่วางจำหน่ายเป้าหมายอาจเปลี่ยนแปลงได้ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การปรับปรุงความพร้อมใช้งานการให้บริการ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=/dynamics365/finance/toc.json)

| วันที่นำออกใช้เป้าหมาย | พร้อมใช้งานโดยทั่วไป (อัปเดตด้วยตนเอง) |
| --- | --- |
| 10.0.15 | 4 ธันวาคม 2020 |
| 10.0.16 | 22 มกราคม 2021 |

