---
title: สร้างราคาตลาด
description: วิธีการสร้างราคาตลาดใน Project Service
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdd05aea-27a3-431d-9a80-2e220fb25e53
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 756af2fe3bc73d478b0355493aae6f0e49ac5835
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756515"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="6582a-103">สร้างราคาตลาด (Project Service)</span><span class="sxs-lookup"><span data-stu-id="6582a-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="6582a-104">ราคาตลาดกำหนดแม่แบบที่ผู้จัดการฝ่ายบัญชีของคุณสามารถใช้สำหรับการสร้างใบเสนอราคาและโครงการ และสำหรับเชื่อมต่อกับต้นทุนของโครงการ</span><span class="sxs-lookup"><span data-stu-id="6582a-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="6582a-105">ราคาตลาดกำหนดรายการสินค้าของบทบาทและค่าใช้จ่าย และราคาที่คุณจะคิดค่าธรรมเนียมสำหรับแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="6582a-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="6582a-106">คุณสามารถสร้างราคาตลาดมากมาย เพื่อให้คุณสามารถรักษาโครงสร้างราคาแบบแยกสำหรับภูมิภาคต่างๆ ที่คุณขายผลิตภัณฑ์ในช่องทางการขายต่างๆ ได้</span><span class="sxs-lookup"><span data-stu-id="6582a-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="6582a-107">เป็นความคิดที่ดีในการสร้างราคาตลาดอย่างน้อยหนึ่งราคาสำหรับทุกสกุลเงินที่คุณวางแผนที่จะเรียกเก็บเงินจากลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="6582a-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="6582a-108">เมื่อต้องการสร้างการประมาณการด้านการเงินสำหรับงานที่จะส่ง ตรวจสอบให้แน่ใจว่าทุกโครงการมีต้นทุนสำรองและราคาตลาดขาย</span><span class="sxs-lookup"><span data-stu-id="6582a-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="6582a-109">ตั้งค่าทุนเริ่มต้นและรายการราคาขายที่ใช้กับโครงการทั้งหมดที่สร้างขึ้นในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="6582a-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="6582a-110">ราคาตลาดขึ้นอยู่กับบทบาทและประเภทค่าใช้จ่าย ดังนั้น ก่อนที่คุณสร้างราคาตลาด ทำให้แน่ใจว่าคุณได้กำหนดค่าบทบาทและประเภทของค่าใช้จ่ายที่คุณต้องการใช้ในขณะที่สร้างราคาตลาดแล้ว</span><span class="sxs-lookup"><span data-stu-id="6582a-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="6582a-111">ไปที่ **Project Service > ราคาตลาด**</span><span class="sxs-lookup"><span data-stu-id="6582a-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="6582a-112">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6582a-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="6582a-113">ใน **บริบท** เลือกว่าราคาตลาดนี้สำหรับ **ต้นทุน**, **ซื้อ** หรือ **ขาย**</span><span class="sxs-lookup"><span data-stu-id="6582a-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="6582a-114">ใน **ชื่อ** ป้อนชื่อสำหรับราคาตลาด</span><span class="sxs-lookup"><span data-stu-id="6582a-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="6582a-115">ใน **สกุลเงิน** เลือกสกุลเงินที่คุณกำลังจะใช้สำหรับการเรียกเก็บเงิน หรือการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6582a-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="6582a-116">ใน **หน่วยเวลา** ระบุรอบระยะเวลาที่มีใช้ราคา เช่นวันหรือชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="6582a-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="6582a-117">กรอกข้อมูล **วันเริ่ม**, **วันสิ้นสุด** และ **คำอธิบาย** ตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="6582a-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="6582a-118">คลิก **บันทึก** เพื่อสร้างเรกคอร์ดเพื่อที่คุณจะสามารถทำการแก้ไขตอไปได้</span><span class="sxs-lookup"><span data-stu-id="6582a-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="6582a-119">เมื่อต้องการเพิ่มราคาตามบทบาทในราคาตลาด คลิก **+**  ภายใต้ **ราคาตามบทบาท**</span><span class="sxs-lookup"><span data-stu-id="6582a-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="6582a-120">บนบานหน้าต่าง **ราคาตามบทบาท** เติมรายละเอียด แล้วคลิก **บันทึก**.</span><span class="sxs-lookup"><span data-stu-id="6582a-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="6582a-121">การเพิ่มราคาตามบทบาทตามความจำเป็นต่อไป</span><span class="sxs-lookup"><span data-stu-id="6582a-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="6582a-122">เมื่อคุณทำเสร็จแล้ว คลิก **บันทึก** ที่มุมล่างขวาของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="6582a-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="6582a-123">เมื่อต้องการเพิ่มราคาประเภทค่าใช้จ่ายไปยังราคาตลาด คลิก **+** ภายใต้ **ราคาตามประเภท**</span><span class="sxs-lookup"><span data-stu-id="6582a-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="6582a-124">บนบานหน้าต่าง **ราคาตามประเภทของธุรกรรม** เติมรายละเอียด แล้วคลิก **บันทึก**.</span><span class="sxs-lookup"><span data-stu-id="6582a-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="6582a-125">การเพิ่มราคาตามประเภทตามความจำเป็นต่อไป</span><span class="sxs-lookup"><span data-stu-id="6582a-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="6582a-126">เมื่อคุณทำเสร็จแล้ว คลิก **บันทึก** ที่มุมล่างขวาของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="6582a-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="6582a-127">เมื่อต้องการเพิ่มรายการในรายการราคาลงในราคาตลาด คลิก **+** ภายใต้ **รายการในรายการราคา**</span><span class="sxs-lookup"><span data-stu-id="6582a-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="6582a-128">บนบานหน้าต่าง **รายการในรายการราคา** เติมรายละเอียด แล้วคลิก **บันทึก**.</span><span class="sxs-lookup"><span data-stu-id="6582a-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="6582a-129">การเพิ่มรายการในรายการราคาตามความจำเป็นต่อไป</span><span class="sxs-lookup"><span data-stu-id="6582a-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="6582a-130">เมื่อคุณทำเสร็จแล้ว คลิก **บันทึก** ที่มุมล่างขวาของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="6582a-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="6582a-131">เมื่อต้องการเพิ่มความสัมพันธ์ของอาณาเขตในราคาตลาด คลิก **+** ภายใต้ **ความสัมพันธ์ของอาณาเขต**</span><span class="sxs-lookup"><span data-stu-id="6582a-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="6582a-132">บนหน้าต่าง **การเชื่อมต่อใหม่** เติมรายละเอียด แล้วคลิก **บันทึก**.</span><span class="sxs-lookup"><span data-stu-id="6582a-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="6582a-133">ทำการเพิ่มความสัมพันธ์ของอาณาเขตตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="6582a-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="6582a-134">เมื่อคุณทำเสร็จแล้ว คลิก **บันทึก** ที่มุมล่างขวาของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="6582a-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="6582a-135">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6582a-135">See Also</span></span>  
 [<span data-ttu-id="6582a-136">การตั้งค่า Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6582a-136">Configure Project Service Automation</span></span>](../project-service/configure.md)
