---
title: โมเดลความปลอดภัย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับโมเดลความปลอดภัยใน Dynamics 365 Project Operations
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 3f65d13809fef342be8bec682c11d95c4d9e9b19
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276821"
---
# <a name="security-model"></a><span data-ttu-id="3212c-103">รูปแบบความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="3212c-103">Security Model</span></span>

<span data-ttu-id="3212c-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="3212c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3212c-105">Microsoft Dynamics 365 Project Operations มีโมเดลความปลอดภัยเฉพาะที่อนุญาตให้ใช้โมเดลความปลอดภัยทางธุรกิจตามบทบาทที่ทำงานร่วมกันกับกลุ่ม Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="3212c-105">Microsoft Dynamics 365 Project Operations contains a unique security model that allows for a role-based business security model that collaborates with Microsoft Office Groups.</span></span> 


## <a name="security-roles"></a><span data-ttu-id="3212c-106">บทบาทความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="3212c-106">Security roles</span></span>
<span data-ttu-id="3212c-107">ความสามารถส่วนหน้าของ Project Operations ประกอบด้วยบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3212c-107">Project Operations front-end capabilities include the following roles:</span></span>

| <span data-ttu-id="3212c-108">บทบาท</span><span class="sxs-lookup"><span data-stu-id="3212c-108">Role</span></span>                          | <span data-ttu-id="3212c-109">รายละเอียด</span><span class="sxs-lookup"><span data-stu-id="3212c-109">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="3212c-110">Scope</span><span class="sxs-lookup"><span data-stu-id="3212c-110">Scope</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="3212c-111">ผู้จัดการด้านการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="3212c-111">Practice manager</span></span>              | <span data-ttu-id="3212c-112">สนับสนุนการรายงานข้ามโครงการ</span><span class="sxs-lookup"><span data-stu-id="3212c-112">Supports cross-project reporting.</span></span>                                                                                                            | <span data-ttu-id="3212c-113">หน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="3212c-113">Business unit</span></span>              |
| <span data-ttu-id="3212c-114">ผู้อนุมัติโครงการ</span><span class="sxs-lookup"><span data-stu-id="3212c-114">Project approver</span></span>              | <span data-ttu-id="3212c-115">อนุมัติเวลาและค่าใช้จ่ายของโครงการ</span><span class="sxs-lookup"><span data-stu-id="3212c-115">Approves time and expenses against a project.</span></span>                                                                                                                              | <span data-ttu-id="3212c-116">หน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="3212c-116">Business unit</span></span> |
| <span data-ttu-id="3212c-117">ผู้ดูแลการเรียกเก็บเงินโครงการ</span><span class="sxs-lookup"><span data-stu-id="3212c-117">Project billing administrator</span></span> | <span data-ttu-id="3212c-118">สร้างข้อเสนอใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="3212c-118">Creates the invoice proposal.</span></span>                                                                                                                                                 | <span data-ttu-id="3212c-119">หน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="3212c-119">Business unit</span></span> |
| <span data-ttu-id="3212c-120">ผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="3212c-120">Project manager</span></span>               | <span data-ttu-id="3212c-121">สร้างแผนโครงการและร้องขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="3212c-121">Creates the project plan and requests resources.</span></span>                                                                                                                              | <span data-ttu-id="3212c-122">หน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="3212c-122">Business unit</span></span> |
| <span data-ttu-id="3212c-123">ทรัพยากรโครงการ</span><span class="sxs-lookup"><span data-stu-id="3212c-123">Project resource</span></span>              | <span data-ttu-id="3212c-124">สมาชิกทีมที่สามารถจองและรายงานเวลา</span><span class="sxs-lookup"><span data-stu-id="3212c-124">Team members who can be booked and report time.</span></span>                                                                                                          | <span data-ttu-id="3212c-125">หน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="3212c-125">Business unit</span></span>|
| <span data-ttu-id="3212c-126">ผู้จัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="3212c-126">Resource manager</span></span>              | <span data-ttu-id="3212c-127">ผู้จัดการทรัพยากรทั้งหมดทำหน้าที่ เช่น ตอบสนองคำขอทรัพยากรและการจอง ซึ่งแยกกันเพื่อสนับสนุนการกำหนดค่าผู้จัดการโครงการ + ผู้จัดการทรัพยากรแบบไฮบริด และบทบาทผู้จัดการทรัพยากรแบบเดี่ยวและแบบรวมศูนย์</span><span class="sxs-lookup"><span data-stu-id="3212c-127">All resource management functions, such as fulfill resource requests and bookings, separated to support a hybrid Project manager + Resource manager configuration and a single and centralized Resource manager role.</span></span> | <span data-ttu-id="3212c-128">หน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="3212c-128">Business unit</span></span> |


<span data-ttu-id="3212c-129">Microsoft Project สำหรับเว็บมีบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3212c-129">Microsoft Project for the Web includes the following roles:</span></span>

