---
title: ค่าใช้จ่ายส่วนตัวในรายงานค่าใช้จ่าย
description: หัวข้อนี้อธิบายถึงสองวิธีในการจัดการค่าใช้จ่ายส่วนตัวของพนักงานใน Microsoft Dynamics 365 Finance
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6b9d4fa0f69b4b0fe4bd1786958d22e5580a321
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960900"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="c4d13-103">ค่าใช้จ่ายส่วนตัวในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="c4d13-103">Personal expenses on an expense report</span></span>

<span data-ttu-id="c4d13-104">ในระหว่างการเดินทางเพื่อธุรกิจ บางครั้งพนักงานอาจเรียกเก็บค่าใช้จ่ายส่วนตัวจากบัตรเครดิตขององค์กร</span><span class="sxs-lookup"><span data-stu-id="c4d13-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="c4d13-105">หากคุณไม่กำหนดกระบวนการจัดการค่าใช้จ่ายส่วนตัว กระบวนการอนุมัติรายงานค่าใช้จ่ายอาจหยุดชะงัก เมื่อพนักงานส่งรายงานค่าใช้จ่ายแบบแยกรายการ</span><span class="sxs-lookup"><span data-stu-id="c4d13-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="c4d13-106">มีสองวิธีในการจัดการค่าใช้จ่ายส่วนตัวของพนักงาน:</span><span class="sxs-lookup"><span data-stu-id="c4d13-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="c4d13-107">**จ่ายโดยพนักงาน** - องค์กรของคุณไม่จ่ายค่าใช้จ่ายส่วนตัวที่ปรากฏในใบเรียกเก็บเงินสำหรับบัตรเครดิตขององค์กร</span><span class="sxs-lookup"><span data-stu-id="c4d13-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="c4d13-108">แต่จะสร้างรายงานที่แสดงค่าใช้จ่ายส่วนตัวพร้อมกับค่าใช้จ่ายขององค์กรที่เรียกเก็บจากบัตรเครดิตขององค์กรแทน</span><span class="sxs-lookup"><span data-stu-id="c4d13-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="c4d13-109">**จ่ายโดยบริษัท** - องค์กรของคุณจ่ายค่าบัตรเครดิตของบริษัททั้งใบ จากนั้นจะหักเงินจากบัญชีของพนักงานสำหรับค่าใช้จ่ายส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="c4d13-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="c4d13-110">คุณสามารถเลือกวิธีการที่องค์กรของคุณใช้ในหน้า **พารามิเตอร์การจัดการค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="c4d13-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
