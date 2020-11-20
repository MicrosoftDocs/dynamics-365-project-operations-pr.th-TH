---
title: สร้างใบแจ้งหนี้ชั่วคราวด้วยตนเอง - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการยืนยันใบแจ้งหนี้ชั่วคราวใน Project Operations ด้วยตนเอง
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176409"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="ebb53-103">สร้างใบแจ้งหนี้ชั่วคราวด้วยตนเอง - Lite</span><span class="sxs-lookup"><span data-stu-id="ebb53-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="ebb53-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="ebb53-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ebb53-105">ใน Dynamics 365 Project Operations สามารถสร้างใบแจ้งหนี้ชั่วคราวด้วยตนเองได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="ebb53-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="ebb53-106">คุณสามารถสร้างใบแจ้งหนี้ชั่วคราวด้วยตนเองจากหน้ารายการ **สัญญาโครงการ** หรือจากหน้ารายละเอียด **สัญญาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="ebb53-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="ebb53-107">หน้ารายการของสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="ebb53-107">Project Contracts list page</span></span>

<span data-ttu-id="ebb53-108">จากหน้ารายการ **สัญญาโครงการ** ให้เลือกสัญญาโครงการอย่างน้อยหนึ่งสัญญาและสร้างใบแจ้งหนี้สำหรับเรกคอร์ดที่เลือกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="ebb53-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="ebb53-109">ระบบจะตรวจสอบว่าสัญญาโครงการใดที่เลือกมีงาน **พร้อมที่จะออกใบแจ้งหนี้** ที่ค้างอยู่ก่อนวันนี้</span><span class="sxs-lookup"><span data-stu-id="ebb53-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="ebb53-110">จากสัญญาเหล่านั้น ระบบจะสร้างใบแจ้งหนี้ชั่วคราวแบบร่าง</span><span class="sxs-lookup"><span data-stu-id="ebb53-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="ebb53-111">หากสัญญาโครงการมีลูกค้าหลายราย อาจมีการสร้างใบแจ้งหนี้หนึ่งใบต่อลูกค้า และใบแจ้งหนี้หลายใบต่อสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="ebb53-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="ebb53-112">ใบแจ้งหนี้โครงการที่สร้างขึ้นทั้งหมดมีอยู่ในหน้า **ใบแจ้งหนี้** ในส่วน **การเรียกเก็บเงิน** ของพื้นที่ **การขาย**</span><span class="sxs-lookup"><span data-stu-id="ebb53-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="ebb53-113">หน้ารายละเอียดสัญญาของโครงการ</span><span class="sxs-lookup"><span data-stu-id="ebb53-113">Project Contract details page</span></span>

<span data-ttu-id="ebb53-114">นอกจากนี้ยังสามารถสร้างใบแจ้งหนี้ชั่วคราวจากหน้ารายละเอียด **สัญญาโครงการ** ซึ่งสร้างใบแจ้งหนี้สำหรับสัญญาโครงการเฉพาะนั้น</span><span class="sxs-lookup"><span data-stu-id="ebb53-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="ebb53-115">ระบบจะตรวจสอบว่าสัญญาโครงการใดที่มีงาน **พร้อมที่จะออกใบแจ้งหนี้** ที่ค้างอยู่ก่อนวันนี้</span><span class="sxs-lookup"><span data-stu-id="ebb53-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="ebb53-116">จากสัญญาเหล่านี้ ระบบจะสร้างใบแจ้งหนี้ชั่วคราวแบบร่างตามจำนวนลูกค้าในแต่ละรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="ebb53-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="ebb53-117">เมื่อมีการสร้างใบแจ้งหนี้ชั่วคราวเดียว หน้า **ใบแจ้งหนี้** หน้าจะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="ebb53-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="ebb53-118">หากมีการสร้างใบแจ้งหนี้หลายใบสำหรับสัญญาโครงการนั้น หน้ารายการ **ใบแจ้งหนี้** จะเปิดขึ้นเพื่อแสดงใบแจ้งหนี้ที่สร้างขึ้นทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="ebb53-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
