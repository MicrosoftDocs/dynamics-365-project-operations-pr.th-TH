---
title: ซิงโครไนซ์การประมาณการโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations
description: หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้เพื่อซิงโครไนซ์การประมาณชั่วโมงโครงการและค่าใช้จ่ายโครงการโดยตรงจาก Microsoft Dynamics 365 Project Service Automation ไปยัง Dynamics 365 Finance
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
ms.openlocfilehash: 58e204b2c1238e00ffb16533cc82dad69fbf77a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289482"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="70bdd-103">ซิงโครไนซ์การประมาณการโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="70bdd-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="70bdd-104">หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้เพื่อซิงโครไนซ์การประมาณชั่วโมงโครงการและค่าใช้จ่ายโครงการโดยตรงจาก Dynamics 365 Project Service Automation ไปยัง Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="70bdd-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="70bdd-105">การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประมาณชั่วโมง การประมาณค่าใช้จ่าย และการล็อกฟังก์ชัน จะพร้อมใช้งานในเวอร์ชัน 8.0</span><span class="sxs-lookup"><span data-stu-id="70bdd-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="70bdd-106">การรวมจริงพร้อมใช้งานในเวอร์ชัน 8.0.1 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="70bdd-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="70bdd-107">โฟลว์ข้อมูลสำหรับ Project Service Automation กับ Finance</span><span class="sxs-lookup"><span data-stu-id="70bdd-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="70bdd-108">โซลูชันการรวม Project Service Automation กับ Finance ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนซ์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance</span><span class="sxs-lookup"><span data-stu-id="70bdd-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="70bdd-109">แม่แบบการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ของข้อมูลเกี่ยวกับการประมาณชั่วโมงโครงการและค่าใช้จ่ายโครงการจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="70bdd-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="70bdd-110">ภาพประกอบต่อไปนี้แสดงวิธีซิงโครไนซ์ข้อมูลระหว่าง Project Service Automation และ Finance</span><span class="sxs-lookup"><span data-stu-id="70bdd-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="70bdd-111">[![โฟลว์ข้อมูลสำหรับการรวม Project Service Automation กับ Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="70bdd-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="70bdd-112">การประมาณการชั่วโมงโครงการ</span><span class="sxs-lookup"><span data-stu-id="70bdd-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="70bdd-113">แม่แบบและงาน</span><span class="sxs-lookup"><span data-stu-id="70bdd-113">Template and tasks</span></span>

<span data-ttu-id="70bdd-114">ในการเข้าถึงแม่แบบที่พร้อมใช้งาน ในศูนย์การจัดการ Microsoft Power Apps เลือก **โครงการ** และจากนั้น ที่มุมขวาบน ให้เลือก **โครงการใหม่** เพื่อเลือกแม่แบบสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="70bdd-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="70bdd-115">แม่แบบและงานพื้นฐานต่อไปนี้ถูกใช้เพื่อซิงโครไนซ์การประมาณชั่วโมงโครงการจาก Project Service Automation ไปยัง Finance:</span><span class="sxs-lookup"><span data-stu-id="70bdd-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="70bdd-116">**ชื่อของแม่แบบในการรวมข้อมูล:** การประมาณชั่วโมงโครงการ (PSA ไปยัง Fin และ Ops)</span><span class="sxs-lookup"><span data-stu-id="70bdd-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="70bdd-117">**ชื่อของงานในโครงการ:**</span><span class="sxs-lookup"><span data-stu-id="70bdd-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="70bdd-118">ความสัมพันธ์ของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="70bdd-118">Transaction relationships</span></span>
    - <span data-ttu-id="70bdd-119">การประเมินค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="70bdd-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="70bdd-120">ชุดเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="70bdd-120">Entity set</span></span>

| <span data-ttu-id="70bdd-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="70bdd-121">Project Service Automation</span></span> | <span data-ttu-id="70bdd-122">Finance</span><span class="sxs-lookup"><span data-stu-id="70bdd-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="70bdd-123">งานโครงการ</span><span class="sxs-lookup"><span data-stu-id="70bdd-123">Project tasks</span></span>              | <span data-ttu-id="70bdd-124">เอนทิตีการรวมสำหรับการประมาณชั่วโมงของโครงการ</span><span class="sxs-lookup"><span data-stu-id="70bdd-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="70bdd-125">โฟลว์เอนทิตี</span><span class="sxs-lookup"><span data-stu-id="70bdd-125">Entity flow</span></span>

