---
title: เปิดใช้งานคุณลักษณะแอป Project Finder Mobile
description: วิธีการเปิดใช้งานคุณลักษณะแอป Project Finder Mobile สำหรับ Project Service
author: JohnPBurrows
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: 1b70182125d607aa17528ef3dc4ea2345b76acd1
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144571"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>เปิดใช้งานคุณลักษณะแอป Project Finder Mobile (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

ทรัพยากรของคุณสามารถใช้แอป Project Finder Mobile บนโทรศัพท์ของพวกเขาด้วย [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] เพื่อค้นหาโครงการใหม่ที่จะทำงาน และอัปเดตชุดทักษะของพวกเขา  
  
 แอปพร้อมใช้งานสำหรับ [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)] [!INCLUDE[tn_android](../includes/tn-android.md)] โทรศัพท์และ [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)]  
    
 เพื่ออนุญาตให้ผู้ใช้สามารถดูความต้องการทรัพยากรของโครงการ และอัปเดตทักษะ คุณต้องเลือกตัวเลือกในการตั้งค่าพารามิเตอร์สำหรับหน่วยขององค์กรของคุณ
  
> [!NOTE]
>  แอป Project Finder Mobile ทำงานกับ [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] เท่านั้น ไม่ทำงานกับการติดตั้งแบบ on-premises  
  
1. ไปที่ **Project Service >พารามิเตอร์**  
  
2. คลิกการตั้งค่าพารามิเตอร์ที่คุณต้องการใช้ สำหรับการอนุญาตแอป Project Finder Mobile  
  
3. ในพื้นที่ **ทั่วไป** ตั้งค่า **ความต้องการทรัพยากรให้สามารถมองเห็นทรัพยากร** เป็น **ใช่**  
  
4. ตั้งค่า **อนุญาตการอัพเดตทักษะโดยทรัพยากร** เป็น **ใช่**  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   นี่คือการตั้งค่าสากล ผู้จัดการโครงการสามารถตั้งค่าว่าโครงการแต่ละโครงการจะปรากฏอยู่บนหน้า **ทีมโครงการ** ของโครงการนั้นหรือไม่  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>การแจ้งเตือนทางอีเมล  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ส่งอีเมลที่เกี่ยวข้องกับการร้องขอทรัพยากร ไปยังผู้รับต่อไปนี้ตามช่วงเวลาต่อไปนี้:  
  
|ผู้รับ|กิจกรรมพิเศษ|  
|---------------|-----------|  
|ผู้จัดการโครงการ|- ทรัพยากรลงทะเบียนสำหรับโครงการที่มีแอป Project Finder Mobile|  
|ทรัพยากร|- งานโครงการที่ทรัพยากรได้ลงทะเบียนให้ ได้มีการดำเนินการเรียบร้อยแล้วโดยทรัพยากรอื่น<br />- คำขอการอนุมัติทักษะได้รับอนุมัติ หรือถูกปฏิเสธ<br />- คำขอการลงทะเบียนโครงการได้รับอนุมัติ หรือถูกปฏิเสธ|  
  
## <a name="privacy-notice"></a>ประกาศเกี่ยวกับความเป็นส่วนตัว  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>ดูเพิ่มเติม  
 [ตั้งค่าทรัพยากรที่สามารถจองได้](../psa/set-up-resources.md)
