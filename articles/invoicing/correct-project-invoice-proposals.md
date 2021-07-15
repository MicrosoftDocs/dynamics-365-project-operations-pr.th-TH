---
title: แก้ไขการบัญชีบนข้อเสนอใบแจ้งหนี้โครงการฉบับร่าง
description: หัวข้อนี้อธิบายวิธีปรับข้อมูลที่เกี่ยวข้องกับการบัญชีในร่างข้อเสนอใบแจ้งหนี้
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251285"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a><span data-ttu-id="70f95-103">แก้ไขการบัญชีบนข้อเสนอใบแจ้งหนี้โครงการฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="70f95-103">Correct the accounting on draft project invoice proposals</span></span>

<span data-ttu-id="70f95-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="70f95-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="70f95-105">*รายละเอียดการดำเนินงาน* สำหรับใบแจ้งหนี้ของโครงการจะได้รับการดูแลโดยผู้จัดการโครงการในใบแจ้งหนี้ชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="70f95-105">*Operational details* for project invoices are maintained by the project manager on a pro forma invoice.</span></span> <span data-ttu-id="70f95-106">รายละเอียดเหล่านี้รวมถึงการตัดสินใจเกี่ยวกับชั่วโมง ค่าใช้จ่าย วัสดุ หรือเหตุการณ์สำคัญที่ต้องออกใบแจ้งหนี้ อัตรา และการใช้เงินเงินทดรองและค่าธรรมเนียมล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="70f95-106">These details include the decision about the hours, expenses, materials, or milestones that must be invoiced, the rates, and the application of advance and retainer amounts.</span></span> <span data-ttu-id="70f95-107">หลังจากที่คุณยืนยันใบแจ้งหนี้ชั่วคราวต้นฉบับ คุณสามารถปรับรายละเอียดการดำเนินงานได้โดยการสร้างและยืนยัน [ใบแจ้งหนี้ชั่วคราวที่ถูกต้อง](../proforma-invoicing/corrective-invoices.md)</span><span class="sxs-lookup"><span data-stu-id="70f95-107">After you confirm the original pro forma invoice, you can adjust the operational details by creating and confirming a [corrective pro forma invoice](../proforma-invoicing/corrective-invoices.md).</span></span>

<span data-ttu-id="70f95-108">*รายละเอียดการบัญชี* สำหรับใบแจ้งหนี้ของโครงการจะคงอยู่ในเอกสารใบแจ้งหนี้ที่มีการเชื่อมต่อกับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="70f95-108">*Accounting details* for project invoices are maintained in a customer-facing invoice document.</span></span> <span data-ttu-id="70f95-109">รายละเอียดเหล่านี้รวมถึงการคำนวณภาษีขายและมิติทางการเงินที่ใช้กับใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="70f95-109">These details include the sales tax calculation and the financial dimensions that are applied to the invoice.</span></span> <span data-ttu-id="70f95-110">หัวข้อนี้ให้รายละเอียดเกี่ยวกับวิธีการปรับปรุงรายละเอียดทางบัญชีเหล่านี้ในร่างข้อเสนอใบแจ้งหนี้โครงการ</span><span class="sxs-lookup"><span data-stu-id="70f95-110">This topic provides details about how these accounting details can be adjusted on a draft project invoice proposal.</span></span>

## <a name="adjust-sales-tax"></a><span data-ttu-id="70f95-111">ปรับปรุงภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="70f95-111">Adjust sales tax</span></span>

<span data-ttu-id="70f95-112">กลุ่มภาษีขายที่เรียกเก็บเงินเริ่มต้นและกลุ่มภาษีขายตามประเภทสินค้าสามารถปรับปรุงได้โดยตรงในเอกสารข้อเสนอใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="70f95-112">Default billing sales tax groups and item sales tax groups can be adjusted directly on the invoice proposal document.</span></span> <span data-ttu-id="70f95-113">ในการปรับปรุงกลุ่มเหล่านี้ ให้เลือก **แก้ไข** จากนั้นในแต่ละรายการข้อเสนอใบแจ้งหนี้ของโครงการ ให้ป้อนค่าใหม่ในฟิลด์ **กลุ่มภาษีขาย** หรือ **กลุ่มภาษีขายสินค้า**</span><span class="sxs-lookup"><span data-stu-id="70f95-113">To adjust these groups, select **Edit**, and then, on each project invoice proposal line, enter a new value in the **Sales tax group** or **Item sales tax group** field.</span></span>

## <a name="adjust-financial-dimensions"></a><span data-ttu-id="70f95-114">ปรับปรุงมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="70f95-114">Adjust financial dimensions</span></span>

