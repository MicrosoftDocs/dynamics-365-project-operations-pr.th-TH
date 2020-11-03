---
title: กำหนดค่าการจัดการค่าใช้จ่าย
description: บทความนี้อธิบายถึงข้อควรพิจารณาและการตัดสินใจที่คุณต้องทำในระหว่างกระบวนการวางแผนก่อนที่คุณจะกำหนดค่าการจัดการค่าใช้จ่ายใน Microsoft Dynamics 365 Finance
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2291515cc154fb5b34ca5802135791958bea1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086080"
---
# <a name="configure-expense-management"></a>กำหนดค่าการจัดการค่าใช้จ่าย

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายถึงข้อควรพิจารณาและการตัดสินใจที่คุณต้องทำในระหว่างกระบวนการวางแผนก่อนที่คุณจะกำหนดค่าการจัดการค่าใช้จ่าย ในการจัดการค่าใช้จ่าย คุณสามารถจัดเก็บข้อมูลเกี่ยวกับวิธีการชำระเงิน ใบเบิกค่าเดินทาง รายงานค่าใช้จ่าย นโยบาย และอื่น ๆ

เนื่องจากการตัดสินใจหลายอย่างที่คุณทำเมื่อคุณวางแผนการกำหนดค่าสำหรับการจัดการค่าใช้จ่ายนั้น ขึ้นอยู่กับลำดับชั้นและโครงสร้างทางการเงินขององค์กรของคุณ คุณจึงต้องอ้างถึงเอกสารการวางแผนสำหรับพื้นที่เหล่านั้น

## <a name="intercompany-expenses"></a>ค่าใช้จ่ายระหว่างบริษัท

เมื่อคุณเปิดใช้งานค่าใช้จ่ายระหว่างบริษัท คุณอนุญาตให้นิติบุคคลและพนักงานต้องเสียค่าใช้จ่ายในนามของนิติบุคคลอื่น และเรียกเก็บเงินจากนิติบุคคลของการจ้างงานภายในองค์กรของคุณ ตัวอย่างเช่น พนักงานในนิติบุคคล A ดำเนินโครงการสำหรับนิติบุคคล B และโครงการต้องเสียค่าใช้จ่ายที่เกี่ยวข้องกับการเดินทาง หากเปิดใช้งานค่าใช้จ่ายระหว่างบริษัท พนักงานสามารถยื่นรายงานค่าใช้จ่ายที่จะโพสต์รายการค่าใช้จ่ายไปยังนิติบุคคล B จากนั้นค่าใช้จ่ายจะต้องจ่ายโดยนิติบุคคล A หากองค์กรของคุณไม่ได้มีหลายนิติบุคคล คุณไม่ต้องเปิดใช้งานค่าใช้จ่ายระหว่างบริษัท

**การตัดสินใจ:** คุณต้องการเปิดใช้งานค่าใช้จ่ายระหว่างบริษัทหรือไม่

## <a name="financial-management"></a>การจัดการทางการเงิน

การจัดการค่าใช้จ่ายถูกรวมเข้ากับการจัดการทางการเงินขององค์กรของคุณอย่างแน่นหนา การกำหนดค่าจำนวนมากของคุณสำหรับการจัดการค่าใช้จ่ายจะขึ้นอยู่กับการตัดสินใจที่คุณได้ทำเกี่ยวกับการเงินขององค์กรของคุณ ส่วนต่อไปนี้อธิบายถึงพื้นที่ต่างๆ ที่ต้องมีการวางแผนและการตัดสินใจ โดยพิจารณาจากการตัดสินใจทางการเงินขององค์กรและคำแนะนำจากทีมผู้นำของคุณ

### <a name="per-diems"></a>เบี้ยเลี้ยง

