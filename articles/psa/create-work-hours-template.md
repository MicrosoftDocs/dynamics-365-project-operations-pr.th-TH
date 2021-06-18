---
title: สร้างแม่แบบชั่วโมงทำงาน
description: หัวข้อนี้อธิบายวิธีการสร้างเท็มเพลตชั่วโมงทำงานใน Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997219"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="5c72d-103">สร้างเท็มเพลตชั่วโมงทำงาน (Project Service)</span><span class="sxs-lookup"><span data-stu-id="5c72d-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5c72d-104">ในการสร้างและจัดการโครงการ คุณต้องใช้เทมเพลตปฏิทินกับโครงการ</span><span class="sxs-lookup"><span data-stu-id="5c72d-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="5c72d-105">เทมเพลตปฏิทินกำหนดแอตทริบิวต์โครงการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5c72d-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="5c72d-106">เวลาทำงาน ซึ่งรวมถึงเวลาเริ่มต้นและเวลาสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="5c72d-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="5c72d-107">วันทำงาน</span><span class="sxs-lookup"><span data-stu-id="5c72d-107">Working days</span></span>
- <span data-ttu-id="5c72d-108">ข้อยกเว้นของปฏิทิน เช่น วันที่ไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="5c72d-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="5c72d-109">เทมเพลตปฏิทินที่ใช้กับโครงการคือ สำเนาของเทมเพลตปฏิทินที่กำหนดไว้ในการตั้งค่าขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="5c72d-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="5c72d-110">หากคุณเปลี่ยนเทมเพลตปฏิทิน การเปลี่ยนแปลงเหล่านั้นจะไม่ส่งผลต่อชั่วโมงการทำงานของโครงการ</span><span class="sxs-lookup"><span data-stu-id="5c72d-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="5c72d-111">ในการเปลี่ยนชั่วโมงการทำงานของโครงการ ต้องใช้เทมเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="5c72d-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="5c72d-112">ในการสร้างเทมเพลตปฏิทินสำหรับองค์กรของคุณ มีข้อกำหนดหลักสองประการ:</span><span class="sxs-lookup"><span data-stu-id="5c72d-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="5c72d-113">กำหนดชั่วโมงการทำงานที่ต้องการของเทมเพลตโดยใช้ทรัพยากรที่จองได้ใหม่หรือที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="5c72d-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="5c72d-114">สร้างเทมเพลตปฏิทินใหม่และเชื่อมโยงเทมเพลตกับทรัพยากรที่จองได้</span><span class="sxs-lookup"><span data-stu-id="5c72d-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="5c72d-115">**กำหนดชั่วโมงการทำงานของเทมเพลต**</span><span class="sxs-lookup"><span data-stu-id="5c72d-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="5c72d-116">ไปที่ **ทรัพยากร** \> **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="5c72d-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="5c72d-117">สร้างทรัพยากรใหม่เพื่ออ้างอิงในเทมเพลตปฏิทิน หรือเลือกทรัพยากรที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="5c72d-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="5c72d-118">เลือกแท็บ **ชั่วโมงทำงาน** ของทรัพยากร และกรอกคำแนะนำใน [กำหนดชั่วโมงการทำงานสำหรับทรัพยากร](/dynamics365/field-service/set-work-hours-resource.md) เพื่อตั้งค่าคอนฟิกกฎปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="5c72d-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="5c72d-119">**สร้างเทมเพลตปฏิทินใหม่**</span><span class="sxs-lookup"><span data-stu-id="5c72d-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="5c72d-120">ไปที่ **การตั้งค่า** \> **เทมเพลตปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="5c72d-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="5c72d-121">เลือก **ใหม่** และป้อนชื่อ คำอธิบาย และทรัพยากรเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="5c72d-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="5c72d-122">เมื่อทรัพยากรถูกอ้างอิงในเทมเพลตปฏิทิน สำเนาปฏิทินของทรัพยากรจะเชื่อมโยงกับเทมเพลตปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="5c72d-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="5c72d-123">หากชั่วโมงการทำงานของเทมเพลตเปลี่ยนแปลง การเปลี่ยนแปลงเหล่านั้นจะไม่ส่งผลต่อเทมเพลตปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="5c72d-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="5c72d-124">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5c72d-124">See Also</span></span>  
 [<span data-ttu-id="5c72d-125">ตั้งค่าทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="5c72d-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
