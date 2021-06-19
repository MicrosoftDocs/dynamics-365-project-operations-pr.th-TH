---
title: สร้างโครงการใหม่
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการสร้างโครงการใหม่
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006264"
---
# <a name="create-a-new-project"></a><span data-ttu-id="c61b1-103">สร้างโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="c61b1-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c61b1-104">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="c61b1-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="c61b1-105">บนหน้า **การจัดการโครงการ** เลือก **โครงการใหม่** และป้อนค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c61b1-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="c61b1-106">**ชนิดโครงการ:** เวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="c61b1-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="c61b1-107">**ชื่อโครงการ:** การอัพเกรด XYZ ระยะที่ 2</span><span class="sxs-lookup"><span data-stu-id="c61b1-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="c61b1-108">**กลุ่มโครงการ:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="c61b1-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="c61b1-109">**รหัสสัญญาโครงการ:** 00000002</span><span class="sxs-lookup"><span data-stu-id="c61b1-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="c61b1-110">เลือก **สร้างโครงการ**</span><span class="sxs-lookup"><span data-stu-id="c61b1-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="c61b1-111">มอบหมายทรัพยากรให้กับโครงการ</span><span class="sxs-lookup"><span data-stu-id="c61b1-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="c61b1-112">ในหน้า **ผู้ปฏิบัติงาน** ในรายการ **ผู้ปฏิบัติงาน** เลือกเรกคอร์ดสำหรับผู้ปฏิบัติงานที่คุณตั้งค่าความสามารถให้ก่อนหน้านี้ และเปิดเรกคอร์ดผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c61b1-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="c61b1-113">ในบานหน้าต่างการดำเนินการ บนแท็บ **โครงการ** ในกลุ่ม **การตั้งค่า** เลือก **มอบหมายโครงการ**</span><span class="sxs-lookup"><span data-stu-id="c61b1-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="c61b1-114">บนหน้า **การมอบหมายโครงการการตรวจสอบทรัพยากร** บนแท็บ **โครงการ** ในฟิลด์ **เพิ่มโครงการไปยังโครงการที่เลือก** กรองข้อมูลในโครงการ **การอัพเกรด XYZ ระยะที่ 2**</span><span class="sxs-lookup"><span data-stu-id="c61b1-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="c61b1-115">ในบานหน้าต่าง **โครงการที่เหลือ** เลือกโครงการ และจากนั้น เลือกปุ่มลูกศรเพื่อเพิ่มลงในบานหน้าต่าง **โครงการที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="c61b1-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="c61b1-116">นอกจากนี้ คุณยังสามารถมอบหมายประเภทสำหรับทรัพยากรได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="c61b1-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="c61b1-117">ชนิดของประเภทคือ **ค่าใช้จ่าย** หรือ **รายได้** อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c61b1-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="c61b1-118">ชนิดของประเภทถูกกำหนดโดยองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="c61b1-118">The category type is determined by your organization.</span></span> <span data-ttu-id="c61b1-119">หากไม่มีการมอบหมายประเภทสำหรับทรัพยากร Finance จะค้นหาประเภทเริ่มต้นตามราคารายชั่วโมงสำหรับต้นทุนและรายได้</span><span class="sxs-lookup"><span data-stu-id="c61b1-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="c61b1-120">ตั้งค่าทรัพยากรโครงการและลักษณะบทบาท</span><span class="sxs-lookup"><span data-stu-id="c61b1-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="c61b1-121">ผู้จัดการโครงการสามารถใช้ฟังก์ชันการจัดเตรียมทรัพยากรของโครงการเพื่อสร้างบทบาทที่จำเป็นสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="c61b1-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="c61b1-122">สามารถใช้บทบาทได้ หากยังไม่ทราบทรัพยากรที่ได้รับการยืนยัน เมื่อมีการสำรองทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c61b1-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="c61b1-123">คุณสามารถสำรองบทบาทไว้ชั่วคราวตามทรัพยากรที่วางแผนไว้ เพื่อให้คุณสามารถดำเนินขั้นตอนการวางแผนโครงการต่อไปได้</span><span class="sxs-lookup"><span data-stu-id="c61b1-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="c61b1-124">[![ตัวอย่างบทบาท](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="c61b1-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="c61b1-125">**สถานการณ์:** Contoso ได้รับการว่าจ้างให้ทำโครงการเวลาและวัสดุที่มีกฎบัตรโครงการที่ได้รับอนุมัติให้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="c61b1-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="c61b1-126">ผู้จัดการโครงการรุ่นเยาว์ยังคงทำให้ขอบเขตของโครงการสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="c61b1-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="c61b1-127">ขณะนี้ Resource Manager กำลังระบุทรัพยากรเฉพาะที่จะสงวนไว้เพื่อทำงานในโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="c61b1-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="c61b1-128">เนื่องจากลักษณะสำคัญของโครงการ ผู้สนับสนุนโครงการจึงขอให้ผู้จัดการโครงการอาวุโสเป็นหนึ่งในบทบาท</span><span class="sxs-lookup"><span data-stu-id="c61b1-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="c61b1-129">ผู้จัดการทรัพยากรต้องได้รับทรัพยากรใหม่และกำหนดบทบาทในระบบ ในกรณีที่ผู้จัดการโครงการรุ่นเยาว์ต้องการข้อมูลทรัพยากรในระหว่างการวางแผนโครงการ</span><span class="sxs-lookup"><span data-stu-id="c61b1-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="c61b1-130">ขั้นตอนต่อไปนี้แสดงวิธีที่ Resource Manager สามารถตั้งค่าบทบาทผู้จัดการโครงการอาวุโสและเชื่อมโยงคุณลักษณะของทรัพยากรด้วย</span><span class="sxs-lookup"><span data-stu-id="c61b1-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="c61b1-131">ในภายหลัง สามารถใช้บทบาทเพื่อค้นหาทรัพยากรที่มีอยู่ซึ่งตรงกับความสามารถของทรัพยากรที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c61b1-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="c61b1-132">บนหน้า **ตั้งค่าบทบาท** เลือก **สร้าง** และป้อนค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c61b1-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="c61b1-133">**รหัสบทบาท:** ผู้จัดการโครงการอาวุโส</span><span class="sxs-lookup"><span data-stu-id="c61b1-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="c61b1-134">**Description:** ผู้จัดการโครงการอาวุโส</span><span class="sxs-lookup"><span data-stu-id="c61b1-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="c61b1-135">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c61b1-135">Select **Create**.</span></span>
3. <span data-ttu-id="c61b1-136">เลือกบทบาท **ผู้จัดการโครงการอาวุโส** แล้วจากนั้น เลือก **ตั้งค่าคอนฟิกลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="c61b1-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="c61b1-137">ในฟิลด์ **ชนิดของลักษณะ** ให้เลือก **ทักษะ**</span><span class="sxs-lookup"><span data-stu-id="c61b1-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="c61b1-138">ในฟิลด์ **ลักษณะที่พร้อมใช้งาน** ป้อนทักษะที่ต้องการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c61b1-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="c61b1-139">ในฟิลด์ **ชนิดของลักษณะ** ให้เลือก **ใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="c61b1-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="c61b1-140">ในฟิลด์ **ลักษณะที่พร้อมใช้งาน** ป้อนชนิดใบรับรองที่ต้องการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c61b1-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="c61b1-141">มอบหมายทรัพยากรของโครงการให้กับโครงการ</span><span class="sxs-lookup"><span data-stu-id="c61b1-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="c61b1-142">บนหน้า **โครงการทั้งหมด** เลือกโครงการ **การอัพเกรด XYZ ระยะที่ 2**</span><span class="sxs-lookup"><span data-stu-id="c61b1-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="c61b1-143">บนแท็บ **กลุ่มคนของโครงการและการจัดกำหนดการ** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="c61b1-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="c61b1-144">ในฟิลด์ **บทบาท** ให้เลือก **สมาชิกในกลุ่มคน**</span><span class="sxs-lookup"><span data-stu-id="c61b1-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="c61b1-145">เลือก **จองจากปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="c61b1-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="c61b1-146">บนหน้า **ความพร้อมของทรัพยากร** ให้เลือก **ดูการตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="c61b1-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="c61b1-147">บนหน้า **ปรับการตั้งค่ามุมมอง** ป้อนค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c61b1-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="c61b1-148">**รูปแบบสำหรับมุมมองของช่วงวันที่:** วัน</span><span class="sxs-lookup"><span data-stu-id="c61b1-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="c61b1-149">**แสดง Description ความพร้อมใช้งาน:** ใช่</span><span class="sxs-lookup"><span data-stu-id="c61b1-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="c61b1-150">**แสดงกำลังการผลิตคงเหลือ:** ใช่</span><span class="sxs-lookup"><span data-stu-id="c61b1-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="c61b1-151">ในรายการของทรัพยากร เลือกทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c61b1-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="c61b1-152">เลือก **จองแบบตายตัว** และ **กำลังการผลิตแบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="c61b1-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="c61b1-153">มอบหมายทรัพยากรให้แก่บทบาทเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c61b1-153">Assign a resource to a default role</span></span>

