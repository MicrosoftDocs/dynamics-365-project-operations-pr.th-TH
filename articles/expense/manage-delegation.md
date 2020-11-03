---
title: จัดการการมอบสิทธิ์
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีที่ผู้รับมอบสิทธิ์ค่าใช้จ่ายสามารถสร้างและจัดการรายงานค่าใช้จ่ายสำหรับพนักงานคนอื่นได้
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: bfc141c6f1072314bdfaef835d730c6ca82bae1a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085933"
---
# <a name="manage-delegation"></a><span data-ttu-id="a9435-103">จัดการการมอบสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="a9435-103">Manage delegation</span></span>
<span data-ttu-id="a9435-104">ผู้รับมอบสิทธิ์ค่าใช้จ่ายสามารถสร้างและจัดการรายงานค่าใช้จ่ายสำหรับพนักงานคนอื่นได้</span><span class="sxs-lookup"><span data-stu-id="a9435-104">An expense delegate can create and manage expense reports for another employee.</span></span>

## <a name="configuring-expense-delegation"></a><span data-ttu-id="a9435-105">การกำหนดค่าการมอบสิทธิ์ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a9435-105">Configuring expense delegation</span></span>

<span data-ttu-id="a9435-106">หากต้องการตั้งค่าผู้รับมอบสิทธิ์ค่าใช้จ่าย ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a9435-106">To set up a user as an expense delegate, complete the following steps.</span></span> 
1. <span data-ttu-id="a9435-107">ไปที่ **การจัดการค่าใช้จ่าย** > **ตั้งค่า** > **ทั่วไป** > **ผู้รับมอบสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="a9435-107">Go to **Expense management** > **Setup** > **General** > **Delegates**.</span></span> 
2. <span data-ttu-id="a9435-108">บนเพจ **ผู้รับมอบสิทธิ์** ให้เลือก **ใหม่** จากนั้นเลือกพนักงานที่จะมีการกำหนดเป็นผู้รับมอบสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="a9435-108">On the **Delegates** page, select **New** and then select the employee that will have a delegate defined.</span></span> 
3. <span data-ttu-id="a9435-109">ป้อนนามแฝงของผู้ใช้ที่เป็นผู้รับมอบสิทธิ์และวันที่เริ่มต้นและวันที่สิ้นสุดสำหรับช่วงเวลาการมอบสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="a9435-109">Enter the alias of the delegate user, and the start and end date for the delegation period.</span></span>

## <a name="manage-expenses-on-behalf-of-another-employee"></a><span data-ttu-id="a9435-110">จัดการค่าใช้จ่ายในนามของพนักงานคนอื่น</span><span class="sxs-lookup"><span data-stu-id="a9435-110">Manage expenses on behalf of another employee</span></span>

<span data-ttu-id="a9435-111">หากคีย์การจัดการคุณลักษณะ **เพจรายการเปิดใช้งานผู้รับมอบสิทธิ์ค่าใช้จ่าย** เปิดใช้งานอยู่ เพจรายการ **ค่าใช้จ่ายที่มอบสิทธิ์ให้ฉัน** จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a9435-111">If the feature management key **Enable expense delegates list page** is enabled, the **Expenses delegated to me** list page will be available.</span></span> <span data-ttu-id="a9435-112">ไปที่ **การจัดการค่าใช้จ่าย** > **ค่าใช้จ่ายของฉัน** > **ค่าใช้จ่ายที่มอบสิทธิ์ให้ฉัน**</span><span class="sxs-lookup"><span data-stu-id="a9435-112">Go to **Expense management** > **My expenses** > **Expenses delegated to me**.</span></span>

<span data-ttu-id="a9435-113">ผู้รับมอบสิทธิ์สามารถกรองและค้นหารายงานค่าใช้จ่ายที่มีอยู่ซึ่งมีการมอบหมายให้พวกเขาไปแล้วได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="a9435-113">A delegate can quickly filter and search on existing expense reports that have been delegated to them.</span></span> <span data-ttu-id="a9435-114">ผู้รับมอบสิทธิ์ยังสามารถสร้างรายงานค่าใช้จ่ายใหม่สำหรับผู้ใช้รายอื่นได้อย่างรวดเร็วโดยการเลือก **รายงานค่าใช้จ่ายใหม่**</span><span class="sxs-lookup"><span data-stu-id="a9435-114">The delegate can also quickly create a new expense report for other users by selecting **New expense report**.</span></span>

<span data-ttu-id="a9435-115">ผู้รับมอบสิทธิ์สามารถสร้างและจัดการรายงานค่าใช้จ่ายสำหรับพนักงานคนอื่นๆ ได้โดยไปที่ **การจัดการค่าใช้จ่าย** > **ค่าใช้จ่ายของฉัน** > **รายงานค่าใช้จ่าย** และเลือก **เปิดค่าใช้จ่ายของผู้ใช้รายอื่น**</span><span class="sxs-lookup"><span data-stu-id="a9435-115">Delegates can create and manage expense reports for other employees by going to **Expense management** > **My expenses** > **Expense reports** and selecting **Open other user's expenses**.</span></span>
