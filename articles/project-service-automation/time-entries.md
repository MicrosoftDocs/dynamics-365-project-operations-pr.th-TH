---
title: สร้างรายการเวลา
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการสร้างรายการเวลา
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 90f6450b-e0c4-4d86-b8f5-ffb1a2b1e38a
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ae3af7d62d93884c7fa9881394b7129daeb8bf7e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756468"
---
# <a name="create-time-entries"></a><span data-ttu-id="ba5ee-103">สร้างรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="ba5ee-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ba5ee-104">ในรุ่นก่อนหน้าของ Dynamics 365 Project Service Automation จะมีการป้อนรายการเวลาเป็นรายสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="ba5ee-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="ba5ee-105">ในรุ่นที่3 ของ Project Service Automation รายการเวลาจะถูกป้อนเป็นรายวัน</span><span class="sxs-lookup"><span data-stu-id="ba5ee-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="ba5ee-106">อย่างไรก็ตาม หลังจากที่มีการสร้างรายการได้สองสามรายการแล้ว คุณสามารถสร้างรายการจำนวนมากหรือคัดลอกรายการได้</span><span class="sxs-lookup"><span data-stu-id="ba5ee-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="ba5ee-107">สร้างรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="ba5ee-107">Create a time entry</span></span>

<span data-ttu-id="ba5ee-108">ทำตามขั้นตอนเหล่านี้เพื่อสร้างรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="ba5ee-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="ba5ee-109">ในเพจ **รายการเวลา** เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="ba5ee-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="ba5ee-110">ในกล่องโต้ตอบ **สร้างด่วน: รายการเวลา** ป้อนระยะเวลาของรายการเวลาในหน่วยนาที ชั่วโมง หรือวัน</span><span class="sxs-lookup"><span data-stu-id="ba5ee-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="ba5ee-111">ระยะเวลาต้องถูกป้อนในรูปแบบต่อไปนี้: *x* นาที *x* ชั่วโมง หรือ *x* วัน</span><span class="sxs-lookup"><span data-stu-id="ba5ee-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="ba5ee-112">ชั่วโมงและวันยังสามารถป้อนโดยใช้ค่าทศนิยม ตัวอย่างเช่น *x.x* ชั่วโมง หรือ *x.x* วัน</span><span class="sxs-lookup"><span data-stu-id="ba5ee-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="ba5ee-113">เลือกชนิดของรายการเวลาและโครงการที่คุณกำลังป้องรายการเวลาให้</span><span class="sxs-lookup"><span data-stu-id="ba5ee-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="ba5ee-114">ในฟิลด์ **งานโครงการ** ค้นหางานสำหรับรายการเวลานี้</span><span class="sxs-lookup"><span data-stu-id="ba5ee-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ba5ee-115">หากคุณกำลังสร้างรายการเวลาสำหรับงานที่ไม่ได้มอบหมายให้กับผู้ใช้ใด ในฟิลด์ **งานโครงการ** เลือกปุ่ม **ค้นหา** แล้วเลือก **เปลี่ยนมุมมอง** และเลือก **งานโครงการที่ใช้งานทั้งหมด** เพื่อแสดงงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="ba5ee-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="ba5ee-116">หากต้องการคำอธิบาย ป้อนคำอธิบายแล้วเลือก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="ba5ee-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="ba5ee-117">หลังจากที่สร้างและบันทึกรายการเวลาแล้ว คุณสามารถแก้ไขได้ในกริดรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="ba5ee-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="ba5ee-118">กริดรายการเวลาสนับสนุนการป้อนข้อมูลสองรูปแบบ:</span><span class="sxs-lookup"><span data-stu-id="ba5ee-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="ba5ee-119">คุณสามารถป้อนรายการเวลาในรูปแบบ **hh:mm**</span><span class="sxs-lookup"><span data-stu-id="ba5ee-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="ba5ee-120">รูปแบบนี้จะถูกแปลงเป็นชั่วโมงและเศษส่วน</span><span class="sxs-lookup"><span data-stu-id="ba5ee-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="ba5ee-121">คุณสามารถป้อนชั่วโมงและเศษส่วนได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="ba5ee-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="ba5ee-122">โปรดทราบว่าเศษส่วนของชั่วโมงไม่ใช่นาที</span><span class="sxs-lookup"><span data-stu-id="ba5ee-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="ba5ee-123">ดังนั้น 1.5 ชั่วโมงหมายถึง 1 ชั่วโมง 30 นาที</span><span class="sxs-lookup"><span data-stu-id="ba5ee-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="ba5ee-124">กฎเดียวกันนี้ใช้กับเศษส่วนของวัน</span><span class="sxs-lookup"><span data-stu-id="ba5ee-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="ba5ee-125">หนึ่งวันมี 24 ชั่วโมง และ 0.5 วันหมายถึง 12 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="ba5ee-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="ba5ee-126">สร้างรายการเวลาจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="ba5ee-126">Bulk create time entries</span></span>

