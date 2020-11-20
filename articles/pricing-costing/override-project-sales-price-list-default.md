---
title: แทนที่รายการราคาสำหรับการขายของโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการสร้างราคาตลาดการขายที่กำหนดเอง
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c97dca8685c2db7d256017cf4442416feb0e005b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130871"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="66d5b-103">แทนที่รายการราคาสำหรับการขายของโครงการ</span><span class="sxs-lookup"><span data-stu-id="66d5b-103">Override project sales price lists</span></span>

<span data-ttu-id="66d5b-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="66d5b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="66d5b-105">ราคาตลาดของโครงการเฉพาะลูกค้า</span><span class="sxs-lookup"><span data-stu-id="66d5b-105">Customer-specific project price lists</span></span>

<span data-ttu-id="66d5b-106">ข้อตกลงราคาเฉพาะลูกค้าสามารถตั้งค่าเป็นราคาตลาดโครงการบนเรกคอร์ดบัญชีใน Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="66d5b-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="66d5b-107">ในการตั้งค่าราคาตลาดของโครงการเฉพาะลูกค้า ในพื้นที่ **การขาย** ไปที่เรกคอร์ดบัญชี</span><span class="sxs-lookup"><span data-stu-id="66d5b-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="66d5b-108">เปิดหน้ารายการ **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="66d5b-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="66d5b-109">ค้นหาและคลิกสองครั้งที่เรกคอร์ดลูกค้าเพื่อเปิดหน้ารายละเอียด **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="66d5b-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="66d5b-110">บนแท็บ **ราคาตลาดโครงการ** เลือก \*\*+ ราคาตลาดโครงการใหม่^^</span><span class="sxs-lookup"><span data-stu-id="66d5b-110">On the **Project Price lists** tab, select \*\*+ New Project Price List^^.</span></span>
4. <span data-ttu-id="66d5b-111">บนหน้า **ราคาตลาดโครงการใหม่** เลือกราคาตลาดจากเมนูแบบเลื่อนลง</span><span class="sxs-lookup"><span data-stu-id="66d5b-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="66d5b-112">เฉพาะราคาตลาดที่มีบริบทที่กำหนดเป็น **การขาย** และสกุลเงินที่ตรงกับสกุลเงินของบัญชีจะรวมอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="66d5b-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="66d5b-113">ตั้งชื่อการเชื่อมโยง จากนั้นเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="66d5b-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="66d5b-114">ราคาตลาดของโครงการเฉพาะลูกค้าจะสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="66d5b-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="66d5b-115">ราคาตลาดนี้จะใช้เพื่อเริ่มต้นราคาโครงการในใบเสนอโครงการหรือสัญญาที่สร้างขึ้นสำหรับลูกค้ารายนี้ โดยที่วันที่สร้างใบเสนอราคาหรือสัญญาโครงการอยู่ภายในวันที่มีผลบังคับใช้ของราคาตลาด</span><span class="sxs-lookup"><span data-stu-id="66d5b-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="66d5b-116">กำหนดราคาเองสำหรับใบเสนอราคาโครงการ</span><span class="sxs-lookup"><span data-stu-id="66d5b-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="66d5b-117">ในใบเสนอราคาโครงการ คุณสามารถกำหนดราคาโครงการที่เริ่มต้นด้วยราคาตลาดมาตรฐานเริ่มต้นที่เป็นค่าเริ่มต้นจากลูกค้าหรือจากพารามิเตอร์โครงการ</span><span class="sxs-lookup"><span data-stu-id="66d5b-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="66d5b-118">เมื่อคุณต้องการกำหนดราคาที่กำหนดเองสำหรับงานที่เกี่ยวข้องกับโครงการในใบเสนอราคาเฉพาะ คุณสามารถรับได้จากราคาตลาดของโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="66d5b-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="66d5b-119">ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าราคาโครงการเฉพาะใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="66d5b-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="66d5b-120">เปิดใบเสนอราคาโครงการและเลือกแท็บ **ราคาตลาดโครงการ**</span><span class="sxs-lookup"><span data-stu-id="66d5b-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="66d5b-121">ในตารางย่อย เลือก **สร้างการกำหนดราคาที่กำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="66d5b-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="66d5b-122">ราคาตลาดโครงการทั้งหมดที่แนบมากับใบเสนอราคาจะถูกคัดลอกไปยังราคาตลาดใหม่</span><span class="sxs-lookup"><span data-stu-id="66d5b-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="66d5b-123">ชื่อของราคาตลาดใหม่แสดงถึงชื่อของใบเสนอราคาที่มีการประทับวันที่และเว ลาเมื่อสร้างราคาตลาดเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="66d5b-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="66d5b-124">คุณสามารถใช้ราคาตลาดแต่ละรายการและทำการอัปเดตราคาแรงงาน (ราคาตามบทบาท) และราคาค่าใช้จ่าย (ราคาประเภท)</span><span class="sxs-lookup"><span data-stu-id="66d5b-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="66d5b-125">ราคาเหล่านี้จะใช้ได้กับใบเสนอราคาโครงการนี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="66d5b-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="66d5b-126">ราคาตลาดของสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="66d5b-126">Price lists on a project contract</span></span>

<span data-ttu-id="66d5b-127">ในสัญญาโครงการ การกำหนดราคาโครงการจะกำหนดค่าเริ่มต้นเป็นราคาตลาดที่กำหนดเองโดยมีชื่อของสัญญาและการประทับวันที่ที่สร้างไว้ต่อท้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="66d5b-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="66d5b-128">นี่เป็นความจริงไม่ว่าจะเป็นสัญญาที่สร้างขึ้นเมื่อได้รับใบเสนอราคาหรือสัญญาที่สร้างขึ้นตั้งแต่ต้น</span><span class="sxs-lookup"><span data-stu-id="66d5b-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="66d5b-129">หากจำเป็น คุณสามารถลบการเชื่อมโยงนี้กับราคาตลาดที่กำหนดเอง และเชื่อมโยงราคาตลาดมาตรฐานกับสัญญาโครงการแทน</span><span class="sxs-lookup"><span data-stu-id="66d5b-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="66d5b-130">เมื่อคุณเชื่อมโยงราคาตลาดมาตรฐานกับราคาตลาดโครงการตามใบเสนอราคาหรือสัญญา การเปลี่ยนแปลงใด ๆ ที่เกิดขึ้นกับราคาในราคาตลาดจะส่งผลต่อราคาและสัญญาทั้งหมดที่ใช้ราคาตลาด</span><span class="sxs-lookup"><span data-stu-id="66d5b-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>
