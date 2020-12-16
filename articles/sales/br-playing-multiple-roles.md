---
title: ประมาณการยอดขายและต้นทุนโครงการ เมื่อทรัพยากรที่จองได้เติมเต็มหลายบทบาทในโครงการ
description: หัวข้อนี้จะอธิบายวิธีใช้มิติการกำหนดราคาเพื่อสนับสนุนค่าประมาณการกำหนดราคาและการคิดต้นทุนสำหรับทรัพยากรที่เติมเต็มหลายบทบาทในโครงการ
author: rumant
manager: tfehr
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: da17f0f58623128d51fda0f5529182cd37ea41b9
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531577"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a><span data-ttu-id="c7590-103">ประมาณการยอดขายและต้นทุนโครงการ เมื่อทรัพยากรที่จองได้เติมเต็มหลายบทบาทในโครงการ</span><span class="sxs-lookup"><span data-stu-id="c7590-103">Estimate project sales and costs when a bookable resource fills multiple roles on a project</span></span> 

<span data-ttu-id="c7590-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว Project Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ตามการผลิต_</span><span class="sxs-lookup"><span data-stu-id="c7590-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing, Project Operations for stocked/production-based scenarios_</span></span> 

<span data-ttu-id="c7590-105">บริษัทตามโครงการมักมีความต้องการทรัพยากรหนึ่งรายการเพื่อเติมเต็มหลายบทบาทในโครงการ</span><span class="sxs-lookup"><span data-stu-id="c7590-105">Project-based companies often have the need for one resource to fill multiple roles on a project.</span></span> <span data-ttu-id="c7590-106">สามารถกำหนดราคาและต้นทุนแต่ละบทบาทได้แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="c7590-106">Each role can be priced and costed differently.</span></span> <span data-ttu-id="c7590-107">นี่หมายความว่าเวลาของทรัพยากรเดียวกันในโครงการอาจได้รับการประมาณทางการเงินที่แตกต่างกัน โดยขึ้นอยู่กับอัตราการเรียกเก็บเงินและอัตราต้นทุนสำหรับแต่ละบทบาท</span><span class="sxs-lookup"><span data-stu-id="c7590-107">This means that the same resource's time on a project could get a different financial estimate depending on the bill and cost rates for each role.</span></span> <span data-ttu-id="c7590-108">คุณสามารถตั้งค่าในเรกคอร์ดสมาชิกในกลุ่มคนสำหรับทรัพยากรที่มีชื่อ โดยมีการแทนที่ที่แตกต่างกันสำหรับแต่ละงานที่สมาชิกในกลุ่มคนได้รับมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="c7590-108">You can set up the values on the team member record for the named resource with different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="c7590-109">ตัวอย่างต่อไปนี้จะอธิบายวิธีการที่การแทนที่ค่าอย่างง่ายช่วยให้ทรัพยากรมีหลายบทบาทในโครงการที่มีอัตราต้นทุนและอัตราการเรียกเก็บเงินที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="c7590-109">The following example walks you through how the simple override of a value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="c7590-110">สร้างงาน</span><span class="sxs-lookup"><span data-stu-id="c7590-110">Create tasks</span></span>
<span data-ttu-id="c7590-111">ในการสร้างงาน คุณต้องเพิ่มงานและงานสรุป หลังจากนั้นคุณต้องมอบหมายงานก่อนที่จะคุณเพิ่มระยะเวลาของงาน</span><span class="sxs-lookup"><span data-stu-id="c7590-111">To create tasks, you need to add tasks, as well as summary tasks, after which you need to assign the task before you add task duration.</span></span> 

### <a name="add-tasks-and-summary-tasks"></a><span data-ttu-id="c7590-112">เพิ่มงานและงานสรุป</span><span class="sxs-lookup"><span data-stu-id="c7590-112">Add tasks and summary tasks</span></span>
<span data-ttu-id="c7590-113">เมื่อต้องการเพิ่มงาน ทำตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="c7590-113">To add a task, complete the following steps.</span></span>

