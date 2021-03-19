---
title: ทำไมราคาที่กำหนดค่าเริ่มต้นเป็นศูนย์ในต้นทุนค่าใช้จ่ายจริง?
description: การแก้ปัญหาว่าทำไมราคากำหนดค่าเริ่มต้นเป็นศูนย์ในต้นทุนค่าใช้จ่ายจริง
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: 742b0b9c495b4b3ecb4705be3ece5656f0322ca9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285882"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="d6342-103">ทำไมราคาที่กำหนดค่าเริ่มต้นเป็นศูนย์ในต้นทุนค่าใช้จ่ายจริง</span><span class="sxs-lookup"><span data-stu-id="d6342-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d6342-104">คำถามที่ถามบ่อยนี้ใช้กับค่าใช้จ่ายที่เกิดขึ้นจริง ซึ่งคลาสธุรกรรมถูกกำหนดเป็นค่าใช้จ่าย และชนิดของธุรกรรมเป็นต้นทุน</span><span class="sxs-lookup"><span data-stu-id="d6342-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="d6342-105">การแก้ไขปัญหาอัตราต้นทุนในค่าใช้จ่ายต้นทุนจริง</span><span class="sxs-lookup"><span data-stu-id="d6342-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="d6342-106">ไปที่รายการค่าใช้จ่ายที่เกี่ยวข้อง และตรวจสอบให้แน่ใจว่า ไม่มียอดเงินในฟิลด์รายการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d6342-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="d6342-107">ถ้ารายการค่าใช้จ่ายเริ่มต้นไม่ได้มีการกรอกข้อมูลฟิลด์ยอดเงิน แล้วคุณจะแยกปัญหาออกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="d6342-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="d6342-108">เมื่อต้องการแก้ไขปัญหานี้ สร้างใหม่รายการค่าใช้จ่ายที่มียอดเงินที่ถูกต้อง และอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="d6342-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]