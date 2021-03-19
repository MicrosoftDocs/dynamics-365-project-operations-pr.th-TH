---
title: จองคำขอแบบไม่ตายตัว
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการจองคำขอแบบไม่ตายตัว
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 736d59976ad0f456a694cedbb28b516c90632fe6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282941"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="8e0ee-103">จองคำขอแบบไม่ตายตัว</span><span class="sxs-lookup"><span data-stu-id="8e0ee-103">Soft-book requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8e0ee-104">คำขอทรัพยากรสามารถจองแบบตายตัวได้</span><span class="sxs-lookup"><span data-stu-id="8e0ee-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="8e0ee-105">การจองแบบตายตัวจะสร้างการประชุมข้อเสนอที่ใช้กำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8e0ee-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="8e0ee-106">การประชุมข้อเสนอจะถูกส่งกลับไปยังผู้ขอเพื่อการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="8e0ee-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="8e0ee-107">การจองแบบไม่ตายตัว จะเพิ่มทรัพยากรไปยังทีมของโครงการแบบไม่แน่นอน และมีสถานะที่แตกต่างในตารางกำหนดการ แต่จะไม่ใช้กำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8e0ee-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="8e0ee-108">หากต้องการจองทรัพยากรแบบไม่ตายตัวจากตารางกำหนดการ ให้ตั้งค่าฟิลด์ **สถานะการจอง** เป็น **ไม่ตายตัว**</span><span class="sxs-lookup"><span data-stu-id="8e0ee-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![สถานะการจองถูกตั้งค่าเป็นไม่ตายตัวแล้ว](media/Resource-Management-image77.png)

<span data-ttu-id="8e0ee-110">เมื่อแท็บ **ทีม** อยู่ในมุมมอง **สมาชิกทีมที่ตั้งชื่อ** ทรัพยากรจะปรากฏที่นี่</span><span class="sxs-lookup"><span data-stu-id="8e0ee-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="8e0ee-111">ชั่วโมงที่จองแบบไม่ตายตัวจะถูกรายงานในคอลัมน์ **ชั่วโมงที่จองแบบไม่ตายตัว**</span><span class="sxs-lookup"><span data-stu-id="8e0ee-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![ชั่วโมงที่ทำการจองแบบไม่ตายตัวอยู่ในมุมมองสมาชิกทีมที่ตั้งชื่อ](media/Resource-Management-image78.png)

<span data-ttu-id="8e0ee-113">สมาชิกทีมที่จองแบบไม่ตายตัวสามารถถูกมอบหมายงานให้สมาชิกได้</span><span class="sxs-lookup"><span data-stu-id="8e0ee-113">Soft-booked team members can be assigned to tasks.</span></span>

![สมาชิกทีมที่จองแบบไม่ตายตัวถูกมอบหมายงานให้](media/Resource-Management-image79.png)

<span data-ttu-id="8e0ee-115">ในแท็บ **การกระทบยอด** ไม่มีการจองที่แสดงสำหรับการจองทรัพยากรแบบไม่ตายตัว เนื่องจากแท็บ **การกระทบยอด** จะพิจารณาเฉพาะการจองแบบตายตัว</span><span class="sxs-lookup"><span data-stu-id="8e0ee-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![การจองทรัพยากรแบบไม่ตายตัว โดยไม่มีการจองในแท็บการกระทบยอด](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="8e0ee-117">คุณไม่สามารถจองทรัพยากรแบบไม่ตายตัวจากคำขอที่ถูกสร้างจากสมาชิกทีมทั่วไปได้</span><span class="sxs-lookup"><span data-stu-id="8e0ee-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="8e0ee-118">ในตารางกำหนดการ สีที่แตกต่างจะถูกใช้สำหรับการจองทรัพยากรแบบไม่ตายตัว</span><span class="sxs-lookup"><span data-stu-id="8e0ee-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![การจองแบบไม่ตายตัวในตารางกำหนดการ](media/Resource-Management-image81.png)

<span data-ttu-id="8e0ee-120">ในการแปลงจากการจองแบบไม่ตายตัวไปเป็นการจองแบบตายตัว ในตารางกำหนดการ ให้คลิกขวาที่การจองแบบไม่ตายตัว แล้วเลือก **เปลี่ยนสถานะ** \> **การจองแบบตายตัว** \> **แบบตายตัว**</span><span class="sxs-lookup"><span data-stu-id="8e0ee-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![เปลี่ยนสถานะการจองไปเป็นแบบตายตัว](media/Resource-Management-image82.png)

<span data-ttu-id="8e0ee-122">การจองถูกเปลี่ยนแปลงแล้ว และสถานะถูกเปลี่ยนในตารางกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="8e0ee-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="8e0ee-123">เนื่องจากสถานะการจองกลายเป็น **ตายตัว** แล้ว ทรัพยากรที่แสดงว่าจองแกล้ว และกำลังการผลิตและความพร้อมใช้งานถูกปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="8e0ee-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="8e0ee-124">คุณสามารถใช้วิธีเดียวกันในการยกเลิกการจองแบบตายตัวหรือแบบไม่ตายตัวจากตารางกำหนดการได้</span><span class="sxs-lookup"><span data-stu-id="8e0ee-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="8e0ee-125">ในการแปลงทรัพยากรที่ถูกจองแบบไม่ตายตัวไปยังแบบตายตัว ในแท็บ **ทีม** ของโครงการ เลือกทรัพยากร แล้วเลือก **ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="8e0ee-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![ยืนยันคำสั่ง](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]