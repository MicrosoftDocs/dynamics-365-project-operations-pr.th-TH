---
title: เตรียมใช้งานสภาพแวดล้อมใหม่
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการเตรียมใช้งานสภาพแวดล้อม Project Operations ของคุณ
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949385"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="44f0b-103">เตรียมใช้งานสภาพแวดล้อมใหม่</span><span class="sxs-lookup"><span data-stu-id="44f0b-103">Provision a new environment</span></span>

<span data-ttu-id="44f0b-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="44f0b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="44f0b-105">หัวข้อนี้ให้ข้อมูลเกี่ยวกับการเตรียมใช้งานสภาพแวดล้อม Dynamics 365 Project Operations ใหม่สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="44f0b-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="44f0b-106">เปิดใช้งานการเตรียมใช้งานอัตโนมัติของ Project Operations ในโครงการ LCS</span><span class="sxs-lookup"><span data-stu-id="44f0b-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="44f0b-107">ใช้ขั้นตอนต่อไปนี้เพื่อเปิดใช้งานขั้นตอนการเตรียมใช้งานอัตโนมัติของ Project Operations สำหรับโครงการ LCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="44f0b-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="44f0b-108">ไปที่ [LCS](https://lcs.dynamics.com/v2) และเลือกไทล์ **การจัดการคุณลักษณะพรีวิว**</span><span class="sxs-lookup"><span data-stu-id="44f0b-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="44f0b-109">ในรายการ **คุณลักษณะพรีวิว** เลือก **Project Operations** และเลือก **เปิดใช้คุณลักษณะพรีวิวแล้ว** เพื่อเปิดใช้งาน Project Operations</span><span class="sxs-lookup"><span data-stu-id="44f0b-109">In the **Preview feature** list, select **Project Operations** and the select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="44f0b-110">ขั้นตอนนี้ดำเนินการเพียงครั้งเดียวต่อโครงการ LCS</span><span class="sxs-lookup"><span data-stu-id="44f0b-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="44f0b-111">เตรียมใช้งานสภาพแวดล้อม Project Operations</span><span class="sxs-lookup"><span data-stu-id="44f0b-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="44f0b-112">เปิดการปรับใช้งาน Dynamics 365 Finance [สภาพแวดล้อมสาธิต](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) หรือ [sandbox/ สภาพแวดล้อมการทำงานจริง](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure)</span><span class="sxs-lookup"><span data-stu-id="44f0b-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="44f0b-113">ดำเนินการตามวิซาร์ด **การเตรียมใช้งานสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="44f0b-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="44f0b-114">ตรวจสอบว่าเวอร์ชันของแอปพลิเคชันที่เลือกคือ 10.0.13 หรือสูงกว่า</span><span class="sxs-lookup"><span data-stu-id="44f0b-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="44f0b-115">เพื่อเตรียมใช้งาน Project Operations ภายใต้ **การตั้งค่าขั้นสูง** เลือก **Common Data Service**</span><span class="sxs-lookup"><span data-stu-id="44f0b-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="44f0b-116">เปิดใช้งาน **การตั้งค่า Common Data Service** โดยการเลือก **ใช่** จากนั้นป้อนข้อมูลในฟิลด์ที่จำเป็น:</span><span class="sxs-lookup"><span data-stu-id="44f0b-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="44f0b-117">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="44f0b-117">Name</span></span>
  - <span data-ttu-id="44f0b-118">ขอบเขต</span><span class="sxs-lookup"><span data-stu-id="44f0b-118">Region</span></span>
  - <span data-ttu-id="44f0b-119">ภาษา</span><span class="sxs-lookup"><span data-stu-id="44f0b-119">Language</span></span>
  - <span data-ttu-id="44f0b-120">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="44f0b-120">Currency</span></span>
 
