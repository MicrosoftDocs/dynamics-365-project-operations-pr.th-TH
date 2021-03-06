---
title: ปิดใบเสนอราคา
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการปิดใบเสนอราคาใน Project Operations
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c429fa14b4b95420c67a91a6a59af7db2660f68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898914"
---
# <a name="close-a-quote"></a>ปิดใบเสนอราคา

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_

การเสนอราคาโครงการสามารถปิดเป็นชนะหรือแพ้ เพราะฟังก์ชันเปิดใช้งานและแก้ไขไม่ได้รองรับใบเสนอราคาใน Microsoft Dynamics 365 Project Operations คุณจึงสามารถปิดใบเสนอราคาแบบร่างได้

## <a name="close-a-quote-as-won"></a>ปิดใบเสนอราคาเป็นชนะ

การปิดใบเสนอราคาโครงการเป็นชนะจะตั้งค่าใบเสนอราคาเป็น **ปิดแล้ว** และคำอธิบายรายการของสถานะเป็น **ชนะ** การปิดใบเสนอราคาทำให้ใบเสนอราคาโครงการเป็นแบบอ่านอย่างเดียวและสร้างสัญญาโครงการฉบับร่างที่มีข้อมูลใบเสนอราคาทั้งหมด เนื่องจากไม่สามารถเปิดใบเสนอราคาที่ปิดแล้วใหม่ได้ ก่อนที่คุณจะปิดใบเสนอราคา กล่องโต้ตอบการยืนยันจะยืนยันการเปลี่ยนแปลงของคุณ

นอกจากนี้ สัญญาโครงการที่สร้างขึ้นจากใบเสนอราคาโครงการยังมีอยู่ในโมดูลการจัดการและการบัญชีโครงการของ Project Operations หากไม่มีการแม็ปสัญญาโครงการกับโครงการในรายการใดๆ สัญญาโครงการนี้จะมีอยู่เป็นสัญญาโครงการที่ไม่ใช้งานและจะกลับมาใช้งานได้ทันทีที่มีการจับคู่โครงการกับรายละเอียดการให้บริการตามสัญญาอย่างน้อยหนึ่งรายการ

หากมีการแนบใบเสนอราคาเข้ากับโอกาสทางการขาย ใบเสนอราคาโครงการอื่นๆ เกี่ยวกับโอกาสทางการขายจะถูกปิดเป็นแพ้โดยอัตโนมัติ

### <a name="financial-impact-of-closing-a-quote-as-won"></a>ผลกระทบทางการเงินของการปิดใบเสนอราคาเป็นแพ้

หากมีการบันทึกเวลาจริงไว้ในโครงการในขณะที่ยังแนบอยู่กับใบเสนอราคาแบบร่าง ระบบจะบันทึกเฉพาะต้นทุนของเวลาหรือค่าใช้จ่ายเท่านั้น หลังจากปิดใบเสนอราคาเป็นชนะ แอปพลิเคชันจะปรับโครงสร้างต้นทุนใหม่โดยการย้อนกลับต้นทุนจริงที่เก่ากว่าและสร้างต้นทุนจริงใหม่ขึ้นมาใหม่ แอปพลิเคชันจะประมวลผลต้นทุนจริงตามวิธีการเรียกเก็บเงินของรายละเอียดการให้บริการตามสัญญาโครงการที่เกี่ยวข้อง หากต้นทุนจริงอ้างอิงตามเวลาและรายละเอียดการให้บริการตามสัญญาวัสดุ ระบบจะสร้างยอดขายจริงที่ยังไม่เรียกเก็บเงินที่สอดคล้องกันโดยอัตโนมัติเมื่อปิดใบเสนอราคาและมีการสร้างสัญญาโครงการ หากต้นทุนจริงอ้างอิงรายละเอียดการให้บริการตามสัญญาที่มีราคาคงที่ แอปพลิเคชันจะหยุดประมวลผลต้นทุนจริงตามกฎการเรียกเก็บเงินแบบแบ่งจ่ายสำหรับลูกค้าสัญญาโครงการ

ข้อมูลจริงที่ประมวลผลซ้ำทั้งหมดมีอยู่ในโมดูลการจัดการและการบัญชีโครงการสำหรับให้นักบัญชีโครงการตรวจสอบ ปรับปรุง และลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไป 

## <a name="close-a-quote-as-lost"></a>ปิดใบเสนอราคาเป็นแพ้

การปิดใบเสนอราคาโครงการเป็น แพ้ จะตั้งค่าสถานะเป็น **ปิดแล้ว** และคำอธิบายรายการของสถานะเป็น **แพ้** การปิดใบเสนอราคาจะทำให้เป็นแบบอ่านอย่างเดียว เนื่องจากไม่สามารถเปิดใบเสนอราคาที่ปิดแล้วใหม่ได้และก่อนที่คุณจะปิดใบเสนอราคา กล่องโต้ตอบการยืนยันจะยืนยันการเปลี่ยนแปลงของคุณ

หากการเสนอราคาโครงการที่ปิดเป็นแพ้ มีโครงการที่อ้างอิงในรายการใดๆ โครงการนั้นจะถูกทำเครื่องหมายเป็นปิดแล้ว และการจองทรัพยากรใดๆ นับจากวันนั้นจะถูกยกเลิก

> [!NOTE]
> ใน Project Operations การปิดใบเสนอราคาเป็นชนะหรือแพ้จะไม่ส่งผลกระทบต่อสถานะของโอกาสทางการขาย ซึ่งโอกาสทางการขายจะยังคงเปิดอยู่จนกว่าจะมีการปิดด้วยตนเอง
