---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 32 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation รุ่นการปรับปรุง 32 V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129689"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="fba37-103">มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 32 V3</span><span class="sxs-lookup"><span data-stu-id="fba37-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fba37-104">เรายินดีที่จะประกาศการอัปเดตล่าสุดสำหรับแอป Microsoft Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="fba37-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="fba37-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fba37-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fba37-106">เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="fba37-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fba37-107">หากต้องการอัปเดตเป็นรุ่นนี้ ให้ไปที่หน้าศูนย์การจัดการสำหรับโซลูชันออนไลน์ของ Dynamics 365 และติดตั้งการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="fba37-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="fba37-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="fba37-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fba37-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation V3 รุ่นการปรับปรุง 32</span><span class="sxs-lookup"><span data-stu-id="fba37-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="fba37-110">รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.53.108 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตด้วยตนเองในเดือนมิถุนายน 2021</span><span class="sxs-lookup"><span data-stu-id="fba37-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="fba37-111">รุ่นการปรับปรุง 32</span><span class="sxs-lookup"><span data-stu-id="fba37-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fba37-112">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="fba37-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="fba37-113">ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="fba37-113">General</span></span>

- <span data-ttu-id="fba37-114">เมื่อการอัปเกรดหลักล้มเหลว ควรบล็อกเฉพาะจุดเข้าใช้งานแอปพลิเคชันหลักเท่านั้น เพื่อให้แน่ใจว่ายังคงเข้าถึงเอนทิตีที่ใช้ร่วมกันได้</span><span class="sxs-lookup"><span data-stu-id="fba37-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="fba37-115">เวลาและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="fba37-115">Time and Expense</span></span>

<span data-ttu-id="fba37-116">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="fba37-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="fba37-117">**TimeEntriesImportFromResourceAssignment** ไม่รักษาเวลาเริ่มต้นและสิ้นสุดของส่วนเส้นขอบการกำหนดทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="fba37-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="fba37-118">เมื่อคุณเลือก **เปิดรายการ** บนกริด **รายการเวลา** คุณอาจถูกป้องกันไม่ให้เลือกฟอร์มอื่น</span><span class="sxs-lookup"><span data-stu-id="fba37-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="fba37-119">ในขณะที่คุณนำเข้าการกำหนดไปยังรายการเวลา แบบสอบถามรหัสไคลเอนต์สามารถสร้าง URL ที่ยาวซึ่งล้มเหลวในการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="fba37-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="fba37-120">ในกริด **รายการเวลา** หลังจากที่ค่าถูกลบออกจากเซลล์แล้ว โฟกัสจะไม่คงอยู่ในตาราง</span><span class="sxs-lookup"><span data-stu-id="fba37-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="fba37-121">ปุ่ม **ปฏิเสธ** ถูกลบออกจากมุมมอง **กำลังดำเนินการอนุมัติ** เพื่อการอนุมัติที่ทันสมัย</span><span class="sxs-lookup"><span data-stu-id="fba37-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="fba37-122">ความเสถียรและประสิทธิภาพของการอนุมัติรายการเวลาจำนวนมากได้รับผลกระทบจากการชะงักงันและความล้มเหลวในการจัดการการปรับแต่งที่เกี่ยวข้องกับเอนทิตี **รายการเวลา**</span><span class="sxs-lookup"><span data-stu-id="fba37-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="fba37-123">การวางแผนโครงการ</span><span class="sxs-lookup"><span data-stu-id="fba37-123">Project Planning</span></span>

- <span data-ttu-id="fba37-124">ข้อยกเว้นการอ้างอิง null ถูกสร้างขึ้นเมื่อคุณอัปเดตโครงการที่มีค่า null ในฟิลด์ **หน่วยตามสัญญา**</span><span class="sxs-lookup"><span data-stu-id="fba37-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="fba37-125">**รีเฟรชผลรวมของโครงการ** คำนวณต้นทุนที่เหลืออยู่และยอดขายที่เหลืออยู่ในโครงการอย่างไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="fba37-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="fba37-126">การคำนวณราคาที่ซ้ำซ้อนส่งผลต่อประสิทธิภาพการทำงานที่เกี่ยวข้องกับการอัปเดตในโครงร่างการกำหนดทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="fba37-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="fba37-127">การจัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="fba37-127">Resource Management</span></span>

<span data-ttu-id="fba37-128">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="fba37-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="fba37-129">เมื่อความจุปฏิทินของทรัพยากรที่สามารถจองได้มีมากกว่า 1 Project Service Automation จะรับรู้ความจุเป็น 0 (ศูนย์) อย่างไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="fba37-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="fba37-130">ดังนั้น การวนซ้ำไม่สิ้นสุดจึงเกิดขึ้นในมุมมองกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="fba37-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="fba37-131">การขาย</span><span class="sxs-lookup"><span data-stu-id="fba37-131">Sales</span></span>

<span data-ttu-id="fba37-132">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="fba37-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="fba37-133">เมื่อมีการสร้างรายการสมุดรายวันที่มีประเภทธุรกรรมแบบกำหนดเอง ข้อยกเว้นการอ้างอิง null ต่อไปนี้จะเกิดขึ้น: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType (TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*</span><span class="sxs-lookup"><span data-stu-id="fba37-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="fba37-134">บทบาทและหมวดหมู่ที่ปิดใช้งานก่อนที่จะคัดลอกใบเสนอราคาไม่ควรเพิ่มไปยังบทบาทและหมวดหมู่ที่คิดค่าธรรมเนียมได้ของใบเสนอราคาที่คัดลอกใหม่</span><span class="sxs-lookup"><span data-stu-id="fba37-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="fba37-135">วันที่ของเอกสารและวันที่บัญชีไม่สอดคล้องกับวันที่เริ่มต้นที่ระบุไว้ในรายละเอียดรายการใบแจ้งหนี้ที่สร้างขึ้นโดยตรงบนร่างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="fba37-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="fba37-136">ข้อยกเว้นการอ้างอิงที่เป็นค่าว่างถูกสร้างขึ้นในสถานการณ์ที่เกี่ยวข้องกับการปิดใช้งานบทบาทและประเภทก่อนที่จะคัดลอกใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="fba37-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="fba37-137">การดำเนินการ **อัปเดตราคา** บนหน้า **โครงการ** ไม่ปรับปรุงประมาณการค่าใช้จ่ายและการประมาณการวัสดุ</span><span class="sxs-lookup"><span data-stu-id="fba37-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
