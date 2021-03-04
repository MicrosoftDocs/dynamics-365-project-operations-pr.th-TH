---
title: ข้อควรพิจารณาในการอัพเกรดสำหรับโครงสร้างการแบ่งงาน
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการอัพเกรดโครงสร้างการแบ่งงานจาก Project Service Automation 2.x เป็น 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: cea8ce7f61fbc0f0c8c8deb522bc332be102238d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149566"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>ข้อควรพิจารณาในการอัพเกรดสำหรับโครงสร้างการแบ่งงาน

[!include [banner](../includes/psa-now-project-operations.md)]

หัวข้อนี้แสดงข้อมูลเกี่ยวกับการอัพเกรดโครงสร้างการแบ่งงานจาก Project Service Automation 2.x เป็น 3.x. หัวข้อนี้กำหนดสถานะสุขภาพของโครงการใน Project Service Automation (PSA) ที่จำเป็นสำหรับการอัพเกรดที่ประสบความสำเร็จ นอกจากนี้ยังมีข้อมูลเกี่ยวกับเงื่อนไขการปิดกั้นทั่วไปที่จะทำให้การอัพเกรดล้มเหลว สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการกำหนดงานของโครงการและฟังก์ชันภายในกำหนดการโครงการ ให้ดูที่ [ตารางเวลาโครงการ](project-creating.md)

## <a name="key-entities"></a>เอนทิตีคีย์
สำหรับโครงสร้างการแบ่งงานที่ถูกต้องที่ถูกโหลดด้วยทรัพยากรอยู่แล้ว จำเป็นต้องมีเอนทิตีต่อไปนี้:

- [โครงการ](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [ทีมโครงการ](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [งานโครงการ](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [การมอบหมายทรัพยากร](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [การขึ้นต่อกันของงานโครงการ](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [ทรัพยากรที่สามารถจองได้](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

ในการกำหนดโครงสร้างการแบ่งงานที่โหลดทรัพยากร คุณต้องดำเนินการขั้นตอนต่อไปนี้:

1. สร้างโครงการใหม่ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างโครงการใหม่ ให้ดูที่ [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
2. สร้างงานอย่างน้อยหนึ่งภารกิจ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างงาน ให้ดูที่ [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
3. กำหนดการขึ้นต่อกันของงาน สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
4. มอบหมายสมาชิกทีมโครงการให้กับโครงการ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
5. มอบหมายสมาชิกทีมโครงการให้กับงาน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)

## <a name="project-team-relationships"></a>ความสัมพันธ์ของสมาชิกทีมโครงการ

เพื่อให้แน่ใจว่าการอัพเกรดประสบความสำเร็จ จะต้องมีการรักษาความสัมพันธ์ต่อไปนี้อย่างถูกต้อง:
- สมาชิกในทีมโครงการทั้งหมดต้องเชื่อมโยงกับทรัพยากรที่สามารถจองได้
- สมาชิกในทีมโครงการทั้งหมดต้องเชื่อมโยงกับโครงการเดียวกัน 

## <a name="project-task-relationships"></a>ความสัมพันธ์ของงานโครงการ
เพื่อให้แน่ใจว่าการอัพเกรดประสบความสำเร็จ จะต้องมีการรักษาความสัมพันธ์ต่อไปนี้อย่างถูกต้อง:

- งานที่เกี่ยวข้องใดๆต้องเชื่อมโยงกับโครงการเดียวกัน
- ทุกงานในรายการต้องมีงานหลัก
- ทุกงานต้องมีโครงการหลัก

### <a name="valid-conditions"></a>เงื่อนไขที่ถูกต้อง

- ระยะเวลาของงานทั้งหมดต้องมากกว่าหรือเท่ากับ (> =) หนึ่งชั่วโมงและน้อยกว่า 1,800,000 นาที (1,250 วัน)*
- งานทั้งหมดต้องมีวันที่เริ่มต้นไม่เร็วกว่า 2000/01/01 *
- งานทั้งหมดต้องมีวันที่เริ่มต้นไม่เกิน 17 ปีนับจากวันปัจจุบัน*
- งานทั้งหมดต้องมีวันที่เริ่มต้นเร็วกว่าหรือเท่ากับวันที่เสร็จสิ้น
- ชนิดธุรกรรมทั้งหมดในการจัดประเภท (ค่าใช้จ่าย วัสดุ ภาษี และเวลา) ต้องมีค่าสำหรับ **หน่วยเริ่มต้น** และ **กลุ่มของหน่วยนับ**
- ควรหลีกเลี่ยงรูปแบบวันที่ที่มีตัวอักษร

### <a name="potential-mitigation-steps"></a>ขั้นตอนการบรรเทาที่มีศักยภาพ
- ใช้การค้นหาขั้นสูงเพื่อระบุงานโครงการที่ไม่มีรหัสโครงการ
- ใช้การค้นหาขั้นสูงเพื่อระบุงานโครงการที่ระยะเวลาที่กำหนดมากกว่า > 1,800,000
- ก่อนทำการเปลี่ยนแปลงข้อมูลใดๆ คุณควรตรวจสอบการปรับแต่งใดๆ ที่เกี่ยวข้องกับเอนทิตีที่อาจนำไปสู่การนำข้อมูลเข้าสู่สถานะไม่ดี การกำหนดการเหล่านี้ควรได้รับการแก้ไขก่อนที่จะดำเนินการอัปเดตที่เกี่ยวข้องกับข้อมูลใดๆ
- สำหรับงานที่ระบุที่ได้รับการลงทะเบียนแล้ว ให้พิจารณาลบงานเหล่านี้หากไม่จำเป็น หรือหากคิดว่าควรเกี่ยวข้องกับโครงการหลักที่ถูกต้อง
- สำหรับงานใดๆ ที่มีระยะเวลามากกว่า 1,250 วัน ให้พิจารณาเพิ่มงานหลายรายการเพื่อแสดงระยะเวลารวมหากเป็นไปได้

> [!NOTE]
> รายการที่ระบุด้วยเครื่องหมายดอกจัน (\*) มีขีดจำกัดที่เนื่องจากข้อเท็จจริงที่ว่าการจัดการความสัมพันธ์ลูกค้า (CRM) สนับสนุนเฉพาะการขยายการเกิดขึ้นประจำ 7,320 รายการ คุณต้องอยู่ต่ำกว่าขีดจำกัดนี้

## <a name="resource-assignment-relationships"></a>ความสัมพันธ์การมอบหมายทรัพยากร
เพื่อให้แน่ใจว่าการอัพเกรดประสบความสำเร็จ จะต้องมีการรักษาความสัมพันธ์ต่อไปนี้อย่างถูกต้อง:

- การมอบหมายทรัพยากรทั้งหมดในโครงสร้างการแบ่งงานต้องเกี่ยวข้องกับโครงการเดียวกัน
- การมอบหมายทรัพยากรทั้งหมดในโครงสร้างการแบ่งงานต้องเกี่ยวข้องกับสมาชิกทีมโครงการในโครงการเดียวกัน

### <a name="potential-mitigation-steps"></a>ขั้นตอนการบรรเทาที่มีศักยภาพ
- ระบุงานทั้งหมดที่อยู่นอกเงื่อนไขที่อธิบายไว้ข้างต้น  
- ควรลบการกำหนดทรัพยากรใดๆ ที่ไม่ถูกต้องอีกต่อไป

## <a name="project-task-dependency-relationships"></a>ความสัมพันธ์การขึ้นต่อกันของงานโครงการ
เพื่อให้แน่ใจว่าการอัพเกรดประสบความสำเร็จ จะต้องมีการรักษาความสัมพันธ์ต่อไปนี้อย่างถูกต้อง:

- การขึ้นต่อกันของงานโครงการทั้งหมดต้องเกี่ยวข้องกับโครงการเดียวกัน
- งานไม่สามารถมีการอ้างอิงการขึ้นต่อกันเหมือนกันมากกว่าหนึ่งครั้ง


[!INCLUDE[footer-include](../includes/footer-banner.md)]