<span data-ttu-id="c61b1-154">เพื่อช่วยผู้จัดการโครงการหรือ Resource Manager ในการดูรายละเอียดแนวลึกเพิ่มเติมเกี่ยวกับทรัพยากรที่จองไว้สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="c61b1-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="c61b1-155">คุณสามารถเชื่อมโยงบทบาทเริ่มต้นกับทรัพยากรที่มีอยู่หรือทรัพยากรที่ได้มาใหม่</span><span class="sxs-lookup"><span data-stu-id="c61b1-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="c61b1-156">ตัวอย่างเช่น เมื่อ Daniel ได้รับการว่าจ้าง เขามีประสบการณ์และทักษะที่จะเติมเต็มบทบาทนักวิเคราะห์ธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="c61b1-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="c61b1-157">Resource Manager มอบหมายบทบาทนี้เป็นบทบาทเริ่มต้นของ Daniel</span><span class="sxs-lookup"><span data-stu-id="c61b1-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="c61b1-158">ดังนั้น Resource Manager จึงเพิ่ม Daniel เข้าไปในกลุ่มของนักวิเคราะห์ธุรกิจที่พร้อมทำงานในโครงการต่างๆ</span><span class="sxs-lookup"><span data-stu-id="c61b1-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="c61b1-159">ในระหว่างการสำรองทรัพยากร ผู้จัดการโครงการสามารถกรองทรัพยากรบทบาทที่พร้อมใช้งานในโครงการได้</span><span class="sxs-lookup"><span data-stu-id="c61b1-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="c61b1-160">พวกเขาสามารถใช้ข้อมูลนี้เป็นเกณฑ์เดียว เมื่อพวกเขาทำการวิเคราะห์การตัดสินใจหลายเกณฑ์ในระหว่างการเติมเต็มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c61b1-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="c61b1-161">นอกจากนี้ พวกเขายังสามารถเพิ่มลักษณะทรัพยากรอื่นๆ ในตัวกรอง เพื่อค้นหาทรัพยากรที่มีทักษะ การศึกษา และประสบการณ์เฉพาะ สำหรับโครงการนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="c61b1-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="c61b1-162">**สถานการณ์:** โครงการที่ได้รับอนุมัติเริ่มต้น และบทบาทผู้จัดการโครงการอาวุโสถูกสงวนไว้เป็นทรัพยากรตามแผนในระหว่างลำดับขั้นการวางแผนโครงการ</span><span class="sxs-lookup"><span data-stu-id="c61b1-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="c61b1-163">ขณะนี้ Resource Manager ได้รับทรัพยากรเพื่อตอบสนองบทบาทผู้จัดการโครงการอาวุโส</span><span class="sxs-lookup"><span data-stu-id="c61b1-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="c61b1-164">บนหน้า **รายการทรัพยากร** ให้เลือก **Daniel Goldschmidt**</span><span class="sxs-lookup"><span data-stu-id="c61b1-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="c61b1-165">บนหน้า **บทบาททรัพยากร** เลือก **สร้าง** และป้อนค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c61b1-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="c61b1-166">**มีผลบังคับใช้:** ป้อนวันที่ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="c61b1-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="c61b1-167">**การหมดอายุ:** ป้อน **ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="c61b1-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="c61b1-168">**บทบาท:** ป้อน **ผู้จัดการโครงการอาวุโส**</span><span class="sxs-lookup"><span data-stu-id="c61b1-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="c61b1-169">เลือก **บันทึก** แล้วจากนั้น ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c61b1-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="c61b1-170">บนแท็บ **ความสามารถ** เพิ่มทักษะ **ProjectMgmt** และใบรับรอง **PMP**</span><span class="sxs-lookup"><span data-stu-id="c61b1-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]