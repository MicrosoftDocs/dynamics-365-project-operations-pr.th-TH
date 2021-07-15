---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 33 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation รุ่นการปรับปรุง 33 V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334611"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="cc7d5-103">มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 33 V3</span><span class="sxs-lookup"><span data-stu-id="cc7d5-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cc7d5-104">เรายินดีที่จะประกาศการอัปเดตล่าสุดสำหรับแอป Microsoft Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cc7d5-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="cc7d5-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cc7d5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cc7d5-106">เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="cc7d5-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cc7d5-107">หากต้องการอัปเดตเป็นรุ่นนี้ ให้ไปที่หน้าศูนย์การจัดการสำหรับโซลูชันออนไลน์ของ Dynamics 365 และติดตั้งการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="cc7d5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="cc7d5-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="cc7d5-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cc7d5-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation V3 รุ่นการปรับปรุง 33</span><span class="sxs-lookup"><span data-stu-id="cc7d5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="cc7d5-110">รุ่นนี้มีหมายเลขการสร้างเป็น V3.10.54.98 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตตนเองในเดือนกรกฎาคม 2021</span><span class="sxs-lookup"><span data-stu-id="cc7d5-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="cc7d5-111">รุ่นการปรับปรุง 33</span><span class="sxs-lookup"><span data-stu-id="cc7d5-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cc7d5-112">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="cc7d5-112">Bug fixes</span></span>

<span data-ttu-id="cc7d5-113">**เวลาและค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="cc7d5-113">**Time and Expense**</span></span>

<span data-ttu-id="cc7d5-114">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="cc7d5-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc7d5-115">สองฟิลด์ที่ถูกล็อค **msdyn_description** และ **msdyn_externaldescription** สามารถแก้ไขได้หลังจากส่ง</span><span class="sxs-lookup"><span data-stu-id="cc7d5-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="cc7d5-116">ข้อความแสดงข้อผิดพลาดเกิดขึ้นหากมีการสร้างค่าใช้จ่ายที่ไม่เกี่ยวข้องกับโครงการ</span><span class="sxs-lookup"><span data-stu-id="cc7d5-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="cc7d5-117">เมื่อมีการสร้างรายการเวลา บทบาททรัพยากรจะมีค่าเริ่มต้นเป็นบทบาทที่ไม่ได้ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cc7d5-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="cc7d5-118">บรรทัดสมุดรายวันที่เกี่ยวข้องกับค่าใช้จ่ายที่ถูกเรียกคืนและถูกลบจะไม่ถูกลบ</span><span class="sxs-lookup"><span data-stu-id="cc7d5-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="cc7d5-119">บน **ฟอร์มสร้างด่วนรายการเวลา** ปรับปรุงมุมมอง **รายการงานโครงการ** เพื่อเปลี่ยนวันที่ที่แสดงโดยค่าเริ่มต้นเป็นวันที่เริ่มต้นของงาน</span><span class="sxs-lookup"><span data-stu-id="cc7d5-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="cc7d5-120">เมื่อคุณสร้างรายการเวลาจากแท็บ **ที่เกี่ยวข้อง** ของทรัพยากรที่สามารถจองได้ รายการเวลาถูกสร้างขึ้นอย่างไม่ถูกต้องสำหรับผู้ใช้ที่ลงชื่อเข้าใช้แทนที่จะเป็นทรัพยากรหลักที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="cc7d5-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="cc7d5-121">ฟิลด์ใหม่จะถูกเพิ่มไปยังกล่องโต้ตอบ **MDD การอนุมัติจำนวนมาก**</span><span class="sxs-lookup"><span data-stu-id="cc7d5-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="cc7d5-122">**การวางแผนโครงการ**</span><span class="sxs-lookup"><span data-stu-id="cc7d5-122">**Project planning**</span></span>

<span data-ttu-id="cc7d5-123">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="cc7d5-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="cc7d5-124">ประสิทธิภาพการสร้างโครงการช้าเมื่อใช้แม่แบบชั่วโมงการทำงานของโครงการกับปฏิทินที่ซับซ้อน</span><span class="sxs-lookup"><span data-stu-id="cc7d5-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="cc7d5-125">เมื่อวันที่เริ่มต้นมากกว่าวันที่สิ้นสุด ข้อผิดพลาดจะปรากฏขึ้นบนแม่แบบโครงการคัดลอกเนื่องจากความแตกต่างในองค์ประกอบเวลาของแต่ละฟิลด์</span><span class="sxs-lookup"><span data-stu-id="cc7d5-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="cc7d5-126">**การจัดการทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="cc7d5-126">**Resource management**</span></span>

<span data-ttu-id="cc7d5-127">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="cc7d5-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="cc7d5-128">พารามิเตอร์ที่ไม่ถูกต้องถูกใช้ในแบบสอบถามการใช้ทรัพยากร และ XML นำไปสู่ผลลัพธ์การกรองที่ไม่ถูกต้องบนตาราง **การใช้ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="cc7d5-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="cc7d5-129">การยืนยัน **ขยายการจอง** แสดงวันที่สิ้นสุดการจองไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="cc7d5-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="cc7d5-130">**การขาย**</span><span class="sxs-lookup"><span data-stu-id="cc7d5-130">**Sales**</span></span>

<span data-ttu-id="cc7d5-131">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="cc7d5-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="cc7d5-132">เกิดข้อความข้อผิดพลาดหากมีการสร้างราคาประเภทโดยมีค่าที่ขาดหายไป</span><span class="sxs-lookup"><span data-stu-id="cc7d5-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="cc7d5-133">มีข้อความข้อผิดพลาดเกิดขึ้นหากมีการสร้างเหตุการณ์สำคัญของรายละเอียดการให้บริการตามสัญญาโดยไม่มีรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="cc7d5-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
