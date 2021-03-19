---
title: กำหนดการโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการสร้างกำหนดการ
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8f1a0b0ed610ade094546782a1fa517682a390e4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284020"
---
# <a name="project-schedules"></a><span data-ttu-id="b7ccf-103">กำหนดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-103">Project schedules</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b7ccf-104">กำหนดการโครงการบอกให้ทราบว่าจะต้องทำงานใดให้เสร็จสิ้น ต้องใช้ทรัพยากรใดบ้าง และกรอบเวลาที่งานนั้น ๆ จะต้องเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="b7ccf-104">A project schedule communicates what work must be completed, which resources will do the work, and the timeframe that the work must be finished in.</span></span> <span data-ttu-id="b7ccf-105">ซึ่งสะท้อนถึงกระบวนงานทั้งหมดที่เกี่ยวข้องกับระยะเวลาส่งมอบโครงการ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-105">It reflects all the work that is associated with delivering the project on time.</span></span> <span data-ttu-id="b7ccf-106">ใน Dynamics 365 Project Service Automation คุณจะสามารถสร้างกำหนดการโครงการได้โดยการแยกรายละเอียดของงานลงในงานที่จัดการได้ ประมาณช่วงเวลาที่ต้องการใช้ในแต่ละงาน กำหนขอบเขตงาน กำหนดระยะเวลางาน และประมาณการทรัพยากรทั่วไปที่จะใช้ในงาน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-106">In Dynamics 365 Project Service Automation, you create a project schedule by breaking the work down into manageable tasks, estimating the time that is required to do each task, setting task dependencies, setting task durations, and estimating the generic resources that will do the tasks.</span></span> <span data-ttu-id="b7ccf-107">กำหนดการโครงการจะถูกสร้างขึ้นบนแท็บ **Schedule** ของหน้าโครงการ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-107">The project schedule is created on the **Schedule** tab of the project page.</span></span>
 
## <a name="tasks"></a><span data-ttu-id="b7ccf-108">งาน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-108">Tasks</span></span>

<span data-ttu-id="b7ccf-109">ขั้นแรกในการสร้างกำหนดการโครงการคือการแยกรายละเอียดงานเป็นส่วนที่จัดการได้</span><span class="sxs-lookup"><span data-stu-id="b7ccf-109">The first step in creating a project schedule is to break the work down into manageable portions.</span></span> <span data-ttu-id="b7ccf-110">กำหนดการใน PSA สนับสนุนลักษณะการทำงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b7ccf-110">The schedule in PSA supports the following features:</span></span>

- <span data-ttu-id="b7ccf-111">โหนดรากของโครงการ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-111">Project root node</span></span>
- <span data-ttu-id="b7ccf-112">งานสรุปหรือคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="b7ccf-112">Summary or container tasks</span></span>
- <span data-ttu-id="b7ccf-113">งานโหนดปลายสุด</span><span class="sxs-lookup"><span data-stu-id="b7ccf-113">Leaf node tasks</span></span>

### <a name="project-root-node"></a><span data-ttu-id="b7ccf-114">โหนดรากของโครงการ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-114">Project root node</span></span>

<span data-ttu-id="b7ccf-115">โหนดรากของโครงการ คือ การสรุปงานระดับสูงสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-115">The project root node is the top-level summary task for the project.</span></span> <span data-ttu-id="b7ccf-116">มีการสร้างงานโครงการอื่นๆทั้งหมดภายใต้นั้น</span><span class="sxs-lookup"><span data-stu-id="b7ccf-116">All other project tasks are created under it.</span></span> <span data-ttu-id="b7ccf-117">ชื่อของโหนดรากจะถูกตั้งค่าเป็นชื่อโครงการเสมอ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-117">The name of the root node is always set to the project name.</span></span> <span data-ttu-id="b7ccf-118">ความพยายาม วันที่ และระยะเวลาของโหนดรากจะถูกสรุปตามค่าที่อยู่ในลำดับด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="b7ccf-118">The effort, dates, and duration of the root node are summarized based on the values in the hierarchy below it.</span></span> <span data-ttu-id="b7ccf-119">คุณไม่สามารถแก้ไขคุณสมบัติของโหนดรากได้</span><span class="sxs-lookup"><span data-stu-id="b7ccf-119">You can't edit the properties of the root node.</span></span> <span data-ttu-id="b7ccf-120">และคุณไม่สามารถลบโหนดรากได้</span><span class="sxs-lookup"><span data-stu-id="b7ccf-120">You also can't delete the root node.</span></span>

