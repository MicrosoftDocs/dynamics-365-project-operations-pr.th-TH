---
title: จัดกำหนดการทรัพยากรสำหรับโครงการ
description: วิธีการจัดกำหนดการทรัพยากรสำหรับโครงการใน Project Service
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
ms.openlocfilehash: db69348aac96cbfaaa865228c9230cbda4b1e784
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086138"
---
# <a name="schedule-resources-for-a-project-project-service"></a>จัดกำหนดการทรัพยากรสำหรับโครงการ (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

คุณสามารถตรวจสอบความพร้อมใช้งานของทรัพยากรเพื่อดูมุมมองโดยรวมของวิธีการจองทรัพยากรของคุณคือ หรือคุณสามารถกรองมุมมองตามทักษะ ทีม ที่ตั้ง และตัวเลือกอื่นๆ  
  
บอร์ดกำหนดการแสดงรายการของทรัพยากรและความพร้อม เลือกโหมดมุมมองเพื่อแสดงความพร้อมใช้งานตาม **ชั่วโมง** **วัน** **สัปดาห์** หรือ **เดือน**  
  
ก่อนที่คุณจะใช้ตารางกำหนดการ สิ่งสำคัญคือการตั้งค่า สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่าคอนฟิกบอร์ดกำหนดการ (Field Service หรือ Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board)
  
ถ้าคุณกำลังใช้รุ่นที่เก่ากว่า สำหรับความพร้อมใช้งานของทรัพยากร โปรดดู [ดูความพร้อมใช้งานของทรัพยากร](../psa/view-resource-availability.md)  

> [!IMPORTANT]
>  เมื่อต้องการใช้ฟังก์ชันการจองของตารางกำหนดการ พิกัดทางภูมิศาสตร์ และบริการตำแหน่งที่ตั้ง คุณจะต้องเปิดบนแผนผัง  
> 
> 1. บนเมนูหลัก เลือก **การจัดกำหนดการทรัพยากร** > **การจัดการ**  
> 2. คลิก **พารามิเตอร์การจัดกำหนดการ**  
> 3. เปิดเรกคอร์ดและเลื่อนลงไปที่ส่วน **Resource Scheduling Optimization**  
> 4. ในฟิลด์ **เชื่อมต่อกับแผนผัง** เลือก **ใช่**  
> 5. ยอมรับข้อกำหนด และบันทึกเรกคอร์ด  
> 6. บนเมนูหลัก เลือก **Project Service** > **บอร์ดกำหนดการ** จากที่นี่ มีวิธีหลายวิธีในการจัดกำหนดการความต้องการในการจองด้วยตนเอง เลือกวิธีการที่เหมาะสมสำหรับคุณ
  
## <a name="find-available-resources"></a>ค้นหาทรัพยากรที่พร้อมใช้งาน

1.  จากรายการ **ความต้องการในการจอง** คลิกขวาที่การจองที่ไม่ได้จัดกำหนดการ และเลือกรายการใดรายการหนึ่งต่อไปนี้:  
  
- เลือก **ค้นหาความพร้อมใช้งาน - ทรัพยากรปัจจุบัน** เพื่อค้นหาทรัพยากรที่พร้อมใช้งานจากรายการบนตารางกำหนดการ  
- เลือก **ค้นหาความพร้อมใช้งาน - ทรัพยากรทั้งหมด** เพื่อค้นหาทรัพยากรที่พร้อมใช้งานจากทรัพยากรในระบบ  
   > [!NOTE]
   >  เมื่อคุณทำเช่นนี้ ตัวกรองที่จะแสดงตัวเลือกสำหรับความต้องการในการจองที่ถูกเลือก  
  
2. เมื่อคุณเห็นช่องที่พร้อมใช้งาน คลิกขวาที่ช่องเวลาบนบอร์ดกำหนดการ และเลือก **จองที่นี่** หรือลากแล้วปล่อยความต้องการในการจอง ไปที่ช่องเวลาที่พร้อมใช้งาน  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>จองทรัพยากรโดยใช้มุมมองรายวัน และค้นหาผู้ที่ไม่ได้จอง
  
1.  บนบอร์ดกำหนดการ เลือก **โหมดมุมมอง** และเลือก **วัน**  
  
    ฟิลด์นี้แสดงมุมมองกริดของจำนวนชั่วโมงที่ทรัพยากรถูกจองสำหรับแต่ละวัน และวันที่ไม่ถูกจอง  
  
2.  คลิกที่ชื่อของทรัพยากรที่คุณต้องการจอง และจากนั้น เลือก **จอง**  
  
3.  ในกล่องโต้ตอบ **การจองทรัพยากร (สร้าง)** เลือกโครงการที่คุณต้องการจองทรัพยากร รวมทั้งวิธีการจอง และเวลาเริ่มต้นและเวลาสิ้นสุด  
  
4.  เมื่อคุณทำเสร็จแล้ว เลือก **จอง**  
  
## <a name="view-to-the-schedule-board"></a>ดูไปยังบอร์ดกำหนดการ
  
1.  เลือกความต้องการในการจองที่ไม่ได้จัดกำหนดจากรายการด้านล่าง  
  
2.  ลากความต้องการในการจองไปที่ทรัพยากรที่พร้อมใช้งาน/ช่องเวลาในตารางกำหนดการ  
  
3.  เมื่อคุณทำเสร็จแล้ว เลือก **จอง**  
  
### <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม  
 [คู่มือของผู้จัดการทรัพยากร](../psa/resource-manager-guide.md)