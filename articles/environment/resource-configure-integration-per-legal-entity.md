---
title: กำหนดค่าการรวม Project Operations ตามนิติบุคคล
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการตั้งค่าการรวมโดยนิติบุคคลใน Project Operations
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096775"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="eb92a-103">กำหนดค่าการรวม Project Operations ตามนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="eb92a-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="eb92a-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="eb92a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="eb92a-105">หัวข้อนี้จะแนะนำคุณตลอดขั้นตอนที่จำเป็นในการกำหนดค่า Dynamics 365 Project Operations ต่อนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="eb92a-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="eb92a-106">เปิดใช้งานคีย์คุณลักษณะใน Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="eb92a-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="eb92a-107">ทำตามขั้นตอนต่อไปนี้เพื่อเปิดใช้งานคุณลักษณะที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="eb92a-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="eb92a-108">ใน Dynamics 365 Finance ไปที่พื้นที่ทำงาน **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="eb92a-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="eb92a-109">ใน **รายการคุณลักษณะ** ค้นหาและเปิดใช้งานคุณลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="eb92a-109">In **Feature list** , find and enable the following features:</span></span>
  
    - <span data-ttu-id="eb92a-110">**เปิดใช้งานรายละเอียดการให้บริการตามสัญญาหลายรายการสำหรับโครงการ**</span><span class="sxs-lookup"><span data-stu-id="eb92a-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="eb92a-111">**เปิดใช้งาน Project Operations บน Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="eb92a-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="eb92a-112">ถ้าคุณไม่เห็น **คีย์คุณลักษณะ** ในรายการ ตรวจสอบว่ารุ่น Finance ของคุณตรงตามข้อกำหนดรุ่นขั้นต่ำหรือไม่ (โปรแกรมประยุกต์รุ่น 10.0.13 ที่ใช้การอัปเดตคุณภาพทั้งหมดหรือสูงกว่า)</span><span class="sxs-lookup"><span data-stu-id="eb92a-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="eb92a-113">เลือก **ตรวจสอบสำหรับการอัปเดต** เพื่อรีเฟรชรายการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="eb92a-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="eb92a-114">กำหนดสถานการณ์จำลองการปรับใช้ Project Operations สำหรับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="eb92a-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="eb92a-115">คุณสามารถเปิดใช้งาน Project Operations ได้บน Dynamics 365 Customer Engagement ในระดับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="eb92a-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="eb92a-116">คุณสามารถมีนิติบุคคลได้หนึ่งแห่งโดยใช้ Project Operations บน Dynamics 365 Customer Engagement สำหรับสถานการณ์ที่อิงตามทรัพยากร / ไม่มีสต็อก</span><span class="sxs-lookup"><span data-stu-id="eb92a-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="eb92a-117">ในสภาพแวดล้อมเดียวกัน คุณสามารถมีนิติบุคคลอื่นโดยใช้ Project Operations สำหรับสถานการณ์จำลองในสต็อก / ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="eb92a-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="eb92a-118">ใน Dynamics 365 Finance ไปที่ **การจัดการโครงการและการบัญชี** > **การตั้งค่า** > **พารามิเตอร์การจัดการโครงการส่วนกลางและการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="eb92a-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="eb92a-119">ในรายการนิติบุคคลที่มี ให้เลือกนิติบุคคลที่รายละเอียดการให้บริการตามสัญญาและ Project Operations หลายรายการบนคุณลักษณะ Dynamics 365 Customer Engagement จะถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="eb92a-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="eb92a-120">ปล่อยให้นิติบุคคลที่จะใช้ Project Operations สำหรับสถานการณ์จำลองในสต็อก / ใบสั่งผลิตไม่ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="eb92a-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="eb92a-121">นิติบุคคลสามารถเลือกได้ก็ต่อเมื่อไม่มีโครงการอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="eb92a-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="eb92a-122">กำหนดค่าพารามิเตอร์การจัดการโครงการและการบัญชี</span><span class="sxs-lookup"><span data-stu-id="eb92a-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="eb92a-123">นิติบุคคลแต่ละรายที่ใช้ Project Operations บน Dynamics 365 Customer Engagement ต้องการชุดพารามิเตอร์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="eb92a-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="eb92a-124">พารามิเตอร์เหล่านี้ได้รับการกำหนดค่าบนแท็บ **Project Operations** บนหน้า **พารามิเตอร์การจัดการโครงการและการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="eb92a-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="eb92a-125">พารามิเตอร์คือ:</span><span class="sxs-lookup"><span data-stu-id="eb92a-125">The parameters are:</span></span>

  - <span data-ttu-id="eb92a-126">**ค่าเริ่มต้นชนิดการเรียกเก็บเงิน** : Project Operations ใช้ชุดค่าเริ่มต้นของชนิดการเรียกเก็บเงินคงที่ ซึ่งต้องแมปกับคุณสมบัติรายการ Finance</span><span class="sxs-lookup"><span data-stu-id="eb92a-126">**Billing type defaults** : Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="eb92a-127">สร้างเรกคอร์ดสำหรับการเรียกเก็บเงินแต่ละชนิด: **ไม่ระบุ** **คิดค่าบริการ** **ไม่คิดเงิน** **ฟรี** และ **ไม่สามารถใช้ได้**</span><span class="sxs-lookup"><span data-stu-id="eb92a-127">Create a record for each billing type: **Not specified** , **Chargeable** , **Non-chargeable** , **Complimentary** , and **Not available**.</span></span>
  - <span data-ttu-id="eb92a-128">**ค่าเริ่มต้นชนิดโครงการ** : เลือกประเภทโครงการเริ่มต้นที่จะใช้สำหรับธุรกรรมแต่ละชนิด</span><span class="sxs-lookup"><span data-stu-id="eb92a-128">**Project category defaults** : Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="eb92a-129">ค่าเริ่มต้นเหล่านี้จะถูกใช้ใน **สมุดรายวันเกี่ยวกับการรวม Project Operations** และในการประมาณการที่ไม่มีการระบุประเภทธุรกรรมสำหรับโครงการจริง</span><span class="sxs-lookup"><span data-stu-id="eb92a-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="eb92a-130">**การคาดการณ์** : เลือกแบบจำลองการคาดการณ์ที่จะใช้สำหรับเวลาและค่าใช้จ่ายโดยประมาณ</span><span class="sxs-lookup"><span data-stu-id="eb92a-130">**Forecasts** : Select the forecast model to be used for time and expense estimates.</span></span>
