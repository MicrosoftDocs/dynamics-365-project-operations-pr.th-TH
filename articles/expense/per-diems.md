---
title: เบี้ยเลี้ยง
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับกฎค่าเบี้ยเลี้ยงต่อวันที่ใช้ในการจัดการค่าใช้จ่าย
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b1476bfc0386412762c30e5a00acaff65bfbe3c7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995284"
---
# <a name="per-diems"></a><span data-ttu-id="1dfcc-103">เบี้ยเลี้ยง</span><span class="sxs-lookup"><span data-stu-id="1dfcc-103">Per diems</span></span>

<span data-ttu-id="1dfcc-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="1dfcc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="1dfcc-105">ค่าเบี้ยเลี้ยงต่อวันคือเบี้ยเลี้ยงที่จ่ายให้กับผู้ปฏิบัติงานที่กำลังเดินทางไปทำงาน</span><span class="sxs-lookup"><span data-stu-id="1dfcc-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="1dfcc-106">ในการจัดการค่าใช้จ่าย คุณสามารถสร้างกฎค่าเบี้ยเลี้ยงต่อวันสำหรับสถานการณ์การเดินทางต่างๆ</span><span class="sxs-lookup"><span data-stu-id="1dfcc-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="1dfcc-107">ค่าเบี้ยเลี้ยงต่อวันอาจขึ้นอยู่กับช่วงเวลาของปี สถานที่เดินทาง หรือทั้งสองอย่าง</span><span class="sxs-lookup"><span data-stu-id="1dfcc-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="1dfcc-108">เมื่อคุณสร้างกฎค่าเบี้ยเลี้ยงต่อวัน คุณสามารถระบุว่าเปอร์เซ็นต์ของอัตราค่าเบี้ยเลี้ยงต่อวันจะถูกระงับหากผู้ปฏิบัติงานได้รับอาหารหรือบริการฟรี</span><span class="sxs-lookup"><span data-stu-id="1dfcc-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="1dfcc-109">คุณยังสามารถกำหนดจำนวนชั่วโมงขั้นต่ำและสูงสุดที่อัตราค่าเบี้ยเลี้ยงต่อวันใช้กับการเดินทางของผู้ปฏิบัติงานได้</span><span class="sxs-lookup"><span data-stu-id="1dfcc-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="1dfcc-110">การกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="1dfcc-110">Configuration</span></span> 

1. <span data-ttu-id="1dfcc-111">หากต้องการเพิ่มสถานที่สำหรับค่าเบี้ยเลี้ยงต่อวัน ให้ไปที่ **ตั้งค่า** > **การคำนวณและรหัส** > **สถานที่สำหรับค่าเบี้ยเลี้ยงต่อวัน**</span><span class="sxs-lookup"><span data-stu-id="1dfcc-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="1dfcc-112">สำหรับแต่ละสถานที่ที่เพิ่มไว้ข้างต้น ให้เลือกอัตราค่าเบี้ยเลี้ยงต่อวันและสกุลเงินที่ใช้ได้ระหว่างวันที่เริ่มต้นและวันที่สิ้นสุดที่เฉพาะเจาะจงสำหรับโรงแรม มื้ออาหาร และค่าใช้จ่ายอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="1dfcc-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="1dfcc-113">อัตราค่าเบี้ยเลี้ยงต่อวันและสกุลเงินได้รับการกำหนดค่าภายใต้ **ตั้งค่า** > **การคำนวณและรหัส** > **ค่าเบี้ยเลี้ยงต่อวัน**</span><span class="sxs-lookup"><span data-stu-id="1dfcc-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="1dfcc-114">บนเพจ **สถานที่สำหรับค่าเบี้ยเลี้ยงต่อวัน** กำหนดค่าระดับอัตราค่าเบี้ยเลี้ยงต่อวัน</span><span class="sxs-lookup"><span data-stu-id="1dfcc-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="1dfcc-115">ระดับอัตราค่าเบี้ยเลี้ยงต่อวันช่วยให้คุณสามารถกำหนดเปอร์เซ็นต์การแบ่งค่าเบี้ยเลี้ยงรายวันสำหรับโรงแรม มื้ออาหาร และค่าใช้จ่ายอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="1dfcc-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="1dfcc-116">หากต้องการระบุการลดเปอร์เซ็นต์ค่าอาหารสำหรับมื้อเช้า กลางวัน หรือเย็น ให้ปรับปรุงฟิลด์ในเพจ **พารามิเตอร์การจัดการค่าใช้จ่าย** บนแท็บ **ค่าเบี้ยเลี้ยงต่อวัน**</span><span class="sxs-lookup"><span data-stu-id="1dfcc-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="1dfcc-117">ส่งค่าใช้จ่ายโดยใช้ค่าเบี้ยเลี้ยงต่อวัน</span><span class="sxs-lookup"><span data-stu-id="1dfcc-117">Submit expenses using per diem</span></span>
<span data-ttu-id="1dfcc-118">หากต้องการส่งค่าใช้จ่ายที่ใช้ค่าเบี้ยเลี้ยงต่อวัน ให้ใช้ประเภทค่าใช้จ่าย **ค่าเบี้ยเลี้ยงต่อวัน** เมื่อคุณสร้างรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="1dfcc-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="1dfcc-119">ป้อน **ค่าเบี้ยเลี้ยงต่อวันจากวันที่**, **ค่าเบี้ยเลี้ยงต่อวันถึงวันที่** และ **สถานที่สำหรับค่าเบี้ยเลี้ยงต่อวัน**</span><span class="sxs-lookup"><span data-stu-id="1dfcc-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="1dfcc-120">จำนวนเงินจะคำนวณตามอัตราค่าเบี้ยเลี้ยงต่อวันสำหรับสถานที่ที่เลือกและการลดมื้ออาหารจะคำนวณตามระดับอัตราค่าเบี้ยเลี้ยงต่อวัน</span><span class="sxs-lookup"><span data-stu-id="1dfcc-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]