---
title: สร้างใบแจ้งหนี้ของลูกค้าและผู้ขายระหว่างบริษัท
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีสร้างใบแจ้งหนี้ของลูกค้าและผู้ขายระหว่างบริษัท
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f1560469d2bdbb8e81dc26c16b272c44446ab20a
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595568"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a><span data-ttu-id="4fa3a-103">สร้างใบแจ้งหนี้ของลูกค้าและผู้ขายระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="4fa3a-103">Create intercompany customer and vendor invoices</span></span>

<span data-ttu-id="4fa3a-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="4fa3a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4fa3a-105">นักบัญชีโครงการในนิติบุคคลที่ให้ยืมสร้างใบแจ้งหนี้ของลูกค้าระหว่างบริษัท สำหรับต้นทุนโครงการที่จะถูกโอนไปยังนิติบุคคลที่ยืม</span><span class="sxs-lookup"><span data-stu-id="4fa3a-105">A project accountant in a lending legal entity creates an intercompany customer invoice for the project costs that are being transferred to the borrowing entity.</span></span> <span data-ttu-id="4fa3a-106">หลังจากที่ใบแจ้งหนี้ของลูกค้าระหว่างบริษัทได้รับการอนุมัติและลงรายการบัญชีแล้ว นิติบุคคลที่ให้ยืมจะส่งใบแจ้งหนี้ระหว่างบริษัทไปยังนิติบุคคลที่ยืม</span><span class="sxs-lookup"><span data-stu-id="4fa3a-106">After the intercompany customer invoice is approved and posted, the lending legal entity sends the intercompany invoice to the borrowing legal entity.</span></span>

<span data-ttu-id="4fa3a-107">นักบัญชีโครงการสำหรับนิติบุคคลที่ให้ยืมสามารถตั้งค่ากระบวนการชุดงานเพื่อสร้างใบแจ้งหนี้ระหว่างบริษัทเป็นประจำได้</span><span class="sxs-lookup"><span data-stu-id="4fa3a-107">The project accountant for the lending legal entity can set up a batch process to generate intercompany invoices on a recurring basis.</span></span> <span data-ttu-id="4fa3a-108">นักบัญชีโครงการระบุเกณฑ์ เช่น โครงการเฉพาะ เพื่อสร้างใบแจ้งหนี้ระหว่างบริษัทในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="4fa3a-108">The project accountant specifies the criteria, such as specific projects, to create intercompany invoices in a batch.</span></span>

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a><span data-ttu-id="4fa3a-109">สร้างใบแจ้งหนี้ของลูกค้าระหว่างบริษัทด้วยตนเอง สำหรับธุรกรรมโครงการ</span><span class="sxs-lookup"><span data-stu-id="4fa3a-109">Manually create an intercompany customer invoice for project transactions</span></span> 

<span data-ttu-id="4fa3a-110">ใช้กระบวนการนี้สร้างใบแจ้งหนี้ของลูกค้าระหว่างบริษัทด้วยตนเอง สำหรับธุรกรรมโครงการ</span><span class="sxs-lookup"><span data-stu-id="4fa3a-110">Use this procedure to manually create an intercompany customer invoice for project transactions.</span></span> <span data-ttu-id="4fa3a-111">ค้นหาชั่วโมงที่คนงานโพสต์ในโครงการในนิติบุคคลที่ยืม และค่าใช้จ่ายที่เกิดขึ้นโดยนิติบุคคลของคุณในนามของนิติบุคคลที่ยืม</span><span class="sxs-lookup"><span data-stu-id="4fa3a-111">Search for hours that were posted by workers on projects in the borrowing legal entities and for expenses that were incurred by your legal entity on behalf of borrowing legal entities.</span></span> <span data-ttu-id="4fa3a-112">คุณสามารถค้นหาตามชื่อนิติบุคคล หมายเลขสัญญาโครงการ หมายเลขโครงการ ช่วงวันที่ หรือตัวเลือกเหล่านี้ผสมกัน</span><span class="sxs-lookup"><span data-stu-id="4fa3a-112">You can search by legal entity name, project contract number, project number, date range, or any combination of these options.</span></span> <span data-ttu-id="4fa3a-113">ในผลลัพธ์การค้นหา เลือกธุรกรรมที่จะเพิ่มลงในใบแจ้งหนี้ระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="4fa3a-113">In the search results, select the transactions to add to an intercompany invoice.</span></span>

