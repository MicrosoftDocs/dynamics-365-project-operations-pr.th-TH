---
title: ตั้งค่าโมเดลความชำนาญ
description: วิธีการตั้งค่าโมเดลความชำนาญใน Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 779255971ed4f48bc9410fee76d6591ca13383b9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282446"
---
# <a name="set-up-proficiency-models-project-service"></a><span data-ttu-id="9d81d-103">ตั้งค่าโมเดลความชำนาญ (Project Service)</span><span class="sxs-lookup"><span data-stu-id="9d81d-103">Set up proficiency models (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="9d81d-104">ตอนนี้หลังจากที่คุณได้เพิ่มทักษะสำหรับโครงการในไคลเอนต์ของคุณ คุณจำต้องมีวิธีในการจัดอันดับทักษะที่ปรึกษาของคุณเพื่อให้คุณสามารถจับคู่กับความต้องการของโครงการได้</span><span class="sxs-lookup"><span data-stu-id="9d81d-104">Now that you’ve added the skills for your clients’ projects, you need a way to rate your consultants’ skills so you can match them to project requirements.</span></span> <span data-ttu-id="9d81d-105">คุณสามารถใช้โมเดลความชำนาญเริ่มต้น แก้ไข หรือสร้างขึ้นใหม่เพื่อให้ตรงกับความต้องการขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="9d81d-105">You can use the default proficiency model, edit it, or create a new one to match the needs of your organization.</span></span>  
  
1.  <span data-ttu-id="9d81d-106">ไปที่ **Project Service > โมเดลความชำนาญ**</span><span class="sxs-lookup"><span data-stu-id="9d81d-106">Go to **Project Service > Proficiency Models**.</span></span>  
  
2.  <span data-ttu-id="9d81d-107">เพื่อดูหรือแก้ไขโมเดลความชำนาญเริ่มต้น คลิก **แบบจำลองการจัดอันดับคะแนนเริ่มต้น** ในรายการ หรือ เพื่อสร้างโมเดลความชำนาญใหม่ คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="9d81d-107">To view or edit the default proficiency model, click **Default Rating Model** in the list, or to create a new proficiency model, click **New**.</span></span>  
  
3.  <span data-ttu-id="9d81d-108">ถ้าคุณกำลังสร้างโมเดลความชำนาญใหม่ กรอกข้อมูลในฟิลด์ในพื้นที่ **ทั่วไป** แล้วคลิก **บันทึก** เพื่อสร้างเรกคอร์ดเพื่อให้คุณสามารถทำการแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="9d81d-108">If you’re creating a new proficiency model, fill in the fields in the **General** area, and then click **Save** to create the record so you can continue editing it.</span></span> <span data-ttu-id="9d81d-109">เมื่อคุณสร้างโมเดลความชำนาญของคุณเอง โปรดทราบว่า หมายเลขที่สูงกว่าจะดีกว่า</span><span class="sxs-lookup"><span data-stu-id="9d81d-109">When you create your own proficiency model, keep in mind that higher numbers are better.</span></span>  
  
     <span data-ttu-id="9d81d-110">ตัวอย่างเช่น ถ้าคุณกำลังดู หรือแก้ไขแบบจำลองการประเมินค่าเริ่มต้น คุณจะเห็นระดับความชำนาญดังต่อไปนี้ใน **ค่าการจัดอันดับคะแนน**</span><span class="sxs-lookup"><span data-stu-id="9d81d-110">For example, if you’re viewing or editing the default rating model, you’ll see the following proficiency levels in **Rating Values**.</span></span>  
  
    |<span data-ttu-id="9d81d-111">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="9d81d-111">Name</span></span>|<span data-ttu-id="9d81d-112">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="9d81d-112">Value</span></span>|  
    |----------|-----------|  
    |<span data-ttu-id="9d81d-113">คุ้นเคย</span><span class="sxs-lookup"><span data-stu-id="9d81d-113">Familiar</span></span>|<span data-ttu-id="9d81d-114">1</span><span class="sxs-lookup"><span data-stu-id="9d81d-114">1</span></span>|  
    |<span data-ttu-id="9d81d-115">ดี</span><span class="sxs-lookup"><span data-stu-id="9d81d-115">Good</span></span>|<span data-ttu-id="9d81d-116">2</span><span class="sxs-lookup"><span data-stu-id="9d81d-116">2</span></span>|  
    |<span data-ttu-id="9d81d-117">มีความชำนาญ</span><span class="sxs-lookup"><span data-stu-id="9d81d-117">Proficient</span></span>|<span data-ttu-id="9d81d-118">3</span><span class="sxs-lookup"><span data-stu-id="9d81d-118">3</span></span>|  
  
4.  <span data-ttu-id="9d81d-119">เพื่อเพิ่มหรือเปลี่ยนแปลงระดับความชำนาญ คลิกปุ่มตาราง และทำการเปลี่ยนแปลงคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="9d81d-119">To add or change a proficiency level, click the table button and make the changes you want.</span></span>  
  
5.  <span data-ttu-id="9d81d-120">คลิกปุ่ม **บันทึก** ที่มุมล่างขวาของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="9d81d-120">Click the **Save** button in the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="9d81d-121">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9d81d-121">See Also</span></span>  
 [<span data-ttu-id="9d81d-122">ตั้งค่าทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="9d81d-122">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]