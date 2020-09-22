---
title: คำถามที่ถามบ่อยเกี่ยวกับการจัดการทรัพยากร
description: หัวข้อนี้แสดงคำตอบของคำถามที่ถามบ่อยเกี่ยวกับการจัดการทรัพยากร
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: fdf7f1e2-e4a2-4c68-aa03-4a41c7b10531
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 87da759b3b30ed6d38866c045194cde79837c209
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756477"
---
# <a name="resource-management-faq"></a><span data-ttu-id="67547-103">คำถามที่ถามบ่อยเกี่ยวกับการจัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="67547-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="67547-104">ความแตกต่างระหว่างสมาชิกในทีมและความต้องการทรัพยากรคืออะไร</span><span class="sxs-lookup"><span data-stu-id="67547-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="67547-105">สมาชิกในทีมโครงการสามารถมอบหมายให้กับงานที่จองหรือที่จองเกินและตั้งค่าเป็นผู้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="67547-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="67547-106">ความต้องการทรัพยากรสามารถมีอยู่ได้โดยไม่มีสมาชิกทีมโครงการเป็นบันทึกย่อแบบร่างของความต้องการ</span><span class="sxs-lookup"><span data-stu-id="67547-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="67547-107">ความแตกต่างระหว่างชั่วโมงที่นำเสนอและชั่วโมงที่จองแบบไม่ตายตัวคืออะไร?</span><span class="sxs-lookup"><span data-stu-id="67547-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="67547-108">ชั่วโมงที่นำเสนอและชั่วโมงที่จองแบบไม่ตายตัวแตกต่างกันในการแสดงผล</span><span class="sxs-lookup"><span data-stu-id="67547-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="67547-109">ชั่วโมงที่นำเสนอจะแสดงผลเฉพาะกับผู้จัดการทรัพยากรและผู้จัดการโครงการที่เริ่มต้นความต้องการโดยใช้คำขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="67547-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="67547-110">ชั่วโมงที่จองแบบไม่ตายตัวสามารถแสดงผลกับทุกคนที่สามารถเข้าถึงตารางหมายกำหนดการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="67547-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="67547-111">ฉันจะดูชั่วโมงที่จองแบบไม่ตายตัวสำหรับทรัพยากรในทีมได้อย่างไร?</span><span class="sxs-lookup"><span data-stu-id="67547-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="67547-112">ชั่วโมงที่จองแบบไม่ตายตัวสามารถจองเมื่อคุณจองความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="67547-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="67547-113">ทรัพยากรที่มีการมีการจองแบบไม่ตายตัวบนทีมโครงการจะปรากฏเป็นสมาชิกทีมที่มีชั่วโมงที่จองแบบไม่ตายตัว</span><span class="sxs-lookup"><span data-stu-id="67547-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="67547-114">จะปรากฏบนตารางหมายกำหนดการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="67547-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="67547-115">ฉันจะเปลี่ยนชั่วโมงที่ต้องการและวันที่เริ่มต้นและสิ้นสุดสำหรับทรัพยากร (ทั่วไปหรือที่ระบุชื่อ) ที่ฉันจองได้อย่างไร?</span><span class="sxs-lookup"><span data-stu-id="67547-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="67547-116">หลังจากที่ทรัพยากรมีการจองให้เลือก **รักษาการจอง** เพื่อทำการเปลี่ยนแปลงใดๆที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="67547-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="67547-117">ทรัพยากรชนิดใดบ้างที่สนับสนุน Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="67547-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="67547-118">**ผู้ใช้** และ **ผู้ติดต่อ** เป็นชนิดทรัพยากรเฉพาะที่ได้รับการสนับสนุนใน Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="67547-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="67547-119">แม้ว่าคุณจะสามารถสร้างทรัพยากรชนิดอื่นได้ (เช่น **อุปกรณ์** และ **กลุ่ม**) ไม่มีกรณีการใช้งานแบบ end-to-end มาสนับสนุนทรัพยากรเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="67547-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="67547-120">ความแตกต่างระหว่างการมอบหมายและการจองคืออะไร?</span><span class="sxs-lookup"><span data-stu-id="67547-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="67547-121">การมอบหมายคือการมอบหมายของทรัพยากรให้กับงานโครงการในหมายกำหนดการให้บริการโครงการ</span><span class="sxs-lookup"><span data-stu-id="67547-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="67547-122">ทรัพยากรสามารถเป็นได้ทั้งทรัพยากรจริงหรือทั่วไป</span><span class="sxs-lookup"><span data-stu-id="67547-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="67547-123">การจองคือการจัดสรรที่ตายตัวและไม่ตายตัวของทรัพยากรให้กับโครงการ</span><span class="sxs-lookup"><span data-stu-id="67547-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="67547-124">การจองแบบตายตัวใช้กำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="67547-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="67547-125">ตามหลักการแล้วสำหรับทรัพยากรจริง การจองและการมอบหมายควรยอมรับเพราะพวกเขาไม่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="67547-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="67547-126">อย่างไรก็ตาม PSA ไม่บังคับใช้ข้อตกลงนี้</span><span class="sxs-lookup"><span data-stu-id="67547-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="67547-127">มุมมองการกระทบยอดแสดงตำแหน่งผู้จัดการโครงการที่การจองและการมอบหมายทรัพยากรไม่เห็นด้วย</span><span class="sxs-lookup"><span data-stu-id="67547-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
