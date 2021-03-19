---
title: สร้างการมอบหมายทรัพยากร
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการสร้างการมอบหมายทรัพยากรทั่วไปและที่ระบุชื่อ
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a6f4f12a962cb570e8b83d8ee7a01fc0cc2c6155
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287126"
---
# <a name="create-resource-assignments"></a><span data-ttu-id="0b721-103">สร้างการมอบหมายทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="0b721-103">Create resource assignments</span></span>

<span data-ttu-id="0b721-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="0b721-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="0b721-105">การมอบหมายทรัพยากรเป็นการเชื่อมโยงโดยตรงของสมาชิกทีมโครงการกับงานโหนดปลายสุด</span><span class="sxs-lookup"><span data-stu-id="0b721-105">A resource assignment is the direct association of a project team member to a leaf node task.</span></span> <span data-ttu-id="0b721-106">หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการมอบหมายทรัพยากรในลักษณะต่างๆ</span><span class="sxs-lookup"><span data-stu-id="0b721-106">This topic provides information about the different ways to assign resources.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="0b721-107">สร้างสมาชิกทีมทั่วไปผ่านการมอบหมายงาน</span><span class="sxs-lookup"><span data-stu-id="0b721-107">Create a generic team member through task assignment</span></span>


<span data-ttu-id="0b721-108">เมื่อคุณสร้างสมาชิกทีมทั่วไปผ่านการมอบหมาย คุณจะสร้างตัวยึดตำแหน่งหรือทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="0b721-108">When you create a generic team member through task assignment, you create a placeholder or generic resource.</span></span> <span data-ttu-id="0b721-109">ทรัพยากรทั่วไปนี้อธิบายลักษณะของทรัพยากรที่มีชื่อที่คุณต้องการทำงานในตอนท้าย</span><span class="sxs-lookup"><span data-stu-id="0b721-109">This generic resource describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="0b721-110">จากนั้น คุณสร้างความต้องการ หรือส่งการร้องขอโดยใช้ความต้องการที่ใช้ในการค้นหา และจองทรัพยากรที่ระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="0b721-110">You then generate a requirement, or submit a request using the requirement, that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="0b721-111">บนตาราง กำหนดการ สำหรับงาน เลือกไอคอน ทรัพยากร ในเซลล์ **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="0b721-111">On the Schedule grid for a task, select the Resource icon in the **Resource** cell.</span></span>
2. <span data-ttu-id="0b721-112">พิมพ์ชื่อที่จะใช้เป็นชื่อของทรัพยากรตัวยึด</span><span class="sxs-lookup"><span data-stu-id="0b721-112">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="0b721-113">ตัวอย่างเช่น Program Manager</span><span class="sxs-lookup"><span data-stu-id="0b721-113">For example, Program Manager.</span></span>
3. <span data-ttu-id="0b721-114">เลือก **สร้าง** และในฟิลด์ **การสร้างสมาชิกทีมโครงการแบบด่วน** กำหนดบทบาทสำหรับทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="0b721-114">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>
4. <span data-ttu-id="0b721-115">มอบหมายงานตามที่จำเป็นให้กับทรัพยากรตัวยึดนี้ โดยการเลือกทรัพยากรใน **ตัวเลือกทรัพยากร** สำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="0b721-115">Assign tasks as needed to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="0b721-116">ทรัพยากรมีการแสดงไว้ภายใต้ **สมาชิกทีม**</span><span class="sxs-lookup"><span data-stu-id="0b721-116">The resources listed under **Team Members**.</span></span>
5. <span data-ttu-id="0b721-117">เมื่อคุณเสร็จสิ้นการมอบหมายทรัพยากรทั่วไป เลือกทรัพยากรทั่วไปบนแท็บ **ทีม** เลือกทรัพยากรทั่วไป และเลือก **สร้างความต้องการ** เพื่อสร้างความต้องการทรัพยากรสำหรับทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="0b721-117">When you’re finished assigning the generic resource, on the **Team** tab, select the generic resource, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>
6. <span data-ttu-id="0b721-118">เลือก **จอง** สำหรับทรัพยากรทั่วไป และจากนั้น ใช้ตารางกำหนดการเพื่อค้นหาและจองทรัพยากรจริงได้</span><span class="sxs-lookup"><span data-stu-id="0b721-118">Select **Book** for the generic resource and then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="0b721-119">นอกจากนี้ คุณยังสามารถส่งความต้องการสำหรับการบรรลุเป้าหมายโดยผู้จัดการทรัพยากรได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="0b721-119">You can also submit the requirement for fulfillment by a resource manager.</span></span>
7. <span data-ttu-id="0b721-120">เมื่อมีการเติมเต็มทรัพยากรทั่วไปอย่างสมบูรณ์ (การเติมเต็มความต้องการทรัพยากรบางส่วนจะไม่ส่งผลให้มีการมอบหมายทรัพยากร) ด้วยทรัพยากรที่ระบุชื่อ ทรัพยากรทั่วไปจะถูกลบออกจากทีม</span><span class="sxs-lookup"><span data-stu-id="0b721-120">When the generic resource is fully fulfilled (partial resource requirement fulfillment will not result in a resource assignment) with a named resource, the generic resource is removed from the team.</span></span> <span data-ttu-id="0b721-121">การมอบหมายงานสำหรับทรัพยากรทั่วไปจะมีการมอบหมายให้กับทรัพยากรที่ระบุชื่อที่ตรงตามความต้องการทรัพยากรของทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="0b721-121">The task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="0b721-122">การมอบหมายทรัพยากรที่ระบุชื่อจากรายการของทรัพยากรที่จองได้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0b721-122">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="0b721-123">คุณสามารถใช้กล่องค้นหาใน **ตัวเลือกทรัพยากร** เพื่อค้นหาทรัพยากรที่จองได้ที่ใช้งานอยู่ทั้งหมดและมอบหมายให้กับงานโหนดปลายสุด</span><span class="sxs-lookup"><span data-stu-id="0b721-123">You can use the search box in the **Resource Picker** to search all active bookable resources and assign them to any leaf node task.</span></span> <span data-ttu-id="0b721-124">ทรัพยากรที่ถูกมอบหมายด้วยวิธีนี้ จะถูกเพิ่มเข้าไปในทีมโดยไม่ต้องทำการจองใด ๆ</span><span class="sxs-lookup"><span data-stu-id="0b721-124">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="0b721-125">คล้ายกับการเพิ่มสมาชิกในทีมและเลือก **ไม่มี** เป็นวิธีการจัดสรร</span><span class="sxs-lookup"><span data-stu-id="0b721-125">This is similar to adding a team member and selecting **None** as the allocation method.</span></span> <span data-ttu-id="0b721-126">ทรัพยากรนั้นถูกแสดงในแท็บ **ทีม**, **การมอบหมายทรัพยากร** และ **การกระทบยอด** เป็นทรัพยากรที่มีการมอบหมายเท่านั้นและการจองที่ขาด</span><span class="sxs-lookup"><span data-stu-id="0b721-126">The resource is displayed on the **Team**, **Resource Assignment**, and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="0b721-127">จองรายการเหล่านี้ ถ้าคุณต้องการใช้ความพร้อมใช้งานของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="0b721-127">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="0b721-128">จากตารางงาน ตารางหรือเส้นเวลา ไปที่เซลล์ **มอบหมายให้**</span><span class="sxs-lookup"><span data-stu-id="0b721-128">From the task grid, board, or timeline, navigate to the **Assigned To** cell.</span></span>
2. <span data-ttu-id="0b721-129">เริ่มพิมพ์ชื่อในช่องค้นหา</span><span class="sxs-lookup"><span data-stu-id="0b721-129">In the search box, start typing a name.</span></span> <span data-ttu-id="0b721-130">ผลลัพธ์การค้นหาสำหรับชื่อที่แสดงใน **ตัวเลือกทรัพยากร** ภายใต้ **ทรัพยากรอื่น ๆ**</span><span class="sxs-lookup"><span data-stu-id="0b721-130">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>
3. <span data-ttu-id="0b721-131">เลือกทรัพยากรที่คุณต้องการมอบหมายให้กับงาน หรือเลือกชื่อของทรัพยากรภายใต้ **ทรัพยากรอื่นๆ ของทีม**</span><span class="sxs-lookup"><span data-stu-id="0b721-131">Select the resource that you want to assign to the task or select the name of the resource under **Other Team Resources**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]