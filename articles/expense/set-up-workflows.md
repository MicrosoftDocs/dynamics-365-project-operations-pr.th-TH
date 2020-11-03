---
title: ตั้งค่าเวิร์กโฟลว์สำหรับการจัดการค่าใช้จ่าย
description: คุณสามารถตั้งค่ากระบวนการเวิร์กโฟลว์ที่ใช้ในการตรวจสอบและอนุมัติเอกสารการเดินทางและค่าใช้จ่าย
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: db1bda71e18369550cd2d38fee1d0ac40e07555d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085959"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="3e7eb-103">ตั้งค่าเวิร์กโฟลว์สำหรับการจัดการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="3e7eb-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="3e7eb-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="3e7eb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3e7eb-105">คุณสามารถตั้งค่ากระบวนการเวิร์กโฟลว์ในการตรวจสอบและอนุมัติเอกสารการเดินทางและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="3e7eb-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="3e7eb-106">คุณสามารถกำหนดเวิร์กโฟลว์สำหรับรายงานค่าใช้จ่าย ใบเบิกค่าเดินทาง และคำขอเบิกเงินสดล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="3e7eb-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="3e7eb-107">เวิร์กโฟลว์แสดงถึงกระบวนการทางธุรกิจและกำหนดวิธีที่เอกสารดำเนินการผ่านระบบ</span><span class="sxs-lookup"><span data-stu-id="3e7eb-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="3e7eb-108">เวิร์กโฟลว์ยังระบุว่าใครต้องทำงานให้เสร็จหรืออนุมัติเอกสารอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="3e7eb-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="3e7eb-109">การใช้ระบบเวิร์กโฟลว์ในองค์กรของคุณมีประโยชน์หลายประการ:</span><span class="sxs-lookup"><span data-stu-id="3e7eb-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="3e7eb-110">**กระบวนการที่สอดคล้องกัน** : คุณสามารถกำหนดขั้นตอนการอนุมัติสำหรับเอกสารเฉพาะ เช่น ใบขอซื้อและรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="3e7eb-110">**Consistent processes** : You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="3e7eb-111">การใช้ระบบเวิร์กโฟลว์ช่วยให้มั่นใจได้ว่าเอกสารได้รับการประมวลผลและอนุมัติอย่างสม่ำเสมอและมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="3e7eb-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="3e7eb-112">**การมองเห็นกระบวนการ** : คุณสามารถติดตามสถานะ ประวัติ และเมตริกประสิทธิภาพของอินสแตนซ์ของเวิร์กโฟลว์เฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="3e7eb-112">**Process visibility** : You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="3e7eb-113">ซึ่งช่วยให้คุณตัดสินใจได้ว่าควรทำการเปลี่ยนแปลงกับเวิร์กโฟลว์เพื่อปรับปรุงประสิทธิภาพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3e7eb-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="3e7eb-114">**รายการงานส่วนกลาง** : ผู้ใช้สามารถดูรายการงานส่วนกลางเพื่อดูงานและการอนุมัติของเวิร์กโฟลว์ที่มอบหมายให้พวกเขา</span><span class="sxs-lookup"><span data-stu-id="3e7eb-114">**Centralized work list** : Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="3e7eb-115">ชนิดของเวิร์กโฟลว์</span><span class="sxs-lookup"><span data-stu-id="3e7eb-115">Workflow types</span></span>

<span data-ttu-id="3e7eb-116">ตารางต่อไปนี้แสดงชนิดของเวิร์กโฟลว์ที่คุณสามารถสร้างใน **การจัดการค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="3e7eb-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="3e7eb-117"><strong>ชนิด</strong></span><span class="sxs-lookup"><span data-stu-id="3e7eb-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="3e7eb-118"><strong>ใช้ชนิดนี้เพื่อ</strong></span><span class="sxs-lookup"><span data-stu-id="3e7eb-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="3e7eb-119"><strong>การอนุมัติรายงานค่าใช้จ่ายอัตโนมัติ</strong></span><span class="sxs-lookup"><span data-stu-id="3e7eb-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="3e7eb-120">สร้างเวิร์กโฟลว์การอนุมัติสำหรับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="3e7eb-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="3e7eb-121"><strong>การลงรายการบัญชีรายงานค่าใช้จ่ายอัตโนมัติ</strong></span><span class="sxs-lookup"><span data-stu-id="3e7eb-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="3e7eb-122">สร้างเวิร์กโฟลว์การลงรายการบัญชีอัตโนมัติสำหรับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="3e7eb-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="3e7eb-123"><strong>สินค้าในรายการค่าใช้จ่าย</strong></span><span class="sxs-lookup"><span data-stu-id="3e7eb-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="3e7eb-124">สร้างเวิร์กโฟลว์การอนุมัติสำหรับสินค้าในรายการของรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="3e7eb-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="3e7eb-125"><strong>การลงรายการบัญชีสินค้าในรายการค่าใช้จ่ายอัตโนมัติ</strong></span><span class="sxs-lookup"><span data-stu-id="3e7eb-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="3e7eb-126">สร้างเวิร์กโฟลว์การลงรายการบัญชีอัตโนมัติสำหรับสินค้าในรายการของรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="3e7eb-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="3e7eb-127"><strong>ใบเบิกค่าเดินทาง</strong></span><span class="sxs-lookup"><span data-stu-id="3e7eb-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="3e7eb-128">สร้างเวิร์กโฟลว์การอนุมัติสำหรับใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="3e7eb-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="3e7eb-129"><strong>คำขอเบิกเงินสดล่วงหน้า</strong></span><span class="sxs-lookup"><span data-stu-id="3e7eb-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="3e7eb-130">สร้างเวิร์กโฟลว์การอนุมัติสำหรับคำขอเบิกเงินสดล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="3e7eb-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="3e7eb-131"><strong>การหักคืนภาษี VAT</strong></span><span class="sxs-lookup"><span data-stu-id="3e7eb-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="3e7eb-132">สร้างเวิร์กโฟลว์การอนุมัติสำหรับการหักคืนภาษีมูลค่าเพิ่ม (VAT)</span><span class="sxs-lookup"><span data-stu-id="3e7eb-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