คุณต้องกำหนดค่าเบี้ยเลี้ยงต่อวันของพนักงานที่องค์กรของคุณจัดหาให้ เนื่องจากโดยทั่วไปแล้วค่าเบี้ยเลี้ยงต่อวันจะใช้เพื่อครอบคลุมค่าใช้จ่ายต่างๆ เช่น ค่าอาหาร ค่าที่พัก และค่าใช้จ่ายอื่น ๆ คุณสามารถสร้างกฎสำหรับค่าเบี้ยเลี้ยงต่อวันที่องค์กรของคุณเสนอได้ ค่าเบี้ยเลี้ยงต่อวันอาจขึ้นอยู่กับช่วงเวลาของปี สถานที่เดินทาง หรือทั้งสองอย่าง เมื่อคุณกำหนดกฎค่าเบี้ยเลี้ยงต่อวัน คุณสามารถระบุว่าเปอร์เซ็นต์ของอัตราค่าเบี้ยเลี้ยงต่อวันจะถูกระงับหากผู้ปฏิบัติงานได้รับอาหารหรือบริการฟรี คุณยังสามารถกำหนดระดับอัตราค่าเบี้ยเลี้ยงต่อวันเพื่อกำหนดจำนวนชั่วโมงขั้นต่ำและสูงสุดที่อัตราค่าเบี้ยเลี้ยงต่อวันสามารถใช้กับการเดินทางของผู้ปฏิบัติงานได้

**การตัดสินใจ:**

- กฎค่าเบี้ยเลี้ยงต่อวันเริ่มต้นสำหรับวันแรกและวันสุดท้าย:

    - จำนวนชั่วโมงขั้นต่ำที่พนักงานสามารถอ้างสิทธิ์ได้ในหนึ่งวันและยังคงได้รับค่าเบี้ยเลี้ยงต่อวันคือเท่าใด
    - มีการลดให้การสนับสนุนค่าอาหารสำหรับวันแรกและวันสุดท้ายหรือไม่ ถ้ามีการลดลง เปอร์เซ็นต์ของการลดคือเท่าใด
    - มีการลดให้การสนับสนุนค่าโรงแรมสำหรับวันแรกและวันสุดท้ายหรือไม่ ถ้ามีการลดลง เปอร์เซ็นต์ของการลดคือเท่าใด
    - มีการลดให้การสนับสนุนค่าใช้จ่ายอื่นๆ ที่เกิดขึ้นในวันแรกและวันสุดท้ายหรือไม่ ถ้ามีการลดลง เปอร์เซ็นต์ของการลดคือเท่าใด

- กฎค่าเบี้ยเลี้ยงต่อวันเริ่มต้น:

    - มีการลดเปอร์เซ็นต์ของค่าเบี้ยเลี้ยงต่อวันสำหรับอาหารแต่ละมื้อหรือไม่ถ้าหาก ตัวอย่างเช่นอาหารนั้นฟรี ถ้ามีการลดลง เปอร์เซ็นต์ของการลดสำหรับอาหารแต่ละมื้อคือเท่าใด
    - การลดมื้ออาหารคำนวณต่อวัน ต่อเที่ยว หรือตามจำนวนมื้อต่อวัน
    - จำนวนค่าเบี้ยเลี้ยงต่อวันควรปัดตามปกติหรือปัดขึ้น
    - ค่าเบี้ยเลี้ยงต่อวันคำนวณตามระยะเวลา 24 ชั่วโมง หรือในวันตามปฏิทิน

- กฎค่าเบี้ยเลี้ยงต่อวันที่ขึ้นอยู่กับสถานที่:

    - อัตราค่าเบี้ยเลี้ยงต่อวันแตกต่างกันไปตามสถานที่หรือไม่ รวมสถานที่ใดบ้าง
    - หากอัตราค่าเบี้ยเลี้ยงต่อวันแตกต่างกันไปตามสถานที่ตั้ง สำหรับแต่ละสถานที่ จะมีการระบุจำนวนเปอร์เซ็นต์ใดสำหรับค่าใช้จ่ายประเภทต่อไปนี้:

        - ค่าอาหาร
        - โรงแรม
        - ค่าใช้จ่ายอื่นๆ

### <a name="expense-management-journals-and-accounts"></a>สมุดรายวันและบัญชีการจัดการค่าใช้จ่าย

การจัดการค่าใช้จ่ายต้องการให้คุณใช้สมุดรายวันและบัญชีหลายรายการ ตัวอย่างเช่น คุณต้องตัดสินใจว่าจะใช้บัญชีเดียวกันสำหรับการเบิกเงินสดล่วงหน้าและข้อพิพาทเกี่ยวกับบัตรเครดิตหรือไม่

**การตัดสินใจ:**

