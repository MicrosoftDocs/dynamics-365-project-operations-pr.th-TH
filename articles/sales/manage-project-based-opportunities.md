---
title: จัดการโอกาสทางการขายตามโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการทำงานกับโอกาสทางการขายที่เกี่ยวข้องกับโครงการ
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5a8bfea5540432a62d7075443cf237571bfa4de
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118496"
---
# <a name="manage-project-based-opportunities"></a><span data-ttu-id="d285c-103">จัดการโอกาสทางการขายตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="d285c-103">Manage project-based opportunities</span></span>

<span data-ttu-id="d285c-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="d285c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d285c-105">โดยทั่วไปบริษัทตามโครงการจะมีการดำเนินงานในการจัดส่งสินค้ากระจายอยู่ในหลายประเทศและภูมิภาคต่างๆ</span><span class="sxs-lookup"><span data-stu-id="d285c-105">Project-based companies typically have their operations for delivery spread across multiple countries and geographies.</span></span> <span data-ttu-id="d285c-106">ค่าใช้จ่ายในการดำเนินโครงการและการส่งมอบอาจแตกต่างกันไปขึ้นอยู่กับพื้นที่ทางภูมิศาสตร์หรือแผนกที่จัดการการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="d285c-106">The cost of the project execution and delivery can vary  based on which geography or division manages the delivery.</span></span> <span data-ttu-id="d285c-107">ซึ่งอาจส่งผลต่อระยะขอบของดีลได้</span><span class="sxs-lookup"><span data-stu-id="d285c-107">In turn, this can impact the margins of the deal.</span></span> <span data-ttu-id="d285c-108">การนำส่งบริการตามโครงการมักเกี่ยวข้องกับเวลาทรัพยากรบุคคลจำนวนมาก ค่าใช้จ่ายจำนวนมากสำหรับการเดินทาง ค่าวัสดุ และค่าใช้จ่ายอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="d285c-108">Delivery of project-based services typically involves large quantities of human resource time, considerable expenses for travel, material costs, and other expenses.</span></span>

<span data-ttu-id="d285c-109">โอกาสทางการขายตามโครงการใน Dynamics 365 Project Operations ออกแบบมาพร้อมส่วนขยายให้ Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="d285c-109">Project-based opportunities in Dynamics 365 Project Operations are designed with extensions to Dynamics 365 Sales.</span></span> <span data-ttu-id="d285c-110">หัวข้อให้รายละเอียดเกี่ยวกับฟิลด์ต่างๆ และตรรกะทางธุรกิจที่รวมอยู่ในฟังก์ชันเพิ่มเติมที่บริษัทตามโครงการต้องการในการจัดการโอกาสทางการขายตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="d285c-110">The topic provides details about the different fields and business logic included in the additional functionality that is required by project-based companies to manage project-based opportunities.</span></span>

## <a name="view-all-project-based-opportunities"></a><span data-ttu-id="d285c-111">ดูโอกาสทางการขายตามโครงการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d285c-111">View all project-based opportunities</span></span>

<span data-ttu-id="d285c-112">รายการโอกาสทางการขายตามโครงการทั้งหมดสามารถดูได้จากหน้ารายการ **โอกาสทางการขาย**</span><span class="sxs-lookup"><span data-stu-id="d285c-112">A list of all the project-based opportunities can be seen from the **Opportunity** list page.</span></span> 

1. <span data-ttu-id="d285c-113">ไปที่ **การขาย** > **โอกาสทางการขาย**</span><span class="sxs-lookup"><span data-stu-id="d285c-113">Go to **Sales** > **Opportunities**.</span></span>
2. <span data-ttu-id="d285c-114">ใช้ **ดูตัวสลับ** เพื่อเลือกมุมมองที่กรองอื่น ๆ ของโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="d285c-114">Use the **View switcher** to select other filtered views of the opportunities.</span></span> <span data-ttu-id="d285c-115">คุณสามารถสร้างมุมมองของคุณเองด้วยเกณฑ์ตัวกรองที่กำหนดเอง เพื่อกำหนดค่าตัวเลือกมุมมองและการนำทางเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="d285c-115">You can create your own views with custom filter criteria to configure these views and navigation options.</span></span>

<span data-ttu-id="d285c-116">โอกาสทางการขายของโครงการสามารถสร้างหรือลบออกจากหน้ารายการนี้หรือหน้ารายละเอียด</span><span class="sxs-lookup"><span data-stu-id="d285c-116">Project Opportunities can be created or deleted from this list page or the detail page.</span></span>

