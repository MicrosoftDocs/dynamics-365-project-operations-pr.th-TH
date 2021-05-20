---
title: กำหนดปฏิทินโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีใช้เทมเพลตปฏิทินกับโครงการเพื่อติดตามกำหนดการของโครงการ
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981323"
---
# <a name="define-project-calendars"></a><span data-ttu-id="48b87-103">กำหนดปฏิทินโครงการ</span><span class="sxs-lookup"><span data-stu-id="48b87-103">Define project calendars</span></span>

<span data-ttu-id="48b87-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="48b87-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="48b87-105">ในการสร้างและจัดการโครงการ คุณต้องใช้เทมเพลตปฏิทินกับโครงการ</span><span class="sxs-lookup"><span data-stu-id="48b87-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="48b87-106">เทมเพลตปฏิทินกำหนดแอตทริบิวต์โครงการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="48b87-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="48b87-107">เวลาทำงาน ซึ่งรวมถึงเวลาเริ่มต้นและเวลาสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="48b87-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="48b87-108">วันทำงาน</span><span class="sxs-lookup"><span data-stu-id="48b87-108">Working days</span></span>
- <span data-ttu-id="48b87-109">ข้อยกเว้นของปฏิทิน เช่น วันที่ไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="48b87-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="48b87-110">เทมเพลตปฏิทินที่ใช้กับโครงการคือ สำเนาของเทมเพลตปฏิทินที่กำหนดไว้ในการตั้งค่าขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="48b87-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="48b87-111">หากคุณเปลี่ยนเทมเพลตปฏิทิน การเปลี่ยนแปลงเหล่านั้นจะไม่ส่งผลต่อชั่วโมงการทำงานของโครงการ</span><span class="sxs-lookup"><span data-stu-id="48b87-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="48b87-112">ในการเปลี่ยนชั่วโมงการทำงานของโครงการ ต้องใช้เทมเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="48b87-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="48b87-113">ในการสร้างเทมเพลตปฏิทินสำหรับองค์กรของคุณ มีข้อกำหนดหลักสองประการ:</span><span class="sxs-lookup"><span data-stu-id="48b87-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="48b87-114">กำหนดชั่วโมงการทำงานที่ต้องการของเทมเพลตโดยใช้ทรัพยากรที่จองได้ใหม่หรือที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="48b87-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="48b87-115">สร้างเทมเพลตปฏิทินใหม่และเชื่อมโยงเทมเพลตกับทรัพยากรที่จองได้</span><span class="sxs-lookup"><span data-stu-id="48b87-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="48b87-116">**กำหนดชั่วโมงการทำงานของเทมเพลต**</span><span class="sxs-lookup"><span data-stu-id="48b87-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="48b87-117">ไปที่ **ทรัพยากร** \> **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="48b87-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="48b87-118">สร้างทรัพยากรใหม่เพื่ออ้างอิงในเทมเพลตปฏิทิน หรือเลือกทรัพยากรที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="48b87-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="48b87-119">เลือกแท็บ **ชั่วโมงทำงาน** ของทรัพยากร และกรอกคำแนะนำใน [กำหนดชั่วโมงการทำงานสำหรับทรัพยากร](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) เพื่อตั้งค่าคอนฟิกกฎปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="48b87-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="48b87-120">**สร้างเทมเพลตปฏิทินใหม่**</span><span class="sxs-lookup"><span data-stu-id="48b87-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="48b87-121">ไปที่ **การตั้งค่า** \> **เทมเพลตปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="48b87-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="48b87-122">เลือก **ใหม่** และป้อนชื่อ คำอธิบาย และทรัพยากรเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="48b87-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="48b87-123">เมื่อทรัพยากรถูกอ้างอิงในเทมเพลตปฏิทิน สำเนาปฏิทินของทรัพยากรจะเชื่อมโยงกับเทมเพลตปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="48b87-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="48b87-124">หากชั่วโมงการทำงานของเทมเพลตเปลี่ยนแปลง การเปลี่ยนแปลงเหล่านั้นจะไม่ส่งผลต่อเทมเพลตปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="48b87-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="48b87-125">ขณะนี้คุณสามารถเชื่อมโยงแม่แบบงานกับแม่แบบปฏิทินโครงการได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="48b87-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

