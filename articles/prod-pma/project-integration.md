---
title: การรวม Microsoft Project Client
description: การวางแผนและการดูแลกำหนดการโครงการอาจมีความซับซ้อน ดังนั้นผู้จัดการโครงการจึงจำเป็นต้องใช้เครื่องมือที่ช่วยจัดการงานนี้ การรวมกับ Microsoft Project Client ให้การสนับสนุนในการเปิดและจัดการโครงสร้างการแบ่งงานโครงการ
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085993"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="25a61-104">การรวม Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="25a61-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25a61-105">การวางแผนและการดูแลกำหนดการโครงการอาจมีความซับซ้อน ดังนั้นผู้จัดการโครงการจึงจำเป็นต้องใช้เครื่องมือที่ช่วยจัดการงานนี้</span><span class="sxs-lookup"><span data-stu-id="25a61-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="25a61-106">การรวมกับ Microsoft Project Client ให้การสนับสนุนในการเปิดและจัดการโครงสร้างการแบ่งงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="25a61-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="25a61-107">ผู้จัดการโครงการสามารถเผยแพร่การเปลี่ยนแปลงใดๆ กลับไปที่โครงสร้างการแบ่งงานโครงการของ Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="25a61-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="25a61-108">หากคุณใช้การอัปเดตเดือนกรกฎาคม (เวอร์ชัน 10.0.4) คุณต้องติดตั้ง KB 4054797 และ 4055884</span><span class="sxs-lookup"><span data-stu-id="25a61-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="25a61-109">กำหนดค่า Add-in ของ Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="25a61-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="25a61-110">ในการเปิดใช้งานการรวมกับ Microsoft Project Client จำเป็นต้องติดตั้ง Add-in Microsoft Dynamics 365 ในแอปพลิเคชัน Microsoft Project ไคลเอ็นต์ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="25a61-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="25a61-111">ทำได้โดยการเปิด **พื้นที่ทำงานการจัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="25a61-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="25a61-112">•   คลิก **กำหนดค่า Add-in ไคลเอนต์โครงการ** จากส่วน **ลิงก์** > **ติดตั้ง** ของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="25a61-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="25a61-113">•   คลิก **เปิด** จากนั้นคลิก **เรียกใช้** เมื่อได้รับแจ้ง</span><span class="sxs-lookup"><span data-stu-id="25a61-113">•   Click **Open** , then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="25a61-114">เปิดและแก้ไขโครงสร้างการแบ่งงานแบบร่างที่มีอยู่ใน Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="25a61-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="25a61-115">หากโครงการใน Dynamics 365 Finance มีโครงสร้างการแบ่งงานที่สร้างขึ้นแล้ว โครงสร้างการแบ่งงานสามารถเปิดได้ในแอปพลิเคชัน Microsoft Project Client หากโครงสร้างการแบ่งงานอยู่ในสถานะแบบร่าง</span><span class="sxs-lookup"><span data-stu-id="25a61-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="25a61-116">เพื่อเปิดจากหน้า **โครงการ** ให้คลิก **เปิดใน Microsoft Project** จากแท็บ **วางแผน** หน้านี้สามารถเปิดได้จากภายในแอปพลิเคชัน Microsoft Project Client โดยคลิก **เปิด** ในแท็บ **Microsoft Dynamics 365** เลือก **นิติบุคคล** และ **โครงการ** จากรายการ</span><span class="sxs-lookup"><span data-stu-id="25a61-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="25a61-117">หากคุณกำลังใช้ Internet Explorer เป็นเบราว์เซอร์ของคุณ คุณจะต้องคลิก **บันทึก** เพื่อเปิดจากตำแหน่งที่ดาวน์โหลดไฟล์ไปด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="25a61-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="25a61-118">หรือคลิก **บันทึกและเปิด** เพื่อเปิดไฟล์ใน Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="25a61-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="25a61-119">อย่าเปลี่ยนชื่อไฟล์เมื่อทำการบันทึก</span><span class="sxs-lookup"><span data-stu-id="25a61-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="25a61-120">ก่อนทำการแก้ไขไฟล์โดยใช้ Microsoft Project Client คุณต้องตรวจสอบก่อน คลิก **เช็คเอาท์** ในแท็บ **Microsoft Dynamics 365** วิธีนี้จะป้องกันไม่ให้ผู้ใช้รายอื่นแก้ไขโครงสร้างการแบ่งงานจากภายใน Finance ในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="25a61-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="25a61-121">หากต้องการเผยแพร่โครงสร้างการแบ่งงานหลังจากแก้ไขเสร็จแล้ว ให้คลิก **เช็คอิน** บนแท็บ **Microsoft Dynamics 365**</span><span class="sxs-lookup"><span data-stu-id="25a61-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="25a61-122">หากเพิ่มทีมโครงการลงในโครงการใน Finance แล้วรายการทรัพยากรจะถูกเติมด้วยสมาชิกในทีม</span><span class="sxs-lookup"><span data-stu-id="25a61-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="25a61-123">หากยังไม่ได้เพิ่มทีมโครงการลงในโครงการ คุณสามารถเลือกทรัพยากรและสร้างทีมภายใน Microsoft Project Client โดยคลิกที่ปุ่ม **ทรัพยากร** บนแท็บ **Microsoft Dynamics 365**</span><span class="sxs-lookup"><span data-stu-id="25a61-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="25a61-124">ข้อมูลต่อไปนี้จะซิงค์กลับไปที่ Finance โดยเป็นส่วนหนึ่งของกระบวนการเช็คอิน:</span><span class="sxs-lookup"><span data-stu-id="25a61-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="25a61-125">•   ชื่องาน</span><span class="sxs-lookup"><span data-stu-id="25a61-125">•   Task name</span></span>

