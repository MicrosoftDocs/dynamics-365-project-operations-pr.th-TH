---
title: การปรับปรุง Project Operations
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับรุ่นที่นำออกใช้ของ Dynamics 365 Project Operations
author: sigitac
manager: Annbe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: acafb97b2bb20deaf12db12cd9238cf5ad0817a9
ms.sourcegitcommit: 87dd3b9bb23384e4d0c3208f0341a3de295eefc8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689433"
---
# <a name="project-operations-updates"></a><span data-ttu-id="a71ca-103">การปรับปรุง Project Operations</span><span class="sxs-lookup"><span data-stu-id="a71ca-103">Project Operations updates</span></span>

<span data-ttu-id="a71ca-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว และProject Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ตามการผลิต_</span><span class="sxs-lookup"><span data-stu-id="a71ca-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing, and Project Operations for stocked/production-based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="project-operations-components"></a><span data-ttu-id="a71ca-105">ส่วนประกอบ Project Operations</span><span class="sxs-lookup"><span data-stu-id="a71ca-105">Project Operations components</span></span>

<span data-ttu-id="a71ca-106">Dynamics 365 Project Operations ประกอบด้วยสององค์ประกอบ:</span><span class="sxs-lookup"><span data-stu-id="a71ca-106">Dynamics 365 Project Operations consists of two components:</span></span>

- <span data-ttu-id="a71ca-107">Project Operations บนสภาพแวดล้อม Common Data Service (CDS)ครอบคลุมถึงความสามารถตั้งแต่โอกาสทางการขายไปจนถึงการออกใบแจ้งหนี้ชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="a71ca-107">Project Operations on Common Data Service (CDS) environment covers capabilities from opportunity to proforma invoicing.</span></span> <span data-ttu-id="a71ca-108">CDS ถูกใช้ในการปรับใช้งานแบบ Lite และการปรับใช้สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลังของ Project Operations</span><span class="sxs-lookup"><span data-stu-id="a71ca-108">CDS is used in the lite deployment and resource/non-stocked scenarios deployment of Project Operations.</span></span>
- <span data-ttu-id="a71ca-109">การจัดการโครงการและการบัญชีในสภาพแวดล้อม Dynamics 365 Finance ครอบคลุมถึงความสามารถในการจัดการค่าใช้จ่าย การบัญชีโครงการ และการรับรู้รายได้</span><span class="sxs-lookup"><span data-stu-id="a71ca-109">Project management and accounting in the Dynamics 365 Finance environment covers expense management capabilities, project accounting, and revenue recognition.</span></span> <span data-ttu-id="a71ca-110">สภาพแวดล้อมแอป Finance and Operations ใช้ใน Project Operations สำหรับสถานการณ์ตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก และ Project Operations สำหรับสถานการณ์วัสดุที่เก็บในคลัง/ตามการผลิต</span><span class="sxs-lookup"><span data-stu-id="a71ca-110">The Finance and Operations app environment is used in Project Operations for resource/non-stocked based scenarios and Project Operations for stocked/production-based scenarios.</span></span>

## <a name="project-operations-latest-version"></a><span data-ttu-id="a71ca-111">Project Operations รุ่นล่าสุด</span><span class="sxs-lookup"><span data-stu-id="a71ca-111">Project Operations latest version</span></span>

| <span data-ttu-id="a71ca-112">การดำเนินงานโครงการบนสภาพแวดล้อม CDS</span><span class="sxs-lookup"><span data-stu-id="a71ca-112">Project Operations on CDS environment</span></span> | <span data-ttu-id="a71ca-113">การจัดการโครงการและการบัญชีในสภาพแวดล้อมแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a71ca-113">Project management and accounting in Finance and Operations apps environments</span></span> |
| --- | --- |
| <span data-ttu-id="a71ca-114">4.5.0.134</span><span class="sxs-lookup"><span data-stu-id="a71ca-114">4.5.0.134</span></span> | <span data-ttu-id="a71ca-115">10.0.15</span><span class="sxs-lookup"><span data-stu-id="a71ca-115">10.0.15</span></span> |

