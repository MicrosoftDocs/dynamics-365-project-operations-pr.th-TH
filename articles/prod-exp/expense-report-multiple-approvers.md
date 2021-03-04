---
title: ผู้อนุมัติหลายรายบนรายงานค่าใช้จ่าย
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับรายงานค่าใช้จ่ายที่ต้องได้รับการอนุมัติจากหลายบุคคล
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960630"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="171e1-103">ผู้อนุมัติหลายรายบนรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="171e1-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="171e1-104">ขึ้นอยู่กับนโยบายการอนุมัติค่าใช้จ่ายขององค์กรของคุณ อาจมีบุคคลมากกว่าหนึ่งคนในการอนุมัติรายงานค่าใช้จ่ายที่ส่งจากพนักงาน</span><span class="sxs-lookup"><span data-stu-id="171e1-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="171e1-105">เมื่อคุณตั้งค่ากระบวนการเวิร์กโฟลว์สำหรับการอนุมัติรายงานค่าใช้จ่าย คุณสามารถเพิ่มองค์ประกอบเวิร์กโฟลว์ที่รวมงานหรือขั้นตอนสำหรับผู้อนุมัติรายงานค่าใช้จ่ายตั้งแต่หนึ่งรายขึ้นไปได้</span><span class="sxs-lookup"><span data-stu-id="171e1-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="171e1-106">ตัวอย่างเช่น คุณอาจกำหนดให้รายงานค่าใช้จ่ายทั้งหมดได้รับการอนุมัติโดยผู้จัดการของพนักงานที่ส่งรายงานก่อน และจากนั้นโดยผู้ประสานงานบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="171e1-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="171e1-107">หากคุณตัดสินใจว่าต้องการผู้อนุมัติรายงานค่าใช้จ่ายหลายคน คุณสามารถเพิ่มองค์ประกอบเวิร์กโฟลว์ด้วยวิธีใดก็ได้ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="171e1-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="171e1-108">เพิ่มองค์ประกอบการอนุมัติหนึ่งรายการที่มีขั้นตอนเดียว</span><span class="sxs-lookup"><span data-stu-id="171e1-108">Add one approval element that has one step.</span></span> <span data-ttu-id="171e1-109">ตัวอย่างเช่น ขั้นตอนดังกล่าวอาจกำหนดให้มีการกำหนดรายงานค่าใช้จ่ายให้กับกลุ่มผู้ใช้ และต้องได้รับการอนุมัติ 50 เปอร์เซ็นต์ของสมาชิกกลุ่มผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="171e1-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="171e1-110">เพิ่มองค์ประกอบการอนุมัติหนึ่งรายการที่มีหลายขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="171e1-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="171e1-111">ตัวอย่างเช่น องค์ประกอบการอนุมัติอาจมีขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="171e1-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="171e1-112">ผู้จัดการของพนักงานที่ส่งรายงานค่าใช้จ่ายเป็นผู้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="171e1-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="171e1-113">เสมียนบัญชีเจ้าหนี้ตรวจสอบใบเสร็จรับเงินและรายการในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="171e1-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="171e1-114">เจ้าของงบประมาณอนุมัติรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="171e1-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="171e1-115">เพิ่มองค์ประกอบการอนุมัติหลายรายการ ซึ่งแต่ละองค์ประกอบมีขั้นตอนเดียว</span><span class="sxs-lookup"><span data-stu-id="171e1-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="171e1-116">ตัวอย่างเช่น คุณอาจเพิ่มองค์ประกอบการอนุมัติแยกต่างหากสำหรับแต่ละขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="171e1-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="171e1-117">ผู้จัดการของพนักงานเป็นผู้อนุมัติรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="171e1-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="171e1-118">เจ้าของงบประมาณอนุมัติรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="171e1-118">The budget owner approves the expense report.</span></span>
