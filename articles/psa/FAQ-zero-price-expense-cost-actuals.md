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
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122141"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="a2a54-103">ทำไมราคาที่กำหนดค่าเริ่มต้นเป็นศูนย์ในต้นทุนค่าใช้จ่ายจริง?</span><span class="sxs-lookup"><span data-stu-id="a2a54-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a2a54-104">คำถามที่ถามบ่อยนี้ใช้กับค่าใช้จ่ายที่เกิดขึ้นจริง ซึ่งคลาสธุรกรรมถูกกำหนดเป็นค่าใช้จ่าย และชนิดของธุรกรรมเป็นต้นทุน</span><span class="sxs-lookup"><span data-stu-id="a2a54-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="a2a54-105">การแก้ไขปัญหาอัตราต้นทุนในค่าใช้จ่ายต้นทุนจริง</span><span class="sxs-lookup"><span data-stu-id="a2a54-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="a2a54-106">ไปที่รายการค่าใช้จ่ายที่เกี่ยวข้อง และตรวจสอบให้แน่ใจว่า ไม่มียอดเงินในฟิลด์รายการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a2a54-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="a2a54-107">ถ้ารายการค่าใช้จ่ายเริ่มต้นไม่ได้มีการกรอกข้อมูลฟิลด์ยอดเงิน แล้วคุณจะแยกปัญหาออกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="a2a54-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="a2a54-108">เมื่อต้องการแก้ไขปัญหานี้ สร้างใหม่รายการค่าใช้จ่ายที่มียอดเงินที่ถูกต้อง และอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="a2a54-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
