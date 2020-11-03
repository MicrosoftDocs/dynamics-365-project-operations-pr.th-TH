---
title: กำหนดการตั้งค่าพารามิเตอร์เพิ่มเติม
description: วิธีการตั้งค่าคอนฟิกการตั้งค่าพารามิเตอร์เพิ่มเติมใน Project Service
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
ms.openlocfilehash: 24a4fe83471da916fb91cfe20e739279c08d8e5e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085932"
---
# <a name="configure-additional-parameter-settings-project-service"></a>ตั้งค่าคอนฟิกการตั้งค่าพารามิเตอร์เพิ่มเติม (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

หลังจากที่คุณได้ตั้งค่าคอนฟิกสินค้าในหัวข้อก่อนหน้านี้ คุณจำเป็นต้องตั้งค่าพารามิเตอร์โครงการเพิ่มเติมเพื่อใช้สำหรับโครงการของคุณ เมื่อคุณติดตั้ง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ในตอนแรก คุณได้สร้างการตั้งค่าพารามิเตอร์เพื่อสร้างเรกคอร์ดทั้งหมดที่จำเป็นสำหรับให้ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ทำงานเป็นลำดับแรก ขณะนี้ เป็นเวลาในการย้อนกลับ และตั้งค่าคอนฟิกฟิลด์เพิ่มเติมสำหรับการตั้งค่าเหล่านี้  
  
 คุณจะต้องตั้งค่าคอนฟิกการตั้งค่าต่อไปนี้:  
  
-   หน่วยองค์กร  
  
-   ความถี่ของใบแจ้งหนี้  
  
-   เท็มเพลตชั่วโมงทำงาน  
  
-   ราคาตลาด  
 
ในขั้นตอนนี้ คุณจะยังระบุชนิดของการปันส่วนทรัพยากรที่คุณต้องการด้วย:  
  
- **กลาง** เฉพาะผู้จัดการทรัพยากรสามารถปันส่วนทรัพยากรให้กับโครงการได้  
  
- **ไฮบริด** ผู้จัดการทรัพยากร ผู้จัดการโครงการ และผู้จัดการฝ่ายบัญชีสามารถปันส่วนทรัพยากรให้กับโครงการได้  
  
 
เพื่อตั้งค่าพารามิเตอร์โครงการ:  
  
1. ไปที่ **Project Service >พารามิเตอร์**  
  
2. คลิกการตั้งค่าพารามิเตอร์ที่คุณต้องการกำหนดค่า (รายการที่สร้างขึ้นเมื่อคุณติดตั้ง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ในตอนแรก) หรือคลิก **สร้าง** เพื่อสร้างขึ้นใหม่  
  
3. ในพื้นที่ **ทั่วไป** ตั้งค่าตัวเลือกทั้งหมดสำหรับพารามิเตอร์โครงการของคุณ  
  
4. ในพื้นที่ **ราคาตลาด** คลิก **+** เมื่อต้องการเพิ่มราคาตลาด เลือกราคาตลาดในรายการแบบหล่นลง **ราคาตลาดของพารามิเตอร์โครงการ** และจากนั้นคลิก **บันทึก**  
  
5. คลิกปุ่ม **บันทึก** ที่มุมล่างขวาของหน้าจอ  

> [!NOTE]
> เรกคอร์ดพารามิเตอร์ของโครงการต้องได้รับการปรับปรุงเพื่อให้ Project Service ทำงานได้อย่างถูกต้อง ไม่ควรลบเรกคอร์ดนี้

### <a name="see-also"></a>ดูเพิ่มเติม  
 [ตั้งค่าทรัพยากรที่สามารถจองได้](../psa/set-up-resources.md)
