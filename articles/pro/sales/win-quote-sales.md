---
title: ปิดใบเสนอราคา - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการปิดใบเสนอราคาใน Project Operations
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175734"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="a8295-103">ปิดใบเสนอราคา - Lite</span><span class="sxs-lookup"><span data-stu-id="a8295-103">Close a quote - lite</span></span>

<span data-ttu-id="a8295-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="a8295-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a8295-105">การเสนอราคาโครงการสามารถปิดเป็นชนะหรือแพ้</span><span class="sxs-lookup"><span data-stu-id="a8295-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="a8295-106">ไม่รองรับการดำเนินการเปิดใช้งานและแก้ไขในใบเสนอราคาใน Microsoft Dynamics 365 Project Operations ดังนั้นจึงสามารถปิดใบเสนอราคาแบบร่างได้</span><span class="sxs-lookup"><span data-stu-id="a8295-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="a8295-107">ปิดใบเสนอราคาเป็นชนะ</span><span class="sxs-lookup"><span data-stu-id="a8295-107">Close a quote as Won</span></span>

<span data-ttu-id="a8295-108">การปิดใบเสนอราคาโครงการเป็นชนะจะปิดใบเสนอราคาโดยตั้งค่าสถานะเป็นปิดแล้วและคำอธิบายรายการของสถานะตั้งค่าเป็นชนะ</span><span class="sxs-lookup"><span data-stu-id="a8295-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="a8295-109">การปิดใบเสนอราคาทำให้ใบเสนอราคาโครงการเป็นแบบอ่านอย่างเดียวและสร้างสัญญาโครงการฉบับร่างที่มีข้อมูลใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="a8295-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="a8295-110">เนื่องจากไม่สามารถเปิดใบเสนอราคาที่ปิดใหม่ได้ กล่องโต้ตอบการยืนยันจะมีกล่องโต้ตอบการยืนยันก่อนที่การเปลี่ยนแปลงจะเสร็จสิ้น เนื่องจากไม่สามารถเปิดใบเสนอราคาที่ปิดใหม่ได้และการเปลี่ยนแปลงจะไม่สามารถย้อนกลับได้</span><span class="sxs-lookup"><span data-stu-id="a8295-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="a8295-111">หากมีการแนบใบเสนอราคาเข้ากับโอกาสทางการขาย ใบเสนอราคาโครงการอื่นๆ เกี่ยวกับโอกาสทางการขายจะถูกปิดเป็นแพ้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a8295-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="a8295-112">ผลกระทบทางการเงินของการปิดใบเสนอราคาเป็นแพ้</span><span class="sxs-lookup"><span data-stu-id="a8295-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="a8295-113">หากมีการบันทึกเวลาจริงไว้ในโครงการในขณะที่ยังแนบอยู่กับใบเสนอราคาแบบร่าง ระบบจะบันทึกเฉพาะต้นทุนของเวลาหรือค่าใช้จ่ายเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a8295-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="a8295-114">หลังจากปิดใบเสนอราคาเป็นชนะ แอปพลิเคชันจะปรับโครงสร้างต้นทุนใหม่โดยการย้อนกลับต้นทุนจริงที่เก่ากว่าและสร้างต้นทุนจริงใหม่ขึ้นมาใหม่</span><span class="sxs-lookup"><span data-stu-id="a8295-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="a8295-115">แอปพลิเคชันจะประมวลผลต้นทุนจริงตามวิธีการเรียกเก็บเงินของรายละเอียดการให้บริการตามสัญญาโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="a8295-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="a8295-116">หากต้นทุนจริงอ้างอิงตามเวลาและรายละเอียดการให้บริการตามสัญญาวัสดุ ระบบจะสร้างยอดขายจริงที่ยังไม่เรียกเก็บเงินที่สอดคล้องกันโดยอัตโนมัติเมื่อปิดใบเสนอราคาและมีการสร้างสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="a8295-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="a8295-117">หากต้นทุนจริงอ้างอิงรายละเอียดการให้บริการตามสัญญาที่มีราคาคงที่ แอปพลิเคชันจะหยุดประมวลผลต้นทุนจริงตามกฎการเรียกเก็บเงินแบบแบ่งจ่ายสำหรับลูกค้าสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="a8295-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="a8295-118">การปิดใบเสนอราคาเป็นแพ้:</span><span class="sxs-lookup"><span data-stu-id="a8295-118">Closing a quote as lost:</span></span>

<span data-ttu-id="a8295-119">การปิดใบเสนอราคาโครงการเป็น แพ้ จะตั้งสถานะเป็น ปิดแล้ว และคำอธิบายรายการของสถานะเป็นแพ้</span><span class="sxs-lookup"><span data-stu-id="a8295-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="a8295-120">การปิดใบเสนอราคาทำให้ใบเสนอราคาโครงการเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="a8295-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="a8295-121">เนื่องจากไม่สามารถเปิดใบเสนอราคาที่ปิดแล้วใหม่ได้และก่อนที่คุณจะปิดใบเสนอราคา กล่องโต้ตอบการยืนยันจะยืนยันการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="a8295-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="a8295-122">หากการเสนอราคาโครงการที่ปิดเป็นแพ้ มีโครงการที่อ้างอิงในรายการใดๆ โครงการนั้นจะถูกทำเครื่องหมายเป็นปิดแล้ว และการจองทรัพยากรใดๆ นับจากวันนั้นจะถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="a8295-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="a8295-123">ใน Project Operations การปิดใบเสนอราคาเป็นชนะหรือแพ้จะไม่ส่งผลกระทบต่อสถานะของโอกาสทางการขาย ซึ่งโอกาสทางการขายจะยังคงเปิดอยู่จนกว่าจะมีการปิดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a8295-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
