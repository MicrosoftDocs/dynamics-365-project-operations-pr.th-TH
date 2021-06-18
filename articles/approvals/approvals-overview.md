---
title: ภาพรวมการอนุมัติ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการทำงานกับการอนุมัติใน Project Operations
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 5e30b8a386805faee869f77e695d5ee492d78cdb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996724"
---
# <a name="approvals-overview"></a><span data-ttu-id="2e8f1-103">ภาพรวมการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="2e8f1-103">Approvals overview</span></span>

<span data-ttu-id="2e8f1-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="2e8f1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2e8f1-105">การส่งเวลา ค่าใช้จ่าย และการใช้วัสดุจะเลื่อนผ่านเวิร์กโฟลว์การอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="2e8f1-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="2e8f1-106">หลังจากรายการได้รับการอนุมัติ จะมีการบันทึกการทำรายการในข้อมูลจริงหรือมีการจองเวลาไว้ในตาราง</span><span class="sxs-lookup"><span data-stu-id="2e8f1-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="2e8f1-107">เวิร์กโฟลว์การอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="2e8f1-107">Approvals workflow</span></span>
<span data-ttu-id="2e8f1-108">เมื่อคุณสร้างและส่งรายการเวลา ค่าใช้จ่าย หรือการใช้วัสดุ จะมีการสร้างเรกคอร์ดการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="2e8f1-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="2e8f1-109">ผู้อนุมัติหรือผู้จัดการโครงการจะตรวจสอบและอนุมัติรายการ</span><span class="sxs-lookup"><span data-stu-id="2e8f1-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="2e8f1-110">หากรายการนั้นเกี่ยวข้องกับโครงการ จะมีการสร้างข้อมูลจริงเมื่อได้รับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="2e8f1-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="2e8f1-111">ซึ่งทำให้สามารถติดตามค่าใช้จ่ายและการเรียกเก็บเงินได้</span><span class="sxs-lookup"><span data-stu-id="2e8f1-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="2e8f1-112">อนุมัติรายการ</span><span class="sxs-lookup"><span data-stu-id="2e8f1-112">Approve an entry</span></span>
<span data-ttu-id="2e8f1-113">เพจ **การอนุมัติ** ช่วยให้คุณสามารถสลับไปมาระหว่างมุมมองต่างๆ เพื่อให้คุณสามารถดูการอนุมัติประเภทต่างๆ ได้</span><span class="sxs-lookup"><span data-stu-id="2e8f1-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="2e8f1-114">ไปที่เพจ **การอนุมัติ** และเลือก **ค่าใช้จ่าย**, **เวลา**, **การใช้วัสดุ** หรือ **การเรียกคืน**</span><span class="sxs-lookup"><span data-stu-id="2e8f1-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="2e8f1-115">ตรวจสอบการอนุมัติแต่ละรายการ และเลือกรายการที่คุณต้องการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="2e8f1-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="2e8f1-116">เลือก **อนุมัติ** เพื่ออนุมัติรายการที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2e8f1-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="2e8f1-117">ระบบจะประมวลผลรายการเหล่านี้และสร้างข้อมูลจริง</span><span class="sxs-lookup"><span data-stu-id="2e8f1-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="2e8f1-118">ปฏิเสธรายการ</span><span class="sxs-lookup"><span data-stu-id="2e8f1-118">Reject an entry</span></span>
<span data-ttu-id="2e8f1-119">ในฐานะผู้อนุมัติโครงการ คุณอาจต้องส่งรายการกลับไปยังผู้ใช้เพื่อให้ทำการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="2e8f1-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="2e8f1-120">ไปที่เพจ **การอนุมัติ** และเลือกรายการที่จะปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="2e8f1-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="2e8f1-121">เลือก **ปฏิเสธ**</span><span class="sxs-lookup"><span data-stu-id="2e8f1-121">Select **Reject**.</span></span>
3. <span data-ttu-id="2e8f1-122">หรือเพิ่มข้อคิดเห็นในกล่องโต้ตอบ **ข้อคิดเห็นในการปฏิเสธ** เพื่อแจ้งให้ผู้ใช้ทราบว่าเหตุใดจึงมีการปฏิเสธรายการนั้นได้</span><span class="sxs-lookup"><span data-stu-id="2e8f1-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="2e8f1-123">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2e8f1-123">Select **OK**.</span></span> <span data-ttu-id="2e8f1-124">รายการจะมีการส่งกลับไปยังผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2e8f1-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="2e8f1-125">ยกเลิกการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="2e8f1-125">Cancel approval</span></span>
<span data-ttu-id="2e8f1-126">ในบางกรณี คุณอาจต้องยกเลิกรายการที่ได้รับการอนุมัติก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="2e8f1-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="2e8f1-127">การยกเลิกรายการที่ได้รับอนุมัติก่อนหน้านี้จะมีผลกระทบทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="2e8f1-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="2e8f1-128">การอนุมัติคำขอการเรียกคืน</span><span class="sxs-lookup"><span data-stu-id="2e8f1-128">Approving recall requests</span></span>
<span data-ttu-id="2e8f1-129">ในบางกรณี ที่ปรึกษาอาจจำเป็นต้องเรียกคืนรายการที่ได้รับอนุมัติก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="2e8f1-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="2e8f1-130">การยกเลิกรายการที่ได้รับอนุมัติก่อนหน้านี้จะมีผลกระทบทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="2e8f1-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="2e8f1-131">ผู้อนุมัติโครงการจะต้องอนุมัติการเรียกคืนเพื่อย้อนกลับธุรกรรมในข้อมูลจริง</span><span class="sxs-lookup"><span data-stu-id="2e8f1-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="2e8f1-132">ระบุผู้อนุมัติโครงการ</span><span class="sxs-lookup"><span data-stu-id="2e8f1-132">Specify Project approvers</span></span>
<span data-ttu-id="2e8f1-133">แต่ละโครงการมีสมาชิกทีมโครงการจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="2e8f1-133">Each project has a number of project team members.</span></span> <span data-ttu-id="2e8f1-134">คุณสามารถระบุสมาชิกทีมที่เป็นผู้อนุมัติโครงการได้</span><span class="sxs-lookup"><span data-stu-id="2e8f1-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="2e8f1-135">ไปที่เพจ **โครงการ** และเปิดโครงการจากรายการ</span><span class="sxs-lookup"><span data-stu-id="2e8f1-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="2e8f1-136">บนแท็บ **ทีม** เลือกสมาชิกทีมที่จะเป็นผู้อนุมัติโครงการ จากนั้นเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="2e8f1-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="2e8f1-137">ตั้งค่าฟิลด์ **ผู้อนุมัติโครงการ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="2e8f1-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="2e8f1-138">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="2e8f1-138">Select **Save**.</span></span>
5. <span data-ttu-id="2e8f1-139">ทำซ้ำขั้นตอนที่ 2-4 เพื่อเพิ่มผู้อนุมัติโครงการเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2e8f1-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="2e8f1-140">กำหนดค่าผู้จัดการของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2e8f1-140">Configure the user's manager</span></span>

1. <span data-ttu-id="2e8f1-141">ไปที่ **การตั้งค่า** > **ความปลอดภัย** > **ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="2e8f1-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="2e8f1-142">เลือกผู้ใช้ที่คุณจะกำหนดให้เป็นผู้จัดการและในพื้นที่ **ข้อมูลองค์กร** ให้เลือกผู้จัดการจากรายการ</span><span class="sxs-lookup"><span data-stu-id="2e8f1-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="2e8f1-143">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="2e8f1-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
