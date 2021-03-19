---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุงโปรแกรมแก้ไขด่วน 27.6 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation รุ่นการปรับปรุงโปรแกรมแก้ไขด่วน 27.6 V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/17/2021
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
ms.openlocfilehash: f6576c6c5660ff6e8e53286ae226c8278a33f2be
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/04/2021
ms.locfileid: "5481329"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-276-v3"></a><span data-ttu-id="ad63a-103">มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 27.6 V3</span><span class="sxs-lookup"><span data-stu-id="ad63a-103">What's new or changed in Project Service Automation Update Release 27.6, V3</span></span>

<span data-ttu-id="ad63a-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ad63a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ad63a-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ad63a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ad63a-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="ad63a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ad63a-107">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชัน เพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="ad63a-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ad63a-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="ad63a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ad63a-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation V3 รุ่นการปรับปรุง 27.6</span><span class="sxs-lookup"><span data-stu-id="ad63a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 27.6.</span></span> <span data-ttu-id="ad63a-110">รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.45.120 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตด้วยตนเองในเดือนมกราคม 2021</span><span class="sxs-lookup"><span data-stu-id="ad63a-110">This version has a build number of V3.10.45.120 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-276"></a><span data-ttu-id="ad63a-111">รุ่นการปรับปรุง 27.6</span><span class="sxs-lookup"><span data-stu-id="ad63a-111">Update Release 27.6</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ad63a-112">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="ad63a-112">Bug fixes</span></span>


<span data-ttu-id="ad63a-113">**การจัดการทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="ad63a-113">**Resource Management**</span></span>

<span data-ttu-id="ad63a-114">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="ad63a-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="ad63a-115">เมื่อพบความพร้อมบริการของทรัพยากร จะมีการเรียก **ExpandCalendar** สำหรับทรัพยากรแต่ละรายการที่ไม่มีการใช้กฎปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="ad63a-115">When finding resource availability, **ExpandCalendar** is called for each resource that has no calendar rules applied.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
