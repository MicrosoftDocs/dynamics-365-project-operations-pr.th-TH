---
title: ปรับใช้งาน Project Operations แบบ Lite
description: บทความนี้ให้ข้อมูลเกี่ยวกับวิธีการติดตั้งการปรับใช้งาน Project Operations แบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811002"
---
# <a name="deploy-project-operations-lite"></a>ปรับใช้งาน Project Operations แบบ Lite

_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_



Project Operations รองรับรูปแบบการปรับใช้งานหลายแบบ หากต้องการกำหนดรูปแบบการปรับใช้งานที่ดีที่สุด โปรดดู [ชนิดการปรับใช้งาน](determine-deployment-type.md)


> [!IMPORTANT]
> การปรับใช้งานนี้ การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราวส่งผลในการปรับใช้งานเฉพาะ **Dataverse ของ Project Operations**

- [ติดตั้ง Project Operations ในสภาพแวดล้อม Dataverse ใหม่](#new)
- [ติดตั้งในสภาพแวดล้อม Dataverse ที่มีอยู่](#existing)
- [ติดตั้งในสภาพแวดล้อม Dataverse ที่มีอยู่ซึ่งมีส่วนประกอบการรวมแบบสองทิศทาง](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>ติดตั้ง Project Operations แบบLite ในสภาพแวดล้อม Dataverse ใหม่

1. ในฐานะ [ผู้ดูแลระบบส่วนกลางหรือผู้ดูแลระบบ Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) ที่มีสิทธิ์การใช้งาน Project Operations ให้สร้างสภาพแวดล้อม Dataverse ใหม่ใน [ศูนย์จัดการ PowerPlatform](https://admin.powerplatform.com) ทำให้แน่ใจว่า **สร้างฐานข้อมูลสำหรับสภาพแวดล้อมนี้** และ **แอป Dynamics 365** เปิดใช้งานอยู่ สำหรับข้อมูลเพิ่มเติม ดูที่ [สร้างและจัดการสภาพแวดล้อมในศูนย์จัดการ Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center)
1. เลือก **Microsoft Dynamics 365 Project Operations** จากรายการการปรับใช้แอป Dynamics 365


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>ติดตั้ง Project Operations แบบ Lite ในสภาพแวดล้อม Dataverse ที่มีอยู่ 
1. ในฐานะ [ผู้ดูแลระบบส่วนกลางหรือผู้ดูแลระบบ Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) ที่มีสิทธิ์การใช้งาน Project Operations ให้ค้นหาสภาพแวดล้อมใน [ศูนย์จัดการ Power Platform](https://admin.powerplatform.com) ที่คุณต้องการติดตั้ง Project Operations
1. ติดตั้ง **Microsoft Dynamics 365 Project Operations** จากรายการการปรับใช้แอป Dynamics 365 สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [จัดการแอป Dynamics Dynamics 365](/power-platform/admin/manage-apps)

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>ติดตั้ง Project Operations แบบ Lite ในสภาพแวดล้อม Dataverse ที่มีอยู่ซึ่งมีโซลูชันการรวมแบบสองทิศทางอยู่แล้ว

หากคุณต้องการรัเรียกใช้ Project Operations ต่อไปในโหมดการปรับใช้เวอร์ชัน Lite คุณควรทำตามขั้นตอนเหล่านี้:

1. ในฐานะ [ผู้ดูแลระบบส่วนกลางหรือผู้ดูแลระบบ Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) ที่มีสิทธิ์การใช้งาน Project Operations ให้ค้นหาสภาพแวดล้อมใน [ศูนย์จัดการ Power Platform](https://admin.powerplatform.com) ที่คุณต้องการติดตั้ง Project Operations
1. ติดตั้ง **Microsoft Dynamics 365 Project Operations** จากรายการการปรับใช้แอป Dynamics 365 สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [จัดการแอป Dynamics Dynamics 365](/power-platform/admin/manage-apps)
1. เนื่องจากสภาพแวดล้อมของคุณมีส่วนประกอบการรวมแบบสองทิศทางที่ช่วยในการรวมเข้ากับแอปการเงินและการดำเนินงานที่ติดตั้ง การติดตั้ง Project Operations จะติดตั้งความสามารถและส่วนขยายที่จำเป็นในการรวมข้อมูลที่เกี่ยวข้องกับโครงการเข้ากับแอปการเงินและการดำเนินงาน เนื่องจากคุณต้องการเรียกใช้ Project Operations ในการปรับใช้แบบ Lite จึงควรลบส่วนประกอบการรวมเหล่านี้ออก เนื่องจากจะสร้างข้อจำกัดและค่าใช้จ่ายสำหรับสถานการณ์การปรับใช้แบบ Lite ถอนการติดตั้งโซลูชัน **การรวมแบบสองทิศทางของ Dynamics 365 Project Operations** และ **แผนผังเอนทิตีการรวมแบบสองทิศทางของ Dynamics 365 Project Operations** ด้วยตนเองเพื่อลบส่วนประกอบเหล่านี้
1. ไปที่ **Project Operations -> การตั้งค่า -> พารามิเตอร์** เปิดหน้ารายละเอียด **พารามิเตอร์โครงการ** และตั้งค่าฟิลด์ **ลักษณะการทำงานการอัปเกรดโซลูชัน** เป็น **แบบ Lite เท่านั้น** ซึ่งทำให้มั่นใจได้ว่าการอัปเกรด Project Operations ที่ตามมาจะไม่นำส่วนประกอบการรวมกลับเข้าสู่ Project Operations  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
