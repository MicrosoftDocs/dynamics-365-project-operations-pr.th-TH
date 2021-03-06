---
title: เบี้ยเลี้ยง
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับกฎค่าเบี้ยเลี้ยงต่อวันที่ใช้ในการจัดการค่าใช้จ่าย
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908674"
---
# <a name="per-diems"></a>เบี้ยเลี้ยง

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_


ค่าเบี้ยเลี้ยงต่อวันคือเบี้ยเลี้ยงที่จ่ายให้กับผู้ปฏิบัติงานที่กำลังเดินทางไปทำงาน ในการจัดการค่าใช้จ่าย คุณสามารถสร้างกฎค่าเบี้ยเลี้ยงต่อวันสำหรับสถานการณ์การเดินทางต่างๆ ค่าเบี้ยเลี้ยงต่อวันอาจขึ้นอยู่กับช่วงเวลาของปี สถานที่เดินทาง หรือทั้งสองอย่าง เมื่อคุณสร้างกฎค่าเบี้ยเลี้ยงต่อวัน คุณสามารถระบุว่าเปอร์เซ็นต์ของอัตราค่าเบี้ยเลี้ยงต่อวันจะถูกระงับหากผู้ปฏิบัติงานได้รับอาหารหรือบริการฟรี คุณยังสามารถกำหนดจำนวนชั่วโมงขั้นต่ำและสูงสุดที่อัตราค่าเบี้ยเลี้ยงต่อวันใช้กับการเดินทางของผู้ปฏิบัติงานได้

## <a name="configuration"></a>การกำหนดค่า 

1. หากต้องการเพิ่มสถานที่สำหรับค่าเบี้ยเลี้ยงต่อวัน ให้ไปที่ **ตั้งค่า** > **การคำนวณและรหัส** > **สถานที่สำหรับค่าเบี้ยเลี้ยงต่อวัน**
2. สำหรับแต่ละสถานที่ที่เพิ่มไว้ข้างต้น ให้เลือกอัตราค่าเบี้ยเลี้ยงต่อวันและสกุลเงินที่ใช้ได้ระหว่างวันที่เริ่มต้นและวันที่สิ้นสุดที่เฉพาะเจาะจงสำหรับโรงแรม มื้ออาหาร และค่าใช้จ่ายอื่นๆ อัตราค่าเบี้ยเลี้ยงต่อวันและสกุลเงินได้รับการกำหนดค่าภายใต้ **ตั้งค่า** > **การคำนวณและรหัส** > **ค่าเบี้ยเลี้ยงต่อวัน**
3. บนเพจ **สถานที่สำหรับค่าเบี้ยเลี้ยงต่อวัน** กำหนดค่าระดับอัตราค่าเบี้ยเลี้ยงต่อวัน ระดับอัตราค่าเบี้ยเลี้ยงต่อวันช่วยให้คุณสามารถกำหนดเปอร์เซ็นต์การแบ่งค่าเบี้ยเลี้ยงรายวันสำหรับโรงแรม มื้ออาหาร และค่าใช้จ่ายอื่นๆ 
4. หากต้องการระบุการลดเปอร์เซ็นต์ค่าอาหารสำหรับมื้อเช้า กลางวัน หรือเย็น ให้ปรับปรุงฟิลด์ในเพจ **พารามิเตอร์การจัดการค่าใช้จ่าย** บนแท็บ **ค่าเบี้ยเลี้ยงต่อวัน** 
    
## <a name="submit-expenses-using-per-diem"></a>ส่งค่าใช้จ่ายโดยใช้ค่าเบี้ยเลี้ยงต่อวัน
หากต้องการส่งค่าใช้จ่ายที่ใช้ค่าเบี้ยเลี้ยงต่อวัน ให้ใช้ประเภทค่าใช้จ่าย **ค่าเบี้ยเลี้ยงต่อวัน** เมื่อคุณสร้างรายงานค่าใช้จ่าย ป้อน **ค่าเบี้ยเลี้ยงต่อวันจากวันที่**, **ค่าเบี้ยเลี้ยงต่อวันถึงวันที่** และ **สถานที่สำหรับค่าเบี้ยเลี้ยงต่อวัน** จำนวนเงินจะคำนวณตามอัตราค่าเบี้ยเลี้ยงต่อวันสำหรับสถานที่ที่เลือกและการลดมื้ออาหารจะคำนวณตามระดับอัตราค่าเบี้ยเลี้ยงต่อวัน
