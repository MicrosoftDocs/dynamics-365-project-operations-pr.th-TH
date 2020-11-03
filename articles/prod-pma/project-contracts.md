---
title: สัญญาโครงการ
description: หัวข้อนี้ให้ตัวอย่างสัญญาโครงการที่คุณสามารถสร้างขึ้นสำหรับโครงการประเภทต่างๆ และแหล่งเงินทุนและวิธีจัดการสัญญาและใบแจ้งหนี้ลูกค้าโครงการ
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7d15523f1b22bb8813a47f9f822f12bc4162104
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086063"
---
# <a name="project-contracts"></a><span data-ttu-id="24725-103">สัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24725-104">บทความนี้ให้ตัวอย่างสัญญาโครงการที่คุณสามารถสร้างขึ้นสำหรับโครงการประเภทต่างๆ และแหล่งเงินทุนและวิธีจัดการสัญญาและใบแจ้งหนี้ลูกค้าโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="24725-105">ชนิดของโครงการที่คุณสร้างสำหรับสัญญาโครงการจะกำหนดวิธีการที่ใช้ในการออกใบแจ้งหนี้ให้กับลูกค้าโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="24725-106">คุณเปลี่ยนแปลงสัญญาโครงการและโครงการที่เกี่ยวข้องได้ แต่ไม่สามารถเปลี่ยนประเภทโครงการได้</span><span class="sxs-lookup"><span data-stu-id="24725-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="24725-107">ด้วยการใช้สัญญาโครงการ คุณสามารถออกใบแจ้งหนี้โครงการอย่างน้อยหนึ่งโครงการในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="24725-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="24725-108">สัญญาโครงการยังช่วยรับประกันขั้นตอนการออกใบแจ้งหนี้ที่สอดคล้องกันสำหรับทุกโครงการย่อยในโครงสร้างโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="24725-109">ทุกโครงการที่จะออกใบแจ้งหนี้จะต้องเชื่อมโยงกับสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="24725-110">การตั้งค่าสำหรับสัญญาโครงการใช้กับโครงการและโครงการย่อยทั้งหมดที่เชื่อมโยงกับสัญญาโครงการนั้น</span><span class="sxs-lookup"><span data-stu-id="24725-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="24725-111">สัญญาโครงการสามารถระบุแหล่งเงินทุนได้ตั้งแต่หนึ่งแห่งขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="24725-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="24725-112">ดังนั้นคุณสามารถแบ่งการเรียกเก็บเงินระหว่างผู้ให้ทุนหลายราย ตั้งค่าขีดจำกัด การระดมทุนเพื่อไม่ให้มีการเรียกเก็บเงินจากแหล่งเงินทุนเกินจำนวนที่กำหนด และกำหนดค่ากฎการระดมทุนสำหรับการเรียกเก็บเงินค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="24725-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="24725-113">เงินทุนสำหรับสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-113">Funding for project contracts</span></span>
<span data-ttu-id="24725-114">สัญญาบางโครงการระบุว่าหลายฝ่ายมีส่วนรับผิดชอบในการระดมทุนค่าใช้จ่ายของโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="24725-115">นี่คือตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="24725-115">Here are some examples:</span></span>

