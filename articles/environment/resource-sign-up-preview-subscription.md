---
title: ลงทะเบียนการสมัครใช้งานรุ่นพรีวิวของ Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีสมัครใช้งานและปรับใช้งาน Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334850"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="8f8b1-103">ลงทะเบียนการสมัครใช้งานรุ่นพรีวิวของ Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="8f8b1-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="8f8b1-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="8f8b1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8f8b1-105">หัวข้อนี้อธิบายวิธีสมัครรับข้อเสนอรุ่นทดลองใช้งานและปรับใช้สภาพแวดล้อมของ Project Operations สำหรับสถานการณ์ตามทรัพยากร/สินค้าที่ไม่ได้เก็บในสต็อก</span><span class="sxs-lookup"><span data-stu-id="8f8b1-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8f8b1-106">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="8f8b1-106">Prerequisites</span></span>
- <span data-ttu-id="8f8b1-107">ผู้ใช้ที่ปรับใช้งานรุ่นพรีวิวต้องมีสิทธิ์ของผู้ดูแลระบบส่วนกลางของลูกค้า Azure</span><span class="sxs-lookup"><span data-stu-id="8f8b1-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="8f8b1-108">คุณสามารถสร้างผู้เช่าได้ในระหว่างการแลกรับข้อเสนอครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="8f8b1-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="8f8b1-109">การปรับใช้งานสภาพแวดล้อม Finance จำเป็นต้องมีการสมัครใช้งาน Azure ที่ถูกต้อง ซึ่งจะมีการเรียกเก็บเงินตามสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="8f8b1-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="8f8b1-110">คุณสามารถใช้การสมัครใช้งานที่มีอยู่ขององค์กรหรือใช้ [การทดลองใช้ Azure](https://azure.microsoft.com/en-us/free/) เพื่อเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8f8b1-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="8f8b1-111">สภาพแวดล้อม CDS จะให้บริการฟรีเป็นเวลา 30 วัน</span><span class="sxs-lookup"><span data-stu-id="8f8b1-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f8b1-112">มีเพียงคนเดียวคือ ผู้เช่าที่เป็นผู้ดูแลระบบ ในองค์กรเท่านั้นที่ต้องทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="8f8b1-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="8f8b1-113">หากคุณไม่ใช่สมาชิกของรุ่นนี้ ให้รอจนกว่าองค์กรของคุณจะลงทะเบียนและคุณได้รับข้อมูลประจำตัวของผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8f8b1-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="8f8b1-114">รุ่นทดลองใช้เป็นแบบใช้ครั้งเดียวในผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="8f8b1-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="8f8b1-115">คุณสามารถเรียกใช้รุ่นทดลองใช้เพียงครั้งเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8f8b1-115">You can only run a trial one time.</span></span> <span data-ttu-id="8f8b1-116">เราขอแนะนำให้คุณสร้างผู้เช่าใหม่เพื่อวัตถุประสงค์ในรุ่นทดลองใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8f8b1-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="8f8b1-117">Dynamics 365 Project Operations (CE) - รุ่นทดลองใช้งานตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8f8b1-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="8f8b1-118">ก่อนที่คุณจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณได้ลงชื่อเข้าใช้เบราว์เซอร์ด้วยบัญชีงานของผู้ใช้ในผู้เช่าที่คุณต้องการดูตัวอย่าง Project Operations</span><span class="sxs-lookup"><span data-stu-id="8f8b1-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="8f8b1-119">แลกรหัสข้อเสนอแรก **Dynamics 365 Project Operations** ที่นี่ [รุ่นทดลองใช้Project Operations](https://aka.ms/try-po)</span><span class="sxs-lookup"><span data-stu-id="8f8b1-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="8f8b1-120">ยืนยันใบสั่งของคุณ</span><span class="sxs-lookup"><span data-stu-id="8f8b1-120">Confirm your order.</span></span>

  <span data-ttu-id="8f8b1-121">คุณจะเห็นข้อเสนอยืนยันแลกสำเร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="8f8b1-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="8f8b1-122">การทดลองใช้รุ่นพรีวิวของ Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="8f8b1-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="8f8b1-123">ไปที่ [รุ่นทดลองใช้งานตัวอย่าง Dynamics 365 for Finance](https://aka.ms/trypoche) และทำซ้ำขั้นตอนจากส่วนก่อนหน้าด้วยข้อเสนอ ลงชื่อสมัครใช้สภาพแวดล้อมที่เป็นโฮสต์บนระบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="8f8b1-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="8f8b1-124">มอบหมายสิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8f8b1-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f8b1-125">คุณจะต้องมีสิทธิ์การเข้าถึงระดับผู้ดูแลระบบสำหรับพอร์ทัล Microsoft 365 ขององค์กรของคุณเพื่อทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8f8b1-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="8f8b1-126">ไปที่ [ศูนย์จัดการ Microsoft 365](https://portal.office.com/) เพื่อมอบหมายสิทธิ์การใช้งานให้กับผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8f8b1-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="8f8b1-127">บนเพจ **ผู้ใช้ที่ใช้งานอยู่** เลือกผู้ใช้ที่คุณต้องการมอบหมายสิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8f8b1-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="8f8b1-128">ตรวจสอบว่าเลือกสิทธิ์การใช้งาน **Dynamics 365 Project Operations** และเลือก **บันทึกการเปลี่ยนแปลง**</span><span class="sxs-lookup"><span data-stu-id="8f8b1-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="8f8b1-129">ข้อเสนอการทดลองใช้ Finance ไม่จำเป็นต้องมอบหมายให้กับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="8f8b1-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="8f8b1-130">เริ่มต้นโครงการใหม่ใน LCS</span><span class="sxs-lookup"><span data-stu-id="8f8b1-130">Start a new project in LCS</span></span>

<span data-ttu-id="8f8b1-131">สร้างโครงการ LCS ใหม่ตามที่อธิบายไว้ในหัวข้อ [เริ่มโครงการใหม่ใน LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="8f8b1-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="8f8b1-132">เพิ่มการสมัครใช้งาน Azure ไปยังโครงการ LCS</span><span class="sxs-lookup"><span data-stu-id="8f8b1-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="8f8b1-133">ทำตามขั้นตอนในหัวข้อ [เพิ่มการสมัครใช้งาน Azure ไปยังโครงการ LCS](resource-add-azure-subscription-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="8f8b1-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="8f8b1-134">ปรับใช้งานสภาพแวดล้อมสาธิต Finance ด้วย Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="8f8b1-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="8f8b1-135">ทำตามคำแนะนำในหัวข้อ [จัดเตรียมสภาพแวดล้อมใหม่](resource-provision-new-environment.md) เพื่อทำให้การปรับใช้งานเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="8f8b1-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="8f8b1-136">ใช้ชนิดการปรับใช้งาน [สภาพแวดล้อมสาธิต](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) สำหรับพรีวิว</span><span class="sxs-lookup"><span data-stu-id="8f8b1-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="8f8b1-137">ติดตั้งโปรแกรมตั้งค่า CDS และข้อมูลการกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="8f8b1-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="8f8b1-138">ติดตั้งโปรแกรมตั้งค่า CDS และข้อมูลการกำหนดค่าตามที่อธิบายไว้ในหัวข้อ [ตั้งค่าและใช้ข้อมูลการกำหนดค่าใน Common Data Service](resource-apply-pro-setup-config-data.md)</span><span class="sxs-lookup"><span data-stu-id="8f8b1-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="8f8b1-139">ทำตามขั้นตอนนี้หลังจากปรับใช้สภาพแวดล้อมสาธิตทางการเงินและข้อมูลสาธิตพร้อมแล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8f8b1-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
