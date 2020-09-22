---
title: ใช้ Add-in ของ Project Service เพื่อวางแผนการทำงานของคุณใน Microsoft Project | MicrosoftDocs
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการเพิ่ม การตั้งค่าคอนฟิก และการใช้ add-in ของ Microsoft Project สำหรับ Project Service
author: ruhercul
manager: kfend
ms.service: Dynamics 365 Project Service Automation
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: efd589e0-8233-4abf-bf7e-5c1e83c4daea
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0ad503ff0c27f1543d15b60714c2be46b8487d18
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756389"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="43ef3-103">ใช้ Add-in Project Service Automation เพื่อวางแผนการทำงานของคุณใน Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="43ef3-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="43ef3-104">ทำให้การวางแผนโครงการของคุณ รวมถึงการประเมินง่ายขึ้นสำหรับคุณ</span><span class="sxs-lookup"><span data-stu-id="43ef3-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="43ef3-105">คุณสามารถกำหนดงาน เพื่อให้ต้นทุน ความพยายาม และมูลค่าขายนั้นชัดเจน เมื่อข้อเสนอขั้นสุดท้ายถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="43ef3-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="43ef3-106">ขณะนี้ คุณสามารถติดตั้ง [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] และทำงานด้านการวางแผนของคุณในสภาพแวดล้อมที่คุ้นเคยของ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="43ef3-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="43ef3-107">ใช้ความสามารถในการวางแผนและการจัดการที่สมบูรณ์ของ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] แล้วอัพเดตแผนโครงการของคุณใน Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="43ef3-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="43ef3-108">ในการใช้คุณลักษณะการจัดการเอกสารของ SharePoint เพื่อจัดเก็บไฟล์ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ของคุณ สำหรับโครงการ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ผู้ดูแลระบบ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ของคุณ จำเป็นต้องเปิดใช้งานการจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="43ef3-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="43ef3-109">[เปิดใช้งานการจัดการเอกสาร SharePoint สำหรับเอนทิตีที่ระบุ](../admin/enable-sharepoint-document-management-specific-entities.md)</span><span class="sxs-lookup"><span data-stu-id="43ef3-109">[Enable SharePoint document management for specific entities](../admin/enable-sharepoint-document-management-specific-entities.md)</span></span>  
> - <span data-ttu-id="43ef3-110">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] จะเข้ากันได้กับ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="43ef3-110">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="43ef3-111">ดาวน์โหลดและติดตั้ง add-in</span><span class="sxs-lookup"><span data-stu-id="43ef3-111">Download and install the add-in</span></span>  
 <span data-ttu-id="43ef3-112">เตรียมข้อมูลการลงชื่อเข้าใช้ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ของคุณให้พร้อม</span><span class="sxs-lookup"><span data-stu-id="43ef3-112">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="43ef3-113">คุณจะต้องใช้ข้อมูลนี้ในการเชื่อมต่อจาก [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]</span><span class="sxs-lookup"><span data-stu-id="43ef3-113">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="43ef3-114">จากศูนย์ดาวน์โหลด ดาวน์โหลด Add-in สำหรับรุ่นที่ได้รับการสนับสนุนของ Project Service ของคุณ ทั้ง [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) หรือ [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956)</span><span class="sxs-lookup"><span data-stu-id="43ef3-114">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="43ef3-115">คลิกการเชื่อมโยงดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="43ef3-115">Click the download link.</span></span>  

3.  <span data-ttu-id="43ef3-116">เมื่อการดาวน์โหลดเสร็จสมบูรณ์ คลิก **ใช่** เพื่อติดตั้ง add-in</span><span class="sxs-lookup"><span data-stu-id="43ef3-116">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="43ef3-117">ตั้งค่าคอนฟิก add-in</span><span class="sxs-lookup"><span data-stu-id="43ef3-117">Configure the add-in</span></span>  

1. <span data-ttu-id="43ef3-118">เปิดโครงการ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] และคลิกแท็บ **Project Service**</span><span class="sxs-lookup"><span data-stu-id="43ef3-118">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="43ef3-119">คลิก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="43ef3-119">Click **Connect**.</span></span>  