1. <span data-ttu-id="c7590-114">ไปที่ **โครงการ** และเปิดโครงการที่คุณต้องการเพิ่มงาน</span><span class="sxs-lookup"><span data-stu-id="c7590-114">Go to **Projects** and open the project to which you want to add tasks.</span></span>
2. <span data-ttu-id="c7590-115">เลือก **เพิ่มงานใหม่**</span><span class="sxs-lookup"><span data-stu-id="c7590-115">Select **Add new task**.</span></span> <span data-ttu-id="c7590-116">ตั้งชื่องาน และจากนั้น กด **ป้อน**</span><span class="sxs-lookup"><span data-stu-id="c7590-116">Name the task, and then press **Enter**.</span></span>
3. <span data-ttu-id="c7590-117">ป้อนชื่องานอื่น และกด **ป้อน**</span><span class="sxs-lookup"><span data-stu-id="c7590-117">Enter another task name and press **Enter**.</span></span> <span data-ttu-id="c7590-118">ทำซ้ำจนกว่าคุณจะมีรายการงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c7590-118">Repeat this until you have a full list of tasks.</span></span>
3. <span data-ttu-id="c7590-119">เพื่อเยื้องงานภายใต้งาน **สรุป** เลือกจุดแนวตั้งสามจุดตามชื่องาน และจากนั้น เลือก **สร้างงานย่อย**</span><span class="sxs-lookup"><span data-stu-id="c7590-119">To indent tasks under **Summary** tasks, select the three vertical dots by the task name, and then select **Make subtask**.</span></span> 

  > [!TIP]
  > <span data-ttu-id="c7590-120">ในการเลือกงานมากกว่าหนึ่งงาน ให้เลือกงาน กด **Ctrl** ค้างไว้ แล้วจากนั้น เลือกงานอื่น</span><span class="sxs-lookup"><span data-stu-id="c7590-120">To select more than one task, select a task, press and hold **Ctrl**, and then select another task.</span></span>
  >
  > <span data-ttu-id="c7590-121">นอกจากนี้ คุณยังสามารถเลือก **เลื่อนระดับงานย่อย** เพื่อย้ายงานออกจากภายใต้งาน **สรุป**</span><span class="sxs-lookup"><span data-stu-id="c7590-121">You can also choose **Promote subtask** to move tasks out from under **Summary** tasks.</span></span>

### <a name="assign-tasks"></a><span data-ttu-id="c7590-122">มอบหมายงาน</span><span class="sxs-lookup"><span data-stu-id="c7590-122">Assign tasks</span></span>

<span data-ttu-id="c7590-123">ทำตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์เพื่อมอบหมายงาน</span><span class="sxs-lookup"><span data-stu-id="c7590-123">Complete the following steps to assign tasks.</span></span>

1. <span data-ttu-id="c7590-124">ในคอลัมน์ **ได้รับมอบหมายให้** สำหรับงาน เลือกไอคอนบุคคล</span><span class="sxs-lookup"><span data-stu-id="c7590-124">In the  **Assigned to**  column for a task, select the person icon.</span></span>
2. <span data-ttu-id="c7590-125">เลือกสมาชิกในกลุ่มคนจากรายการ หรือป้อนข้อความเพื่อค้นหาชื่อ</span><span class="sxs-lookup"><span data-stu-id="c7590-125">Choose a team member from the list or enter text to search for a name.</span></span>

### <a name="add-task-duration-and-columns"></a><span data-ttu-id="c7590-126">เพิ่มระยะเวลาและคอลัมน์ของงาน</span><span class="sxs-lookup"><span data-stu-id="c7590-126">Add task duration and columns</span></span>

<span data-ttu-id="c7590-127">มักจะง่ายที่สุดในการเริ่มสร้างโครงการของคุณด้วยระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="c7590-127">It's often easiest to begin constructing your project with duration.</span></span> <span data-ttu-id="c7590-128">ทำตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์เพื่อเพิ่มระยะเวลางาน</span><span class="sxs-lookup"><span data-stu-id="c7590-128">Complete the following steps to add a task duration.</span></span>

1. <span data-ttu-id="c7590-129">ในคอลัมน์ **ระยะเวลา** สำหรับงาน พิมพ์จำนวนวันที่คุณคิดว่าจะใช้เวลาในการทำงานให้สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="c7590-129">In the **Duration** column for a task, type the number of days you think it will take to accomplish the task.</span></span> <span data-ttu-id="c7590-130">หากคุณต้องการใช้หน่วยเวลาอื่น ให้ป้อนตัวเลขบวกคำว่า **ชั่วโมง** **สัปดาห์** หรือ **เดือน**</span><span class="sxs-lookup"><span data-stu-id="c7590-130">If you want to use a different unit of time, enter a number plus the word **hours**, **weeks**, or **months**.</span></span>
2. <span data-ttu-id="c7590-131">หากคุณต้องการให้งานของคุณปรากฏเป็นเหตุการณ์สำคัญรูปเพชรในมุมมอง **ไทม์ไลน์** ในคอลัมน์ **ระยะเวลา** ให้ป้อน **0 วัน**</span><span class="sxs-lookup"><span data-stu-id="c7590-131">If you want your task to appear as a diamond-shaped milestone in the **Timeline** view, in the **Duration** column, enter **0 days** .</span></span>
3. <span data-ttu-id="c7590-132">กด **ป้อน** เพื่อไปที่ฟิลด์ **ระยะเวลา** ของงานถัดไป และป้อนระยะเวลาต่อไป</span><span class="sxs-lookup"><span data-stu-id="c7590-132">Press **Enter**  to go to the next task's **Duration** field and continue entering durations.</span></span>

  > [!NOTE]
  > <span data-ttu-id="c7590-133">คุณไม่สามารถป้อนระยะเวลาสำหรับงานสรุป</span><span class="sxs-lookup"><span data-stu-id="c7590-133">You can't enter a duration for summary tasks.</span></span>

