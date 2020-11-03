---
title: กำหนดค่าบทบาทของทรัพยากร
description: วิธีการตั้งค่าคอนฟิกบทบาทของทรัพยากรใน Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 5f899d17980df16602c964bab4bbab1e976b3ebf
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085930"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="4cca7-103">ตั้งค่าคอนฟิกบทบาทของทรัพยากร (Project Service)</span><span class="sxs-lookup"><span data-stu-id="4cca7-103">Configure resource roles (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="4cca7-104">บทบาทเล่นส่วนสำคัญในการวางแผนโครงการ การกำหนดความต้องการทรัพยากรหรือต้นทุนของโครงการ</span><span class="sxs-lookup"><span data-stu-id="4cca7-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="4cca7-105">สำหรับแต่ละบทบาทที่โครงการของคุณจำเป็นต้องมี คุณจำเป็นต้องสร้างบทบาทของทรัพยากรและเชื่อมโยงทักษะและความชำนาญกับบทบาทนั้น</span><span class="sxs-lookup"><span data-stu-id="4cca7-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="4cca7-106">ตัวอย่างเช่น คุณอาจต้องการสร้างบทบาทสำหรับนักพัฒนา ผู้จัดการโครงการ หรือผู้ทดสอบเกม</span><span class="sxs-lookup"><span data-stu-id="4cca7-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="4cca7-107">คุณยังสามารถกำหนดทักษะและระดับความชำนาญที่จำเป็นสำหรับบทบาท</span><span class="sxs-lookup"><span data-stu-id="4cca7-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="4cca7-108">การกำหนดค่ากบทบาททรัพยากรเพื่อให้แน่ใจว่าการประเมินโครงการจะผลบังคับใช้สำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="4cca7-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="4cca7-109">หรือทำให้แน่ใจว่า คุณตั้งค่าชนิดการเรียกเก็บเงินได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="4cca7-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="4cca7-110">การตั้งค่ารายการด้วยชนิดการเรียกเก็บเงินมีชนิดที่ไม่สามารถคิดค่าธรรมเนียมได้จะไม่แสดงค่าบนบรรทัดในสัญญาหรือในใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="4cca7-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="4cca7-111">ทันทีที่คุณได้ติดตั้งบทบาททรัพยากร คุณสามารถตั้งค่าต้นทุนและราคาขายกับราคาตลาด</span><span class="sxs-lookup"><span data-stu-id="4cca7-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="4cca7-112">สำหรับแต่ละบทบาทที่คุณต้องการเพิ่ม ให้ทำสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4cca7-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="4cca7-113">ไปที่ **Project Service > บทบาทของทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="4cca7-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="4cca7-114">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="4cca7-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="4cca7-115">ในพื้นที่ **ทั่วไป** ป้อนชื่อสำหรับบทบาทใน **ชื่อ** แล้วกรอกข้อมูลในฟิลด์อื่นๆ ตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="4cca7-115">In the **General** area, enter a name for the role in **Name** , and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="4cca7-116">คลิก **บันทึก** เพื่อสร้างเรกคอร์ดเพื่อที่คุณจะสามารถทำการแก้ไขตอไปได้</span><span class="sxs-lookup"><span data-stu-id="4cca7-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="4cca7-117">ในพื้นที่ **ทักษะ** คลิก **+** เพื่อเพิ่มทักษะ</span><span class="sxs-lookup"><span data-stu-id="4cca7-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="4cca7-118">ในบานหน้าต่าง **ข้อกำหนดความสามารถของบทบาท** คลิกในฟิลด์ **ทักษะ** คลิกปุ่ม **ค้นหา** แล้วเลือกทักษะ</span><span class="sxs-lookup"><span data-stu-id="4cca7-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="4cca7-119">เลือกความชำนาญสำหรับทักษะนั้น แล้วคลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="4cca7-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="4cca7-120">การเพิ่มทักษะตามความจำเป็นต่อไป</span><span class="sxs-lookup"><span data-stu-id="4cca7-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="4cca7-121">เมื่อคุณทำเสร็จแล้ว คลิก **บันทึก** ที่มุมล่างขวาของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="4cca7-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="4cca7-122">เพื่อทำให้บทบาทของทรัพยากรพร้อมใช้งานสำหรับโครงการที่จะใช้ คลิก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="4cca7-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="4cca7-123">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4cca7-123">See Also</span></span>  
 [<span data-ttu-id="4cca7-124">ตั้งค่าทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="4cca7-124">Set up resources</span></span>](../psa/set-up-resources.md)
