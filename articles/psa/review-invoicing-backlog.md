---
title: ตรวจทานรายการคงค้างการออกใบแจ้งหนี้ในโครงการและสัญญาโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีที่จะตรวจทานเวลา ค่าใช้จ่าย และรายการคงค้างผลิตภัณฑ์ และวิธีที่จะทำเครื่องหมายว่าพร้อมสำหรับการออกใบแจ้งหนี้
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: bcdcc0cae06ce61bd582d56a8398e718051ff564
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123986"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="89fdd-103">ตรวจทานรายการคงค้างการออกใบแจ้งหนี้ในโครงการและสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="89fdd-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="89fdd-104">เมื่อธุกรรมพ้อมที่จะออกใบแจ้งหนี้และประมวลผล ธุรกรรมนั้นควรมีการทำเครื่องหมาย **พร้อมที่จะออกใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="89fdd-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="89fdd-105">หัวข้อนี้อธิบายชนิดของการทำธุรกรรมที่สามารถสร้างได้</span><span class="sxs-lookup"><span data-stu-id="89fdd-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="89fdd-106">ตรวจทานเวลาและรายการคงค้างของการเรียกเก็บเงินเวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="89fdd-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="89fdd-107">เมื่อรายการเวลาหรือค่าใช้จ่ายถูกส่งและอนุมัติสำหรับโครงการ PSA จะสร้างโครงการจริง</span><span class="sxs-lookup"><span data-stu-id="89fdd-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="89fdd-108">หาชุดข้อมูลของโครงการและคลาสธุรกรรมถูกแม็ปกับรายละเอียดการให้บริการตามสัญญาสำหรับโครงการเวลาและวัสดุ จะมีโครงการจริงถูกสร้างขึ้นเมื่อรายการได้รับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="89fdd-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="89fdd-109">จำนวนจริงของต้นทุน</span><span class="sxs-lookup"><span data-stu-id="89fdd-109">Cost actual</span></span> 
- <span data-ttu-id="89fdd-110">การขายที่เกิดขึ้นจริงที่ยังไม่ได้เรียกเก็บ</span><span class="sxs-lookup"><span data-stu-id="89fdd-110">Unbilled sales actual</span></span>

<span data-ttu-id="89fdd-111">การขายที่เกิดขึ้นจริงที่ยังไม่ได้เรียกเก็บ แสดงถึงรายการคงค้างการเรียกเก็บเงิน และสถานะการเรียกเก็บเงินที่ต้องตั้งเป็น **พร้อมที่จะออกใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="89fdd-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="89fdd-112">เมื่อมีการสร้างใบแจ้งหนี้โครงการ การขายจริงที่ยังไม่ได้เรียกเก็บเงินที่ถูกทำเครื่องหมายเป็น **พร้อมที่จะออกใบแจ้งหนี้** จะถูกคัดลอกเป็นรายละเอียดรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="89fdd-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="89fdd-113">ในการตรวจทานรายการคงค้างการเรียกเก็บเงินสำหรับเวลาและวัสดุ ไปที่ **การขาย** \> **การเรียกเก็บเงิน** \> **รายการคงค้างของการเรียกเก็บเงินสำหรับเวลาและวัสดุ**</span><span class="sxs-lookup"><span data-stu-id="89fdd-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="89fdd-114">เลือกการขายจริงที่ยังไม่ได้เรียกเก็บเงินทั้งหมดที่พร้อมที่จะออกใบแจ้งหนี้ แล้วเลือก **พร้อมที่จะออกใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="89fdd-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="89fdd-115">สถานะการเรียกเก็บเงินของรายการจริงเหล่านี้จะถูกเปลี่ยนเป็น **พร้อมที่จะออกใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="89fdd-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![รายการคงค้างการเรียกเก็บเงินสำหรับเวลาและวัสดุ](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="89fdd-117">ตรวจทานรายการคงค้างของการเรียกเก็บเงินสำหรับเวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="89fdd-117">Review the product billing backlog</span></span>

<span data-ttu-id="89fdd-118">ใน PSA เมื่อสัญญาโครงการมีรายการสัญญาที่อิงกับผลิตภัณฑ์ รายการเหล่านั้นถือว่าใช้สำหรับการออกใบแจ้งหนี้ในทุกครั้งที่ใบแจ้งหนี้ถูกสร้างขึ้นสำหรับสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="89fdd-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="89fdd-119">ผลิตภัณฑ์ใดๆ ที่มีรายละเอียดการให้บริการตามสัญญาที่ถูกทำเครื่องหมายเป็น **พร้อมที่จะออกใบแจ้งหนี้** จะถูกคัดลอกไปยังใบแจ้งหนี้โครงการในฐานะรายการใบแจ้งหนี้ของโครงการ</span><span class="sxs-lookup"><span data-stu-id="89fdd-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="89fdd-120">หากต้องการตรวจทานรายการคงค้างการเรียกเก็บเงินสำหรัลผลิตภัณฑ์ ไปที่ **การขาย** \> **การเรียกเก็บเงิน** \> **รายการคงค้างของการเรียกเก็บเงินผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="89fdd-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="89fdd-121">เลือกรายละเอียดการให้บริการตามสัญญาที่อิงตามผลิตภัณฑ์ที่พร้อมสำหรับการออกใบแจ้งนี้ แล้วเลือก **พร้อมที่จะออกใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="89fdd-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="89fdd-122">สถานะการเรียกเก็บเงินของรายการเหล่านี้จะถูกเปลี่ยนเป็น **พร้อมที่จะออกใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="89fdd-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![รายการคงค้างของการเรียกเก็บเงินผลิตภัณฑ์](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="89fdd-124">ตรวจทานเหตุการณ์สำคัญเป้าหมายราคาคงที่ในสัญญาที่มีราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="89fdd-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="89fdd-125">แต่ละรายละเอียดการให้บริการสัญญาของโครงการที่มีวิธีการเรียกเก็บเงินที่มีราคาแบบคงที่ต้องกำหนดเหตุการณ์สำคัญของสัญญา</span><span class="sxs-lookup"><span data-stu-id="89fdd-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="89fdd-126">เหตุการณ์สำคัญของสัญญาเหล่านี้สามารถออกใบแจ้งหนี้ได้ก็ต่อเมื่อถูกทำเครื่องหมายเป็น **พร้อมที่จะออกใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="89fdd-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="89fdd-127">ในการตรวจทานเหตุการณ์สำคัญเป้าหมายราคาคงที่ ไปที่ **การขาย** \> **การเรียกเก็บเงิน** \> **หลักเป้าหมายราคาคงที่**</span><span class="sxs-lookup"><span data-stu-id="89fdd-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="89fdd-128">เลือกเหตุการณ์สำคัญที่พร้อมที่จะออกใบแจ้งหนี้ แล้วเลือก **พร้อมที่จะออกใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="89fdd-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="89fdd-129">สถานะการเรียกเก็บเงินของเหตุการณ์สำคัญเหล่านี้จะถูกเปลี่ยนเป็น **พร้อมที่จะออกใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="89fdd-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![หลักเป้าหมายราคาคงที่](media/FPBacklog.png)