-   <span data-ttu-id="24725-116">ลูกค้ารายใหญ่ที่มีหลายแผนกขอให้แบ่งเงินทุนของโครงการตามแผนก</span><span class="sxs-lookup"><span data-stu-id="24725-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="24725-117">บริษัทของคุณแบ่งปันต้นทุนของโครงการขนาดใหญ่กับองค์กรภายนอก</span><span class="sxs-lookup"><span data-stu-id="24725-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="24725-118">โครงการถนนได้รับการสนับสนุนจากเทศบาลสองแห่ง</span><span class="sxs-lookup"><span data-stu-id="24725-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="24725-119">โครงการสะพานได้รับทุนจากรัฐบาลและบริษัทเอกชน</span><span class="sxs-lookup"><span data-stu-id="24725-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="24725-120">ใน Dynamics 365 Finance คุณสามารถแบ่งการเรียกเก็บเงินสำหรับธุรกรรมเดียวหรือทั้งโครงการระหว่างลูกค้า ทุน หรือองค์กรหลายราย</span><span class="sxs-lookup"><span data-stu-id="24725-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="24725-121">ในโครงการที่มีผู้ให้ทุนหลายคน ทุกฝ่ายที่ให้การสนับสนุนเงินทุนของโครงการทุนขั้นสูงเรียกว่าแหล่งเงินทุน</span><span class="sxs-lookup"><span data-stu-id="24725-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="24725-122">หลังจากที่ลูกค้า องค์กร หรือเงินช่วยเหลือถูกกำหนดให้เป็นแหล่งเงินทุนแล้ว สามารถกำหนดให้เป็นกฎการระดมทุนอย่างน้อยหนึ่งข้อ</span><span class="sxs-lookup"><span data-stu-id="24725-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="24725-123">กฎการระดมทุนประกอบด้วยเกณฑ์ที่กำหนดวิธีการจัดสรรค่าใช้จ่ายให้กับแหล่งเงินทุนต่างๆ สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="24725-124">เนื่องจากสินค้าที่เก็บในสต็อก เช่น รายการที่ปรากฏในใบขอซื้อและใบสั่งซื้อไม่สามารถแยกได้ จึงไม่สามารถแบ่งยอดต้นทุนระหว่างแหล่งเงินทุนหลายแหล่งในเวลาที่จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="24725-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="24725-125">ดังนั้นมูลค่าแหล่งเงินทุนจะยังคงเป็น 0 (ศูนย์) จนกว่าจะมีการลงรายการบัญชีปัญหาสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="24725-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="24725-126">เมื่อมีการลงรายการบัญชีปัญหาสินค้าคงคลัง จำนวนต้นทุนจะถูกกระจายตามกฎการแจกจ่ายบัญชีสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="24725-127">ต่อไปนี้คือขั้นตอนบางส่วนที่คุณสามารถทำได้เพื่อให้ง่ายต่อการแยกการเรียกเก็บเงินระหว่างแหล่งเงินทุนต่างๆ</span><span class="sxs-lookup"><span data-stu-id="24725-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="24725-128">ระบุว่าธุรกรรมทั้งหมดที่ป้อนสำหรับโครงการใช้สกุลเงินการขายเดียวกับสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="24725-129">ตั้งค่าขีดจำกัดการระดมทุนเพื่อไม่ให้มีการออกใบแจ้งหนี้เกินจำนวนที่ระบุสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="24725-130">กำหนดค่ากฎการระดมทุนและขีดจำกัดการระดมทุนสำหรับผู้ปฏิบัติงาน สินค้า หมวดหมู่ กลุ่มหมวดหมู่ และประเภทธุรกรรม (หรือสำหรับประเภทธุรกรรมทั้งหมด)</span><span class="sxs-lookup"><span data-stu-id="24725-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="24725-131">เลือกวันเริ่มต้นและวันสิ้นสุดที่ไม่บังคับเพื่อกำหนดช่วงเวลาที่กฎการระดมทุนแต่ละข้อถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="24725-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="24725-132">ระบุเปอร์เซ็นต์ที่แหล่งเงินทุนแต่ละแห่งรับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="24725-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="24725-133">ระบุแหล่งเงินทุนที่รับผิดชอบในการปัดเศษความแตกต่างที่เกิดจากการคำนวณการจัดสรรเงินทุน</span><span class="sxs-lookup"><span data-stu-id="24725-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="24725-134">ตั้งกฎที่กำหนดวิธีการออกใบแจ้งหนี้ต้นทุนโครงการให้กับลูกค้าภายนอกและเรียกเก็บจากองค์กรภายใน</span><span class="sxs-lookup"><span data-stu-id="24725-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="24725-135">บันทึกธุรกรรมในบัญชีเงินทุนที่ถูกระงับจนกว่าจะได้รับเงินเพิ่มเติมหรือจนกว่าคุณจะตัดสินใจแบกรับค่าใช้จ่ายภายใน</span><span class="sxs-lookup"><span data-stu-id="24725-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="24725-136">หากต้องการกำหนดกลุ่มภาษีที่จะเชื่อมโยงกับธุรกรรม โครงการจะค้นหาการกำหนดกลุ่มภาษี</span><span class="sxs-lookup"><span data-stu-id="24725-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="24725-137">หากไม่มีการกำหนดกลุ่มภาษีในระดับโครงการ ระบบจะค้นหาสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="24725-138">ตัวอย่าง: แหล่งเงินทุนหลายแหล่ง (แบบง่าย)</span><span class="sxs-lookup"><span data-stu-id="24725-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="24725-139">ตารางต่อไปนี้แสดงสถานการณ์จำลองสำหรับการจัดการการจัดสรรเงินทุนระหว่างแหล่งเงินทุนต่างๆ</span><span class="sxs-lookup"><span data-stu-id="24725-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="24725-140">สถานการณ์เหล่านี้ตั้งอยู่บนสมมติฐานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="24725-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="24725-141">การตั้งค่าลำดับความสำคัญจะรวมอยู่ในการจัดสรรเงินก่อนที่จะใช้เกณฑ์กฎการระดมทุนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="24725-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="24725-142">ไม่มีการระบุช่วงวันที่เพื่อกำหนดช่วงเวลา d เมื่อกฎการระดมทุนถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="24725-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24725-143"><strong>สถานการณ์สมมติ</strong></span><span class="sxs-lookup"><span data-stu-id="24725-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="24725-144"><strong>แหล่งเงินทุน</strong></span><span class="sxs-lookup"><span data-stu-id="24725-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="24725-145"><strong>เปอร์เซ็นต์การจัดสรร</strong></span><span class="sxs-lookup"><span data-stu-id="24725-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="24725-146"><strong>ลำดับความสำคัญของการจัดสรร</strong></span><span class="sxs-lookup"><span data-stu-id="24725-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24725-147">คุณต้องการจัดสรรต้นทุนให้กับแหล่งเงินทุนหนึ่งจนกว่าเงินทุนจะหมด จัดสรรต้นทุนไปยังแหล่งเงินทุนแห่งที่สองจนกว่าเงินทุนจะหมด และสุดท้ายจัดสรรต้นทุนที่เหลือไปยังแหล่งเงินทุนที่สาม</span><span class="sxs-lookup"><span data-stu-id="24725-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="24725-148">แหล่งเงินทุนที่ 1</span><span class="sxs-lookup"><span data-stu-id="24725-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="24725-149">แหล่งเงินทุนที่ 2</span><span class="sxs-lookup"><span data-stu-id="24725-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="24725-150">แหล่งเงินทุนที่ 3</span><span class="sxs-lookup"><span data-stu-id="24725-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="24725-151">100%</span><span class="sxs-lookup"><span data-stu-id="24725-151">100%</span></span></li>
<li><span data-ttu-id="24725-152">100%</span><span class="sxs-lookup"><span data-stu-id="24725-152">100%</span></span></li>
<li><span data-ttu-id="24725-153">100%</span><span class="sxs-lookup"><span data-stu-id="24725-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="24725-154">1</span><span class="sxs-lookup"><span data-stu-id="24725-154">1</span></span></li>
<li><span data-ttu-id="24725-155">2</span><span class="sxs-lookup"><span data-stu-id="24725-155">2</span></span></li>
<li><span data-ttu-id="24725-156">3</span><span class="sxs-lookup"><span data-stu-id="24725-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24725-157">คุณต้องการจัดสรรต้นทุน 75 เปอร์เซ็นต์ให้กับแหล่งเงินทุนหนึ่งและ 25 เปอร์เซ็นต์ไปยังแหล่งเงินทุนที่สอง</span><span class="sxs-lookup"><span data-stu-id="24725-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="24725-158">เมื่อแหล่งเงินทุนใดแหล่งหนึ่งหมด คุณต้องการจ่ายค่าใช้จ่ายที่เหลือจากแหล่งเงินทุนที่สาม</span><span class="sxs-lookup"><span data-stu-id="24725-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="24725-159">แหล่งเงินทุนที่ 1</span><span class="sxs-lookup"><span data-stu-id="24725-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="24725-160">แหล่งเงินทุนที่ 2</span><span class="sxs-lookup"><span data-stu-id="24725-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="24725-161">แหล่งเงินทุนที่ 3</span><span class="sxs-lookup"><span data-stu-id="24725-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="24725-162">75%</span><span class="sxs-lookup"><span data-stu-id="24725-162">75%</span></span></li>
<li><span data-ttu-id="24725-163">25%</span><span class="sxs-lookup"><span data-stu-id="24725-163">25%</span></span></li>
<li><span data-ttu-id="24725-164">100%</span><span class="sxs-lookup"><span data-stu-id="24725-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="24725-165">1</span><span class="sxs-lookup"><span data-stu-id="24725-165">1</span></span></li>
<li><span data-ttu-id="24725-166">1</span><span class="sxs-lookup"><span data-stu-id="24725-166">1</span></span></li>
<li><span data-ttu-id="24725-167">2</span><span class="sxs-lookup"><span data-stu-id="24725-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24725-168">คุณต้องการจัดสรรต้นทุน 75 เปอร์เซ็นต์ให้กับแหล่งเงินทุนหนึ่งและ 25 เปอร์เซ็นต์ไปยังแหล่งเงินทุนที่สอง</span><span class="sxs-lookup"><span data-stu-id="24725-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="24725-169">เมื่อแหล่งเงินทุนใดแหล่งหนึ่งหมด คุณต้องการcpdค่าใช้จ่ายที่เหลือระหว่างแหล่งเงินทุนที่สามกับแหล่งเงินทุนที่สี่</span><span class="sxs-lookup"><span data-stu-id="24725-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="24725-170">แหล่งเงินทุนที่ 1</span><span class="sxs-lookup"><span data-stu-id="24725-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="24725-171">แหล่งเงินทุนที่ 2</span><span class="sxs-lookup"><span data-stu-id="24725-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="24725-172">แหล่งเงินทุนที่ 3</span><span class="sxs-lookup"><span data-stu-id="24725-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="24725-173">แหล่งเงินทุนที่ 4</span><span class="sxs-lookup"><span data-stu-id="24725-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="24725-174">75%</span><span class="sxs-lookup"><span data-stu-id="24725-174">75%</span></span></li>
<li><span data-ttu-id="24725-175">25%</span><span class="sxs-lookup"><span data-stu-id="24725-175">25%</span></span></li>
<li><span data-ttu-id="24725-176">50%</span><span class="sxs-lookup"><span data-stu-id="24725-176">50%</span></span></li>
<li><span data-ttu-id="24725-177">50%</span><span class="sxs-lookup"><span data-stu-id="24725-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="24725-178">1</span><span class="sxs-lookup"><span data-stu-id="24725-178">1</span></span></li>
<li><span data-ttu-id="24725-179">1</span><span class="sxs-lookup"><span data-stu-id="24725-179">1</span></span></li>
<li><span data-ttu-id="24725-180">2</span><span class="sxs-lookup"><span data-stu-id="24725-180">2</span></span></li>
<li><span data-ttu-id="24725-181">2</span><span class="sxs-lookup"><span data-stu-id="24725-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24725-182">คุณต้องการจัดสรรต้นทุน 25 เปอร์เซ็นต์แรกให้กับแหล่งเงินทุนหนึ่งและที่เหลือไปยังแหล่งเงินทุนที่สอง</span><span class="sxs-lookup"><span data-stu-id="24725-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="24725-183">แหล่งเงินทุนที่ 1</span><span class="sxs-lookup"><span data-stu-id="24725-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="24725-184">แหล่งเงินทุนที่ 2</span><span class="sxs-lookup"><span data-stu-id="24725-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="24725-185">25%</span><span class="sxs-lookup"><span data-stu-id="24725-185">25%</span></span></li>
<li><span data-ttu-id="24725-186">100%</span><span class="sxs-lookup"><span data-stu-id="24725-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="24725-187">1</span><span class="sxs-lookup"><span data-stu-id="24725-187">1</span></span></li>
<li><span data-ttu-id="24725-188">2</span><span class="sxs-lookup"><span data-stu-id="24725-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="24725-189">ตัวอย่าง: แหล่งเงินทุนหลายแหล่ง (แบบซับซ้อน)</span><span class="sxs-lookup"><span data-stu-id="24725-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="24725-190">คุณมีแหล่งเงินทุนสามแหล่งที่คุณต้องการใช้ตามลำดับต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="24725-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="24725-191">ใช้แหล่งเงินทุนที่ 2 และแหล่งเงินทุนที่ 3 เท่าๆ กันจนกว่าแหล่งเงินทุนที่ 2 จะหมด</span><span class="sxs-lookup"><span data-stu-id="24725-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="24725-192">ใช้แหล่งเงินทุนที่ 3 ต่อไปจนกว่าจะหมด</span><span class="sxs-lookup"><span data-stu-id="24725-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="24725-193">ใช้แหล่งเงินทุนที่ 1 หลังจากแหล่งเงินทุนที่ 3 หมด</span><span class="sxs-lookup"><span data-stu-id="24725-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="24725-194">หากต้องการให้เป้าหมายนี้สำเร็จ คุณต้องทำสิ่งต่อไปนี้ก่อน:</span><span class="sxs-lookup"><span data-stu-id="24725-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="24725-195">กำหนดวงเงินสำหรับแหล่งเงินทุนที่ 2 และแหล่งเงินทุนที่ 3 สำหรับจำนวนเงินที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="24725-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="24725-196">สร้างกฎเงินทุนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="24725-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="24725-197">กฎข้อที่ 1 (ลำดับความสำคัญที่ 1): จัดสรรธุรกรรม 50 เปอร์เซ็นต์ไปยังแหล่งเงินทุนที่ 2 และ 50 เปอร์เซ็นต์ให้กับแหล่งเงินที่ 3</span><span class="sxs-lookup"><span data-stu-id="24725-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="24725-198">กฎข้อที่ 2 (ลำดับความสำคัญที่ 2): จัดสรรธุรกรรม 100 เปอร์เซ็นต์ให้กับแหล่งเงินทุนที่ 3</span><span class="sxs-lookup"><span data-stu-id="24725-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="24725-199">กฎข้อที่ 3 (ลำดับความสำคัญที่ 3): จัดสรรธุรกรรม 100 เปอร์เซ็นต์ให้กับแหล่งเงินทุนที่ 1</span><span class="sxs-lookup"><span data-stu-id="24725-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="24725-200">การตั้งค่านี้ใช้งานได้เนื่องจากการทำธุรกรรมถูกตรวจสอบตามกฎและขีดจำกัด เพื่อพิจารณาว่ารายการใดใช้กับธุรกรรมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="24725-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="24725-201">หากไม่มีการใช้กฎหรือข้อจำกัดเฉพาะกับธุรกรรม กฎธุรกรรมทั้งหมดจะมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="24725-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="24725-202">กฎธุรกรรมทั้งหมดตรงกับธุรกรรมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="24725-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="24725-203">หากพบกฎที่ตรงกับธุรกรรม เปอร์เซ็นต์ที่ได้รับการจัดสรรในกฎนั้นจะถูกนำไปใช้ก่อน แต่หลังจากการจับคู่จะถูกตรวจสอบกับขีดจำกัดใดๆ ที่ได้ตั้งค่าไว้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="24725-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="24725-204">หากถึงขีดจำกัดและเงินของแหล่งเงินทุนหมด กฎการระดมทุนที่เกี่ยวข้องกับวงเงินการระดมทุนจะไม่ถูกนำมาพิจารณาและโปรแกรมจะตรวจสอบกฎถัดไปที่บังคับใช้</span><span class="sxs-lookup"><span data-stu-id="24725-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="24725-205">ในบางกรณีสามารถจัดสรรธุรกรรมได้เพียงบางส่วนภายใต้กฎ</span><span class="sxs-lookup"><span data-stu-id="24725-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="24725-206">สิ่งนี้อาจเกิดขึ้นเนื่องจากถึงขีดจำกัด เมื่อมีการจัดสรรธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="24725-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="24725-207">ในกรณีนี้จะจัดสรรเพียงจำนวนหนึ่งตามกฎนั้น เช่น 50 เปอร์เซ็นต์ให้กับแหล่งเงินทุนแต่ละแห่ง</span><span class="sxs-lookup"><span data-stu-id="24725-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="24725-208">นี่เป็นกรณีในกฎข้อที่ 1 ซึ่งอธิบายไว้ก่อนหน้านี้ในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="24725-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="24725-209">ส่วนที่เหลือจะถูกจัดสรรตามกฎถัดไปในลำดับ</span><span class="sxs-lookup"><span data-stu-id="24725-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="24725-210">ตารางต่อไปนี้ตรวจสอบสถานการณ์นี้ในรายละเอียดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="24725-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24725-211"><strong>โฟกัส</strong></span><span class="sxs-lookup"><span data-stu-id="24725-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="24725-212"><strong>รายละเอียด</strong></span><span class="sxs-lookup"><span data-stu-id="24725-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24725-213">กฎการระดมทุน</span><span class="sxs-lookup"><span data-stu-id="24725-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="24725-214">กฎที่ 1 (ลำดับความสำคัญที่ 1): ธุรกรรมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="24725-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="24725-215">จัดสรรแหล่งเงินทุนที่ 2 ที่ 50% และแหล่งเงินทุนที่ 3 ที่ 50%</span><span class="sxs-lookup"><span data-stu-id="24725-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="24725-216">กฎที่ 2 (ลำดับความสำคัญที่ 2): ธุรกรรมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="24725-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="24725-217">จัดสรรแหล่งเงินทุนที่ 3 ที่ 100%</span><span class="sxs-lookup"><span data-stu-id="24725-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="24725-218">กฎที่ 3 (ลำดับความสำคัญที่ 2): ธุรกรรมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="24725-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="24725-219">จัดสรรแหล่งเงินทุนที่ 1 ที่ 100%</span><span class="sxs-lookup"><span data-stu-id="24725-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24725-220">ขีดจำกัดเงินทุน</span><span class="sxs-lookup"><span data-stu-id="24725-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="24725-221">ขีดจำกัดแหล่งเงินทุนที่ 1 = 10,000.00</span><span class="sxs-lookup"><span data-stu-id="24725-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="24725-222">ขีดจำกัดแหล่งเงินทุนที่ 2 = 500.00</span><span class="sxs-lookup"><span data-stu-id="24725-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="24725-223">ขีดจำกัดแหล่งเงินทุนที่ 3 = 750.00</span><span class="sxs-lookup"><span data-stu-id="24725-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24725-224">ธุรกรรม 1</span><span class="sxs-lookup"><span data-stu-id="24725-224">Transaction 1</span></span></td>
<td><span data-ttu-id="24725-225"><strong>จำนวนธุรกรรม:</strong> 100.00<strong>เงินทุน:</strong> ธุรกรรมจะได้รับการชำระเงินตามกฎที่ 1 เท่านั้น เนื่องจากธุรกรรมได้รับการชำระเงินเต็มจำนวนหลังจากใช้กฎที่ 1</span><span class="sxs-lookup"><span data-stu-id="24725-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="24725-226">ธุรกรรมนี้ได้รับการสนับสนุนอย่างเท่าเทียมกันระหว่างแหล่งเงินทุนที่ 2 และแหล่งเงินทุนที่ 3</span><span class="sxs-lookup"><span data-stu-id="24725-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="24725-227">แหล่งเงินทุนที่ 2: 50.00</span><span class="sxs-lookup"><span data-stu-id="24725-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="24725-228">แหล่งเงินทุนที่ 3: 50.00</span><span class="sxs-lookup"><span data-stu-id="24725-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24725-229">ธุรกรรม 2</span><span class="sxs-lookup"><span data-stu-id="24725-229">Transaction 2</span></span></td>
<td><span data-ttu-id="24725-230"><strong>จำนวนธุรกรรม:</strong> 5,000.00<strong>เงินทุน:</strong> การทำธุรกรรมได้รับการชำระเงินตามกฎทั้งสามข้อ</span><span class="sxs-lookup"><span data-stu-id="24725-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="24725-231"><strong>กฎที่ 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="24725-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="24725-232">แหล่งเงินทุนที่ 2: 450.00</span><span class="sxs-lookup"><span data-stu-id="24725-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="24725-233">แหล่งเงินทุนที่ 3: 450.00</span><span class="sxs-lookup"><span data-stu-id="24725-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="24725-234">
<strong>กฎที่ 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="24725-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="24725-235">แหล่งเงินทุนที่ 3: 250.00 (= 750.00 – 50.00 – 450.00)</span><span class="sxs-lookup"><span data-stu-id="24725-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="24725-236">
<strong>กฎที่ 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="24725-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="24725-237">แหล่งเงินทุนที่ 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span><span class="sxs-lookup"><span data-stu-id="24725-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24725-238">เงินทุนทั้งหมดที่กระจายไปสำหรับแหล่งเงินทุนแต่ละแห่ง</span><span class="sxs-lookup"><span data-stu-id="24725-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="24725-239">แหล่งเงินทุนที่ 1: 3,850.00</span><span class="sxs-lookup"><span data-stu-id="24725-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="24725-240">แหล่งเงินทุนที่ 2: 500.00</span><span class="sxs-lookup"><span data-stu-id="24725-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="24725-241">แหล่งเงินทุนที่ 3: 750.00</span><span class="sxs-lookup"><span data-stu-id="24725-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="24725-242">กฎการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="24725-242">Billing rules</span></span>
<span data-ttu-id="24725-243">เมื่อคุณเจรจาสัญญาโครงการกับลูกค้า คุณจะกำหนดวิธีและเวลาที่คุณสามารถออกใบแจ้งหนี้ให้กับลูกค้าเพื่อทำงานในโครงการได้</span><span class="sxs-lookup"><span data-stu-id="24725-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="24725-244">หลังจากตั้งค่าสัญญาโครงการและโครงการแล้ว คุณสามารถตั้งค่ากฎการเรียกเก็บเงินสำหรับโครงการได้</span><span class="sxs-lookup"><span data-stu-id="24725-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="24725-245">กฎการเรียกเก็บเงินเป็นไปตามเงื่อนไขโครงการที่ระบุไว้ในสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="24725-246">กฎการเรียกเก็บเงินที่คุณสามารถสร้างขึ้นอยู่กับเงื่อนไขของสัญญาโครงการและประเภทโครงการ เช่น เวลาและวัสดุหรือราคาคงที่ที่คุณเชื่อมโยงกับกฎการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="24725-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="24725-247">คุณสามารถสร้างกฎการเรียกเก็บเงินสำหรับสัญญาโครงการได้มากกว่าหนึ่งกฎ</span><span class="sxs-lookup"><span data-stu-id="24725-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="24725-248">คุณยังสามารถกำหนดกฎการเรียกเก็บเงินให้กับหลายโครงการที่เชื่อมโยงกับสัญญาโครงการเดียวกันและมีเงื่อนไขการเรียกเก็บเงินที่คล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="24725-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="24725-249">คุณสามารถตั้งกฎการเรียกเก็บเงินประเภทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="24725-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="24725-250">**หน่วยการจัดส่ง** - ออกใบแจ้งหนี้ให้ลูกค้าเมื่อคุณจัดส่งเสร็จ</span><span class="sxs-lookup"><span data-stu-id="24725-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="24725-251">คุณกำหนดหน่วยการจัดส่งในสัญญา</span><span class="sxs-lookup"><span data-stu-id="24725-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="24725-252">**ความคืบหน้า** - ออกใบแจ้งหนี้ลูกค้าเมื่อคุณทำตามเปอร์เซ็นต์ที่ระบุของโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="24725-253">คุณสามารถตั้งค่ากฎการเรียกเก็บเงินเพื่อคำนวณเปอร์เซ็นต์ของงานที่เสร็จสมบูรณ์โดยอัตโนมัติ หรือคุณสามารถคำนวณเปอร์เซ็นต์ของงานที่เสร็จสมบูรณ์และจำนวนเงินที่จะออกใบแจ้งหนี้ให้กับลูกค้าด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="24725-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="24725-254">**เป้าหมาย** - ออกใบแจ้งหนี้ให้กับลูกค้าตามจำนวนเต็มของเป้าหมายของโครงการเมื่อถึงเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="24725-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="24725-255">**ค่าธรรมเนียม** - ออกใบแจ้งหนี้ให้ลูกค้าสำหรับบริการของคุณพร้อมค่าธรรมเนียมการจัดการ ซึ่งโดยทั่วไปจะเป็นเปอร์เซ็นต์ของต้นทุนบริการ</span><span class="sxs-lookup"><span data-stu-id="24725-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="24725-256">**เวลาและวัสดุ** - ออกใบแจ้งหนี้ลูกค้าตามมูลค่าของเวลาและวัสดุที่ใช้ในโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="24725-257">สำหรับกฎการเรียกเก็บเงินทุกประเภท คุณสามารถระบุเปอร์เซ็นต์การเก็บรักษาที่หักออกจากใบแจ้งหนี้ของลูกค้าจนกว่าโครงการจะถึงขั้นตอนที่ตกลงกัน</span><span class="sxs-lookup"><span data-stu-id="24725-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="24725-258">เปอร์เซ็นต์การเก็บรักษาการชำระเงินระบุไว้ในสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="24725-259">จำนวนเงินจะคำนวณตามและลบออกจากมูลค่ารวมของรายการในใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="24725-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="24725-260">สำหรับกฎการเรียกเก็บเงิน **เวลาและวัสดุ** และ **ความคืบหน้า** คุณสามารถกำหนดหมวดหมู่ที่เรียกเก็บเงินได้</span><span class="sxs-lookup"><span data-stu-id="24725-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="24725-261">ประเภทที่เรียกเก็บเงินได้ระบุธุรกรรมที่ควรรวมอยู่ในใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="24725-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="24725-262">เมื่อคุณพร้อมที่จะออกใบแจ้งหนี้ให้กับลูกค้า จำนวนเงินในใบแจ้งหนี้สำหรับโครงการจะคำนวณตามกฎการเรียกเก็บเงิน และจะมีการสร้างข้อเสนอใบแจ้งหนี้โครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="24725-263">ส่วนต่อไปนี้เป็นตัวอย่างที่แสดงวิธีตั้งค่าและจัดการกฎการเรียกเก็บเงินสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="24725-264">ตัวอย่าง: สร้างกฎการเรียกเก็บเงินตามจำนวนหน่วยที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="24725-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="24725-265">องค์กรของคุณทำข้อตกลงในการจัดให้มีการฝึกอบรมทั้งหมดห้าครั้งแก่พนักงานของลูกค้าโดยมีค่าใช้จ่าย 10,000 ต่อการฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="24725-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="24725-266">คุณออกใบแจ้งหนี้ลูกค้าหลังการฝึกอบรมแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="24725-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="24725-267">เมื่อคุณตั้งค่ากฎการเรียกเก็บเงินสำหรับสัญญา คุณจะใช้ค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="24725-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="24725-268">หน่วยส่งคือหนึ่งการฝึก</span><span class="sxs-lookup"><span data-stu-id="24725-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="24725-269">ราคาต่อหน่วยคือ 10,000 ต่อการฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="24725-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="24725-270">จำนวนหน่วยทั้งหมดคือการฝึกอบรมห้าครั้ง</span><span class="sxs-lookup"><span data-stu-id="24725-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="24725-271">เมื่อคุณเสร็จสิ้นการฝึกอบรมหนึ่งครั้ง คุณสามารถสร้างใบแจ้งหนี้ 10,000 รายการสำหรับหน่วยแรกที่ส่งมอบและส่งใบแจ้งหนี้ให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="24725-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="24725-272">ตัวอย่าง: สร้างกฎการเรียกเก็บเงินตามเปอร์เซ็นต์ที่ระบุของการเสร็จสิ้นโครงการ (การคำนวณด้วยตนเอง)</span><span class="sxs-lookup"><span data-stu-id="24725-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="24725-273">องค์กรของคุณซึ่งเป็นบริษัทที่ปรึกษาด้านซอฟต์แวร์ ทำข้อตกลงกับลูกค้าในการพัฒนาส่วนหนึ่งของผลิตภัณฑ์ที่ลูกค้ากำลังพัฒนา</span><span class="sxs-lookup"><span data-stu-id="24725-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="24725-274">องค์กรของคุณตกลงที่จะส่งมอบรหัสซอฟต์แวร์ในช่วงหกเดือน</span><span class="sxs-lookup"><span data-stu-id="24725-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="24725-275">ลูกค้าตกลงที่จะจ่ายเงินให้องค์กรของคุณทั้งหมด 100,000 สำหรับการทำงาน</span><span class="sxs-lookup"><span data-stu-id="24725-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="24725-276">คุณสร้างกฎการเรียกเก็บเงินเพื่อออกใบแจ้งหนี้ให้กับลูกค้าตามเปอร์เซ็นต์ของงานที่เสร็จสมบูรณ์ในโครงการตามที่ระบุไว้ในสัญญา</span><span class="sxs-lookup"><span data-stu-id="24725-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="24725-277">เมื่อสิ้นเดือนแรกคุณจะพบกับลูกค้าเพื่อกำหนดเปอร์เซ็นต์ของงานที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="24725-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="24725-278">หลังจากที่คุณและลูกค้าตรวจสอบโครงการแล้วคุณตัดสินใจว่าโครงการเสร็จสมบูรณ์ไป 15 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="24725-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="24725-279">คุณสร้างใบแจ้งหนี้สำหรับ 15,000 (15 เปอร์เซ็นต์ของ 100,000) และส่งให้ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="24725-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="24725-280">ตัวอย่าง: สร้างกฎการเรียกเก็บเงินตามเปอร์เซ็นต์ที่ระบุของการเสร็จสิ้นโครงการ (การคำนวณอัตโนมัติ)</span><span class="sxs-lookup"><span data-stu-id="24725-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="24725-281">องค์กรของคุณซึ่งเป็นบริษัทพัฒนาซอฟต์แวร์ตกลงที่จะพัฒนาแพ็คเกจบัญชีเงินเดือนสำหรับลูกค้าเป็นจำนวน 30,000</span><span class="sxs-lookup"><span data-stu-id="24725-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="24725-282">ลูกค้าตกลงที่จะจ่ายเงินให้องค์กรของคุณทั้งหมดตามเปอร์เซ็นต์งานที่สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="24725-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="24725-283">คุณประเมินว่าต้นทุนโครงการคือ 20,000</span><span class="sxs-lookup"><span data-stu-id="24725-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="24725-284">สัญญาโครงการระบุประเภทของงานที่คุณใช้ในกระบวนการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="24725-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="24725-285">คุณตั้งค่ากฎการเรียกเก็บเงินที่คำนวณยอดเงินในใบแจ้งหนี้โดยอัตโนมัติสำหรับเปอร์เซ็นต์ของงานที่เสร็จสมบูรณ์สำหรับแต่ละประเภท</span><span class="sxs-lookup"><span data-stu-id="24725-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="24725-286">คุณตั้งงบประมาณสำหรับแต่ละหมวดหมู่:</span><span class="sxs-lookup"><span data-stu-id="24725-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="24725-287">**การพัฒนา** - ต้นทุน 15,000 และรายได้ 20,000</span><span class="sxs-lookup"><span data-stu-id="24725-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="24725-288">**การติดตั้ง** - ต้นทุน 5,000 และรายได้ 10,000</span><span class="sxs-lookup"><span data-stu-id="24725-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="24725-289">เมื่อคุณสร้างใบแจ้งหนี้ของลูกค้าเป็นครั้งแรก ยอดเงินในใบแจ้งหนี้จะคำนวณโดยอัตโนมัติตามข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="24725-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="24725-290">หลังจากผ่านไปหนึ่งเดือน ผู้ปฏิบัติงานในโครงการจะส่งแผ่นเวลาสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="24725-291">ค่าชั่วโมงของคนงานคือ 5,000 สำหรับการพัฒนาและ 1,000 สำหรับการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="24725-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="24725-292">งานพัฒนาแล้วเสร็จ 33 เปอร์เซ็นต์ (ต้นทุนจริง 5,000/ต้นทุนงบประมาณ 15,000) และงานติดตั้งเสร็จ 20 เปอร์เซ็นต์ (ต้นทุนจริง 1,000/ต้นทุนงบประมาณ 5,000)</span><span class="sxs-lookup"><span data-stu-id="24725-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="24725-293">จำนวนใบแจ้งหนี้ 8,667 จะคำนวณโดยอัตโนมัติ (33 เปอร์เซ็นต์ของ 20,000 + 20 เปอร์เซ็นต์ของ 10,000)</span><span class="sxs-lookup"><span data-stu-id="24725-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="24725-294">คุณสร้างใบแจ้งหนี้สำหรับ 8,667 และส่งให้ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="24725-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="24725-295">ตัวอย่าง: สร้างกฎการเรียกเก็บเงินที่เป็นไปตามเป้าหมายที่ตกลงกัน</span><span class="sxs-lookup"><span data-stu-id="24725-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="24725-296">องค์กรของคุณซึ่งเป็นบริษัทที่ปรึกษาด้านการจัดการตกลงที่จะทำการวิจัยตลาดสำหรับผลิตภัณฑ์สำหรับผู้บริโภคที่ลูกค้าวางแผนจะขาย</span><span class="sxs-lookup"><span data-stu-id="24725-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="24725-297">ลูกค้าตกลงที่จะใช้บริการของคุณเป็นระยะเวลาสามเดือนเริ่มตั้งแต่เดือนมีนาคม และตกลงที่จะจ่ายเงินให้องค์กรของคุณ 50,000</span><span class="sxs-lookup"><span data-stu-id="24725-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="24725-298">โครงการนี้มีสามเป้าหมาย:</span><span class="sxs-lookup"><span data-stu-id="24725-298">The project has three milestones:</span></span>