<span data-ttu-id="a71ca-116">บันทึกย่อ Project Operations ประจำรุ่นธนวาคม 2020 สำหรับ [ทรัพยากร/ที่ไม่เก็บในคลัง](whats-new-dec-2020-resource-based.md)</span><span class="sxs-lookup"><span data-stu-id="a71ca-116">Project Operations December 2020 release notes for [Resource/non-stocked](whats-new-dec-2020-resource-based.md).</span></span>

## <a name="release-schedule-for-project-operations-on-cds-environment"></a><span data-ttu-id="a71ca-117">กำหนดการเผยแพร่สำหรับ Project Operations บนสภาพแวดล้อม CDS</span><span class="sxs-lookup"><span data-stu-id="a71ca-117">Release schedule for Project Operations on CDS environment</span></span>

<span data-ttu-id="a71ca-118">การอัปเดตสำหรับ Project Operations บนสภาพแวดล้อม CDS มีให้บริการทุกเดือน</span><span class="sxs-lookup"><span data-stu-id="a71ca-118">Updates for Project Operations on CDS environment are available monthly.</span></span> 

| <span data-ttu-id="a71ca-119">สถานี</span><span class="sxs-lookup"><span data-stu-id="a71ca-119">Station</span></span>   | <span data-ttu-id="a71ca-120">ขอบเขต</span><span class="sxs-lookup"><span data-stu-id="a71ca-120">Region</span></span>        | <span data-ttu-id="a71ca-121">รุ่นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="a71ca-121">Current version</span></span> | <span data-ttu-id="a71ca-122">รุ่นถัดไป</span><span class="sxs-lookup"><span data-stu-id="a71ca-122">Next version</span></span> | <span data-ttu-id="a71ca-123">พร้อมใช้งานโดยทั่วไป</span><span class="sxs-lookup"><span data-stu-id="a71ca-123">Generally available</span></span> |
|-----------|---------------|-----------------|--------------|---------------------|
| <span data-ttu-id="a71ca-124">สถานี 2</span><span class="sxs-lookup"><span data-stu-id="a71ca-124">Station 2</span></span> |   &nbsp;      |    &nbsp;       | &nbsp;       |      &nbsp;         |
|   &nbsp;  | <span data-ttu-id="a71ca-125">อเมริกาใต้</span><span class="sxs-lookup"><span data-stu-id="a71ca-125">South America</span></span> |  <span data-ttu-id="a71ca-126">4.5.0.134</span><span class="sxs-lookup"><span data-stu-id="a71ca-126">4.5.0.134</span></span>       | <span data-ttu-id="a71ca-127">TBD</span><span class="sxs-lookup"><span data-stu-id="a71ca-127">TBD</span></span>     | <span data-ttu-id="a71ca-128">08 ม.ค. 21</span><span class="sxs-lookup"><span data-stu-id="a71ca-128">08-Jan-21</span></span>           |
|    &nbsp; | <span data-ttu-id="a71ca-129">แคนาดา</span><span class="sxs-lookup"><span data-stu-id="a71ca-129">Canada</span></span>        |  <span data-ttu-id="a71ca-130">4.5.0.134</span><span class="sxs-lookup"><span data-stu-id="a71ca-130">4.5.0.134</span></span>       | <span data-ttu-id="a71ca-131">TBD</span><span class="sxs-lookup"><span data-stu-id="a71ca-131">TBD</span></span>     | <span data-ttu-id="a71ca-132">08 ม.ค. 21</span><span class="sxs-lookup"><span data-stu-id="a71ca-132">08-Jan-21</span></span>          |
|   &nbsp;  | <span data-ttu-id="a71ca-133">อินเดีย</span><span class="sxs-lookup"><span data-stu-id="a71ca-133">India</span></span>         |  <span data-ttu-id="a71ca-134">4.5.0.134</span><span class="sxs-lookup"><span data-stu-id="a71ca-134">4.5.0.134</span></span>       | <span data-ttu-id="a71ca-135">TBD</span><span class="sxs-lookup"><span data-stu-id="a71ca-135">TBD</span></span>     | <span data-ttu-id="a71ca-136">08 ม.ค. 21</span><span class="sxs-lookup"><span data-stu-id="a71ca-136">08-Jan-21</span></span>           |
| <span data-ttu-id="a71ca-137">สถานี 3</span><span class="sxs-lookup"><span data-stu-id="a71ca-137">Station 3</span></span>  |      &nbsp;   |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | <span data-ttu-id="a71ca-138">ญี่ปุ่น</span><span class="sxs-lookup"><span data-stu-id="a71ca-138">Japan</span></span>         |  <span data-ttu-id="a71ca-139">4.5.0.134</span><span class="sxs-lookup"><span data-stu-id="a71ca-139">4.5.0.134</span></span>       | <span data-ttu-id="a71ca-140">TBD</span><span class="sxs-lookup"><span data-stu-id="a71ca-140">TBD</span></span>     | <span data-ttu-id="a71ca-141">15 ม.ค. 21</span><span class="sxs-lookup"><span data-stu-id="a71ca-141">15-Jan-21</span></span>           |
|   &nbsp;  | <span data-ttu-id="a71ca-142">เอเชียแปซิฟิก</span><span class="sxs-lookup"><span data-stu-id="a71ca-142">Asia Pacific</span></span>  |  <span data-ttu-id="a71ca-143">4.5.0.134</span><span class="sxs-lookup"><span data-stu-id="a71ca-143">4.5.0.134</span></span>       | <span data-ttu-id="a71ca-144">TBD</span><span class="sxs-lookup"><span data-stu-id="a71ca-144">TBD</span></span>     | <span data-ttu-id="a71ca-145">15 ม.ค. 21</span><span class="sxs-lookup"><span data-stu-id="a71ca-145">15-Jan-21</span></span>           |
|   &nbsp;  | <span data-ttu-id="a71ca-146">สหราชอาณาจักร</span><span class="sxs-lookup"><span data-stu-id="a71ca-146">Great Britain</span></span> |  <span data-ttu-id="a71ca-147">4.5.0.134</span><span class="sxs-lookup"><span data-stu-id="a71ca-147">4.5.0.134</span></span>       | <span data-ttu-id="a71ca-148">TBD</span><span class="sxs-lookup"><span data-stu-id="a71ca-148">TBD</span></span>     | <span data-ttu-id="a71ca-149">15 ม.ค. 21</span><span class="sxs-lookup"><span data-stu-id="a71ca-149">15-Jan-21</span></span>           |
|   &nbsp;  | <span data-ttu-id="a71ca-150">โอเชียเนีย</span><span class="sxs-lookup"><span data-stu-id="a71ca-150">Oceania</span></span>       |  <span data-ttu-id="a71ca-151">4.5.0.134</span><span class="sxs-lookup"><span data-stu-id="a71ca-151">4.5.0.134</span></span>       | <span data-ttu-id="a71ca-152">TBD</span><span class="sxs-lookup"><span data-stu-id="a71ca-152">TBD</span></span>     | <span data-ttu-id="a71ca-153">15 ม.ค. 21</span><span class="sxs-lookup"><span data-stu-id="a71ca-153">15-Jan-21</span></span>           |
| <span data-ttu-id="a71ca-154">สถานี 4</span><span class="sxs-lookup"><span data-stu-id="a71ca-154">Station 4</span></span> |     &nbsp;    |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | <span data-ttu-id="a71ca-155">ยุโรป</span><span class="sxs-lookup"><span data-stu-id="a71ca-155">Europe</span></span>        |  <span data-ttu-id="a71ca-156">4.4.0.70</span><span class="sxs-lookup"><span data-stu-id="a71ca-156">4.4.0.70</span></span>       | <span data-ttu-id="a71ca-157">4.5.0.134</span><span class="sxs-lookup"><span data-stu-id="a71ca-157">4.5.0.134</span></span>     | <span data-ttu-id="a71ca-158">11 ธ.ค. 20</span><span class="sxs-lookup"><span data-stu-id="a71ca-158">11-Dec-20</span></span>           |
| <span data-ttu-id="a71ca-159">สถานี 5</span><span class="sxs-lookup"><span data-stu-id="a71ca-159">Station 5</span></span> |     &nbsp;    |     &nbsp;      |     &nbsp;   |      &nbsp;         |
|   &nbsp;  | <span data-ttu-id="a71ca-160">อเมริกาเหนือ</span><span class="sxs-lookup"><span data-stu-id="a71ca-160">North America</span></span> |  <span data-ttu-id="a71ca-161">4.4.0.70</span><span class="sxs-lookup"><span data-stu-id="a71ca-161">4.4.0.70</span></span>       | <span data-ttu-id="a71ca-162">4.5.0.134</span><span class="sxs-lookup"><span data-stu-id="a71ca-162">4.5.0.134</span></span>     | <span data-ttu-id="a71ca-163">18 ธ.ค. 20</span><span class="sxs-lookup"><span data-stu-id="a71ca-163">18-Dec-20</span></span>           |

## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a><span data-ttu-id="a71ca-164">กำหนดการเผยแพร่สำหรับการจัดการโครงการและการบัญชีในสภาพแวดล้อมของแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a71ca-164">Release schedule for Project management and accounting in the Finance and Operations apps environment</span></span>

<span data-ttu-id="a71ca-165">การอัปเดตสำหรับการจัดการโครงการและการบัญชีมีการเผยแพร่แปดครั้งต่อปี</span><span class="sxs-lookup"><span data-stu-id="a71ca-165">Updates for Project management and accounting are released eight times a year.</span></span>

| <span data-ttu-id="a71ca-166">การเผยแพร่ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="a71ca-166">Supported release</span></span> | <span data-ttu-id="a71ca-167">พร้อมใช้งานโดยทั่วไป (อัปเดตด้วยตนเอง)</span><span class="sxs-lookup"><span data-stu-id="a71ca-167">Generally available (self-update)</span></span> |
| --- | --- |
| <span data-ttu-id="a71ca-168">10.0.15</span><span class="sxs-lookup"><span data-stu-id="a71ca-168">10.0.15</span></span> | <span data-ttu-id="a71ca-169">4 ธันวาคม 2020</span><span class="sxs-lookup"><span data-stu-id="a71ca-169">December 4, 2020</span></span> |
| <span data-ttu-id="a71ca-170">10.0.14</span><span class="sxs-lookup"><span data-stu-id="a71ca-170">10.0.14</span></span> | <span data-ttu-id="a71ca-171">23 ตุลาคม 2020</span><span class="sxs-lookup"><span data-stu-id="a71ca-171">October 23, 2020</span></span> |