### <a name="summary-or-container-tasks"></a><span data-ttu-id="b7ccf-121">งานสรุปหรือคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="b7ccf-121">Summary or container tasks</span></span> 

<span data-ttu-id="b7ccf-122">คุณสามารถปรับเปลี่ยนงานปลึกย่อยหรืองานคอนเทนเนอร์ด้านล่างได้</span><span class="sxs-lookup"><span data-stu-id="b7ccf-122">Summary tasks have sub-tasks or container tasks under them.</span></span> <span data-ttu-id="b7ccf-123">ซึ่งไม่มมีความพยายามของงานหรือต้นทุนใด ๆ ทั้งสิ้น</span><span class="sxs-lookup"><span data-stu-id="b7ccf-123">They have no work effort or cost of their own.</span></span> <span data-ttu-id="b7ccf-124">แต่ความพยายามของงานและต้นทุนของงาน เป็นการสะสมความพยายามของงานและต้นทุนของงานคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="b7ccf-124">Instead, their work effort and cost are a rollup of the work effort and cost of their container tasks.</span></span> <span data-ttu-id="b7ccf-125">วันที่เริ่มต้นแรกสุดของการสรุปงานเป็นวันเริ่มต้นของงานคอนเทนเนอร์ และวันที่สิ้นสุดงานเป็นวันที่สิ้นสุดงานคอนเทนเนอร์เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-125">The start date of the summary task is the start date of the container tasks, and the end date is the end date of the container tasks.</span></span> <span data-ttu-id="b7ccf-126">คุณสามารถปรับเปลี่ยนชื่อของการสรุปงาน แต่คุณไม่สามารถปรับเปลี่ยนคุณสมบัติการจัดกำหนดการในส่วนของความพยายาม วันที่ และระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="b7ccf-126">The name of a summary task can be edited, but scheduling properties (effort, dates, and duration) can't be edited.</span></span> <span data-ttu-id="b7ccf-127">ถ้าคุณลบการสรุปงาน เท่ากับคุณลบงานคอนเทนเนอร์ทั้งหมดด้วย</span><span class="sxs-lookup"><span data-stu-id="b7ccf-127">If you delete a summary task, you also delete all its container tasks.</span></span>

### <a name="leaf-node-tasks"></a><span data-ttu-id="b7ccf-128">งานโหนดปลายสุด</span><span class="sxs-lookup"><span data-stu-id="b7ccf-128">Leaf node tasks</span></span>

<span data-ttu-id="b7ccf-129">งานโหนดปลายสุดแสดงถึงงานที่ละเอียดที่สุดในโครงการ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-129">Leaf node tasks represent the most granular work on the project.</span></span> <span data-ttu-id="b7ccf-130">มีข้อมูลการประมาณการความพยายาม ทรัพยากร แผนงานของวันเริ่มต้นและวันสิ้นสุด และระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="b7ccf-130">They have an estimated effort, resources, planned start and end dates, and a duration.</span></span>
 
## <a name="creating-a-task-hierarchy"></a><span data-ttu-id="b7ccf-131">การสร้างลำดับขั้นของงาน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-131">Creating a task hierarchy</span></span>

<span data-ttu-id="b7ccf-132">คุณสามารถสร้างลำดับขั้นของงานโดยใช้วิธีการต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b7ccf-132">You can create a task hierarchy by using the following options:</span></span>

