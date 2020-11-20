---
title: มอบหมายทรัพยากรทั่วไปที่จองได้ให้กับงานและทีมโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการจองทรัพยากรทั่วไปให้กับงานและทีมโครงการ
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
ms.openlocfilehash: 19761b3e570ad664522e832069a8ac50fffead64
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127091"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="86e0a-103">มอบหมายทรัพยากรทั่วไปที่จองได้ให้กับงานและสร้างความต้องการทั่วไปของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="86e0a-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="86e0a-104">นอกเหนือจากการจองและการกำหนดทรัพยากรที่มีชื่อหรือทรัพยากรจริงให้กับโครงการของคุณแล้ว คุณสามารถกำหนดทรัพยากรทั่วไปให้กับงานของโครงการได้</span><span class="sxs-lookup"><span data-stu-id="86e0a-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="86e0a-105">ทรัพยากรเหล่านี้สามารถทำหน้าที่เป็นตัวยึดสำหรับทรัพยากรที่มีชื่อจนกว่าคุณจะพร้อมที่จะสรรหาพนักงานสำหรับโครงการของคุณด้วยทรัพยากรที่มีชื่อ</span><span class="sxs-lookup"><span data-stu-id="86e0a-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="86e0a-106">ใน Project Service Automation (PSA) เปิดหน้า **โครงการ** และบนแท็บ **กำหนดการ** ป้อนชื่อตำแหน่งของทรัพยากรทั่วไปในเซลล์ **ทรัพยากร** ของกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="86e0a-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="86e0a-107">หรือคลิกไอคอน **ทรัพยากร** ในเซลล์เพื่อเปิดตัวเลือกทรัพยากรแล้วป้อนชื่อของทรัพยากรทั่วไปที่คุณต้องการสร้าง</span><span class="sxs-lookup"><span data-stu-id="86e0a-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![การสร้างและการกำหนดสมาชิกในทีมทั่วไป](media/RM-how-to-9.png)

<span data-ttu-id="86e0a-109">การทำเช่นนี้จะเป็นการเปิดแผง **การสร้างด่วน: สมาชิกทีมโครงการ** </span><span class="sxs-lookup"><span data-stu-id="86e0a-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="86e0a-110">ป้อนบทบาทและหน่วยองค์กรของสมาชิกทีมทรัพยากรทั่วไป แล้วคลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="86e0a-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![สมาชิกในทีมทั่วไปสร้างอย่างรวดเร็ว](media/RM-how-to-10.png)

3. <span data-ttu-id="86e0a-112">หลังจากที่คุณได้สร้างสมาชิกทีมทรัพยากรทั่วไปใหม่แล้วจะมีการกำหนดไปให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="86e0a-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="86e0a-113">คุณสามารถกำหนดทรัพยากรทั่วไปให้กับงานอื่นๆ ในกำหนดการงานได้ต่อไป</span><span class="sxs-lookup"><span data-stu-id="86e0a-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![การกำหนดสมาชิกในทีมทั่วไปที่มีอยู่ให้กับงาน](media/RM-how-to-11.png)

4. <span data-ttu-id="86e0a-115">หลังจากที่คุณได้กำหนดทรัพยากรทั่วไปแล้ว คุณสามารถสร้างความต้องการของทรัพยากรและทำให้เสร็จได้โดยการจองโดยตรงหรือส่งการร้องขอทรัพยากรไปยังผู้จัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="86e0a-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![การสร้างความต้องการสำหรับสมาชิกทั่วไปในทีม](media/RM-how-to-12.png)

<span data-ttu-id="86e0a-117">ในกริดสมาชิกทีม นอกเหนือจากความสามารถในการใช้ตัวเลือกทรัพยากรดังกล่าวข้างต้น คุณสามารถเพิ่มทรัพยากรทั่วไปได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="86e0a-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="86e0a-118">ทรัพยากรจะถูกเพิ่มด้วยความต้องการทรัพยากรที่ขึ้นอยู่กับวันที่เริ่มต้น/สิ้นสุด และวิธีการจัดสรรที่ระบุไว้ในแผง **การสร้างด่วน: สมาชิกทีมโครงการ**</span><span class="sxs-lookup"><span data-stu-id="86e0a-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="86e0a-119">คุณสามารถดูความแตกต่างหากคุณเพิ่มสมาชิกในทีมทั่วไปโดยตรง จากนั้นกำหนดงานเพิ่มเติมให้กับทรัพยากรทั่วไปมากกว่าชั่วโมงที่ครอบคลุมที่พวกเขาต้องการ</span><span class="sxs-lookup"><span data-stu-id="86e0a-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="86e0a-120">คลิก **สร้างความต้องการ** เพื่อสร้างข้อกำหนดในการสร้างความสมดุลให้กับจำนวนชั่วโมงที่ต้องการกับการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="86e0a-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="86e0a-121">นอกจากนี้คุณยังสามารถคลิกการเชื่อมโยง **ความต้องการทรัพยากร** ในกริดทีมเพื่อเปิดความต้องการและเพิ่มทักษะ ทรัพยากรที่ต้องการ ฯลฯ</span><span class="sxs-lookup"><span data-stu-id="86e0a-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![ความต้องการทรัพยากร](media/RM-how-to-13.png)

