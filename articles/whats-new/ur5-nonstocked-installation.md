---
title: อัปเดต Project Operations ในสภาพแวดล้อม Finance ของคุณ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีอัปเดต Project Operations ในสภาพแวดล้อม Dynamics 365 Finance ของคุณ
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 249b8dba17165da04596ec46a625131b9b4daeb5
ms.sourcegitcommit: f4fc6e3a81e8551da050e92f8fde85f8d7b52fbd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/29/2020
ms.locfileid: "4816648"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="174d6-103">อัปเดต Project Operations ในสภาพแวดล้อม Finance ของคุณ</span><span class="sxs-lookup"><span data-stu-id="174d6-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="174d6-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="174d6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="174d6-105">หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีอัปเดต Dynamics 365 Project Operations ในสภาพแวดล้อม Dynamics 365 Finance ของคุณ</span><span class="sxs-lookup"><span data-stu-id="174d6-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="174d6-106">มีสามกระบวนงานที่จำเป็นในการอัปเดต Project Operations เป็น Update 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="174d6-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="174d6-107">นำเข้าแพคเกจไปยังโครงการตัวอย่างของคุณ</span><span class="sxs-lookup"><span data-stu-id="174d6-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="174d6-108">ใช้การปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="174d6-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="174d6-109">อัปเดตสภาพแวดล้อม Dataverse ของคุณ</span><span class="sxs-lookup"><span data-stu-id="174d6-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="174d6-110">นำเข้าแพคเกจไปยังโครงการ LCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="174d6-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="174d6-111">เข้าสู่ระบบ [Lifecycle Services (LCS)](https://lcs.dynamics.com/) ในฐานะเจ้าของโครงการหรือผู้จัดการสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="174d6-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="174d6-112">จากรายการโครงการ เลือกโครงการ LCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="174d6-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="174d6-113">บนหน้า **โครงการ** ในกลุ่ม **สภาพแวดล้อม** เปิดสภาพแวดล้อมที่คุณต้องการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="174d6-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="174d6-114">ตรวจสอบว่าสภาพแวดล้อมกำลังทำงานอยู่</span><span class="sxs-lookup"><span data-stu-id="174d6-114">Verify that the environment is running.</span></span> <span data-ttu-id="174d6-115">หากยังไม่เริ่มต้น ให้เริ่มสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="174d6-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="174d6-116">ในส่วน **รุ่นใหม่** ภายใต้ **การอัปเดตที่มีอยู่** เลือก **ดูการอัปเดต** สำหรับ 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="174d6-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![ดูปุ่มอัปเดต](media/view-update.png)

6. <span data-ttu-id="174d6-118">บนหน้า **การปรับปรุงไบนารี** ให้เลือก **บันทึกแพคเกจ**</span><span class="sxs-lookup"><span data-stu-id="174d6-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="174d6-119">บนหน้า **ตรวจทานและบันทึกอัปเดต** ให้เลือก **บันทึกแพคเกจ**</span><span class="sxs-lookup"><span data-stu-id="174d6-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="174d6-120">บนบานหน้าต่าง **บันทึกแพคเกจลงในไลบรารีสินทรัพย์** ที่เปิดขึ้น ให้ป้อนชื่อแพคเกจแล้วเลือก **บันทึกแพคเกจ**</span><span class="sxs-lookup"><span data-stu-id="174d6-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="174d6-121">เมื่อ LCS บันทึกแพคเกจเสร็จแล้ว ปุ่ม **เสร็จแล้ว** เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="174d6-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="174d6-122">เลือก **สำเร็จ**</span><span class="sxs-lookup"><span data-stu-id="174d6-122">Select **Done**.</span></span> <span data-ttu-id="174d6-123">LCS จะตรวจสอบแพคเกจ</span><span class="sxs-lookup"><span data-stu-id="174d6-123">LCS will verify the package.</span></span> <span data-ttu-id="174d6-124">การยืนยันอาจใช้เวลาสองสามนาทีหรือนานถึงหนึ่งชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="174d6-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="174d6-125">ใช้การปรับปรุงแพคเกจ</span><span class="sxs-lookup"><span data-stu-id="174d6-125">Apply the package update</span></span>

1. <span data-ttu-id="174d6-126">ใน LCS บนหน้า **รายละเอียดสภาพแวดล้อม** ให้เลือก **รักษา** > **ใช้การปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="174d6-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="174d6-127">จากรายการเลือกแพคเกจที่คุณบันทึกไว้ก่อนหน้านี้ จากนั้นเลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="174d6-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="174d6-128">เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการปรับใช้แพคเกจ</span><span class="sxs-lookup"><span data-stu-id="174d6-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![กล่องโต้ตอบยืนยันการปรับใช้แพคเกจ](media/confirm-package-deployment.png)

