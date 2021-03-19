---
title: การประเมินค่าใช้จ่าย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการกำหนดหรือการประเมินค่าใช้จ่ายตามโครงการ
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3f0429366c69346113003355679c055cd2c74ca3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287081"
---
# <a name="expense-estimates"></a><span data-ttu-id="c90ef-103">การประเมินค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="c90ef-103">Expense estimates</span></span>
<span data-ttu-id="c90ef-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="c90ef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c90ef-105">นอกเหนือจากการกำหนดประมาณการตามทรัพยากรแล้ว Dynamics 365 Project Operations ยังช่วยให้ผู้จัดการโครงการสามารถกำหนดค่าใช้จ่ายตามโครงการสำหรับแต่ละโครงการได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="c90ef-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="c90ef-106">รายการค่าใช้จ่ายแต่ละรายการสามารถเชื่อมโยงกับงานโครงการเฉพาะหรือประเภทค่าใช้จ่ายได้</span><span class="sxs-lookup"><span data-stu-id="c90ef-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="c90ef-107">โดยทั่วไปแล้ว ประเภทค่าใช้จ่ายจะกำหนดที่ระดับองค์กร</span><span class="sxs-lookup"><span data-stu-id="c90ef-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="c90ef-108">โดยทั่วไป การกำหนดราคาสำหรับค่าใช้จ่ายแต่ละประเภทจะกำหนดตามลำดับชั้นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c90ef-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="c90ef-109">องค์กร</span><span class="sxs-lookup"><span data-stu-id="c90ef-109">Organization</span></span>
- <span data-ttu-id="c90ef-110">ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c90ef-110">Customer</span></span>
- <span data-ttu-id="c90ef-111">ใบเสนอราคา/สัญญา</span><span class="sxs-lookup"><span data-stu-id="c90ef-111">Quote/contract</span></span>

<span data-ttu-id="c90ef-112">ทำตามขั้นตอนต่อไปนี้เพื่อดู เพิ่ม หรือลบค่าใช้จ่ายโครงการ</span><span class="sxs-lookup"><span data-stu-id="c90ef-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="c90ef-113">ไปที่ **โครงการ** แล้วเลือกโครงการที่คุณต้องการทำงานด้วย</span><span class="sxs-lookup"><span data-stu-id="c90ef-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="c90ef-114">เลือกแท็บ **ประมาณการของโครงการ** และดูรายการของค่าใช้จ่ายโครงการ</span><span class="sxs-lookup"><span data-stu-id="c90ef-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="c90ef-115">เลือก **ค่าใช้จ่ายใหม่** เพื่อเพิ่มค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="c90ef-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="c90ef-116">หรือเลือกค่าใช้จ่ายที่จะลบ จากนั้นเลือก **ลบค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="c90ef-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="c90ef-117">แอตทริบิวต์ต่อไปนี้กำหนดไว้สำหรับข้อมูลในการแสดงรายการค่าใช้จ่ายแต่ละรายการ:</span><span class="sxs-lookup"><span data-stu-id="c90ef-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="c90ef-118">**ประเภท**: การจัดกลุ่มทั่วไปที่ใช้เพื่ออธิบายค่าใช้จ่ายทั้งหมดที่เกิดขึ้นในโครงการ</span><span class="sxs-lookup"><span data-stu-id="c90ef-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="c90ef-119">**วันที่เริ่มต้น**: วันที่คาดการณ์ว่าค่าใช้จ่ายจะเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="c90ef-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="c90ef-120">**ปริมาณ**: จำนวนของรายการค่าใช้จ่ายโดยประมาณสำหรับประเภทเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="c90ef-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="c90ef-121">**ราคาต้นทุนต่อหน่วย**: ราคาต่อหน่วยที่ใช้ในการคำนวณต้นทุนของค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="c90ef-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="c90ef-122">**ราคาขายต่อหน่วย**: ราคาต่อหน่วยที่ใช้ในการคำนวณราคาขายของค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="c90ef-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]