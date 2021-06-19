---
title: ค่าใช้จ่ายระหว่างบริษัท
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการใช้ค่าใช้จ่ายระหว่างบริษัท เพื่อมอบหมายค่าใช้จ่ายของผู้ปฏิบัติงานให้กับนิติบุคคลที่ทำการดำเนินงาน
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005094"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="c1db7-103">ค่าใช้จ่ายระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="c1db7-103">Intercompany expenses</span></span>

<span data-ttu-id="c1db7-104">พนักงานที่ถูกว่าจ้างโดยนิติบุคคลหนึ่งในองค์กรอาจทำงานให้กับนิติบุคคลอื่นในองค์กรเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="c1db7-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="c1db7-105">คุณสามารถใช้ค่าใช้จ่ายระหว่างบริษัท เพื่อมอบหมายค่าใช้จ่ายของผู้ปฏิบัติงานให้กับนิติบุคคลที่ทำการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="c1db7-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="c1db7-106">นิติบุคคลที่จ้างพนักงานเรียกว่า นิติบุคคลให้กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="c1db7-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="c1db7-107">นิติบุคคลที่พนักงานต้องเสียค่าใช้จ่าย เรียกว่า นิติบุคคลที่กู้ยืมเงิน</span><span class="sxs-lookup"><span data-stu-id="c1db7-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="c1db7-108">ก่อนที่พนักงานจะสามารถสร้างและส่งค่าใช้จ่ายระหว่างบริษัท คุณต้องเปิดใช้งานรายการค่าใช้จ่ายระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="c1db7-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="c1db7-109">ในนิติบุคคลที่ให้กู้ยืม บนหน้า **พารามิเตอร์การจัดการค่าใช้จ่าย** ให้เลือก **อนุญาตรายการค่าใช้จ่ายระหว่างบริษัท**</span><span class="sxs-lookup"><span data-stu-id="c1db7-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="c1db7-110">การลงรายการบัญชีภาษีสำหรับค่าใช้จ่ายระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="c1db7-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1db7-111">ก่อนที่คุณจะสามารถใช้กลุ่มภาษีที่เชื่อมโยงกับนิติบุคคลที่ให้กู้ยืม (ต้นทาง) แทนนิติบุคคลที่ยืม (ปลายทาง) ในรายงานค่าใช้จ่ายของคุณ คุณต้องเปิดใช้งานฟังก์ชันในการตั้งค่าภาษีขายบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="c1db7-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="c1db7-112">เมื่อพารามิเตอร์ **นิติบุคคลสำหรับการลงรายการบัญชีภาษีระหว่างบริษัท** ถูกตั้งค่าเป็น **ที่มา** และ **ใช้กฎการจัดเก็บภาษีขาย** ถูกตั้งค่าเป็น **ไม่** จะมีการใช้การรวมภาษีสำหรับนิติบุคคลที่ให้กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="c1db7-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="c1db7-113">เมื่อพารามิเตอร์เดียวกันถูกตั้งค่าเป็น **ปลายทาง** การรวมภาษีจะใช้สำหรับนิติบุคคลที่กู้ยืมเงิน</span><span class="sxs-lookup"><span data-stu-id="c1db7-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="c1db7-114">สำหรับนิติบุคคลในสหรัฐอเมริกา เมื่อพารามิเตอร์ถูกตั้งค่าเป็น **ที่มา** ฟิลด์ **ลูกหนี้ภาษีขาย** ต้องกำหนดค่าใหม่บนหน้า **กลุ่มการลงรายการบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="c1db7-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="c1db7-115">เอ็นจินการบัญชีจะใช้ข้อมูลจากฟิลด์นี้สำหรับรายการบัญชีที่เกี่ยวข้องกับภาษี</span><span class="sxs-lookup"><span data-stu-id="c1db7-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="c1db7-116">ลักษณะการทำงานสอดคล้องกันสำหรับรายการค่าใช้จ่ายที่ลงรายการบัญชีโดยมีหรือไม่มีโครงการ</span><span class="sxs-lookup"><span data-stu-id="c1db7-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]