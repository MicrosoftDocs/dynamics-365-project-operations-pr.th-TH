---
title: ลงทะเบียนการสมัครใช้งานรุ่นพรีวิวของ Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีสมัครใช้งานและปรับใช้งาน Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4c2cd4c5d4dfbb95398932d432864cf0d4d5d54d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276866"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="ded2c-103">ลงทะเบียนการสมัครใช้งานรุ่นพรีวิวของ Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="ded2c-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="ded2c-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="ded2c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ded2c-105">หัวข้อนี้อธิบายถึงวิธีการสมัครรับข้อเสนอรุ่นพรีวิว/คู่ค้าและปรับใช้งานสภาพแวดล้อม Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="ded2c-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ded2c-106">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="ded2c-106">Prerequisites</span></span>

- <span data-ttu-id="ded2c-107">คุณจะได้รับอีเมลเชิญให้คุณเข้าร่วมในการทดลองใช้รุ่นพรีวิว</span><span class="sxs-lookup"><span data-stu-id="ded2c-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="ded2c-108">คุณสามารถขอรุ่นพรีวิวได้ที่ [เว็บไซต์ Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/)</span><span class="sxs-lookup"><span data-stu-id="ded2c-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="ded2c-109">ผู้ใช้ที่ปรับใช้งานรุ่นพรีวิวต้องมีสิทธิ์ของผู้ดูแลระบบส่วนกลางของลูกค้า Azure</span><span class="sxs-lookup"><span data-stu-id="ded2c-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="ded2c-110">การปรับใช้งานสภาพแวดล้อม Finance จำเป็นต้องมีการสมัครใช้งาน Azure ที่ถูกต้อง ซึ่งจะมีการเรียกเก็บเงินตามสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="ded2c-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="ded2c-111">คุณสามารถใช้การสมัครใช้งานที่มีอยู่ขององค์กรหรือใช้ [การทดลองใช้ Azure](https://azure.microsoft.com/en-us/free/) เพื่อเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ded2c-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="ded2c-112">สภาพแวดล้อม CDS จะให้บริการฟรีเป็นเวลา 30 วัน</span><span class="sxs-lookup"><span data-stu-id="ded2c-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="ded2c-113">สมัครรับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ded2c-113">Subscribe</span></span>

<span data-ttu-id="ded2c-114">เมื่อ [คำขอรุ่นพรีวิว](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) ของคุณได้รับการอนุมัติ คุณจะได้รับข้อเสนอสามรายการจาก Microsoft ทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="ded2c-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="ded2c-115">ข้อเสนอเหล่านี้ช่วยให้คุณสามารถปรับใช้งาน Project Operations รุ่นพรีวิว:</span><span class="sxs-lookup"><span data-stu-id="ded2c-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="ded2c-116">Dynamics 365 Project Operations (CRM) - การทดลองใช้รุ่นพรีวิว</span><span class="sxs-lookup"><span data-stu-id="ded2c-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="ded2c-117">Office 365 Project Operations - การทดลองใช้รุ่นพรีวิว</span><span class="sxs-lookup"><span data-stu-id="ded2c-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="ded2c-118">Dynamics 365 Finance - การทดลองใช้รุ่นพรีวิว</span><span class="sxs-lookup"><span data-stu-id="ded2c-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ded2c-119">มีเพียงคนเดียวคือ ผู้เช่าที่เป็นผู้ดูแลระบบ ในองค์กรเท่านั้นที่ต้องทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="ded2c-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="ded2c-120">หากคุณไม่ใช่สมาชิกของรุ่นนี้ ให้รอจนกว่าองค์กรของคุณจะลงทะเบียนและคุณได้รับข้อมูลประจำตัวของผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ded2c-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="ded2c-121">Dynamics 365 Project Operations (CRM) - การทดลองใช้รุ่นพรีวิว</span><span class="sxs-lookup"><span data-stu-id="ded2c-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="ded2c-122">ก่อนที่คุณจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณได้ลงชื่อเข้าใช้เบราว์เซอร์ด้วยบัญชีงานของผู้ใช้ในผู้เช่าที่คุณต้องการดูตัวอย่าง Project Operations</span><span class="sxs-lookup"><span data-stu-id="ded2c-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="ded2c-123">แลกรหัสข้อเสนอแรก **Dynamics 365 Project Operations (CRM) - การทดลองใช้รุ่นพรีวิว** โดยวางลงใน URL ของเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="ded2c-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![แลกรับข้อเสนอ](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="ded2c-125">ยืนยันใบสั่งของคุณ</span><span class="sxs-lookup"><span data-stu-id="ded2c-125">Confirm your order.</span></span>

![ยืนยันคำสั่งซื้อ](./media/17ConfirmOrderNew.png)

<span data-ttu-id="ded2c-127">คุณจะเห็นข้อเสนอยืนยันแลกสำเร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="ded2c-127">You will see confirmation offer was successfully redeemed.</span></span>

![การยืนยัน](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="ded2c-129">Office 365 Project Operations - การทดลองใช้รุ่นพรีวิว</span><span class="sxs-lookup"><span data-stu-id="ded2c-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="ded2c-130">ทำซ้ำขั้นตอนเดียวกันกับรหัสข้อเสนอแรก</span><span class="sxs-lookup"><span data-stu-id="ded2c-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="ded2c-131">อย่าลืมเพิ่มรหัสข้อเสนอที่สองโดยใช้บัญชีผู้ใช้เดียวกับที่ใช้กับรหัสข้อเสนอแรก</span><span class="sxs-lookup"><span data-stu-id="ded2c-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="ded2c-132">การทดลองใช้รุ่นพรีวิวของ Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="ded2c-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="ded2c-133">ทำตามขั้นตอนเดิมซ้ำสำหรับข้อเสนอสุดท้ายจากอีเมลต้อนรับ</span><span class="sxs-lookup"><span data-stu-id="ded2c-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="ded2c-134">มอบหมายสิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ded2c-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ded2c-135">คุณจะต้องมีสิทธิ์การเข้าถึงระดับผู้ดูแลระบบสำหรับพอร์ทัล Microsoft 365 ขององค์กรของคุณเพื่อทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ded2c-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="ded2c-136">ไปที่ [ศูนย์จัดการ Microsoft 365](https://portal.office.com/) เพื่อมอบหมายสิทธิ์การใช้งานให้กับผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ded2c-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![โฮมเพจศูนย์การจัดการ](./media/14AdminPortal.png)

2. <span data-ttu-id="ded2c-138">บนเพจ **ผู้ใช้ที่ใช้งานอยู่** เลือกผู้ใช้ที่คุณต้องการมอบหมายสิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ded2c-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![มอบหมายสิทธิ์การใช้งาน](./media/15AssignLicenses.png)

3. <span data-ttu-id="ded2c-140">ตรวจสอบว่าสิทธิ์การใช้งาน **พรีวิว Dynamics 365 Project Operations (CRM)** และ **Office 365 Project Operations - พรีวิว** ถูกเลือกและเลือก **บันทึกการเปลี่ยนแปลง**</span><span class="sxs-lookup"><span data-stu-id="ded2c-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="ded2c-141">ข้อเสนอการทดลองใช้ Finance ไม่จำเป็นต้องมอบหมายให้กับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ded2c-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="ded2c-142">เริ่มต้นโครงการใหม่ใน LCS</span><span class="sxs-lookup"><span data-stu-id="ded2c-142">Start a new project in LCS</span></span>

<span data-ttu-id="ded2c-143">สร้างโครงการ LCS ใหม่ตามที่อธิบายไว้ในหัวข้อ [เริ่มโครงการใหม่ใน LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="ded2c-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="ded2c-144">เพิ่มการสมัครใช้งาน Azure ไปยังโครงการ LCS</span><span class="sxs-lookup"><span data-stu-id="ded2c-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="ded2c-145">ทำตามขั้นตอนในหัวข้อ [เพิ่มการสมัครใช้งาน Azure ไปยังโครงการ LCS](resource-add-azure-subscription-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="ded2c-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="ded2c-146">ปรับใช้งานสภาพแวดล้อมสาธิต Finance ด้วย Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="ded2c-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="ded2c-147">ทำตามคำแนะนำในหัวข้อ [จัดเตรียมสภาพแวดล้อมใหม่](resource-provision-new-environment.md) เพื่อทำให้การปรับใช้งานเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ded2c-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="ded2c-148">ใช้ชนิดการปรับใช้งาน [สภาพแวดล้อมสาธิต](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) สำหรับพรีวิว</span><span class="sxs-lookup"><span data-stu-id="ded2c-148">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="ded2c-149">ติดตั้งโปรแกรมตั้งค่า CDS และข้อมูลการกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="ded2c-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="ded2c-150">ติดตั้งโปรแกรมตั้งค่า CDS และข้อมูลการกำหนดค่าตามที่อธิบายไว้ในหัวข้อ [ตั้งค่าและใช้ข้อมูลการกำหนดค่าใน Common Data Service](resource-apply-pro-setup-config-data.md)</span><span class="sxs-lookup"><span data-stu-id="ded2c-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="ded2c-151">ทำตามขั้นตอนนี้หลังจากที่สภาพแวดล้อมการสาธิต Finance ถูกปรับใช้ และข้อมูลสาธิตใน FO พร้อมแล้ว</span><span class="sxs-lookup"><span data-stu-id="ded2c-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]