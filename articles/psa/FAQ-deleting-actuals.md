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
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="2880e-103">ทำไมฉันจึงไม่สามารถลบเรกคอร์ดออกจากเอนทิตีจำนวนจริงได้</span><span class="sxs-lookup"><span data-stu-id="2880e-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2880e-104">Project Service Automation (PSA) ไม่อนุญาตให้คุณลบจำนวนจริงเนื่องจากเป็นแหล่งที่มาของความจริงสำหรับธุรกรรม ที่เกียวข้องทางการเงินกับระบบดาวน์สตรีม เช่น บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="2880e-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="2880e-105">ถ้าสามารถลบจำนวนจริงได้ ความสมบูรณ์ของรายงานธุรกรรมทางการเงินอาจถูกสงสัยได้</span><span class="sxs-lookup"><span data-stu-id="2880e-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="2880e-106">เพื่อสร้างหลักฐานในการตรวจสอบ ลูกค้าควรใช้สมุดรายวันสร้างธุรกรรมการชดเชย</span><span class="sxs-lookup"><span data-stu-id="2880e-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

