---
title: ลงทะเบียนการสมัครใช้งานรุ่นพรีวิวของ Project Operations สำหรับสถานการณ์ทรัพยากร/ไม่ได้เก็บในคลัง
description: บทความนี้ให้ข้อมูลเกี่ยวกับวิธีการสมัครใช้งานและปรับใช้ Project Operations สำหรับสถานการณ์ตามทรัพยากร/ไม่ได้เก็บในคลัง
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fb196a50b4cb9e8533db52414e8536d77a30e425
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920129"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>ลงทะเบียนการสมัครใช้งานรุ่นพรีวิวของ Project Operations สำหรับสถานการณ์ทรัพยากร/ไม่ได้เก็บในคลัง

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ทรัพยากร/ไม่ได้เก็บในคลัง_



บทความนี้อธิบายวิธีการสมัครใช้งานข้อเสนอการทดลองใช้และปรับใช้สภาพแวดล้อม Project Operations สำหรับสถานการณ์ตามทรัพยากร/ไม่ได้เก็บในคลัง

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น
- ผู้ใช้ที่ปรับใช้งานรุ่นพรีวิวต้องมีสิทธิ์ของผู้ดูแลระบบส่วนกลางของลูกค้า Azure คุณสามารถสร้างผู้เช่าได้ในระหว่างการแลกรับข้อเสนอครั้งแรก 
- การปรับใช้งานสภาพแวดล้อม Finance จำเป็นต้องมีการสมัครใช้งาน Azure ที่ถูกต้อง ซึ่งจะมีการเรียกเก็บเงินตามสภาพแวดล้อม คุณสามารถใช้การสมัครใช้งานที่มีอยู่ขององค์กรหรือใช้ [การทดลองใช้ Azure](https://azure.microsoft.com/free/) เพื่อเริ่มต้นใช้งาน สภาพแวดล้อม CDS จะให้บริการฟรีเป็นเวลา 30 วัน

> [!IMPORTANT]
> มีเพียงคนเดียวคือ ผู้เช่าที่เป็นผู้ดูแลระบบ ในองค์กรเท่านั้นที่ต้องทำงานนี้ หากคุณไม่ใช่สมาชิกของรุ่นนี้ ให้รอจนกว่าองค์กรของคุณจะลงทะเบียนและคุณได้รับข้อมูลประจำตัวของผู้ใช้ของคุณ
> 
> รุ่นทดลองใช้เป็นแบบใช้ครั้งเดียวในผู้เช่า คุณสามารถเรียกใช้รุ่นทดลองใช้เพียงครั้งเดียวเท่านั้น เราขอแนะนำให้คุณสร้างผู้เช่าใหม่เพื่อวัตถุประสงค์ในรุ่นทดลองใช้งาน


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - รุ่นทดลองใช้งานตัวอย่าง 

ก่อนที่คุณจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณได้ลงชื่อเข้าใช้เบราว์เซอร์ด้วยบัญชีงานของผู้ใช้ในผู้เช่าที่คุณต้องการดูตัวอย่าง Project Operations

1. แลกรหัสข้อเสนอแรก **Dynamics 365 Project Operations** ที่นี่ [รุ่นทดลองใช้Project Operations](https://aka.ms/try-po)
2. ยืนยันใบสั่งของคุณ

  คุณจะเห็นข้อเสนอยืนยันแลกสำเร็จแล้ว

### <a name="dynamics-365-finance-preview-trial"></a>การทดลองใช้ Dynamics 365 Finance รุ่นพรีวิว

ไปที่ [รุ่นทดลองใช้งานตัวอย่าง Dynamics 365 for Finance](https://aka.ms/trypoche) และทำซ้ำขั้นตอนจากส่วนก่อนหน้าด้วยข้อเสนอ ลงชื่อสมัครใช้สภาพแวดล้อมที่เป็นโฮสต์บนระบบคลาวด์  

## <a name="assign-licenses"></a>มอบหมายสิทธิ์การใช้งาน

> [!IMPORTANT]
> คุณจะต้องมีสิทธิ์การเข้าถึงระดับผู้ดูแลระบบสำหรับพอร์ทัล Microsoft 365 ขององค์กรของคุณเพื่อทำตามขั้นตอนต่อไปนี้

1. ไปที่ [ศูนย์การจัดการ Microsoft 365](https://portal.office.com/) เพื่อกำหนดสิทธิ์การใช้งานให้กับผู้ใช้ของคุณ

2. บนเพจ **ผู้ใช้ที่ใช้งานอยู่** เลือกผู้ใช้ที่คุณต้องการมอบหมายสิทธิ์การใช้งาน

3. ตรวจสอบว่าเลือกสิทธิ์การใช้งาน **Dynamics 365 Project Operations** และเลือก **บันทึกการเปลี่ยนแปลง**

> [!NOTE]
> ข้อเสนอการทดลองใช้ Finance ไม่จำเป็นต้องมอบหมายให้กับผู้ใช้

## <a name="start-a-new-project-in-lcs"></a>เริ่มต้นโครงการใหม่ใน LCS

สร้างโครงการ LCS ใหม่ตามที่อธิบายไว้ในบทความ [เริ่มโครงการใหม่ใน LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>เพิ่มการสมัครใช้งาน Azure ไปยังโครงการ LCS

เพื่อให้งานนี้เสร็จสมบูรณ์ ให้ทำตามขั้นตอนในบทความ [เพิ่มการสมัครใช้งาน Azure ไปยังโครงการ LCS](resource-add-azure-subscription-lcs-project.md)

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>ปรับใช้งานสภาพแวดล้อมสาธิต Finance ด้วย Project Operations สำหรับสถานการณ์ทรัพยากร/ไม่ได้เก็บในคลัง

ทำตามคำแนะนำในบทความ [จัดเตรียมสภาพแวดล้อมใหม่](resource-provision-new-environment.md) เพื่อดำเนินการปรับใช้ให้เสร็จสิ้น ใช้ชนิดการปรับใช้งาน [สภาพแวดล้อมสาธิต](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) สำหรับพรีวิว 

## <a name="install-cds-setup-and-configuration-data"></a>ติดตั้งโปรแกรมตั้งค่า CDS และข้อมูลการกำหนดค่า

ติดตั้งข้อมูลการตั้งค่าและการกำหนดค่า CDS ตามที่อธิบายไว้ในบทความ [ตั้งค่าและใช้ข้อมูลการกำหนดค่าใน Common Data Service](resource-apply-pro-setup-config-data.md)
ทำตามขั้นตอนนี้หลังจากปรับใช้สภาพแวดล้อมสาธิตทางการเงินและข้อมูลสาธิตพร้อมแล้วเท่านั้น


[!INCLUDE[footer-include](../includes/footer-banner.md)]
