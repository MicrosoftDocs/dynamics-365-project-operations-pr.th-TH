---
title: ปรับรุ่นโฮมเพจ
description: หัวข้อนี้แสดงตำแหน่งที่จะหาข้อมูลที่สำคัญเกี่ยวกับคุณลักษณะใหม่และคุณลักษณะที่เปลี่ยนแปลงใน Dynamics 365 Project Service Automation และกระบวนการสำหรับการปรับรุ่นเป็นรุ่นใหม่ล่าสุด
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fa25d069de8098c0e8788c9ebb8aa3426eec5db9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121781"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="d87fd-103">ปรับรุ่นโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="d87fd-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="d87fd-104">ปรับรุ่นจาก PSA รุ่น 2.x หรือ 1.x เป็นรุ่น 3.x</span><span class="sxs-lookup"><span data-stu-id="d87fd-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="d87fd-105">อินสแตนซ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="d87fd-105">New instances</span></span>

<span data-ttu-id="d87fd-106">ณ วันที่ 17 พฤษภาคม 2019 เมื่อมีการเลือก Project Service Automation ในระหว่างการเตรียมใช้งานอินสแตนซ์ใหม่ รุ่น 3.x ถูกติดตั้งโดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d87fd-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="d87fd-107">อินสแตนซ์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="d87fd-107">Existing instances</span></span>