## <a name="business-process-flow-for-project-based-deals"></a><span data-ttu-id="d285c-117">โฟลว์กระบวนการธุรกิจสำหรับข้อตกลงตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="d285c-117">Business process flow for project-based deals</span></span>

<span data-ttu-id="d285c-118">โฟลว์กระบวนการธุรกิจต่อไปนี้ได้รับการสนับสนุนสำหรับข้อตกลงตามโครงการใน Project Operations:</span><span class="sxs-lookup"><span data-stu-id="d285c-118">The following business process flows are supported for project-based deals in Project Operations:</span></span>

- <span data-ttu-id="d285c-119">กระบวนการธุรกิจของลูกค้าเป้าหมายถึงโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="d285c-119">Lead to Opportunity business process</span></span>
- <span data-ttu-id="d285c-120">กระบวนการขายของโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="d285c-120">Opportunity sales process</span></span>

### <a name="lead-to-opportunity-business-process"></a><span data-ttu-id="d285c-121">กระบวนการธุรกิจของลูกค้าเป้าหมายถึงโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="d285c-121">Lead to opportunity business process</span></span> 
<span data-ttu-id="d285c-122">กระบวนการธุรกิจของลูกค้าเป้าหมายถึงโอกาสทางการขายสนับสนุนลำดับขั้นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d285c-122">The lead to opportunity business process supports the following stages:</span></span>

| <span data-ttu-id="d285c-123">ขั้น</span><span class="sxs-lookup"><span data-stu-id="d285c-123">Stage</span></span> | <span data-ttu-id="d285c-124">เอนทิตีที่แม็ป</span><span class="sxs-lookup"><span data-stu-id="d285c-124">Mapped entity</span></span> | <span data-ttu-id="d285c-125">ฟังก์ชันการทำงาน</span><span class="sxs-lookup"><span data-stu-id="d285c-125">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d285c-126">เข้าเกณฑ์</span><span class="sxs-lookup"><span data-stu-id="d285c-126">Qualify</span></span> | <span data-ttu-id="d285c-127">ลูกค้าเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="d285c-127">Lead</span></span> | <span data-ttu-id="d285c-128">รับรองลูกค้าเป้าหมายเพื่อสร้างบัญชี ผู้ติดต่อ และโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="d285c-128">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="d285c-129">จัดทำ</span><span class="sxs-lookup"><span data-stu-id="d285c-129">Develop</span></span> | <span data-ttu-id="d285c-130">โอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="d285c-130">Opportunity</span></span> | <span data-ttu-id="d285c-131">พัฒนาโอกาสทางการขายเพื่อเพิ่มข้อมูลเพิ่มเติมเกี่ยวกับงานที่เกี่ยวข้อง ผู้มีส่วนได้ส่วนเสียหลัก และการแข่งขัน</span><span class="sxs-lookup"><span data-stu-id="d285c-131">Develop the opportunity to add more information on the work involved, key stakeholders, and competition.</span></span> |
| <span data-ttu-id="d285c-132">เสนอ</span><span class="sxs-lookup"><span data-stu-id="d285c-132">Propose</span></span> | <span data-ttu-id="d285c-133">โอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="d285c-133">Opportunity</span></span> | <span data-ttu-id="d285c-134">พัฒนาข้อเสนอและขอรับการอนุมัติจากทีมตรวจสอบภายใน</span><span class="sxs-lookup"><span data-stu-id="d285c-134">Develop the proposal and get approval from the internal review team.</span></span> |
| <span data-ttu-id="d285c-135">ปิด</span><span class="sxs-lookup"><span data-stu-id="d285c-135">Close</span></span> | <span data-ttu-id="d285c-136">โอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="d285c-136">Opportunity</span></span> | <span data-ttu-id="d285c-137">ชนะโอกาสทางการขายเพื่อปิดข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="d285c-137">Win the opportunity to close the deal.</span></span> |

### <a name="opportunity-sales-process"></a><span data-ttu-id="d285c-138">กระบวนการขายของโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="d285c-138">Opportunity sales process</span></span>
<span data-ttu-id="d285c-139">กระบวนการขายของโอกาสทางการขายใน Project Operations เป็นส่วนเสริมของโฟลว์ธุรกิจของกระบวนการขายของโอกาสทางการขายในแอปพลิเคชัน Sales</span><span class="sxs-lookup"><span data-stu-id="d285c-139">The Opportunity sales process in Project Operations is an extension to the Opportunity sales process business flow in the Sales application.</span></span> <span data-ttu-id="d285c-140">กระบวนการทางธุรกิจนี้ได้รับการออกแบบสำเร็จรูป เพื่อรองรับขั้นตอนต่อไปนี้ในโอกาสทางการขายตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="d285c-140">This business process is designed out-of-the-box to support the following stages in a project-based opportunity.</span></span>

