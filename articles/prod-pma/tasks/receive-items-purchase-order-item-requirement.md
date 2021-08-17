---
title: รับสินค้าในใบสั่งซื้อจากความต้องการสินค้า
description: หัวข้อนี้อธิบายวิธีการรับสินค้าในใบสั่งซื้อจากความต้องการสินค้า
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: da5eff576040f20cc206800b4d4ca987d08b0185ec5364bc1efc940f85d36371
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998979"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>รับสินค้าในใบสั่งซื้อจากความต้องการสินค้า

[!include [banner](../../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการรับสินค้าในใบสั่งซื้อจากความต้องการสินค้า

ด้วยการใช้ความต้องการสินค้าแทนธุรกรรมสินค้า คุณสามารถวางแผนการจัดส่งก่อนที่สินค้าจะถูกใช้จริง สร้างใบสั่งซื้อ รวมสินค้าในกรอบเวลาของข้อตกลงทางการค้า และรวมความต้องการสินค้าในการวางแผนการผลิต 

งานนี้ใช้ชุดข้อมูล USSI

1. ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > โครงการ > โครงการทั้งหมด**
2. ในรายการ ให้เลือกลิงค์ในแถวที่ต้องการ
3. ในบานหน้าต่างการดำเนินการ เลือก **วางแผน**
4. เลือก **ความต้องการสินค้า**
5. เลือก **สร้าง**
6. ในแถวใหม่ ให้ป้อนหรือเลือกค่าในฟิลด์ **หมายเลขสินค้า**
7. ในฟิลด์ **ปริมาณ** ป้อนตัวเลข
8. เลือก **บันทึก**
9. ในบานหน้าต่างการดำเนินการ เลือก **จัดการ**
10. เลือก **ฟังก์ชัน**
11. เลือก **สร้างใบสั่งซื้อ**
12. เลือกกล่องกาเครื่องหมาย **รวมทั้งหมด**
13. ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ป้อนหรือเลือกค่า
14. เลือก **ตกลง**
15. ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด**
16. ในรายการ ให้เลือกลิงค์ในแถวที่ต้องการ
17. ในบานหน้าต่างการดำเนินการ เลือก **ซื้อ**
18. เลือก **ยืนยัน**
19. ในบานหน้าต่างการดำเนินการ เลือก **รับ**
20. เลือก **ใบรับสินค้า**
21. ใน **ใบรับสินค้า** พิมพ์ค่า
22. เลือก **ตกลง**



[!INCLUDE[footer-include](../../includes/footer-banner.md)]