- <span data-ttu-id="b7ccf-133">กดปุ่ม **Add task**</span><span class="sxs-lookup"><span data-stu-id="b7ccf-133">**Add task** button</span></span>
- <span data-ttu-id="b7ccf-134">กดปุ่ม **Indent task**</span><span class="sxs-lookup"><span data-stu-id="b7ccf-134">**Indent task** button</span></span>
- <span data-ttu-id="b7ccf-135">กดปุ่ม **Outdent task**</span><span class="sxs-lookup"><span data-stu-id="b7ccf-135">**Outdent task** button</span></span>
- <span data-ttu-id="b7ccf-136">กดปุ่ม **Move up** และ **Move down**</span><span class="sxs-lookup"><span data-stu-id="b7ccf-136">**Move up** and **Move down** buttons</span></span>
- <span data-ttu-id="b7ccf-137">การเข้าถึงและแป้นพิมพ์ลัด</span><span class="sxs-lookup"><span data-stu-id="b7ccf-137">Accessibility and keyboard shortcuts</span></span>

### <a name="add-task"></a><span data-ttu-id="b7ccf-138">การเพิ่มงาน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-138">Add task</span></span>

<span data-ttu-id="b7ccf-139">ปุุ่ม **Add task** จะทำให้คุณสามารถสร้างงานใหม่ในลำดับขั้นของงานได้</span><span class="sxs-lookup"><span data-stu-id="b7ccf-139">The **Add task** button lets you create a new task in the hierarchy.</span></span> <span data-ttu-id="b7ccf-140">ถ้าคุณไม่เลือกตำแหน่ง งานจะถูกวางไว้ที่ตอนท้าย</span><span class="sxs-lookup"><span data-stu-id="b7ccf-140">If you don't select a position, the task is inserted at the end.</span></span> 

<span data-ttu-id="b7ccf-141">รหัสของกำหนดการจะถูกกำหนดในทุกงาน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-141">A schedule ID is assigned to every task.</span></span> <span data-ttu-id="b7ccf-142">รหัสของกำหนดการแสดงถึงความลึกของงานและตำแหน่งในลำดับขั้น</span><span class="sxs-lookup"><span data-stu-id="b7ccf-142">The schedule ID represents the task's depth and position in the hierarchy.</span></span> <span data-ttu-id="b7ccf-143">โดยการใช้หมายเลขเค้าร่าง</span><span class="sxs-lookup"><span data-stu-id="b7ccf-143">It uses outline numbering.</span></span> <span data-ttu-id="b7ccf-144">สำหรับงานในระดับแรกภายใต้โหนดรากของโครงการ จะใช้ชุดการกำหนดหมายเลขของ 1, 2, 3 และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-144">For tasks in the first level under the project root node, a numbering scheme of 1, 2, 3, and so on, is used.</span></span> <span data-ttu-id="b7ccf-145">สำหรับงานภายใต้ระดับแรก จะใช้ชุดการกำหนดหมายเลขของ 1.1, 1.2, 1.3 และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-145">For tasks under the first level, a numbering scheme of 1.1, 1.2, 1.3, and so on, is used.</span></span>

### <a name="indent-task"></a><span data-ttu-id="b7ccf-146">การย่อหน้างาน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-146">Indent task</span></span>

<span data-ttu-id="b7ccf-147">เมื่อมีการย่อหน้างาน เป็นการทำให้ข้อมูลนั้นกลายเป็นข้อมูลลูกของงานที่อยู่ด้านบน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-147">When a task is indented, it becomes a child of the task that is directly above it.</span></span> <span data-ttu-id="b7ccf-148">รหัสกำหนดการของงานจะถูกคำนวณใหม่ตามรหัสกำหนดการของข้อมูลหลักใหม่ และตามชุดการกำหนดหมายเลขเค้าร่าง</span><span class="sxs-lookup"><span data-stu-id="b7ccf-148">The schedule ID of the task is then recalculated so that it's based on the schedule ID of its new parent and follows the outline numbering scheme.</span></span> <span data-ttu-id="b7ccf-149">ในตอนนี้งานหลักจะกลายเป็นงานที่สรุปหรืองานคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="b7ccf-149">The parent task is now a summary task or a container task.</span></span> <span data-ttu-id="b7ccf-150">ดังนั้น จึงเป็นการสะสมงานลูกของงานนั้น ๆ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-150">Therefore, it becomes a rollup of its child tasks.</span></span>

