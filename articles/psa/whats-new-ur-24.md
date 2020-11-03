---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 24 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation รุ่นการปรับปรุง 24 V3
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6c8348e65307f63a251f97bf1ea17578e7026da8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085884"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="d6f4b-103">Project Service Automation รุ่นการปรับปรุง 24 V3</span><span class="sxs-lookup"><span data-stu-id="d6f4b-103">Project Service Automation Update Release 24, V3</span></span>

<span data-ttu-id="d6f4b-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="d6f4b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d6f4b-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d6f4b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d6f4b-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="d6f4b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d6f4b-107">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชัน เพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="d6f4b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d6f4b-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="d6f4b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d6f4b-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation V3 รุ่นการปรับปรุง 24</span><span class="sxs-lookup"><span data-stu-id="d6f4b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="d6f4b-110">รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.42.43 และโดยทั่วไปจะพร้อมใช้งานผ่านการปรับปรุงด้วยตนเองในเดือนตุลาคม 2020</span><span class="sxs-lookup"><span data-stu-id="d6f4b-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="d6f4b-111">รุ่นการปรับปรุง 24</span><span class="sxs-lookup"><span data-stu-id="d6f4b-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d6f4b-112">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="d6f4b-112">Bug fixes</span></span>

<span data-ttu-id="d6f4b-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d6f4b-113">**Sales**</span></span>

<span data-ttu-id="d6f4b-114">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="d6f4b-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="d6f4b-115">ปัญหาขณะตั้งค่ารายการราคาเริ่มต้นของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="d6f4b-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="d6f4b-116">ประสิทธิภาพของการชนะใบเสนอราคาช้าลงเนื่องจากรายการราคาและสำเนาบันทึกราคาตามบทบาทที่ฝังไว้</span><span class="sxs-lookup"><span data-stu-id="d6f4b-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="d6f4b-117">**สัญญาโครงการ/ฮับการขาย** > **รายการสินค้าในรายการ/ปริมาณรายการในใบสั่ง** จะถูกปัดเศษเป็นจำนวนเต็มที่ใกล้เคียงที่สุดโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d6f4b-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="d6f4b-118">ยกระดับเป็นสิทธิ์ของระบบเมื่ออ่านรายการราคา</span><span class="sxs-lookup"><span data-stu-id="d6f4b-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="d6f4b-119">คัดลอกฟิลด์ที่อยู่ลูกค้า **address1_freighttermscode** และ **address1_shippingmethodcode** ไปยังใบเสนอราคา/ใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="d6f4b-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="d6f4b-120">**เวลาและค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="d6f4b-120">**Time and Expense**</span></span>

<span data-ttu-id="d6f4b-121">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="d6f4b-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="d6f4b-122">**ตารางรายการเวลา** ไม่รองรับลักษณะการทำงานของเวลา **วันที่เท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="d6f4b-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="d6f4b-123">**รายการเวลา** ไม่รีเฟรชโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d6f4b-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="d6f4b-124">จำเป็นต้องมีการรีเฟรชด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="d6f4b-124">A manual refresh is required.</span></span>
- <span data-ttu-id="d6f4b-125">ไม่สามารถนำเข้ารายการเวลาจากการมอบหมายเมื่อมีช่วงพัก (0 ชั่วโมง) ในการมอบหมายของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="d6f4b-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="d6f4b-126">เมื่อสร้างรายการเวลา ให้ตั้งค่าเริ่มต้นเหมือนกับ **msdyn_date**</span><span class="sxs-lookup"><span data-stu-id="d6f4b-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="d6f4b-127">เปิดใช้งานการแก้ไขจำนวนมากอีกครั้งสำหรับรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="d6f4b-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="d6f4b-128">**การจัดการทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="d6f4b-128">**Resource Management**</span></span>

<span data-ttu-id="d6f4b-129">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="d6f4b-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="d6f4b-130">การพยายามปรับปรุงสถานะของการจองระหว่างวันโดยไม่มีความต้องการจะทำให้เกิดข้อยกเว้น null-ref</span><span class="sxs-lookup"><span data-stu-id="d6f4b-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="d6f4b-131">เกิดข้อผิดพลาดในการโหลด **มุมมองการกระทบยอด**</span><span class="sxs-lookup"><span data-stu-id="d6f4b-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="d6f4b-132">**การจัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="d6f4b-132">**Project Management**</span></span>

<span data-ttu-id="d6f4b-133">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="d6f4b-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="d6f4b-134">ใน **กำหนดการโครงการ** เมื่อเปลี่ยนจาก **ด้วยตนเอง** เป็น **อัตโนมัติ** การบันทึกอัตโนมัติจะไม่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="d6f4b-134">In the **Project Schedule** , when changing from **Manual** to **Auto** , auto save is not completing.</span></span>
- <span data-ttu-id="d6f4b-135">ต้นทุนค่าใช้จ่ายไม่ควรคำนวณตามผลต่างของ **ตารางการติดตามโครงการ**</span><span class="sxs-lookup"><span data-stu-id="d6f4b-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="d6f4b-136">ลักษณะการทำงานที่ไม่สอดคล้องกันสำหรับคอลัมน์ **แท็กประมาณการ** ระหว่างการโหลดเทียบกับการเปลี่ยนชนิด **ระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="d6f4b-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="d6f4b-137">ต้นทุนจริงของโครงการอาจไม่สะท้อนถึงยอดรวมจาก **ตามจริง**</span><span class="sxs-lookup"><span data-stu-id="d6f4b-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="d6f4b-138">**วันที่เสร็จสิ้นโดยประมาณ** บนแท็บ **สรุป** ไม่ตรงกับ **กำหนดการ WBS**</span><span class="sxs-lookup"><span data-stu-id="d6f4b-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="d6f4b-139">**ปรับปรุงชั่วโมงจริง** เมื่อล้าสมัยทำงานไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="d6f4b-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="d6f4b-140">ผู้จัดการโครงการที่อยู่ภายนอกรูท **BU** ไม่สามารถสร้างโครงการได้</span><span class="sxs-lookup"><span data-stu-id="d6f4b-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="d6f4b-141">การเปลี่ยนแปลงงานหรือประเภทบน **ประมาณการค่าใช้จ่าย** จะไม่คงอยู่</span><span class="sxs-lookup"><span data-stu-id="d6f4b-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="d6f4b-142">**สำเนาของสัญญา** คัดลอกกำหนดการใบแจ้งหนี้และสถานะการเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="d6f4b-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="d6f4b-143">ปุ่ม **รีเฟรชตามจริง** คำนวณงานสรุปไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="d6f4b-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="d6f4b-144">Microsoft Project Add-in: แก้ไขข้อผิดพลาดในการอ้างอิงเป็น null หากสมาชิกทีมมีหน่วยจัดหาทรัพยากรที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="d6f4b-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

