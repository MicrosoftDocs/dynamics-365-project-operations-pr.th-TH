---
title: จัดการรายการราคาของโครงการในสัญญาโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการจัดการราคาตลาดโครงการในสัญญาโครงการ
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 030684576e1f53d27921907b07c9e5e0c5efe612
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133460"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="99031-103">จัดการรายการราคาของโครงการในสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="99031-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="99031-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="99031-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="99031-105">สัญญาโครงการใน Dynamics 365 Project Operations ได้รับการออกแบบมาเพื่อสนับสนุนราคาตลาดการขายที่มีผลในวันที่หลายรายการในสัญญา</span><span class="sxs-lookup"><span data-stu-id="99031-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="99031-106">ใน Project Operations มีเอนทิตีที่เกี่ยวข้องใหม่ที่เรียกว่า **ราคาตลาดโครงการ**</span><span class="sxs-lookup"><span data-stu-id="99031-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="99031-107">เอนทิตีนี้มีความสัมพันธ์แบบหนึ่งต่อกลุ่มกับสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="99031-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="99031-108">รายการราคาโครงการใช้เพื่อกำหนดราคาธุรกรรมเวลาและมค่าใช้จ่ายในโครงการ</span><span class="sxs-lookup"><span data-stu-id="99031-108">Project price lists are used to price time and expense transactions on a project.</span></span> <span data-ttu-id="99031-109">เมื่อสัญญามีราคาตลาดของโครงการอย่างน้อยหนึ่งรายการ ราคาตลาดเหล่านี้จะใช้ในการกำหนดราคาสำหรับเวลาและค่าใช้จ่ายโดยประมาณและตามความเป็นจริงของโครงการที่เกี่ยวข้องกับสัญญาผ่านทางรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="99031-109">When a contract has one or more project price lists, these price lists are used to price for time and expense estimates and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="99031-110">เมื่อไม่มีราคาตลาดโครงการในสัญญาโครงการ คุณจะเห็นข้อความเตือนว่าไม่มีราคาตลาดโครงการ และจะไม่มีการกำหนดราคาประมาณการ งานโครงการจริง และค่าใช้จ่ายของคุณ</span><span class="sxs-lookup"><span data-stu-id="99031-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, and expenses will not be priced.</span></span> <span data-ttu-id="99031-111">จะไม่มีราคาสำหรับมูลค่าการขาย</span><span class="sxs-lookup"><span data-stu-id="99031-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="99031-112">เชื่อมโยงหรือยกเลิกการเชื่อมโยงราคาตลาดโครงการในสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="99031-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a><span data-ttu-id="99031-113">สร้างหรือเชื่อมโยงราคาตลาดเฉพาะสำหรับการประมาณงานและค่าใช้จ่ายตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="99031-113">Create or associate a specific price list for estimating project-based work and expenses</span></span>

1. <span data-ttu-id="99031-114">ในสัญญาโครงการ เลือกแท็บ **ราคาตลาดโครงการ**</span><span class="sxs-lookup"><span data-stu-id="99031-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="99031-115">ในตารางย่อย ให้เลือก **+ เพิ่มราคาตลาดโครงการใหม่**</span><span class="sxs-lookup"><span data-stu-id="99031-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="99031-116">บนแถบเลื่อน **สร้างด่วน** เลือกราคาตลาด</span><span class="sxs-lookup"><span data-stu-id="99031-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="99031-117">รายการแบบหล่นลงจะแสดงราคาตลาดทั้งหมดที่มีบริบทตั้งค่าเป็น **การขาย** โดยที่สกุลเงินในราคาตลาดตรงกับสกุลเงินในสัญญา</span><span class="sxs-lookup"><span data-stu-id="99031-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="99031-118">ป้อนคำอธิบายสำหรับการเชื่อมโยงราคาตลาดของโครงการ เลือก **บันทึก** แล้วปิดตัวเลื่อน **สร้างด่วน**</span><span class="sxs-lookup"><span data-stu-id="99031-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="99031-119">ระบบจะสร้างการเชื่อมโยงรายการราคาโครงการ</span><span class="sxs-lookup"><span data-stu-id="99031-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="99031-120">ทำซ้ำขั้นตอนที่ 1-4 เพื่อเชื่อมโยงราคาตลาดโครงการมากกว่าหนึ่งรายการกับสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="99031-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="99031-121">สร้างราคาตลาดของโครงการหลายรายการเท่านั้น หากคุณมีวันที่ที่มีผลบังคับใช้ที่แตกต่างกันในแต่ละราคาตลาดของโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="99031-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="99031-122">การดำเนินงานโครงการไม่สนับสนุนการทับซ้อนวันที่มีผลบังคับใช้ของราคาตลาดโครงการ</span><span class="sxs-lookup"><span data-stu-id="99031-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="99031-123">หากมีราคาตลาดโครงการหลายรายการสำหรับธุรกรรมที่มีวันที่ กำหนดราคาของธุรกรรมนั้นจะถูกตั้งค่าเริ่มต้นเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="99031-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="99031-124">นำการเชื่อมโยงราคาตลาดของผลิตภัณฑ์ออก</span><span class="sxs-lookup"><span data-stu-id="99031-124">Remove a project price list association</span></span>

