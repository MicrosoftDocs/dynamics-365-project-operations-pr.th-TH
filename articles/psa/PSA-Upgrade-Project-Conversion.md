---
title: การเปลี่ยนแปลงคุณลักษณะสำหรับ Project Service Automation เป็น Project Operations
description: บทความนี้ให้ภาพรวมของการเปลี่ยนแปลงคุณลักษณะจาก Microsoft Dynamics 365 Project Service Automation เป็น Dynamics 365 Project Operations
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621270"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>การเปลี่ยนแปลงคุณลักษณะสำหรับ Project Service Automation เป็น Project Operations

หลังจากอัปเกรดโครงการสำเร็จจาก Microsoft Dynamics 365 Project Service Automation 3.X เป็น Dynamics 365 Project Operations Lite ไม่สามารถแก้ไขงานโครงการในโครงสร้างการแบ่งงานในตารางงาน (WBS) ได้ ลูกค้าจะสามารถตรวจสอบ WBS ในตารางการติดตามที่มีการเพิ่มฟิลด์ใหม่เพื่อให้รายละเอียดทั้งหมดที่เกี่ยวข้องกับงาน สำหรับโครงการที่จำเป็นต้องมีการแก้ไข WBS คุณสามารถเลือกแปลงโครงการที่มีสิทธิ์เป็นประสบการณ์การจัดกำหนดการ Project for the Web ได้

## <a name="project-conversion-process"></a>กระบวนการการแปลงโครงการ

เพื่อแปลงโครงการ ทำตามขั้นตอนเหล่านี้

1. เปิดหน้าหลักของโครงการ แล้วเลือก **แปลง** บนบานหน้าต่างการดำเนินการ
1. ในกล่องข้อความยืนยัน ให้เลือก **ตกลง** เพื่อเริ่มการแปลงโครงการ การดำเนินการต่อไปนี้จะเกิดขึ้น:

    1. แถบข้อความที่ปรากฏบนหน้าหลักของโครงการระบุว่า "กำลังแปลงกำหนดการโครงการ คุณไม่สามารถเปลี่ยนแปลงโครงการได้จนกว่าการแปลงจะเสร็จสมบูรณ์"
    1. คุณถูกเปลี่ยนเส้นทางไปยังรายการโครงการ

    หลังจากการแปลงโครงการเสร็จสิ้น การดำเนินการต่อไปนี้จะเกิดขึ้น:

    1. ผู้จัดการโครงการที่ได้รับมอบหมายจะได้รับการแจ้งเตือนทางด้านขวาของแอปพลิเคชัน
    1. แถบข้อความที่ระบุว่ากำลังดำเนินการแปลงจะถูกลบออก
    1. แท็บ **กำหนดการ** แสดงประสบการณ์การจัดกำหนดการใหม่กับ Project for the Web ผู้ใช้ที่มีสิทธิ์ใช้งานและบทบาทความปลอดภัยที่เหมาะสมสามารถแก้ไข WBS ได้
    1. ฟิลด์ **โปรแกรมการจัดกำหนดการ** อัปเดตเป็น **Project for the Web**
    1. ปุ่ม **แปลง** จะถูกลบออกจากบานหน้าต่างการดำเนินการ

> [!IMPORTANT]
> ไม่อนุญาตให้แปลงโครงการจำนวนมาก ความพยายามใดๆ ในการอัปเดตโครงการจำนวนมากพร้อมกันจะถูกควบคุมปริมาณ ข้อจำกัดนี้ช่วยให้มั่นใจว่ามีประสิทธิภาพสูงสำหรับลูกค้าทุกคน

## <a name="manual-tasks-vs-automatic-tasks"></a>งานที่ทำด้วยตนเองกับงานอัตโนมัติ

เมื่อสภาพแวดล้อมได้รับการอัปเกรดจาก Project Service Automation เป็น Project Operations งานทั้งหมดใน WBS จะถูกจัดกำหนดการโดยอัตโนมัติ แนวคิดของงานที่จัดกำหนดการด้วยตนเองไม่พร้อมใช้งานใน Project for the web อย่างไรก็ตาม คุณสามารถกำหนดลักษณะการจัดกำหนดการที่ต้องการสำหรับโครงการของคุณโดยใช้การตั้งค่า [โหมดการจัดกำหนดการ](/project-management/scheduling-modes.md) เมื่อคุณสร้างโครงการใหม่

