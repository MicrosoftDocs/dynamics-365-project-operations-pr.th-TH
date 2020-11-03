---
title: ภาพรวมระบบจัดการกำหนดการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการทำงานกับระบบจัดการกำหนดการเพื่อจองทรัพยากร
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085788"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="e1d44-103">ภาพรวมระบบจัดการกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="e1d44-103">Schedule assistant overview</span></span>

<span data-ttu-id="e1d44-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="e1d44-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e1d44-105">ระบบจัดการกำหนดการใช้เพื่อจองทรัพยากรตามความต้องการที่กำหนดโดยผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="e1d44-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="e1d44-106">ระบบจัดการกำหนดการจะอาศัยพารามิเตอร์ที่ระบุในความต้องการทรัพยากรเพื่อค้นหาทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="e1d44-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="e1d44-107">ระบบจัดการกำหนดการจะแนะนำทรัพยากรที่ตรงกับความต้องการที่เกี่ยวข้อง เช่น ช่วงเวลาหรือทักษะที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="e1d44-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="e1d44-108">หลังจากระบุทรัพยากรที่เหมาะสมแล้ว ผู้จัดการทรัพยากรหรือโครงการสามารถจองทรัพยากรให้กับงานได้</span><span class="sxs-lookup"><span data-stu-id="e1d44-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e1d44-109">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="e1d44-109">Prerequisites</span></span>

<span data-ttu-id="e1d44-110">ระบบจัดการกำหนดการเป็นส่วนหนึ่งของโซลูชัน Universal Resource Scheduling</span><span class="sxs-lookup"><span data-stu-id="e1d44-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="e1d44-111">โซลูชันนี้รวมและติดตั้งกับ Dynamics 365 Project Operations, Dynamics 365 Field Service และ Dynamics 365 Customer Service</span><span class="sxs-lookup"><span data-stu-id="e1d44-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="e1d44-112">ความต้องการการจับคู่ และทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="e1d44-112">Matching requirements and resources</span></span>

<span data-ttu-id="e1d44-113">ความต้องการทรัพยากรที่สร้างขึ้นจะขึ้นอยู่กับรายละเอียด เช่น:</span><span class="sxs-lookup"><span data-stu-id="e1d44-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="e1d44-114">คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="e1d44-114">Characteristics</span></span>
-   <span data-ttu-id="e1d44-115">บทบาท</span><span class="sxs-lookup"><span data-stu-id="e1d44-115">Roles</span></span>
-   <span data-ttu-id="e1d44-116">หน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="e1d44-116">Business units</span></span>
-   <span data-ttu-id="e1d44-117">การกำหนดลักษณะทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="e1d44-117">Resource preferences</span></span>
-   <span data-ttu-id="e1d44-118">ลักษณะกำลังคน</span><span class="sxs-lookup"><span data-stu-id="e1d44-118">Effort contours</span></span>
-   <span data-ttu-id="e1d44-119">เขตเวลา</span><span class="sxs-lookup"><span data-stu-id="e1d44-119">Time zone</span></span>

<span data-ttu-id="e1d44-120">ระบบจัดการกำหนดการใช้รายละเอียดเหล่านี้เพื่อกรองทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="e1d44-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="e1d44-121">เปิดใช้ระบบจัดการกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="e1d44-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="e1d44-122">การเปิดระบบจัดการกำหนดการมีอยู่สองวิธี</span><span class="sxs-lookup"><span data-stu-id="e1d44-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="e1d44-123">หากคุณกำลังใช้โหมดไฮบริด ในตารางสมาชิกทีม คุณสามารถเลือกสมาชิกทีมที่มีความต้องการทรัพยากรที่ยังไม่ได้รับการเติมเต็ม จากนั้นเลือก **จอง**</span><span class="sxs-lookup"><span data-stu-id="e1d44-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="e1d44-124">หากคุณกำลังใช้โหมดส่วนกลาง ผู้จัดการทรัพยากรจะค้นหาและเลือกทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="e1d44-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="e1d44-125">ตัวกรองระบบจัดการกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="e1d44-125">Schedule assistant filters</span></span>

<span data-ttu-id="e1d44-126">หลังจากระบบจัดการกำหนดการทำงาน รายละเอียดจากความต้องการทรัพยากรจะแสดงเป็นค่าที่กรองแล้วในบานหน้าต่างด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="e1d44-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="e1d44-127">ผู้จัดการทรัพยากรหรือผู้จัดการโครงการสามารถปรับแต่งผลลัพธ์โดยการปรับตัวกรองเพื่อให้ตรงกับความต้องการในการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="e1d44-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="e1d44-128">บานหน้าต่างตัวกรองจะแสดงตัวเลือกเกี่ยวกับงาน ซึ่งรวมถึง:</span><span class="sxs-lookup"><span data-stu-id="e1d44-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="e1d44-129">งานเริ่มต้นและสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="e1d44-129">Work start and end</span></span>
-   <span data-ttu-id="e1d44-130">คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="e1d44-130">Characteristics</span></span>
-   <span data-ttu-id="e1d44-131">บทบาท</span><span class="sxs-lookup"><span data-stu-id="e1d44-131">Roles</span></span>
-   <span data-ttu-id="e1d44-132">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="e1d44-132">Organizational units</span></span>
-   <span data-ttu-id="e1d44-133">บริษัทที่จัดหาทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="e1d44-133">Resourcing company</span></span>
-   <span data-ttu-id="e1d44-134">ชนิดทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="e1d44-134">Resource types</span></span>
-   <span data-ttu-id="e1d44-135">ทรัพยากรที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="e1d44-135">Preferred resources</span></span>
