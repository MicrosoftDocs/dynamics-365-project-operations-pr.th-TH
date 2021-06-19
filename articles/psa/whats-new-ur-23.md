---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 23 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation รุ่นการปรับปรุง 23 V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: adf893a0627ae59f2132bb46686110dafda01d3d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006489"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="a255d-103">Project Service Automation รุ่นการปรับปรุง 23 V3</span><span class="sxs-lookup"><span data-stu-id="a255d-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a255d-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a255d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a255d-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a255d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a255d-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="a255d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a255d-107">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชัน เพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="a255d-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="a255d-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="a255d-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a255d-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation V3 รุ่นการปรับปรุง 23</span><span class="sxs-lookup"><span data-stu-id="a255d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="a255d-110">รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.34.30 และโดยทั่วไปจะพร้อมใช้งานผ่านการปรับปรุงด้วยตนเองในเดือนสิงหาคม 2020</span><span class="sxs-lookup"><span data-stu-id="a255d-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="a255d-111">รุ่นการปรับปรุง 23</span><span class="sxs-lookup"><span data-stu-id="a255d-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a255d-112">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="a255d-112">Bug fixes</span></span>

<span data-ttu-id="a255d-113">**เวลาและค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="a255d-113">**Time and Expense**</span></span>

<span data-ttu-id="a255d-114">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="a255d-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="a255d-115">จัดการปัญหาใน **การลบสมาชิกทีมของโครงการ** เพื่อให้ข้อยกเว้นที่เป็นประโยชน์</span><span class="sxs-lookup"><span data-stu-id="a255d-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="a255d-116">การนำเข้าการมอบหมายส่งผลให้หน้าจอนำออกว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="a255d-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="a255d-117">**การจัดการทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="a255d-117">**Resource Management**</span></span>

<span data-ttu-id="a255d-118">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="a255d-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="a255d-119">**บัตรทรัพยากรในตารางการใช้ทรัพยากร** แสดงข้อมูลที่ไม่ถูกต้องเมื่อมาตราส่วนเวลามากกว่าห้าวัน</span><span class="sxs-lookup"><span data-stu-id="a255d-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="a255d-120">เมื่อลูกค้าสร้างทรัพยากรที่สามารถจองได้ ปลั๊กอินจะไม่สามารถเพิ่มทรัพยากรลงในกลุ่ม Microsoft Office 365 ได้เป็นระยะ</span><span class="sxs-lookup"><span data-stu-id="a255d-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="a255d-121">มุมมอง **การกระทบยอด** แสดงเส้นชั้นแบบกำหนดด้วยตนเองไม่ถูกต้องในมุมมอง **สัปดาห์** หรือ **เดือน**</span><span class="sxs-lookup"><span data-stu-id="a255d-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="a255d-122">**การจัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="a255d-122">**Project Management**</span></span>

<span data-ttu-id="a255d-123">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="a255d-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="a255d-124">จำนวนที่มากเกินไปของเอนทิตี **RetrieveMultiple สำหรับการตั้งค่าผู้ใช้** ทำให้ประสิทธิภาพการทำงานลดลงสำหรับการอนุมัติโครงการและการดำเนินการอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="a255d-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="a255d-125">การค้นหาทรัพยากรในตาราง **การวางแผนงาน** จำกัดให้แสดงเฉพาะสมาชิกทีมไม่เกินห้าคนจากทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="a255d-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="a255d-126">การค้นหาทรัพยากรในตาราง **การวางแผนงาน** ไม่กรองทรัพยากรที่ไม่ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a255d-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="a255d-127">โหมดกำหนดด้วยตนเองไม่ทำงานตามที่คาดไว้ในโครงสร้างการแบ่งงานของการวางแผนโครงการ</span><span class="sxs-lookup"><span data-stu-id="a255d-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="a255d-128">ตาราง **การวางแผนงาน** แสดง **ประเภทธุรกรรมที่ไม่ใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="a255d-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="a255d-129">ตาราง **การกำหนดทรัพยากร** ปัดเศษไม่ถูกต้องเมื่องานมีการมอบหมายหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="a255d-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="a255d-130">ค่าการปัดเศษจะแตกต่างกันระหว่างต้นทุนตามแผนและต้นทุนจริงสำหรับงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="a255d-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="a255d-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="a255d-131">**Sales**</span></span>

<span data-ttu-id="a255d-132">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="a255d-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="a255d-133">การดับเบิลคลิก **ดึงข้อมูลประเภทธุรกรรมทั้งหมด** จะสร้างหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="a255d-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]