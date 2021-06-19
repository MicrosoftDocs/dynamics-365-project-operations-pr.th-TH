---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 14 V3
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับสิ่งใหม่ในรุ่นการปรับปรุง Project Service Automation 14 V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 8754f8eace50f1fa5743c5611d94f8c86693ebc9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006894"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="fad58-103">Project Service Automation รุ่นการปรับปรุง 14 V3</span><span class="sxs-lookup"><span data-stu-id="fad58-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fad58-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Dynamics 365 Project Service Automation (PSA)</span><span class="sxs-lookup"><span data-stu-id="fad58-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="fad58-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fad58-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fad58-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="fad58-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fad58-107">หากต้องการอัปเดตเป็นรุ่นนี้ ให้ไปที่ศูนย์ผู้ดูแลระบบสำหรับ Dynamics 365 ออนไลน์ และไปที่หน้าโซลูชันเพื่อติดตั้งการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="fad58-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="fad58-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="fad58-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fad58-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่เป็นของใหม่หรือที่เปลี่ยนแปลงสำหรับ PSA V3, รุ่นการปรับปรุง 14</span><span class="sxs-lookup"><span data-stu-id="fad58-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="fad58-110">รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.4.21 และพร้อมใช้งานตามกำหนดการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fad58-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="fad58-111">**ความพร้อมใช้งานทั่วไป (อัปเดตด้วยตนเอง):** มกราคม 2020</span><span class="sxs-lookup"><span data-stu-id="fad58-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="fad58-112">**อัปเดตอัตโนมัติ:** กุมภาพันธ์ 2020</span><span class="sxs-lookup"><span data-stu-id="fad58-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="fad58-113">รุ่นการปรับปรุง 14</span><span class="sxs-lookup"><span data-stu-id="fad58-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="fad58-114">การปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="fad58-114">Enhancements</span></span>

- <span data-ttu-id="fad58-115">Sales</span><span class="sxs-lookup"><span data-stu-id="fad58-115">Sales</span></span>

     - <span data-ttu-id="fad58-116">ค่าฟิลด์ที่กำหนดเองจาก **รายละเอียดบรรทัดใบเสนอราคา** ถูกคัดลอกไปยัง **รายละเอียดบรรทัดสัญญาโครงการ** เมื่อมีการปรับปรุงใบเสนอราคาเป็น **ปิดในสถานะชนะ**</span><span class="sxs-lookup"><span data-stu-id="fad58-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="fad58-117">โครงการที่ได้รับการยืนยันสามารถถูก **ปิดในสถานะแพ้**</span><span class="sxs-lookup"><span data-stu-id="fad58-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="fad58-118">การจัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="fad58-118">Resource Management</span></span>

     - <span data-ttu-id="fad58-119">เมื่อขยายการจอง ผู้ใช้จะได้รับแจ้งพร้อมกล่องโต้ตอบการยืนยันเพื่อสรุปผลการจองและให้ลิงก์ไปยังการรักษาการจอง</span><span class="sxs-lookup"><span data-stu-id="fad58-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="fad58-120">การแก้ไขข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="fad58-120">Bug fixes</span></span>

- <span data-ttu-id="fad58-121">เวลาและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="fad58-121">Time and Expense</span></span>

     - <span data-ttu-id="fad58-122">แก้ไข: ปรับปรุงประสบการณ์ผู้ใช้เมื่อผู้ใช้ไม่ได้เลือกรายการใดๆ ที่จะแก้ไข</span><span class="sxs-lookup"><span data-stu-id="fad58-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="fad58-123">การจัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="fad58-123">Resource Management</span></span>

     - <span data-ttu-id="fad58-124">แก้ไข: จองทรัพยากรหลายครั้งทำให้มีชื่อของทรัพยากรที่จองได้มากเกินไป</span><span class="sxs-lookup"><span data-stu-id="fad58-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="fad58-125">Sales</span><span class="sxs-lookup"><span data-stu-id="fad58-125">Sales</span></span>

     - <span data-ttu-id="fad58-126">แก้ไข: ราคาขายทั้งหมดจะไม่ถูกคำนวณจนกว่าผู้ใช้จะป้อนราคาต้นทุนสำหรับการประมาณการค่าใช้จ่ายในโครงการ</span><span class="sxs-lookup"><span data-stu-id="fad58-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="fad58-127">แก้ไข: การปิดใบเสนอราคาเป็น **ชนะ** ล้มเหลวหากสัญญาโครงการที่เกี่ยวข้องไม่ได้อยู่ในสถานะ **ร่าง**</span><span class="sxs-lookup"><span data-stu-id="fad58-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]