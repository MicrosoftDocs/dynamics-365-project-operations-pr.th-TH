---
title: กำหนดทักษะและความเชี่ยวชาญ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการตั้งค่าแบบจำลองความเชี่ยวชาญที่จะจัดอันดับทรัพยากร
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.openlocfilehash: 8738a4743554704ef76807c81fdefcd74e668e1b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124796"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="9c7e5-103">กำหนดทักษะและความเชี่ยวชาญ</span><span class="sxs-lookup"><span data-stu-id="9c7e5-103">Define skills and proficiencies</span></span>

<span data-ttu-id="9c7e5-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="9c7e5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9c7e5-105">ทักษะ คือคุณลักษณะทรัพยากรที่ใช้ร่วมกันระหว่าง Dynamics 365 Project Operations และ Dynamics 365 Field Service (ถ้ามี)</span><span class="sxs-lookup"><span data-stu-id="9c7e5-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="9c7e5-106">เมื่อต้องการรักษาการบันทึกทักษะใน Project Operations ไปที่ **ทรัพยากร** \> **ทักษะของทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="9c7e5-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="9c7e5-107">ใช้แบบจำลองความชำนาญเพื่อจัดอันดับคะแนนทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="9c7e5-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="9c7e5-108">ทักษะสำหรับทรัพยากรจะถูกจัดอันดับคะแนนโดยแบบจำลองความชำนาญ</span><span class="sxs-lookup"><span data-stu-id="9c7e5-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="9c7e5-109">การจัดอันดับคะแนนรายบุคคลจะอยู่ในรูปแบบที่มีความชำนาญ</span><span class="sxs-lookup"><span data-stu-id="9c7e5-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="9c7e5-110">หากต้องการสร้างแบบจำลองความชำนาญ ไปที่ **ทรัพยากร** \> **แบบจำลองความชำนาญ** แล้วเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="9c7e5-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="9c7e5-111">ในแบบจำลองการจัดอันดับคะแนนใหม่ ระบุค่าการจัดอันดับต่ำสุด ค่าจัดอันดับสูงสุด และเอนทิตี้ที่กำลังทำการจัดอันดับคะแนนให้</span><span class="sxs-lookup"><span data-stu-id="9c7e5-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="9c7e5-112">ในกริดย่อย **ค่าการจัดอันดับคะแนน** คุณสามารถกำหนดค่าการจัดอันดับที่แตกต่างกันได้ตั้งแต่ต่ำสุดไปจนถึงสูงสุด</span><span class="sxs-lookup"><span data-stu-id="9c7e5-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="9c7e5-113">ค่าอันดับคะแนนเหล่านี้จะแสดงในตัวกรอง **ความต้องการทรัพยากร** **ตารางกำหนดการ** และ **ตัวช่วยจัดการกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="9c7e5-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