1. <span data-ttu-id="4fa3a-114">ใน Dynamics 365 Finance ไปที่ **การจัดการโครงการและการบัญชี** > **ใบแจ้งหนี้โครงการ** > **ใบแจ้งหนี้ของลูกค้าระหว่างบริษัท**</span><span class="sxs-lookup"><span data-stu-id="4fa3a-114">In Dynamics 365 Finance, go to **Project management and accounting** > **Project invoices** > **Intercompany customer invoices**.</span></span> <span data-ttu-id="4fa3a-115">บนหน้ารายการ **ใบแจ้งหนี้ของลูกค้าระหว่างบริษัท** บนบานหน้าต่างการดำเนินการ เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="4fa3a-115">On the **Intercompany customer invoices**  list page, on the Action Pane, select **New.**</span></span>
2. <span data-ttu-id="4fa3a-116">บนหน้า **สร้างใบแจ้งหนี้ระหว่างบริษัท** ในฟิลด์ **นิติบุคคล** เลือกนิติบุคคลที่ยืม</span><span class="sxs-lookup"><span data-stu-id="4fa3a-116">On the **Create intercompany invoice** page, in the **Legal entity** field, select a borrowing legal entity.</span></span>
3. <span data-ttu-id="4fa3a-117">ทางเลือก: ป้อนสัญญาโครงการเฉพาะและหมายเลขโครงการ</span><span class="sxs-lookup"><span data-stu-id="4fa3a-117">Optional: Enter a specific project contract and project number.</span></span>
4. <span data-ttu-id="4fa3a-118">จำกัดการค้นหาให้แคบลงโดยเลือกช่วงวันที่</span><span class="sxs-lookup"><span data-stu-id="4fa3a-118">Narrow the search by selecting a date range.</span></span> <span data-ttu-id="4fa3a-119">ป้อนวันที่ที่ต้องการในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="4fa3a-119">Enter specific dates in the **Start date** and **End date** fields.</span></span> <span data-ttu-id="4fa3a-120">เฉพาะธุรกรรมระหว่างบริษัทที่ลงรายการบัญชีภายในช่วงวันที่นี้เท่านั้นที่จะแสดงในผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4fa3a-120">Only intercompany transactions that are posted within this date range are displayed in the search results.</span></span>
5. <span data-ttu-id="4fa3a-121">ตั้งค่า **พารามิเตอร์บรรทัดสมุดรายวันขั้นสูงของโครงการ** เป็น **ใช่** และเลือก **ค้นหา**</span><span class="sxs-lookup"><span data-stu-id="4fa3a-121">Set **Project advanced journal line parameter** to **Yes** and select **Search**.</span></span>
6. <span data-ttu-id="4fa3a-122">ในผลลัพธ์การค้นหา เลือกธุรกรรมที่จะรวมไว้ในข้อเสนอใบแจ้งหนี้ระหว่างบริษัท จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4fa3a-122">In the search results, select the transactions to include in the intercompany invoice proposal, and then select **OK**.</span></span>
7. <span data-ttu-id="4fa3a-123">บนหน้า **ใบแจ้งหนี้ของลูกค้าระหว่างบริษัท** ธุรกรรมโครงการระหว่างบริษัทที่คุณเลือกจากผลการค้นหาจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="4fa3a-123">On the **Intercompany customer invoice** page, the intercompany project transactions that you selected from the search results are displayed.</span></span> <span data-ttu-id="4fa3a-124">ในการแก้ไขธุรกรรมก่อนที่คุณจะส่งใบแจ้งหนี้ไปยังนิติบุคคลที่ยืม ให้ทำดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4fa3a-124">To modify the transactions before you send the invoice to the borrowing legal entity, do the following:</span></span>
  
    1. <span data-ttu-id="4fa3a-125">เปิดหน้า **สร้างข้อเสนอใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="4fa3a-125">Open the **Create invoice proposal** page.</span></span> <span data-ttu-id="4fa3a-126">เลือกธุรกรรมระหว่างบริษัทเพิ่มเติมสำหรับใบแจ้งหนี้ปัจจุบัน จากนั้นเลือก **เพิ่มบรรทัด**</span><span class="sxs-lookup"><span data-stu-id="4fa3a-126">Select additional intercompany transactions for the current invoice, and then select **Add line**.</span></span>
    2. <span data-ttu-id="4fa3a-127">เมื่อต้องการเอาบรรทัดออก ให้เลือกบรรทัด แล้วเลือก **เอาออก**</span><span class="sxs-lookup"><span data-stu-id="4fa3a-127">To remove a line, select it, and then select **Remove**.</span></span>
    3. <span data-ttu-id="4fa3a-128">ดูความคิดเห็น เหตุผล มิติทางการเงิน และข้อมูลอื่นๆ เกี่ยวกับบรรทัดที่เลือกในแท็บด่วน **บรรทัดใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="4fa3a-128">View comments, reasons, financial dimensions, and other information about a selected line on the  **Invoice lines**  FastTab.</span></span>
    
