---
title: จัดการรายการราคาของโครงการในสัญญาโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการจัดการรายการราคาโครงการในสัญญาโครงการ
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3313eef74b5e7a0624b32d2a336cd986dfdda839
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010404"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="46395-103">จัดการรายการราคาของโครงการในสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="46395-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="46395-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="46395-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="46395-105">สัญญาโครงการใน Dynamics 365 Project Operations ได้รับการออกแบบมาเพื่อสนับสนุนรายการราคาการขายที่มีผลในวันที่หลายรายการในสัญญา</span><span class="sxs-lookup"><span data-stu-id="46395-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="46395-106">ใน Project Operations มีเอนทิตีที่เกี่ยวข้องใหม่ที่เรียกว่า **รายการราคาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="46395-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="46395-107">เอนทิตีนี้มีความสัมพันธ์แบบหนึ่งต่อกลุ่มกับสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="46395-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="46395-108">รายการราคาของโครงการใช้เพื่อกำหนดราคาของธุรกรรมเวลา วัสดุ และค่าใช้จ่ายในโครงการ</span><span class="sxs-lookup"><span data-stu-id="46395-108">Project price lists are used to price time, material, and expense transactions on a project.</span></span> <span data-ttu-id="46395-109">เมื่อสัญญามีรายการราคาของโครงการอย่างน้อยหนึ่งรายการ รายการราคาเหล่านี้จะใช้ในการกำหนดราคาสำหรับประมาณการและข้อมูลจริงของเวลา วัสดุ ค่าใช้จ่ายในโครงการที่เกี่ยวข้องกับสัญญาผ่านรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="46395-109">When a contract has one or more project price lists, these price lists are used to price for time, material, expense estimates, and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="46395-110">เมื่อไม่มีรายการราคาของโครงการในสัญญาโครงการ คุณจะเห็นข้อความเตือนว่าไม่มีรายการราคาของโครงการและประมาณการของคุณ งานโครงการจริง วัสดุ และค่าใช้จ่ายที่บันทึกไว้จะไม่มีราคา</span><span class="sxs-lookup"><span data-stu-id="46395-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, material, and expenses logged will not be priced.</span></span> <span data-ttu-id="46395-111">จะไม่มีราคาสำหรับมูลค่าการขาย</span><span class="sxs-lookup"><span data-stu-id="46395-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="46395-112">เชื่อมโยงหรือยกเลิกการเชื่อมโยงรายการราคาโครงการในสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="46395-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a><span data-ttu-id="46395-113">สร้างหรือเชื่อมโยงรายการราคาเฉพาะสำหรับการประมาณงานตามโครงการ วัสดุ และค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="46395-113">Create or associate a specific price list for estimating project-based work, material, and expenses</span></span>

1. <span data-ttu-id="46395-114">ในสัญญาโครงการ เลือกแท็บ **รายการราคาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="46395-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="46395-115">ในตารางย่อย ให้เลือก **+ เพิ่มรายการราคาโครงการใหม่**</span><span class="sxs-lookup"><span data-stu-id="46395-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="46395-116">บนแถบเลื่อน **สร้างด่วน** เลือกรายการราคา</span><span class="sxs-lookup"><span data-stu-id="46395-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="46395-117">รายการแบบหล่นลงจะแสดงรายการราคาทั้งหมดที่มีบริบทตั้งค่าเป็น **การขาย** โดยที่สกุลเงินในรายการราคาตรงกับสกุลเงินในสัญญา</span><span class="sxs-lookup"><span data-stu-id="46395-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="46395-118">ป้อนคำอธิบายสำหรับการเชื่อมโยงรายการราคาของโครงการ เลือก **บันทึก** แล้วปิดตัวเลื่อน **สร้างด่วน**</span><span class="sxs-lookup"><span data-stu-id="46395-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="46395-119">ระบบจะสร้างการเชื่อมโยงรายการราคาโครงการ</span><span class="sxs-lookup"><span data-stu-id="46395-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="46395-120">ทำซ้ำขั้นตอนที่ 1-4 เพื่อเชื่อมโยงรายการราคาโครงการมากกว่าหนึ่งรายการกับสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="46395-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="46395-121">สร้างรายการราคาของโครงการหลายรายการเท่านั้น หากคุณมีวันที่ที่มีผลบังคับใช้ที่แตกต่างกันในแต่ละรายการราคาของโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="46395-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="46395-122">การดำเนินงานโครงการไม่สนับสนุนการทับซ้อนวันที่มีผลบังคับใช้ของรายการราคาโครงการ</span><span class="sxs-lookup"><span data-stu-id="46395-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="46395-123">หากมีรายการราคาโครงการหลายรายการสำหรับธุรกรรมที่มีวันที่ กำหนดราคาของธุรกรรมนั้นจะถูกตั้งค่าเริ่มต้นเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="46395-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="46395-124">นำการเชื่อมโยงรายการราคาของผลิตภัณฑ์ออก</span><span class="sxs-lookup"><span data-stu-id="46395-124">Remove a project price list association</span></span>

