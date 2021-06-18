---
title: ปิดใบเสนอราคา
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการปิดใบเสนอราคาใน Project Operations
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3f46bf61bc3e492a648d65e86750a25609d5ab7a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995959"
---
# <a name="close-a-quote"></a><span data-ttu-id="3e560-103">ปิดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="3e560-103">Close a quote</span></span>

<span data-ttu-id="3e560-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="3e560-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3e560-105">การเสนอราคาโครงการสามารถปิดเป็นชนะหรือแพ้</span><span class="sxs-lookup"><span data-stu-id="3e560-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="3e560-106">เนื่องจากฟังก์ชัน เริ่มการใช้งาน และ ทบทวน ไม่รองรับสำหรับใบเสนอราคาใน Microsoft Dynamics 365 Project Operations คุณสามารถปิดใบเสนอราคาฉบับร่างได้</span><span class="sxs-lookup"><span data-stu-id="3e560-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="3e560-107">ปิดใบเสนอราคาเป็นชนะ</span><span class="sxs-lookup"><span data-stu-id="3e560-107">Close a quote as Won</span></span>

<span data-ttu-id="3e560-108">การปิดใบเสนอราคาโครงการเป็นชนะจะตั้งค่าใบเสนอราคาเป็น **ปิดแล้ว** และคำอธิบายรายการของสถานะเป็น **ชนะ**</span><span class="sxs-lookup"><span data-stu-id="3e560-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="3e560-109">การปิดใบเสนอราคาทำให้ใบเสนอราคาโครงการเป็นแบบอ่านอย่างเดียวและสร้างสัญญาโครงการฉบับร่างที่มีข้อมูลใบเสนอราคาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3e560-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="3e560-110">เนื่องจากไม่สามารถเปิดใบเสนอราคาที่ปิดแล้วใหม่ได้ ก่อนที่คุณจะปิดใบเสนอราคา กล่องโต้ตอบการยืนยันจะยืนยันการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="3e560-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="3e560-111">นอกจากนี้ สัญญาโครงการที่สร้างขึ้นจากใบเสนอราคาโครงการยังมีอยู่ในโมดูลการจัดการและการบัญชีโครงการของ Project Operations</span><span class="sxs-lookup"><span data-stu-id="3e560-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="3e560-112">หากไม่มีการแม็ปสัญญาโครงการกับโครงการในรายการใดๆ สัญญาโครงการนี้จะมีอยู่เป็นสัญญาโครงการที่ไม่ใช้งานและจะกลับมาใช้งานได้ทันทีที่มีการจับคู่โครงการกับรายละเอียดการให้บริการตามสัญญาอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="3e560-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="3e560-113">หากมีการแนบใบเสนอราคาเข้ากับโอกาสทางการขาย ใบเสนอราคาโครงการอื่นๆ เกี่ยวกับโอกาสทางการขายจะถูกปิดเป็นแพ้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3e560-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="3e560-114">ผลกระทบทางการเงินของการปิดใบเสนอราคาเป็นแพ้</span><span class="sxs-lookup"><span data-stu-id="3e560-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="3e560-115">หากมีการบันทึกเวลาจริงไว้ในโครงการในขณะที่ยังแนบอยู่กับใบเสนอราคาแบบร่าง ระบบจะบันทึกเฉพาะต้นทุนของเวลาหรือค่าใช้จ่ายเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3e560-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="3e560-116">หลังจากปิดใบเสนอราคาเป็นชนะ แอปพลิเคชันจะปรับโครงสร้างต้นทุนใหม่โดยการย้อนกลับต้นทุนจริงที่เก่ากว่าและสร้างต้นทุนจริงใหม่ขึ้นมาใหม่</span><span class="sxs-lookup"><span data-stu-id="3e560-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="3e560-117">แอปพลิเคชันจะประมวลผลต้นทุนจริงตามวิธีการเรียกเก็บเงินของรายละเอียดการให้บริการตามสัญญาโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3e560-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="3e560-118">หากต้นทุนจริงอ้างอิงตามเวลาและรายละเอียดการให้บริการตามสัญญาวัสดุ ระบบจะสร้างยอดขายจริงที่ยังไม่เรียกเก็บเงินที่สอดคล้องกันโดยอัตโนมัติเมื่อปิดใบเสนอราคาและมีการสร้างสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="3e560-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="3e560-119">หากต้นทุนจริงอ้างอิงรายละเอียดการให้บริการตามสัญญาที่มีราคาคงที่ แอปพลิเคชันจะหยุดประมวลผลต้นทุนจริงตามกฎการเรียกเก็บเงินแบบแบ่งจ่ายสำหรับลูกค้าสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="3e560-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="3e560-120">ข้อมูลจริงที่ประมวลผลซ้ำทั้งหมดมีอยู่ในโมดูลการจัดการและการบัญชีโครงการสำหรับให้นักบัญชีโครงการตรวจสอบ ปรับปรุง และลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="3e560-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="3e560-121">ปิดใบเสนอราคาเป็นแพ้</span><span class="sxs-lookup"><span data-stu-id="3e560-121">Close a quote as Lost</span></span>

<span data-ttu-id="3e560-122">การปิดใบเสนอราคาโครงการเป็น แพ้ จะตั้งค่าสถานะเป็น **ปิดแล้ว** และคำอธิบายรายการของสถานะเป็น **แพ้**</span><span class="sxs-lookup"><span data-stu-id="3e560-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="3e560-123">การปิดใบเสนอราคาจะทำให้เป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="3e560-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="3e560-124">เนื่องจากไม่สามารถเปิดใบเสนอราคาที่ปิดแล้วใหม่ได้และก่อนที่คุณจะปิดใบเสนอราคา กล่องโต้ตอบการยืนยันจะยืนยันการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="3e560-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="3e560-125">หากการเสนอราคาโครงการที่ปิดเป็นแพ้ มีโครงการที่อ้างอิงในรายการใดๆ โครงการนั้นจะถูกทำเครื่องหมายเป็นปิดแล้ว และการจองทรัพยากรใดๆ นับจากวันนั้นจะถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="3e560-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="3e560-126">ใน Project Operations การปิดใบเสนอราคาเป็นชนะหรือแพ้จะไม่ส่งผลกระทบต่อสถานะของโอกาสทางการขาย ซึ่งโอกาสทางการขายจะยังคงเปิดอยู่จนกว่าจะมีการปิดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="3e560-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]