---
title: สร้างแม่แบบชั่วโมงทำงาน
description: วิธีการสร้างเท็มเพลตชั่วโมงทำงานใน Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: a0fce327587940e557e0214c8c0897116ac91901
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133076"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="4b6fb-103">สร้างเท็มเพลตชั่วโมงทำงาน (Project Service)</span><span class="sxs-lookup"><span data-stu-id="4b6fb-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="4b6fb-104">ก่อนที่คุณจะสามารถสร้างกำหนดการโครงการได้ คุณจำเป็นต้องตั้งค่าปฏิทินโครงการที่กำหนดจำนวนของชั่วโมงการทำงานเพื่อให้เหมาะสมกับแต่ละวันในกำหนดการและระยะเวลาที่ปิดดำเนินการใดๆ</span><span class="sxs-lookup"><span data-stu-id="4b6fb-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="4b6fb-105">คุณทำเช่นนี้กับแม่แบบชั่วโมงทำงาน ซึ่งประกอบด้วยรายละเอียดเกี่ยวกับชั่วโมงทำงานต่อวัน วันหยุด และระยะเวลาที่ปิดดำเนินการอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="4b6fb-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="4b6fb-106">เมื่อคุณกำลังสร้างโครงการ คุณเชื่อมโยงแม่แบบงานไปยังปฏิทินโครงการเพื่อใช้การจัดกำหนดการสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="4b6fb-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="4b6fb-107">มีสองวิธีที่คุณสามารถสร้างต้นแบบชั่วโมงทำงาน:</span><span class="sxs-lookup"><span data-stu-id="4b6fb-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="4b6fb-108">สร้างแม่แบบชั่วโมงทำงานตามปฏิทินของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4b6fb-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="4b6fb-109">สร้างแม่แบบชั่วโมงทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="4b6fb-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="4b6fb-110">เพื่อสร้างต้นแบบชั่วโมงทำงานตามปฏิทินของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4b6fb-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="4b6fb-111">ไปที่ **Project Service > ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="4b6fb-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="4b6fb-112">เลือกทรัพยากรคุณต้องการให้ชั่วโมงการทำงานของคุณยึดตาม</span><span class="sxs-lookup"><span data-stu-id="4b6fb-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="4b6fb-113">คลิก **บันทึกปฏิทินเป็น** ป้อนชื่อสำหรับแม่แบบชั่วโมงทำงาน แล้วคลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="4b6fb-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="4b6fb-114">เมื่อคุณเสร็จสิ้นการแก้ไขตัวเลือกแล้ว ให้คลิก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="4b6fb-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="4b6fb-115">คลิกปุ่ม **บันทึก** ที่มุมล่างขวาของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="4b6fb-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="4b6fb-116">เพื่อสร้างแม่แบบชั่วโมงทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="4b6fb-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="4b6fb-117">ไปที่ **Project Service > แม่แบบชั่วโมงทำงาน**</span><span class="sxs-lookup"><span data-stu-id="4b6fb-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="4b6fb-118">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="4b6fb-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="4b6fb-119">ป้อนชื่อสำหรับแม่แบบชั่วโมงทำงาน</span><span class="sxs-lookup"><span data-stu-id="4b6fb-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="4b6fb-120">เลือกทรัพยากรที่จะให้ชั่วโมงการทำงานยึดตาม แล้ว คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="4b6fb-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="4b6fb-121">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4b6fb-121">See Also</span></span>  
 [<span data-ttu-id="4b6fb-122">ตั้งค่าทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="4b6fb-122">Set up resources</span></span>](../psa/set-up-resources.md)
