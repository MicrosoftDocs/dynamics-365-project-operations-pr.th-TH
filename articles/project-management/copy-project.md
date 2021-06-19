---
title: คัดลอกโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการคัดลอกโครงการใน Dynamics 365 Project Operations
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091277"
---
# <a name="copy-a-project"></a><span data-ttu-id="4d34d-103">คัดลอกโครงการ</span><span class="sxs-lookup"><span data-stu-id="4d34d-103">Copy a project</span></span>

<span data-ttu-id="4d34d-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="4d34d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4d34d-105">ด้วย Dynamics 365 Project Operations คุณสามารถสร้างโครงการใหม่ได้อย่างรวดเร็วโดยเลือก **คัดลอกโครงการ** บนแบบฟอร์ม **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="4d34d-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="4d34d-106">ในการคัดลอกโครงการ ให้เปิดโครงการที่คุณต้องการคัดลอก จากนั้นเลือก **คัดลอกโครงการ**</span><span class="sxs-lookup"><span data-stu-id="4d34d-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="4d34d-107">การดำเนินการจะคัดลอกสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4d34d-107">The action will copy the following:</span></span>

- <span data-ttu-id="4d34d-108">คุณสมบัติของโครงการ</span><span class="sxs-lookup"><span data-stu-id="4d34d-108">Project properties</span></span> 
- <span data-ttu-id="4d34d-109">โครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="4d34d-109">Work breakdown structure</span></span>
- <span data-ttu-id="4d34d-110">สมาชิกของทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="4d34d-110">Project team members</span></span>
- <span data-ttu-id="4d34d-111">การประมาณการโครงการ</span><span class="sxs-lookup"><span data-stu-id="4d34d-111">Project estimates</span></span>
- <span data-ttu-id="4d34d-112">การประมาณการค่าใช้จ่ายโครงการ</span><span class="sxs-lookup"><span data-stu-id="4d34d-112">Project expense estimates</span></span>
- <span data-ttu-id="4d34d-113">ประมาณการวัสดุโครงการ</span><span class="sxs-lookup"><span data-stu-id="4d34d-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="4d34d-114">คุณสมบัติของโครงการ</span><span class="sxs-lookup"><span data-stu-id="4d34d-114">Project properties</span></span>

