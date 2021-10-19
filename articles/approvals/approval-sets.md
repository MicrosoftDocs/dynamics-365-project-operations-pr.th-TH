---
title: ชุดการอนุมัติ
description: หัวข้อนี้อธิบายวิธีการทำงานกับชุดการอนุมัติ คำขอ และชุดย่อยของการดำเนินการเหล่านั้น
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323259"
---
# <a name="approval-sets"></a>ชุดการอนุมัติ

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

การอนุมัติจะกำหนดคำขออนุมัติกลุ่มไว้ด้วยกันเป็นส่วนย่อยของการดำเนินงาน การจัดกลุ่มนี้อนุญาตให้ประมวลผลการอนุมัติตามโครงการในลำดับเฉพาะและอนุญาตการลองใหม่และการกำหนดลำดับ การจัดกลุ่มคำขอการอนุมัติเข้าด้วยกันจะช่วยเพิ่มความน่าเชื่อถือและความสามารถในการตรวจสอบย้อนกลับของการประมวลผลการอนุมัติสำหรับการอนุมัติปริมาณมาก

ชุดการอนุมัติระบุสถานะการประมวลผลโดยรวมของเรกคอร์ดที่เกี่ยวข้อง เมื่อมีการประมวลผลเรกคอร์ดการอนุมัติโดยใช้ชุดการอนุมัติ เรกคอร์ดจะย้ายจาก **ส่งแล้ว** เป็น **อนุมัติแล้ว** และไม่ได้เชื่อมโยงกับชุดการอนุมัติอีกต่อไป หากเรกคอร์ดล้มเหลวเมื่อส่งเพื่อขออนุมัติ เรกคอร์ดจะยังคงอยู่ในสถานะ **ส่ง** และชุดการอนุมัติถูกทำเครื่องหมายว่าล้มเหลว ชุดการอนุมัติจะบันทึกข้อความแสดงข้อผิดพลาดของความล้มเหลว

## <a name="processing-approvals-and-approval-sets"></a>การประมวลผลการอนุมัติและชุดการอนุมัติ
การอนุมัติที่อยู่ในคิวสำหรับการประมวลผลจะปรากฏในมุมมอง **การประมวลผลการอนุมัติ** ระบบจะประมวลผลรายการทั้งหมดแบบอะซิงโครนัสหลายครั้ง รวมถึงการอนุมัติใหม่อีกครั้งหากความพยายามครั้งก่อนล้มเหลว

ฟิลด์ **อายุการใช้งานชุดการอนุมัติ** จะบันทึกจำนวนครั้งที่เหลือในการประมวลผลชุดก่อนที่จะถูกทำเครื่องหมายว่าล้มเหลว

## <a name="failed-approvals-and-approval-sets"></a>การอนุมัติและชุดการอนุมัติล้มเหลว
มุมมอง **การอนุมัติที่ล้มเหลว** แสดงรายการของการอนุมัติทั้งหมดที่ต้องมีการแทรกแซงจากผู้ใช้ เปิดบันทึกชุดการอนุมัติที่เกี่ยวข้องเพื่อระบุสาเหตุของความล้มเหลว
การเลือก **ลองอีกครั้ง** เพิ่มการนับอายุการใช้งานชุดการอนุมัติ ย้ายชุดการอนุมัติกลับเป็นสถานะ **กำลังดำเนินการ** และพยายามประมวลผลเรกคอร์ดที่เหลือ

## <a name="configure-approval-sets"></a>กำหนดค่าชุดการอนุมัติ

### <a name="enable-the-approval-sets-feature"></a>เปิดใช้งานคุณสมบัติชุดการอนุมัติ
ก่อนที่คุณจะเปิดใช้งานคุณลักษณะชุดการอนุมัติ ให้ตรวจสอบว่าไม่มีการอนุมัติที่กำลังดำเนินการอยู่

- ไปที่หน้า **พารามิเตอร์โครงการ** และเลือก **การควบคุมคุณลักษณะ** > **เปิดใช้งานการอนุมัติสมัยใหม่**

### <a name="turn-off-the-approval-sets-feature"></a>ปิดใช้งานคุณสมบัติชุดการอนุมัติ
ก่อนที่คุณจะปิดใช้งานคุณลักษณะชุดการอนุมัติ ให้ตรวจสอบว่าไม่มีการอนุมัติที่กำลังดำเนินการอยู่

- ไปที่หน้า **พารามิเตอร์โครงการ** และเลือก **การควบคุมคุณลักษณะ** > **ปิดใช้งานการอนุมัติสมัยใหม่**

### <a name="configuring-the-asynchronous-threshold"></a>การกำหนดค่าขีดจำกัดแบบอะซิงโครนัส 
เมื่อมีการสร้างชุดการอนุมัติ การประมวลผลจะย้ายไปเบื้องหลังเมื่อจำนวนเรกคอร์ดที่เลือกสำหรับการอนุมัติเกินเกณฑ์ที่ระบุ ใช้ฟิลด์ **เกณฑ์แบบอะซิงโครนัส** เพื่อกำหนดค่าเมื่อการประมวลผลการอนุมัติควรทำงานแบบซิงโครนัสหรืออะซิงโครนัส เลือกอย่างน้อยหนึ่งค่าต่อไปนี้:

  - ศูนย์: คำขอทั้งหมดควรได้รับการประมวลผลแบบอะซิงโครนัส 
  - ตัวเลขที่มากกว่าศูนย์: การอนุมัติจะได้รับการประมวลผลแบบอะซิงโครนัสเฉพาะเมื่อจำนวนการอนุมัติที่ส่งเกินค่านี้

[!INCLUDE[footer-include](../includes/footer-banner.md)]