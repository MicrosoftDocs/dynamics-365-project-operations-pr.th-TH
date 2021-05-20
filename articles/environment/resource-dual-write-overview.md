---
title: การรวมแบบสองทิศทางของ Project Operations
description: หัวข้อนี้ให้ภาพรวมของการรวมแบบสองทิศทางของ Project Operations
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955681"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="14dee-103">ภาพรวมการรวมแบบสองทิศทางของ Project Operations</span><span class="sxs-lookup"><span data-stu-id="14dee-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="14dee-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="14dee-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="14dee-105">Project Operations ใช้ [ความสามารถในการรวมแบบสองทิศทาง](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) เพื่อซิงโครไนซ์ข้อมูลระหว่าง Microsoft Dataverse และ Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="14dee-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="14dee-106">ภาพประกอบต่อไปนี้แสดงให้เห็นวิธีการที่ข้อมูลถูกซิงโครไนซ์เป็นส่วนหนึ่งของการรวมระหว่าง Dataverse และ Finance</span><span class="sxs-lookup"><span data-stu-id="14dee-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![ภาพรวมโฟลว์ข้อมูลของ Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="14dee-108">Project Operations ใน Dataverse มีอินเทอร์เฟซผู้ใช้ที่ทันสมัย (UI) และความสามารถในการเพิ่มที่ไม่มีรหัส/ที่เขียนโค้ดเล็กน้อยอย่างง่าย โดยใช้ความสามารถ Power Platform</span><span class="sxs-lookup"><span data-stu-id="14dee-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="14dee-109">ผู้จัดการโครงการ ผู้จัดการทรัพยากร สมาชิกในกลุ่มคนของโครงการ และบุคลากรส่วนหน้าอื่นๆ ดำเนินกิจกรรมของพวกเขาใน Project Operations ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="14dee-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="14dee-110">Project Operations ใน Finance ให้การสนับสนุนการบัญชีโครงการและการรับรู้รายได้</span><span class="sxs-lookup"><span data-stu-id="14dee-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="14dee-111">Project Operations เชื่อมต่อกับกรอบงานทางการเงินใน Finance สำหรับการคำนวณภาษีขาย อัตราแลกเปลี่ยนสกุลเงิน การรายงานมิติทางการเงิน และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="14dee-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="14dee-112">ประสบการณ์ของนักบัญชีโครงการส่วนใหญ่อยู่ใน Finance</span><span class="sxs-lookup"><span data-stu-id="14dee-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="14dee-113">การรวม Project Operations ประกอบด้วยการรวมองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14dee-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="14dee-114">การตั้งค่าและการรวมข้อมูลการตั้งค่าคอนฟิกของ Project Operations</span><span class="sxs-lookup"><span data-stu-id="14dee-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="14dee-115">การประมาณการและข้อมูลจริงของโครงการ</span><span class="sxs-lookup"><span data-stu-id="14dee-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="14dee-116">ใบแจ้งหนี้ของโครงการ</span><span class="sxs-lookup"><span data-stu-id="14dee-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="14dee-117">การจัดการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="14dee-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="14dee-118">ใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="14dee-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)