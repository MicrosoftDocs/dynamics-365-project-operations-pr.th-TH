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
ms.openlocfilehash: c34634817fc8e4c993261024a8b19d45052bf5e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085942"
---
# <a name="create-a-work-hours-template-project-service"></a>สร้างเท็มเพลตชั่วโมงทำงาน (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

ก่อนที่คุณจะสามารถสร้างกำหนดการโครงการได้ คุณจำเป็นต้องตั้งค่าปฏิทินโครงการที่กำหนดจำนวนของชั่วโมงการทำงานเพื่อให้เหมาะสมกับแต่ละวันในกำหนดการและระยะเวลาที่ปิดดำเนินการใดๆ คุณทำเช่นนี้กับแม่แบบชั่วโมงทำงาน ซึ่งประกอบด้วยรายละเอียดเกี่ยวกับชั่วโมงทำงานต่อวัน วันหยุด และระยะเวลาที่ปิดดำเนินการอื่นๆ  
  
 เมื่อคุณกำลังสร้างโครงการ คุณเชื่อมโยงแม่แบบงานไปยังปฏิทินโครงการเพื่อใช้การจัดกำหนดการสำหรับโครงการ  
  
 มีสองวิธีที่คุณสามารถสร้างต้นแบบชั่วโมงทำงาน:  
  
-   สร้างแม่แบบชั่วโมงทำงานตามปฏิทินของทรัพยากร  
  
-   สร้างแม่แบบชั่วโมงทำงานใหม่  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a>เพื่อสร้างต้นแบบชั่วโมงทำงานตามปฏิทินของทรัพยากร  
  
1.  ไปที่ **Project Service > ทรัพยากร**  
  
2.  เลือกทรัพยากรคุณต้องการให้ชั่วโมงการทำงานของคุณยึดตาม  
  
3.  คลิก **บันทึกปฏิทินเป็น** ป้อนชื่อสำหรับแม่แบบชั่วโมงทำงาน แล้วคลิก **บันทึก**  
  
4.  เมื่อคุณเสร็จสิ้นการแก้ไขตัวเลือกแล้ว ให้คลิก **บันทึกและปิด**  
  
5.  คลิกปุ่ม **บันทึก** ที่มุมล่างขวาของหน้าจอ  
  
#### <a name="to-create-a-new-work-hours-template"></a>เพื่อสร้างแม่แบบชั่วโมงทำงานใหม่  
  
1.  ไปที่ **Project Service > แม่แบบชั่วโมงทำงาน**  
  
2.  คลิก **สร้าง**  
  
3.  ป้อนชื่อสำหรับแม่แบบชั่วโมงทำงาน  
  
4.  เลือกทรัพยากรที่จะให้ชั่วโมงการทำงานยึดตาม แล้ว คลิก **บันทึก**  
  
### <a name="see-also"></a>ดูเพิ่มเติม  
 [ตั้งค่าทรัพยากรที่สามารถจองได้](../psa/set-up-resources.md)
