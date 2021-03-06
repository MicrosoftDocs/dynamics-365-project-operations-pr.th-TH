---
title: การขอคืน VAT ในการจัดการค่าใช้จ่าย
description: หัวข้อนี้จะอธิบายวิธีขอรับเงินคืนสำหรับธุรกรรมภาษีมูลค่าเพิ่ม (VAT) ที่มีสิทธิ์
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 2c20e4a7fa9748e03bf1729fc2f7bdbfc2f292d1
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908672"
---
# <a name="vat-recovery-in-expense-management"></a>การขอคืน VAT ในการจัดการค่าใช้จ่าย

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_

ในการขอรับเงินคืนสำหรับธุรกรรมภาษีมูลค่าเพิ่ม (VAT) ที่มีสิทธิ์ บริษัทหรือองค์กรต้องระบุ รวบรวม ตรวจสอบ และส่งข้อมูลที่ถูกต้อง กระบวนการนี้รวมถึงงานหลายงาน และขึ้นอยู่กับขนาดของบริษัทของคุณ สามารถรวมพนักงานหรือบทบาทได้หลายรายการ

หากต้องการขอคืน VAT ในโมดูล **การจัดการค่าใช้จ่าย** ต้องมีสิ่งที่จำเป็นดังต่อไปนี้:

- ต้องสร้างรหัสภาษีสำหรับประเทศ/ภูมิภาคที่จัดสรรให้กับประเภทค่าใช้จ่าย
- ต้องสร้างกลุ่มภาษีขายสำหรับแต่ละรหัสภาษี
- ต้องสร้างรหัสภาษีขายสินค้าสำหรับกลุ่มภาษีขายแต่ละกลุ่ม

หลังจากข้อกำหนดเบื้องต้นเสร็จแล้ว ขั้นตอนต่อไปนี้จะต้องดำเนินการเพื่อขอคืนเงินสำหรับธุรกรรม VAT

1. ในรายงานค่าใช้จ่าย ให้ป้อนข้อมูลภาษีเกี่ยวกับธุรกรรมบัตรเครดิตเพื่อระบุการขอคืน VAT ที่มีสิทธิ์
2. ตรวจสอบว่าข้อมูลภาษีครบถ้วนแล้วลงรายการบัญชีรายงานค่าใช้จ่าย
3. ดำเนินการกับค่าใช้จ่ายที่มีสิทธิ์ในการขอคืน VAT ระหว่างประเทศ
4. ส่งข้อมูลการขอคืน VAT ไปยังผู้จำหน่ายบุคคลที่สามเพื่อยื่นขอคืนระหว่างประเทศ
5. ดำเนินการกับค่าใช้จ่ายสำหรับการขอคืน VAT ในประเทศ

ส่วนต่อไปนี้เป็นตัวอย่างที่แสดงให้เห็นว่าพนักงานของ Contoso ทำแต่ละขั้นตอนอย่างไร

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>ป้อนข้อมูลภาษีเกี่ยวกับธุรกรรมบัตรเครดิตเพื่อระบุการขอคืน VAT ที่มีสิทธิ์

Nancy ตัวแทนฝ่ายขายของ Contoso ซึ่งประจำอยู่ในสหรัฐอเมริกาเพิ่งกลับจากการเดินทางของฝ่ายขายที่สหราชอาณาจักร ระหว่างการเดินทาง Nancy มีค่าใช้จ่ายผ่านบัตรเครดิตส่วนตัวสำหรับมื้ออาหาร ตอนนี้ Nancy ต้องสร้างรายงานค่าใช้จ่ายเพื่อกระทบยอดค่าใช้จ่าย

