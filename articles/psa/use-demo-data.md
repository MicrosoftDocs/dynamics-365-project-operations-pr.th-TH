---
title: ทดลองกับข้อมูลสาธิต
description: วิธีการดาวน์โหลด และทดลองกับข้อมูลสาธิตสำหรับ Project Service Automation
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
ms.openlocfilehash: e1f3ebf8d0cd6c8e25fcab6775cd92d544867af8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151141"
---
# <a name="experiment-with-demo-data-project-service"></a><span data-ttu-id="b2a3f-103">ทดลองกับข้อมูลสาธิต (Project Service)</span><span class="sxs-lookup"><span data-stu-id="b2a3f-103">Experiment with demo data (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b2a3f-104">เมื่อต้องการทำความคุ้นเคยกับ Dynamics 365 Project Service Automation มีประโยชน์ที่จะมีสภาพแวดล้อมที่กำหนดไว้ล่วงหน้าสำหรับการสำรวจ</span><span class="sxs-lookup"><span data-stu-id="b2a3f-104">To become familiar with Dynamics 365 Project Service Automation, it’s useful to have a pre-configured environment to explore.</span></span> <span data-ttu-id="b2a3f-105">สำหรับวัตถุประสงค์นี้ เราได้สร้างแพ็คเกจการติดตั้งข้อมูลตัวอย่างแยกต่างหาก (ภาษาอังกฤษเท่านั้นในขณะนี้) ที่ทำให้ง่ายต่อการเรียนรู้เกี่ยวกับวิธีการแก้ไขปัญหาเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="b2a3f-105">For this purpose, we’ve created a separate sample data installation package (English-language only at this time) that makes it easier to learn about these solutions.</span></span> 

<span data-ttu-id="b2a3f-106">แพ็คเกจการติดตั้งที่มีอยู่บน [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=859966)</span><span class="sxs-lookup"><span data-stu-id="b2a3f-106">The installation package is available on the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=859966).</span></span>  

<span data-ttu-id="b2a3f-107">การเรียกใช้การติดตั้ง Package Deployer จะทำการดำเนินการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b2a3f-107">Running the Package Deployer install performs the following actions:</span></span> 
  
-   <span data-ttu-id="b2a3f-108">สร้างหรือตั้งค่าพารามิเตอร์เริ่มต้นที่กระตุ้นพฤติกรรมของ Project Service</span><span class="sxs-lookup"><span data-stu-id="b2a3f-108">Creates or sets default parameters that drive behavior of Project Service</span></span>  
  
-   <span data-ttu-id="b2a3f-109">นำเข้าข้อมูลการตัวอย่าง เช่น ทรัพยากรที่สามารถจองได้ บทบาท การขาย และรายการราคาต้นทุน หน่วยทางองค์กร เรกคอร์ดการประมวลผลการขายที่เกี่ยวข้อง ใบสั่งผลิตและโครงการ</span><span class="sxs-lookup"><span data-stu-id="b2a3f-109">Imports sample data such as Bookable Resources, Roles, Sales and Cost Price lists, Organizational Units, relevant sales process records, Work Orders and Projects</span></span>    
  
> [!IMPORTANT]
> <span data-ttu-id="b2a3f-110">**ไม่มีวิธีการยกเลิกการติดตั้งข้อมูลสาธิต**</span><span class="sxs-lookup"><span data-stu-id="b2a3f-110">**There is no way to un-install the demo data.**</span></span> <span data-ttu-id="b2a3f-111">ดังนั้น คุณควรใช้แพคเกจนี้ในการสาธิต การประเมิน การฝึก และระบบทดสอบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b2a3f-111">Therefore, you should only use this package on demonstration, evaluation, training and test systems.</span></span>

<span data-ttu-id="b2a3f-112">สำหรับข้อมูลเพิ่มเติม โปรดดู [blog](https://blogs.msdn.microsoft.com/crm/2017/10/24/microsoft-dynamics-365-for-field-service-and-project-service-automation-sample-data) นี้</span><span class="sxs-lookup"><span data-stu-id="b2a3f-112">For more information, see this [blog](https://blogs.msdn.microsoft.com/crm/2017/10/24/microsoft-dynamics-365-for-field-service-and-project-service-automation-sample-data).</span></span>





  
### <a name="see-also"></a><span data-ttu-id="b2a3f-113">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b2a3f-113">See Also</span></span>  
 <span data-ttu-id="b2a3f-114">[คู่มือของผู้ดูแลระบบ](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="b2a3f-114">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="b2a3f-115">[คำแนะนำผู้จัดการลูกค้าองค์กร](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="b2a3f-115">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="b2a3f-116">[คำแนะนำของผู้จัดการโครงการ](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="b2a3f-116">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="b2a3f-117">[คำแนะนำของผู้จัดการทรัพยากร](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="b2a3f-117">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="b2a3f-118">เวลา ค่าใช้จ่าย และคำแนะนำในการทำงานร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="b2a3f-118">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
