---
title: นำข้อมูลสาธิตไปใช้กับสภาพแวดล้อมที่เป็นโฮสต์บนระบบคลาวด์ของ Finance
description: หัวข้อนี้อธิบายถึงวิธีการใช้ข้อมูลสาธิตจาก Project Operations กับภาพแวดล้อมที่โฮสต์บนระบบคลาวด์ของ Dynamics 365 Finance
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7239301dc8b775dc4a53a1cf6c0bcba3956125a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289887"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="dab90-103">นำข้อมูลสาธิตไปใช้กับสภาพแวดล้อมที่เป็นโฮสต์บนระบบคลาวด์ของ Finance</span><span class="sxs-lookup"><span data-stu-id="dab90-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="dab90-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="dab90-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dab90-105">หัวข้อนี้ใช้ได้เฉพาะ Microsoft Dynamics 365 Finance เวอร์ชัน 10.0.13 เท่านั้นและสามารถทำได้บนสภาพแวดล้อมที่โฮสต์บนระบบคลาวด์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="dab90-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="dab90-106">ทำตามขั้นตอนในหัวข้อนี้ **ก่อน** คุณจึงจะสามารถใช้การปรับปรุงคุณภาพกับสภาพแวดล้อมได้</span><span class="sxs-lookup"><span data-stu-id="dab90-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="dab90-107">ในโครงการ LCS ของคุณ ให้เปิดเพจ **รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="dab90-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="dab90-108">สังเกตว่ามีรายละเอียดที่จำเป็นในการเชื่อมต่อกับสภาพแวดล้อมโดยใช้โพรโทคอลการใช้เดสก์ท็อประยะไกล (RDP)</span><span class="sxs-lookup"><span data-stu-id="dab90-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![ รายละเอียดสภาพแวดล้อม](./media/1EnvironmentDetails.png)

<span data-ttu-id="dab90-110">ข้อมูลประจำตัวที่ไฮไลต์ชุดแรกคือข้อมูลประจำตัวของบัญชีภายในเครื่องและมีไฮเปอร์ลิงก์ไปยังการเชื่อมต่อเดสก์ท็อประยะไกล</span><span class="sxs-lookup"><span data-stu-id="dab90-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="dab90-111">ข้อมูลประจำตัวงรวมถึงชื่อผู้ใช้และรหัสผ่านของผู้ดูแลระบบสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="dab90-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="dab90-112">ข้อมูลประจำตัวชุดที่สองใช้เพื่อเข้าสู่ระบบ SQL Server ในสภาพแวดล้อมนี้</span><span class="sxs-lookup"><span data-stu-id="dab90-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="dab90-113">เชื่อมต่อกับสภาพแวดล้อมจากระบะไกลโดยใช้ไฮเปอร์ลิงก์ใน **บัญชีภายในเครื่อง** และใช้ **ข้อมูลประจำตัวบัญชีภายในเครื่อง** เพื่อรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="dab90-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="dab90-114">ไปที่ **บริการข้อมูลอินเทอร์เน็ต** > **แอปพลิเคชันพูล** > **AOSService** และหยุดบริการ</span><span class="sxs-lookup"><span data-stu-id="dab90-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="dab90-115">คุณกำลังหยุดบริการในตอนนี้เพื่อให้คุณสามารถแทนที่ฐานข้อมูล SQL ต่อไปได้</span><span class="sxs-lookup"><span data-stu-id="dab90-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![หยุด AOS](./media/2StopAOS.png)

4. <span data-ttu-id="dab90-117">ไปที่ **บริการ** และหยุดสองรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="dab90-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="dab90-118">Microsoft Dynamics 365 Unified Operations: บริการจัดการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="dab90-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="dab90-119">Microsoft Dynamics 365 Unified Operations: กรอบงานการนำเข้าส่งออกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="dab90-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![หยุดบริการ](./media/3StopServices.png)