### <a name="outdent-task"></a><span data-ttu-id="b7ccf-151">งานที่เยื้องไปด้านหน้า</span><span class="sxs-lookup"><span data-stu-id="b7ccf-151">Outdent task</span></span> 

<span data-ttu-id="b7ccf-152">เมื่อคุณเยื้องงานไปด้านหน้า ก็จะไม่เป็นงานลูกของงานที่เคยเป็นงานหลักอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="b7ccf-152">When a task is outdented, it's no longer a child of the task that was its parent.</span></span> <span data-ttu-id="b7ccf-153">รหัสของกำหนดการก็จะถูกคำนวณใหม่ ซึ่งจะสะท้อนถึงการอัพเดตความลึกของงานและตำแหน่งในลำดับขั้น</span><span class="sxs-lookup"><span data-stu-id="b7ccf-153">The schedule ID is then recalculated so that it reflects the task's updated depth and position in the hierarchy.</span></span> <span data-ttu-id="b7ccf-154">ความพยายาม ต้นทุน และวันที่ของงานงานหลักก่อนหน้านี้จะถูกคำนวณใหม่โดยแยกออกจากงานนี้</span><span class="sxs-lookup"><span data-stu-id="b7ccf-154">The effort, cost, and dates of the previous parent task are recalculated so that they don't include this task.</span></span>

### <a name="move-up-and-move-down"></a><span data-ttu-id="b7ccf-155">เลื่อนขึ้นและเลื่อนลง</span><span class="sxs-lookup"><span data-stu-id="b7ccf-155">Move up and Move down</span></span> 

<span data-ttu-id="b7ccf-156">ปุ๋ม **เลื่อนขึ้น** และ **เลื่อนลง** จะเปลี่ยนตำแหน่งของงานภายในลำดับชั้นหลัก</span><span class="sxs-lookup"><span data-stu-id="b7ccf-156">The **Move up** and **Move down** buttons change the position of a task within its parent hierarchy.</span></span> <span data-ttu-id="b7ccf-157">การเปลี่ยนแปลงนี้ไม่มีผลกับความพยายามของงาน ต้นทุน วันที่ หรือระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="b7ccf-157">Changes of this type don't affect the task's effort, cost, dates, or duration.</span></span> <span data-ttu-id="b7ccf-158">จะกระทบเฉพาะรหัสของกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-158">Only the task's schedule ID is affected.</span></span> <span data-ttu-id="b7ccf-159">รหัสของกำหนดการก็จะถูกคำนวณใหม่ ซึ่งจะสะท้อนถึงตำแหน่งใหม่ของงานในงานหลักของงานลูกนั้น ๆ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-159">The schedule ID is recalculated so that it reflects the task's new position in the parent's list of child tasks.</span></span>

### <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="b7ccf-160">การเข้าถึงและแป้นพิมพ์ลัด</span><span class="sxs-lookup"><span data-stu-id="b7ccf-160">Accessibility and keyboard shortcuts</span></span>

<span data-ttu-id="b7ccf-161">ตาราง **Schedule** สามารถใช้งานได้และสามารถใช้กับโปรแกรมอ่านหน้าจอ เช่น Narrator, JAWS, or NVDA ได้</span><span class="sxs-lookup"><span data-stu-id="b7ccf-161">The **Schedule** grid is fully accessible and can be used with screen readers such as Narrator, JAWS, or NVDA.</span></span> <span data-ttu-id="b7ccf-162">คุณสามารถเลื่อนผ่านพื้นที่ของตารางโดยการใช้ปุ่มลูกศร เช่นเดียวกับใน Microsoft Excel คุณสามารถใช้กดปุ่ม Tab เพื่อยกระดับกาารตอบโต้กับ UI elements และคุณสามารถใช้ปุ่มลูกศรชี้ลง ปุ่ม Enter หรือ Spacebar ในการเลือกและเรียกใช้ drop-down menus</span><span class="sxs-lookup"><span data-stu-id="b7ccf-162">You can move through the grid area by using arrow keys (as in Microsoft Excel), you can use the Tab key to advance through the interactive UI elements, and you can use the Down arrow key, the Enter key, or the Spacebar to select and invoke the drop-down menus.</span></span> <span data-ttu-id="b7ccf-163">ส่วนหัวของคอลัมน์ก็สามารถตอบโต้ได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-163">The column headers are also interactive.</span></span> <span data-ttu-id="b7ccf-164">คุณสามารถซ่อนหรือแสดงคอลัมน์ โดยการใช้ปุ่ม Tab และปุ่มลูกศร ในการเลื่อนผ่านส่วนหัวของคอลัมน์ และใช้ปุ่ม action บนแถบเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-164">You can hide and show columns, use the Tab key and arrow keys to move through the column headers, and use the action buttons on the toolbar.</span></span> <span data-ttu-id="b7ccf-165">นอกจากนี้ คุณสามารถใช้ทางลัดของคีย์บอร์ดดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b7ccf-165">In addition, you can use the following keyboard shortcuts:</span></span>

