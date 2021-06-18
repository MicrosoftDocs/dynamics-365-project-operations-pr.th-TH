---
title: ตั้งค่าทรัพยากรโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการตั้งค่าหรือการร้องขอทรัพยากรโครงการ
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49e0ca6254518079d2e01d92ac2e31d119468c4b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997714"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="b82a3-103">ตั้งค่าทรัพยากรโครงการ</span><span class="sxs-lookup"><span data-stu-id="b82a3-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b82a3-104">คุณต้องตั้งค่าปฏิทินและเชื่อมโยงกับพนักงานหรือผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="b82a3-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="b82a3-105">ปฏิทินถูกใช้เพื่อจัดกำหนดการโครงการและเวลาทำงานของทรัพยากรที่จองไว้สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="b82a3-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="b82a3-106">ในระหว่างการตั้งค่าปฏิทิน ผู้จัดการโครงการสามารถปรับระดับทรัพยากรโดยเป็นส่วนหนึ่งของการเพิ่มประสิทธิภาพทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="b82a3-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="b82a3-107">โดยยึดตามกำหนดการในปฏิทิน สามารถวางข้อจำกัดในทรัพยากรได้</span><span class="sxs-lookup"><span data-stu-id="b82a3-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="b82a3-108">คุณสามารถตั้งค่าปฏิทินในหน้า **ปฏิทิน** ได้</span><span class="sxs-lookup"><span data-stu-id="b82a3-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="b82a3-109">เมื่อคุณตั้งค่าผู้ปฏิบัติงานเป็นทรัพยากรของโครงการ คุณสามารถเลือกจากผู้ปฏิบัติงานที่ทำงานในบริษัทที่คุณกำลังตั้งค่าทรัพยากรให้ได้</span><span class="sxs-lookup"><span data-stu-id="b82a3-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="b82a3-110">หรือคุณสามารถเลือกผู้ปฏิบัติงานจากบริษัทอื่นๆ ในองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="b82a3-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="b82a3-111">ผู้ปฏิบัติงานเหล่านี้เรียกว่า ทรัพยากรระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="b82a3-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="b82a3-112">กระบวนงานต่อไปนี้จะอธิบายวิธีการตั้งค่าผู้ปฏิบัติงานเป็นทรัพยากรของโครงการในบริษัทของคุณ และวิธีการตั้งค่าทรัพยากรของโครงการระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="b82a3-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="b82a3-113">ตั้งค่าผู้ปฏิบัติงานเป็นทรัพยากรของโครงการ</span><span class="sxs-lookup"><span data-stu-id="b82a3-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="b82a3-114">ในหน้า **ผู้ปฏิบัติงาน** ในรายการ **ผู้ปฏิบัติงาน** เลือกผู้ปฏิบัติงานที่คุณกำลังเพิ่มเป็นทรัพยากรของโครงการ และเปิดเรกคอร์ดผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="b82a3-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="b82a3-115">ในบานหน้าต่างการดำเนินการ เลือก **โครงการ** &gt; **การตั้งค่า** &gt; **การตั้งค่าโครงการ**</span><span class="sxs-lookup"><span data-stu-id="b82a3-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="b82a3-116">เลือกปฏิทิน และจากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b82a3-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="b82a3-117">นอกจากนี้ คุณยังสามารถระบุโครงการเริ่มต้นสำหรับทรัพยากรเป็นชนิดของการมอบหมายล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="b82a3-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="b82a3-118">สามารถใช้การมอบหมายล่วงหน้าเมื่อ Resource Manager หรือผู้จัดการโครงการทราบโครงการที่ทรัพยากรจะทำงานด้วยล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="b82a3-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="b82a3-119">นอกจากนี้ การมอบหมายล่วงหน้าอาจเป็นไปตามคำขอของผู้สนับสนุนโครงการหรือลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b82a3-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="b82a3-120">ในการมอบหมายโครงการล่วงหน้า บนหน้า **มอบหมายโครงการ** บนแท็บ **โครงการ** ในรายการ **โครงการที่เหลือ** เลือกโครงการที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="b82a3-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="b82a3-121">ตั้งค่าทรัพยากรระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="b82a3-121">Set up an intercompany resource</span></span>

<span data-ttu-id="b82a3-122">เมื่อคุณตั้งค่าผู้ปฏิบัติงานเป็นทรัพยากรระหว่างบริษัท คุณต้องดำเนินการการตั้งค่าให้เสร็จสิ้นทั้งในบริษัทที่ให้กู้ยืมและบริษัทที่ยืม</span><span class="sxs-lookup"><span data-stu-id="b82a3-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="b82a3-123">ในบริษัทที่ให้กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="b82a3-123">In the lending company</span></span>

