---
title: การกำหนดค่า Project Service Automation
description: ขั้นตอนสำหรับการตั้งค่าคอนฟิก Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: ec5381f91b1fe5198bd93ac8d6015b1fea38738d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146956"
---
# <a name="configure-project-service"></a>ตั้งค่าคอนฟิก Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

ก่อนที่คุณจะสามารถใช้ความสามารถอัตโนมัติของ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ใน [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] เพื่อจัดการบัญชี โครงการ และทรัพยากรของคุณ คุณจำเป็นต้องทำขั้นตอนการกำหนดค่าบางอย่างให้เสร็จสมบูรณ์ เพื่อให้แน่ใจว่าโซลูชัน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ตรงกับความต้องการขององค์กรของคุณ ขั้นตอนเหล่านี้รวมถึง:  
  
-   [ตั้งค่าหน่วยเวลา](../psa/set-up-time-units.md) การกำหนดค่าหน่วยเวลาในแค็ตตาล็อกผลิตภัณฑ์ที่คุณจะใช้เป็นฐานสำหรับการจัดกำหนดการและการเรียกเก็บเงินโครงการของคุณ  
  
-   [ตั้งค่าสกุลเงินและอัตราแลกเปลี่ยน](../psa/set-up-currencies-exchange-rates.md) ตั้งค่าสกุลเงินที่จะใช้สำหรับโครงการของคุณ  
  
-   [สร้างหน่วยองค์กร](../psa/create-organizational-units.md) ตั้งค่ากลุ่มที่บริษัทของคุณใช้เพื่อแบ่งธุรกิจ ไม่ว่าจะโดยภูมิศาสตร์ ฟังก์ชันธุรกิจ หรือฝ่ายตรรกะอื่นๆ  
  
-   [ตั้งค่าความถี่ของใบแจ้งหนี้](../psa/set-up-invoice-frequencies.md) ตั้งค่าระยะเวลาที่คุณต้องการใช้สำหรับการเรียกเก็บเงินไคลเอ็นต์ของคุณ  
  
-   [กำหนดค่าประเภทธุรกรรม](../psa/configure-transaction-categories.md) ตั้งค่าประเภทธุรกรรมเพื่อที่ปรึกษาของคุณจะสามารถเรียกเก็บค่าธรรมเนียมที่สามารถเรียกเก็บเงินได้และค่าใช้จ่ายที่ยังไม่ได้เรียกเก็บ  
  
-   [กำหนดค่าประเภทค่าใช้จ่าย](../psa/configure-expense-categories.md) ตั้งค่าประเภทที่ปรึกษาของคุณจะสามารถเรียกเก็บค่าธรรมเนียมที่สามารถเรียกเก็บเงินได้และค่าใช้จ่ายที่ยังไม่ได้เรียกเก็บ  
  
-   [การสร้างสินค้าแค็ตตาล็อกผลิตภัณฑ์](../psa/create-product-catalog-items.md) เพิ่มผลิตภัณฑ์ที่คุณขาย เช่น สิทธิ์การใช้งานซอฟต์แวร์ ไปยังแค็ตตาล็อกผลิตภัณฑ์  
  
-   [สร้างราคาตลาด](../psa/create-price-list.md) กำหนดค่ารายการราคาที่แตกต่างกัน ขึ้นอยู่กับจำนวนที่คุณต้องการเรียกเก็บจากไคลเอนต์ของคุณสำหรับแต่ละบทบาทโครงการที่จำเป็นของพวกเขา  
  
-   [ตั้งค่าทรัพยากร](../psa/set-up-resources.md) เพิ่มทักษะ ความชำนาญ บทบาทของทรัพยากร และข้อมูลทรัพยากรอื่นๆ ที่คุณต้องมีสำหรับโครงการของคุณ  
  
### <a name="see-also"></a>ดูเพิ่มเติม  
 [ภาพรวมของ Project Service Automation](../psa/overview.md)   
 [การกำหนดค่า Project Service Automation](../psa/configure.md)   
 [คำแนะนำผู้จัดการลูกค้าองค์กร](../psa/account-manager-guide.md)   
 [คำแนะนำของผู้จัดการโครงการ](../psa/project-manager-guide.md)   
 [คำแนะนำของผู้จัดการทรัพยากร](../psa/resource-manager-guide.md)   
 [เวลา ค่าใช้จ่าย และคำแนะนำในการทำงานร่วมกัน](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]