5. <span data-ttu-id="44f0b-121">ในฟิลด์ **แม่แบบ Common Data Service** ให้เลือก **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="44f0b-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="44f0b-122">เลือกชนิดชนิดสภาพแวดล้อมสำหรับการปรับใช้งานของคุณ</span><span class="sxs-lookup"><span data-stu-id="44f0b-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="44f0b-123">การทดลองใช้ตามการสมัครใช้งานจะช่วยให้คุณสามารถปรับใช้งานสภาพแวดล้อม CDS เป็นเวลา 30 วัน</span><span class="sxs-lookup"><span data-stu-id="44f0b-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![การตั้งค่าการปรับใช้งาน](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="44f0b-125">เลือก **ตกลง** เพื่อรับทราบข้อกำหนดในการให้บริการ จากนั้นเลือก **เสร็จแล้ว** เพื่อกลับไปที่การตั้งค่าการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="44f0b-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![การยินยอมการปรับใช้งาน](./media/2DeploymentConsent.png)

7. <span data-ttu-id="44f0b-127">กรอกข้อมูลในฟิลด์ที่จำเป็นที่เหลือในวิซาร์ดและยืนยันการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="44f0b-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="44f0b-128">เวลาในการเตรียมใช้งานสภาพแวดล้อมจะแตกต่างกันไปตามชนิดสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="44f0b-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="44f0b-129">การเตรียมใช้งานอาจใช้เวลาถึงหกชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="44f0b-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="44f0b-130">หลังจากการปรับใช้งานเสร็จสมบูรณ์ สภาพแวดล้อมจะแสดงเป็น **ปรับใช้งานแล้ว**</span><span class="sxs-lookup"><span data-stu-id="44f0b-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="44f0b-131">เพื่อยืนยันว่าสภาพแวดล้อมได้รับการปรับใช้งานเรียบร้อยแล้ว ให้เลือก **เข้าสู่ระบบ** และเข้าสู่สภาพแวดล้อมเพื่อยืนยัน</span><span class="sxs-lookup"><span data-stu-id="44f0b-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![ รายละเอียดสภาพแวดล้อม](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="44f0b-133">ใช้ข้อมูลสาธิต Project Operations Finance (ขั้นตอนทางเลือก)</span><span class="sxs-lookup"><span data-stu-id="44f0b-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="44f0b-134">ใช้ข้อมูลสาธิต Project Operations Finance กับสภาพแวดล้อมที่โฮสต์บนระบบคลาวด์รุ่นบริการ 10.0.13 ตามที่อธิบายไว้ใน [บทความนี้](resource-apply-finance-demo-data.md)</span><span class="sxs-lookup"><span data-stu-id="44f0b-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="44f0b-135">ใช้การปรับปรุงกับสภาพแวดล้อม Finance</span><span class="sxs-lookup"><span data-stu-id="44f0b-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="44f0b-136">Project Operations ต้องการสภาพแวดล้อม Finance ที่มีเวอร์ชันของแอปพลิเคชัน **10.0.13 (10.0.569.20009)** หรือสูงกว่า</span><span class="sxs-lookup"><span data-stu-id="44f0b-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="44f0b-137">คุณอาจต้องใช้การปรับปรุงคุณภาพกับสภาพแวดล้อม Finance ของคุณเพื่อรับเวอร์ชันนี้</span><span class="sxs-lookup"><span data-stu-id="44f0b-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="44f0b-138">ใน LCS บนเพจ **รายละเอียดสภาพแวดล้อม** ใน **การปรับปรุงที่มีอยู่** ให้เลือก **ดูการปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="44f0b-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![ดูการปรับปรุง](./media/5ViewUpdates.png)

2. <span data-ttu-id="44f0b-140">บนเพจ **การปรับปรุงไบนารี** ให้เลือก **บันทึกแพคเกจ**</span><span class="sxs-lookup"><span data-stu-id="44f0b-140">On the **Binary updates** page, select **Save package.**</span></span>

![บันทึกแพคเกจ](./media/6SavePackage.png)

3. <span data-ttu-id="44f0b-142">คลิก **เลือกทั้งหมด** แล้วเลือก **บันทึกแพคเกจ**</span><span class="sxs-lookup"><span data-stu-id="44f0b-142">Click **Select all** and then select **Save package**.</span></span>

