---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 15 V3
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับสิ่งใหม่ในรุ่นการปรับปรุง Project Service Automation 15, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: fe1e2b2046faeee4e4c71484a976d70e8722e090
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949342"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="e96f9-103">Project Service Automation รุ่นการปรับปรุง 15 V3</span><span class="sxs-lookup"><span data-stu-id="e96f9-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e96f9-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Dynamics 365 Project Service Automation (PSA)</span><span class="sxs-lookup"><span data-stu-id="e96f9-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="e96f9-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e96f9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e96f9-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="e96f9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e96f9-107">หากต้องการอัปเดตเป็นรุ่นนี้ ให้ไปที่ศูนย์ผู้ดูแลระบบสำหรับ Dynamics 365 ออนไลน์ และไปที่หน้าโซลูชันเพื่อติดตั้งการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="e96f9-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="e96f9-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="e96f9-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e96f9-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่เป็นของใหม่หรือที่เปลี่ยนแปลงสำหรับ PSA V3, รุ่นการปรับปรุง 15</span><span class="sxs-lookup"><span data-stu-id="e96f9-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="e96f9-110">รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.5.28 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตด้วยตนเองในเดือนมกราคม 2020</span><span class="sxs-lookup"><span data-stu-id="e96f9-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="e96f9-111">รุ่นการปรับปรุง 15</span><span class="sxs-lookup"><span data-stu-id="e96f9-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="e96f9-112">การปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="e96f9-112">Enhancements</span></span>

- <span data-ttu-id="e96f9-113">การจัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="e96f9-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e96f9-114">การแก้ไขข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="e96f9-114">Bug fixes</span></span>

- <span data-ttu-id="e96f9-115">เวลาและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="e96f9-115">Time and Expense</span></span>

  - <span data-ttu-id="e96f9-116">แก้ไข: เพิ่มการจัดการข้อผิดพลาดการโหลดในมุมมองการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="e96f9-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="e96f9-117">แก้ไข: ฮับทรัพยากรโครงการ: เปลี่ยนชื่อ **จำนวน** เพื่อลดความกำกวม</span><span class="sxs-lookup"><span data-stu-id="e96f9-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="e96f9-118">แก้ไข: ปรับมุมมอง **คัดลอกคอลัมน์รายการเวลา** เพื่อรวมประเภท</span><span class="sxs-lookup"><span data-stu-id="e96f9-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="e96f9-119">แก้ไข: การแก้ไขระยะเวลาการป้อนข้อมูลเวลาในมุมมองกริดโดยใช้ตัวเลขทศนิยมส่งผลให้เกิดข้อผิดพลาดที่ไม่รู้จักสำหรับบางหมายเลข</span><span class="sxs-lookup"><span data-stu-id="e96f9-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="e96f9-120">การจัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="e96f9-120">Project Management</span></span>

  - <span data-ttu-id="e96f9-121">แก้ไข: เมนูแบบเลื่อนลงสำหรับ **ใช้ในมุมมองการติดตาม** ตอนนี้ขยายตามความกว้างของตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="e96f9-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="e96f9-122">แก้ไข: เมื่อจัดการโครงการในโซนเวลา +13 การคำนวณงานอาจแสดงผลลัพธ์ที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e96f9-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="e96f9-123">แก้ไข: **เวลาสิ้นสุดของสมาชิกทีม** ได้รับการแก้ไขเมื่อใช้ปฏิทิน 24 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="e96f9-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="e96f9-124">แก้ไข: เปิดใช้งาน **BPF** อีกครั้งในแบบฟอร์มหลัก **msdyn_project**</span><span class="sxs-lookup"><span data-stu-id="e96f9-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="e96f9-125">แก้ไข: การคำนวณการมอบหมายไม่ละเว้นระยะเวลาหนึ่งวันอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="e96f9-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="e96f9-126">แก้ไข: มีการเพิ่มแบนเนอร์แจ้งเตือนใหม่ลงในแบบฟอร์มโครงการเมื่อโซนเวลาแตกต่างกันระหว่างผู้ใช้กับโครงการ</span><span class="sxs-lookup"><span data-stu-id="e96f9-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="e96f9-127">Sales</span><span class="sxs-lookup"><span data-stu-id="e96f9-127">Sales</span></span>

  - <span data-ttu-id="e96f9-128">แก้ไข: การค้นหาหมวดหมู่การประเมิณค่าใช้จ่ายสามารถใช้กรองรายการที่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="e96f9-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="e96f9-129">แก้ไข: รหัสใน **PluginDomain.ExecuteInTryCatchBlock(..)** จะไม่ซ่อนที่มาของข้อยกเว้นอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="e96f9-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="e96f9-130">แก้ไข: ไม่มีข้อความแสดงข้อผิดพลาดอีกต่อไปใน **การค้นหาโครงการ** ในฟอร์ม **บรรทัดการเสนอราคา** เมื่อมีมากกว่า 1,000 โครงการ</span><span class="sxs-lookup"><span data-stu-id="e96f9-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="e96f9-131">แก้ไข: กริด **การประมาณการ** สำหรับการประมาณการแรงงานและการประมาณการค่าใช้จ่ายในขณะนี้แสดงสัญลักษณ์สกุลเงินที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e96f9-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="e96f9-132">แก้ไข: หลังจากองค์กรอัปเดต PSA จากการปรับปรุงรุ่น 14 เป็นการปรับปรุงรุ่น 15 แล้ว แท็บ **ตารางเวลา** จะไม่ปรากฏเป็นช่องว่างในฟอร์ม **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="e96f9-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]