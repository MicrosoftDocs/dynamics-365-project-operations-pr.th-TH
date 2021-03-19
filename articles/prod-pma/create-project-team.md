---
title: สร้างทีมโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการสร้างและจัดการทีมโครงการ
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 121a007d91c2da4f3b9951901781757b8bcca8fe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270881"
---
# <a name="create-a-project-team"></a><span data-ttu-id="bc01c-103">สร้างกลุ่มคนของโครงการ</span><span class="sxs-lookup"><span data-stu-id="bc01c-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc01c-104">ในการใช้บทบาทที่ถูกตั้งค่าไว้ก่อนหน้านี้ในโครงการ ผู้จัดการโครงการต้องเชื่อมโยงบทบาทกับโครงการ</span><span class="sxs-lookup"><span data-stu-id="bc01c-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="bc01c-105">สามารถมอบหมายได้หลายบทบาทสำหรับหนึ่งโครงการ</span><span class="sxs-lookup"><span data-stu-id="bc01c-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="bc01c-106">เพื่อป้องกันความสับสน บทบาทเหล่านี้จะถูกติดป้ายกำกับโดยอัตโนมัติระหว่างการจอง</span><span class="sxs-lookup"><span data-stu-id="bc01c-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="bc01c-107">ตัวอย่างเช่น หากผู้จัดการโครงการต้องการวิศวกรซอฟต์แวร์สามคน บทบาทวิศวกรซอฟต์แวร์สามบทบาทที่มี **วิศวกรซอฟต์แวร์ 1** **วิศวกรซอฟต์แวร์ 2** และ **วิศวกรซอฟต์แวร์ 3** เป็นป้ายกำกับของพวกเขา จะถูกสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="bc01c-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="bc01c-108">หากก่อนหน้านี้มีการตั้งค่าคุณลักษณะของบทบาทสำหรับบทบาท คุณลักษณะเหล่านี้จะถูกนำไปใช้เป็นตัวกรองในระหว่างการค้นหาทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="bc01c-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="bc01c-109">สามารถเพิ่มคุณสมบัติเพิ่มเติมได้ตามต้องการ เพื่อปรับแต่งการค้นหาเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="bc01c-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="bc01c-110">นอกจากนี้ ยังสามารถปรับแต่งการตั้งค่ามุมมองเพื่อให้มุมมองที่ดีขึ้นเกี่ยวกับความพร้อมของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="bc01c-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="bc01c-111">มีตัวเลือกในการแสดงความพร้อมใช้งานรายชั่วโมง รายวัน รายสัปดาห์ รายเดือน รายไตรมาส และรายปี</span><span class="sxs-lookup"><span data-stu-id="bc01c-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="bc01c-112">นอกจากนี้ ยังมีตัวเลือกในการแสดงความสามารถที่พร้อมใช้งานและที่คงเหลือในทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="bc01c-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="bc01c-113">ตัวเลือกนี้มีประโยชน์สำหรับการจัดการเวลา เมื่อคุณประมาณเวลาที่พร้อมใช้งานสำหรับกิจกรรมหรือความพร้อมของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="bc01c-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="bc01c-114">ผู้จัดการโครงการสามารถเลือกบทบาทบนหน้า และจากนั้น หากมีทรัพยากรที่พร้อมใช้งานซึ่งตรงกับความต้องการ ให้เลือกเพื่อจองทรัพยากรเพื่อเติมเต็มบทบาท</span><span class="sxs-lookup"><span data-stu-id="bc01c-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="bc01c-115">โปรดทราบว่าไม่จำเป็นต้องจองทรัพยากร ณ จุดนี้ ในลำดับขั้นการวางแผน</span><span class="sxs-lookup"><span data-stu-id="bc01c-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="bc01c-116">เมื่อคุณสร้าง WBS คุณสามารถแทนที่บทบาทด้วยทรัพยากรที่มีการจัดเตรียมพนักงานสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="bc01c-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="bc01c-117">หากบทบาทถูกแทนที่ด้วยทรัพยากรที่มีการจัดเตรียมพนักงานใน WBS การตั้งค่าทรัพยากรจะปรับปรุงการแสดงรายชื่อกลุ่มคนของโครงการและการจัดกำหนดการโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="bc01c-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="bc01c-118">[![การแสดงรายชื่อกลุ่มคนของโครงการที่มีทั้งบทบาทและทรัพยากรจริง](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="bc01c-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="bc01c-119">ผู้จัดการโครงการมีตัวเลือกต่างๆ สำหรับการจองทรัพยากรสำหรับโครงการ เช่น **กำลังการผลิตที่เหลืออยู่** **กำลังการผลิตแบบเต็ม** **เปอร์เซ็นต์กำลังการผลิต** และ **ระบุชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="bc01c-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="bc01c-120">ตัวเลือกการจองเหล่านี้สามารถยกเลิกได้ทุกเมื่อ หากการมอบหมายทรัพยากรเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="bc01c-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="bc01c-121">รองรับการจองสองชนิด:</span><span class="sxs-lookup"><span data-stu-id="bc01c-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="bc01c-122">**จองแบบตายตัว** – การจองทรัพยากรได้รับการอนุมัติและยืนยันว่าจะทำงานในการมีส่วนร่วมในตามระยะเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="bc01c-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="bc01c-123">**จองแบบไม่ตายตัว** – การจองทรัพยากรถูกตั้งค่าอย่างไม่แน่นอนให้ทำงานในการมีส่วนร่วมในตามระยะเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="bc01c-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="bc01c-124">กระบวนงานต่อไปนี้อธิบายวิธีการสร้างกลุ่มคนของโครงการ</span><span class="sxs-lookup"><span data-stu-id="bc01c-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="bc01c-125">สร้างกลุ่มคนของโครงการ</span><span class="sxs-lookup"><span data-stu-id="bc01c-125">Create a project team</span></span>

