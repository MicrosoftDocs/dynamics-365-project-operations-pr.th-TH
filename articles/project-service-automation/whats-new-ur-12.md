---
title: มีอะไรใหม่ในรุ่นการปรับปรุง Project Service Automation 12, V3
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับสิ่งใหม่ในรุ่นการปรับปรุง Project Service Automation 12, V3
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756426"
---
# <a name="project-service-automation-v3-update-release-12"></a><span data-ttu-id="72e30-103">Project Service Automation V3 รุ่นการปรับปรุง 12</span><span class="sxs-lookup"><span data-stu-id="72e30-103">Project Service Automation V3, Update Release 12</span></span>
<span data-ttu-id="72e30-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Dynamics 365 Project Service Automation (PSA)</span><span class="sxs-lookup"><span data-stu-id="72e30-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="72e30-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="72e30-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="72e30-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="72e30-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="72e30-107">หากต้องการอัปเดตเป็นรุ่นนี้ ให้ไปที่ศูนย์ผู้ดูแลระบบสำหรับ Dynamics 365 ออนไลน์ และไปที่หน้าโซลูชันเพื่อติดตั้งการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="72e30-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="72e30-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="72e30-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="72e30-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation V3 รุ่นการปรับปรุง 12</span><span class="sxs-lookup"><span data-stu-id="72e30-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="72e30-110">รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.2.34 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตด้วยตนเองในเดือนตุลาคม 2019</span><span class="sxs-lookup"><span data-stu-id="72e30-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="72e30-111">รุ่นการปรับปรุง 12</span><span class="sxs-lookup"><span data-stu-id="72e30-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="72e30-112">การแก้ไขข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="72e30-112">Bug fixes</span></span>

- <span data-ttu-id="72e30-113">เวลาและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="72e30-113">Time and Expense</span></span>

    - <span data-ttu-id="72e30-114">แก้ไข: การส่งข้อความข้อผิดพลาดในรายกาเวลาได้รับการปรับปรุงด้วยบริบทที่เกี่ยวข้องมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="72e30-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="72e30-115">แก้ไข: กริดรายการเวลาและกำหนดการแสดงแถบเลื่อนแนวตั้งอย่างถูกต้องเมื่อจำเป็น</span><span class="sxs-lookup"><span data-stu-id="72e30-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="72e30-116">แก้ไข: สามารถอนุมัติรายการเวลาและค่าใช้จ่ายที่ส่งไปแล้ว</span><span class="sxs-lookup"><span data-stu-id="72e30-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="72e30-117">แก้ไข: ยกเลิกข้อความโต้ตอบการยืนยันการอนุมัติได้รับการแก้ไขเพื่อให้สะท้อนถึงสถานะของการอนุมัติเมื่อเปลี่ยนจาก **ได้รับการอนุมัติ** เป็น **ส่งแล้ว**</span><span class="sxs-lookup"><span data-stu-id="72e30-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="72e30-118">แก้ไข: ฟิลด์ **ราคา** **หน่วย** และ **ปริมาณ** ตอนนี้จะถูกล็อคในเรกคอร์ดค่าใช้จ่ายหลังจากได้รับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="72e30-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="72e30-119">การจัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="72e30-119">Project Management</span></span>

    - <span data-ttu-id="72e30-120">แก้ไข: การดำเนินการ **ใหม่** บนฟอร์มหลัก **สมาชิกในทีม** ถูกลบออกแล้ว</span><span class="sxs-lookup"><span data-stu-id="72e30-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="72e30-121">แก้ไข: การมอบหมายทรัพยากรได้รับการปรับปรุงเป็นบัญชีสำหรับข้อผิดพลาดในการปัดเศษที่ไม่ถูกต้อง ซึ่งนำไปสู่การเปลี่ยนแปลงในวันที่สิ้นสุดของงาน</span><span class="sxs-lookup"><span data-stu-id="72e30-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="72e30-122">แก้ไข: ในกริดงาน ข้อผิดพลาดฝั่งเซิร์ฟเวอร์ที่เกี่ยวข้องจะปรากฏขึ้นกับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="72e30-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="72e30-123">แก้ไข: ตอนนี้ชื่อสมาชิกในทีมแสดงผลในตัวเลือกคนทำงานแทนชื่อตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="72e30-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="72e30-124">การจัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="72e30-124">Resource Management</span></span>

    - <span data-ttu-id="72e30-125">แก้ไข: รายละเอียดความต้องการทรัพยากรสำหรับโครงการที่สร้างจากแม่แบบตอนนี้ใช้ปฏิทินโครงการ</span><span class="sxs-lookup"><span data-stu-id="72e30-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="72e30-126">แก้ไข: ทักษะและความสามารถตอนนี้เริ่มต้นจากข้อมูลหลักของบทบาทไปจนถึงความต้องการทรัพยากรที่สร้างขึ้นสำหรับบทบาทนั้น</span><span class="sxs-lookup"><span data-stu-id="72e30-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="72e30-127">Sales</span><span class="sxs-lookup"><span data-stu-id="72e30-127">Sales</span></span>

    - <span data-ttu-id="72e30-128">แก้ไข: ทำซ้ำรหัสออบเจ็กต์ที่พบในแบบฟอร์ม **หลักสัญญา**</span><span class="sxs-lookup"><span data-stu-id="72e30-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="72e30-129">แก้ไข: ตรรกะได้รับการปรับปรุงเพื่อให้แท็บ **การวิเคราะห์ใบเสนอราคา** มองเห็นได้ เพื่อให้แสดงการตั้งค่าข้อมูลเมตาของแท็บ</span><span class="sxs-lookup"><span data-stu-id="72e30-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="72e30-130">แก้ไข: วันที่บัญชีในเรกคอร์ดจริงตอนนี้มาจากวันที่ของเวลา/วันที่ของรายการค่าใช้จ่ายและไม่ใช่วันที่ได้รับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="72e30-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
