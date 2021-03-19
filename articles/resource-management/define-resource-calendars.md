---
title: กำหนดปฏิทินทรัพยากร
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีกำหนดปฏิทินชั่วโมงการทำงานสำหรับทรัพยากรใน Project Operations
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a7b7c45ad2116519b0369bfd3d7cf6743704f4e1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279836"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="b55af-103">กำหนดปฏิทินทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="b55af-103">Define resource calendars</span></span>

<span data-ttu-id="b55af-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="b55af-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b55af-105">ทรัพยากรที่จองได้แต่ละรายการที่ทำงานในโครงการต้องมีปฏิทินชั่วโมงการทำงานเพื่อกำหนดความพร้อมของตน</span><span class="sxs-lookup"><span data-stu-id="b55af-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="b55af-106">ชั่วโมงการทำงานของทรัพยากรสามารถกำหนดได้สองวิธี:</span><span class="sxs-lookup"><span data-stu-id="b55af-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="b55af-107">กำหนดกฎปฏิทินแต่ละรายการสำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="b55af-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="b55af-108">ใช้แม่แบบปฏิทินที่มีอยู่สำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="b55af-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="b55af-109">กำหนดชั่วโมงการทำงานของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="b55af-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="b55af-110">บนเมนู **ทรัพยากร** ให้เลือก **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="b55af-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="b55af-111">จากมุมมองตาราง เลือก **ทรัพยากรที่สามารถจองได้** ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="b55af-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="b55af-112">บนเพจ **รายละเอียดทรัพยากร** เลือกแท็บ **ชั่วโมงการทำงาน** ตามค่าเริ่มต้น ปฏิทินทรัพยากรที่สามารถจองได้จะมีค่าเริ่มต้นเป็นชั่วโมงการทำงานของแม่แบบชั่วโมงทำงานเริ่มต้นที่กำหนดไว้สำหรับองค์กร</span><span class="sxs-lookup"><span data-stu-id="b55af-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="b55af-113">หากต้องการปรับปรุงชั่วโมงการทำงานให้ ให้คลิกขวาวันที่เริ่มต้นของกฎปฏิทินที่เสนอที่จะกำหนด</span><span class="sxs-lookup"><span data-stu-id="b55af-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="b55af-114">ใช้เมนูกฎปฏิทินเพื่อกำหนดกฎปฏิทินสำหรับวันเฉพาะ ส่วนที่เหลือของชุด หรือปฏิทินทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b55af-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="b55af-115">หลังจากเลือกตัวเลือกแล้ว คุณสามารถกำหนด:</span><span class="sxs-lookup"><span data-stu-id="b55af-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="b55af-116">วันในสัปดาห์ที่จะใช้ชั่วโมงการทำงาน</span><span class="sxs-lookup"><span data-stu-id="b55af-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="b55af-117">เวลาการทำงานในแต่ละวัน</span><span class="sxs-lookup"><span data-stu-id="b55af-117">The working times within each day.</span></span>
    - <span data-ttu-id="b55af-118">โซนเวลาสำหรับกฎของปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="b55af-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="b55af-119">หากเป็นไปได้ คุณสามารถระบุเวลาที่ไม่ทำงานสำหรับกฎได้</span><span class="sxs-lookup"><span data-stu-id="b55af-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="b55af-120">การนำแม่แบบปฏิทินไปใช้กับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="b55af-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="b55af-121">บนเมนู **ทรัพยากร** ให้เลือก **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="b55af-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="b55af-122">จากมุมมองตาราง ให้เลือก **ทรัพยากรที่สามารถจองได้** สูงสุด 25 รายการเพื่อปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="b55af-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="b55af-123">เลือก **ตั้งค่าปฏิทิน** และกล่องโต้ตอบจะแจ้งรายการแม่แบบชั่วโมงการทำงานที่มีอยู่กับคุณ</span><span class="sxs-lookup"><span data-stu-id="b55af-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="b55af-124">เลือกแม่แบบที่คุณต้องการใช้ จากนั้นเลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="b55af-124">Select the template you want to use, and then select **Apply**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]