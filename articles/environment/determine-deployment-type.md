---
title: กำหนดชนิดการปรับใช้งานของคุณ
description: หัวข้อนี้ให้ข้อมูลที่จะช่วยคุณกำหนดชนิดการปรับใช้งานที่ถูกต้องของ Project Operations สำหรับบริษัทของคุณ
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085936"
---
# <a name="determine-your-deployment-type"></a>กำหนดชนิดการปรับใช้งานของคุณ

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

> [!IMPORTANT]
> หลังจากที่คุณซื้อสิทธิ์การใช้งานแล้ว ให้เริ่มที่นี่เพื่อกำหนดรูปแบบการปรับใช้งานที่ดีที่สุดของ Dynamics 365 Project Operations โดยใช้ [ขั้นตอนการติดตั้งที่แนะนำ](https://aka.ms/provisionprojectoperations)
> หลังจากที่คุณเสร็จสิ้นขั้นตอนการติดตั้งที่แนะนำแล้ว ระบบจะนำคุณไปยังพอร์ทัลการจัดการที่ถูกต้องเพื่อทำการติดตั้งของคุณให้เสร็จสมบูรณ์ ดูรายละเอียดการปรับใช้งานเพื่อทำการติดตั้งให้เสร็จสมบูรณ์


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>ลูกค้าปัจจุบันของ Dynamics ที่ใช้ Dynamics 365 Project Service Automation
Project Operations ประกอบด้วยความสามารถต่างๆ ที่มาพร้อมกับ Project Service Automation พาธสำหรับการปรับรุ่นจะเผยแพร่ให้กับลูกค้าเหล่านี้ในอนาคต

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>ลูกค้าปัจจุบันของ Dynamics 365 Finance ที่ใช้การจัดการและการบัญชีโครงการ 

ลูกค้าปัจจุบันของ Finance ที่ใช้ฟังก์ชันการจัดการและการบัญชีโครงการสามารถใช้รายการนี้ต่อไปได้ตามที่เป็นอยู่ ดูที่ [Project Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ใบสั่งผลิต](#pma)


## <a name="deployment-types"></a>ชนิดการปรับใช้งาน
Project Operations รองรับตัวเลือกการปรับใช้งานที่หลากหลายเพื่อให้ตรงกับความต้องการของคุณ ไม่ว่าคุณจะเป็นลูกค้า Dynamics 365 รายใหม่หรือปัจจุบัน Project Operations สามารถรองรับความต้องการของคุณได้

[แบบสอบถามการปรับใช้งาน](https://aka.ms/provisionprojectoperations) ของเราจะช่วยให้คุณกำหนดการปรับใช้งานที่เหมาะสม ผลลัพธ์ดังกล่าวจะนำคุณไปสู่ชนิดการปรับใช้งานอย่างหนึ่งอย่างใดต่อไปนี้:

- [การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว](#lite)
- [Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง](#integrated)
- [Project Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ใบสั่งผลิต](#pma)

Project Operations รองรับสถานการณ์วัสดุที่เก็บในคลัง/ใบสั่งผลิตและสถานการณ์ตามวัสดุที่ไม่ได้เก็บในคลัง/ทรัพยากรบนสภาพแวดล้อมเดียวกันผ่านการกำหนดค่าระดับนิติบุคคล ตัวอย่างเช่น Contoso สามารถใช้ความสามารถในการสั่งซื้อสต็อก/ใบสั่งผลิตในโรงงานผลิตในสหรัฐอเมริกา (นิติบุคคล = Contoso Manufacturing United States) Contoso สามารถใช้ความสามารถที่ไม่เก็บสต็อก/ตามทรัพยากรในสถานที่ให้บริการ Contoso Robotics Arms ในสหราชอาณาจักร (นิติบุคคล = Contoso Robotics สหราชอาณาจักร)

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>การปรับใช้งานอย่างง่าย - จัดการกับการออกใบแจ้งหนี้ชั่วคราว

การปรับใช้งานรุ่นใช้งานง่ายประกอบด้วยความสามารถดังต่อไปนี้:

- การวางแผนโครงการโดยใช้ Microsoft Project สำหรับเว็บ
- การกำหนดราคาแบบหลายมิติ
- การจัดการทรัพยากรแบบรวม
- การติดตามเวลา
- ค่าใช้จ่ายเบื้องต้น
- ข้อเสนอใบแจ้งหนี้

#### <a name="deployment-steps"></a>ขั้นตอนการปรับใช้งาน
กำหนดรูปแบบการปรับใช้งานที่ดีที่สุดของ Project Operations โดยใช้ [แบบสอบถามการปรับใช้งาน](https://aka.ms/provisionprojectoperations)

สำหรับการปรับใช้งานนี้ โปรดดู [ลงทะเบียนสมัครใช้งานพรีวิว](lite-preview-subscription-sign-up.md) และ [การจัดเตรียมสภาพแวดล้อมใหม่](lite-deployment.md) 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง
Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่เก็บในคลังประกอบด้วยความสามารถต่อไปนี้
  
- การวางแผนโครงการโดยใช้ Microsoft Project สำหรับเว็บ
- การกำหนดราคาแบบหลายมิติ
- การจัดการทรัพยากรแบบรวม
- การติดตามเวลา
- ค่าใช้จ่ายเบื้องต้น
- ค่าใช้จ่ายเต็ม
- OCR ใบรับสินค้า
- การออกใบแจ้งหนี้ทั้งหมด
- การรับรู้รายได้

#### <a name="deployment-steps"></a>ขั้นตอนการปรับใช้งาน
กำหนดรูปแบบการปรับใช้งานที่ดีที่สุดของ Project Operations โดยใช้ [แบบสอบถามการปรับใช้งาน](https://aka.ms/provisionprojectoperations)

สำหรับการปรับใช้งานนี้ โปรดดู [ลงทะเบียนสมัครใช้งานพรีวิว](resource-sign-up-preview-subscription.md) และ [การจัดเตรียมสภาพแวดล้อมใหม่](resource-provision-new-environment.md) 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ใบสั่งผลิต

- การวางแผนโครงการโดยใช้ WBS
- การจัดการทรัพยากร
- การติดตามเวลา
- ค่าใช้จ่ายเต็ม
- OCR ใบรับสินค้า
- การออกใบแจ้งหนี้ทั้งหมด
- การรับรู้รายได้
- ใบสั่งผลิต
- การสนับสนุนวัสดุ

#### <a name="deployment-steps"></a>ขั้นตอนการปรับใช้งาน
กำหนดรูปแบบการปรับใช้งานที่ดีที่สุดของ Project Operations โดยใช้ [แบบสอบถามการปรับใช้งาน](https://aka.ms/provisionprojectoperations)

สำหรับการปรับใช้งานนี้ โปรดดู [ลงทะเบียนสมัครใช้งานพรีวิว](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) และ [การจัดเตรียมสภาพแวดล้อมใหม่](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json) 

