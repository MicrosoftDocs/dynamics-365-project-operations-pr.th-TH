---
title: ฉันจะกำหนดโฟลว์กระบวนการธุรกิจของลำดับขั้นของโครงการได้อย่างไร?
description: ภาพรวมของวิธีการกำหนดโฟลว์กระบวนการธุรกิจของลำดับขั้นของโครงการเอง
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: 36f7df9e-117d-4f85-af4b-d842e93321bd
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d4b99f67e929ebcd1a684bcd1124756140107d17
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756381"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="bd75c-103">ฉันจะกำหนดโฟลว์กระบวนการธุรกิจของลำดับขั้นของโครงการได้อย่างไร?</span><span class="sxs-lookup"><span data-stu-id="bd75c-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="bd75c-104">มีข้อจำกัดที่ทราบในรุ่นก่อนหน้าของแอพพลิเคชัน Project Service ที่ชื่อของขั้นตอนในโฟลว์กระบวนการธุรกิจของ Project Stages ต้องเหมือนกับชื่อที่เป็นภาษาอังกฤษที่คาดไว้ (**Quote** **Plan** **Close**)</span><span class="sxs-lookup"><span data-stu-id="bd75c-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="bd75c-105">มิฉะนั้น ตรรกะทางธุรกิจ ซึ่งขึ้นกับชื่อขั้นตอนภาษาอังกฤษ จะไม่ทำงานตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="bd75c-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="bd75c-106">นั่นคือเหตุผลที่คุณไม่คุ้นเคยกับการกระทำ เช่น **สลับกระบวนการ** หรือ **แก้ไขกระบวนการ** พร้อมใช้งานบนแบบฟอร์มโครงการ และการกำหนดโฟลว์กระบวนการธุรกิจเองไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="bd75c-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="bd75c-107">ข้อจำกัดนี้ถูกระบุไว้ในรุ่น 2.4.5.48 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="bd75c-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="bd75c-108">บทความนี้แสดงวิธีแก้ไขปัญหาที่แนะนำ ถ้าคุณต้องการกำหนดโฟลว์กระบวนการธุรกิจเริ่มต้นสำหรับรุ่นก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="bd75c-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="bd75c-109">ตรรกะทางธุรกิจจำเป็นต้องมีข้อมูลตรงกับชื่อขั้นตอนภาษาอังกฤษทุกประการ</span><span class="sxs-lookup"><span data-stu-id="bd75c-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="bd75c-110">โฟลว์กระบวนการธุรกิจของ Project Stages มีตรรกะทางธุรกิจที่ไดรฟ์ลักษณะการทำงานต่อไปนี้ในแอพ:</span><span class="sxs-lookup"><span data-stu-id="bd75c-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="bd75c-111">เมื่อโครงการถูกเชื่อมโยงกับใบเสนอราคา รหัสจะตั้งค่าโฟลว์กระบวนการธุรกิจเป็นขั้นตอน **Quote**</span><span class="sxs-lookup"><span data-stu-id="bd75c-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="bd75c-112">เมื่อโครงการถูกเชื่อมโยงกับสัญญา รหัสจะตั้งค่าโฟลว์กระบวนการธุรกิจเป็นขั้นตอน **Plan**</span><span class="sxs-lookup"><span data-stu-id="bd75c-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="bd75c-113">เมื่อโฟลว์กระบวนการธุรกิจคืบหน้าไปยังขั้นตอน **Close** เรกคอร์ดโครงการจะถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bd75c-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="bd75c-114">เมื่อโครงการถูกปิดใช้งาน แบบฟอร์มโครงการ และโครงสร้างการแบ่งงาน (WBS) ถูกตั้งค่าเป็นแบบอ่านอย่างเดียว การจองทรัพยากรที่มีชื่อถูกนำออกใช้ และมีการปิดใช้งานราคาตลาดที่เกี่ยวข้องใดๆ</span><span class="sxs-lookup"><span data-stu-id="bd75c-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="bd75c-115">ตรรกะทางธุรกิจนี้อาศัยชื่อที่เป็นภาษาอังกฤษสำหรับระยะโครงการ</span><span class="sxs-lookup"><span data-stu-id="bd75c-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="bd75c-116">การขึ้นต่อกันนี้ในชื่อขั้นตอนภาษาอังกฤษ เป็นเหตุผลหลักที่การกำหนดเองของโฟลว์กระบวนการธุรกิจ Project Stages ไม่ได้รับการสนับสนุน รวมเหตุผลที่คุณไม่เห็นการดำเนินการโฟลว์กระบวนการธุรกิจทั่วไป เช่น **สลับกระบวนการ** หรือ **แก้ไขกระบวนการ** บนเอนทิตีของโครงการ</span><span class="sxs-lookup"><span data-stu-id="bd75c-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="bd75c-117">จะเกิดอะไรขึ้น หากชื่อขั้นตอนไม่ตรงกับชื่อที่เป็นภาษาอังกฤษ?</span><span class="sxs-lookup"><span data-stu-id="bd75c-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="bd75c-118">ในรุ่นของแอพ Project Service รุ่น 1.x บนแพลตฟอร์ม 8.2 เมื่อชื่อขั้นตอนในโฟลว์กระบวนการธุรกิจไม่ตรงกันทุกประการกับชื่อขั้นตอนไม่ตรงกับชื่อที่เป็นภาษาอังกฤษ ตรรกะทางธุรกิจที่ตั้งค่าขั้นตอนที่ถูกต้องสำหรับใบเสนอราคาหรือสัญญา หรือที่ปิดโครงการ จะถูกข้าม</span><span class="sxs-lookup"><span data-stu-id="bd75c-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="bd75c-119">ไม่มีข้อผิดพลาดแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="bd75c-119">No error messages are displayed.</span></span> <span data-ttu-id="bd75c-120">ดังนั้น จะปรากฏขึ้นว่า คุณสามารถกำหนดโฟลว์กระบวนการธุรกิจของ Project Stages ได้</span><span class="sxs-lookup"><span data-stu-id="bd75c-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="bd75c-121">อย่างไรก็ตาม คุณจะไม่เห็นข้อมูลใดๆ ของกระบวนการอัตโนมัติที่ทำงานให้กับใบเสนอราคา สัญญา และโครงการ ปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="bd75c-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="bd75c-122">ในแอพ Project Service รุ่น 2.4.4.30 หรือรุ่นก่อนหน้านี้ บนแพลตฟอร์ม 9.0 มีการเปลี่ยนแปลงทางสถาปัตยกรรมที่สำคัญ ซึ่งจำเป็นต้องใช้การเขียนใหม่ของของตรรกะทางธุรกิจของโฟลว์กระบวนการธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="bd75c-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="bd75c-123">ดังนั้น ถ้าชื่อขั้นตอนของกระบวนการไม่ตรงกับชื่อที่เป็นภาษาอังกฤษที่คาดไว้ คุณจะได้รับข้อความแสดงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="bd75c-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="bd75c-124">ดังนั้น ถ้าคุณต้องการกำหนดโฟลว์กระบวนการธุรกิจของ Project Stages สำหรับเอนทิตีโครงการ คุณสามารถเพิ่มขั้นตอนใหม่ไปยังโฟลว์กระบวนการธุรกิจสำหรับเอนทิตีโครงการได้เท่านั้น ในขณะที่เก็บรักษาขั้นตอน **ใบเสนอราคา** **วางแผน** และ **ปิด** ตามที่เป็นอยู่</span><span class="sxs-lookup"><span data-stu-id="bd75c-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="bd75c-125">ข้อจำกัดนี้ช่วยให้มั่นใจว่า คุณไม่ได้รับข้อผิดพลาดจากตรรกะทางธุรกิจที่คาดหวังชื่อขั้นตอนภาษาอังกฤษในโฟลว์กระบวนการธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="bd75c-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="bd75c-126">ในรุ่น 2.4.5.48 หรือรุ่นที่ใหม่กว่า ตรรกะทางธุรกิจที่อธิบายไว้ในบทความนี้ได้ถูกเอาออกจากโฟลว์กระบวนการธุรกิจเริ่มต้นสำหรับเอนทิตีของโครงการ</span><span class="sxs-lookup"><span data-stu-id="bd75c-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="bd75c-127">การปรับรุ่นเป็นรุ่นนั้นหรือรุ่นที่ใหม่กว่า จะช่วยให้คุณกำหนดหรือแทนที่โฟลว์กระบวนการธุรกิจเริ่มต้นด้วยหนึ่งในรายการของตัวคุณเอง</span><span class="sxs-lookup"><span data-stu-id="bd75c-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="bd75c-128">วิธีการแก้ปัญหาสำหรับรุ่นที่ก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="bd75c-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="bd75c-129">ถ้าการปรับรุ่นไม่ใช่ทางเลือก คุณสามารถเลือกกำหนดโฟลว์กระบวนการธุรกิจของ Project Stages สำหรับเอนทิตีของโครงการในหนึ่งในวิธีสองวิธีเหล่านี้ได้:</span><span class="sxs-lookup"><span data-stu-id="bd75c-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="bd75c-130">เพิ่มลำดับขั้นเพิ่มเติมไปยังการตั้งค่าคอนฟิกเริ่มต้น ขณะที่ยังรักษาชื่อลำดับขั้นภาษาอังกฤษสำหรับ **ใบเสนอราคา** **วางแผน** และ **ปิด**</span><span class="sxs-lookup"><span data-stu-id="bd75c-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="bd75c-131">![ภาพหน้าจอของการเพิ่มขั้นตอนไปยังการตั้งค่าคอนฟิกเริ่มต้น](media/FAQ-Customize-BPF-1.png)</span><span class="sxs-lookup"><span data-stu-id="bd75c-131">![Screenshot of adding stages to default configuration](media/FAQ-Customize-BPF-1.png)</span></span>
 
