---
title: ใช้ตารางหมายกำหนดการให้บริการในการจองทรัพยากรของโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการจองทรัพยากร
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: fa7e34b12f3767e89cc13ddde930e5c9f8ebc565
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086154"
---
# <a name="use-the-schedule-board-to-book-project-resources"></a><span data-ttu-id="3d821-103">ใช้ตารางหมายกำหนดการให้บริการในการจองทรัพยากรของโครงการ</span><span class="sxs-lookup"><span data-stu-id="3d821-103">Use the Schedule Board to book project resources</span></span>

<span data-ttu-id="3d821-104">นอกเหนือจากการจองทรัพยากรในโครงการจากภายในโครงการแล้ว คุณยังสามารถทำการจองทรัพยากรแบบตายตัวหรือแบบไม่ตายตัวจากตารางหมายกำหนดการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="3d821-104">In addition to booking resources on a project from within a project, you can hard-book or soft-book resources from the Schedule Board.</span></span>

<span data-ttu-id="3d821-105">ก่อนที่คุณจะสามารถจองจากตารางหมายกำหนดการให้บริการ คุณต้องสร้างหรือผลิตความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="3d821-105">Before you can book from the Schedule Board, you must create or generate resource requirements.</span></span> <span data-ttu-id="3d821-106">ปฏิบัติตามขั้นตอนเหล่านี้เพื่อนสร้างความต้องการทรัพยากรจากตารางหมายกำหนดการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="3d821-106">Follow these steps to create resource requirements from the Schedule Board.</span></span>

1. <span data-ttu-id="3d821-107">ถ้าหน้าต่าง **ความต้องการในการจอง** ที่ด้านล่างของหน้าถูกยุบ ให้เลือกตัวควบคุมแผ่เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="3d821-107">If the **Booking Requirements** pane at the bottom of the page is collapsed, select the expander control to expand it.</span></span>
2. <span data-ttu-id="3d821-108">ในหน้าต่าง **ความต้องการในการจอง** ในแท็บ **โครงการ** ให้เลือกความต้องการที่ต้องการจะจอง</span><span class="sxs-lookup"><span data-stu-id="3d821-108">In the **Booking Requirements** pane, on the **Project** tab, select the requirement to book.</span></span>

    ![ความต้องการที่เลือกบนแท็บโครงการ](media/Resource-Management-image73.png)

3. <span data-ttu-id="3d821-110">เลือก **ค้นหาความพร้อมใช้งาน** เพื่อกรองทรัพยากรที่สามารถจองได้และดูทรัพยากรที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3d821-110">Select **Find Availability** to filter the bookable resources and view the available resources.</span></span> 
4. <span data-ttu-id="3d821-111">เลือกทรัพยากรอย่างน้อยหนึ่งรายการจากตารางหมายกำหนดการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="3d821-111">Select one or more resources from the Schedule Board.</span></span> 
5. <span data-ttu-id="3d821-112">ในหน้าต่าง **สร้างการจองทรัพยากร** ทางด้านขวาของหน้า ให้ป้อนข้อมูลการจองแล้วเลือก **จองและออก**</span><span class="sxs-lookup"><span data-stu-id="3d821-112">In the **Create Resource Booking** pane on the right side of the page, enter the booking information, and then select **Book and exit**.</span></span>

    ![หน้าต่างสร้างการจองทรัพยากรสำหรับทรัพยากรที่สำรองที่สามารถจองได้ที่เลือกไว้](media/Resource-Management-image74.png)

6. <span data-ttu-id="3d821-114">ในขณะที่ความต้องการถูกเลือกในหน้าต่าง **สร้างการจองทรัพยากร** ให้เลือกเซลล์หนึ่งรายการขึ้นไปของทรัพยากรไปสร้างการจอง</span><span class="sxs-lookup"><span data-stu-id="3d821-114">While the requirement is selected in the **Create Resource Booking** pane, select one or more cells of a resource to create the booking.</span></span>

    ![หลายเซลล์ที่เลือกสำหรับทรัพยากร](media/Resource-Management-image75.png)

7. <span data-ttu-id="3d821-116">เลือก **จอง**</span><span class="sxs-lookup"><span data-stu-id="3d821-116">Select **Book**.</span></span>

<span data-ttu-id="3d821-117">ความต้องการจะดำเนินการโดยการใช้ทรัพยากรที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3d821-117">The requirement is fulfilled by using the selected resource.</span></span> <span data-ttu-id="3d821-118">ในหน้าต่าง **ความต้องการในการจอง** ให้สังเกตว่าความต้องการได้รับการอัพเดตและทรัพยากรจะถูกแสดงเป็นจองในโครงการ</span><span class="sxs-lookup"><span data-stu-id="3d821-118">In the **Booking Requirements** pane, notice that the requirement has been updated, and the resource is shown as booked on the project.</span></span>

![ทรัพยากรที่จองไว้ในโครงการ](media/Resource-Management-image76.png)
