---
title: จัดการใบเสนอราคาโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับใบเสนอราคาโครงการ
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87921221ea210e67a3ddc53bd124f292de80de99
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272951"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="a7c2a-103">จัดการใบเสนอราคาโครงการ</span><span class="sxs-lookup"><span data-stu-id="a7c2a-103">Manage project quotes</span></span>

<span data-ttu-id="a7c2a-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="a7c2a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a7c2a-105">ใน Dynamics 365 Project Operations ใบเสนอราคาโครงการออกแบบมาเพื่อช่วยสร้างข้อเสนอสำหรับงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="a7c2a-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="a7c2a-106">โครงสร้างของใบเสนอราคาโครงการใน Project Operations ได้รับการปรับให้เหมาะกับข้อเสนอโครงการโดยมีส่วนประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a7c2a-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="a7c2a-107">รายละเอียดการให้บริการตามใบเสนอราคาที่ระบุส่วนประกอบที่ไม่ต่อเนื่องของงาน ซึ่งจะถูกนำเสนอเป็นส่วนประกอบระดับสูง</span><span class="sxs-lookup"><span data-stu-id="a7c2a-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="a7c2a-108">รายละเอียดการให้บริการตามใบเสนอราคาที่ระบุและประมาณการงานสำหรับองค์ประกอบระดับสูงหรือรายละเอียดการให้บริการตามใบเสนอราคาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="a7c2a-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="a7c2a-109">การประมาณกำหนดการหรือวันที่และมุมมองด้านการเงินสำหรับงานเชื่อมโยงกับรายละเอียดการให้บริการตามใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="a7c2a-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="a7c2a-110">โมเดลการทำสัญญาและส่วนประกอบที่คิดค่าบริการได้รับการตั้งค่าสำหรับแต่ละรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="a7c2a-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="a7c2a-111">การตั้งค่านี้ช่วยประมาณส่วนต่างของรายได้ ค่าใช้จ่าย และความสามารถในการทำกำไรสำหรับแต่ละรายการใบเสนอราคาและใบเสนอราคาโดยรวม</span><span class="sxs-lookup"><span data-stu-id="a7c2a-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="a7c2a-112">ดูใบเสนอราคาตามโครงการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a7c2a-112">View all project-based quotes</span></span>

<span data-ttu-id="a7c2a-113">รายชื่อใบเสนอราคาโครงการทั้งหมดสามารถดูได้จากหน้ารายการ **ใบเสนอราคา**</span><span class="sxs-lookup"><span data-stu-id="a7c2a-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="a7c2a-114">ไปที่ **การขาย** > **ใบเสนอราคา**</span><span class="sxs-lookup"><span data-stu-id="a7c2a-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="a7c2a-115">รายการใบเสนอราคาโครงการทั้งหมดของคุณในระบบจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="a7c2a-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="a7c2a-116">ใช้ **ดูตัวสลับ** เพื่อเลือกมุมมองที่กรองอื่น ๆ ของใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="a7c2a-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="a7c2a-117">เมื่อใช้เกณฑ์ตัวกรองที่กำหนดเอง คุณสามารถกำหนดค่ามุมมองและตัวเลือกการนำทางของคุณเองได้</span><span class="sxs-lookup"><span data-stu-id="a7c2a-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="a7c2a-118">ใบเสนอราคาสามารถสร้างหรือลบได้จากหน้ารายการนี้หรือหน้ารายละเอียด</span><span class="sxs-lookup"><span data-stu-id="a7c2a-118">Quotes can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]