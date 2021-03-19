---
title: ตั้งค่าและใช้ข้อมูลการกำหนดค่าใน Common Data Service
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการตั้งค่าและการใช้ข้อมูลการกำหนดค่าใน Project Operations
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1651d3b3b85d3dc581bf61976fada249bafd6b7b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289842"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="c7316-103">ตั้งค่าและใช้ข้อมูลการกำหนดค่าใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c7316-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="c7316-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="c7316-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="c7316-105">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="c7316-105">Prerequisites</span></span>

<span data-ttu-id="c7316-106">ก่อนที่คุณจะกำหนดค่าข้อมูลใน Common Data Service (CDS) ต้องปฏิบัติตามข้อกำหนดเบื้องต้นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c7316-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="c7316-107">จัดเตรียมสภาพแวดล้อม CDS และสภาพแวดล้อม Dynamics 365 Finance สำหรับ Project Operations</span><span class="sxs-lookup"><span data-stu-id="c7316-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="c7316-108">ข้อมูลนิติบุคคลจาก Dynamics 365 Finance ถูกแบ่งปันกับสภาพแวดล้อม CDS</span><span class="sxs-lookup"><span data-stu-id="c7316-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="c7316-109">ซึ่งหมายความว่าเอนทิตี **บริษัท** ใน CDS มีเรกคอร์ดบริษัทดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c7316-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="c7316-110">THPM</span><span class="sxs-lookup"><span data-stu-id="c7316-110">THPM</span></span>
  - <span data-ttu-id="c7316-111">USPM</span><span class="sxs-lookup"><span data-stu-id="c7316-111">USPM</span></span>
  - <span data-ttu-id="c7316-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="c7316-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="c7316-113">ติดตั้งโปรแกรมตั้งค่าและข้อมูลการกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="c7316-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="c7316-114">ดาวน์โหลด ยกเลิกการบล็อก และ unzip [แพคเกจโปรแรกมตั้งค่าและข้อมูลการกำหนดค่า](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip)</span><span class="sxs-lookup"><span data-stu-id="c7316-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="c7316-115">ไปที่โฟลเดอร์ที่ unzip และเรียกใช้ไฟล์ปฏิบัติการ *DataMigrationUtility*</span><span class="sxs-lookup"><span data-stu-id="c7316-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="c7316-116">ในเพจ 1 ของวิซาร์ดการย้ายการกำหนดค่า Common Data Service (CMT) เลือก **นำเข้าข้อมูล** แล้วเลือก **ดำเนินการต่อ**</span><span class="sxs-lookup"><span data-stu-id="c7316-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![การโอนย้ายการตั้งค่าคอนฟิก](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="c7316-118">ในเพจ 2 ของวิซาร์ด CMT ให้เลือก **Microsoft 365** เป็น **ชนิดการปรับใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="c7316-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="c7316-119">เลือกกล่องกาเครื่องหมาย **แสดงรายชื่อขององค์กรที่มีอยู่** และ **แสดงขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="c7316-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="c7316-120">เลือกภูมิภาคของผู้เช่าของคุณ ป้อนข้อมูลประจำตัวของคุณ และเลือก **เข้าสู่ระบบ**</span><span class="sxs-lookup"><span data-stu-id="c7316-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![การลงชื่อเข้าใช้การกำหนดค่า](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="c7316-122">ในเพจ 3 จากรายชื่อองค์กรในผู้เช่า ให้เลือกองค์กรที่คุณต้องการนำเข้าข้อมูลสาธิต และเลือก **เข้าสู่ระบบ**</span><span class="sxs-lookup"><span data-stu-id="c7316-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="c7316-123">ในเพจ 4 เลือกไฟล์ zip *SampleSetupAndConfigData* จากโฟลเดอร์ที่ขยาย</span><span class="sxs-lookup"><span data-stu-id="c7316-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![การเลือกไฟล์ Zip](./media/3ZipFile.png)

![เลือกไฟล์](./media/4SelectAFile.png)

9. <span data-ttu-id="c7316-126">หลังจากเลือกไฟล์ zip แล้ว ให้เลือก **นำเข้าข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="c7316-126">After the zip file is selected, select **Import Data**.</span></span>

![นำเข้าข้อมูล](./media/5ImportData.png)

10. <span data-ttu-id="c7316-128">การนำเข้าจะทำงานประมาณสองถึงสิบนาที ขึ้นอยู่กับความเร็วเครือข่ายของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7316-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="c7316-129">หลังจากนำเข้าเสร็จแล้ว ให้ออกจากวิซาร์ด CMT</span><span class="sxs-lookup"><span data-stu-id="c7316-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="c7316-130">ตรวจสอบองค์กรของคุณสำหรับข้อมูลใน 19 เอนทิตีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c7316-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="c7316-131">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="c7316-131">Currency</span></span>
  - <span data-ttu-id="c7316-132">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="c7316-132">Organizational Unit</span></span>
  - <span data-ttu-id="c7316-133">ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="c7316-133">Contact</span></span>
  - <span data-ttu-id="c7316-134">กลุ่มภาษี</span><span class="sxs-lookup"><span data-stu-id="c7316-134">Tax Group</span></span>
  - <span data-ttu-id="c7316-135">กลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c7316-135">Customer Group</span></span>
  - <span data-ttu-id="c7316-136">หน่วย</span><span class="sxs-lookup"><span data-stu-id="c7316-136">Unit</span></span>
  - <span data-ttu-id="c7316-137">กลุ่มของหน่วย</span><span class="sxs-lookup"><span data-stu-id="c7316-137">Unit Group</span></span>
  - <span data-ttu-id="c7316-138">รายการราคา</span><span class="sxs-lookup"><span data-stu-id="c7316-138">Price List</span></span>
  - <span data-ttu-id="c7316-139">รายการราคาสำหรับพารามิเตอร์โครงการ</span><span class="sxs-lookup"><span data-stu-id="c7316-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="c7316-140">ความถี่ของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c7316-140">Invoice Frequency</span></span>
  - <span data-ttu-id="c7316-141">ประเภททรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="c7316-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="c7316-142">ประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="c7316-142">Transaction Category</span></span>
  - <span data-ttu-id="c7316-143">ประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="c7316-143">Expense Category</span></span>
  - <span data-ttu-id="c7316-144">ราคาตามบทบาท</span><span class="sxs-lookup"><span data-stu-id="c7316-144">Role Price</span></span>
  - <span data-ttu-id="c7316-145">ราคาของประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="c7316-145">Transaction Category Price</span></span>
  - <span data-ttu-id="c7316-146">คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="c7316-146">Characteristic</span></span>
  - <span data-ttu-id="c7316-147">ทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="c7316-147">Bookable Resource</span></span>
  - <span data-ttu-id="c7316-148">การกำหนดประเภททรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="c7316-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="c7316-149">คุณลักษณะทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="c7316-149">Bookable Resource Characteristic</span></span>

![การนำเข้าเสร็จสมบูรณ์](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="c7316-151">ปรับปรุงการกำหนดค่า Project Operations</span><span class="sxs-lookup"><span data-stu-id="c7316-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="c7316-152">นำทางไปยังสภาพแวดล้อม CE</span><span class="sxs-lookup"><span data-stu-id="c7316-152">Navigate to the CE environment.</span></span> <span data-ttu-id="c7316-153">คุณสามารถค้นหาได้โดยเปิด [ศูนย์จัดการ Power Platform](https://admin.powerplatform.microsoft.com/environments) เลือกสภาพแวดล้อม แล้วเลือก **เปิดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="c7316-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![เปิดสภาพแวดล้อม](./media/7OpenEnvironment.png)

2. <span data-ttu-id="c7316-155">ไปที่ **โครงการ** > **ทรัพยากร** จากนั้นเลือก **ใหม่** เพื่อสร้างทรัพยากรที่สามารถจองได้สำหรับผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7316-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![ทรัพยากรที่สามารถจองได้](./media/8BookableResources.png)

3. <span data-ttu-id="c7316-157">บนแท็บ **ทั่วไป** เลือกผู้ใช้ที่เป็นผู้ดูแลระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7316-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="c7316-158">ตรวจสอบว่าโซนเวลาตรงกับสถานที่ที่คุณอยู่</span><span class="sxs-lookup"><span data-stu-id="c7316-158">Verify that the time zone matches the one you are in.</span></span> 

![ทรัพยากรที่สามารถจองได้ใหม่](./media/9NewBookableResource.png)

4. <span data-ttu-id="c7316-160">บนแท็บ **การจัดกำหนดการ** ในฟิลด์ **บริษัท** เลือกบริษัท **USPM** แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c7316-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![แท็บการจัดกำหนดการ](./media/10SchedulingTab.png)

5. <span data-ttu-id="c7316-162">เลือกแท็บ **ชั่วโมงทำงาน**</span><span class="sxs-lookup"><span data-stu-id="c7316-162">Select the **Work hours** tab.</span></span>  

![ชั่วโมงทำงาน](./media/11WorkHours.png)

6. <span data-ttu-id="c7316-164">ดับเบิลคลิกที่ค่าใดๆ ในปฏิทิน และเลือก **แก้ไข** > **เหตุการณ์ทั้งหมดในชุด**</span><span class="sxs-lookup"><span data-stu-id="c7316-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![ปฏิทินงาน](./media/12WorkCalendar.png)

7. <span data-ttu-id="c7316-166">เปลี่ยนชั่วโมงทำงานเป็นแปด (8) ชั่วโมงต่อวัน ทำเครื่องหมายวันหยุดสุดสัปดาห์เป็นวันที่ไม่ทำงาน และตรวจสอบให้แน่ใจว่าโซนเวลาตรงกับสถานที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7316-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="c7316-167">เลือก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="c7316-167">Select **Save and close**.</span></span>

![ปรับปรุงปฏิทิน](./media/13UpdateCalendar.png)

9. <span data-ttu-id="c7316-169">ไปที่ **การตั้งค่า** > **แม่แบบปฏิทิน** และเลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c7316-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![แม่แบบปฏิทิน](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="c7316-171">ป้อนชื่อ เลือกทรัพยากรแม่แบบที่คุณสร้างขึ้น จากนั้นเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c7316-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![บันทึกแม่แบบปฏิทิน](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="c7316-173">ไปที่ **พารามิเตอร์** แล้วดับเบิลคลิกที่เรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="c7316-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![พารามิเตอร์โครงการ](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="c7316-175">ปรับปรุงฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c7316-175">Update the following fields:</span></span>

 - <span data-ttu-id="c7316-176">**บริษัทเริ่มต้น**: USPM</span><span class="sxs-lookup"><span data-stu-id="c7316-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="c7316-177">**หน่วยองค์กรเริ่มต้น**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="c7316-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="c7316-178">**ความถี่ของใบแจ้งหนี้**: วันที่เจ็ดและวันสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="c7316-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="c7316-179">**แม่แบบชั่วโมงทำงาน**: เปลี่ยนเป็นแม่แบบที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="c7316-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="c7316-180">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c7316-180">Select **Save**.</span></span> 

![พารามิเตอร์โครงการที่ปรับปรุง](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]