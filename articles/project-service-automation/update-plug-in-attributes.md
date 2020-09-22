---
title: อัพเดตแอททริบิวต์ของปลั๊กอินเพื่อรวมมิติการกำหนดราคาใหม่
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการอัพเดตแอททริบิวต์ปลั๊กอินสำหรับมิติการกำหนดราคา
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: e9b7e752-39c3-4610-8ced-25d9e197b705
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 746b9978f9ae63c05e1031afc31c8134f05ec195
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756463"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="6558e-103">อัพเดตแอททริบิวต์ของปลั๊กอินเพื่อรวมมิติการกำหนดราคาใหม่</span><span class="sxs-lookup"><span data-stu-id="6558e-103">Update plug-in attributes to include new pricing dimensions</span></span>

> [!NOTE]
> <span data-ttu-id="6558e-104">ถ้าคุณไม่ได้ใช้คุณลักษณะการอ้างถึง Project Service Automation (PSA) และทำสัญญา คุณสามารถข้ามหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="6558e-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="6558e-105">หัวข้อนี้อนุมานว่าคุณได้ทำตามขั้นตอนในหัวข้อ [สร้างฟิลด์ที่กำหนดเองและเอนทิตี](create-custom-fields-entities.md) [เพิ่มฟิลด์แบบกำหนดเองในการตั้งค่าราคาและเอนทิตีทางธุรกรรม](field-references.md) และ [ตั้งค่าฟิลด์แบบกำหนดเองเป็นมิติการกำหนดราคา](set-up-pricing-dimensions.md)</span><span class="sxs-lookup"><span data-stu-id="6558e-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="6558e-106">ถ้าคุณยังไม่ได้ดำเนินการตามขั้นตอนเหล่านั้น ให้ย้อนกลับและทำให้เสร็จสมบูรณ์แล้วกลับมายังหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="6558e-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="6558e-107">เมื่อมีการสร้างรายละเอียดบรรทัดใบเสนอราคาในเพจ **บรรทัดใบเสนอราคา** สำหรับโครงการบรรทัดใบเสนอราคา ระบบจะสร้างสองบรรทัดการประเมินในพื้นหลัง -- หนึ่งบรรทัดสำหรับด้านต้นทุนของการประเมินและอีกหนึ่งบรรทัดสำหรับด้านการขาย</span><span class="sxs-lookup"><span data-stu-id="6558e-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="6558e-108">นี่เป็นเหมือนกันสำหรับโครงการรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="6558e-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="6558e-109">เมื่อคุณทำการเปลี่ยนแปลงปริมาณหรือฟิลด์ในด้านต้นทุน จะมีการเผยแพร่การเปลี่ยนแปลงไปยังด้านการขาย</span><span class="sxs-lookup"><span data-stu-id="6558e-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="6558e-110">นี่เป็นไปได้เนื่องจากปลั๊กอินต่อไปนี้ต้องลงทะเบียนใหม่หลังจากการเปลี่ยนแปลงมิติการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="6558e-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="6558e-111">PreOperationContractLineDetailUpdate - การปรับปรุง **msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="6558e-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="6558e-112">PreOperationQuoteLineDetailUpdate - การปรับปรุง **msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="6558e-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="6558e-113">ขั้นตอนต่อไปนี้อธิบายถึงกระบวนการลงทะเบียนปลั๊กอิน</span><span class="sxs-lookup"><span data-stu-id="6558e-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="6558e-114">เปิด **PluginRegistrationTool** และเชื่อมต่อกับอินสแตนซ์ออนไลน์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6558e-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="6558e-115">คลิก **ค้นหา** และค้นหาปลั๊กอินที่จะอัพเดต</span><span class="sxs-lookup"><span data-stu-id="6558e-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![ภาพหน้าจอของทรีการค้นหา](media/PRT-1.png)

3. <span data-ttu-id="6558e-117">หลังจากที่พบปลั๊กอินแล้ว ให้เลือกจากนั้นคลิก **เลือกบนฟอร์มหลัก**</span><span class="sxs-lookup"><span data-stu-id="6558e-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="6558e-118">เลือกขั้นตอนของปลั๊กอินที่จะปรับปรุง คลิกขวา และจากนั้นเลือก **การปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="6558e-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![ภาพหน้าจอของปลั๊กอินที่จะอัพเดต](media/PRT-2.png)
 
5. <span data-ttu-id="6558e-120">ในหน้าต่างการปรับปรุง ให้คลิกจุดไข่ปลา (**...**) ในการกรองแอตทริบิวต์</span><span class="sxs-lookup"><span data-stu-id="6558e-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![ภาพหน้าจอของการปรับปรุงข้อมูลการกำหนดค่าขั้นตอนที่มีอยู่](media/PRT-3.png)
 
6. <span data-ttu-id="6558e-122">เลือกกล่องกาเครื่องหมายแอททริบิวต์การกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="6558e-122">Select the pricing attribute check boxes.</span></span>

 ![ภาพหน้าจอที่แสดงการเลือกช่องทำเครื่องหมายสำหรับแอตทริบิวต์การกำหนดราคา](media/PRT-4.png)

7. <span data-ttu-id="6558e-124">คลิก **ตกลง** เพื่อปิดเพจและจากนั้นเลือก **ขั้นตอนการปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="6558e-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![ภาพหน้าจอที่แสดงปุ่ม "ขั้นตอนการปรับปรุง"](media/PRT-5.png)
 
8. <span data-ttu-id="6558e-126">ทำซ้ำกระบวนการนี้สำหรับปลั๊กอินที่สอง **preOperationQuoteLineDetail - การปรับปรุงของ msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="6558e-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="6558e-127">ปิด Plug-in Registration Tool</span><span class="sxs-lookup"><span data-stu-id="6558e-127">Close the plug-in registration tool.</span></span>