- <span data-ttu-id="b7ccf-166">**การรีเฟรช**: ALT+SHIFT+F5</span><span class="sxs-lookup"><span data-stu-id="b7ccf-166">**Refresh**: ALT+SHIFT+F5</span></span>
- <span data-ttu-id="b7ccf-167">**การเพิ่ม**: ALT+SHIFT+Insert</span><span class="sxs-lookup"><span data-stu-id="b7ccf-167">**Add**: ALT+SHIFT+Insert</span></span>
- <span data-ttu-id="b7ccf-168">**การลบ**: ALT+SHIFT+Delete</span><span class="sxs-lookup"><span data-stu-id="b7ccf-168">**Delete**: ALT+SHIFT+Delete</span></span>
- <span data-ttu-id="b7ccf-169">**การเลื่อนขึ้นลง**: ALT+SHIFT+Up/Down arrows</span><span class="sxs-lookup"><span data-stu-id="b7ccf-169">**Move up/down**: ALT+SHIFT+Up/Down arrows</span></span>
- <span data-ttu-id="b7ccf-170">**การย่อหน้าและการเยื้องไปด้านหน้า**: ALT_SHIFT+Left/Right arrows</span><span class="sxs-lookup"><span data-stu-id="b7ccf-170">**Indent/Outdent**: ALT_SHIFT+Left/Right arrows</span></span>
- <span data-ttu-id="b7ccf-171">**การเพิ่มหรือลดลำดับ**: ALT+SHIFT+Plus/Minus keys</span><span class="sxs-lookup"><span data-stu-id="b7ccf-171">**Expand/Collapse Hierarchies**: ALT+SHIFT+Plus/Minus keys</span></span>

## <a name="task-attributes"></a><span data-ttu-id="b7ccf-172">แอตทริบิวต์งาน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-172">Task attributes</span></span>

<span data-ttu-id="b7ccf-173">ชื่อของงานแสดงว่างานต้องเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b7ccf-173">A task's name describes the work that must be completed.</span></span> <span data-ttu-id="b7ccf-174">ใน PSA คุณลักษณะที่เกี่ยวข้องกับงานจะบอกถึงกำหนดการของงานและความต้องการแรงงาน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-174">In PSA, the attributes that are associated with a task describe the schedule of the task and its staffing requirements.</span></span>

> ![แอตทริบิวต์งาน](media/project-2.png)
 
### <a name="schedule-attributes"></a><span data-ttu-id="b7ccf-176">แอททริบิวต์กำหนดการ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-176">Schedule attributes</span></span>

<span data-ttu-id="b7ccf-177">คุณสมบัติ **ความพยายาม**, **วันเริ่มต้น**, **วันสิ้นสุด**, and **ระยะเวลา** เป็นตัวกำหนดกำหนดการของงาน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-177">The **Effort**, **Start date**, **End date**, and **Duration** attributes define the schedule for the task.</span></span>

<span data-ttu-id="b7ccf-178">คุณลักษณะของกำหนดการเพิ่มเติม ได้แก่:</span><span class="sxs-lookup"><span data-stu-id="b7ccf-178">Additional schedule attributes include:</span></span>