- สมุดรายวันบัญชีแยกประเภทใดที่ได้รับการอนุมัติรายงานค่าใช้จ่ายที่โพสต์รายการไป
- บัญชีใดใช้สำหรับการเบิกเงินสดล่วงหน้า
- ควรโพสต์เงินสดล่วงหน้าทันทีหรือไม่?

### <a name="payment-methods"></a>วิธีการชำระเงิน

เมื่อคุณอนุญาตให้พนักงานออกค่าใช้จ่ายในนามของธุรกิจ คุณต้องกำหนดวิธีการชำระเงินที่พนักงานได้รับอนุญาตให้ใช้ ตัวอย่างเช่น คุณอาจอนุญาตให้พนักงานใช้เงินสดหรือบัตรเครดิตขององค์กร คุณอาจอนุญาตให้พนักงานใช้บัตรเครดิตส่วนบุคคล แล้วคืนเงินให้พนักงาน คุณต้องตัดสินใจต่อไปนี้สำหรับวิธีการชำระเงินแต่ละวิธีที่คุณอนุญาต

**การตัดสินใจ:**

- วิธีการชำระเงินใดที่ได้รับอนุญาต
- ใครเป็นเจ้าของค่าใช้จ่ายวิธีการชำระเงิน
- มีชนิดบัญชีออฟเซ็ตหรือไม่ ถ้ามีชนิดบัญชีออฟเซ็ต คืออะไร
- ถ้ามีชนิดบัญชีออฟเซ็ต บัญชีคืออะไร
- หากวิธีการชำระเงินเป็นบัตรเครดิต ควรใช้วิธีการชำระเงินกับธุรกรรมที่นำเข้าเท่านั้นหรือไม่

### <a name="expense-categories-and-shared-categories"></a>ประเภทของค่าใช้จ่ายและประเภทที่ใช้ร่วมกัน

เมื่อพนักงานสร้างรายงานค่าใช้จ่าย ค่าใช้จ่ายแต่ละรายการที่พวกเขาบันทึกจะต้องเชื่อมโยงกับประเภทค่าใช้จ่าย ประเภทค่าใช้จ่ายมาจากประเภทที่ใช้ร่วมกัน ซึ่งสามารถใช้ร่วมกันระหว่างนิติบุคคลในองค์กรของคุณ นอกจากนี้ยังสามารถแชร์หมวดหมู่เหล่านี้ได้ในการจัดการโครงการและการบัญชี ทั้งนี้ขึ้นอยู่กับวิธีการกำหนดขององค์กรของคุณ ตามข้อกำหนดขององค์กรของคุณและคำแนะนำจากทีมการนำไปใช้งาน กำหนดว่าประเภทที่ใช้ในการจัดการค่าใช้จ่ายจะใช้เฉพาะในการจัดการค่าใช้จ่าย หรือว่าพวกเขาควรใช้ร่วมกันระหว่างการจัดการและการบัญชีโครงการ และการจัดการค่าใช้จ่ายด้วย โปรดทราบว่าประเภทเหล่านี้สามารถใช้ร่วมกันระหว่างโครงการและค่าใช้จ่าย หรือโครงการและการผลิต แต่ไม่ใช่ระหว่างค่าใช้จ่ายและการผลิต คุณต้องตัดสินใจต่อไปนี้สำหรับค่าใช้จ่ายแต่ละประเภท

**การตัดสินใจ:**

- ประเภทค่าใช้จ่ายคืออะไร ตัวอย่างได้แก่ ประเภทสำหรับเที่ยวบิน โรงแรม หรือระยะไมล์
- ประเภทค่าใช้จ่ายสามารถใช้ในการจัดการและการบัญชีโครงการได้หรือไม่
- ชนิดค่าใช้จ่ายคืออะไร
- วิธีการชำระเงินเริ่มต้นสำหรับประเภทค่าใช้จ่ายคืออะไร
- ค่าใช้จ่ายในประเภทค่าใช้จ่ายต้องแยกรายการหรือไม่
- บัญชีเริ่มต้นหลักสำหรับประเภทค่าใช้จ่ายคืออะไร
- กลุ่มภาษีขายสินค้าเริ่มต้นสำหรับประเภทค่าใช้จ่ายคืออะไร
- สามารถใช้วิธีการชำระเงินเพิ่มเติมสำหรับประเภทค่าใช้จ่ายได้หรือไม่ หากอนุญาตวิธีการชำระเงินเพิ่มเติม มีอะไรบ้าง
- มีประเภทย่อยในประเภทค่าใช้จ่ายนี้หรือไม่ หากมีประเภทย่อย คุณต้องตัดสินใจเกี่ยวกับเรื่องต่อไปนี้ด้วย

    - ประเภทย่อยใดๆ ไม่รวมอยู่ในการขอคืนภาษีหรือไม่
    - กลุ่มภาษีขายสินค้าของประเภทย่อยคืออะไร

