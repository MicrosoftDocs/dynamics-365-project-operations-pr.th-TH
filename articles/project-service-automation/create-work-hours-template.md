---
title: สร้างแม่แบบชั่วโมงทำงาน
description: วิธีการสร้างเท็มเพลตชั่วโมงทำงานใน Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 1a519487-25f1-4e9d-b739-1c1becf1d649
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5e7ef4af5f22419cccd8f29ea2a0a0a21a75875a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756453"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="588be-103">สร้างเท็มเพลตชั่วโมงทำงาน (Project Service)</span><span class="sxs-lookup"><span data-stu-id="588be-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="588be-104">ก่อนที่คุณจะสามารถสร้างกำหนดการโครงการได้ คุณจำเป็นต้องตั้งค่าปฏิทินโครงการที่กำหนดจำนวนของชั่วโมงการทำงานเพื่อให้เหมาะสมกับแต่ละวันในกำหนดการและระยะเวลาที่ปิดดำเนินการใดๆ</span><span class="sxs-lookup"><span data-stu-id="588be-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="588be-105">คุณทำเช่นนี้กับแม่แบบชั่วโมงทำงาน ซึ่งประกอบด้วยรายละเอียดเกี่ยวกับชั่วโมงทำงานต่อวัน วันหยุด และระยะเวลาที่ปิดดำเนินการอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="588be-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="588be-106">เมื่อคุณกำลังสร้างโครงการ คุณเชื่อมโยงแม่แบบงานไปยังปฏิทินโครงการเพื่อใช้การจัดกำหนดการสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="588be-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="588be-107">มีสองวิธีที่คุณสามารถสร้างต้นแบบชั่วโมงทำงาน:</span><span class="sxs-lookup"><span data-stu-id="588be-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="588be-108">สร้างแม่แบบชั่วโมงทำงานตามปฏิทินของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="588be-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="588be-109">สร้างแม่แบบชั่วโมงทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="588be-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="588be-110">เพื่อสร้างต้นแบบชั่วโมงทำงานตามปฏิทินของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="588be-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="588be-111">ไปที่ **Project Service > ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="588be-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="588be-112">เลือกทรัพยากรคุณต้องการให้ชั่วโมงการทำงานของคุณยึดตาม</span><span class="sxs-lookup"><span data-stu-id="588be-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="588be-113">คลิก **บันทึกปฏิทินเป็น** ป้อนชื่อสำหรับแม่แบบชั่วโมงทำงาน แล้วคลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="588be-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="588be-114">เมื่อคุณเสร็จสิ้นการแก้ไขตัวเลือกแล้ว ให้คลิก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="588be-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="588be-115">คลิกปุ่ม **บันทึก** ที่มุมล่างขวาของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="588be-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="588be-116">เพื่อสร้างแม่แบบชั่วโมงทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="588be-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="588be-117">ไปที่ **Project Service > แม่แบบชั่วโมงทำงาน**</span><span class="sxs-lookup"><span data-stu-id="588be-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="588be-118">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="588be-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="588be-119">ป้อนชื่อสำหรับแม่แบบชั่วโมงทำงาน</span><span class="sxs-lookup"><span data-stu-id="588be-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="588be-120">เลือกทรัพยากรที่จะให้ชั่วโมงการทำงานยึดตาม แล้ว คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="588be-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="588be-121">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="588be-121">See Also</span></span>  
 [<span data-ttu-id="588be-122">ตั้งค่าทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="588be-122">Set up resources</span></span>](../project-service/set-up-resources.md)