- <span data-ttu-id="b7ccf-179">**ชั่วโมงการทำงาน** ป้อนค่าประมาณของชั่วโมงการทำงานที่ต้องการใช้ในการทำงานให้สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-179">**Effort hours**: Enter an estimate of the hours that are required to complete the task.</span></span> 
- <span data-ttu-id="b7ccf-180">**ระยะเวลา** ระบุจำนวนวันทำงานที่ต้องการใช้ในการทำงานให้สำเร็จ </span><span class="sxs-lookup"><span data-stu-id="b7ccf-180">**Duration**: Specify the number of workdays that are required to complete the task.</span></span>
- <span data-ttu-id="b7ccf-181">**รหัสของกำหนดการ** รหัสที่ถูกสร้างขึ้นเองโดยอัตโนมัติจะถูกใช้ในการสั่งงานที่อยู่ในลำดับ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-181">**Schedule ID**: This automatically generated ID is used to order tasks in the hierarchy.</span></span> <span data-ttu-id="b7ccf-182">ขอบเขตระหว่างงานจะช่วยจัดการคำสั่งจริงในส่วนที่งานนั้นต้องดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-182">Dependencies between the tasks manage the actual order in which the tasks are worked on.</span></span>
 
### <a name="staffing-attributes"></a><span data-ttu-id="b7ccf-183">แอตทริบิวต์การสรรหาพนักงาน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-183">Staffing attributes</span></span>

<span data-ttu-id="b7ccf-184">คุณลักษณะของการจ้างงานจะสามารถใช้ได้ในฟิลด์ **Resources** ในกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-184">Staffing attributes are accessed through the **Resources** field in the schedule.</span></span> <span data-ttu-id="b7ccf-185">คุณมาสารถหาทรัพยากรที่มีอยู่ หรือคลิก **Create** และในหน้าต่าง **Quick Create** เพิ่มข้อมูลสมาชิกทีมของโครงการเป็นทรัพยากรใหม่</span><span class="sxs-lookup"><span data-stu-id="b7ccf-185">You can either search for an existing resource, or click **Create** and in the **Quick Create** pane, add a project team member as a new resource.</span></span>

<span data-ttu-id="b7ccf-186">ฟิลด์ **Role**, **Resourcing Unit**, and **Position Name** จะถูกใช้ในการอธิบายความต้องการของแรงงานสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-186">The **Role**, **Resourcing Unit**, and **Position Name** fields are used to describe the staffing requirements for the task.</span></span> <span data-ttu-id="b7ccf-187">คุณลักษณะเหล่านี้ของพนักงานและกำหนดการงานจะถูกใช้ในการเสาะหาทรัพยากรที่มีอยู่เพื่อมาทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="b7ccf-187">These staffing attributes together with the task schedule are used to find available resources to do this task.</span></span>

<span data-ttu-id="b7ccf-188">**บทบาท** ระบุชนิดของทรัพยากรที่ต้องการใช้ในงานนี้</span><span class="sxs-lookup"><span data-stu-id="b7ccf-188">**Role** - Specify the type of resource that is required to do the task.</span></span>

<span data-ttu-id="b7ccf-189">**Resourcing unit** ระบุว่าหน่วยงานนั้นจะได้รับการมอบหมายงานจาก</span><span class="sxs-lookup"><span data-stu-id="b7ccf-189">**Resourcing unit** - Specify the unit that resources for the task should be assigned from.</span></span> <span data-ttu-id="b7ccf-190">คุณลักษณะนี้จะกระทบกับต้นทุนและการประมาณการยอดขายสำหรับงาน ถ้าต้นทุนและอัตราค่าบริการสำหรับการสรรหาทรัพยากรที่ถูกกำหนดตามหน่วยของการสรรหาทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="b7ccf-190">This attribute affects the cost and sales estimate for the task if the cost and bill rate for the resource are set based on resourcing units.</span></span>

<span data-ttu-id="b7ccf-191">**Position name** ป้อนชื่อเกี่ยวกับทรัพยากรที่เข้าใจได้ง่ายเพื่อทำหน้าที่เป็นสัญลักษณ์ของทรัพยากรที่จะใช้ในงาน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-191">**Position name** – Enter a friendly name for the generic resource that serves as a placeholder for the resource that will ultimately do the work.</span></span>