8. <span data-ttu-id="4fa3a-129">การโพสร์ใบแจ้งหนี้ของลูกค้าระหว่างบริษัท บนบานหน้าต่างการดำเนินการ เลือก **โพสต์**</span><span class="sxs-lookup"><span data-stu-id="4fa3a-129">To post the intercompany customer invoice, on the Action Pane, select **Post**.</span></span>

> [!NOTE]
> <span data-ttu-id="4fa3a-130">หากองค์กรของคุณต้องการให้มีการตรวจสอบใบแจ้งหนี้ระหว่างบริษัทก่อนที่จะโพสต์ ผู้ดูแลระบบอาจตั้งค่าเวิร์กโฟลว์สำหรับใบแจ้งหนี้ระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="4fa3a-130">If your organization requires that intercompany invoices be reviewed before they are posted, a system administrator might set up a workflow for intercompany invoices.</span></span> <span data-ttu-id="4fa3a-131">หากไม่ได้ตั้งค่าเวิร์กโฟลว์สำหรับใบแจ้งหนี้ระหว่างบริษัท คุณสามารถโพสต์ใบแจ้งหนี้ระหว่างบริษัทได้</span><span class="sxs-lookup"><span data-stu-id="4fa3a-131">If a workflow is not set up for intercompany invoices, you can post the intercompany invoice.</span></span>

## <a name="create-a-batch-job-for-intercompany-invoices"></a><span data-ttu-id="4fa3a-132">สร้างชุดงานสำหรับใบแจ้งหนี้ระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="4fa3a-132">Create a batch job for intercompany invoices</span></span>

<span data-ttu-id="4fa3a-133">คุณสามารถสร้างใบแจ้งหนี้ระหว่างบริษัทหลายใบในเวลาเดียวกัน สำหรับนิติบุคคลที่ยืมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4fa3a-133">You can create multiple intercompany invoices at the same time for all borrowing legal entities.</span></span> <span data-ttu-id="4fa3a-134">ตัวอย่างเช่น เมื่อใช้ฟังก์ชันการค้นหาคุณสามารถค้นหาธุรกรรมทั้งหมดที่โพสต์โดยคนงานที่ยืมและเกี่ยวข้องกับโครงการที่จัดการโดยนิติบุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="4fa3a-134">Using search functionality, you can for example, search for all transactions that are posted by borrowed workers and related to projects that are managed by other legal entities.</span></span> <span data-ttu-id="4fa3a-135">จากนั้น สำหรับนิติบุคคลที่ยืมแต่ละราย คุณสามารถสร้างใบแจ้งหนี้ระหว่างบริษัทสำหรับธุรกรรมที่ระบุในผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4fa3a-135">Then, for each borrowing legal entity, you can create an intercompany invoice for the transactions provided in the search results.</span></span>

1. <span data-ttu-id="4fa3a-136">ไปที่ **การจัดการโครงการและการบัญชี** > **เป็นระยะ** > **ใบแจ้งหนี้โครงการ** > **สร้างใบแจ้งหนี้ของลูกค้าระหว่างบริษัท**</span><span class="sxs-lookup"><span data-stu-id="4fa3a-136">Go to **Project management and accounting** > **Periodic** > **Project invoices** > **Create intercompany customer invoices**.</span></span>
2. <span data-ttu-id="4fa3a-137">บนหน้า **สร้างใบแจ้งหนี้ของลูกค้าระหว่างบริษัท** ในฟิลด์ **บริษัท**  เลือกนิติบุคคลที่จะออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="4fa3a-137">On the **Create intercompany customer invoices** page, in the **Company**  field, select a legal entity to invoice.</span></span> <span data-ttu-id="4fa3a-138">หากคุณไม่ได้เลือกบริษัท ธุรกรรมทั้งหมดที่ตรงตามเกณฑ์การค้นหาจะแสดงสำหรับนิติบุคคลที่ยืมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4fa3a-138">If you don't select a company, all transactions that meet the search criteria are displayed for all borrowing legal entities.</span></span>
3. <span data-ttu-id="4fa3a-139">ใน **สร้างหนึ่งใบแจ้งหนี้ต่อ** เลือกว่าจะสร้างใบแจ้งหนี้สำหรับธุรกรรมระหว่างบริษัทตามโครงการหรือตามนิติบุคคลที่ยืม</span><span class="sxs-lookup"><span data-stu-id="4fa3a-139">In **Create one invoice per**, select whether to create an invoice for intercompany transactions based on a project or based on a borrowing legal entity.</span></span>
4. <span data-ttu-id="4fa3a-140">ทางเลือก: หากต้องการเลือกโครงการเฉพาะและสัญญาโครงการเพื่อสร้างใบแจ้งหนี้ระหว่างบริษัท ให้คลิก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="4fa3a-140">Optional: To select a specific project and project contract to create intercompany invoices for, click **Select**.</span></span> <span data-ttu-id="4fa3a-141">บนหน้า **สอบถาม** ในฟิลด์ **เกณฑ์** เลือกสัญญาโครงกา รหมายเลขโครงการ หรือทั้งสอง อย่างจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4fa3a-141">On the **Inquiry** page, in the **Criteria** field, select the project contract, project number, or both, and then select **OK**.</span></span>
5. <span data-ttu-id="4fa3a-142">บนแท็บ **ชุดงาน** ตั้งค่ากระบวนการชุดงานเพื่อสร้างใบแจ้งหนี้ระหว่างบริษัทเป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="4fa3a-142">On the **Batch** tab, set up a batch process to create intercompany invoices on a recurring basis.</span></span> <span data-ttu-id="4fa3a-143">สำหรับข้อมูลเพิ่มเติม โปรดดู [ส่งงานการประมวลผลชุดงานจากฟอร์ม](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form)</span><span class="sxs-lookup"><span data-stu-id="4fa3a-143">For more information, see [Submit a batch processing job from a form](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).</span></span>
6. <span data-ttu-id="4fa3a-144">การโพสร์ใบแจ้งหนี้ระหว่างบริษัท บนบานหน้าต่างการดำเนินการ เลือก **โพสต์**</span><span class="sxs-lookup"><span data-stu-id="4fa3a-144">To post the intercompany invoices, on the Action Pane, select **Post**.</span></span>