<span data-ttu-id="d87fd-108">ก่อนหน้านี้ ลูกค้าที่มีอินสแตนซ์ของ PSA รุ่น 2.x และต้องปรับรุ่นเป็นรุ่น 3.x ซึ่งเป็นรุ่นที่ใช้ส่วนติดต่อไคลเอ็นต์แบบรวม (UCI) ของ PSA ต้องติดต่อ Microsoft Support และให้รายละเอียดของอินสแตนซ์ของพวกเขา เพื่อให้ฝ่ายสนับสนุนสามารถเปิดใช้งานอินสแตนซ์สำหรับการปรับรุ่นเป็นรุ่น 3.x ได้</span><span class="sxs-lookup"><span data-stu-id="d87fd-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="d87fd-109">ณ วันที่ 1 มีนาคม 2020 ลูกค้าที่มีอินสแตนซ์ของ PSA รุ่น 2.x และจำเป็นต้องอัปเกรดเป็นรุ่น 3.x จะสามารถอัปเกรดอินสแตนซ์ของตนได้โดยตรงจากพอร์ทัลผู้ดูแลระบบโดยไม่ต้องติดต่อ Microsoft Support</span><span class="sxs-lookup"><span data-stu-id="d87fd-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="d87fd-110">PSA รุ่น 3.x ประกอบด้วยการเปลี่ยนแปลงที่สำคัญ</span><span class="sxs-lookup"><span data-stu-id="d87fd-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="d87fd-111">มีการสร้างขึ้นบนกรอบงานส่วนติดต่อแบบรวมเพื่อช่วยให้มีประสบการณ์การใช้งานของผู้ใช้ที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="d87fd-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="d87fd-112">แอปที่ออกแบบใหม่มอบส่วนติดต่อผู้ใช้ (UI) ที่เป็นรูปแบบเดียวกันซึ่งสอดคล้องกัน และเป็นไปตามหลักการดีไซน์ที่ตอบสนองต่อการดูที่เหมาะสมกับขนาดหน้าจอหรืออุปกรณ์ใดๆ</span><span class="sxs-lookup"><span data-stu-id="d87fd-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="d87fd-113">มีการเปลี่ยนแปลงอื่นๆ ทั่วทั้งโปรแกรมประยุกต์</span><span class="sxs-lookup"><span data-stu-id="d87fd-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="d87fd-114">บางพื้นที่ที่มีการเปลี่ยนแปลงรวมถึงการกำหนดราคา การจอง และการกำหนดทรัพยากร เวลา ค่าใช้จ่าย และการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="d87fd-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="d87fd-115">ก่อนที่คุณจะเริ่มกระบวนการปรับรุ่น เราขอแนะนำให้คุณดำเนินงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d87fd-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="d87fd-116">ตรวจสอบว่าทั้ง Dynamics 365 Field Service และ Project Service Automation มีการติดตั้งบนอินสแตนซ์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="d87fd-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="d87fd-117">ถ้ามีการติดตั้งโซลูชันทั้งสองรายการ คุณควรวางแผนที่จะปรับรุ่นทั้งสองรายการ ก่อนที่คุณจะดำเนินการใช้อินสแตนซ์ตามปกติ</span><span class="sxs-lookup"><span data-stu-id="d87fd-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="d87fd-118">ตรวจสอบหัวข้อต่อไปนี้อย่างละเอียด</span><span class="sxs-lookup"><span data-stu-id="d87fd-118">Carefully review the following topics.</span></span> <span data-ttu-id="d87fd-119">การรับรู้และความเข้าใจในการเปลี่ยนแปลงระหว่างรุ่นจะช่วยคุณในกระบวนการปรับรุ่น</span><span class="sxs-lookup"><span data-stu-id="d87fd-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="d87fd-120">หัวข้อเหล่านี้จะให้ข้อมูลเกี่ยวกับการเปลี่ยนแปลงที่สำคัญใน PSA พร้อมกับข้อควรพิจารณาและคำแนะนำสำหรับการวางแผนการปรับรุ่นเป็นเวอร์ชัน 3.x</span><span class="sxs-lookup"><span data-stu-id="d87fd-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="d87fd-121">มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Project Service Automation รุ่น 3</span><span class="sxs-lookup"><span data-stu-id="d87fd-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="d87fd-122">"ข้อควรพิจารณาในการปรับรุ่น - Project Service Automation รุ่น 2.x หรือ 1.x เป็นรุ่น 3.x"</span><span class="sxs-lookup"><span data-stu-id="d87fd-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="d87fd-123">ปรับรุ่นอินสแตนซ์แบบ Sandbox ของคุณเพื่อประเมินการเปลี่ยนแปลงในการดำเนินงานของคุณ ก่อนที่คุณจะปรับรุ่นอินสแตนซ์การใช้งานจริงของคุณ</span><span class="sxs-lookup"><span data-stu-id="d87fd-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="d87fd-124">หลังจากที่คุณได้ตรวจสอบหัวข้อที่ได้กล่าวถึงก่อนหน้านี้แล้ว และพร้อมที่จะปรับรุ่นเป็น PSA รุ่น3.x หรือรุ่นที่ใช้ UCI ให้ส่งการร้องขอไปยังฝ่ายสนับสนุนของ Microsoft เพื่อทำให้การปรับรุ่นพร้อมใช้งานจากศูนย์การจัดการ</span><span class="sxs-lookup"><span data-stu-id="d87fd-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="d87fd-125">ในคำขอของคุณ ให้ใส่รายละเอียดของอินสแตนซ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d87fd-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="d87fd-126">รุ่นเก่าของ PSA (PSA รุ่น 2.x) ในอินสแตนซ์ที่สร้างขึ้นใหม่</span><span class="sxs-lookup"><span data-stu-id="d87fd-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="d87fd-127">ณ วันที่ 17 พฤษภาคม 2019 อินสแตนซ์ใหม่ทั้งหมดจะมี UCI เป็นไคลเอ็นต์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d87fd-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="d87fd-128">สำหรับการจัดตำแหน่งด้วยการเปลี่ยนแปลงนี้ PSA รุ่น 3.x และ Field Service รุ่น 8.x จะถูกเตรียมใช้งานโดยค่าเริ่มต้นอเนื่องจากรุ่นเหล่านี้ได้รับการออกแบบมาเพื่อทำงานกับไคลเอ็นต์ UCI</span><span class="sxs-lookup"><span data-stu-id="d87fd-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="d87fd-129">ตั้งแต่วันที่ 1 มีนาคม 2020 ลูกค้าของ Dynamics PSA จะไม่สามารถสร้างสภาพแวดล้อมใหม่ด้วย PSA รุ่นเก่าได้อีกต่อไป ตัวอย่างเช่น PSA รุ่น 2.x หรือต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="d87fd-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="d87fd-130">สภาพแวดล้อมใหม่ใดๆ จะได้รับเฉพาะรุ่น 3.x ของ PSA</span><span class="sxs-lookup"><span data-stu-id="d87fd-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="d87fd-131">สำหรับประสบการณ์ที่ดีที่สุดเมื่อคุณใช้โปรแกรมประยุกต์ Field Service และโปรแกรมประยุกต์ PSA รุ่นที่เก่ากว่า ไปที่หน้า **การตั้งค่าระบบ** และสำหรับฟิลด์ **ใช้ส่วนติดต่อแบบรวมใหม่เท่านั้น (แนะนำ)** ให้เลือก **ไม่** เนื่องจากรุ่นเหล่านี้ไม่ได้ถูกออกแบบมาเพื่อให้มีการโหลดอย่างถูกต้องใน UCI</span><span class="sxs-lookup"><span data-stu-id="d87fd-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="d87fd-132">หลังจากที่คุณปิด UCI คุณสามารถเปิดและเรียกใช้รุ่นเหล่านี้ของ Field Service และ PSA โดยใช้เว็บไคลเอ็นต์เก่า</span><span class="sxs-lookup"><span data-stu-id="d87fd-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 
