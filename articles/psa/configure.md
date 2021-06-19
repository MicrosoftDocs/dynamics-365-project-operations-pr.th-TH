---
title: การกำหนดค่า Project Service Automation
description: ขั้นตอนสำหรับการตั้งค่าคอนฟิก Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: ef1724bb92e62ae21472e133fff0978c4faeeffa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002875"
---
# <a name="configure-project-service"></a><span data-ttu-id="60d7f-103">ตั้งค่าคอนฟิก Project Service</span><span class="sxs-lookup"><span data-stu-id="60d7f-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="60d7f-104">ก่อนที่คุณจะสามารถใช้ความสามารถอัตโนมัติของ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ใน [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] เพื่อจัดการบัญชี โครงการ และทรัพยากรของคุณ คุณจำเป็นต้องทำขั้นตอนการกำหนดค่าบางอย่างให้เสร็จสมบูรณ์ เพื่อให้แน่ใจว่าโซลูชัน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ตรงกับความต้องการขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="60d7f-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="60d7f-105">ขั้นตอนเหล่านี้รวมถึง:</span><span class="sxs-lookup"><span data-stu-id="60d7f-105">These steps include:</span></span>  
  
-   <span data-ttu-id="60d7f-106">[ตั้งค่าหน่วยเวลา](../psa/set-up-time-units.md)</span><span class="sxs-lookup"><span data-stu-id="60d7f-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="60d7f-107">การกำหนดค่าหน่วยเวลาในแค็ตตาล็อกผลิตภัณฑ์ที่คุณจะใช้เป็นฐานสำหรับการจัดกำหนดการและการเรียกเก็บเงินโครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="60d7f-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="60d7f-108">[ตั้งค่าสกุลเงินและอัตราแลกเปลี่ยน](../psa/set-up-currencies-exchange-rates.md)</span><span class="sxs-lookup"><span data-stu-id="60d7f-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="60d7f-109">ตั้งค่าสกุลเงินที่จะใช้สำหรับโครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="60d7f-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="60d7f-110">[สร้างหน่วยองค์กร](../psa/create-organizational-units.md)</span><span class="sxs-lookup"><span data-stu-id="60d7f-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="60d7f-111">ตั้งค่ากลุ่มที่บริษัทของคุณใช้เพื่อแบ่งธุรกิจ ไม่ว่าจะโดยภูมิศาสตร์ ฟังก์ชันธุรกิจ หรือฝ่ายตรรกะอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="60d7f-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="60d7f-112">[ตั้งค่าความถี่ของใบแจ้งหนี้](../psa/set-up-invoice-frequencies.md)</span><span class="sxs-lookup"><span data-stu-id="60d7f-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="60d7f-113">ตั้งค่าระยะเวลาที่คุณต้องการใช้สำหรับการเรียกเก็บเงินไคลเอ็นต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="60d7f-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="60d7f-114">[กำหนดค่าประเภทธุรกรรม](../psa/configure-transaction-categories.md)</span><span class="sxs-lookup"><span data-stu-id="60d7f-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="60d7f-115">ตั้งค่าประเภทธุรกรรมเพื่อที่ปรึกษาของคุณจะสามารถเรียกเก็บค่าธรรมเนียมที่สามารถเรียกเก็บเงินได้และค่าใช้จ่ายที่ยังไม่ได้เรียกเก็บ</span><span class="sxs-lookup"><span data-stu-id="60d7f-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="60d7f-116">[กำหนดค่าประเภทค่าใช้จ่าย](../psa/configure-expense-categories.md)</span><span class="sxs-lookup"><span data-stu-id="60d7f-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="60d7f-117">ตั้งค่าประเภทที่ปรึกษาของคุณจะสามารถเรียกเก็บค่าธรรมเนียมที่สามารถเรียกเก็บเงินได้และค่าใช้จ่ายที่ยังไม่ได้เรียกเก็บ</span><span class="sxs-lookup"><span data-stu-id="60d7f-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="60d7f-118">[การสร้างสินค้าแค็ตตาล็อกผลิตภัณฑ์](../psa/create-product-catalog-items.md)</span><span class="sxs-lookup"><span data-stu-id="60d7f-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="60d7f-119">เพิ่มผลิตภัณฑ์ที่คุณขาย เช่น สิทธิ์การใช้งานซอฟต์แวร์ ไปยังแค็ตตาล็อกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="60d7f-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="60d7f-120">[สร้างรายการราคา](../psa/create-price-list.md)</span><span class="sxs-lookup"><span data-stu-id="60d7f-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="60d7f-121">กำหนดค่ารายการราคาที่แตกต่างกัน ขึ้นอยู่กับจำนวนที่คุณต้องการเรียกเก็บจากไคลเอนต์ของคุณสำหรับแต่ละบทบาทโครงการที่จำเป็นของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="60d7f-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="60d7f-122">[ตั้งค่าทรัพยากร](../psa/set-up-resources.md)</span><span class="sxs-lookup"><span data-stu-id="60d7f-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="60d7f-123">เพิ่มทักษะ ความชำนาญ บทบาทของทรัพยากร และข้อมูลทรัพยากรอื่นๆ ที่คุณต้องมีสำหรับโครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="60d7f-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="60d7f-124">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="60d7f-124">See Also</span></span>  
 <span data-ttu-id="60d7f-125">[ภาพรวมของ Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="60d7f-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="60d7f-126">[การกำหนดค่า Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="60d7f-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="60d7f-127">[คำแนะนำผู้จัดการลูกค้าองค์กร](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="60d7f-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="60d7f-128">[คำแนะนำของผู้จัดการโครงการ](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="60d7f-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="60d7f-129">[คำแนะนำของผู้จัดการทรัพยากร](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="60d7f-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="60d7f-130">เวลา ค่าใช้จ่าย และคำแนะนำในการทำงานร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="60d7f-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]