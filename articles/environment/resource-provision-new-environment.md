---
title: เตรียมใช้งานสภาพแวดล้อมใหม่
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการเตรียมใช้งานสภาพแวดล้อม Project Operations ของคุณ
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ee9e4c31d1972e3a75ad214071b31527f0ca826
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950557"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="2aa79-103">เตรียมใช้งานสภาพแวดล้อมใหม่</span><span class="sxs-lookup"><span data-stu-id="2aa79-103">Provision a new environment</span></span>

<span data-ttu-id="2aa79-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="2aa79-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2aa79-105">หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการเตรียมใช้งานสภาพแวดล้อม Dynamics 365 Project Operations ใหม่สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="2aa79-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="2aa79-106">เปิดใช้งานการเตรียมใช้งานอัตโนมัติของ Project Operations ในโครงการ LCS</span><span class="sxs-lookup"><span data-stu-id="2aa79-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="2aa79-107">ใช้ขั้นตอนต่อไปนี้เพื่อเปิดใช้งานขั้นตอนการเตรียมใช้งานอัตโนมัติของ Project Operations สำหรับโครงการ LCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2aa79-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="2aa79-108">ไปที่ [LCS](https://lcs.dynamics.com/v2) และเลือกไทล์ **การจัดการคุณลักษณะพรีวิว**</span><span class="sxs-lookup"><span data-stu-id="2aa79-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="2aa79-109">ในรายการ **คุณลักษณะพรีวิว** เลือก **คุณลักษณะ Project Operations** และเลือก **เปิดใช้คุณลักษณะพรีวิวแล้ว** เพื่อเปิดใช้งาน Project Operations</span><span class="sxs-lookup"><span data-stu-id="2aa79-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="2aa79-110">ขั้นตอนนี้ดำเนินการเพียงครั้งเดียวต่อโครงการ LCS</span><span class="sxs-lookup"><span data-stu-id="2aa79-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="2aa79-111">เตรียมใช้งานสภาพแวดล้อม Project Operations</span><span class="sxs-lookup"><span data-stu-id="2aa79-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="2aa79-112">เปิดการปรับใช้งาน Dynamics 365 Finance [สภาพแวดล้อมสาธิต](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) หรือ [sandbox/ สภาพแวดล้อมการทำงานจริง](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure)</span><span class="sxs-lookup"><span data-stu-id="2aa79-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="2aa79-113">ดำเนินการตามวิซาร์ด **การเตรียมใช้งานสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="2aa79-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="2aa79-114">ตรวจสอบว่าเวอร์ชันของแอปพลิเคชันที่เลือกคือ 10.0.13 หรือสูงกว่า</span><span class="sxs-lookup"><span data-stu-id="2aa79-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="2aa79-115">เพื่อเตรียมใช้งาน Project Operations ภายใต้ **การตั้งค่าขั้นสูง** เลือก **Common Data Service**</span><span class="sxs-lookup"><span data-stu-id="2aa79-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="2aa79-116">เปิดใช้งาน **การตั้งค่า Common Data Service** โดยการเลือก **ใช่** จากนั้นป้อนข้อมูลในฟิลด์ที่จำเป็น:</span><span class="sxs-lookup"><span data-stu-id="2aa79-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="2aa79-117">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="2aa79-117">Name</span></span>
  - <span data-ttu-id="2aa79-118">ขอบเขต</span><span class="sxs-lookup"><span data-stu-id="2aa79-118">Region</span></span>
  - <span data-ttu-id="2aa79-119">ภาษา</span><span class="sxs-lookup"><span data-stu-id="2aa79-119">Language</span></span>
  - <span data-ttu-id="2aa79-120">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="2aa79-120">Currency</span></span>
 
