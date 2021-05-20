---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 29 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation รุ่นการปรับปรุง 29 V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948684"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="96c87-103">มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 29 V3</span><span class="sxs-lookup"><span data-stu-id="96c87-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="96c87-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="96c87-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="96c87-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="96c87-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="96c87-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="96c87-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="96c87-107">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชัน เพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="96c87-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="96c87-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="96c87-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="96c87-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation V3 รุ่นการปรับปรุง 29</span><span class="sxs-lookup"><span data-stu-id="96c87-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="96c87-110">รุ่นนี้มีหมายเลขรุ่น V3.10.47.7 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตด้วยตนเองในเดือนกุมภาพันธ์ 2021</span><span class="sxs-lookup"><span data-stu-id="96c87-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="96c87-111">รุ่นการปรับปรุง 29</span><span class="sxs-lookup"><span data-stu-id="96c87-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="96c87-112">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="96c87-112">Bug fixes</span></span>

<span data-ttu-id="96c87-113">**เวลาและค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="96c87-113">**Time and Expense**</span></span>

<span data-ttu-id="96c87-114">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="96c87-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="96c87-115">ผู้ใช้ไม่สามารถดูชั่วโมงการทำงานที่บันทึกไว้ในวันที่ไม่ทำงานในตารางรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="96c87-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="96c87-116">รายการค่าใช้จ่ายที่อนุมัติแล้วสามารถแก้ไขได้ในตาราง</span><span class="sxs-lookup"><span data-stu-id="96c87-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="96c87-117">**การจัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="96c87-117">**Project Management**</span></span>

<span data-ttu-id="96c87-118">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="96c87-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="96c87-119">ไม่มีตรรกะในการตรวจสอบความถูกต้องเพื่อให้แน่ใจว่าชั่วโมงของกำลังคนในการกำหนดทรัพยากรไม่สามารถติดลบ</span><span class="sxs-lookup"><span data-stu-id="96c87-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="96c87-120">การดำเนินการที่กำหนดเอง **AssignResourcesForTask** ปรับปรุงฟิลด์ทั้งหมดแทนที่จะปรับปรุงฟิลด์ที่เปลี่ยนแปลงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="96c87-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="96c87-121">เมื่อคัดลอกโครงการในสภาพแวดล้อมที่มีปลั๊กอินหรือเวิร์กโฟลว์ที่ลงทะเบียนในเหตุการณ์ **CreateProject** แอตทริบิวต์ **msdyn_bulkgenerationstatus** จะไม่ถูกปรับปรุงหาก **CopyWBSToProject** ล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="96c87-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="96c87-122">เมื่อคุณขยายปฏิทินโครงการ วันทำงานจะไม่เรียงลำดับจากน้อยไปหามาก ทำให้การปรับปรุงงานโครงการบางอย่างล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="96c87-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="96c87-123">การเปลี่ยนผู้จัดการโครงการในโครงการที่มีอยู่จะทริกเกอร์ตรรกะการกำหนดค่าเริ่มต้นของหน่วยขององค์กร</span><span class="sxs-lookup"><span data-stu-id="96c87-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="96c87-124">**การขาย**</span><span class="sxs-lookup"><span data-stu-id="96c87-124">**Sales**</span></span>

<span data-ttu-id="96c87-125">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="96c87-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="96c87-126">แท็บ **การปฏิบัติงานตามสัญญา** บนเพจ **สัญญา** ล้มเหลวโดยไม่แจ้งระหว่างการเริ่มการทำงานเมื่อไม่มีรายละเอียดการให้บริการตามสัญญาอยู่</span><span class="sxs-lookup"><span data-stu-id="96c87-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>