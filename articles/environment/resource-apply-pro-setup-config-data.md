---
title: ตั้งค่าและใช้ข้อมูลการกำหนดค่าใน Common Data Service สำหรับ Project Operations
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการตั้งค่าและการใช้ข้อมูลการกำหนดค่าใน Project Operations
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085805"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="df5b7-103">ตั้งค่าและใช้ข้อมูลการกำหนดค่าใน Common Data Service สำหรับ Project Operations</span><span class="sxs-lookup"><span data-stu-id="df5b7-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="df5b7-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="df5b7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="df5b7-105">ติดตั้งโปรแกรมตั้งค่าและข้อมูลการกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="df5b7-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="df5b7-106">ดาวน์โหลด ยกเลิกการบล็อก และ unzip [แพคเกจโปรแรกมตั้งค่าและข้อมูลการกำหนดค่า](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip)</span><span class="sxs-lookup"><span data-stu-id="df5b7-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="df5b7-107">ไปที่โฟลเดอร์ที่ unzip และเรียกใช้ไฟล์ปฏิบัติการ *DataMigrationUtility*</span><span class="sxs-lookup"><span data-stu-id="df5b7-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="df5b7-108">ในเพจ 1 ของวิซาร์ดการย้ายการกำหนดค่า Common Data Service (CMT) เลือก **นำเข้าข้อมูล** แล้วเลือก **ดำเนินการต่อ**</span><span class="sxs-lookup"><span data-stu-id="df5b7-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![การโอนย้ายการตั้งค่าคอนฟิก](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="df5b7-110">ในเพจ 2 ของวิซาร์ด CMT ให้เลือก **Microsoft 365** เป็น **ชนิดการปรับใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="df5b7-110">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="df5b7-111">เลือกกล่องกาเครื่องหมาย **แสดงรายชื่อขององค์กรที่มีอยู่** และ **แสดงขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="df5b7-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="df5b7-112">เลือกภูมิภาคของผู้เช่าของคุณ ป้อนข้อมูลประจำตัวของคุณ และเลือก **เข้าสู่ระบบ**</span><span class="sxs-lookup"><span data-stu-id="df5b7-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![การลงชื่อเข้าใช้การกำหนดค่า](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="df5b7-114">ในเพจ 3 จากรายชื่อองค์กรในผู้เช่า ให้เลือกองค์กรที่คุณต้องการนำเข้าข้อมูลสาธิต และเลือก **เข้าสู่ระบบ**</span><span class="sxs-lookup"><span data-stu-id="df5b7-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="df5b7-115">ในเพจ 4 เลือกไฟล์ zip *SampleSetupAndConfigData* จากโฟลเดอร์ที่ขยาย</span><span class="sxs-lookup"><span data-stu-id="df5b7-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![การเลือกไฟล์ Zip](./media/3ZipFile.png)

![เลือกไฟล์](./media/4SelectAFile.png)

9. <span data-ttu-id="df5b7-118">หลังจากเลือกไฟล์ zip แล้ว ให้เลือก **นำเข้าข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="df5b7-118">After the zip file is selected, select **Import Data**.</span></span>

![นำเข้าข้อมูล](./media/5ImportData.png)

10. <span data-ttu-id="df5b7-120">การนำเข้าจะทำงานประมาณสองถึงสิบนาที ขึ้นอยู่กับความเร็วเครือข่ายของคุณ</span><span class="sxs-lookup"><span data-stu-id="df5b7-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="df5b7-121">หลังจากนำเข้าเสร็จแล้ว ให้ออกจากวิซาร์ด CMT</span><span class="sxs-lookup"><span data-stu-id="df5b7-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="df5b7-122">ตรวจสอบองค์กรของคุณสำหรับข้อมูลใน 19 เอนทิตีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="df5b7-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="df5b7-123">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="df5b7-123">Currency</span></span>
  - <span data-ttu-id="df5b7-124">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="df5b7-124">Organizational Unit</span></span>
  - <span data-ttu-id="df5b7-125">ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="df5b7-125">Contact</span></span>
  - <span data-ttu-id="df5b7-126">กลุ่มภาษี</span><span class="sxs-lookup"><span data-stu-id="df5b7-126">Tax Group</span></span>
  - <span data-ttu-id="df5b7-127">กลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="df5b7-127">Customer Group</span></span>
  - <span data-ttu-id="df5b7-128">หน่วย</span><span class="sxs-lookup"><span data-stu-id="df5b7-128">Unit</span></span>
  - <span data-ttu-id="df5b7-129">กลุ่มของหน่วย</span><span class="sxs-lookup"><span data-stu-id="df5b7-129">Unit Group</span></span>
  - <span data-ttu-id="df5b7-130">ราคาตลาด</span><span class="sxs-lookup"><span data-stu-id="df5b7-130">Price List</span></span>
  - <span data-ttu-id="df5b7-131">ราคาตลาดสำหรับพารามิเตอร์โครงการ</span><span class="sxs-lookup"><span data-stu-id="df5b7-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="df5b7-132">ความถี่ของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="df5b7-132">Invoice Frequency</span></span>
  - <span data-ttu-id="df5b7-133">ประเภททรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="df5b7-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="df5b7-134">ประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="df5b7-134">Transaction Category</span></span>
  - <span data-ttu-id="df5b7-135">ประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="df5b7-135">Expense Category</span></span>
  - <span data-ttu-id="df5b7-136">ราคาตามบทบาท</span><span class="sxs-lookup"><span data-stu-id="df5b7-136">Role Price</span></span>
  - <span data-ttu-id="df5b7-137">ราคาของประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="df5b7-137">Transaction Category Price</span></span>
  - <span data-ttu-id="df5b7-138">คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="df5b7-138">Characteristic</span></span>
  - <span data-ttu-id="df5b7-139">ทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="df5b7-139">Bookable Resource</span></span>
  - <span data-ttu-id="df5b7-140">การกำหนดประเภททรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="df5b7-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="df5b7-141">คุณลักษณะทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="df5b7-141">Bookable Resource Characteristic</span></span>

![การนำเข้าเสร็จสมบูรณ์](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="df5b7-143">ปรับปรุงการกำหนดค่า Project Operations</span><span class="sxs-lookup"><span data-stu-id="df5b7-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="df5b7-144">นำทางไปยังสภาพแวดล้อม CE</span><span class="sxs-lookup"><span data-stu-id="df5b7-144">Navigate to the CE environment.</span></span> <span data-ttu-id="df5b7-145">คุณสามารถค้นหาได้โดยเปิด [ศูนย์จัดการ Power Platform](https://admin.powerplatform.microsoft.com/environments) เลือกสภาพแวดล้อม แล้วเลือก **เปิดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="df5b7-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![เปิดสภาพแวดล้อม](./media/7OpenEnvironment.png)

2. <span data-ttu-id="df5b7-147">ไปที่ **โครงการ** > **ทรัพยากร** จากนั้นเลือก **ใหม่** เพื่อสร้างทรัพยากรที่สามารถจองได้สำหรับผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="df5b7-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![ทรัพยากรที่สามารถจองได้](./media/8BookableResources.png)

3. <span data-ttu-id="df5b7-149">บนแท็บ **ทั่วไป** เลือกผู้ใช้ที่เป็นผู้ดูแลระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="df5b7-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="df5b7-150">ตรวจสอบว่าโซนเวลาตรงกับสถานที่ที่คุณอยู่</span><span class="sxs-lookup"><span data-stu-id="df5b7-150">Verify that the time zone matches the one you are in.</span></span> 

![ทรัพยากรที่สามารถจองได้ใหม่](./media/9NewBookableResource.png)

4. <span data-ttu-id="df5b7-152">บนแท็บ **การจัดกำหนดการ** ในฟิลด์ **บริษัท** เลือกบริษัท **USPM** แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="df5b7-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![แท็บการจัดกำหนดการ](./media/10SchedulingTab.png)

5. <span data-ttu-id="df5b7-154">เลือกแท็บ **ชั่วโมงทำงาน**</span><span class="sxs-lookup"><span data-stu-id="df5b7-154">Select the **Work hours** tab.</span></span>  

![ชั่วโมงทำงาน](./media/11WorkHours.png)

6. <span data-ttu-id="df5b7-156">ดับเบิลคลิกที่ค่าใดๆ ในปฏิทิน และเลือก **แก้ไข** > **เหตุการณ์ทั้งหมดในชุด**</span><span class="sxs-lookup"><span data-stu-id="df5b7-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![ปฏิทินงาน](./media/12WorkCalendar.png)

7. <span data-ttu-id="df5b7-158">เปลี่ยนชั่วโมงทำงานเป็นแปด (8) ชั่วโมงต่อวัน ทำเครื่องหมายวันหยุดสุดสัปดาห์เป็นวันที่ไม่ทำงาน และตรวจสอบให้แน่ใจว่าโซนเวลาตรงกับสถานที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="df5b7-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="df5b7-159">เลือก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="df5b7-159">Select **Save and close**.</span></span>

![ปรับปรุงปฏิทิน](./media/13UpdateCalendar.png)

9. <span data-ttu-id="df5b7-161">ไปที่ **การตั้งค่า** > **แม่แบบปฏิทิน** และเลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="df5b7-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![แม่แบบปฏิทิน](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="df5b7-163">ป้อนชื่อ เลือกทรัพยากรแม่แบบที่คุณสร้างขึ้น จากนั้นเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="df5b7-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![บันทึกแม่แบบปฏิทิน](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="df5b7-165">ไปที่ **พารามิเตอร์** แล้วดับเบิลคลิกที่เรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="df5b7-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![พารามิเตอร์โครงการ](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="df5b7-167">ปรับปรุงฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="df5b7-167">Update the following fields:</span></span>

 - <span data-ttu-id="df5b7-168">**บริษัทเริ่มต้น** : USPM</span><span class="sxs-lookup"><span data-stu-id="df5b7-168">**Default company** : USPM</span></span>
 - <span data-ttu-id="df5b7-169">**หน่วยองค์กรเริ่มต้น** : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="df5b7-169">**Default Organizational Unit** : Contoso Robotics Global</span></span>
 - <span data-ttu-id="df5b7-170">**ความถี่ของใบแจ้งหนี้** : วันที่เจ็ดและวันสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="df5b7-170">**Invoice Frequency** : Seventh and Last day</span></span>
 - <span data-ttu-id="df5b7-171">**แม่แบบชั่วโมงทำงาน** : เปลี่ยนเป็นแม่แบบที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="df5b7-171">**Work hour template** : Change to the template you created.</span></span>

13. <span data-ttu-id="df5b7-172">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="df5b7-172">Select **Save**.</span></span> 

![พารามิเตอร์โครงการที่ปรับปรุง](./media/17UpdatedProjectParameters.png)