5. <span data-ttu-id="2aa79-121">ในฟิลด์ **แม่แบบ Common Data Service** ให้เลือก **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="2aa79-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="2aa79-122">เลือกชนิดชนิดสภาพแวดล้อมสำหรับการปรับใช้งานของคุณ</span><span class="sxs-lookup"><span data-stu-id="2aa79-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="2aa79-123">การทดลองใช้ตามการสมัครใช้งานจะช่วยให้คุณสามารถปรับใช้งานสภาพแวดล้อม CDS เป็นเวลา 30 วัน</span><span class="sxs-lookup"><span data-stu-id="2aa79-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![การตั้งค่าการปรับใช้งาน](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="2aa79-125">เลือก **ตกลง** เพื่อรับทราบข้อกำหนดในการให้บริการ จากนั้นเลือก **เสร็จแล้ว** เพื่อกลับไปที่การตั้งค่าการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2aa79-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![การยินยอมการปรับใช้งาน](./media/2DeploymentConsent.png)

7. <span data-ttu-id="2aa79-127">ทางเลือก - ใช้ข้อมูลสาธิตกับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="2aa79-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="2aa79-128">ไปที่ **การตั้งค่าขั้นสูง** เลือก **ปรับแต่งการตั้งค่าคอนฟิกฐานข้อมูล SQL** และตั้งค่า **ระบุชุดข้อมูลสำหรับฐานข้อมูลแอปพลิเคชัน** เป็น **การสาธิต**</span><span class="sxs-lookup"><span data-stu-id="2aa79-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="2aa79-129">กรอกข้อมูลในฟิลด์ที่จำเป็นที่เหลือในวิซาร์ดและยืนยันการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2aa79-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="2aa79-130">เวลาในการจัดเตรียมสภาพแวดล้อมจะแตกต่างกันไปตามชนิดสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="2aa79-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="2aa79-131">การเตรียมใช้งานอาจใช้เวลาถึงหกชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="2aa79-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="2aa79-132">หลังจากการปรับใช้งานเสร็จสมบูรณ์ สภาพแวดล้อมจะแสดงเป็น **ปรับใช้งานแล้ว**</span><span class="sxs-lookup"><span data-stu-id="2aa79-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="2aa79-133">เพื่อยืนยันว่าสภาพแวดล้อมได้ปรับใช้เรียบร้อยแล้ว ให้เลือก **เข้าสู่ระบบ** และเข้าสู่ระบบเพื่อยืนยัน</span><span class="sxs-lookup"><span data-stu-id="2aa79-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![ รายละเอียดสภาพแวดล้อม](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="2aa79-135">ใช้การปรับปรุงกับสภาพแวดล้อม Finance</span><span class="sxs-lookup"><span data-stu-id="2aa79-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="2aa79-136">Project Operations ต้องการสภาพแวดล้อม Finance ที่มีเวอร์ชันของแอปพลิเคชัน **10.0.13 (10.0.569.20009)** หรือสูงกว่า</span><span class="sxs-lookup"><span data-stu-id="2aa79-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="2aa79-137">คุณอาจต้องใช้การปรับปรุงคุณภาพกับสภาพแวดล้อม Finance ของคุณเพื่อรับเวอร์ชันนี้</span><span class="sxs-lookup"><span data-stu-id="2aa79-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="2aa79-138">ใน LCS บนเพจ **รายละเอียดสภาพแวดล้อม** ใน **การปรับปรุงที่มีอยู่** ให้เลือก **ดูการปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="2aa79-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![ดูการปรับปรุง](./media/5ViewUpdates.png)

2. <span data-ttu-id="2aa79-140">บนเพจ **การปรับปรุงไบนารี** ให้เลือก **บันทึกแพคเกจ**</span><span class="sxs-lookup"><span data-stu-id="2aa79-140">On the **Binary updates** page, select **Save package.**</span></span>

![บันทึกแพคเกจ](./media/6SavePackage.png)

3. <span data-ttu-id="2aa79-142">คลิก **เลือกทั้งหมด** แล้วเลือก **บันทึกแพคเกจ**</span><span class="sxs-lookup"><span data-stu-id="2aa79-142">Click **Select all** and then select **Save package**.</span></span>

![ตรวจทานและบันทึกการปรับปรุง](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="2aa79-144">ป้อนชื่อและคำอธิบายของแพคเกจ จากนั้นเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="2aa79-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="2aa79-145">กระบวนการนี้อาจใช้เวลาสักครู่ ทั้งนี้ขึ้นอยู่กับการเชื่อมต่ออินเทอร์เน็ต</span><span class="sxs-lookup"><span data-stu-id="2aa79-145">Depending on the internet connection, this process might take some time.</span></span>

![อัปโหลดแพคเกจไปยังแอสเซทไลบรารี](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="2aa79-147">หลังจากบันทึกแพคเกจแล้ว ให้เลือก **เสร็จแล้ว** และบันทึกแพคเกจนี้ลงในแอสเซทไลบรารีในโครงการ LCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2aa79-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="2aa79-148">การบันทึกและตรวจสอบความถูกต้องของแพคเกจอาจใช้เวลาประมาณ 15 นาที</span><span class="sxs-lookup"><span data-stu-id="2aa79-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="2aa79-149">หากต้องการใช้การปรับปรุง ให้ไปที่เพจ **รายละเอียดสภาพแวดล้อม** ใน LCS และเลือก **รักษา** > **ใช้การปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="2aa79-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![รักษาสภาพแวดล้อม](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="2aa79-151">ในรายการปรับปรุง ให้เลือกแพคเกจที่คุณสร้าง และเลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="2aa79-151">In the updates list select the package you created, and select **Apply**.</span></span>

![ใช้การปรับปรุง](./media/10ApplyUpdates.png)

<span data-ttu-id="2aa79-153">การดูแลสภาพแวดล้อมจะใช้เวลาพอสมควร</span><span class="sxs-lookup"><span data-stu-id="2aa79-153">Environment servicing will take some time.</span></span> <span data-ttu-id="2aa79-154">หลังจากเสร็จสิ้น สภาพแวดล้อมจะคืนกลับสู่สถานะที่ปรับใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="2aa79-154">After it is complete, the environment will return to a deployed state.</span></span>

![ปรับใช้งานสภาพแวดล้อมแล้ว](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="2aa79-156">สร้างการเชื่อมต่อการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="2aa79-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="2aa79-157">ในโครงการ LCS ของคุณ ไปที่เพจ **รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="2aa79-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="2aa79-158">ภายใต้ **ข้อมูลสภาพแวดล้อม Common Data Service** เลือก **ลิงก์ไปยัง CDS สำหรับแอป**</span><span class="sxs-lookup"><span data-stu-id="2aa79-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="2aa79-159">หลังจากลิงก์เสร็จสมบูรณ์ ให้เลือก **ลิงก์ไปยัง CDS สำหรับแอป** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="2aa79-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="2aa79-160">คุณจะได้รับการเปลี่ยนเส้นทางไปยังการรวมแบบสองทิศทางใน Finance</span><span class="sxs-lookup"><span data-stu-id="2aa79-160">You will be redirected to Dual Write in Finance.</span></span>

![เชื่อมโยงไปยัง CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="2aa79-162">เลือก **ใช้โซลูชัน** เพื่อเข้าถึงเอนทิตีที่จะถูกแม็ปในการรวม</span><span class="sxs-lookup"><span data-stu-id="2aa79-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![ใช้โซลูชัน](./media/13ApplySolutions.png)

5. <span data-ttu-id="2aa79-164">เลือกทั้งสองโซลูชัน **แผนที่เอนทิตีแบบสองทิศทางของ Dynamics 365 Finance and Operations** และ **แผนที่เอนทิตีแบบสองทิศทางของ Dynamics 365 Project Operations** แล้วเลือก **สมัคร**</span><span class="sxs-lookup"><span data-stu-id="2aa79-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![ยืนยันโซลูชัน](./media/14ConfirmSolutions.png)

<span data-ttu-id="2aa79-166">หลังจากใช้โซลูชันแล้ว เอนทิตีการรวมแบบสองทิศทางจะมีการนำไปใช้กับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="2aa79-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![การใช้โซลูชัน](./media/15ApplyingSolutions.png)

<span data-ttu-id="2aa79-168">หลังจากใช้เอนทิตีแล้ว การแม็ปที่มีอยู่ทั้งหมดจะแสดงรายการในสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="2aa79-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![การแม็ปการรวมแบบสองทิศทาง](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="2aa79-170">รีเฟรชเอนทิตีข้อมูลหลังการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="2aa79-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="2aa79-171">ใน Finance ไปที่พื้นที่ทำงาน **การจัดการข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="2aa79-171">In Finance, go to the **Data management** workspace.</span></span>

![พื้นที่ทำงานการจัดการข้อมูล](./media/16DataManagement.png)

2. <span data-ttu-id="2aa79-173">เลือกไทล์ **พารามิเตอร์กรอบงาน**</span><span class="sxs-lookup"><span data-stu-id="2aa79-173">Select the **Framework parameters** tile.</span></span>

![พารามิเตอร์กรอบงาน](./media/17FrameworkParameters.png)

3. <span data-ttu-id="2aa79-175">บนเพจ **การตั้งค่าเอนทิตี** ให้เลือก **รีเฟรชรายการเอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="2aa79-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![รีเฟรชรายการเอนทิตี](./media/18RefreshEntityList.png)

<span data-ttu-id="2aa79-177">การรีเฟรชจะใช้เวลาประมาณ 20 นาที</span><span class="sxs-lookup"><span data-stu-id="2aa79-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="2aa79-178">คุณจะได้รับการแจ้งเตือนเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="2aa79-178">You will receive an alert when it is complete.</span></span>

![รีเฟรชการยืนยัน](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="2aa79-180">อัปเดตการตั้งค่าความปลอดภัยใน Project Operations บน Dataverse</span><span class="sxs-lookup"><span data-stu-id="2aa79-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="2aa79-181">ไปที่ Project Operations บนสภาพแวดล้อม Dataverse ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2aa79-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="2aa79-182">ไปที่ **การตั้งค่า** > **ความปลอดภัย** > **Security roles**</span><span class="sxs-lookup"><span data-stu-id="2aa79-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="2aa79-183">บนหน้า **Security roles** ในรายการของบทบาท ให้เลือก **ผู้ใช้แอปการรวมแบบสองทิศทาง** และเลือกแท็บ **เอนทิตีที่กำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="2aa79-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="2aa79-184">ตรวจสอบว่าบทบาทมีสิทธิ์ **อ่าน** และ **ผนวกกับ** สำหรับ:</span><span class="sxs-lookup"><span data-stu-id="2aa79-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="2aa79-185">**ชนิดอัตราแลกเปลี่ยนสกุลเงิน**</span><span class="sxs-lookup"><span data-stu-id="2aa79-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="2aa79-186">**ผังบัญชี**</span><span class="sxs-lookup"><span data-stu-id="2aa79-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="2aa79-187">**ปฏิทินทางบัญชี**</span><span class="sxs-lookup"><span data-stu-id="2aa79-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="2aa79-188">**บัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="2aa79-188">**Ledger**</span></span>

5. <span data-ttu-id="2aa79-189">หลังจากอัปเดต Security role แล้ว ให้ไปที่ **การตั้งค่า** > **ความปลอดภัย** > **กลุ่มคน** และเลือกกลุ่มคนเริ่มต้นในมุมมองของกลุ่มคน **เจ้าของธุรกิจในพื้นที่**</span><span class="sxs-lookup"><span data-stu-id="2aa79-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="2aa79-190">เลือก **จัดการบทบาท** และตรวจสอบว่าสิทธิ์ความปลอดภัย **ผู้ใช้แอปการรวมแบบสองทิศทาง** ถูกนำไปใช้กับกลุ่มคนนี้</span><span class="sxs-lookup"><span data-stu-id="2aa79-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="2aa79-191">เรียกใช้การแม็ปการรวมแบบสองทิศทางของ Project Operations</span><span class="sxs-lookup"><span data-stu-id="2aa79-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="2aa79-192">ในโครงการ LCS ของคุณ ไปที่เพจ **รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="2aa79-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="2aa79-193">ภายใต้ **ข้อมูลสภาพแวดล้อม Common Data Service** เลือก **ลิงก์ไปยัง CDS สำหรับแอป**</span><span class="sxs-lookup"><span data-stu-id="2aa79-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="2aa79-194">หลังจากคุณเลือกลิงก์ คุณจะได้รับการเปลี่ยนเส้นทางไปยังรายการเอนทิตีในการแม็ป</span><span class="sxs-lookup"><span data-stu-id="2aa79-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="2aa79-195">เริ่มต้นการแม็ปตามที่อธิบายไว้ในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2aa79-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="2aa79-196">ตรวจสอบให้แน่ใจว่าได้ทำตามลำดับที่ระบุไว้</span><span class="sxs-lookup"><span data-stu-id="2aa79-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="2aa79-197">**เอนทิตีแมป**</span><span class="sxs-lookup"><span data-stu-id="2aa79-197">**Entity Map**</span></span> | <span data-ttu-id="2aa79-198">**รีเฟรชเอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="2aa79-198">**Refresh entity**</span></span> | <span data-ttu-id="2aa79-199">**การทำข้อมูลให้ตรงกันครั้งแรก**</span><span class="sxs-lookup"><span data-stu-id="2aa79-199">**Initial sync**</span></span> | <span data-ttu-id="2aa79-200">**ข้อมูลหลักสำหรับการทำข้อมูลให้ตรงกันครั้งแรก**</span><span class="sxs-lookup"><span data-stu-id="2aa79-200">**Master for initial sync**</span></span> | <span data-ttu-id="2aa79-201">**ข้อกำหนดเบื้องต้นการเรียกใช้**</span><span class="sxs-lookup"><span data-stu-id="2aa79-201">**Run prerequisites**</span></span> | <span data-ttu-id="2aa79-202">**ข้อกำหนดเบื้องต้นสำหรับการซิงค์ครั้งแรก**</span><span class="sxs-lookup"><span data-stu-id="2aa79-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="2aa79-203">**บทบาททรัพยากรโครงการสำหรับทุกบริษัท (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="2aa79-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="2aa79-204">ไม่</span><span class="sxs-lookup"><span data-stu-id="2aa79-204">No</span></span> | <span data-ttu-id="2aa79-205">มี</span><span class="sxs-lookup"><span data-stu-id="2aa79-205">Yes</span></span> | <span data-ttu-id="2aa79-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="2aa79-206">Common Data Service</span></span> | <span data-ttu-id="2aa79-207">ไม่</span><span class="sxs-lookup"><span data-stu-id="2aa79-207">No</span></span> | <span data-ttu-id="2aa79-208">N\A</span><span class="sxs-lookup"><span data-stu-id="2aa79-208">N\A</span></span> |
| <span data-ttu-id="2aa79-209">**นิติบุคคล (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="2aa79-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="2aa79-210">ไม่</span><span class="sxs-lookup"><span data-stu-id="2aa79-210">No</span></span> | <span data-ttu-id="2aa79-211">มี</span><span class="sxs-lookup"><span data-stu-id="2aa79-211">Yes</span></span> | <span data-ttu-id="2aa79-212">แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2aa79-212">Finance and Operations apps</span></span> | <span data-ttu-id="2aa79-213">ไม่</span><span class="sxs-lookup"><span data-stu-id="2aa79-213">No</span></span> | <span data-ttu-id="2aa79-214">N\A</span><span class="sxs-lookup"><span data-stu-id="2aa79-214">N\A</span></span> |
| <span data-ttu-id="2aa79-215">**บัญชีแยกประเภท (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="2aa79-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="2aa79-216">ไม่</span><span class="sxs-lookup"><span data-stu-id="2aa79-216">No</span></span> | <span data-ttu-id="2aa79-217">มี</span><span class="sxs-lookup"><span data-stu-id="2aa79-217">Yes</span></span> | <span data-ttu-id="2aa79-218">แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2aa79-218">Finance and Operations apps</span></span> | <span data-ttu-id="2aa79-219">มี</span><span class="sxs-lookup"><span data-stu-id="2aa79-219">Yes</span></span> | <span data-ttu-id="2aa79-220">ใช่ แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2aa79-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="2aa79-221">**ข้อมูลจริงของการรวม Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="2aa79-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="2aa79-222">ไม่</span><span class="sxs-lookup"><span data-stu-id="2aa79-222">No</span></span> | <span data-ttu-id="2aa79-223">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-223">No</span></span> | <span data-ttu-id="2aa79-224">N\A</span><span class="sxs-lookup"><span data-stu-id="2aa79-224">N\A</span></span> | <span data-ttu-id="2aa79-225">มี</span><span class="sxs-lookup"><span data-stu-id="2aa79-225">Yes</span></span> | <span data-ttu-id="2aa79-226">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-226">No</span></span> |
| <span data-ttu-id="2aa79-227">**รายละเอียดการให้บริการตามสัญญาตามโครงการ (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="2aa79-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="2aa79-228">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-228">No</span></span> | <span data-ttu-id="2aa79-229">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-229">No</span></span> | <span data-ttu-id="2aa79-230">N\A</span><span class="sxs-lookup"><span data-stu-id="2aa79-230">N\A</span></span> | <span data-ttu-id="2aa79-231">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-231">No</span></span> | <span data-ttu-id="2aa79-232">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-232">No</span></span> |
| <span data-ttu-id="2aa79-233">**เอนทิตีการรวมสำหรับความสัมพันธ์ธุรกรรมโครงการ (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="2aa79-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="2aa79-234">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-234">No</span></span> | <span data-ttu-id="2aa79-235">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-235">No</span></span> | <span data-ttu-id="2aa79-236">N\A</span><span class="sxs-lookup"><span data-stu-id="2aa79-236">N\A</span></span> | <span data-ttu-id="2aa79-237">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-237">No</span></span> | <span data-ttu-id="2aa79-238">N\A</span><span class="sxs-lookup"><span data-stu-id="2aa79-238">N\A</span></span> |
| <span data-ttu-id="2aa79-239">**หลักเป้าหมายในรายละเอียดการให้บริการตามสัญญาของการรวม Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="2aa79-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="2aa79-240">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-240">No</span></span> | <span data-ttu-id="2aa79-241">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-241">No</span></span> | <span data-ttu-id="2aa79-242">N\A</span><span class="sxs-lookup"><span data-stu-id="2aa79-242">N\A</span></span> | <span data-ttu-id="2aa79-243">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-243">No</span></span> | <span data-ttu-id="2aa79-244">N\A</span><span class="sxs-lookup"><span data-stu-id="2aa79-244">N\A</span></span> |
| <span data-ttu-id="2aa79-245">**เอนทิตีการรวม Project Operations สำหรับการประมาณการค่าใช้จ่าย (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="2aa79-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="2aa79-246">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-246">No</span></span> | <span data-ttu-id="2aa79-247">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-247">No</span></span> | <span data-ttu-id="2aa79-248">N\A</span><span class="sxs-lookup"><span data-stu-id="2aa79-248">N\A</span></span> | <span data-ttu-id="2aa79-249">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-249">No</span></span> | <span data-ttu-id="2aa79-250">N\A</span><span class="sxs-lookup"><span data-stu-id="2aa79-250">N\A</span></span> |
| <span data-ttu-id="2aa79-251">**เอนทิตีการส่งออกชนิดค่าใช้จ่ายโครงการของการรวม Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="2aa79-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="2aa79-252">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-252">No</span></span> | <span data-ttu-id="2aa79-253">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-253">No</span></span> | <span data-ttu-id="2aa79-254">N\A</span><span class="sxs-lookup"><span data-stu-id="2aa79-254">N\A</span></span> | <span data-ttu-id="2aa79-255">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-255">No</span></span> | <span data-ttu-id="2aa79-256">N\A</span><span class="sxs-lookup"><span data-stu-id="2aa79-256">N\A</span></span> |
| <span data-ttu-id="2aa79-257">**เอนทิตีการส่งออกค่าใช้จ่ายโครงการของการรวม Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="2aa79-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="2aa79-258">มี</span><span class="sxs-lookup"><span data-stu-id="2aa79-258">Yes</span></span> | <span data-ttu-id="2aa79-259">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-259">No</span></span> | <span data-ttu-id="2aa79-260">N\A</span><span class="sxs-lookup"><span data-stu-id="2aa79-260">N\A</span></span> | <span data-ttu-id="2aa79-261">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-261">No</span></span> | <span data-ttu-id="2aa79-262">N\A</span><span class="sxs-lookup"><span data-stu-id="2aa79-262">N\A</span></span> |
| <span data-ttu-id="2aa79-263">**เอนทิตีการรวม Project Operations สำหรับการประมาณการชั่วโมง (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="2aa79-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="2aa79-264">มี</span><span class="sxs-lookup"><span data-stu-id="2aa79-264">Yes</span></span> | <span data-ttu-id="2aa79-265">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-265">No</span></span> | <span data-ttu-id="2aa79-266">N\A</span><span class="sxs-lookup"><span data-stu-id="2aa79-266">N\A</span></span> | <span data-ttu-id="2aa79-267">No</span><span class="sxs-lookup"><span data-stu-id="2aa79-267">No</span></span> | <span data-ttu-id="2aa79-268">N\A</span><span class="sxs-lookup"><span data-stu-id="2aa79-268">N\A</span></span> |


4. <span data-ttu-id="2aa79-269">หากต้องการรีเฟรชเอนทิตี เลือกชื่อการแม็ป จากนั้นเลือก **รีเฟรชเอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="2aa79-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![รีเฟรชการแม็ป](./media/20RefreshMapping.png)

5. <span data-ttu-id="2aa79-271">หลังจากการรีเฟรชเสร็จสิ้น เรียกใช้การแม็ป</span><span class="sxs-lookup"><span data-stu-id="2aa79-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="2aa79-272">ก่อนที่คุณจะเปิดใช้งานการแม็ปถัดไป ให้ตรวจสอบว่าการแม็ปในตารางอยู่ในสถานะ **กำลังทำงาน**</span><span class="sxs-lookup"><span data-stu-id="2aa79-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="2aa79-273">การเรียกใช้การแม็ปที่มีข้อกำหนดเบื้องต้นจำนวนมากอาจใช้เวลาสักครู่</span><span class="sxs-lookup"><span data-stu-id="2aa79-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="2aa79-274">หากต้องการเรียกใช้การแม็ปที่มีข้อกำหนดเบื้องต้น ให้เปิดใช้งานการสลับ **แสดงการแม็ปเอนทิตีที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="2aa79-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="2aa79-275">ถ้าตารางระบุ **ข้อกำหนดเบื้องต้นสำหรับการซิงค์ครั้งแรก** เป็น **ไม่** ตรวจสอบว่าค่าสถานะ **การซิงค์ครั้งแรก** เป็น **ปิด** ในการแม็ปข้อกำหนดเบื้องต้นทั้งหมดก่อนที่คุณจะเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="2aa79-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![เรียกใช้การแม็ป](./media/21RunMap.png)

6. <span data-ttu-id="2aa79-277">ตรวจสอบว่าการแม็ปที่เกี่ยวข้องกับโครงการทั้งหมดอยู่ในสถานะกำลังทำงาน</span><span class="sxs-lookup"><span data-stu-id="2aa79-277">Validate all project related maps are in the running state.</span></span>

![การเรียกใช้การแม็ปทั้งหมด](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="2aa79-279">ใช้ข้อมูลการตั้งค่าคอนฟิกใน CDS สำหรับ Project Operations (ไม่จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="2aa79-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="2aa79-280">หากคุณใช้ข้อมูลสาธิตกับสภาพแวดล้อม Finance โปรดดูที่ [ตั้งค่าและใช้ข้อมูลการกำหนดค่าใน Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) เพื่อใช้ข้อมูลสาธิตกับสภาพแวดล้อม CDS</span><span class="sxs-lookup"><span data-stu-id="2aa79-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="2aa79-281">ขณะนี้ สภาพแวดล้อม Project Operations ของคุณได้รับการเตรียมใช้งานและกำหนดค่าแล้ว</span><span class="sxs-lookup"><span data-stu-id="2aa79-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]