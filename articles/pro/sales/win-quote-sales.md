---
title: ปิดใบเสนอราคา - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการปิดใบเสนอราคาใน Project Operations
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d387816f51f63ecd95df6534c7c012b323e6ddc
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764887"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="2424c-103">ปิดใบเสนอราคา - Lite</span><span class="sxs-lookup"><span data-stu-id="2424c-103">Close a quote - lite</span></span>

<span data-ttu-id="2424c-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="2424c-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2424c-105">การเสนอราคาโครงการสามารถปิดเป็นชนะหรือแพ้</span><span class="sxs-lookup"><span data-stu-id="2424c-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="2424c-106">ใบเสนอราคาแบบร่างสามารถปิดได้เนื่องจาก Microsoft Dynamics 365 Project Operations ไม่รองรับการดำเนินการเปิดใช้งานและแก้ไขใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="2424c-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="2424c-107">ปิดใบเสนอราคาเป็นชนะ</span><span class="sxs-lookup"><span data-stu-id="2424c-107">Close a quote as Won</span></span>

<span data-ttu-id="2424c-108">เมื่อคุณปิดใบเสนอราคาโครงการเป็นชนะ สถานะจะตั้งเป็น ปิด และคำอธิบายรายการของสถานะคือ ชนะ</span><span class="sxs-lookup"><span data-stu-id="2424c-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="2424c-109">การปิดใบเสนอราคาทำให้ใบเสนอราคาโครงการเป็นแบบอ่านอย่างเดียวและสร้างสัญญาโครงการฉบับร่างที่มีข้อมูลใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="2424c-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="2424c-110">เนื่องจากไม่สามารถเปิดใบเสนอราคาปิดใหม่ได้ กล่องโต้ตอบการยืนยันจะยืนยันการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="2424c-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="2424c-111">หากมีการแนบใบเสนอราคาเข้ากับโอกาสทางการขาย ใบเสนอราคาโครงการอื่นๆ เกี่ยวกับโอกาสทางการขายจะถูกปิดเป็นแพ้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2424c-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="2424c-112">ผลกระทบทางการเงินของการปิดใบเสนอราคาเป็นแพ้</span><span class="sxs-lookup"><span data-stu-id="2424c-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="2424c-113">หากมีเวลาจริงในโครงการในขณะที่ยังแนบอยู่กับใบเสนอราคาฉบับร่าง ระบบจะบันทึกเฉพาะต้นทุนของเวลาหรือค่าใช้จ่ายเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2424c-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="2424c-114">หลังจากปิดใบเสนอราคาเป็นชนะ แอปพลิเคชันจะปรับโครงสร้างต้นทุนใหม่โดยการย้อนกลับต้นทุนจริงที่เก่ากว่าและสร้างต้นทุนจริงใหม่ขึ้นมาใหม่</span><span class="sxs-lookup"><span data-stu-id="2424c-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="2424c-115">แอปพลิเคชันจะประมวลผลต้นทุนจริงตามวิธีการเรียกเก็บเงินของรายละเอียดการให้บริการตามสัญญาโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="2424c-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="2424c-116">หากต้นทุนจริงอ้างอิงตามรายละเอียดการให้บริการตามสัญญาเวลาและวัสดุ ยอดขายจริงที่ยังไม่เรียกเก็บเงินที่เกี่ยวข้องจะมีการสร้างเมื่อปิดใบเสนอราคาและมีการสร้างสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="2424c-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="2424c-117">หากต้นทุนจริงอ้างอิงรายละเอียดการให้บริการตามสัญญาราคาคงที่ โปรแกรมประยุกต์จะหยุดประมวลผลต้นทุนจริงที่เป็นไปตามกฎการเรียกเก็บเงินแบบแยกสำหรับลูกค้าตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="2424c-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="2424c-118">การปิดใบเสนอราคาเป็นแพ้:</span><span class="sxs-lookup"><span data-stu-id="2424c-118">Closing a quote as lost:</span></span>

<span data-ttu-id="2424c-119">เมื่อคุณปิดใบเสนอราคาโครงการเป็นแพ้ สถานะจะตั้งเป็น ปิด และคำอธิบายรายการของสถานะคือ แพ้</span><span class="sxs-lookup"><span data-stu-id="2424c-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="2424c-120">การปิดใบเสนอราคาทำให้ใบเสนอราคาโครงการเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="2424c-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="2424c-121">เนื่องจากไม่สามารถเปิดใบเสนอราคาที่ปิดแล้วใหม่ได้และก่อนที่คุณจะปิดใบเสนอราคา กล่องโต้ตอบการยืนยันจะยืนยันการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="2424c-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="2424c-122">หากใบเสนอราคาโครงการที่ปิดเป็น แพ้ อ้างอิงโครงการในบรรทัดใด ๆ โครงการนั้นจะถูกทำเครื่องหมายเป็นปิดด้วย</span><span class="sxs-lookup"><span data-stu-id="2424c-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="2424c-123">การจองทรัพยากรใดๆ นับจากวันนั้นไปจะถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="2424c-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="2424c-124">ใน Project Operations การปิดใบเสนอราคาเป็นชนะหรือแพ้จะไม่ส่งผลกระทบต่อสถานะของโอกาสทางการขาย ซึ่งโอกาสทางการขายจะยังคงเปิดอยู่จนกว่าจะมีการปิดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="2424c-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
