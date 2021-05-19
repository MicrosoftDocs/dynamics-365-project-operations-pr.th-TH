---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุงโปรแกรมแก้ไขด่วน 29.5 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation รุ่นการปรับปรุงโปรแกรมแก้ไขด่วน 29.5 V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/26/2021
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
ms.openlocfilehash: 99ba353236ad88b8bdff2c1b25e1247fa4bf3455
ms.sourcegitcommit: 9ebf7dd501898053bfa824f732adabf3f273613b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/26/2021
ms.locfileid: "5715715"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-295-v3"></a><span data-ttu-id="541f0-103">มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 29.5 V3</span><span class="sxs-lookup"><span data-stu-id="541f0-103">What's new or changed in Project Service Automation Update Release 29.5, V3</span></span>

<span data-ttu-id="541f0-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="541f0-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="541f0-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="541f0-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="541f0-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="541f0-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="541f0-107">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชัน เพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="541f0-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="541f0-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="541f0-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="541f0-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation V3 รุ่นการปรับปรุง 29.5</span><span class="sxs-lookup"><span data-stu-id="541f0-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.5.</span></span> <span data-ttu-id="541f0-110">รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.47.150 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตด้วยตนเองในเดือนมกราคม 2021</span><span class="sxs-lookup"><span data-stu-id="541f0-110">This version has a build number of V3.10.47.150 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-295"></a><span data-ttu-id="541f0-111">รุ่นการปรับปรุง 29.5</span><span class="sxs-lookup"><span data-stu-id="541f0-111">Update Release 29.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="541f0-112">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="541f0-112">Bug fixes</span></span>


<span data-ttu-id="541f0-113">**การขาย**</span><span class="sxs-lookup"><span data-stu-id="541f0-113">**Sales**</span></span>

<span data-ttu-id="541f0-114">ปัญหาต่อไปนี้ได้รับการแก้ไขแล้ว:</span><span class="sxs-lookup"><span data-stu-id="541f0-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="541f0-115">มีข้อยกเว้นการอ้างอิงค่า null ที่เป็นไปได้ใน **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** เมื่อคุณปิดใบเสนอราคาเป็นชนะและใบเสนอราคาไม่มีรายการราคา</span><span class="sxs-lookup"><span data-stu-id="541f0-115">A possible null reference exception occurs in **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** when you close a quote as won and the quote has no price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]