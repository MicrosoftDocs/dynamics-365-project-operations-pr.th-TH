---
title: แบบจำลองทักษะและความชำนาญ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้แบบจำลองทักษะและความชำนาญ
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.openlocfilehash: cd243544df062e5801bbfa0a3bd75c4d9a116a6f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086152"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="7a897-103">แบบจำลองทักษะและความชำนาญ</span><span class="sxs-lookup"><span data-stu-id="7a897-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7a897-104">ทักษะ คือคุณลักษณะทรัพยากรที่ใช้ร่วมกันระหว่าง Dynamics 365 Project Service Automation และ Dynamics 365 Field Service (ถ้ามี)</span><span class="sxs-lookup"><span data-stu-id="7a897-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="7a897-105">เมื่อต้องการรักษาการบันทึกทักษะใน Project Service Automation ไปที่ **ทรัพยากร** \> **ทักษะของทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="7a897-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![ทักษะของทรัพยากร](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="7a897-107">ใช้แบบจำลองความชำนาญเพื่อจัดอันดับคะแนนทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7a897-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="7a897-108">ทักษะสำหรับทรัพยากรจะถูกจัดอันดับคะแนนโดยแบบจำลองความชำนาญ</span><span class="sxs-lookup"><span data-stu-id="7a897-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="7a897-109">การจัดอันดับคะแนนรายบุคคลจะอยู่ในรูปแบบที่มีความชำนาญ</span><span class="sxs-lookup"><span data-stu-id="7a897-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="7a897-110">หากต้องการสร้างแบบจำลองความชำนาญ ไปที่ **ทรัพยากร** \> **แบบจำลองความชำนาญ** แล้วเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="7a897-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="7a897-111">ในแบบจำลองการจัดอันดับคะแนนใหม่ ระบุค่าการจัดอันดับต่ำสุด ค่าจัดอันดับสูงสุด และเอนทิตี้ที่กำลังทำการจัดอันดับคะแนนให้</span><span class="sxs-lookup"><span data-stu-id="7a897-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="7a897-112">ใน Sub-grid **ค่าการจัดอันดับคะแนน** คุณสามารถกำหนดค่าการจัดอันดับที่แตกต่างกันได้ตั้งแต่ต่ำสุดไปจนถึงสูงสุด</span><span class="sxs-lookup"><span data-stu-id="7a897-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![ค่าต่ำสุดและสูงสุดของอันดับคะแนนถูกกำหนดแล้ว](media/Resource-Management-image85.png)

<span data-ttu-id="7a897-114">ค่าอันดับคะแนนเหล่านี้จะแสดงในตัวกรอง **ความต้องการทรัพยากร** **ตารางกำหนดการ** และ **ตัวช่วยจัดการกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="7a897-114">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>
