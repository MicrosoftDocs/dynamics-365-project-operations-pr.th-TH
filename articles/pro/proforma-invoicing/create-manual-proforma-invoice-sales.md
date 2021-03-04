---
title: สร้างใบแจ้งหนี้ชั่วคราวด้วยตนเอง - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการยืนยันใบแจ้งหนี้ชั่วคราวใน Project Operations ด้วยตนเอง
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764526"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="29591-103">สร้างใบแจ้งหนี้ชั่วคราวด้วยตนเอง - Lite</span><span class="sxs-lookup"><span data-stu-id="29591-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="29591-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="29591-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="29591-105">ใน Dynamics 365 Project Operations สามารถสร้างใบแจ้งหนี้ชั่วคราวด้วยตนเองได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="29591-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="29591-106">คุณสามารถสร้างใบแจ้งหนี้ชั่วคราวด้วยตนเองจากหน้ารายการ **สัญญาโครงการ** หรือจากหน้ารายละเอียด **สัญญาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="29591-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="29591-107">หน้ารายการของสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="29591-107">Project Contracts list page</span></span>

<span data-ttu-id="29591-108">จากหน้ารายการ **สัญญาโครงการ** ให้เลือกสัญญาโครงการอย่างน้อยหนึ่งสัญญาและสร้างใบแจ้งหนี้สำหรับเรกคอร์ดที่เลือกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="29591-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="29591-109">ระบบจะตรวจสอบเพื่อดูสัญญาโครงการที่เลือกที่มีรายการค้าง **พร้อมที่จะออกใบแจ้งหนี้** ที่ลงวันที่ก่อนวันนี้</span><span class="sxs-lookup"><span data-stu-id="29591-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="29591-110">จากสัญญาเหล่านั้น ระบบจะสร้างใบแจ้งหนี้ชั่วคราวแบบร่าง</span><span class="sxs-lookup"><span data-stu-id="29591-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="29591-111">หากสัญญาโครงการมีลูกค้าหลายราย อาจมีการสร้างใบแจ้งหนี้หนึ่งใบต่อลูกค้า และใบแจ้งหนี้หลายใบต่อสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="29591-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="29591-112">ใบแจ้งหนี้โครงการที่สร้างขึ้นทั้งหมดมีอยู่ในหน้า **ใบแจ้งหนี้** ในส่วน **การเรียกเก็บเงิน** ของพื้นที่ **การขาย**</span><span class="sxs-lookup"><span data-stu-id="29591-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="29591-113">หน้ารายละเอียดสัญญาของโครงการ</span><span class="sxs-lookup"><span data-stu-id="29591-113">Project Contract details page</span></span>

<span data-ttu-id="29591-114">นอกจากนี้ ยังสามารถสร้างใบแจ้งหนี้ชั่วคราวได้จากหน้ารายละเอียด **สัญญาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="29591-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="29591-115">ระบบจะตรวจสอบว่าสัญญาโครงการมีรายการค้าง **พร้อมที่จะออกใบแจ้งหนี้** ที่ลงวันที่ก่อนวันนี้</span><span class="sxs-lookup"><span data-stu-id="29591-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="29591-116">จากสัญญาเหล่านี้ ระบบจะสร้างใบแจ้งหนี้ชั่วคราวแบบร่างตามจำนวนลูกค้าในแต่ละรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="29591-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="29591-117">เมื่อมีการสร้างใบแจ้งหนี้ชั่วคราวเดียว หน้า **ใบแจ้งหนี้** หน้าจะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="29591-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="29591-118">หากมีการสร้างใบแจ้งหนี้หลายใบสำหรับสัญญาโครงการนั้น หน้ารายการ **ใบแจ้งหนี้** จะเปิดขึ้น เพื่อแสดงใบแจ้งหนี้ที่สร้างขึ้นทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="29591-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>
