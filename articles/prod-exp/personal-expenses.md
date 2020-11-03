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
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086081"
---
# <a name="personal-expenses-on-an-expense-report"></a>ค่าใช้จ่ายส่วนตัวในรายงานค่าใช้จ่าย

[!include [banner](../includes/banner.md)]

ในระหว่างการเดินทางเพื่อธุรกิจ บางครั้งพนักงานอาจเรียกเก็บค่าใช้จ่ายส่วนตัวจากบัตรเครดิตขององค์กร หากคุณไม่กำหนดกระบวนการจัดการค่าใช้จ่ายส่วนตัว กระบวนการอนุมัติรายงานค่าใช้จ่ายอาจหยุดชะงัก เมื่อพนักงานส่งรายงานค่าใช้จ่ายแบบแยกรายการ 

มีสองวิธีในการจัดการค่าใช้จ่ายส่วนตัวของพนักงาน:

- **จ่ายโดยพนักงาน** - องค์กรของคุณไม่จ่ายค่าใช้จ่ายส่วนตัวที่ปรากฏในใบเรียกเก็บเงินสำหรับบัตรเครดิตขององค์กร แต่จะสร้างรายงานที่แสดงค่าใช้จ่ายส่วนตัวพร้อมกับค่าใช้จ่ายขององค์กรที่เรียกเก็บจากบัตรเครดิตขององค์กรแทน
- **จ่ายโดยบริษัท** - องค์กรของคุณจ่ายค่าบัตรเครดิตของบริษัททั้งใบ จากนั้นจะหักเงินจากบัญชีของพนักงานสำหรับค่าใช้จ่ายส่วนตัว

คุณสามารถเลือกวิธีการที่องค์กรของคุณใช้ในหน้า **พารามิเตอร์การจัดการค่าใช้จ่าย**