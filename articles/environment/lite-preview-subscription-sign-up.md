---
title: ลงทะเบียนเพื่อการสมัครใช้งานรุ่นพรีวิว - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการสมัครใช้งานและปรับใช้งาน Project Operations Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334805"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="74886-103">ลงทะเบียนเพื่อการสมัครใช้งานรุ่นพรีวิว - Lite</span><span class="sxs-lookup"><span data-stu-id="74886-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="74886-104">หัวข้อนี้อธิบายวิธีสมัครรับข้อเสนอรุ่นทดลองใช้งานและการปรับใช้งาน Dynamics 365 Project Operations แบบ lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="74886-104">This topic explains how to subscribe to the trial offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="74886-105">กระบวนการนี้จะเปลี่ยนไปใน Project Operations รุ่นที่กำลังจะออกมา</span><span class="sxs-lookup"><span data-stu-id="74886-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="74886-106">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="74886-106">Prerequisites</span></span>
- <span data-ttu-id="74886-107">ผู้ใช้ที่ปรับใช้งานรุ่นพรีวิวต้องมีสิทธิ์ของผู้ดูแลระบบส่วนกลางของลูกค้า Azure</span><span class="sxs-lookup"><span data-stu-id="74886-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="74886-108">คุณสามารถสร้างผู้เช่าได้ในระหว่างการแลกรับข้อเสนอครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="74886-108">You can create a tenant during the first offer redemption.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74886-109">มีเพียงคนเดียวคือ ผู้เช่าที่เป็นผู้ดูแลระบบ ในองค์กรเท่านั้นที่ต้องทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="74886-109">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="74886-110">หากคุณไม่ใช่สมาชิกของรุ่นนี้ ให้รอจนกว่าองค์กรของคุณจะลงทะเบียนและคุณได้รับข้อมูลประจำตัวของผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="74886-110">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="74886-111">รุ่นทดลองใช้เป็นแบบใช้ครั้งเดียวในผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="74886-111">Trials are single use in the tenant.</span></span> <span data-ttu-id="74886-112">คุณสามารถเรียกใช้รุ่นทดลองใช้เพียงครั้งเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="74886-112">You can only run a trial one time.</span></span> <span data-ttu-id="74886-113">เราขอแนะนำให้คุณสร้างผู้เช่าใหม่เพื่อวัตถุประสงค์ในรุ่นทดลองใช้งาน</span><span class="sxs-lookup"><span data-stu-id="74886-113">We recommend that you create a new tenant for the purpose of the trial.</span></span>

### <a name="dynamics-365-project-operations-trial"></a><span data-ttu-id="74886-114">การทดลองใช้ Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="74886-114">Dynamics 365 Project Operations trial</span></span> 

<span data-ttu-id="74886-115">ก่อนที่คุณจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณได้ลงชื่อเข้าใช้เบราว์เซอร์ด้วยบัญชีงานของผู้ใช้ในผู้เช่าที่คุณต้องการดูตัวอย่าง Project Operations</span><span class="sxs-lookup"><span data-stu-id="74886-115">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="74886-116">ไปที่ [รุ่นทดลองใช้ Project Operations](https://aka.ms/try-po) เพื่อแลกรหัสข้อเสนอแรก **Dynamics 365 Project Operations**</span><span class="sxs-lookup"><span data-stu-id="74886-116">Go to [Project Operations Trial](https://aka.ms/try-po) to redeem the first offer code, **Dynamics 365 Project Operations**.</span></span>
2. <span data-ttu-id="74886-117">ยืนยันใบสั่งของคุณ</span><span class="sxs-lookup"><span data-stu-id="74886-117">Confirm your order.</span></span>

  <span data-ttu-id="74886-118">คุณจะเห็นว่าแลกรับข้อเสนอการยืนยันเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="74886-118">You'll see the confirmation offer was successfully redeemed.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="74886-119">มอบหมายสิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="74886-119">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74886-120">คุณจะต้องมีสิทธิ์การเข้าถึงระดับผู้ดูแลระบบสำหรับพอร์ทัล Microsoft 365 ขององค์กรของคุณเพื่อทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="74886-120">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="74886-121">ไปที่ [ศูนย์จัดการ Microsoft 365](https://portal.office.com/) เพื่อมอบหมายสิทธิ์การใช้งานให้กับผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="74886-121">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>
2. <span data-ttu-id="74886-122">บนเพจ **ผู้ใช้ที่ใช้งานอยู่** เลือกผู้ใช้ที่คุณต้องการมอบหมายสิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="74886-122">On the **Active users** page, select the users that you want to assign a license to.</span></span>
3. <span data-ttu-id="74886-123">ตรวจสอบว่าเลือกสิทธิ์การใช้งาน **Dynamics 365 Project Operations**</span><span class="sxs-lookup"><span data-stu-id="74886-123">Verify that the **Dynamics 365 Project Operations** license is selected.</span></span> 
4. <span data-ttu-id="74886-124">เลือก **บันทึกการเปลี่ยนแปลง**</span><span class="sxs-lookup"><span data-stu-id="74886-124">Select **Save changes**.</span></span>

## <a name="create-a-new-dataverse-environment"></a><span data-ttu-id="74886-125">สร้างสภาพแวดล้อม Dataverse ใหม่</span><span class="sxs-lookup"><span data-stu-id="74886-125">Create a new Dataverse environment</span></span>

1. <span data-ttu-id="74886-126">จัดเตรียมสภาพแวดล้อมการปรับใช้งาน Project Operations Dataverse ใหม่โดยทำตามคำแนะนำในหัวข้อ [รูปแบบการปรับใช้งาน Dataverse](lite-deployment.md)</span><span class="sxs-lookup"><span data-stu-id="74886-126">Provision a new Project Operations Dataverse deployment environment by following instructions in the topic, [Dataverse deployment model](lite-deployment.md).</span></span> <span data-ttu-id="74886-127">เมื่อคุณเลือกประเภทสภาพแวดล้อม อย่าลืมใช้ **การทดลองใช้ (ตามการสมัครสมาชิก)**</span><span class="sxs-lookup"><span data-stu-id="74886-127">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>

  ![สภาพแวดล้อมใหม่](./media/19CreateEnvironment.png)

2. <span data-ttu-id="74886-129">เลือกการตั้งค่า **เปิดใช้งานแอป Dynamics 365** และปล่อย **ปรับใช้แอปเหล่านี้โดยอัตโนมัติ** ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="74886-129">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="74886-130">เลือก **บันทึก** เพื่อสร้างสภาพแวดล้อมใหม่</span><span class="sxs-lookup"><span data-stu-id="74886-130">Select **Save** to create the environment.</span></span>

  ![เพิ่มฐานข้อมูล](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="74886-132">หลังจากสร้างสภาพแวดล้อมแล้ว ให้ติดตั้งโซลูชัน **Microsoft Dynamics 365 Project Operations**</span><span class="sxs-lookup"><span data-stu-id="74886-132">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![ติดตั้งโซลูชัน](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="74886-134">ติดตั้งการกำหนดค่า CDS และตั้งค่าข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="74886-134">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="74886-135">ติดตั้งการกำหนดค่า CDS และตั้งค่าข้อมูลสาธิตโดยทำตามคำแนะนำในหัวข้อ [ใช้การตั้งค่าการสาธิตและข้อมูลการกำหนดค่า](lite-apply-demo-setup-config-data.md)</span><span class="sxs-lookup"><span data-stu-id="74886-135">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
