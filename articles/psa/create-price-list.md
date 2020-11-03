---
title: สร้างราคาตลาด
description: วิธีการสร้างราคาตลาดใน Project Service
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bf75286fd1837e27a9b6053ccb21b60771ee197d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085968"
---
# <a name="create-a-price-list-project-service"></a>สร้างราคาตลาด (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

ราคาตลาดกำหนดแม่แบบที่ผู้จัดการฝ่ายบัญชีของคุณสามารถใช้สำหรับการสร้างใบเสนอราคาและโครงการ และสำหรับเชื่อมต่อกับต้นทุนของโครงการ ราคาตลาดกำหนดรายการสินค้าของบทบาทและค่าใช้จ่าย และราคาที่คุณจะคิดค่าธรรมเนียมสำหรับแต่ละรายการ คุณสามารถสร้างราคาตลาดมากมาย เพื่อให้คุณสามารถรักษาโครงสร้างราคาแบบแยกสำหรับภูมิภาคต่างๆ ที่คุณขายผลิตภัณฑ์ในช่องทางการขายต่างๆ ได้ เป็นความคิดที่ดีในการสร้างราคาตลาดอย่างน้อยหนึ่งราคาสำหรับทุกสกุลเงินที่คุณวางแผนที่จะเรียกเก็บเงินจากลูกค้าของคุณ  
  
เมื่อต้องการสร้างการประมาณการด้านการเงินสำหรับงานที่จะส่ง ตรวจสอบให้แน่ใจว่าทุกโครงการมีต้นทุนสำรองและราคาตลาดขาย ตั้งค่าทุนเริ่มต้นและรายการราคาขายที่ใช้กับโครงการทั้งหมดที่สร้างขึ้นในองค์กรของคุณ  
  
ราคาตลาดขึ้นอยู่กับบทบาทและประเภทค่าใช้จ่าย ดังนั้น ก่อนที่คุณสร้างราคาตลาด ทำให้แน่ใจว่าคุณได้กำหนดค่าบทบาทและประเภทของค่าใช้จ่ายที่คุณต้องการใช้ในขณะที่สร้างราคาตลาดแล้ว  
  
1.  ไปที่ **Project Service > ราคาตลาด**  
  
2.  คลิก **สร้าง**  
  
3.  ใน **บริบท** เลือกว่าราคาตลาดนี้สำหรับ **ต้นทุน** , **ซื้อ** หรือ **ขาย**  
  
4.  ใน **ชื่อ** ป้อนชื่อสำหรับราคาตลาด  
  
5.  ใน **สกุลเงิน** เลือกสกุลเงินที่คุณกำลังจะใช้สำหรับการเรียกเก็บเงิน หรือการคำนวณต้นทุน  
  
6.  ใน **หน่วยเวลา** ระบุรอบระยะเวลาที่มีใช้ราคา เช่นวันหรือชั่วโมง  
  
7.  กรอกข้อมูล **วันเริ่ม** , **วันสิ้นสุด** และ **คำอธิบาย** ตามความจำเป็น  
  
8.  คลิก **บันทึก** เพื่อสร้างเรกคอร์ดเพื่อที่คุณจะสามารถทำการแก้ไขตอไปได้  
  
9. เมื่อต้องการเพิ่มราคาตามบทบาทในราคาตลาด คลิก **+**  ภายใต้ **ราคาตามบทบาท**  
  
10. บนบานหน้าต่าง **ราคาตามบทบาท** เติมรายละเอียด แล้วคลิก **บันทึก**. การเพิ่มราคาตามบทบาทตามความจำเป็นต่อไป เมื่อคุณทำเสร็จแล้ว คลิก **บันทึก** ที่มุมล่างขวาของหน้าจอ  
  
11. เมื่อต้องการเพิ่มราคาประเภทค่าใช้จ่ายไปยังราคาตลาด คลิก **+** ภายใต้ **ราคาตามประเภท**  
  
12. บนบานหน้าต่าง **ราคาตามประเภทของธุรกรรม** เติมรายละเอียด แล้วคลิก **บันทึก**. การเพิ่มราคาตามประเภทตามความจำเป็นต่อไป เมื่อคุณทำเสร็จแล้ว คลิก **บันทึก** ที่มุมล่างขวาของหน้าจอ  
  
13. เมื่อต้องการเพิ่มรายการในรายการราคาลงในราคาตลาด คลิก **+** ภายใต้ **รายการในรายการราคา**  
  
14. บนบานหน้าต่าง **รายการในรายการราคา** เติมรายละเอียด แล้วคลิก **บันทึก**. การเพิ่มรายการในรายการราคาตามความจำเป็นต่อไป เมื่อคุณทำเสร็จแล้ว คลิก **บันทึก** ที่มุมล่างขวาของหน้าจอ  
  
15. เมื่อต้องการเพิ่มความสัมพันธ์ของอาณาเขตในราคาตลาด คลิก **+** ภายใต้ **ความสัมพันธ์ของอาณาเขต**  
  
16. บนหน้าต่าง **การเชื่อมต่อใหม่** เติมรายละเอียด แล้วคลิก **บันทึก**. ทำการเพิ่มความสัมพันธ์ของอาณาเขตตามความจำเป็น เมื่อคุณทำเสร็จแล้ว คลิก **บันทึก** ที่มุมล่างขวาของหน้าจอ  
  
### <a name="see-also"></a>ดูเพิ่มเติม  
 [การตั้งค่า Project Service Automation](../psa/configure.md)