---
title: กำหนดนโยบายค่าใช้จ่าย
description: คุณสามารถกำหนดนโยบายค่าใช้จ่ายที่ผู้ปฏิบัติงานของคุณต้องปฏิบัติตามเมื่อป้อนและส่งรายงานค่าใช้จ่ายและใบเบิกค่าเดินทาง
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fbab7fd94fa429876216ee82b716da8d847fb01a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896664"
---
# <a name="define-expense-policies"></a><span data-ttu-id="d61f7-103">กำหนดนโยบายค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d61f7-103">Define expense policies</span></span>

<span data-ttu-id="d61f7-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="d61f7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d61f7-105">คุณสามารถกำหนดนโยบายที่ผู้ปฏิบัติงานของคุณต้องปฏิบัติตามเมื่อป้อนและส่งรายงานค่าใช้จ่ายและใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="d61f7-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="d61f7-106">การใช้นโยบายค่าใช้จ่ายสามารถช่วยคุณจัดการค่าใช้จ่ายได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="d61f7-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="d61f7-107">ตัวอย่างเช่น คุณสามารถกำหนดนโยบายสำหรับค่าใช้จ่ายของโรงแรมในนิวยอร์กซิตี ซึ่งระบุว่าค่าใช้จ่ายต่อคืนต้องไม่เกิน USD 250</span><span class="sxs-lookup"><span data-stu-id="d61f7-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="d61f7-108">หากผู้ปฏิบัติงานส่งรายงานค่าใช้จ่ายหรือใบเบิกค่าเดินทางที่มีราคาค่าห้องพักเกินจำนวนนี้ ระบบจะแจ้ง</span><span class="sxs-lookup"><span data-stu-id="d61f7-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="d61f7-109">ผู้ปฏิบัติงานว่าเกินจำนวนเงินตามนโยบายสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d61f7-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="d61f7-110">คุณสามารถกำหนดค่าข้อความที่ผู้ปฏิบัติงานจะได้รับเมื่อคุณ</span><span class="sxs-lookup"><span data-stu-id="d61f7-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="d61f7-111">กำหนดนโยบายได้</span><span class="sxs-lookup"><span data-stu-id="d61f7-111">define the policy.</span></span>      
        
<span data-ttu-id="d61f7-112">คุณสามารถกำหนดนโยบายได้สามชนิด:</span><span class="sxs-lookup"><span data-stu-id="d61f7-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="d61f7-113">**คำเตือน**: อนุญาตให้ผู้ปฏิบัติงานส่งรายงานค่าใช้จ่ายหรือใบเบิกค่าเดินทางได้ แต่จะมีการทำเครื่องหมายค่าใช้จ่ายสำหรับผู้อนุมัติทั้งหมดและ</span><span class="sxs-lookup"><span data-stu-id="d61f7-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="d61f7-114">สำหรับการรายงานในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="d61f7-114">for later reporting.</span></span>        

- <span data-ttu-id="d61f7-115">**ข้อผิดพลาด**: กำหนดให้ผู้ปฏิบัติงานต้องแก้ไขค่าใช้จ่ายเพื่อให้สอดคล้องกับนโยบายก่อนที่จะส่งรายงานค่าใช้จ่ายหรือใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="d61f7-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="d61f7-116">**เหตุผล**: กำหนดให้ผู้ปฏิบัติงานหรือผู้จัดการต้องระบุเหตุผลสำหรับค่าใช้จ่ายเกินจำนวนเงินของนโยบายก่อนที่จะส่งรายงานค่าใช้จ่ายหรือใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="d61f7-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="d61f7-117">เคล็ดลับเกี่ยวกับนโยบาย</span><span class="sxs-lookup"><span data-stu-id="d61f7-117">Policy tips</span></span>
<span data-ttu-id="d61f7-118">ต่อไปนี้เป็นข้อเสนอแนะสองสามข้อที่จะช่วยคุณในการสร้างนโยบายใหม่สำหรับการจัดการค่าใช้จ่าย:</span><span class="sxs-lookup"><span data-stu-id="d61f7-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="d61f7-119">นโยบายเป็นวันที่มีผลบังคับใช้ ซึ่งหมายความว่านโยบายจะไม่มีผลหากสร้างขึ้นด้วยมีวันที่หลังจากวันที่เกิดค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d61f7-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="d61f7-120">ตัวอย่างเช่น คุณสร้างนโยบายใหม่ในวันนี้เพื่อบังคับใช้ค่าอาหารสูงสุด $50</span><span class="sxs-lookup"><span data-stu-id="d61f7-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="d61f7-121">ค่าใช้จ่ายที่มีอยู่ที่ป้อนเมื่อวานนี้จะไม่นำมาตรวจสอบกับนโยบายนี้</span><span class="sxs-lookup"><span data-stu-id="d61f7-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="d61f7-122">เมื่อสร้างนโยบายสำหรับประเภทค่าใช้จ่ายที่สามารถแสดงรายการได้ ให้พิจารณาเพิ่มเงื่อนไขสำหรับชนิดรายการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d61f7-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="d61f7-123">นโยบายบางอย่าง เช่น การต้องใช้ใบเสร็จรับเงินอาจไม่เหมาะกับรายการที่มีการแสดงรายการ</span><span class="sxs-lookup"><span data-stu-id="d61f7-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="d61f7-124">ในสถานการณ์นี้ นโยบายจะนำมาใช้กับรายการส่วนหัวหรือรายการที่ไม่แสดงเป็นรายการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d61f7-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="d61f7-125">นโยบายการจัดการค่าใช้จ่ายจะมีการประเมินเทียบกับเอนทิตีต้นทางตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d61f7-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="d61f7-126">สำหรับสถานการณ์ระหว่างบริษัท คุณสามารถตั้งค่านโยบายให้ประเมินเทียบกับเอนทิตีปลายทาง (เอนทิตีที่ขอยืม) แทนได้</span><span class="sxs-lookup"><span data-stu-id="d61f7-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="d61f7-127">ในการเรียกใช้นโยบายกับเอนทิตีปลายทาง ให้เปิดคุณลักษณะ **ประเมินนโยบายค่าใช้จ่ายเทียบกับนิติบุคคลที่ขอยืม** ในพื้นที่ทำงาน **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="d61f7-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="d61f7-128">เวลาในการประเมินนโยบาย</span><span class="sxs-lookup"><span data-stu-id="d61f7-128">When to evaluate policies</span></span>

<span data-ttu-id="d61f7-129">ในพารามิเตอร์การจัดการค่าใช้จ่าย คุณสามารถเลือกที่จะประเมินนโยบายการจัดการค่าใช้จ่ายเมื่อมีการบันทึกรายการหรือเมื่อมีการส่งรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d61f7-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="d61f7-130">หากคุณเลือกที่จะประเมินเมื่อมีการบันทึกรายการ ผู้ใช้จะสามารถมองเห็นได้ก่อนว่าพวกเขาต้องทำอะไรเพื่อทำรายงานค่าใช้จ่ายให้เสร็จสมบูรณ์ทั้งหมดพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="d61f7-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="d61f7-131">หรือคุณสามารถชะลอการประเมินนโยบายและประหยัดเวลาได้โดยการตรวจสอบความถูกต้องในตอนท้าย ระหว่างการส่งไปยังเวิร์กโฟลว์</span><span class="sxs-lookup"><span data-stu-id="d61f7-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
