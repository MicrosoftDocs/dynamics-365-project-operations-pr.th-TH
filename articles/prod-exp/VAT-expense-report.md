---
title: การกู้คืน VAT
description: หัวข้อนี้จะอธิบายวิธีขอคืนเงินคืนสำหรับธุรกรรมภาษีมูลค่าเพิ่ม (VAT)
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1be96521cdb486dd5a702cded615d3e1015b364
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085974"
---
# <a name="vat-recovery"></a>การกู้คืน VAT 

[!include [banner](../includes/banner.md)]

ในการขอรับเงินคืนสำหรับธุรกรรมภาษีมูลค่าเพิ่ม (VAT) ที่มีสิทธิ์ บริษัทหรือองค์กรต้องระบุ รวบรวม ตรวจสอบ และส่งข้อมูลที่ถูกต้อง กระบวนการนี้รวมถึงงานหลายงาน และขึ้นอยู่กับขนาดของบริษัทของคุณ สามารถรวมพนักงานหรือบทบาทได้หลายรายการ

หากต้องการขอคืน VAT โดยการใช้การจัดการค่าใช้จ่าย ต้องดำเนินการข้อกำหนดเบื้องต้นต่อไปนี้ให้เสร็จสมบูรณ์:

- ต้องสร้างรหัสภาษีสำหรับประเทศ/ภูมิภาคที่จัดสรรให้กับประเภทค่าใช้จ่าย
- ต้องสร้างกลุ่มภาษีขายสำหรับแต่ละรหัสภาษี
- ต้องสร้างรหัสภาษีขายสินค้าสำหรับกลุ่มภาษีขายแต่ละกลุ่ม

หลังจากข้อกำหนดเบื้องต้นเสร็จสมบูรณ์แล้ว พนักงานจะทำตามขั้นตอนเหล่านี้เพื่อขอคืนเงินสำหรับธุรกรรม VAT

1. ในรายงานค่าใช้จ่าย ให้ป้อนข้อมูลภาษีเกี่ยวกับธุรกรรมบัตรเครดิตเพื่อระบุการขอคืน VAT ที่มีสิทธิ์
2. ตรวจสอบให้แน่ใจว่าข้อมูลภาษีครบถ้วน แล้วจากนั้น ลงรายการบัญชีรายงานค่าใช้จ่าย
3. ดำเนินการกับค่าใช้จ่ายที่มีสิทธิ์ในการขอคืน VAT ระหว่างประเทศ
4. ส่งข้อมูลการขอคืน VAT ไปยังผู้จำหน่ายบุคคลที่สามเพื่อยื่นขอคืนระหว่างประเทศ
5. ดำเนินการกับค่าใช้จ่ายสำหรับการขอคืน VAT ในประเทศ

ส่วนต่อไปนี้เป็นตัวอย่างที่แสดงให้เห็นว่าพนักงานของ Contoso ทำแต่ละขั้นตอนอย่างไร

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>ในรายงานค่าใช้จ่าย ให้ป้อนข้อมูลภาษีเกี่ยวกับธุรกรรมบัตรเครดิตเพื่อระบุเงินคืน VAT ที่มีสิทธิ์

Nancy ตัวแทนฝ่ายขายของ Contoso ซึ่งประจำอยู่ในสหรัฐอเมริกา เพิ่งกลับจากการเดินทางของฝ่ายขายที่สหราชอาณาจักร ในระหว่างการเดินทางของเธอ เธอมีค่าใช้จ่ายผ่านบัตรเครดิตส่วนตัวสำหรับมื้ออาหาร ตอนนี้ Nancy ต้องสร้างรายงานค่าใช้จ่ายเพื่อกระทบยอดค่าใช้จ่ายของเธอ

