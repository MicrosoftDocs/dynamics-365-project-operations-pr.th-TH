---
title: ภาพรวมการอนุมัติ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการทำงานกับการอนุมัติใน Project Operations
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961189"
---
# <a name="approvals-overview"></a><span data-ttu-id="ae965-103">ภาพรวมการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="ae965-103">Approvals overview</span></span>

<span data-ttu-id="ae965-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="ae965-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ae965-105">การส่งเวลาและค่าใช้จ่ายจะเลื่นผ่านเวิร์กโฟลว์การอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="ae965-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="ae965-106">หลังจากรายการได้รับการอนุมัติ จะมีการบันทึกการทำรายการในข้อมูลจริงหรือมีการจองเวลาไว้ในตาราง</span><span class="sxs-lookup"><span data-stu-id="ae965-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="ae965-107">เวิร์กโฟลว์การอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="ae965-107">Approvals workflow</span></span>
<span data-ttu-id="ae965-108">เมื่อคุณสร้างและส่งรายการเวลาหรือค่าใช้จ่าย ระบบจะสร้างรายการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="ae965-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="ae965-109">ผู้อนุมัติโครงการหรือผู้จัดการของคุณจะตรวจสอบและอนุมัติรายการของคุณ</span><span class="sxs-lookup"><span data-stu-id="ae965-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="ae965-110">หากรายการเกี่ยวข้องกับโครงการ เมื่อได้รับการอนุมัติแล้วจะมีการสร้างข้อมูลจริง</span><span class="sxs-lookup"><span data-stu-id="ae965-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="ae965-111">ซึ่งทำให้สามารถติดตามค่าใช้จ่ายและการเรียกเก็บเงินได้</span><span class="sxs-lookup"><span data-stu-id="ae965-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="ae965-112">อนุมัติรายการ</span><span class="sxs-lookup"><span data-stu-id="ae965-112">Approve an entry</span></span>
<span data-ttu-id="ae965-113">ฟอร์ม **การอนุมัติ** ช่วยให้คุณสามารถสลับระหว่างมุมมองต่างๆ เพื่อให้คุณสามารถดูการอนุมัติชนิดต่างๆ ได้</span><span class="sxs-lookup"><span data-stu-id="ae965-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="ae965-114">ไปที่ฟอร์ม **การอนุมัติ** และเลือก **ค่าใช้จ่าย**, **เวลา** หรือ **การเรียกคืน**</span><span class="sxs-lookup"><span data-stu-id="ae965-114">Go to the **Approvals** form and select **Expenses**, **Time**, or **Recalls**.</span></span>
2. <span data-ttu-id="ae965-115">ตรวจสอบการอนุมัติแต่ละรายการ และเลือกรายการที่คุณต้องการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="ae965-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="ae965-116">เลือก **อนุมัติ** เพื่ออนุมัติรายการที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ae965-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="ae965-117">ระบบจะประมวลผลรายการเหล่านี้และสร้างข้อมูลจริงหรือการจอง</span><span class="sxs-lookup"><span data-stu-id="ae965-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="ae965-118">ปฏิเสธรายการ</span><span class="sxs-lookup"><span data-stu-id="ae965-118">Reject an entry</span></span>
<span data-ttu-id="ae965-119">ในฐานะผู้อนุมัติโครงการ คุณอาจต้องส่งรายการกลับไปยังผู้ใช้เพื่อให้ทำการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="ae965-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="ae965-120">ไปที่ฟอร์ม **การอนุมัติ** และเลือกรายการที่จะปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="ae965-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="ae965-121">เลือก**ปฏิเสธ**</span><span class="sxs-lookup"><span data-stu-id="ae965-121">Select **Reject**.</span></span>
3. <span data-ttu-id="ae965-122">ไม่บังคับ - เพิ่มข้อคิดเห็นในกล่องโต้ตอบ **ข้อคิดเห็นในการปฏิเสธ** เพื่อแจ้งให้ผู้ใช้ทราบถึงสาเหตุที่มีการปฏิเสธรายการ</span><span class="sxs-lookup"><span data-stu-id="ae965-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="ae965-123">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ae965-123">Select **OK**.</span></span> <span data-ttu-id="ae965-124">รายการจะมีการส่งกลับไปยังผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ae965-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="ae965-125">เรียกคืนรายการ</span><span class="sxs-lookup"><span data-stu-id="ae965-125">Recall entries</span></span>
<span data-ttu-id="ae965-126">ในบางครั้ง คุณอาจต้องเรียกคืนรายการที่ส่งมา</span><span class="sxs-lookup"><span data-stu-id="ae965-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="ae965-127">หากรายการไม่ได้รับการอนุมัติ จะมีการส่งกลับทันที</span><span class="sxs-lookup"><span data-stu-id="ae965-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="ae965-128">อย่างไรก็ตาม รายการที่ได้รับอนุมัติอาจมีผลกระทบอย่างมาก</span><span class="sxs-lookup"><span data-stu-id="ae965-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="ae965-129">ผู้อนุมัติโครงการจำเป็นต้องอนุมัติการเรียกคืนเพื่อย้อนกลับการทำรายการในข้อมูลจริง</span><span class="sxs-lookup"><span data-stu-id="ae965-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="ae965-130">ระบุผู้อนุมัติโครงการ</span><span class="sxs-lookup"><span data-stu-id="ae965-130">Specify Project approvers</span></span>
<span data-ttu-id="ae965-131">แต่ละโครงการมีสมาชิกทีมโครงการจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="ae965-131">Each project has a number of project team members.</span></span> <span data-ttu-id="ae965-132">คุณสามารถระบุสมาชิกทีมที่เป็นผู้อนุมัติโครงการได้</span><span class="sxs-lookup"><span data-stu-id="ae965-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="ae965-133">ไปที่ฟอร์ม **โครงการ** และเปิดโครงการจากรายการ</span><span class="sxs-lookup"><span data-stu-id="ae965-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="ae965-134">บนแท็บ **ทีม** เลือกสมาชิกทีมที่จะเป็นผู้อนุมัติโครงการ จากนั้นเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="ae965-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="ae965-135">ตั้งค่าฟิลด์ **ผู้อนุมัติโครงการ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="ae965-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="ae965-136">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ae965-136">Select **Save**.</span></span>
5. <span data-ttu-id="ae965-137">ทำซ้ำขั้นตอนที่ 2-4 เพื่อเพิ่มผู้อนุมัติโครงการเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ae965-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="ae965-138">กำหนดค่าผู้จัดการของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ae965-138">Configure the user's manager</span></span>

1. <span data-ttu-id="ae965-139">ไปที่ **การตั้งค่า** > **ความปลอดภัย** > **ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="ae965-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="ae965-140">เลือกผู้ใช้ที่คุณจะกำหนดให้เป็นผู้จัดการและในพื้นที่ **ข้อมูลองค์กร** ให้เลือกผู้จัดการจากรายการ</span><span class="sxs-lookup"><span data-stu-id="ae965-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="ae965-141">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ae965-141">Select **Save**.</span></span>


