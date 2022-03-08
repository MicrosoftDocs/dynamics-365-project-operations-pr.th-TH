---
title: การรวม Microsoft Project Client
description: การวางแผนและการดูแลกำหนดการโครงการอาจมีความซับซ้อน ดังนั้นผู้จัดการโครงการจึงจำเป็นต้องใช้เครื่องมือที่ช่วยจัดการงานนี้ การรวมกับ Microsoft Project Client ให้การสนับสนุนในการเปิดและจัดการโครงสร้างการแบ่งงานโครงการ
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 8ef34bc984510f23ab77cc1710c06abbcf80f721703685d696fea28eeaddd732
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988044"
---
# <a name="microsoft-project-client-integration"></a>การรวม Microsoft Project Client

[!include [banner](../includes/banner.md)]

การวางแผนและการดูแลกำหนดการโครงการอาจมีความซับซ้อน ดังนั้นผู้จัดการโครงการจึงจำเป็นต้องใช้เครื่องมือที่ช่วยจัดการงานนี้ การรวมกับ Microsoft Project Client ให้การสนับสนุนในการเปิดและจัดการโครงสร้างการแบ่งงานโครงการ ผู้จัดการโครงการสามารถเผยแพร่การเปลี่ยนแปลงใดๆ กลับไปที่โครงสร้างการแบ่งงานโครงการของ Dynamics 365 Finance

> [!NOTE]
> หากคุณใช้การอัปเดตเดือนกรกฎาคม (เวอร์ชัน 10.0.4) คุณต้องติดตั้ง KB 4054797 และ 4055884

## <a name="configure-the-microsoft-project-client-add-in"></a>กำหนดค่า Add-in ของ Microsoft Project Client
ในการเปิดใช้งานการรวมกับ Microsoft Project Client จำเป็นต้องติดตั้ง Add-in Microsoft Dynamics 365 ในแอปพลิเคชัน Microsoft Project ไคลเอ็นต์ของผู้ใช้ ทำได้โดยการเปิด **พื้นที่ทำงานการจัดการโครงการ**

•   คลิก **กำหนดค่า Add-in ไคลเอนต์โครงการ** จากส่วน **ลิงก์** > **ติดตั้ง** ของพื้นที่ทำงาน

•   คลิก **เปิด** จากนั้นคลิก **เรียกใช้** เมื่อได้รับแจ้ง

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>เปิดและแก้ไขโครงสร้างการแบ่งงานแบบร่างที่มีอยู่ใน Microsoft Project Client
หากโครงการใน Dynamics 365 Finance มีโครงสร้างการแบ่งงานที่สร้างขึ้นแล้ว โครงสร้างการแบ่งงานสามารถเปิดได้ในแอปพลิเคชัน Microsoft Project Client หากโครงสร้างการแบ่งงานอยู่ในสถานะแบบร่าง เพื่อเปิดจากหน้า **โครงการ** ให้คลิก **เปิดใน Microsoft Project** จากแท็บ **วางแผน** หน้านี้สามารถเปิดได้จากภายในแอปพลิเคชัน Microsoft Project Client โดยคลิก **เปิด** ในแท็บ **Microsoft Dynamics 365** เลือก **นิติบุคคล** และ **โครงการ** จากรายการ

> [!NOTE]
> หากคุณกำลังใช้ Internet Explorer เป็นเบราว์เซอร์ของคุณ คุณจะต้องคลิก **บันทึก** เพื่อเปิดจากตำแหน่งที่ดาวน์โหลดไฟล์ไปด้วยตนเอง หรือคลิก **บันทึกและเปิด** เพื่อเปิดไฟล์ใน Microsoft Project Client อย่าเปลี่ยนชื่อไฟล์เมื่อทำการบันทึก

ก่อนทำการแก้ไขไฟล์โดยใช้ Microsoft Project Client คุณต้องตรวจสอบก่อน คลิก **เช็คเอาท์** ในแท็บ **Microsoft Dynamics 365** วิธีนี้จะป้องกันไม่ให้ผู้ใช้รายอื่นแก้ไขโครงสร้างการแบ่งงานจากภายใน Finance ในเวลาเดียวกัน หากต้องการเผยแพร่โครงสร้างการแบ่งงานหลังจากแก้ไขเสร็จแล้ว ให้คลิก **เช็คอิน** บนแท็บ **Microsoft Dynamics 365**

