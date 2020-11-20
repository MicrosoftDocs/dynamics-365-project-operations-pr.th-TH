---
title: ใบแจ้งหนี้ที่แก้ไข
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับใบแจ้งหนี้ที่แก้ไข
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122411"
---
# <a name="corrected-invoices"></a><span data-ttu-id="8db6e-103">ใบแจ้งหนี้ที่แก้ไข</span><span class="sxs-lookup"><span data-stu-id="8db6e-103">Corrected invoices</span></span>

<span data-ttu-id="8db6e-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="8db6e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8db6e-105">ใบแจ้งหนี้ที่ยืนยันแล้วสามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="8db6e-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="8db6e-106">เมื่อคุณแก้ไขใบแจ้งหนี้ที่ยืนยันแล้ว จะมีการสร้างใบแจ้งหนี้ที่แก้ไขฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="8db6e-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="8db6e-107">เนื่องจากสมมติฐานคือคุณต้องการย้อนกลับธุรกรรมและปริมาณทั้งหมดจากใบแจ้งหนี้ต้นฉบับ ใบแจ้งหนี้ที่แก้ไขนี้รวมธุรกรรมทั้งหมดจากใบแจ้งหนี้ต้นฉบับ และปริมาณทั้งหมดบนใบแจ้งหนี้เป็นศูนย์ (0)</span><span class="sxs-lookup"><span data-stu-id="8db6e-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="8db6e-108">เมื่อธุรกรรมใดๆ ไม่จำเป็นต้องแก้ไข คุณสามารถลบออกจากใบแจ้งหนี้ที่แก้ไขฉบับร่างได้</span><span class="sxs-lookup"><span data-stu-id="8db6e-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="8db6e-109">หากต้องการย้อนกลับหรือส่งคืนเฉพาะปริมาณบางส่วน คุณสามารถแก้ไขฟิลด์ ปริมาณ บนรายละเอียดรายการได้</span><span class="sxs-lookup"><span data-stu-id="8db6e-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="8db6e-110">ถ้าคุณเปิดรายละเอียดรายการใบแจ้งหนี้ คุณสามารถดูปริมาณต้นฉบับใบแจ้งหนี้ได้</span><span class="sxs-lookup"><span data-stu-id="8db6e-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="8db6e-111">จากนั้นคุณสามารถแก้ไขปริมาณในใบแจ้งหนี้ปัจจุบันได้ เพื่อให้น้อยกว่าหรือมากกว่าปริมาณในใบแจ้งหนี้ต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="8db6e-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="8db6e-112">เมื่อคุณยืนยันใบแจ้งหนี้ที่มีการแก้ไข การขายที่เรียกเก็บเงินจริงต้นฉบับจะย้อนกลับ และการขายที่เรียกเก็บเงินจริงใหม่จะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="8db6e-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="8db6e-113">ถ้าปริมาณถูกลดลง ความแตกต่างจะทำใหการขายจริงที่ยังไม่ได้เรียกเก็บเงินใหม่ที่ถูกสร้างด้วย</span><span class="sxs-lookup"><span data-stu-id="8db6e-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="8db6e-114">ตัวอย่างเช่น ถ้าการขายที่เรียกเก็บเงินต้นฉบับเป็นเวลา 8 ชั่วโมง และรายละเอียดรายการใบแจ้งหนี้ที่แก้ไขมีปริมาณที่ลดลง 6 ชั่วโมง จะมีการย้อนกลับรายการขายที่เรียกเก็บเงินต้นฉบับ และสร้างใหม่สองรายการจริง</span><span class="sxs-lookup"><span data-stu-id="8db6e-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="8db6e-115">การขายที่มีการเรียกเก็บเงินจริงเป็นเวลาหกชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="8db6e-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="8db6e-116">การขายจริงที่ยังไม่ได้เรียกเก็บเงินป็นเวลาสองชั่วโมงที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="8db6e-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="8db6e-117">คุณสามารถเรียกเก็บเงินธุรกรรมนี้ในภายหลัง หรือทำเครื่องหมายว่าไม่สามารถคิดค่าธรรมเนียมได้ โดยขึ้นอยู่กับการเจรจากับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="8db6e-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
