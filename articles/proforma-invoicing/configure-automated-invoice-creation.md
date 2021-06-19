---
title: กำหนดค่าการสร้างใบแจ้งหนี้อัตโนมัติ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีกำหนดค่าระบบเพื่อสร้างใบแจ้งหนี้โดยอัตโนมัติ
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dffa95c163f7f8d5074e02cd56d6f1ed429a7c72
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005364"
---
# <a name="configure-automatic-invoice-creation"></a><span data-ttu-id="e9369-103">กำหนดค่าการสร้างใบแจ้งหนี้อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e9369-103">Configure automatic invoice creation</span></span>

<span data-ttu-id="e9369-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="e9369-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="e9369-105">ทำตามขั้นตอนต่อไปนี้เพื่อกำหนดค่าใบแจ้งหนี้อัตโนมัติที่ใช้งานใน Dynamics 365 Project operations</span><span class="sxs-lookup"><span data-stu-id="e9369-105">Complete the following steps to configure an automated invoice run in Dynamics 365 Project operations.</span></span>

1. <span data-ttu-id="e9369-106">ไปที่ **การตั้งค่า** > **ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="e9369-106">Go to **Settings** > **Batch jobs**.</span></span>
2. <span data-ttu-id="e9369-107">สร้างชุดงาน และตั้งชื่อว่า **Project Operations สร้างใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="e9369-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="e9369-108">ชื่อของชุดงานต้องมีคำว่า "สร้างใบแจ้งหนี้"</span><span class="sxs-lookup"><span data-stu-id="e9369-108">The name of the batch job must include the words "create invoices."</span></span>
3. <span data-ttu-id="e9369-109">ในฟิลด์ **ชนิดงาน** ให้เลือก **ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="e9369-109">In the **Job Type** field, select **None**.</span></span> <span data-ttu-id="e9369-110">โดยค่าเริ่มต้น **ความถี่รายวัน** และตัวเลือก **เปิดใช้งาน** จะถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="e9369-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="e9369-111">เลือก **เรียกใช้เวิร์กโฟลว์**</span><span class="sxs-lookup"><span data-stu-id="e9369-111">Select **Run Workflow**.</span></span> <span data-ttu-id="e9369-112">ในกล่องโต้ตอบ **การค้นหาเรกคอร์ด** คุณจะเห็นสามเวิร์กโฟลว์</span><span class="sxs-lookup"><span data-stu-id="e9369-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="e9369-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="e9369-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="e9369-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="e9369-114">ProcessRunner</span></span>
    - <span data-ttu-id="e9369-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="e9369-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="e9369-116">เลือก **ProcessRunCaller** จากนั้นเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="e9369-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="e9369-117">ในกล่องโต้ตอบถัดไป ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e9369-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="e9369-118">เวิร์กโฟลว์ **การพักเครื่อง** ตามด้วยเวิร์กโฟลว์ **กระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="e9369-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

  > [!NOTE]
  > <span data-ttu-id="e9369-119">นอกจากนี้คุณยังสามารถเลือก **ProcessRunner** ในขั้นตอนที่5</span><span class="sxs-lookup"><span data-stu-id="e9369-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="e9369-120">จากนั้น เมื่อคุณเลือก **ตกลง** เวิร์กโฟลว์ **กระบวนการ** ตามด้วยเวิร์กโฟลว์ **การพักเครื่อง**</span><span class="sxs-lookup"><span data-stu-id="e9369-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="e9369-121">เวิร์กโฟลว์ **ProcessRunCaller** และ **ProcessRunner** สร้างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="e9369-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="e9369-122">**ProcessRunCaller** เรียกใช้ **ProcessRunner**</span><span class="sxs-lookup"><span data-stu-id="e9369-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="e9369-123">**ProcessRunner** เป็นเวิร์กโฟลว์ที่สร้างใบแจ้งหนี้อย่างแท้จริง</span><span class="sxs-lookup"><span data-stu-id="e9369-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="e9369-124">รวมถึงรายละเอียดการให้บริการตามสัญญาทั้งหมดที่ต้องสร้างใบแจ้งหนี้ และจะมีการสร้างใบแจ้งหนี้สำหรับรายละเอียดเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="e9369-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="e9369-125">ในการกำหนดรายละเอียดการให้บริการตามสัญญาที่ต้องสร้างใบแจ้งหนี้ งานจะดูที่วันที่เรียกใช้ใบแจ้งหนี้สำหรับรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="e9369-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="e9369-126">ถ้ารายละเอียดการให้บริการตามสัญญาที่เป็นของสัญญาเดียวมีวันที่เรียกใช้ใบแจ้งหนี้เดียวกัน ธุรกรรมจะรวมอยู่ในใบแจ้งหนี้เดียวที่มีรายการใบแจ้งหนี้สองรายการ</span><span class="sxs-lookup"><span data-stu-id="e9369-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="e9369-127">ถ้าไม่มีธุรกรรมที่จะสร้างใบแจ้งหนี้ งานจะข้ามการสร้างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="e9369-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="e9369-128">หลังจาก **ProcessRunner** เสร็จสิ้น จะเรียก **ProcessRunCaller** ให้เวลาสิ้นสุด และถูกปิด</span><span class="sxs-lookup"><span data-stu-id="e9369-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="e9369-129">**ProcessRunCallerr** เริ่มต้นการจับเวลาที่ทำงานเป็นเวลา 24 ชั่วโมง ตั้งแต่เวลาสิ้นสุดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="e9369-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="e9369-130">ในตอนท้ายของการจับเวลา **ProcessRunCaller** ถูกปิด</span><span class="sxs-lookup"><span data-stu-id="e9369-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="e9369-131">งานกระบวนการชุดงานสำหรับการสร้างใบแจ้งหนี้เป็นงานที่เกิดขึ้นเป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="e9369-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="e9369-132">ถ้ามีการเรียกใช้กระบวนการชุดงานนี้หลายครั้ง จะมีการสร้างหลายอินสแตนซ์ของงาน และทำให้เกิดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="e9369-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="e9369-133">ดังนั้น คุณควรเริ่มต้นกระบวนการชุดงานเพียงครั้งเดียว และคุณควรเริ่มต้นใหม่เฉพาะเมื่อหยุดทำงาน</span><span class="sxs-lookup"><span data-stu-id="e9369-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="e9369-134">การออกใบแจ้งหนี้แบบกลุ่มทำงานเฉพาะสำหรับรายละเอียดการให้บริการตามสัญญาโครงการที่กำหนดค่าโดยกำหนดการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="e9369-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="e9369-135">รายละเอียดการให้บริการตามสัญญาที่มีวิธีการเรียกเก็บเงินแบบราคาคงที่ ต้องมีการกำหนดค่าหลักเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="e9369-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="e9369-136">รายละเอียดการให้บริการตามสัญญาโครงการที่มีวิธีการเรียกเก็บเงินตามเวลาและวัสดุจะต้องมีการตั้งค่ากำหนดการใบแจ้งหนี้ตามวันที่</span><span class="sxs-lookup"><span data-stu-id="e9369-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="e9369-137">เช่นเดียวกับรายละเอียดการให้บริการตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="e9369-137">The same applies to a project-based contract line.</span></span>     


[!INCLUDE[footer-include](../includes/footer-banner.md)]