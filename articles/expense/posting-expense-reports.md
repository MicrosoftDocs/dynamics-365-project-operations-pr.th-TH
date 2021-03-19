---
title: โพสต์รายงานค่าใช้จ่าย
description: หัวข้อนี้จะอธิบายวิธีการลงรายการบัญชีรายงานค่าใช้จ่าย
author: suvaidya
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: af727e8eb91ff49acb3cc34c225a190f30ba97ed
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276280"
---
# <a name="post-expense-reports"></a><span data-ttu-id="a7895-103">โพสต์รายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a7895-103">Post expense reports</span></span>

<span data-ttu-id="a7895-104">หลังจากรายงานค่าใช้จ่ายได้รับการอนุมัติและโอนไปยังสมุดรายวันทั่วไปแล้ว รายงานสามารถลงรายการบัญชีได้</span><span class="sxs-lookup"><span data-stu-id="a7895-104">After an expense report has been approved and transferred to the general journal, it can be posted.</span></span> <span data-ttu-id="a7895-105">เมื่อคุณลงรายการบัญชีค่าใช้จ่าย จะมีการระบุค่าใช้จ่ายที่สามารถเรียกคืนภาษีมูลค่าเพิ่ม (VAT) ได้</span><span class="sxs-lookup"><span data-stu-id="a7895-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="a7895-106">งานในการตรวจสอบและเรียกคืนการจ่ายภาษีมูลค่าเพิ่มจะมีการมอบหมายให้กับพนักงานที่รับผิดชอบในการตรวจสอบรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a7895-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="a7895-107">หากมีการเรียกเก็บค่าใช้จ่ายในรายงานค่าใช้จ่ายไปยังบริษัทอื่นที่ไม่ใช่บริษัทที่จ้างพนักงาน คุณต้องตรวจสอบทั้งสองบริษัทว่าเป็นหนี้ค่าใช้จ่ายเหล่านั้นและบริษัทที่ค้างชำระ</span><span class="sxs-lookup"><span data-stu-id="a7895-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify both the company that those expenses are owed to and the company that they are owed from.</span></span> <span data-ttu-id="a7895-108">ตัวอย่างเช่น พนักงานที่ส่งรายงานค่าใช้จ่ายทำงานให้กับบริษัท DAT แต่เรียกเก็บเงินจากบริษัท DIR</span><span class="sxs-lookup"><span data-stu-id="a7895-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="a7895-109">ในกรณีนี้ DAT คือบริษัทที่เป็นหนี้ค่าใช้จ่ายและ DIR คือ บริษัทที่ค้างชำระค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="a7895-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="a7895-110">หลังจากที่คุณตรวจสอบบรรทัดสมุดรายวันเหล่านี้ คุณสามารถลงรายการบัญชีรายการค่าใช้จ่ายไปยังบัญชีแยกประเภททั่วไปได้</span><span class="sxs-lookup"><span data-stu-id="a7895-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="a7895-111">หากต้องการลงรายการบัญชีรายงานค่าใช้จ่าย บนเพจ **รายงานค่าใช้จ่ายที่ได้รับอนุมัติ** ให้เลือกรายงานค่าใช้จ่าย จากนั้นบนบานหน้าต่างการดำเนินการ เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="a7895-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="a7895-112">คุณยังสามารถลงรายการบัญชีรายงานค่าใช้จ่ายทั้งหมดในรายการพร้อมกันได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="a7895-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="a7895-113">เลือกรายงานค่าใช้จ่ายทั้งหมด จากนั้นเลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="a7895-113">Select all the expense reports, and then select **Post**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]