<span data-ttu-id="c7590-134">คุณสามารถเพิ่มคอลัมน์ในโครงการของคุณเพื่อให้รายละเอียดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c7590-134">You can add columns to your project to provide more details.</span></span> <span data-ttu-id="c7590-135">ในการดำเนินการนี้ ให้เลือก **เพิ่มคอลัมน์**</span><span class="sxs-lookup"><span data-stu-id="c7590-135">To do this, select **Add column**.</span></span> 

<span data-ttu-id="c7590-136">สำหรับข้อมูลเพิ่มเติม ดู [สร้างโครงการ](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749)</span><span class="sxs-lookup"><span data-stu-id="c7590-136">For more information, see [Create a project](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).</span></span>

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="c7590-137">ตั้งค่าบทบาทและหน่วยองค์กรสำหรับสมาชิกในกลุ่มคนของโครงการทั่วไป</span><span class="sxs-lookup"><span data-stu-id="c7590-137">Set up the role and organization unit for a generic project team member</span></span>
<span data-ttu-id="c7590-138">ทำตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์เพื่อตั้งค่าบทบาทและหน่วยองค์กรสำหรับสมาชิกในกลุ่มคนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="c7590-138">Complete the following steps to set up a role and organizational unit for a generic team member.</span></span>

1. <span data-ttu-id="c7590-139">บนหน้า **งาน** เลือกแถว **งาน** สำหรับ **งาน A**</span><span class="sxs-lookup"><span data-stu-id="c7590-139">On the **Tasks** page, select the **Task** row for **Task A**.</span></span> 
2. <span data-ttu-id="c7590-140">ใน **ได้รับมอบหมายให้** เลือก **เพิ่มทรัพยากรทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="c7590-140">In **Assigned To**, select **Add generic resource**.</span></span> <span data-ttu-id="c7590-141">นี่จะเปิดหน้า **สร้างสมาชิกในกลุ่มคนด่วน**</span><span class="sxs-lookup"><span data-stu-id="c7590-141">This opens the **Team Member Quick Create** page.</span></span>
3. <span data-ttu-id="c7590-142">บนเพจ **การสร้างด่วนของสมาชิกทีม** ให้ระบุแอตทริบิวต์ของสมาชิกทีมทั่วไปที่สามารถทำงานนี้ได้</span><span class="sxs-lookup"><span data-stu-id="c7590-142">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="c7590-143">เลือกบทบาทและหน่วยองค์กรที่เหมาะสม จากนั้นเลือก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="c7590-143">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="c7590-144">มีการสร้างสมาชิกทีมทั่วไปและกำหนดให้กับงานนี้</span><span class="sxs-lookup"><span data-stu-id="c7590-144">A generic team member is created and assigned to this task.</span></span> 
5. <span data-ttu-id="c7590-145">ทำซ้ำขั้นตอนที่ 1-4 สำหรับ **งาน B** อย่างไรก็ตาม **งาน B** ต้องมีการกำหนดบทบาทและหน่วยองค์กรสำหรับสมาชิกในกลุ่มคนทั่วไปที่แตกต่างจาก **งาน A**</span><span class="sxs-lookup"><span data-stu-id="c7590-145">Repeat steps 1-4 for **Task B**. However, **Task B** must have a different role and organizational unit assigned for the generic team member than **Task A**.</span></span> 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="c7590-146">ตั้งค่าบทบาทและหน่วยองค์กรสำหรับงานของโครงการ</span><span class="sxs-lookup"><span data-stu-id="c7590-146">Set up the role and organization unit for a project task</span></span>
<span data-ttu-id="c7590-147">ทำตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์เพื่อตั้งค่าบทบาทและหน่วยองค์กรสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="c7590-147">Complete the following steps to set up a role and organizational unit for a task.</span></span>

