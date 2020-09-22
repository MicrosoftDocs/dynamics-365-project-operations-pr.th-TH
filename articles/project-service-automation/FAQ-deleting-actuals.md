---
title: ทำไมฉันจึงไม่สามารถลบเรกคอร์ดออกจากเอนทิตีจำนวนจริงได้
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับเหตุผลที่คุณไม่สามารถลบเรกคอร์ดออกจากเอนทิตีจำนวนจริงได้
author: JPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.prod: Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: ff504c34-7337-474f-89e8-d8afdd1e0a98
ms.author: Jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5817940933c161dccac0fe549fabacbe57e7077a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756379"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="76abd-103">ทำไมฉันจึงไม่สามารถลบเรกคอร์ดออกจากเอนทิตีจำนวนจริงได้</span><span class="sxs-lookup"><span data-stu-id="76abd-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="76abd-104">Project Service Automation (PSA) ไม่อนุญาตให้คุณลบจำนวนจริงเนื่องจากเป็นแหล่งที่มาของความจริงสำหรับธุรกรรม ที่เกียวข้องทางการเงินกับระบบดาวน์สตรีม เช่น บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="76abd-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="76abd-105">ถ้าสามารถลบจำนวนจริงได้ ความสมบูรณ์ของรายงานธุรกรรมทางการเงินอาจถูกสงสัยได้</span><span class="sxs-lookup"><span data-stu-id="76abd-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="76abd-106">เพื่อสร้างหลักฐานในการตรวจสอบ ลูกค้าควรใช้สมุดรายวันสร้างธุรกรรมการชดเชย</span><span class="sxs-lookup"><span data-stu-id="76abd-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

