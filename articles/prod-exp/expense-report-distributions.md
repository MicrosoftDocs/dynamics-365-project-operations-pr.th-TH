---
title: การแจกจ่ายรายงานค่าใช้จ่าย
description: เมื่อคุณป้อนค่าใช้จ่ายในรายงานค่าใช้จ่าย คุณสามารถกระจายค่าใช้จ่ายให้กับหลายโครงการ นิติบุคคล หรือบัญชีในองค์กรของคุณ
author: ShylaThompson
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8850a8d3f2efc699bc95d4cb4fc76428badb10f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086089"
---
# <a name="expense-report-distributions"></a><span data-ttu-id="910dd-103">การแจกจ่ายรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="910dd-103">Expense report distributions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="910dd-104">เมื่อคุณป้อนค่าใช้จ่ายในรายงานค่าใช้จ่าย คุณสามารถกระจายค่าใช้จ่ายให้กับหลายโครงการ มิติทางการเงิน หรือบัญชีในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="910dd-104">When you enter expenses on an expense report, you can distribute the expense across multiple projects, financial dimensions, or accounts in your organization.</span></span>

<span data-ttu-id="910dd-105">ตัวอย่างเช่น Nancy ตัวแทนขายของ Fabrikam เดินทางจากโคเปนเฮเกนไปแฟรงก์เฟิร์ต</span><span class="sxs-lookup"><span data-stu-id="910dd-105">For example, Nancy, a Fabrikam sales representative, traveled from Copenhagen to Frankfurt.</span></span> <span data-ttu-id="910dd-106">ในแฟรงก์เฟิร์ต เธอได้พบกับสององค์กรเพื่อหารือเกี่ยวกับโครงการที่แยกกันสำหรับแต่ละองค์กร</span><span class="sxs-lookup"><span data-stu-id="910dd-106">In Frankfurt, she met with two organizations to discuss separate projects for each organization.</span></span> <span data-ttu-id="910dd-107">Nancy ใช้เวลาเจ็ดวันทำการในการทำงานกับองค์กร A ในโครงการ A และสามวันทำการในการทำงานกับองค์กร B ในโครงการ B</span><span class="sxs-lookup"><span data-stu-id="910dd-107">Nancy spent seven business days working with organization A on project A, and three business days working with organization B on project B.</span></span>

<span data-ttu-id="910dd-108">เนื่องจาก Nancy ทำงานในสองโครงการแยกกันขณะที่อยู่ในแฟรงก์เฟิร์ต เมื่อเธอป้อนข้อมูลรายงานค่าใช้จ่าย เธอจึงกระจายค่าใช้จ่ายตามความเหมาะสมสำหรับแต่ละโครงการ</span><span class="sxs-lookup"><span data-stu-id="910dd-108">Because Nancy worked on two separate projects when she was in Frankfurt, when she enters her expense report, she distributes her expenses as appropriate for each project.</span></span> <span data-ttu-id="910dd-109">ตารางต่อไปนี้แสดงให้เห็นว่า Nancy กระจายค่าใช้จ่ายของเธออย่างไร</span><span class="sxs-lookup"><span data-stu-id="910dd-109">The following table shows how Nancy distributed her expenses.</span></span>


| <span data-ttu-id="910dd-110">ชนิดค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="910dd-110">Expense type</span></span> | <span data-ttu-id="910dd-111">จำนวนเงินค่าใช้จ่ายรวม</span><span class="sxs-lookup"><span data-stu-id="910dd-111">Total expense amount</span></span>|<span data-ttu-id="910dd-112">จำนวนเงินที่กระจายสำหรับโครงการ A</span><span class="sxs-lookup"><span data-stu-id="910dd-112">Amount distributed to project A</span></span>| <span data-ttu-id="910dd-113">จำนวนเงินที่กระจายสำหรับโครงการ B</span><span class="sxs-lookup"><span data-stu-id="910dd-113">Amount distributed to project B</span></span> |
|--------------|---------------------|-------------------------------|---------------------------------|
|<span data-ttu-id="910dd-114">ค่าโดยสารรถไฟ</span><span class="sxs-lookup"><span data-stu-id="910dd-114">Train fare</span></span>   |<span data-ttu-id="910dd-115">DKK 578</span><span class="sxs-lookup"><span data-stu-id="910dd-115">DKK 578</span></span>              |<span data-ttu-id="910dd-116">DKK 405</span><span class="sxs-lookup"><span data-stu-id="910dd-116">DKK 405</span></span>                        |<span data-ttu-id="910dd-117">DKK 173</span><span class="sxs-lookup"><span data-stu-id="910dd-117">DKK 173</span></span>                          |
|<span data-ttu-id="910dd-118">โรงแรม</span><span class="sxs-lookup"><span data-stu-id="910dd-118">Hotel</span></span>         |<span data-ttu-id="910dd-119">EUR 725</span><span class="sxs-lookup"><span data-stu-id="910dd-119">EUR 725</span></span>              |<span data-ttu-id="910dd-120">EUR 557</span><span class="sxs-lookup"><span data-stu-id="910dd-120">EUR 557</span></span>                        |<span data-ttu-id="910dd-121">EUR 168</span><span class="sxs-lookup"><span data-stu-id="910dd-121">EUR 168</span></span>                          |
|<span data-ttu-id="910dd-122">ค่าอาหาร</span><span class="sxs-lookup"><span data-stu-id="910dd-122">Meals</span></span>         |<span data-ttu-id="910dd-123">EUR 346</span><span class="sxs-lookup"><span data-stu-id="910dd-123">EUR 346</span></span>              |<span data-ttu-id="910dd-124">EUR 284</span><span class="sxs-lookup"><span data-stu-id="910dd-124">EUR 284</span></span>                        |<span data-ttu-id="910dd-125">EUR 62</span><span class="sxs-lookup"><span data-stu-id="910dd-125">EUR 62</span></span>                           |

