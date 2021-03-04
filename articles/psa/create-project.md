---
title: สร้างโครงการ
description: วิธีการสร้างโครงการใน Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: 93958f8e7654ebc4cb038ba7ca0c5e4e02f39937
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148891"
---
# <a name="create-a-project-project-service"></a><span data-ttu-id="3ab9e-103">สร้างโครงการ (Project Service)</span><span class="sxs-lookup"><span data-stu-id="3ab9e-103">Create a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="3ab9e-104">สร้างโครงการโดยใช้ความสามารถของ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ใน [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] เมื่อคุณต้องการสร้างโอกาสทางการขาย ใบเสนอราคา หรือสัญญาสำหรับบริการตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="3ab9e-104">Create a project using the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] when you want to create an opportunity, quote, or contract for project-based services.</span></span> <span data-ttu-id="3ab9e-105">ความสามารถ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ช่วยคุณจัดการโครงการของคุณจากโอกาสทางการขายจนกระทั่งเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="3ab9e-105">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities help you manage your project from opportunity through completion.</span></span> <span data-ttu-id="3ab9e-106">เมื่อคุณสร้างโครงการ คุณจะสร้างโครงสร้างการแบ่งงาน ซึ่งมีผลกับใบเสนอราคา การประมาณการต้นทุน และการจัดการทรัพยากรของคุณ</span><span class="sxs-lookup"><span data-stu-id="3ab9e-106">When you create a project, you’ll also create a work breakdown structure, which affects your quotes, cost estimates, and resource management.</span></span>  
  
1.  <span data-ttu-id="3ab9e-107">ไปที่ **Project Service > โครงการ**</span><span class="sxs-lookup"><span data-stu-id="3ab9e-107">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="3ab9e-108">คลิก **โครงการใหม่**</span><span class="sxs-lookup"><span data-stu-id="3ab9e-108">Click **New Project**.</span></span>  
  
3.  <span data-ttu-id="3ab9e-109">ในพื้นที่ **สรุป** ป้อนชื่อสำหรับโครงการของคุณ แล้วกรอกรายละเอียดให้มากเท่าที่คุณสามารถทำได้</span><span class="sxs-lookup"><span data-stu-id="3ab9e-109">In the **Summary** area, enter a name for your project, and then fill in as many of the details as you can.</span></span> <span data-ttu-id="3ab9e-110">รายการที่มีเครื่องหมายดอกจันสีแดง (\*) จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="3ab9e-110">Items marked with a red asterisk (\*) are required.</span></span>  
  
4.  <span data-ttu-id="3ab9e-111">คลิก **บันทึก** เพื่อสร้างโครงการที่คุณจะสามารถทำการแก้ไขต่อไปได้</span><span class="sxs-lookup"><span data-stu-id="3ab9e-111">Click **Save** to create your project so you can continue editing it.</span></span>  
  
<span data-ttu-id="3ab9e-112">ถัดไป คุณจะสร้างโครงสร้างการแบ่งงานสำหรับโครงการของคุณเพื่อกำหนดงาน การกำหนดเวลา และบทบาทของทรัพยากรที่จำเป็นสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="3ab9e-112">Next, you’ll create a work breakdown structure for your project to define the tasks, timing, and resource roles needed for the project.</span></span>  

> [!NOTE]
> <span data-ttu-id="3ab9e-113">เมื่อจัดกำหนดการ Project Service Automation จะใช้โซนเวลาของแม่แบบ **ชั่วโมงการทำงาน** ที่ใช้</span><span class="sxs-lookup"><span data-stu-id="3ab9e-113">When scheduling, Project Service Automation respects the time zone of the applied **Work Hour** template.</span></span> <span data-ttu-id="3ab9e-114">อย่างไรก็ตามเมื่อดูงานกำหนดการ วันที่เริ่มต้นและวันที่สิ้นสุดของงานจะแสดงในโซนเวลาของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="3ab9e-114">However, when viewing the schedule tasks, the start and end dates of a task will be displayed in the user's time zone.</span></span> <span data-ttu-id="3ab9e-115">การดำเนินการนี้ใช้กับมุมมองแบบระยะเวลาอื่นๆ ในฟอร์ม **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="3ab9e-115">This applies to other time-phased views in the **Project** form.</span></span> <span data-ttu-id="3ab9e-116">หากโซนเวลาของผู้ใช้ไม่ตรงกับโซนเวลาของแม่แบบชั่วโมงการทำงานที่ใช้กับโครงการ คำเตือนที่อธิบายถึงความแตกต่างจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="3ab9e-116">If the user's time zone does not match the time zone of the work hour template applied to the project, a warning which explains the difference will occur.</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="3ab9e-117">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3ab9e-117">See Also</span></span>  
 [<span data-ttu-id="3ab9e-118">คำแนะนำของผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="3ab9e-118">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
