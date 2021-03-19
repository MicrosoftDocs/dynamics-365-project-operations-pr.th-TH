---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 16 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation รุ่นการปรับปรุง 16 V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 1f3bb4442ce1d06807f264003c930dbbee19a5c7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280916"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="fbc10-103">Project Service Automation รุ่นการปรับปรุง 16 V3</span><span class="sxs-lookup"><span data-stu-id="fbc10-103">Project Service Automation Update Release 16, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fbc10-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="fbc10-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="fbc10-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fbc10-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="fbc10-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="fbc10-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fbc10-107">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชันเพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="fbc10-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="fbc10-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง ปรับปรุง โซลูชันที่ต้องการ](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page)</span><span class="sxs-lookup"><span data-stu-id="fbc10-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="fbc10-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่เป็นของใหม่หรือที่เปลี่ยนแปลงสำหรับ PSA V3, รุ่นการปรับปรุง 16</span><span class="sxs-lookup"><span data-stu-id="fbc10-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="fbc10-110">รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.6.34 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตด้วยตนเองในเดือนมกราคม 2020</span><span class="sxs-lookup"><span data-stu-id="fbc10-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="fbc10-111">รุ่นการปรับปรุง 16</span><span class="sxs-lookup"><span data-stu-id="fbc10-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fbc10-112">การแก้ไขข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="fbc10-112">Bug fixes</span></span>

-   <span data-ttu-id="fbc10-113">เวลาและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="fbc10-113">Time and Expense</span></span>

    -   <span data-ttu-id="fbc10-114">แก้ไขแล้ว: ในขณะนี้ ผู้ใช้ที่พยายามส่งเวลาที่ถูกลบและรายการค่าใช้จ่ายสำหรับการอนุมัติ จะได้รับข้อความแสดงข้อผิดพลาดที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="fbc10-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="fbc10-115">การจัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="fbc10-115">Project Management</span></span>

    -   <span data-ttu-id="fbc10-116">แก้ไขแล้ว: หน่วยการจัดหาที่กำหนดไว้สำหรับสมาชิกในกลุ่มคนในแม่แบบ ถูกคำนึงถึงพร้อมกับแม่แบบที่ใช้กับโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="fbc10-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="fbc10-117">แก้ไขแล้ว: ปรับปรุงการจัดการการมอบหมายความเป็นเจ้าของเรคคอร์ดอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="fbc10-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="fbc10-118">แก้ไขแล้ว: โครงการที่อยู่ระหว่างการคัดลอกจะไม่ได้รับอนุญาตให้คัดลอก จนกว่าการดำเนินการคัดลอกทั้งหมดจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fbc10-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="fbc10-119">การจัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="fbc10-119">Resource Management</span></span>

    -   <span data-ttu-id="fbc10-120">แก้ไขแล้ว: ในขณะนี้การขยายการจองจัดการระยะเวลาสั้นๆ ได้อย่างถูกต้อง และไม่สร้างชั่วโมงเป็นศูนย์สำหรับการจองแบบขยาย</span><span class="sxs-lookup"><span data-stu-id="fbc10-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="fbc10-121">แก้ไขแล้ว: มุมมองการปรับยอดขณะนี้แสดงผล เมื่อโซนเวลาของโครงการคือ +5:30 GMT และเวลาของผู้ใช้แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="fbc10-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="fbc10-122">Sales</span><span class="sxs-lookup"><span data-stu-id="fbc10-122">Sales</span></span>

    -   <span data-ttu-id="fbc10-123">แก้ไขแล้ว: เมื่อโครงการที่แม็ปไปยังบรายละเอียดการให้บริการตามสัญญาถูกลบและมีการแม็ปโครงการใหม่ เรกคอร์ดจริงในโครงการใหม่ไม่ได้รับการประเมินอีกครั้งตามกฎการเรียกเก็บเงินและการกำหนดราคาที่กำหนดในรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="fbc10-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="fbc10-124">นี่ได้รับการแก้ไขแล้วในรีลีสนี้</span><span class="sxs-lookup"><span data-stu-id="fbc10-124">This has been fixed in this release.</span></span> <span data-ttu-id="fbc10-125">การกำหนดราคาและเรกคอร์ดจริงในโครงการที่แม็ปใหม่ จะถูกกลับรายการและถูกสร้างใหม่อย่างถูกต้องตามกฎการกำหนดราคาและการเรียกเก็บเงินของรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="fbc10-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="fbc10-126">นอกจากนี้ เรกคอร์ดจริงของโครงการที่ไม่ได้แม็ปยังจะถูกประเมินอีกครั้งและถูกสร้างขึ้นใหม่ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="fbc10-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="fbc10-127">แก้ไขแล้ว: มีการเพิ่มการตรวจสอบความถูกต้องเพิ่มเติมในฟิลด์ **จำนวน** ของรายการการประมาณการ เพื่อให้แน่ใจว่าค่า Null ไม่คงอยู่</span><span class="sxs-lookup"><span data-stu-id="fbc10-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="fbc10-128">แก้ไขแล้ว: เมื่อมีการปรับปรุงข้อมูลจริงในโครงการ ปุ่มรีเฟรชจะถูกเพิ่มไปยังฟอร์มหลักของโครงการเพื่อให้ผู้ใช้สามารถซิงค์ข้อมูลจริงได้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="fbc10-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="fbc10-129">แก้ไขแล้ว: เมื่อผู้ใช้อัพเกรดจาก 2.X เป็น 3.X โครงการที่มีค่า NULL สำหรับชื่อโครงการจะได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="fbc10-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]