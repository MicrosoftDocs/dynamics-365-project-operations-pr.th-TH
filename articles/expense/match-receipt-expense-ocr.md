---
title: จับคู่ใบเสร็จกับค่าใช้จ่ายโดยใช้ OCR
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการประมวลผลการรู้จำอักขระด้วยแสง (OCR) สำหรับใบเสร็จรับเงิน
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
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897024"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a>จับคู่ใบเสร็จกับค่าใช้จ่ายโดยใช้ OCR

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

รายการค่าใช้จ่ายได้รับการปรับปรุงโดยการใช้การประมวลผลการรู้จำอักขระด้วยแสง (OCR) สำหรับใบเสร็จรับเงิน ฟังก์ชันนี้ออกแบบมาเพื่อปรับปรุงประสบการณ์ของผู้ใช้เมื่อสร้างรายงานค่าใช้จ่าย

## <a name="key-features"></a>คุณลักษณะสำคัญ

- ระบบจะแยกชื่อผู้ขาย วันที่ และจำนวนเงินทั้งหมดออกจากใบเสร็จรับเงิน
- ระบบจะพยายามจับคู่ใบเสร็จที่ไม่ได้แนบกับธุรกรรมค่าใช้จ่ายที่ไม่ได้แนบมา
- คุณสามารถสร้างธุรกรรมค่าใช้จ่ายที่ป้อนด้วยตนเองจากใบเสร็จรับเงินได้

## <a name="attach-receipts-to-an-expense-report"></a>แนบใบเสร็จรับเงินกับรายงานค่าใช้จ่าย

หากต้องการแนบใบเสร็จรับเงินที่มีธุรกรรมบัตรเครดิตโดยอัตโนมัติเมื่อสร้างรายงานค่าใช้จ่าย ให้ทำตามขั้นตอนต่อไปนี้

  1. เปิดพื้นที่ทำงาน **การจัดการค่าใช้จ่าย**
  2. บนแท็บ **ใบเสร็จรับเงิน** ตรวจสอบว่ามีใบเสร็จรับเงินที่ไม่ได้แนบอยู่ คุณยังสามารถอัปโหลดใบเสร็จรับเงินในแท็บ **รายรับ**
  3. บนแท็บ **ค่าใช้จ่าย** ตรวจสอบว่ามีใบเสร็จรับเงินที่ไม่ได้แนบอยู่ โดยปกติ ผู้ดดูแลระบบค่าใช้จ่ายจะนำเข้าค่าใช้จ่ายเหล่านี้จากผู้ให้บริการบัตรเครดิต
  4. เลือก **รายงานค่าใช้จ่ายใหม่** สังเกตว่าคุณสามารถรวมค่าใช้จ่ายและใบเสร็จรับเงินได้เช่นกันเดียวกับเมื่อคุณสร้างรายงานค่าใช้จ่าย หากคุณเพิ่มทั้งค่าใช้จ่ายและใบเสร็จรับเงิน การจับคู่ใบเสร็จรับเงินกับค่าใช้จ่ายโดยอัตโนมัติจะถูกทริกเกอร์

## <a name="create-or-match-receipts-to-an-expense-report"></a>สร้างหรือจับคู่ใบเสร็จรับเงินกับรายงานค่าใช้จ่าย
หากต้องการสร้างค่าใช้จ่าย หรือจับคู่ค่าใช้จ่ายจากใบเสร็จรับเงิน ให้ทำตามขั้นตอนต่อไปนี้

  1. ในรายงานค่าใช้จ่าย บนแท็บ **ใบเสร็จรับเงิน** ให้แนบใบเสร็จรับเงินโดยการเลือก **เพิ่มใบเสร็จรับเงิน**
  2. ใต้ภาพใบเสร็จรับเงินที่อัปโหลด โปรดสังเกตตัวเลือก **สร้าง** และ **จับคู่**

      - เลือก **สร้าง** เพื่อสร้างธุรกรรมค่าใช้จ่ายที่ป้อนด้วยตนเองและกรอกค่าที่ดึงออกมาจากใบเสร็จรับเงิน
      - หากคุณเลือก **จับคู่** ระบบจะพยายามจับคู่ค่าใช้จ่ายที่มีอยู่กับใบเสร็จรับเงิน

## <a name="installation"></a>การติดตั้ง

