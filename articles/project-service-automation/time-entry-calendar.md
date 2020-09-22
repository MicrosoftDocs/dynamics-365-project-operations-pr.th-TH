---
title: ปฏิทินรายการเวลา
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ปฏิทินรายการเวลา
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: cc78d9ae-9f1b-4bd4-8cdf-41406f859ff7
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ea8c5113b9ba89e2255218e6a53f062c25badc98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756467"
---
# <a name="time-entry-calendar"></a><span data-ttu-id="62f89-103">ปฏิทินรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="62f89-103">Time entry calendar</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="62f89-104">ในเพจ **รายการเวลา** คุณสามารถดูรายการเวลาในปฏิทินโดยการเลือก **แสดงเป็น** \> **การควบคุมปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="62f89-104">On the **Time Entries** page, you can view the time entries on the calendar by selecting **Show as** \> **Calendar Control**.</span></span>

## <a name="updated-calendar-control"></a><span data-ttu-id="62f89-105">การควบคุมปฏิทินที่ปรับปรุงแล้ว</span><span class="sxs-lookup"><span data-stu-id="62f89-105">Updated calendar control</span></span>

<span data-ttu-id="62f89-106">Dynamics 365 Project Service Automation นำเสนอประสบการณ์รายการเวลาที่ใหม่และยืดหยุ่นได้</span><span class="sxs-lookup"><span data-stu-id="62f89-106">Dynamics 365 Project Service Automation offers a new and extensible time entry experience.</span></span> <span data-ttu-id="62f89-107">ประสบการณ์ใหม่นี้จะแทนที่การควบคุมปฏิทินแบบกำหนดเองที่เคยใช้ในรุ่นก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="62f89-107">This new experience replaces the Custom Calendar Control that was used in earlier versions.</span></span> <span data-ttu-id="62f89-108">อย่างไรก็ตาม คุณยังสามารถดูรายการเวลาผ่านการควบคุมปฏิทินแบบอ่านอย่างเดียวที่เฟรมเวิร์กส่วนติดต่อแบบรวมมีให้สำหรับมุมมอง รายวัน รายสัปดาห์ หรือรายเดือน</span><span class="sxs-lookup"><span data-stu-id="62f89-108">However, you can still view time entries through a read-only calendar control that the Unified Interface Framework provides for daily, weekly, or monthly views.</span></span>

<span data-ttu-id="62f89-109">ปฏิทินไม่สนับสนุนการดำเนินการบนแต่ละรายการปฏิทิน และคุณไม่สามารถเลือกหนึ่งรายการปฏิทินหรือมากกว่าสำหรับการส่งหรือการลบได้</span><span class="sxs-lookup"><span data-stu-id="62f89-109">The calendar doesn't support actions on individual calendar items, and you can't select one or more calendar items for submission or deletion.</span></span> <span data-ttu-id="62f89-110">ให้เลือกรายการปฏิทินเพื่อเปิดเพจเอนทิตี้ **รายการเวลา** ที่คุณสามารถดำเนินการที่จำเป็นให้แล้วเสร็จแทน</span><span class="sxs-lookup"><span data-stu-id="62f89-110">Instead, select a calendar item to open the **Time Entry** entity page, where you can complete the required actions.</span></span>

## <a name="extensibility"></a><span data-ttu-id="62f89-111">ความสามารถในการเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="62f89-111">Extensibility</span></span>

<span data-ttu-id="62f89-112">ในเพจ **รายการเวลา** ที่มีกริดรายการเวลา คุณสามารถเพิ่มฟิลด์แบบกำหนดเอง ตั้งค่าการค้นหาฟิลด์ หรือสร้างมุมมองแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="62f89-112">On the **Time Entries** page that has the time entry grid, you can add custom fields, set up lookup fields, and create custom views.</span></span> <span data-ttu-id="62f89-113">คุณยังสามารถตั้งค่าตรรกะธุรกิจแบบกำหนดเองที่อิงตามค่าที่คุณเลือกหรือป้อนในฟิลด์แบบกำหนดเองได้</span><span class="sxs-lookup"><span data-stu-id="62f89-113">You can also set up custom business logic that is based on the values that are selected or entered in custom fields.</span></span>