<span data-ttu-id="a71ca-172">วันที่วางจำหน่ายเป้าหมายอาจเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="a71ca-172">Targeted release dates are subject to change.</span></span> <span data-ttu-id="a71ca-173">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การปรับปรุงความพร้อมใช้งานการให้บริการ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=/dynamics365/finance/toc.json)</span><span class="sxs-lookup"><span data-stu-id="a71ca-173">For more information, see [Service update availability](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=/dynamics365/finance/toc.json).</span></span>

| <span data-ttu-id="a71ca-174">วันที่นำออกใช้เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="a71ca-174">Targeted release date</span></span> | <span data-ttu-id="a71ca-175">พร้อมใช้งานโดยทั่วไป (อัปเดตด้วยตนเอง)</span><span class="sxs-lookup"><span data-stu-id="a71ca-175">Generally available (self- updated)</span></span> |
| --- | --- |
| <span data-ttu-id="a71ca-176">10.0.16</span><span class="sxs-lookup"><span data-stu-id="a71ca-176">10.0.16</span></span> | <span data-ttu-id="a71ca-177">22 มกราคม 2021</span><span class="sxs-lookup"><span data-stu-id="a71ca-177">January 22, 2021</span></span> |
| <span data-ttu-id="a71ca-178">10.0.17</span><span class="sxs-lookup"><span data-stu-id="a71ca-178">10.0.17</span></span> | <span data-ttu-id="a71ca-179">1 กุมภาพันธ์ 2021</span><span class="sxs-lookup"><span data-stu-id="a71ca-179">February 1, 2021</span></span> |

