---
title: การปรับปรุงแอตทริบิวต์ปลั๊กอินพร้อมมิติการกำหนดราคาแบบใหม่
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการอัพเดตแอททริบิวต์ปลั๊กอินสำหรับมิติการกำหนดราคา
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7999c003a0cf670d586ebf4445901e106fbee39f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274706"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="265ed-103">ปรับปรุงแอตทริบิวต์ปลั๊กอินพร้อมมิติการกำหนดราคาแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="265ed-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="265ed-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการอัพเดตแอททริบิวต์ปลั๊กอินสำหรับมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="265ed-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="265ed-105">หัวข้อนี้ใช้ได้กับคุณลักษณะใบเสนอราคาและสัญญาใน Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="265ed-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="265ed-106">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="265ed-106">Prerequisites</span></span>
<span data-ttu-id="265ed-107">ก่อนที่คุณจะทำตามขั้นตอนในหัวข้อนี้ คุณต้องทำตามขั้นตอนในหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="265ed-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="265ed-108">สร้างฟิลด์แบบกำหนดเองและเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="265ed-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="265ed-109">เพิ่มฟิลด์ที่กำหนดเองในการตั้งค่าราคาและเอนทิตีธุรกรรม </span><span class="sxs-lookup"><span data-stu-id="265ed-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="265ed-110">[ตั้งค่าฟิลด์ที่กำหนดเองเป็นมิติการกำหนดราคา](set-up-custom-fields-pricing-dimensions.md)</span><span class="sxs-lookup"><span data-stu-id="265ed-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="265ed-111">ถ้าคุณยังไม่ได้ดำเนินการตามขั้นตอนเหล่านั้น ทำให้เสร็จสมบูรณ์แล้วกลับมายังหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="265ed-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="265ed-112">ลงทะเบียนปลั๊กอิน</span><span class="sxs-lookup"><span data-stu-id="265ed-112">Register a plug-in</span></span>
<span data-ttu-id="265ed-113">เมื่อสร้างรายละเอียดรายการใบเสนอราคาบนหน้า **รายการใบเสนอราคา** สำหรับรายการใบเสนอราคา โครงการระบบจะสร้างรายการประมาณการสองรายการ</span><span class="sxs-lookup"><span data-stu-id="265ed-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="265ed-114">รายการหนึ่งใช้สำหรับด้านต้นทุนของการประมาณ และอีกรายการสำหรับการขายเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="265ed-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="265ed-115">นี่เป็นเหมือนกันสำหรับโครงการรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="265ed-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="265ed-116">เมื่อคุณทำการเปลี่ยนแปลงปริมาณหรือฟิลด์ในด้านต้นทุน การเปลี่ยนแปลงสร้างขึ้นบนด้านการขาย</span><span class="sxs-lookup"><span data-stu-id="265ed-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="265ed-117">เป็นไปได้เนื่องจากปลั๊กอิน PreOperation บน Quotelinedetail และเอนทิตีรายละเอียด Contractline เชื่อมต่อแอตทริบิวต์เฉพาะทางด้านต้นทุนกับด้านการขายของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="265ed-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="265ed-118">หากคุณต้องการเปลี่ยนแปลงค่ามิติการกำหนดราคาในด้านการขายเพื่อดำเนินการในด้านต้นทุนด้วย คุณต้องลงทะเบียนปลั๊กอินต่อไปนี้อีกครั้งหลังจากทำการเปลี่ยนแปลงมิติราคา</span><span class="sxs-lookup"><span data-stu-id="265ed-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="265ed-119">นี่คือปลั๊กอินสำหรับอัปเดตและลงทะเบียนใหม่:</span><span class="sxs-lookup"><span data-stu-id="265ed-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="265ed-120">PreOperationContractLineDetailUpdate - **ปรับปรุง msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="265ed-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="265ed-121">PreOperationQuoteLineDetailUpdate - **ปรับปรุง msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="265ed-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="265ed-122">ทำตามขั้นตอนต่อไปนี้เพื่ออัปเดตและลงทะเบียนปลั๊กอินใหม่</span><span class="sxs-lookup"><span data-stu-id="265ed-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="265ed-123">เปิด **PluginRegistrationTool** และเชื่อมต่อกับสภาพแวดล้อม Project Operations Dataverse ของคุณ</span><span class="sxs-lookup"><span data-stu-id="265ed-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="265ed-124">เลือก **ค้นหา** และพิมพ์ตัวอักษรสองสามตัวแรกของปลั๊กอินที่จะอัปเดต</span><span class="sxs-lookup"><span data-stu-id="265ed-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="265ed-125">หลังจากที่พบปลั๊กอินแล้ว ให้เลือก จากนั้นเลือก **เลือกบนฟอร์มหลัก**</span><span class="sxs-lookup"><span data-stu-id="265ed-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="265ed-126">เลือกขั้นตอน **ปรับปรุง msdyn_orderlinetransaction** คลิกขวา และจากนั้นเลือก **ปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="265ed-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="265ed-127">ในหน้ากล่องโต้ตอบ **ปรับปรุง** ให้คลิกจุดไข่ปลา (**...**) ในการกรองแอตทริบิวต์</span><span class="sxs-lookup"><span data-stu-id="265ed-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="265ed-128">หน้าต่างแอตทริบิวต์การกรองจะเปิดขึ้นและแสดงรายการแอตทริบิวต์ทั้งหมดในเอนทิตีและมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="265ed-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="265ed-129">เลือกกล่องกาเครื่องหมายสำหรับแอตทริบิวต์มิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="265ed-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="265ed-130">เลือก **ตกลง** เพื่อปิดหน้า และจากนั้นเลือก **ขั้นตอนการปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="265ed-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="265ed-131">ทำซ้ำขั้นตอนที่ 2 ถึง 7 สำหรับปลั๊กอินที่สอง **PreOperationQuoteLineDetail**</span><span class="sxs-lookup"><span data-stu-id="265ed-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="265ed-132">สำหรับปลั๊กอินนี้ คุณต้องปรับปรุงขั้นตอน **การปรับปรุงของ msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="265ed-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="265ed-133">ปิด **PluginRegistrationTool**</span><span class="sxs-lookup"><span data-stu-id="265ed-133">Close **PluginRegistrationTool**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]