<span data-ttu-id="70f95-115">มิติทางการเงินไม่สามารถแก้ไขได้โดยตรงบนรายการข้อเสนอใบแจ้งหนี้ของโครงการ</span><span class="sxs-lookup"><span data-stu-id="70f95-115">Financial dimensions can't be edited directly on a project invoice proposal line.</span></span> <span data-ttu-id="70f95-116">ให้ทำตามขั้นตอนเหล่านี้เพื่อปรับมิติทางการเงินในข้อเสนอใบแจ้งหนี้ของโครงการแทน</span><span class="sxs-lookup"><span data-stu-id="70f95-116">Instead, follow these steps to adjust financial dimensions on a project invoice proposal.</span></span>

1. <span data-ttu-id="70f95-117">ในข้อเสนอใบแจ้งหนี้โครงการ ให้เลือก **ลบทั้งหมด** เพื่อลบรายการข้อเสนอใบแจ้งหนี้โครงการ</span><span class="sxs-lookup"><span data-stu-id="70f95-117">On the project invoice proposal, select **Delete all** to remove the project invoice proposal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="70f95-118">ปุ่ม **ลบทั้งหมด** ใช้ได้เฉพาะหลังจากที่ผู้ดูแลระบบเปิดใช้งานคุณลักษณะ **ลบรายการข้อเสนอใบแจ้งหนี้เมื่อใช้ Project Operations สำหรับสถานการณ์ตามทรัพยากร/สินค้าที่ไม่ได้เก็บในสต็อก** ในพื้นที่ทำงาน **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="70f95-118">The **Delete all** button is available only after the system administrator enables the **Delete invoice proposal lines when using Project Operations for resource based/ non-stocked scenarios** feature in the **Feature management** workspace.</span></span>

2. <span data-ttu-id="70f95-119">ปรับปรุงมิติทางการเงิน:</span><span class="sxs-lookup"><span data-stu-id="70f95-119">Adjust the financial dimensions:</span></span>

    - <span data-ttu-id="70f95-120">**ธุรกรรมในบัญชี (เหตุการณ์สำคัญการเรียกเก็บเงิน):** ไปที่ **โครงการทั้งหมด** \> **จัดการ** \> **ธุรกรรมในบัญชี** และเลือกเหตุการณ์สำคัญที่ต้องการการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="70f95-120">**On-account transactions (billing milestones):** Go to **All projects** \> **Manage** \> **On-account transactions**, and select the milestone that requires adjustment.</span></span> <span data-ttu-id="70f95-121">จากนั้นบนแท็บ **มิติทางการเงิน** อัปเดตค่าตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="70f95-121">Then, on the **Financial dimensions** tab, update the values as required.</span></span>
    - <span data-ttu-id="70f95-122">**ธุรกรรมเวลา ค่าใช้จ่าย และวัสดุ:** บนหน้า **ธุรกรรมโครงการที่ลงรายการบัญชี** เลือก **ปรับปรุงบัญชี** เพื่อปรับปรุงมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="70f95-122">**Time, expense, and material transactions:** On the **Posted project transactions** page, select **Adjust accounting** to update the financial dimensions.</span></span>

3. <span data-ttu-id="70f95-123">หลังจากที่คุณปรับค่ามิติทางการเงินเสร็จแล้ว ให้ไปที่ **การจัดการโครงการและการบัญชี** \> **เป็นระยะ** \> **การรวม Project Operations** และเลือก **นำเข้าจากตารางการจัดเตรียม** เพื่อเรียกใช้กระบวนการเป็นระยะ</span><span class="sxs-lookup"><span data-stu-id="70f95-123">After you've finished adjusting the financial dimension values, go to **Project management and accounting** \> **Periodic** \> **Project Operations integration**, and select **Import from staging table** to run the periodic process.</span></span> <span data-ttu-id="70f95-124">กระบวนการนั้นใช้ค่ามิติทางการเงินที่ปรับปรุงแล้วเพื่อสร้างรายการข้อเสนอใบแจ้งหนี้ของโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="70f95-124">That process uses the updated financial dimension values to re-create the project invoice proposal lines.</span></span> <span data-ttu-id="70f95-125">ค่าที่ปรับปรุงแล้วจะใช้ในบัญชีแยกประเภทย่อยของโครงการและบัญชีแยกประเภททั่วไปเมื่อมีการลงรายการบัญชีใบแจ้งหนี้ของโครงการ</span><span class="sxs-lookup"><span data-stu-id="70f95-125">The updated values are then used in the project subledger and general ledger when the project invoice is posted.</span></span>