| <span data-ttu-id="3212c-130">บทบาท</span><span class="sxs-lookup"><span data-stu-id="3212c-130">Role</span></span>           | <span data-ttu-id="3212c-131">รายละเอียด</span><span class="sxs-lookup"><span data-stu-id="3212c-131">Description</span></span>                                                                                                        | <span data-ttu-id="3212c-132">Scope</span><span class="sxs-lookup"><span data-stu-id="3212c-132">Scope</span></span>  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| <span data-ttu-id="3212c-133">ผู้ใช้โครงการ</span><span class="sxs-lookup"><span data-stu-id="3212c-133">Project user</span></span>   | <span data-ttu-id="3212c-134">ผู้ใช้ของโครงการที่ทำงานร่วมกันซึ่งสามารถสร้างโครงการของตนเองและดูโครงการใดๆ ที่แชร์กับพวกเขาได้</span><span class="sxs-lookup"><span data-stu-id="3212c-134">Collaborative user of Project   who is able to create their own projects and view any projects shared with   them.</span></span> | <span data-ttu-id="3212c-135">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="3212c-135">User</span></span>   |
| <span data-ttu-id="3212c-136">ระบบโครงการ</span><span class="sxs-lookup"><span data-stu-id="3212c-136">Project system</span></span> | <span data-ttu-id="3212c-137">บทบาทที่ใช้สำหรับบริบทของแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="3212c-137">Role used for application   context.</span></span> <span data-ttu-id="3212c-138">ลูกค้าไม่ควรใช้บทบาทระบบนี้</span><span class="sxs-lookup"><span data-stu-id="3212c-138">Customers should not use this system role.</span></span>                                    | <span data-ttu-id="3212c-139">ส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="3212c-139">Global</span></span> |

## <a name="security-enforcement"></a><span data-ttu-id="3212c-140">การบังคับใช้ความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="3212c-140">Security enforcement</span></span>
<span data-ttu-id="3212c-141">การดำเนินการที่ดำเนินการในระดับโครงการจะทำในบริบทของผู้ใช้ที่เข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="3212c-141">Actions that are performed at the project level are performed in the context of the logged in user.</span></span> <span data-ttu-id="3212c-142">ซึ่งหมายความว่าในการสร้าง เปิด หรือลบโครงการ ผู้ใช้จะต้องมีสิทธิ์เข้าถึงที่มีอยู่ใน CDS</span><span class="sxs-lookup"><span data-stu-id="3212c-142">This means that in order to create, open, or delete a project, the user is required to have access available in CDS.</span></span> <span data-ttu-id="3212c-143">การเข้าถึงใน CDS อาจได้รับผ่านกลไกที่เป็นไปได้ที่รวมอยู่ในแพลตฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="3212c-143">Access in CDS may be granted through any of the possible mechanisms included in the platform.</span></span> <span data-ttu-id="3212c-144">ตัวอย่างเช่น ผู้ใช้ที่มีขอบเขตใหญ่กว่าอาจเข้าถึงโครงการหรือหากมีการดำเนินการแชร์โครงการอย่างชัดเจนซึ่งให้สิทธิ์การเข้าถึงแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="3212c-144">For example, a user with a larger scope may access the project or if an explicit project share action has been performed which grants the user access.</span></span>

<span data-ttu-id="3212c-145">สิ่งสำคัญที่ต้องพิจารณาเมื่อสร้างโครงการใน Project Operations</span><span class="sxs-lookup"><span data-stu-id="3212c-145">It's important to consider this when creating projects in Project Operations.</span></span>

## <a name="modern-group-collaboration-with-project-operations"></a><span data-ttu-id="3212c-146">การทำงานร่วมกันเป็นกลุ่มสมัยใหม่กับ Project Operations</span><span class="sxs-lookup"><span data-stu-id="3212c-146">Modern group collaboration with Project Operations</span></span>
<span data-ttu-id="3212c-147">โครงการสำหรับเว็บและ Project Operations สนับสนุนกลุ่มสมัยใหม่สำหรับการทำงานร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="3212c-147">Project for the Web and Project Operations support modern groups for collaboration.</span></span> <span data-ttu-id="3212c-148">ผู้ใช้ที่เพิ่มลงในโครงการผ่านกลุ่มสามารถแก้ไขแผนโครงการได้</span><span class="sxs-lookup"><span data-stu-id="3212c-148">Users added to the project through a group are able to edit the project plan.</span></span>

<span data-ttu-id="3212c-149">โครงการสำหรับเว็บจะเพิ่มผู้ใช้ในกลุ่มโดยอัตโนมัติเมื่อได้รับมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="3212c-149">Project for the Web adds users to the group automatically upon assignment.</span></span>