1. <span data-ttu-id="bc01c-126">บนหน้ารายการ **โครงการทั้งหมด** เลือกโครงการ และจากนั้น เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="bc01c-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="bc01c-127">บนแท็บ **กลุ่มคนของโครงการและการจัดกำหนดการ** ในฟิลด์ **วันที่สิ้นสุดของกำหนดการ** ป้อนวันที่เริ่มต้นของกำหนดการบวกหนึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="bc01c-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="bc01c-128">ตัวอย่างเช่น หากวันที่เริ่มต้นของกำหนดการคือ 24 มิถุนายน 2017 (24/06/2017) ให้ป้อน **24/07/2017**</span><span class="sxs-lookup"><span data-stu-id="bc01c-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="bc01c-129">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="bc01c-129">Select **Add**.</span></span>
4. <span data-ttu-id="bc01c-130">ในบานหน้าต่าง **เพิ่มบทบาทให้กับโครงการ** ใน **บทบาท** ให้เลือก **ผู้จัดการโครงการอาวุโส**</span><span class="sxs-lookup"><span data-stu-id="bc01c-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="bc01c-131">เลือก **ความสามารถที่จำเป็น**</span><span class="sxs-lookup"><span data-stu-id="bc01c-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="bc01c-132">บนหน้า **เลือกลักษณะ** ลักษณะที่คุณตั้งค่าไว้ก่อนหน้านี้สำหรับบทบาทผู้จัดการโครงการอาวุโส จะถูกเลือกโดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="bc01c-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="bc01c-133">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bc01c-133">Select **OK**.</span></span>
7. <span data-ttu-id="bc01c-134">บนหน้า **เพิ่มบทบาทให้กับโครงการ** ในฟิลด์ **จำนวนของทรัพยากร** ป้อน **1**</span><span class="sxs-lookup"><span data-stu-id="bc01c-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="bc01c-135">ในฟิลด์ **ทรัพยากร** การค้นหาจะแสดงทรัพยากรทั้งหมดที่มีความสามารถที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="bc01c-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="bc01c-136">เลือก **Daniel Goldschmidt** แล้วจากนั้น เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="bc01c-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="bc01c-137">บนหน้า **โครงการ** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="bc01c-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="bc01c-138">ในบานหน้าต่าง **เพิ่มบทบาทให้กับโครงการ** ใน **บทบาท** ให้เลือก **สมาชิกในกลุ่มคน**</span><span class="sxs-lookup"><span data-stu-id="bc01c-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="bc01c-139">ในฟิลด์ **จำนวนทรัพยากร** ป้อน **5**</span><span class="sxs-lookup"><span data-stu-id="bc01c-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="bc01c-140">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="bc01c-140">Select **Create**.</span></span>
12. <span data-ttu-id="bc01c-141">บนหน้า **โครงการ** ให้เลือก **เติมเต็มทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="bc01c-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="bc01c-142">ตรวจสอบกลุ่มคนในโครงการ</span><span class="sxs-lookup"><span data-stu-id="bc01c-142">Monitor project teams</span></span>
1. <span data-ttu-id="bc01c-143">บนหน้า **โครงการทั้งหมด** เลือกลิงค์ **รหัสโครงการ** สำหรับโครงการ **การอัพเกรด XYZ ระยะที่ 2**</span><span class="sxs-lookup"><span data-stu-id="bc01c-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="bc01c-144">บน FastTab **กลุ่มคนในโครงการและการจัดกำหนดการ** ตรวจสอบว่าทรัพยากรของโครงการที่มีการแสดงรายการนั้นถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="bc01c-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]