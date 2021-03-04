---
title: คู่มือของผู้จัดการทรัพยากร
description: คู่มือในการจัดการทรัพยากรใน Project Service
author: JohnPBurrows
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
ms.openlocfilehash: 543be23d95b1b821fcdca628612d03c343fd5b06
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147361"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="f160d-103">คู่มือของผู้จัดการทรัพยากร (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f160d-103">Resource manager guide (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f160d-104">ความสามารถของ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ใน [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] ช่วยให้คุณสามารถค้นหาทรัพยากรที่เหมาะสม ณ เวลาที่เหมาะสม สำหรับโครงการที่เหมาะสม และตรวจสอบให้แน่ใจว่า มีการใช้ทรัพยากรทั้งหมดอย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="f160d-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="f160d-105">ปรับใช้ที่ปรึกษาของบริษัทของคุณอย่างมีประสิทธิภาพและประสิทธิผลด้วย [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]</span><span class="sxs-lookup"><span data-stu-id="f160d-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="f160d-106">สิ่งเหล่านี้มีเครื่องมือที่คุณต้องการในการจัดกำหนดการทรัพยากรตามความต้องการและกำหนดการของโครงการที่ปรึกษา และตามทักษะและความพร้อมใช้งานของที่ปรึกษาของคุณ</span><span class="sxs-lookup"><span data-stu-id="f160d-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="f160d-107">คุณสามารถค้นหาที่ปรึกษาที่เหมาะสมที่สุดที่พร้อมทำงานในโครงการได้อย่างรวดเร็ว และคุณสามารถดูวิธีการกำหนดการที่ปรึกษาที่ดีขึ้นในระหว่างหลักสูตรของแต่ละโครงการได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="f160d-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="f160d-108">การจัดกำหนดการทรัพยากรช่วยให้คุณสามารถทำสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f160d-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="f160d-109">จับคู่ทรัพยากรกับโครงการ ตามทักษะของพวกเขาและตามระดับความชำนาญที่ตรงกับความต้องการทรัพยากรของโครงการ</span><span class="sxs-lookup"><span data-stu-id="f160d-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="f160d-110">จับคู่กำหนดการของทรัพยากรกับปฏิทินโครงการ ขึ้นอยู่กับความพร้อมใช้งานของทรัพยากรและตามการจัดกำหนดการ Time Off</span><span class="sxs-lookup"><span data-stu-id="f160d-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="f160d-111">ปฏิทินซึ่งเข้ารหัสสีช่วยให้คุณมองเห็นนัยที่เกี่ยวกับความพร้อมใช้งานของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="f160d-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="f160d-112">ตรวจสอบกำลังการผลิตของที่ปรึกษาแต่ละคน และกำหนดวิธีใช้กำลังการผลิตในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="f160d-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="f160d-113">ซึ่งสามารถช่วยให้คุณค้นหาที่ปรึกษาที่อาจถูกใช้งานน้อยหรือมากเกินไป หรือว่าพวกเขากำลังทำงานอยู่ที่กำลังการผลิตแล้ว</span><span class="sxs-lookup"><span data-stu-id="f160d-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="f160d-114">กำหนดเปอร์เซ็นต์หรือจำนวนที่เจาะจงของชั่วโมงสำหรับกำลังการผลิตของผู้ปฏิบัติงานไปยังโครงการ</span><span class="sxs-lookup"><span data-stu-id="f160d-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="f160d-115">ทำการจองทรัพยากรกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="f160d-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="f160d-116">ทรัพยากรแบบไม่ตายตัวหรือทรัพยากรแบบตายตัว และแปลงชั่วโมงแบบไม่ตายตัวเป็นชั่วโมงแบบตายตัวในขั้นตอนเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="f160d-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="f160d-117">ฟอร์มทีมโครงการขึ้นอยู่กับทรัพยากรที่กำหนดไว้ในโครงสร้างการแบ่งงานของโครงการโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f160d-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="f160d-118">ดำเนินการส่งคำขอทรัพยากร (จอง เสนอ ค้นหาทรัพยากรทดแทน)</span><span class="sxs-lookup"><span data-stu-id="f160d-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="f160d-119">กำหนดทรัพยากรตามส่วนกลาง (กำหนดผู้จัดการทรัพยากร) หรือรูปแบบไฮบริด (ผู้จัดการทรัพยากรและผู้จัดการอื่นๆ สามารถกำหนดได้)</span><span class="sxs-lookup"><span data-stu-id="f160d-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="f160d-120">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าส่วนกลางเทียบกับแบบจำลองการจัดการทรัพยากรไฮบริด ดู [ตั้งค่าคอนฟิกการตั้งค่าพารามิเตอร์เพิ่มเติม (Project Service)](../psa/configure-additional-parameters-settings.md)</span><span class="sxs-lookup"><span data-stu-id="f160d-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../psa/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="f160d-121">คุณสามารถจัดการทรัพยากรสำหรับโครงการต่างๆได้อย่างมีประสิทธิภาพ และให้แน่ใจว่าโครงการจัดเตรียมพนักงานอย่างเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="f160d-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="f160d-122">คุณจะต้องการแท็บนี้เพื่อทำงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f160d-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="f160d-123">[จัดการคำขอของทรัพยากร](../psa/manage-resource-requests.md)</span><span class="sxs-lookup"><span data-stu-id="f160d-123">[Manage resource requests](../psa/manage-resource-requests.md).</span></span> <span data-ttu-id="f160d-124">จับคู่ทักษะและความชำนาญของที่ปรึกษาของคุณไปยังโครงการที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="f160d-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="f160d-125">[ดูความพร้อมใช้งานของทรัพยากร](../psa/view-resource-availability.md)</span><span class="sxs-lookup"><span data-stu-id="f160d-125">[View resource availability](../psa/view-resource-availability.md).</span></span> <span data-ttu-id="f160d-126">ตรวจสอบความพร้อมใช้งานของที่ปรึกษาในมุมมองปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="f160d-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="f160d-127">[ดูการใช้ประโยชน์ของทรัพยากร](../psa/view-resource-utilization.md)</span><span class="sxs-lookup"><span data-stu-id="f160d-127">[View resource utilization](../psa/view-resource-utilization.md).</span></span> <span data-ttu-id="f160d-128">ดูเปอร์เซ็นต์ของเวลาที่ที่ปรึกษาของคุณถูกจองอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="f160d-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="f160d-129">[จัดกำหนดการทรัพยากรสำหรับโครงการ](../psa/schedule-resources-project.md)</span><span class="sxs-lookup"><span data-stu-id="f160d-129">[Schedule resources for a project](../psa/schedule-resources-project.md).</span></span> <span data-ttu-id="f160d-130">จัดกำหนดการที่ปรึกษาสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="f160d-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="f160d-131">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการส่งคำร้องขอทรัพยากรสำหรับแต่ละโครงการ ดู [ส่งคำขอทรัพยากร](../psa/submit-resource-requests.md)</span><span class="sxs-lookup"><span data-stu-id="f160d-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../psa/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f160d-132">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f160d-132">See Also</span></span>  
 <span data-ttu-id="f160d-133">[ภาพรวมของ Project Service](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="f160d-133">[Overview of Project Service](../psa/overview.md) </span></span>  
 <span data-ttu-id="f160d-134">[คู่มือของผู้ดูแลระบบ](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f160d-134">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="f160d-135">[คำแนะนำผู้จัดการลูกค้าองค์กร](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f160d-135">[Account Manager Guiden](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="f160d-136">[คำแนะนำของผู้จัดการโครงการ](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f160d-136">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="f160d-137">เวลา ค่าใช้จ่าย และคำแนะนำในการทำงานร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="f160d-137">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