<span data-ttu-id="70bdd-126">การประมาณชั่วโมงโครงการได้รับการจัดการใน Project Service Automation และมีการซิงโครไนซ์กับ Finance เป็นการคาดการณ์ชั่วโมงของโครงการ</span><span class="sxs-lookup"><span data-stu-id="70bdd-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="70bdd-127">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="70bdd-127">Prerequisites</span></span>

<span data-ttu-id="70bdd-128">ก่อนที่จะซิงโครไนซ์การประมาณชั่วโมงของโครงการได้ คุณต้องซิงโครไนซ์โครงการ งานโครงการ และประเภทธุรกรรมค่าใช้จ่ายโครงการ</span><span class="sxs-lookup"><span data-stu-id="70bdd-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="70bdd-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="70bdd-129">Power Query</span></span>

<span data-ttu-id="70bdd-130">ในแม่แบบประมาณการชั่วโมงของโครงการ คุณต้องใช้ Microsoft Power Query สำหรับ Excel เพื่อทำงานเหล่านี้ให้เสร็จสิ้น:</span><span class="sxs-lookup"><span data-stu-id="70bdd-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="70bdd-131">ตั้งค่ารหัสแบบจำลองการคาดการณ์เริ่มต้นที่จะใช้เมื่อการรวมสร้างการคาดการณ์รายชั่วโมงใหม่</span><span class="sxs-lookup"><span data-stu-id="70bdd-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="70bdd-132">กรองเรกคอร์ดเฉพาะทรัพยากรในงานที่จะทำให้การรวมเข้ากับการคาดการณ์ชั่วโมงล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="70bdd-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="70bdd-133">กรองแถวหมวดหมู่ธุรกรรมที่ว่างเปล่าออก</span><span class="sxs-lookup"><span data-stu-id="70bdd-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="70bdd-134">ความล้มเหลวในการทำงานนี้ให้เสร็จสมบูรณ์อาจส่งผลให้การคาดการณ์ชั่วโมงไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="70bdd-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="70bdd-135">ตั้งค่ารหัสแบบจำลองการคาดการณ์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="70bdd-135">Set the default forecast model ID</span></span>

<span data-ttu-id="70bdd-136">หากต้องการอัปเดตรหัสแบบจำลองการคาดการณ์เริ่มต้นในแม่แบบ ให้คลิกลูกศร **แม็ป** เพื่อเปิดการแม็ป</span><span class="sxs-lookup"><span data-stu-id="70bdd-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="70bdd-137">จากนั้นเลือกลิงก์ **การสืบค้นและการกรองขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="70bdd-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="70bdd-138">หากคุณกำลังใช้แม่แบบการประมาณการชั่วโมงโครงการเริ่มต้น (PSA ไปยัง Fin และ Ops) ให้เลือก **แทรกเงื่อนไข** ในรายการ **ขั้นตอนที่ใช้**</span><span class="sxs-lookup"><span data-stu-id="70bdd-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="70bdd-139">ในรายการ **ฟังก์ชัน** ให้แทนที่ **O\_การคาดการณ์** ด้วยชื่อของรหัสแบบจำลองการคาดการณ์ที่ควรใช้กับการรวม</span><span class="sxs-lookup"><span data-stu-id="70bdd-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="70bdd-140">แม่แบบเริ่มต้นมีรหัสแบบจำลองการคาดการณ์จากข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="70bdd-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="70bdd-141">หากคุณกำลังสร้างแม่แบบใหม่ คุณต้องเพิ่มคอลัมน์นี้</span><span class="sxs-lookup"><span data-stu-id="70bdd-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="70bdd-142">ใน Power Query ให้เลือก **เพิ่มคอลัมน์เงื่อนไข** และป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **ModelID**</span><span class="sxs-lookup"><span data-stu-id="70bdd-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="70bdd-143">ป้อนเงื่อนไขสำหรับคอลัมน์โดย ที่ถ้างานโครงการไม่ว่าง แล้ว \<enter the forecast model ID\>; อื่นว่าง</span><span class="sxs-lookup"><span data-stu-id="70bdd-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="70bdd-144">กรองเรกคอร์ดเฉพาะทรัพยากรออก</span><span class="sxs-lookup"><span data-stu-id="70bdd-144">Filter out resource-specific records</span></span>

