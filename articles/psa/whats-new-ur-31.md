---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 31 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation รุ่นการปรับปรุง 31 V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999154"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="e4388-103">มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 31 V3</span><span class="sxs-lookup"><span data-stu-id="e4388-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e4388-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="e4388-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e4388-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e4388-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e4388-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="e4388-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e4388-107">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชัน เพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="e4388-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="e4388-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="e4388-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e4388-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation V3 รุ่นการปรับปรุง 31</span><span class="sxs-lookup"><span data-stu-id="e4388-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="e4388-110">เวอร์ชันนี้มีหมายเลขรุ่น V3.10.52.77 และจะพร้อมให้ปรับปรุงด้วยตนเองโดยทั่วไปในเดือนพฤษภาคม 2021</span><span class="sxs-lookup"><span data-stu-id="e4388-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="e4388-111">รุ่นการปรับปรุง 31</span><span class="sxs-lookup"><span data-stu-id="e4388-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e4388-112">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="e4388-112">Bug fixes</span></span>

<span data-ttu-id="e4388-113">**เวลาและค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="e4388-113">**Time and Expense**</span></span>

<span data-ttu-id="e4388-114">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="e4388-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="e4388-115">ปุ่มคำสั่งควบคุมรายการเวลาบนหน้า **ทรัพยากรที่สามารถจองได้** ทำให้สับสน</span><span class="sxs-lookup"><span data-stu-id="e4388-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="e4388-116">ข้อยกเว้นการอ้างอิง Null ถูกสร้างขึ้นใน **Project.SetTrackingFields** เมื่ออนุมัติรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="e4388-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="e4388-117">**การจัดการทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="e4388-117">**Resource Management**</span></span>

<span data-ttu-id="e4388-118">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="e4388-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="e4388-119">**สร้างสมาชิกในกลุ่มคน** แสดงการตั้งค่าข้อมูลเมตาการตั้งค่าการจองอย่างไม่ถูกต้องสำหรับ **สถานะที่ยืนยันแล้วของการจองเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="e4388-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="e4388-120">เมื่ออัปเกรดจาก PSA 1.X เป็น 3.X กระบวนการอัปเกรดจะล้มเหลวที่ **UpgradeResourceRequirements**</span><span class="sxs-lookup"><span data-stu-id="e4388-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="e4388-121">**การขาย**</span><span class="sxs-lookup"><span data-stu-id="e4388-121">**Sales**</span></span>

<span data-ttu-id="e4388-122">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="e4388-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="e4388-123">รายได้จริงจะแปลงจำนวนเงินเป็นสกุลเงินของโครงการในกริดการติดตาม</span><span class="sxs-lookup"><span data-stu-id="e4388-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="e4388-124">ค่าเริ่มต้นของสกุลเงินไม่ชัดเจน เมื่อสร้างบรรทัดสมุดรายวัน รายการใบเสนอราคา และรายละเอียดการให้บริการตามสัญญา ในสถานการณ์ที่สกุลเงินพื้นฐานขององค์กรแตกต่างจากสกุลเงินของโครงการ</span><span class="sxs-lookup"><span data-stu-id="e4388-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="e4388-125">การสอบถาม **การตรวจสอบความถูกต้องของสมุดรายวันการแก้ไขที่รอดำเนินการ** ไม่ได้กรองตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="e4388-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="e4388-126">ยอดขายที่เหลือถูกคำนวณอย่างไม่ถูกต้องในโครงการ</span><span class="sxs-lookup"><span data-stu-id="e4388-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="e4388-127">ใบเสนอราคาตามผู้ติดต่อล้มเหลว เมื่อมีการสร้างขึ้นโดยไม่มีรายการราคา</span><span class="sxs-lookup"><span data-stu-id="e4388-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="e4388-128">ไม่มีการแสดงสปินเนอร์การประมวลผล เมื่อคุณเลือก **ยืนยันใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="e4388-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="e4388-129">ไม่มีการแสดงสปินเนอร์การประมวลผล เมื่อคุณเลือก **สร้างใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="e4388-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="e4388-130">การปิดใบเสนอราคาเป็นสูญหาย ไม่ได้เป็นการยกเลิกการจอง</span><span class="sxs-lookup"><span data-stu-id="e4388-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







