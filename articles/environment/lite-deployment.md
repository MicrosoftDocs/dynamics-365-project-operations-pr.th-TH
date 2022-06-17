---
title: ปรับใช้งาน Project Operations - Lite
description: บทความนี้ให้ข้อมูลเกี่ยวกับวิธีการติดตั้งการปรับใช้งาน Project Operations แบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930341"
---
# <a name="deploy-project-operations---lite"></a>ปรับใช้งาน Project Operations - Lite

_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_



Project Operations รองรับรูปแบบการปรับใช้งานหลายแบบ หากต้องการกำหนดรูปแบบการปรับใช้งานที่ดีที่สุด โปรดดู [ชนิดการปรับใช้งาน](determine-deployment-type.md)


> [!IMPORTANT]
> การปรับใช้งานนี้ การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราวส่งผลในการปรับใช้งานเฉพาะ **Dataverse ของ Project Operations**

- [ติดตั้ง Project Operations ในสภาพแวดล้อม Dataverse ใหม่](#new)
- [ติดตั้งในสภาพแวดล้อม Dataverse ที่มีอยู่](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>ติดตั้ง Project Operations ในสภาพแวดล้อม Dataverse ใหม่

1. ในฐานะ [ผู้ดูแลระบบส่วนกลางหรือผู้ดูแลระบบ Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) ที่มีสิทธิ์การใช้งาน Project Operations ให้สร้างสภาพแวดล้อม Dataverse ใหม่ใน [ศูนย์จัดการ PowerPlatform](https://admin.powerplatform.com) ทำให้แน่ใจว่า **สร้างฐานข้อมูลสำหรับสภาพแวดล้อมนี้** และ **แอป Dynamics 365** เปิดใช้งานอยู่ สำหรับข้อมูลเพิ่มเติม ดูที่ [สร้างและจัดการสภาพแวดล้อมในศูนย์จัดการ Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center)
2. เลือก **Microsoft Dynamics 365 Project Operations** จากรายการการปรับใช้แอป Dynamics 365


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>ติดตั้ง Project Operations ในสภาพแวดล้อม Dataverse ที่มีอยู่
1. ตรวจสอบให้แน่ใจว่าไม่ได้กำหนดค่าสภาพแวดล้อมด้วย [การรวมแบบสองทิศทาง](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) เนื่องจากการติดตั้งจะติดตั้งความสามารถของ [Project Operations สำหรับสถานการณ์ตามทรัพยากร/ไม่ได้เก็บในคลัง](project-operations-integrated-deployment-overview.md)
2. ในฐานะ [ผู้ดูแลระบบส่วนกลางหรือผู้ดูแลระบบ Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) ที่มีสิทธิ์การใช้งาน Project Operations ให้ค้นหาสภาพแวดล้อมใน [ศูนย์จัดการ Power Platform](https://admin.powerplatform.com) ที่คุณต้องการติดตั้ง Project Operations
3. ติดตั้ง **Microsoft Dynamics 365 Project Operations** จากรายการการปรับใช้แอป Dynamics 365 สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [จัดการแอป Dynamics Dynamics 365](/power-platform/admin/manage-apps)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
