---
title: กำหนดการตั้งค่าพารามิเตอร์เพิ่มเติม
description: วิธีการตั้งค่าคอนฟิกการตั้งค่าพารามิเตอร์เพิ่มเติมใน Project Service
author: JohnPBurrows
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
ms.openlocfilehash: f4e883e71beacffb6e2b0b56967046c3f38f7d50
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001134"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="16492-103">ตั้งค่าคอนฟิกการตั้งค่าพารามิเตอร์เพิ่มเติม (Project Service)</span><span class="sxs-lookup"><span data-stu-id="16492-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="16492-104">หลังจากที่คุณได้ตั้งค่าคอนฟิกสินค้าในหัวข้อก่อนหน้านี้ คุณจำเป็นต้องตั้งค่าพารามิเตอร์โครงการเพิ่มเติมเพื่อใช้สำหรับโครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="16492-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="16492-105">เมื่อคุณติดตั้ง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ในตอนแรก คุณได้สร้างการตั้งค่าพารามิเตอร์เพื่อสร้างเรกคอร์ดทั้งหมดที่จำเป็นสำหรับให้ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ทำงานเป็นลำดับแรก</span><span class="sxs-lookup"><span data-stu-id="16492-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="16492-106">ขณะนี้ เป็นเวลาในการย้อนกลับ และตั้งค่าคอนฟิกฟิลด์เพิ่มเติมสำหรับการตั้งค่าเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="16492-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="16492-107">คุณจะต้องตั้งค่าคอนฟิกการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="16492-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="16492-108">หน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="16492-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="16492-109">ความถี่ของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="16492-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="16492-110">เท็มเพลตชั่วโมงทำงาน</span><span class="sxs-lookup"><span data-stu-id="16492-110">Work hours template</span></span>  
  
-   <span data-ttu-id="16492-111">รายการราคา</span><span class="sxs-lookup"><span data-stu-id="16492-111">Price list</span></span>  
 
<span data-ttu-id="16492-112">ในขั้นตอนนี้ คุณจะยังระบุชนิดของการปันส่วนทรัพยากรที่คุณต้องการด้วย:</span><span class="sxs-lookup"><span data-stu-id="16492-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="16492-113">**กลาง**</span><span class="sxs-lookup"><span data-stu-id="16492-113">**Central**.</span></span> <span data-ttu-id="16492-114">เฉพาะผู้จัดการทรัพยากรสามารถปันส่วนทรัพยากรให้กับโครงการได้</span><span class="sxs-lookup"><span data-stu-id="16492-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="16492-115">**ไฮบริด**</span><span class="sxs-lookup"><span data-stu-id="16492-115">**Hybrid**.</span></span> <span data-ttu-id="16492-116">ผู้จัดการทรัพยากร ผู้จัดการโครงการ และผู้จัดการฝ่ายบัญชีสามารถปันส่วนทรัพยากรให้กับโครงการได้</span><span class="sxs-lookup"><span data-stu-id="16492-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="16492-117">เพื่อตั้งค่าพารามิเตอร์โครงการ:</span><span class="sxs-lookup"><span data-stu-id="16492-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="16492-118">ไปที่ **Project Service >พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="16492-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="16492-119">คลิกการตั้งค่าพารามิเตอร์ที่คุณต้องการกำหนดค่า (รายการที่สร้างขึ้นเมื่อคุณติดตั้ง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ในตอนแรก) หรือคลิก **สร้าง** เพื่อสร้างขึ้นใหม่</span><span class="sxs-lookup"><span data-stu-id="16492-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="16492-120">ในพื้นที่ **ทั่วไป** ตั้งค่าตัวเลือกทั้งหมดสำหรับพารามิเตอร์โครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="16492-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="16492-121">ในพื้นที่ **รายการราคา** คลิก **+** เมื่อต้องการเพิ่มรายการราคา เลือกรายการราคาในรายการแบบหล่นลง **รายการราคาของพารามิเตอร์โครงการ** และจากนั้นคลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="16492-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="16492-122">คลิกปุ่ม **บันทึก** ที่มุมล่างขวาของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="16492-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="16492-123">เรกคอร์ดพารามิเตอร์ของโครงการต้องได้รับการปรับปรุงเพื่อให้ Project Service ทำงานได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="16492-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="16492-124">ไม่ควรลบเรกคอร์ดนี้</span><span class="sxs-lookup"><span data-stu-id="16492-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="16492-125">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="16492-125">See Also</span></span>  
 [<span data-ttu-id="16492-126">ตั้งค่าทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="16492-126">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]