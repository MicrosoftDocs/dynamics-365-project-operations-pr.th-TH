---
title: การวิเคราะห์ใบเสนอราคาโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการวิเคราะห์ใบเสนอราคาโครงการ
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: acb3f1a2020cfd59f60f828e9092bd7ccde00077
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012474"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="a6074-103">การวิเคราะห์ใบเสนอราคาโครงการ</span><span class="sxs-lookup"><span data-stu-id="a6074-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a6074-104">Dynamics 365 Project Service Automation วิเคราะห์ใบเสนอราคาโครงการเพื่อประเมินผลกำไร</span><span class="sxs-lookup"><span data-stu-id="a6074-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="a6074-105">นอกจากนี้ยังวิเคราะห์ว่าใบเสนอราคาสอดคล้องกับความคาดหวังของลูกค้ามากน้อยแค่ไหน เกี่ยวกับวันที่จัดส่งหรือวันที่เสร็จสมบูรณ์ และเกี่ยวกับงบประมาณ.</span><span class="sxs-lookup"><span data-stu-id="a6074-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="a6074-106">การวิเคราะห์ความสามารถในการทำกำไร</span><span class="sxs-lookup"><span data-stu-id="a6074-106">Profitability analysis</span></span>

<span data-ttu-id="a6074-107">Project Service Automation วิเคราะห์การทำกำไรโดยใช้กำไรขั้นต้นและกำไรขั้นต้นที่ปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="a6074-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="a6074-108">กำไรขั้นต้นจะถูกคำนวณโดยใช้สูตรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a6074-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="a6074-109">กำไรขั้นต้นที่ปรับปรุงจะถูกคำนวณโดยใช้สูตรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a6074-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="a6074-110">ถ้าค่าสำหรับกำไรขั้นต้นและกำไรขั้นต้นที่ปรับปรุงแตกต่างกันไปตามระยะขอบกว้าง การทำงานจำนวนมากในใบเสนอราคาจะถูกจัดประเภทเป็นไม่คิดค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="a6074-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="a6074-111">การวิเคราะห์ความคาดหมายของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="a6074-111">Analysis of customer expectations</span></span>

<span data-ttu-id="a6074-112">คุณสามารถวิเคราะห์ใบเสนอราคาและสร้างแผนภูมิสำหรับความคาดหมายของลูกค้าเกี่ยวกับกำหนดการและงบประมาณ ถ้าคุณป้อนค่าสำหรับฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a6074-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="a6074-113">ฟิลด์ **วันที่จัดส่งที่ร้องขอ** บนส่วนหัวของใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="a6074-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="a6074-114">ฟิลด์ **งบประมาณลูกค้า** สำหรับแต่ละบรรทัดใบเสนอราคา (สำหรับบรรทัดตามโครงการและบรรทัดตามผลิตภัณฑ์)</span><span class="sxs-lookup"><span data-stu-id="a6074-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="a6074-115">การวิเคราะห์ความคาดหมายของลูกค้าเกี่ยวกับกำหนดการจะทำโดยการเปรียบเทียบวันที่สิ้นสุดของรายละเอียดบรรทัดใบเสนอราคากับวันที่จัดส่งที่ร้องขอในบรรทัดใบเสนอราคาทั้งหมดในใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="a6074-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="a6074-116">การวิเคราะห์ความคาดหมายของลูกค้าเกี่ยวกับงบประมาณจะทำโดยการเปรียบเทียบผลรวมของงบประมาณลูกค้ากับยอดเงินที่เสนอในบรรทัดใบเสนอราคาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a6074-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]