<span data-ttu-id="70bdd-145">แม่แบบการประมาณชั่วโมงของโครงการ (PSA ไปยัง Fin และ Ops) มีตัวกรองเริ่มต้นที่ลบเรกคอร์ดเฉพาะทรัพยากรใดๆ</span><span class="sxs-lookup"><span data-stu-id="70bdd-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="70bdd-146">หากคุณสร้างแม่แบบของคุณเอง คุณต้องเพิ่มตัวกรองนี้</span><span class="sxs-lookup"><span data-stu-id="70bdd-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="70bdd-147">เลือกลิงก์ **การสืบค้นและการกรองขั้นสูง** เพื่อกรองคอลัมน์ **msdyn\_islinetask** เพื่อรวมเรกคอร์ด **เท็จ** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="70bdd-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="70bdd-148">กรองแถวหมวดหมู่ธุรกรรมที่ว่างเปล่าออก</span><span class="sxs-lookup"><span data-stu-id="70bdd-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="70bdd-149">คุณต้องเพิ่มตัวกรองเพื่อลบแถวที่มีหมวดหมู่ธุรกรรมว่าง</span><span class="sxs-lookup"><span data-stu-id="70bdd-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="70bdd-150">จำเป็นต้องมีงานนี้ ไม่ว่าคุณจะใช้แม่แบบเริ่มต้นหรือสร้างแม่แบบของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="70bdd-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="70bdd-151">ตัวกรองนี้จะลบแถวสรุปใดๆ ออกจาก Project Service Automation ที่อาจทำให้การคาดการณ์ชั่วโมงใน Finance ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="70bdd-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="70bdd-152">เลือกลิงก์ **การสืบค้นและการกรองขั้นสูง** เพื่อกรองเรกคอร์ด null ในคอลัมน์ **msdyn\_ประเภทธุรกรรม\_มูลค่า**</span><span class="sxs-lookup"><span data-stu-id="70bdd-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="70bdd-153">การแม็ปแม่แบบในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="70bdd-153">Template mapping in Data integration</span></span>

