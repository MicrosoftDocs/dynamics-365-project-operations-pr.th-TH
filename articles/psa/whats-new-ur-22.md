---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 22 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation รุ่นการปรับปรุง 22 V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 456ed68bc1d74c2c8e5d2420a3f5d1fb8e0465d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126641"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="87197-103">Project Service Automation รุ่นการปรับปรุง 22 V3</span><span class="sxs-lookup"><span data-stu-id="87197-103">Project Service Automation Update Release 22, V3</span></span>

<span data-ttu-id="87197-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="87197-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="87197-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="87197-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="87197-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="87197-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="87197-107">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชัน เพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="87197-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="87197-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="87197-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="87197-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation V3 รุ่นการปรับปรุง 22</span><span class="sxs-lookup"><span data-stu-id="87197-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="87197-110">รุ่นนี้มีหมายเลขรุ่น V 3.10.33.48 และจะพร้อมให้ปรับปรุงด้วยตนเองโดยทั่วไปในเดือนมิถุนายน 2020</span><span class="sxs-lookup"><span data-stu-id="87197-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="87197-111">รุ่นการปรับปรุง 22</span><span class="sxs-lookup"><span data-stu-id="87197-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="87197-112">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="87197-112">Bug fixes</span></span>



<span data-ttu-id="87197-113">**เวลาและค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="87197-113">**Time and Expense**</span></span>

<span data-ttu-id="87197-114">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="87197-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="87197-115">**รายการเวลา** จะไม่ถูกเพิ่มโดยอัตโนมัติในกำหนดการรายการเวลาหลังจากนำเข้า</span><span class="sxs-lookup"><span data-stu-id="87197-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="87197-116">เครื่องมือเลือกวันที่ **รายการเวลา** แบบกริดไม่รู้จักการตั้งค่าภูมิภาคของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="87197-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="87197-117">**การจัดการทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="87197-117">**Resource Management**</span></span>

<span data-ttu-id="87197-118">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="87197-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="87197-119">ในโหมดแบบกำหนดเอง การเปลี่ยนเป็นเส้นชั้น **การมอบหมายทรัพยากร** ไม่ถูกรับรู้เมื่อสร้าง **ความต้องการทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="87197-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="87197-120">**คำขอทรัพยากร** ไม่รองรับสถานะคำขอที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="87197-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="87197-121">**การจัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="87197-121">**Project Management**</span></span>

<span data-ttu-id="87197-122">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="87197-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="87197-123">การใช้ดับเบิลคลิกที่ EstimateGridControl จะไม่สามารถแยกวิเคราะห์ตัวเลขรูปแบบภาษาดัตช์ได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="87197-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="87197-124">ชั่วโมงที่ได้รับมอบหมายไม่อัปเดตอย่างถูกต้องเมื่อมีการเปลี่ยนแปลงการมอบหมาย โดยใช้ add-in เดสก์ท็อปของ Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="87197-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="87197-125">กริดการติดตามและประมาณการโครงการ แสดงรหัสสกุลเงินการขายที่ไม่ถูกต้องเมื่อสกุลเงินของสัญญาแตกต่างจากสกุลเงินของลูกค้า และองค์กรได้รับการกำหนดค่าให้แสดงรหัสสกุลเงินแทนสัญลักษณ์สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="87197-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="87197-126">วันที่เสร็จสิ้นของสมาชิกในทีมจะเพิ่มหนึ่งวันหากตารางชั่วโมงการทำงานเป็น 24 ชั่วโมงต่อวัน</span><span class="sxs-lookup"><span data-stu-id="87197-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="87197-127">ในกำหนดการโครงการ การเพิ่มประเภทธุรกรรมในงานจะไม่ทริกเกอร์การบันทึกอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="87197-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="87197-128">ข้อผิดพลาดต่อไปนี้จะแสดงขึ้นเมื่อเพิ่มสมาชิกในทีมในแม่แบบโครงการ: "ข้อกำหนดทรัพยากรไม่สามารถเชื่อมโยงกับแม่แบบโครงการ"</span><span class="sxs-lookup"><span data-stu-id="87197-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="87197-129">สคริปต์กฎของ Ribbon "msdyn.Approval.CanApproveOrReject" แสดงข้อผิดพลาดการหมดเวลา</span><span class="sxs-lookup"><span data-stu-id="87197-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="87197-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="87197-130">**Sales**</span></span>

<span data-ttu-id="87197-131">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="87197-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="87197-132">ข้อความแสดงข้อผิดพลาดในการตรวจสอบความถูกต้องไม่แสดง เมื่อมีการเลือกรายการราคาต้นทุนในการค้นหารายการราคาในแบบฟอร์ม/เอนทิตี 'รายการราคาโครงการใหม่'</span><span class="sxs-lookup"><span data-stu-id="87197-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="87197-133">การปิดใบเสนอราคาเป็นสถานะชนะจะไม่นำทางไปยังสัญญาที่สร้างขึ้น หาก BPF ที่แนบมากับใบเสนอราคาอยู่ในขั้นตอนสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="87197-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="87197-134">การกลับ **รายการราคาต้นทุน** เชื่อมโยงกับต้นทุนเดิมเมื่อมีการเรียกคืนรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="87197-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="87197-135">หลังจากเลือกปุ่ม **ยืนยัน** สถานะใบแจ้งหนี้จะไม่เปลี่ยนเป็น **ยืนยันแล้ว** เว้นแต่จะมีการรีเฟรชใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="87197-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
