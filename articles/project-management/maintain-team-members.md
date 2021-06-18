---
title: ดูแลสมาชิกในทีม
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการจองทรัพยากรที่มีชื่อให้กับทีมโครงการและการมอบหมายงาน
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 00312c5a701768e0042e7e0236477c192690ded3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998659"
---
# <a name="maintain-team-members"></a><span data-ttu-id="9f355-103">ดูแลสมาชิกในทีม</span><span class="sxs-lookup"><span data-stu-id="9f355-103">Maintain team members</span></span>

<span data-ttu-id="9f355-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="9f355-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9f355-105">คุณสามารถเพิ่มทรัพยากรที่มีชื่อให้กับทีมโครงการของคุณโดยการจองโดยตรงไปยังทีม</span><span class="sxs-lookup"><span data-stu-id="9f355-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="9f355-106">ใน Dynamics 365 Project Operations ให้ไปที่ **โครงการ** และเลือกเปิดโครงการที่คุณกำลังทำการจอง</span><span class="sxs-lookup"><span data-stu-id="9f355-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="9f355-107">บนเพจ **โครงการ** บนแท็บ **ทีม** ให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="9f355-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="9f355-108">ในกล่องโต้ตอบ **สร้างสมาชิกทีมโครงการด่วน** ให้เลือกทรัพยากรที่จองได้</span><span class="sxs-lookup"><span data-stu-id="9f355-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="9f355-109">ฟิลด์ **บทบาท** จะเติมข้อมูลด้วยบทบาทเริ่มต้นของทรัพยากรถ้ามีการกำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="9f355-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="9f355-110">คุณสามารถเปลี่ยนบทบาท</span><span class="sxs-lookup"><span data-stu-id="9f355-110">You can change the role.</span></span> 
4. <span data-ttu-id="9f355-111">เลือกวันที่เริ่มต้นและวันที่สิ้นสุดที่จะต้องใช้ทรัพยากรและเลือกวิธีการจัดสรรของความสามารถรองรับของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="9f355-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="9f355-112">ในฟิลด์ **ผู้อนุมัติโครงการ** เลือก **ใช่** หากคุณต้องการให้สมาชิกทีมเป็นผู้อนุมัติโครงการ</span><span class="sxs-lookup"><span data-stu-id="9f355-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="9f355-113">สมาชิกทีมจะสามารถอนุมัติรายการเวลาและค่าใช้จ่ายที่ส่งมาสำหรับโครงการนี้</span><span class="sxs-lookup"><span data-stu-id="9f355-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="9f355-114">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="9f355-114">Select **Save**.</span></span>

<span data-ttu-id="9f355-115">ขณะนี้คุณสามารถกำหนดทรัพยากรที่จองให้กับงานในโครงการได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="9f355-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="9f355-116">บนเพจ **โครงการ** บนแท็บ **กำหนดการ** ให้มอบหมายงานให้กับทรัพยากรใหม่</span><span class="sxs-lookup"><span data-stu-id="9f355-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="9f355-117">ตัวเลือกทรัพยากรที่ถูกเปิดใช้จากฟิลด์ **ทรัพยากร** ในกริดงานจะแสดงสมาชิกในทีมที่คุณสามารถเลือกได้</span><span class="sxs-lookup"><span data-stu-id="9f355-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="9f355-118">ใน Project Operations การจองทรัพยากรและการมอบหมายงานไม่ได้เชื่อมโยงกันอย่างแน่นหนา</span><span class="sxs-lookup"><span data-stu-id="9f355-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="9f355-119">เมื่อคุณใช้ตัวเลือกทรัพยากรในกำหนดการ คุณสามารถกำหนดงานให้กับสมาชิกในทีมด้วยชั่วโมงที่มากกว่าที่ครอบคลุมการจองของพวกเขาในโครงการ</span><span class="sxs-lookup"><span data-stu-id="9f355-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="9f355-120">ความแตกต่างระหว่างการจองสมาชิกทีมและการมอบหมายงานแสดงอยู่ในแท็บ **ทีม** และ **การกระทบยอดทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="9f355-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="9f355-121">คุณยังสามารถกระทบยอดความแตกต่างระหว่างการจองและการมอบหมายทรัพยากรในระดับที่ละเอียดมากขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="9f355-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="9f355-122">ใช้ตัวเลือกทรัพยากรบนแท็บ **กำหนดการ** เพื่อค้นหาและเลือกทรัพยากรที่สามารถจองได้ที่ยังไม่ได้เป็นส่วนหนึ่งของทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="9f355-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="9f355-123">ทรัพยากรนี้จะแสดงในตัวเลือกทรัพยากรเป็น **ทรัพยากรอื่นๆ**</span><span class="sxs-lookup"><span data-stu-id="9f355-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="9f355-124">เมื่อคุณทำการเลือก ทรัพยากรจะถูกเพิ่มไปยังทีมโครงการและกำหนดให้กับงาน แต่จะไม่มีการสร้างการจอง</span><span class="sxs-lookup"><span data-stu-id="9f355-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="9f355-125">คุณสามารถใช้การขยายความสามารถในการจองของแท็บ **การกระทบยอด** หรือ **ตารางกำหนดการ** เพื่อจองความสามารถรองรับของทรัพยากรให้โครงการ</span><span class="sxs-lookup"><span data-stu-id="9f355-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="9f355-126">หลังจากที่สมาชิกทีมในโครงการของคุณมีการจองแล้ว คุณสามารถใช้ **รักษาการจอง** หรือ **ตารางกำหนดการ** เพื่อจัดการการจองของพวกเขาโดยตรง</span><span class="sxs-lookup"><span data-stu-id="9f355-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]