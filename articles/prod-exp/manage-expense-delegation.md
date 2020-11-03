---
title: จัดการการมอบสิทธิ์ค่าใช้จ่าย
description: ผู้ใช้ผู้รับมอบสิทธิ์ค่าใช้จ่ายสามารถสร้างและจัดการรายงานค่าใช้จ่ายในนามของพนักงานคนอื่นในองค์กรได้
author: KimANelson
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2020-01-10
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 2ce1d1cf35745ef4372258e07fd4d2b108ed4827
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086084"
---
# <a name="manage-expense-delegation"></a><span data-ttu-id="fe778-103">จัดการการมอบสิทธิ์ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="fe778-103">Manage expense delegation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe778-104">ผู้ใช้ผู้รับมอบสิทธิ์ค่าใช้จ่ายสามารถสร้างและจัดการรายงานค่าใช้จ่ายในนามของพนักงานคนอื่นในองค์กรได้</span><span class="sxs-lookup"><span data-stu-id="fe778-104">An expense delegate user can create and manage expense reports on behalf of another employee in the organization.</span></span>

## <a name="configuring-expense-delegation"></a><span data-ttu-id="fe778-105">การกำหนดค่าการมอบสิทธิ์ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="fe778-105">Configuring expense delegation</span></span>

<span data-ttu-id="fe778-106">ในการตั้งค่าผู้ใช้เป็นผู้รับมอบสิทธิ์ค่าใช้จ่าย ให้ไปที่ **การจัดการค่าใช้จ่าย > การตั้งค่า > ทั่วไป> ผู้รับมอบสิทธิ์** เพื่อเปิดหน้า **ผู้รับมอบสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="fe778-106">To set up a user as an expense delegate, go to **Expense management > Setup > General > Delegates** to open the **Delegates** page.</span></span> <span data-ttu-id="fe778-107">ให้เลือก **สร้าง** จากนั้นเลือกพนักงานที่จะมีการกำหนดเป็นผู้รับมอบสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="fe778-107">Select **New** and then select the employee that will have a delegate defined.</span></span> <span data-ttu-id="fe778-108">ป้อนนามแฝงของผู้ใช้ที่เป็นผู้รับมอบสิทธิ์และวันที่เริ่มต้นและวันที่สิ้นสุดสำหรับช่วงเวลาการมอบสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="fe778-108">Enter the alias of the delegate user and the start and end date for the delegation period.</span></span>

## <a name="managing-expense-delegation-on-behalf-of-another-employee"></a><span data-ttu-id="fe778-109">จัดการการมอบสิทธิ์ค่าใช้จ่ายในนามของพนักงานคนอื่น</span><span class="sxs-lookup"><span data-stu-id="fe778-109">Managing expense delegation on behalf of another employee</span></span>

<span data-ttu-id="fe778-110">หากคีย์การจัดการคุณลักษณะ **เปิดใช้งานหน้ารายการผู้แทนค่าใช้จ่าย** เปิดใช้งาน หน้ารายการ **ค่าใช้จ่ายที่มอบให้ฉัน** จะพร้อมใช้งานโดยไปที่ **การจัดการค่าใช้จ่าย > ค่าใช้จ่ายของฉัน > ค่าใช้จ่ายที่มอบให้ฉัน**</span><span class="sxs-lookup"><span data-stu-id="fe778-110">If the feature management key **Enable expense delegates list page** is enabled, the **Expenses delegated to me** list page will be available by navigating to **Expense management > My expenses > Expenses delegated to me**.</span></span>

<span data-ttu-id="fe778-111">ผู้ใช้ที่เป็นผู้รับมอบสิทธิ์สามารถกรองและค้นหารายงานค่าใช้จ่ายที่มีอยู่ซึ่งมีการมอบหมายให้ผู้ใช้ไปแล้วได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="fe778-111">A delegate user can quickly filter and search on existing expense reports that hae been delegated to the user.</span></span> <span data-ttu-id="fe778-112">ผู้ใช้ยังสามารถสร้างรายงานค่าใช้จ่ายใหม่ในนามของผู้ใช้รายอื่นได้อย่างรวดเร็วโดยการคลิก **รายงานค่าใช้จ่ายใหม่**</span><span class="sxs-lookup"><span data-stu-id="fe778-112">The user can also quickly create a new expense report on behalf of other users by clicking **New expense report**.</span></span>

<span data-ttu-id="fe778-113">ผู้ใช้ที่เป็นผู้รับมอบสิทธิ์ยังสามารถสร้างและจัดการรายงานค่าใช้จ่ายในนามของพนักงานคนอื่นๆ ได้โดยการนำทางไปที่ **การจัดการค่าใช้จ่าย > ค่าใช้จ่ายของฉัน > รายงานค่าใช้จ่าย** และคลิกปุ่ม **เปิดค่าใช้จ่ายของผู้ใช้รายอื่น**</span><span class="sxs-lookup"><span data-stu-id="fe778-113">Delegate users can also create and manage expense reports on behalf of other employees by navigating to **Expense management > My expenses > Expense reports** and clicking the **Open other user's expenses** button.</span></span>
