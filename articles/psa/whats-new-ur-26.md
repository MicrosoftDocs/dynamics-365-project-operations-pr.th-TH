---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 26 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation รุ่นการปรับปรุง 26 V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 14fcccf5804e5da0926dbc69bdfa040229a7f068
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143581"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="f35b5-103">Project Service Automation รุ่นการปรับปรุง 26 V3</span><span class="sxs-lookup"><span data-stu-id="f35b5-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f35b5-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="f35b5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f35b5-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f35b5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f35b5-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="f35b5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f35b5-107">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชัน เพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="f35b5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="f35b5-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="f35b5-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f35b5-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation รุ่นการปรับปรุง 26 V3</span><span class="sxs-lookup"><span data-stu-id="f35b5-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="f35b5-110">รุ่นนี้มีหมายเลขรุ่น V3.10.44.59 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตด้วยตนเองในเดือนธันวาคม 2020</span><span class="sxs-lookup"><span data-stu-id="f35b5-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="f35b5-111">รุ่นการปรับปรุง 26</span><span class="sxs-lookup"><span data-stu-id="f35b5-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f35b5-112">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="f35b5-112">Bug fixes</span></span>

<span data-ttu-id="f35b5-113">**เวลาและค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="f35b5-113">**Time and Expense**</span></span>

<span data-ttu-id="f35b5-114">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="f35b5-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="f35b5-115">ผู้ใช้สามารถเปลี่ยนงานในรายการเวลาที่ได้รับการอนุมัติ/ส่ง</span><span class="sxs-lookup"><span data-stu-id="f35b5-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="f35b5-116">"ไม่ได้ตั้งค่าการอ้างอิงออบเจ็กต์ " เกิดข้อผิดพลาดเมื่อบันทึกรายการเวลา</span><span class="sxs-lookup"><span data-stu-id="f35b5-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="f35b5-117">การนำเข้ารายการเวลาจากการกำหนดทรัพยากรสร้างรายการเวลาด้วยค่า วันที่เวลา ที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f35b5-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="f35b5-118">เมื่อติดตั้ง Project Service Automation และแอป Field Service แล้ว ปุ่ม **สร้าง** แสดงสองครั้งบนแถบคำสั่งสำหรับรายการเวลาในแอป Field Service</span><span class="sxs-lookup"><span data-stu-id="f35b5-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="f35b5-119">การอัปเดตเซลล์ **หน่วยนับที่อนุญาต** และ **กลุ่มของหน่วยนับ** ทำงานในกริด **ประมาณการค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="f35b5-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="f35b5-120">ฟอร์ม **อัปเดตการแก้ไขรายการเวลา** ประกอบด้วย **เส้นเวลา**</span><span class="sxs-lookup"><span data-stu-id="f35b5-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="f35b5-121">การอนุมัติเวลาสำหรับรายการเวลาที่ไม่ใช่โครงการจะบล็อกระบบเมื่อค้นหาบทบาทผู้อนุมัติโครงการ</span><span class="sxs-lookup"><span data-stu-id="f35b5-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="f35b5-122">**การจัดการทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="f35b5-122">**Resource Management**</span></span>

<span data-ttu-id="f35b5-123">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="f35b5-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="f35b5-124">เพิ่มการตรวจสอบความถูกต้องในปลั๊กอิน **PostProjectCreate** เพื่อตรวจสอบความต้องการหลักก่อนสร้าง</span><span class="sxs-lookup"><span data-stu-id="f35b5-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="f35b5-125">แบบฟอร์มสร้างด่วน **สมาชิกทีมโครงการ** จะแสดงข้อยกเว้นการอ้างอิงที่เป็นโมฆะหากฟิลด์ถูกลบออกจากฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="f35b5-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="f35b5-126">การสร้างข้อกำหนดเป็นเวลา 12 ชั่วโมงใน 1 ปีจะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="f35b5-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="f35b5-127">ปรับปรุงข้อยกเว้นการอ้างอิงว่างเปล่าของข้อความข้อผิดพลาดระหว่างการสร้างความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="f35b5-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="f35b5-128">**การจัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="f35b5-128">**Project Management**</span></span>

<span data-ttu-id="f35b5-129">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="f35b5-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="f35b5-130">ปรับปรุงการตรวจสอบเพื่อแก้ไขข้อยกเว้นการอ้างอิงที่เป็นโมฆะที่สร้างขึ้นในปลั๊กอิน **PreProjectUpdate**</span><span class="sxs-lookup"><span data-stu-id="f35b5-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="f35b5-131">โครงการที่เผยแพร่โดย Add-in บนเดสก์ท็อปของ Microsoft Project ลบการมอบหมายที่ไม่ได้มอบหมาย</span><span class="sxs-lookup"><span data-stu-id="f35b5-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="f35b5-132">เพิ่มการตรวจสอบความถูกต้องใหม่เมื่อการอ้างอิงโครงการของงานไม่ถูกต้อง เนื่องจากข้อยกเว้นการอ้างอิงว่างในปลั๊กอิน **PreValidateProjectTaskUpdate**</span><span class="sxs-lookup"><span data-stu-id="f35b5-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="f35b5-133">กริดสมาชิกทีมไม่แสดงการมอบหมายงานที่แตกต่างกันในเรกคอร์ดสมาชิกทีม</span><span class="sxs-lookup"><span data-stu-id="f35b5-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="f35b5-134">เพิ่มการตรวจสอบความถูกต้องและข้อความแสดงข้อผิดพลาดใหม่เนื่องจากข้อยกเว้นการอ้างอิงว่างในปลั๊กอิน **PreProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="f35b5-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="f35b5-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="f35b5-135">**Sales**</span></span>

<span data-ttu-id="f35b5-136">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="f35b5-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="f35b5-137">เมื่อเลือกรายการตามโครงการในใบเสนอราคาหรือสัญญา ปุ่ม **ข้อเสนอแนะ** ควรมองเห็นได้เฉพาะเมื่อเลือกรายการตามผลิตภัณฑ์ที่เกี่ยวข้องกับผลิตภัณฑ์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="f35b5-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="f35b5-138">แยกสิทธิ์การใช้งาน **Create_Product** จากสิทธิ์การใช้งาน **Create_ProjectContract**</span><span class="sxs-lookup"><span data-stu-id="f35b5-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="f35b5-139">การลบรายการใบแจ้งหนี้ทำให้การอ้างอิงเป็นโมฆะบน **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**</span><span class="sxs-lookup"><span data-stu-id="f35b5-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