<span data-ttu-id="b7ccf-192">ฟิลด์ **Resources** จะยึดกับชื่อตำแหน่งของทรัพยากรที่เกี่ยวข้องหรือทรัพยากรที่มีชื่อแล้วเมื่อค้นพบชื่อใดชื่อหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b7ccf-192">The **Resources** field holds the position name of the generic resource or named resource when one is found.</span></span>

<span data-ttu-id="b7ccf-193">ฟิลด์ **Category** จะยึดค่าที่ระบุชนิดของงานอย่างกว้างที่งานนั้นสามารถรวมเข้าไปได้</span><span class="sxs-lookup"><span data-stu-id="b7ccf-193">The **Category** field holds the values that indicate a broader type of work that the task can be grouped into.</span></span> <span data-ttu-id="b7ccf-194">ฟิลด์นี้ไม่กระทบกับตารางงานหรือการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-194">This field doesn't affect scheduling or staffing.</span></span> <span data-ttu-id="b7ccf-195">ใช้สำหรับการรายงานเท่านั้น </span><span class="sxs-lookup"><span data-stu-id="b7ccf-195">It's used only for reporting.</span></span>

### <a name="task-dependencies"></a><span data-ttu-id="b7ccf-196">การขึ้นต่อกันของงาน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-196">Task dependencies</span></span> 

<span data-ttu-id="b7ccf-197">คุณสามารถใช้กำหนดการใน PSA สร้างความสัมพันธ์ก่อนหน้าระหว่างงานนั้น</span><span class="sxs-lookup"><span data-stu-id="b7ccf-197">You can use the schedule in PSA to create predecessor relationships between tasks.</span></span> <span data-ttu-id="b7ccf-198">ฟิลด์ **Predecessor** ภายใต้ **Tasks** จะนำหนึ่งค่าหรือมากกว่านั้นไปใช้ในการกำหนดการทำงานที่มีงานนั้นเป็นส่วนหนึ่งอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="b7ccf-198">The **Predecessor** field under **Tasks** takes one or more values to indicate the tasks that a task depends on.</span></span> <span data-ttu-id="b7ccf-199">เมื่อมีการกำหนดงานก่อนหน้าให้กับงาน งานนั้นจะสามารถเริ่มต้นหลังจากงานก่อนหน้านั้นทั้งหมดเสร็จสมบูรณ์แล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b7ccf-199">When predecessor values are assigned to a task, the task can start only after all the predecessor tasks have been completed.</span></span> <span data-ttu-id="b7ccf-200">วันที่เริ่มต้นที่วางแผนไว้ของงานจะถูกกำหนดโดยอัตโนมัติให้เป็นวันที่หลังสุดของงานก่อนหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="b7ccf-200">Because of the dependency, the planned start date of the task is reset to the date when the predecessor tasks are completed.</span></span>

<span data-ttu-id="b7ccf-201">โหมดงานไม่มีผลกระทบใดๆ ในการอัพเดตที่ใช้ในการกำหนดวันเริ่มต้นและวันสิ้นสุดของงานก่อนหน้านี้หรืองานอิสระ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-201">The task mode has no effect on updates that are made to the start and end dates of predecessor/dependent tasks.</span></span>

## <a name="task-mode"></a><span data-ttu-id="b7ccf-202">โหมดงาน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-202">Task mode</span></span> 

<span data-ttu-id="b7ccf-203">โหมดงานจะกำหนดการจัดกำหนดการงานระดับงานโหนดปลายสุด:</span><span class="sxs-lookup"><span data-stu-id="b7ccf-203">The task mode determines the scheduling of leaf node tasks.</span></span> <span data-ttu-id="b7ccf-204">PSA สนับสนุนงานสองแบบเพื่อทุกการงาน คือ การกำหนดตารางงานแบบอัตโนมัติและแบบกำหนดด้วยตัวเอง</span><span class="sxs-lookup"><span data-stu-id="b7ccf-204">PSA supports two task modes for every task: automatic scheduling and manual scheduling.</span></span>

### <a name="auto-scheduling"></a><span data-ttu-id="b7ccf-205">การกำหนดตารางงานอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-205">Auto-scheduling</span></span> 
 
