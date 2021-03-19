---
title: ภาพรวมการออกใบแจ้งหนี้ระหว่างบริษัท
description: หัวข้อนี้ให้ข้อมูลและตัวอย่างเกี่ยวกับการออกใบแจ้งหนี้ระหว่างบริษัทสำหรับโครงการ
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287351"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="52241-103">ภาพรวมการออกใบแจ้งหนี้ระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="52241-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="52241-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="52241-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="52241-105">องค์กรของคุณอาจมีหลายแผนก บริษัท หน่วยย่อย และนิติบุคคลอื่นๆ ที่โอนผลิตภัณฑ์และบริการซึ่งกันและกันสำหรับโครงการต่างๆ</span><span class="sxs-lookup"><span data-stu-id="52241-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="52241-106">นิติบุคคลที่ให้บริการหรือผลิตภัณฑ์เรียกว่า *นิติบุคคลที่ให้ยืม*</span><span class="sxs-lookup"><span data-stu-id="52241-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="52241-107">นิติบุคคลที่รับบริการหรือผลิตภัณฑ์เรียกว่า *นิติบุคคลที่กู้ยืม*</span><span class="sxs-lookup"><span data-stu-id="52241-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="52241-108">ภาพประกอบต่อไปนี้แสดงสถานการณ์ทั่วไปที่นิติบุคคล 2 แห่งคือ Contoso Robotics USA (นิติบุคคลที่กู้ยืม) และ Contoso Robotics UK (นิติบุคคลที่ให้ยืม) ใช้ทรัพยากรร่วมกันเพื่อส่งมอบโครงการให้กับลูกค้า Adventure works</span><span class="sxs-lookup"><span data-stu-id="52241-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="52241-109">สำหรับสถานการณ์นี้ Contoso Robotics USA ได้รับสัญญาให้ส่งมอบงานให้กับ Adventure Works</span><span class="sxs-lookup"><span data-stu-id="52241-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![การออกใบแจ้งหนี้ระหว่างบริษัท](./media/IntercompanyScenario.png) 

<span data-ttu-id="52241-111">Dynamics 365 Project Operations ใช้โฟลว์ต่อไปนี้เพื่อประมวลผลธุรกรรมระหว่างบริษัท:</span><span class="sxs-lookup"><span data-stu-id="52241-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="52241-112">ทรัพยากรจากนิติบุคคลที่ให้ยืมบันทึกธุรกรรมเวลาหรือค่าใช้จ่ายระหว่างบริษัทตามเวลาในการจองและค่าใช้จ่ายกับโครงการในนิติบุคคลที่กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="52241-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="52241-113">ต้นทุนเวลาและค่าใช้จ่ายจะถูกบันทึกไว้ในบริษัทที่ให้กู้ยืมโดยใช้รายการราคาต้นทุนต่อหน่วยของบริษัทที่กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="52241-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="52241-114">ธุรกรรมการขายที่ยังไม่ได้เรียกเก็บเงินระหว่างบริษัทจะถูกบันทึกไว้ในบริษัทที่ให้กู้ยืมโดยใช้รายการราคาต้นทุนต่อหน่วยของบริษัทที่กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="52241-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="52241-115">รายได้ที่ยังไม่เรียกเก็บจะถูกบันทึกในบริษัทที่กู้ยืมโดยใช้รายการราคาสำหรับการขายตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="52241-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="52241-116">ลูกค้าสามารถถูกเรียกเก็บเงินได้เมื่อมีการบันทึกรายได้ที่ยังไม่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="52241-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="52241-117">ลูกค้าไม่ต้องรอจนกว่าการประมวลผลใบแจ้งหนี้ระหว่างบริษัทจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="52241-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="52241-118">ใบแจ้งหนี้ของลูกค้าระหว่างบริษัทถูกสร้างขึ้นเป็นระยะในบริษัทที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="52241-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="52241-119">ใบแจ้งหนี้ถูกสร้างขึ้นด้วยตนเองหรือโดยใช้กระบวนการอัตโนมัติเป็นระยะ</span><span class="sxs-lookup"><span data-stu-id="52241-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="52241-120">ใบแจ้งหนี้ใบเดียวสามารถสร้างสำหรับนิติบุคคลที่ยืมแต่ละรายหรือสามารถสร้างใบแจ้งหนี้แยกตามโครงการได้</span><span class="sxs-lookup"><span data-stu-id="52241-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="52241-121">เมื่อใบแจ้งหนี้ของลูกค้าระหว่างบริษัทมีการลงรายการบัญชีในนิติบุคคลที่ให้ยืม ใบแจ้งหนี้ของผู้ขายที่รอดำเนินการได้ที่เกี่ยวข้องจะสร้างในนิติบุคคลที่กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="52241-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="52241-122">ต้นทุนในใบแจ้งหนี้ของผู้ขายที่รอดำเนินการจะถูกบันทึกไปยังบัญชีแยกประเภทย่อยโครงการเมื่อมีการลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="52241-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="52241-123">แผนภาพต่อไปนี้แสดงการออกใบแจ้งหนี้ระหว่างบริษัท เนื่องจากเกี่ยวข้องกับเหตุการณ์ทางบัญชีและการผ่านรายการที่คาดไว้ไปยังบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="52241-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![โฟลว์ระหว่างบริษัท](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="52241-125">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="52241-125">Additional resources</span></span>

- [<span data-ttu-id="52241-126">กำหนดค่าการออกใบแจ้งหนี้ระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="52241-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="52241-127">บันทึกธุรกรรมระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="52241-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="52241-128">สร้างใบแจ้งหนี้ของลูกค้าและผู้ขายระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="52241-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]