---
title: กำหนดนโยบายค่าใช้จ่าย
description: คุณสามารถกำหนดนโยบายค่าใช้จ่ายที่ผู้ปฏิบัติงานของคุณต้องปฏิบัติตามเมื่อป้อนและส่งรายงานค่าใช้จ่ายและใบเบิกค่าเดินทาง
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fbab7fd94fa429876216ee82b716da8d847fb01a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896664"
---
# <a name="define-expense-policies"></a>กำหนดนโยบายค่าใช้จ่าย

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

คุณสามารถกำหนดนโยบายที่ผู้ปฏิบัติงานของคุณต้องปฏิบัติตามเมื่อป้อนและส่งรายงานค่าใช้จ่ายและใบเบิกค่าเดินทาง         
การใช้นโยบายค่าใช้จ่ายสามารถช่วยคุณจัดการค่าใช้จ่ายได้อย่างมีประสิทธิภาพ         

ตัวอย่างเช่น คุณสามารถกำหนดนโยบายสำหรับค่าใช้จ่ายของโรงแรมในนิวยอร์กซิตี ซึ่งระบุว่าค่าใช้จ่ายต่อคืนต้องไม่เกิน USD 250       
หากผู้ปฏิบัติงานส่งรายงานค่าใช้จ่ายหรือใบเบิกค่าเดินทางที่มีราคาค่าห้องพักเกินจำนวนนี้ ระบบจะแจ้ง         
ผู้ปฏิบัติงานว่าเกินจำนวนเงินตามนโยบายสำหรับค่าใช้จ่าย คุณสามารถกำหนดค่าข้อความที่ผู้ปฏิบัติงานจะได้รับเมื่อคุณ        
กำหนดนโยบายได้      
        
คุณสามารถกำหนดนโยบายได้สามชนิด:         
        
- **คำเตือน**: อนุญาตให้ผู้ปฏิบัติงานส่งรายงานค่าใช้จ่ายหรือใบเบิกค่าเดินทางได้ แต่จะมีการทำเครื่องหมายค่าใช้จ่ายสำหรับผู้อนุมัติทั้งหมดและ         
  สำหรับการรายงานในภายหลัง        

- **ข้อผิดพลาด**: กำหนดให้ผู้ปฏิบัติงานต้องแก้ไขค่าใช้จ่ายเพื่อให้สอดคล้องกับนโยบายก่อนที่จะส่งรายงานค่าใช้จ่ายหรือใบเบิกค่าเดินทาง        
 
 - **เหตุผล**: กำหนดให้ผู้ปฏิบัติงานหรือผู้จัดการต้องระบุเหตุผลสำหรับค่าใช้จ่ายเกินจำนวนเงินของนโยบายก่อนที่จะส่งรายงานค่าใช้จ่ายหรือใบเบิกค่าเดินทาง        

## <a name="policy-tips"></a>เคล็ดลับเกี่ยวกับนโยบาย
ต่อไปนี้เป็นข้อเสนอแนะสองสามข้อที่จะช่วยคุณในการสร้างนโยบายใหม่สำหรับการจัดการค่าใช้จ่าย: 

- นโยบายเป็นวันที่มีผลบังคับใช้ ซึ่งหมายความว่านโยบายจะไม่มีผลหากสร้างขึ้นด้วยมีวันที่หลังจากวันที่เกิดค่าใช้จ่าย ตัวอย่างเช่น คุณสร้างนโยบายใหม่ในวันนี้เพื่อบังคับใช้ค่าอาหารสูงสุด $50 ค่าใช้จ่ายที่มีอยู่ที่ป้อนเมื่อวานนี้จะไม่นำมาตรวจสอบกับนโยบายนี้
- เมื่อสร้างนโยบายสำหรับประเภทค่าใช้จ่ายที่สามารถแสดงรายการได้ ให้พิจารณาเพิ่มเงื่อนไขสำหรับชนิดรายการค่าใช้จ่าย นโยบายบางอย่าง เช่น การต้องใช้ใบเสร็จรับเงินอาจไม่เหมาะกับรายการที่มีการแสดงรายการ ในสถานการณ์นี้ นโยบายจะนำมาใช้กับรายการส่วนหัวหรือรายการที่ไม่แสดงเป็นรายการเท่านั้น 
- นโยบายการจัดการค่าใช้จ่ายจะมีการประเมินเทียบกับเอนทิตีต้นทางตามค่าเริ่มต้น สำหรับสถานการณ์ระหว่างบริษัท คุณสามารถตั้งค่านโยบายให้ประเมินเทียบกับเอนทิตีปลายทาง (เอนทิตีที่ขอยืม) แทนได้ ในการเรียกใช้นโยบายกับเอนทิตีปลายทาง ให้เปิดคุณลักษณะ **ประเมินนโยบายค่าใช้จ่ายเทียบกับนิติบุคคลที่ขอยืม** ในพื้นที่ทำงาน **การจัดการคุณลักษณะ**

## <a name="when-to-evaluate-policies"></a>เวลาในการประเมินนโยบาย

ในพารามิเตอร์การจัดการค่าใช้จ่าย คุณสามารถเลือกที่จะประเมินนโยบายการจัดการค่าใช้จ่ายเมื่อมีการบันทึกรายการหรือเมื่อมีการส่งรายงานค่าใช้จ่าย หากคุณเลือกที่จะประเมินเมื่อมีการบันทึกรายการ ผู้ใช้จะสามารถมองเห็นได้ก่อนว่าพวกเขาต้องทำอะไรเพื่อทำรายงานค่าใช้จ่ายให้เสร็จสมบูรณ์ทั้งหมดพร้อมกัน หรือคุณสามารถชะลอการประเมินนโยบายและประหยัดเวลาได้โดยการตรวจสอบความถูกต้องในตอนท้าย ระหว่างการส่งไปยังเวิร์กโฟลว์