1. <span data-ttu-id="c7590-148">หลังจากที่คุณสร้าง **งาน A** เลือกงาน และจากนั้น เลือกไอคอน **i** เพื่อเปิดบานหน้าต่าง **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="c7590-148">After you create **Task A**, select the task, and then select the **i** icon to open the **Task Details** pane.</span></span> 
2. <span data-ttu-id="c7590-149">บนบานหน้าต่าง **รายละเอียดงาน** เลื่อนไปที่ด้านล่าง แล้วเลือก **ดูรายละเอียด** เพื่อเปิดหน้า **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="c7590-149">On the **Task Details** pane, scroll to the bottom and select **View Details** to open the **Task Details** page.</span></span>
3. <span data-ttu-id="c7590-150">บนหน้า **รายละเอียดงาน** ใน **บทบาท** และ **หน่วยองค์กร** เพิ่มค่าที่จำเป็นในการดำเนินงานนี้สำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c7590-150">On the **Task Details** page, in **Role** and **Organizational Unit**, add the values that are required to perform this task for the resource.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="c7590-151">ถ้าคุณดำเนินสถานการณ์นี้ให้เสร็จสมบูรณ์โดยใช้ข้อมูลสาธิต Project Operations ให้เลือก **หัวหน้าที่ปรึกษา** สำหรับบทบาท และ **Fabrikam US** เป็นหน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="c7590-151">If you complete this scenario using the Project Operations demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

4. <span data-ttu-id="c7590-152">เลือก **งาน B** และจากนั้น เลือกงาน</span><span class="sxs-lookup"><span data-stu-id="c7590-152">Select **Task B**, and then select the task.</span></span>
5. <span data-ttu-id="c7590-153">เลือกไอคอน **i** เพื่อเปิดบานหน้าต่าง **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="c7590-153">Select the **i** icon to open **Task Details** pane.</span></span> 
6. <span data-ttu-id="c7590-154">บนบานหน้าต่าง **รายละเอียดงาน** เลื่อนไปที่ด้านล่าง แล้วเลือก **ดูรายละเอียด** เพื่อเปิดหน้า **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="c7590-154">On the **Task Details** pane, scroll to the bottom and select **View details** to open the **Task Details** page.</span></span>
7. <span data-ttu-id="c7590-155">บนหน้า **รายละเอียดงาน** ใน **บทบาท** และ **หน่วยองค์กร** เพิ่มค่าที่จำเป็นของทรัพยากรที่จะดำเนินงานนี้</span><span class="sxs-lookup"><span data-stu-id="c7590-155">On the **Task Details** page, in **Role** and **Organizational Unit**, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="c7590-156">ค่าใน **บทบาท** และ **หน่วยองค์กร** สำหรับ **งาน B** ต้องแตกต่างจากค่าสำหรับ **งาน A**</span><span class="sxs-lookup"><span data-stu-id="c7590-156">The values in **Role** and **Organizational Unit** for **Task B** must be different than those for **Task A**.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="c7590-157">ถ้าคุณดำเนินสถานการณ์นี้ให้เสร็จสมบูรณ์โดยใช้ข้อมูลสาธิต Project Operations ให้เลือก **ช่างเทคนิคเครือข่าย** สำหรับบทบาท และ **Fabrikam US** เป็นหน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="c7590-157">If you complete this scenario using the Project Operations demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

8. <span data-ttu-id="c7590-158">บันทึกและปิดเพจ **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="c7590-158">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="c7590-159">สมาชิกในกลุ่มคนและพฤติกรรมการประมาณ</span><span class="sxs-lookup"><span data-stu-id="c7590-159">Team member and estimates behavior</span></span> 
<span data-ttu-id="c7590-160">เพื่อทำความเข้าใจพฤติกรรมบนกริด **สมาชิกในกลุ่มคน** และการประมาณ ทำตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="c7590-160">To understand the behavior on the **Team Member** grid and the estimates, complete the following steps.</span></span>

