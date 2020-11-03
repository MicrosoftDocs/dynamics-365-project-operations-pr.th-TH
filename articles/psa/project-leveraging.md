---
title: การประมาณการณ์ยอดขายและโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับข้อดีของการวางแผนและการประมาณการณ์ในกระบวนการขาย
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: eafe60362003198a223026526f56261de414bb4a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085950"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="cc646-103">การประมาณการณ์ยอดขายและโครงการ</span><span class="sxs-lookup"><span data-stu-id="cc646-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cc646-104">ในระหว่างกระบวนการขาย คุณสามารถทำการประมาณการณ์ยอดขายได้โดยเชื่อมต่อโครงการเข้ากับใบแจ้งราคา</span><span class="sxs-lookup"><span data-stu-id="cc646-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="cc646-105">โดยวิธีการนี้ การระบุยอดประมาณการณ์สามารถเกิดขึ้นได้ระหว่างกระบวนการขายซึ่งเป็นข้อดีของการวางแผนงานและการประเมินความสามารถ</span><span class="sxs-lookup"><span data-stu-id="cc646-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="cc646-106">หากยอดขายเกิดขึ้นจริง แผนงานที่ใข้ในการประมาณการณ์ยอดขายจะถูกนำมาใช้เป็นเกณฑ์ในการกำหนดแผนงานของโครงการ</span><span class="sxs-lookup"><span data-stu-id="cc646-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="cc646-107">การเชื่อมโยงโครงการกับใบแจ้งราคา</span><span class="sxs-lookup"><span data-stu-id="cc646-107">Linking a project to a quote line</span></span>

<span data-ttu-id="cc646-108">เมื่อคุณสร้างโครงการจากใบแจ้งราคา คุณสามารถสร้างโครงการใหม่หรือเชื่อมโยงกับโครงการที่มีอยู่เดิมบนหน้า **Quote Line**</span><span class="sxs-lookup"><span data-stu-id="cc646-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![รายการที่เสนอราคา (แบบฟอร์ม)](media/project-8.png)
 
<span data-ttu-id="cc646-110">เมื่อคุณสร้างโครงการใหม่รายละเอียดรายการที่เสนอราคา คุณจะสามารถใช้งานเท็มเพลตของโครงการได้</span><span class="sxs-lookup"><span data-stu-id="cc646-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="cc646-111">เท็มเพลตของโครงการเป็นแบบจำลองของโครงการที่นำเสนอแผนการมาตรฐานของโครงการและการประมาณการทางการเงินที่เป็นรูปแบบขององค์กร</span><span class="sxs-lookup"><span data-stu-id="cc646-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="cc646-112">เท็มเพลตดังกล่าวยังสามารถแสดงสำเนาของแผนการโครงการและประมาณการจากโครงการที่ผ่านมาได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="cc646-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![รายละเอียดบรรทัดใบเสนอราคา](media/project-9.png)
  
<span data-ttu-id="cc646-114">เมื่อมีการสร้างโครงการจากใบแจ้งราคาแล้ว โครงการจะเชื่อมโยงข้อมูลกับรายการที่แจ้งราคาโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="cc646-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="cc646-115">ส่วนประกอบของการประมาณโครงการ</span><span class="sxs-lookup"><span data-stu-id="cc646-115">Components of estimates in a project</span></span>

<span data-ttu-id="cc646-116">ตารางงานจะทำให้คุณสามารถแบ่งงานออกเป็นขั้นๆ โดยยังคงไว้ซึ่งลำดับของงานที่ต้องทำ ระบุทรัพยากรที่ต้องใช้เพื่อให้งานบรรลุผล และประมาณการเวลาที่ต้องใช้ในแต่ละงานด้วย</span><span class="sxs-lookup"><span data-stu-id="cc646-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="cc646-117">คุณสามารถกำหนดเวลางานและประมาณการแผนงานได้โดยใช้ฟิลด์บนแท็บ **Schedule** ของหน้า **Project**</span><span class="sxs-lookup"><span data-stu-id="cc646-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="cc646-118">เนื่องจากรายการราคามีความเกี่ยวข้องกับโครงการ การประมาณการทางการเงินจะถูกคำนวณโดยการใช้ราคาต้นทุนและราคาขายที่ระบุในรายการราคา</span><span class="sxs-lookup"><span data-stu-id="cc646-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="cc646-119">การนำเข้าค่าประมาณจากโครงการสู่ใบแจ้งราคา</span><span class="sxs-lookup"><span data-stu-id="cc646-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="cc646-120">หลังจากที่คุณระบุการประมาณโครงการแล้ว คุณสามารถนำข้อมูลนั้นเข้าสู่รายการที่เสนอราคาได้</span><span class="sxs-lookup"><span data-stu-id="cc646-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="cc646-121">บนหน้า **Quote Line Details** เลือก **Import from estimates** บนแถบรายการเพื่อสรุปการประมาณโครงการตามระดับของการซื้อขาย ประเภท บทบาท หรือประเภทงาน</span><span class="sxs-lookup"><span data-stu-id="cc646-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
