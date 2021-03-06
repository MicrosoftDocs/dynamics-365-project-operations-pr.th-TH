---
title: ตั้งค่าประเภทค่าใช้จ่าย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีตั้งค่าประเภทค่าใช้จ่ายและประเภทที่ใช้ร่วมกันสำหรับรายงานค่าใช้จ่าย
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896709"
---
# <a name="set-up-expense-categories"></a>ตั้งค่าประเภทค่าใช้จ่าย

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_

เมื่อพนักงานสร้างรายงานค่าใช้จ่าย ค่าใช้จ่ายแต่ละรายการที่พวกเขาบันทึกจะต้องเชื่อมโยงกับประเภทค่าใช้จ่าย ประเภทค่าใช้จ่ายมาจากประเภทที่ใช้ร่วมกัน ซึ่งสามารถใช้ร่วมกันระหว่างนิติบุคคลในองค์กรของคุณ ขึ้นอยู่กับว่าองค์กรของคุณกำหนดไว้อย่างไร ประเภทค่าใช้จ่ายเหล่านี้ยังสามารถใช้ร่วมกันในพื้นที่อื่นๆ ด้วย ตามข้อกำหนดขององค์กรของคุณและคำแนะนำจากทีมการนำไปใช้งาน คุณต้องกำหนดว่าประเภทที่ใช้ในการจัดการค่าใช้จ่ายจะใช้เฉพาะในการจัดการค่าใช้จ่ายหรือควรใช้ร่วมกันในด้านอื่นๆ ด้วย

> [!NOTE]
> ประเภทเหล่านี้สามารถใช้ร่วมกันระหว่างการจัดการและการบัญชีโครงการ และการจัดการค่าใช้จ่าย หรือระหว่างการจัดการและการบัญชีโครงการและการผลิต อย่างไรก็ตาม ไม่สามารถใช้ร่วมกันระหว่างการจัดการค่าใช้จ่ายและการผลิตได้

ก่อนที่คุณจะเริ่มกระบวนการตั้งค่า คุณต้องตัดสินใจต่อไปนี้สำหรับค่าใช้จ่ายแต่ละประเภท:

- ประเภทค่าใช้จ่ายคืออะไร ตัวอย่างได้แก่ ประเภทสำหรับเที่ยวบิน โรงแรม หรือระยะไมล์
- ประเภทค่าใช้จ่ายสามารถใช้ในการจัดการและการบัญชีโครงการได้หรือไม่ หากสามารถใช้ได้ คุณต้องตัดสินใจเกี่ยวกับเรื่องต่อไปนี้ด้วย

    - บัญชีต้นทุนใดที่จะใช้สำหรับค่าใช้จ่ายต่อไปนี้

        - ต้นทุน
        - การจัดสรรเงินเดือน
        - WIP-มูลค่าต้นทุน
        - ต้นทุน-สินค้า
        - WIP-มูลค่าต้นทุน-สินค้า
        - ขาดทุนสะสม
        - WIP-ขาดทุนสะสม

    - บัญชีรายได้ใดที่จะใช้สำหรับแหล่งรายได้ต่อไปนี้

        - รายได้ที่ออกใบแจ้งหนี้
        - มูลค่าการขายของรายได้ค้างรับ
        - WIP-มูลค่าการขาย
        - รายได้ค้างรับ-การผลิต
        - WIP-การผลิต
        - รายได้ค้างรับ-กำไร
        - WIP-กำไร
        - รายได้ค้างรับ-การสมัครใช้งาน
        - WIP-การสมัครใช้งาน

- ชนิดค่าใช้จ่ายคืออะไร
- วิธีการชำระเงินเริ่มต้นสำหรับประเภทค่าใช้จ่ายคืออะไร
- ค่าใช้จ่ายในประเภทค่าใช้จ่ายต้องแยกรายการหรือไม่
- บัญชีเริ่มต้นหลักสำหรับประเภทค่าใช้จ่ายคืออะไร
- กลุ่มภาษีขายสินค้าเริ่มต้นสำหรับประเภทค่าใช้จ่ายคืออะไร
- สามารถใช้วิธีการชำระเงินเพิ่มเติมสำหรับประเภทค่าใช้จ่ายได้หรือไม่ ถ้าเป็นเช่นนั้น คืออะไรบ้าง
- มีประเภทย่อยในประเภทค่าใช้จ่ายนี้หรือไม่ หากมีประเภทย่อย คุณต้องตัดสินใจเกี่ยวกับเรื่องต่อไปนี้ด้วย

    - ประเภทย่อยใดๆ ไม่รวมอยู่ในการขอคืนภาษีหรือไม่
    - กลุ่มภาษีขายสินค้าของประเภทย่อยคืออะไร
