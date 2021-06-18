---
title: ภาพรวมการใช้ประโยชน์ของทรัพยากร
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการใช้ประโยชน์ของทรัพยากรใน Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a683931bcd6a357c5feec9198b190b948ad17a40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000819"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="44d1a-103">ภาพรวมการใช้ประโยชน์ของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="44d1a-103">Resource utilization overview</span></span>

<span data-ttu-id="44d1a-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="44d1a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="44d1a-105">ทรัพยากรสามารถมีการใช้ประโยชน์ที่เรียกเก็บเงินได้ของเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="44d1a-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="44d1a-106">การใช้ประโยชน์เป้าหมายนี้ถูกกำหนดเป็นแอตทริบิวต์ในบทบาทเริ่มต้นของทรัพยากร หรือตั้งค่าในเรกคอร์ดของทรัพยากรที่สามารถจองได้แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="44d1a-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="44d1a-107">การคำนวณการใช้ประโยชน์จะขึ้นอยู่กับชั่วโมงจริงที่ทรัพยากรได้ถูกรายงานโดยใช้รายการเวลาที่ได้รับอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="44d1a-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="44d1a-108">สูตรต่อไปนี้จะใช้ในการคำนวณการใช้ประโยชน์:</span><span class="sxs-lookup"><span data-stu-id="44d1a-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="44d1a-109">การใช้ประโยชน์ที่เรียกเก็บเงินได้ = ชั่วโมงที่คิดค่าธรรมเนียมจริง ÷ กำลังการผลิตทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="44d1a-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="44d1a-110">การใช้ประโยชน์ที่เรียกเก็บเงินไม่ได้ = เวลาจริงกับรหัสชนิดของการชำระเงิน = ไม่สามารถคิดค่าธรรมเนียมได้หรือไม่มีอยู่ ÷ กำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="44d1a-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="44d1a-111">ภายใน = เวลาจริงโดยไม่มีสัญญาขาย ÷ กำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="44d1a-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="44d1a-112">กำลังการผลิตทรัพยากร = ชั่วโมงทำงานของทรัพยากร – ไม่อยู่ที่สำนักงาน – วันที่ไม่ใช่วันทำงาน</span><span class="sxs-lookup"><span data-stu-id="44d1a-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="44d1a-113">คุณสามารถพบมุมมอง **การใช้ประโยชน์ทรัพยากร** ได้ในบานหน้าต่าง **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="44d1a-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="44d1a-114">แต่ละเซลล์ในกริดแสดงเปอร์เซ็นต์การใช้ประโยชน์ที่เรียกเก็บเงินได้ของทรัพยากรในรอบระยะเวลานึง เช่นเป็นวัน เป็นสัปดาห์ หรือเป็นเดือน</span><span class="sxs-lookup"><span data-stu-id="44d1a-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="44d1a-115">สูตรต่อไปนี้จะใช้ในการลงสีให้เซลล์:</span><span class="sxs-lookup"><span data-stu-id="44d1a-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="44d1a-116">**สีเขียว**: การใช้ประโยชน์ที่เรียกเก็บเงินได้ > =การใช้ประโยชน์เป้าหมายทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="44d1a-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="44d1a-117">**สีเหลือง**: การใช้ประโยชน์เป้าหมาย – 20 < = การใช้ประโยชน์ที่เรียกเก็บเงินได้ < การใช้ประโยชน์เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="44d1a-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="44d1a-118">**สีแดง**: การใช้ประโยชน์ที่เรียกเก็บเงินได้ < การใช้ประโยชน์เป้าหมาย – 20</span><span class="sxs-lookup"><span data-stu-id="44d1a-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="44d1a-119">เนื่องจากมุมมอง **การใช้ทรัพยากร** อิงตามตารางกำหนดการ คุณสามารถใช้ความสามารถในการกรองของตารางกำหนดการเพื่อกรองผลลัพธ์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="44d1a-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="44d1a-120">กริดจำเป็นต้องให้คุณตั้งค่าการใช้ประโยชน์เป้าหมายในบทบาทหรือทรัพยากรแต่ละอย่าง</span><span class="sxs-lookup"><span data-stu-id="44d1a-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="44d1a-121">เมื่อต้องการดำเนินการนี้ ไปที่ **ทรัพยากร** > **บทบาทของทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="44d1a-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="44d1a-122">นอกจากนี้ บทบาทเริ่มต้นต้องถูกมอบหมายให้กับทรัพยากรที่สามารถจองได้แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="44d1a-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="44d1a-123">ไปที่ **ทรัพยากร** > **ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="44d1a-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="44d1a-124">ในแท็บ **Project Service** ให้ตรวจสอบว่ามีการมอบหมายบทบาททรัพยากร และฟิลด์ **เป็นค่าเริ่มต้น** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="44d1a-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="44d1a-125">คุณสามารถเพิ่มบทบาทเพิ่มเติมที่การตั้งค่า **เป็นค่าเริ่มต้น** = **ไม่**</span><span class="sxs-lookup"><span data-stu-id="44d1a-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="44d1a-126">บทบาทที่ **เป็นค่าเริ่มต้น** = **ใช่** จะถูกใช้ในการประเมินผลการใช้ของทรัพยากรเทียบกับเป้าหมายสำหรับบทบาทนั้น</span><span class="sxs-lookup"><span data-stu-id="44d1a-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="44d1a-127">บนแท็บ **Project Service** คุณสามารถตั้งค่าการใช้งานเป้าหมายแต่ละรายการสำหรับทรัพยากรได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="44d1a-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="44d1a-128">การคำนวณการใช้ประโยชน์จะใช้การใช้ประโยชน์เป้าหมายนั้นเพื่อประเมินเป้าหมายของทรัพยากรแทนที่จะประเมินจากเป้าหมายของบทบาทเริ่มต้นของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="44d1a-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="44d1a-129">การใช้ประโยชน์จะแสดงขึ้นสำหรับทรัพยากรเท่านั้น หากทรัพยากรนั้นได้การรับอนุมัติ เวลาที่คิดค่าธรรมเนียมในระหว่างรอบระยะเวลาจะแสดงในกริด</span><span class="sxs-lookup"><span data-stu-id="44d1a-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]