- <span data-ttu-id="46395-125">เลือกรายการราคาของโครงการ จากนั้นเลือก **ลบรายการราคาโครงการตามสัญญา** บนตารางย่อย</span><span class="sxs-lookup"><span data-stu-id="46395-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="46395-126">รายการราคาจะถูกลบออกจากรายการราคาโครงการในสัญญา</span><span class="sxs-lookup"><span data-stu-id="46395-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="46395-127">รายการราคาเองจะไม่ถูกลบ</span><span class="sxs-lookup"><span data-stu-id="46395-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="46395-128">ระบบจะลบเฉพาะการเชื่อมโยงกับสัญญาเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="46395-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="46395-129">ตั้งค่าเริ่มต้นของรายการราคาโครงการโดยอัตโนมัติในสัญญา</span><span class="sxs-lookup"><span data-stu-id="46395-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="46395-130">คุณสามารถตั้งค่ารายการราคาของโครงการเป็นรายการราคาเริ่มต้นของโครงการได้</span><span class="sxs-lookup"><span data-stu-id="46395-130">A project price list can be set up as the default project price list.</span></span> <span data-ttu-id="46395-131">การตั้งค่านี้ช่วยให้มั่นใจได้ว่าสัญญาทั้งหมดในองค์กรของคุณจะเริ่มต้นด้วยรายการราคาของโครงการมาตรฐานสำหรับช่วงราคานั้นเสมอ</span><span class="sxs-lookup"><span data-stu-id="46395-131">This setup ensures that all contracts in your organization always start with a standard project price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="46395-132">ตั้งค่าเริ่มต้นขององค์กรสำหรับรายการราคาโครงการ</span><span class="sxs-lookup"><span data-stu-id="46395-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="46395-133">ไปที่  **การตั้งค่า** > **ทั่วไป** จากนั้นเลือก **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="46395-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="46395-134">ในหน้ารายการ **พารามิเตอร์ที่ใช้งานอยู่** เลือกและดับเบิลคลิกที่บันทึกเพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="46395-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="46395-135">ในขณะที่ดับเบิลคลิก ตรวจสอบให้แน่ใจว่าคุณไม่ได้คลิกค่าฟิลด์ที่เป็นไฮเปอร์ลิงก์</span><span class="sxs-lookup"><span data-stu-id="46395-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="46395-136">บนหน้า **พารามิเตอร์ที่ใช้งานอยู่** เลือกแท็บ **รายการราคา** ตารางย่อยแสดงรายการราคาเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="46395-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="46395-137">นี่คือรายการต้นทุนมาตรฐานและรายการราคาการขาย</span><span class="sxs-lookup"><span data-stu-id="46395-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="46395-138">การมีรายการราคา **การขาย** ที่เชื่อมโยงที่นี่สำหรับทุกสกุลเงินที่คุณขายเพื่อให้แน่ใจว่ารายการราคาการขายเป็นค่าเริ่มต้นของสัญญาใด ๆ ที่คุณสร้างขึ้นสำหรับลูกค้าที่ทำธุรกรรมในสกุลเงินนี้</span><span class="sxs-lookup"><span data-stu-id="46395-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="46395-139">ตั้งค่ารายการราคาของโครงการเฉพาะลูกค้า</span><span class="sxs-lookup"><span data-stu-id="46395-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="46395-140">นอกจากนี้คุณยังสามารถตั้งค่ารายการราคาโครงการเฉพาะสำหรับลูกค้า เมื่อคุณได้เจรจาข้อตกลงการกำหนดราคาหลักกับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="46395-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="46395-141">ไปที่ **การขาย** > **ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="46395-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="46395-142">จากรายการบัญชีที่ใช้งานอยู่ ให้เลือกลูกค้าที่มีรายการราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="46395-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="46395-143">เลือกเรกคอร์ดลูกค้าเพื่อเปิด จากนั้นเลือกแท็บ **รายการราคาโครงการ** ตารางย่อยแสดงรายการราคาโครงการเฉพาะสำหรับลูกค้ารายนี้</span><span class="sxs-lookup"><span data-stu-id="46395-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="46395-144">สร้างการเชื่อมโยงรายการราคาใหม่ที่นี่ เพื่อให้มีรายการราคาเฉพาะสำหรับลูกค้ารายนี้</span><span class="sxs-lookup"><span data-stu-id="46395-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="46395-145">กำหนดราคาตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="46395-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="46395-146">หลังจากที่คุณมีรายการราคาเริ่มต้นของโครงการสำหรับองค์กรและลูกค้าโดยเฉพาะแล้ว สัญญาโครงการของคุณจะถูกสร้างขึ้นพร้อมกับการเชื่อมโยงรายการราคาของโครงการโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="46395-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="46395-147">อย่างไรก็ตาม รายการราคาโครงการในสัญญาโครงการจะถูกคัดลอกโดยมีวันที่และชื่อสัญญาต่อท้ายเสมอ</span><span class="sxs-lookup"><span data-stu-id="46395-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="46395-148">จากนั้นผู้จัดการบัญชีและโครงการจะเริ่มแก้ไขราคาในสำเนาเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="46395-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="46395-149">ราคาที่เปลี่ยนแปลงเหล่านี้จะใช้ได้กับสัญญาโครงการนี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="46395-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
