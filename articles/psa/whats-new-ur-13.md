---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 13 V3
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับสิ่งใหม่ในรุ่นการปรับปรุง Project Service Automation 13 V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: dbdcb811bfeacf17e841d679f097c591c16cd4c0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281051"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="83d0d-103">Project Service Automation รุ่นการปรับปรุง 13 V3</span><span class="sxs-lookup"><span data-stu-id="83d0d-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="83d0d-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Dynamics 365 Project Service Automation (PSA)</span><span class="sxs-lookup"><span data-stu-id="83d0d-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="83d0d-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="83d0d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="83d0d-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="83d0d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="83d0d-107">หากต้องการอัปเดตเป็นรุ่นนี้ ให้ไปที่ศูนย์ผู้ดูแลระบบสำหรับ Dynamics 365 ออนไลน์ และไปที่หน้าโซลูชันเพื่อติดตั้งการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="83d0d-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="83d0d-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="83d0d-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="83d0d-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขใหม่หรือที่เปลี่ยนแปลงสำหรับ Project Service Automation V3 รุ่นการปรับปรุง 13</span><span class="sxs-lookup"><span data-stu-id="83d0d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="83d0d-110">รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.3.18 และพร้อมใช้งานตามกำหนดการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="83d0d-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="83d0d-111">**ความพร้อมใช้งานทั่วไป (อัปเดตด้วยตนเอง):** พฤศจิกายน 2019</span><span class="sxs-lookup"><span data-stu-id="83d0d-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="83d0d-112">**การปรับปรุงอัตโนมัติ:** ธันวาคม 2019</span><span class="sxs-lookup"><span data-stu-id="83d0d-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="83d0d-113">รุ่นการปรับปรุง 13</span><span class="sxs-lookup"><span data-stu-id="83d0d-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="83d0d-114">การแก้ไขข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="83d0d-114">Bug fixes</span></span>

- <span data-ttu-id="83d0d-115">เวลาและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="83d0d-115">Time and Expense</span></span>

     - <span data-ttu-id="83d0d-116">แก้ไข: ฟังก์ชันการค้นหาในหน้า **การอนุมัติค่าใช้จ่าย** ไม่ทำงานเมื่อค้นหาตามจุดประสงค์ของค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="83d0d-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="83d0d-117">การจัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="83d0d-117">Resource Management</span></span>

     - <span data-ttu-id="83d0d-118">แก้ไข: หมายเลขในการกระทบยอดได้รับการอัปเดตเพื่อให้มีความชอบธรรม</span><span class="sxs-lookup"><span data-stu-id="83d0d-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="83d0d-119">แก้ไข: ทรัพยากรที่มีชื่อไม่สามารถกำหนดให้กับงานผ่านแท็บ **จัดกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="83d0d-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="83d0d-120">การจัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="83d0d-120">Project Management</span></span>

     - <span data-ttu-id="83d0d-121">แก้ไข: ข้อยกเว้นอ้างอิงเป็นศูนย์เมื่อการกำหนดสมาชิกทีมเมื่อ **TransactionType** ไม่มีข้อมูลการตั้งค่าสำหรับ **หน่วย** และ **DefaultGroup**</span><span class="sxs-lookup"><span data-stu-id="83d0d-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="83d0d-122">Sales</span><span class="sxs-lookup"><span data-stu-id="83d0d-122">Sales</span></span>

     - <span data-ttu-id="83d0d-123">แก้ไข: เร็กคอร์ดชนิดธุรกรรมที่ซ้ำกันส่งคืนข้อผิดพลาดเมื่อสร้างเรกคอร์ดราคาบทบาท</span><span class="sxs-lookup"><span data-stu-id="83d0d-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="83d0d-124">แก้ไข: ปุ่มพิเศษสำหรับ **โอกาสทางการขายใหม่** **ใบเสนอราคา** **รายการใบสั่ง** และ **เพิ่มผลิตภัณฑ์** สามารถมองเห็นได้ในคำสั่งสำหรับโอกาสทางการขาย ใบเสนอราคา ผลิตภัณฑ์ในใบสั่ง และกริดย่อยรายการตามโครงการ</span><span class="sxs-lookup"><span data-stu-id="83d0d-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]