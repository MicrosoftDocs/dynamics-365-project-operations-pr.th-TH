---
title: ทดลองกับข้อมูลสาธิต
description: วิธีการดาวน์โหลด และทดลองกับข้อมูลสาธิตสำหรับ Project Service Automation
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: b195e5c8-63bc-4e90-914c-f29b8d565942
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 76dd5ff14cbafbfc5341885f0469a6e3e71dd66f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756459"
---
# <a name="experiment-with-demo-data-project-service"></a><span data-ttu-id="6db46-103">ทดลองกับข้อมูลสาธิต (Project Service)</span><span class="sxs-lookup"><span data-stu-id="6db46-103">Experiment with demo data (Project Service)</span></span>

<span data-ttu-id="6db46-104">เมื่อต้องการทำความคุ้นเคยกับ Dynamics 365 Project Service Automation มีประโยชน์ที่จะมีสภาพแวดล้อมที่กำหนดไว้ล่วงหน้าสำหรับการสำรวจ</span><span class="sxs-lookup"><span data-stu-id="6db46-104">To become familiar with Dynamics 365 Project Service Automation, it’s useful to have a pre-configured environment to explore.</span></span> <span data-ttu-id="6db46-105">สำหรับวัตถุประสงค์นี้ เราได้สร้างแพ็คเกจการติดตั้งข้อมูลตัวอย่างแยกต่างหาก (ภาษาอังกฤษเท่านั้นในขณะนี้) ที่ทำให้ง่ายต่อการเรียนรู้เกี่ยวกับวิธีการแก้ไขปัญหาเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="6db46-105">For this purpose, we’ve created a separate sample data installation package (English-language only at this time) that makes it easier to learn about these solutions.</span></span> 

<span data-ttu-id="6db46-106">แพ็คเกจการติดตั้งที่มีอยู่บน [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=859966)</span><span class="sxs-lookup"><span data-stu-id="6db46-106">The installation package is available on the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=859966).</span></span>  

<span data-ttu-id="6db46-107">การเรียกใช้การติดตั้ง Package Deployer จะทำการดำเนินการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6db46-107">Running the Package Deployer install performs the following actions:</span></span> 
  
-   <span data-ttu-id="6db46-108">สร้างหรือตั้งค่าพารามิเตอร์เริ่มต้นที่กระตุ้นพฤติกรรมของ Project Service</span><span class="sxs-lookup"><span data-stu-id="6db46-108">Creates or sets default parameters that drive behavior of Project Service</span></span>  
  
-   <span data-ttu-id="6db46-109">นำเข้าข้อมูลการตัวอย่าง เช่น ทรัพยากรที่สามารถจองได้ บทบาท การขาย และรายการราคาต้นทุน หน่วยทางองค์กร เรกคอร์ดการประมวลผลการขายที่เกี่ยวข้อง ใบสั่งผลิตและโครงการ</span><span class="sxs-lookup"><span data-stu-id="6db46-109">Imports sample data such as Bookable Resources, Roles, Sales and Cost Price lists, Organizational Units, relevant sales process records, Work Orders and Projects</span></span>    
  
> [!IMPORTANT]
> <span data-ttu-id="6db46-110">**ไม่มีวิธีการยกเลิกการติดตั้งข้อมูลสาธิต**</span><span class="sxs-lookup"><span data-stu-id="6db46-110">**There is no way to un-install the demo data.**</span></span> <span data-ttu-id="6db46-111">ดังนั้น คุณควรใช้แพคเกจนี้ในการสาธิต การประเมิน การฝึก และระบบทดสอบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6db46-111">Therefore, you should only use this package on demonstration, evaluation, training and test systems.</span></span>

<span data-ttu-id="6db46-112">สำหรับข้อมูลเพิ่มเติม โปรดดู [blog](https://blogs.msdn.microsoft.com/crm/2017/10/24/microsoft-dynamics-365-for-field-service-and-project-service-automation-sample-data) นี้</span><span class="sxs-lookup"><span data-stu-id="6db46-112">For more information, see this [blog](https://blogs.msdn.microsoft.com/crm/2017/10/24/microsoft-dynamics-365-for-field-service-and-project-service-automation-sample-data).</span></span>





  
### <a name="see-also"></a><span data-ttu-id="6db46-113">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6db46-113">See Also</span></span>  
 <span data-ttu-id="6db46-114">[คู่มือของผู้ดูแลระบบ](../project-service/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="6db46-114">[Administrator Guide](../project-service/admin-guide.md) </span></span>  
 <span data-ttu-id="6db46-115">[คำแนะนำผู้จัดการลูกค้าองค์กร](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="6db46-115">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="6db46-116">[คำแนะนำของผู้จัดการโครงการ](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="6db46-116">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="6db46-117">[คำแนะนำของผู้จัดการทรัพยากร](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="6db46-117">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="6db46-118">เวลา ค่าใช้จ่าย และคำแนะนำในการทำงานร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="6db46-118">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)
