---
title: แทนที่รายการราคาสำหรับการขายของโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการสร้างรายการราคาการขายที่กำหนดเอง
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275561"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="7690a-103">แทนที่รายการราคาสำหรับการขายของโครงการ</span><span class="sxs-lookup"><span data-stu-id="7690a-103">Override project sales price lists</span></span>

<span data-ttu-id="7690a-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="7690a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="7690a-105">รายการราคาของโครงการเฉพาะลูกค้า</span><span class="sxs-lookup"><span data-stu-id="7690a-105">Customer-specific project price lists</span></span>

<span data-ttu-id="7690a-106">ข้อตกลงราคาเฉพาะลูกค้าสามารถตั้งค่าเป็นรายการราคาโครงการบนเรกคอร์ดบัญชีใน Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="7690a-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="7690a-107">ในการตั้งค่ารายการราคาของโครงการเฉพาะลูกค้า ในพื้นที่ **การขาย** ไปที่เรกคอร์ดบัญชี</span><span class="sxs-lookup"><span data-stu-id="7690a-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="7690a-108">เปิดหน้ารายการ **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="7690a-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="7690a-109">ค้นหาและคลิกสองครั้งที่เรกคอร์ดลูกค้าเพื่อเปิดหน้ารายละเอียด **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="7690a-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="7690a-110">บนแท็บ **รายการราคาโครงการ** เลือก **+ รายการราคาโครงการใหม่**</span><span class="sxs-lookup"><span data-stu-id="7690a-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="7690a-111">บนหน้า **รายการราคาโครงการใหม่** เลือกรายการราคาจากเมนูแบบเลื่อนลง</span><span class="sxs-lookup"><span data-stu-id="7690a-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="7690a-112">เฉพาะรายการราคาที่มีบริบทที่กำหนดเป็น **การขาย** และสกุลเงินที่ตรงกับสกุลเงินของบัญชีจะรวมอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="7690a-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="7690a-113">ตั้งชื่อการเชื่อมโยง จากนั้นเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7690a-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="7690a-114">รายการราคาของโครงการเฉพาะลูกค้าจะสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="7690a-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="7690a-115">รายการราคานี้จะใช้เพื่อเริ่มต้นราคาโครงการในใบเสนอโครงการหรือสัญญาที่สร้างขึ้นสำหรับลูกค้ารายนี้ โดยที่วันที่สร้างใบเสนอราคาหรือสัญญาโครงการอยู่ภายในวันที่มีผลบังคับใช้ของรายการราคา</span><span class="sxs-lookup"><span data-stu-id="7690a-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="7690a-116">กำหนดราคาเองสำหรับใบเสนอราคาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7690a-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="7690a-117">ในใบเสนอราคาโครงการ คุณสามารถกำหนดราคาโครงการที่เริ่มต้นด้วยรายการราคามาตรฐานเริ่มต้นที่เป็นค่าเริ่มต้นจากลูกค้าหรือจากพารามิเตอร์โครงการ</span><span class="sxs-lookup"><span data-stu-id="7690a-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="7690a-118">เมื่อคุณต้องการกำหนดราคาที่กำหนดเองสำหรับงานที่เกี่ยวข้องกับโครงการในใบเสนอราคาเฉพาะ คุณสามารถรับได้จากรายการราคาของโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="7690a-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="7690a-119">ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าราคาโครงการเฉพาะใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="7690a-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="7690a-120">เปิดใบเสนอราคาโครงการและเลือกแท็บ **รายการราคาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="7690a-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="7690a-121">ในตารางย่อย เลือก **สร้างการกำหนดราคาที่กำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="7690a-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="7690a-122">รายการราคาโครงการทั้งหมดที่แนบมากับใบเสนอราคาจะถูกคัดลอกไปยังรายการราคาใหม่</span><span class="sxs-lookup"><span data-stu-id="7690a-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="7690a-123">ชื่อของรายการราคาใหม่แสดงถึงชื่อของใบเสนอราคาที่มีการประทับวันที่และเว ลาเมื่อสร้างรายการราคาเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="7690a-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="7690a-124">คุณสามารถใช้รายการราคาแต่ละรายการและทำการอัปเดตราคาแรงงาน (ราคาตามบทบาท) และราคาค่าใช้จ่าย (ราคาประเภท)</span><span class="sxs-lookup"><span data-stu-id="7690a-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="7690a-125">ราคาเหล่านี้จะใช้ได้กับใบเสนอราคาโครงการนี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="7690a-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="7690a-126">รายการราคาของสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="7690a-126">Price lists on a project contract</span></span>

<span data-ttu-id="7690a-127">ในสัญญาโครงการ การกำหนดราคาโครงการจะกำหนดค่าเริ่มต้นเป็นรายการราคาที่กำหนดเองโดยมีชื่อของสัญญาและการประทับวันที่ที่สร้างไว้ต่อท้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="7690a-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="7690a-128">นี่เป็นความจริงไม่ว่าจะเป็นสัญญาที่สร้างขึ้นเมื่อได้รับใบเสนอราคาหรือสัญญาที่สร้างขึ้นตั้งแต่ต้น</span><span class="sxs-lookup"><span data-stu-id="7690a-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="7690a-129">หากจำเป็น คุณสามารถลบการเชื่อมโยงนี้กับรายการราคาที่กำหนดเอง และเชื่อมโยงรายการราคามาตรฐานกับสัญญาโครงการแทน</span><span class="sxs-lookup"><span data-stu-id="7690a-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="7690a-130">เมื่อคุณเชื่อมโยงรายการราคามาตรฐานกับรายการราคาโครงการตามใบเสนอราคาหรือสัญญา การเปลี่ยนแปลงใด ๆ ที่เกิดขึ้นกับราคาในรายการราคาจะส่งผลต่อราคาและสัญญาทั้งหมดที่ใช้รายการราคา</span><span class="sxs-lookup"><span data-stu-id="7690a-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]