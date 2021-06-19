---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 21 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation รุ่นการปรับปรุง 21 V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: dd894f27baac70238d0bd9e9b1a21a9a499e1ea7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002350"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="09320-103">Project Service Automation รุ่นการปรับปรุง 21 V3</span><span class="sxs-lookup"><span data-stu-id="09320-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="09320-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="09320-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="09320-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="09320-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="09320-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="09320-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="09320-107">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชัน เพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="09320-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="09320-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="09320-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="09320-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation V3 รุ่นการปรับปรุง 21</span><span class="sxs-lookup"><span data-stu-id="09320-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="09320-110">รุ่นนี้มีหมายเลขรุ่น V 3.10.32.50 และจะพร้อมให้ปรับปรุงด้วยตนเองโดยทั่วไปในเดือนมิถุนายน 2020</span><span class="sxs-lookup"><span data-stu-id="09320-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="09320-111">รุ่นการปรับปรุง 21</span><span class="sxs-lookup"><span data-stu-id="09320-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="09320-112">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="09320-112">Bug fixes</span></span>

<span data-ttu-id="09320-113">**เวลาและค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="09320-113">**Time and Expense**</span></span>

<span data-ttu-id="09320-114">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="09320-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="09320-115">เมื่อโฮสต์ไฟล์ **การควบคุมตารางรายการเวลา** ในแดชบอร์ด กริดไม่ใช้ความกว้างเต็มของคอนเทนเนอร์กริดแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="09320-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="09320-116">สำหรับโซนเวลาที่เฉพาะเจาะจงการควบคุมตาราง **รายการเวลา** ไม่แสดงเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="09320-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="09320-117">รายการเวลาที่อยู่หลัง 21:00 น. ปรากฏผิดวัน</span><span class="sxs-lookup"><span data-stu-id="09320-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="09320-118">ผู้ใช้ไม่สามารถส่งค่าใช้จ่ายได้หากหมวดค่าใช้จ่าย **ต้องใช้ใบเสร็จรับเงิน** ไม่มีค่า</span><span class="sxs-lookup"><span data-stu-id="09320-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="09320-119">**การจัดการทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="09320-119">**Resource Management**</span></span>

<span data-ttu-id="09320-120">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="09320-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="09320-121">การจองที่ไม่ใช้งานจะแสดงในมุมมอง **การกระทบยอด**</span><span class="sxs-lookup"><span data-stu-id="09320-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="09320-122">การเติมเต็มทรัพยากรทั่วไปขาดการตรวจสอบความถูกต้องเพื่อให้แน่ใจว่ามีสถานะการจองที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="09320-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="09320-123">**การจัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="09320-123">**Project Management**</span></span>

<span data-ttu-id="09320-124">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="09320-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="09320-125">แบบฟอร์มกริด **โครงการ** (**การมอบหมายทรัพยากร** **งาน** มุมมอง **การกระทบยอด** **ประมาณการค่าใช้จ่าย**) ยังคงสามารถแก้ไขได้แม้ว่าโปรเจ็กต์จะไม่ใช้งานแล้วก็ตาม</span><span class="sxs-lookup"><span data-stu-id="09320-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="09320-126">ไม่สามารถรวมลูกค้าที่ซ้ำกับลูกค้าที่เชื่อมโยงกับสัญญาโครงการที่ยืนยันได้</span><span class="sxs-lookup"><span data-stu-id="09320-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="09320-127">เมื่อเพิ่มทรัพยากรที่ไม่มีปฏิทินที่ถูกต้อง ระบบจะไม่ส่งคืนข้อความแสดงข้อผิดพลาดที่เป็นมิตรกับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="09320-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="09320-128">ปุ่ม **เพิ่มงาน** บนตารางงานถูกเปิดใช้งานเมื่อเชื่อมโยงโครงการกับ **add-in ของ Microsoft Project**</span><span class="sxs-lookup"><span data-stu-id="09320-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="09320-129">ความพยายามเพิ่มขึ้นอย่างไม่สามารถควบคุมได้เมื่องานที่มีหมวดหมู่ถูกกำหนดให้กับทรัพยากรที่มีบทบาท ซึ่งมีการกำหนดราคาต้นทุน</span><span class="sxs-lookup"><span data-stu-id="09320-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="09320-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="09320-130">**Sales**</span></span>

<span data-ttu-id="09320-131">ได้ทำการปรับปรุงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="09320-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="09320-132">**ความถี่ของใบแจ้งหนี้** และ **เริ่มต้นการเรียกเก็บเงิน** ถูกย้ายไปที่แถบ **กำหนดการใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="09320-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="09320-133">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="09320-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="09320-134">**ยอดรวมราคาขาย** เป็นศูนย์ (0) สำหรับ **ประเภท** ถึงแม้ว่า **บทบาท** มีราคาขายรวมที่ไม่ใช่ศูนย์</span><span class="sxs-lookup"><span data-stu-id="09320-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="09320-135">ลูกค้าไม่สามารถเปลี่ยนค่าของฟิลด์ **สถานะใบแจ้งหนี้** เป็น **พร้อมสำหรับการออกใบแจ้งหนี้** เมื่อกระบวนการที่กำหนดเองอื่นกำลังอัปเดตฟิลด์เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="09320-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="09320-136">ปุ่ม **รีเฟรชบรรทัดใบแจ้งหนี้** สามารถสร้างบรรทัดที่ซ้ำกันได้หลายบรรทัดหากเลือกซ้ำ ๆ</span><span class="sxs-lookup"><span data-stu-id="09320-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="09320-137">ปุ่ม **อัปเดตราคา** ไม่ทำงานบนกริดย่อย **ราคาบทบาท** ในฟอร์ม **แสดงผลแบบด่วน**</span><span class="sxs-lookup"><span data-stu-id="09320-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="09320-138">ตรรกะ **การแก้ไขปัญหารายการราคาสำหรับการขาย** จัดการเขตเวลาไม่ถูกต้อง ส่งผลให้การเลือกรายการราคาไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="09320-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="09320-139">**ต้นทุนจริงทั้งหมด** ของโครงการสามารถปิดด้วยจำนวนเศษหลังจากอนุมัติการป้อนครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="09320-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="09320-140">ตรรกะ **การแก้ไขปัญหาราคา** ไม่มีข้อความแสดงข้อผิดพลาดที่ใช้งานง่ายหาก **เรียกข้อมูล RolePrice แล้ว** ไม่มีค่าในฟิลด์ **'หน่วยหลัก'** และ **'ราคาในหน่วยหลัก'**</span><span class="sxs-lookup"><span data-stu-id="09320-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]