2. <span data-ttu-id="bd75c-132">สร้างโฟลว์กระบวนการธุรกิจของคุณเอง และทำให้เป็นโฟลว์กระบวนการธุรกิจหลักสำหรับโครงการเอนทิตี ซึ่งช่วยให้คุณมีชื่อลำดับขั้นใดๆ ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="bd75c-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="bd75c-133">อย่างไรก็ตาม ถ้าคุณต้องการใช้ลำดับขั้นโครงการมาตรฐานเหมือนกัน **ใบเสนอราคา** **วางแผน** และ **ปิด** คุณจำเป็นต้องทำการกำหนดเองบางอย่างที่ถูกขับออกจากชื่อขั้นตอนแบบกำหนดเองของคุณ</span><span class="sxs-lookup"><span data-stu-id="bd75c-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="bd75c-134">ตรรกะที่ซับซ้อนมากขึ้นอยู่ในการปิดของโครงการ ซึ่งคุณยังคงสามารถทริกเกอร์ได้โดยเพียงการปิดใช้งานเรกคอร์ดโครงการ</span><span class="sxs-lookup"><span data-stu-id="bd75c-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="bd75c-135">![ภาพหน้าจอของการแก้ไข/ปรับปรุงตามคำสั่ง BPF](media/FAQ-Customize-BPF-2.png)</span><span class="sxs-lookup"><span data-stu-id="bd75c-135">![Screenshot of BPF customization](media/FAQ-Customize-BPF-2.png)</span></span>

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="bd75c-136">ข้อควรพิจารณาเพิ่มเติม สำหรับแอพ Project Service รุ่น 2.4.4.30 หรือรุ่นก่อนหน้านี้ บนแพลตฟอร์ม 9.0</span><span class="sxs-lookup"><span data-stu-id="bd75c-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="bd75c-137">ใน Project Service 2.4.4.30 หรือรุ่นก่อนหน้านี้ บนแพลตฟอร์ม 9.0 ที่มีโฟลว์กระบวนการธุรกิจแบบกำหนดเอง ฟิลด์ **ชื่อลำดับขั้น** บนเอนทิตีของโครงการที่ใช้ในมุมมองรายการแผนภูมิและโครงการ **โครงการตามลำดับขั้น** จะไม่ปรับปรุง เนื่องจากถูกจับคู่กับโฟลว์กระบวนการธุรกิจของ Project Stages ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="bd75c-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="bd75c-138">คุณสามารถแก้ปัญหานี้ได้โดยขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bd75c-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="bd75c-139">เพิ่มฟิลด์แบบกำหนดเองเพื่อจับภาพขั้นตอนของโฟลว์กระบวนการธุรกิจปัจจุบันที่มีการปรับปรุง เมื่อผู้ใช้คืบหน้าไปยังโฟลว์กระบวนการธุรกิจแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="bd75c-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="bd75c-140">ปรับเปลี่ยนแผนภูมิ **โครงการตามลำดับขั้น** เพื่อทำงานกับฟิลด์แบบกำหนดเองของคุณ แทนที่จะเป็นการตั้งค่าคอนฟิกเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="bd75c-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="bd75c-141">ขั้นตอนในการสร้างโฟลว์กระบวนการธุรกิจของคุณเอง สำหรับเอนทิตีโครงการ</span><span class="sxs-lookup"><span data-stu-id="bd75c-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="bd75c-142">ในการสร้างโฟลว์กระบวนการธุรกิจของคุณเอง สำหรับเอนทิตีโครงการ ให้ดำเนินการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bd75c-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="bd75c-143">ไปที่ **การตั้งค่า** > **ศูนย์กระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="bd75c-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="bd75c-144">ห้ามคัดลอกโฟลว์กระบวนการธุรกิจของ Project Stages เนื่องจากจะคัดลอกตรรกะทางธุรกิจของ Project Service ด้วย</span><span class="sxs-lookup"><span data-stu-id="bd75c-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="bd75c-145">![ภาพหน้าจอของการแก้ไข/ปรับปรุงตามคำสั่ง BPF](media/FAQ-Customize-BPF-3.png)</span><span class="sxs-lookup"><span data-stu-id="bd75c-145">![Screenshot of BPF customization](media/FAQ-Customize-BPF-3.png)</span></span>