- <span data-ttu-id="99031-125">เลือกราคาตลาดของโครงการ จากนั้นเลือก **ลบราคาตลาดโครงการตามสัญญา** บนตารางย่อย</span><span class="sxs-lookup"><span data-stu-id="99031-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="99031-126">ราคาตลาดจะถูกลบออกจากราคาตลาดโครงการในสัญญา</span><span class="sxs-lookup"><span data-stu-id="99031-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="99031-127">ราคาตลาดเองจะไม่ถูกลบ</span><span class="sxs-lookup"><span data-stu-id="99031-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="99031-128">ระบบจะลบเฉพาะการเชื่อมโยงกับสัญญาเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="99031-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="99031-129">ตั้งค่าเริ่มต้นของราคาตลาดโครงการโดยอัตโนมัติในสัญญา</span><span class="sxs-lookup"><span data-stu-id="99031-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="99031-130">ราคาตลาดโครงการสามารถตั้งเป็นรายการเริ่มต้นในสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="99031-130">A project price list can be set up as the default list on a project contract.</span></span> <span data-ttu-id="99031-131">การตั้งค่านี้สามารถช่วยให้มั่นใจได้ว่าสัญญาทั้งหมดในองค์กรของคุณจะเริ่มต้นด้วยราคาตลาดมาตรฐานสำหรับช่วงราคานั้นเสมอ</span><span class="sxs-lookup"><span data-stu-id="99031-131">This setup can help ensure that all contracts in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="99031-132">ตั้งค่าเริ่มต้นขององค์กรสำหรับราคาตลาดโครงการ</span><span class="sxs-lookup"><span data-stu-id="99031-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="99031-133">ไปที่  **การตั้งค่า** > **ทั่วไป** จากนั้นเลือก **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="99031-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="99031-134">ในหน้ารายการ **พารามิเตอร์ที่ใช้งานอยู่** เลือกและดับเบิลคลิกที่บันทึกเพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="99031-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="99031-135">ในขณะที่ดับเบิลคลิก ตรวจสอบให้แน่ใจว่าคุณไม่ได้คลิกค่าฟิลด์ที่เป็นไฮเปอร์ลิงก์</span><span class="sxs-lookup"><span data-stu-id="99031-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="99031-136">บนหน้า **พารามิเตอร์ที่ใช้งานอยู่** เลือกแท็บ **ราคาตลาด** ตารางย่อยแสดงราคาตลาดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="99031-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="99031-137">นี่คือรายการต้นทุนมาตรฐานและราคาตลาดการขาย</span><span class="sxs-lookup"><span data-stu-id="99031-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="99031-138">การมีราคาตลาด **การขาย** ที่เชื่อมโยงที่นี่สำหรับทุกสกุลเงินที่คุณขายเพื่อให้แน่ใจว่าราคาตลาดการขายเป็นค่าเริ่มต้นของสัญญาใด ๆ ที่คุณสร้างขึ้นสำหรับลูกค้าที่ทำธุรกรรมในสกุลเงินนี้</span><span class="sxs-lookup"><span data-stu-id="99031-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="99031-139">ตั้งค่าราคาตลาดของโครงการเฉพาะลูกค้า</span><span class="sxs-lookup"><span data-stu-id="99031-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="99031-140">นอกจากนี้คุณยังสามารถตั้งค่าราคาตลาดโครงการเฉพาะสำหรับลูกค้า เมื่อคุณได้เจรจาข้อตกลงการกำหนดราคาหลักกับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="99031-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="99031-141">ไปที่ **การขาย** > **ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="99031-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="99031-142">จากรายการบัญชีที่ใช้งานอยู่ ให้เลือกลูกค้าที่มีราคาตลาดพิเศษ</span><span class="sxs-lookup"><span data-stu-id="99031-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="99031-143">เลือกเรกคอร์ดลูกค้าเพื่อเปิด จากนั้นเลือกแท็บ **ราคาตลาดโครงการ** ตารางย่อยแสดงราคาตลาดโครงการเฉพาะสำหรับลูกค้ารายนี้</span><span class="sxs-lookup"><span data-stu-id="99031-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="99031-144">สร้างการเชื่อมโยงราคาตลาดใหม่ที่นี่ เพื่อให้มีราคาตลาดเฉพาะสำหรับลูกค้ารายนี้</span><span class="sxs-lookup"><span data-stu-id="99031-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="99031-145">กำหนดราคาตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="99031-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="99031-146">หลังจากที่คุณมีราคาตลาดเริ่มต้นของโครงการสำหรับองค์กรและลูกค้าโดยเฉพาะแล้ว สัญญาโครงการของคุณจะถูกสร้างขึ้นพร้อมกับการเชื่อมโยงราคาตลาดของโครงการโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="99031-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="99031-147">อย่างไรก็ตาม ราคาตลาดโครงการในสัญญาโครงการจะถูกคัดลอกโดยมีวันที่และชื่อสัญญาต่อท้ายเสมอ</span><span class="sxs-lookup"><span data-stu-id="99031-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="99031-148">จากนั้นผู้จัดการบัญชีและโครงการจะเริ่มแก้ไขราคาในสำเนาเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="99031-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="99031-149">ราคาที่เปลี่ยนแปลงเหล่านี้จะใช้ได้กับสัญญาโครงการนี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="99031-149">These changed prices will be applicable to this project contract only.</span></span>
