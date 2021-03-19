---
title: ภาพรวมกระบวนการออกใบแจ้งหนี้
description: หัวข้อนี้ให้ภาพรวมกระบวนการของการออกใบแจ้งหนี้ใน Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในคลัง
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9dc424cf69abfccc10bf551272a14e5cefb3dff0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275831"
---
# <a name="invoicing-process-overview"></a><span data-ttu-id="cad32-103">ภาพรวมกระบวนการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="cad32-103">Invoicing process overview</span></span>

<span data-ttu-id="cad32-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="cad32-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cad32-105">Project Operations สำหรับสถานการณ์จำลองตามทรัพยากร/ที่ไม่ได้เก็บในคลัง นำเสนอความสามารถที่ครอบคลุมซึ่งปรับแต่งให้เหมาะกับความต้องการของทั้งผู้จัดการโครงการและเสมียน/นักบัญชีโครงการของบัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="cad32-105">Project Operations for resource/non-stocked based scenarios offers comprehensive capabilities tailored to fit the needs of both Project manager and Accounts receivable clerk/project accountant.</span></span> <span data-ttu-id="cad32-106">สำหรับกระบวนการออกใบแจ้งหนี้ ผู้จัดการโครงการจะจัดการรายการที่ค้างอยู่ในการเรียกเก็บเงินของโครงการ และเสมียน/นักบัญชีโครงการของบัญชีลูกหนี้จะสร้างเอกสารใบแจ้งหนี้ที่ตรงตามข้อกำหนดและที่ติดต่อกับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cad32-106">For the invoicing process, the Project manager manages the project billing backlog and the Accounts receivable clerk/project accountant creates a compliant and accurate customer-facing invoice document.</span></span>

![ไดอะแกรมโฟลว์การออกใบแจ้งหนี้](./media/invoicing-flow.png)

<span data-ttu-id="cad32-108">รายละเอียดการให้บริการตามสัญญาโครงการ จะกำหนดวิธีการเรียกเก็บเงินสำหรับธุรกรรมโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="cad32-108">The project contract line defines the billing method for associated project transactions.</span></span> <span data-ttu-id="cad32-109">เมื่อผู้จัดการโครงการอนุมัติธุรกรรมเวลาและค่าใช้จ่าย ระบบจะบันทึกธุรกรรมในเอนทิตี **ข้อมูลจริงของโครงการ** และส่งข้อมูลไปยังโมดูล **การจัดการโครงการและการบัญชี** ใน Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="cad32-109">When the Project manager approves time and expense transactions, the system records the transactions in the **Project Actuals** entity and sends the information to the **Project management and accounting** module in Dynamics 365 Finance.</span></span> <span data-ttu-id="cad32-110">จากนั้น นักบัญชีโครงการจะตรวจสอบและลงรายการบัญชีโดยใช้ [สมุดรายวัน Project Operations Integration](../project-accounting/project-operations-integration-journal.md)</span><span class="sxs-lookup"><span data-stu-id="cad32-110">The Project accountant then reviews and posts the records using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="cad32-111">สมุดรายวันนี้มีรายละเอียดการบัญชีที่สำคัญสำหรับข้อมูลจริงของโครงการ เช่น การเรียกเก็บเงิน กลุ่มภาษีขาย กลุ่มภาษีขายของรายการเรียกเก็บเงิน และมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="cad32-111">This journal includes important accounting details for project actuals, such as billing, sales tax group, billing item sales tax group, and financial dimensions.</span></span>

<span data-ttu-id="cad32-112">ผู้จัดการโครงการสามารถตรวจสอบธุรกรรมการขายที่ยังไม่เรียกเก็บเงินโดยใช้วิธีการเวลาและการเรียกเก็บเงินวัสดุใน [เวลาและรายการคงค้างของการเรียกเก็บเงินวัสดุ](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) และการเรียกเก็บเงินราคาคงที่ใน [เหตุการณ์สำคัญของราคาคงที่](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones)</span><span class="sxs-lookup"><span data-stu-id="cad32-112">The Project manager can review unbilled sales transactions using the time and material billing method in the [Time and material billing backlog](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) and fixed price billing in [Fixed price milestones](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones).</span></span> <span data-ttu-id="cad32-113">มุมมองเหล่านี้ช่วยให้คุณสามารถกรองและเลือกธุรกรรมที่ต้องรวมไว้ในรอบการเรียกเก็บเงินถัดไป และจากนั้น ทำเครื่องหมายเป็น **พร้อมที่จะออกใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="cad32-113">These views allow you to filter and select transactions that need to be included in the next billing cycle and then mark them as **Ready to Invoice**.</span></span>

<span data-ttu-id="cad32-114">คุณสามารถ [สร้างใบแจ้งหนี้ชั่วคราวด้วยตนเอง](../proforma-invoicing/create-manual-proforma-invoice.md) หรือใช้ [กระบวนการเป็นระยะ](../proforma-invoicing/configure-automated-invoice-creation.md)</span><span class="sxs-lookup"><span data-stu-id="cad32-114">You can [manually create a proforma invoice](../proforma-invoicing/create-manual-proforma-invoice.md) or use a [periodic process](../proforma-invoicing/configure-automated-invoice-creation.md).</span></span> <span data-ttu-id="cad32-115">ผู้จัดการโครงการสามารถ [ปรับใบแจ้งหนี้ชั่วคราวแบบร่าง](../proforma-invoicing/manage-proforma-invoice.md) ตามต้องการ แล้วจากนั้น ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="cad32-115">The Project manager can [adjust a draft proforma invoice](../proforma-invoicing/manage-proforma-invoice.md) as needed and then confirm it.</span></span>

<span data-ttu-id="cad32-116">ใบแจ้งหนี้ชั่วคราวที่ยืนยันแล้วจะถูกส่งไปยังโมดูล **การจัดการโครงการและการบัญชี** ใน Finance</span><span class="sxs-lookup"><span data-stu-id="cad32-116">The confirmed proforma invoice is sent to the **Project management and accounting** module in Finance.</span></span> <span data-ttu-id="cad32-117">นักบัญชีโครงการจัดรูปแบบและปรับปรุงข้อเสนอใบแจ้งหนี้โครงการ และจากนั้น ลงรายการบัญชีและพิมพ์เอกสาร</span><span class="sxs-lookup"><span data-stu-id="cad32-117">The Project accountant formats and updates the project invoice proposal, and then posts and prints the document.</span></span> <span data-ttu-id="cad32-118">ใบแจ้งหนี้โครงการที่ลงรายการบัญชีแล้วจะถูกบันทึกไว้ในบัญชีแยกประเภททั่วไป เช่นเดียวกับบัญชีแยกประเภทย่อยของลูกค้าและโครงการ</span><span class="sxs-lookup"><span data-stu-id="cad32-118">Posted project invoices are recorded in the General ledger, as well as the Customer and Project subledgers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]