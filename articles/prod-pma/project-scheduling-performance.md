---
title: ประสิทธิภาพการจัดกำหนดการทรัพยากรโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีปรับปรุงประสิทธิภาพของการจัดกำหนดการทรัพยากรสำหรับโครงการจำนวนมาก
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 34c31570778f9b64c23387112cf56fa1139cd0fd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289032"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="cf312-103">ประสิทธิภาพการจัดกำหนดการทรัพยากรโครงการ</span><span class="sxs-lookup"><span data-stu-id="cf312-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="cf312-104">ปัญหาด้านประสิทธิภาพที่เกี่ยวข้องกับการจัดกำหนดการทรัพยากรอาจเกิดขึ้นได้เมื่อจำนวนโครงการถึงหลักพัน</span><span class="sxs-lookup"><span data-stu-id="cf312-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="cf312-105">เพื่อปรับปรุงประสิทธิภาพการจัดกำหนดการทรัพยากร มีคุณลักษณะที่ช่วยให้ผู้ใช้สามารถลดเวลาในการเปิดใช้ฟอร์มความพร้อมใช้งานของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="cf312-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="cf312-106">โดยเฉพาะ สิ่งนี้จะลบกระบวนการซิงโครไนซ์การรวบรวมความจุของทรัพยากร และใช้ตาราง **ResProjectResource** เพื่อเพิ่มความเร็วในการค้นหาทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="cf312-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="cf312-107">โปรดทราบว่าตาราง **ResRollup** จะไม่ถูกใช้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="cf312-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf312-108">หากมีการพึ่งพากระบวนการซิงโครไนซ์การรวบรวมความจุทรัพยากรหรือตาราง **ResProjectResource** ห้ามใช้คุณลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="cf312-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="cf312-109">เปิดใช้งานการปรับปรุงประสิทธิภาพการทำงานการจัดกำหนดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="cf312-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="cf312-110">ในการเปิดใช้งานการปรับปรุงประสิทธิภาพการทำงานการจัดกำหนดการทรัพยากร ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cf312-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="cf312-111">ไปที่ **การจัดการคุณลักษณะ** > **ทั้งหมด** และในรายการคุณลักษณะ ให้ค้นหา **เปิดใช้งานคุณลักษณะการปรับปรุงประสิทธิภาพการทำงานการจัดกำหนดการทรัพยากรโครงการ**</span><span class="sxs-lookup"><span data-stu-id="cf312-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="cf312-112">เลือก **เปิดใช้งานตอนนี้**</span><span class="sxs-lookup"><span data-stu-id="cf312-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="cf312-113">หากคุณไม่พบคุณลักษณะในรายการ ให้เลือก **ตรวจสอบสำหรับการอัปเดต** เพื่อรีเฟรชรายการ</span><span class="sxs-lookup"><span data-stu-id="cf312-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="cf312-114">รีเฟรชเบราว์เซอร์ของคุณ แล้วไปที่ **การจัดการโครงการและการบัญชี** > **เป็นระยะ** > **ทรัพยากรโครงการ** > **ซิงโครไนซ์ความจุปฏิทินทรัพยากรในทุกบริษัท**</span><span class="sxs-lookup"><span data-stu-id="cf312-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="cf312-115">ตั้งค่า **ลบเรกคอร์ดความจุที่มีอยู่** เป็น **ใช่** เพื่อลบข้อมูลก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="cf312-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="cf312-116">หากคุณต้องการสร้างข้อมูลส่วนเพิ่ม ให้ตั้งค่าเป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="cf312-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="cf312-117">ในฟิลด์ **รหัสรอบระยะเวลา** เลือกช่วงเวลาที่ควรสร้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cf312-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="cf312-118">หากคุณเลือกรหัสรอบระยะเวลา ไม่จำเป็นต้องกำหนดวันที่เริ่มต้นและวันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="cf312-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="cf312-119">หากคุณทิ้งฟิลด์ **รหัสรอบระยะเวลา** ว่าง เลือกวันที่เริ่มต้นและวันที่สิ้นสุดที่ต้องการเพื่อสร้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cf312-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="cf312-120">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cf312-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="cf312-121">สิ่งนี้จะกระจายข้อมูลทั่วไปไปยังตาราง **ResCalendarCapacity** ทั่วบริษัททั้งหมดในสภาพแวดล้อมของคุณ ดังนั้นชุดงานจะต้องทำงานในนิติบุคคลเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="cf312-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="cf312-122">ข้อมูลในชุดงานนี้จำเป็นในการคำนวณความจุของทรัพยากรผ่านปฏิทินที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="cf312-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="cf312-123">ไปที่ **การจัดการโครงการและการบัญชี** > **เป็นระยะ** > **ทรัพยากรโครงการ** > **เติมทรัพยากรโครงการในทุกบริษัท** จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cf312-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="cf312-124">นี่คือสคริปต์อัปเกรดข้อมูลสำหรับข้อมูลทั่วไปในตาราง **ResProjectResource** **ResCalendarDateTimeRange** และ **ResEffectiveDateTimeRange**</span><span class="sxs-lookup"><span data-stu-id="cf312-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="cf312-125">ค่าสำหรับฟิลด์ **PSAPRojSchedRole.RootActivity** มีการอัปเดตด้วย</span><span class="sxs-lookup"><span data-stu-id="cf312-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="cf312-126">หากไม่ได้เรียกใช้ คุณจะได้รับคำเตือนเมื่อคุณพยายามเรียกใช้การดำเนินการจัดกำหนดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="cf312-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="cf312-127">ปิดใช้งานการปรับปรุงประสิทธิภาพการทำงานการจัดกำหนดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="cf312-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="cf312-128">ไปที่ **การจัดการคุณลักษณะ** > **ทั้งหมด**  และค้นหา **เปิดใช้งานคุณลักษณะการปรับปรุงประสิทธิภาพการทำงานการจัดกำหนดการทรัพยากรโครงการ**</span><span class="sxs-lookup"><span data-stu-id="cf312-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="cf312-129">เลือกคุณสมบัติ จากนั้นเลือกปุ่ม **ปิดการใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="cf312-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="cf312-130">รีเฟรชเบราว์เซอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cf312-130">Refresh your browser.</span></span>
4. <span data-ttu-id="cf312-131">ไปที่ **การจัดการโครงการและการบัญชี** > **เป็นระยะ** > **การซิงโครไนซ์กำลังการผลิต** > **ซิงโครไนซ์ค่าสะสมของกำลังการผลิตของทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="cf312-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="cf312-132">บนหน้า **การซิงโครไนซ์การรวบรวมความจุ** ตั้งค่า **ลบเรกคอร์ดความจุที่มีอยู่** เป็น **ใช่** เพื่อลบข้อมูลก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="cf312-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="cf312-133">หากคุณต้องการสร้างข้อมูลส่วนเพิ่ม ให้ตั้งค่าเป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="cf312-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="cf312-134">ในฟิลด์ **รหัสรอบระยะเวลา** เลือกช่วงเวลาที่ควรสร้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cf312-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="cf312-135">หากคุณเลือกรหัสรอบระยะเวลา ไม่จำเป็นต้องกำหนดวันที่เริ่มต้นและวันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="cf312-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="cf312-136">หากคุณทิ้งฟิลด์ **รหัสรอบระยะเวลา** ว่าง เลือกวันที่เริ่มต้นและวันที่สิ้นสุดที่ต้องการเพื่อสร้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cf312-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="cf312-137">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cf312-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="cf312-138">สิ่งนี้จะกระจายข้อมูลทั่วไปไปยังตาราง **ResRollup** ทั่วบริษัททั้งหมดในสภาพแวดล้อมของคุณ ดังนั้นชุดงานจะต้องทำงานในนิติบุคคลเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="cf312-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="cf312-139">งานชุดนี้จำเป็นสำหรับมุมมอง **ความพร้อมของทรัพยากร** ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="cf312-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="cf312-140">หากไม่ได้เรียกใช้งานชุดนี้ ข้อมูล **ResRollup** จะถูกสร้างขึ้นทันที ซึ่งอาจต้องใช้เวลา</span><span class="sxs-lookup"><span data-stu-id="cf312-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]