## <a name="restricted-operations-for-pre-conversion-projects"></a>การดำเนินการที่จำกัดสำหรับโครงการก่อนการแปลง

ส่วนนี้สรุปความแตกต่างด้านฟังก์ชันที่คุณสามารถคาดหวังได้เมื่อโครงการยังไม่ได้แปลง

### <a name="copy-project"></a>คัดลอกโครงการ

การดำเนินการ **คัดลอก** ได้รับการสนับสนุนเฉพาะในโครงการที่แปลงแล้ว ไม่สามารถคัดลอกโครงการที่อัปเกรดก่อนการแปลง

### <a name="move-project"></a>ย้ายโครงการ

การเปลี่ยนแปลงวันที่เริ่มต้นของโครงการจะไม่ย้ายการเริ่มต้นของงานตามสัดส่วน เว้นแต่โครงการจะถูกแปลง

## <a name="frequently-asked-questions"></a>คำถามที่ถามบ่อย

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>อะไรคือความแตกต่างระหว่างโครงการที่แปลงแล้วและโครงการใหม่ที่สร้างขึ้นหลังจากการอัปเกรดเสร็จสิ้น

สำหรับโครงการที่แปลงหลังจากอัปเกรดสภาพแวดล้อมแล้ว แฟล็กจะถูกตั้งค่าที่สั่งให้กำหนดการตามเฉพาะปฏิทินโครงการเท่านั้น ลักษณะการทำงานนี้ตรงกับลักษณะการทำงานใน Project Service Automation อย่างไรก็ตาม ระบบจะไม่ตั้งค่าสถานะสำหรับโครงการใหม่ที่สร้างขึ้นหลังจากการอัปเกรด ดังนั้น กำหนดการจะพิจารณาชั่วโมงการทำงานของทรัพยากรเมื่อมีการมอบหมายงาน

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>ฉันควรทำอย่างไรหากไม่สามารถแปลงโครงการของฉันได้

หากโครงการของคุณไม่สามารถแปลงได้ ขั้นตอนแรกคือการตรวจทานบันทึกข้อผิดพลาดเพื่อระบุปัญหาทั่วไปที่เกี่ยวข้องกับ WBS ของคุณ หากบันทึกไม่ได้ระบุข้อผิดพลาดเฉพาะที่คุณสามารถดำเนินการได้ โปรดติดต่อฝ่ายสนับสนุนลูกค้าเพื่อให้กรณีของคุณได้รับการตรวจสอบเพิ่มเติม

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>มีการจัดการระยะเวลาที่ปิดดำเนินการใน Project for the Web อย่างไร

Project for the Web ไม่ทำตามระยะเวลาที่ปิดดำเนินการที่องค์กรกำหนดไว้ที่ระดับองค์กร อย่างไรก็ตาม จะทำตามวันหยุดประเภทอื่นๆ ที่กำหนดไว้ในแม่แบบชั่วโมงทำงานที่กำหนด

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Project for the Web มีข้อจำกัดอะไร

ดูที่ [สร้างโครงสร้างการแบ่งงาน: ข้อจำกัดของโครงการ](/project-management/create-wbs#project-limitations.md)

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>ฉันสามารถคาดหวังการเปลี่ยนแปลงในการประมาณการต้นทุนและการขายของฉันได้หรือไม่

ในกรณีที่ไม่ค่อยเกิดขึ้นซึ่งมีการคำนวณโครงร่างการกำหนดทรัพยากรใหม่ หรืออยู่ในขอบเขตวันที่ที่แตกต่างจากโครงการต้นทาง คุณอาจเห็นความแตกต่างในการประเมินยอดขายและต้นทุน ในกระบวนการอัปเกรด ลูกค้าจะต้องทดสอบชุดตัวอย่างที่เป็นตัวแทนของโครงการ เพื่อให้สามารถเข้าใจการเปลี่ยนแปลงกำหนดการที่อาจเกิดขึ้นได้