<span data-ttu-id="25a61-126">•   วันที่เริ่ม</span><span class="sxs-lookup"><span data-stu-id="25a61-126">•   Start date</span></span>

<span data-ttu-id="25a61-127">•   วันที่เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="25a61-127">•   Finish date</span></span>

<span data-ttu-id="25a61-128">•   งานที่ต้องทำก่อน</span><span class="sxs-lookup"><span data-stu-id="25a61-128">•   Predecessors</span></span>

<span data-ttu-id="25a61-129">•   ชื่อทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="25a61-129">•   Resource names</span></span>

<span data-ttu-id="25a61-130">•   ประเภท</span><span class="sxs-lookup"><span data-stu-id="25a61-130">•   Category</span></span>

<span data-ttu-id="25a61-131">•   ประเภททรัพยากร</span><span class="sxs-lookup"><span data-stu-id="25a61-131">•   Resource category</span></span>

<span data-ttu-id="25a61-132">•   ชั่วโมงทำงาน:</span><span class="sxs-lookup"><span data-stu-id="25a61-132">•   Work hours</span></span>

<span data-ttu-id="25a61-133">•   บันทึกย่อ</span><span class="sxs-lookup"><span data-stu-id="25a61-133">•   Notes</span></span>

<span data-ttu-id="25a61-134">•   ลำดับความสำคัญ</span><span class="sxs-lookup"><span data-stu-id="25a61-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="25a61-135">หากคุณเพิ่มคอลัมน์อื่นๆ ลงในไฟล์ Microsoft Project Client ของคุณ คอลัมน์เหล่านี้จะไม่ถูกบันทึกลงในไฟล์และจะไม่แสดงเมื่อเปิดไฟล์อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="25a61-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="25a61-136">สร้างโครงสร้างการแบ่งงานสำหรับโครงการที่มีอยู่ โดยใช้ Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="25a61-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="25a61-137">หากต้องการสร้างโครงสร้างการแบ่งงานโดยใช้ Microsoft Project Client ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="25a61-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="25a61-138">เปิด Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="25a61-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="25a61-139">บนแท็บ **Microsoft Dynamics 365** ให้คลิก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="25a61-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="25a61-140">เลือก **นิติบุคคล** สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="25a61-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="25a61-141">เลือก **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="25a61-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="25a61-142">คลิก **เช็คเอาท์** บนแท็บ **Microsoft Dynamics 365**</span><span class="sxs-lookup"><span data-stu-id="25a61-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="25a61-143">เมื่อพร้อมเผยแพร่ไปยัง Finance คลิก **เช็คอิน** บนแท็บ **Microsoft Dynamics 365**</span><span class="sxs-lookup"><span data-stu-id="25a61-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="25a61-144">แทนที่โครงสร้างการแบ่งงานสำหรับโครงการที่มีอยู่ โดยใช้ Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="25a61-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="25a61-145">เมื่อต้องการสร้างโครงสร้างการแบ่งงานใหม่โดยใช้ Microsoft Project Client และแทนที่โครงสร้างการแบ่งงานที่มีอยู่สำหรับโครงการที่มีอยู่ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="25a61-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="25a61-146">เปิด Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="25a61-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="25a61-147">สร้างกำหนดการใน Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="25a61-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="25a61-148">บนแท็บ **Microsoft Dynamics 365** คลิก **บันทึกการเปลี่ยนแปลง** > **แทนที่โครงการที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="25a61-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="25a61-149">เลือก **นิติบุคคล** สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="25a61-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="25a61-150">เลือก **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="25a61-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="25a61-151">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="25a61-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="25a61-152">สร้างโครงการใหม่จากภายใน Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="25a61-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="25a61-153">เปิด Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="25a61-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="25a61-154">สร้างกำหนดการใน Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="25a61-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="25a61-155">บนแท็บ **Microsoft Dynamics 365** คลิก **บันทึกการเปลี่ยนแปลง** > **บันทึกเป็นโครงการใหม่**</span><span class="sxs-lookup"><span data-stu-id="25a61-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="25a61-156">เลือก **นิติบุคคล** สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="25a61-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="25a61-157">ป้อน **รหัสโครงการ** ในกรณีที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="25a61-157">Enter the **Project ID** , if necessary.</span></span>

6.  <span data-ttu-id="25a61-158">ป้อน **ชื่อโครงการ**</span><span class="sxs-lookup"><span data-stu-id="25a61-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="25a61-159">เลือก **ประเภทโครงการ** **กลุ่มโครงการ** และ **รหัสสัญญาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="25a61-159">Select the **Project type** , **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="25a61-160">หรือคุณสามารถสร้างสัญญาโครงการใหม่ได้โดยคลิก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="25a61-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="25a61-161">เลือก **ปฏิทิน** เพื่อใช้ในการจัดหาทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="25a61-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="25a61-162">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="25a61-162">Click **OK**.</span></span>