หากต้องการใช้ความสามารถของค่าใช้จ่ายขั้นสูงเหล่านี้ ให้ติดตั้ง Add-in ของ บริการจัดการค่าใช้จ่ายสำหรับ Microsoft Dynamics 365 Finance และเปิดคุณลักษณะในอินสแตนซ์ของคุณ คุณสามารถเข้าถึง Add-in จากโครงการของคุณใน Microsoft Dynamics Lifecycle Services (LCS)

1. ลงชื่อเข้าใช้ LCS และเปิดสภาพแวดล้อมที่ต้องการ
2. ไปที่ **รายละเอียดทั้งหมด**
3. เลือก **รักษา** หรือเลื่อนลงไปที่แท็บด่วน **Add-in ของสภาพแวดล้อม**
4. เลือก **ติดตั้ง Add-in ใหม่**
5. เลือก **บริการจัดการค่าใช้จ่าย**
6. ปฏิบัติตามคู่มือการติดตั้ง และยอมรับข้อกำหนดและเงื่อนไข
7. เลือก **ติดตั้ง**

ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** เปิดคุณลักษณะต่อไปนี้:

- รายงานค่าใช้จ่ายที่สมมติขึ้น
- จับคู่อัตโนมัติและสร้างค่าใช้จ่ายจากใบเสร็จรับเงิน

เมื่อคุณเปิดคุณลักษณะเหล่านี้ การดำเนินการต่อไปนี้จะเกิดขึ้น:

- พื้นที่ทำงาน **การจัดการค่าใช้จ่าย** ที่มีอยู่จะถูกแทนที่ด้วยพื้นที่ทำงานใหม่
- ระบบจะเพิ่มรายการเมนูใหม่สำหรับการมองเห็นฟิลด์ค่าใช้จ่าย
- คุณยังสามารถเปิดเพจ **รายงานค่าใช้จ่าย** ของเดิมได้โดยไปที่ **การจัดการค่าใช้จ่าย > ค่าใช้จ่ายของฉัน > รายงานค่าใช้จ่าย**
- เวิร์กโฟลว์และการอนุมัติใดๆ ยังคงนำคุณไปยังเพจรายงานค่าใช้จ่ายที่มีอยู่
- ใบเสร็จรับเงินจะได้รับการดำเนินการผ่าน Microsoft Azure Cognitive Services และเมตาดาต้าจะถูกแยกและเพิ่ม
- มีการเพิ่มตัวเลือกที่ช่วยให้คุณสามารถสร้างรายงานค่าใช้จ่ายที่มีใบเสร็จรับเงินที่ไม่ได้แนบที่ตรงกัน
- ตัวเลือกที่เพิ่มลงในรายงานค่าใช้จ่ายช่วยให้คุณสามารถสร้างรายการค่าใช้จ่ายจากใบเสร็จรับเงิน หรือพยายามจับคู่ใบเสร็จรับเงินที่มีอยู่กับรายการค่าใช้จ่ายที่มีอยู่

## <a name="frequently-asked-questions"></a>คำถามที่ถามบ่อย

**Microsoft ใช้ข้อมูลของฉันสำหรับแบบจำลองหรือไม่**

ไม่ Microsoft สร้างแบบจำลองการเรียนรู้ของเครื่องทั่วไปสำหรับบริการประมวลผลใบเสร็จรับเงิน แบบจำลองนี้ไม่ได้ขึ้นอยู่กับใบเสร็จรับเงินที่คุณอัปโหลด

**คุณลักษณะนี้มีให้บริการและประมวลผลที่ไหน**

ปัจจุบัน รองรับในสหรัฐอเมริกา

**ใบเสร็จรับเงินของฉันไปที่ไหน**

Finance จะติดต่อ Cognitive Services เพื่อดึงข้อมูลภาคสนาม Cognitive Services จะเก็บสำเนาใบเสร็จรับเงินของคุณไว้เป็นเวลา 24 ชั่วโมงในขณะที่มีการประมวลผล หลังจากการประมวลผลเสร็จสิ้น Cognitive Services จะลบใบเสร็จรับเงินออก ใบเสร็จรับเงินยังคงเก็บไว้ใน Finance

สำหรับข้อมูลเพิ่มเติม โปรดดู [เปิดใช้งานการทำความเข้าใจใบเสร็จรับเงินด้วยความสามารถใหม่ของตัวรู้จำฟอร์ม](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)
