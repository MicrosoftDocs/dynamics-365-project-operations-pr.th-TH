---
title: กำหนดชนิดการปรับใช้งานของคุณ
description: หัวข้อนี้ให้ข้อมูลที่จะช่วยคุณกำหนดชนิดการปรับใช้งานที่ถูกต้องของ Project Operations สำหรับบริษัทของคุณ
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ad700a84edd6c39609bc5b4f09ca74af3059a0dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997129"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="d21a1-103">กำหนดชนิดการปรับใช้งานของคุณ</span><span class="sxs-lookup"><span data-stu-id="d21a1-103">Determine your deployment type</span></span>

<span data-ttu-id="d21a1-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="d21a1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d21a1-105">หลังจากที่คุณซื้อสิทธิ์การใช้งาน ให้เริ่มต้นที่นี่ด้วยการกำหนดรูปแบบการปรับใช้งานที่ดีที่สุดของ Dynamics 365 Project Operations โดยใช้ [โฟลว์การติดตั้งที่แนะนำ](https://aka.ms/provisionprojectoperations)</span><span class="sxs-lookup"><span data-stu-id="d21a1-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="d21a1-106">หลังจากที่คุณเสร็จสิ้นขั้นตอนการติดตั้งที่แนะนำแล้ว ระบบจะนำคุณไปยังพอร์ทัลการจัดการที่ถูกต้องเพื่อทำการติดตั้งของคุณให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="d21a1-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="d21a1-107">ดูรายละเอียดการปรับใช้งานเพื่อทำการติดตั้งให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="d21a1-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="d21a1-108">ลูกค้าปัจจุบันของ Dynamics ที่ใช้ Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="d21a1-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="d21a1-109">Project Operations ประกอบด้วยความสามารถต่างๆ ที่มาพร้อมกับ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="d21a1-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="d21a1-110">พาธการอัปเกรดจะออกให้กับลูกค้าเหล่านี้ในเวฟ 1 รุ่นปี 2021</span><span class="sxs-lookup"><span data-stu-id="d21a1-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="d21a1-111">ลูกค้าปัจจุบันของ Dynamics 365 Finance ที่ใช้การจัดการและการบัญชีโครงการ</span><span class="sxs-lookup"><span data-stu-id="d21a1-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="d21a1-112">ลูกค้าปัจจุบันของ Finance ที่ใช้ฟังก์ชันการจัดการโครงการและการบัญชีสามารถใช้งานได้ตามที่เป็นอยู่</span><span class="sxs-lookup"><span data-stu-id="d21a1-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="d21a1-113">ดูที่ [Project Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ใบสั่งผลิต](#pma)</span><span class="sxs-lookup"><span data-stu-id="d21a1-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-regions"></a><span data-ttu-id="d21a1-114">ภูมิภาคที่มีการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d21a1-114">Deployment regions</span></span>
<span data-ttu-id="d21a1-115">ในการพิจารณาว่าภูมิภาคที่ใดรองรับการปรับใช้งาน Project Operations โปรดดู [รายงานความพร้อมใช้งานตามภูมิศาสตร์สำหรับ Dynamics 365 และ Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/)</span><span class="sxs-lookup"><span data-stu-id="d21a1-115">To determine which regions support Project Operations deployment, see [Geographical availability for Dynamics 365 and Power Platform report](https://dynamics.microsoft.com/en-us/geographic-availability/).</span></span> <span data-ttu-id="d21a1-116">เลือก **ดูรายงาน** และขยาย **Dynamics 365> แอป Operations > Dynamics 365 Project Operations** เพื่อดูภูมิภาคที่รองรับ</span><span class="sxs-lookup"><span data-stu-id="d21a1-116">Select **View Report**, and expand **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** to view the supported regions.</span></span>

## <a name="deployment-types"></a><span data-ttu-id="d21a1-117">ชนิดการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d21a1-117">Deployment types</span></span>
<span data-ttu-id="d21a1-118">Project Operations รองรับตัวเลือกการปรับใช้งานที่หลากหลายเพื่อให้ตรงกับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="d21a1-118">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="d21a1-119">ไม่ว่าคุณจะเป็นลูกค้า Dynamics 365 รายใหม่หรือปัจจุบัน Project Operations สามารถรองรับความต้องการของคุณได้</span><span class="sxs-lookup"><span data-stu-id="d21a1-119">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="d21a1-120">[แบบสอบถามการปรับใช้งาน](https://aka.ms/provisionprojectoperations) ของเราจะช่วยให้คุณกำหนดการปรับใช้งานที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="d21a1-120">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="d21a1-121">ผลลัพธ์ดังกล่าวจะนำคุณไปสู่ชนิดการปรับใช้งานอย่างหนึ่งอย่างใดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d21a1-121">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="d21a1-122">การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="d21a1-122">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="d21a1-123">Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="d21a1-123">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="d21a1-124">Project Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="d21a1-124">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="d21a1-125">Project Operations รองรับสถานการณ์วัสดุที่เก็บในคลัง/ใบสั่งผลิตและสถานการณ์ตามวัสดุที่ไม่ได้เก็บในคลัง/ทรัพยากรบนสภาพแวดล้อมเดียวกันผ่านการกำหนดค่าระดับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="d21a1-125">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="d21a1-126">ตัวอย่างเช่น, Contoso สามารถใช้ความสามารถในการสั่งซื้อสินค้าที่เก็บในคลัง/การผลิตในโรงงานผลิตของสหรัฐอเมริกา (นิติบุคคล = การผลิตของ Contoso ในสหรัฐอเมริกา)</span><span class="sxs-lookup"><span data-stu-id="d21a1-126">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="d21a1-127">Contoso สามารถใช้ความสามารถสินค้าที่ไม่เก็บในคลัง/ตามทรัพยากรในโรงงานสำหรับการบริการ Contoso Robotics Arms ในสหราชอาณาจักร (นิติบุคคล = Contoso Robotics สหราชอาณาจักร)</span><span class="sxs-lookup"><span data-stu-id="d21a1-127">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="d21a1-128">การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="d21a1-128">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="d21a1-129">การปรับใช้งานรุ่นใช้งานง่ายประกอบด้วยความสามารถดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d21a1-129">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="d21a1-130">กระบวนการขายสำหรับโครงการที่ขยายประสบการณ์โปรแกรมประยุกต์ Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="d21a1-130">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="d21a1-131">การวางแผนโครงการโดยใช้ Microsoft Project สำหรับเว็บ</span><span class="sxs-lookup"><span data-stu-id="d21a1-131">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="d21a1-132">การกำหนดราคาแบบหลายมิติ</span><span class="sxs-lookup"><span data-stu-id="d21a1-132">Multi-dimensional pricing</span></span>
- <span data-ttu-id="d21a1-133">การจัดการทรัพยากรแบบรวม</span><span class="sxs-lookup"><span data-stu-id="d21a1-133">Unified resource management</span></span>
- <span data-ttu-id="d21a1-134">การติดตามเวลา</span><span class="sxs-lookup"><span data-stu-id="d21a1-134">Time tracking</span></span>
- <span data-ttu-id="d21a1-135">ค่าใช้จ่ายเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="d21a1-135">Basic expense</span></span>
- <span data-ttu-id="d21a1-136">การออกใบแจ้งหนี้ชั่วคราวสำหรับการตรวจสอบและแก้ไขของผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="d21a1-136">Proforma invoicing for Project manager's review and edits</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="d21a1-137">ขั้นตอนการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d21a1-137">Deployment steps</span></span>
<span data-ttu-id="d21a1-138">กำหนดรูปแบบการปรับใช้งานที่ดีที่สุดของ Project Operations โดยใช้ [แบบสอบถามการปรับใช้งาน](https://aka.ms/provisionprojectoperations)</span><span class="sxs-lookup"><span data-stu-id="d21a1-138">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="d21a1-139">สำหรับการปรับใช้งานนี้ โปรดดู [ลงทะเบียนสมัครใช้งานพรีวิว](lite-preview-subscription-sign-up.md) และ [การจัดเตรียมสภาพแวดล้อมใหม่](lite-deployment.md)</span><span class="sxs-lookup"><span data-stu-id="d21a1-139">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="d21a1-140">Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="d21a1-140">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="d21a1-141">Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่เก็บในคลังประกอบด้วยความสามารถต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d21a1-141">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="d21a1-142">กระบวนการขายสำหรับโครงการที่ขยายโปรแกรมประยุกต์ Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="d21a1-142">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="d21a1-143">การวางแผนโครงการโดยใช้ Microsoft Project สำหรับเว็บ</span><span class="sxs-lookup"><span data-stu-id="d21a1-143">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="d21a1-144">การกำหนดราคาแบบหลายมิติ</span><span class="sxs-lookup"><span data-stu-id="d21a1-144">Multi-dimensional pricing</span></span>
- <span data-ttu-id="d21a1-145">การจัดการทรัพยากรแบบรวม</span><span class="sxs-lookup"><span data-stu-id="d21a1-145">Unified resource management</span></span>
- <span data-ttu-id="d21a1-146">การติดตามเวลา</span><span class="sxs-lookup"><span data-stu-id="d21a1-146">Time tracking</span></span>
- <span data-ttu-id="d21a1-147">ค่าใช้จ่ายเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="d21a1-147">Basic expense</span></span>
- <span data-ttu-id="d21a1-148">ค่าใช้จ่ายเต็ม</span><span class="sxs-lookup"><span data-stu-id="d21a1-148">Full expense</span></span>
- <span data-ttu-id="d21a1-149">OCR ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="d21a1-149">Receipt OCR</span></span>
- <span data-ttu-id="d21a1-150">การออกใบแจ้งหนี้สำหรับลูกค้าและชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="d21a1-150">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="d21a1-151">การรับรู้รายได้สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="d21a1-151">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="d21a1-152">ขั้นตอนการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d21a1-152">Deployment steps</span></span>
<span data-ttu-id="d21a1-153">กำหนดรูปแบบการปรับใช้งานที่ดีที่สุดของ Project Operations โดยใช้ [แบบสอบถามการปรับใช้งาน](https://aka.ms/provisionprojectoperations)</span><span class="sxs-lookup"><span data-stu-id="d21a1-153">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="d21a1-154">สำหรับการปรับใช้งานนี้ โปรดดู [ลงทะเบียนสมัครใช้งานพรีวิว](resource-sign-up-preview-subscription.md) และ [การจัดเตรียมสภาพแวดล้อมใหม่](resource-provision-new-environment.md)</span><span class="sxs-lookup"><span data-stu-id="d21a1-154">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="d21a1-155">Project Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="d21a1-155">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="d21a1-156">การวางแผนโครงการโดยใช้ WBS</span><span class="sxs-lookup"><span data-stu-id="d21a1-156">Project planning using WBS</span></span>
- <span data-ttu-id="d21a1-157">การจัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="d21a1-157">Resource management</span></span>
- <span data-ttu-id="d21a1-158">การติดตามเวลา</span><span class="sxs-lookup"><span data-stu-id="d21a1-158">Time tracking</span></span>
- <span data-ttu-id="d21a1-159">ค่าใช้จ่ายเต็ม</span><span class="sxs-lookup"><span data-stu-id="d21a1-159">Full expense</span></span>
- <span data-ttu-id="d21a1-160">OCR ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="d21a1-160">Receipt OCR</span></span>
- <span data-ttu-id="d21a1-161">การออกใบแจ้งหนี้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d21a1-161">Full invoicing</span></span>
- <span data-ttu-id="d21a1-162">การรับรู้รายได้</span><span class="sxs-lookup"><span data-stu-id="d21a1-162">Revenue recognition</span></span>
- <span data-ttu-id="d21a1-163">ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="d21a1-163">Production orders</span></span>
- <span data-ttu-id="d21a1-164">การสนับสนุนวัสดุที่เก็บในคลังด้วยสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="d21a1-164">Stocked materials support with inventory</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="d21a1-165">ขั้นตอนการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d21a1-165">Deployment steps</span></span>
<span data-ttu-id="d21a1-166">กำหนดรูปแบบการปรับใช้งานที่ดีที่สุดของ Project Operations โดยใช้ [แบบสอบถามการปรับใช้งาน](https://aka.ms/provisionprojectoperations)</span><span class="sxs-lookup"><span data-stu-id="d21a1-166">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="d21a1-167">สำหรับการปรับใช้งานนี้ โปรดดู [ลงทะเบียนสมัครใช้งานพรีวิว](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) และ [การจัดเตรียมสภาพแวดล้อมใหม่](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="d21a1-167">For this deployment, see [Sign-up for preview subscriptions](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) and [Provision new environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json).</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]