4. <span data-ttu-id="174d6-130">เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการอัปเดตโปรแกรมประยุกต์</span><span class="sxs-lookup"><span data-stu-id="174d6-130">Select **Yes** to confirm that you want to update the application.</span></span>

![ยืนยันกล่องโต้ตอบการอัปเดตโปรแกรมประยุกต์](media/confirm-application-update.png)

<span data-ttu-id="174d6-132">การปรับใช้และการอัปเดตโปรแกรมประยุกต์จะเริ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="174d6-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="174d6-133">บนหน้า **รายละเอียดสภาพแวดล้อม** ที่มุมบนขวา สถานะสภาพแวดล้อมจะอัปเดตเป็น **บริการ**</span><span class="sxs-lookup"><span data-stu-id="174d6-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="174d6-134">ในเวลาประมาณสองชั่วโมง การอัปเดตจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="174d6-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="174d6-135">ข้อมูลการเปิดตัวโปรแกรมประยุกต์จะอัปเดตเป็น **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** และสถานะสภาพแวดล้อมจะอัปเดตเป็น **ปรับใช้แล้ว**</span><span class="sxs-lookup"><span data-stu-id="174d6-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="174d6-136">อัปเดตสภาพแวดล้อม Dataverse ของคุณ</span><span class="sxs-lookup"><span data-stu-id="174d6-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="174d6-137">ลงชื่อเข้าใช้ใน [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.com/)</span><span class="sxs-lookup"><span data-stu-id="174d6-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="174d6-138">ในรายการ ค้นหาและเปิดสภาพแวดล้อมที่คุณใช้เพื่อติดตั้ง Project Operations</span><span class="sxs-lookup"><span data-stu-id="174d6-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="174d6-139">บนหน้า **สภาพแวดล้อม** ให้เลือก **ทรัพยากร** > **แอป Dynamics 365**</span><span class="sxs-lookup"><span data-stu-id="174d6-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="174d6-140">ในรายการ ค้นหา **Microsoft Dynamics 365 Project Operations** และในคอลัมน์ **สถานะ** เลือก **มีการปรับปรุงที่พร้อมใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="174d6-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="174d6-141">เลือกกล่องกาเครื่องหมาย **ฉันยอมรับข้อตกลงในการให้บริการ** แล้วเลือก **อัปเดต**</span><span class="sxs-lookup"><span data-stu-id="174d6-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="174d6-142">รุ่นล่าสุดของโซลูชันจะได้รับการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="174d6-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="174d6-143">หลังจากการติดตั้งเสร็จสมบูรณ์ คุณจะมีรุ่น 4.5.0.134 ติดตั้งอยู่</span><span class="sxs-lookup"><span data-stu-id="174d6-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="174d6-144">กำหนดค่าคุณลักษณะใหม่</span><span class="sxs-lookup"><span data-stu-id="174d6-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="174d6-145">เปิดใช้งานการเขียนแมปตารางการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="174d6-145">Enable dual-write mapping</span></span>

<span data-ttu-id="174d6-146">หลังจากที่คุณทำการอัปเดต Finance และ Dataverse คุณสามารถเปิดใช้งานการแมปการรวมแบบสองทิศทางที่ต้องการได้</span><span class="sxs-lookup"><span data-stu-id="174d6-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="174d6-147">ดำเนินการกระบวนการต่อไปนี้ให้สำเร็จเพื่อเปิดใช้งานการแมปการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="174d6-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="174d6-148">อัปเดตการตั้งค่าความปลอดภัยบนสภาพแวดล้อม Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="174d6-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="174d6-149">รีเฟรชเอนทิตีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="174d6-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="174d6-150">อัปเดตและเรียกใช้การแมปการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="174d6-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="174d6-151">อัปเดตการตั้งค่าความปลอดภัยบนสภาพแวดล้อม Dataverse</span><span class="sxs-lookup"><span data-stu-id="174d6-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="174d6-152">การอัปเดตต่อไปนี้สำหรับสิทธิ์การใช้งานการรักษาความปลอดภัยสำหรับเอนทิตีเป็นส่วนหนึ่งของการอัปเดตเป็น UR5</span><span class="sxs-lookup"><span data-stu-id="174d6-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="174d6-153">ในสภาพแวดล้อม Dataverse ไปที่ **การตั้งค่า** และในกลุ่ม **ระบบ** เลือก **ความปลอดภัย**</span><span class="sxs-lookup"><span data-stu-id="174d6-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![การตั้งค่าสภาพแวดล้อม Dataverse](media/Picture21.png)