<span data-ttu-id="b7ccf-206">เมื่อโหมดงานถูกกำหนดเป็น **Automatically Scheduled** ระบบการจัดกำหนดการจะใช้กฎการจัดกำหนดการบนคุณลักษณะของานเพื่อระบุกำหนดการของงานนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-206">When task mode is set to **Automatically Scheduled** for a task, the task scheduling engine uses the scheduling rules on task attributes to determine the schedule for the task.</span></span>

#### <a name="scheduling-rules"></a><span data-ttu-id="b7ccf-207">กฎการกำหนดตารางงาน</span><span class="sxs-lookup"><span data-stu-id="b7ccf-207">Scheduling rules</span></span>

<span data-ttu-id="b7ccf-208">เพื่อเป็นการกำหนดค่าเริ่มต้น งานโหนดปลายสุดที่ไม่มีรายการก่อนหน้าจะถูกตั้งค่าโดยอัตโนมัติให้เป็นวันที่เริ่มต้นการจัดกำหนดการของโครงการ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-208">By default, if a leaf node task doesn't have predecessors, its start date is set to the project's scheduled start date.</span></span> <span data-ttu-id="b7ccf-209">ระยะเวลาของงานโหนดปลายสุดจะคำนวณเป็นจำนวนวันทำงานระหว่างวันที่เริ่มต้นและสิ้นสุดเสมอ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-209">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="b7ccf-210">เมื่องานถูกจัดการกำหนดการอัตโนมัติแล้ว กลไกจัดการกำหนดการจะเป็นไปตามกฎเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="b7ccf-210">When a task is automatically scheduled, the scheduling engine follows these rules:</span></span>

- <span data-ttu-id="b7ccf-211">วันที่เริ่มต้นและสิ้นสุดของงานต้องเป็นวันทำงาน ตามปฏิทินการจัดกำหนดการของโครงการ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-211">The start and end dates of the task must be working days, according to the project's scheduling calendar.</span></span> 
- <span data-ttu-id="b7ccf-212">สำหรับงานใด ๆ ที่มีงานก่อนหน้า วันที่เริ่มต้นงานจะถูกกำหนดโดยอัตโนมัติให้เป็นวันที่หลังสุดของงานก่อนหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="b7ccf-212">For any task that has predecessor tasks, the start date is automatically set to the latest end date of its predecessors.</span></span>
- <span data-ttu-id="b7ccf-213">จำนวนของแรงงาน สามารถคำนวณได้จากสูตรนี้ จำนวนบุคลากร × ระยะเวลาการ × จำนวนชั่วโมงในหนึ่งวันทำงานมาตรฐานในปฏิทินโครงการ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-213">Effort is calculated by using this formula: Number of people × Duration × Hours in a standard workday in the project calendar.</span></span>

### <a name="manual-scheduling"></a><span data-ttu-id="b7ccf-214">การจัดกำหนดการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b7ccf-214">Manual scheduling</span></span>

<span data-ttu-id="b7ccf-215">ถ้ากฎของการจัดการกำหนดการอัตโนมัติไม่เหมาะสมกับความต้องการของคุณ คุณสามารถกำหนดโหมดงานเป็น **Manually Scheduled** ได้</span><span class="sxs-lookup"><span data-stu-id="b7ccf-215">If the rules of automatic scheduling don't meet your requirements, you can set the task mode for the task to **Manually Scheduled**.</span></span> <span data-ttu-id="b7ccf-216">การกำหนดนี้จะหยุดกลไกจัดการการจัดกำหนดการจากการคำนวณค่าของคุณลักษณะการจัดกำหนดการอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="b7ccf-216">This setting stops the scheduling engine from calculating the values of other scheduling attributes.</span></span> <span data-ttu-id="b7ccf-217">หากไม่มีโหมดงาน หากคุณตั้งค่างานก่อนหน้านี้บนคำสั่งงาน จะทำให้กระทบกับวันเริ่มต้นงานของงานอิสระทุกครั้ง</span><span class="sxs-lookup"><span data-stu-id="b7ccf-217">Regardless of the task mode, if you set predecessors on tasks, you always affect the dependent task's start date.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]