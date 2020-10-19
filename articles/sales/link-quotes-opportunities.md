---
title: สร้างใบเสนอราคาโครงการจากโอกาสทางการขาย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการสร้างใบเสนอราคาโครงการจากโอกาสทางการขาย
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898555"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="4dbe5-103">สร้างใบเสนอราคาโครงการจากโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="4dbe5-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="4dbe5-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="4dbe5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4dbe5-105">คุณสามารถสร้างใบเสนอราคาจากโอกาสทางการขายของโครงการได้ด้วยวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4dbe5-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="4dbe5-106">จากแท็บ **ใบเสนอราคา** บนเพจ **โอกาสทางการขายของโครงการ**</span><span class="sxs-lookup"><span data-stu-id="4dbe5-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="4dbe5-107">จากโฟลว์กระบวนการขายของโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="4dbe5-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="4dbe5-108">ด้วยการปรับปรุงการอ้างอิงโอกาสทางการขายในใบเสนอราคาที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="4dbe5-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="4dbe5-109">จากแท็บ ใบเสนอราคา ของเพจ โอกาสทางการขายของโครงการ</span><span class="sxs-lookup"><span data-stu-id="4dbe5-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="4dbe5-110">หากต้องการสร้างใบเสนอราคาโครงการจากโอกาสทางการขาย ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4dbe5-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="4dbe5-111">เปิดเพจ **โอกาสทางการขายของโครงการ** และเลือกแท็บ **ใบเสนอราคา**</span><span class="sxs-lookup"><span data-stu-id="4dbe5-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="4dbe5-112">บนตารางย่อย **ใบเสนอราคา** เลือก **+** เพื่อสร้างใบเสนอราคาของโครงการใหม่ที่อิงตามโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="4dbe5-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="4dbe5-113">รายการโอกาสทางการขายและรายการราคาโครงการที่เกี่ยวข้องทั้งหมดจะมีการคัดลอกไปยังใบเสนอราคาใหม่จากโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="4dbe5-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="4dbe5-114">จากโฟลว์กระบวนการขายของโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="4dbe5-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="4dbe5-115">หากต้องการสร้างใบเสนอราคาจากโฟลว์กระบวนการขายของโอกาสทางการขาย ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4dbe5-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="4dbe5-116">จากจากโฟลว์กระบวนการขายของโอกาสทางการขาย ให้เปิดโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="4dbe5-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="4dbe5-117">เลือกลำดับขั้น **รับรอง**</span><span class="sxs-lookup"><span data-stu-id="4dbe5-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="4dbe5-118">เลือก **ถัดไป** จากนั้นเลือก **+ สร้าง** เพื่อสร้างใบเสนอราคาใหม่</span><span class="sxs-lookup"><span data-stu-id="4dbe5-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="4dbe5-119">ข้อมูลส่วนใหญ่ในแท็บ **สรุป** สำหรับใบเสนอราคาใหม่นี้จะกำหนดเป็นค่าเริ่มต้นจากโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="4dbe5-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="4dbe5-120">ป้อนข้อมูลที่จำเป็นที่ขาดหายไปหรือ ปรับปรุงค่าเริ่มต้นตามความจำเป็นในแท็บ **สรุป**</span><span class="sxs-lookup"><span data-stu-id="4dbe5-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="4dbe5-121">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="4dbe5-121">Select **Save**.</span></span> <span data-ttu-id="4dbe5-122">ระบบจะสร้างใบเสนอราคาใหม่และเชื่อมโยงกับโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="4dbe5-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="4dbe5-123">ตอนนี้ คุณสามารถดูข้อมูลใบเสนอราคาในเพจ **ใบเสนอราคา** ของเพจ **โอกาสทางการขาย**</span><span class="sxs-lookup"><span data-stu-id="4dbe5-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="4dbe5-124">กระบวนการขายของโอกาสทางการขายจะเลื่อนไปสู่ลำดับขั้นต่อไปคือ **เสนอ**</span><span class="sxs-lookup"><span data-stu-id="4dbe5-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="4dbe5-125">ด้วยการปรับปรุงการอ้างอิงโอกาสทางการขายในใบเสนอราคาที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="4dbe5-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="4dbe5-126">ใบเสนอราคาที่มีอยู่สามารถเชื่อมโยงกับโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="4dbe5-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="4dbe5-127">ทำตามขั้นตอนต่อไปนี้เพื่อปรับปรุงข้อมูลโอกาสทางการขายในใบเสนอราคาที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="4dbe5-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="4dbe5-128">เปิดเพจ **ใบเสนอราคา** และเลือกแท็บ **สรุป**</span><span class="sxs-lookup"><span data-stu-id="4dbe5-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="4dbe5-129">ในฟิลด์ **โอกาสทางการขาย** เลือกโอกาสทางการขายที่คุณต้องการเชื่อมโยงกับใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="4dbe5-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="4dbe5-130">คุณสามารถดูใบเสนอราคาในตาราง **ใบเสนอราคา** ของโอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="4dbe5-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="4dbe5-131">การใช้กระบวนการขายของโอกาสทางการขาย สามารถย้ายโอกาสทางการขายไปยังลำดับขั้นถัดไปคือ **เสนอ**</span><span class="sxs-lookup"><span data-stu-id="4dbe5-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="4dbe5-132">เมื่อคุณย้ายโอกาสทางการขายไปยังลำดับขั้นนี้ คุณสามารถเลือกใบเสนอราคานี้จากรายการของใบเสนอราคาที่เกี่ยวข้องกับโอกาสทางการขายนี้ได้</span><span class="sxs-lookup"><span data-stu-id="4dbe5-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="4dbe5-133">การเลือกใบเสนอราคานี้บ่งบอกว่าคุณกำลังเลื่อนไปข้างหน้า</span><span class="sxs-lookup"><span data-stu-id="4dbe5-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="4dbe5-134">ใบเสนอราคาอื่นๆ ทั้งหมดที่เกี่ยวข้องกับโอกาสทางการขายนี้จะยังคงมีอยู่และใช้งานได้จนกว่าจะได้รับหนึ่งในใบเสนอราคานั้น</span><span class="sxs-lookup"><span data-stu-id="4dbe5-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="4dbe5-135">คุณสามารถย้ายกระบวนการขายกลับไปยังลำดับขั้นก่อนหน้า ซึ่งคือ **รับรอง** และเลือกใบเสนอราคาอื่นเพื่อเลื่อนไปข้างหน้า</span><span class="sxs-lookup"><span data-stu-id="4dbe5-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