1. <span data-ttu-id="c7590-161">บนกริด **สมาชิกในกลุ่มคน** เลือกสมาชิกในกลุ่มคนทั่วไปสองคน และจากนั้น เลือก **สร้างข้อกำหนด**</span><span class="sxs-lookup"><span data-stu-id="c7590-161">On the **Team Member** grid, select the two generic team members, and then select **Generate Requirements**.</span></span> <span data-ttu-id="c7590-162">การดำเนินการนี้จะสร้างความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c7590-162">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="c7590-163">เลือกแถวของสมาชิกในกลุ่มคนสำหรับ **หัวหน้าที่ปรึกษา** และจากนั้น เลือก **จอง**</span><span class="sxs-lookup"><span data-stu-id="c7590-163">Select the team member row for **Consulting Lead**, and then select **Book**.</span></span> <span data-ttu-id="c7590-164">บอร์ดกำหนดการจะเปิดขึ้นพร้อมรายการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c7590-164">The schedule board opens with a list of resources.</span></span> <span data-ttu-id="c7590-165">เลือกทรัพยากร และจากนั้น เลือก **จอง** เพื่อจองทรัพยากรตามความต้องการนั้น</span><span class="sxs-lookup"><span data-stu-id="c7590-165">Select a resource and then select **Book** to book the resource to that requirement.</span></span>
3. <span data-ttu-id="c7590-166">เลือกแถวของสมาชิกในกลุ่มคนสำหรับ **ช่างเทคนิคเครือข่าย** และจากนั้น เลือก **จอง**</span><span class="sxs-lookup"><span data-stu-id="c7590-166">Select the team member row for **Network Technician**, and then select **Book**.</span></span> <span data-ttu-id="c7590-167">บอร์ดกำหนดการจะเปิดขึ้นพร้อมรายการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c7590-167">The schedule board opens with a list of resources.</span></span> <span data-ttu-id="c7590-168">เลือกทรัพยากรเดียวกันกับข้างต้น และจากนั้น เลือก **จอง** เพื่อจองทรัพยากรตามความต้องการนั้น</span><span class="sxs-lookup"><span data-stu-id="c7590-168">Select the same resource as above and then select **Book** to book the resource to that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="c7590-169">ตารางสมาชิกทีม</span><span class="sxs-lookup"><span data-stu-id="c7590-169">Team Member grid</span></span> 

<span data-ttu-id="c7590-170">บนกริด **สมาชิกในกลุ่มคน** เรกคอร์ดสมาชิกในกลุ่มคนทั่วไปสองรายการจะถูกลบและแทนที่ด้วยทรัพยากรเพียงรายการเดียว</span><span class="sxs-lookup"><span data-stu-id="c7590-170">On the **Team Member** grid, the two generic team member records are deleted and replaced with only one resource.</span></span> <span data-ttu-id="c7590-171">มีชุดของค่าหนึ่งสำหรับทรัพยากรนั้น ซึ่งเป็นชุดของค่าเริ่มต้นสำหรับ **บทบาท** และ **หน่วยองค์กร**</span><span class="sxs-lookup"><span data-stu-id="c7590-171">There is one set of values for that resource, which are a default set of values for **Role** and **Organizational Unit**.</span></span>

<span data-ttu-id="c7590-172">เมื่อคุณขยายแถวสำหรับเรกคอร์ดสมาชิกในกลุ่มคนนั้น คุณจะเห็นการมอบหมายงานที่แตกต่างกันในเรกคอร์ดสมาชิกในกลุ่มคนสำหรับทั้งสองงาน</span><span class="sxs-lookup"><span data-stu-id="c7590-172">When you expand the row for that team member record, you can see distinct assignments on the team member record for both tasks.</span></span> <span data-ttu-id="c7590-173">แถวการมอบหมายแต่ละแถวมีค่าเฉพาะงานสำหรับ **บทบาท** และ **หน่วยองค์กร**</span><span class="sxs-lookup"><span data-stu-id="c7590-173">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="c7590-174">ตารางประมาณการ</span><span class="sxs-lookup"><span data-stu-id="c7590-174">Estimates grid</span></span> 

<span data-ttu-id="c7590-175">บนกริด **การประมาณ** การมอบหมายทั้งสองรายการสำหรับทรัพยากรเดียวกันถูกกำหนดราคาโดยแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="c7590-175">On the **Estimates** grid, both assignments for the same resource are priced differently.</span></span> <span data-ttu-id="c7590-176">การมอบหมายงานสำหรับทรัพยากรใน **งาน A** ถูกกำหนดราคาโดยใช้ค่าแอตทริบิวต์ **บทบาท** ของ **หัวหน้าที่ปรึกษา**</span><span class="sxs-lookup"><span data-stu-id="c7590-176">The assignment for the resource on **Task A** is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="c7590-177">การมอบหมายงานสำหรับทรัพยากรเดียวกันใน **งาน B** ถูกกำหนดราคาโดยใช้ค่าแอตทริบิวต์ **บทบาท** ของ **ช่างเทคนิคเครือข่าย**</span><span class="sxs-lookup"><span data-stu-id="c7590-177">The assignment for the same resource on **Task B** is priced using the **Role** attribute value of **Network Technician**.</span></span>
