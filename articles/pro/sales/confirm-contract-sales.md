---
title: ยืนยันสัญญาโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการยืนยันสัญญาใน Project Operations
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: babce9c64098a9c87072786d914d2340251a8986
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086052"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="94565-103">ยืนยันสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="94565-103">Confirm a project contract</span></span>

<span data-ttu-id="94565-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="94565-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="94565-105">สัญญาโครงการใน Dynamics 365 Project Operations สามารถใช้งานได้ด้วยเหตุผลของการ **ได้รับการยืนยัน** หรือปิดด้วยเหตุผลของการ **แพ้**</span><span class="sxs-lookup"><span data-stu-id="94565-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed** , or closed with a reason of **Lost**.</span></span> <span data-ttu-id="94565-106">เมื่อคุณยืนยันสัญญาโครงการ สถานะจะอัปเดตจาก **แบบร่าง** เป็น **ใช้งาน** และคำอธิบายรายการของสถานะคือ **ได้รับการยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="94565-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="94565-107">ไม่สามารถแก้ไขหรือเปิดสัญญาที่ใช้งานอยู่หรือปิดได้</span><span class="sxs-lookup"><span data-stu-id="94565-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="94565-108">ผลกระทบทางการเงินของการยืนยันสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="94565-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="94565-109">หลังจากยืนยันสัญญาโครงการ แอปพลิเคชันจะคำนวนต้นทุนใหม่โดยการย้อนกลับต้นทุนจริงที่เก่ากว่าและสร้างต้นทุนจริงใหม่ขึ้นมาใหม่</span><span class="sxs-lookup"><span data-stu-id="94565-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="94565-110">ต้นทุนจริงใหม่จะประมวลผลตามวิธีการเรียกเก็บเงินของรายละเอียดการให้บริการตามสัญญาโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="94565-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="94565-111">หากต้นทุนจริงอ้างอิงตามรายละเอียดการให้บริการตามสัญญาเวลาและวัสดุ แอปพลิเคชันจะสร้างการขายที่ยังไม่เรียกเก็บเงินตามจริงขึ้นมาใหม่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="94565-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="94565-112">หากต้นทุนจริงอ้างอิงรายละเอียดการให้บริการตามสัญญาราคาคงที่ แอปพลิเคชันจะหยุดประมวลผลต้นทุนจริงอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="94565-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="94565-113">วงเงินที่ต้องไม่เกิน การตั้งค่าความสามารถในการเรียกเก็บเงินและการกำหนดราคาและต้นทุนตามจริงจะได้รับการประเมินแล้วอัปเดตเป็นส่วนหนึ่งของกระบวนการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="94565-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="94565-114">ปิดสัญญาโครงการเป็นแพ้</span><span class="sxs-lookup"><span data-stu-id="94565-114">Close a project contract as lost</span></span>

<span data-ttu-id="94565-115">เมื่อคุณปิดสัญญาโครงการเป็นแพ้ สถานะสัญญาจะอัปเดตเป็น **ปิด** และคำอธิบายรายการของสถานะคือ **แพ้**</span><span class="sxs-lookup"><span data-stu-id="94565-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="94565-116">สัญญาโครงการกลายเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="94565-116">The project contract becomes read-only.</span></span> <span data-ttu-id="94565-117">กล่องโต้ตอบการยืนยันมีให้ก่อนที่การเปลี่ยนแปลงจะเสร็จสมบูรณ์ เนื่องจากคุณไม่สามารถเปิดสัญญาโครงการที่ปิดได้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="94565-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="94565-118">หากสัญญาโครงการที่ถูกปิดเป็นแพ้โดยอ้างถึงโครงการในบรรทัด โครงการนั้นจะถูกทำเครื่องหมายเป็นปิดด้วย</span><span class="sxs-lookup"><span data-stu-id="94565-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="94565-119">การจองทรัพยากรใดๆ นับจากวันนั้นไปจะถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="94565-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="94565-120">การขายจริงที่ยังไม่ได้เรียกเก็บเงินในสัญญาโครงการที่ไม่ได้อยู่ในใบแจ้งหนี้จะถูกย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="94565-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="94565-121">ใน Dynamics 365 Project Operations การปิดสัญญาโครงการเป็นแพ้จะไม่ส่งผลกระทบต่อสถานะของโอกาสทางการขายที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="94565-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="94565-122">โอกาสทางการขายนี้จะยังคงเปิดอยู่และต้องปิดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="94565-122">The opportunity will remain open and must be manually closed.</span></span>
