---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 20 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation รุ่นการปรับปรุง 20 V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 124dad5438f9489d1ddbc952cecaee977b6b7f01
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949117"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="3b317-103">Project Service Automation รุ่นการปรับปรุง 20 V3</span><span class="sxs-lookup"><span data-stu-id="3b317-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3b317-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3b317-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3b317-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3b317-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3b317-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="3b317-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3b317-107">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชัน เพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="3b317-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="3b317-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="3b317-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3b317-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation V3 รุ่นการปรับปรุง 20</span><span class="sxs-lookup"><span data-stu-id="3b317-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="3b317-110">รุ่นนี้มีหมายเลขรุ่น V 3.10.31.37 และจะพร้อมให้ปรับปรุงด้วยตนเองโดยทั่วไปในเดือนมิถุนายน 2020</span><span class="sxs-lookup"><span data-stu-id="3b317-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="3b317-111">รุ่นการปรับปรุง 20</span><span class="sxs-lookup"><span data-stu-id="3b317-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3b317-112">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="3b317-112">Bug fixes</span></span>

<span data-ttu-id="3b317-113">**การจัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="3b317-113">**Project Management**</span></span>

<span data-ttu-id="3b317-114">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="3b317-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="3b317-115">การนำเข้าสมาชิกทีมโครงการด้วยวิธีการจัดสรรที่ต้องใช้ชั่วโมง ส่งผลให้เกิดข้อผิดพลาดที่ไม่ชัดเจนเมื่อเวลาที่ระบุเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="3b317-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="3b317-116">ผู้ใช้จะได้รับข้อผิดพลาดที่ไม่ถูกต้องเมื่อป้อนจำนวนอักขระสูงสุดในฟิลด์ **คำอธิบาย** สำหรับงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="3b317-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="3b317-117">เพจ **ดาวน์โหลด Add-in ของ Microsoft Dynamics 365 Project Service Automation** เปลี่ยนเส้นทางไปยังเพจดาวน์โหลดภาษาอังกฤษเมื่อตั้งค่าภาษาของผู้ใช้เป็นภาษาญี่ปุ่น</span><span class="sxs-lookup"><span data-stu-id="3b317-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="3b317-118">เมื่อเกิดข้อผิดพลาดเซิร์ฟเวอร์ ป้ายชื่อการทำข้อมูลให้ตรงกันบนแท็บ **จัดกำหนดการ** ของฟอร์ม **โครงการ** บางครั้งจะยังคงอยู่</span><span class="sxs-lookup"><span data-stu-id="3b317-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="3b317-119">การปรับปรุงงานซ้ำซ้อนจะถูกส่งไปยังเซิร์ฟเวอร์เมื่อมีการแก้ไขงาน</span><span class="sxs-lookup"><span data-stu-id="3b317-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="3b317-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="3b317-120">**Sales**</span></span>

<span data-ttu-id="3b317-121">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="3b317-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="3b317-122">บนแบบฟอร์ม **สัญญา** ดับเบิลคลิก **สร้างใบแจ้งหนี้** เพื่อสร้างใบแจ้งหนี้สองใบสำหรับเรกคอร์ดจริงหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="3b317-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="3b317-123">ใน Internet Explorer 11 ผู้ใช้ไม่สามารถสร้างรายการค่าใช้จ่ายได้</span><span class="sxs-lookup"><span data-stu-id="3b317-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="3b317-124">การย้อนกลับของต้นทุนและการย้อนกลับของการขายตามจริงที่ยังไม่ได้เรียกเก็บเงินจะไม่ถูกลิงก์</span><span class="sxs-lookup"><span data-stu-id="3b317-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="3b317-125">ปุ่ม **รีเฟรชข้อมูลจริง** บนแบบฟอร์ม **โครงการ** จะไม่รีเฟรช **ชั่วโมงทำงานจริง**</span><span class="sxs-lookup"><span data-stu-id="3b317-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="3b317-126">ปลั๊กอิน **PreValidateProjectTeamMemberCreate** สามารถสร้างทรัพยากรที่จองได้ทั่วไปที่ซ้ำกันเมื่อแอตทริบิวต์ **msdyn_isgenericresourceprojectscoped** ถูกตั้งค่าเป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="3b317-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="3b317-127">**คำนวณใหม่** ล้างค่าใช้จ่ายที่มีต้นทุนที่คิดค่าธรรมเนียมได้ของรายละเอียดบรรทัดใบเสนอราคาตามผลิตภัณฑ์ และรายละเอียดของบรรทัดสัญญา</span><span class="sxs-lookup"><span data-stu-id="3b317-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="3b317-128">ในบางสถานการณ์ ปลั๊กอิน **PostEstimateLineUpdate** แสดงข้อผิดพลาดข้อยกเว้นการอ้างอิงเป็นโมฆะ</span><span class="sxs-lookup"><span data-stu-id="3b317-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="3b317-129">ระยะเวลาของระยะเวลาใน **แผนภูมิการวิเคราะห์ความสามารถในการทำกำไร** ไม่ตรงกับระยะเวลาของต้นทุนในรายละเอียดของบรรทัดใบเสนอราคาคงที่ของใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="3b317-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="3b317-130">ค่าหน่วยและกลุ่มหน่วยเริ่มต้นไม่ถูกต้องสำหรับประเภทค่าใช้จ่ายใน **รายละเอียดบรรทัดสัญญา** และฟอร์ม **รายละเอียดบรรทัดใบเสนอราคา**</span><span class="sxs-lookup"><span data-stu-id="3b317-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="3b317-131">**ราคาต้นทุนต่อหน่วยองค์กร** แสดงรายการอนุญาตให้ทับซ้อนในวันที่มีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="3b317-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="3b317-132">ผู้ใช้ไม่ได้รับอนุญาตให้เปลี่ยน **หน่วยงานขององค์กร** เมื่อประเภทคำสั่งไม่ได้ทำงานตามเพราะจะนำไปสู่ข้อผิดพลาดข้อยกเว้นอ้างอิงโมฆะ</span><span class="sxs-lookup"><span data-stu-id="3b317-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="3b317-133">เมื่อพยายามที่จะนำทางจากแบบฟอร์ม **รายละเอียดบรรทัดใบเสนอราคา** ให้กลับไปที่แท็บ **ใบเสนอราคา** ฟอร์มจะรีเฟรชและแสดงแท็บ **สรุป**</span><span class="sxs-lookup"><span data-stu-id="3b317-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]