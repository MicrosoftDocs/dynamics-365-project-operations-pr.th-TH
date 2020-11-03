---
title: กำลังส่งคำขอทรัพยากร
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการส่งคำขอสำหรับทรัพยากรโครงการ
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086025"
---
# <a name="submitting-a-resource-request"></a>กำลังส่งคำขอทรัพยากร

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

คุณสามารถส่งคำขอทรัพยากรที่สร้างขึ้นเป็นคำขอทรัพยากรได้ จากนั้นคำขอจะถูกส่งไปยังผู้จัดการทรัพยากรเพื่อทำตามคำขอ

1. ใน Project Service Automation (PSA) ในเพจ **โครงการ** ให้คลิกแท็บ **ทีม** เพื่อดูรายการทรัพยากรที่สามารถจองได้ 
2. เลือกทรัพยากรทั่วไปที่มีความจำเป็นจากในรายการ จากนั้นคลิก **ส่งคำขอ**

![กำลังส่งคำขอทรัพยากร](media/RM-how-to-18.png)

สถานะของคำขอของสมาชิกทีมทั่วไปจะถูกเปลี่ยนเป็น **ส่งแล้ว**

หลังจากคำขอได้รับการทำตามโดยผู้จัดการทรัพยากร ทรัพยากรทั่วไปจะถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อ หากผู้จัดการทรัพยากรทำตามคำขอด้วยการจองของทรัพยากรที่ระบุชื่อ มิฉะนั้น ทรัพยากรทั่วไปจะยังคงอยู่ในทีมและสถานะคำขอจะถูกเปลี่ยนเป็น **ตามมีการตรวจทาน** หากผู้จัดการทรัพยากรได้เสนอทรัพยากรที่ระบุชื่อ
