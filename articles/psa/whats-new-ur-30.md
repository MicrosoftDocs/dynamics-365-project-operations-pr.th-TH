---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 30 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation รุ่นการปรับปรุง 30 V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010449"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="32d1b-103">มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 30 V3</span><span class="sxs-lookup"><span data-stu-id="32d1b-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="32d1b-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="32d1b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="32d1b-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="32d1b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="32d1b-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="32d1b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="32d1b-107">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชัน เพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="32d1b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="32d1b-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution.md)</span><span class="sxs-lookup"><span data-stu-id="32d1b-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="32d1b-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation V3 รุ่นการปรับปรุง 30</span><span class="sxs-lookup"><span data-stu-id="32d1b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="32d1b-110">เวอร์ชันนี้มีหมายเลขรุ่น V3.10.51.61 และจะพร้อมให้ปรับปรุงด้วยตนเองโดยทั่วไปในเดือนเมษายน 2021</span><span class="sxs-lookup"><span data-stu-id="32d1b-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="32d1b-111">รุ่นการปรับปรุง 30</span><span class="sxs-lookup"><span data-stu-id="32d1b-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="32d1b-112">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="32d1b-112">Bug fixes</span></span>

<span data-ttu-id="32d1b-113">**เวลาและค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="32d1b-113">**Time and Expense**</span></span>

<span data-ttu-id="32d1b-114">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="32d1b-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="32d1b-115">เกิดข้อผิดพลาดเมื่อคุณสร้างและบันทึกรายการเวลาในเพจ **สร้างด่วน** ถ้ามีการเอาฟิลด์ **บทบาท** ออก</span><span class="sxs-lookup"><span data-stu-id="32d1b-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="32d1b-116">ตัวกรองรายการเวลาใช้ตัวดำเนินการตัวกรองที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="32d1b-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="32d1b-117">ใบบันทึกเวลาที่คัดลอกไม่แสดงโดยอัตโนมัติเมื่อคุณเลือก **คัดลอกสัปดาห์** ในตัวควบคุมรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="32d1b-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="32d1b-118">**การจัดการทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="32d1b-118">**Resource Management**</span></span>

<span data-ttu-id="32d1b-119">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="32d1b-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="32d1b-120">เมื่อคุณขยายการจอง สถานะการจองที่กำหนดให้กับการจองแบบตายตัวไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="32d1b-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="32d1b-121">การขยายการจองเป็นไปตามสถานะการจองที่กำหนดเป็น **ยืนยันแล้ว** ในเมตาดาต้าของการตั้งค่าการจอง</span><span class="sxs-lookup"><span data-stu-id="32d1b-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="32d1b-122">เมื่อไม่ได้ระบุสถานะการจองที่ถูกต้อง ข้อความแสดงข้อผิดพลาดแปลไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="32d1b-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="32d1b-123">**การจัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="32d1b-123">**Project Management**</span></span>

<span data-ttu-id="32d1b-124">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="32d1b-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="32d1b-125">ไม่สามารถสร้างโครงการในสกุลเงินเดียวและรวมงานที่เกี่ยวข้องในสกุลเงินอื่น</span><span class="sxs-lookup"><span data-stu-id="32d1b-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="32d1b-126">**การขาย**</span><span class="sxs-lookup"><span data-stu-id="32d1b-126">**Sales**</span></span>

<span data-ttu-id="32d1b-127">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="32d1b-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="32d1b-128">เมื่อคัดลอกรายการราคา จะไม่มีการปรับปรุงราคา</span><span class="sxs-lookup"><span data-stu-id="32d1b-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="32d1b-129">การปิดใบเสนอราคาเป็นชนะล้มเหลวเมื่อรายละเอียดต้นทุนมีค่าสำหรับต้นทาง</span><span class="sxs-lookup"><span data-stu-id="32d1b-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="32d1b-130">ในเอนทิตี **งานโครงการ** มีการเปลี่ยนชื่อ **ต้นทุนโดยประมาณ** เป็น **ต้นทุนตามแผน (ฐาน)**</span><span class="sxs-lookup"><span data-stu-id="32d1b-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="32d1b-131">ข้อยกเว้นการอ้างอิงที่เป็น null มีการสร้างขึ้นเมื่อมีการสร้างหรือลบใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="32d1b-131">A null reference exception is generated when invoices are created or deleted.</span></span>
