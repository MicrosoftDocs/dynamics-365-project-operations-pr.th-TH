---
title: ภาพรวมของ Project Service Automation
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับโซลูชันการรวม Dynamics 365 Project Service Automation กับ Dynamics 365 Finance
author: ruhercul
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c756caec6cd7eda8f891446d3e8309aca3b2482
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369642"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="5d9c2-103">ภาพรวมของ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="5d9c2-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5d9c2-104">โซลูชันการรวม Project Service Automation กับ Finance ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนซ์ข้อมูลระหว่างอินสแตนซ์ของ Dynamics 365 Finance และ Dynamics 365 Project Service Automation ผ่าน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="5d9c2-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="5d9c2-105">แม่แบบการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ของโครงการ สัญญาโครงการ รายละเอียดการให้บริการตามสัญญาโครงการ เหตุการณ์สำคัญของรายละเอียดการให้บริการตามสัญญาโครงการ งานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประมาณการชั่วโมง และการประมาณการค่าใช้จ่าย จาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="5d9c2-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="5d9c2-106">หากคุณใช้เวอร์ชัน 7.3.0 คุณต้องติดตั้ง KB 4074835</span><span class="sxs-lookup"><span data-stu-id="5d9c2-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="5d9c2-107">จากนั้น คุณจะสามารถรวมโครงการราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="5d9c2-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="5d9c2-108">หากคุณใช้เวอร์ชัน 7.3.0 และคุณนำธุรกรรมค่าธรรมเนียมมาจาก Project Service Automation คุณต้องติดตั้ง KB 4345320 เพื่อรวมค่าธรรมเนียมเหล่านั้นในใบแจ้งหนี้โครงการ</span><span class="sxs-lookup"><span data-stu-id="5d9c2-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="5d9c2-109">หากคุณใช้เวอร์ชัน 8.0 คุณจะสามารถใช้การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประมาณชั่วโมง การประมาณค่าใช้จ่าย และการล็อกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="5d9c2-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="5d9c2-110">หากคุณใช้เวอร์ชัน 8.0.1 หรือใหม่กว่า คุณจะสามารถซิงโครไนซ์ข้อมูลจริงได้</span><span class="sxs-lookup"><span data-stu-id="5d9c2-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="5d9c2-111">ก่อนที่คุณจะสามารถรวม Project Service Automation Finance คุณต้องตั้งค่าคอนฟิกพารามิเตอร์การรวม Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="5d9c2-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="5d9c2-112">สำหรับข้อมูลเพิ่มเติม ดู [พารามิเตอร์การรวม Project Service Automation](PSA-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="5d9c2-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="5d9c2-113">โซลูชันการรวมนี้เปิดใช้งานการซิงโครไนซ์โดยตรงในสถานการณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5d9c2-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="5d9c2-114">รักษาสัญญาโครงการใน Project Service Automation และซิงโครไนซ์โดยตรงจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="5d9c2-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="5d9c2-115">สร้างโครงการใน Project Service Automation และซิงโครไนซ์โดยตรงจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="5d9c2-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="5d9c2-116">รักษารายละเอียดการให้บริการตามสัญญาโครงการใน Project Service Automation และซิงโครไนซ์โดยตรงจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="5d9c2-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="5d9c2-117">รักษาเหตุการณ์สำคัญของรายละเอียดการให้บริการตามสัญญาโครงการใน Project Service Automation และซิงโครไนซ์โดยตรงจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="5d9c2-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="5d9c2-118">รักษางานใน Project Service Automation และซิงโครไนซ์โดยตรงจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="5d9c2-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="5d9c2-119">รักษาประเภทธุรกรรมค่าใช้จ่ายใน Finance และซิงโครไนซ์โดยตรงจาก Finance ไปยัง Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="5d9c2-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="5d9c2-120">สร้างการประมาณชั่วโมงของโครงการใน Project Service Automation และซิงโครไนซ์โดยตรงจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="5d9c2-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="5d9c2-121">สร้างการประมาณค่าใช้จ่ายของโครงการใน Project Service Automation และซิงโครไนซ์โดยตรงจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="5d9c2-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="5d9c2-122">สร้างเวลาโครงการ ค่าใช้จ่าย และค่าธรรมเนียมที่เกิดขึ้นจริงใน Project Service Automation และสร้างธุรกรรมโครงการในสมุดรายวันการรวม Project Service Automation เพื่อให้สามารถลงรายการบัญชีใน Finance</span><span class="sxs-lookup"><span data-stu-id="5d9c2-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="5d9c2-123">การซิงโครไนซ์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5d9c2-123">Data synchronization</span></span>

<span data-ttu-id="5d9c2-124">ภาพประกอบต่อไปนี้แสดงวิธีซิงโครไนซ์ข้อมูลโดยเป็นส่วนหนึ่งของการรวมระหว่าง Project Service Automation และ Finance</span><span class="sxs-lookup"><span data-stu-id="5d9c2-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="5d9c2-125">ขณะนี้แม่แบบพร้อมใช้งานบางรายการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5d9c2-125">Not all templates are currently available.</span></span> <span data-ttu-id="5d9c2-126">แม่แบบจะถูกนำออกใช้ เมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="5d9c2-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="5d9c2-127">[![การรวม Project Service Automation กับ Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="5d9c2-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="5d9c2-128">ข้อกำหนดของระบบสำหรับ Finance</span><span class="sxs-lookup"><span data-stu-id="5d9c2-128">System requirements for Finance</span></span>

<span data-ttu-id="5d9c2-129">ในการใช้โซลูชันการรวม Project Service Automation กับ Finance คุณต้องติดตั้ง Enterprise edition 7.3 ที่มีการปรับปรุง Platform 12 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="5d9c2-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="5d9c2-130">ข้อกำหนดของระบบสำหรับ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="5d9c2-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="5d9c2-131">ในการใช้โซลูชันการรวม Project Service Automation กับ Finance คุณต้องติดตั้งส่วนประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5d9c2-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="5d9c2-132">Dynamics 365 Project Service Automationรุ่น 9.0.0.0 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="5d9c2-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="5d9c2-133">โซลูชัน Prospect to cash สำหรับ Dynamics 365 Sales รุ่น 1.14.0.0 (v14) หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="5d9c2-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="5d9c2-134">โซลูชัน Project Service Automation to Finance สำหรับ Dynamics 365 Project Service Automation รุ่น 1.0.0.0 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="5d9c2-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="5d9c2-135">ติดตั้งโซลูชันการรวม Project Service Automation กับ Finance ในอินสแตนซ์ Project Service Automation ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5d9c2-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="5d9c2-136">ดาวน์โหลดโซลูชันการรวม Project Service Automation กับ Finance จาก [ศูนย์ดาวน์โหลด Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) และปฏิบัติตามคำแนะนำที่มาพร้อมกับโซลูชัน</span><span class="sxs-lookup"><span data-stu-id="5d9c2-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]