---
title: ค่าใช้จ่ายระหว่างบริษัท
description: พนักงานที่ถูกว่าจ้างโดยนิติบุคคลหนึ่งในองค์กรอาจทำงานให้กับนิติบุคคลอื่นในองค์กรเดียวกัน ในสถานการณ์นี้ คุณสามารถใช้คุณลักษณะค่าใช้จ่ายระหว่างบริษัท เพื่อกำหนดค่าใช้จ่ายของพนักงานให้กับนิติบุคคลที่ดำเนินงาน
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086083"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="72de1-104">ค่าใช้จ่ายระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="72de1-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72de1-105">พนักงานที่ถูกว่าจ้างโดยนิติบุคคลหนึ่งในองค์กรอาจทำงานให้กับนิติบุคคลอื่นในองค์กรเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="72de1-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="72de1-106">ในสถานการณ์นี้ คุณสามารถใช้คุณลักษณะค่าใช้จ่ายระหว่างบริษัท เพื่อกำหนดค่าใช้จ่ายของพนักงานให้กับนิติบุคคลที่ดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="72de1-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="72de1-107">นิติบุคคลที่จ้างพนักงานเรียกว่า นิติบุคคลให้กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="72de1-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="72de1-108">นิติบุคคลที่พนักงานต้องเสียค่าใช้จ่าย เรียกว่า นิติบุคคลที่กู้ยืมเงิน</span><span class="sxs-lookup"><span data-stu-id="72de1-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="72de1-109">ก่อนที่พนักงานจะสามารถสร้างและส่งค่าใช้จ่ายสำหรับงานที่ดำเนินการให้กับนิติบุคคลอื่น ในนิติบุคคลที่ให้กู้ยืมเงินบนหน้า **พารามิเตอร์การจัดการค่าใช้จ่าย** เลือกตัวเลือก **อนุญาตรายการค่าใช้จ่ายระหว่างบริษัท**</span><span class="sxs-lookup"><span data-stu-id="72de1-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="72de1-110">การลงรายการบัญชีภาษีสำหรับค่าใช้จ่ายระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="72de1-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72de1-111">หากคุณต้องการใช้กลุ่มภาษีที่เชื่อมโยงกับนิติบุคคลที่ให้กู้ยืม (ต้นทาง) แทนนิติบุคคลที่กู้ยืมเงิน (ปลายทาง) ในรายงานค่าใช้จ่ายของคุณ คุณจะต้องกำหนดค่านี้ในการตั้งค่าภาษีการขายบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="72de1-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="72de1-112">เมื่อพารามิเตอร์บัญชีแยกประเภททั่วไป **นิติบุคคลสำหรับการลงรายการบัญชีภาษีระหว่างบริษัท** ถูกตั้งค่าเป็น **ที่มา** และ **ใช้กฎการจัดเก็บภาษีการขาย** ถูกตั้งค่าเป็น **ไม่** การรวมภาษีจะใช้สำหรับนิติบุคคลที่ให้กู้ยืมเงิน</span><span class="sxs-lookup"><span data-stu-id="72de1-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="72de1-113">เมื่อพารามิเตอร์เดียวกันถูกตั้งค่าเป็น **ปลายทาง** การรวมภาษีจะใช้สำหรับนิติบุคคลที่กู้ยืมเงิน</span><span class="sxs-lookup"><span data-stu-id="72de1-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="72de1-114">สำหรับนิติบุคคลในสหรัฐอเมริกา เมื่อพารามิเตอร์ถูกตั้งค่าเป็น **ที่มา** ฟิลด์ **ลูกหนี้ภาษีขาย** ต้องกำหนดค่าใหม่บนหน้า **กลุ่มการลงรายการบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="72de1-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="72de1-115">กลไกจัดการบัญชีจะใช้ข้อมูลจากฟิลด์นี้สำหรับรายการบัญชีที่เกี่ยวข้องกับภาษี</span><span class="sxs-lookup"><span data-stu-id="72de1-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="72de1-116">ลักษณะการทำงานสอดคล้องกันสำหรับรายการค่าใช้จ่ายที่ลงรายการบัญชีโดยมีหรือไม่มีโครงการ</span><span class="sxs-lookup"><span data-stu-id="72de1-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
