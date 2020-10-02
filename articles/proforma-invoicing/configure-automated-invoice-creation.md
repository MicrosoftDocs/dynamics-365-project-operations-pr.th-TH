---
title: กำหนดค่าการสร้างใบแจ้งหนี้อัตโนมัติ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีกำหนดค่าระบบเพื่อสร้างใบแจ้งหนี้โดยอัตโนมัติ
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898149"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="cc8e0-103">กำหนดค่าการสร้างใบแจ้งหนี้อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="cc8e0-103">Configure automated invoice creation</span></span>

<span data-ttu-id="cc8e0-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="cc8e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cc8e0-105">ทำตามขั้นตอนต่อไปนี้เพื่อกำหนดค่าใบแจ้งหนี้อัตโนมัติที่ใช้งานใน Project operations</span><span class="sxs-lookup"><span data-stu-id="cc8e0-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="cc8e0-106">ไปที่ **การตั้งค่า** \> **ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="cc8e0-107">สร้างชุดงาน และตั้งชื่อว่า **Project Operations สร้างใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="cc8e0-108">ชื่อของชุดงานต้องมีคำว่า "สร้างใบแจ้งหนี้"</span><span class="sxs-lookup"><span data-stu-id="cc8e0-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="cc8e0-109">ในฟิลด์ **ชนิดงาน** ให้เลือก **ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="cc8e0-110">โดยค่าเริ่มต้น **ความถี่รายวัน** และตัวเลือก **เปิดใช้งาน** จะถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="cc8e0-111">เลือก **เรียกใช้เวิร์กโฟลว์**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-111">Select **Run Workflow**.</span></span> <span data-ttu-id="cc8e0-112">ในกล่องโต้ตอบ **การค้นหาเรกคอร์ด** คุณจะเห็นสามเวิร์กโฟลว์</span><span class="sxs-lookup"><span data-stu-id="cc8e0-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="cc8e0-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="cc8e0-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="cc8e0-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="cc8e0-114">ProcessRunner</span></span>
    - <span data-ttu-id="cc8e0-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="cc8e0-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="cc8e0-116">เลือก **ProcessRunCaller** จากนั้นเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="cc8e0-117">ในกล่องโต้ตอบถัดไป ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="cc8e0-118">เวิร์กโฟลว์ **การพักเครื่อง** ตามด้วยเวิร์กโฟลว์ **กระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="cc8e0-119">นอกจากนี้คุณยังสามารถเลือก **ProcessRunner** ในขั้นตอนที่5</span><span class="sxs-lookup"><span data-stu-id="cc8e0-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="cc8e0-120">จากนั้น เมื่อคุณเลือก **ตกลง** เวิร์กโฟลว์ **กระบวนการ** ตามด้วยเวิร์กโฟลว์ **การพักเครื่อง**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="cc8e0-121">เวิร์กโฟลว์ **ProcessRunCaller** และ **ProcessRunner** สร้างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="cc8e0-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="cc8e0-122">**ProcessRunCaller** เรียกใช้ **ProcessRunner**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="cc8e0-123">**ProcessRunner** เป็นเวิร์กโฟลว์ที่สร้างใบแจ้งหนี้อย่างแท้จริง</span><span class="sxs-lookup"><span data-stu-id="cc8e0-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="cc8e0-124">รวมถึงรายละเอียดการให้บริการตามสัญญาทั้งหมดที่ต้องสร้างใบแจ้งหนี้ และจะมีการสร้างใบแจ้งหนี้สำหรับรายละเอียดเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="cc8e0-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="cc8e0-125">ในการกำหนดรายละเอียดการให้บริการตามสัญญาที่ต้องสร้างใบแจ้งหนี้ งานจะดูที่วันที่เรียกใช้ใบแจ้งหนี้สำหรับรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="cc8e0-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="cc8e0-126">ถ้ารายละเอียดการให้บริการตามสัญญาที่เป็นของสัญญาเดียวมีวันที่เรียกใช้ใบแจ้งหนี้เดียวกัน ธุรกรรมจะรวมอยู่ในใบแจ้งหนี้เดียวที่มีรายการใบแจ้งหนี้สองรายการ</span><span class="sxs-lookup"><span data-stu-id="cc8e0-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="cc8e0-127">ถ้าไม่มีธุรกรรมที่จะสร้างใบแจ้งหนี้ งานจะข้ามการสร้างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="cc8e0-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="cc8e0-128">หลังจาก **ProcessRunner** เสร็จสิ้น จะเรียก **ProcessRunCaller** ให้เวลาสิ้นสุด และถูกปิด</span><span class="sxs-lookup"><span data-stu-id="cc8e0-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="cc8e0-129">**ProcessRunCallerr** เริ่มต้นการจับเวลาที่ทำงานเป็นเวลา 24 ชั่วโมง ตั้งแต่เวลาสิ้นสุดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="cc8e0-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="cc8e0-130">ในตอนท้ายของการจับเวลา **ProcessRunCaller** ถูกปิด</span><span class="sxs-lookup"><span data-stu-id="cc8e0-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="cc8e0-131">งานกระบวนการชุดงานสำหรับการสร้างใบแจ้งหนี้เป็นงานที่เกิดขึ้นเป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="cc8e0-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="cc8e0-132">ถ้ามีการเรียกใช้กระบวนการชุดงานนี้หลายครั้ง จะมีการสร้างหลายอินสแตนซ์ของงาน และทำให้เกิดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="cc8e0-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="cc8e0-133">ดังนั้น คุณควรเริ่มต้นกระบวนการชุดงานเพียงครั้งเดียว และคุณควรเริ่มต้นใหม่เฉพาะเมื่อหยุดทำงาน</span><span class="sxs-lookup"><span data-stu-id="cc8e0-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="cc8e0-134">การออกใบแจ้งหนี้แบบกลุ่มทำงานเฉพาะสำหรับรายละเอียดการให้บริการตามสัญญาโครงการที่กำหนดค่าโดยกำหนดการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="cc8e0-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="cc8e0-135">รายละเอียดการให้บริการตามสัญญาที่มีวิธีการเรียกเก็บเงินแบบราคาคงที่ ต้องมีการกำหนดค่าเหตุการณ์สำคัญ</span><span class="sxs-lookup"><span data-stu-id="cc8e0-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="cc8e0-136">รายละเอียดการให้บริการตามสัญญาโครงการที่มีวิธีการเรียกเก็บเงินตามเวลาและวัสดุจะต้องมีการตั้งค่ากำหนดการใบแจ้งหนี้ตามวันที่</span><span class="sxs-lookup"><span data-stu-id="cc8e0-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="cc8e0-137">เช่นเดียวกับรายละเอียดการให้บริการตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="cc8e0-137">The same applies to a project-based contract line.</span></span>     
