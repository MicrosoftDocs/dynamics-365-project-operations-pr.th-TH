---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 26 V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643286"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="e527f-102">Project Service Automation รุ่นการปรับปรุง 26 V3</span><span class="sxs-lookup"><span data-stu-id="e527f-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="e527f-103">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="e527f-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e527f-104">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e527f-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e527f-105">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="e527f-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e527f-106">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชัน เพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="e527f-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="e527f-107">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="e527f-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e527f-108">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation รุ่นการปรับปรุง 26 V3</span><span class="sxs-lookup"><span data-stu-id="e527f-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="e527f-109">รุ่นนี้มีหมายเลขรุ่น V3.10.44.59 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตด้วยตนเองในเดือนธันวาคม 2020</span><span class="sxs-lookup"><span data-stu-id="e527f-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="e527f-110">รุ่นการปรับปรุง 26</span><span class="sxs-lookup"><span data-stu-id="e527f-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="e527f-111">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="e527f-111">Bug fixes</span></span>

<span data-ttu-id="e527f-112">**เวลาและค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="e527f-112">**Time and Expense**</span></span>

<span data-ttu-id="e527f-113">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="e527f-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="e527f-114">ผู้ใช้สามารถเปลี่ยนงานในรายการเวลาที่ได้รับการอนุมัติ/ส่ง</span><span class="sxs-lookup"><span data-stu-id="e527f-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="e527f-115">"ไม่ได้ตั้งค่าการอ้างอิงออบเจ็กต์ " เกิดข้อผิดพลาดเมื่อบันทึกรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="e527f-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="e527f-116">การนำเข้ารายการเวลาจากการกำหนดทรัพยากรสร้างรายการเวลาด้วยค่า วันที่เวลา ที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e527f-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="e527f-117">เมื่อติดตั้ง Project Service Automation และแอป Field Service แล้ว ปุ่ม **สร้าง** แสดงสองครั้งบนแถบคำสั่งสำหรับรายการเวลาในแอป Field Service</span><span class="sxs-lookup"><span data-stu-id="e527f-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="e527f-118">การอัปเดตเซลล์ **หน่วยนับที่อนุญาต** และ **กลุ่มของหน่วยนับ** ทำงานในกริด **ประมาณการค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="e527f-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="e527f-119">ฟอร์ม **อัปเดตการแก้ไขรายการเวลา** ประกอบด้วย **เส้นเวลา**</span><span class="sxs-lookup"><span data-stu-id="e527f-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="e527f-120">การอนุมัติเวลาสำหรับรายการเวลาที่ไม่ใช่โครงการจะบล็อกระบบเมื่อค้นหาบทบาทผู้อนุมัติโครงการ</span><span class="sxs-lookup"><span data-stu-id="e527f-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="e527f-121">**การจัดการทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="e527f-121">**Resource Management**</span></span>

<span data-ttu-id="e527f-122">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="e527f-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="e527f-123">เพิ่มการตรวจสอบความถูกต้องในปลั๊กอิน **PostProjectCreate** เพื่อตรวจสอบความต้องการหลักก่อนสร้าง</span><span class="sxs-lookup"><span data-stu-id="e527f-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="e527f-124">แบบฟอร์มสร้างด่วน **สมาชิกทีมโครงการ** จะแสดงข้อยกเว้นการอ้างอิงที่เป็นโมฆะหากฟิลด์ถูกลบออกจากฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="e527f-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="e527f-125">การสร้างข้อกำหนดเป็นเวลา 12 ชั่วโมงใน 1 ปีจะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="e527f-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="e527f-126">ปรับปรุงข้อยกเว้นการอ้างอิงว่างเปล่าของข้อความข้อผิดพลาดระหว่างการสร้างความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="e527f-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="e527f-127">**การจัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="e527f-127">**Project Management**</span></span>

<span data-ttu-id="e527f-128">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="e527f-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="e527f-129">ปรับปรุงการตรวจสอบเพื่อแก้ไขข้อยกเว้นการอ้างอิงที่เป็นโมฆะที่สร้างขึ้นในปลั๊กอิน **PreProjectUpdate**</span><span class="sxs-lookup"><span data-stu-id="e527f-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="e527f-130">โครงการที่เผยแพร่โดย Add-in บนเดสก์ท็อปของ Microsoft Project ลบการมอบหมายที่ไม่ได้มอบหมาย</span><span class="sxs-lookup"><span data-stu-id="e527f-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="e527f-131">เพิ่มการตรวจสอบความถูกต้องใหม่เมื่อการอ้างอิงโครงการของงานไม่ถูกต้อง เนื่องจากข้อยกเว้นการอ้างอิงว่างในปลั๊กอิน **PreValidateProjectTaskUpdate**</span><span class="sxs-lookup"><span data-stu-id="e527f-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="e527f-132">กริดสมาชิกทีมไม่แสดงการมอบหมายงานที่แตกต่างกันในเรกคอร์ดสมาชิกทีม</span><span class="sxs-lookup"><span data-stu-id="e527f-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="e527f-133">เพิ่มการตรวจสอบความถูกต้องและข้อความแสดงข้อผิดพลาดใหม่เนื่องจากข้อยกเว้นการอ้างอิงว่างในปลั๊กอิน **PreProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="e527f-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="e527f-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="e527f-134">**Sales**</span></span>

<span data-ttu-id="e527f-135">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="e527f-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="e527f-136">เมื่อเลือกรายการตามโครงการในใบเสนอราคาหรือสัญญา ปุ่ม **ข้อเสนอแนะ** ควรมองเห็นได้เฉพาะเมื่อเลือกรายการตามผลิตภัณฑ์ที่เกี่ยวข้องกับผลิตภัณฑ์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="e527f-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="e527f-137">แยกสิทธิ์การใช้งาน **Create_Product** จากสิทธิ์การใช้งาน **Create_ProjectContract**</span><span class="sxs-lookup"><span data-stu-id="e527f-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="e527f-138">การลบรายการใบแจ้งหนี้ทำให้การอ้างอิงเป็นโมฆะบน **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**</span><span class="sxs-lookup"><span data-stu-id="e527f-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
