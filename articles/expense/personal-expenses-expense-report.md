---
title: ทำงานกับค่าใช้จ่ายส่วนบุคคลในรายงานค่าใช้จ่าย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการทำงานโดยมีค่าใช้จ่ายส่วนบุคคลที่เกิดขึ้นกับพนักงาน ขณะที่เดินทางเพื่อจุดประสงค์ทางธุรกิจ
author: suvaidya
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: d2d558ad4f1a35f83af93d37e377db66d7f70e4f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276261"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="0d1a2-103">ทำงานกับค่าใช้จ่ายส่วนบุคคลในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="0d1a2-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="0d1a2-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="0d1a2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0d1a2-105">ในระหว่างการเดินทางเพื่อธุรกิจ พนักงานอาจเรียกเก็บค่าใช้จ่ายส่วนบุคคลจากบัตรเครดิตของบริษัทของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="0d1a2-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="0d1a2-106">หากไม่ได้กำหนดกระบวนการสำหรับจัดการค่าใช้จ่ายส่วนบุคคล กระบวนการอนุมัติรายงานค่าใช้จ่ายอาจหยุดชะงัก เมื่อพนักงานส่งรายงานค่าใช้จ่ายแบบแยกรายการของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="0d1a2-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="0d1a2-107">มีวิธีสองวิธีที่คุณสามารถใช้เพื่อทำงานกับค่าใช้จ่ายส่วนบุคคลของพนักงาน:</span><span class="sxs-lookup"><span data-stu-id="0d1a2-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="0d1a2-108">**จ่ายโดยพนักงาน**: องค์กรของคุณไม่จ่ายค่าใช้จ่ายส่วนบุคคลที่ปรากฏในใบเรียกเก็บเงินสำหรับบัตรเครดิตขององค์กร</span><span class="sxs-lookup"><span data-stu-id="0d1a2-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="0d1a2-109">แต่พนักงานจะจ่ายให้กับผู้จำหน่ายบัตรเครดิตโดยตรงสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="0d1a2-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="0d1a2-110">**จ่ายโดยบริษัท**: องค์กรของคุณจ่ายค่าบัตรเครดิตของบริษัทเต็มจำนวน และจากนั้น จะหักเงินจากบัญชีของพนักงานเป็นค่าใช้จ่ายส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="0d1a2-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="0d1a2-111">คุณสามารถเลือกวิธีการที่องค์กรของคุณใช้ในหน้า **พารามิเตอร์การจัดการค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="0d1a2-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]