1. <span data-ttu-id="b82a3-124">ใน Finance ตรวจสอบว่าได้เลือกบริษัทที่ให้กู้ยืม แล้วจากนั้นดำเนินกระบวนงานในส่วนก่อนหน้าให้เสร็จสมบูรณ์ "ตั้งค่าผู้ปฏิบัติงานเป็นทรัพยากรของโครงการ"</span><span class="sxs-lookup"><span data-stu-id="b82a3-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="b82a3-125">บนหน้า **การบัญชีระหว่างบริษัท** เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="b82a3-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="b82a3-126">ในฟิลด์ **รหัสเอนทิตีทางกฎหมาย** เลือกบริษัทที่ให้กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="b82a3-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="b82a3-127">กรอกข้อมูลฟิลด์ที่เหลือตามความเหมาะสม และจากนั้น เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b82a3-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="b82a3-128">บนหน้า **ราคาการโอนย้าย** เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="b82a3-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="b82a3-129">ในฟิลด์ **เอนทิตีทางกฎหมายที่ยืม** เลือกบริษัทที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="b82a3-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="b82a3-130">ในการให้บริษัทที่ยืมยืมเฉพาะทรัพยากรที่คุณสร้างขึ้นในตอนต้นของส่วนนี้ ในฟิลด์ **ทรัพยากร** เลือกชื่อของทรัพยากรที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="b82a3-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="b82a3-131">ในการทำให้ทรัพยากรทั้งหมดในบริษัทที่ให้ยืมสามารถใช้ได้กับบริษัทที่ยืม ให้ปล่อยให้ฟิลด์ **ทรัพยากร** ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="b82a3-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="b82a3-132">บนหน้า **พารามิเตอร์การจัดการโครงการและการบัญชี** บนแท็บ **ระหว่างบริษัท** ตั้งค่าตัวเลือก **เปิดใช้งานการจัดกำหนดการทรัพยากรระหว่างบริษัทและแผ่นเวลา** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="b82a3-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="b82a3-133">ในบริษัทที่ยืม</span><span class="sxs-lookup"><span data-stu-id="b82a3-133">In the borrowing company</span></span>

- <span data-ttu-id="b82a3-134">บนหน้า **รายการทรัพยากร** ในตัวกรองการค้นหา ป้อนชื่อของทรัพยากรที่คุณสร้างขึ้นสำหรับบริษัทที่ให้ยืม เพื่อตรวจสอบว่าชื่อนั้นถูกรวมอยู่ในรายการทรัพยากรสำหรับบริษัทที่ยืม</span><span class="sxs-lookup"><span data-stu-id="b82a3-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="b82a3-135">ร้องขอทรัพยากรของโครงการ</span><span class="sxs-lookup"><span data-stu-id="b82a3-135">Request project resources</span></span>
<span data-ttu-id="b82a3-136">ฟังก์ชันสำหรับการจัดกำหนดการทรัพยากรของโครงการ ทำให้ Resource Manager สามารถแจกจ่ายทรัพยากรที่มีการจัดเตรียมพนักงานในการมีส่วนร่วมหรือโครงการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b82a3-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="b82a3-137">ในการเปิดใช้งานฟังก์ชันนี้ ให้ดำเนินงานต่อไปนี้ให้เสร็จสมบูรณ์ หรือตรวจสอบว่าเสร็จสิ้นแล้ว:</span><span class="sxs-lookup"><span data-stu-id="b82a3-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="b82a3-138">ตั้งค่าลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="b82a3-138">Set up number sequences.</span></span>
- <span data-ttu-id="b82a3-139">ตั้งค่าเวิร์กโฟลว์การจัดการโครงการและการบัญชี</span><span class="sxs-lookup"><span data-stu-id="b82a3-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="b82a3-140">เปิดใช้งานเวิร์กโฟลว์คำขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="b82a3-140">Enable resource request workflows.</span></span>

<span data-ttu-id="b82a3-141">หลังจากที่งานก่อนหน้านี้เสร็จสิ้น คุณสามารถทำงานต่อไปนี้ให้เสร็จสมบูรณ์ได้ตามที่คุณต้องการ:</span><span class="sxs-lookup"><span data-stu-id="b82a3-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="b82a3-142">สร้างคำขอทรัพยากรจากทรัพยากรที่มีการจัดเตรียมพนักงานซึ่งมีการจองแบบไม่ตายตัว</span><span class="sxs-lookup"><span data-stu-id="b82a3-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="b82a3-143">ตรวจสอบคำขอของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="b82a3-143">Monitor resource requests.</span></span>
- <span data-ttu-id="b82a3-144">เติมเต็มคำขอของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="b82a3-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="b82a3-145">ร้องขอทรัพยากรที่มีการจัดเตรียมพนักงานจาก WBS</span><span class="sxs-lookup"><span data-stu-id="b82a3-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="b82a3-146">จองทรัพยากรไปยังโครงการโดยไม่ต้องมีการร้องขอทรัพยากรที่มีการจัดเตรียมพนักงาน</span><span class="sxs-lookup"><span data-stu-id="b82a3-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]