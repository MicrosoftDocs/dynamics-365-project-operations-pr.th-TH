---
title: สร้างหน่วยองค์กร
description: วิธีการสร้างหน่วยองค์กรใน Project Service
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
ms.openlocfilehash: 4c653f5bd066fd174c8fb0996820628c1b281519
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085981"
---
# <a name="create-organizational-units-project-service"></a><span data-ttu-id="af63d-103">สร้างหน่วยองค์กร (Project Service)</span><span class="sxs-lookup"><span data-stu-id="af63d-103">Create organizational units (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="af63d-104">บริษัทของคุณอาจจะจัดระเบียบธุรกิจให้คำปรึกษาตามภูมิศาสตร์ ฟังก์ชัน หรือพื้นที่อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="af63d-104">Your company probably organizes its consulting business by geography, function, or other areas.</span></span> <span data-ttu-id="af63d-105">คุณสามารถสร้างหน่วยองค์กรที่สะท้อนถึงธุรกิจให้คำปรึกษาได้</span><span class="sxs-lookup"><span data-stu-id="af63d-105">You can create organizational units that reflect your consulting business.</span></span> <span data-ttu-id="af63d-106">หน่วยองค์กร [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] เป็นกลุ่มหรือส่วนงานในบริษัทการบริการแบบมืออาชีพที่ใช้ทรัพยากรที่เรียกเก็บเงินได้ ด้วยอัตราต้นทุนที่แตกต่างจากกลุ่มหรือแผนกอื่นๆ ในบริษัท</span><span class="sxs-lookup"><span data-stu-id="af63d-106">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] organizational unit is a group or division in a professional services company that employs billable resources with cost rates that are distinct from other such groups or divisions in the company.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="af63d-107">หน่วยองค์กร [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] จะแยกต่างหากจากหน่วยธุรกิจใน [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)]</span><span class="sxs-lookup"><span data-stu-id="af63d-107">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] organizational unit is separate from a business unit in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="af63d-108">หน่วยธุรกิจมีมากขึ้นจากโครงสร้างการรักษาความปลอดภัยที่มีผลต่อระดับการเข้าถึงข้อมูล [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] และปกติจะถูกจัดระเบียบรอบๆ แผนกของบริษัท เช่น บริษัทแม่ และบริษัทในเครือหรือแผนก</span><span class="sxs-lookup"><span data-stu-id="af63d-108">Business units are more of a security structure that affects levels of access to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] information, and are usually organized around company divisions, like parent company and subsidiaries or divisions.</span></span> <span data-ttu-id="af63d-109">หน่วยองค์กรแสดงถึงวิธีที่บริษัทให้คำปรึกษาของคุณแยกประเภทความแตกต่างของธุรกิจ ตามที่ตั้งทางภูมิศาสตร์ที่ (เช่น EMEA หรือ LATAM), ตามฟังก์ชัน (เช่น การพัฒนาผลิตภัณฑ์หรือเอาท์ซอร์ส IT), หรือตามพารามิเตอร์อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="af63d-109">Organizational units represent how your consulting company categorizes its different businesses, whether by geographic location (like EMEA or LATAM), by function (like Product Development or IT Outsourcing), or by other parameters.</span></span>  
  
1.  <span data-ttu-id="af63d-110">ไปที่ **Project Service > หน่วยองค์กร**</span><span class="sxs-lookup"><span data-stu-id="af63d-110">Go to **Project Service > Organizational Units**.</span></span>  
  
2.  <span data-ttu-id="af63d-111">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="af63d-111">Click **New**.</span></span>  
  
3.  <span data-ttu-id="af63d-112">ในพื้นที่ **ทั่วไป** ป้อนชื่อสำหรับหน่วยองค์กรใน **ชื่อ** แล้วกรอกข้อมูลในฟิลด์อื่นๆ ตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="af63d-112">In the **General** area, enter a name for the organization unit in **Name** , and fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="af63d-113">คลิก **บันทึก** เพื่อสร้างเรกคอร์ดเพื่อที่คุณจะสามารถทำการแก้ไขตอไปได้</span><span class="sxs-lookup"><span data-stu-id="af63d-113">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="af63d-114">ภายใต้ **รายการราคาต้นทุน** คลิก **+** เพื่อเพิ่มราคาตลาด</span><span class="sxs-lookup"><span data-stu-id="af63d-114">Under **Cost Price Lists** , click **+** to add a price list.</span></span> <span data-ttu-id="af63d-115">คุณสามารถเพิ่มราคาตลาดได้เฉพาะกับบริบทที่นี่ได้ **ต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="af63d-115">You can only add price lists with the **Cost** context here.</span></span>  
  
6.  <span data-ttu-id="af63d-116">ในฟิลด์ **ชื่อ** คลิกปุ่ม **ค้นหา** และเลือกราคาตลาดคุณต้องการทำให้ร้อมใช้งานไปที่หน่วยองค์กรนี้</span><span class="sxs-lookup"><span data-stu-id="af63d-116">In the **Name** field, click the **Search** button and select a price list you want to make available to this organizational unit.</span></span> <span data-ttu-id="af63d-117">การเพิ่มราคาตลาดต่อไปตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="af63d-117">Continue adding price lists as needed.</span></span>  
  
7.  <span data-ttu-id="af63d-118">เมื่อคุณทำเสร็จแล้ว คลิก **บันทึก** ที่มุมล่างขวาของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="af63d-118">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="af63d-119">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="af63d-119">See Also</span></span>  
 [<span data-ttu-id="af63d-120">การตั้งค่า Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="af63d-120">Configure Project Service Automation</span></span>](../psa/configure.md)
