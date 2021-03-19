---
title: การตอบสนองความต้องการทรัพยากรทั่วไป
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการจองทรัพยากรที่มีชื่อสำหรับความต้องการทรัพยากรทั่วไป
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fef896ae12c196d5566ad54f3e15373020e4e28a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279611"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="8f933-103">การตอบสนองความต้องการทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="8f933-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="8f933-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="8f933-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8f933-105">คุณสามารถจองทรัพยากรที่มีชื่อเพื่อแทนที่ทรัพยากรทั่วไปที่มีความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8f933-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="8f933-106">บนหน้า **โครงการ** ให้เลือก **ทีม**</span><span class="sxs-lookup"><span data-stu-id="8f933-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="8f933-107">เลือกทรัพยากรทั่วไปที่มีความต้องการทรัพยากรจากรายการ จากนั้นเลือก **จอง**</span><span class="sxs-lookup"><span data-stu-id="8f933-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="8f933-108">หรือเปิดความต้องการทรัพยากร แล้วเลือก **จอง**</span><span class="sxs-lookup"><span data-stu-id="8f933-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="8f933-109">บนหน้า **ตัวช่วยจัดกำหนดการ** ให้เลือกทรัพยากรที่มีชื่อเพื่อจองลงในทีมโครงการของคุณ แล้วเลือก **จอง**</span><span class="sxs-lookup"><span data-stu-id="8f933-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="8f933-110">เมื่อการจองเสร็จสมบูรณ์และบรรลุเป้าหมายโดยทรัพยากรที่มีชื่อแล้ว ทรัพยากรทั่วไปจะถูกแทนที่ด้วยทรัพยากรที่มีชื่อ</span><span class="sxs-lookup"><span data-stu-id="8f933-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="8f933-111">การกำหนดในกำหนดการจะมีการปรับปรุงด้วยทรัพยากรที่มีชื่อเช่นเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="8f933-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="8f933-112">เติมเต็มทรัพยากรทั่วไปด้วยหลายทรัพยากรที่มีชื่อ</span><span class="sxs-lookup"><span data-stu-id="8f933-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="8f933-113">เติมเต็มความต้องการสำหรับทรัพยากรทั่วไปด้วยหลายทรัพยากรที่มีชื่อจะคล้ายกับการกำหนดทรัพยากรที่มีชื่อเดียว</span><span class="sxs-lookup"><span data-stu-id="8f933-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="8f933-114">ตัวอย่างเช่น มีงานที่มีระยะเวลาห้าวัน และ 120 ชั่วโมงของความพยายาม</span><span class="sxs-lookup"><span data-stu-id="8f933-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="8f933-115">งานนี้ไม่สามารถเสร็จสมบูรณ์โดยทรัพยากรหนึ่งที่ทำงานเป็นเวลาแปดชั่วโมงทั่วไปในระยะห้าวันต่อสัปดาห์ได้</span><span class="sxs-lookup"><span data-stu-id="8f933-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="8f933-116">ข้อกำหนดคือสำหรับ 120 ชั่วโมงของวิศวกรรมหุ่นยนต์ในห้าวัน ซึ่งเป็น 24 ชั่วโมงต่อวัน</span><span class="sxs-lookup"><span data-stu-id="8f933-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="8f933-117">นี่คือตัวอย่างเมื่อหลายทรัพยากรที่มีชื่อมีความจำเป็นในการตอบสนองการร้องขอของทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="8f933-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="8f933-118">คุณจะต้องจองทรัพยากรหลายรายการเพื่อตอบสนองความต้องการ</span><span class="sxs-lookup"><span data-stu-id="8f933-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="8f933-119">ความแตกต่างหลักในสถานการณ์สมมตินี้คือว่า ทรัพยากรทั่วไปยังคงอยู่บนทีมที่กำหนดให้กับงาน และสมาชิกทีมทรัพยากรที่มีชื่อไม่ได้ถูกกำหนดเป็นส่วนหนึ่งของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="8f933-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="8f933-120">ผู้จัดการโครงการสามารถกำหนดงานตามความเหมาะสมกับทรัพยากรที่มีชื่อ</span><span class="sxs-lookup"><span data-stu-id="8f933-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="8f933-121">มุมมอง **การกระทบยอด** สามารถช่วยผู้จัดการโครงการในการแบ่งการจองในหลายทรัพยากรไปเป็นการมอบหมายงาน</span><span class="sxs-lookup"><span data-stu-id="8f933-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="8f933-122">จะไม่มีการทำโดยอัตโนมัติเพราะในสถานการณ์ที่ซับซ้อนมากขึ้นกว่าตัวอย่างง่ายๆ ข้างต้น เช่น เมื่อคุณมีกลุ่มของงานที่ทำให้เกิดความต้องการขึ้น หรือเจตนาของวิธีการที่ผู้จัดการโครงการต้องการที่จะกำหนด จะต้องมีการสันนิษฐานโดยระบบ</span><span class="sxs-lookup"><span data-stu-id="8f933-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="8f933-123">เนื่องจากระบบไม่สามารถเข้าใจเจตนา มีโอกาสที่สมมติฐานจะแตกต่างจากที่ตั้งใจ และผลลัพธ์ที่เกิดขึ้นอาจไม่ถูกต้องหรือคาดเดาไม่ได้</span><span class="sxs-lookup"><span data-stu-id="8f933-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="8f933-124">ผลลัพธ์ที่คาดการณ์ได้คือเมื่อทรัพยากรทั่วไปยังคงถูกกำหนดไว้จนกว่าผู้จัดการโครงการจะสร้างงานมอบหมายโดยเจตนา ด้วยความช่วยเหลือของมุมมอง **การกระทบยอด**</span><span class="sxs-lookup"><span data-stu-id="8f933-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]