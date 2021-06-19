---
title: ชุดการอนุมัติ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับชุดการอนุมัติ คำขอ และชุดย่อยของการดำเนินการเหล่านั้น
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116894"
---
# <a name="approval-sets"></a><span data-ttu-id="63a45-103">ชุดการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="63a45-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="63a45-104">การอนุมัติจะกำหนดคำขออนุมัติกลุ่มไว้ด้วยกันเป็นส่วนย่อยของการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="63a45-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="63a45-105">การจัดกลุ่มนี้อนุญาตให้ประมวลผลการอนุมัติตามลำดับตามโครงการและอนุญาตให้ลองใหม่และจัดลำดับ</span><span class="sxs-lookup"><span data-stu-id="63a45-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="63a45-106">การจัดกลุ่มช่วยเพิ่มความน่าเชื่อถือและความสามารถในการตรวจสอบย้อนกลับของการประมวลผลการอนุมัติสำหรับการอนุมัติปริมาณมาก</span><span class="sxs-lookup"><span data-stu-id="63a45-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="63a45-107">ชุดการอนุมัติระบุสถานะการประมวลผลโดยรวมของเรกคอร์ดที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="63a45-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="63a45-108">เมื่อมีการประมวลผลเรกคอร์ดการอนุมัติโดยใช้ชุดการอนุมัติ เรกคอร์ดจะย้ายจาก **ส่ง** เป็น **อนุมัติ** และถูกยกเลิกการเชื่อมโยงจากชุดการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="63a45-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="63a45-109">หากเรกคอร์ดล้มเหลวเมื่อส่งเพื่อขออนุมัติ เรกคอร์ดจะยังคงอยู่ในสถานะ **ส่ง** และชุดการอนุมัติถูกทำเครื่องหมายว่าล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="63a45-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="63a45-110">ชุดการอนุมัติจะบันทึกข้อความแสดงข้อผิดพลาดของความล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="63a45-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="63a45-111">การประมวลผลการอนุมัติและชุดการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="63a45-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="63a45-112">การอนุมัติที่อยู่ในคิวสำหรับการประมวลผลจะปรากฏในมุมมอง **การประมวลผลการอนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="63a45-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="63a45-113">ระบบพยายามประมวลผลรายการทั้งหมดหลายครั้งแบบอะซิงโครนัส รวมถึงการลองอนุมัติอีกครั้งหากความพยายามครั้งก่อนล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="63a45-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="63a45-114">ฟิลด์ **อายุการใช้งานชุดการอนุมัติ** จะบันทึกจำนวนครั้งที่เหลือในการประมวลผลชุดก่อนที่จะถูกทำเครื่องหมายว่าล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="63a45-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="63a45-115">การอนุมัติและชุดการอนุมัติล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="63a45-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="63a45-116">มุมมอง **การอนุมัติล้มเหลว** แสดงการอนุมัติทั้งหมดที่ต้องมีการแทรกแซงจากผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="63a45-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="63a45-117">เปิดบันทึกชุดการอนุมัติที่เกี่ยวข้องเพื่อระบุสาเหตุของความล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="63a45-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="63a45-118">การเลือก **ลองอีกครั้ง** เพิ่มการนับอายุการใช้งานชุดการอนุมัติ ย้ายชุดการอนุมัติกลับเป็นสถานะ **กำลังดำเนินการ** และพยายามประมวลผลเรกคอร์ดที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="63a45-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="63a45-119">กำหนดค่าชุดการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="63a45-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="63a45-120">เปิดใช้งานคุณสมบัติชุดการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="63a45-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="63a45-121">ก่อนที่คุณจะเปิดใช้งานคุณลักษณะชุดการอนุมัติ ให้ตรวจสอบว่าไม่มีการอนุมัติที่กำลังดำเนินการอยู่</span><span class="sxs-lookup"><span data-stu-id="63a45-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="63a45-122">ไปที่หน้า **พารามิเตอร์โครงการ** และเลือก **การควบคุมคุณลักษณะ** > **เปิดใช้งานการอนุมัติสมัยใหม่**</span><span class="sxs-lookup"><span data-stu-id="63a45-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="63a45-123">ปิดใช้งานคุณสมบัติชุดการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="63a45-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="63a45-124">ก่อนที่คุณจะปิดใช้งานคุณลักษณะชุดการอนุมัติ ให้ตรวจสอบว่าไม่มีการอนุมัติที่กำลังดำเนินการอยู่</span><span class="sxs-lookup"><span data-stu-id="63a45-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="63a45-125">ไปที่หน้า **พารามิเตอร์โครงการ** และเลือก **การควบคุมคุณลักษณะ** > **ปิดใช้งานการอนุมัติสมัยใหม่**</span><span class="sxs-lookup"><span data-stu-id="63a45-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="63a45-126">การกำหนดค่าขีดจำกัดแบบอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="63a45-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="63a45-127">เมื่อมีการสร้างชุดการอนุมัติ การประมวลผลจะย้ายไปเบื้องหลังเมื่อจำนวนเรกคอร์ดที่เลือกสำหรับการอนุมัติเกินเกณฑ์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="63a45-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="63a45-128">ใช้ฟิลด์ **เกณฑ์แบบอะซิงโครนัส** เพื่อกำหนดค่าเมื่อการประมวลผลการอนุมัติควรทำงานแบบซิงโครนัสหรืออะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="63a45-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="63a45-129">ค่าที่ใช้ได้คือ:</span><span class="sxs-lookup"><span data-stu-id="63a45-129">Valid values are:</span></span>

  - <span data-ttu-id="63a45-130">ศูนย์: คำขอทั้งหมดควรได้รับการประมวลผลแบบอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="63a45-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="63a45-131">ตัวเลขที่มากกว่าศูนย์: การอนุมัติจะได้รับการประมวลผลแบบอะซิงโครนัสเฉพาะเมื่อจำนวนการอนุมัติที่ส่งเกินค่านี้</span><span class="sxs-lookup"><span data-stu-id="63a45-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
