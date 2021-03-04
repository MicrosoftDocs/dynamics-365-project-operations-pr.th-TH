---
title: โพสต์รายงานค่าใช้จ่าย
description: หัวข้อนี้อธิบายถึงวิธีการลงรายการบัญชีรายงานค่าใช้จ่ายไปยังบัญชีแยกประเภททั่วไป
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 982b7621c35547448b5d756f77f3873b9fbbcb9d
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960135"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="b21c5-103">โพสต์รายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="b21c5-103">Post an expense report</span></span>

<span data-ttu-id="b21c5-104">หลังจากรายงานค่าใช้จ่ายได้รับการอนุมัติและโอนไปยังสมุดรายวันทั่วไปแล้ว รายงานสามารถลงรายการบัญชีแยกประเภททั่วไปได้</span><span class="sxs-lookup"><span data-stu-id="b21c5-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="b21c5-105">เมื่อคุณลงรายการบัญชีค่าใช้จ่าย จะมีการระบุค่าใช้จ่ายที่สามารถเรียกคืนภาษีมูลค่าเพิ่ม (VAT) ได้</span><span class="sxs-lookup"><span data-stu-id="b21c5-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="b21c5-106">งานในการตรวจสอบและเรียกคืนการจ่ายภาษีมูลค่าเพิ่มจะมีการมอบหมายให้กับพนักงานที่รับผิดชอบในการตรวจสอบรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="b21c5-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="b21c5-107">หากมีการเรียกเก็บค่าใช้จ่ายในรายงานค่าใช้จ่ายไปยังบริษัทอื่นที่ไม่ใช่บริษัทที่จ้างพนักงาน คุณต้องตรวจสอบบริษัทว่าเป็นหนี้ค่าใช้จ่ายเหล่านั้นและบริษัทที่ค้างชำระ</span><span class="sxs-lookup"><span data-stu-id="b21c5-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="b21c5-108">ตัวอย่างเช่น พนักงานที่ส่งรายงานค่าใช้จ่ายทำงานให้กับบริษัท DAT แต่เรียกเก็บเงินจากบริษัท DIR</span><span class="sxs-lookup"><span data-stu-id="b21c5-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="b21c5-109">ในกรณีนี้ DAT คือบริษัทที่เป็นหนี้ค่าใช้จ่ายและ DIR คือ บริษัทที่ค้างชำระค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="b21c5-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="b21c5-110">หลังจากที่คุณตรวจสอบบรรทัดสมุดรายวันเหล่านี้ คุณสามารถลงรายการบัญชีรายการค่าใช้จ่ายไปยังบัญชีแยกประเภททั่วไปได้</span><span class="sxs-lookup"><span data-stu-id="b21c5-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="b21c5-111">หากต้องการลงรายการบัญชีรายงานค่าใช้จ่าย บนเพจ **รายงานค่าใช้จ่ายที่ได้รับอนุมัติ** ให้เลือกรายงานค่าใช้จ่าย จากนั้นบนบานหน้าต่างการดำเนินการ เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="b21c5-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="b21c5-112">คุณยังสามารถลงรายการบัญชีรายงานค่าใช้จ่ายทั้งหมดในรายการพร้อมกันได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="b21c5-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="b21c5-113">เลือกรายงานค่าใช้จ่ายทั้งหมด จากนั้นเลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="b21c5-113">Select all the expense reports, and then select **Post**.</span></span>
