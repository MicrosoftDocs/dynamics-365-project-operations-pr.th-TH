---
title: มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงในการเข้าถึงก่อนสำหรับ Project Service Automation เวฟ 1 2021, V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานในการเข้าถึงก่อนสำหรับ Project Service Automation เวฟ 1 2021, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2021
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
ms.openlocfilehash: d99906b11b0189fc8227accd68bd0457f6baa42c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281186"
---
# <a name="whats-new-or-changed-in-project-service-automation-early-access-wave-1-2021-v3"></a><span data-ttu-id="c1bfb-103">มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงในการเข้าถึงก่อนสำหรับ Project Service Automation เวฟ 1 2021, V3</span><span class="sxs-lookup"><span data-stu-id="c1bfb-103">What's new or changed in Project Service Automation Early Access Wave 1 2021, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

## <a name="project-service-automation-early-access-wave-1-2021-v3"></a><span data-ttu-id="c1bfb-104">การเข้าถึงก่อนสำหรับ Project Service Automation เวฟ 1 2021, V3</span><span class="sxs-lookup"><span data-stu-id="c1bfb-104">Project Service Automation Early Access Wave 1 2021, V3</span></span>

<span data-ttu-id="c1bfb-105">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c1bfb-105">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="c1bfb-106">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c1bfb-106">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c1bfb-107">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="c1bfb-107">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c1bfb-108">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชัน เพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="c1bfb-108">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="c1bfb-109">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="c1bfb-109">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c1bfb-110">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation V3 เวฟ 1 2021</span><span class="sxs-lookup"><span data-stu-id="c1bfb-110">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Early Access Wave 1 2021.</span></span> <span data-ttu-id="c1bfb-111">รุ่นนี้มีหมายเลขรุ่น V3.10.49.3 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตด้วยตนเองในเดือนกุมภาพันธ์ 2021</span><span class="sxs-lookup"><span data-stu-id="c1bfb-111">This version has a build number of V3.10.49.3 and is generally available through a self-update in February 2021.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="c1bfb-112">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="c1bfb-112">Bug fixes</span></span>

<span data-ttu-id="c1bfb-113">**เวลาและค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="c1bfb-113">**Time and Expense**</span></span>

<span data-ttu-id="c1bfb-114">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="c1bfb-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="c1bfb-115">วันที่สิ้นสุดเติมอัตโนมัติเมื่อรายการเวลาถูกสร้างขึ้นหากระยะเวลาเป็นโมฆะ</span><span class="sxs-lookup"><span data-stu-id="c1bfb-115">End dates auto-populate when a time entry is created if the duration is null.</span></span>
- <span data-ttu-id="c1bfb-116">ผู้ใช้สามารถเปลี่ยนงานในรายการเวลาที่ได้รับการอนุมัติหรือส่ง</span><span class="sxs-lookup"><span data-stu-id="c1bfb-116">Users can change the task on a time entry that has been approved or submitted.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]