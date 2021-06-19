---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 18 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation รุ่นการปรับปรุง 18 V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: f7def50e77a83fd790b81b1b4fd36008ce293b0c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006669"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="fb453-103">Project Service Automation รุ่นการปรับปรุง 18 V3</span><span class="sxs-lookup"><span data-stu-id="fb453-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fb453-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="fb453-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="fb453-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fb453-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fb453-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="fb453-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fb453-107">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชันเพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="fb453-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="fb453-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="fb453-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fb453-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation V3 รุ่นการปรับปรุง 18</span><span class="sxs-lookup"><span data-stu-id="fb453-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="fb453-110">เวอร์ชันนี้มีหมายเลขรุ่น V3.10.8.12 และจะพร้อมให้ปรับปรุงด้วยตนเองโดยทั่วไปในเดือนเมษายน 2020</span><span class="sxs-lookup"><span data-stu-id="fb453-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="fb453-111">รุ่นการปรับปรุง 18</span><span class="sxs-lookup"><span data-stu-id="fb453-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fb453-112">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="fb453-112">Bug fixes</span></span>

<span data-ttu-id="fb453-113">**เวลาและค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="fb453-113">**Time and Expense**</span></span>

- <span data-ttu-id="fb453-114">แก้ไขแล้ว: โฟลว์ **เรียกคืน** **ร้องขอ** และ **ยกเลิกการอนุมัติ** อยู่นอกกระบวนการข้อยกเว้นและมีข้อความแสดงข้อผิดพลาดที่ไม่ชัดเจน</span><span class="sxs-lookup"><span data-stu-id="fb453-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="fb453-115">แก้ไขแล้ว: เมื่อ **ยกเลิกการอนุมัติ** ใช้ไม่ได้สำหรับค่าใช้จ่าย ข้อผิดพลาดของข้อยกเว้นที่เกี่ยวข้องจะไม่ถูกแสดง</span><span class="sxs-lookup"><span data-stu-id="fb453-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="fb453-116">แก้ไขแล้ว: กริดรายการเวลาแสดงผลวันที่ไม่ใช่วันทำงานในออสเตรเลียผิดพลาดหลังจากเปลี่ยนการเลื่อนเวลาตามฤดูกาล (DST) ในเดือนตุลาคม</span><span class="sxs-lookup"><span data-stu-id="fb453-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="fb453-117">แก้ไขแล้ว: ตรรกะค่าเริ่มต้นที่ไม่ถูกต้องทำให้ไม่สามารถส่งค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="fb453-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="fb453-118">แก้ไขแล้ว: เมื่อการอนุมัติรายการเวลาล้มเหลว การอนุมัติจะยังคงอยู่ในสถานะ **รอดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="fb453-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="fb453-119">แก้ไขแล้ว: ข้อผิดพลาดของ SQL ในการอนุมัติจำนวนมาก (การระงับ/หมดเวลา)</span><span class="sxs-lookup"><span data-stu-id="fb453-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="fb453-120">แก้ไขแล้ว: ปัญหาด้านประสิทธิภาพที่สำคัญเกี่ยวกับประสบการณ์ใช้งานของผู้ใช้ที่เกิดขึ้นจากการปรับปรุงสมาชิกทีมขณะอนุมัติรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="fb453-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="fb453-121">**การจัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="fb453-121">**Project Management**</span></span>

- <span data-ttu-id="fb453-122">แก้ไขแล้ว: การแจ้งเตือนโซนเวลาย้ายจากมุมมอง **การกระทบยอด** ไปยังฟอร์มหลักของ **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="fb453-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="fb453-123">แก้ไขแล้ว: ค่าเริ่มต้นของแม่แบบปฏิทินไม่ถูกต้องเมื่อเปิดฟอร์มโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="fb453-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="fb453-124">แก้ไขแล้ว: สำหรับเบราว์เซอร์ที่ใช้ chromium ผู้ใช้มีปัญหาในการเลือกลบงานก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="fb453-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="fb453-125">แก้ไขแล้ว: การสร้างหรือคัดลอก **โครงการจากแม่แบบเปล่า** จะดึงข้อมูลการมอบหมายที่ไม่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="fb453-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="fb453-126">แก้ไขแล้ว: ในบางกรณี การสร้างการมอบหมายใหม่จากกริดงานจะทำให้เกิดเรดคอร์ดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="fb453-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="fb453-127">แก้ไขแล้ว: ในโหมดด้วยตนเอง ผู้ใช้จะไม่สามารถอัปเดตวันที่เริ่มต้นหลังจากวันที่ในปัจจุบันที่บันทึกไว้ได้</span><span class="sxs-lookup"><span data-stu-id="fb453-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="fb453-128">**การจัดการทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="fb453-128">**Resource Management**</span></span>

- <span data-ttu-id="fb453-129">แก้ไขแล้ว: แถวผลรวมย่อยในมุมมอง **การกระทบยอด** คำนวณผลต่างการจองไม่ถูกต้องหลังจากขยายการจอง</span><span class="sxs-lookup"><span data-stu-id="fb453-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="fb453-130">แก้ไขแล้ว: มุมมอง **การกระทบยอด** แสดงการมอบหมายทรัพยากรไม่ถูกต้องเมื่อทรัพยากรที่สามารถจองได้มีปฏิทินที่ไม่ตรงกับปฏิทินโครงการ</span><span class="sxs-lookup"><span data-stu-id="fb453-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="fb453-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="fb453-131">**Sales**</span></span>

- <span data-ttu-id="fb453-132">แก้ไขแล้ว: เมื่อรายการเวลาได้รับอนุมัติใหม่ (**อนุมัติ > ยกเลิก >** อนุมัติอีกครั้ง) ระบบจะสร้างค่าใช้จ่ายจริงที่ไม่สามารถคิดค่าธรรมเนียมได้ซ้ำ</span><span class="sxs-lookup"><span data-stu-id="fb453-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]