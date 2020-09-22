---
title: ติดตามสถานะของโครงการ
description: วิธีการติดตามสถานะของโครงการใน Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7610aecb-318c-422b-b626-9106b0736b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: e4d53b6235c3b941bce525dca09ee3d647c3d242
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756497"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="0e3de-103">ติดตามสถานะของโครงการ (Project Service)</span><span class="sxs-lookup"><span data-stu-id="0e3de-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0e3de-104">ใช้ [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] เพื่อติดตามความคืบหน้าของโครงการของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0e3de-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="0e3de-105">เป็นความคืบหน้าการร่วมดำเนินการ การปรับปรุงลำดับขั้นโครงการเพื่อสะท้อนลำดับขั้นของการร่วมดำเนินงาน:</span><span class="sxs-lookup"><span data-stu-id="0e3de-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="0e3de-106">**สร้าง**</span><span class="sxs-lookup"><span data-stu-id="0e3de-106">**New**</span></span>    | <span data-ttu-id="0e3de-107">เมื่อคุณสร้างโครงการ ลำดับขั้นจะถูกตั้งค่าเป็น **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="0e3de-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="0e3de-108">ถ้าคุณสร้างโครงการจากแม่แบบ ในระยะนี้โครงการอาจมีกำหนดการ การประเมิน และข้อมูลทีม</span><span class="sxs-lookup"><span data-stu-id="0e3de-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="0e3de-109">มิฉะนั้น จะเป็นเค้าร่างของโครงการและคุณจำเป็นต้องป้อนส่วนที่เหลือของส่วนประกอบต่างๆของโครงการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="0e3de-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="0e3de-110">**ใบเสนอราคา**</span><span class="sxs-lookup"><span data-stu-id="0e3de-110">**Quote**</span></span>   |      <span data-ttu-id="0e3de-111">เมื่อคุณเชื่อมโยงโครงการกับใบเสนอราคา หรือสร้างจากใบเสนอราคา ลำดับขั้นของโครงการถูกตั้งค่าเป็น **ใบเสนอราคา**และการประเมินวันเริ่มต้นและสิ้นสุดจะถูกอัพเดตด้วย</span><span class="sxs-lookup"><span data-stu-id="0e3de-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="0e3de-112">เมื่อโครงการอยู่ในลำดับขั้นใบเสนอราคา รายละเอียดในใบเสนอราคาจะแสดงในแท็บ **การขาย** บนหน้า **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="0e3de-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="0e3de-113">**แผน**</span><span class="sxs-lookup"><span data-stu-id="0e3de-113">**Plan**</span></span>   |                                     <span data-ttu-id="0e3de-114">เมื่อคุณชนะใบเสนอราคาที่เกี่ยวข้องกับโครงการ และเมื่อการร่วมดำเนินงานคืบหน้าไปยังลำดับขั้นสัญญา ลำดับขั้นโครงการอัพเดตไปยัง **แผน**</span><span class="sxs-lookup"><span data-stu-id="0e3de-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="0e3de-115">รายละเอียดสัญญาแสดงผลบนแท็บ **การขาย** บนหน้า **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="0e3de-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="0e3de-116">**เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="0e3de-116">**Complete**</span></span> |                    <span data-ttu-id="0e3de-117">เมื่องานโครงการเสร็จสมบูรณ์แล้ว คุณสามารถสลับขั้นไป **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="0e3de-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="0e3de-118">เมื่อตั้งค่าขั้นของโครงการเสร็จสมบูรณ์ จะเข้าใจว่างานจะเสร็จสมบูรณ์ 100% แต่โครงการจะยังคงเปิดไว้สำหรับเวลาที่ค้างอยู่หรือการบันทึกรายการค่าใช้จ่ายใดๆ</span><span class="sxs-lookup"><span data-stu-id="0e3de-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="0e3de-119">**ปิด**</span><span class="sxs-lookup"><span data-stu-id="0e3de-119">**Close**</span></span>   |           <span data-ttu-id="0e3de-120">เมื่อธุรกรรมทั้งหมดได้ถูกบันทึกไว้ในโครงการ และคุณไม่ได้คาดหวังให้การเพิ่มใดๆเข้าสู่ระบบอีก คุณสามารถตั้งค่าลำดับขั้นเป็น **ปิด**ได้</span><span class="sxs-lookup"><span data-stu-id="0e3de-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="0e3de-121">เมื่อการตั้งค่าโครงการเป็น **ปิด**คุณไม่สามารถบันทึกธุรกรรมใดๆเพิ่มในโครงการได้ และโครงการจะเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="0e3de-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="0e3de-122">เพื่อติดตามสถานะของโครงการ (Project Service)</span><span class="sxs-lookup"><span data-stu-id="0e3de-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="0e3de-123">ไปที่ **Project Service > โครงการ**</span><span class="sxs-lookup"><span data-stu-id="0e3de-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="0e3de-124">คลิกโครงการที่คุณต้องการทำงาน</span><span class="sxs-lookup"><span data-stu-id="0e3de-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="0e3de-125">ในแถบที่ด้านบนของหน้าจอ เลือกกลูกศรลงที่อยู่ถัดจากชื่อโครงการ แล้วคลิก **การติดตามโครงการ**</span><span class="sxs-lookup"><span data-stu-id="0e3de-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="0e3de-126">เลือก **การติดตามความพยายาม** หรือ **การติดตามต้นทุน** ในรายการดรอปดาวน์ด้านบนของรายการงาน</span><span class="sxs-lookup"><span data-stu-id="0e3de-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="0e3de-127">คลิกสองครั้งที่งานใดๆเพื่อทำการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="0e3de-127">Double-click any task to edit it.</span></span> <span data-ttu-id="0e3de-128">นอกจากนี้คุณยังสามารถย้ายหรือปรับขนาดแถบต่างๆภายในแผนภูมิ Gantt เพื่อเปลี่ยนแปลงเวลาและความคืบหน้าของงาน</span><span class="sxs-lookup"><span data-stu-id="0e3de-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="0e3de-129">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0e3de-129">See Also</span></span>  
 [<span data-ttu-id="0e3de-130">คำแนะนำของผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e3de-130">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