หากเพิ่มทีมโครงการลงในโครงการใน Finance แล้วรายการทรัพยากรจะถูกเติมด้วยสมาชิกในทีม หากยังไม่ได้เพิ่มทีมโครงการลงในโครงการ คุณสามารถเลือกทรัพยากรและสร้างทีมภายใน Microsoft Project Client โดยคลิกที่ปุ่ม **ทรัพยากร** บนแท็บ **Microsoft Dynamics 365** 

ข้อมูลต่อไปนี้จะซิงค์กลับไปที่ Finance โดยเป็นส่วนหนึ่งของกระบวนการเช็คอิน:

•   ชื่องาน

•   วันที่เริ่ม

•   วันที่เสร็จสิ้น

•   งานที่ต้องทำก่อน

•   ชื่อทรัพยากร

•   ประเภท

•   ประเภททรัพยากร

•   ชั่วโมงทำงาน:

•   บันทึกย่อ

•   ลำดับความสำคัญ

> [!NOTE]
> หากคุณเพิ่มคอลัมน์อื่นๆ ลงในไฟล์ Microsoft Project Client ของคุณ คอลัมน์เหล่านี้จะไม่ถูกบันทึกลงในไฟล์และจะไม่แสดงเมื่อเปิดไฟล์อีกครั้ง

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>สร้างโครงสร้างการแบ่งงานสำหรับโครงการที่มีอยู่ โดยใช้ Microsoft Project Client
หากต้องการสร้างโครงสร้างการแบ่งงานโดยใช้ Microsoft Project Client ให้ทำตามขั้นตอนเหล่านี้:


1.  เปิด Microsoft Project Client

2.  บนแท็บ **Microsoft Dynamics 365** ให้คลิก **เปิด**

3.  เลือก **นิติบุคคล** สำหรับโครงการ

4.  เลือก **โครงการ**

5.  คลิก **เช็คเอาท์** บนแท็บ **Microsoft Dynamics 365**

6.  เมื่อพร้อมเผยแพร่ไปยัง Finance คลิก **เช็คอิน** บนแท็บ **Microsoft Dynamics 365**

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>แทนที่โครงสร้างการแบ่งงานสำหรับโครงการที่มีอยู่ โดยใช้ Microsoft Project Client
เมื่อต้องการสร้างโครงสร้างการแบ่งงานใหม่โดยใช้ Microsoft Project Client และแทนที่โครงสร้างการแบ่งงานที่มีอยู่สำหรับโครงการที่มีอยู่ ให้ทำตามขั้นตอนเหล่านี้:

1.  เปิด Microsoft Project Client

2.  สร้างกำหนดการใน Microsoft Project Client

3.  บนแท็บ **Microsoft Dynamics 365** คลิก **บันทึกการเปลี่ยนแปลง** > **แทนที่โครงการที่มีอยู่**

4.  เลือก **นิติบุคคล** สำหรับโครงการ

5.  เลือก **โครงการ**

6.  คลิก **ตกลง**

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>สร้างโครงการใหม่จากภายใน Microsoft Project Client


1.  เปิด Microsoft Project Client

2.  สร้างกำหนดการใน Microsoft Project Client

3.  บนแท็บ **Microsoft Dynamics 365** คลิก **บันทึกการเปลี่ยนแปลง** > **บันทึกเป็นโครงการใหม่**

4.  เลือก **นิติบุคคล** สำหรับโครงการ

5.  ป้อน **รหัสโครงการ** ในกรณีที่จำเป็น

6.  ป้อน **ชื่อโครงการ**

7.  เลือก **ประเภทโครงการ** **กลุ่มโครงการ** และ **รหัสสัญญาโครงการ** หรือคุณสามารถสร้างสัญญาโครงการใหม่ได้โดยคลิก **ใหม่**

8.  เลือก **ปฏิทิน** เพื่อใช้ในการจัดหาทรัพยากร

11. คลิก **ตกลง**

> [!NOTE]
> Add-in ของไคลเอ็นต์ Project ไม่สนับสนุนอักขระต่อไปนี้ในรูปแบบรหัสโครงการ:
> 
>   - ขีดล่าง
>   - รอบระยะเวลา
>   - สเปซ
>   - เครื่องหมายทับ

[!INCLUDE[footer-include](../includes/footer-banner.md)]
