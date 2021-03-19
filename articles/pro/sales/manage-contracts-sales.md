---
title: จัดการสัญญาโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการดูสัญญาตามโครงการ
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a4357d5cf184a3c6ada3ae33631694c31bb5b00
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273235"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="384b8-103">จัดการสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="384b8-103">Manage project contracts</span></span>

<span data-ttu-id="384b8-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="384b8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="384b8-105">สัญญาโครงการใน Dynamics 365 Project Operations รวบรวมและจัดการข้อตกลงตามสัญญาเกี่ยวกับภาระผูกพันและรายละเอียดการเรียกเก็บเงินของโครงการ</span><span class="sxs-lookup"><span data-stu-id="384b8-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="384b8-106">โครงสร้างของสัญญาโครงการใน Project Operations ได้รับการปรับให้เหมาะกับงานตามโครงการโดยมีส่วนประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="384b8-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="384b8-107">รายละเอียดการให้บริการตามสัญญาที่ระบุส่วนประกอบที่ไม่ต่อเนื่องของงาน ซึ่งจะถูกนำเสนอเป็นส่วนประกอบระดับสูงในใบแจ้งหนี้โครงการ</span><span class="sxs-lookup"><span data-stu-id="384b8-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="384b8-108">รายละเอียดการให้บริการตามสัญญาที่ระบุและประมาณการงานสำหรับองค์ประกอบระดับสูงหรือรายละเอียดการให้บริการตามสัญญาแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="384b8-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="384b8-109">การประมาณการรวมถึงกำหนดการและมุมมองด้านการเงินสำหรับงานที่เชื่อมโยงกับรายละเอียดการให้บริการตามสัญญา</span><span class="sxs-lookup"><span data-stu-id="384b8-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="384b8-110">รูปแบบการทำสัญญาและส่วนประกอบที่คิดค่าบริการได้รับการตั้งค่าสำหรับแต่ละรายละเอียดการให้บริการตามสัญญาที่มีการจัดการการเรียกเก็บเงินสำหรับแต่ละรายละเอียดการให้บริการตามสัญญาและสัญญาโดยรวม</span><span class="sxs-lookup"><span data-stu-id="384b8-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="384b8-111">ดูสัญญาตามโครงการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="384b8-111">View all project-based contracts</span></span>

<span data-ttu-id="384b8-112">รายชื่อสัญญาโครงการทั้งหมดสามารถดูได้ในหน้ารายการ **สัญญา**</span><span class="sxs-lookup"><span data-stu-id="384b8-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="384b8-113">ไปที่ **การขาย** > **สัญญา**</span><span class="sxs-lookup"><span data-stu-id="384b8-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="384b8-114">รายการสัญญาโครงการทั้งหมดของคุณในระบบจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="384b8-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="384b8-115">เลือก **ดูตัวสลับ** (ลูกศรแบบเลื่อนลงถัดจากชื่อของมุมมอง) เพื่อเลือกมุมมองที่กรองอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="384b8-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="384b8-116">คุณสามารถสร้างมุมมองของคุณเองด้วยเกณฑ์ตัวกรองที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="384b8-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="384b8-117">สามารถสร้างหรือลบสัญญาได้จากหน้ารายการนี้หรือหน้ารายละเอียด</span><span class="sxs-lookup"><span data-stu-id="384b8-117">Contracts can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]