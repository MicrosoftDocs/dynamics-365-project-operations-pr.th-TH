---
title: สร้างเท็มเพลตโครงการ
description: วิธีการสร้างเท็มเพลตโครงการใน Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ba15d6d5-a43b-456a-9488-db6e92023fa1
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 50e12d65d5ed957565485413490b8d9f0e2f47ab
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756385"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="f63b5-103">สร้างเท็มเพลตโครงการ (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f63b5-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f63b5-104">เท็มเพลตโครงการประหยัดเวลาของคุณ ถ้าบริษัทของคุณประมูลบนโครงการที่มีชนิดคล้ายกันเป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="f63b5-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="f63b5-105">พวกเขาให้ชุดของบทบาทมาตรฐาน และชั่วโมงที่ประเมินสำหรับชนิดของโครงการ</span><span class="sxs-lookup"><span data-stu-id="f63b5-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="f63b5-106">ผู้จัดการฝ่ายบัญชีและผู้จัดการโครงการสามารถสร้างโครงการที่ยึดตามเท็มเพลตโครงการ หรือพวกเขาสามารถคัดลอกเท็มเพลต และสร้างของตนเอง</span><span class="sxs-lookup"><span data-stu-id="f63b5-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="f63b5-107">องค์ประกอบของเท็มเพลตโครงการ</span><span class="sxs-lookup"><span data-stu-id="f63b5-107">Components of project template</span></span>
 <span data-ttu-id="f63b5-108">เท็มเพลตโครงการประกอบด้วยองค์ประกอบสามรายการ:</span><span class="sxs-lookup"><span data-stu-id="f63b5-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="f63b5-109">**โครงสร้างการแบ่งงาน**: โครงสร้างการแบ่งงานในเท็มเพลตโครงการมีชุดขององค์ประกอบเหมือนกันกับในโครงการ</span><span class="sxs-lookup"><span data-stu-id="f63b5-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="f63b5-110">คุณสามารถสร้างลำดับชั้นงาน เชื่อมโยงบทบาทกับงาน กำหนดแอททริบิวต์การจัดกำหนดการ ตั้งค่าการอ้างอิง และดูข้อมูลทั้งหมดในแผนภูมิ Gantt</span><span class="sxs-lookup"><span data-stu-id="f63b5-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="f63b5-111">นอกจากนี้ โครงสร้างการแบ่งงานในเท็มเพลตโครงการยังสนับสนุนโหมดงานสำหรับงานแต่ละงาน</span><span class="sxs-lookup"><span data-stu-id="f63b5-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="f63b5-112">ไม่มีความแตกต่างใดๆ ระหว่างเท็มเพลตโครงการและโครงการเมื่อมีการสร้างกำหนดการทำงาน</span><span class="sxs-lookup"><span data-stu-id="f63b5-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="f63b5-113">**โครงการประเมิน**: โครงการประเมินในเท็มเพลตทำงานแบบเดียวกับที่ทำในโครงการ ยกเว้นรายการราคาสำหรับการกำหนดค่าเริ่มต้นของต้นทุน และราคาขายเป็นต้นทุนค่าเริ่มต้นเสมอ และรายการราคาขายที่กำหนดไว้ในพารามิเตอร์ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]</span><span class="sxs-lookup"><span data-stu-id="f63b5-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="f63b5-114">ส่วนเหลือของฟังก์ชันการทำงานจะเหมือนกับในโครงการ</span><span class="sxs-lookup"><span data-stu-id="f63b5-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="f63b5-115">**การสร้างแบบฟอร์มของทีมโครงการ**: เมื่อมีการสร้างแบบฟอร์มทีมโครงการสำหรับเท็มเพลตโครงการ คุณไม่สามารถจองทรัพยากรที่มีชื่อในเท็มเพลตได้</span><span class="sxs-lookup"><span data-stu-id="f63b5-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="f63b5-116">คุณสามารถใช้ **สร้างทีมโครงการ** ในโครงสร้างการแบ่งงานเพื่อสร้างชุดของทรัพยากรทั่วไปได้</span><span class="sxs-lookup"><span data-stu-id="f63b5-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="f63b5-117">คุณยังสามารถระบุทักษะที่จำเป็นและประสิทธิภาพสำหรับทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="f63b5-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="f63b5-118">คุณไม่สามารถแทนที่ทรัพยากรทั่วไปด้วยทรัพยากรที่สามารถจองได้เท็มเพลตโครงการ</span><span class="sxs-lookup"><span data-stu-id="f63b5-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="f63b5-119">สร้างโครงการจากเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="f63b5-119">Create a project from a template</span></span>  
 <span data-ttu-id="f63b5-120">คุณสามารถสร้างโครงการจากเท็มเพลตเหล่านี้ด้วยวิธีการดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f63b5-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="f63b5-121">เมื่อมีการสร้างโครงการจากใบเสนอราคา คุณสามารถเลือกเท็มเพลตโครงการ ในแบบฟอร์มการสร้างด่วนของโครงการ</span><span class="sxs-lookup"><span data-stu-id="f63b5-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="f63b5-122">เมื่อมีการสร้างโครงการโดยการคลิก **โครงการใหม่** แบบฟอร์มโครงการจะแสดงก่อนที่คุณบันทึกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="f63b5-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="f63b5-123">จากที่นี่ คุณสามารถคลิกฟิลด์ **เลือกเท็มเพลต** เพื่อเลือกจากรายการของเท็มเพลตโครงการที่กำหนดไว้ล่วงหน้าในองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="f63b5-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="f63b5-124">คลิก **สร้างโครงการจากเท็มเพลต** ในหน้า **เท็มเพลตโครงการ** เพื่อสร้างโครงการจากเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="f63b5-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="f63b5-125">การคัดลอกองค์ประกอบของเท็มเพลตไปยังโครงการ</span><span class="sxs-lookup"><span data-stu-id="f63b5-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="f63b5-126">เมื่อคุณคัดลอกส่วนประกอบของเท็มเพลตลงในโครงการ มีบางสิ่งที่คุณควรรู้</span><span class="sxs-lookup"><span data-stu-id="f63b5-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="f63b5-127">**การคัดลอกโครงสร้างการแบ่งงาน**: เมื่อคุณคัดลอกโครงสร้างการแบ่งงานจากเท็มเพลตโครงการ ถ้าโครงการมีปฏิทินโครงการที่แตกต่างกว่าเท็มเพลต ชั่วโมงทำงานจากปฏิทินของโครงการจะถูกนำมาใช้กับกำหนดการของงาน</span><span class="sxs-lookup"><span data-stu-id="f63b5-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="f63b5-128">นี่ปรับเปลี่ยนกำหนดการไปยังปฏิทินโครงการสำรอง</span><span class="sxs-lookup"><span data-stu-id="f63b5-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="f63b5-129">ในทำนองเดียวกัน งานแรกในโครงสร้างการแบ่งงานใช้วันที่เริ่มต้นของโครงการ ดังนั้นส่วนเหลือของกำหนดการของลำดับชั้นจะถูกอัพเดตตามระยะเวลาและการอ้างอิงที่ระบุไว้ในโครงสร้างการแบ่งงานของเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="f63b5-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="f63b5-130">**การคัดลอกการประเมินโครงการ**: เมื่อคุณคัดลอกข้ามรายการการประเมินโครงการ ราคาตลาดถูกอัพเดตตามหน่วยความเป็นเจ้าของของโครงการสำหรับรายการราคาขายและลูกค้าสำหรับราคาตลาดการขาย</span><span class="sxs-lookup"><span data-stu-id="f63b5-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="f63b5-131">ต้นทุนต่อหน่วยและราคาขายจะถูกกำหนดจากราคาตลาดเหล่านี้ ในโครงการที่เชื่อมโยงกับเอนทิตีการขาย</span><span class="sxs-lookup"><span data-stu-id="f63b5-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="f63b5-132">**การคัดลอกทีมโครงการ**: เมื่อคุณคัดลอกทีมโครงการจากเท็มเพลตโครงการ ทรัพยากรทั่วไปจะถูกการคัดลอกทั้งหมด พร้อมด้วยทักษะและประสิทธิภาพที่กำหนดไว้ในเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="f63b5-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="f63b5-133">การกำหนดทรัพยากรทั่วไปยังจะได้รับการดูแลรักษาเป็นเท็มเพลตโครงการ</span><span class="sxs-lookup"><span data-stu-id="f63b5-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f63b5-134">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f63b5-134">See Also</span></span>  
 [<span data-ttu-id="f63b5-135">คำแนะนำของผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="f63b5-135">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
