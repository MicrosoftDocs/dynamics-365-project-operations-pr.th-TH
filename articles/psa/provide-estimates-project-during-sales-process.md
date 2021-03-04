---
title: ให้ทำประเมินสำหรับโครงการในระหว่างกระบวนการขาย
description: วิธีการให้การประเมินงานสำหรับโครงการในระหว่างกระบวนการขายใน Project Service
author: ruhercul
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
ms.openlocfilehash: e9382127b2ce0b157d681fc77d67200ba9c5e59d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147991"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="618fe-103">ให้การประเมินงานสำหรับโครงการในระหว่างกระบวนการขาย (Project Service)</span><span class="sxs-lookup"><span data-stu-id="618fe-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="618fe-104">ในระหว่างกระบวนการขาย คุณสามารถคิดประมาณการยอดขายจากพื้นฐานด้วยบรรทัดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="618fe-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="618fe-105">ความสามารถของ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ใน [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] จะเป็นวิธีทางวิทยาศาสตร์มากขึ้น และวิธีที่กำหนดที่ตามมาด้วยการประเมินการขาย ด้วยการแบ่งกลุ่มรายการงานและกำหนดความสัมพันธ์ของแอททริบิวต์ที่เกี่ยวข้องไปยังการประเมินสำหรับโครงการในโครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="618fe-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="618fe-106">เมื่อคุณชนะการขาย คุณสามารถใช้โครงสร้างการแบ่งงานที่เกี่ยวข้องในแผนงานโครงการของคุณ ปรับได้ตามความจำเป็นสำหรับความสำเร็จของโครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="618fe-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="618fe-107">เชื่อมโยงโครงการไปยังบรรทัดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="618fe-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="618fe-108">เมื่อสร้างบรรทัดใบเสนอราคาตามโครงการ คุณสามารถสร้างโครงการใหม่จากบรรทัดใบเสนอราคาได้</span><span class="sxs-lookup"><span data-stu-id="618fe-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="618fe-109">จากนั้นคุณสามารถใช้แม่แบบโครงการ ซึ่งเป็นแผนโครงการมาตรฐานที่กำหนดไว้ล่วงหน้าและการประเมินทางการเงินทั่วไปกับองค์กรของคุณ หรือสำเนาของการวางแผนโครงการและการประเมินจากโครงการในอดีต</span><span class="sxs-lookup"><span data-stu-id="618fe-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="618fe-110">เมื่อคุณสร้างโครงการ การเลือกแม่แบบโครงการให้เป็นข้อมูลพื้นฐานในการปรับปรุงโครงการแผน การประเมิน และบทบาทของความต้องการ</span><span class="sxs-lookup"><span data-stu-id="618fe-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="618fe-111">โดยการสร้างโครงการของคุณจากใบเสนอราคา โครงการจะเกี่ยวข้องกับบรรทัดใบเสนอราคาโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="618fe-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="618fe-112">ส่วนประกอบของการประเมินโครงการ</span><span class="sxs-lookup"><span data-stu-id="618fe-112">Project estimate components</span></span>  
 <span data-ttu-id="618fe-113">โครงสร้างการแบ่งงานในโครงการให้วิธีการแบ่งงานเป็นงาน การรักษาลำดับชั้นของงาน และกำหนดค่าประมาณของความพยายามที่ต้องใช้ในการดำเนินงานแต่ละงาน</span><span class="sxs-lookup"><span data-stu-id="618fe-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="618fe-114">นอกจากนี้คุณสามารถเชื่อมโยงบทบาทให้งานเพื่อบ่งชี้ว่าการประเมินของชนิดของทรัพยากรจำเป็นในการดำเนินงานให้เสร็จสมบูรณ์และการกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="618fe-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="618fe-115">โครงสร้างการแบ่งงานช่วยให้คุณระบุความพยายามในการทำงานและการประเมินกำหนดการได้</span><span class="sxs-lookup"><span data-stu-id="618fe-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="618fe-116">โดยค่าเริ่มต้น โครงการใช้ราคาตลาดเริ่มต้นที่คุณกำหนดไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="618fe-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="618fe-117">ต้นทุนและราคาขายที่กำหนดไว้ในราคาตลาดช่วยตรวจสอบการประเมินทางการเงินสำหรับการแบ่งงานของโครงการ</span><span class="sxs-lookup"><span data-stu-id="618fe-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="618fe-118">ถ้าโครงการของคุณเชื่อมโยงกับใบเสนอราคา และใบเสนอราคามีราคาตลาดที่แตกต่างจากค่าเริ่มต้น ราคาตลาดของใบเสนอราคาจะถูกใช้สำหรับการประเมินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="618fe-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="618fe-119">นำเข้าการประเมินจากโครงการลงในใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="618fe-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="618fe-120">เมื่อคุณประเมินโครงการในโครงการ คุณสามารถนำเข้าการประเมินเหล่านี้ลงในบรรทัดใบเสนอราคา:</span><span class="sxs-lookup"><span data-stu-id="618fe-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="618fe-121">ใน **รายละเอียดบรรทัดใบเสนอราคา** คลิก **นำเข้าจากการประมาณการ**</span><span class="sxs-lookup"><span data-stu-id="618fe-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="618fe-122">เลือกว่าจะนำเข้าการประเมินโครงการที่สรุปตามชนิดของธุรกรรม บทบาท หรือระดับโหนดโครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="618fe-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="618fe-123">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="618fe-123">See Also</span></span>  
 [<span data-ttu-id="618fe-124">คำแนะนำของผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="618fe-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
