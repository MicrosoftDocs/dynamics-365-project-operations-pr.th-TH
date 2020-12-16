---
title: ค่าเริ่มต้นของมิติทางการเงิน
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีตั้งค่าเริ่มต้นมิติทางการเงิน
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 03b9a9028c1610b191db9c1bfb0163adc88bdf3e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642386"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="e59ec-103">ค่าเริ่มต้นของมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e59ec-103">Financial dimension defaults</span></span>

<span data-ttu-id="e59ec-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="e59ec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e59ec-105">Dynamics 365 Project Operations ใช้กรอบงาน [มิติทางการเงิน](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) ใน Dynamics 365 Finance เพื่อให้ข้อมูลเชิงลึกเพิ่มเติมเกี่ยวกับการทำธุรกรรมบัญชีแยกประเภทย่อยและบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="e59ec-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="e59ec-106">มิติทางการเงินเริ่มต้นสามารถตั้งค่าบนลูกค้า แหล่งเงินทุนของโครงการ หลักเป้าหมาย รายละเอียดการให้บริการตามสัญญาโครงการ หรือโครงการ</span><span class="sxs-lookup"><span data-stu-id="e59ec-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="e59ec-107">กำหนดมิติทางการเงินเริ่มต้นสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e59ec-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="e59ec-108">ค่าเริ่มต้นของมิติลูกค้าระบุไว้ใน Finance</span><span class="sxs-lookup"><span data-stu-id="e59ec-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="e59ec-109">ดำเนินการขั้นตอนต่อไปนี้เพื่อตั้งค่ามิติให้สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="e59ec-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="e59ec-110">ไปที่ **บัญชีลูกหนี้** > **ลูกค้า** > **ลูกค้าทุกท่าน**</span><span class="sxs-lookup"><span data-stu-id="e59ec-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="e59ec-111">บนหน้า **ลูกค้า** บนแท็บ **มิติทางการเงิน** ตั้งค่ามิติทางการเงินสำหรับลูกค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="e59ec-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="e59ec-112">กำหนดมิติทางการเงินเริ่มต้นสำหรับสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="e59ec-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="e59ec-113">สัญญาโครงการถูกสร้างและเก็บใน Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="e59ec-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="e59ec-114">แอตทริบิวต์การบัญชีสำหรับสัญญาโครงการกำหนดไว้ในโมดูล **การจัดการโครงการและการบัญชี** ใน Finance</span><span class="sxs-lookup"><span data-stu-id="e59ec-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="e59ec-115">ตั้งค่ามิติทางการเงินสำหรับแหล่งเงินทุนของโครงการ</span><span class="sxs-lookup"><span data-stu-id="e59ec-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="e59ec-116">ไปที่ **การจัดการและการบัญชีโครงการ** > **โครงการ** > **สัญญาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="e59ec-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="e59ec-117">เลือกเรกคอร์ดที่คุณต้องการอัปเดต และบนแท็บ **สัญญาโครงการ** เลือก **แสดงการบัญชีเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="e59ec-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="e59ec-118">ขยาย **ข้อมูลที่เกี่ยวข้อง** และเลือกแท็บ **แหล่งเงินทุน**</span><span class="sxs-lookup"><span data-stu-id="e59ec-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="e59ec-119">ตั้งค่าเริ่มต้นของมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e59ec-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="e59ec-120">โปรดสังเกตว่ามิติทางการเงินเริ่มต้นจากบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e59ec-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="e59ec-121">ตั้งค่ามิติทางการเงินสำหรับรายละเอียดการให้บริการตามสัญญาของโครงการ</span><span class="sxs-lookup"><span data-stu-id="e59ec-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="e59ec-122">ไปที่ **การจัดการและการบัญชีโครงการ** > **โครงการ** > **สัญญาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="e59ec-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="e59ec-123">เลือกเรกคอร์ดที่คุณต้องการอัปเดต และบนแท็บ **สัญญาโครงการ** เลือก **แสดงการบัญชีเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="e59ec-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="e59ec-124">ขยาย **ข้อมูลที่เกี่ยวข้อง** และเลือกแท็บ **รายละเอียดการให้บริการตามสัญญา**</span><span class="sxs-lookup"><span data-stu-id="e59ec-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="e59ec-125">ตั้งค่าเริ่มต้นของมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e59ec-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="e59ec-126">ค่าเริ่มต้นของมิติทางการเงินมีผลบังคับใช้และสามารถใช้ได้กับรายละเอียดการให้บริการตามสัญญาแบบราคาคงที่ (หลักเป้าหมาย) เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e59ec-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="e59ec-127">ค่าเริ่มต้นเหล่านี้ใช้กับธุรกรรมในบัญชีและรายการใบแจ้งหนี้ของโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="e59ec-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="e59ec-128">กำหนดมิติทางการเงินเริ่มต้นสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="e59ec-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="e59ec-129">โครงการถูกสร้างและเก็บใน (CDS)</span><span class="sxs-lookup"><span data-stu-id="e59ec-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="e59ec-130">แอตทริบิวต์การบัญชีสำหรับโครงการกำหนดไว้ในโมดูล **การจัดการโครงการและการบัญชี** ใน Finance</span><span class="sxs-lookup"><span data-stu-id="e59ec-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="e59ec-131">ไปที่ **การจัดการและการบัญชีโครงการ** > **โครงการ** > **โครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="e59ec-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="e59ec-132">เลือกเรกคอร์ดที่คุณต้องการอัปเดต และบนแท็บ **โครงการ** เลือก **แสดงการบัญชีเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="e59ec-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="e59ec-133">ขยาย **ข้อมูลที่เกี่ยวข้อง** และเลือกแท็บ **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="e59ec-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="e59ec-134">ตั้งค่าเริ่มต้นของมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e59ec-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="e59ec-135">โปรดสังเกตว่ามิติทางการเงินเริ่มต้นจากบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e59ec-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="e59ec-136">ถ้าโครงการเชื่อมโยงกับรายละเอียดการให้บริการตามสัญญากับลูกค้าตามสัญญาโครงการหลายราย ลูกค้าหลักจะถูกใช้เพื่อเริ่มต้นมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e59ec-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="e59ec-137">มิติทางการเงินเริ่มต้นของโครงการถูกใช้เพื่อตั้งค่าเริ่มต้นของรายการสมุดรายวันสำหรับเวลา ค่าใช้จ่าย และธุรกรรมค่าธรรมเนียมใน **สมุดรายวันการรวม Project Operations** และในรายการใบแจ้งหนี้โครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="e59ec-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>