5. <span data-ttu-id="dab90-121">เปิด Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="dab90-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="dab90-122">เข้าสู่ระบบด้วยข้อมูลประจำตัวของ SQL Server และใช้ผู้ใช้ axdbadmin และรหัสผ่านจากเพจ **รายละเอียดสภาพแวดล้อม** ของ LCS</span><span class="sxs-lookup"><span data-stu-id="dab90-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="dab90-124">ใน Object Explorer, **ฐานข้อมูล** และค้นหา **AXDB**</span><span class="sxs-lookup"><span data-stu-id="dab90-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="dab90-125">คุณจะแทนที่ฐานข้อมูลด้วยฐานข้อมูลใหม่ที่อยู่ใน [ศูนย์ดาวน์โหลด](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip)</span><span class="sxs-lookup"><span data-stu-id="dab90-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="dab90-126">คัดลอกไฟล์ zip ไปยัง VM ที่คุณเข้าถึงระยะไกลและแยกเนื้อหา zip</span><span class="sxs-lookup"><span data-stu-id="dab90-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="dab90-127">ใน SQL Server Management Studio คลิกขวา **AxDB** แล้วเลือก **งาน** > **คืนค่า** > **ฐานข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="dab90-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![คืนค่าฐานข้อมูล](./media/5RestoreDatabase.png)

9. <span data-ttu-id="dab90-129">เลือก **อุปกรณ์ต้นทาง** และไปที่ไฟล์ที่แยกจาก zip ที่คุณคัดลอก</span><span class="sxs-lookup"><span data-stu-id="dab90-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![อุปกรณ์ต้นทาง](./media/6SourceDevice.png)

10. <span data-ttu-id="dab90-131">เลือก **ตัวเลือก** แล้วเลือก **เขียนทับฐานข้อมูลที่มีอยู่** และ **ปิดการเชื่อมต่อไปยังฐานข้อมูลปลายทางที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="dab90-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="dab90-132">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="dab90-132">Select **OK**.</span></span>

![คืนค่าการตั้งค่า](./media/7RestoreSetting.png)

<span data-ttu-id="dab90-134">คุณจะได้รับการยืนยันว่าการคืนค่า AXDB สำเร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="dab90-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="dab90-135">หลังจากที่คุณได้รับการยืนยันนี้ คุณสามารถปิด SQL Services Management Studio</span><span class="sxs-lookup"><span data-stu-id="dab90-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="dab90-136">กลับไปที่ **บริการข้อมูลอินเทอร์เน็ต** > **แอปพลิเคชันพูล** > **AOSService** และเริ่มต้น AOSService</span><span class="sxs-lookup"><span data-stu-id="dab90-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="dab90-137">ไปที่ **บริการ** และเริ่มบริการสองอย่างที่คุณหยุดไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="dab90-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="dab90-138">ค้นหาเครื่องมือ AdminUserProvisioning บน VM นี้</span><span class="sxs-lookup"><span data-stu-id="dab90-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="dab90-139">ดูที่ K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe</span><span class="sxs-lookup"><span data-stu-id="dab90-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="dab90-140">เรียกใช้ไฟล์ .ext โดยใช้ที่อยู่ผู้ใช้ของคุณในฟิลด์ **ที่อยู่อีเมล**</span><span class="sxs-lookup"><span data-stu-id="dab90-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="dab90-141">เลือก **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="dab90-141">Select **Submit**.</span></span>

![การจัดเตรียมผู้ใช้ที่เป็นผู้ดูแลระบบ](./media/8AdminUserProvisioning.png)

<span data-ttu-id="dab90-143">การดำเนินการนี้ใช้เวลาสองถึงสามนาที</span><span class="sxs-lookup"><span data-stu-id="dab90-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="dab90-144">คุณควรได้รับข้อความยืนยันว่าปรับปรุงผู้ใช้ที่เป็นผู้ดูแลระบบเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="dab90-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="dab90-145">สุดท้ายเรียกใช้พร้อมท์รับคำสั่งเป็นผู้ดูแลระบบและดำเนินการ iisreset</span><span class="sxs-lookup"><span data-stu-id="dab90-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![ตั้งค่า IIS ใหม่](./media/9IISReset.png)

18. <span data-ttu-id="dab90-147">ปิดเซสชันเดสก์ท็อประยะไกลและใช้เพจ **รายละเอียดสภาพแวดล้อม** ของ LCS เพื่อเข้าสู่สภาพแวดล้อมในการยืนยันว่าทำงานได้ตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="dab90-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]