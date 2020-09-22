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
ms.prod: ''
ms.technology: ''
ms.assetid: eb5ab6a1-fdff-490e-9c2a-19aef493de11
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4431c1c894a01bfecc132575d8981ebc9fe50b51
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756404"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="0cab7-103">การประมาณการณ์ยอดขายและโครงการ</span><span class="sxs-lookup"><span data-stu-id="0cab7-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0cab7-104">ในระหว่างกระบวนการขาย คุณสามารถทำการประมาณการณ์ยอดขายได้โดยเชื่อมต่อโครงการเข้ากับใบแจ้งราคา</span><span class="sxs-lookup"><span data-stu-id="0cab7-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="0cab7-105">โดยวิธีการนี้ การระบุยอดประมาณการณ์สามารถเกิดขึ้นได้ระหว่างกระบวนการขายซึ่งเป็นข้อดีของการวางแผนงานและการประเมินความสามารถ</span><span class="sxs-lookup"><span data-stu-id="0cab7-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="0cab7-106">หากยอดขายเกิดขึ้นจริง แผนงานที่ใข้ในการประมาณการณ์ยอดขายจะถูกนำมาใช้เป็นเกณฑ์ในการกำหนดแผนงานของโครงการ</span><span class="sxs-lookup"><span data-stu-id="0cab7-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="0cab7-107">การเชื่อมโยงโครงการกับใบแจ้งราคา</span><span class="sxs-lookup"><span data-stu-id="0cab7-107">Linking a project to a quote line</span></span>

<span data-ttu-id="0cab7-108">เมื่อคุณสร้างโครงการจากใบแจ้งราคา คุณสามารถสร้างโครงการใหม่หรือเชื่อมโยงกับโครงการที่มีอยู่เดิมบนหน้า **Quote Line**</span><span class="sxs-lookup"><span data-stu-id="0cab7-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![รายการที่เสนอราคา (แบบฟอร์ม)](media/project-8.png)
 
<span data-ttu-id="0cab7-110">เมื่อคุณสร้างโครงการใหม่รายละเอียดรายการที่เสนอราคา คุณจะสามารถใช้งานเท็มเพลตของโครงการได้</span><span class="sxs-lookup"><span data-stu-id="0cab7-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="0cab7-111">เท็มเพลตของโครงการเป็นแบบจำลองของโครงการที่นำเสนอแผนการมาตรฐานของโครงการและการประมาณการทางการเงินที่เป็นรูปแบบขององค์กร</span><span class="sxs-lookup"><span data-stu-id="0cab7-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="0cab7-112">เท็มเพลตดังกล่าวยังสามารถแสดงสำเนาของแผนการโครงการและประมาณการจากโครงการที่ผ่านมาได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="0cab7-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![รายละเอียดบรรทัดใบเสนอราคา](media/project-9.png)
  
<span data-ttu-id="0cab7-114">เมื่อมีการสร้างโครงการจากใบแจ้งราคาแล้ว โครงการจะเชื่อมโยงข้อมูลกับรายการที่แจ้งราคาโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="0cab7-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="0cab7-115">ส่วนประกอบของการประมาณโครงการ</span><span class="sxs-lookup"><span data-stu-id="0cab7-115">Components of estimates in a project</span></span>

<span data-ttu-id="0cab7-116">ตารางงานจะทำให้คุณสามารถแบ่งงานออกเป็นขั้นๆ โดยยังคงไว้ซึ่งลำดับของงานที่ต้องทำ ระบุทรัพยากรที่ต้องใช้เพื่อให้งานบรรลุผล และประมาณการเวลาที่ต้องใช้ในแต่ละงานด้วย</span><span class="sxs-lookup"><span data-stu-id="0cab7-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="0cab7-117">คุณสามารถกำหนดเวลางานและประมาณการแผนงานได้โดยใช้ฟิลด์บนแท็บ **Schedule** ของหน้า **Project**</span><span class="sxs-lookup"><span data-stu-id="0cab7-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="0cab7-118">เนื่องจากรายการราคามีความเกี่ยวข้องกับโครงการ การประมาณการทางการเงินจะถูกคำนวณโดยการใช้ราคาต้นทุนและราคาขายที่ระบุในรายการราคา</span><span class="sxs-lookup"><span data-stu-id="0cab7-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="0cab7-119">การนำเข้าค่าประมาณจากโครงการสู่ใบแจ้งราคา</span><span class="sxs-lookup"><span data-stu-id="0cab7-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="0cab7-120">หลังจากที่คุณระบุการประมาณโครงการแล้ว คุณสามารถนำข้อมูลนั้นเข้าสู่รายการที่เสนอราคาได้</span><span class="sxs-lookup"><span data-stu-id="0cab7-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="0cab7-121">บนหน้า **Quote Line Details** เลือก **Import from estimates** บนแถบรายการเพื่อสรุปการประมาณโครงการตามระดับของการซื้อขาย ประเภท บทบาท หรือประเภทงาน</span><span class="sxs-lookup"><span data-stu-id="0cab7-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
