---
title: กำหนดปฏิทินโครงการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีใช้เทมเพลตปฏิทินกับโครงการเพื่อติดตามกำหนดการของโครงการ
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999019"
---
# <a name="define-project-calendars"></a><span data-ttu-id="c0fbb-103">กำหนดปฏิทินโครงการ</span><span class="sxs-lookup"><span data-stu-id="c0fbb-103">Define project calendars</span></span>

<span data-ttu-id="c0fbb-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="c0fbb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c0fbb-105">ในการสร้างและจัดการโครงการ คุณต้องใช้เทมเพลตปฏิทินกับโครงการ</span><span class="sxs-lookup"><span data-stu-id="c0fbb-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="c0fbb-106">เทมเพลตปฏิทินกำหนดแอตทริบิวต์โครงการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c0fbb-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="c0fbb-107">เวลาทำงาน ซึ่งรวมถึงเวลาเริ่มต้นและเวลาสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="c0fbb-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="c0fbb-108">วันทำงาน</span><span class="sxs-lookup"><span data-stu-id="c0fbb-108">Working days</span></span>
- <span data-ttu-id="c0fbb-109">ข้อยกเว้นของปฏิทิน เช่น วันที่ไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c0fbb-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="c0fbb-110">เทมเพลตปฏิทินที่ใช้กับโครงการคือ สำเนาของเทมเพลตปฏิทินที่กำหนดไว้ในการตั้งค่าขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="c0fbb-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="c0fbb-111">หากคุณเปลี่ยนเทมเพลตปฏิทิน การเปลี่ยนแปลงเหล่านั้นจะไม่ส่งผลต่อชั่วโมงการทำงานของโครงการ</span><span class="sxs-lookup"><span data-stu-id="c0fbb-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="c0fbb-112">ในการเปลี่ยนชั่วโมงการทำงานของโครงการ ต้องใช้เทมเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="c0fbb-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="c0fbb-113">ในการสร้างเทมเพลตปฏิทินสำหรับองค์กรของคุณ มีข้อกำหนดหลักสองประการ:</span><span class="sxs-lookup"><span data-stu-id="c0fbb-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="c0fbb-114">กำหนดชั่วโมงการทำงานที่ต้องการของเทมเพลตโดยใช้ทรัพยากรที่จองได้ใหม่หรือที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="c0fbb-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="c0fbb-115">สร้างเทมเพลตปฏิทินใหม่และเชื่อมโยงเทมเพลตกับทรัพยากรที่จองได้</span><span class="sxs-lookup"><span data-stu-id="c0fbb-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="c0fbb-116">**กำหนดชั่วโมงการทำงานของเทมเพลต**</span><span class="sxs-lookup"><span data-stu-id="c0fbb-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="c0fbb-117">ไปที่ **ทรัพยากร** \> **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="c0fbb-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="c0fbb-118">สร้างทรัพยากรใหม่เพื่ออ้างอิงในเทมเพลตปฏิทิน หรือเลือกทรัพยากรที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="c0fbb-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="c0fbb-119">เลือกแท็บ **ชั่วโมงทำงาน** ของทรัพยากร และกรอกคำแนะนำใน [กำหนดชั่วโมงการทำงานสำหรับทรัพยากร](/dynamics365/field-service/set-work-hours-resource.md) เพื่อตั้งค่าคอนฟิกกฎปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="c0fbb-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="c0fbb-120">**สร้างเทมเพลตปฏิทินใหม่**</span><span class="sxs-lookup"><span data-stu-id="c0fbb-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="c0fbb-121">ไปที่ **การตั้งค่า** \> **เทมเพลตปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="c0fbb-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="c0fbb-122">เลือก **ใหม่** และป้อนชื่อ คำอธิบาย และทรัพยากรเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="c0fbb-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="c0fbb-123">เมื่อทรัพยากรถูกอ้างอิงในเทมเพลตปฏิทิน สำเนาปฏิทินของทรัพยากรจะเชื่อมโยงกับเทมเพลตปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="c0fbb-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="c0fbb-124">หากชั่วโมงการทำงานของเทมเพลตเปลี่ยนแปลง การเปลี่ยนแปลงเหล่านั้นจะไม่ส่งผลต่อเทมเพลตปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="c0fbb-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="c0fbb-125">ขณะนี้คุณสามารถเชื่อมโยงแม่แบบงานกับแม่แบบปฏิทินโครงการได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c0fbb-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

