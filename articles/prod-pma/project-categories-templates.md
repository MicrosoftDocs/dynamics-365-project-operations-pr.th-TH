---
title: ซิงโครไนซ์ประเภทค่าใช้จ่ายโครงการระหว่าง Finance and Operations และ Project Service Automation
description: หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้เพื่อซิงโครไนซ์ประเภทค่าใช้จ่ายของโครงการระหว่าง Microsoft Dynamics 365 Finance และ Dynamics 365 Project Service Automation
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999874"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="95e70-103">ซิงโครไนซ์ประเภทค่าใช้จ่ายโครงการระหว่าง Finance and Operations และ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="95e70-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="95e70-104">หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้เพื่อซิงโครไนซ์ประเภทค่าใช้จ่ายของโครงการระหว่าง Dynamics 365 Finance และ Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="95e70-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="95e70-105">การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประมาณชั่วโมง การประมาณค่าใช้จ่าย และการล็อกฟังก์ชัน จะพร้อมใช้งานในเวอร์ชัน 8.0</span><span class="sxs-lookup"><span data-stu-id="95e70-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="95e70-106">การรวมจริงพร้อมใช้งานในเวอร์ชัน 8.0.1 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="95e70-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="95e70-107">หากคุณใช้ Enterprise Edition 7.3.0 หลังจากที่คุณติดตั้ง KB 4132657 และ KB 4132660 คุณจะสามารถใช้แม่แบบเพื่อรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประมาณชั่วโมง การประมาณค่าใช้จ่ายและข้อมูลจริง และเพื่อตั้งค่าคอนฟิกการล็อกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="95e70-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="95e70-108">หากคุณต้องรีเซ็ตการกระจายการลงบัญชี เราขอแนะนำให้คุณติดตั้ง KB 4131710 ด้วย</span><span class="sxs-lookup"><span data-stu-id="95e70-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="95e70-109">โฟลว์ข้อมูลสำหรับ Project Service Automation และ Finance</span><span class="sxs-lookup"><span data-stu-id="95e70-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="95e70-110">โซลูชันการรวม Project Service Automation และ Finance ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนซ์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance</span><span class="sxs-lookup"><span data-stu-id="95e70-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="95e70-111">แม่แบบการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ของข้อมูลเกี่ยวกับประเภทธุรกรรมค่าใช้จ่ายโครงการระหว่าง Project Service Automation และ Finance</span><span class="sxs-lookup"><span data-stu-id="95e70-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="95e70-112">ถ้าประเภทค่าใช้จ่ายของโครงการมีการต่อยอดใน Finance ขั้นตอนการรวมจะเริ่มจาก Finance ไปยัง Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="95e70-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="95e70-113">จากนั้นรหัสการรวมของประเภทค่าใช้จ่ายโครงการจะถูกอัปเดตผ่านการซิงโครไนซ์จาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="95e70-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="95e70-114">ถ้าประเภทค่าใช้จ่ายของโครงการมีการต่อยอดใน Project Service Automation โฟลว์การรวมจะเริ่มจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="95e70-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="95e70-115">ประเภทโครงการต้องได้รับการกำหนดค่าไว้แล้วใน Finance ก่อนการซิงโครไนซ์จาก Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="95e70-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="95e70-116">จากนั้นซิงโครไนซ์จาก Finance กลับไปยัง Project Service Automation จากนั้นจาก Project Service Automation ไปยัง Finance อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="95e70-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="95e70-117">ด้วยวิธีนี้คุณช่วยรับประกันได้ว่าประเภทต่างๆ จะเชื่อมโยงกันและไม่มีการสร้างรายการซ้ำ</span><span class="sxs-lookup"><span data-stu-id="95e70-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="95e70-118">โดยทั่วไปแล้วประเภทค่าใช้จ่ายโครงการจะมีการต่อยอดในด้านการเงิน</span><span class="sxs-lookup"><span data-stu-id="95e70-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="95e70-119">อย่างไรก็ตามหากไม่เป็นเช่นนั้นหรือหากมีการสร้างประเภทค่าใช้จ่ายใน Project Service Automation ก่อนอื่นคุณต้องซิงโครไนซ์โดยใช้แม่แบบประเภทธุรกรรมค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin และ Ops)</span><span class="sxs-lookup"><span data-stu-id="95e70-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="95e70-120">จากนั้นซิงโครไนซ์โดยใช้แม่แบบประเภทธุรกรรมค่าใช้จ่ายโครงการ (Fin และ Ops ไปยัง PSA)</span><span class="sxs-lookup"><span data-stu-id="95e70-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="95e70-121">จากนั้นคุณควรเรียกใช้การซิงโครไนซ์จาก Project Service Automation ไปยัง Finance อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="95e70-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="95e70-122">ถ้าคุณซิงโครไนซ์ก่อนจาก Project Service Automation ต้องปฏิบัติตามข้อกำหนดต่อไปนี้ใน Finance ก่อนที่จะรันการซิงโครไนซ์:</span><span class="sxs-lookup"><span data-stu-id="95e70-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="95e70-123">ประเภทที่ใช้ร่วมกันที่ตรงกับประเภทโครงการที่ตั้งค่าใน Project Service Automation ต้องมีอยู่และต้องเปิดใช้งานสำหรับทั้ง **โครงการ** และ **ค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="95e70-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="95e70-124">สำหรับนิติบุคคลทางการเงินแต่ละรายที่ต้องรวมเข้าด้วยกัน ต้องมีประเภทโครงการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="95e70-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="95e70-125">**ประเภทโครงการ** มีอยู่</span><span class="sxs-lookup"><span data-stu-id="95e70-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="95e70-126">เปิดใช้งาน **ใช้ในค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="95e70-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="95e70-127">เปิดใช้งาน **ใช้งานอยู่ในสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="95e70-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="95e70-128">**ประเภทธุรกรรม** ถูกตั้งค่าเป็น **ค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="95e70-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="95e70-129">ภาพประกอบต่อไปนี้แสดงวิธีซิงโครไนซ์ข้อมูลระหว่าง Project Service Automation และ Finance</span><span class="sxs-lookup"><span data-stu-id="95e70-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="95e70-130">[![โฟลว์ข้อมูลสำหรับการรวม Project Service Automation กับ Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="95e70-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="95e70-131">การซิงโครไนซ์ประเภทค่าใช้จ่ายโครงการจาก Finance ไปยัง Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="95e70-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="95e70-132">แม่แบบและงาน</span><span class="sxs-lookup"><span data-stu-id="95e70-132">Template and task</span></span>

<span data-ttu-id="95e70-133">ในการเข้าถึงแม่แบบ ในศูนย์การจัดการ Microsoft Power Apps เลือก **โครงการ** และจากนั้น ที่มุมขวาบน ให้เลือก **โครงการใหม่** เพื่อเลือกแม่แบบสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="95e70-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="95e70-134">แม่แบบและงานพื้นฐานต่อไปนี้ถูกใช้เพื่อซิงโครไนซ์ประเภทค่าใช้จ่ายโครงการจาก Finance ไปยัง Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="95e70-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="95e70-135">**ชื่อของแม่แบบในการรวมข้อมูล:** ประเภทธุรกรรมค่าใช้จ่ายโครงการ (Fin และ Ops ไปยัง PSA)</span><span class="sxs-lookup"><span data-stu-id="95e70-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="95e70-136">**ชื่อของงานในโครงการ:** ซิงค์ประเภทกับ PSA</span><span class="sxs-lookup"><span data-stu-id="95e70-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="95e70-137">ชุดเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="95e70-137">Entity set</span></span>

| <span data-ttu-id="95e70-138">Finance</span><span class="sxs-lookup"><span data-stu-id="95e70-138">Finance</span></span>                           | <span data-ttu-id="95e70-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="95e70-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="95e70-140">เอนทิตีการรวมสำหรับประเภท</span><span class="sxs-lookup"><span data-stu-id="95e70-140">Integration entity for categories</span></span> | <span data-ttu-id="95e70-141">ประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="95e70-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="95e70-142">โฟลว์เอนทิตี</span><span class="sxs-lookup"><span data-stu-id="95e70-142">Entity flow</span></span>

<span data-ttu-id="95e70-143">ประเภทค่าใช้จ่ายโครงการได้รับการจัดการใน Finance และมีการซิงโครไนซ์กับ Project Service Automation เป็นประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="95e70-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="95e70-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="95e70-144">Power Query</span></span>

<span data-ttu-id="95e70-145">เมื่อคุณซิงโครไนซ์กับ Project Service Automation คุณต้องใช้ Microsoft Power Query สำหรับ Excel เพื่อตั้งค่าประเภทการเรียกเก็บเงินในประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="95e70-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="95e70-146">แม่แบบประเภทธุรกรรมค่าใช้จ่ายโครงการ (Fin และ Ops ไปยัง PSA) มีคอลัมน์และการแม็ปเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="95e70-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="95e70-147">หากคุณสร้างแม่แบบของคุณเอง คุณต้องเพิ่มคอลัมน์เงื่อนไขใน Power Query</span><span class="sxs-lookup"><span data-stu-id="95e70-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="95e70-148">ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="95e70-148">Follow these steps.</span></span>

1. <span data-ttu-id="95e70-149">คลิกลูกศรเพื่อเปิดการแม็ปของงานประเภทค่าใช้จ่ายโครงการในแม่แบบประเภทธุรกรรมค่าใช้จ่ายโครงการ (Fin และ Ops ไปยัง PSA)</span><span class="sxs-lookup"><span data-stu-id="95e70-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="95e70-150">คลิกลิงก์ **การสืบค้นและการกรองขั้นสูง** เพื่อเปิด Power Query</span><span class="sxs-lookup"><span data-stu-id="95e70-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="95e70-151">เลือก **เพิ่มคอลัมน์เงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="95e70-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="95e70-152">ป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **BillingType**</span><span class="sxs-lookup"><span data-stu-id="95e70-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="95e70-153">ป้อนเงื่อนไขต่อไปนี้: **ถ้า CATEGORYID ไม่เท่ากับ null ดังนั้นเท่ากับ 19235001 มิฉะนั้นจะเป็น null**</span><span class="sxs-lookup"><span data-stu-id="95e70-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="95e70-154">คลิก **ตกลง** บนคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="95e70-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="95e70-155">อย่าลืมแม็ปคอลัมน์ใหม่นี้ในหน้าการแม็ป</span><span class="sxs-lookup"><span data-stu-id="95e70-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="95e70-156">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานแม่แบบในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="95e70-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="95e70-157">การแม็ปแสดงข้อมูลฟิลด์ที่จะซิงโครไนซ์จาก Finance ไปยัง Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="95e70-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="95e70-158">[![ซ์ประเภทค่าใช้จ่ายโครงการไปยังการแม็ปแม่แบบ Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="95e70-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="95e70-159">การซิงโครไนซ์ประเภทค่าใช้จ่ายโครงการจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="95e70-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="95e70-160">แม่แบบและงาน</span><span class="sxs-lookup"><span data-stu-id="95e70-160">Template and task</span></span>

<span data-ttu-id="95e70-161">แม่แบบและงานพื้นฐานต่อไปนี้ถูกใช้เพื่อซิงโครไนซ์ประเภทค่าใช้จ่ายโครงการจาก Project Service Automation ไปยัง Finance:</span><span class="sxs-lookup"><span data-stu-id="95e70-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="95e70-162">**ชื่อของแม่แบบในการรวมข้อมูล:** ประเภทธุรกรรมค่าใช้จ่ายโครงการ (PSA ไปยัง Fin และ Ops)</span><span class="sxs-lookup"><span data-stu-id="95e70-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="95e70-163">**ชื่อของงานในโครงการ:** ซิงค์ประเภทกับ Fin Ops</span><span class="sxs-lookup"><span data-stu-id="95e70-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="95e70-164">ชุดเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="95e70-164">Entity set</span></span>

| <span data-ttu-id="95e70-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="95e70-165">Project Service Automation</span></span> | <span data-ttu-id="95e70-166">Finance</span><span class="sxs-lookup"><span data-stu-id="95e70-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="95e70-167">ประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="95e70-167">Transaction categories</span></span>     | <span data-ttu-id="95e70-168">เอนทิตีการรวมสำหรับประเภท</span><span class="sxs-lookup"><span data-stu-id="95e70-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="95e70-169">โฟลว์เอนทิตี</span><span class="sxs-lookup"><span data-stu-id="95e70-169">Entity flow</span></span>

<span data-ttu-id="95e70-170">ประเภทค่าใช้จ่ายโครงการได้รับการจัดการใน Finance และมีการซิงโครไนซ์กับ Project Service Automation เป็นประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="95e70-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="95e70-171">การซิงโครไนซ์กลับไปที่ Finance จะอัปเดตประเภทโครงการใน Finance ด้วยรหัสการรวมจาก Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="95e70-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="95e70-172">การแม็ปแม่แบบในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="95e70-172">Template mapping in Data integration</span></span>

<span data-ttu-id="95e70-173">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานแม่แบบในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="95e70-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="95e70-174">การแม็ปแสดงข้อมูลฟิลด์ที่จะซิงโครไนซ์จาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="95e70-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="95e70-175">[![การแม็ปแม่แบบ Project Service Automation กับ Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="95e70-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]