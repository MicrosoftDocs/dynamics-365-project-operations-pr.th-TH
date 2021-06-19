---
title: ทำงานกับค่าใช้จ่ายส่วนบุคคลในรายงานค่าใช้จ่าย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการทำงานโดยมีค่าใช้จ่ายส่วนบุคคลที่เกิดขึ้นกับพนักงาน ขณะที่เดินทางเพื่อจุดประสงค์ทางธุรกิจ
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025707"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="f2b71-103">ทำงานกับค่าใช้จ่ายส่วนบุคคลในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="f2b71-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="f2b71-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="f2b71-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f2b71-105">ในระหว่างการเดินทางเพื่อธุรกิจ พนักงานอาจเรียกเก็บค่าใช้จ่ายส่วนบุคคลจากบัตรเครดิตของบริษัทของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="f2b71-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="f2b71-106">หากไม่ได้กำหนดกระบวนการสำหรับจัดการค่าใช้จ่ายส่วนบุคคล กระบวนการอนุมัติรายงานค่าใช้จ่ายอาจหยุดชะงัก เมื่อพนักงานส่งรายงานค่าใช้จ่ายแบบแยกรายการของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="f2b71-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="f2b71-107">มีวิธีสองวิธีที่คุณสามารถใช้เพื่อทำงานกับค่าใช้จ่ายส่วนบุคคลของพนักงาน:</span><span class="sxs-lookup"><span data-stu-id="f2b71-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="f2b71-108">**จ่ายโดยพนักงาน**: องค์กรของคุณไม่จ่ายค่าใช้จ่ายส่วนบุคคลที่ปรากฏในใบเรียกเก็บเงินสำหรับบัตรเครดิตขององค์กร</span><span class="sxs-lookup"><span data-stu-id="f2b71-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="f2b71-109">แต่พนักงานจะจ่ายให้กับผู้จำหน่ายบัตรเครดิตโดยตรงสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="f2b71-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="f2b71-110">**จ่ายโดยบริษัท**: องค์กรของคุณจ่ายค่าบัตรเครดิตของบริษัทเต็มจำนวน และจากนั้น จะหักเงินจากบัญชีของพนักงานเป็นค่าใช้จ่ายส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="f2b71-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="f2b71-111">คุณสามารถเลือกวิธีการที่องค์กรของคุณใช้ในหน้า **พารามิเตอร์การจัดการค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="f2b71-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="f2b71-112">เปิดใช้งานฟังก์ชันแยกค่าใช้จ่ายเมื่อฟิลด์ยอดเงินส่วนบุคคลมีค่าที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="f2b71-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="f2b71-113">คุณลักษณะ **เปิดใช้งานฟังก์ชันแยกค่าใช้จ่ายเมื่อฟิลด์ยอดเงินส่วนบุคคลมีค่าที่กำหนดไว้** นำไปใช้กับรายงานค่าใช้จ่ายที่ได้รับอนุมัติโดยใช้เวิร์กโฟลว์ระดับรายการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f2b71-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="f2b71-114">รายงานได้รับการอนุมัติโดยไปที่ **ประมวลผลรายงานค่าใช้จ่าย** > **รายงานค่าใช้จ่ายที่ได้รับมอบหมายให้ฉัน** > **เปิดรายงานค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="f2b71-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="f2b71-115">หากต้องการเปิดใช้งานคุณสมบัตินี้ ให้ไปที่ **พื้นที่ทำงาน** > **การจัดการคุณสมบัติ** เลือก **เปิดใช้งานฟังก์ชันแยกค่าใช้จ่ายเมื่อฟิลด์ยอดเงินส่วนบุคคลมีค่าที่กำหนดไว้** แล้วเลือก **เปิดใช้งานทันที**</span><span class="sxs-lookup"><span data-stu-id="f2b71-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="f2b71-116">เมื่อเปิดใช้งานคุณลักษณะ รายการค่าใช้จ่ายที่ใช้ฟังก์ชันนี้จะสร้างสองรายการเมื่อส่งรายงาน</span><span class="sxs-lookup"><span data-stu-id="f2b71-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="f2b71-117">มีการสร้างสองบรรทัดเพื่อให้ผู้อนุมัติสามารถอนุมัติแต่ละบรรทัดแยกกัน</span><span class="sxs-lookup"><span data-stu-id="f2b71-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
