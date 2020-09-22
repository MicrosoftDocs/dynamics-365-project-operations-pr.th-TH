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
ms.prod: ''
ms.technology: ''
ms.assetid: 038c5c66-f136-4c7e-88c2-30ada80bbf38
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9265ee78b20899026277e5af8e589112cd9fac74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756360"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="3b455-103">เปิดใช้งานคุณลักษณะแอป Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="3b455-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="3b455-104">ทรัพยากรของคุณสามารถใช้แอพ Project Finder Mobile บนโทรศัพท์ของพวกเขาด้วย [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] เพื่อค้นหาโครงการใหม่ที่จะทำงาน และอัพเดตชุดทักษะของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="3b455-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="3b455-105">แอปพร้อมใช้งานสำหรับ [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)] [!INCLUDE[tn_android](../includes/tn-android.md)] โทรศัพท์และ [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)]</span><span class="sxs-lookup"><span data-stu-id="3b455-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="3b455-106">คุณต้องตั้งค่าตัวเลือกสองตัวเลือกในพารามิเตอร์ ที่ตั้งค่าสำหรับหน่วยขององค์กรเพื่ออนุญาตให้ผู้ใช้สามารถดูความต้องการทรัพยากรของโครงการ และอัพเดตทักษะของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="3b455-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3b455-107">แอป Project Finder Mobile ทำงานกับ [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] เท่านั้น ไม่ทำงานกับการติดตั้งแบบ on-premises</span><span class="sxs-lookup"><span data-stu-id="3b455-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="3b455-108">ไปที่ **Project Service >พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="3b455-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="3b455-109">คลิกการตั้งค่าพารามิเตอร์ที่คุณต้องการใช้ สำหรับการอนุญาตแอป Project Finder Mobile</span><span class="sxs-lookup"><span data-stu-id="3b455-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="3b455-110">ในพื้นที่ **ทั่วไป** ตั้งค่า **ความต้องการทรัพยากรให้สามารถมองเห็นทรัพยากร** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="3b455-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="3b455-111">ตั้งค่า **อนุญาตการอัพเดตทักษะโดยทรัพยากร** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="3b455-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="3b455-112">![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="3b455-112">![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="3b455-113">นี่คือการตั้งค่าสากล</span><span class="sxs-lookup"><span data-stu-id="3b455-113">This is a global setting.</span></span> <span data-ttu-id="3b455-114">ผู้จัดการโครงการสามารถตั้งค่าว่าโครงการแต่ละโครงการจะปรากฏอยู่บนหน้า **ทีมโครงการ** ของโครงการนั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3b455-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="3b455-115">![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="3b455-115">![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="3b455-116">การแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="3b455-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="3b455-117">ส่งอีเมลที่เกี่ยวข้องกับการร้องขอทรัพยากร ไปยังผู้รับต่อไปนี้ตามช่วงเวลาต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3b455-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="3b455-118">ผู้รับ</span><span class="sxs-lookup"><span data-stu-id="3b455-118">Recipient</span></span>|<span data-ttu-id="3b455-119">กิจกรรมพิเศษ</span><span class="sxs-lookup"><span data-stu-id="3b455-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="3b455-120">ผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="3b455-120">Project manager</span></span>|<span data-ttu-id="3b455-121">-   เมื่อทรัพยากรลงทะเบียนสำหรับโครงการที่มีแอป Project Finder Mobile</span><span class="sxs-lookup"><span data-stu-id="3b455-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="3b455-122">ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="3b455-122">Resource</span></span>|<span data-ttu-id="3b455-123">-   เมื่อทรัพยากรของงานโครงการได้ลงชื่อสมัครสำหรับการได้มีการการเติมเรียบร้อยแล้วโดยทรัพยากรอื่น</span><span class="sxs-lookup"><span data-stu-id="3b455-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="3b455-124">-   เมื่อคำขอการอนุมัติทักษะของพวกเขาได้รับการอนุมัติ หรือถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="3b455-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="3b455-125">-   เมื่อคำขอการลงทะเบียนโครงการของพวกเขาได้รับการอนุมัติ หรือถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="3b455-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="3b455-126">ประกาศเกี่ยวกับความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="3b455-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="3b455-127">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3b455-127">See Also</span></span>  
 [<span data-ttu-id="3b455-128">ตั้งค่าทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="3b455-128">Set up resources</span></span>](../project-service/set-up-resources.md)