เมื่อ Nancy ป้อนข้อมูลในรายงานค่าใช้จ่ายของเธอ เธอจะเลือก **สหราชอาณาจักร** ในฟิลด์ **ประเทศ/ภูมิภาค** บนหน้า **แก้ไขรายงานค่าใช้จ่าย** จากนั้น จะมีการกรองรายการกลุ่มภาษีขายเพื่อให้แสดงเฉพาะกลุ่มที่ใช้กับสหราชอาณาจักร Nancy เลือกกลุ่มภาษีขาย **สหราชอาณาจักร 001** แล้วเลือกกลุ่มภาษีขายสินค้า **มื้ออาหาร** จากนั้น เธอเพิ่มธุรกรรมใหม่สำหรับที่พักของเธอ เนื่องจากมีกลุ่มภาษีขายเพียงกลุ่มเดียวและกลุ่มภาษีขายสินค้าหนึ่งกลุ่มสำหรับที่พักในสหราชอาณาจักร ข้อมูลนี้จะมีการกรอกโดยอัตโนมัติในรายงานค่าใช้จ่ายของ Nancy

ตามนโยบาย Contoso ค่าใช้จ่ายทั้งหมดต้องมีใบเสร็จรับเงินที่ตรงกัน ดังนั้น เมื่อ Nancy บันทึกรายงานค่าใช้จ่ายของเธอ เธอจะได้รับข้อความที่ระบุว่าเธอต้องแนบใบเสร็จรับเงินสำหรับธุรกรรมแต่ละรายการที่เธอระบุไว้ในรายงานค่าใช้จ่ายของเธอ Nancy ตรวจสอบว่าเธอได้แนบภาพดิจิทัลของใบเสร็จรับเงินของธุรกรรมแต่ละรายการในรายงานค่าใช้จ่ายของเธอแล้ว จากนั้นจึงส่งรายงานเพื่อขออนุมัติ จากนั้น เธอจะส่งใบเสร็จรับเงินให้กับทีมประมวลผลส่วนสนับสนุน ทีมนี้จะส่งข้อมูลการขอคืน VAT ไปยังผู้จัดจำหน่ายบุคคลที่สามที่ยื่นการขอคืน VAT ระหว่างประเทศสำหรับ Contoso

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>ตรวจสอบให้แน่ใจว่าข้อมูลภาษีครบถ้วน แล้วจากนั้น ลงรายการบัญชีรายงานค่าใช้จ่าย

April ผู้ประสานงานบัญชีเจ้าหนี้สำหรับ Contoso สามารถป้อนข้อมูลภาษีใดๆ ที่ขาดหายไปจากรายงานค่าใช้จ่าย ก่อนที่จะสามารถลงรายการบัญชีรายงานได้ เธอเปิดเพจ **รายละเอียดรายงานค่าใช้จ่าย** และเห็นรายงานค่าใช้จ่ายที่ได้รับอนุมัติของ Nancy จากนั้น April จะเปิดรายงานค่าใช้จ่ายเพื่อดูรายละเอียดของธุรกรรม เธอเห็นว่า Nancy ไม่ได้ป้อนกลุ่มภาษีการขายสินค้าสำหรับธุรกรรมรายการใดรายการหนึ่ง เนื่องจากไม่ได้ให้ข้อมูลนี้ April จึงไม่สามารถลงรายการบัญชีรายงานค่าใช้จ่ายได้ ดังนั้น April จึงดูที่หน้า **การตั้งค่าคอนฟิกภาษี** ในการจัดการค่าใช้จ่าย และค้นหากลุ่มภาษีขายสินค้าที่เหมาะสมสำหรับประเทศ/ภูมิภาค และชนิดธุรกรรม ตอนนี้ April สามารถลงรายการบัญชีรายงานค่าใช้จ่ายไปยังบัญชีแยกประเภททั่วไปได้แล้ว

เมื่อ April ลงรายการบัญชีรายงานค่าใช้จ่าย จะมีการสร้างรายการงานที่ขอคืน VAT รายการงานนี้มีการกำหนดให้กับสมาชิกของทีมประมวลผลส่วนสนับสนุน April ได้รับข้อความที่ยืนยันว่าการลงรายการบัญชีสำเร็จ ข้อความนี้ยังแสดงจำนวนธุรกรรม VAT ที่ถูกระบุสำหรับการขอคืน

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>ดำเนินการกับค่าใช้จ่ายที่มีสิทธิ์ในการขอคืน VAT ระหว่างประเทศ

