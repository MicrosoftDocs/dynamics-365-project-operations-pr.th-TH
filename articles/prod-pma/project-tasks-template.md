---
title: ซิงโครไนซ์งานโครงการโดยตรงจาก Project Service Automation ถึง Finance and Operations
description: หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้เพื่อซิงโครไนซ์งานโครงการโดยตรงจาก Microsoft Dynamics 365 Project Service Automation ถึง Dynamics 365 Finance
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288942"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="c6cfa-103">ซิงโครไนซ์งานโครงการโดยตรงจาก Project Service Automation ถึง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6cfa-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c6cfa-104">หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้เพื่อซิงโครไนซ์งานโครงการโดยตรงจาก Dynamics 365 Project Service Automation ถึง Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="c6cfa-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="c6cfa-105">การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประมาณชั่วโมง การประมาณค่าใช้จ่าย และการล็อกฟังก์ชัน จะพร้อมใช้งานในเวอร์ชัน 8.0</span><span class="sxs-lookup"><span data-stu-id="c6cfa-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="c6cfa-106">หากคุณใช้ Enterprise Edition 7.3.0 หลังจากที่คุณติดตั้ง KB 4132657 และ KB 4132660 คุณจะสามารถใช้แม่แบบเพื่อรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประมาณชั่วโมง การประมาณค่าใช้จ่ายและข้อมูลจริง และเพื่อตั้งค่าคอนฟิกการล็อกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="c6cfa-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="c6cfa-107">หากคุณต้องรีเซ็ตการกระจายการลงบัญชี เราขอแนะนำให้คุณติดตั้ง KB 4131710 ด้วย</span><span class="sxs-lookup"><span data-stu-id="c6cfa-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="c6cfa-108">การรวมจริงพร้อมใช้งานในเวอร์ชัน 8.0.1 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="c6cfa-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="c6cfa-109">โฟลว์ข้อมูลสำหรับ Project Service Automation กับ Finance</span><span class="sxs-lookup"><span data-stu-id="c6cfa-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="c6cfa-110">โซลูชันการรวม Project Service Automation กับ Finance ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนซ์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance</span><span class="sxs-lookup"><span data-stu-id="c6cfa-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="c6cfa-111">แม่แบบการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ของข้อมูลเกี่ยวกับงานโครงการจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="c6cfa-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c6cfa-112">ภาพประกอบต่อไปนี้แสดงวิธีซิงโครไนซ์ข้อมูลระหว่าง Project Service Automation และ Finance</span><span class="sxs-lookup"><span data-stu-id="c6cfa-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="c6cfa-113">[![โฟลว์ข้อมูลสำหรับการรวม Project Service Automation กับ Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="c6cfa-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="c6cfa-114">แม่แบบและงาน</span><span class="sxs-lookup"><span data-stu-id="c6cfa-114">Template and task</span></span>

<span data-ttu-id="c6cfa-115">ในการเข้าถึงแม่แบบ ในศูนย์การจัดการ Microsoft Power Apps เลือก **โครงการ** และจากนั้น ที่มุมขวาบน ให้เลือก **โครงการใหม่** เพื่อเลือกแม่แบบสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="c6cfa-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="c6cfa-116">แม่แบบและงานพื้นฐานต่อไปนี้ถูกใช้เพื่อซิงโครไนซ์งานโครงการจาก Project Service Automation ถึง Finance:</span><span class="sxs-lookup"><span data-stu-id="c6cfa-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="c6cfa-117">**ชื่อของแม่แบบในการรวมข้อมูล:** งานโครงการ (PSA ถึง Fin และ Ops)</span><span class="sxs-lookup"><span data-stu-id="c6cfa-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="c6cfa-118">**ชื่อของงานในโครงการ:** งานโครงการ</span><span class="sxs-lookup"><span data-stu-id="c6cfa-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="c6cfa-119">ก่อนที่จะเกิดการซิงโครไนซ์งานโครงการ คุณต้องซิงโครไนซ์สัญญาโครงการและโครงการ</span><span class="sxs-lookup"><span data-stu-id="c6cfa-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="c6cfa-120">ชุดเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="c6cfa-120">Entity set</span></span>

| <span data-ttu-id="c6cfa-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c6cfa-121">Project Service Automation</span></span> | <span data-ttu-id="c6cfa-122">Finance</span><span class="sxs-lookup"><span data-stu-id="c6cfa-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="c6cfa-123">งานโครงการ</span><span class="sxs-lookup"><span data-stu-id="c6cfa-123">Project Tasks</span></span>              | <span data-ttu-id="c6cfa-124">เอนทิตีการรวมสำหรับงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="c6cfa-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="c6cfa-125">โฟลว์เอนทิตี</span><span class="sxs-lookup"><span data-stu-id="c6cfa-125">Entity flow</span></span>

<span data-ttu-id="c6cfa-126">งานโครงการได้รับการจัดการใน Project Service Automation และมีการซิงโครไนซ์กับ Finance เป็นกิจกรรมของโครงการ</span><span class="sxs-lookup"><span data-stu-id="c6cfa-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c6cfa-127">ข้อกำหนดเบื้องต้นและการตั้งค่าการแม็ป</span><span class="sxs-lookup"><span data-stu-id="c6cfa-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="c6cfa-128">ก่อนที่จะเกิดการซิงโครไนซ์งานโครงการ คุณต้องซิงโครไนซ์สัญญาโครงการและโครงการ</span><span class="sxs-lookup"><span data-stu-id="c6cfa-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="c6cfa-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="c6cfa-129">Power Query</span></span>

<span data-ttu-id="c6cfa-130">คุณต้องใช้ Microsoft Power Query สำหรับ Excel เพื่อกรองข้อมูล หากตรงตามเงื่อนไขนี้:</span><span class="sxs-lookup"><span data-stu-id="c6cfa-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="c6cfa-131">คุณมีเรกคอร์ดเฉพาะทรัพยากรในงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="c6cfa-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="c6cfa-132">หากคุณต้องใช้ Power Query ให้ปฏิบัติตามแนวทางนี้:</span><span class="sxs-lookup"><span data-stu-id="c6cfa-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="c6cfa-133">แม่แบบงานโครงการ (PSA ถึง Fin และ Ops) มีตัวกรองเริ่มต้นที่แยกเรกคอร์ดเฉพาะทรัพยากรออกจากงานโครงการ โดยตั้งค่าตัวกรองใน **IsLineTask** เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="c6cfa-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="c6cfa-134">หากคุณสร้างแม่แบบของคุณเอง คุณต้องเพิ่มตัวกรองนี้</span><span class="sxs-lookup"><span data-stu-id="c6cfa-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c6cfa-135">การแม็ปแม่แบบในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c6cfa-135">Template mapping in Data integration</span></span>

<span data-ttu-id="c6cfa-136">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานแม่แบบในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c6cfa-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="c6cfa-137">การแม็ปแสดงข้อมูลฟิลด์ที่จะซิงโครไนซ์จาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="c6cfa-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c6cfa-138">[![การแม็ปแม่แบบ](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="c6cfa-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]