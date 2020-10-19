---
title: ลงทะเบียนการสมัครใช้งานรุ่นพรีวิวของ Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีสมัครใช้งานและปรับใช้งาน Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949112"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="2b652-103">ลงทะเบียนการสมัครใช้งานรุ่นพรีวิวของ Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="2b652-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="2b652-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="2b652-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2b652-105">หัวข้อนี้อธิบายถึงวิธีการสมัครรับข้อเสนอรุ่นพรีวิว/คู่ค้าและปรับใช้งานสภาพแวดล้อม Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="2b652-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2b652-106">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="2b652-106">Prerequisites</span></span>

- <span data-ttu-id="2b652-107">คุณจะได้รับอีเมลเชิญให้คุณเข้าร่วมในการทดลองใช้รุ่นพรีวิว</span><span class="sxs-lookup"><span data-stu-id="2b652-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="2b652-108">คุณสามารถขอรุ่นพรีวิวได้ที่ [เว็บไซต์ Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/)</span><span class="sxs-lookup"><span data-stu-id="2b652-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="2b652-109">ผู้ใช้ที่ปรับใช้งานรุ่นพรีวิวต้องมีสิทธิ์ของผู้ดูแลระบบส่วนกลางของลูกค้า Azure</span><span class="sxs-lookup"><span data-stu-id="2b652-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="2b652-110">การปรับใช้งานสภาพแวดล้อม Finance จำเป็นต้องมีการสมัครใช้งาน Azure ที่ถูกต้อง ซึ่งจะมีการเรียกเก็บเงินตามสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="2b652-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="2b652-111">คุณสามารถใช้การสมัครใช้งานที่มีอยู่ขององค์กรหรือใช้ [การทดลองใช้ Azure](https://azure.microsoft.com/en-us/free/) เพื่อเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2b652-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="2b652-112">สภาพแวดล้อม CDS จะให้บริการฟรีเป็นเวลา 30 วัน</span><span class="sxs-lookup"><span data-stu-id="2b652-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="2b652-113">สมัครรับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2b652-113">Subscribe</span></span>

<span data-ttu-id="2b652-114">เมื่อ [คำขอรุ่นพรีวิว](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) ของคุณได้รับการอนุมัติ คุณจะได้รับข้อเสนอสองรายการจาก Microsoft ทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="2b652-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="2b652-115">ข้อเสนอเหล่านี้ช่วยให้คุณสามารถปรับใช้งาน Project Operations รุ่นพรีวิว:</span><span class="sxs-lookup"><span data-stu-id="2b652-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="2b652-116">Dynamics 365 Project Operations – การทดลองใช้รุ่นพรีวิว</span><span class="sxs-lookup"><span data-stu-id="2b652-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="2b652-117">การทดลองใช้รุ่นพรีวิวของ Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2b652-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2b652-118">มีเพียงคนเดียวคือ ผู้เช่าที่เป็นผู้ดูแลระบบ ในองค์กรเท่านั้นที่ต้องทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="2b652-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="2b652-119">หากคุณไม่ใช่สมาชิกของรุ่นนี้ ให้รอจนกว่าองค์กรของคุณจะลงทะเบียนและคุณได้รับข้อมูลประจำตัวของผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2b652-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="2b652-120">Dynamics 365 Project Operations – การทดลองใช้รุ่นพรีวิว</span><span class="sxs-lookup"><span data-stu-id="2b652-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="2b652-121">แลกรับข้อเสนอแรก **การทดลองใช้ Dynamics 365 Project Operations** ด้วย URL ที่ให้ไว้ในอีเมลต้อนรับของคุณ</span><span class="sxs-lookup"><span data-stu-id="2b652-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![ข้อเสนอแรก](./media/1FirstOffer.png)

2. <span data-ttu-id="2b652-123">ตรวจสอบว่าคุณเข้าสู่ระบบในฐานะผู้ใช้ที่เป็นขององค์กรที่จะสมัครใช้บริการ</span><span class="sxs-lookup"><span data-stu-id="2b652-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="2b652-124">ดำเนินการแลกรับข้อเสนอต่อไป</span><span class="sxs-lookup"><span data-stu-id="2b652-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="2b652-125">เลือก **ใช่ เพิ่มลงในบัญชีของฉัน**</span><span class="sxs-lookup"><span data-stu-id="2b652-125">Select **Yes, add it to my account**.</span></span>

![แลกรับข้อเสนอ](./media/2RedeemFirstOffer.png)

![ยืนยันข้อเสนอ](./media/3ConfirmFirstOffer.png)

![แลกรับข้อเสนอแล้ว](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="2b652-129">การทดลองใช้รุ่นพรีวิวของ Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="2b652-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="2b652-130">ทำตามขั้นตอนเดิมซ้ำสำหรับข้อเสนอที่สองจากอีเมลต้อนรับ</span><span class="sxs-lookup"><span data-stu-id="2b652-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="2b652-131">มอบหมายสิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2b652-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2b652-132">คุณจะต้องมีสิทธิ์การเข้าถึงระดับผู้ดูแลระบบสำหรับพอร์ทัล Office 365 ขององค์กรของคุณเพื่อทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2b652-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="2b652-133">ไปที่ [ศูนย์จัดการ Microsoft 365](https://portal.office.com/) เพื่อมอบหมายสิทธิ์การใช้งานให้กับผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2b652-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![พอร์ทัลผู้ดูแลระบบของ Office](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="2b652-135">บนเพจ **ผู้ใช้ที่ใช้งานอยู่** เลือกผู้ใช้ที่คุณต้องการมอบหมายสิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2b652-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![มอบหมายสิทธิ์การใช้งาน](./media/6AssignLicenses.png)

3. <span data-ttu-id="2b652-137">ตรวจสอบว่าได้เลือกสิทธิ์การใช้งาน Project Operations แล้ว และเลือก **บันทึกการเปลี่ยนแปลง**</span><span class="sxs-lookup"><span data-stu-id="2b652-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="2b652-138">ข้อเสนอการทดลองใช้ Finance ไม่จำเป็นต้องมอบหมายให้กับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2b652-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="2b652-139">เริ่มต้นโครงการใหม่ใน LCS</span><span class="sxs-lookup"><span data-stu-id="2b652-139">Start a new project in LCS</span></span>

<span data-ttu-id="2b652-140">สร้างโครงการ LCS ใหม่ตามที่อธิบายไว้ในหัวข้อ [เริ่มโครงการใหม่ใน LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="2b652-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="2b652-141">เพิ่มการสมัครใช้งาน Azure ไปยังโครงการ LCS</span><span class="sxs-lookup"><span data-stu-id="2b652-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="2b652-142">ทำตามขั้นตอนในหัวข้อ [เพิ่มการสมัครใช้งาน Azure ไปยังโครงการ LCS](resource-add-azure-subscription-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="2b652-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="2b652-143">ปรับใช้งานสภาพแวดล้อมสาธิต Finance ด้วย Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="2b652-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="2b652-144">ทำตามคำแนะนำในหัวข้อ [จัดเตรียมสภาพแวดล้อมใหม่](resource-provision-new-environment.md) เพื่อทำให้การปรับใช้งานเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="2b652-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="2b652-145">ใช้ชนิดการปรับใช้งาน [สภาพแวดล้อมสาธิต](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) สำหรับพรีวิว</span><span class="sxs-lookup"><span data-stu-id="2b652-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="2b652-146">ติดตั้งโปรแกรมตั้งค่า CDS และข้อมูลการกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="2b652-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="2b652-147">ติดตั้งโปรแกรมตั้งค่า CDS และข้อมูลการกำหนดค่าตามที่อธิบายไว้ในหัวข้อ [ตั้งค่าและใช้ข้อมูลการกำหนดค่าใน Common Data Service](resource-apply-pro-setup-config-data.md)</span><span class="sxs-lookup"><span data-stu-id="2b652-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

