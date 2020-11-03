---
title: กำหนดชนิดการปรับใช้งานของคุณ
description: หัวข้อนี้ให้ข้อมูลที่จะช่วยคุณกำหนดชนิดการปรับใช้งานที่ถูกต้องของ Project Operations สำหรับบริษัทของคุณ
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085936"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="4e65d-103">กำหนดชนิดการปรับใช้งานของคุณ</span><span class="sxs-lookup"><span data-stu-id="4e65d-103">Determine your deployment type</span></span>

<span data-ttu-id="4e65d-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="4e65d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e65d-105">หลังจากที่คุณซื้อสิทธิ์การใช้งานแล้ว ให้เริ่มที่นี่เพื่อกำหนดรูปแบบการปรับใช้งานที่ดีที่สุดของ Dynamics 365 Project Operations โดยใช้ [ขั้นตอนการติดตั้งที่แนะนำ](https://aka.ms/provisionprojectoperations)</span><span class="sxs-lookup"><span data-stu-id="4e65d-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="4e65d-106">หลังจากที่คุณเสร็จสิ้นขั้นตอนการติดตั้งที่แนะนำแล้ว ระบบจะนำคุณไปยังพอร์ทัลการจัดการที่ถูกต้องเพื่อทำการติดตั้งของคุณให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4e65d-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="4e65d-107">ดูรายละเอียดการปรับใช้งานเพื่อทำการติดตั้งให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4e65d-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="4e65d-108">ลูกค้าปัจจุบันของ Dynamics ที่ใช้ Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="4e65d-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="4e65d-109">Project Operations ประกอบด้วยความสามารถต่างๆ ที่มาพร้อมกับ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="4e65d-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="4e65d-110">พาธสำหรับการปรับรุ่นจะเผยแพร่ให้กับลูกค้าเหล่านี้ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="4e65d-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="4e65d-111">ลูกค้าปัจจุบันของ Dynamics 365 Finance ที่ใช้การจัดการและการบัญชีโครงการ</span><span class="sxs-lookup"><span data-stu-id="4e65d-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="4e65d-112">ลูกค้าปัจจุบันของ Finance ที่ใช้ฟังก์ชันการจัดการและการบัญชีโครงการสามารถใช้รายการนี้ต่อไปได้ตามที่เป็นอยู่</span><span class="sxs-lookup"><span data-stu-id="4e65d-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="4e65d-113">ดูที่ [Project Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ใบสั่งผลิต](#pma)</span><span class="sxs-lookup"><span data-stu-id="4e65d-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="4e65d-114">ชนิดการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4e65d-114">Deployment types</span></span>
<span data-ttu-id="4e65d-115">Project Operations รองรับตัวเลือกการปรับใช้งานที่หลากหลายเพื่อให้ตรงกับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="4e65d-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="4e65d-116">ไม่ว่าคุณจะเป็นลูกค้า Dynamics 365 รายใหม่หรือปัจจุบัน Project Operations สามารถรองรับความต้องการของคุณได้</span><span class="sxs-lookup"><span data-stu-id="4e65d-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="4e65d-117">[แบบสอบถามการปรับใช้งาน](https://aka.ms/provisionprojectoperations) ของเราจะช่วยให้คุณกำหนดการปรับใช้งานที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="4e65d-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="4e65d-118">ผลลัพธ์ดังกล่าวจะนำคุณไปสู่ชนิดการปรับใช้งานอย่างหนึ่งอย่างใดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4e65d-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="4e65d-119">การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="4e65d-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="4e65d-120">Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="4e65d-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="4e65d-121">Project Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="4e65d-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="4e65d-122">Project Operations รองรับสถานการณ์วัสดุที่เก็บในคลัง/ใบสั่งผลิตและสถานการณ์ตามวัสดุที่ไม่ได้เก็บในคลัง/ทรัพยากรบนสภาพแวดล้อมเดียวกันผ่านการกำหนดค่าระดับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="4e65d-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="4e65d-123">ตัวอย่างเช่น Contoso สามารถใช้ความสามารถในการสั่งซื้อสต็อก/ใบสั่งผลิตในโรงงานผลิตในสหรัฐอเมริกา (นิติบุคคล = Contoso Manufacturing United States)</span><span class="sxs-lookup"><span data-stu-id="4e65d-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="4e65d-124">Contoso สามารถใช้ความสามารถที่ไม่เก็บสต็อก/ตามทรัพยากรในสถานที่ให้บริการ Contoso Robotics Arms ในสหราชอาณาจักร (นิติบุคคล = Contoso Robotics สหราชอาณาจักร)</span><span class="sxs-lookup"><span data-stu-id="4e65d-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="4e65d-125">การปรับใช้งานอย่างง่าย - จัดการกับการออกใบแจ้งหนี้ชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="4e65d-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="4e65d-126">การปรับใช้งานรุ่นใช้งานง่ายประกอบด้วยความสามารถดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4e65d-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="4e65d-127">การวางแผนโครงการโดยใช้ Microsoft Project สำหรับเว็บ</span><span class="sxs-lookup"><span data-stu-id="4e65d-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="4e65d-128">การกำหนดราคาแบบหลายมิติ</span><span class="sxs-lookup"><span data-stu-id="4e65d-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="4e65d-129">การจัดการทรัพยากรแบบรวม</span><span class="sxs-lookup"><span data-stu-id="4e65d-129">Unified Resource Management</span></span>
- <span data-ttu-id="4e65d-130">การติดตามเวลา</span><span class="sxs-lookup"><span data-stu-id="4e65d-130">Time Tracking</span></span>
- <span data-ttu-id="4e65d-131">ค่าใช้จ่ายเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="4e65d-131">Basic Expense</span></span>
- <span data-ttu-id="4e65d-132">ข้อเสนอใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="4e65d-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="4e65d-133">ขั้นตอนการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4e65d-133">Deployment steps</span></span>
<span data-ttu-id="4e65d-134">กำหนดรูปแบบการปรับใช้งานที่ดีที่สุดของ Project Operations โดยใช้ [แบบสอบถามการปรับใช้งาน](https://aka.ms/provisionprojectoperations)</span><span class="sxs-lookup"><span data-stu-id="4e65d-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="4e65d-135">สำหรับการปรับใช้งานนี้ โปรดดู [ลงทะเบียนสมัครใช้งานพรีวิว](lite-preview-subscription-sign-up.md) และ [การจัดเตรียมสภาพแวดล้อมใหม่](lite-deployment.md)</span><span class="sxs-lookup"><span data-stu-id="4e65d-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="4e65d-136">Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="4e65d-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="4e65d-137">Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่เก็บในคลังประกอบด้วยความสามารถต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4e65d-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="4e65d-138">การวางแผนโครงการโดยใช้ Microsoft Project สำหรับเว็บ</span><span class="sxs-lookup"><span data-stu-id="4e65d-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="4e65d-139">การกำหนดราคาแบบหลายมิติ</span><span class="sxs-lookup"><span data-stu-id="4e65d-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="4e65d-140">การจัดการทรัพยากรแบบรวม</span><span class="sxs-lookup"><span data-stu-id="4e65d-140">Unified Resource Management</span></span>
- <span data-ttu-id="4e65d-141">การติดตามเวลา</span><span class="sxs-lookup"><span data-stu-id="4e65d-141">Time Tracking</span></span>
- <span data-ttu-id="4e65d-142">ค่าใช้จ่ายเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="4e65d-142">Basic Expense</span></span>
- <span data-ttu-id="4e65d-143">ค่าใช้จ่ายเต็ม</span><span class="sxs-lookup"><span data-stu-id="4e65d-143">Full Expense</span></span>
- <span data-ttu-id="4e65d-144">OCR ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="4e65d-144">Receipt OCR</span></span>
- <span data-ttu-id="4e65d-145">การออกใบแจ้งหนี้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4e65d-145">Full Invoicing</span></span>
- <span data-ttu-id="4e65d-146">การรับรู้รายได้</span><span class="sxs-lookup"><span data-stu-id="4e65d-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="4e65d-147">ขั้นตอนการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4e65d-147">Deployment steps</span></span>
<span data-ttu-id="4e65d-148">กำหนดรูปแบบการปรับใช้งานที่ดีที่สุดของ Project Operations โดยใช้ [แบบสอบถามการปรับใช้งาน](https://aka.ms/provisionprojectoperations)</span><span class="sxs-lookup"><span data-stu-id="4e65d-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="4e65d-149">สำหรับการปรับใช้งานนี้ โปรดดู [ลงทะเบียนสมัครใช้งานพรีวิว](resource-sign-up-preview-subscription.md) และ [การจัดเตรียมสภาพแวดล้อมใหม่](resource-provision-new-environment.md)</span><span class="sxs-lookup"><span data-stu-id="4e65d-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="4e65d-150">Project Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="4e65d-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="4e65d-151">การวางแผนโครงการโดยใช้ WBS</span><span class="sxs-lookup"><span data-stu-id="4e65d-151">Project planning using WBS</span></span>
- <span data-ttu-id="4e65d-152">การจัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4e65d-152">Resource Management</span></span>
- <span data-ttu-id="4e65d-153">การติดตามเวลา</span><span class="sxs-lookup"><span data-stu-id="4e65d-153">Time Tracking</span></span>
- <span data-ttu-id="4e65d-154">ค่าใช้จ่ายเต็ม</span><span class="sxs-lookup"><span data-stu-id="4e65d-154">Full Expense</span></span>
- <span data-ttu-id="4e65d-155">OCR ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="4e65d-155">Receipt OCR</span></span>
- <span data-ttu-id="4e65d-156">การออกใบแจ้งหนี้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4e65d-156">Full Invoicing</span></span>
- <span data-ttu-id="4e65d-157">การรับรู้รายได้</span><span class="sxs-lookup"><span data-stu-id="4e65d-157">Revenue Recognition</span></span>
- <span data-ttu-id="4e65d-158">ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="4e65d-158">Production Orders</span></span>
- <span data-ttu-id="4e65d-159">การสนับสนุนวัสดุ</span><span class="sxs-lookup"><span data-stu-id="4e65d-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="4e65d-160">ขั้นตอนการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4e65d-160">Deployment steps</span></span>
<span data-ttu-id="4e65d-161">กำหนดรูปแบบการปรับใช้งานที่ดีที่สุดของ Project Operations โดยใช้ [แบบสอบถามการปรับใช้งาน](https://aka.ms/provisionprojectoperations)</span><span class="sxs-lookup"><span data-stu-id="4e65d-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="4e65d-162">สำหรับการปรับใช้งานนี้ โปรดดู [ลงทะเบียนสมัครใช้งานพรีวิว](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) และ [การจัดเตรียมสภาพแวดล้อมใหม่](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json)</span><span class="sxs-lookup"><span data-stu-id="4e65d-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

