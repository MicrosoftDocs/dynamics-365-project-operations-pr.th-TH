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
ms.openlocfilehash: 49ea8327ae34a69eba1585f1b1b4e557fd4eac93
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283571"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="37811-103">ให้การประเมินงานสำหรับโครงการในระหว่างกระบวนการขาย (Project Service)</span><span class="sxs-lookup"><span data-stu-id="37811-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="37811-104">ในระหว่างกระบวนการขาย คุณสามารถคิดประมาณการยอดขายจากพื้นฐานด้วยบรรทัดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="37811-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="37811-105">ความสามารถของ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ใน [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] จะเป็นวิธีทางวิทยาศาสตร์มากขึ้น และวิธีที่กำหนดที่ตามมาด้วยการประเมินการขาย ด้วยการแบ่งกลุ่มรายการงานและกำหนดความสัมพันธ์ของแอททริบิวต์ที่เกี่ยวข้องไปยังการประเมินสำหรับโครงการในโครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="37811-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="37811-106">เมื่อคุณชนะการขาย คุณสามารถใช้โครงสร้างการแบ่งงานที่เกี่ยวข้องในแผนงานโครงการของคุณ ปรับได้ตามความจำเป็นสำหรับความสำเร็จของโครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="37811-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="37811-107">เชื่อมโยงโครงการไปยังบรรทัดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="37811-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="37811-108">เมื่อสร้างบรรทัดใบเสนอราคาตามโครงการ คุณสามารถสร้างโครงการใหม่จากบรรทัดใบเสนอราคาได้</span><span class="sxs-lookup"><span data-stu-id="37811-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="37811-109">จากนั้นคุณสามารถใช้แม่แบบโครงการ ซึ่งเป็นแผนโครงการมาตรฐานที่กำหนดไว้ล่วงหน้าและการประเมินทางการเงินทั่วไปกับองค์กรของคุณ หรือสำเนาของการวางแผนโครงการและการประเมินจากโครงการในอดีต</span><span class="sxs-lookup"><span data-stu-id="37811-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="37811-110">เมื่อคุณสร้างโครงการ การเลือกแม่แบบโครงการให้เป็นข้อมูลพื้นฐานในการปรับปรุงโครงการแผน การประเมิน และบทบาทของความต้องการ</span><span class="sxs-lookup"><span data-stu-id="37811-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="37811-111">โดยการสร้างโครงการของคุณจากใบเสนอราคา โครงการจะเกี่ยวข้องกับบรรทัดใบเสนอราคาโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="37811-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="37811-112">ส่วนประกอบของการประเมินโครงการ</span><span class="sxs-lookup"><span data-stu-id="37811-112">Project estimate components</span></span>  
 <span data-ttu-id="37811-113">โครงสร้างการแบ่งงานในโครงการให้วิธีการแบ่งงานเป็นงาน การรักษาลำดับชั้นของงาน และกำหนดค่าประมาณของความพยายามที่ต้องใช้ในการดำเนินงานแต่ละงาน</span><span class="sxs-lookup"><span data-stu-id="37811-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="37811-114">นอกจากนี้คุณสามารถเชื่อมโยงบทบาทให้งานเพื่อบ่งชี้ว่าการประเมินของชนิดของทรัพยากรจำเป็นในการดำเนินงานให้เสร็จสมบูรณ์และการกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="37811-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="37811-115">โครงสร้างการแบ่งงานช่วยให้คุณระบุความพยายามในการทำงานและการประเมินกำหนดการได้</span><span class="sxs-lookup"><span data-stu-id="37811-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="37811-116">โดยค่าเริ่มต้น โครงการใช้รายการราคาเริ่มต้นที่คุณกำหนดไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="37811-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="37811-117">ต้นทุนและราคาขายที่กำหนดไว้ในรายการราคาช่วยตรวจสอบการประเมินทางการเงินสำหรับการแบ่งงานของโครงการ</span><span class="sxs-lookup"><span data-stu-id="37811-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="37811-118">ถ้าโครงการของคุณเชื่อมโยงกับใบเสนอราคา และใบเสนอราคามีรายการราคาที่แตกต่างจากค่าเริ่มต้น รายการราคาของใบเสนอราคาจะถูกใช้สำหรับการประเมินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="37811-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="37811-119">นำเข้าการประเมินจากโครงการลงในใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="37811-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="37811-120">เมื่อคุณประเมินโครงการในโครงการ คุณสามารถนำเข้าการประเมินเหล่านี้ลงในบรรทัดใบเสนอราคา:</span><span class="sxs-lookup"><span data-stu-id="37811-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="37811-121">ใน **รายละเอียดบรรทัดใบเสนอราคา** คลิก **นำเข้าจากการประมาณการ**</span><span class="sxs-lookup"><span data-stu-id="37811-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="37811-122">เลือกว่าจะนำเข้าการประเมินโครงการที่สรุปตามชนิดของธุรกรรม บทบาท หรือระดับโหนดโครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="37811-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="37811-123">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="37811-123">See Also</span></span>  
 [<span data-ttu-id="37811-124">คำแนะนำของผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="37811-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]