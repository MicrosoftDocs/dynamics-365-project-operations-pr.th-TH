---
title: ปรับใช้แอป Project Operations Dataverse พร้อมการรองรับการรวมแบบสองทิศทาง
description: หัวข้อนี้อธิบายวิธีปรับใช้แอป Project Operations Dataverse ด้วยตนเองเพื่อรองรับการรวมแบบสองทิศทาง
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274031"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="62efa-103">ปรับใช้แอป Project Operations Dataverse พร้อมการรองรับการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="62efa-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="62efa-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="62efa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="62efa-105">หัวข้อนี้อธิบายวิธีปรับใช้ Microsoft Dynamics 365 Project Operations ใน Microsoft Dataverse ด้วยตนเองเพื่อรองรับการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="62efa-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="62efa-106">Project Operations ตรวจพบการกำหนดค่าของสภาพแวดล้อมและเพิ่มการสนับสนุนเพิ่มเติมสำหรับการรวมแบบสองทิศทางหากตรงตามข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="62efa-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="62efa-107">ในระหว่างการปรับใช้งานผ่าน Microsoft Dynamics Lifecycle Services (LCS) หากคุณได้ปฏิบัติตามคำแนะนำในหัวข้อนี้ คุณสามารถข้ามการปรับใช้งานของการรวม Microsoft Power Platform ได้ (เดิมเรียกว่าสภาพแวดล้อม Common Data Service)</span><span class="sxs-lookup"><span data-stu-id="62efa-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="62efa-108">กระบวนการปรับใช้งาน Project Operations ใน Dataverse เพื่อให้รองรับการรวมแบบสองทิศทางมีสี่ขั้นตอนหลัก:</span><span class="sxs-lookup"><span data-stu-id="62efa-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="62efa-109">[สร้างสภาพแวดล้อมใหม่ใน Dataverse ที่รองรับการรวมแบบสองทิศทาง](#create)</span><span class="sxs-lookup"><span data-stu-id="62efa-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="62efa-110">[เพิ่มข้อกำหนดเบื้องต้นในการรวมแบบสองทิศทางให้กับสภาพแวดล้อม](#prerequisites)</span><span class="sxs-lookup"><span data-stu-id="62efa-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="62efa-111">[เพิ่มแอป Project Operations Dataverse](#dataverse)</span><span class="sxs-lookup"><span data-stu-id="62efa-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="62efa-112">[เชื่อมโยงสภาพแวดล้อมของคุณ](#link)</span><span class="sxs-lookup"><span data-stu-id="62efa-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="62efa-113">สร้างสภาพแวดล้อมใหม่ใน Dataverse ที่รองรับการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="62efa-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="62efa-114">หากต้องการทำขั้นตอนนี้เสร็จสมบูรณ์ คุณต้องเข้าสู่ระบบเป็นผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="62efa-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="62efa-115">เปิด [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.com) และเข้าสู่ระบบเป็นผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="62efa-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="62efa-116">สร้างสภาพแวดล้อมใหม่และตั้งชื่อ</span><span class="sxs-lookup"><span data-stu-id="62efa-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="62efa-117">เลือกชนิดของสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="62efa-117">Select the environment type.</span></span> <span data-ttu-id="62efa-118">หากคุณสมัครรับข้อเสนอทดลองใช้ ให้เลือก **รุ่นทดลองใช้ (ตามการสมัครรับข้อมูล)**</span><span class="sxs-lookup"><span data-stu-id="62efa-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="62efa-119">ยืนยันภูมิภาคการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="62efa-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="62efa-120">เปิดใช้งานตัวเลือก **สร้างฐานข้อมูลสำหรับสภาพแวดล้อมนี้**</span><span class="sxs-lookup"><span data-stu-id="62efa-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="62efa-121">ยืนยันภาษา แล้วยืนยันว่าสกุลเงินตรงกับสกุลเงินสำหรับแอป Finance and Operations ของคุณ</span><span class="sxs-lookup"><span data-stu-id="62efa-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="62efa-122">เปิดใช้งานตัวเลือก **แอป Dynamics 365** และยืนยันว่าฟิลด์ **ปรับใช้แอปเหล่านี้โดยอัตโนมัติ** ถูกตั้งค่าเป็น **ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="62efa-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="62efa-123">เพิ่มกลุ่มความปลอดภัย หากต้องการกลุ่มความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="62efa-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="62efa-124">เลือก **บันทึก** เพื่อสร้างสภาพแวดล้อมใหม่</span><span class="sxs-lookup"><span data-stu-id="62efa-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="62efa-125">รอจนกว่าการปรับใช้จะเสร็จสิ้นและสภาพแวดล้อมไปถึงสถานะ **พร้อม**</span><span class="sxs-lookup"><span data-stu-id="62efa-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="62efa-126">เพิ่มข้อกำหนดเบื้องต้นในการรวมแบบสองทิศทางให้กับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="62efa-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="62efa-127">การสนับสนุนการรวมแบบสองทิศทางรวมถึงฟิลด์เพิ่มเติมที่เพิ่มไปยังเอนทิตีหลัก เช่น เอนทิตี **บริษัท**</span><span class="sxs-lookup"><span data-stu-id="62efa-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="62efa-128">หากคุณกำลังเพิ่มการสนับสนุนการรวมแบบสองทิศทางในสภาพแวดล้อมที่มีอยู่ คุณอาจต้องอัปเดตข้อมูลเพื่อเปิดใช้งานการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="62efa-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="62efa-129">สำหรับข้อมูลเกี่ยวกับวิธีการเริ่มต้นข้อมูล โปรดดูที่ [การเริ่มต้นข้อมูลบริษัท](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data)</span><span class="sxs-lookup"><span data-stu-id="62efa-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="62efa-130">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการรวมแบบสองทิศทาง โปรดดูที่ [ข้อกำหนดของระบบการรวมแบบสองทิศทาง](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req)</span><span class="sxs-lookup"><span data-stu-id="62efa-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="62efa-131">ทำตามขั้นตอนนี้เพื่อเพิ่มข้อกำหนดเบื้องต้นในการรวมแบบสองทิศทางให้กับสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="62efa-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="62efa-132">เปิดสภาพแวดล้อมที่คุณเพิ่งสร้างขึ้น จากนั้นไปที่ **ทรัพยากร** \> **แอป Dynamics 365**</span><span class="sxs-lookup"><span data-stu-id="62efa-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="62efa-133">เลือก **โซลูชันหลักการรวมแบบสองทิศทาง** ในรายการแอป และติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="62efa-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="62efa-134">รอจนกว่าการติดตั้งจะเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="62efa-134">Wait until the installation is completed.</span></span> <span data-ttu-id="62efa-135">จากนั้นเลือก **โซลูชันการปฏิบัติของโปรแกรมประยุกต์การรวมแบบสองทิศทาง** ในรายการแอป และติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="62efa-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="62efa-136">เพิ่มแอป Project Operations Dataverse</span><span class="sxs-lookup"><span data-stu-id="62efa-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="62efa-137">คุณสามารถทำตามขั้นตอนนี้ได้ก็ต่อเมื่อคุณทำขั้นตอนก่อนหน้านี้เสร็จสิ้นก่อนที่คุณจะติดตั้ง Project Operations</span><span class="sxs-lookup"><span data-stu-id="62efa-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="62efa-138">ระหว่างการติดตั้ง ระบบจะวิเคราะห์การกำหนดค่าสภาพแวดล้อมและเพิ่มการสนับสนุนสำหรับการรวมแบบสองทิศทาง หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="62efa-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="62efa-139">เปิดสภาพแวดล้อมที่คุณเพิ่งสร้างขึ้นก่อนหน้า จากนั้นไปที่ **ทรัพยากร** \> **แอป Dynamics 365**</span><span class="sxs-lookup"><span data-stu-id="62efa-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="62efa-140">เลือก **Microsoft Dynamics 365 Project Operations** ในรายการแอป และติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="62efa-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="62efa-141">เชื่อมโยงสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="62efa-141">Link your environments</span></span>

<span data-ttu-id="62efa-142">หลังจากสภาพแวดล้อม Dataverse ถูกปรับใช้ คุณสามารถตั้งค่าลิงค์ในแอป Finance and Operations ของคุณ</span><span class="sxs-lookup"><span data-stu-id="62efa-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="62efa-143">ทำตามขั้นตอนใน [ใช้ตัวช่วยสร้างการรวมแบบสองทิศทางเพื่อเชื่อมโยงสภาพแวดล้อมของคุณ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment)</span><span class="sxs-lookup"><span data-stu-id="62efa-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
