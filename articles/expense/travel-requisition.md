---
title: ใบเบิกค่าเดินทาง
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับใบเบิกค่าเดินทาง
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085801"
---
# <a name="travel-requisitions"></a><span data-ttu-id="6ac6e-103">ใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="6ac6e-103">Travel requisitions</span></span>

<span data-ttu-id="6ac6e-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="6ac6e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6ac6e-105">ใบเบิกค่าเดินทางแสดงรายการค่าใช้จ่ายที่จะเกิดขึ้นตามวัตถุประสงค์ของการเดินทาง</span><span class="sxs-lookup"><span data-stu-id="6ac6e-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="6ac6e-106">มีการส่งใบเบิกค่าเดินทางเพื่อตรวจสอบและสามารถใช้ในการอนุมัติค่าใช้จ่ายได้</span><span class="sxs-lookup"><span data-stu-id="6ac6e-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="6ac6e-107">คุณอาจต้องส่งใบเบิกค่าเดินทางก่อนที่คุณจะทำให้เกิดค่าใช้จ่ายใดๆ ที่เรียกเก็บจากองค์กร</span><span class="sxs-lookup"><span data-stu-id="6ac6e-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="6ac6e-108">ข้อกำหนดนี้มีผลบังคับใช้ไม่ว่าคุณจะเรียกเก็บค่าใช้จ่ายจากบัตรเครดิตขององค์กร ใช้จ่ายเงินสดที่คุณได้รับจากการเบิกเงินสดล่วงหน้า หรือต้องเสียค่าใช้จ่ายนอกวงเงินซึ่งจะมีการเบิกคืนจากองค์กร</span><span class="sxs-lookup"><span data-stu-id="6ac6e-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="6ac6e-109">ใบเบิกค่าเดินทางและนโยบายสามารถใช้เพื่อช่วยจัดการค่าใช้จ่ายขององค์กร</span><span class="sxs-lookup"><span data-stu-id="6ac6e-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="6ac6e-110">ตัวอย่างเช่น หากองค์กรของคุณกำลังทำงานในโครงการที่มีราคาคงที่ ซึ่งต้องมีการเดินทาง ค่าใช้จ่ายในการเดินทางของสมาชิกทีมของโครงการจะต้องพอดีกับงบประมาณของโครงการ</span><span class="sxs-lookup"><span data-stu-id="6ac6e-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="6ac6e-111">โดยค่าใช้จ่ายในการเดินทางได้ต้องรับการอนุมัติก่อนที่จะเกิดขึ้น องค์กรสามารถช่วยให้แน่ใจว่าโครงการยังคงอยู่ในงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="6ac6e-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="6ac6e-112">การกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="6ac6e-112">Configuration</span></span> 

<span data-ttu-id="6ac6e-113">ใบเบิกค่าเดินทางสามารถกำหนดค่าเป็น "บังคับ" ได้โดยการเปิดใช้งานพารามิเตอร์ "การขออนุมัติการเดินทางล่วงหน้าเป็นสิ่งจำเป็น" ในพารามิเตอร์การจัดการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="6ac6e-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="6ac6e-114">สร้างและส่งใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="6ac6e-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="6ac6e-115">ไปที่ **ค่าใช้จ่ายของฉัน: ใบเบิกค่าเดินทาง** และเลือก **ใบเบิกค่าเดินทางใหม่**</span><span class="sxs-lookup"><span data-stu-id="6ac6e-115">Go to **My expenses: Travel Requisition** , and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="6ac6e-116">ป้อนวัตถุประสงค์และปลายทางสำหรับใบเบิก</span><span class="sxs-lookup"><span data-stu-id="6ac6e-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="6ac6e-117">ในฟิลด์ **คำอธิบายการเดินทาง** ให้ป้อนข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6ac6e-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="6ac6e-118">สำหรับค่าใช้จ่ายที่คาดว่าจะเกิดขึ้น เช่น เที่ยวบิน มื้ออาหาร หรือค่าเช่ารถ ให้สร้างการแสดงรายการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="6ac6e-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="6ac6e-119">รวมวันที่โดยประมาณ จำนวนเงินโดยประมาณ และสกุลเงินสำหรับค่าใช้จ่ายแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="6ac6e-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="6ac6e-120">เมื่อคุณเพิ่มค่าใช้จ่ายที่คาดไว้เสร็จแล้ว ให้เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6ac6e-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="6ac6e-121">เมื่อคุณพร้อมที่จะส่งใบเบิกค่าเดินทาง ให้เลือก **เวิร์กโฟลว์** > **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="6ac6e-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="6ac6e-122">คุณสามารถดูใบเบิกค่าเดินทางที่ได้รับอนุมัติของคุณได้ที่ **ค่าใช้จ่ายของฉัน: ใบเบิกค่าเดินทาง**</span><span class="sxs-lookup"><span data-stu-id="6ac6e-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="6ac6e-123">ดูใบเบิกค่าเดินทางที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="6ac6e-123">View available travel requisitions</span></span>

<span data-ttu-id="6ac6e-124">คุณสามารถดูใบเบิกค่าเดินทางทั้งหมดของคุณได้ที่ **ค่าใช้จ่ายของฉัน: ใบเบิกค่าเดินทาง**</span><span class="sxs-lookup"><span data-stu-id="6ac6e-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="6ac6e-125">ใบเบิกค่าเดินทางที่ได้รับอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="6ac6e-125">Approve travel requisitions</span></span>

<span data-ttu-id="6ac6e-126">เลือกใบเบิกค่าเดินทางที่คุณต้องการอนุมัติ จากนั้นเลือก **เวิร์กโฟลว์** > **อนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="6ac6e-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="6ac6e-127">ส่งรายงานค่าใช้จ่ายโดยใช้ใบเบิกค่าเดินทางที่ได้รับอนุมัติของคุณ</span><span class="sxs-lookup"><span data-stu-id="6ac6e-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="6ac6e-128">สร้างรายงานค่าใช้จ่ายใหม่และในส่วนหัวของรายงานค่าใช้จ่ายและจากรายการใบเบิกค่าเดินทางที่ได้รับอนุมัติ ให้เลือก **แม็ปไปยังใบเบิกค่าเดินทาง**</span><span class="sxs-lookup"><span data-stu-id="6ac6e-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="6ac6e-129">ฟิลด์ **จำนวนเงินของใบเบิกค่าเดินทาง** จะปรับปรุงโดยอัตโนมัติในส่วนหัวของรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="6ac6e-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="6ac6e-130">เพิ่มค่าใช้จ่ายแต่ละรายการที่เกิดขึ้นสำหรับการเดินทาง</span><span class="sxs-lookup"><span data-stu-id="6ac6e-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="6ac6e-131">ถ้าเปิดใช้งานฟิลด์ **อนุญาตล่วงหน้าแล้ว** จำนวนเงินที่กระทบยอดและจำนวนเงินที่ได้รับอนุญาตสำหรับประเภทค่าใช้จ่ายเฉพาะจะได้รับการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="6ac6e-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="6ac6e-132">เมื่อคุณจับคู่รายงานค่าใช้จ่ายกับใบเบิกค่าเดินทางที่ได้รับอนุมัติ จำนวนเงินของธุรกรรมต้องไม่เกินจำนวนเงินที่ได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="6ac6e-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 