<span data-ttu-id="4d34d-115">เมื่อมีการคัดลอกโครงการ จะมีการคัดลอกค่าในฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4d34d-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="4d34d-116">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="4d34d-116">Name</span></span>
- <span data-ttu-id="4d34d-117">รายละเอียด</span><span class="sxs-lookup"><span data-stu-id="4d34d-117">Description</span></span>
- <span data-ttu-id="4d34d-118">ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4d34d-118">Customer</span></span>
- <span data-ttu-id="4d34d-119">แม่แบบปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="4d34d-119">Calendar Template</span></span>
- <span data-ttu-id="4d34d-120">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="4d34d-120">Currency</span></span>
- <span data-ttu-id="4d34d-121">หน่วยที่ทำสัญญา</span><span class="sxs-lookup"><span data-stu-id="4d34d-121">Contracting Unit</span></span>
- <span data-ttu-id="4d34d-122">ผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="4d34d-122">Project Manager</span></span>
- <span data-ttu-id="4d34d-123">สถานะ</span><span class="sxs-lookup"><span data-stu-id="4d34d-123">Status</span></span>
- <span data-ttu-id="4d34d-124">สถานะโครงการโดยรวม</span><span class="sxs-lookup"><span data-stu-id="4d34d-124">Overall Project Status</span></span>
- <span data-ttu-id="4d34d-125">ความคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="4d34d-125">Comments</span></span>
- <span data-ttu-id="4d34d-126">ประมาณการ</span><span class="sxs-lookup"><span data-stu-id="4d34d-126">Estimates</span></span>
- <span data-ttu-id="4d34d-127">วันที่เริ่มต้นโดยประมาณ: นี่คือวันที่สร้างโครงการจากสำเนา</span><span class="sxs-lookup"><span data-stu-id="4d34d-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="4d34d-128">วันที่เสร็จสิ้นโดยประมาณ: วันที่นี้จะถูกปรับปรุงตามวันที่เริ่มต้นของโครงการใหม่ที่สร้างขึ้นจากสำเนา</span><span class="sxs-lookup"><span data-stu-id="4d34d-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="4d34d-129">การดำเนินการ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="4d34d-129">Effort (Hours)</span></span>
- <span data-ttu-id="4d34d-130">ต้นทุนค่าแรงโดยประมาณ</span><span class="sxs-lookup"><span data-stu-id="4d34d-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="4d34d-131">ต้นทุนค่าใช้จ่ายโดยประมาณ</span><span class="sxs-lookup"><span data-stu-id="4d34d-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="4d34d-132">ต้นทุนวัสดุโดยประมาณ</span><span class="sxs-lookup"><span data-stu-id="4d34d-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="4d34d-133">โครงการคัดลอกเป็นการดำเนินการที่ยาวนาน</span><span class="sxs-lookup"><span data-stu-id="4d34d-133">Copy project is a long running operation.</span></span> <span data-ttu-id="4d34d-134">เรกคอร์ดโครงการ คุณลักษณะที่เกี่ยวข้อง และเอนทิตีที่เกี่ยวข้องจำนวนมากก็ถูกคัดลอกเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="4d34d-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="4d34d-135">เนื่องจากลักษณะการดำเนินการที่ใช้เวลานาน หลังจากเริ่มการคัดลอก หน้าโครงการเป้าหมายจะถูกล็อกสำหรับการแก้ไขจนกว่าการดำเนินการคัดลอกจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4d34d-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="4d34d-136">โครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="4d34d-136">Work breakdown structure</span></span>

<span data-ttu-id="4d34d-137">เมื่อมีการคัดลอกโครงการ จะมีการคัดลอกโครงสร้างการแบ่งงานที่โหลดทรัพยากรทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4d34d-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="4d34d-138">จะมีการแทนที่ทรัพยากรที่ระบุชื่อด้วยทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="4d34d-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="4d34d-139">หากทรัพยากรที่ระบุชื่อไม่มีชั่วโมงการทำงานเดียวกันกับทรัพยากรทั่วไป ระบบจะคำนวณกำหนดการใหม่และระยะเวลาของงานอาจเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="4d34d-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="4d34d-140">สมาชิกของทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="4d34d-140">Project team members</span></span>

<span data-ttu-id="4d34d-141">เมื่อมีการคัดลอกทีมโครงการจากโครงการต้นทาง จะมีการคัดลอกทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="4d34d-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="4d34d-142">การมอบหมายทรัพยากรทรัพยากรทั่วไปยังจะได้รับการดูแลรักษาตามที่อยู่ในโครงการต้นทาง</span><span class="sxs-lookup"><span data-stu-id="4d34d-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="4d34d-143">ทรัพยากรที่ระบุชื่อจะมีการแปลงเป็นสมาชิกทีมทั่วไป</span><span class="sxs-lookup"><span data-stu-id="4d34d-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="4d34d-144">ประมาณการ</span><span class="sxs-lookup"><span data-stu-id="4d34d-144">Estimates</span></span>

<span data-ttu-id="4d34d-145">เมื่อมีการคัดลอกโครงการ รายการทรัพยากร ค่าใช้จ่าย และวัสดุจะถูกคัดลอกจากโครงการต้นทาง</span><span class="sxs-lookup"><span data-stu-id="4d34d-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="4d34d-146">สำหรับข้อมูลเกี่ยวกับวิธีการเข้าถึงการคัดลอกโครงการโดยทางโปรแกรม โปรดดู [พัฒนาแม่แบบโครงการด้วย คัดลอกโครงการ](dev-copy-project.md)</span><span class="sxs-lookup"><span data-stu-id="4d34d-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
