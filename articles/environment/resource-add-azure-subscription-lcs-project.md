---
title: เพิ่มการสมัครใช้งาน Azure ไปยังโครงการ LCS
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีเชื่อมต่อการสมัครใช้งาน Azure กับโครงการ LCS
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6daa86d453ec5022cdd75dff0394c8818292406c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000639"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="8594d-103">เพิ่มการสมัครใช้งาน Azure ไปยังโครงการ LCS</span><span class="sxs-lookup"><span data-stu-id="8594d-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="8594d-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="8594d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8594d-105">ต้องปรับใช้งานสภาพแวดล้อมที่โฮสต์บนระบบคลาวด์โดยใช้การสมัครใช้งาน Azure ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="8594d-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="8594d-106">หัวข้อนี้อธิบายข้อมูลเกี่ยวกับวิธีเชื่อมต่อการสมัครใช้งาน Azure ที่มีอยู่กับโครงการ LCS</span><span class="sxs-lookup"><span data-stu-id="8594d-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="8594d-107">ให้ความยินยอมของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="8594d-107">Grant admin consent</span></span>

1. <span data-ttu-id="8594d-108">ในโครงการ LCS ของคุณ ในส่วน **สภาพแวดล้อม** ให้เลือก **การตั้งค่า Microsoft Azure**</span><span class="sxs-lookup"><span data-stu-id="8594d-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![การตั้งค่า Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="8594d-110">บนเพจ **การตั้งค่าโครงการ** บนแท็บ **ตัวเชื่อมต่อ Azure** เลือก **อนุญาต**</span><span class="sxs-lookup"><span data-stu-id="8594d-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="8594d-111">การดำเนินการนี้ช่วยให้สามารถปรับใช้สภาพแวดล้อมกับโครงการนี้ได้</span><span class="sxs-lookup"><span data-stu-id="8594d-111">This allows environments to be deployed to this project.</span></span>

![ตัวเชื่อมต่อ Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="8594d-113">เลือก **อนุญาต** อีกครั้งเพื่อให้ความยินยอมของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="8594d-113">Select **Authorize** again to provide admin consent.</span></span>

![ให้ความยินยอมของผู้ดูแลระบบ](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="8594d-115">ยอมรับคำขอสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="8594d-115">Accept the permissions request.</span></span>

![ยอมรับคำขอสิทธิ์](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="8594d-117">ขณะนี้ การอนุญาตเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="8594d-117">The authorization is now complete.</span></span> 

![การอนุมัติสำเร็จ](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="8594d-119">ให้การเข้าถึงบริการปรับใช้งาน Dynamics กับการสมัครใช้งาน Azure ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8594d-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="8594d-120">ไปที่ [การเรียกเก็บเงินของ Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) และเลือกการสมัครใช้งานของคุณ</span><span class="sxs-lookup"><span data-stu-id="8594d-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="8594d-121">บริการปรับใช้งาน Dynamics จำเป็นต้องเข้าถึงการสมัครใช้งานนี้เพื่อให้สามารถปรับใช้งานสภาพแวดล้อมได้</span><span class="sxs-lookup"><span data-stu-id="8594d-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![รายละเอียดการสมัครใช้งาน Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="8594d-123">เลือก **การควบคุมการเข้าถึง (IAM)** ในบานหน้าต่างนำทาง แล้วเลือก **เพิ่มการกำหนดบทบาท**</span><span class="sxs-lookup"><span data-stu-id="8594d-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="8594d-124">ในแถบเลื่อนทางด้านขวา ให้เลือก **บทบาทผู้มีส่วนร่วม** และในรายการที่มี ให้ค้นหาและเลือก **บริการปรับใช้งาน Dynamics**</span><span class="sxs-lookup"><span data-stu-id="8594d-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="8594d-125">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8594d-125">Select **Save**.</span></span>

![การเข้าถึงการสมัครใช้งาน](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="8594d-127">เพิ่มตัวเชื่อมต่อการสมัครใช้งานไปยังโครงการ LCS</span><span class="sxs-lookup"><span data-stu-id="8594d-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="8594d-128">ในโครงการ LCS ของคุณ ในเพจ **การตั้งค่า Microsoft Azure** ให้เลือก **เพิ่ม** เพื่อเพิ่มตัวเชื่อมต่อใหม่</span><span class="sxs-lookup"><span data-stu-id="8594d-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="8594d-129">ป้อน ID การสมัครใช้งาน Azure ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8594d-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="8594d-130">คุณสามารถค้นหา ID การสมัครใช้งาน Azure ของคุณได้ใน [พอร์ทัล Azure](https://ms.portal.azure.com/) ภายใต้ **การตั้งค่า** ที่ด้านล่างซ้ายของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="8594d-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="8594d-131">ในฟิลด์ **กำหนดค่าเพื่อใช้ Azure Resource Manager** ให้เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="8594d-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="8594d-132">ตรวจสอบให้แน่ใจว่าโดเมนผู้เช่า AAD การสมัครใช้งานของ Azure ตรงกับการสมัครใช้งาน Azure ที่เป็นเจ้าของโดเมนที่คุณใช้อยู่ และเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="8594d-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="8594d-133">บนหน้าจอ **การตั้งค่า Microsoft Azure** เลือก **ถัดไป** เพื่อยืนยัน</span><span class="sxs-lookup"><span data-stu-id="8594d-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="8594d-134">หากคุณได้รับข้อผิดพลาดบนหน้าจอนี้ ให้กลับไปที่ส่วน [ให้การเข้าถึงบริการปรับใช้งาน Dynamics กับการสมัครใช้งาน Azure](#provide) ในหัวข้อนี้และตรวจสอบให้แน่ใจว่าคุณได้ทำตามขั้นตอนทั้งหมดเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="8594d-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="8594d-135">ดาวน์โหลดใบรับรองการจัดการ Azure ไปยังโฟลเดอร์ภายในเครื่องบนคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8594d-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="8594d-136">ขอให้ผู้ดูแลระบบการสมัครใช้งาน Azure ของคุณอัปโหลดใบรับรองไปยัง Azure Management Portal โดยเลือกการสมัครใช้งาน และไปที่ **การตั้งค่า** > **ใบรับรองการจัดการ**</span><span class="sxs-lookup"><span data-stu-id="8594d-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="8594d-137">ใบรับรองนี้ช่วยให้ LCS สามารถสื่อสารกับ Azure ในนามของคุณ</span><span class="sxs-lookup"><span data-stu-id="8594d-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="8594d-138">คุณสามารถข้ามขั้นตอนนี้ได้หากผู้ใช้ของคุณสามารถเข้าถึงการสมัครใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="8594d-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="8594d-139">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="8594d-139">Select  **Next**.</span></span>
8. <span data-ttu-id="8594d-140">เลือกภูมิภาค Azure เพื่อปรับใช้งานและเลือกศูนย์ข้อมูลที่อยู่ใกล้กับที่ที่คุณวางแผนจะใช้ระบบนี้</span><span class="sxs-lookup"><span data-stu-id="8594d-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="8594d-141">เลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="8594d-141">Select  **Connect**.</span></span>

<span data-ttu-id="8594d-142">คุณได้เชื่อมต่อการสมัครใช้งาน Azure ของคุณเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="8594d-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="8594d-143">ตอนนี้คุณสามารถปรับใช้งานสภาพแวดล้อมที่โฮสต์บนระบบคลาวด์ของ Dynamics 365 Finance เรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="8594d-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