3. <span data-ttu-id="43ef3-120">ป้อนข้อมูลการเข้าสู่ระบบของคุณ และจากนั้นคลิก **ลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="43ef3-120">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="43ef3-121">ตอนนี้ คุณสามารถเริ่มการใช้ add-in ได้</span><span class="sxs-lookup"><span data-stu-id="43ef3-121">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="43ef3-122">อ่านจากเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="43ef3-122">Read from a template</span></span>  
 <span data-ttu-id="43ef3-123">อ่านจากเท็มเพลตที่คุณได้สร้างขึ้นใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] และได้คัดลอกลงใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] เพื่อเริ่มการวางแผนโครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="43ef3-123">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="43ef3-124">[สร้างเท็มเพลตโครงการ (Project Service Automation)](../project-service/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="43ef3-124">[Create a project template (Project Service Automation)](../project-service/create-project-template.md)</span></span>  

1.  <span data-ttu-id="43ef3-125">จากแท็บ **Project Service** คลิก **อ่าน** > **เท็มเพลต Project Service Automation**</span><span class="sxs-lookup"><span data-stu-id="43ef3-125">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="43ef3-126">เลือกเท็มเพลตโครงการจากรายการ และจากนั้นคลิก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="43ef3-126">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="43ef3-127">โดยค่าเริ่มต้น งานที่จะถูกคัดลอกจากเท็มเพลตลงในโครงการจะถูกตั้งค่าเป็น จัดกำหนดการแล้วด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="43ef3-127">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="43ef3-128">มอบหมายบทบาท [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ให้กับทรัพยากรโครงการ</span><span class="sxs-lookup"><span data-stu-id="43ef3-128">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="43ef3-129">เปิดโครงการและคลิกที่ ribbon ของ **งาน**</span><span class="sxs-lookup"><span data-stu-id="43ef3-129">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="43ef3-130">คลิกเมนู **แผนภูมิ Gantt** แล้วเลือก **แผ่นงานทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="43ef3-130">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="43ef3-131">บนแผ่นงานทรัพยากร คลิกเมนูแบบหล่นลงของ **บทบาททรัพยากรของ Project Service** และเลือกบทบาท Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="43ef3-131">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="43ef3-132">หาพนักงานให้กับโครงการของคุณพร้อมกับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="43ef3-132">Staff your project with resources</span></span>  

1.  <span data-ttu-id="43ef3-133">จากแท็บ Project Service ทั้งหมด ให้เลือกแถว และคลิก **ค้นหาทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="43ef3-133">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="43ef3-134">บนหน้าจอ **จองทรัพยากร** เลือกทรัพยากรที่คุณต้องการใช้สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="43ef3-134">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="43ef3-135">คลิก **จอง** แล้วคลิก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="43ef3-135">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="43ef3-136">เผยแพร่โครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="43ef3-136">Publish your project</span></span>  
<span data-ttu-id="43ef3-137">เมื่อการวางแผนโครงการของคุณเสร็จสมบูรณ์แล้ว ขั้นตอนถัดไปคือการนำเข้าและการเผยแพร่โครงการใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]</span><span class="sxs-lookup"><span data-stu-id="43ef3-137">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="43ef3-138">โครงการจะนำเข้าไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]</span><span class="sxs-lookup"><span data-stu-id="43ef3-138">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="43ef3-139">กระบวนการการกำหนดราคาและการสร้างทีมงานจะถูกนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="43ef3-139">The pricing and team generation process are applied.</span></span> <span data-ttu-id="43ef3-140">เปิดโครงการใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] เพื่อดูว่าทีม การประเมินโครงการ และโครงสร้างการแบ่งงาน ได้ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="43ef3-140">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="43ef3-141">ตารางต่อไปนี้แสดงตำแหน่งที่จะพบผลลัพธ์:</span><span class="sxs-lookup"><span data-stu-id="43ef3-141">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="43ef3-142">**แผนภูมิแกนต์**</span><span class="sxs-lookup"><span data-stu-id="43ef3-142">**Gantt Chart**</span></span>   | <span data-ttu-id="43ef3-143">นำเข้าลงในหน้าจอ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **โครงสร้างการแบ่งงาน**</span><span class="sxs-lookup"><span data-stu-id="43ef3-143">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="43ef3-144">**รีเฟรชแผ่นงานทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="43ef3-144">**Resource Sheet**</span></span> |   <span data-ttu-id="43ef3-145">นำเข้าลงในหน้าจอ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]**สมาชิกทีมโครงการ**</span><span class="sxs-lookup"><span data-stu-id="43ef3-145">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="43ef3-146">**ใช้การใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="43ef3-146">**Use Usage**</span></span>    |    <span data-ttu-id="43ef3-147">นำเข้าลงในหน้าจอ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **การประเมินโครงการ**</span><span class="sxs-lookup"><span data-stu-id="43ef3-147">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="43ef3-148">**เมื่อต้องการนำเข้าและเผยแพร่โครงการของคุณ**</span><span class="sxs-lookup"><span data-stu-id="43ef3-148">**To import and publish your project**</span></span>  
1. <span data-ttu-id="43ef3-149">จากแท็บ **Project Service** คลิก **เผยแพร่** > **Project Service Automation ใหม่**</span><span class="sxs-lookup"><span data-stu-id="43ef3-149">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="43ef3-150">ในกล่องโต้ตอบ **เผยแพร่ไปยังโครงการใหม่ใน Project Service** ป้อน **ชื่อโครงการ** และเลือก **ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="43ef3-150">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="43ef3-151">สามารถเลือกที่จะตรวจสอบ **เชื่อมโยงแผนงานโครงการกับ Project Service Automation** เพื่อเชื่อมโยงแฟ้มโครงการของแผนไปยัง Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="43ef3-151">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="43ef3-152">คลิก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="43ef3-152">Click **Publish**.</span></span>  

   <span data-ttu-id="43ef3-153">การเชื่อมโยงแฟ้มโครงการไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ทำให้แฟ้มโครงการเป็นต้นแบบ และตั้งค่าโครงสร้างการแบ่งงานใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ให้เป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="43ef3-153">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="43ef3-154">เมื่อต้องการทำการเปลี่ยนแปลงไปยังรายการแผนการของโครงการ คุณต้องดำเนินการใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] และเผยแพร่เป็นการปรับปรุงไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]</span><span class="sxs-lookup"><span data-stu-id="43ef3-154">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="43ef3-155">แก้ไขโครงการที่ได้มีการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="43ef3-155">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="43ef3-156">เมื่อต้องการทำการเปลี่ยนแปลงไปยังการวางแผนโครงการ ที่ได้ถูกนำเข้าลงใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] คุณมีสองตัวเลือก:</span><span class="sxs-lookup"><span data-stu-id="43ef3-156">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="43ef3-157">เปิดแฟ้มหลัก และแก้ไขใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="43ef3-157">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="43ef3-158">ยกเลิกการเชื่อมโยงแฟ้ม และแก้ไขใน Project Service โดยตรง</span><span class="sxs-lookup"><span data-stu-id="43ef3-158">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="43ef3-159">โดยค่าเริ่มต้น โครงการที่ได้ถูกอัพโหลดจากโครงการของ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ถูกล็อก และสามารถแก้ไขได้ในโครงการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="43ef3-159">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="43ef3-160">เมื่อต้องการแก้ไขแฟ้มใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] แฟ้มต้องถูกยกเลิกการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="43ef3-160">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="43ef3-161">แก้ไขใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="43ef3-161">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="43ef3-162">จากเมนูหลัก คลิก **Project Service** > **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="43ef3-162">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="43ef3-163">จากรายการของโครงการ เปิดรายการที่คุณสร้างขึ้นใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="43ef3-163">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="43ef3-164">คลิก **เปิดในโครงการ MS** จาก ribbon</span><span class="sxs-lookup"><span data-stu-id="43ef3-164">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="43ef3-165">นี่จะเปิดแฟ้มหลักที่เชื่อมโยงในโครงการของ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="43ef3-165">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="43ef3-166">ยกเลิกการเชื่อมโยงแฟ้ม และแก้ไขใน Project Service ของ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="43ef3-166">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="43ef3-167">จากเมนูหลัก คลิก **Project Service** > **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="43ef3-167">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="43ef3-168">จากรายการของโครงการ เปิดรายการที่คุณสร้างขึ้นใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="43ef3-168">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="43ef3-169">คลิก **ยกเลิกการเชื่อมโยงจากโครงการ MS** จาก ribbon</span><span class="sxs-lookup"><span data-stu-id="43ef3-169">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="43ef3-170">อัพโหลดแฟ้มโครงการไปยัง SharePoint หรือกลุ่ม Office</span><span class="sxs-lookup"><span data-stu-id="43ef3-170">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="43ef3-171">คุณสามารถอัพโหลดแฟ้มโครงการของคุณไปยัง SharePoint และค้นหาภายใต้เอกสารที่เกี่ยวข้องสำหรับโครงการ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ของคุณ</span><span class="sxs-lookup"><span data-stu-id="43ef3-171">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="43ef3-172">คุณจำเป็นต้องให้ผู้ดูแลของคุณตั้งค่าคอนฟิกการจัดการเอกสารของ SharePoint และเปิดใช้งานสำหรับเอนทิตีของโครงการ</span><span class="sxs-lookup"><span data-stu-id="43ef3-172">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="43ef3-173">[ตั้งค่าการรวม SharePoint](../admin/set-up-sharepoint-integration.md)</span><span class="sxs-lookup"><span data-stu-id="43ef3-173">[Set up SharePoint integration](../admin/set-up-sharepoint-integration.md)</span></span>  

 <span data-ttu-id="43ef3-174">นอกจากนี้ คุณยังสามารถอัพโหลดแฟ้มโครงการของคุณไปยัง [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] ได้ ถ้าคุณได้ตั้งค่ากลุ่มของ Office</span><span class="sxs-lookup"><span data-stu-id="43ef3-174">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="43ef3-175">[ทำงานร่วมกับผู้ร่วมงานของคุณโดยใช้กลุ่ม Office 365](../basics/collaborate-with-colleagues-using-office-365-groups.md)</span><span class="sxs-lookup"><span data-stu-id="43ef3-175">[Collaborate with your colleagues using Office 365 Groups](../basics/collaborate-with-colleagues-using-office-365-groups.md)</span></span>  

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="43ef3-176">อัปโหลดไฟล์ สำหรับ SharePoint</span><span class="sxs-lookup"><span data-stu-id="43ef3-176">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="43ef3-177">จากเมนูหลัก คลิก **Project Service** > **อัพโหลด**</span><span class="sxs-lookup"><span data-stu-id="43ef3-177">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="43ef3-178">เลือก **ไปยังเอกสารโครงการของ Project Service Automation**</span><span class="sxs-lookup"><span data-stu-id="43ef3-178">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="43ef3-179">ในกล่องโต้ตอบ **เปิดใช้งานการเปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** เลือก **ใช่** หรือ **ไม่ใช่**</span><span class="sxs-lookup"><span data-stu-id="43ef3-179">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="43ef3-180">เมื่อคุณคลิก **ใช่** คุณจะสามารถเลือกปุ่ม **เปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ใน Project Service Automation เปิดใช้งาน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] และโหลดแฟ้มโครงการจากไลบรารีเอกสาร SharePoint</span><span class="sxs-lookup"><span data-stu-id="43ef3-180">If you click **Yes**, you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="43ef3-181">หากคุณคลิก **ไม่ใช่** การเชื่อมโยงสำหรับปุ่ม **เปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** จะไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="43ef3-181">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="43ef3-182">แฟ้ม [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] สามารถถูกพบได้ใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ภายใต้ **เอกสาร** สำหรับโครงการ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] เฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="43ef3-182">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="43ef3-183">อัพโหลดแฟ้มสำหรับกลุ่ม Office</span><span class="sxs-lookup"><span data-stu-id="43ef3-183">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="43ef3-184">จากเมนูหลัก คลิก **Project Service** > **อัพโหลด**</span><span class="sxs-lookup"><span data-stu-id="43ef3-184">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="43ef3-185">เลือก **ไปยังเอกสารโครงการของ Project Service Automation**</span><span class="sxs-lookup"><span data-stu-id="43ef3-185">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="43ef3-186">ในกล่องโต้ตอบ **เปิดใช้งานการเปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** เลือก **ใช่** หรือ **ไม่ใช่**</span><span class="sxs-lookup"><span data-stu-id="43ef3-186">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="43ef3-187">เมื่อคุณคลิก **ใช่** คุณจะสามารถเลือกปุ่ม **เปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ใน Project Service Automation เปิดใช้งาน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] และโหลดแฟ้มโครงการจากไลบรารีเอกสาร SharePoint</span><span class="sxs-lookup"><span data-stu-id="43ef3-187">If you click **Yes**, you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="43ef3-188">หากคุณคลิก **ไม่ใช่** การเชื่อมโยงสำหรับปุ่ม **เปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** จะไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="43ef3-188">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="43ef3-189">แฟ้ม [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] สามารถถูกพบได้ใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ภายใต้ **เอกสาร** สำหรับโครงการ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] เฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="43ef3-189">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="43ef3-190">เผยแพร่โครงการของคุณเป็นเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="43ef3-190">Publish  your project as a template</span></span>  
 <span data-ttu-id="43ef3-191">คุณสามารถบันทึกโครงการของคุณ และนำมาใช้ใหม่ได้โดยการบันทึกเป็นเท็มเพลตโครงการใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]</span><span class="sxs-lookup"><span data-stu-id="43ef3-191">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="43ef3-192">เท็มเพลตโครงการเป็นแผนโครงการที่สามารถนำมาใช้ใหม่ได้ใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]</span><span class="sxs-lookup"><span data-stu-id="43ef3-192">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="43ef3-193">[สร้างเท็มเพลตโครงการ (Project Service Automation)](../project-service/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="43ef3-193">[Create a project template (Project Service Automation)](../project-service/create-project-template.md)</span></span>  

1. <span data-ttu-id="43ef3-194">จากแท็บ **Project Service** คลิก **เผยแพร่** > **เท็มเพลตโครงการ Project Service Automation ใหม่**</span><span class="sxs-lookup"><span data-stu-id="43ef3-194">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="43ef3-195">ในกล่องโต้ตอบ **เผยแพร่ไปยังโครงการใหม่ในเท็มเพลต Project Service** ป้อน **ชื่อเท็มเพลตโครงการ**</span><span class="sxs-lookup"><span data-stu-id="43ef3-195">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="43ef3-196">หรือสามารถเลือกตรวจสอบ **เชื่อมโยงแผนงานโครงการกับ Project Service Automation** เพื่อเชื่อมโยงแฟ้มโครงการไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]</span><span class="sxs-lookup"><span data-stu-id="43ef3-196">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="43ef3-197">คลิก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="43ef3-197">Click **Publish**.</span></span>  

<span data-ttu-id="43ef3-198">การเชื่อมโยงแฟ้มโครงการไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ทำให้แฟ้มโครงการเป็นต้นแบบ และตั้งค่าโครงสร้างการแบ่งงานในเท็มเพลต [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ให้เป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="43ef3-198">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="43ef3-199">เมื่อต้องการทำการเปลี่ยนแปลงไปยังรายการแผนการของโครงการ คุณต้องดำเนินการใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] และเผยแพร่เป็นการปรับปรุงไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]</span><span class="sxs-lookup"><span data-stu-id="43ef3-199">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="43ef3-200">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="43ef3-200">See Also</span></span>  
 [<span data-ttu-id="43ef3-201">คำแนะนำของผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="43ef3-201">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
