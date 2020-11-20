---
title: ปรับใช้งาน Project Operations - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการติดตั้งการปรับใช้งาน Project Operations Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0633585fcef91d9218d6140764addb7cf96ab31d
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175689"
---
# <a name="deploy-project-operations---lite"></a>ปรับใช้งาน Project Operations - Lite

_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

Project Operations รองรับรูปแบบการปรับใช้งานหลายแบบ หากต้องการกำหนดรูปแบบการปรับใช้งานที่ดีที่สุด โปรดดู [ชนิดการปรับใช้งาน](determine-deployment-type.md)


> [!IMPORTANT]
> การปรับใช้งานนี้ การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราวส่งผลในการปรับใช้งานเฉพาะ **Common Data Service ของ Project Operations**

- [ติดตั้ง Project Operations ในสภาพแวดล้อม CDS ใหม่](#new)
- [ติดตั้งในสภาพแวดล้อม CDS ที่มีอยู่](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>ติดตั้ง Project Operations ในสภาพแวดล้อม CDS ใหม่

1. ในฐานะ [ผู้ดูแลระบบส่วนกลางหรือผู้ดูแลระบบ Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) ที่มีสิทธิ์การใช้งาน Project Operations ให้สร้างสภาพแวดล้อม CDS ใหม่ใน [ศูนย์จัดการ Power Platform](https://admin.powerplatform.com) ทำให้แน่ใจว่า **ฐานข้อมูล CDS** และ **แอป Dynamics 365** ถูกเปิดใช้งาน สำหรับข้อมูลเพิ่มเติม ดูที่ [สร้างและจัดการสภาพแวดล้อมในศูนย์จัดการ Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center)
2. เลือก **Microsoft Dynamics 365 Project Operations** จากรายการปรับใช้งานแอป Dynamics 365


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>ติดตั้ง Project Operations ในสภาพแวดล้อม CDS ที่มีอยู่

1. ในฐานะ [ผู้ดูแลระบบส่วนกลางหรือผู้ดูแลระบบ Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) ที่มีสิทธิ์การใช้งาน Project Operations ให้ค้นหาสภาพแวดล้อมใน [ศูนย์จัดการ Power Platform](https://admin.powerplatform.com) ที่คุณต้องการติดตั้ง Project Operations
2. ติดตั้ง **Microsoft Dynamics 365 Project Operations** จากรายการปรับใช้งานแอป Dynamics 365 สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [จัดการแอป Dynamics Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps)


