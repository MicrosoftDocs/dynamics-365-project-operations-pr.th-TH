---
title: ทำไมฉันจึงไม่สามารถลบเรกคอร์ดออกจากเอนทิตีจำนวนจริงได้
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับเหตุผลที่คุณไม่สามารถลบเรกคอร์ดออกจากเอนทิตีจำนวนจริงได้
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: e3122c5d9495b3ff9a683f477e719ce0c228a84d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286091"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="22d81-103">ทำไมฉันจึงไม่สามารถลบเรกคอร์ดออกจากเอนทิตีจำนวนจริงได้</span><span class="sxs-lookup"><span data-stu-id="22d81-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="22d81-104">Project Service Automation (PSA) ไม่อนุญาตให้คุณลบจำนวนจริงเนื่องจากเป็นแหล่งที่มาของความจริงสำหรับธุรกรรม ที่เกียวข้องทางการเงินกับระบบดาวน์สตรีม เช่น บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="22d81-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="22d81-105">ถ้าสามารถลบจำนวนจริงได้ ความสมบูรณ์ของรายงานธุรกรรมทางการเงินอาจถูกสงสัยได้</span><span class="sxs-lookup"><span data-stu-id="22d81-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="22d81-106">เพื่อสร้างหลักฐานในการตรวจสอบ ลูกค้าควรใช้สมุดรายวันสร้างธุรกรรมการชดเชย</span><span class="sxs-lookup"><span data-stu-id="22d81-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]