<span data-ttu-id="70bdd-154">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานแม่แบบในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="70bdd-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="70bdd-155">การแม็ปแสดงข้อมูลฟิลด์ที่จะซิงโครไนซ์จาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="70bdd-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="70bdd-156">[![การแม็ปงานแม่แบบในการรวมข้อมูล](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="70bdd-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="70bdd-157">การประมาณการค่าใช้จ่ายโครงการ</span><span class="sxs-lookup"><span data-stu-id="70bdd-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="70bdd-158">แม่แบบและงาน</span><span class="sxs-lookup"><span data-stu-id="70bdd-158">Template and tasks</span></span>

<span data-ttu-id="70bdd-159">แม่แบบและงานพื้นฐานต่อไปนี้ถูกใช้เพื่อซิงโครไนซ์การประมาณค่าใช้จ่ายโครงการจาก Project Service Automation ไปยัง Finance:</span><span class="sxs-lookup"><span data-stu-id="70bdd-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="70bdd-160">**ชื่อของแม่แบบในการรวมข้อมูล:** การประมาณค่าใช้จ่ายโครงการ (PSA ไปยัง Fin และ Ops)</span><span class="sxs-lookup"><span data-stu-id="70bdd-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="70bdd-161">**ชื่อของงานในโครงการ:**</span><span class="sxs-lookup"><span data-stu-id="70bdd-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="70bdd-162">ความสัมพันธ์ของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="70bdd-162">Transaction relationships</span></span> 
    - <span data-ttu-id="70bdd-163">การประเมินค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="70bdd-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="70bdd-164">ชุดเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="70bdd-164">Entity set</span></span>

| <span data-ttu-id="70bdd-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="70bdd-165">Project Service Automation</span></span> | <span data-ttu-id="70bdd-166">Finance</span><span class="sxs-lookup"><span data-stu-id="70bdd-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="70bdd-167">การเชื่อมต่อธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="70bdd-167">Transaction Connections</span></span>    | <span data-ttu-id="70bdd-168">เอนทิตีการรวมสำหรับความสัมพันธ์ธุรกรรมโครงการ</span><span class="sxs-lookup"><span data-stu-id="70bdd-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="70bdd-169">บรรทัดการประมาณการ</span><span class="sxs-lookup"><span data-stu-id="70bdd-169">Estimate Lines</span></span>             | <span data-ttu-id="70bdd-170">เอนทิตีการรวมสำหรับการประมาณค่าใช้จ่ายของโครงการ</span><span class="sxs-lookup"><span data-stu-id="70bdd-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="70bdd-171">โฟลว์เอนทิตี</span><span class="sxs-lookup"><span data-stu-id="70bdd-171">Entity flow</span></span>

<span data-ttu-id="70bdd-172">การประมาณค่าใช้จ่ายโครงการได้รับการจัดการใน Project Service Automation และมีการซิงโครไนซ์กับ Finance เป็นการคาดการณ์ค่าใช้จ่ายของโครงการ</span><span class="sxs-lookup"><span data-stu-id="70bdd-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="70bdd-173">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="70bdd-173">Prerequisites</span></span>

<span data-ttu-id="70bdd-174">ก่อนที่จะซิงโครไนซ์การประมาณค่าใช้จ่ายของโครงการได้ คุณต้องซิงโครไนซ์โครงการ งานโครงการ และประเภทธุรกรรมค่าใช้จ่ายโครงการ</span><span class="sxs-lookup"><span data-stu-id="70bdd-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="70bdd-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="70bdd-175">Power Query</span></span>

<span data-ttu-id="70bdd-176">ในแม่แบบประมาณการค่าใช้จ่ายของโครงการ คุณต้องใช้ Power Query เพื่อทำงานต่อไปนี้ให้เสร็จสิ้น:</span><span class="sxs-lookup"><span data-stu-id="70bdd-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="70bdd-177">กรองเพื่อรวมเฉพาะเรกคอร์ดรายการประมาณการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="70bdd-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="70bdd-178">ตั้งค่ารหัสแบบจำลองการคาดการณ์เริ่มต้นที่จะใช้เมื่อการรวมสร้างการคาดการณ์รายชั่วโมงใหม่</span><span class="sxs-lookup"><span data-stu-id="70bdd-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="70bdd-179">เปลี่ยนประเภทการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="70bdd-179">Transform the billing types.</span></span>
- <span data-ttu-id="70bdd-180">เปลี่ยนประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="70bdd-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="70bdd-181">กรองเพื่อรวมเฉพาะรายการประมาณการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="70bdd-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="70bdd-182">แม่แบบประมาณการค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin และ Ops) มีตัวกรองเริ่มต้นที่รวมเฉพาะรายการค่าใช้จ่ายในการรวม</span><span class="sxs-lookup"><span data-stu-id="70bdd-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="70bdd-183">หากคุณสร้างแม่แบบของคุณเอง คุณต้องเพิ่มตัวกรองนี้</span><span class="sxs-lookup"><span data-stu-id="70bdd-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="70bdd-184">เลือกงาน **ความสัมพันธ์ของธุรกรรม** แล้วคลิกลูกศร **แม็ป** เพื่อเปิดการแม็ป</span><span class="sxs-lookup"><span data-stu-id="70bdd-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="70bdd-185">เลือกลิงก์ **การสืบค้นและการกรองขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="70bdd-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="70bdd-186">กรองคอลัมน์ **msdyn\_transactiontype1** เพื่อให้รวมเฉพาะ **msdyn\_estimateline**</span><span class="sxs-lookup"><span data-stu-id="70bdd-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="70bdd-187">ตั้งค่ารหัสแบบจำลองการคาดการณ์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="70bdd-187">Set the default forecast model ID</span></span>

<span data-ttu-id="70bdd-188">หากต้องการอัปเดตรหัสแบบจำลองการคาดการณ์เริ่มต้นในแม่แบบ ให้เลือกงาน **ประมาณการค่าใช้จ่าย** จากนั้นคลิกลูกศร **แม็ป** เพื่อเปิดการแม็ป</span><span class="sxs-lookup"><span data-stu-id="70bdd-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="70bdd-189">เลือกลิงก์ **การสืบค้นและการกรองขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="70bdd-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="70bdd-190">หากคุณกำลังใช้แม่แบบการประมาณการค่าใช้จ่ายโครงการเริ่มต้น (PSA ไปยัง Fin และ Ops) ใน Power Query ให้เลือก **แทรกเงื่อนไข** จากส่วน **ขั้นตอนที่ใช้**</span><span class="sxs-lookup"><span data-stu-id="70bdd-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="70bdd-191">ในรายการ **ฟังก์ชัน** ให้แทนที่ **O\_การคาดการณ์** ด้วยชื่อของรหัสแบบจำลองการคาดการณ์ที่ควรใช้กับการรวม</span><span class="sxs-lookup"><span data-stu-id="70bdd-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="70bdd-192">แม่แบบเริ่มต้นมีรหัสแบบจำลองการคาดการณ์จากข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="70bdd-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="70bdd-193">หากคุณกำลังสร้างแม่แบบใหม่ คุณต้องเพิ่มคอลัมน์นี้</span><span class="sxs-lookup"><span data-stu-id="70bdd-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="70bdd-194">ใน Power Query ให้เลือก **เพิ่มคอลัมน์เงื่อนไข** และป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **ModelID**</span><span class="sxs-lookup"><span data-stu-id="70bdd-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="70bdd-195">ป้อนเงื่อนไขสำหรับคอลัมน์โดย ที่ถ้ารหัสรายการประมาณการไม่ว่าง แล้ว \<enter the forecast model ID\>; อื่นว่าง</span><span class="sxs-lookup"><span data-stu-id="70bdd-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="70bdd-196">เปลี่ยนประเภทการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="70bdd-196">Transform the billing types</span></span>

<span data-ttu-id="70bdd-197">แม่แบบการประมาณการค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin และ Ops) ประกอบด้วยคอลัมน์เงื่อนไขที่ใช้ในการแปลงประเภทการเรียกเก็บเงินที่ได้รับจาก Project Service Automation ระหว่างการรวม</span><span class="sxs-lookup"><span data-stu-id="70bdd-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="70bdd-198">หากคุณสร้างแม่แบบของคุณเอง คุณต้องเพิ่มคอลัมน์เงื่อนไขนี้</span><span class="sxs-lookup"><span data-stu-id="70bdd-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="70bdd-199">เลือกลิงก์ **การสืบค้นและการกรองขั้นสูง** จากนั้นเลือก **เพิ่มคอลัมน์เงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="70bdd-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="70bdd-200">ป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **BillingType**</span><span class="sxs-lookup"><span data-stu-id="70bdd-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="70bdd-201">จากนั้นใส่เงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="70bdd-201">Then enter the following condition:</span></span>

