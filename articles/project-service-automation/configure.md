---
title: การกำหนดค่า Project Service Automation
description: ขั้นตอนสำหรับการตั้งค่าคอนฟิก Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756409"
---
# <a name="configure-project-service"></a>ตั้งค่าคอนฟิก Project Service

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

ก่อนที่คุณจะสามารถใช้ความสามารถอัตโนมัติของ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ใน [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] เพื่อจัดการบัญชี โครงการ และทรัพยากรของคุณ คุณจำเป็นต้องทำขั้นตอนการกำหนดค่าบางอย่างให้เสร็จสมบูรณ์ เพื่อให้แน่ใจว่าโซลูชัน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ตรงกับความต้องการขององค์กรของคุณ ขั้นตอนเหล่านี้รวมถึง:  
  
-   [ตั้งค่าหน่วยเวลา](../project-service/set-up-time-units.md) การกำหนดค่าหน่วยเวลาในแค็ตตาล็อกผลิตภัณฑ์ที่คุณจะใช้เป็นฐานสำหรับการจัดกำหนดการและการเรียกเก็บเงินโครงการของคุณ  
  
-   [ตั้งค่าสกุลเงินและอัตราแลกเปลี่ยน](../project-service/set-up-currencies-exchange-rates.md) ตั้งค่าสกุลเงินที่จะใช้สำหรับโครงการของคุณ  
  
-   [สร้างหน่วยองค์กร](../project-service/create-organizational-units.md) ตั้งค่ากลุ่มที่บริษัทของคุณใช้เพื่อแบ่งธุรกิจ ไม่ว่าจะโดยภูมิศาสตร์ ฟังก์ชันธุรกิจ หรือฝ่ายตรรกะอื่นๆ  
  
-   [ตั้งค่าความถี่ของใบแจ้งหนี้](../project-service/set-up-invoice-frequencies.md) ตั้งค่าระยะเวลาที่คุณต้องการใช้สำหรับการเรียกเก็บเงินไคลเอ็นต์ของคุณ  
  
-   [กำหนดค่าประเภทธุรกรรม](../project-service/configure-transaction-categories.md) ตั้งค่าประเภทธุรกรรมเพื่อที่ปรึกษาของคุณจะสามารถเรียกเก็บค่าธรรมเนียมที่สามารถเรียกเก็บเงินได้และค่าใช้จ่ายที่ยังไม่ได้เรียกเก็บ  
  
-   [กำหนดค่าประเภทค่าใช้จ่าย](../project-service/configure-expense-categories.md) ตั้งค่าประเภทที่ปรึกษาของคุณจะสามารถเรียกเก็บค่าธรรมเนียมที่สามารถเรียกเก็บเงินได้และค่าใช้จ่ายที่ยังไม่ได้เรียกเก็บ  
  
-   [การสร้างสินค้าแค็ตตาล็อกผลิตภัณฑ์](../project-service/create-product-catalog-items.md) เพิ่มผลิตภัณฑ์ที่คุณขาย เช่น สิทธิ์การใช้งานซอฟต์แวร์ ไปยังแค็ตตาล็อกผลิตภัณฑ์  
  
-   [สร้างราคาตลาด](../project-service/create-price-list.md) กำหนดค่ารายการราคาที่แตกต่างกัน ขึ้นอยู่กับจำนวนที่คุณต้องการเรียกเก็บจากไคลเอนต์ของคุณสำหรับแต่ละบทบาทโครงการที่จำเป็นของพวกเขา  
  
-   [ตั้งค่าทรัพยากร](../project-service/set-up-resources.md) เพิ่มทักษะ ความชำนาญ บทบาทของทรัพยากร และข้อมูลทรัพยากรอื่นๆ ที่คุณต้องมีสำหรับโครงการของคุณ  
  
### <a name="see-also"></a>ดูเพิ่มเติม  
 [ภาพรวมของ Project Service Automation](../project-service/overview.md)   
 [การกำหนดค่า Project Service Automation](../project-service/configure.md)   
 [คำแนะนำผู้จัดการลูกค้าองค์กร](../project-service/account-manager-guide.md)   
 [คำแนะนำของผู้จัดการโครงการ](../project-service/project-manager-guide.md)   
 [คำแนะนำของผู้จัดการทรัพยากร](../project-service/resource-manager-guide.md)   
 [เวลา ค่าใช้จ่าย และคำแนะนำในการทำงานร่วมกัน](../project-service/time-expense-collaboration-guide.md)
