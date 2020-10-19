---
title: คัดลอกโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการคัดลอกโครงการใน Dynamics 365 Project Operations
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908671"
---
# <a name="copy-a-project"></a><span data-ttu-id="629fb-103">คัดลอกโครงการ</span><span class="sxs-lookup"><span data-stu-id="629fb-103">Copy a project</span></span>

<span data-ttu-id="629fb-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="629fb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="629fb-105">ด้วย Dynamics 365 Project Operations คุณสามารถสร้างโครงการใหม่ได้อย่างรวดเร็วโดยใช้การดำเนินการ **คัดลอกโครงการ** ในฟอร์ม **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="629fb-105">With Dynamics 365 Project Operations, you can quickly build new projects by using the **Copy Project** action on the **Projects** from.</span></span> <span data-ttu-id="629fb-106">หากต้องการคัดลอกโครงการ ให้เลือกโครงการ จากนั้นเลือก **คัดลอก**</span><span class="sxs-lookup"><span data-stu-id="629fb-106">To copy a project, select a project, and then select **Copy**.</span></span> <span data-ttu-id="629fb-107">การดำเนินการนี้จะคัดลอก:</span><span class="sxs-lookup"><span data-stu-id="629fb-107">The action will copy:</span></span>

- <span data-ttu-id="629fb-108">คุณสมบัติของโครงการ</span><span class="sxs-lookup"><span data-stu-id="629fb-108">Project properties</span></span>
- <span data-ttu-id="629fb-109">โครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="629fb-109">The Work breakdown structure</span></span>
- <span data-ttu-id="629fb-110">สมาชิกของทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="629fb-110">Project team members</span></span>
- <span data-ttu-id="629fb-111">การประมาณการโครงการ</span><span class="sxs-lookup"><span data-stu-id="629fb-111">Project estimates</span></span>
- <span data-ttu-id="629fb-112">การประมาณการค่าใช้จ่ายโครงการ</span><span class="sxs-lookup"><span data-stu-id="629fb-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="629fb-113">คุณสมบัติของโครงการ</span><span class="sxs-lookup"><span data-stu-id="629fb-113">Project properties</span></span>

<span data-ttu-id="629fb-114">เมื่อมีการคัดลอกโครงการ จะมีการคัดลอกค่าในฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="629fb-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="629fb-115">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="629fb-115">Name</span></span>
- <span data-ttu-id="629fb-116">รายละเอียด</span><span class="sxs-lookup"><span data-stu-id="629fb-116">Description</span></span>
- <span data-ttu-id="629fb-117">ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="629fb-117">Customer</span></span>
- <span data-ttu-id="629fb-118">แม่แบบปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="629fb-118">Calendar Template</span></span>
- <span data-ttu-id="629fb-119">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="629fb-119">Currency</span></span>
- <span data-ttu-id="629fb-120">หน่วยตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="629fb-120">Contracting Unit</span></span>
- <span data-ttu-id="629fb-121">ผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="629fb-121">Project Manager</span></span>
- <span data-ttu-id="629fb-122">สถานะ</span><span class="sxs-lookup"><span data-stu-id="629fb-122">Status</span></span>
- <span data-ttu-id="629fb-123">สถานะโครงการโดยรวม</span><span class="sxs-lookup"><span data-stu-id="629fb-123">Overall Project Status</span></span>
- <span data-ttu-id="629fb-124">ความคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="629fb-124">Comments</span></span>
- <span data-ttu-id="629fb-125">การประมาณการ</span><span class="sxs-lookup"><span data-stu-id="629fb-125">Estimates</span></span>
- <span data-ttu-id="629fb-126">วันที่เริ่มต้นโดยประมาณ</span><span class="sxs-lookup"><span data-stu-id="629fb-126">Estimated Start Date</span></span>
- <span data-ttu-id="629fb-127">วันที่เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="629fb-127">Finish Date</span></span>
- <span data-ttu-id="629fb-128">การดำเนินการ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="629fb-128">Effort (Hours)</span></span>
- <span data-ttu-id="629fb-129">ต้นทุนค่าแรงโดยประมาณ</span><span class="sxs-lookup"><span data-stu-id="629fb-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="629fb-130">ต้นทุนค่าใช้จ่ายโดยประมาณ</span><span class="sxs-lookup"><span data-stu-id="629fb-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="629fb-131">โครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="629fb-131">Work breakdown structure</span></span>

<span data-ttu-id="629fb-132">เมื่อมีการคัดลอกโครงการ จะมีการคัดลอกโครงสร้างการแบ่งงานที่โหลดทรัพยากรทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="629fb-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="629fb-133">จะมีการแทนที่ทรัพยากรที่ระบุชื่อด้วยทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="629fb-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="629fb-134">หากทรัพยากรที่ระบุชื่อไม่มีชั่วโมงการทำงานเดียวกันกับทรัพยากรทั่วไป ระบบจะคำนวณกำหนดการใหม่และระยะเวลาของงานอาจเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="629fb-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="629fb-135">สมาชิกของทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="629fb-135">Project team members</span></span>

<span data-ttu-id="629fb-136">เมื่อมีการคัดลอกทีมโครงการจากโครงการต้นทาง จะมีการคัดลอกทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="629fb-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="629fb-137">การมอบหมายทรัพยากรทรัพยากรทั่วไปยังจะได้รับการดูแลรักษาตามที่อยู่ในโครงการต้นทาง</span><span class="sxs-lookup"><span data-stu-id="629fb-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="629fb-138">ทรัพยากรที่ระบุชื่อจะมีการแปลงเป็นสมาชิกทีมทั่วไป</span><span class="sxs-lookup"><span data-stu-id="629fb-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="629fb-139">การประมาณการ</span><span class="sxs-lookup"><span data-stu-id="629fb-139">Estimates</span></span>

<span data-ttu-id="629fb-140">เมื่อคัดลอกโครงการ ทั้งรายการประมาณการทรัพยากรและค่าใช้จ่ายจะได้รับการคัดลอกจากโครงการต้นทาง</span><span class="sxs-lookup"><span data-stu-id="629fb-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span>