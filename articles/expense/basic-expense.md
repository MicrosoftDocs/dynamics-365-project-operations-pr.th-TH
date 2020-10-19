---
title: รายการค่าใช้จ่าย (Lite)
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการทำงานกับรายการค่าใช้จ่ายในการปรับใช้งานรุ่นใช้งานง่าย
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965908"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="eaaee-103">รายการค่าใช้จ่าย (Lite)</span><span class="sxs-lookup"><span data-stu-id="eaaee-103">Expense entry (lite)</span></span>

<span data-ttu-id="eaaee-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="eaaee-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="eaaee-105">การจัดการค่าใช้จ่ายเบื้องต้นหรือแบบ Lite เป็นความสามารถในการบันทึกค่าใช้จ่ายแบบง่าย</span><span class="sxs-lookup"><span data-stu-id="eaaee-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="eaaee-106">คุณสามารถบันทึกค่าใช้จ่ายต่อโครงการ จากนั้นผู้อนุมัติโครงการจะตรวจสอบและอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="eaaee-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="eaaee-107">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับความสามารถด้านค่าใช้จ่ายใน Dynamics 365 Project Operations ดูที่ [ภาพรวมของค่าใช้จ่าย](expense-overview.md)</span><span class="sxs-lookup"><span data-stu-id="eaaee-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="eaaee-108">บันทึกค่าใช้จ่ายเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="eaaee-108">Capture a basic expense</span></span>

<span data-ttu-id="eaaee-109">คุณสามารถบันทึกค่าใช้จ่ายของคุณเพื่อส่งให้ผู้อนุมัติได้</span><span class="sxs-lookup"><span data-stu-id="eaaee-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="eaaee-110">ไปที่ **ค่าใช้จ่าย** และเลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="eaaee-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="eaaee-111">บนเพจ **ค่าใช้จ่ายใหม่** ให้ป้อนข้อมูลค่าใช้จ่ายที่จำเป็น จากนั้นเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="eaaee-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="eaaee-112">ส่งค่าใช้จ่ายเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="eaaee-112">Submit a basic expense</span></span>

<span data-ttu-id="eaaee-113">หลังจากที่คุณบันทึกค่าใช้จ่ายทั้งหมดของคุณเสร็จแล้วและคุณพร้อมที่จะให้มีการอนุมัติ คุณต้องส่งค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="eaaee-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="eaaee-114">ไปที่ **ค่าใช้จ่าย** และเลือกค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="eaaee-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="eaaee-115">หรือเลือกค่าใช้จ่ายทั้งหมดโดยใช้กล่องกาเครื่องหมายที่ส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="eaaee-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="eaaee-116">เลือก **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="eaaee-116">Select **Submit**.</span></span> <span data-ttu-id="eaaee-117">ระบบจะประมวลผลรายการที่เลือก จากนั้นสร้างคำขออนุมัติค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="eaaee-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="eaaee-118">เรียกคืนค่าใช้จ่ายเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="eaaee-118">Recall a basic expense</span></span>

<span data-ttu-id="eaaee-119">เมื่อคุณส่งค่าใช้จ่ายโดยไม่ได้ตั้งใจ คุณสามารถเรียกคืนได้</span><span class="sxs-lookup"><span data-stu-id="eaaee-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="eaaee-120">เวลาที่ต้องเรียกคืนรายการค่าใช้จ่ายขึ้นอยู่กับขั้นตอนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="eaaee-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="eaaee-121">หากผู้อนุมัติยังไม่อนุมัติรายการ การเรียกคืนสามารถเกิดขึ้นได้ทันที</span><span class="sxs-lookup"><span data-stu-id="eaaee-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="eaaee-122">อย่างไรก็ตาม หากรายการได้รับการอนุมัติแล้ว ผู้อนุมัติจะได้รับการขอให้อนุมัติการเรียกคืน และย้อนกลับการทำรายการ</span><span class="sxs-lookup"><span data-stu-id="eaaee-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="eaaee-123">ไปที่ **ค่าใช้จ่าย** จากนั้นในรายการค่าใช้จ่าย ให้เลือกค่าใช้จ่ายที่จะเรียกคืน</span><span class="sxs-lookup"><span data-stu-id="eaaee-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="eaaee-124">เลือก **การเรียกคืน**</span><span class="sxs-lookup"><span data-stu-id="eaaee-124">Select **Recall**.</span></span> <span data-ttu-id="eaaee-125">หากรายการค่าใช้จ่ายยังไม่ได้รับการอนุมัติ ระบบจะเรียกคืนทันที</span><span class="sxs-lookup"><span data-stu-id="eaaee-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="eaaee-126">หากรายการค่าใช้จ่ายได้รับการอนุมัติแล้ว ระบบจะสร้างคำขอเรียกคืนขึ้นเพื่อแจ้งให้ผู้อนุมัติทราบว่าคุณต้องการย้อนกลับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="eaaee-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="eaaee-127">จากนั้นผู้อนุมัติจะยืนยันว่าการกลับรายการสามารถทำได้ และจะส่งคืนรายการ</span><span class="sxs-lookup"><span data-stu-id="eaaee-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="eaaee-128">ลบค่าใช้จ่ายเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="eaaee-128">Delete a basic expense</span></span>

<span data-ttu-id="eaaee-129">ค่าใช้จ่ายที่ยังไม่ได้ส่งสามารถลบได้</span><span class="sxs-lookup"><span data-stu-id="eaaee-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="eaaee-130">หากต้องการลบค่าใช้จ่ายที่ส่งไปแล้ว คุณต้องเรียกคืนก่อน</span><span class="sxs-lookup"><span data-stu-id="eaaee-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="eaaee-131">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="eaaee-131">See also</span></span>

- [<span data-ttu-id="eaaee-132">ภาพรวมการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="eaaee-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
