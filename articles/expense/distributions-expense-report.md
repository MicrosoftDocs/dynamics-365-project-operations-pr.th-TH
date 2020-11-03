---
title: การแจกจ่ายในรายงานค่าใช้จ่าย
description: เมื่อคุณป้อนค่าใช้จ่ายในรายงานค่าใช้จ่าย คุณสามารถกระจายให้กับหลายโครงการ นิติบุคคล หรือบัญชีในองค์กรของคุณ
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a1fa7383e7715fe57380de0a006ccc4e020bb5a5
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085813"
---
# <a name="distributions-on-an-expense-report"></a><span data-ttu-id="e7117-103">การแจกจ่ายในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="e7117-103">Distributions on an expense report</span></span>

<span data-ttu-id="e7117-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="e7117-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e7117-105">เมื่อคุณป้อนค่าใช้จ่ายในรายงานค่าใช้จ่าย คุณสามารถกระจายให้กับหลายโครงการ มิติทางการเงิน หรือบัญชีในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="e7117-105">When you enter expenses on an expense report, you can distribute them across multiple projects, financial dimensions, or accounts in your organization.</span></span>

<span data-ttu-id="e7117-106">ตัวอย่างเช่น Nancy ตัวแทนขายของ Fabrikam เดินทางจากโคเปนเฮเกนไปแฟรงก์เฟิร์ต</span><span class="sxs-lookup"><span data-stu-id="e7117-106">For example, Nancy, a Fabrikam sales representative, traveled from Copenhagen to Frankfurt.</span></span> <span data-ttu-id="e7117-107">ในแฟรงก์เฟิร์ต Nancy ได้พบกับสององค์กรเพื่อหารือเกี่ยวกับโครงการที่แยกกันสำหรับแต่ละองค์กร</span><span class="sxs-lookup"><span data-stu-id="e7117-107">In Frankfurt, Nancy met with two organizations to discuss separate projects for each organization.</span></span> <span data-ttu-id="e7117-108">Nancy ใช้เวลาเจ็ดวันทำการในการทำงานกับองค์กร A ในโครงการ A และสามวันทำการในการทำงานกับองค์กร B ในโครงการ B</span><span class="sxs-lookup"><span data-stu-id="e7117-108">Nancy spent seven business days working with organization A on project A, and three business days working with organization B on project B.</span></span>

<span data-ttu-id="e7117-109">เนื่องจาก Nancy ทำงานในสองโครงการแยกกันขณะที่อยู่ในแฟรงก์เฟิร์ต เมื่อเธอป้อนข้อมูลรายงานค่าใช้จ่าย Nancy จึงกระจายค่าใช้จ่ายตามความเหมาะสมสำหรับแต่ละโครงการ</span><span class="sxs-lookup"><span data-stu-id="e7117-109">Because Nancy worked on two separate projects while was in Frankfurt, when she enters the expense report, Nancy distributes the expenses as appropriate for each project.</span></span> <span data-ttu-id="e7117-110">ตารางต่อไปนี้แสดงให้เห็นว่า Nancy กระจายค่าใช้จ่ายอย่างไร</span><span class="sxs-lookup"><span data-stu-id="e7117-110">The following table shows how Nancy distributed the expenses.</span></span>

| <span data-ttu-id="e7117-111">ชนิดค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="e7117-111">Expense type</span></span> | <span data-ttu-id="e7117-112">จำนวนเงินค่าใช้จ่ายรวม</span><span class="sxs-lookup"><span data-stu-id="e7117-112">Total expense amount</span></span> | <span data-ttu-id="e7117-113">จำนวนเงินที่กระจายสำหรับโครงการ A</span><span class="sxs-lookup"><span data-stu-id="e7117-113">Amount distributed to project A</span></span> | <span data-ttu-id="e7117-114">จำนวนเงินที่กระจายสำหรับโครงการ B</span><span class="sxs-lookup"><span data-stu-id="e7117-114">Amount distributed to project B</span></span> |
|--------------|----------------------|---------------------------------|---------------------------------|
| <span data-ttu-id="e7117-115">ค่าโดยสารรถไฟ</span><span class="sxs-lookup"><span data-stu-id="e7117-115">Train fare</span></span>   | <span data-ttu-id="e7117-116">DKK 578</span><span class="sxs-lookup"><span data-stu-id="e7117-116">DKK 578</span></span>              | <span data-ttu-id="e7117-117">DKK 405</span><span class="sxs-lookup"><span data-stu-id="e7117-117">DKK 405</span></span>                         | <span data-ttu-id="e7117-118">DKK 173</span><span class="sxs-lookup"><span data-stu-id="e7117-118">DKK 173</span></span>                         |
| <span data-ttu-id="e7117-119">โรงแรม</span><span class="sxs-lookup"><span data-stu-id="e7117-119">Hotel</span></span>        | <span data-ttu-id="e7117-120">EUR 725</span><span class="sxs-lookup"><span data-stu-id="e7117-120">EUR 725</span></span>              | <span data-ttu-id="e7117-121">EUR 557</span><span class="sxs-lookup"><span data-stu-id="e7117-121">EUR 557</span></span>                         | <span data-ttu-id="e7117-122">EUR 168</span><span class="sxs-lookup"><span data-stu-id="e7117-122">EUR 168</span></span>                         |
| <span data-ttu-id="e7117-123">ค่าอาหาร</span><span class="sxs-lookup"><span data-stu-id="e7117-123">Meals</span></span>        | <span data-ttu-id="e7117-124">EUR 346</span><span class="sxs-lookup"><span data-stu-id="e7117-124">EUR 346</span></span>              | <span data-ttu-id="e7117-125">EUR 284</span><span class="sxs-lookup"><span data-stu-id="e7117-125">EUR 284</span></span>                         | <span data-ttu-id="e7117-126">EUR 62</span><span class="sxs-lookup"><span data-stu-id="e7117-126">EUR 62</span></span>                          |
