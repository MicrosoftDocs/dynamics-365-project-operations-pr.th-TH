---
title: ภาพรวมโหมดการจัดการทรัพยากร
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันการจัดการทรัพยากรใน Dynamics 365 Project Operations
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d132bcbef5421202d2f4899091f0dc75166dd66
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949972"
---
# <a name="resource-management-modes-overview"></a>ภาพรวมโหมดการจัดการทรัพยากร

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_


Dynamics 365 Project Operations รองรับสองโหมดเพื่อให้คุณสามารถดำเนินการตามโฟลว์การจองโดยรวม โหมดการจัดการมีการกำหนดเป็นพารามิเตอร์โครงการและสามารถแก้ไขได้หากธุรกิจของคุณต้องการการเปลี่ยนแปลง    

## <a name="central-mode"></a>โหมดส่วนกลาง
สำหรับองค์กรที่รวมศูนย์การจัดสรรทรัพยากรให้กับโครงการ โหมดส่วนกลางจะกำหนดวิธีที่จะทำให้ผู้จัดการโครงการสามารถกำหนดความต้องการทรัพยากรในระดับโครงการได้ การปฏิบัติตามความต้องการทรัพยากรถูกมอบหมายให้กับผู้จัดการทรัพยากร ผู้จัดการโครงการสามารถยอมรับหรือปฏิเสธทรัพยากรที่เสนอโดยผู้จัดการทรัพยากรได้

![โหมดส่วนกลาง](./media/resource-management-central.png)

หากต้องการจัดการทรัพยากรด้วยโหมดส่วนกลาง โปรดดู:

- [มอบหมายทรัพยากรทั่วไปที่จองได้ให้กับงานและสร้างความต้องการของทรัพยากร](/dynamics365/project-service/assign-generic-bookable-resource)
- [จองทรัพยากรที่ระบุชื่อจากความต้องการทรัพยากร](/dynamics365/project-service/book-named-resource)
- [ส่งคำขอทรัพยากร](/dynamics365/project-service/submit-resource-request)
- [เติมเต็มคำขอทรัพยากร](/dynamics365/project-service/resource-management-fulfill-requests)
- [ยอมรับหรือปฏิเสธทรัพยากรโครงการที่นำเสนอจากคำขอทรัพยากร](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>โหมดไฮบริด
สำหรับองค์กรที่ต้องการความยืดหยุ่นในการจัดสรรทรัพยากร โหมดไฮบริดช่วยให้ทั้งผู้จัดการโครงการและผู้จัดการทรัพยากรสามารถจองทรัพยากรได้

![โหมดไฮบริด](./media/resource-management-hybrid.png)

นอกเหนือจากกระบวนการของโหมดส่วนกลางที่รองรับแล้ว โปรดดูหัวข้อต่อไปนี้เพื่อจัดการขั้นตอนการจองที่รองรับอื่นๆ ทั้งหมดในโหมดไฮบริด:

จองทรัพยากรให้กับโครงการโดยตรง
- [จองทรัพยากรที่มีชื่อว่าสามารถจองได้ให้ทีมโครงการและมอบหมายงาน](/dynamics365/project-service/assign-named-bookable-resource)

จองทรัพยากรจากความต้องการทรัพยากร:
- [มอบหมายทรัพยากรทั่วไปที่จองได้ให้กับงานและสร้างความต้องการของทรัพยากร](/dynamics365/project-service/assign-generic-bookable-resource)
- [จองทรัพยากรที่ระบุชื่อจากความต้องการทรัพยากร](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]