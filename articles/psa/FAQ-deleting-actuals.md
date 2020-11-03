---
title: ทำไมฉันจึงไม่สามารถลบเรกคอร์ดออกจากเอนทิตีจำนวนจริงได้
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับเหตุผลที่คุณไม่สามารถลบเรกคอร์ดออกจากเอนทิตีจำนวนจริงได้
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086058"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>ทำไมฉันจึงไม่สามารถลบเรกคอร์ดออกจากเอนทิตีจำนวนจริงได้

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) ไม่อนุญาตให้คุณลบจำนวนจริงเนื่องจากเป็นแหล่งที่มาของความจริงสำหรับธุรกรรม ที่เกียวข้องทางการเงินกับระบบดาวน์สตรีม เช่น บัญชีแยกประเภททั่วไป ถ้าสามารถลบจำนวนจริงได้ ความสมบูรณ์ของรายงานธุรกรรมทางการเงินอาจถูกสงสัยได้ เพื่อสร้างหลักฐานในการตรวจสอบ ลูกค้าควรใช้สมุดรายวันสร้างธุรกรรมการชดเชย

