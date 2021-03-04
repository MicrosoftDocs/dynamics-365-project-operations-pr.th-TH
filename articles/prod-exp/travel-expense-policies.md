---
title: ตั้งค่านโยบายค่าใช้จ่าย
description: คุณสามารถตั้งค่านโยบายค่าใช้จ่ายที่ผู้ปฏิบัติงานของคุณต้องปฏิบัติตาม เมื่อป้อนและส่งรายงานค่าใช้จ่ายและใบขอเดินทางใน Microsoft Dynamics 365 Finance
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab99c0ec769eb2e0914fc7d993f83d20e2c327f6
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960720"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="03ee4-103">ตั้งค่านโยบายค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="03ee4-103">Set up expense policies</span></span>

<span data-ttu-id="03ee4-104">คุณสามารถกำหนดนโยบายที่ผู้ปฏิบัติงานของคุณต้องปฏิบัติตามเมื่อป้อนและส่งรายงานค่าใช้จ่ายและใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="03ee4-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="03ee4-105">การใช้นโยบายค่าใช้จ่ายสามารถช่วยคุณจัดการค่าใช้จ่ายได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="03ee4-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="03ee4-106">ตัวอย่างเช่น คุณสามารถกำหนดนโยบายสำหรับค่าใช้จ่ายของโรงแรมในนิวยอร์กซิตี ซึ่งระบุว่าค่าใช้จ่ายต่อคืนต้องไม่เกิน USD 250</span><span class="sxs-lookup"><span data-stu-id="03ee4-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="03ee4-107">หากผู้ปฏิบัติงานส่งรายงานค่าใช้จ่ายหรือใบขอเดินทางที่มีราคาค่าห้องพักเกินจำนวนนี้ ระบบจะแจ้ง</span><span class="sxs-lookup"><span data-stu-id="03ee4-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="03ee4-108">ผู้ปฏิบัติงานว่าเกินจำนวนเงินตามนโยบายสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="03ee4-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="03ee4-109">คุณสามารถกำหนดค่าข้อความที่ผู้ปฏิบัติงานจะได้รับเมื่อคุณ</span><span class="sxs-lookup"><span data-stu-id="03ee4-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="03ee4-110">กำหนดนโยบายได้</span><span class="sxs-lookup"><span data-stu-id="03ee4-110">define the policy.</span></span>      
        
<span data-ttu-id="03ee4-111">คุณสามารถกำหนดนโยบายได้สามชนิด:</span><span class="sxs-lookup"><span data-stu-id="03ee4-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="03ee4-112">คำเตือน – อนุญาตให้ผู้ปฏิบัติงานส่งรายงานค่าใช้จ่ายหรือใบเบิกค่าเดินทางได้ แต่จะมีการทำเครื่องหมายค่าใช้จ่ายสำหรับผู้อนุมัติทั้งหมดและ</span><span class="sxs-lookup"><span data-stu-id="03ee4-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="03ee4-113">สำหรับการรายงานในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="03ee4-113">for later reporting.</span></span>        

- <span data-ttu-id="03ee4-114">ข้อผิดพลาด – กำหนดให้ผู้ปฏิบัติงานต้องแก้ไขค่าใช้จ่ายเพื่อให้สอดคล้องกับนโยบาย ก่อนที่จะส่งรายงานค่าใช้จ่ายหรือใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="03ee4-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="03ee4-115">เหตุผล – กำหนดให้ผู้ปฏิบัติงานหรือผู้จัดการต้องระบุเหตุผลสำหรับค่าใช้จ่ายเกินจำนวนเงินของนโยบาย ก่อนที่จะส่งรายงานค่าใช้จ่ายหรือใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="03ee4-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="03ee4-116">เคล็ดลับเกี่ยวกับนโยบาย</span><span class="sxs-lookup"><span data-stu-id="03ee4-116">Policy tips</span></span>
<span data-ttu-id="03ee4-117">ต่อไปนี้เป็นข้อเสนอแนะสองสามข้อที่จะช่วยคุณ เมื่อสร้างนโยบายใหม่สำหรับการจัดการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="03ee4-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="03ee4-118">นโยบายเป็นวันที่มีผลบังคับใช้ และจะไม่มีผล หากนโยบายถูกสร้างขึ้นด้วยวันที่หลังจากวันที่ที่เกิดค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="03ee4-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="03ee4-119">ตัวอย่างเช่น หากวันนี้คุณสร้างนโยบายใหม่เพื่อบังคับใช้ค่าอาหารสูงสุด $50 ค่าใช้จ่ายที่มีอยู่ใดๆ ที่ป้อนเมื่อวานนี้ จะไม่ถูกตรวจสอบกับนโยบายนี้</span><span class="sxs-lookup"><span data-stu-id="03ee4-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="03ee4-120">เมื่อสร้างนโยบายสำหรับประเภทค่าใช้จ่ายที่สามารถแสดงรายการได้ ให้พิจารณาเพิ่มเงื่อนไขสำหรับชนิดรายการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="03ee4-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="03ee4-121">นโยบายบางอย่าง เช่น การต้องใช้ใบเสร็จ อาจไม่เหมาะสมสำหรับรายการที่แยกรายการ และควรใช้กับบรรทัดส่วนหัวหรือบรรทัดที่ไม่แสดงรายการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="03ee4-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="03ee4-122">นโยบายการจัดการค่าใช้จ่ายจะมีการประเมินเทียบกับเอนทิตีต้นทางตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="03ee4-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="03ee4-123">สำหรับสถานการณ์ระหว่างบริษัท คุณสามารถตั้งค่านโยบายให้ประเมินเทียบกับเอนทิตีปลายทาง (เอนทิตีที่ขอยืม) แทนได้</span><span class="sxs-lookup"><span data-stu-id="03ee4-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="03ee4-124">ในการเรียกใช้นโยบายกับเอนทิตีปลายทาง ให้เปิดคุณลักษณะ "ประเมินนโยบายค่าใช้จ่ายเทียบกับนิติบุคคลที่ขอยืม" ในพื้นที่ทำงาน **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="03ee4-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="03ee4-125">เวลาในการประเมินนโยบาย</span><span class="sxs-lookup"><span data-stu-id="03ee4-125">When to evaluate policies</span></span>

<span data-ttu-id="03ee4-126">ในพารามิเตอร์การจัดการค่าใช้จ่าย มีตัวเลือกในการประเมินนโยบายการจัดการค่าใช้จ่าย เมื่อมีการบันทึกรายการ หรือเมื่อมีการส่งรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="03ee4-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="03ee4-127">หากคุณเลือกที่จะประเมินเมื่อมีการบันทึกรายการ นี่จะทำให้มั่นใจว่าผู้ใช้สามารถมองเห็นล่วงหน้าในสิ่งที่พวกเขาต้องทำเพื่อให้รายงานค่าใช้จ่ายของพวกเขาเสร็จสมบูรณ์ทั้งหมดพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="03ee4-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="03ee4-128">หรือคุณสามารถชะลอการประเมินนโยบายและประหยัดเวลาได้ หากคุณมีการตรวจสอบความถูกต้องในตอนท้าย ระหว่างการส่งไปยังเวิร์กโฟลว์</span><span class="sxs-lookup"><span data-stu-id="03ee4-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
