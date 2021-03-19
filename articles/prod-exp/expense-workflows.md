---
title: ตั้งค่าเวิร์กโฟลว์การจัดการค่าใช้จ่าย
description: คุณสามารถตั้งค่ากระบวนการเวิร์กโฟลว์ในการตรวจสอบและอนุมัติเอกสารการเดินทางและค่าใช้จ่าย
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36ab1edc4769013684fa9248e6c5eac025637bbd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271646"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="34d35-103">ตั้งค่าเวิร์กโฟลว์การจัดการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="34d35-103">Set up Expense management workflows</span></span>

<span data-ttu-id="34d35-104">คุณสามารถตั้งค่ากระบวนการเวิร์กโฟลว์ที่ใช้ในการตรวจสอบและอนุมัติเอกสารการเดินทางและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="34d35-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="34d35-105">เอกสารสำหรับเวิร์กโฟลว์ที่สามารถกำหนดได้รวมถึงรายงานค่าใช้จ่าย ใบขอเดินทาง และคำขอเบิกเงินสดล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="34d35-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="34d35-106">เวิร์กโฟลว์แสดงถึงกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="34d35-106">A workflow represents a business process.</span></span> <span data-ttu-id="34d35-107">กำหนดวิธีการที่โฟลว์เอกสารผ่านระบบและระบุว่าใครต้องทำงานให้เสร็จหรืออนุมัติเอกสาร</span><span class="sxs-lookup"><span data-stu-id="34d35-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="34d35-108">การใช้ระบบเวิร์กโฟลว์ในองค์กรของคุณมีประโยชน์หลายประการ:</span><span class="sxs-lookup"><span data-stu-id="34d35-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="34d35-109">**กระบวนการที่สอดคล้องกัน** คุณสามารถกำหนดขั้นตอนการอนุมัติสำหรับเอกสารเฉพาะ เช่น ใบขอซื้อและรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="34d35-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="34d35-110">การใช้ระบบเวิร์กโฟลว์ช่วยให้มั่นใจได้ว่าเอกสารได้รับการประมวลผลและอนุมัติอย่างสม่ำเสมอและมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="34d35-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="34d35-111">การมองเห็นกระบวนการ: คุณสามารถติดตามสถานะ ประวัติ และการวัดประสิทธิภาพของอินสแตนซ์ของเวิร์กโฟลว์เฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="34d35-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="34d35-112">ซึ่งช่วยให้คุณตัดสินใจได้ว่าควรทำการเปลี่ยนแปลงกับเวิร์กโฟลว์เพื่อปรับปรุงประสิทธิภาพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="34d35-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="34d35-113">รายการงานส่วนกลาง: ผู้ใช้สามารถดูรายการงานส่วนกลางเพื่อดูงานและการอนุมัติของเวิร์กโฟลว์ที่มอบหมายให้พวกเขา</span><span class="sxs-lookup"><span data-stu-id="34d35-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="34d35-114">**ประเภทเวิร์กโฟลว์ที่คุณสามารถสร้างได้**</span><span class="sxs-lookup"><span data-stu-id="34d35-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="34d35-115">ตารางต่อไปนี้แสดงชนิดของเวิร์กโฟลว์ที่คุณสามารถสร้างใน **ค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="34d35-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="34d35-116"><strong>ชนิด</strong></span><span class="sxs-lookup"><span data-stu-id="34d35-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="34d35-117"><strong>ใช้ชนิดนี้เพื่อ</strong></span><span class="sxs-lookup"><span data-stu-id="34d35-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="34d35-118"><strong>รายงานค่าใช้จ่าย</strong></span><span class="sxs-lookup"><span data-stu-id="34d35-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="34d35-119">สร้างเวิร์กโฟลว์การอนุมัติสำหรับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="34d35-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="34d35-120"><strong>การลงรายการบัญชีรายงานค่าใช้จ่ายอัตโนมัติ</strong></span><span class="sxs-lookup"><span data-stu-id="34d35-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="34d35-121">สร้างเวิร์กโฟลว์การลงรายการบัญชีอัตโนมัติสำหรับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="34d35-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="34d35-122"><strong>สินค้าในรายการค่าใช้จ่าย</strong></span><span class="sxs-lookup"><span data-stu-id="34d35-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="34d35-123">สร้างเวิร์กโฟลว์การอนุมัติสำหรับสินค้าในรายการของรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="34d35-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="34d35-124"><strong>การลงรายการบัญชีสินค้าในรายการค่าใช้จ่ายอัตโนมัติ</strong></span><span class="sxs-lookup"><span data-stu-id="34d35-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="34d35-125">สร้างเวิร์กโฟลว์การลงรายการบัญชีอัตโนมัติสำหรับสินค้าในรายการของรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="34d35-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="34d35-126"><strong>ใบเบิกค่าเดินทาง</strong></span><span class="sxs-lookup"><span data-stu-id="34d35-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="34d35-127">สร้างเวิร์กโฟลว์การอนุมัติสำหรับใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="34d35-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="34d35-128"><strong>คำขอเบิกเงินสดล่วงหน้า</strong></span><span class="sxs-lookup"><span data-stu-id="34d35-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="34d35-129">สร้างเวิร์กโฟลว์การอนุมัติสำหรับคำขอเบิกเงินสดล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="34d35-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="34d35-130"><strong>การหักคืนภาษี VAT</strong></span><span class="sxs-lookup"><span data-stu-id="34d35-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="34d35-131">สร้างเวิร์กโฟลว์การอนุมัติสำหรับการหักคืนภาษีมูลค่าเพิ่ม (VAT)</span><span class="sxs-lookup"><span data-stu-id="34d35-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]