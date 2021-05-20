---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 17.5 Hotfix V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation V3 รุ่นการปรับปรุง 17.5 V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/13/2020
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
ms.openlocfilehash: b3d58cb4a2f8fea1495d143dd985ad17a5cc4130
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949297"
---
# <a name="project-service-automation-update-release-175-v3"></a><span data-ttu-id="5d444-103">Project Service Automation รุ่นการปรับปรุง 17.5 V3</span><span class="sxs-lookup"><span data-stu-id="5d444-103">Project Service Automation Update Release 17.5, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="5d444-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="5d444-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="5d444-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="5d444-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="5d444-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="5d444-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5d444-107">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชันเพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="5d444-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="5d444-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="5d444-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="5d444-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่เป็นของใหม่หรือที่เปลี่ยนแปลงสำหรับ V3 รุ่นการปรับปรุง 17.5</span><span class="sxs-lookup"><span data-stu-id="5d444-109">This topic lists the features and fixes that are new or changed for V3, Update Release 17.5.</span></span> <span data-ttu-id="5d444-110">รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.7.32 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตด้วยตนเองในเดือนมีนาคม 2020</span><span class="sxs-lookup"><span data-stu-id="5d444-110">This version has a build number of V3.10.7.32 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-175"></a><span data-ttu-id="5d444-111">รุ่นการปรับปรุง 17.5</span><span class="sxs-lookup"><span data-stu-id="5d444-111">Update Release 17.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="5d444-112">การแก้ไขข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="5d444-112">Bug fixes</span></span>


<span data-ttu-id="5d444-113">**การจัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="5d444-113">**Project Management**</span></span>

- <span data-ttu-id="5d444-114">แก้ไขแล้ว: ระบุปัญหาการซิงโครไนซ์ฝั่งเซิร์ฟเวอร์ที่เกิดขึ้นกับงานที่ต้องใช้เวลานาน</span><span class="sxs-lookup"><span data-stu-id="5d444-114">Fixed: Addressed server-side synchronization issues that occur with long duration tasks.</span></span>
- <span data-ttu-id="5d444-115">แก้ไขแล้ว: ระบุแม่แบบชั่วโมงการทำงาน 24 ชั่วโมงซึ่งเพิ่มวันเพิ่มเติมให้กับงานโดยไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5d444-115">Fixed: Addressed 24-hour work hour templates inaccurately adding an additional day to tasks.</span></span>
- <span data-ttu-id="5d444-116">แก้ไขแล้ว: ระบุแม่แบบชั่วโมงการทำงาน GMT +13 ที่เปลี่ยนแปลงเวลาไปหนึ่งวันล่วงหน้าโดยไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5d444-116">Fixed: Addressed +13 GMT work hour templates inaccurately shifting tasks one day ahead.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]