![ตรวจทานและบันทึกการปรับปรุง](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="44f0b-144">ป้อนชื่อและคำอธิบายของแพคเกจ จากนั้นเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="44f0b-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="44f0b-145">กระบวนการนี้อาจใช้เวลาสักครู่ ทั้งนี้ขึ้นอยู่กับการเชื่อมต่ออินเทอร์เน็ต</span><span class="sxs-lookup"><span data-stu-id="44f0b-145">Depending on the internet connection, this process might take some time.</span></span>

![อัปโหลดแพคเกจไปยังแอสเซทไลบรารี](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="44f0b-147">หลังจากบันทึกแพคเกจแล้ว ให้เลือก **เสร็จแล้ว** และบันทึกแพคเกจนี้ลงในแอสเซทไลบรารีในโครงการ LCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="44f0b-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="44f0b-148">การบันทึกและตรวจสอบความถูกต้องของแพคเกจอาจใช้เวลาประมาณ 15 นาที</span><span class="sxs-lookup"><span data-stu-id="44f0b-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="44f0b-149">หากต้องการใช้การปรับปรุง ให้ไปที่เพจ **รายละเอียดสภาพแวดล้อม** ใน LCS และเลือก **รักษา** > **ใช้การปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="44f0b-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![รักษาสภาพแวดล้อม](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="44f0b-151">ในรายการปรับปรุง ให้เลือกแพคเกจที่คุณสร้าง และเลือก**นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="44f0b-151">In the updates list select the package you created, and select **Apply**.</span></span>

![ใช้การปรับปรุง](./media/10ApplyUpdates.png)

<span data-ttu-id="44f0b-153">การดูแลสภาพแวดล้อมจะใช้เวลาพอสมควร</span><span class="sxs-lookup"><span data-stu-id="44f0b-153">Environment servicing will take some time.</span></span> <span data-ttu-id="44f0b-154">หลังจากเสร็จสิ้น สภาพแวดล้อมจะคืนกลับสู่สถานะที่ปรับใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="44f0b-154">After it is complete, the environment will return to a deployed state.</span></span>

![ปรับใช้งานสภาพแวดล้อมแล้ว](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="44f0b-156">สร้างการเชื่อมต่อการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="44f0b-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="44f0b-157">ในโครงการ LCS ของคุณ ไปที่เพจ **รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="44f0b-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="44f0b-158">ภายใต้ **ข้อมูลสภาพแวดล้อม Common Data Service** เลือก **ลิงก์ไปยัง CDS สำหรับแอป**</span><span class="sxs-lookup"><span data-stu-id="44f0b-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="44f0b-159">หลังจากลิงก์เสร็จสมบูรณ์ ให้เลือก **ลิงก์ไปยัง CDS สำหรับแอป** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="44f0b-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="44f0b-160">คุณจะได้รับการเปลี่ยนเส้นทางไปยังการรวมแบบสองทิศทางใน Finance</span><span class="sxs-lookup"><span data-stu-id="44f0b-160">You will be redirected to Dual Write in Finance.</span></span>

![เชื่อมโยงไปยัง CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="44f0b-162">เลือก **ใช้โซลูชัน** เพื่อเข้าถึงเอนทิตีที่จะถูกแม็ปในการรวม</span><span class="sxs-lookup"><span data-stu-id="44f0b-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![ใช้โซลูชัน](./media/13ApplySolutions.png)

5. <span data-ttu-id="44f0b-164">เลือกทั้งสองโซลูชัน **การแม็ปเอนทิตีการรวมแบบสองทิศทางของ Dynamics 365 Finance and Operations** และ **การแม็ปเอนทิตีการรวมแบบสองทิศทางของ Dynamics 365 Project Operations** แล้วเลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="44f0b-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![ยืนยันโซลูชัน](./media/14ConfirmSolutions.png)

<span data-ttu-id="44f0b-166">หลังจากใช้โซลูชันแล้ว เอนทิตีการรวมแบบสองทิศทางจะมีการนำไปใช้กับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="44f0b-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![การใช้โซลูชัน](./media/15ApplyingSolutions.png)

<span data-ttu-id="44f0b-168">หลังจากใช้เอนทิตีแล้ว การแม็ปที่มีอยู่ทั้งหมดจะแสดงรายการในสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="44f0b-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![การแม็ปการรวมแบบสองทิศทาง](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="44f0b-170">รีเฟรชเอนทิตีข้อมูลหลังการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="44f0b-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="44f0b-171">ใน Finance ไปที่พื้นที่ทำงาน **การจัดการข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="44f0b-171">In Finance, go to the **Data management** workspace.</span></span>

![พื้นที่ทำงานการจัดการข้อมูล](./media/16DataManagement.png)

2. <span data-ttu-id="44f0b-173">เลือกไทล์ **พารามิเตอร์กรอบงาน**</span><span class="sxs-lookup"><span data-stu-id="44f0b-173">Select the **Framework parameters** tile.</span></span>

![พารามิเตอร์กรอบงาน](./media/17FrameworkParameters.png)

3. <span data-ttu-id="44f0b-175">บนเพจ **การตั้งค่าเอนทิตี** ให้เลือก **รีเฟรชรายการเอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="44f0b-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![รีเฟรชรายการเอนทิตี](./media/18RefreshEntityList.png)

<span data-ttu-id="44f0b-177">การรีเฟรชจะใช้เวลาประมาณ 20 นาที</span><span class="sxs-lookup"><span data-stu-id="44f0b-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="44f0b-178">คุณจะได้รับการแจ้งเตือนเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="44f0b-178">You will receive an alert when it is complete.</span></span>

![รีเฟรชการยืนยัน](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="44f0b-180">เรียกใช้การแม็ปการรวมแบบสองทิศทางของ Project Operations</span><span class="sxs-lookup"><span data-stu-id="44f0b-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="44f0b-181">ในโครงการ LCS ของคุณ ไปที่เพจ **รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="44f0b-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="44f0b-182">ภายใต้ **ข้อมูลสภาพแวดล้อม Common Data Service** เลือก **ลิงก์ไปยัง CDS สำหรับแอป**</span><span class="sxs-lookup"><span data-stu-id="44f0b-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="44f0b-183">หลังจากคุณเลือกลิงก์ คุณจะได้รับการเปลี่ยนเส้นทางไปยังรายการเอนทิตีในการแม็ป</span><span class="sxs-lookup"><span data-stu-id="44f0b-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="44f0b-184">เริ่มต้นการแม็ปตามที่อธิบายไว้ในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="44f0b-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="44f0b-185">ตรวจสอบให้แน่ใจว่าได้ทำตามลำดับที่ระบุไว้</span><span class="sxs-lookup"><span data-stu-id="44f0b-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="44f0b-186">**เอนทิตีแมป**</span><span class="sxs-lookup"><span data-stu-id="44f0b-186">**Entity Map**</span></span> | <span data-ttu-id="44f0b-187">**รีเฟรชเอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="44f0b-187">**Refresh entity**</span></span> | <span data-ttu-id="44f0b-188">**การทำข้อมูลให้ตรงกันครั้งแรก**</span><span class="sxs-lookup"><span data-stu-id="44f0b-188">**Initial sync**</span></span> | <span data-ttu-id="44f0b-189">**ข้อมูลหลักสำหรับการทำข้อมูลให้ตรงกันครั้งแรก**</span><span class="sxs-lookup"><span data-stu-id="44f0b-189">**Master for initial sync**</span></span> | <span data-ttu-id="44f0b-190">**ข้อกำหนดเบื้องต้นการเรียกใช้**</span><span class="sxs-lookup"><span data-stu-id="44f0b-190">**Run prerequisites**</span></span> | <span data-ttu-id="44f0b-191">**ข้อกำหนดเบื้องต้นสำหรับการซิงค์ครั้งแรก**</span><span class="sxs-lookup"><span data-stu-id="44f0b-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="44f0b-192">**บทบาททรัพยากรโครงการสำหรับทุกบริษัท (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="44f0b-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="44f0b-193">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-193">No</span></span> | <span data-ttu-id="44f0b-194">มี</span><span class="sxs-lookup"><span data-stu-id="44f0b-194">Yes</span></span> | <span data-ttu-id="44f0b-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="44f0b-195">Common Data Service</span></span> | <span data-ttu-id="44f0b-196">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-196">No</span></span> | <span data-ttu-id="44f0b-197">N\A</span><span class="sxs-lookup"><span data-stu-id="44f0b-197">N\A</span></span> |
| <span data-ttu-id="44f0b-198">**นิติบุคคล (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="44f0b-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="44f0b-199">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-199">No</span></span> | <span data-ttu-id="44f0b-200">มี</span><span class="sxs-lookup"><span data-stu-id="44f0b-200">Yes</span></span> | <span data-ttu-id="44f0b-201">แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="44f0b-201">Finance and Operations apps</span></span> | <span data-ttu-id="44f0b-202">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-202">No</span></span> | <span data-ttu-id="44f0b-203">N\A</span><span class="sxs-lookup"><span data-stu-id="44f0b-203">N\A</span></span> |
| <span data-ttu-id="44f0b-204">**ข้อมูลจริงของการรวม Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="44f0b-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="44f0b-205">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-205">No</span></span> | <span data-ttu-id="44f0b-206">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-206">No</span></span> | <span data-ttu-id="44f0b-207">N\A</span><span class="sxs-lookup"><span data-stu-id="44f0b-207">N\A</span></span> | <span data-ttu-id="44f0b-208">มี</span><span class="sxs-lookup"><span data-stu-id="44f0b-208">Yes</span></span> | <span data-ttu-id="44f0b-209">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-209">No</span></span> |
| <span data-ttu-id="44f0b-210">**รายละเอียดการให้บริการตามสัญญาตามโครงการ (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="44f0b-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="44f0b-211">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-211">No</span></span> | <span data-ttu-id="44f0b-212">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-212">No</span></span> | <span data-ttu-id="44f0b-213">N\A</span><span class="sxs-lookup"><span data-stu-id="44f0b-213">N\A</span></span> | <span data-ttu-id="44f0b-214">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-214">No</span></span> | <span data-ttu-id="44f0b-215">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-215">No</span></span> |
| <span data-ttu-id="44f0b-216">**เอนทิตีการรวมสำหรับความสัมพันธ์ธุรกรรมโครงการ (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="44f0b-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="44f0b-217">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-217">No</span></span> | <span data-ttu-id="44f0b-218">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-218">No</span></span> | <span data-ttu-id="44f0b-219">N\A</span><span class="sxs-lookup"><span data-stu-id="44f0b-219">N\A</span></span> | <span data-ttu-id="44f0b-220">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-220">No</span></span> | <span data-ttu-id="44f0b-221">N\A</span><span class="sxs-lookup"><span data-stu-id="44f0b-221">N\A</span></span> |
| <span data-ttu-id="44f0b-222">**หลักเป้าหมายในรายละเอียดการให้บริการตามสัญญาของการรวม Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="44f0b-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="44f0b-223">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-223">No</span></span> | <span data-ttu-id="44f0b-224">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-224">No</span></span> | <span data-ttu-id="44f0b-225">N\A</span><span class="sxs-lookup"><span data-stu-id="44f0b-225">N\A</span></span> | <span data-ttu-id="44f0b-226">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-226">No</span></span> | <span data-ttu-id="44f0b-227">N\A</span><span class="sxs-lookup"><span data-stu-id="44f0b-227">N\A</span></span> |
| <span data-ttu-id="44f0b-228">**เอนทิตีการรวม Project Operations สำหรับการประมาณการค่าใช้จ่าย (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="44f0b-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="44f0b-229">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-229">No</span></span> | <span data-ttu-id="44f0b-230">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-230">No</span></span> | <span data-ttu-id="44f0b-231">N\A</span><span class="sxs-lookup"><span data-stu-id="44f0b-231">N\A</span></span> | <span data-ttu-id="44f0b-232">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-232">No</span></span> | <span data-ttu-id="44f0b-233">N\A</span><span class="sxs-lookup"><span data-stu-id="44f0b-233">N\A</span></span> |
| <span data-ttu-id="44f0b-234">**เอนทิตีการรวม Project Operations สำหรับการประมาณการชั่วโมง (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="44f0b-234">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="44f0b-235">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-235">No</span></span> | <span data-ttu-id="44f0b-236">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-236">No</span></span> | <span data-ttu-id="44f0b-237">N\A</span><span class="sxs-lookup"><span data-stu-id="44f0b-237">N\A</span></span> | <span data-ttu-id="44f0b-238">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-238">No</span></span> | <span data-ttu-id="44f0b-239">N\A</span><span class="sxs-lookup"><span data-stu-id="44f0b-239">N\A</span></span> |
| <span data-ttu-id="44f0b-240">**เอนทิตีการส่งออกค่าใช้จ่ายโครงการของการรวม Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="44f0b-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="44f0b-241">มี</span><span class="sxs-lookup"><span data-stu-id="44f0b-241">Yes</span></span> | <span data-ttu-id="44f0b-242">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-242">No</span></span> | <span data-ttu-id="44f0b-243">N\A</span><span class="sxs-lookup"><span data-stu-id="44f0b-243">N\A</span></span> | <span data-ttu-id="44f0b-244">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-244">No</span></span> | <span data-ttu-id="44f0b-245">N\A</span><span class="sxs-lookup"><span data-stu-id="44f0b-245">N\A</span></span> |
| <span data-ttu-id="44f0b-246">**เอนทิตีการรวม Project Operations สำหรับการประมาณการชั่วโมง (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="44f0b-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="44f0b-247">มี</span><span class="sxs-lookup"><span data-stu-id="44f0b-247">Yes</span></span> | <span data-ttu-id="44f0b-248">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-248">No</span></span> | <span data-ttu-id="44f0b-249">N\A</span><span class="sxs-lookup"><span data-stu-id="44f0b-249">N\A</span></span> | <span data-ttu-id="44f0b-250">No</span><span class="sxs-lookup"><span data-stu-id="44f0b-250">No</span></span> | <span data-ttu-id="44f0b-251">N\A</span><span class="sxs-lookup"><span data-stu-id="44f0b-251">N\A</span></span> |

4. <span data-ttu-id="44f0b-252">หากต้องการรีเฟรชเอนทิตี เลือกชื่อการแม็ป จากนั้นเลือก **รีเฟรชเอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="44f0b-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 
5. <span data-ttu-id="44f0b-253">ดำเนินการต่อโดยเรียกใช้การแม็ปหลังจากการรีเฟรชเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="44f0b-253">Proceed with running the map after the refresh is complete.</span></span>

![รีเฟรชการแม็ป](./media/20RefreshMapping.png)

<span data-ttu-id="44f0b-255">ก่อนที่คุณจะเปิดใช้งานการแม็ปถัดไป ให้ตรวจสอบว่าการแม็ปในตารางอยู่ในสถานะ **กำลังทำงาน**</span><span class="sxs-lookup"><span data-stu-id="44f0b-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="44f0b-256">การเรียกใช้การแม็ปที่มีข้อกำหนดเบื้องต้นจำนวนมากอาจใช้เวลาสักครู่</span><span class="sxs-lookup"><span data-stu-id="44f0b-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="44f0b-257">หากต้องการเรียกใช้การแม็ปที่มีข้อกำหนดเบื้องต้น ให้เปิดใช้งานการสลับ **แสดงการแม็ปเอนทิตีที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="44f0b-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="44f0b-258">ถ้าตารางระบุ **ข้อกำหนดเบื้องต้นสำหรับการซิงค์ครั้งแรก** เป็น **ไม่** ตรวจสอบว่าค่าสถานะ **การซิงค์ครั้งแรก** เป็น **ปิด** ในการแม็ปข้อกำหนดเบื้องต้นทั้งหมดก่อนที่คุณจะเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="44f0b-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![เรียกใช้การแม็ป](./media/21RunMap.png)

6. <span data-ttu-id="44f0b-260">ตรวจสอบว่าการแม็ปที่เกี่ยวข้องกับโครงการทั้งหมดอยู่ในสถานะกำลังทำงาน</span><span class="sxs-lookup"><span data-stu-id="44f0b-260">Validate all project related maps are in the running state.</span></span>

![การเรียกใช้การแม็ปทั้งหมด](./media/22AllMapsRunning.png)

<span data-ttu-id="44f0b-262">ขณะนี้ สภาพแวดล้อม Project Operations ของคุณได้รับการเตรียมใช้งานและกำหนดค่าแล้ว</span><span class="sxs-lookup"><span data-stu-id="44f0b-262">Your Project Operations environment is now provisioned and configured.</span></span>