2. <span data-ttu-id="bd75c-146">ใช้ตัวออกแบบกระบวนการ เพื่อสร้างชื่อของลำดับขั้นที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="bd75c-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="bd75c-147">ถ้าคุณต้องการฟังก์ชันเดียวกันกับขั้นตอนเริ่มต้นสำหรับ **ใบเสนอราคา** **วางแผน** และ **ปิด** คุณจะต้องสร้างรายการนั้นโดยยึดตามชื่อขั้นตอนของโฟลว์กระบวนการธุรกิจแบบกำหนดเองของคุณ</span><span class="sxs-lookup"><span data-stu-id="bd75c-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="bd75c-148">![ภาพหน้าจอของตัวออกแบบกระบวนการที่ใช้ในการกำหนด BPF](media/FAQ-Customize-BPF-4.png)</span><span class="sxs-lookup"><span data-stu-id="bd75c-148">![Screenshot of Process Designer used to customize BPF](media/FAQ-Customize-BPF-4.png)</span></span> 

3. <span data-ttu-id="bd75c-149">ในตัวออกแบบของกระบวนการ คลิก **ขั้นตอนของกระบวนการใบสั่ง** เพื่อทำให้โฟลว์กระบวนการธุรกิจแบบกำหนดเองเป็นโฟลว์กระบวนการธุรกิจหลักสำหรับเอนทิตีของโครงการ โดยการย้ายไปด้านบนโฟลว์กระบวนการธุรกิจของ Project Stagesไปยังด้านบนสุดของรายการ</span><span class="sxs-lookup"><span data-stu-id="bd75c-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="bd75c-150">![ภาพหน้าจอของการใช้ขั้นตอนการประมวลผลใบสั่ง](media/FAQ-Customize-BPF-5-720.png)</span><span class="sxs-lookup"><span data-stu-id="bd75c-150">![Screenshot of using Order Process Flow](media/FAQ-Customize-BPF-5-720.png)</span></span>

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="bd75c-151">ขั้นตอนต่อไปนี้นำไปใช้กับแอพ Project Service 2.4.4.30 หรือรุ่นก่อนหน้านี้ บนแพลตฟอร์ม 9.0</span><span class="sxs-lookup"><span data-stu-id="bd75c-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="bd75c-152">เพิ่มฟิลด์แบบกำหนดเองใหม่ลงในเอนทิตีโครงการ เพื่อจับภาพขั้นตอนแบบกำหนดเองในโฟลว์กระบวนการธุรกิจแบบกำหนดเองของคุณ</span><span class="sxs-lookup"><span data-stu-id="bd75c-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="bd75c-153">คุณจะต้องเพิ่มตรรกะทางธุรกิจ (ปลั๊กอิน/เวิร์กโฟลว์) เพื่อปรับปรุงฟิลด์นี้ เมื่อขั้นตอนในโฟลว์กระบวนการธุรกิจแบบกำหนดเองถูกปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="bd75c-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="bd75c-154">![ภาพหน้าจอของเอนทิตีของโครงการที่กำหนดด้วยตนเอง](media/FAQ-Customize-BPF-6-720.png)</span><span class="sxs-lookup"><span data-stu-id="bd75c-154">![Screenshot of customizing Project entity](media/FAQ-Customize-BPF-6-720.png)</span></span>

