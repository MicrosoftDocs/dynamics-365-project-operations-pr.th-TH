---
title: เวิร์กโฟลว์สำหรับการจัดการค่าใช้จ่าย
description: หัวข้อนี้อธิบายถึงวิธีที่คุณสามารถใช้ระบบเวิร์กโฟลว์ใน Microsoft Dynamics 365 Finance เพื่อตั้งค่ากระบวนการตรวจสอบรายงานค่าใช้จ่ายในการจัดการค่าใช้จ่าย
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
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086087"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="46820-103">เวิร์กโฟลว์สำหรับการจัดการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="46820-103">Expense management workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46820-104">คุณสามารถใช้ระบบเวิร์กโฟลว์ในเพื่อตั้งค่ากระบวนการตรวจสอบรายงานค่าใช้จ่ายในการจัดการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="46820-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="46820-105">คุณสามารถตั้งค่าเวิร์กโฟลว์ที่ใช้เกณฑ์ต่อไปนี้เพื่อกำหนดว่าใครเป็นผู้อนุมัติรายงานค่าใช้จ่าย:</span><span class="sxs-lookup"><span data-stu-id="46820-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="46820-106">ลำดับชั้นการรายงานของพนักงานและขีดจำกัดการอนุมัติที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="46820-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="46820-107">การอนุมัติหลายระดับที่สนับสนุนผู้อนุมัติชั่วคราวและผู้อนุมัติขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="46820-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="46820-108">มิติทางการเงินและความรับผิดชอบโครงการ</span><span class="sxs-lookup"><span data-stu-id="46820-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="46820-109">การกำหนดให้กับผู้ใช้เฉพาะหรือกลุ่มผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="46820-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="46820-110">สามารถสร้างการอนุมัติเวิร์กโฟลว์สำหรับรายงานค่าใช้จ่าย ใบขอเดินทาง การเบิกเงินสดล่วงหน้า และการกู้คืนภาษีมูลค่าเพิ่ม (VAT)</span><span class="sxs-lookup"><span data-stu-id="46820-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="46820-111">**ตัวอย่างเช่น**</span><span class="sxs-lookup"><span data-stu-id="46820-111">**Example**</span></span>

<span data-ttu-id="46820-112">กระบวนการต่อไปนี้เป็นตัวอย่างของเวิร์กโฟลว์การจัดการค่าใช้จ่ายสำหรับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="46820-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="46820-113">พนักงานสร้างและบันทึกรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="46820-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="46820-114">พนักงานส่งรายงานค่าใช้จ่ายเพื่อรับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="46820-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="46820-115">ผู้อนุมัติจะถูกระบุตามกฎที่กำหนดไว้เมื่อตั้งค่าเวิร์กโฟลว์</span><span class="sxs-lookup"><span data-stu-id="46820-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="46820-116">ผู้อนุมัติจะได้รับการแจ้งเตือนว่ารายงานค่าใช้จ่ายพร้อมสำหรับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="46820-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="46820-117">ผู้อนุมัติตรวจสอบรายงานค่าใช้จ่ายและตรวจสอบว่าเป็นไปตามเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="46820-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="46820-118">ค่าใช้จ่ายไม่ละเมิดนโยบายค่าใช้จ่ายใดๆ</span><span class="sxs-lookup"><span data-stu-id="46820-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="46820-119">หากค่าใช้จ่ายละเมิดนโยบาย ผู้อนุมัติจะตรวจสอบว่ารายงานค่าใช้จ่ายมีเหตุผลทางธุรกิจที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="46820-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="46820-120">ใบเสร็จรับเงินอิเล็กทรอนิกส์แนบมากับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="46820-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="46820-121">ผู้อนุมัติจะอนุมัติรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="46820-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="46820-122">รายงานค่าใช้จ่ายถูกกำหนดให้กับผู้ประสานงานบัญชีเจ้าหนี้สำหรับการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="46820-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="46820-123">หนึ่งในขั้นตอนต่อไปนี้เกิดขึ้นโดยขึ้นอยู่กับว่ามีการกำหนดค่าการลงบัญชีอัตโนมัติ:</span><span class="sxs-lookup"><span data-stu-id="46820-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="46820-124">หากมีการกำหนดค่าการลงรายการบัญชีอัตโนมัติ รายงานค่าใช้จ่ายจะถูกประมวลผลสำหรับการชำระเงินและสถานะของรายงานค่าใช้จ่ายจะได้รับการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="46820-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="46820-125">หากไม่ได้กำหนดค่าการลงรายการบัญชีอัตโนมัติ ผู้ประสานงานบัญชีเจ้าหนี้จะตรวจสอบว่าได้ส่งใบเสร็จรับเงินต้นฉบับทั้งหมดแล้วและใบเสร็จรับเงินจะสอดคล้องกับค่าใช้จ่ายในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="46820-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="46820-126">รหัสภาษีทั้งหมดที่ป้อนในรายงานค่าใช้จ่ายจะต้องได้รับการยืนยันว่าถูกต้องด้วย</span><span class="sxs-lookup"><span data-stu-id="46820-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="46820-127">หลังจากตรวจสอบข้อกำหนดเหล่านี้แล้ว รายงานค่าใช้จ่ายจะถูกลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="46820-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="46820-128">หลังจากลงรายการบัญชีรายงานค่าใช้จ่าย การชำระเงินจะได้รับอนุญาตสำหรับรายงานค่าใช้จ่ายและพนักงานจะได้รับเงินคืน</span><span class="sxs-lookup"><span data-stu-id="46820-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
