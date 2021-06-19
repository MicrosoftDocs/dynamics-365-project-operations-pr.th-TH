---
title: โหมดการจัดกำหนดการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับโหมดการจัดกำหนดการ
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116730"
---
# <a name="scheduling-modes"></a><span data-ttu-id="7e1c1-103">โหมดการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="7e1c1-103">Scheduling modes</span></span>

<span data-ttu-id="7e1c1-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="7e1c1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7e1c1-105">Dynamics 365 Project Operations ให้ความสามารถสำหรับองค์กรในการกำหนดวิธีจัดการการเปลี่ยนแปลงไปยังตัวแปรหลักในงานภายในโครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="7e1c1-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="7e1c1-106">ตามความต้องการเฉพาะขององค์กร ผู้จัดการโครงการสามารถทำการเปลี่ยนแปลงไปยังโหมดการจัดกำหนดการ เมื่อมีการสร้างโครงการ</span><span class="sxs-lookup"><span data-stu-id="7e1c1-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="7e1c1-107">มีโหมดการจัดกำหนดการสามโหมดที่พร้อมใช้งานใน Project Operations:</span><span class="sxs-lookup"><span data-stu-id="7e1c1-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="7e1c1-108">ระยะเวลาคงที่ (นี่คือโหมดเริ่มต้น)</span><span class="sxs-lookup"><span data-stu-id="7e1c1-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="7e1c1-109">ความพยายามคงที่ (*งาน*)</span><span class="sxs-lookup"><span data-stu-id="7e1c1-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="7e1c1-110">หน่วยคงที่</span><span class="sxs-lookup"><span data-stu-id="7e1c1-110">Fixed units</span></span>

<span data-ttu-id="7e1c1-111">ค่าที่ได้รับผลกระทบจากคำจำกัดความของโหมดการจัดกำหนดการเฉพาะ ถูกกำหนดโดยสูตรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7e1c1-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="7e1c1-112">ความพยายาม = ระยะเวลา x หน่วย</span><span class="sxs-lookup"><span data-stu-id="7e1c1-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="7e1c1-113">เมื่อคุณกำหนดโหมดการจัดกำหนดการของโครงการ คุณกำลังตั้งค่าหนึ่งในค่าเหล่านี้ ซึ่งจะไม่สามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="7e1c1-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="7e1c1-114">การถือค่านี้เป็นค่าคงที่จะจัดลำดับความสำคัญให้กับค่านั้น ซึ่งจะแจ้งให้ระบบไม่เปลี่ยนแปลงเมื่อค่าอีกสองค่าเปลี่ยนไป</span><span class="sxs-lookup"><span data-stu-id="7e1c1-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="7e1c1-115">ตารางต่อไปนี้ให้ข้อมูลเกี่ยวกับผลกระทบของการเลือกโหมดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="7e1c1-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="7e1c1-116">**ในงานนี้**</span><span class="sxs-lookup"><span data-stu-id="7e1c1-116">**In this task**</span></span>             | <span data-ttu-id="7e1c1-117">**หากคุณแก้ไขหน่วย**</span><span class="sxs-lookup"><span data-stu-id="7e1c1-117">**If you revise units**</span></span>   | <span data-ttu-id="7e1c1-118">**หากคุณแก้ไขระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="7e1c1-118">**If you revise duration**</span></span> | <span data-ttu-id="7e1c1-119">**หากคุณแก้ไขความพยายาม**</span><span class="sxs-lookup"><span data-stu-id="7e1c1-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="7e1c1-120">งานที่หน่วยคงที่</span><span class="sxs-lookup"><span data-stu-id="7e1c1-120">Fixed units task</span></span>     | <span data-ttu-id="7e1c1-121">ระยะเวลาจะถูกคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="7e1c1-121">Duration is recalculated.</span></span> | <span data-ttu-id="7e1c1-122">ความพยายามถูกคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="7e1c1-122">Effort is recalculated.</span></span>    | <span data-ttu-id="7e1c1-123">ระยะเวลาจะถูกคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="7e1c1-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="7e1c1-124">งานที่ความพยายามคงที่</span><span class="sxs-lookup"><span data-stu-id="7e1c1-124">Fixed effort task</span></span>    | <span data-ttu-id="7e1c1-125">ระยะเวลาจะถูกคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="7e1c1-125">Duration is recalculated.</span></span> | <span data-ttu-id="7e1c1-126">หน่วยจะถูกคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="7e1c1-126">Units are recalculated.</span></span>    | <span data-ttu-id="7e1c1-127">ระยะเวลาจะถูกคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="7e1c1-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="7e1c1-128">งานที่ระยะเวลาคงที่</span><span class="sxs-lookup"><span data-stu-id="7e1c1-128">Fixed duration task</span></span>  | <span data-ttu-id="7e1c1-129">ความพยายามถูกคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="7e1c1-129">Effort is recalculated.</span></span>   | <span data-ttu-id="7e1c1-130">ความพยายามถูกคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="7e1c1-130">Effort is recalculated.</span></span>    | <span data-ttu-id="7e1c1-131">หน่วยจะถูกคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="7e1c1-131">Units are recalculated.</span></span>   |

