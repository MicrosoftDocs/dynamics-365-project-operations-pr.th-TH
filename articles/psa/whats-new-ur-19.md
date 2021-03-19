---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 19 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation รุ่นการปรับปรุง 19 V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: b9baeca9e79e233c25a6310e426d755b9162bbad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280736"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="86ba6-103">Project Service Automation รุ่นการปรับปรุง 19 V3</span><span class="sxs-lookup"><span data-stu-id="86ba6-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="86ba6-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="86ba6-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="86ba6-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="86ba6-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="86ba6-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="86ba6-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="86ba6-107">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชัน เพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="86ba6-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="86ba6-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="86ba6-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="86ba6-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่เป็นของใหม่หรือที่เปลี่ยนแปลงสำหรับ PSA V3, รุ่นการปรับปรุง 19</span><span class="sxs-lookup"><span data-stu-id="86ba6-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="86ba6-110">เวอร์ชันนี้มีหมายเลขรุ่น V3.10.30.41 และจะพร้อมให้ปรับปรุงด้วยตนเองโดยทั่วไปในเดือนพฤษภาคม 2020</span><span class="sxs-lookup"><span data-stu-id="86ba6-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="86ba6-111">รุ่นการปรับปรุง 19</span><span class="sxs-lookup"><span data-stu-id="86ba6-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="86ba6-112">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="86ba6-112">Bug fixes</span></span>

<span data-ttu-id="86ba6-113">**เวลาและค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="86ba6-113">**Time and Expense**</span></span>

<span data-ttu-id="86ba6-114">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="86ba6-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="86ba6-115">ข้อผิดพลาดที่ได้จากการนำเข้ารายการเวลาจะไม่ปรากฏขึ้นอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="86ba6-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="86ba6-116">กริกรายการเวลาไม่สนับสนุนลักษณะการทำงานของฟิลด์ **วันที่เท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="86ba6-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="86ba6-117">ทรัพยากรของโครงการไม่สามารถสร้างค่าใช้จ่ายกับโครงการ</span><span class="sxs-lookup"><span data-stu-id="86ba6-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="86ba6-118">**การจัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="86ba6-118">**Project Management**</span></span>

<span data-ttu-id="86ba6-119">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="86ba6-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="86ba6-120">งานเพจย่อยทำให้การประมาณการความพยายามไม่ถูกต้องในระหว่างการคำนวณการทำให้เสร็จสมบูรณ์ (EAC)</span><span class="sxs-lookup"><span data-stu-id="86ba6-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="86ba6-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="86ba6-121">**Sales**</span></span>

<span data-ttu-id="86ba6-122">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="86ba6-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="86ba6-123">การดำเนินการ **คำนวณใหม่** ไม่ทำงานกับรายละเอียดบรรทัดสัญญาของค่าใช้จ่ายหรือรายละเอียดบรรทัดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="86ba6-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="86ba6-124">**ปรับปรุงราคา** หายไปสำหรับการประมาณการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="86ba6-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="86ba6-125">ลูกค้าไม่สามารถเลือกเหตุผลสถานะสัญญาที่กำหนดเองจากหน้า **สัญญาโครงการ** ได้</span><span class="sxs-lookup"><span data-stu-id="86ba6-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="86ba6-126">ลูกค้าประสบกับประสิทธิภาพที่ลดลงเมื่อสร้างรายการราคาที่กำหนดเองจากใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="86ba6-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="86ba6-127">ลูกค้าประสบกับความไม่สอดคล้องกับ **หน่วย** เริ่มต้นบนหน้า **รายละเอียดบรรทัดใบเสนอราคา** และ **รายละเอียดบรรทัดสัญญา**</span><span class="sxs-lookup"><span data-stu-id="86ba6-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="86ba6-128">การเพิ่มรายการประเภทการทำธุรกรรมที่ไม่สามารถคิดค่าธรรมเนียมได้ลงในบรรทัดสัญญาที่คิดค่าธรรมเนียมได้ จะไม่เกี่ยวข้องกับประเภทการเรียกเก็บเงิน **Non-chargeable** ของประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="86ba6-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="86ba6-129">ลูกค้าไม่สามารถใช้บทบาทและประเภทที่เพิ่มใหม่ในสัญญาที่สร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="86ba6-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="86ba6-130">ลูกค้าประสบกับประสิทธิภาพที่ลดลง ไม่จำเป็นต้องเรียกข้อมูลใน PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="86ba6-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="86ba6-131">การตั้งค่าบทบาทเป็นไม่สามารถคิดค่าธรรมเนียมได้ในรายการ **ประเภททรัพยากร** ควรจะเพิ่มไปยังแท็บ **บทบาทที่สามารถคิดเงินได้** เป็น **Non-chargeable** ในบรรทัดสัญญาสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="86ba6-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="86ba6-132">ลูกค้าอาจประสบปัญหาประสิทธิภาพลดลงเมื่อสร้างโครงการเพราะ **GetBookableResourceIdFromUser** เรียกข้อมูลคอลัมน์ทั้งหมดของแหล่งข้อมูลที่จองได้แทนที่จะเป็นเพียงรหัสหลัก</span><span class="sxs-lookup"><span data-stu-id="86ba6-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="86ba6-133">เอนทิตี **TransactionType** ขาดปลั๊กอินการอัปเดตการตรวจสอบล่วงหน้าเพื่อป้องกันผู้ใช้จากการเข้าสู่ **หน่วย** และ **กลุ่มของหน่วย** ที่ไม่ถูกต้องสำหรับประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="86ba6-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="86ba6-134">ขั้นตอน **ลบ** ไม่ทำงานสำหรับการนำเข้ารายการเวลา</span><span class="sxs-lookup"><span data-stu-id="86ba6-134">The **Remove** step does not work for time entry import.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]