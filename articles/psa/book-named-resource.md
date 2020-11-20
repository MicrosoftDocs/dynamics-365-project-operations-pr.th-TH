---
title: จองทรัพยากรที่มีชื่อจากความต้องการทรัพยากร
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการจองทรัพยากรที่มีชื่อสำหรับความต้องการทรัพยากรทั่วไป
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: d7ff58ec08661adc702867c6c26805a74a3637c9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125921"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="8cd6c-103">จองทรัพยากรที่มีชื่อจากความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8cd6c-103">Book named resources from resource requirements</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8cd6c-104">คุณสามารถจองทรัพยากรที่มีชื่อเพื่อแทนที่ทรัพยากรทั่วไปที่มีความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8cd6c-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="8cd6c-105">ใน Project Service Automation (PSA) บนหน้า **โครงการ** ให้คลิกแท็บ **ทีม**</span><span class="sxs-lookup"><span data-stu-id="8cd6c-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="8cd6c-106">เลือกทรัพยากรทั่วไปที่มีความต้องการทรัพยากรจากรายการ จากนั้นคลิก **จอง**</span><span class="sxs-lookup"><span data-stu-id="8cd6c-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="8cd6c-107">หรือเปิดความต้องการทรัพยากรแล้วคลิก **จอง**</span><span class="sxs-lookup"><span data-stu-id="8cd6c-107">Or, open the resource requirement and then click **Book**.</span></span>


![จองสมาชิกทีมทั่วไป](media/RM-how-to-14.png)


3. <span data-ttu-id="8cd6c-109">บนหน้า **ตัวช่วยจัดกำหนดการ** ให้เลือกทรัพยากรที่มีชื่อเพื่อจองลงในทีมโครงการของคุณ แล้วคลิก **จอง**</span><span class="sxs-lookup"><span data-stu-id="8cd6c-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![การจองสมาชิกในทีมทั่วไปโดยใช้ผู้ช่วยจัดกำหนดการ](media/RM-how-to-15.png)

<span data-ttu-id="8cd6c-111">เมื่อการจองเสร็จสมบูรณ์และบรรลุเป้าหมายโดยทรัพยากรที่มีชื่อแล้ว ทรัพยากรทั่วไปจะถูกแทนที่ด้วยทรัพยากรที่มีชื่อ</span><span class="sxs-lookup"><span data-stu-id="8cd6c-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![สมาชิกในทีมที่มีชื่อแทนที่สมาชิกในทีมทั่วไป](media/RM-how-to-16.png)

<span data-ttu-id="8cd6c-113">การกำหนดในกำหนดการจะมีการปรับปรุงด้วยทรัพยากรที่มีชื่อเช่นเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="8cd6c-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![สมาชิกทีมที่มีชื่อถูกมอบหมายให้กับงานโครงการ](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="8cd6c-115">เติมเต็มทรัพยากรทั่วไปด้วยหลายทรัพยากรที่มีชื่อ</span><span class="sxs-lookup"><span data-stu-id="8cd6c-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="8cd6c-116">เติมเต็มความต้องการสำหรับทรัพยากรทั่วไปด้วยหลายทรัพยากรที่มีชื่อจะคล้ายกับการกำหนดทรัพยากรที่มีชื่อเดียว</span><span class="sxs-lookup"><span data-stu-id="8cd6c-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="8cd6c-117">ตัวอย่างเช่น มีงานที่มีระยะเวลาห้าวัน และ 120 ชั่วโมงของความพยายาม</span><span class="sxs-lookup"><span data-stu-id="8cd6c-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="8cd6c-118">งานนี้ไม่สามารถเสร็จสมบูรณ์โดยทรัพยากรหนึ่งที่ทำงานเป็นเวลาแปดชั่วโมงทั่วไปในระยะห้าวันต่อสัปดาห์ได้</span><span class="sxs-lookup"><span data-stu-id="8cd6c-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![งานที่ต้องใช้ความพยายาม 120 ชั่วโมงมากกว่าห้าวัน](media/RM-how-to-21.png)

<span data-ttu-id="8cd6c-120">ข้อกำหนดคือสำหรับ 120 ชั่วโมงของวิศวกรรมหุ่นยนต์ในห้าวัน ซึ่งเป็น 24 ชั่วโมงต่อวัน</span><span class="sxs-lookup"><span data-stu-id="8cd6c-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![ข้อกำหนดต่อวัน](media/RM-how-to-22.png)

<span data-ttu-id="8cd6c-122">นี่คือตัวอย่างเมื่อหลายทรัพยากรที่มีชื่อมีความจำเป็นในการตอบสนองการร้องขอของทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="8cd6c-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="8cd6c-123">คุณจะต้องจองทรัพยากรหลายรายการเพื่อตอบสนองความต้องการ</span><span class="sxs-lookup"><span data-stu-id="8cd6c-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![การจองทรัพยากรหลายรายการเพื่อตอบสนองความต้องการ](media/RM-how-to-23.png)

<span data-ttu-id="8cd6c-125">ความแตกต่างหลักในสถานการณ์สมมตินี้คือว่า ทรัพยากรทั่วไปยังคงอยู่บนทีมที่กำหนดให้กับงาน และสมาชิกทีมทรัพยากรที่มีชื่อไม่ได้ถูกกำหนดเป็นส่วนหนึ่งของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="8cd6c-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="8cd6c-126">ผู้จัดการโครงการสามารถกำหนดงานตามความเหมาะสมกับทรัพยากรที่มีชื่อ</span><span class="sxs-lookup"><span data-stu-id="8cd6c-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="8cd6c-127">มุมมอง **การกระทบยอด** สามารถช่วยผู้จัดการโครงการในการแบ่งการจองในหลายทรัพยากรไปเป็นการมอบหมายงาน</span><span class="sxs-lookup"><span data-stu-id="8cd6c-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="8cd6c-128">จะไม่มีการทำโดยอัตโนมัติเพราะในสถานการณ์ที่ซับซ้อนมากขึ้นกว่าตัวอย่างง่ายๆ ข้างต้น เช่น เมื่อคุณมีกลุ่มของงานที่ทำให้เกิดความต้องการขึ้น เจตนาของวิธีการที่ผู้จัดการโครงการต้องการที่จะกำหนด จะต้องมีการสันนิษฐานโดยระบบ</span><span class="sxs-lookup"><span data-stu-id="8cd6c-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="8cd6c-129">เนื่องจากระบบไม่สามารถเข้าใจเจตนา ก็มีโอกาสที่สมมติฐานจะแตกต่างจากที่ตั้งใจและผลลัพธ์ที่เกิดขึ้นอาจไม่ถูกต้องหรือคาดเดาไม่ได้</span><span class="sxs-lookup"><span data-stu-id="8cd6c-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="8cd6c-130">ผลลัพธ์ที่คาดการณ์ได้คือเมื่อทรัพยากรทั่วไปยังคงถูกกำหนดไว้จนกว่าผู้จัดการโครงการจะสร้างงานมอบหมายโดยเจตนา ด้วยความช่วยเหลือของมุมมอง **การกระทบยอด**</span><span class="sxs-lookup"><span data-stu-id="8cd6c-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


