---
title: ใช้การตั้งค่าสาธิตและข้อมูลการกำหนดค่า
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีใช้การตั้งค่าการสาธิตและข้อมูลการกำหนดค่าสำหรับ Project Operations
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085797"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="0362b-103">ใช้การตั้งค่าการสาธิตและข้อมูลการกำหนดค่าสำหรับการปรับใช้งานแบบ Lite ของ Project Operations - จัดการกับการออกใบแจ้งหนี้ชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="0362b-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="0362b-104">_\*\*การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="0362b-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="0362b-105">ดาวน์โหลด [แพคเกจข้อมูลหลัก](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip)</span><span class="sxs-lookup"><span data-stu-id="0362b-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="0362b-106">ไปที่โฟลเดอร์ *ProjOpsDemoDataSetupAndMaster - CMT แบบในตัว* และเรียกใช้ไฟล์ปฏิบัติการ *DataMigrationUtility*</span><span class="sxs-lookup"><span data-stu-id="0362b-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="0362b-107">ในเพจ 1 ของวิซาร์ดการย้ายการกำหนดค่า Common Data Service (CMT) เลือก **นำเข้าข้อมูล** แล้วเลือก **ดำเนินการต่อ**</span><span class="sxs-lookup"><span data-stu-id="0362b-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![การโอนย้ายการตั้งค่าคอนฟิก](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="0362b-109">ในเพจ 2 ของวิซาร์ด CMT ให้เลือก **Microsoft 365** เป็น **ชนิดการปรับใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="0362b-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="0362b-110">เลือกกล่องกาเครื่องหมาย **แสดงรายชื่อขององค์กรที่มีอยู่** และ **แสดงขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="0362b-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="0362b-111">เลือกภูมิภาคของผู้เช่าของคุณ ป้อนข้อมูลประจำตัวของคุณ จากนั้นเลือก **เข้าสู่ระบบ**</span><span class="sxs-lookup"><span data-stu-id="0362b-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![การลงชื่อเข้าใช้การกำหนดค่า](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="0362b-113">ในเพจ 3 จากรายชื่อองค์กรในผู้เช่า ให้เลือกองค์กรที่คุณต้องการนำเข้าข้อมูลสาธิต จากนั้นเลือก **เข้าสู่ระบบ**</span><span class="sxs-lookup"><span data-stu-id="0362b-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="0362b-114">ในเพจ 4 เลือกไฟล์ zip *MasterAndSetupData* จากโฟลเดอร์ที่ขยาย *ProjOpsDemoDataSetupAndMaster - CMT ในตัว*</span><span class="sxs-lookup"><span data-stu-id="0362b-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![ไฟล์ Zip](./media/3ZipFile.png)

![เลือกไฟล์](./media/4SelectAFile.png)

9. <span data-ttu-id="0362b-117">หลังจากเลือกไฟล์ zip แล้ว ให้เลือก **นำเข้าข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="0362b-117">After the zip file is selected, select **Import Data**.</span></span>

![การนำเข้าข้อมูล](./media/5ImportData.png)

10. <span data-ttu-id="0362b-119">การนำเข้าจะทำงานประมาณสองถึงสิบนาที ขึ้นอยู่กับความเร็วเครือข่ายของคุณ</span><span class="sxs-lookup"><span data-stu-id="0362b-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="0362b-120">หลังจากเสร็จสิ้น ให้ออกจากวิซาร์ด CMT</span><span class="sxs-lookup"><span data-stu-id="0362b-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="0362b-121">ตรวจสอบองค์กรของคุณสำหรับข้อมูลใน 20 เอนทิตีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0362b-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="0362b-122">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="0362b-122">Currency</span></span>
- <span data-ttu-id="0362b-123">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="0362b-123">Organizational Unit</span></span>
- <span data-ttu-id="0362b-124">ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="0362b-124">Contact</span></span>
- <span data-ttu-id="0362b-125">กลุ่มภาษี</span><span class="sxs-lookup"><span data-stu-id="0362b-125">Tax Group</span></span>
- <span data-ttu-id="0362b-126">กลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0362b-126">Customer Group</span></span>
- <span data-ttu-id="0362b-127">หน่วย</span><span class="sxs-lookup"><span data-stu-id="0362b-127">Unit</span></span>
- <span data-ttu-id="0362b-128">กลุ่มของหน่วย</span><span class="sxs-lookup"><span data-stu-id="0362b-128">Unit Group</span></span>
- <span data-ttu-id="0362b-129">ราคาตลาด</span><span class="sxs-lookup"><span data-stu-id="0362b-129">Price List</span></span>
- <span data-ttu-id="0362b-130">ราคาตลาดสำหรับพารามิเตอร์โครงการ</span><span class="sxs-lookup"><span data-stu-id="0362b-130">Project Parameter Price List</span></span>
- <span data-ttu-id="0362b-131">ความถี่ของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="0362b-131">Invoice Frequency</span></span>
- <span data-ttu-id="0362b-132">รายละเอียดความถี่ของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="0362b-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="0362b-133">ประเภททรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="0362b-133">Bookable Resource Category</span></span>
- <span data-ttu-id="0362b-134">ประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="0362b-134">Transaction Category</span></span>
- <span data-ttu-id="0362b-135">ประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="0362b-135">Expense Category</span></span>
- <span data-ttu-id="0362b-136">ราคาตามบทบาท</span><span class="sxs-lookup"><span data-stu-id="0362b-136">Role Price</span></span>
- <span data-ttu-id="0362b-137">ราคาของประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="0362b-137">Transaction Category Price</span></span>
- <span data-ttu-id="0362b-138">คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="0362b-138">Characteristic</span></span>
- <span data-ttu-id="0362b-139">ทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="0362b-139">Bookable Resource</span></span>
- <span data-ttu-id="0362b-140">การกำหนดประเภททรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="0362b-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="0362b-141">คุณลักษณะทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="0362b-141">Bookable Resource Characteristic</span></span>

![การนำเข้าเสร็จสมบูรณ์](./media/6CompleteImport.png)
