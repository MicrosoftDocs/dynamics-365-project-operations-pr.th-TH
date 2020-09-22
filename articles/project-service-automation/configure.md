---
title: การกำหนดค่า Project Service Automation
description: ขั้นตอนสำหรับการตั้งค่าคอนฟิก Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756409"
---
# <a name="configure-project-service"></a><span data-ttu-id="64dca-103">ตั้งค่าคอนฟิก Project Service</span><span class="sxs-lookup"><span data-stu-id="64dca-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="64dca-104">ก่อนที่คุณจะสามารถใช้ความสามารถอัตโนมัติของ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ใน [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] เพื่อจัดการบัญชี โครงการ และทรัพยากรของคุณ คุณจำเป็นต้องทำขั้นตอนการกำหนดค่าบางอย่างให้เสร็จสมบูรณ์ เพื่อให้แน่ใจว่าโซลูชัน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ตรงกับความต้องการขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="64dca-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="64dca-105">ขั้นตอนเหล่านี้รวมถึง:</span><span class="sxs-lookup"><span data-stu-id="64dca-105">These steps include:</span></span>  
  
-   <span data-ttu-id="64dca-106">[ตั้งค่าหน่วยเวลา](../project-service/set-up-time-units.md)</span><span class="sxs-lookup"><span data-stu-id="64dca-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="64dca-107">การกำหนดค่าหน่วยเวลาในแค็ตตาล็อกผลิตภัณฑ์ที่คุณจะใช้เป็นฐานสำหรับการจัดกำหนดการและการเรียกเก็บเงินโครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="64dca-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="64dca-108">[ตั้งค่าสกุลเงินและอัตราแลกเปลี่ยน](../project-service/set-up-currencies-exchange-rates.md)</span><span class="sxs-lookup"><span data-stu-id="64dca-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="64dca-109">ตั้งค่าสกุลเงินที่จะใช้สำหรับโครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="64dca-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="64dca-110">[สร้างหน่วยองค์กร](../project-service/create-organizational-units.md)</span><span class="sxs-lookup"><span data-stu-id="64dca-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="64dca-111">ตั้งค่ากลุ่มที่บริษัทของคุณใช้เพื่อแบ่งธุรกิจ ไม่ว่าจะโดยภูมิศาสตร์ ฟังก์ชันธุรกิจ หรือฝ่ายตรรกะอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="64dca-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="64dca-112">[ตั้งค่าความถี่ของใบแจ้งหนี้](../project-service/set-up-invoice-frequencies.md)</span><span class="sxs-lookup"><span data-stu-id="64dca-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="64dca-113">ตั้งค่าระยะเวลาที่คุณต้องการใช้สำหรับการเรียกเก็บเงินไคลเอ็นต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="64dca-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="64dca-114">[กำหนดค่าประเภทธุรกรรม](../project-service/configure-transaction-categories.md)</span><span class="sxs-lookup"><span data-stu-id="64dca-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="64dca-115">ตั้งค่าประเภทธุรกรรมเพื่อที่ปรึกษาของคุณจะสามารถเรียกเก็บค่าธรรมเนียมที่สามารถเรียกเก็บเงินได้และค่าใช้จ่ายที่ยังไม่ได้เรียกเก็บ</span><span class="sxs-lookup"><span data-stu-id="64dca-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="64dca-116">[กำหนดค่าประเภทค่าใช้จ่าย](../project-service/configure-expense-categories.md)</span><span class="sxs-lookup"><span data-stu-id="64dca-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="64dca-117">ตั้งค่าประเภทที่ปรึกษาของคุณจะสามารถเรียกเก็บค่าธรรมเนียมที่สามารถเรียกเก็บเงินได้และค่าใช้จ่ายที่ยังไม่ได้เรียกเก็บ</span><span class="sxs-lookup"><span data-stu-id="64dca-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="64dca-118">[การสร้างสินค้าแค็ตตาล็อกผลิตภัณฑ์](../project-service/create-product-catalog-items.md)</span><span class="sxs-lookup"><span data-stu-id="64dca-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="64dca-119">เพิ่มผลิตภัณฑ์ที่คุณขาย เช่น สิทธิ์การใช้งานซอฟต์แวร์ ไปยังแค็ตตาล็อกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="64dca-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="64dca-120">[สร้างราคาตลาด](../project-service/create-price-list.md)</span><span class="sxs-lookup"><span data-stu-id="64dca-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="64dca-121">กำหนดค่ารายการราคาที่แตกต่างกัน ขึ้นอยู่กับจำนวนที่คุณต้องการเรียกเก็บจากไคลเอนต์ของคุณสำหรับแต่ละบทบาทโครงการที่จำเป็นของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="64dca-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="64dca-122">[ตั้งค่าทรัพยากร](../project-service/set-up-resources.md)</span><span class="sxs-lookup"><span data-stu-id="64dca-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="64dca-123">เพิ่มทักษะ ความชำนาญ บทบาทของทรัพยากร และข้อมูลทรัพยากรอื่นๆ ที่คุณต้องมีสำหรับโครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="64dca-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="64dca-124">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="64dca-124">See Also</span></span>  
 <span data-ttu-id="64dca-125">[ภาพรวมของ Project Service Automation](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="64dca-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="64dca-126">[การกำหนดค่า Project Service Automation](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="64dca-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="64dca-127">[คำแนะนำผู้จัดการลูกค้าองค์กร](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="64dca-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="64dca-128">[คำแนะนำของผู้จัดการโครงการ](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="64dca-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="64dca-129">[คำแนะนำของผู้จัดการทรัพยากร](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="64dca-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="64dca-130">เวลา ค่าใช้จ่าย และคำแนะนำในการทำงานร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="64dca-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
