---
title: การประมาณการทรัพยากร
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการคำนวณประมาณการทรัพยากรใน Project Operations
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127405"
---
# <a name="resource-estimates"></a>การประมาณการทรัพยากร

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

ประมาณการทรัพยากรมาจากกำลังคนตามระยะเวลาที่กำหนดไว้ในโครงสร้างการแบ่งงานพร้อมกับมิติการกำหนดราคาที่เกี่ยวข้อง โดยปกติ การคำนวณคือ **อัตรา/ชม. สำหรับแต่ละบทบาท x ชั่วโมง** กำลังคนตามระยะเวลาสำหรับแต่ละทรัพยากรจะมีการเก็บไว้ในเรกคอร์ดการมอบหมายทรัพยากร การกำหนดราคาจะมีการเก็บไว้ในรายการราคาที่กำหนดไว้ล่วงหน้า การแปลงหน่วยใช้ตามรายการราคาที่เกี่ยวข้อง

![ประมาณการทรัพยากร](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>ราคาต้นทุนและสกุลเงินต้นทุนเริ่มต้น

ราคาต้นทุนเป็นเริ่มต้นจากหน่วยองค์กร

## <a name="default-bill-rate-and-sales-currency"></a>อัตราการเรียกเก็บค่าใช้จ่ายและสกุลเงินการขายเริ่มต้น

ราคาขายจะใช้หนึ่งครั้งต่อข้อตกลง ลำดับชั้นสำหรับรายการราคาขายที่เป็นค่าเริ่มต้นเป็นดังนี้:

1. องค์กร
2. ลูกค้า
3. ใบเสนอราคา/สัญญา


[!INCLUDE[footer-include](../includes/footer-banner.md)]