---
title: ประมาณการยอดขายและต้นทุนของโครงการเมื่อทรัพยากรที่จองได้มีหลายบทบาทในโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีที่สามารถใช้มิติข้อมูลการกำหนดราคาเพื่อสนับสนุนการกำหนดราคาและการคิดต้นทุนสำหรับทรัพยากรที่มีหลายบทบาทในโครงการ
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085984"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a>ประมาณการยอดขายและต้นทุนของโครงการเมื่อทรัพยากรที่จองได้มีหลายบทบาทในโครงการ 

บริษัทตามโครงการมักมีความต้องการทรัพยากรเดียวเพื่อทำหน้าที่หลายบทบาทในโครงการ แต่ละบทบาทเหล่านี้อาจมีราคาและต้นทุนแตกต่างกัน ซึ่งหมายความว่าเวลาของทรัพยากรเดียวกันในโครงการอาจได้รับการประมาณทางการเงินที่แตกต่างกัน ขึ้นอยู่กับอัตราในการเรียกเก็บเงินและต้นทุนสำหรับแต่ละบทบาท Project Service Automation อนุญาตให้ตั้งค่าในเรกคอร์ดสมาชิกทีมสำหรับทรัพยากรที่ระบุชื่อและอนุญาตให้มีการแทนที่ที่แตกต่างกันสำหรับแต่ละงานที่สมาชิกทีมได้รับมอบหมาย

ตัวอย่างต่อไปนี้อธิบายว่าการแทนที่ค่านี้อย่างง่ายทำให้ทรัพยากรมีหลายบทบาทในโครงการที่มีอัตราต้นทุนและค่าบริการที่แตกต่างกันได้อย่างไร

## <a name="create-tasks"></a>สร้างงาน
สร้างงานโครงการสองงานครั้งละ 40 ชั่วโมง คือ งาน A และงาน B เลือกงาน A เป็นงานก่อนหน้างาน B

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>ตั้งค่าบทบาทและหน่วยองค์กรสำหรับสมาชิกทีมโครงการทั่วไป

1. บนเพจ **กำหนดการ** เลือกแถว **งาน** สำหรับงาน A 
2. ในฟิลด์ **ทรัพยากร** ให้เลือก **สร้าง** ในรายการแบบหล่นลง
3. บนเพจ **การสร้างด่วนของสมาชิกทีม** ให้ระบุแอตทริบิวต์ของสมาชิกทีมทั่วไปที่สามารถทำงานนี้ได้
4. เลือกบทบาทและหน่วยองค์กรที่เหมาะสม จากนั้นเลือก **บันทึกและปิด** มีการสร้างสมาชิกทีมทั่วไปและกำหนดให้กับงานนี้ 

ทำซ้ำขั้นตอนเหล่านี้สำหรับงาน B และตรวจสอบให้แน่ใจว่าบทบาทและหน่วยองค์กรในสมาชิกทีมทั่วไปที่สร้างขึ้นสำหรับงาน B นั้นแตกต่างจากงาน A 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>ตั้งค่าบทบาทและหน่วยองค์กรสำหรับงานโครงการ

1. หลังจากที่คุณสร้างงาน A ให้เลือกงาน จากนั้นเลือก **แก้ไขงาน**
2. บนเพจ **รายละเอียดงาน** ให้ค้นหาฟิลด์ **บทบาท** และ **หน่วยองค์กร** เพิ่มค่าที่จำเป็นสำหรับทรัพยากรที่จะทำงานนี้ 

  > [!NOTE]
  > ถ้าคุณกำลังทำสถานการณ์นี้ให้เสร็จสมบูรณ์โดยใช้ข้อมูลสาธิตของ Project Service Automation ให้เลือก **หัวหน้าที่ปรึกษา** สำหรับบทบาท และ **Fabrikam US** เป็นหน่วยองค์กร

3. เลือกงาน B จากนั้นเลือก **แก้ไขงาน**
4. บนเพจ **รายละเอียดงาน** ให้ค้นหาฟิลด์ **บทบาท** และ **หน่วยองค์กร** เพิ่มค่าที่จำเป็นสำหรับทรัพยากรที่จะทำงานนี้ ตรวจสอบให้แน่ใจว่าค่าในฟิลด์ **บทบาท** และ **หน่วยองค์กร** สำหรับงาน B แตกต่างจากฟิลด์สำหรับงาน A 

  > [!NOTE]
  > ถ้าคุณกำลังทำสถานการณ์นี้ให้เสร็จสมบูรณ์โดยใช้ข้อมูลสาธิตของ Project Service Automation ให้เลือก **ช่างเทคนิคเครือข่าย** สำหรับบทบาท และ **Fabrikam US** เป็นหน่วยองค์กร

5. บันทึกและปิดเพจ **รายละเอียดงาน** 

## <a name="team-member-and-estimates-behaviour"></a>ลักษณะการทำงานของสมาชิกทีมและประมาณการ 

1. บนเพจ **รายละเอียดงาน** บน **สมาชิกทีม** เลือกสมาชิกทีมทั่วไปสองคน จากนั้นเลือก **สร้างความต้องการ** การดำเนินการนี้จะสร้างความต้องการทรัพยากร 
2. เลือกแถวสมาชิกทีมสำหรับ **หัวหน้าที่ปรึกษา** จากนั้นเลือก **จอง** ตารางกำหนดการจะเปิดขึ้นและจองทรัพยากรตามความต้องการนั้น
3. เลือกแถวสมาชิกทีมสำหรับ **ช่างเทคนิคเครือข่าย** จากนั้นเลือก **จอง** ตารางกำหนดการจะเปิดขึ้นและจองทรัพยากรเดียวกันสำหรับความต้องการนั้น

### <a name="team-member-grid"></a>ตารางสมาชิกทีม 
บนตาราง **สมาชิกทีม** โปรดสังเกตว่าเรกคอร์ดสมาชิกทีมทั่วไปสองรายการถูกลบและแทนที่ด้วยทรัพยากรหนึ่งรายการ มีชุดค่าหนึ่งชุดสำหรับทรัพยากรที่แสดงชุดค่าเริ่มต้นสำหรับ **บทบาท** และ **หน่วยองค์กร**
เมื่อคุณขยายแถวของเรกคอร์ดสมาชิกทีม คุณจะเห็นการมอบหมายงานที่แตกต่างกันในเรกคอร์ดสมาชิกทีมสำหรับทั้งสองงานนั้น แถวการมอบหมายแต่ละแถวมีค่าเฉพาะงานสำหรับ **บทบาท** และ **หน่วยองค์กร** 

### <a name="estimates-grid"></a>ตารางประมาณการ 
เมื่อคุณไปที่ตาราง **ประมาณการ** คุณจะสังเกตเห็นว่าการมอบหมายทั้งสองงานสำหรับทรัพยากรเดียวกันมีราคาต่างกัน
การมอบหมายงานสำหรับทรัพยากรในงาน A มีการกำหนดราคาโดยใช้ค่าแอตทริบิวต์ **บทบาท** ของ **หัวหน้าที่ปรึกษา** การมอบหมายงานสำหรับทรัพยากรเดียวกันในงาน B มีการกำหนดราคาโดยใช้ค่าแอตทริบิวต์ **บทบาท** ของ **ช่างเทคนิคเครือข่าย**




