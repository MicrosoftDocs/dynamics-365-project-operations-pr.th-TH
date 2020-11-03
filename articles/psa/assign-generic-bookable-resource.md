---
title: มอบหมายทรัพยากรทั่วไปที่จองได้ให้กับงานและทีมโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการจองทรัพยากรทั่วไปให้กับงานและทีมโครงการ
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085947"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>มอบหมายทรัพยากรทั่วไปที่จองได้ให้กับงานและสร้างความต้องการทั่วไปของทรัพยากร 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

นอกเหนือจากการจองและการกำหนดทรัพยากรที่มีชื่อหรือทรัพยากรจริงให้กับโครงการของคุณแล้ว คุณสามารถกำหนดทรัพยากรทั่วไปให้กับงานของโครงการได้ ทรัพยากรเหล่านี้สามารถทำหน้าที่เป็นตัวยึดสำหรับทรัพยากรที่มีชื่อจนกว่าคุณจะพร้อมที่จะสรรหาพนักงานสำหรับโครงการของคุณด้วยทรัพยากรที่มีชื่อ 

1. ใน Project Service Automation (PSA) เปิดหน้า **โครงการ** และบนแท็บ **กำหนดการ** ป้อนชื่อตำแหน่งของทรัพยากรทั่วไปในเซลล์ **ทรัพยากร** ของกำหนดการ หรือคลิกไอคอน **ทรัพยากร** ในเซลล์เพื่อเปิดตัวเลือกทรัพยากรแล้วป้อนชื่อของทรัพยากรทั่วไปที่คุณต้องการสร้าง

![การสร้างและการกำหนดสมาชิกในทีมทั่วไป](media/RM-how-to-9.png)

การทำเช่นนี้จะเป็นการเปิดแผง **การสร้างด่วน: สมาชิกทีมโครงการ**  

2. ป้อนบทบาทและหน่วยองค์กรของสมาชิกทีมทรัพยากรทั่วไป แล้วคลิก **บันทึก**

![สมาชิกในทีมทั่วไปสร้างอย่างรวดเร็ว](media/RM-how-to-10.png)

3. หลังจากที่คุณได้สร้างสมาชิกทีมทรัพยากรทั่วไปใหม่แล้วจะมีการกำหนดไปให้กับงาน คุณสามารถกำหนดทรัพยากรทั่วไปให้กับงานอื่นๆ ในกำหนดการงานได้ต่อไป

![การกำหนดสมาชิกในทีมทั่วไปที่มีอยู่ให้กับงาน](media/RM-how-to-11.png)

4. หลังจากที่คุณได้กำหนดทรัพยากรทั่วไปแล้ว คุณสามารถสร้างความต้องการของทรัพยากรและทำให้เสร็จได้โดยการจองโดยตรงหรือส่งการร้องขอทรัพยากรไปยังผู้จัดการทรัพยากร

![การสร้างความต้องการสำหรับสมาชิกทั่วไปในทีม](media/RM-how-to-12.png)

ในกริดสมาชิกทีม นอกเหนือจากความสามารถในการใช้ตัวเลือกทรัพยากรดังกล่าวข้างต้น คุณสามารถเพิ่มทรัพยากรทั่วไปได้โดยตรง ทรัพยากรจะถูกเพิ่มด้วยความต้องการทรัพยากรที่ขึ้นอยู่กับวันที่เริ่มต้น/สิ้นสุด และวิธีการจัดสรรที่ระบุไว้ในแผง **การสร้างด่วน: สมาชิกทีมโครงการ**

คุณสามารถดูความแตกต่างหากคุณเพิ่มสมาชิกในทีมทั่วไปโดยตรง จากนั้นกำหนดงานเพิ่มเติมให้กับทรัพยากรทั่วไปมากกว่าชั่วโมงที่ครอบคลุมที่พวกเขาต้องการ คลิก **สร้างความต้องการ** เพื่อสร้างข้อกำหนดในการสร้างความสมดุลให้กับจำนวนชั่วโมงที่ต้องการกับการมอบหมาย

นอกจากนี้คุณยังสามารถคลิกการเชื่อมโยง **ความต้องการทรัพยากร** ในกริดทีมเพื่อเปิดความต้องการและเพิ่มทักษะ ทรัพยากรที่ต้องการ ฯลฯ

![ความต้องการทรัพยากร](media/RM-how-to-13.png)
