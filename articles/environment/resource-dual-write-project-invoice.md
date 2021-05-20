---
title: การรวมใบแจ้งหนี้ของโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการรวมแบบสองทิศทางของ Project Operations สำหรับการออกใบแจ้งหนี้ของลูกค้า
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 102a7cdba467a2071119c5b32d2e75e48170c783
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955847"
---
# <a name="project-invoice-integration"></a><span data-ttu-id="65443-103">การรวมใบแจ้งหนี้ของโครงการ</span><span class="sxs-lookup"><span data-stu-id="65443-103">Project invoice integration</span></span>

<span data-ttu-id="65443-104">หัวข้อนี้ให้ข้อมูลเกี่ยวกับการรวมแบบสองทิศทางของ Project Operations สำหรับการออกใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="65443-104">This topic provides information about Project Operations dual-write integration for customer invoicing.</span></span>

<span data-ttu-id="65443-105">ใน Project Operations ผู้จัดการโครงการจะจัดการรายการค้างชำระของการเรียกเก็บเงินโครงการ และสร้างใบแจ้งหนี้ชั่วคราวสำหรับลูกค้าใน Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="65443-105">In Project Operations, the Project manager manages the project billing backlog and creates a proforma invoice for the customer in Microsoft Dataverse.</span></span> <span data-ttu-id="65443-106">จากใบแจ้งหนี้ชั่วคราวนี้ เสมียนบัญชีลูกหนี้หรือนักบัญชีโครงการจะสร้างใบแจ้งหนี้สำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="65443-106">Based on this proforma invoice, the Accounts receivable clerk or Project accountant creates a customer-facing invoice.</span></span> <span data-ttu-id="65443-107">การรวมแบบสองทิศทางช่วยให้มั่นใจได้ว่า รายละเอียดใบแจ้งหนี้ชั่วคราวจะถูกซิงโครไนซ์กับแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="65443-107">Dual-write integration ensures that the proforma invoice details are synchronized to Finance and Operations apps.</span></span> <span data-ttu-id="65443-108">หลังจากมีการลงรายการบัญชีใบแจ้งหนี้สำหรับลูกค้า ระบบจะอัปเดตข้อมูลจริงของโครงการที่เกี่ยวข้องใน Dataverse พร้อมรายละเอียดการบัญชี</span><span class="sxs-lookup"><span data-stu-id="65443-108">After the customer-facing invoice is posted, the system updates the relevant project actuals in Dataverse with the accounting detail.</span></span> <span data-ttu-id="65443-109">กราฟิกต่อไปนี้แสดงภาพรวมแนวคิดระดับสูงของการรวมนี้</span><span class="sxs-lookup"><span data-stu-id="65443-109">The following graphic provides a high-level conceptual overview of this integration.</span></span>

   ![การรวมใบแจ้งหนี้ของโครงการ](./media/DW5Invoicing.png)

<span data-ttu-id="65443-111">หลังจากผู้จัดการโครงการยืนยันใบแจ้งหนี้ชั่วคราวใน Dataverse ข้อมูลส่วนหัวของใบแจ้งหนี้ชั่วคราวจะซิงโครไนซ์กับแอป Finance and Operations ที่ใช้แผนที่ตารางการรวมแบบสองทิศทาง **ข้อเสนอใบแจ้งหนี้โครงการ V2 (ใบแจ้งหนี้)**</span><span class="sxs-lookup"><span data-stu-id="65443-111">After the Project manager confirms the proforma invoice in Dataverse, the proforma invoice header information synchronizes to Finance and Operations apps using the dual-write table map, **Project invoice proposal V2 (invoices)**.</span></span> <span data-ttu-id="65443-112">นี่คือการรวมทางเดียวจาก Dataverse กับแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="65443-112">This is a one-way integration from Dataverse to Finance and Operations apps.</span></span> <span data-ttu-id="65443-113">ไม่รองรับการสร้างหรือการลบข้อเสนอใบแจ้งหนี้โครงการโดยตรงในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="65443-113">Creating or deleting Project invoice proposals directly in Finance and Operations apps isn't supported.</span></span>

<span data-ttu-id="65443-114">นอกจากนี้ การยืนยันใบแจ้งหนี้ใน Dataverse ยังทริกเกอร์ตรรกะทางธุรกิจเพื่อสร้างเรกคอร์ดที่เกี่ยวข้องกับการเรียกเก็บเงินในเอนทิตี **ข้อมูลจริง**</span><span class="sxs-lookup"><span data-stu-id="65443-114">Invoice confirmation in Dataverse also triggers the business logic to create billing-related records in the **Actuals** entity.</span></span> <span data-ttu-id="65443-115">เรกคอร์ดเหล่านี้ถูกซิงโครไนซ์กับ Finance and Operations โดยใช้แผนที่ตารางการรวมแบบสองทิศทาง **ข้อมูลจริงของการรวม Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="65443-115">These records are synchronized to Finance and Operations using the dual-write table map, **Project Operations integration actuals (msdyn\_actuals).**</span></span> <span data-ttu-id="65443-116">สำหรับข้อมูลเพิ่มเติม ดูที่ [การประมาณการและข้อมูลจริงของโครงการ](resource-dual-write-estimates-actuals.md)</span><span class="sxs-lookup"><span data-stu-id="65443-116">For more information, see [Project estimates and actuals](resource-dual-write-estimates-actuals.md).</span></span> 

<span data-ttu-id="65443-117">รายการข้อเสนอใบแจ้งหนี้โครงการถูกสร้างขึ้นโดยกระบวนการเป็นระยะ **นำเข้าการจัดเตรียมฟอร์ม**</span><span class="sxs-lookup"><span data-stu-id="65443-117">Project invoice proposal lines are created by the periodic process, **Import form staging**.</span></span> <span data-ttu-id="65443-118">กระบวนการนี้ขึ้นอยู่กับรายละเอียดข้อมูลจริงการขายที่เรียกเก็บเงินในตาราง **การจัดเตรียมข้อมูลจริง**</span><span class="sxs-lookup"><span data-stu-id="65443-118">This process is based on the billed sales actuals details in the **Actuals staging** table.</span></span> <span data-ttu-id="65443-119">สำหรับข้อมูลเพิ่มเติม โปรดดู [จัดการข้อเสนอใบแจ้งหนี้โครงการ](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals)</span><span class="sxs-lookup"><span data-stu-id="65443-119">For more information, see [Manage project invoice proposals](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals).</span></span> 
