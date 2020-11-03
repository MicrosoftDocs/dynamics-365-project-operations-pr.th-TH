---
title: ภาพรวมโหมดการจัดการทรัพยากร
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันการจัดการทรัพยากรใน Dynamics 365 Project Operations
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085820"
---
# <a name="resource-management-modes-overview"></a>ภาพรวมโหมดการจัดการทรัพยากร

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_


Dynamics 365 Project Operations รองรับสองโหมดเพื่อให้คุณดำเนินการตามขั้นตอนการจองโดยรวม โหมดการจัดการมีการกำหนดเป็นพารามิเตอร์โครงการและสามารถแก้ไขได้หากธุรกิจของคุณต้องการการเปลี่ยนแปลง    

## <a name="central-mode"></a>โหมดส่วนกลาง
สำหรับองค์กรที่รวมศูนย์การจัดสรรทรัพยากรให้กับโครงการ โหมดส่วนกลางจะกำหนดวิธีที่จะทำให้ผู้จัดการโครงการสามารถกำหนดความต้องการทรัพยากรในระดับโครงการได้ การปฏิบัติตามความต้องการทรัพยากรถูกมอบหมายให้กับผู้จัดการทรัพยากร ผู้จัดการโครงการสามารถยอมรับหรือปฏิเสธทรัพยากรที่เสนอโดยผู้จัดการทรัพยากรได้

![โหมดส่วนกลาง](./media/resource-management-central.png)

หากต้องการจัดการทรัพยากรด้วยโหมดส่วนกลาง โปรดดู:

- [มอบหมายทรัพยากรทั่วไปที่จองได้ให้กับงานและสร้างความต้องการของทรัพยากร](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [จองทรัพยากรที่ระบุชื่อจากความต้องการทรัพยากร](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [ส่งคำขอทรัพยากร](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [เติมเต็มคำขอทรัพยากร](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [ยอมรับหรือปฏิเสธทรัพยากรโครงการที่นำเสนอจากคำขอทรัพยากร](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>โหมดไฮบริด
สำหรับองค์กรที่ต้องการความยืดหยุ่นในการจัดสรรทรัพยากร โหมดไฮบริดช่วยให้ทั้งผู้จัดการโครงการและผู้จัดการทรัพยากรสามารถจองทรัพยากรได้

![โหมดไฮบริด](./media/resource-management-hybrid.png)

นอกเหนือจากกระบวนการของโหมดส่วนกลางที่รองรับแล้ว โปรดดูหัวข้อต่อไปนี้เพื่อจัดการขั้นตอนการจองที่รองรับอื่นๆ ทั้งหมดในโหมดไฮบริด:

จองทรัพยากรให้กับโครงการโดยตรง
- [จองทรัพยากรที่มีชื่อว่าสามารถจองได้ให้ทีมโครงการและมอบหมายงาน](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

จองทรัพยากรจากความต้องการทรัพยากร:
- [มอบหมายทรัพยากรทั่วไปที่จองได้ให้กับงานและสร้างความต้องการของทรัพยากร](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [จองทรัพยากรที่ระบุชื่อจากความต้องการทรัพยากร](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
