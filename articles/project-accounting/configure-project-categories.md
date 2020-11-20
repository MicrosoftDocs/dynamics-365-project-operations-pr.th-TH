---
title: กำหนดค่าประเภทโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการตั้งค่าประเภทต่างๆ ของโครงการ
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131951"
---
# <a name="configure-project-categories"></a><span data-ttu-id="daa86-103">กำหนดค่าประเภทโครงการ</span><span class="sxs-lookup"><span data-stu-id="daa86-103">Configure project categories</span></span>

<span data-ttu-id="daa86-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="daa86-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="daa86-105">Project Operations นำเสนอความสามารถที่ยอดเยี่ยมสำหรับการจัดประเภทรายได้และค่าใช้จ่ายในโครงการ</span><span class="sxs-lookup"><span data-stu-id="daa86-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="daa86-106">ประเภทให้ความสามารถในการรายงานและวิเคราะห์ธุรกรรมโครงการและส่งเสริมการลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="daa86-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="daa86-107">แผนภาพต่อไปนี้แสดงให้เห็นถึงความสัมพันธ์ระหว่างประเภทธุรกรรม ประเภทที่ใช้ร่วมกัน และประเภทของโครงการ</span><span class="sxs-lookup"><span data-stu-id="daa86-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="daa86-108">ประเภทธุรกรรมเป็นการจัดกลุ่มเบื้องต้นสำหรับธุรกรรมโครงการ</span><span class="sxs-lookup"><span data-stu-id="daa86-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="daa86-109">ภายในการจัดกลุ่มนั้น มีชุดของประเภทที่ใช้ร่วมกันซึ่งสามารถใช้ร่วมกันระหว่างแอปพลิเคชันและโมดูลต่างๆ</span><span class="sxs-lookup"><span data-stu-id="daa86-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="daa86-110">ประเภทของโครงการเป็นระดับที่ละเอียดที่สุดของประเภทเพื่อให้ข้อมูลที่เฉพาะเจาะจงมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="daa86-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="daa86-111">ประเภทของโครงการมีเฉพาะสำหรับนิติบุคคล โมดูล และแอปพลิเคชันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="daa86-111">Project categories are specific to legal entity, module, and application.</span></span>

![ความสัมพันธ์ระหว่างประเภทธุรกรรม ประเภทที่ใช้ร่วมกัน และประเภทของโครงการ](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="daa86-113">ประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="daa86-113">Transaction categories</span></span>

<span data-ttu-id="daa86-114">ประเภทธุรกรรมแสดงถึงการจัดกลุ่มเบื้องต้นสำหรับธุรกรรมโครงการและไม่ใช่ประเภทเฉพาะบริษัทหรือเฉพาะชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="daa86-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="daa86-115">ตัวอย่างเช่น Contoso Robotics ใช้ประเภทธุรกรรมการออกแบบ การเดินทาง การติดตั้ง และบริการเพื่อจัดกลุ่มธุรกรรมโครงการ</span><span class="sxs-lookup"><span data-stu-id="daa86-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="daa86-116">ประเภทธุรกรรมมีการกำหนดไว้ในโมดูล Project Operations</span><span class="sxs-lookup"><span data-stu-id="daa86-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="daa86-117">ไปที่ **การตั้งค่า** \> **ประเภทธุรกรรม** เพื่อเปิดฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="daa86-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="daa86-118">สร้างประเภทธุรกรรมใหม่โดยการเลือก **ใหม่** หรือโดยการเลือก **นำเข้าจาก Excel**</span><span class="sxs-lookup"><span data-stu-id="daa86-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="daa86-119">ประเภทที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="daa86-119">Shared categories</span></span>

<span data-ttu-id="daa86-120">Dynamics 365 ใช้แนวคิดประเภทที่ใช้ร่วมกันเพื่อจัดประเภทค่าใช้จ่ายในแอปพลิเคชันต่างๆ เช่น Dynamics 365 Finance, Dynamics 365 Supply Chain และ Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="daa86-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="daa86-121">สำหรับประเภทธุรกรรมแต่ละรายการที่สร้างขึ้น Project Operations จะสร้างประเภทที่ใช้ร่วมกันที่เกี่ยวข้องสี่ประเภทโดยอัตโนมัติ ได้แก่ ชั่วโมง ค่าใช้จ่าย ค่าธรรมเนียม และสินค้า</span><span class="sxs-lookup"><span data-stu-id="daa86-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="daa86-122">คุณสามารถตรวจสอบและปรับปรุงประเภทที่ใช้ร่วมกันได้โดยไปที่ **การจัดการและการบัญชีโครงการ** \> **ตั้งค่า** \> **ประเภท** \> **ประเภทที่ใช้ร่วมกัน**</span><span class="sxs-lookup"><span data-stu-id="daa86-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="daa86-123">ประเภทโครงการ</span><span class="sxs-lookup"><span data-stu-id="daa86-123">Project categories</span></span>

<span data-ttu-id="daa86-124">ประเภทของโครงการแสดงถึงการกำหนดค่าประเภทในระดับที่ละเอียดที่สุด และต้องกำหนดค่าแยกกัน และสำหรับแต่ละบริษัทโดยนักบัญชีของโครงการ</span><span class="sxs-lookup"><span data-stu-id="daa86-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="daa86-125">ไปที่ **การจัดการและการบัญชีโครงการ** \> **ตั้งค่า** \> **ประเภท** \> **ประเภทของโครงการ**</span><span class="sxs-lookup"><span data-stu-id="daa86-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="daa86-126">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="daa86-126">Select **New**.</span></span>
3. <span data-ttu-id="daa86-127">เลือก **รหัสประเภท** ของประเภทที่ใช้ร่วมกันที่คุณสร้างไว้ในส่วนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="daa86-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="daa86-128">Project Operations อนุญาตให้ใช้เฉพาะประเภทที่ใช้ร่วมกันที่เชื่อมโยงกับประเภทธุรกรรมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="daa86-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="daa86-129">เลือกกลุ่มประเภท</span><span class="sxs-lookup"><span data-stu-id="daa86-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="daa86-130">กลุ่มประเภท</span><span class="sxs-lookup"><span data-stu-id="daa86-130">Category groups</span></span>

<span data-ttu-id="daa86-131">กลุ่มประเภทใช้เพื่อใช้คุณสมบัติร่วมกัน โดยส่วนใหญ่จะเป็นโปรไฟล์การลงรายการบัญชีระหว่างประเภทของโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="daa86-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="daa86-132">โดยต้องมีกลุ่มประเภทอย่างน้อยหนึ่งกลุ่มสำหรับแต่ละชนิดธุรกรรมและแต่ละประเภทโครงการกำหนดให้กลุ่ม</span><span class="sxs-lookup"><span data-stu-id="daa86-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="daa86-133">ข้อกำหนดเฉพาะการลงรายการบัญชีใน Project Operations มีการกำหนดโดยกฎต้นทุนโครงการและโปรไฟล์รายได้ ประเภทของโครงการ และกลุ่มประเภท</span><span class="sxs-lookup"><span data-stu-id="daa86-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="daa86-134">คุณสามารถตั้งค่ากลุ่มประเภทได้โดยไปที่ **การจัดการและการบัญชีโครงการ** \> **ตั้งค่า** \> **ประเภท** \> **กลุ่มประเภท**</span><span class="sxs-lookup"><span data-stu-id="daa86-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