<span data-ttu-id="70bdd-202">ถ้า **msdyn\_billingtype** = 192350000 ดังนั้น **ไม่คิดค่าบริการ**</span><span class="sxs-lookup"><span data-stu-id="70bdd-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="70bdd-203">หรือถ้า **msdyn\_billingtype** = 192350001 ดังนั้น **คิดค่าบริการ**</span><span class="sxs-lookup"><span data-stu-id="70bdd-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="70bdd-204">หรือถ้า **msdyn\_billingtype** = 192350002 ดังนั้น **ส่วนเสริม**</span><span class="sxs-lookup"><span data-stu-id="70bdd-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="70bdd-205">หรือ **ไม่พร้อมใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="70bdd-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="70bdd-206">เปลี่ยนประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="70bdd-206">Transform the transaction types</span></span>

<span data-ttu-id="70bdd-207">แม่แบบการประมาณการค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin และ Ops) ประกอบด้วยคอลัมน์เงื่อนไขที่ใช้ในการแปลงประเภทธุรกรรมที่ได้รับจาก Project Service Automation ระหว่างการรวม</span><span class="sxs-lookup"><span data-stu-id="70bdd-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="70bdd-208">หากคุณสร้างแม่แบบของคุณเอง คุณต้องเพิ่มคอลัมน์เงื่อนไขนี้</span><span class="sxs-lookup"><span data-stu-id="70bdd-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="70bdd-209">เลือกลิงก์ **การสืบค้นและการกรองขั้นสูง** จากนั้นเลือก **เพิ่มคอลัมน์เงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="70bdd-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="70bdd-210">ป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **TransactionType**</span><span class="sxs-lookup"><span data-stu-id="70bdd-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="70bdd-211">จากนั้นใส่เงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="70bdd-211">Then enter the following condition:</span></span>

<span data-ttu-id="70bdd-212">ถ้า **msdyn\_transactiontypecode** = 192350000 แล้ว **ค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="70bdd-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="70bdd-213">หรือถ้า **msdyn\_transactiontypecode** = 192350005 ดังนั้น **ยอดขาย**</span><span class="sxs-lookup"><span data-stu-id="70bdd-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="70bdd-214">หรือ **null**</span><span class="sxs-lookup"><span data-stu-id="70bdd-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="70bdd-215">การแม็ปแม่แบบในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="70bdd-215">Template mapping in Data integration</span></span>

<span data-ttu-id="70bdd-216">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานแม่แบบในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="70bdd-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="70bdd-217">การแม็ปแสดงข้อมูลฟิลด์ที่จะซิงโครไนซ์จาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="70bdd-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="70bdd-218">[![การแม็ปแม่แบบของธุรกรรมประมาณการค่าใช้จ่าย](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="70bdd-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="70bdd-219">[![การแม็ปแม่แบบของประมาณการค่าใช้จ่าย](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="70bdd-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]