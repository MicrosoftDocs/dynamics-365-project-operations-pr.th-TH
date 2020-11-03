---
title: ทดลองกับข้อมูลสาธิต
description: วิธีการดาวน์โหลด และทดลองกับข้อมูลสาธิตสำหรับ Project Service Automation
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
ms.openlocfilehash: d0bc6d171f2f3080b7b1c34222de49e93415a139
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086011"
---
# <a name="experiment-with-demo-data-project-service"></a>ทดลองกับข้อมูลสาธิต (Project Service)

เมื่อต้องการทำความคุ้นเคยกับ Dynamics 365 Project Service Automation มีประโยชน์ที่จะมีสภาพแวดล้อมที่กำหนดไว้ล่วงหน้าสำหรับการสำรวจ สำหรับวัตถุประสงค์นี้ เราได้สร้างแพ็คเกจการติดตั้งข้อมูลตัวอย่างแยกต่างหาก (ภาษาอังกฤษเท่านั้นในขณะนี้) ที่ทำให้ง่ายต่อการเรียนรู้เกี่ยวกับวิธีการแก้ไขปัญหาเหล่านี้ 

แพ็คเกจการติดตั้งที่มีอยู่บน [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=859966)  

การเรียกใช้การติดตั้ง Package Deployer จะทำการดำเนินการต่อไปนี้: 
  
-   สร้างหรือตั้งค่าพารามิเตอร์เริ่มต้นที่กระตุ้นพฤติกรรมของ Project Service  
  
-   นำเข้าข้อมูลการตัวอย่าง เช่น ทรัพยากรที่สามารถจองได้ บทบาท การขาย และรายการราคาต้นทุน หน่วยทางองค์กร เรกคอร์ดการประมวลผลการขายที่เกี่ยวข้อง ใบสั่งผลิตและโครงการ    
  
> [!IMPORTANT]
> **ไม่มีวิธีการยกเลิกการติดตั้งข้อมูลสาธิต** ดังนั้น คุณควรใช้แพคเกจนี้ในการสาธิต การประเมิน การฝึก และระบบทดสอบเท่านั้น

สำหรับข้อมูลเพิ่มเติม โปรดดู [blog](https://blogs.msdn.microsoft.com/crm/2017/10/24/microsoft-dynamics-365-for-field-service-and-project-service-automation-sample-data) นี้





  
### <a name="see-also"></a>ดูเพิ่มเติม  
 [คู่มือของผู้ดูแลระบบ](../psa/admin-guide.md)   
 [คำแนะนำผู้จัดการลูกค้าองค์กร](../psa/account-manager-guide.md)   
 [คำแนะนำของผู้จัดการโครงการ](../psa/project-manager-guide.md)   
 [คำแนะนำของผู้จัดการทรัพยากร](../psa/resource-manager-guide.md)   
 [เวลา ค่าใช้จ่าย และคำแนะนำในการทำงานร่วมกัน](../psa/time-expense-collaboration-guide.md)