5. <span data-ttu-id="bd75c-155">ปรับเปลี่ยนแผนภูมิ **โครงการตามลำดับขั้น** เพื่อใช้ฟิลด์ใหม่ที่กำหนดเองของคุณสำหรับลำดับขั้น</span><span class="sxs-lookup"><span data-stu-id="bd75c-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="bd75c-156">![ภาพหน้าจอของการใช้แผนภูมิโครงการตามลำดับขั้น](media/FAQ-Customize-BPF-7-720.png)</span><span class="sxs-lookup"><span data-stu-id="bd75c-156">![Screenshot of using the Project By Stage chart](media/FAQ-Customize-BPF-7-720.png)</span></span>

6. <span data-ttu-id="bd75c-157">ปรับเปลี่ยนมุมมองใดๆ สำหรับเอนทิตีของโครงการ เพื่อรวมฟิลด์ใหม่ที่กำหนดเองของคุณสำหรับลำดับขั้น</span><span class="sxs-lookup"><span data-stu-id="bd75c-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="bd75c-158">![ภาพหน้าจอของการปรับเปลี่ยนมุมมองในเอนทิตีของโครงการ](media/FAQ-Customize-BPF-8-720.png)</span><span class="sxs-lookup"><span data-stu-id="bd75c-158">![Screenshot of modifying views on the Project entity](media/FAQ-Customize-BPF-8-720.png)</span></span>