2. <span data-ttu-id="174d6-155">เลือก **Security role**</span><span class="sxs-lookup"><span data-stu-id="174d6-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="174d6-156">จากรายการบทบาท ให้เลือก **ผู้ใช้แอปการรวมแบบสองทิศทาง** และเลือกแท็บ **เอนทิตีที่กำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="174d6-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="174d6-157">ตรวจสอบว่าบทบาทมีสิทธิ์ **อ่าน** และ **ผนวกกับ** สำหรับ:</span><span class="sxs-lookup"><span data-stu-id="174d6-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="174d6-158">**ชนิดอัตราแลกเปลี่ยนสกุลเงิน**</span><span class="sxs-lookup"><span data-stu-id="174d6-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="174d6-159">**ผังบัญชี**</span><span class="sxs-lookup"><span data-stu-id="174d6-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="174d6-160">**ปฏิทินการเงิน**</span><span class="sxs-lookup"><span data-stu-id="174d6-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="174d6-161">**บัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="174d6-161">**Ledger**</span></span>

5. <span data-ttu-id="174d6-162">หลังจากอัปเดตบทบาทความปลอดภัยแล้ว ให้ไปที่ **การตั้งค่า** > **ความปลอดภัย** > **Teams**</span><span class="sxs-lookup"><span data-stu-id="174d6-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="174d6-163">ตรวจสอบว่าบทบาท **ผู้ใช้แอปการรวมแบบสองทิศทาง** ถูกนำไปใช้กับทีม</span><span class="sxs-lookup"><span data-stu-id="174d6-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="174d6-164">รีเฟรชเอนทิตีข้อมูลจากการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="174d6-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="174d6-165">ในสภาพแวดล้อม Finance ของคุณ ให้เปิดพื้นที่ทำงาน **การจัดการข้อมูล** แล้วเปิดหน้า **พารามิเตอร์กรอบงาน**</span><span class="sxs-lookup"><span data-stu-id="174d6-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="174d6-166">บนแท็บ **การตั้งค่าเอนทิตี** เลือก **รีเฟรชรายการเอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="174d6-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="174d6-167">เลือก **ปิด** เพื่อยืนยันการรีเฟรชเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="174d6-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="174d6-168">กระบวนการนี้จะใช้เวลาประมาณ 20 นาที</span><span class="sxs-lookup"><span data-stu-id="174d6-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="174d6-169">คุณจะได้รับแจ้งเมื่อการรีเฟรชเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="174d6-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="174d6-170">อัปเดตการแมปการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="174d6-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="174d6-171">ในพื้นที่ทำงาน **การจัดการข้อมูล** เลือก **การรวมแบบสองทิศทาง**</span><span class="sxs-lookup"><span data-stu-id="174d6-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="174d6-172">เลือก **ใช้โซลูชัน** เลือกทั้งสองวิธีในรายการ จากนั้นเลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="174d6-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="174d6-173">บนหน้า **การรวมแบบสองทิศทาง** เลือกแผนที่ตารางต่อไปนี้ จากนั้นเลือก **หยุด**</span><span class="sxs-lookup"><span data-stu-id="174d6-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="174d6-174">**ข้อมูลจริงของการรวม Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="174d6-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="174d6-175">**ประเภทค่าใช้จ่ายโครงการการรวม Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="174d6-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="174d6-176">**เอนทิตีการส่งออกค่าใช้จ่ายโครงการข้อมูลจริงของการรวม Project Operations (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="174d6-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="174d6-177">บนหน้า **รุ่นแผนที่ตาราง** ใช้รุ่นใหม่ของแผนที่กับแต่ละเอนทิตีทั้งสาม</span><span class="sxs-lookup"><span data-stu-id="174d6-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="174d6-178">บนหน้า **การรวมแบบสองทิศทาง** เลือกรันเพื่อรีสตาร์ทแผนที่</span><span class="sxs-lookup"><span data-stu-id="174d6-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="174d6-179">จากรายการแผนที่ เลือกแมป **บัญชีแยกประเภท (msdyn_ledgers)** ด้วยข้อกำหนดเบื้องต้นทั้งหมดและเลือกกล่องกาเครื่องหมาย **การทำข้อมูลให้ตรงกันครั้งแรก**</span><span class="sxs-lookup"><span data-stu-id="174d6-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="174d6-180">ในฟิลด์ **ข้อมูลหลักสำหรับการทำข้อมูลให้ตรงกันครั้งแรก** ให้เลือก **แอป Finance and Operations** จากนั้นเลือก **เรียกใช้**</span><span class="sxs-lookup"><span data-stu-id="174d6-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![การทำข้อมูลแมปบัญชีแยกประเภทให้ตรงกัน](media/DW6.png)
 