| <span data-ttu-id="d285c-141">ขั้น</span><span class="sxs-lookup"><span data-stu-id="d285c-141">Stage</span></span> | <span data-ttu-id="d285c-142">เอนทิตีที่แม็ป</span><span class="sxs-lookup"><span data-stu-id="d285c-142">Mapped entity</span></span> | <span data-ttu-id="d285c-143">ฟังก์ชันการทำงาน</span><span class="sxs-lookup"><span data-stu-id="d285c-143">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d285c-144">เข้าเกณฑ์</span><span class="sxs-lookup"><span data-stu-id="d285c-144">Qualify</span></span> | <span data-ttu-id="d285c-145">โอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="d285c-145">Opportunity</span></span> | <span data-ttu-id="d285c-146">รับรองลูกค้าเป้าหมายเพื่อสร้างบัญชี ผู้ติดต่อ และโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="d285c-146">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="d285c-147">เสนอ</span><span class="sxs-lookup"><span data-stu-id="d285c-147">Propose</span></span> | <span data-ttu-id="d285c-148">ใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="d285c-148">Quote</span></span> | <span data-ttu-id="d285c-149">พัฒนาข้อเสนอโดยใช้ใบเสนอราคาโครงการและขอรับการอนุมัติจากทีมตรวจสอบภายใน</span><span class="sxs-lookup"><span data-stu-id="d285c-149">Develop the proposal using project quotes and get approval from the internal review team.</span></span> |
| <span data-ttu-id="d285c-150">สัญญา</span><span class="sxs-lookup"><span data-stu-id="d285c-150">Contract</span></span> | <span data-ttu-id="d285c-151">สัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="d285c-151">Project Contract</span></span> | <span data-ttu-id="d285c-152">รับใบเสนอราคาเพื่อสร้างสัญญา และเริ่มดำเนินการและส่งมอบโครงการ</span><span class="sxs-lookup"><span data-stu-id="d285c-152">Win the quote to create the contract and begin execution and delivery on the project.</span></span> |
| <span data-ttu-id="d285c-153">ปิด</span><span class="sxs-lookup"><span data-stu-id="d285c-153">Close</span></span> | <span data-ttu-id="d285c-154">สัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="d285c-154">Project Contract</span></span> | <span data-ttu-id="d285c-155">จบงานสำเร็จ และปิดสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="d285c-155">Finish the work successfully and close the project contract.</span></span> |

> [!NOTE]
> <span data-ttu-id="d285c-156">หากข้อตกลงตามโครงการของคุณเริ่มต้นด้วยลูกค้าเป้าหมาย กระบวนการธุรกิจของลูกค้าเป้าหมายถึงโอกาสทางการขายจะมีความสำคัญเหนือกว่า</span><span class="sxs-lookup"><span data-stu-id="d285c-156">If your project-based deal started with a Lead, the Lead to Opportunity business process takes precedence.</span></span>
>
> <span data-ttu-id="d285c-157">หากข้อตกลงตามโครงการของคุณเริ่มต้นด้วยโอกาสทางการขาย กระบวนการขายของโอกาสทางการขายจะมีความสำคัญเหนือกว่า</span><span class="sxs-lookup"><span data-stu-id="d285c-157">If your project-based deal started with an Opportunity, the Opportunity sales process takes precedence.</span></span>

<span data-ttu-id="d285c-158">คุณสามารถแก้ไขโฟลว์กระบวนการธุรกิจผลิตภัณฑ์ หรือสร้างโฟลว์กระบวนการธุรกิจของคุณเอง เพื่อติดตามกระบวนการขายของคุณได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="d285c-158">You can edit the product business process flow or create your own business process flows to track your sales process as needed.</span></span> <span data-ttu-id="d285c-159">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโฟลว์กระบวนการธุรกิจ โปรดดูที่ [ภาพรวมโฟลว์กระบวนการธุรกิจ](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview)</span><span class="sxs-lookup"><span data-stu-id="d285c-159">For more information about the business process flow, see [Business process flows overview](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span></span>
