---
title: เปิดใช้งานคุณลักษณะแอป Project Finder Mobile
description: วิธีการเปิดใช้งานคุณลักษณะแอป Project Finder Mobile สำหรับ Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085939"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="c7696-103">เปิดใช้งานคุณลักษณะแอป Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c7696-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c7696-104">ทรัพยากรของคุณสามารถใช้แอพ Project Finder Mobile บนโทรศัพท์ของพวกเขาด้วย [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] เพื่อค้นหาโครงการใหม่ที่จะทำงาน และอัพเดตชุดทักษะของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="c7696-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="c7696-105">แอปพร้อมใช้งานสำหรับ [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)] [!INCLUDE[tn_android](../includes/tn-android.md)] โทรศัพท์และ [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)]</span><span class="sxs-lookup"><span data-stu-id="c7696-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="c7696-106">คุณต้องตั้งค่าตัวเลือกสองตัวเลือกในพารามิเตอร์ ที่ตั้งค่าสำหรับหน่วยขององค์กรเพื่ออนุญาตให้ผู้ใช้สามารถดูความต้องการทรัพยากรของโครงการ และอัพเดตทักษะของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="c7696-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c7696-107">แอป Project Finder Mobile ทำงานกับ [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] เท่านั้น ไม่ทำงานกับการติดตั้งแบบ on-premises</span><span class="sxs-lookup"><span data-stu-id="c7696-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="c7696-108">ไปที่ **Project Service >พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="c7696-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="c7696-109">คลิกการตั้งค่าพารามิเตอร์ที่คุณต้องการใช้ สำหรับการอนุญาตแอป Project Finder Mobile</span><span class="sxs-lookup"><span data-stu-id="c7696-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="c7696-110">ในพื้นที่ **ทั่วไป** ตั้งค่า **ความต้องการทรัพยากรให้สามารถมองเห็นทรัพยากร** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="c7696-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="c7696-111">ตั้งค่า **อนุญาตการอัพเดตทักษะโดยทรัพยากร** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="c7696-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="c7696-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="c7696-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="c7696-113">นี่คือการตั้งค่าสากล</span><span class="sxs-lookup"><span data-stu-id="c7696-113">This is a global setting.</span></span> <span data-ttu-id="c7696-114">ผู้จัดการโครงการสามารถตั้งค่าว่าโครงการแต่ละโครงการจะปรากฏอยู่บนหน้า **ทีมโครงการ** ของโครงการนั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c7696-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="c7696-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="c7696-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="c7696-116">การแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="c7696-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="c7696-117">ส่งอีเมลที่เกี่ยวข้องกับการร้องขอทรัพยากร ไปยังผู้รับต่อไปนี้ตามช่วงเวลาต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c7696-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="c7696-118">ผู้รับ</span><span class="sxs-lookup"><span data-stu-id="c7696-118">Recipient</span></span>|<span data-ttu-id="c7696-119">กิจกรรมพิเศษ</span><span class="sxs-lookup"><span data-stu-id="c7696-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="c7696-120">ผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="c7696-120">Project manager</span></span>|<span data-ttu-id="c7696-121">-   เมื่อทรัพยากรลงทะเบียนสำหรับโครงการที่มีแอป Project Finder Mobile</span><span class="sxs-lookup"><span data-stu-id="c7696-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="c7696-122">ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c7696-122">Resource</span></span>|<span data-ttu-id="c7696-123">-   เมื่อทรัพยากรของงานโครงการได้ลงชื่อสมัครสำหรับการได้มีการการเติมเรียบร้อยแล้วโดยทรัพยากรอื่น</span><span class="sxs-lookup"><span data-stu-id="c7696-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="c7696-124">-   เมื่อคำขอการอนุมัติทักษะของพวกเขาได้รับการอนุมัติ หรือถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="c7696-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="c7696-125">-   เมื่อคำขอการลงทะเบียนโครงการของพวกเขาได้รับการอนุมัติ หรือถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="c7696-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="c7696-126">ประกาศเกี่ยวกับความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="c7696-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="c7696-127">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c7696-127">See Also</span></span>  
 [<span data-ttu-id="c7696-128">ตั้งค่าทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="c7696-128">Set up resources</span></span>](../psa/set-up-resources.md)
