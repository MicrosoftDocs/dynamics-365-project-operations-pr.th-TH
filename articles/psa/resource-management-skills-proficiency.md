---
title: แบบจำลองทักษะและความชำนาญ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้แบบจำลองทักษะและความชำนาญ
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.openlocfilehash: cd243544df062e5801bbfa0a3bd75c4d9a116a6f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086152"
---
# <a name="skills-and-proficiency-models"></a>แบบจำลองทักษะและความชำนาญ

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

ทักษะ คือคุณลักษณะทรัพยากรที่ใช้ร่วมกันระหว่าง Dynamics 365 Project Service Automation และ Dynamics 365 Field Service (ถ้ามี) 

เมื่อต้องการรักษาการบันทึกทักษะใน Project Service Automation ไปที่ **ทรัพยากร** \> **ทักษะของทรัพยากร** 

> ![ทักษะของทรัพยากร](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>ใช้แบบจำลองความชำนาญเพื่อจัดอันดับคะแนนทรัพยากร

ทักษะสำหรับทรัพยากรจะถูกจัดอันดับคะแนนโดยแบบจำลองความชำนาญ การจัดอันดับคะแนนรายบุคคลจะอยู่ในรูปแบบที่มีความชำนาญ 

1. หากต้องการสร้างแบบจำลองความชำนาญ ไปที่ **ทรัพยากร** \> **แบบจำลองความชำนาญ** แล้วเลือก **สร้าง**
2. ในแบบจำลองการจัดอันดับคะแนนใหม่ ระบุค่าการจัดอันดับต่ำสุด ค่าจัดอันดับสูงสุด และเอนทิตี้ที่กำลังทำการจัดอันดับคะแนนให้
3. ใน Sub-grid **ค่าการจัดอันดับคะแนน** คุณสามารถกำหนดค่าการจัดอันดับที่แตกต่างกันได้ตั้งแต่ต่ำสุดไปจนถึงสูงสุด

> ![ค่าต่ำสุดและสูงสุดของอันดับคะแนนถูกกำหนดแล้ว](media/Resource-Management-image85.png)

ค่าอันดับคะแนนเหล่านี้จะแสดงในตัวกรอง **ความต้องการทรัพยากร** **ตารางกำหนดการ** และ **ตัวช่วยจัดการกำหนดการ**