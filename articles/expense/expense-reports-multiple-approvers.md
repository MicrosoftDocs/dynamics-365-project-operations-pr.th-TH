---
title: รายงานค่าใช้จ่ายและผู้อนุมัติหลายราย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับรายงานค่าใช้จ่ายที่ต้องได้รับการอนุมัติจากบุคคลมากกว่าหนึ่งคน
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2502b2975ad3aebad720970e693ea68eac0a302c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002079"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="47277-103">รายงานค่าใช้จ่ายและผู้อนุมัติหลายราย</span><span class="sxs-lookup"><span data-stu-id="47277-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="47277-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="47277-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="47277-105">ขึ้นอยู่กับนโยบายการอนุมัติค่าใช้จ่ายขององค์กรของคุณ อาจมีบุคคลมากกว่าหนึ่งคนในการอนุมัติรายงานค่าใช้จ่ายที่ส่งมา</span><span class="sxs-lookup"><span data-stu-id="47277-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="47277-106">เมื่อคุณตั้งค่ากระบวนการเวิร์กโฟลว์สำหรับการอนุมัติรายงานค่าใช้จ่าย คุณสามารถเพิ่มองค์ประกอบเวิร์กโฟลว์ที่รวมงานหรือขั้นตอนสำหรับผู้อนุมัติรายงานค่าใช้จ่ายตั้งแต่หนึ่งรายขึ้นไปได้</span><span class="sxs-lookup"><span data-stu-id="47277-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="47277-107">ตัวอย่างเช่น คุณอาจกำหนดให้รายงานค่าใช้จ่ายทั้งหมดได้รับการอนุมัติโดยบุคคลสองคนที่แยกจากกัน ผู้จัดการของพนักงานที่ส่งรายงาน และผู้ประสานงานบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="47277-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="47277-108">หากคุณตัดสินใจว่าต้องการผู้อนุมัติรายงานค่าใช้จ่ายหลายคน คุณสามารถเพิ่มองค์ประกอบเวิร์กโฟลว์ด้วยวิธีใดก็ได้ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="47277-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="47277-109">เพิ่มองค์ประกอบการอนุมัติหนึ่งรายการที่มีขั้นตอนเดียว</span><span class="sxs-lookup"><span data-stu-id="47277-109">Add one approval element that has one step.</span></span> <span data-ttu-id="47277-110">ตัวอย่างเช่น ขั้นตอนดังกล่าวอาจกำหนดให้มีการกำหนดรายงานค่าใช้จ่ายให้กับกลุ่มผู้ใช้ และต้องได้รับการอนุมัติ 50 เปอร์เซ็นต์ของสมาชิกกลุ่มผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="47277-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="47277-111">เพิ่มองค์ประกอบการอนุมัติหนึ่งรายการที่มีหลายขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="47277-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="47277-112">ตัวอย่างเช่น องค์ประกอบการอนุมัติอาจมีขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="47277-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="47277-113">ผู้จัดการของพนักงานที่ส่งรายงานค่าใช้จ่ายเป็นผู้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="47277-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="47277-114">เสมียนบัญชีเจ้าหนี้ตรวจสอบใบเสร็จรับเงินและรายการในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="47277-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="47277-115">เจ้าของงบประมาณอนุมัติรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="47277-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="47277-116">เพิ่มองค์ประกอบการอนุมัติหลายรายการ ซึ่งแต่ละองค์ประกอบมีขั้นตอนเดียว</span><span class="sxs-lookup"><span data-stu-id="47277-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="47277-117">ตัวอย่างเช่น คุณอาจเพิ่มองค์ประกอบการอนุมัติแยกต่างหากสำหรับแต่ละขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="47277-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="47277-118">ผู้จัดการของพนักงานเป็นผู้อนุมัติรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="47277-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="47277-119">เจ้าของงบประมาณอนุมัติรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="47277-119">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]