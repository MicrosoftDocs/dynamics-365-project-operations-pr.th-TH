---
title: มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Project Service Automation รุ่นการปรับปรุง 17 V3
description: หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่พร้อมใช้งานใน Project Service Automation รุ่นการปรับปรุง 17 V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 364a64e0ea501ac5b7faaf254c7af3648cfe1f9b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006714"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="a5a0b-103">Project Service Automation รุ่นการปรับปรุง 17 V3</span><span class="sxs-lookup"><span data-stu-id="a5a0b-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a5a0b-104">เรายินดีที่จะประกาศการปรับปรุงล่าสุดสำหรับแอปพลิเคชัน Project Service Automation สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a5a0b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a5a0b-105">รุ่นนี้มีการปรับปรุงที่สำคัญบางอย่างเกี่ยวกับคุณภาพ ประสิทธิภาพ และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a5a0b-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="a5a0b-106">รุ่นนี้เข้ากันได้กับ Dynamics 365 9.x</span><span class="sxs-lookup"><span data-stu-id="a5a0b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a5a0b-107">หากต้องการปรับปรุงเป็นรุ่นนี้ ให้เยี่ยมชมศูนย์การจัดการสำหรับ Dynamics 365 ออนไลน์ และหน้าโซลูชันเพื่อติดตั้งการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="a5a0b-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="a5a0b-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ติดตั้ง อัปเดต หรือลบโซลูชันที่ต้องการ](/power-platform/admin/install-remove-preferred-solution)</span><span class="sxs-lookup"><span data-stu-id="a5a0b-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a5a0b-109">หัวข้อนี้แสดงรายการคุณลักษณะและการแก้ไขที่เป็นของใหม่หรือที่เปลี่ยนแปลงสำหรับ PSA V3, รุ่นการปรับปรุง 17</span><span class="sxs-lookup"><span data-stu-id="a5a0b-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="a5a0b-110">รุ่นนี้มีหมายเลขรุ่นเป็น V3.10.6.34 และโดยทั่วไปจะพร้อมใช้งานผ่านการอัปเดตด้วยตนเองในเดือนมีนาคม 2020</span><span class="sxs-lookup"><span data-stu-id="a5a0b-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="a5a0b-111">รุ่นการปรับปรุง 17</span><span class="sxs-lookup"><span data-stu-id="a5a0b-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a5a0b-112">การแก้ไขข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="a5a0b-112">Bug fixes</span></span>

<span data-ttu-id="a5a0b-113">**ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="a5a0b-113">**General**</span></span>

- <span data-ttu-id="a5a0b-114">แก้ไขแล้ว: ปรับปรุง Project Service Automation เพื่อบังคับใช้สิทธิ์การใช้งานของ Team Member (Project Resource Hub จะรวมข้อมูลเมตาของแผน Team Member Service 3.x)</span><span class="sxs-lookup"><span data-stu-id="a5a0b-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="a5a0b-115">**เวลาและค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="a5a0b-115">**Time and Expense**</span></span>

- <span data-ttu-id="a5a0b-116">แก้ไขแล้ว: เป็นไปไม่ได้ที่จะเปลี่ยนการประมาณการค่าใช้จ่ายจากราคาที่ไม่เป็นศูนย์เป็นศูนย์ (0)</span><span class="sxs-lookup"><span data-stu-id="a5a0b-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="a5a0b-117">การเปลี่ยนแปลงจะถูกละเว้น</span><span class="sxs-lookup"><span data-stu-id="a5a0b-117">The change is ignored.</span></span>

<span data-ttu-id="a5a0b-118">**การจัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="a5a0b-118">**Project Management**</span></span>

- <span data-ttu-id="a5a0b-119">แก้ไขแล้ว: การตรวจสอบค่า Null ถูกเพิ่มในชื่อตำแหน่งของสมาชิกกลุ่มคน</span><span class="sxs-lookup"><span data-stu-id="a5a0b-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="a5a0b-120">แก้ไขแล้ว: ฟิลด์ **msdyn_userresourceid** บนเอนทิตี **msdyn_resourceassignment** ถูกเลิกใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="a5a0b-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="a5a0b-121">แก้ไขแล้ว: ในขณะนี้การอัปเกรดจาก 2.x เป็น 3.x จัดการกับเส้นชั้นของความพยายามที่ว่างเปล่าในการมอบหมายงาน</span><span class="sxs-lookup"><span data-stu-id="a5a0b-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="a5a0b-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="a5a0b-122">**Sales**</span></span>

- <span data-ttu-id="a5a0b-123">แก้ไขแล้ว: **Invoice.PreValidateInvoiceUpdate** ตอนนี้จัดการสถานการณ์จำลองของการมอบหมายเจ้าของเรกคอร์ดใหม่อย่างเหมาะสมอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="a5a0b-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="a5a0b-124">แก้ไขแล้ว: เมื่อคลาสธุรกรรมคือ **เวลา** **UnitGroup** เป็นแบบไม่สามารถแก้ไขได้สำหรับเอนทิตีทั้งหมด ซึ่งรวมถึง **QuoteLineDetails** **JournalLine** **InvoiceLineDetail** และ **ContractLineDetails**</span><span class="sxs-lookup"><span data-stu-id="a5a0b-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="a5a0b-125">อย่างไรก็ตาม **หน่วย** เป็นแบบไม่สามารถแก้ไขได้ เฉพาะสำหรับ **JournalLine** และ **InvoiceLineDetails**</span><span class="sxs-lookup"><span data-stu-id="a5a0b-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]