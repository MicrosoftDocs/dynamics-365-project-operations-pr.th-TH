---
title: มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Project Service Automation รุ่น 3.x เวฟ 1 2020
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับสิ่งใหม่และสิ่งที่เปลี่ยนแปลงใน Project Service Automation รุ่น 3 เวฟ 1 2020
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2308f83e09c25059b6a36599b04b5b00f66c704f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126506"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="0ec0f-103">มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Project Service Automation รุ่น 3 เวฟ 1 2020</span><span class="sxs-lookup"><span data-stu-id="0ec0f-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="0ec0f-104">หัวข้อเน้นข้อควรพิจารณาในการปรับรุ่นของคีย์เมื่อย้ายไปยังรุ่นล่าสุดของ Project Service Automation (PSA) รุ่น 3.x เวฟ 1 2020</span><span class="sxs-lookup"><span data-stu-id="0ec0f-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="0ec0f-105">รายการเวลา</span><span class="sxs-lookup"><span data-stu-id="0ec0f-105">Time entry</span></span>
<span data-ttu-id="0ec0f-106">ประสบการณ์รายการเวลาได้รับการขยายเพื่อมอบความสามารถในการขยายเวลาเข้าสู่สถานการณ์ลูกค้ามากขึ้น</span><span class="sxs-lookup"><span data-stu-id="0ec0f-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="0ec0f-107">ซึ่งรวมถึงความสามารถในการเพิ่มประเภทรายการ ซึ่งตอนนี้กระตุ้นให้เกิดพฤติกรรมที่เฉพาะเจาะจง ขึ้นอยู่กับชื่อ Schema **การตั้งค่ารายการเวลา** แสดงเป็น **แหล่งเวลา**</span><span class="sxs-lookup"><span data-stu-id="0ec0f-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="0ec0f-108">มีการเพิ่มโซลูชันใหม่ที่เรียกว่าเวลา ค่าใช้จ่าย สถานะ และการอนุมัติ (TESA) เพื่อรองรับฟังก์ชันการทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="0ec0f-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="0ec0f-109">ข้อควรพิจารณาในการปรับรุ่น</span><span class="sxs-lookup"><span data-stu-id="0ec0f-109">Upgrade consideration</span></span>
<span data-ttu-id="0ec0f-110">เพื่อรองรับฟังก์ชันนี้ บทบาทภายใน PSA ได้รับการปรับปรุงเพื่อรวมสิทธิการใช้งานใหม่ๆ</span><span class="sxs-lookup"><span data-stu-id="0ec0f-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="0ec0f-111">สิทธิ์การใช้งานเหล่านี้ให้สิทธิ์การอ่านเพื่อเข้าถึงเอนทิตีใหม่ **การตั้งค่ารายการเวลา**</span><span class="sxs-lookup"><span data-stu-id="0ec0f-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="0ec0f-112">ผู้ใช้ที่ต้องการความสามารถในการบันทึกเวลาควรได้รับบทบาทผู้ใช้ **ผู้ใช้รายการเวลา** นอกเหนือจากบทบาทที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="0ec0f-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="0ec0f-113">บทบาทนี้รวมถึงฟังก์ชันใหม่และช่วยให้มั่นใจได้ว่ารายการเวลาจะทำงานต่อ</span><span class="sxs-lookup"><span data-stu-id="0ec0f-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="0ec0f-114">นอกจากนี้หากคุณมีโมดูลแอปที่กำหนดเองที่มีทุกรูปแบบสำหรับเอนทิตีรายการเวลา คุณจะต้องลบ **แบบฟอร์มการสร้างด่วนของรายการเวลาของ TESA** ออกจากโมดูล</span><span class="sxs-lookup"><span data-stu-id="0ec0f-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="0ec0f-115">การเปลี่ยนแปลงรายการเวลาที่นานขึ้นในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="0ec0f-115">Currently extended time entry changes</span></span>
<span data-ttu-id="0ec0f-116">เพื่อลดผลกระทบต่อผู้ใช้งานปัจจุบันของรายการเวลา การเปลี่ยนแปลงบทบาทนี้เป็นข้อกำหนดหลักเพียงอย่างเดียวที่จำเป็นในการใช้ประโยชน์จากรายการเวลาต่อไป</span><span class="sxs-lookup"><span data-stu-id="0ec0f-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="0ec0f-117">หากคุณสร้างมุมมองที่กำหนดเองหรือประสบการณ์รายการเวลาแยกกันคุณต้องตั้งค่าฟิลด์ **การตั้งค่ารายการเวลา** เป็นค่า PSA ที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="0ec0f-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