<span data-ttu-id="7e1c1-132">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับผลกระทบของโหมดที่กำหนด โปรดดู [เปลี่ยนชนิดงานเพื่อการจัดกำหนดการที่แม่นยำยิ่งขึ้น](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72)</span><span class="sxs-lookup"><span data-stu-id="7e1c1-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="7e1c1-133">ในหัวข้อ คำว่า **งาน** ถูกใช้แทน **ความพยายาม**</span><span class="sxs-lookup"><span data-stu-id="7e1c1-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="7e1c1-134">เปลี่ยนโหมดการจัดกำหนดการขององค์กร</span><span class="sxs-lookup"><span data-stu-id="7e1c1-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="7e1c1-135">ทำตามขั้นตอนต่อไปนี้เพื่อกำหนดโหมดการจัดกำหนดการขององค์กร</span><span class="sxs-lookup"><span data-stu-id="7e1c1-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="7e1c1-136">ไปที่ **การตั้งค่า** \> **ทั่วไป** \> **พารามิเตอร์** แล้วจากนั้น เลือกพารามิเตอร์โครงการ</span><span class="sxs-lookup"><span data-stu-id="7e1c1-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="7e1c1-137">บนหน้า **พารามิเตอร์โครงการ** เลือกโหมดการจัดกำหนดการเริ่มต้นสำหรับองค์กร และจากนั้น กำหนดความสามารถให้ผู้จัดการโครงการในการแทนที่การตั้งค่า เมื่อสร้างโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="7e1c1-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="7e1c1-138">เปลี่ยนการตั้งค่าโหมดการจัดกำหนดการในโครงการ</span><span class="sxs-lookup"><span data-stu-id="7e1c1-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="7e1c1-139">ถ้าองค์กรอนุญาตให้ผู้จัดการโครงการแทนที่โหมดการจัดกำหนดการเริ่มต้น ผู้จัดการโครงการสามารถทำการเปลี่ยนแปลงนั้นได้ เมื่อพวกเขาสร้างโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="7e1c1-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="7e1c1-140">อย่างไรก็ตาม หลังจากบันทึกโครงการแล้ว จะไม่สามารถเปลี่ยนโหมดการจัดกำหนดการได้</span><span class="sxs-lookup"><span data-stu-id="7e1c1-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="7e1c1-141">โครงการที่คัดลอก</span><span class="sxs-lookup"><span data-stu-id="7e1c1-141">Copied projects</span></span>

<span data-ttu-id="7e1c1-142">เนื่องจากโครงการถูกสร้างขึ้นเมื่อมีการดำเนินการคัดลอกโครงการ ผู้จัดการโครงการจึงไม่สามารถตั้งค่าโหมดการจัดกำหนดการได้</span><span class="sxs-lookup"><span data-stu-id="7e1c1-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="7e1c1-143">โครงการปลายทางจะเริ่มต้นเป็นโหมดที่กำหนดไว้ในระดับองค์กรเสมอ</span><span class="sxs-lookup"><span data-stu-id="7e1c1-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="7e1c1-144">งานที่คัดลอก</span><span class="sxs-lookup"><span data-stu-id="7e1c1-144">Copied tasks</span></span>

<span data-ttu-id="7e1c1-145">เมื่องานถูกคัดลอกจากโครงการหนึ่งไปยังอีกโครงการหนึ่ง งานจะสืบทอดโหมดการจัดกำหนดการของโครงการปลายทาง</span><span class="sxs-lookup"><span data-stu-id="7e1c1-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
