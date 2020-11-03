---
title: แนวคิดหลัก
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับแนวคิดหลักสำหรับการจัดการทรัพยากรใน Project Service Automation
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 1e5e78bbeb1086fada799cf7ac66173e5a563e2d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086156"
---
# <a name="key-concepts"></a>แนวคิดหลัก

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

ตารางต่อไปนี้กำหนดแนวคิดหลักที่ใช้ในแอป Dynamics 365 Project Service Automation

| แนวคิด                    | คำจำกัดความ |
|----------------------------|------------|
| สมาชิกของทีมโครงการ        | ในฐานะที่เป็นส่วนหนึ่งของทีมโครงการ สมาชิกทีมโครงการสามารถเป็นทรัพยากรที่มีชื่อที่มีการจอง ทรัพยากรที่ระบุชื่อที่ไม่มีการจอง หรือทรัพยากรทั่วไป ทรัพยากรทั่วไปไม่มีการจอง เป็นท้องถิ่นของโครงการ และไม่มีข้อจำกัดกำลังการผลิตในโครงการ |
| ทรัพยากรทั่วไปของโครงการ   | ตัวยึดทรัพยากรที่ช่วยให้คุณสามารถสร้างทีมงานและสรรหาแผนโครงการโดยไม่ต้องรู้ทรัพยากรที่ระบุชื่อ ปฏิทินโครงการจะถูกใช้เป็นปฏิทินของทรัพยากรทั่วไป ทรัพยากรทั่วไปสามารถเพิ่มไปยังทีมโครงการและการมอบหมายให้กับงานได้ |
| ชั่วโมงที่จอง               | ชั่วโมงทรัพยากรมีการจองแบบตายตัวกับโครงการเพื่อช่วยรับประกันว่างานโครงการเสร็จสมบูรณ์แล้ว ชั่วโมงที่จองจะถูกใช้จากกำลังการผลิตโดยรวมของทรัพยากร การจองจะเทียบกับทรัพยากรที่ระบุชื่อเท่านั้นไม่ได้เทียบกับทรัพยากรทั่วไป |
| ชั่วโมงที่มอบหมาย             | ชั่วโมงทรัพยากรจะถูกมอบหมายให้กับงานในหมายกำหนดการให้บริการโครงการ การมอบหมายจะสามารถเทียบได้กับทรัพยากรที่ระบุชื่อหรือทรัพยากรทั่วไปอย่างใดอย่างหนึ่ง การมอบหมายสามารถเป็นอิสระจากการจอง |
| ชั่วโมงที่ต้องการ             | กำลังการผลิตที่จำเป็นแต่ยังไม่ได้ดำเนินการโดยทรัพยากรที่ระบุชื่อ ชั่วโมงที่ต้องการจะเกี่ยวข้องเฉพาะกับสมาชิกในทีมทั่วไปที่สร้างความต้องการทรัพยากรเท่านั้น |
| ตามความต้องการ                     | ปริมาณงานปัจจุบันและที่กำลังเข้ามา ใน Project Service Automation ความต้องการจะแสดงเป็นความต้องการทรัพยากรหรือคำขอทรัพยากร |
| ความต้องการทรัพยากร       | เอนทิตีที่ใช้ในการบันทึกชั่วโมงที่ต้องการ วันที่เริ่มต้นและสิ้นสุด ทักษะ ภูมิศาสตร์ และมิติการกำหนดราคาอื่นๆสำหรับทรัพยากรที่จำเป็น ความต้องการทรัพยากรจะถูกสร้างขึ้นจากสมาชิกในทีมโครงการหรือที่สร้างขึ้นเป็นรายบุคคลอย่างใดอย่างหนึ่ง |
| คำขอทรัพยากร           | เอนทิตีที่ใช้เป็น "จดหมาย" เพื่อดำเนินการตามความต้องการทรัพยากรที่ต้องปฏิบัติตามผู้จัดการทรัพยากร |
| บทบาทเริ่มต้นของทรัพยากร:      | บทบาทที่ทรัพยากรมีการจัดกลุ่มทรัพยากรภายใต้สำหรับการคำนวณการใช้ประโยชน์ ทรัพยากรจะถูกสันนิษฐานว่ามีทักษะที่จำเป็นสำหรับบทบาทและเพื่อให้เป็นไปตามการใช้ประโยชน์เป้าหมายสำหรับบทบาทนั้น |
| หน่ององค์กรทรัพยากร | หน่วยองค์กรทรัพยากรที่ทรัพยากรถูกมอบหมายให้ |
| เส้นชั้น                    | งาน ความต้องการ หรือชั่วโมงการมอบหมายเนื่องจากถูกแบ่งออกเป็นการกระจายรายวัน ตัวอย่างเช่น งาน 5 วัน 40 ชั่วโมงสามารถแบ่งเส้นชั้นได้เป็น 8 ชั่วโมงต่อวันมากกว่า 5 วัน |
| มุมมองการกระทบยอด        | มุมมองที่แสดงการจองและงานมอบหมายสำหรับสมาชิกทีมโครงการแต่ละคน มุมมองนี้ช่วยให้ผู้จัดการโครงการมองหาสิ่งใดๆที่ไม่ตรงกันระหว่างการจองและการมอบหมาย และการดำเนินการแก้ไขถ้ามีสิ่งใดที่ไม่ตรงกันเกิดขึ้น |
| ชั่่วโมงทำงาน                 | เอนทิตีที่ใช้ในการระบุกำลังการผลิตของทรัพยากรและเวลาที่ทำงานและที่ไม่ทำงาน เอนทิตีนี้เรียกอีกอย่างว่าปฏิทินทรัพยากร |