เมื่อ Nancy ป้อนข้อมูลในรายงานค่าใช้จ่าย เธอจะเลือก **อังกฤษ** ในฟิลด์ **ประเทศ/ภูมิภาค** บนเพจ **แก้ไขรายงานค่าใช้จ่าย** จากนั้น จะมีการกรองรายการกลุ่มภาษีขายเพื่อให้แสดงเฉพาะกลุ่มที่ใช้กับสหราชอาณาจักร Nancy เลือกกลุ่มภาษีขาย **สหราชอาณาจักร 001** แล้วเลือกกลุ่มภาษีขายสินค้า **มื้ออาหาร** จากนั้น Nancy เพิ่มธุรกรรมใหม่สำหรับที่พัก เนื่องจากมีกลุ่มภาษีขายเพียงกลุ่มเดียวและกลุ่มภาษีขายสินค้าหนึ่งกลุ่มสำหรับที่พักในสหราชอาณาจักร ข้อมูลนี้จะมีการกรอกโดยอัตโนมัติในรายงานค่าใช้จ่ายของ Nancy

ตามนโยบาย Contoso ค่าใช้จ่ายทั้งหมดต้องมีใบเสร็จรับเงินที่ตรงกัน ดังนั้นเมื่อ Nancy บันทึกรายงานค่าใช้จ่าย เธอจะได้รับข้อความที่ระบุว่าเธอต้องแนบใบเสร็จรับเงินสำหรับธุรกรรมแต่ละรายการที่เธอระบุไว้ในรายงานค่าใช้จ่ายของเธอ Nancy ตรวจสอบว่าเธอได้แนบภาพดิจิทัลของใบเสร็จรับเงินของธุรกรรมแต่ละรายการในรายงานค่าใช้จ่ายของเธอแล้ว จากนั้นจึงส่งรายงานเพื่อขออนุมัติ จากนั้น เธอจะส่งใบเสร็จรับเงินให้กับทีมประมวลผลส่วนสนับสนุน ทีมนี้จะส่งข้อมูลการขอคืน VAT ไปยังผู้จัดจำหน่ายบุคคลที่สามที่ยื่นการขอคืน VAT ระหว่างประเทศสำหรับ Contoso

## <a name="verify-tax-information-and-post-an-expense-report"></a>ตรวจสอบข้อมูลภาษีและลงรายการบัญชีรายงานค่าใช้จ่าย

ก่อนที่ April ผู้ประสานงานบัญชีเจ้าหนี้ของ Contoso สามารถลงรายการบัญชีรายงานค่าใช้จ่าย เธอต้องป้อนข้อมูลภาษีใดๆ ที่ขาดหายไป เธอเปิดเพจ **รายละเอียดรายงานค่าใช้จ่าย** และเห็นรายงานค่าใช้จ่ายที่ได้รับอนุมัติของ Nancy จากนั้น April จะเปิดรายงานค่าใช้จ่ายเพื่อดูรายละเอียดของธุรกรรม เธอเห็นว่า Nancy ไม่ได้ป้อนกลุ่มภาษีการขายสินค้าสำหรับธุรกรรมรายการใดรายการหนึ่ง เนื่องจากไม่ได้ให้ข้อมูลนี้ April จึงไม่สามารถลงรายการบัญชีรายงานค่าใช้จ่ายได้ ดังนั้นเธอจึงดูที่เพจ **การกำหนดค่าภาษี** ในการจัดการค่าใช้จ่าย และค้นหากลุ่มภาษีขายสินค้าที่เหมาะสมสำหรับประเทศ/ภูมิภาค และชนิดธุรกรรม ตอนนี้ April สามารถลงรายการบัญชีรายงานค่าใช้จ่ายไปยังบัญชีแยกประเภททั่วไปได้แล้ว

เมื่อ April ลงรายการบัญชีรายงานค่าใช้จ่าย จะมีการสร้างรายการงานที่ขอคืน VAT รายการงานนี้มีการกำหนดให้กับสมาชิกของทีมประมวลผลส่วนสนับสนุน April ได้รับข้อความที่ยืนยันว่าการลงรายการบัญชีสำเร็จ ข้อความนี้ยังแสดงจำนวนธุรกรรม VAT ที่ถูกระบุสำหรับการขอคืน

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>ดำเนินการกับค่าใช้จ่ายที่มีสิทธิ์ในการขอคืน VAT ระหว่างประเทศ

