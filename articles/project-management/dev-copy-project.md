---
title: พัฒนาแม่แบบโครงการด้วย คัดลอกโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีสร้างแม่แบบโครงการโดยใช้การดำเนินการ คัดลอกโครงการ แบบกำหนดเอง
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085872"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="61555-103">พัฒนาแม่แบบโครงการด้วย คัดลอกโครงการ</span><span class="sxs-lookup"><span data-stu-id="61555-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="61555-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="61555-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="61555-105">Dynamics 365 Project Operations สนับสนุนความสามารถในการคัดลอกโครงการและเปลี่ยนการมอบหมายกลับไปยังทรัพยากรทั่วไปที่แสดงถึงบทบาท</span><span class="sxs-lookup"><span data-stu-id="61555-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="61555-106">ลูกค้าสามารถใช้ฟังก์ชันนี้เพื่อสร้างแม่แบบโครงการพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="61555-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="61555-107">เมื่อคุณเลือก **คัดลอกโครงการ** สถานะของโครงการเป้าหมายจะได้รับการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="61555-107">When you select **Copy Project** , the status of the target project is updated.</span></span> <span data-ttu-id="61555-108">ใช้ **คำอธิบายรายการของสถานะ** เพื่อพิจารณาว่าการคัดลอกเสร็จสมบูรณ์เมื่อใด</span><span class="sxs-lookup"><span data-stu-id="61555-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="61555-109">กำลังเลือก **คัดลอกโครงการ** นอกจากนี้ยังอัปเดตวันที่เริ่มต้นของโครงการเป็นวันที่เริ่มต้นปัจจุบันหากไม่พบวันที่เป้าหมายในเอนทิตีโครงการเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="61555-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="61555-110">การดำเนินการ คัดลอกโครงการ แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="61555-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="61555-111">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="61555-111">Name</span></span> 

<span data-ttu-id="61555-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="61555-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="61555-113">พารามิเตอร์อินพุต</span><span class="sxs-lookup"><span data-stu-id="61555-113">Input parameters</span></span>
<span data-ttu-id="61555-114">มีพารามิเตอร์ข้อมูลป้อนเข้าสามรายการ:</span><span class="sxs-lookup"><span data-stu-id="61555-114">There are three input parameters:</span></span>

| <span data-ttu-id="61555-115">พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="61555-115">Parameter</span></span>          | <span data-ttu-id="61555-116">พิมพ์ข้อความ</span><span class="sxs-lookup"><span data-stu-id="61555-116">Type</span></span>   | <span data-ttu-id="61555-117">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="61555-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="61555-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="61555-118">ProjectCopyOption</span></span>  | <span data-ttu-id="61555-119">String</span><span class="sxs-lookup"><span data-stu-id="61555-119">String</span></span> | <span data-ttu-id="61555-120">**{"removeNamedResources":true}** หรือ **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="61555-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="61555-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="61555-121">SourceProject</span></span>      | <span data-ttu-id="61555-122">การอ้างอิงเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="61555-122">Entity Reference</span></span> | <span data-ttu-id="61555-123">โครงการต้นทาง</span><span class="sxs-lookup"><span data-stu-id="61555-123">Source Project</span></span> |
| <span data-ttu-id="61555-124">เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="61555-124">Target</span></span>             | <span data-ttu-id="61555-125">การอ้างอิงเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="61555-125">Entity Reference</span></span> | <span data-ttu-id="61555-126">โครงการเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="61555-126">Target Project</span></span> |


- <span data-ttu-id="61555-127">**{"clearTeamsAndAssignments":true}** : เป็นลักษณะการทำงานเริ่มต้นสำหรับโครงการสำหรับเว็บและจะลบการมอบหมายงานและสมาชิกในทีมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="61555-127">**{"clearTeamsAndAssignments":true}** : Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="61555-128">**{"removeNamedResources":true}** ลักษณะการทำงานเริ่มต้นสำหรับ Project Operations และจะเปลี่ยนการมอบหมายกลับเป็นทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="61555-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="61555-129">สำหรับค่าเริ่มต้นบนการดำเนินการ ดูที่ [ใช้การดำเนินการ API เว็บ](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="61555-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="61555-130">ระบุช่องที่จะคัดลอก</span><span class="sxs-lookup"><span data-stu-id="61555-130">Specify fields to copy</span></span> 
<span data-ttu-id="61555-131">เมื่อมีการเรียกการดำเนินการ **คัดลอกโครงการ** จะดูมุมมองโครงการ **คัดลอกคอลัมน์โครงการ** เพื่อกำหนดฟิลด์ที่จะคัดลอกเมื่อโครงการถูกคัดลอก</span><span class="sxs-lookup"><span data-stu-id="61555-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
