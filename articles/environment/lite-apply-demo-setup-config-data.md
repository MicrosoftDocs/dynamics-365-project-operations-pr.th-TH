---
title: ใช้การตั้งค่าสาธิตและข้อมูลการกำหนดค่า - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีใช้การตั้งค่าการสาธิตและข้อมูลการกำหนดค่าสำหรับ Project Operations
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997174"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>ใช้การตั้งค่าสาธิตและข้อมูลการกำหนดค่าสำหรับ Project Operations - Lite 

_**การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มการกำหนดค่า คุณต้องมีสภาพแวดล้อม Common Data Service (CDS) ที่จัดเตรียมไว้สำหรับ Dynamics 365 Project Operations


## <a name="instructions"></a>คำแนะนำ

1. ดาวน์โหลด [แพคเกจข้อมูลหลัก](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip) 
2. นำทางไปยังโฟลเดอร์ *ProjOpsSampleSetupData - CE เท่านั้น CMT* และเรียกใช้ไฟล์ปฏิบัติการ *DataMigrationUtility*
3. ในเพจ 1 ของวิซาร์ดการย้ายการกำหนดค่า Common Data Service (CMT) เลือก **นำเข้าข้อมูล** แล้วเลือก **ดำเนินการต่อ**

    ![การโอนย้ายการตั้งค่าคอนฟิก](./media/1ConfigurationMigration.png)

4. ในเพจ 2 ของวิซาร์ด CMT ให้เลือก **Microsoft 365** เป็น **ชนิดการปรับใช้งาน**
5. เลือกกล่องกาเครื่องหมาย **แสดงรายชื่อขององค์กรที่มีอยู่** และ **แสดงขั้นสูง**
6. เลือกภูมิภาคของผู้เช่าของคุณ ป้อนข้อมูลประจำตัวของคุณ จากนั้นเลือก **เข้าสู่ระบบ**

   ![การลงชื่อเข้าใช้การกำหนดค่า](./media/2ConfigurationSignin.png)

7. ในเพจ 3 จากรายชื่อองค์กรในผู้เช่า ให้เลือกองค์กรที่คุณต้องการนำเข้าข้อมูลสาธิต จากนั้นเลือก **เข้าสู่ระบบ**
8. ในหน้า 4 เลือกไฟล์ zip *SampleSetupAndConfigData* จากโฟลเดอร์ที่ขยาย *ProjOpsSampleSetupData - CMT เฉพาะ CE*

   ![ไฟล์ Zip](./media/3ZipFile.png)

   ![เลือกไฟล์](./media/4SelectAFile.png)

9. หลังจากเลือกไฟล์ zip แล้ว ให้เลือก **นำเข้าข้อมูล**

   ![การนำเข้าข้อมูล](./media/5ImportData.png)

10. การนำเข้าจะทำงานประมาณสองถึงสิบนาที ขึ้นอยู่กับความเร็วเครือข่ายของคุณ หลังจากเสร็จสิ้น ให้ออกจากวิซาร์ด CMT 
11. ตรวจสอบองค์กรของคุณสำหรับข้อมูลใน 18 เอนทิตีต่อไปนี้:

    -   สกุลเงิน
    -   บัญชี
    -   หน่วยองค์กร
    -   ผู้ติดต่อ
    -   หน่วย
    -   กลุ่มของหน่วย
    -   รายการราคา
    -   รายการราคาสำหรับพารามิเตอร์โครงการ 
    -   ความถี่ของใบแจ้งหนี้
    -   ประเภททรัพยากรที่สามารถจองได้
    -   ประเภทธุรกรรม
    -   ประเภทค่าใช้จ่าย
    -   ราคาตามบทบาท
    -   ราคาของประเภทธุรกรรม
    -   คุณลักษณะ
    -   ทรัพยากรที่สามารถจองได้
    -   การกำหนดประเภททรัพยากรที่สามารถจองได้
    -   คุณลักษณะทรัพยากรที่สามารถจองได้

    ![การนำเข้าเสร็จสมบูรณ์](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