Arnie ซึ่งเป็นสมาชิกของทีมประมวลผลส่วนสนับสนุนของ Contoso มีหน้าที่ตรวจสอบว่าข้อมูลที่จำเป็นทั้งหมดสำหรับการขอคืน VAT รวมอยู่ในรายงานค่าใช้จ่าย เขาเปิดเพจ **การขอคืนภาษีค่าใช้จ่าย** และเลือกรายงานค่าใช้จ่ายที่ Nancy ส่งมา จากนั้น Arnie จะตรวจสอบว่ามีการแนบใบเสร็จรับเงินที่จำเป็นทั้งหมดและป้อนกลุ่มภาษีขายและรหัสภาษีขายสินค้าที่ถูกต้อง

เมื่อ Arnie ได้รับใบเสร็จรับเงินจาก Nancy เขาจะตรวจสอบใบเสร็จรับเงินดิจิทัล จากนั้นจึงเปลี่ยนสถานะของรายงานค่าใช้จ่ายเป็น **พร้อมสำหรับการขอคืน**

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>ส่งข้อมูลการขอคืน VAT ไปยังผู้จำหน่ายบุคคลที่สาม

เมื่อ Arnie พร้อมที่จะส่งข้อมูลรายงานค่าใช้จ่ายไปยังผู้จัดจำหน่ายบุคคลที่สามซึ่งจะยื่นแบบแสดงรายการขอคืน VAT เขาจะเปิดเพจ **การขอคืนภาษีค่าใช้จ่าย** เขากรองเพจเพื่อให้แสดงเฉพาะรายงานค่าใช้จ่ายที่ทำเครื่องหมายเป็น **พร้อมสำหรับการขอคืน** จากนั้น Arnie เลือก **ไฟล์** &gt; **ส่งออกเป็น Excel** ข้อมูล VAT จากรายงานค่าใช้จ่ายจะถูกส่งออกเป็นเวิร์กชีต Microsoft Excel Arnie ส่งเวิร์กชีตนี้ไปยังผู้จัดจำหน่ายบุคคลที่สามและมีข้อความที่ระบุว่าผู้จัดส่งได้ส่งเอกสารใบเสร็จรับเงินแล้ว

## <a name="process-expenses-for-domestic-vat-recovery"></a>ดำเนินการกับค่าใช้จ่ายสำหรับการขอคืน VAT ในประเทศ

Arnie ต้องตรวจสอบว่าธุรกรรมของรายงานค่าใช้จ่ายมีสิทธิ์ได้รับการขอคืน VAT และมีการแนบใบเสร็จดิจิทัลกับรายงาน หากต้องการเริ่มประมวลผลค่าใช้จ่ายที่มีสิทธิ์สำหรับการขอคืนในประเทศ Arnie เปิดเพจ **การขอคืนภาษีค่าใช้จ่าย** และเลือกรายงานค่าใช้จ่ายที่ต้องการการตรวจสอบ เขาตรวจสอบว่าใบเสร็จรับเงินออกในชื่อบริษัทไม่ใช่ชื่อพนักงาน (สำหรับการขอคืน VAT ใบเสร็จรับเงินต้องออกในชื่อบริษัท) จากนั้น Arnie จะตรวจสอบว่ามีการแนบใบเสร็จรับเงินที่จำเป็นทั้งหมดและป้อนกลุ่มภาษีขายและรหัสภาษีขายสินค้าที่ถูกต้อง

เมื่อ Arnie ได้รับเอกสารใบเสร็จรับเงิน เขาจะเปลี่ยนสถานะของรายงานค่าใช้จ่ายเป็น **พร้อมสำหรับการขอคืน** จากนั้นเขาสามารถยื่นแบบแสดงรายการขอคืนกับหน่วยงานด้านภาษีที่เหมาะสม ในกรณีนี้ หน่วยงานด้านภาษีที่เหมาะสมในสหรัฐอเมริกาคือ Internal Revenue Service (IRS)
