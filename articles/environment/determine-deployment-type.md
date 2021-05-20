---
title: กำหนดชนิดการปรับใช้งานของคุณ
description: หัวข้อนี้ให้ข้อมูลที่จะช่วยคุณกำหนดชนิดการปรับใช้งานที่ถูกต้องของ Project Operations สำหรับบริษัทของคุณ
author: stsporen
manager: Annbe
ms.date: 03/15/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1aae04230104d27db2f62db8e674697fd83460ac
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948145"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="9b5da-103">กำหนดชนิดการปรับใช้งานของคุณ</span><span class="sxs-lookup"><span data-stu-id="9b5da-103">Determine your deployment type</span></span>

<span data-ttu-id="9b5da-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="9b5da-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b5da-105">หลังจากที่คุณซื้อสิทธิ์การใช้งาน ให้เริ่มต้นที่นี่ด้วยการกำหนดรูปแบบการปรับใช้งานที่ดีที่สุดของ Dynamics 365 Project Operations โดยใช้ [โฟลว์การติดตั้งที่แนะนำ](https://aka.ms/provisionprojectoperations)</span><span class="sxs-lookup"><span data-stu-id="9b5da-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="9b5da-106">หลังจากที่คุณเสร็จสิ้นขั้นตอนการติดตั้งที่แนะนำแล้ว ระบบจะนำคุณไปยังพอร์ทัลการจัดการที่ถูกต้องเพื่อทำการติดตั้งของคุณให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="9b5da-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="9b5da-107">ดูรายละเอียดการปรับใช้งานเพื่อทำการติดตั้งให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="9b5da-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="9b5da-108">ลูกค้าปัจจุบันของ Dynamics ที่ใช้ Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9b5da-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="9b5da-109">Project Operations ประกอบด้วยความสามารถต่างๆ ที่มาพร้อมกับ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9b5da-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="9b5da-110">พาธการอัปเกรดจะออกให้กับลูกค้าเหล่านี้ในเวฟ 1 รุ่นปี 2021</span><span class="sxs-lookup"><span data-stu-id="9b5da-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="9b5da-111">ลูกค้าปัจจุบันของ Dynamics 365 Finance ที่ใช้การจัดการและการบัญชีโครงการ</span><span class="sxs-lookup"><span data-stu-id="9b5da-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="9b5da-112">ลูกค้าปัจจุบันของ Finance ที่ใช้ฟังก์ชันการจัดการโครงการและการบัญชีสามารถใช้งานได้ตามที่เป็นอยู่</span><span class="sxs-lookup"><span data-stu-id="9b5da-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="9b5da-113">ดูที่ [Project Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ใบสั่งผลิต](#pma)</span><span class="sxs-lookup"><span data-stu-id="9b5da-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-regions"></a><span data-ttu-id="9b5da-114">ภูมิภาคที่มีการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9b5da-114">Deployment regions</span></span>
<span data-ttu-id="9b5da-115">ในการพิจารณาว่าภูมิภาคที่ใดรองรับการปรับใช้งาน Project Operations โปรดดู [รายงานความพร้อมใช้งานตามภูมิศาสตร์สำหรับ Dynamics 365 และ Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/)</span><span class="sxs-lookup"><span data-stu-id="9b5da-115">To determine which regions support Project Operations deployment, see [Geographical availability for Dynamics 365 and Power Platform report](https://dynamics.microsoft.com/en-us/geographic-availability/).</span></span> <span data-ttu-id="9b5da-116">เลือก **ดูรายงาน** และขยาย **Dynamics 365> แอป Operations > Dynamics 365 Project Operations** เพื่อดูภูมิภาคที่รองรับ</span><span class="sxs-lookup"><span data-stu-id="9b5da-116">Select **View Report**, and expand **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** to view the supported regions.</span></span>

## <a name="deployment-types"></a><span data-ttu-id="9b5da-117">ชนิดการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9b5da-117">Deployment types</span></span>
<span data-ttu-id="9b5da-118">Project Operations รองรับตัวเลือกการปรับใช้งานที่หลากหลายเพื่อให้ตรงกับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="9b5da-118">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="9b5da-119">ไม่ว่าคุณจะเป็นลูกค้า Dynamics 365 รายใหม่หรือปัจจุบัน Project Operations สามารถรองรับความต้องการของคุณได้</span><span class="sxs-lookup"><span data-stu-id="9b5da-119">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="9b5da-120">[แบบสอบถามการปรับใช้งาน](https://aka.ms/provisionprojectoperations) ของเราจะช่วยให้คุณกำหนดการปรับใช้งานที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="9b5da-120">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="9b5da-121">ผลลัพธ์ดังกล่าวจะนำคุณไปสู่ชนิดการปรับใช้งานอย่างหนึ่งอย่างใดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9b5da-121">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="9b5da-122">การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="9b5da-122">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="9b5da-123">Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="9b5da-123">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="9b5da-124">Project Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="9b5da-124">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="9b5da-125">Project Operations รองรับสถานการณ์วัสดุที่เก็บในคลัง/ใบสั่งผลิตและสถานการณ์ตามวัสดุที่ไม่ได้เก็บในคลัง/ทรัพยากรบนสภาพแวดล้อมเดียวกันผ่านการกำหนดค่าระดับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="9b5da-125">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="9b5da-126">ตัวอย่างเช่น, Contoso สามารถใช้ความสามารถในการสั่งซื้อสินค้าที่เก็บในคลัง/การผลิตในโรงงานผลิตของสหรัฐอเมริกา (นิติบุคคล = การผลิตของ Contoso ในสหรัฐอเมริกา)</span><span class="sxs-lookup"><span data-stu-id="9b5da-126">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="9b5da-127">Contoso สามารถใช้ความสามารถสินค้าที่ไม่เก็บในคลัง/ตามทรัพยากรในโรงงานสำหรับการบริการ Contoso Robotics Arms ในสหราชอาณาจักร (นิติบุคคล = Contoso Robotics สหราชอาณาจักร)</span><span class="sxs-lookup"><span data-stu-id="9b5da-127">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="9b5da-128">การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="9b5da-128">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="9b5da-129">การปรับใช้งานรุ่นใช้งานง่ายประกอบด้วยความสามารถดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9b5da-129">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="9b5da-130">กระบวนการขายสำหรับโครงการที่ขยายประสบการณ์โปรแกรมประยุกต์ Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="9b5da-130">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="9b5da-131">การวางแผนโครงการโดยใช้ Microsoft Project สำหรับเว็บ</span><span class="sxs-lookup"><span data-stu-id="9b5da-131">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="9b5da-132">การกำหนดราคาแบบหลายมิติ</span><span class="sxs-lookup"><span data-stu-id="9b5da-132">Multi-dimensional pricing</span></span>
- <span data-ttu-id="9b5da-133">การจัดการทรัพยากรแบบรวม</span><span class="sxs-lookup"><span data-stu-id="9b5da-133">Unified resource management</span></span>
- <span data-ttu-id="9b5da-134">การติดตามเวลา</span><span class="sxs-lookup"><span data-stu-id="9b5da-134">Time tracking</span></span>
- <span data-ttu-id="9b5da-135">ค่าใช้จ่ายเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="9b5da-135">Basic expense</span></span>
- <span data-ttu-id="9b5da-136">การออกใบแจ้งหนี้ชั่วคราวสำหรับการตรวจสอบและแก้ไขของผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="9b5da-136">Proforma invoicing for Project manager's review and edits</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="9b5da-137">ขั้นตอนการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9b5da-137">Deployment steps</span></span>
<span data-ttu-id="9b5da-138">กำหนดรูปแบบการปรับใช้งานที่ดีที่สุดของ Project Operations โดยใช้ [แบบสอบถามการปรับใช้งาน](https://aka.ms/provisionprojectoperations)</span><span class="sxs-lookup"><span data-stu-id="9b5da-138">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="9b5da-139">สำหรับการปรับใช้งานนี้ โปรดดู [ลงทะเบียนสมัครใช้งานพรีวิว](lite-preview-subscription-sign-up.md) และ [การจัดเตรียมสภาพแวดล้อมใหม่](lite-deployment.md)</span><span class="sxs-lookup"><span data-stu-id="9b5da-139">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="9b5da-140">Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="9b5da-140">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="9b5da-141">Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่เก็บในคลังประกอบด้วยความสามารถต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9b5da-141">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="9b5da-142">กระบวนการขายสำหรับโครงการที่ขยายโปรแกรมประยุกต์ Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="9b5da-142">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="9b5da-143">การวางแผนโครงการโดยใช้ Microsoft Project สำหรับเว็บ</span><span class="sxs-lookup"><span data-stu-id="9b5da-143">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="9b5da-144">การกำหนดราคาแบบหลายมิติ</span><span class="sxs-lookup"><span data-stu-id="9b5da-144">Multi-dimensional pricing</span></span>
- <span data-ttu-id="9b5da-145">การจัดการทรัพยากรแบบรวม</span><span class="sxs-lookup"><span data-stu-id="9b5da-145">Unified resource management</span></span>
- <span data-ttu-id="9b5da-146">การติดตามเวลา</span><span class="sxs-lookup"><span data-stu-id="9b5da-146">Time tracking</span></span>
- <span data-ttu-id="9b5da-147">ค่าใช้จ่ายเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="9b5da-147">Basic expense</span></span>
- <span data-ttu-id="9b5da-148">ค่าใช้จ่ายเต็ม</span><span class="sxs-lookup"><span data-stu-id="9b5da-148">Full expense</span></span>
- <span data-ttu-id="9b5da-149">OCR ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="9b5da-149">Receipt OCR</span></span>
- <span data-ttu-id="9b5da-150">การออกใบแจ้งหนี้สำหรับลูกค้าและชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="9b5da-150">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="9b5da-151">การรับรู้รายได้สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="9b5da-151">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="9b5da-152">ขั้นตอนการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9b5da-152">Deployment steps</span></span>
<span data-ttu-id="9b5da-153">กำหนดรูปแบบการปรับใช้งานที่ดีที่สุดของ Project Operations โดยใช้ [แบบสอบถามการปรับใช้งาน](https://aka.ms/provisionprojectoperations)</span><span class="sxs-lookup"><span data-stu-id="9b5da-153">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="9b5da-154">สำหรับการปรับใช้งานนี้ โปรดดู [ลงทะเบียนสมัครใช้งานพรีวิว](resource-sign-up-preview-subscription.md) และ [การจัดเตรียมสภาพแวดล้อมใหม่](resource-provision-new-environment.md)</span><span class="sxs-lookup"><span data-stu-id="9b5da-154">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="9b5da-155">Project Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="9b5da-155">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="9b5da-156">การวางแผนโครงการโดยใช้ WBS</span><span class="sxs-lookup"><span data-stu-id="9b5da-156">Project planning using WBS</span></span>
- <span data-ttu-id="9b5da-157">การจัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="9b5da-157">Resource management</span></span>
- <span data-ttu-id="9b5da-158">การติดตามเวลา</span><span class="sxs-lookup"><span data-stu-id="9b5da-158">Time tracking</span></span>
- <span data-ttu-id="9b5da-159">ค่าใช้จ่ายเต็ม</span><span class="sxs-lookup"><span data-stu-id="9b5da-159">Full expense</span></span>
- <span data-ttu-id="9b5da-160">OCR ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="9b5da-160">Receipt OCR</span></span>
- <span data-ttu-id="9b5da-161">การออกใบแจ้งหนี้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="9b5da-161">Full invoicing</span></span>
- <span data-ttu-id="9b5da-162">การรับรู้รายได้</span><span class="sxs-lookup"><span data-stu-id="9b5da-162">Revenue recognition</span></span>
- <span data-ttu-id="9b5da-163">ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="9b5da-163">Production orders</span></span>
- <span data-ttu-id="9b5da-164">การสนับสนุนวัสดุที่เก็บในคลังด้วยสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="9b5da-164">Stocked materials support with inventory</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="9b5da-165">ขั้นตอนการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9b5da-165">Deployment steps</span></span>
<span data-ttu-id="9b5da-166">กำหนดรูปแบบการปรับใช้งานที่ดีที่สุดของ Project Operations โดยใช้ [แบบสอบถามการปรับใช้งาน](https://aka.ms/provisionprojectoperations)</span><span class="sxs-lookup"><span data-stu-id="9b5da-166">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="9b5da-167">สำหรับการปรับใช้งานนี้ โปรดดู [ลงทะเบียนสมัครใช้งานพรีวิว](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) และ [การจัดเตรียมสภาพแวดล้อมใหม่](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="9b5da-167">For this deployment, see [Sign-up for preview subscriptions](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) and [Provision new environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json).</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]