<span data-ttu-id="ba5ee-127">อย่างไรก็ตาม หลังจากที่มีการสร้างรายการได้สองสามรายการแล้ว คุณสามารถสร้างรายการเวลาเพิ่มเติมได้หลายรายการในครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="ba5ee-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="ba5ee-128">ในเพจ **รายการเวลา** เลือก **คัดลอกสัปดาห์**</span><span class="sxs-lookup"><span data-stu-id="ba5ee-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="ba5ee-129">ในกลุ่มฟิลด์ **รอบระยะเวลาเริ่มต้น** ในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** ให้กำหนดระยะวันที่ที่จะคัดลอกรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="ba5ee-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="ba5ee-130">ในกลุ่มฟิลด์ **รอบระยะเวลาสิ้นสุด** ในฟิลด์ **วันที่เริ่มต้น** ให้ระบุวันที่ที่ต้องการสร้างรายการเวลาให้</span><span class="sxs-lookup"><span data-stu-id="ba5ee-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="ba5ee-131">เลือก **คัดลอก** เพื่อสร้างการคัดลอกของรายการเวลาที่เกี่ยวของกับวันของสัปดาห์ที่ได้ระบุไว้ในกลุ่มฟิลด์ **รอบระยะเวลาสิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="ba5ee-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="ba5ee-132">ตัวอย่างเช่น รายการเวลาสำหรับวันจันทร์ของสัปดาห์ที่ผ่านมา จะถูกคัดลอกไปยังวันจันทร์ของสัปดาห์ได้ระบุไว้ในกลุ่มฟิลด์ **รอบระยะเวลาที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="ba5ee-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="ba5ee-133">นำเข้าข้อมูลสำหรับรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="ba5ee-133">Import data for time entries</span></span>

<span data-ttu-id="ba5ee-134">คุณสามารถนำเข้าข้อมูลจากการจองและการมอบหมายโครงการ</span><span class="sxs-lookup"><span data-stu-id="ba5ee-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="ba5ee-135">เมื่อคุณนำเข้าข้อมูล คุณสามารถระบุช่วงวันที่ของการจอง ที่จะนำเข้าและเลือกการจองอย่างชัดเจนที่ควรจะถูกสร้างเป็นรายการเวลา **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="ba5ee-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="ba5ee-136">ความสามารถของการจัดกลุ่ม การเรียง การค้นหาและการกรอง</span><span class="sxs-lookup"><span data-stu-id="ba5ee-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="ba5ee-137">คุณสามารถจัดกลุ่มและกรองรายการเวลาเรียงตามมิติที่ระบุในคอลัมน์ได้</span><span class="sxs-lookup"><span data-stu-id="ba5ee-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="ba5ee-138">ในฟิลด์ **จัดกลุ่มตาม** ให้เลือกมิติเพื่อใช้กรองรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="ba5ee-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="ba5ee-139">คุณยังสามารถเรียงเรกคอร์ดรายการเวลาจากน้อยไปหามากหรือจากมากไปหาน้อยโดยใช้ลูกศรจัดเรียงหรือใช้ส่วนหัวของคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="ba5ee-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="ba5ee-140">นอกจากนี้ คุณสามารถแสดงหรือซ่อนรายการโดยการเลือกปุ่ม **กรอง** ในส่วนหัวของคอลัมน์จากนั้นในกล่อง **ค้นหา** ป้อนข้อความที่จะใช้ในการค้นหารายการเวลาตามชื่อโครงการ ตามงานโครงการ ตามรายการเวลา หรือตามทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="ba5ee-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
