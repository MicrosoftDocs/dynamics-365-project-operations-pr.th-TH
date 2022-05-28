---
title: ทำไมราคาที่กำหนดค่าเริ่มต้นเป็นศูนย์ในต้นทุนค่าใช้จ่ายจริง?
description: การแก้ปัญหาว่าทำไมราคากำหนดค่าเริ่มต้นเป็นศูนย์ในต้นทุนค่าใช้จ่ายจริง
author: rumant
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7de9f660bf38629bb2af4e0fb1ebf815f5e525e2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595613"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>ทำไมราคาที่กำหนดค่าเริ่มต้นเป็นศูนย์ในต้นทุนค่าใช้จ่ายจริง

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

คำถามที่ถามบ่อยนี้ใช้กับค่าใช้จ่ายที่เกิดขึ้นจริง ซึ่งคลาสธุรกรรมถูกกำหนดเป็นค่าใช้จ่าย และชนิดของธุรกรรมเป็นต้นทุน

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>การแก้ไขปัญหาอัตราต้นทุนในค่าใช้จ่ายต้นทุนจริง

ไปที่รายการค่าใช้จ่ายที่เกี่ยวข้อง และตรวจสอบให้แน่ใจว่า ไม่มียอดเงินในฟิลด์รายการค่าใช้จ่าย ถ้ารายการค่าใช้จ่ายเริ่มต้นไม่ได้มีการกรอกข้อมูลฟิลด์ยอดเงิน แล้วคุณจะแยกปัญหาออกต่างหาก
 
เมื่อต้องการแก้ไขปัญหานี้ สร้างใหม่รายการค่าใช้จ่ายที่มียอดเงินที่ถูกต้อง และอนุมัติ


[!INCLUDE[footer-include](../includes/footer-banner.md)]
