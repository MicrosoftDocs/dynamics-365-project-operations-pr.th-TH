---
title: ตั้งค่าและใช้ข้อมูลการกำหนดค่าใน Common Data Service
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการตั้งค่าและการใช้ข้อมูลการกำหนดค่าใน Project Operations
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001314"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="98211-103">ตั้งค่าและใช้ข้อมูลการกำหนดค่าใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="98211-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="98211-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="98211-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="98211-105">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="98211-105">Prerequisites</span></span>

<span data-ttu-id="98211-106">ก่อนที่คุณจะเริ่มกำหนดค่าข้อมูลใน Common Data Service (CDS) ต้องเป็นไปตามข้อกำหนดเบื้องต้นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="98211-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="98211-107">จัดเตรียมสภาพแวดล้อม CDS และสภาพแวดล้อม Dynamics 365 Finance สำหรับ Project Operations</span><span class="sxs-lookup"><span data-stu-id="98211-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="98211-108">ข้อมูลนิติบุคคลจาก Dynamics 365 Finance ถูกแบ่งปันกับสภาพแวดล้อม CDS</span><span class="sxs-lookup"><span data-stu-id="98211-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="98211-109">ซึ่งหมายความว่าเอนทิตี **บริษัท** ใน CDS มีเรกคอร์ดบริษัทดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="98211-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="98211-110">THPM</span><span class="sxs-lookup"><span data-stu-id="98211-110">THPM</span></span>
  - <span data-ttu-id="98211-111">USPM</span><span class="sxs-lookup"><span data-stu-id="98211-111">USPM</span></span>
  - <span data-ttu-id="98211-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="98211-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="98211-113">ติดตั้งโปรแกรมตั้งค่าและข้อมูลการกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="98211-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="98211-114">ดาวน์โหลด ยกเลิกการบล็อก และ unzip [แพคเกจโปรแรกมตั้งค่าและข้อมูลการกำหนดค่า](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip)</span><span class="sxs-lookup"><span data-stu-id="98211-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="98211-115">ไปที่โฟลเดอร์ที่ unzip และเรียกใช้ไฟล์ปฏิบัติการ *DataMigrationUtility*</span><span class="sxs-lookup"><span data-stu-id="98211-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="98211-116">ในเพจ 1 ของวิซาร์ดการย้ายการกำหนดค่า Common Data Service (CMT) เลือก **นำเข้าข้อมูล** แล้วเลือก **ดำเนินการต่อ**</span><span class="sxs-lookup"><span data-stu-id="98211-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![การโอนย้ายการตั้งค่าคอนฟิก](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="98211-118">ในเพจ 2 ของวิซาร์ด CMT ให้เลือก **Microsoft 365** เป็น **ชนิดการปรับใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="98211-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="98211-119">เลือกกล่องกาเครื่องหมาย **แสดงรายชื่อขององค์กรที่มีอยู่** และ **แสดงขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="98211-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="98211-120">เลือกภูมิภาคของผู้เช่าของคุณ ป้อนข้อมูลประจำตัวของคุณ และเลือก **เข้าสู่ระบบ**</span><span class="sxs-lookup"><span data-stu-id="98211-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![การลงชื่อเข้าใช้การกำหนดค่า](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="98211-122">ในเพจ 3 จากรายชื่อองค์กรในผู้เช่า ให้เลือกองค์กรที่คุณต้องการนำเข้าข้อมูลสาธิต และเลือก **เข้าสู่ระบบ**</span><span class="sxs-lookup"><span data-stu-id="98211-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="98211-123">ในเพจ 4 เลือกไฟล์ zip *SampleSetupAndConfigData* จากโฟลเดอร์ที่ขยาย</span><span class="sxs-lookup"><span data-stu-id="98211-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![การเลือกไฟล์ Zip](./media/3ZipFile.png)

![เลือกไฟล์](./media/4SelectAFile.png)

9. <span data-ttu-id="98211-126">หลังจากเลือกไฟล์ zip แล้ว ให้เลือก **นำเข้าข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="98211-126">After the zip file is selected, select **Import Data**.</span></span>

![นำเข้าข้อมูล](./media/5ImportData.png)

10. <span data-ttu-id="98211-128">การนำเข้าจะทำงานประมาณสองถึงสิบนาที ขึ้นอยู่กับความเร็วเครือข่ายของคุณ</span><span class="sxs-lookup"><span data-stu-id="98211-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="98211-129">หลังจากนำเข้าเสร็จแล้ว ให้ออกจากวิซาร์ด CMT</span><span class="sxs-lookup"><span data-stu-id="98211-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="98211-130">ตรวจสอบองค์กรของคุณสำหรับข้อมูลใน 26 เอนทิตีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="98211-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="98211-131">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="98211-131">Currency</span></span>
  - <span data-ttu-id="98211-132">แผนภูมิของบัญชี</span><span class="sxs-lookup"><span data-stu-id="98211-132">Chart of Accounts</span></span>
  - <span data-ttu-id="98211-133">ปฏิทินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="98211-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="98211-134">ชนิดอัตราแลกเปลี่ยนสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="98211-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="98211-135">วันที่การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="98211-135">Payment Day</span></span>
  - <span data-ttu-id="98211-136">กำหนดการของการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="98211-136">Payment Schedule</span></span>
  - <span data-ttu-id="98211-137">เงื่อนไขการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="98211-137">Payment Term</span></span>
  - <span data-ttu-id="98211-138">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="98211-138">Organizational Unit</span></span>
  - <span data-ttu-id="98211-139">ผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="98211-139">Contact</span></span>
  - <span data-ttu-id="98211-140">กลุ่มภาษี</span><span class="sxs-lookup"><span data-stu-id="98211-140">Tax Group</span></span>
  - <span data-ttu-id="98211-141">กลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="98211-141">Customer Group</span></span>
  - <span data-ttu-id="98211-142">กลุ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="98211-142">Vendor Group</span></span>
  - <span data-ttu-id="98211-143">หน่วย</span><span class="sxs-lookup"><span data-stu-id="98211-143">Unit</span></span>
  - <span data-ttu-id="98211-144">กลุ่มของหน่วย</span><span class="sxs-lookup"><span data-stu-id="98211-144">Unit Group</span></span>
  - <span data-ttu-id="98211-145">ราคาตลาด</span><span class="sxs-lookup"><span data-stu-id="98211-145">Price List</span></span>
  - <span data-ttu-id="98211-146">ราคาตลาดสำหรับพารามิเตอร์โครงการ</span><span class="sxs-lookup"><span data-stu-id="98211-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="98211-147">ความถี่ของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="98211-147">Invoice Frequency</span></span>
  - <span data-ttu-id="98211-148">ประเภททรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="98211-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="98211-149">ประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="98211-149">Transaction Category</span></span>
  - <span data-ttu-id="98211-150">ประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="98211-150">Expense Category</span></span>
  - <span data-ttu-id="98211-151">ราคาตามบทบาท</span><span class="sxs-lookup"><span data-stu-id="98211-151">Role Price</span></span>
  - <span data-ttu-id="98211-152">ราคาของประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="98211-152">Transaction Category Price</span></span>
  - <span data-ttu-id="98211-153">คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="98211-153">Characteristic</span></span>
  - <span data-ttu-id="98211-154">ทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="98211-154">Bookable Resource</span></span>
  - <span data-ttu-id="98211-155">การกำหนดประเภททรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="98211-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="98211-156">คุณลักษณะทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="98211-156">Bookable Resource Characteristic</span></span>

![การนำเข้าเสร็จสมบูรณ์](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="98211-158">ปรับปรุงการกำหนดค่า Project Operations</span><span class="sxs-lookup"><span data-stu-id="98211-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="98211-159">นำทางไปยังสภาพแวดล้อม CE</span><span class="sxs-lookup"><span data-stu-id="98211-159">Navigate to the CE environment.</span></span> <span data-ttu-id="98211-160">คุณสามารถค้นหาได้โดยเปิด [ศูนย์จัดการ Power Platform](https://admin.powerplatform.microsoft.com/environments) เลือกสภาพแวดล้อม แล้วเลือก **เปิดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="98211-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![เปิดสภาพแวดล้อม](./media/7OpenEnvironment.png)

2. <span data-ttu-id="98211-162">ไปที่ **โครงการ** > **ทรัพยากร** จากนั้นเลือก **ใหม่** เพื่อสร้างทรัพยากรที่สามารถจองได้สำหรับผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="98211-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![ทรัพยากรที่สามารถจองได้](./media/8BookableResources.png)

3. <span data-ttu-id="98211-164">บนแท็บ **ทั่วไป** เลือกผู้ใช้ที่เป็นผู้ดูแลระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="98211-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="98211-165">ตรวจสอบว่าโซนเวลาตรงกับสถานที่ที่คุณอยู่</span><span class="sxs-lookup"><span data-stu-id="98211-165">Verify that the time zone matches the one you are in.</span></span> 

![ทรัพยากรที่สามารถจองได้ใหม่](./media/9NewBookableResource.png)

4. <span data-ttu-id="98211-167">บนแท็บ **การจัดกำหนดการ** ในฟิลด์ **บริษัท** เลือกบริษัท **USPM** แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="98211-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![แท็บการจัดกำหนดการ](./media/10SchedulingTab.png)

5. <span data-ttu-id="98211-169">เลือกแท็บ **ชั่วโมงทำงาน**</span><span class="sxs-lookup"><span data-stu-id="98211-169">Select the **Work hours** tab.</span></span>  

![ชั่วโมงทำงาน](./media/11WorkHours.png)

6. <span data-ttu-id="98211-171">ดับเบิลคลิกที่ค่าใดๆ ในปฏิทิน และเลือก **แก้ไข** > **เหตุการณ์ทั้งหมดในชุด**</span><span class="sxs-lookup"><span data-stu-id="98211-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![ปฏิทินงาน](./media/12WorkCalendar.png)

7. <span data-ttu-id="98211-173">เปลี่ยนชั่วโมงทำงานเป็นแปด (8) ชั่วโมงต่อวัน ทำเครื่องหมายวันหยุดสุดสัปดาห์เป็นวันที่ไม่ทำงาน และตรวจสอบให้แน่ใจว่าโซนเวลาตรงกับสถานที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="98211-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="98211-174">เลือก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="98211-174">Select **Save and close**.</span></span>

![ปรับปรุงปฏิทิน](./media/13UpdateCalendar.png)

9. <span data-ttu-id="98211-176">ไปที่ **การตั้งค่า** > **แม่แบบปฏิทิน** และเลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="98211-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![แม่แบบปฏิทิน](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="98211-178">ป้อนชื่อ เลือกทรัพยากรแม่แบบที่คุณสร้างขึ้น จากนั้นเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="98211-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![บันทึกแม่แบบปฏิทิน](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="98211-180">ไปที่ **พารามิเตอร์** แล้วดับเบิลคลิกที่เรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="98211-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![พารามิเตอร์โครงการ](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="98211-182">ปรับปรุงฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="98211-182">Update the following fields:</span></span>

 - <span data-ttu-id="98211-183">**บริษัทเริ่มต้น**: USPM</span><span class="sxs-lookup"><span data-stu-id="98211-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="98211-184">**หน่วยองค์กรเริ่มต้น**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="98211-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="98211-185">**ความถี่ของใบแจ้งหนี้**: วันที่เจ็ดและวันสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="98211-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="98211-186">**แม่แบบชั่วโมงทำงาน**: เปลี่ยนเป็นแม่แบบที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="98211-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="98211-187">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="98211-187">Select **Save**.</span></span> 

![พารามิเตอร์โครงการที่ปรับปรุง](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
