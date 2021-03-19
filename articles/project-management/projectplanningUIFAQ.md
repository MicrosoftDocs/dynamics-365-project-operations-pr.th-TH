---
title: แก้ไขปัญหาการทำงานในกริดงาน
description: หัวข้อนี้ให้ข้อมูลการแก้ไขปัญหาที่จำเป็น เมื่อทำงานในกริดงาน
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031560"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="8fe4b-103">แก้ไขปัญหาการทำงานในกริดงาน</span><span class="sxs-lookup"><span data-stu-id="8fe4b-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="8fe4b-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="8fe4b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8fe4b-105">หัวข้อนี้อธิบายถึงวิธีการแก้ไขปัญหาที่คุณอาจพบ ขณะทำงานกับการจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8fe4b-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="8fe4b-106">เปิดใช้งานคุกกี้</span><span class="sxs-lookup"><span data-stu-id="8fe4b-106">Enable cookies</span></span>

<span data-ttu-id="8fe4b-107">Project Operations ต้องการให้เปิดใช้งานคุกกี้ของบุคคลที่สามเพื่อแสดงโครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="8fe4b-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="8fe4b-108">เมื่อไม่ได้เปิดใช้งานคุกกี้ของบุคคลที่สาม แทนที่จะเห็นงาน คุณจะเห็นหน้าว่างเปล่า เมื่อคุณเลือกแท็บ **งาน** บนหน้า **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="8fe4b-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![แท็บว่างเมื่อไม่ได้เปิดใช้งานคุกกี้ของบุคคลที่สาม](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="8fe4b-110">การแก้ไข</span><span class="sxs-lookup"><span data-stu-id="8fe4b-110">Workaround</span></span>
<span data-ttu-id="8fe4b-111">สำหรับเบราว์เซอร์ Microsoft Edge หรือ Google Chrome กระบวนงานต่อไปนี้จะอธิบายวิธีอัปเดตการตั้งค่าเบราว์เซอร์ของคุณเพื่อเปิดใช้งานคุกกี้ของบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="8fe4b-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="8fe4b-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8fe4b-112">Microsoft Edge</span></span>

1. <span data-ttu-id="8fe4b-113">เปิดเบราว์เซอร์ Edge ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8fe4b-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="8fe4b-114">ที่มุมบนขวา ให้เลือก **จุดไข่ปลา** (...) และจากนั้น เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="8fe4b-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="8fe4b-115">ภายใต้ **คุกกี้และสิทธิ์ของไซต์** เลือก **คุกกี้และข้อมูลไซต์**</span><span class="sxs-lookup"><span data-stu-id="8fe4b-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="8fe4b-116">ปิด **บล็อกคุกกี้ของบุคคลที่สาม**</span><span class="sxs-lookup"><span data-stu-id="8fe4b-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="8fe4b-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="8fe4b-117">Google Chrome</span></span>

1. <span data-ttu-id="8fe4b-118">เปิดเบราว์เซอร์ Chrome ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8fe4b-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="8fe4b-119">ในมุมขวาบน เลือกจุดแนวตั้งสามจุด และจากนั้นเลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="8fe4b-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="8fe4b-120">ภายใต้ **ความเป็นส่วนตัวและความปลอดภัย** เลือก **คุกกี้และข้อมูลไซต์อื่น**</span><span class="sxs-lookup"><span data-stu-id="8fe4b-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="8fe4b-121">เลือก **ยอมรับคุกกี้ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="8fe4b-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8fe4b-122">หากคุณปิดกั้นคุกกี้ของบุคคลที่สาม คุกกี้และข้อมูลไซต์ทั้งหมดจากไซต์อื่นๆ จะถูกบล็อก แม้ว่าไซต์นั้นจะได้รับอนุญาตในรายการข้อยกเว้นของคุณก็ตาม</span><span class="sxs-lookup"><span data-stu-id="8fe4b-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="8fe4b-123">จุดสิ้นสุด PEX</span><span class="sxs-lookup"><span data-stu-id="8fe4b-123">PEX Endpoint</span></span>

<span data-ttu-id="8fe4b-124">Project Operations ต้องการให้พารามิเตอร์โครงการอ้างอิงจุดสิ้นสุด PEX</span><span class="sxs-lookup"><span data-stu-id="8fe4b-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="8fe4b-125">จุดสิ้นสุดนี้จำเป็นในการสื่อสารกับบริการที่ใช้ในการแสดงผลโครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="8fe4b-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="8fe4b-126">หากไม่ได้เปิดใช้งานพารามิเตอร์ คุณจะได้รับข้อผิดพลาด "พารามิเตอร์โครงการไม่ถูกต้อง"</span><span class="sxs-lookup"><span data-stu-id="8fe4b-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="8fe4b-127">การแก้ไข</span><span class="sxs-lookup"><span data-stu-id="8fe4b-127">Workaround</span></span>
 ![ฟิลด์จุดสิ้นสุด PEX บนพารามิเตอร์โครงการ](media/projectparameter.png)

1. <span data-ttu-id="8fe4b-129">เพิ่มฟิลด์ **จุดสิ้นสุด PEX** ไปยังหน้า **พารามิเตอร์โครงการ**</span><span class="sxs-lookup"><span data-stu-id="8fe4b-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="8fe4b-130">อัปเดตฟิลด์ด้วยค่าต่อไปนี้: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="8fe4b-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="8fe4b-131">ลบฟิลด์ออกจากหน้า **พารามิเตอร์โครงการ**</span><span class="sxs-lookup"><span data-stu-id="8fe4b-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="8fe4b-132">สิทธิ์การใช้งานสำหรับโครงการสำหรับเว็บ</span><span class="sxs-lookup"><span data-stu-id="8fe4b-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="8fe4b-133">Project Operations อาศัยบริการการจัดกำหนดการภายนอก</span><span class="sxs-lookup"><span data-stu-id="8fe4b-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="8fe4b-134">บริการต้องการให้ผู้ใช้มีหลายบทบาทที่ได้รับมอบหมาย เพื่ออ่านและเขียนไปยังเอนทิตีที่เกี่ยวข้องกับโครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="8fe4b-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="8fe4b-135">เอนทิตีเหล่านี้รวมถึงงานโครงการ การมอบหมายทรัพยากร และการอ้างอิงงาน</span><span class="sxs-lookup"><span data-stu-id="8fe4b-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="8fe4b-136">หากผู้ใช้ไม่สามารถแสดงโครงสร้างการแบ่งงานได้ เมื่อไปที่แท็บ **งาน** อาจเป็นเพราะยังไม่ได้เปิดใช้งาน Project for Project Operations</span><span class="sxs-lookup"><span data-stu-id="8fe4b-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="8fe4b-137">ผู้ใช้อาจได้รับข้อผิดพลาด Security role หรือข้อผิดพลาดที่เกี่ยวข้องกับการปฏิเสธการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="8fe4b-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="8fe4b-138">การแก้ไข</span><span class="sxs-lookup"><span data-stu-id="8fe4b-138">Workaround</span></span>

1. <span data-ttu-id="8fe4b-139">ไปที่ **การตั้งค่า > ความปลอดภัย > ผู้ใช้ > ผู้ใช้แอปพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="8fe4b-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![ตัวอ่านแอปพลิเคชัน](media/applicationuser.jpg)
   
2. <span data-ttu-id="8fe4b-141">คลิกสองครั้งที่เรกคอร์ดผู้ใช้แอปพลิเคชันเพื่อตรวจสอบสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8fe4b-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="8fe4b-142">ผู้ใช้มีสิทธิ์เข้าถึงโครงการ</span><span class="sxs-lookup"><span data-stu-id="8fe4b-142">The user has access to the project.</span></span> <span data-ttu-id="8fe4b-143">โดยทั่วไปการตรวจสอบนี้ทำได้โดยการตรวจสอบว่าผู้ใช้มี Security role **ผู้จัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="8fe4b-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="8fe4b-144">มีผู้ใช้แอปพลิเคชัน Microsoft Project อยู่ และได้รับการตั้งค่าคอนฟิกอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="8fe4b-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="8fe4b-145">หากไม่มีผู้ใช้นี้ คุณสามารถสร้างเรกคอร์ดผู้ใช้ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="8fe4b-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="8fe4b-146">เลือก **ผู้ใช้ใหม่**</span><span class="sxs-lookup"><span data-stu-id="8fe4b-146">Select **New Users**.</span></span> <span data-ttu-id="8fe4b-147">เปลี่ยนฟอร์มรายการเป็น **ผู้ใช้แอปพลิเคชัน** แล้วจากนั้นเพิ่ม **รหัสแอปพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="8fe4b-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![รายละเอียดผู้ใช้แอปพลิเคชัน](media/applicationuserdetails.jpg)

4. <span data-ttu-id="8fe4b-149">ตรวจสอบว่าผู้ใช้ได้รับมอบหมายสิทธิ์การใช้งานที่ถูกต้อง และมีการเปิดใช้บริการในรายละเอียดแผนบริการของสิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8fe4b-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="8fe4b-150">ตรวจสอบว่าผู้ใช้สามารถเปิด project.microsoft.com ได้</span><span class="sxs-lookup"><span data-stu-id="8fe4b-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="8fe4b-151">ตรวจสอบผ่านพารามิเตอร์โครงการที่ระบบชี้ไปยังจุดสิ้นสุดโครงการที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="8fe4b-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="8fe4b-152">ตรวจสอบว่าผู้ใช้แอปพลิเคชันโครงการถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="8fe4b-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="8fe4b-153">ใช้ Security role ต่อไปนี้กับผู้ใช้:</span><span class="sxs-lookup"><span data-stu-id="8fe4b-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="8fe4b-154">ผู้ใช้ Dataverse</span><span class="sxs-lookup"><span data-stu-id="8fe4b-154">Dataverse User</span></span>
  - <span data-ttu-id="8fe4b-155">ระบบ Project Operations</span><span class="sxs-lookup"><span data-stu-id="8fe4b-155">Project Operations System</span></span>
  - <span data-ttu-id="8fe4b-156">ระบบโครงการ</span><span class="sxs-lookup"><span data-stu-id="8fe4b-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="8fe4b-157">เกิดข้อผิดพลาดขณะอัปเดตโครงสร้างการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="8fe4b-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="8fe4b-158">เมื่อมีการอัปเดตอย่างน้อยหนึ่งรายการไปยังโครงสร้างการแบ่งงาน การเปลี่ยนแปลงจะล้มเหลวและไม่ได้รับการบันทึกในที่สุด</span><span class="sxs-lookup"><span data-stu-id="8fe4b-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="8fe4b-159">เกิดข้อผิดพลาดในกริดกำหนดการโดยระบุว่า "ไม่สามารถบันทึกการเปลี่ยนแปลงล่าสุดที่คุณทำไว้ได้"</span><span class="sxs-lookup"><span data-stu-id="8fe4b-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="8fe4b-160">การแก้ไข</span><span class="sxs-lookup"><span data-stu-id="8fe4b-160">Workaround</span></span>

1. <span data-ttu-id="8fe4b-161">ตรวจสอบว่าผู้ใช้ได้รับมอบหมายสิทธิ์การใช้งานที่ถูกต้อง และมีการเปิดใช้บริการในรายละเอียดแผนบริการของสิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8fe4b-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="8fe4b-162">ตรวจสอบว่าผู้ใช้สามารถเปิด project.microsoft.com ได้</span><span class="sxs-lookup"><span data-stu-id="8fe4b-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="8fe4b-163">ตรวจสอบว่าระบบชี้ไปยังจุดสิ้นสุดโครงการที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="8fe4b-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="8fe4b-164">ตรวจสอบว่าผู้ใช้แอปพลิเคชัน Project ได้ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="8fe4b-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="8fe4b-165">ใช้ Security role ต่อไปนี้กับผู้ใช้:</span><span class="sxs-lookup"><span data-stu-id="8fe4b-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="8fe4b-166">ผู้ใช้ Dataverse หรือผู้ใช้ฐาน</span><span class="sxs-lookup"><span data-stu-id="8fe4b-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="8fe4b-167">ระบบ Project Operations</span><span class="sxs-lookup"><span data-stu-id="8fe4b-167">Project Operations System</span></span>
  - <span data-ttu-id="8fe4b-168">ระบบโครงการ</span><span class="sxs-lookup"><span data-stu-id="8fe4b-168">Project System</span></span>
  - <span data-ttu-id="8fe4b-169">ระบบเขียนคู่ของ Project Operations (บทบาทนี้จำเป็น หากคุณกำลังปรับใช้สถานการณ์จำลองตามทรัพยากร/ที่ไม่ได้เก็บในคลังของ Project Operations)</span><span class="sxs-lookup"><span data-stu-id="8fe4b-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>