<span data-ttu-id="3212c-150">กลุ่มอนุญาตให้สิทธิ์ของโครงการและการสนับสนุนอาร์ติแฟกต์การทำงานร่วมกันในการทำงานร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="3212c-150">Groups allow the permissions of the project and supporting collaboration artifacts to be worked on collaboratively.</span></span> <span data-ttu-id="3212c-151">แผนภาพต่อไปนี้แสดงให้เห็นถึงเหตุการณ์และการเปลี่ยนแปลงสถานะที่เกิดขึ้นระหว่างกระบวนการกำหนดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="3212c-151">The following diagram depicts the events and state changes that happen during the group assignment process.</span></span>

<span data-ttu-id="3212c-152">Project Operations ไม่ได้สร้างกลุ่มผ่านการดำเนินการโดยนัยและดำเนินการผ่านการดำเนินการอย่างชัดเจนของกลุ่มที่กดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3212c-152">Project Operations does not create a group through implicit action and only does so through the explicit action of pressing groups.</span></span>

<span data-ttu-id="3212c-153">การค้นหาสมาชิกกลุ่มในกล่องโต้ตอบ **การจัดการกลุ่ม** จำกัดเฉพาะผู้ที่ถูกตั้งค่าให้เป็นส่วนหนึ่งของกลุ่มความปลอดภัยของสภาพแวดล้อมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3212c-153">Group member search in the **Group management** dialog, is limited to those who are set as part of the environment's security group.</span></span> <span data-ttu-id="3212c-154">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ควบคุมการเข้าถึงสภาพแวดล้อมของผู้ใช้: กลุ่มการรักษาความปลอดภัยและสิทธิ์การใช้งาน](https://docs.microsoft.com/power-platform/admin/control-user-access)</span><span class="sxs-lookup"><span data-stu-id="3212c-154">For more information, see [Control user access to environments: security groups and licenses](https://docs.microsoft.com/power-platform/admin/control-user-access).</span></span>

![โหมดกลุ่ม](./media/groupsmode.png)

1. <span data-ttu-id="3212c-156">มีการสร้างโครงการและเป็นเจ้าของโดยผู้ใช้ที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="3212c-156">The Project is created and owned by the creating User.</span></span>
2. <span data-ttu-id="3212c-157">มีการปรับปรุงเจ้าของโครงการเข้าสู่ทีม</span><span class="sxs-lookup"><span data-stu-id="3212c-157">The Project owner is updated to the team.</span></span>
3. <span data-ttu-id="3212c-158">ทีมเจ้าของถูกแม็ปกับกลุ่ม Office ที่ระบุหรือสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="3212c-158">The Owner team is mapped to the specified or created Office Group.</span></span>
4. <span data-ttu-id="3212c-159">เจ้าของของโครงการเดิมจะถูกเพิ่มเข้าไปในกลุ่ม Office</span><span class="sxs-lookup"><span data-stu-id="3212c-159">The original owner of the Project is added to the Office Group.</span></span>

## <a name="deployment-recommendation"></a><span data-ttu-id="3212c-160">คำแนะนำการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3212c-160">Deployment recommendation</span></span>
<span data-ttu-id="3212c-161">เมื่อรูปแบบการทำงานร่วมกันของกลุ่ม Office มีการพัฒนาขึ้น จะมีการเพิ่มฟังก์ชันการทำงานเพื่อให้สามารถควบคุมได้อย่างละเอียดมากขึ้นตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="3212c-161">As the Office group collaboration model evolves, functionality will be added to provide more detailed control over time.</span></span> <span data-ttu-id="3212c-162">ลูกค้าที่ปรับใช้ Project Operations ในปัจจุบันได้รับการสนับสนุนให้มุ่งเน้นรูปแบบความปลอดภัย Microsoft Dynamics 365 แบบดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="3212c-162">Customers that deploy Project Operations today are encouraged to focus on a traditional Microsoft Dynamics 365 security model.</span></span>

<span data-ttu-id="3212c-163">สำหรับข้อมูลเพิ่มเติม ดูที่ [ความปลอดภัยใน Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security)</span><span class="sxs-lookup"><span data-stu-id="3212c-163">For more information, see [Security in Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).</span></span>

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a><span data-ttu-id="3212c-164">ความปลอดภัยของ Project Operations และ Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="3212c-164">Project Operations and Microsoft Dynamics 365 Finance security</span></span>
<span data-ttu-id="3212c-165">Project Operations ประกอบด้วยบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3212c-165">Project Operations includes the following roles:</span></span>

- <span data-ttu-id="3212c-166">ผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="3212c-166">Project manager</span></span>
- <span data-ttu-id="3212c-167">นักบัญชีของโครงการ</span><span class="sxs-lookup"><span data-stu-id="3212c-167">Project accountant</span></span>

<span data-ttu-id="3212c-168">สำหรับข้อมูลเกี่ยวกับความปลอดภัยใน Finance ดูที่ [ความปลอดภัยตามบทบาท](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security)</span><span class="sxs-lookup"><span data-stu-id="3212c-168">For more information about security in Finance, see [Role-based security](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]