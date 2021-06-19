---
title: จัดกำหนดการโครงการที่มีโครงสร้างการแบ่งงาน
description: วิธีการจัดกำหนดการโครงการที่มีโครงสร้างการแบ่งงานใน Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 027bcbc8995ed39af78c7ff9b1028f401c3b0d4d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008604"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="6683d-103">จัดกำหนดการโครงการที่มีโครงสร้างการแบ่งงาน (Project Service)</span><span class="sxs-lookup"><span data-stu-id="6683d-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="6683d-104">กำหนดการโครงการติดต่อกับงานที่ต้องการดำเนินการ ทรัพยากรที่จะดำเนินงาน และกรอบเวลาที่งานจำเป็นต้องเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6683d-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="6683d-105">กำหนดการของโครงการสะท้อนถึงงานทั้งหมดที่เกี่ยวข้องกับการจัดส่งโครงการที่ตรงเวลา</span><span class="sxs-lookup"><span data-stu-id="6683d-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="6683d-106">หนึ่งในขั้นตอนแรกในระยะเริ่มต้นของโครงการคือ การสร้างกำหนดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="6683d-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="6683d-107">เมื่อต้องการสร้างกำหนดการโครงการ คุณต้องสร้างโครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="6683d-108">สร้างโครงสร้างโครงการที่มีโครงสร้างการแบ่งงานซึ่งช่วยคุณ:</span><span class="sxs-lookup"><span data-stu-id="6683d-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="6683d-109">แบ่งงานออกเป็นงานที่สามารถจัดการได้ง่าย</span><span class="sxs-lookup"><span data-stu-id="6683d-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="6683d-110">ประเมินเวลาที่ใช้ในการดำเนินงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6683d-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="6683d-111">ตั้งค่าการขึ้นต่อกันของงานและระยะเวลาของงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="6683d-112">กำหนดบทบาทที่จำเป็นในการดำเนินงานแต่ละงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6683d-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="6683d-113">กำหนดการของโครงการในโครงสร้างการแบ่งงานมีลักษณะที่ปรากฏและความรู้สึกที่คุ้นเคย ดำเนินการให้สมบูรณ์ด้วยแผนภูมิ Gantt แบบโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="6683d-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="6683d-114">สร้างโครงสร้างการแบ่งงานสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="6683d-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="6683d-115">สร้างโครงสร้างการแบ่งงานเพื่อแสดงถึงลำดับของงานในโครงการ</span><span class="sxs-lookup"><span data-stu-id="6683d-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="6683d-116">โครงสร้างการแบ่งงานรวมงาน ความต้องการสำหรับงานแต่ละงาน และข้อมูลรายได้และต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6683d-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="6683d-117">ในโครงสร้างการแบ่งงานของคุณ คุณสามารถเพิ่ม:</span><span class="sxs-lookup"><span data-stu-id="6683d-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="6683d-118">ลำดับของงานในลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="6683d-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="6683d-119">งานอื่นๆ ถ้ามี ที่ต้องเสร็จสิ้นก่อนที่จะสามารถเริ่มต้นงานได้</span><span class="sxs-lookup"><span data-stu-id="6683d-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="6683d-120">วันที่เริ่มต้น วันที่สิ้นสุด และระยะเวลาของงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="6683d-121">จำนวนชั่วโมงที่ต้องการสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="6683d-122">ทักษะของผู้ปฏิบัติงานที่จำเป็นใดๆ และการศึกษา</span><span class="sxs-lookup"><span data-stu-id="6683d-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="6683d-123">ผู้ปฏิบัติงานที่ถูกกำหนดให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="6683d-124">รายได้และต้นทุนโดยประมาณ</span><span class="sxs-lookup"><span data-stu-id="6683d-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="6683d-125">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-125">Task types</span></span>  
<span data-ttu-id="6683d-126">คุณจะใช้ชนิดของงานต่อไปนี้มื่อมีการสร้างโครงสร้างการแบ่งงานของคุณ:</span><span class="sxs-lookup"><span data-stu-id="6683d-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="6683d-127">**โหนดรากของโครงการ**</span><span class="sxs-lookup"><span data-stu-id="6683d-127">**Project root node**</span></span> | <span data-ttu-id="6683d-128">งานสรุประดับสูงสุดสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="6683d-128">The top-level summary task for the project.</span></span> <span data-ttu-id="6683d-129">มีการสร้างงานโครงการอื่นๆทั้งหมดภายใต้นั้น</span><span class="sxs-lookup"><span data-stu-id="6683d-129">All other project tasks are created under it.</span></span> <span data-ttu-id="6683d-130">ชื่อของงานรากคือ ชื่อโครงการ</span><span class="sxs-lookup"><span data-stu-id="6683d-130">The name of the root task is the project name.</span></span> <span data-ttu-id="6683d-131">ความพยายาม วันที่ และระยะเวลาของโหนดราก จะขึ้นอยู่กับค่าในลำดับชั้นภายใต้สิ่งนี้</span><span class="sxs-lookup"><span data-stu-id="6683d-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="6683d-132">คุณไม่สามารถแก้ไขคุณสมบัติของโหนดราก หรือลบโหนดรากได้</span><span class="sxs-lookup"><span data-stu-id="6683d-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="6683d-133">**งานสรุปหรือคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="6683d-133">**Summary or container tasks**</span></span> | <span data-ttu-id="6683d-134">งานสรุปคือ งานที่มีงานย่อยอยู่ภายใต้</span><span class="sxs-lookup"><span data-stu-id="6683d-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="6683d-135">งานสรุปไม่มีความพยายามในการทำงานหรือต้นทุนของตัวเองใดๆ</span><span class="sxs-lookup"><span data-stu-id="6683d-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="6683d-136">ความพยายามในการทำงานและต้นทุนเป็นค่าสะสมของงานย่อย</span><span class="sxs-lookup"><span data-stu-id="6683d-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="6683d-137">คุณสามารถเปลี่ยนชื่อของงานสรุป แต่คุณไม่สามารถเปลี่ยนแปลงความพยายาม วันที่ หรือระยะเวลา เนื่องจากสิ่งเหล่านั้นถูกคำนวณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6683d-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="6683d-138">การลบงานสรุป จะลบงานและงานย่อยทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6683d-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="6683d-139">**งานโหนดปลายสุด**</span><span class="sxs-lookup"><span data-stu-id="6683d-139">**Leaf node tasks**</span></span> | <span data-ttu-id="6683d-140">งานโหนดปลายสุดแสดงถึงงานที่มีรายละเอียดมากที่สุดในโครงการ</span><span class="sxs-lookup"><span data-stu-id="6683d-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="6683d-141">มีความพยายามที่ประเมินไว้ หมายเลขทรัพยากรที่วางแผนไว้ วันเริ่มต้นและสิ้นสุดที่วางแผนไว้ และระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="6683d-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="6683d-142">ลำดับชั้นของงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-142">Task hierarchy</span></span>  
 <span data-ttu-id="6683d-143">คุณมีตัวเลือกต่อไปนี้เมื่อมีการสร้างลำดับชั้นของงาน:</span><span class="sxs-lookup"><span data-stu-id="6683d-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="6683d-144">**เพิ่มงาน**</span><span class="sxs-lookup"><span data-stu-id="6683d-144">**Add task**.</span></span>   <span data-ttu-id="6683d-145">คุณสามารถเพิ่มงานที่ตำแหน่งที่คุณเลือกในลำดับชั้นของงานได้</span><span class="sxs-lookup"><span data-stu-id="6683d-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="6683d-146">ถ้าคุณไม่เลือกตำแหน่ง งานใหม่ของคุณปรากฏขึ้นตอนท้าย</span><span class="sxs-lookup"><span data-stu-id="6683d-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="6683d-147">**เยื้องงานเข้า**</span><span class="sxs-lookup"><span data-stu-id="6683d-147">**Indent task**.</span></span>   <span data-ttu-id="6683d-148">เยื้องงานเข้าเพื่อทำให้เป็นงานย่อยของงานโดยตรงที่อยู่ด้านบน</span><span class="sxs-lookup"><span data-stu-id="6683d-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="6683d-149">**งานเยื้องออก**</span><span class="sxs-lookup"><span data-stu-id="6683d-149">**Outdent task**.</span></span>   <span data-ttu-id="6683d-150">เยื้องงานออกเพื่อดำเนินงาน ดังนั้นจึงไม่เป็นงานย่อยของงานหลักของต้นฉบับอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="6683d-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="6683d-151">**ย้ายขึ้นและย้ายลง**</span><span class="sxs-lookup"><span data-stu-id="6683d-151">**Move up and Move down**.</span></span>   <span data-ttu-id="6683d-152">ย้ายงานขึ้นและลงในลำดับชั้นของงานหลัก</span><span class="sxs-lookup"><span data-stu-id="6683d-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="6683d-153">การย้ายงานขึ้นหรือลง ไม่มีผลต่อความพยายาม ต้นทุน วันที่ หรือระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="6683d-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="6683d-154">แอตทริบิวต์งาน</span><span class="sxs-lookup"><span data-stu-id="6683d-154">Task attributes</span></span>  
 <span data-ttu-id="6683d-155">ชื่อของงานอธิบายงานที่ต้องทำให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6683d-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="6683d-156">คุณสามารถใช้แอตทริบิวต์งานต่างๆเพื่ออธิบายกำหนดการและความต้องการการสรรหาพนักงานสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="6683d-157">แอททริบิวต์กำหนดการ</span><span class="sxs-lookup"><span data-stu-id="6683d-157">Schedule attributes</span></span>

 - <span data-ttu-id="6683d-158">กำหนดค่าไปยัง **ชั่วโมงความพยายาม** **จำนวนทรัพยากร** **วันที่เริ่มต้น** **วันที่สิ้นสุด** และ **ระยะเวลา** เพื่อกำหนดกำหนดการสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="6683d-159">**ความพยายาม** เป็นการประเมินของชั่วโมงที่ใช้ในการดำเนินงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6683d-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="6683d-160">**จำนวนของทรัพยากร** เป็นการประเมินที่ผู้จัดการโครงการใส่ลงไปในงาน เพื่อช่วยให้เกิดกำหนดการที่เป็นไปได้ที่ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="6683d-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="6683d-161">**ระยะเวลา** (เป็นวัน) บ่งชี้จำนวนของวันทำงานที่จะใช้ในการดำเนินงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6683d-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="6683d-162">แอตทริบิวต์การสรรหาพนักงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-162">Staffing attributes</span></span>

 - <span data-ttu-id="6683d-163">**บทบาท** **หน่วยงานทรัพยากร** **จำนวนทรัพยากร** และ **ทรัพยากร** อธิบายความต้องการการสรรหาพนักงานสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="6683d-164">**บทบาท** อธิบายถึงชนิดของทรัพยากรที่จำเป็นในการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="6683d-165">**หน่วยงานทรัพยากร** บ่งชี้หน่วยงานซึ่งทรัพยากรควรถูกสรรหาพนักงานสำหรับงานนั้น นอกจากนี้ยังมีผลต่อการประเมินต้นทุนและยอดขายของงานด้วย เนื่องจากถูกนำมาพิจารณาเมื่อมีการกำหนดราคาขายต่อหน่วยสำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="6683d-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="6683d-166">**ทรัพยากร** เก็บทรัพยากรทั่วไปหรือทรัพยากรที่มีชื่อเมื่อถูกพบ</span><span class="sxs-lookup"><span data-stu-id="6683d-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="6683d-167">การขึ้นต่อกันของงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-167">Task dependencies</span></span>  
 <span data-ttu-id="6683d-168">คุณสามารถสร้างความสัมพันธ์งานที่ต้องทำก่อนระหว่างงานอย่างน้อยหนึ่งรายการในโครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="6683d-169">คุณสามารถตั้งค่าอย่างน้อยหนึ่งค่าสำหรับฟิลด์งานที่ต้องทำก่อนในงาน เพื่อระบุงานที่จะถูกอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="6683d-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="6683d-170">เมื่อคุณกำหนดค่างานที่ต้องทำก่อนไปยังงาน งานสามารถเริ่มเฉพาะเมื่องานที่ต้องทำก่อนทั้งหมดได้เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="6683d-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="6683d-171">การตั้งค่าการอ้างอิงนี้ในงานจะส่งผลในการคำนวณซ้ำของวันที่เริ่มต้นที่วางแผนไว้ของงาน ซึ่งเป็นจุดสิ้นสุดล่าสุดของงานที่ต้องทำก่อนนั้นทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6683d-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="6683d-172">ผลกระทบที่เกี่ยวข้องกับงานที่ต้องทำก่อนในกำหนดการ จะไม่ถูกจำกัดโดยโหมดงานที่กำหนดไว้แล้วสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="6683d-173">โหมดงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-173">Task mode</span></span>  
 <span data-ttu-id="6683d-174">โหมดงานเป็นปัจจัยสำคัญที่กำหนดในการจัดกำหนดการงานโหนดปลายสุด</span><span class="sxs-lookup"><span data-stu-id="6683d-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="6683d-175">มีโหมดงานสองโหมดสำหรับทุกๆงาน: โหมดการจัดกำหนดการอัตโนมัติ และโหมดการจัดกำหนดการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="6683d-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="6683d-176">**การจัดกำหนดการอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="6683d-176">**Auto scheduling**.</span></span>   <span data-ttu-id="6683d-177">เมื่อคุณตั้งค่าโหมดงานไปยังการจัดกำหนดการโดยอัตโนมัติ กลไกการจัดกำหนดการงานจะใช้กฎการจัดกำหนดการในแอตทริบิวต์งานต่อไปนี้ เพื่อกำหนดกำหนดการสำหรับงาน:</span><span class="sxs-lookup"><span data-stu-id="6683d-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="6683d-178">งานที่ต้องทำก่อน</span><span class="sxs-lookup"><span data-stu-id="6683d-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="6683d-179">ความพยายาม</span><span class="sxs-lookup"><span data-stu-id="6683d-179">Effort</span></span>  
  
    -   <span data-ttu-id="6683d-180">จำนวนทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="6683d-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="6683d-181">วันที่เริ่มต้นและวันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="6683d-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="6683d-182">**การจัดกำหนดการกฎ**</span><span class="sxs-lookup"><span data-stu-id="6683d-182">**Scheduling rules**.</span></span>   <span data-ttu-id="6683d-183">วันที่เริ่มต้นของงานโหนดปลายสุดที่ไม่มีค่าเริ่มต้นของงานที่ต้องทำก่อน ถึงวันที่เริ่มต้นของการจัดกำหนดการของโครงการ</span><span class="sxs-lookup"><span data-stu-id="6683d-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="6683d-184">ระยะเวลาของงานโหนดปลายสุดจะคำนวณเป็นจำนวนวันทำงานระหว่างวันที่เริ่มต้นและสิ้นสุดเสมอ</span><span class="sxs-lookup"><span data-stu-id="6683d-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="6683d-185">เมื่องานถูกจัดกำหนดการโดยอัตโนมัติ กลไกการจัดกำหนดการเป็นไปตามกฎด้านล่าง:</span><span class="sxs-lookup"><span data-stu-id="6683d-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="6683d-186">วันที่เริ่มต้นและสิ้นสุดของงานต้องเป็นวันทำงาน ตามปฏิทินการจัดกำหนดของโครงการเสมอ</span><span class="sxs-lookup"><span data-stu-id="6683d-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="6683d-187">วันที่เริ่มต้นของงานที่มีค่าเริ่มต้นของงานที่ต้องทำก่อน ถึงวันที่สิ้นสุดล่าสุดของงานที่ต้องทำก่อน</span><span class="sxs-lookup"><span data-stu-id="6683d-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="6683d-188">ความพยายาม = จำนวนคน \* ระยะเวลา \* ชั่วโมงในหนึ่งวันทำงานมาตรฐานของปฏิทินโครงการ</span><span class="sxs-lookup"><span data-stu-id="6683d-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="6683d-189">**การจัดกำหนดการด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="6683d-189">**Manual scheduling**.</span></span>   <span data-ttu-id="6683d-190">ในบางกรณี คุณอาจต้องการดำเนินงานที่แตกต่างไปจากกฎเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="6683d-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="6683d-191">ในกรณีเหล่านี้ คุณสามารถตั้งค่าโหมดงานสำหรับงานที่จะถูกจัดกำหนดการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="6683d-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="6683d-192">ซึ่งเป็นการหยุดกลไกการจัดกำหนดการจากการคำนวณค่าสำหรับแอททริบิวต์การจัดกำหนดการอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="6683d-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="6683d-193">การตั้งค่างานที่ต้องทำก่อนของงาน มีผลต่อวันที่เริ่มต้นของงานที่เกี่ยวข้องเสมอ</span><span class="sxs-lookup"><span data-stu-id="6683d-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="6683d-194">สร้างโครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="6683d-195">ไปที่ **Project Service > โครงการ**</span><span class="sxs-lookup"><span data-stu-id="6683d-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="6683d-196">คลิกโครงการที่คุณต้องการทำงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="6683d-197">ในแถบที่ด้านบนของหน้าจอ ให้เลือกกลูกศรลงที่อยู่ถัดจากชื่อโครงการ แล้วคลิกโครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="6683d-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="6683d-198">เมื่อต้องการเพิ่มงาน ให้คลิก **เพิ่มงาน**</span><span class="sxs-lookup"><span data-stu-id="6683d-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="6683d-199">กรอกข้อมูลในฟิลด์สำหรับงาน และจากนั้นให้คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6683d-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="6683d-200">ดำเนินการเพิ่มงานต่อ จนกระทั่งโครงสร้างการแบ่งงานของคุณเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6683d-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="6683d-201">ขณะกำลังสร้างโครงสร้างการแบ่งงานของคุณ คุณสามารถดำเนินการจัดระเบียบงานของคุณได้ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6683d-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="6683d-202">เลือกงานและคลิก **เยื้องเข้า** เพื่อย้ายไปภายใต้งานอื่น หรือคลิก เยื้องออก เพื่อย้ายชื่อนั้นออกไปหนึ่งระดับ</span><span class="sxs-lookup"><span data-stu-id="6683d-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="6683d-203">เลือกงานและคลิก **เลื่อนขึ้น** หรือ **เลื่อนลง** เมื่อต้องการย้ายขึ้นหรือลงในรายการ</span><span class="sxs-lookup"><span data-stu-id="6683d-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="6683d-204">คลิก **ซ่อน Gantt** เพื่อซ่อนแผนภูมิ Gantt และคลิก **แสดง Gantt** เพื่อแสดงอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="6683d-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="6683d-205">เลือกรอบระยะเวลาที่แตกต่างกันของเวลาสำหรับแผนภูมิ Gantt ใน **สเกลเวลา**</span><span class="sxs-lookup"><span data-stu-id="6683d-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="6683d-206">เมื่อต้องการเพิ่มบทบาทที่คุณระบุไว้ในโครงสร้างการแบ่งงานของคุณไปยังสมาชิกทีมของโครงการของคุณ ให้คลิก **สร้างทีมโครงการ**</span><span class="sxs-lookup"><span data-stu-id="6683d-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="6683d-207">คลิก **บันทึก** ที่มุมล่างขวาของหน้าจอ เมื่อคุณเสร็จสิ้นการดำเนินการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="6683d-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="6683d-208">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6683d-208">See Also</span></span>  
 [<span data-ttu-id="6683d-209">คู่มือของผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="6683d-209">Project manager guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]