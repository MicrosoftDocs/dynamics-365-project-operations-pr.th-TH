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
ms.openlocfilehash: 3c33adabbd03cca19ae5e7f401f08a716e9242b2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177849"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="236fd-103">จัดการใบเสนอราคาโครงการ</span><span class="sxs-lookup"><span data-stu-id="236fd-103">Manage project quotes</span></span>

<span data-ttu-id="236fd-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="236fd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="236fd-105">ใน Dynamics 365 Project Operations ใบเสนอราคาโครงการออกแบบมาเพื่อช่วยสร้างข้อเสนอสำหรับงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="236fd-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="236fd-106">โครงสร้างของใบเสนอราคาโครงการใน Project Operations ได้รับการปรับให้เหมาะกับข้อเสนอโครงการโดยมีส่วนประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="236fd-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="236fd-107">รายละเอียดการให้บริการตามใบเสนอราคาที่ระบุส่วนประกอบที่ไม่ต่อเนื่องของงาน ซึ่งจะถูกนำเสนอเป็นส่วนประกอบระดับสูง</span><span class="sxs-lookup"><span data-stu-id="236fd-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="236fd-108">รายละเอียดการให้บริการตามใบเสนอราคาที่ระบุและประมาณการงานสำหรับองค์ประกอบระดับสูงหรือรายละเอียดการให้บริการตามใบเสนอราคาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="236fd-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="236fd-109">การประมาณกำหนดการหรือวันที่และมุมมองด้านการเงินสำหรับงานเชื่อมโยงกับรายละเอียดการให้บริการตามใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="236fd-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="236fd-110">โมเดลการทำสัญญาและส่วนประกอบที่คิดค่าบริการได้รับการตั้งค่าสำหรับแต่ละรายการใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="236fd-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="236fd-111">การตั้งค่านี้ช่วยประมาณส่วนต่างของรายได้ ค่าใช้จ่าย และความสามารถในการทำกำไรสำหรับแต่ละรายการใบเสนอราคาและใบเสนอราคาโดยรวม</span><span class="sxs-lookup"><span data-stu-id="236fd-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="236fd-112">ดูใบเสนอราคาตามโครงการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="236fd-112">View all project-based quotes</span></span>

<span data-ttu-id="236fd-113">รายชื่อใบเสนอราคาโครงการทั้งหมดสามารถดูได้จากหน้ารายการ **ใบเสนอราคา**</span><span class="sxs-lookup"><span data-stu-id="236fd-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="236fd-114">ไปที่ **การขาย** > **ใบเสนอราคา**</span><span class="sxs-lookup"><span data-stu-id="236fd-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="236fd-115">รายการใบเสนอราคาโครงการทั้งหมดของคุณในระบบจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="236fd-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="236fd-116">ใช้ **ดูตัวสลับ** เพื่อเลือกมุมมองที่กรองอื่น ๆ ของใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="236fd-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="236fd-117">เมื่อใช้เกณฑ์ตัวกรองที่กำหนดเอง คุณสามารถกำหนดค่ามุมมองและตัวเลือกการนำทางของคุณเองได้</span><span class="sxs-lookup"><span data-stu-id="236fd-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="236fd-118">ใบเสนอราคาสามารถสร้างหรือลบได้จากหน้ารายการนี้หรือหน้ารายละเอียด</span><span class="sxs-lookup"><span data-stu-id="236fd-118">Quotes can be created or deleted from this list page or detail pages.</span></span>