-   <span data-ttu-id="24725-299">เป้าหมายที่ 1: รวบรวมข้อมูลผู้บริโภค - 31 มีนาคม</span><span class="sxs-lookup"><span data-stu-id="24725-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="24725-300">เป้าหมายที่ 2: วิเคราะห์ข้อมูลผู้บริโภค - 30 เมษายน</span><span class="sxs-lookup"><span data-stu-id="24725-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="24725-301">เป้าหมายที่ 3: นำเสนอข้อเสนอความแพร่หลายของผลิตภัณฑ์ - 31 พฤษภาคม</span><span class="sxs-lookup"><span data-stu-id="24725-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="24725-302">ลูกค้ายินยอมที่จะจ่ายเงินให้องค์กรของคุณ 10,000 สำหรับเป้าหมายแรก 20,000 สำหรับเป้าหมายที่สองและ 20,000 สำหรับเป้าหมายที่สาม</span><span class="sxs-lookup"><span data-stu-id="24725-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="24725-303">เมื่อคุณตั้งค่าสัญญาโครงการ คุณตกลงที่จะเรียกเก็บเงินจากลูกค้าตามเป้าหมายที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="24725-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="24725-304">การตั้งค่ากฎการเรียกเก็บเงินประกอบด้วยขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="24725-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="24725-305">กำหนดเป้าหมายของโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-305">Define the project milestones.</span></span>
-   <span data-ttu-id="24725-306">กำหนดจำนวนเงินที่จะออกใบแจ้งหนี้ให้กับลูกค้าเมื่อแต่ละเป้าหมายสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="24725-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="24725-307">เมื่อเป้าหมายแรกเสร็จสิ้นในวันที่ 31 มีนาคม คุณจะทำเครื่องหมายเป้าหมายว่าเสร็จสมบูรณ์จากนั้นสร้างใบแจ้งหนี้จำนวน 10,000 ใบและส่งให้ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="24725-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="24725-308">คุณไม่สามารถสร้างใบแจ้งหนี้สำหรับเป้าหมายสำคัญได้จนกว่าคุณจะทำเครื่องหมายเป้าหมายว่าเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="24725-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="24725-309">ตัวอย่าง: สร้างกฎการเรียกเก็บเงินตามบริการบวกค่าธรรมเนียมการจัดการ</span><span class="sxs-lookup"><span data-stu-id="24725-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="24725-310">องค์กรของคุณซึ่งเป็นบริษัทที่ปรึกษาด้านการจัดการตกลงที่จะทำการวิจัยตลาดเพื่อประเมินความเป็นไปได้ของผลิตภัณฑ์ที่ลูกค้าซึ่งเป็นบริษัทค้าปลีกกำลังพัฒนา</span><span class="sxs-lookup"><span data-stu-id="24725-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="24725-311">เงื่อนไขของข้อตกลงระบุว่าคุณจะให้บริการของที่ปรึกษาด้านการจัดการระดับสูงสามคนของคุณซึ่งจะทำการวิจัยตามเวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="24725-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="24725-312">ลูกค้าตกลงที่จะจ่าย 100 ต่อชั่วโมง บวกค่าธรรมเนียมการจัดการ 10 เปอร์เซ็นต์สำหรับชั่วโมงการให้คำปรึกษาที่เรียกเก็บจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="24725-313">เมื่อคุณตั้งค่าสัญญาโครงการ ให้สร้างกฎการเรียกเก็บเงินเพื่อเพิ่มค่าธรรมเนียมการจัดการ 10 เปอร์เซ็นต์ให้กับชั่วโมงการให้คำปรึกษาที่เรียกเก็บจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="24725-314">เมื่อคุณสร้างใบแจ้งหนี้สำหรับลูกค้า ลูกค้าจะถูกเรียกเก็บค่าธรรมเนียมการจัดการ 10 เปอร์เซ็นต์บวกค่าชั่วโมงการให้คำปรึกษา</span><span class="sxs-lookup"><span data-stu-id="24725-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="24725-315">ตัวอย่างเช่น หากที่ปรึกษาทั้งสามทำงานรวม 200 ชั่วโมงในโครงการใบแจ้งหนี้สำหรับ 22,000 จะถูกสร้างขึ้นตามการคำนวณต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="24725-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="24725-316">200 ชั่วโมงที่ 100 ต่อชั่วโมง = 20,000</span><span class="sxs-lookup"><span data-stu-id="24725-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="24725-317">ค่าธรรมเนียมการจัดการ 10 เปอร์เซ็นต์ = 2,000</span><span class="sxs-lookup"><span data-stu-id="24725-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="24725-318">จำนวนใบแจ้งหนี้ทั้งหมด = 22,000</span><span class="sxs-lookup"><span data-stu-id="24725-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="24725-319">หากลูกค้าต้องเสียภาษีค่าธรรมเนียมและคุณเลือกกลุ่มภาษีขายในสัญญาโครงการ กลุ่มภาษีขายจะถูกป้อนโดยอัตโนมัติในกฎการเรียกเก็บเงินสำหรับค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="24725-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="24725-320">ตัวอย่าง: สร้างกฎการเรียกเก็บเงินสำหรับมูลค่าของเวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="24725-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="24725-321">องค์กรของคุณซึ่งเป็นบริษัทที่ปรึกษาด้านซอฟต์แวร์ตกลงที่จะจัดหาที่ปรึกษาด้านเทคนิคห้าคนเพื่อทำงานในโครงการพัฒนาซอฟต์แวร์สำหรับลูกค้าในหกเดือนข้างหน้า</span><span class="sxs-lookup"><span data-stu-id="24725-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="24725-322">ลูกค้าตกลงที่จะจ่าย 150 สำหรับแต่ละชั่วโมงการให้คำปรึกษาบวกกับค่าเครื่องใช้สำนักงาน</span><span class="sxs-lookup"><span data-stu-id="24725-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="24725-323">องค์กรของคุณจะส่งใบแจ้งหนี้ให้ลูกค้าทุกสิ้นเดือน</span><span class="sxs-lookup"><span data-stu-id="24725-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="24725-324">เมื่อคุณตั้งค่าสัญญาโครงการ คุณตกลงที่จะเรียกเก็บเงินจากลูกค้าทุกเดือนสำหรับเวลาและวัสดุในโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="24725-325">คุณสร้างกฎการเรียกเก็บเงินที่มีข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="24725-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="24725-326">ระยะเวลาสัญญาหกเดือน</span><span class="sxs-lookup"><span data-stu-id="24725-326">The contract period is six months.</span></span>
-   <span data-ttu-id="24725-327">เวลาให้คำปรึกษาคำนวณในอัตรา 150 ต่อชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="24725-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="24725-328">เครื่องใช้สำนักงานออกใบแจ้งหนี้ในราคาทุนและต้นทุนรวมสำหรับโครงการต้องไม่เกิน 10,000</span><span class="sxs-lookup"><span data-stu-id="24725-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="24725-329">คุณสร้างใบแจ้งหนี้ของลูกค้าเมื่อสิ้นสุดแต่ละเดือนตามปฏิทินในระหว่างโครงการ</span><span class="sxs-lookup"><span data-stu-id="24725-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="24725-330">ในช่วงเดือนแรกที่ปรึกษาของโครงการจะบันทึกเวลาทั้งหมด 800 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="24725-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="24725-331">ค่าเครื่องใช้สำนักงานที่เรียกเก็บจากโครงการคือ 2,000</span><span class="sxs-lookup"><span data-stu-id="24725-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="24725-332">ดังนั้นเมื่อสิ้นเดือนคุณสร้างใบแจ้งหนี้จำนวน 122,000 ซึ่งคำนวณเป็น 800 ชั่วโมงที่ 150 ต่อชั่วโมง บวกกับ 2,000 สำหรับวัสดุสำนักงาน</span><span class="sxs-lookup"><span data-stu-id="24725-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



