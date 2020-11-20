---
title: ใช้การตั้งค่าสาธิตและข้อมูลการกำหนดค่า - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีใช้การตั้งค่าการสาธิตและข้อมูลการกำหนดค่าสำหรับ Project Operations
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401286"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="2be64-103">ใช้การตั้งค่าสาธิตและข้อมูลการกำหนดค่าสำหรับ Project Operations - Lite</span><span class="sxs-lookup"><span data-stu-id="2be64-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="2be64-104">_\*\*การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="2be64-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2be64-105">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="2be64-105">Prerequisites</span></span>

<span data-ttu-id="2be64-106">ก่อนที่คุณจะเริ่มการกำหนดค่า คุณต้องมีสภาพแวดล้อม Common Data Service (CDS) ที่จัดเตรียมไว้สำหรับ Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="2be64-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="2be64-107">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="2be64-107">Instructions</span></span>

1. <span data-ttu-id="2be64-108">ดาวน์โหลด [แพคเกจข้อมูลหลัก](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip)</span><span class="sxs-lookup"><span data-stu-id="2be64-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="2be64-109">ไปที่โฟลเดอร์ *ProjOpsDemoDataSetupAndMaster - CMT แบบในตัว* และเรียกใช้ไฟล์ปฏิบัติการ *DataMigrationUtility*</span><span class="sxs-lookup"><span data-stu-id="2be64-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="2be64-110">ในเพจ 1 ของวิซาร์ดการย้ายการกำหนดค่า Common Data Service (CMT) เลือก **นำเข้าข้อมูล** แล้วเลือก **ดำเนินการต่อ**</span><span class="sxs-lookup"><span data-stu-id="2be64-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![การโอนย้ายการตั้งค่าคอนฟิก](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="2be64-112">ในเพจ 2 ของวิซาร์ด CMT ให้เลือก **Microsoft 365** เป็น **ชนิดการปรับใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="2be64-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="2be64-113">เลือกกล่องกาเครื่องหมาย **แสดงรายชื่อขององค์กรที่มีอยู่** และ **แสดงขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="2be64-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="2be64-114">เลือกภูมิภาคของผู้เช่าของคุณ ป้อนข้อมูลประจำตัวของคุณ จากนั้นเลือก **เข้าสู่ระบบ**</span><span class="sxs-lookup"><span data-stu-id="2be64-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![การลงชื่อเข้าใช้การกำหนดค่า](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="2be64-116">ในเพจ 3 จากรายชื่อองค์กรในผู้เช่า ให้เลือกองค์กรที่คุณต้องการนำเข้าข้อมูลสาธิต จากนั้นเลือก **เข้าสู่ระบบ**</span><span class="sxs-lookup"><span data-stu-id="2be64-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="2be64-117">ในเพจ 4 เลือกไฟล์ zip *MasterAndSetupData* จากโฟลเดอร์ที่ขยาย *ProjOpsDemoDataSetupAndMaster - CMT ในตัว*</span><span class="sxs-lookup"><span data-stu-id="2be64-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![ไฟล์ Zip](./media/3ZipFile.png)

![เลือกไฟล์](./media/4SelectAFile.png)

9. <span data-ttu-id="2be64-120">หลังจากเลือกไฟล์ zip แล้ว ให้เลือก **นำเข้าข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="2be64-120">After the zip file is selected, select **Import Data**.</span></span>

![การนำเข้าข้อมูล](./media/5ImportData.png)

10. <span data-ttu-id="2be64-122">การนำเข้าจะทำงานประมาณสองถึงสิบนาที ขึ้นอยู่กับความเร็วเครือข่ายของคุณ</span><span class="sxs-lookup"><span data-stu-id="2be64-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="2be64-123">หลังจากเสร็จสิ้น ให้ออกจากวิซาร์ด CMT</span><span class="sxs-lookup"><span data-stu-id="2be64-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="2be64-124">ตรวจสอบองค์กรของคุณสำหรับข้อมูลใน 20 เอนทิตีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2be64-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="2be64-125">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="2be64-125">Currency</span></span>
-   <span data-ttu-id="2be64-126">บัญชี</span><span class="sxs-lookup"><span data-stu-id="2be64-126">Account</span></span>
-   <span data-ttu-id="2be64-127">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="2be64-127">Organizational Unit</span></span>
-   <span data-ttu-id="2be64-128">ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="2be64-128">Contact</span></span>
-   <span data-ttu-id="2be64-129">กลุ่มภาษี</span><span class="sxs-lookup"><span data-stu-id="2be64-129">Tax Group</span></span>
-   <span data-ttu-id="2be64-130">กลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="2be64-130">Customer Group</span></span>
-   <span data-ttu-id="2be64-131">หน่วย</span><span class="sxs-lookup"><span data-stu-id="2be64-131">Unit</span></span>
-   <span data-ttu-id="2be64-132">กลุ่มของหน่วย</span><span class="sxs-lookup"><span data-stu-id="2be64-132">Unit Group</span></span>
-   <span data-ttu-id="2be64-133">ราคาตลาด</span><span class="sxs-lookup"><span data-stu-id="2be64-133">Price List</span></span>
-   <span data-ttu-id="2be64-134">ราคาตลาดสำหรับพารามิเตอร์โครงการ</span><span class="sxs-lookup"><span data-stu-id="2be64-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="2be64-135">ความถี่ของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="2be64-135">Invoice Frequency</span></span>
-   <span data-ttu-id="2be64-136">ประเภททรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="2be64-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="2be64-137">ประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="2be64-137">Transaction Category</span></span>
-   <span data-ttu-id="2be64-138">ประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="2be64-138">Expense Category</span></span>
-   <span data-ttu-id="2be64-139">ราคาตามบทบาท</span><span class="sxs-lookup"><span data-stu-id="2be64-139">Role Price</span></span>
-   <span data-ttu-id="2be64-140">ราคาของประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="2be64-140">Transaction Category Price</span></span>
-   <span data-ttu-id="2be64-141">คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="2be64-141">Characteristic</span></span>
-   <span data-ttu-id="2be64-142">ทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="2be64-142">Bookable Resource</span></span>
-   <span data-ttu-id="2be64-143">การกำหนดประเภททรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="2be64-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="2be64-144">คุณลักษณะทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="2be64-144">Bookable Resource Characteristic</span></span>

![การนำเข้าเสร็จสมบูรณ์](./media/6CompleteImport.png)