หากยังใช้ประเภทค่าใช้จ่ายในการจัดการโครงการและการบัญชีด้วย ให้ตอบคำถามที่เหลือ มิฉะนั้น ไปยังส่วนถัดไป

- บัญชีต้นทุนใดที่จะใช้สำหรับค่าใช้จ่ายต่อไปนี้

    - ต้นทุน
    - การจัดสรรเงินเดือน
    - WIP-มูลค่าต้นทุน
    - ต้นทุน-สินค้า
    - WIP-มูลค่าต้นทุน-สินค้า
    - ขาดทุนสะสม
    - WIP-ขาดทุนสะสม

- บัญชีรายได้ใดที่จะใช้สำหรับต่อไปนี้

    - รายได้ที่ออกใบแจ้งหนี้
    - มูลค่าการขายของรายได้ค้างรับ
    - WIP-มูลค่าการขาย
    - รายได้ค้างรับ-การผลิต
    - WIP-การผลิต
    - รายได้ค้างรับ-กำไร
    - WIP-กำไร
    - รายได้ค้างรับ-การสมัครใช้งาน
    - WIP-การสมัครใช้งาน

### <a name="taxes"></a>ภาษี

สำหรับภาษีที่เกี่ยวข้องกับค่าใช้จ่าย คุณต้องกำหนดสิ่งที่รวมหรือเปิดใช้งานในรายงานค่าใช้จ่าย

**การตัดสินใจ:**

- ภาษีการขายรวมอยู่ในยอดค่าใช้จ่ายหรือไม่
- ควรเปิดใช้การกู้คืนภาษีสำหรับค่าใช้จ่ายหรือไม่

    > [!NOTE]
    > เมื่อคุณวางแผนบัญชีแยกประเภททั่วไป หากคุณตัดสินใจที่จะใช้ภาษีการขายของสหรัฐอเมริกาและใช้กฎภาษี คุณจะไม่สามารถเปิดใช้งานการกู้คืนภาษีสำหรับค่าใช้จ่ายได้ (หากต้องการใช้ภาษีการขายของสหรัฐอเมริกาและใช้กฎภาษี ให้ตั้งค่าตัวเลือก **ใช้กฎภาษีการขาย** เป็น **ใช่** )

## <a name="policies"></a>นโยบาย

การสร้างนโยบายรายงานค่าใช้จ่าย คุณสามารถช่วยให้องค์กรของคุณประหยัดเวลาและค่าใช้จ่าย เมื่อพนักงานต้องเสียค่าใช้จ่ายในนามขององค์กร นโยบายช่วยรับประกันว่าพนักงานจะอยู่ในงบประมาณ ให้ข้อมูลที่จำเป็นทั้งหมด และใช้จ่ายเงินตามที่ต้องการเท่านั้น คุณต้องทำการตัดสินใจต่อไปนี้สำหรับนโยบายรายงานค่าใช้จ่ายและนโยบายการอนุมัติรายงานค่าใช้จ่ายแต่ละรายการที่คุณสร้างขึ้น

**การตัดสินใจ:**

- นโยบายชื่ออะไร
- นโยบายค่าใช้จ่ายมีไว้ทำอะไร
- หากก่อนหน้านี้คุณตัดสินใจเปิดใช้ค่าใช้จ่ายระหว่างบริษัท นโยบายนี้จะนำไปใช้กับบริษัทใดในองค์กรของคุณ
- นโยบายนี้มีผลบังคับใช้เมื่อใด
- นโยบายจะหมดอายุเมื่อใด
- กฎของนโยบายคืออะไร
- ผลลัพธ์ของกฎของนโยบายคืออะไร