Arnie ซึ่งเป็นสมาชิกของกลุ่มคนประมวลผลส่วนสนับสนุนของ Contoso มีหน้าที่ยืนยันว่าข้อมูลที่จำเป็นทั้งหมดสำหรับการขอคืน VAT ถูกรวมอยู่ในรายงานค่าใช้จ่าย เขาเปิดเพจ **การขอคืนภาษีค่าใช้จ่าย** และเลือกรายงานค่าใช้จ่ายที่ Nancy ส่งมา Arnie จะตรวจสอบว่ามีการแนบใบเสร็จรับเงินที่จำเป็นทั้งหมดและมีการป้อนกลุ่มภาษีขายและรหัสภาษีขายสินค้าที่ถูกต้อง

เมื่อ Arnie ได้รับใบเสร็จรับเงินจาก Nancy เขาจะตรวจสอบใบเสร็จรับเงินเทียบกับใบเสร็จรับเงินดิจิทัล และจากนั้น จึงเปลี่ยนสถานะของรายงานค่าใช้จ่ายเป็น **พร้อมสำหรับการขอคืน**

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>ส่งข้อมูลการขอคืน VAT ไปยังผู้จำหน่ายบุคคลที่สามเพื่อยื่นขอคืนระหว่างประเทศ

เมื่อ Arnie พร้อมที่จะส่งข้อมูลรายงานค่าใช้จ่ายไปยังผู้จัดจำหน่ายบุคคลที่สามซึ่งจะยื่นแบบแสดงรายการขอคืน VAT เขาจะเปิดเพจ **การขอคืนภาษีค่าใช้จ่าย** เขากรองเพจเพื่อให้แสดงเฉพาะรายงานค่าใช้จ่ายที่ทำเครื่องหมายเป็น **พร้อมสำหรับการขอคืน** จากนั้น Arnie เลือก **ไฟล์** &gt; **ส่งออกเป็น Excel** ข้อมูล VAT จากรายงานค่าใช้จ่ายจะถูกส่งออกเป็นเวิร์กชีต Microsoft Excel Arnie ส่งเวิร์กชีตนี้ไปยังผู้จัดจำหน่ายบุคคลที่สามและมีข้อความที่ระบุว่าผู้จัดส่งได้ส่งเอกสารใบเสร็จรับเงินแล้ว

## <a name="process-expenses-for-domestic-vat-recovery"></a>ดำเนินการกับค่าใช้จ่ายสำหรับการขอคืน VAT ในประเทศ

Arnie ต้องตรวจสอบว่าธุรกรรมของรายงานค่าใช้จ่ายมีสิทธิ์ได้รับการขอคืน VAT และมีการแนบใบเสร็จดิจิทัลกับรายงาน หากต้องการเริ่มประมวลผลค่าใช้จ่ายที่มีสิทธิ์สำหรับการขอคืนในประเทศ Arnie เปิดเพจ **การขอคืนภาษีค่าใช้จ่าย** และเลือกรายงานค่าใช้จ่ายที่ต้องการการตรวจสอบ เขาตรวจสอบว่าใบเสร็จรับเงินออกในชื่อบริษัทไม่ใช่ชื่อพนักงาน สำหรับการขอคืน VAT ใบเสร็จรับเงินจะต้องเป็นชื่อของบริษัท จากนั้น Arnie ยืนยันว่ามีการใช้กลุ่มภาษีขายและรหัสภาษีขายสินค้าที่ถูกต้อง

เมื่อ Arnie ได้รับเอกสารใบเสร็จรับเงิน เขาจะเปลี่ยนสถานะของรายงานค่าใช้จ่ายเป็น **พร้อมสำหรับการขอคืน** จากนั้นเขาสามารถยื่นแบบแสดงรายการขอคืนกับหน่วยงานด้านภาษีที่เหมาะสม ในกรณีนี้ หน่วยงานด้านภาษีที่เหมาะสมในสหรัฐอเมริกาคือ Internal Revenue Service (IRS)