> [!NOTE]
> <span data-ttu-id="4fa3a-145">หากองค์กรของคุณต้องการให้มีการตรวจสอบใบแจ้งหนี้ระหว่างบริษัทก่อนที่จะโพสต์ ผู้ดูแลระบบอาจตั้งค่าเวิร์กโฟลว์สำหรับใบแจ้งหนี้ระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="4fa3a-145">If your organization requires intercompany invoices be reviewed before they are posted, a system administrator might set up a workflow for intercompany invoices.</span></span> <span data-ttu-id="4fa3a-146">หากไม่ได้ตั้งค่าเวิร์กโฟลว์สำหรับใบแจ้งหนี้ระหว่างบริษัท คุณสามารถโพสต์ใบแจ้งหนี้ระหว่างบริษัทได้</span><span class="sxs-lookup"><span data-stu-id="4fa3a-146">If a workflow is not set up for intercompany invoices, you can post the intercompany invoices.</span></span>

## <a name="post-the-intercompany-vendor-invoice"></a><span data-ttu-id="4fa3a-147">โพสต์ใบแจ้งหนี้ของผู้ขายระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="4fa3a-147">Post the intercompany vendor invoice</span></span>

<span data-ttu-id="4fa3a-148">นักบัญชีโครงการในนิติบุคคลที่ให้ยืมสามารถตรวจสอบใบแจ้งหนี้ของผู้ขายระหว่างบริษัทที่รอดำเนินการได้ เมื่อมีการลงรายการบัญชีใบแจ้งหนี้ของลูกค้าระหว่างบริษัท ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="4fa3a-148">A project accountant in the borrowing legal entity can review intercompany pending vendor invoices when the corresponding intercompany customer invoice is posted.</span></span> <span data-ttu-id="4fa3a-149">ในการเงิน ในนิติบุคคลที่ยืม ไปที่ **บัญชีเจ้าหนี้** > **ใบแจ้งหนี้** > **ใบแจ้งหนี้ของผู้ขายที่รอดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="4fa3a-149">In Finance, in the borrowing legal entity, go to **Accounts payable** > **Invoices** > **Pending vendor invoice**.</span></span> <span data-ttu-id="4fa3a-150">หมายเลขใบแจ้งหนี้ที่รอดำเนินการจะตรงกับหมายเลขใบแจ้งหนี้ของลูกค้าระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="4fa3a-150">The pending invoice number will match the intercompany customer invoice number.</span></span> <span data-ttu-id="4fa3a-151">ตรวจสอบว่าใบแจ้งหนี้ถูกต้อง แล้วโพสต์ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="4fa3a-151">Verify that the invoice is correct and then post the invoice.</span></span> <span data-ttu-id="4fa3a-152">การโพสต์ใบแจ้งหนี้ของผู้ขายระหว่างบริษัท จะสร้างธุรกรรมบัญชีแยกประเภทย่อยของโครงการและบัญชีแยกประเภททั่วไป ที่สะท้อนต้นทุนธุรกรรมในนิติบุคคลที่ยืม</span><span class="sxs-lookup"><span data-stu-id="4fa3a-152">Posting intercompany vendor invoice creates a project subledger and a general ledger transaction that reflects the transaction costs in the borrowing legal entity.</span></span>