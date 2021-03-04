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
ms.openlocfilehash: b90de169bd9ed2c408f1fded20a6fe95f55ce230
ms.sourcegitcommit: 625b5244aaadff5a24a79d9addff91f87c6b015a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/09/2021
ms.locfileid: "5141230"
---
# <a name="project-operations-updates"></a>การปรับปรุง Project Operations

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว และProject Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ตามการผลิต_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="project-operations-components"></a>ส่วนประกอบ Project Operations

Dynamics 365 Project Operations ประกอบด้วยสององค์ประกอบ:

- Project Operations บนสภาพแวดล้อม Dataverse ครอบคลุมถึงความสามารถตั้งแต่โอกาสทางการขายไปจนถึงการออกใบแจ้งหนี้ชั่วคราว Dataverse ถูกใช้ในการปรับใช้งานอย่างง่าย และการปรับใช้สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลังของ Project Operations
- การจัดการโครงการและการบัญชีในสภาพแวดล้อม Dynamics 365 Finance ครอบคลุมถึงความสามารถในการจัดการค่าใช้จ่าย การบัญชีโครงการ และการรับรู้รายได้ สภาพแวดล้อมแอป Finance and Operations ใช้ใน Project Operations สำหรับสถานการณ์ตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก และ Project Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ตามการผลิต

## <a name="project-operations-latest-version"></a>Project Operations รุ่นล่าสุด

| Project Operations บนสภาพแวดล้อม Dataverse | การจัดการโครงการและการบัญชีในสภาพแวดล้อมแอป Finance and Operations |
| --- | --- |
| 4.7.0.95 | 10.0.16 |

บันทึกย่อประจำรุ่นของ Project Operations เดือนมกราคม 2021 สำหรับสถานการณ์จำลอง [ทรัพยากร/ที่ไม่เก็บในคลัง](whats-new-feb-2021-resource-based.md) [การปรับใช้งานอย่างง่าย](../pro/whats-new/whats-new-feb-2021-lite.md) และ [ที่เก็บในคลัง/การผลิต](../prod-pma/whats-new/whats-new-jan-2021-stocked.md)

## <a name="release-schedule-for-project-operations-on-dataverse-environment"></a>กำหนดการเผยแพร่สำหรับ Project Operations บนสภาพแวดล้อม Dataverse

การอัปเดตสำหรับ Project Operations บนสภาพแวดล้อม Dataverse มีให้บริการทุกเดือน 

| สถานี   | ภูมิภาค        | รุ่นปัจจุบัน | รุ่นถัดไป | พร้อมใช้งานโดยทั่วไป |
|-----------|---------------|-----------------|--------------|---------------------|
| สถานี 1 |   &nbsp;      |    &nbsp;       | &nbsp;       |      &nbsp;         |
|   &nbsp;  | การเปิดตัวครั้งแรก |  4.7.0.95       | TBD     | 19 ก.พ. 21           |
| สถานี 2 |   &nbsp;      |    &nbsp;       | &nbsp;       |      &nbsp;         |
|   &nbsp;  | อเมริกาใต้ |  4.7.0.95       | TBD     | 19 ก.พ. 21           |
|    &nbsp; | แคนาดา        |  4.7.0.95       | TBD     | 19 ก.พ. 21           |
|   &nbsp;  | อินเดีย         |  4.7.0.95       | TBD     | 19 ก.พ. 21           |
|   &nbsp;  | ฝรั่งเศส         |  4.7.0.95       | TBD     | 19 ก.พ. 21           |
|   &nbsp;  | สหรัฐอาหรับเอมิเรตส์         |  4.7.0.95       | TBD     | 19 ก.พ. 21           |
| สถานี 3  |      &nbsp;   |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | ญี่ปุ่น         |  4.7.0.95       | TBD     | 26 ก.พ. 21           |
|   &nbsp;  | เอเชียแปซิฟิก  |  4.7.0.95       | TBD     | 26 ก.พ. 21           |
|   &nbsp;  | สหราชอาณาจักร |  4.7.0.95       | TBD     | 26 ก.พ. 21           |
|   &nbsp;  | โอเชียเนีย       |  4.7.0.95       | TBD     | 26 ก.พ. 21           |
| สถานี 4 |     &nbsp;    |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | ยุโรป        |  4.6.0.161       | 4.7.0.95     | 12 ก.พ. 21           |
| สถานี 5 |     &nbsp;    |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | อเมริกาเหนือ |  4.6.0.161       | 4.7.0.95     | 19 ก.พ. 21           |

## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a>กำหนดการเผยแพร่สำหรับการจัดการโครงการและการบัญชีในสภาพแวดล้อมของแอป Finance and Operations

การอัปเดตสำหรับการจัดการโครงการและการบัญชีมีการเผยแพร่แปดครั้งต่อปี

| การเผยแพร่ที่สนับสนุน | พร้อมใช้งานโดยทั่วไป (อัปเดตด้วยตนเอง) |
| --- | --- |
| 10.0.16 | 22 มกราคม 2021 |
| 10.0.15 | 4 ธันวาคม 2020 |


วันที่วางจำหน่ายเป้าหมายอาจเปลี่ยนแปลงได้ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การปรับปรุงความพร้อมใช้งานการให้บริการ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=/dynamics365/finance/toc.json)

| วันที่นำออกใช้เป้าหมาย | พร้อมใช้งานโดยทั่วไป (อัปเดตด้วยตนเอง) |
| --- | --- |
| 10.0.17 | 19 มีนาคม 2021 |
| 10.0.18 | 16 เมษายน 2021 |
