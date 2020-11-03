---
title: ประมาณการยอดขายและต้นทุนของโครงการเมื่อทรัพยากรที่จองได้มีหลายบทบาทในโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีที่สามารถใช้มิติข้อมูลการกำหนดราคาเพื่อสนับสนุนการกำหนดราคาและการคิดต้นทุนสำหรับทรัพยากรที่มีหลายบทบาทในโครงการ
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085984"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="a6816-103">ประมาณการยอดขายและต้นทุนของโครงการเมื่อทรัพยากรที่จองได้มีหลายบทบาทในโครงการ</span><span class="sxs-lookup"><span data-stu-id="a6816-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="a6816-104">บริษัทตามโครงการมักมีความต้องการทรัพยากรเดียวเพื่อทำหน้าที่หลายบทบาทในโครงการ</span><span class="sxs-lookup"><span data-stu-id="a6816-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="a6816-105">แต่ละบทบาทเหล่านี้อาจมีราคาและต้นทุนแตกต่างกัน ซึ่งหมายความว่าเวลาของทรัพยากรเดียวกันในโครงการอาจได้รับการประมาณทางการเงินที่แตกต่างกัน ขึ้นอยู่กับอัตราในการเรียกเก็บเงินและต้นทุนสำหรับแต่ละบทบาท</span><span class="sxs-lookup"><span data-stu-id="a6816-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="a6816-106">Project Service Automation อนุญาตให้ตั้งค่าในเรกคอร์ดสมาชิกทีมสำหรับทรัพยากรที่ระบุชื่อและอนุญาตให้มีการแทนที่ที่แตกต่างกันสำหรับแต่ละงานที่สมาชิกทีมได้รับมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="a6816-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="a6816-107">ตัวอย่างต่อไปนี้อธิบายว่าการแทนที่ค่านี้อย่างง่ายทำให้ทรัพยากรมีหลายบทบาทในโครงการที่มีอัตราต้นทุนและค่าบริการที่แตกต่างกันได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="a6816-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="a6816-108">สร้างงาน</span><span class="sxs-lookup"><span data-stu-id="a6816-108">Create tasks</span></span>
<span data-ttu-id="a6816-109">สร้างงานโครงการสองงานครั้งละ 40 ชั่วโมง คือ งาน A และงาน B เลือกงาน A เป็นงานก่อนหน้างาน B</span><span class="sxs-lookup"><span data-stu-id="a6816-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="a6816-110">ตั้งค่าบทบาทและหน่วยองค์กรสำหรับสมาชิกทีมโครงการทั่วไป</span><span class="sxs-lookup"><span data-stu-id="a6816-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="a6816-111">บนเพจ **กำหนดการ** เลือกแถว **งาน** สำหรับงาน A</span><span class="sxs-lookup"><span data-stu-id="a6816-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="a6816-112">ในฟิลด์ **ทรัพยากร** ให้เลือก **สร้าง** ในรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="a6816-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="a6816-113">บนเพจ **การสร้างด่วนของสมาชิกทีม** ให้ระบุแอตทริบิวต์ของสมาชิกทีมทั่วไปที่สามารถทำงานนี้ได้</span><span class="sxs-lookup"><span data-stu-id="a6816-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="a6816-114">เลือกบทบาทและหน่วยองค์กรที่เหมาะสม จากนั้นเลือก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="a6816-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="a6816-115">มีการสร้างสมาชิกทีมทั่วไปและกำหนดให้กับงานนี้</span><span class="sxs-lookup"><span data-stu-id="a6816-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="a6816-116">ทำซ้ำขั้นตอนเหล่านี้สำหรับงาน B และตรวจสอบให้แน่ใจว่าบทบาทและหน่วยองค์กรในสมาชิกทีมทั่วไปที่สร้างขึ้นสำหรับงาน B นั้นแตกต่างจากงาน A</span><span class="sxs-lookup"><span data-stu-id="a6816-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="a6816-117">ตั้งค่าบทบาทและหน่วยองค์กรสำหรับงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="a6816-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="a6816-118">หลังจากที่คุณสร้างงาน A ให้เลือกงาน จากนั้นเลือก **แก้ไขงาน**</span><span class="sxs-lookup"><span data-stu-id="a6816-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="a6816-119">บนเพจ **รายละเอียดงาน** ให้ค้นหาฟิลด์ **บทบาท** และ **หน่วยองค์กร** เพิ่มค่าที่จำเป็นสำหรับทรัพยากรที่จะทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="a6816-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="a6816-120">ถ้าคุณกำลังทำสถานการณ์นี้ให้เสร็จสมบูรณ์โดยใช้ข้อมูลสาธิตของ Project Service Automation ให้เลือก **หัวหน้าที่ปรึกษา** สำหรับบทบาท และ **Fabrikam US** เป็นหน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="a6816-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="a6816-121">เลือกงาน B จากนั้นเลือก **แก้ไขงาน**</span><span class="sxs-lookup"><span data-stu-id="a6816-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="a6816-122">บนเพจ **รายละเอียดงาน** ให้ค้นหาฟิลด์ **บทบาท** และ **หน่วยองค์กร** เพิ่มค่าที่จำเป็นสำหรับทรัพยากรที่จะทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="a6816-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="a6816-123">ตรวจสอบให้แน่ใจว่าค่าในฟิลด์ **บทบาท** และ **หน่วยองค์กร** สำหรับงาน B แตกต่างจากฟิลด์สำหรับงาน A</span><span class="sxs-lookup"><span data-stu-id="a6816-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="a6816-124">ถ้าคุณกำลังทำสถานการณ์นี้ให้เสร็จสมบูรณ์โดยใช้ข้อมูลสาธิตของ Project Service Automation ให้เลือก **ช่างเทคนิคเครือข่าย** สำหรับบทบาท และ **Fabrikam US** เป็นหน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="a6816-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="a6816-125">บันทึกและปิดเพจ **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="a6816-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="a6816-126">ลักษณะการทำงานของสมาชิกทีมและประมาณการ</span><span class="sxs-lookup"><span data-stu-id="a6816-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="a6816-127">บนเพจ **รายละเอียดงาน** บน **สมาชิกทีม** เลือกสมาชิกทีมทั่วไปสองคน จากนั้นเลือก **สร้างความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="a6816-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="a6816-128">การดำเนินการนี้จะสร้างความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="a6816-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="a6816-129">เลือกแถวสมาชิกทีมสำหรับ **หัวหน้าที่ปรึกษา** จากนั้นเลือก **จอง**</span><span class="sxs-lookup"><span data-stu-id="a6816-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="a6816-130">ตารางกำหนดการจะเปิดขึ้นและจองทรัพยากรตามความต้องการนั้น</span><span class="sxs-lookup"><span data-stu-id="a6816-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="a6816-131">เลือกแถวสมาชิกทีมสำหรับ **ช่างเทคนิคเครือข่าย** จากนั้นเลือก **จอง**</span><span class="sxs-lookup"><span data-stu-id="a6816-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="a6816-132">ตารางกำหนดการจะเปิดขึ้นและจองทรัพยากรเดียวกันสำหรับความต้องการนั้น</span><span class="sxs-lookup"><span data-stu-id="a6816-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="a6816-133">ตารางสมาชิกทีม</span><span class="sxs-lookup"><span data-stu-id="a6816-133">Team Member grid</span></span> 
<span data-ttu-id="a6816-134">บนตาราง **สมาชิกทีม** โปรดสังเกตว่าเรกคอร์ดสมาชิกทีมทั่วไปสองรายการถูกลบและแทนที่ด้วยทรัพยากรหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="a6816-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="a6816-135">มีชุดค่าหนึ่งชุดสำหรับทรัพยากรที่แสดงชุดค่าเริ่มต้นสำหรับ **บทบาท** และ **หน่วยองค์กร**</span><span class="sxs-lookup"><span data-stu-id="a6816-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="a6816-136">เมื่อคุณขยายแถวของเรกคอร์ดสมาชิกทีม คุณจะเห็นการมอบหมายงานที่แตกต่างกันในเรกคอร์ดสมาชิกทีมสำหรับทั้งสองงานนั้น</span><span class="sxs-lookup"><span data-stu-id="a6816-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="a6816-137">แถวการมอบหมายแต่ละแถวมีค่าเฉพาะงานสำหรับ **บทบาท** และ **หน่วยองค์กร**</span><span class="sxs-lookup"><span data-stu-id="a6816-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="a6816-138">ตารางประมาณการ</span><span class="sxs-lookup"><span data-stu-id="a6816-138">Estimates grid</span></span> 
<span data-ttu-id="a6816-139">เมื่อคุณไปที่ตาราง **ประมาณการ** คุณจะสังเกตเห็นว่าการมอบหมายทั้งสองงานสำหรับทรัพยากรเดียวกันมีราคาต่างกัน</span><span class="sxs-lookup"><span data-stu-id="a6816-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="a6816-140">การมอบหมายงานสำหรับทรัพยากรในงาน A มีการกำหนดราคาโดยใช้ค่าแอตทริบิวต์ **บทบาท** ของ **หัวหน้าที่ปรึกษา**</span><span class="sxs-lookup"><span data-stu-id="a6816-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="a6816-141">การมอบหมายงานสำหรับทรัพยากรเดียวกันในงาน B มีการกำหนดราคาโดยใช้ค่าแอตทริบิวต์ **บทบาท** ของ **ช่างเทคนิคเครือข่าย**</span><span class="sxs-lookup"><span data-stu-id="a6816-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





