---
title: เอนทิตี, การควบคุม และการเปลี่ยนแปลงส่วนติดต่อผู้ใช้ (Project Service Automation 3.x)
description: หัวข้อนี้อธิบายถึงการเปลี่ยนแปลงโซลูชันสำหรับ Project Service Automation 3.x Microsoft Dynamics
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 48062eda1f524dd3ca0d5feccf11fd5577521275
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148756"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>เอนทิตี, การควบคุม และการเปลี่ยนแปลงส่วนติดต่อผู้ใช้ (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


ด้วยการเปิดตัว Project Service Automation (PSA) 3.x Microsoft Dynamics ได้สร้างการเปลี่ยนแปลงจำนวนมากกับเอนทิตี, การควบคุม, มุมมอง และส่วนติดต่อผู้ใช้ หัวข้อนี้ให้ข้อมูลเกี่ยวกับการเปลี่ยนแปลงที่สำคัญเหล่านี้

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>ความสัมพันธ์หลัก-รองของเอนทิตีเอกสารการขาย, รายการเอกสารการขาย และรายละเอียดรายการเอกสารการขาย
ในรุ่นต่าง ๆ ของ Dynamics 365 Project Service Automation (PSA) ที่ถูกนำออกใช้ก่อนเวอร์ชัน 3.0 บางความสัมพันธ์ระหว่างเอนทิตีเอกสารการขาย, รายการเอกสารการขาย และรายละเอียดรายการเอกสารการขาย ได้ถูกนำมาใช้ผ่านฟิลด์สตริงที่จะเป็นตัวแทนสตริงของ GUID ของเอนทิตีที่เกี่ยวข้อง เนื่องมาจากข้อจำกัดของแพลตฟอร์มที่จำเป็นต้องใช้รหัสสำคัญที่กำหนดเองบนเซิร์ฟเวอร์ และด้านไคลเอ็นต์ของโซลูชัน เพื่อทำให้ความสัมพันธ์ทำงานคล้ายกับความสัมพันธ์เอนทิตี Dynamics CRM ทั่วไป และเพื่อทำให้ฟิลด์สตริงมีการกระทำเหมือนฟิลด์การค้นหา

PSA 3.0 ได้รับการปรับปรุงเพื่อใช้ประโยชน์จากความสัมพันธ์ใหม่ของเอนทิตีระหว่างเอนทิตีเอกสารการขาย และรายการเอกสารการขาย

เนื่องจากปัจจุบันฟิลด์การค้นหาสามารถใช้ระบุการอ้างอิงถึงเอนทิตี ฟิลด์ที่จัดเก็บค่าสตริงของ GUID ของเอนทิตีที่เกี่ยวข้องในรุ่นก่อนหน้าจึงไม่จำเป็นต้องใช้อีกต่อไป และดังนั้นจึงถูกตัดออก ไคลเอ็นต์แบบกำหนดเองและรหัสฝั่งเซิร์ฟเวอร์ที่จัดการความสัมพันธ์ ถูกกำหนดโดยสตริงฟิลด์แบบดั้งเดิมได้ถูกสนับสนุนเช่นกัน

### <a name="entity-schema-changes"></a>การเปลี่ยนแปลง Schema ของเอนทิตี
ตารางต่อไปนี้แสดงรายการแบบหนึ่งต่อหนึ่งของฟิลด์สตริงที่ไม่ได้รับการสนับสนุน และฟิลด์การค้นหาใหม่สำหรับเอนทิตี 

 เอนทิตี |   ฟิลด์ที่ไม่ได้รับการสนับสนุน (สตริง) | ฟิลด์ใหม่ (การค้นหา)
--- | --- | ---
รายละเอียดใบแจ้งหนี้ (รายการใบแจ้งหนี้) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (จริง) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (กำหนดการใบแจ้งหนี้สำหรับรายละเอียดการให้บริการตามสัญญาของโครงการ) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (เหตุการณ์สำคัญในรายละเอียดการให้บริการตามสัญญาของโครงการ) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (ข้อเท็จจริง) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (รายละเอียดบรรทัดใบแจ้งหนี้) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (บรรทัดสมุดรายวัน) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (ประเภททรัพยากรในรายละเอียดการให้บริการตามสัญญาโครงการ) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (บรรทัดรายละเอียดการให้บริการตามสัญญาโครงการ) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (ประเภทธุรกรรมในรายละเอียดการให้บริการตามสัญญาโครงการ) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (การจัดประเภทธุรกรรมในรายละเอียดการให้บริการตามสัญญาโครงการ) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (กำหนดการใบแจ้งหนี้สำหรับบรรทัดใบเสนอราคา) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (ประเภททรัพยากรของบรรทัดใบเสนอราคา) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (เหตุการณ์สำคัญของบรรทัดใบเสนอราคา) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (รายละเอียดบรรทัดใบเสนอราคา) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (ประเภทธุรกรรมของบรรทัดใบเสนอราคา) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (ประเภทธุรกรรมของบรรทัดใบเสนอราคา) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (บรรทัดใบสั่ง) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>มุมมองและการควบคุมแบบกำหนดเองที่ไม่ได้รับการสนับสนุน
มุมมองและการควบคุมแบบกำหนดเองต่อไปนี้ และสิ่งประดิษฐ์ที่เกี่ยวข้องของพวกเขาได้ถูกเลิกใช้แล้ว

- มุมมองการคิดค่าธรรมเนียม
- กริดแบบกำหนดเองสำหรับแสดงรายละเอียดรายการใบเสนอราคาบนเพจ **ข้อมูลโครงการ** สำหรับรายการใบเสนอราคา
- กริดแบบกำหนดเองสำหรับแสดงรายละเอียดการให้บริการตามสัญญาโครงการบนเพจ **ข้อมูลโครงการ** สำหรับรายการในใบสั่งขาย

> [!NOTE]
> สำหรับรายการทรัพยากรที่ไม่ได้รับการสนับสนุนทั้งหมด ดู [ทรัพยากรบนเว็บที่ไม่สนับสนุนใน Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Unified Client Interface App Module
ด้วยการแนะนำ Unified Client Interface (UCI) App Modules ทำให้รายการแผนผังเว็บไซต์ PSA ถูกเอาออกจากระบบ  
ฟังก์ชันที่เกี่ยวข้องกับการสลับฟอร์มสำหรับโอกาสทางการขาย, ใบเสนอราคา, ใบสั่ง, ใบแจ้งหนี้ถูกเลิกใช้เนื่องจากไม่จำเป็นอีกต่อไป เพราะ UCI App Module มีฟอร์มรุ่น PSA เท่านั้น  

ทรัพยากรบนเว็บต่อไปนี้ได้ถูกเลิกใช้:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> สำหรับรายการทรัพยากรที่ไม่ได้รับการสนับสนุนทั้งหมด ดู [ทรัพยากรบนเว็บที่ไม่สนับสนุนใน Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]