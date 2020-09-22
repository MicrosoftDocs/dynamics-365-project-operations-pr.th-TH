---
title: จัดการทรัพยากร
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับวิธีที่คุณสามารถจัดการกับทรัพยากร
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 39893019-123b-4bc6-8a2b-a37bc517dc97
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 6c199cbadd1c78e7e29c0cda0febde4236a13d96
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756513"
---
# <a name="manage-resources"></a><span data-ttu-id="962f4-103">จัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-103">Manage resources</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="962f4-104">Dynamics 365 Project Service Automation รวมแดชบอร์ดผู้จัดการทรัพยากรที่ให้ภาพรวมที่เห็นได้ของความต้องการของทรัพยากรและการใช้ประโยชน์ทั่วทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="962f4-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="962f4-105">คุณสามารถใช้แผนภูมิบนแดชบอร์ดนี้เพื่อช่วยแสดงภาพของของข้อมูลดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="962f4-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="962f4-106">**ความต้องการของทรัพยากร** – แผนภูมิ **Active Resource Request** แสดงทรัพยากรที่ถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="962f4-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="962f4-107">ทรัพยากรถูกรวมเข้าด้วยกันโดยบทบาทหรือโครงการ</span><span class="sxs-lookup"><span data-stu-id="962f4-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="962f4-108">**ความต้องการของทรัพยากรที่ไม่ได้ส่งมา** – แผนภูมิ **Unassigned Resource Demand** จะแสดงข้อกำหนดของทรัพยากรทั้งหมดที่ไม่ได้ถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="962f4-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="962f4-109">ยังช่วยผู้จัดการทรัพยากรดูความต้องการที่ยังไม่ได้รับการยืนยันหรือที่อาจจะส่งผ่านการร้องขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="962f4-110">**การใช้ประโยชน์ที่เรียกเก็บได้สำหรับสัปดาห์ที่ผ่านมา** – แผนภูมิ **การใช้ประโยชน์ตามบทบาท** แสดงเปอร์เซ็นต์ของการใช้ประโยชน์ที่เรียกเก็บได้จริงขององค์กรตามบทบาทเทียบกับการใช้ประโยชน์ที่เรียกเก็บเงินได้ตามเป้าหมายตามบทบาท</span><span class="sxs-lookup"><span data-stu-id="962f4-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="962f4-111">เพื่อทำให้แผนภูมิ **การใช้ประโยชน์ตามบทบาท** พร้อมใช้งาน สร้างงานที่รันเวิร์กโฟลว์ UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="962f4-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="962f4-112">งานที่เกิดซ้ำนี้รันทุกๆเจ็ดเพื่อคำนวณการใช้ประโยชน์ที่เรียกเก็บได้สำหรับเจ็ดวันก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="962f4-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="962f4-113">ผลลัพธ์ถูกรวมเข้าด้วยกันโดยบทบาท</span><span class="sxs-lookup"><span data-stu-id="962f4-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="962f4-114">จัดการสมาชิกในทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="962f4-114">Manage project team members</span></span>

<span data-ttu-id="962f4-115">ผู้จัดการโครงการสามารถใช้แดชบอร์ดผู้จัดการทรัพยากรเพื่อจัดการทรัพยากรในโครงการ</span><span class="sxs-lookup"><span data-stu-id="962f4-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="962f4-116">ตัวอย่างเช่น พวกเขาสามารถเพิ่มสมาชิกทีมไปที่โครงการและจองสมาชิกในทีมเพื่อตอบสนองความต้องการทรัพยากรที่ถูกบันทึกโดยทรัพยากรทั่วไปได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="962f4-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="962f4-117">เพิ่มสมาชิกในกลุ่มไปยังโครงการได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="962f4-117">Add a team member directly to a project</span></span>

<span data-ttu-id="962f4-118">เพื่อเพิ่มสมาชิกในกลุ่มไปยังโครงการได้โดยตรง บนเพจ **โครงการ** บนแท็บ **ทีม** เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="962f4-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="962f4-119">**สร้างด่วน: สมาชิกในทีมโครงการ** กล่องโต้ตอบปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="962f4-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="962f4-120">ในกล่องโต้ตอบนี้ คุณสามารถทำงานเหล่านี้ได้:</span><span class="sxs-lookup"><span data-stu-id="962f4-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="962f4-121">**จองทรัพยากรที่ระบุชื่อ** – ในฟิล์ด **Bookable Resource** แล้วเลือกชื่อของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="962f4-122">จากนั้นเลือกบทบาท กำหนดระยะเวลา และเลือกวิธีการจัดสรร</span><span class="sxs-lookup"><span data-stu-id="962f4-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="962f4-123">ทรัพยากรที่ระบุชื่อที่คุณเลือกได้ถูกเพิ่มไปในโครงการโดยการใช้วิธีการจัดสรรและปฏิทินทรัพยากรที่เลือกมา</span><span class="sxs-lookup"><span data-stu-id="962f4-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="962f4-124">**เพิ่มทรัพยากรทั่วไป** – เว้นฟิล์ด **ทรัพยากรที่สามารถจองได้** ว่างไว้ จากนั้นเลือกบทบาท กำหนดระยะเวลา เลือกวิธีการจัดสรรที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="962f4-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="962f4-125">ทรัพยากรทั่วไปถูกเพิ่มไปยังทีมเป็นตัวยึดตำแหน่งเพื่อถือรูปแบบความต้องการที่ถูกใช้ในการจองทรัพยากรที่ระบุชื่อในทีม</span><span class="sxs-lookup"><span data-stu-id="962f4-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="962f4-126">ความต้องการเกิดขึ้นตามปฏิทินโครงการ</span><span class="sxs-lookup"><span data-stu-id="962f4-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="962f4-127">**เพิ่มทรัพยากรที่ระบุชื่อในทีมโดยไม่ต้องใช้กำลังการผลิตของทรัพยากร** – ในฟิล์ด **Bookable Resource** แล้วเลือกทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="962f4-128">จากนั้นเลือกระยะเวลา และเลือก **ไม่มี** เป็นวิธีการจัดสรร</span><span class="sxs-lookup"><span data-stu-id="962f4-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="962f4-129">ทรัพยากรที่ถูกเพิ่มไปยังทีมแต่กำลังการผลิตของทรัพยากรยังไม่ถูกใช้ผ่านการจอง</span><span class="sxs-lookup"><span data-stu-id="962f4-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="962f4-130">จองสมาชิกในทีมเพื่อทำตามความต้อองการทรัพยากรสำหรับทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="962f4-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="962f4-131">ใน PSA คุณสามารถจองทรัพยากรทั่วไปในทีมโครงการและสามารถระบุบทบาท กำลังการผลิตที่ต้องการ และวิธีที่การผลิตนั้นกระจายออกไป</span><span class="sxs-lookup"><span data-stu-id="962f4-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="962f4-132">ในความต้องการทรัพยากร คุณสามารถระบุแอตทริบิวต์ที่เกี่ยวข้องกับทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="962f4-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="962f4-133">แอตทริบิวต์เหล่านี้รวมไปถึงทักษะที่จำเป็น หน่อยองค์กรที่ต้องการ และทรัพยากรที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="962f4-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="962f4-134">ทำตามขั้นตอนต่อไปนี้เพื่อระบุทักษะที่จำเป็นในทรัพยากรทั่วไปสำหรับนักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="962f4-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="962f4-135">ในหน้า **โครงการ** , ในแท็บ **ทีม** , เลือก **สร้าง** เพื่อจองทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="962f4-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![ทรัพยากรทั่วไปที่จองไว้ในทีม](media/Resource-Management-image9.png)

2. <span data-ttu-id="962f4-137">ในมุมมอง **สมาชิกในทีมทั้งหมด** ในคอลัมน์ **ความต้องการทรัพยากร** เลือกลิงก์เพื่อเพิ่มทักษะที่จำเป็นสำหรับทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="962f4-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![ลิงก์ความต้องการ](media/Resource-Management-image10.png)

3. <span data-ttu-id="962f4-139">บนหน้า **ความต้องการทรัพยากร** ที่ปรากฏในกริด **ทักษะ** เลือกจุดไข่ปลา (**...**) และจากนั้นเลือก **เพิ่มคุณสมบัติที่จำเป็นใหม่** เพื่อเพิ่มคุณลักษณะที่จำเป็นสำหรับนักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="962f4-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![เพิ่มคำสั่งคุณลักษณะที่จำเป็นใหม่](media/Resource-Management-image11.png)

4. <span data-ttu-id="962f4-141">ในกล่องโต้ตอบ **สร้างด่วน: คุณลักษณะที่จำเป็น** ที่ปรากฏในฟิล์ด **คุณลักษณะ** เลื่อกทักษะที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="962f4-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="962f4-142">หลังจากนั้น ในฟิล์ด **ค่าการจัดอันดับ** เลือกเลือกระดับความเชี่ยวชาญสำหรับทักษะนั้น</span><span class="sxs-lookup"><span data-stu-id="962f4-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="962f4-143">สุดท้ายนี้ในฟิล์ด **ความต้องการทรัพยากร** ให้กำหนดความต้องการให้กับแหล่งข้อมูลจากหน่วยองค์กรหรือแม้กระทั่งทรัพยากรที่ระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="962f4-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="962f4-144">เมื่อคุณทำเสร็จแล้ว ให้เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="962f4-144">When you've finished, select **Save**.</span></span>

    ![สร้างด่วน: กล่องโต้ตอบของคุณลักษณะที่จำเป็น](media/Resource-Management-image12.png)

5. <span data-ttu-id="962f4-146">ในหน้า **ความต้องการทรัพยากร** เลือก **จอง** เพื่อตอบสนองความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![ปุ่มจองบนหน้าทรัพยากรที่จำเป็น](media/Resource-Management-image13.png)

    <span data-ttu-id="962f4-148">คุณยังสามารถเลือกทรัพยากรทั่วไปในกริด **All Team Members** และจากนั้นเลือก **จอง**</span><span class="sxs-lookup"><span data-stu-id="962f4-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![ปุ่มจองที่อยู่บนกริดสมาชิกทีมทั้งหมด](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="962f4-150">ในตัวอย่างนี้ มี 40 ชั่วโมงที่ต้องการแต่ไม่มีชั่วโมงที่จองจริงเนื่องจากทรัพยากรทั่วไปไม่มีการจอง</span><span class="sxs-lookup"><span data-stu-id="962f4-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="962f4-151">นอกจากนั้น ไม่มีชั่วโมงที่มอบหมายเนื่องจากทรัพยากรทั่วไปถูกเพิ่มไปยังทีมโดยตรง</span><span class="sxs-lookup"><span data-stu-id="962f4-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="962f4-152">ยังไม่ถูกเพิ่มโดยการใช้การมอบหมายงาน</span><span class="sxs-lookup"><span data-stu-id="962f4-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="962f4-153">ในหน้า **ตัวช่วยจัดหมายกำหนดการให้บริการ** คุณสามารถกรองทรัพยากรที่มีอยู่ตามความต้องการที่ระบุไว้ในความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="962f4-154">ทรัพยากรถูกเรียงลำดับตามพารามิเตอร์การเรียงลำดับที่ระบุไว้ในตารางหมายกำหนดการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="962f4-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![หน้าตัวช่วยจัดหมายกำหนดการให้บริการ](media/Resource-Management-image15.png)

    <span data-ttu-id="962f4-156">นี่คือตัวกรองบางตัวที่ใช้บ่อย:</span><span class="sxs-lookup"><span data-stu-id="962f4-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="962f4-157">**คุณลักษณะพร้อมกับการจัดอันดับ** กรองโดยทักษะ ประกาศนียบัตร และคุณภาพทรัพยากรอื่นๆพร้อมกับการจัดอันดับความเชี่ยวชาญ</span><span class="sxs-lookup"><span data-stu-id="962f4-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="962f4-158">**บทบาท** กรองตามบทบาทเริ่มต้นที่ถูกกำหนดให้กับทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="962f4-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="962f4-159">**หน่วยองค์กร** กรองทรัพยากรที่สามารถจองได้โดยหน่วยองค์กรที่ได้รับมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="962f4-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="962f4-160">หากคุณไม่พอใจกับผลลัพธ์ของการค้นหาความต้องการเริ่มต้น คุณสามารถเปลี่ยนเกณฑ์ตัวกรองได้</span><span class="sxs-lookup"><span data-stu-id="962f4-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="962f4-161">ขยายบานหน้าต่าง **มุมมองตัวกรอง** ที่อยู่ทางด้านซ้ายและจากนั้นเลือก **ค้นหา** เพื่อหาทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="962f4-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![หน้าต่างมุมมองตัวกรอง](media/Resource-Management-image16.png)

7. <span data-ttu-id="962f4-163">เพื่อเปลี่ยนวิธีที่ผลลัพธ์ถูกเรียงลำดับ เลือก **เรียงลำดับ**</span><span class="sxs-lookup"><span data-stu-id="962f4-163">To change how the results are sorted, select **Sort**.</span></span>

    ![คำสั่งให้เรียงลำดับ](media/Resource-Management-image17.png)

8. <span data-ttu-id="962f4-165">เลือกทรัพยากรตามความต้องการที่ระบุไว้ในความต้องการตามที่ระบุไว้ที่ด้านบนของกริด</span><span class="sxs-lookup"><span data-stu-id="962f4-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="962f4-166">คุณสามารถล้างการเลือกของเซลล์ในกริดและปล่อยให้ทรัพยากรเปิดกำลังการผลิต</span><span class="sxs-lookup"><span data-stu-id="962f4-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="962f4-167">สามารถเลือกได้เพียงหนึ่งทรัพยากรเท่านั้นในแต่ละครั้งที่จองไว้</span><span class="sxs-lookup"><span data-stu-id="962f4-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="962f4-168">เลือก **สมุด** เพื่อจองทรัพยากรที่เลือกและปล่อยให้ตารางหมายกำหนดการให้บริการเปิดไว้เพื่อให้คุณสามารถเลือกทรัพยากรเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="962f4-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="962f4-169">หรือเลือก **จอง & ออก** เพื่อจองทรัพยากรที่เลือกและปิดตารางหมายกำหนดการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="962f4-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![ทรัพยากรสำหรับจอง](media/Resource-Management-image19.png)

    <span data-ttu-id="962f4-171">คุณจะได้รับการแจ้งเตือนเกี่ยวกับชั่วโมงที่จองไว้</span><span class="sxs-lookup"><span data-stu-id="962f4-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="962f4-172">ตัวชี้วัดความต้องการแสดงจำนวนความต้องการในการจองที่มีความพึงพอใจและจำนวนที่ยังคงอยู่</span><span class="sxs-lookup"><span data-stu-id="962f4-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="962f4-173">นอกจากนี้คุณยังสามารถดูว่ากำลังการผลิตของทรัพยากรที่เลือกมีการใช้มากน้อยเพียงใด</span><span class="sxs-lookup"><span data-stu-id="962f4-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="962f4-174">เลือก **ขยาย** เพื่อดูรายละเอียดเพิ่มเติมเกี่ยวกับการจองทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="962f4-175">กลับไปที่มุมมอง **สมาชิกในทีมทั้งหมด** </span><span class="sxs-lookup"><span data-stu-id="962f4-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="962f4-176">ในกริดให้สังเกตว่าทรัพยากรทั่วไปถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อและมี 40 ชั่วโมงที่ถูกแสดงว่าจองสำหรับทรัพยากรนั้น</span><span class="sxs-lookup"><span data-stu-id="962f4-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![อัปเดตกริดสมาชิกทีมทั้งหมดแล้ว](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="962f4-178">ไม่มีชั่วโมงที่กำหนดไว้แสดงขึ้นเนื่องจากมีการจองโดยตรงกับทีม</span><span class="sxs-lookup"><span data-stu-id="962f4-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="962f4-179">พวกเขาไม่ได้จองโดยใช้การมอบหมายงาน</span><span class="sxs-lookup"><span data-stu-id="962f4-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="962f4-180">มอบหมายทรัพยากรทั่วไปให้กับงานและสร้างความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="962f4-181">ใน PSA คุณสามารถสร้างงานและจากนั้นมอบหมายทรัพยากรทั่วไปให้กับพวกเขา</span><span class="sxs-lookup"><span data-stu-id="962f4-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="962f4-182">ด้วยวิธีนี้ ความต้องการทรัพยากรสามารถแสดงด้วยตัวยึดตำแหน่งในขณะที่คุณประเมินหมายกำหนดการให้บริการและหมายเลขทางการเงินของคุณ</span><span class="sxs-lookup"><span data-stu-id="962f4-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="962f4-183">จากนั้นคุณสามารถสร้างความต้องการทรัพยากรสำหรับทรัพยากรทั่วไปและเติมความต้องการเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="962f4-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="962f4-184">บนหน้า **โครงการ** บนแท็บ **หมายกำหนดการให้บริการ** ให้เลือก **เพิ่ม** เพื่อสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="962f4-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![สร้างงานใหม่](media/Resource-Management-image21.png)

2. <span data-ttu-id="962f4-186">ในฟิลด์ **ทรัพยากร** ให้เลือกสัญลักษณ์ **ตัวเลือกทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="962f4-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="962f4-187">ตัวเลือกทรัพยากรปรากฏขึ้นและแสดงสมาชิกในทีมที่มีอยู่สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="962f4-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![ตัวเลือกทรัพยากร](media/Resource-Management-image22.png)

3. <span data-ttu-id="962f4-189">ป้อนชื่อของทรัพยากรทั่วไปใหม่แล้วเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="962f4-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![ชื่อของทรัพยากรทั่วไปใหม่ได้ป้อนแล้ว](media/Resource-Management-image23.png)

4. <span data-ttu-id="962f4-191">ในกล่องโต้ตอบ **สร้างด่วน: สมาชิกทีมโครงการ** ที่ปรากฏขึ้นในฟิล์ด **บทบาท** ให้เลือกบทบาทสำหรับทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="962f4-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="962f4-192">ในฟิลด์ **หน่วยทรัพยากร** ให้เลือกหน่วยองค์กรสำหรับทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="962f4-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="962f4-193">จากนั้นเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="962f4-193">Then select **Save**.</span></span>

    ![สร้างด่วน: กล่องโต้ตอบสมาชิกทีมโครงการ](media/Resource-Management-image24.png)

    <span data-ttu-id="962f4-195">ขณะนี้สมาชิกทีมทั่วไปได้รับการมอบหมายให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="962f4-195">The generic team member is now assigned to the task.</span></span>

    ![สมาชิกทีมทั่วไปได้รับการมอบหมายให้กับงาน](media/Resource-Management-image25.png)

    <span data-ttu-id="962f4-197">บนแท็บ **ทีม** คุณจะเห็นสมาชิกในทีมทั่วไปใหม่</span><span class="sxs-lookup"><span data-stu-id="962f4-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="962f4-198">ขอให้สังเกตว่ามีเพียงชั่วโมงที่ได้รับมอบหมายเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="962f4-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="962f4-199">ชั่วโมงเหล่านี้คือผลรวมของงานทั้งหมดที่ได้มอบหมายให้กับสมาชิกในทีมทั่วไป</span><span class="sxs-lookup"><span data-stu-id="962f4-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="962f4-200">สมาชิกในทีมทั่วไปยังไม่มีชั่วโมงที่ต้องการหรือความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![สมาชิกในทีมทั่วไปบนแท็บทีม](media/Resource-Management-image26.png)

5. <span data-ttu-id="962f4-202">ขณะนี้คุณสามารถมอบหมายสมาชิกในทีมทั่วไปให้กับงานอื่นๆโดยใช้ตัวเลือกทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![สมาชิกในทีมทั่วไปในตัวใช้เลือกทรัพยากร](media/Resource-Management-image27.png)

    <span data-ttu-id="962f4-204">เมื่อคุณมอบหมายทรัพยากรทั่วไปให้กับงานเสร็จสิ้นแล้วคุณสามารถสร้างความต้องการทรัพยากรสำหรับทรัพยากรทั่วไปได้</span><span class="sxs-lookup"><span data-stu-id="962f4-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="962f4-205">บนแท็บ **ทีม** ให้เลือกทรัพยากรทั่วไปและจากนั้นให้เลือก **สร้างความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="962f4-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![คำสั่งสร้างความต้องการ](media/Resource-Management-image28.png)

    <span data-ttu-id="962f4-207">เมื่อความต้องการถูกสร้างขึ้น สมาชิกในทีมทั่วไปจะมีชั่วโมงที่ต้องการและลิงก์สำหรับความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![ลิงก์สำหรับความต้องการทรัพยากร](media/Resource-Management-image29.png)

    <span data-ttu-id="962f4-209">หลังจากที่คุณจองทรัพยากรที่ระบุชื่อเสร็จสมบูรณ์ ทรัพยากรทั่วไปจะถูกลบออกจากทีมและถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="962f4-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![ทรัพยากรทั่วไปถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อ](media/Resource-Management-image30.png)

    <span data-ttu-id="962f4-211">บนแท็บ **หมายกำหนดการให้บริการ** การมอบหมายงานของทรัพยากรทั่วไปจะถูกเอาออกและแทนที่ด้วยทรัพยากรที่ระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="962f4-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![การมอบหมายทรัพยากรทั่วไปจะถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อบนแท็บหมายกำหนดการให้บริการ ](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="962f4-213">ลักษณะการทำงานนี้เกิดขึ้นเฉพาะเมื่อทรัพยากรที่ระบุชื่อมีการจองจนเต็มสำหรับความต้องการทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="962f4-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="962f4-214">เมื่อทรัพยากรที่ระบุชื่อบางส่วนแทนที่ความต้องการทรัพยากรทั่วไปหรือทรัพยากรที่ระบุชื่อจำนวนมากแทนที่ความต้องการทรัพยากรทั่วไปอย่างใดอย่างหนึ่ง ทรัพยากรทั่วไปยังคงได้รับมอบหมายให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="962f4-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="962f4-215">ในภาพประกอบต่อไปนี้ แผนงาน 80 ชั่วโมงได้รับการวางแผนสำหรับระยะเวลาห้าวัน (16 ชั่วโมงต่อวันมากกว่าห้าวัน) และได้มอบหมายให้กับทรัพยากรทั่วไปที่มีชื่อว่า **ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="962f4-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![80-ชั่วโมง, งาน 5 วันที่ได้มอบหมายให้กับทรัพยากรทั่วไปที่ทำงานได้](media/Resource-Management-image32.png)

    <span data-ttu-id="962f4-217">เมื่อคุณสร้างความต้องการ ใช้เวลา 80 ชั่วโมงมากกว่า 5 วัน</span><span class="sxs-lookup"><span data-stu-id="962f4-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![ความต้องการที่สร้างขึ้นสำหรับ 80 ชั่วโมงมากกว่า 5 วัน](media/Resource-Management-image33.png)

    <span data-ttu-id="962f4-219">เนื่องจากทรัพยากรที่มีอยู่ทำงานได้เพียง 8 ชั่วโมงต่อวัน ต้องใช้ทรัพยากรสองตัวเพื่อตอบสนองความต้องการได้</span><span class="sxs-lookup"><span data-stu-id="962f4-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![ทรัพยากรที่สอง](media/Resource-Management-image35.png)

    <span data-ttu-id="962f4-221">บนแท็บ **ทีม** ขณะนี้คุณสามารถดูว่าทรัพยากรทั่วไปไม่มีชั่วโมงที่ต้องการ แต่ชั่วโมงที่มอบหมายยังคงปรากฏพร้อมกับทรัพยากรที่ระบุชื่อทั้งสองที่ประกอบกันเป็นการบรรลุเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="962f4-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![ทรัพยากรที่ระบุชื่อทั้งสองบนแท็บทีม](media/Resource-Management-image36.png)

    <span data-ttu-id="962f4-223">บนแท็บ **หมายกำหนดการให้บริการ** ทรัพยากรทั่วไปยังคงได้รับมอบหมายให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="962f4-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![ทรัพยากรทั่วไปบนแท็บหมายกำหนดการให้บริการ](media/Resource-Management-image37.png)

<span data-ttu-id="962f4-225">PSA ไม่ได้มอบหมายทรัพยากรทั้งสองให้กับงาน เนื่องจากลักษณะการทำงานนั้นจะสร้างหมายกำหนดการให้บริการที่คาดการณ์ได้น้อยลง</span><span class="sxs-lookup"><span data-stu-id="962f4-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="962f4-226">ในตัวอย่างง่ายๆนี้ เป็นเรื่องง่ายที่จะแบ่งชั่วโมงเท่าๆกันระหว่างสองทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="962f4-227">อย่างไรก็ตาม ในสถานการณ์ที่ซับซ้อนมากขึ้นที่เกี่ยวข้องกับงานหลายและทรัพยากรต่างๆ PSA จะต้องทำสมมติฐานเกี่ยวกับวิธีการจัดสรรการจองที่ได้รับสำหรับหลายๆทรัพยากรในหลายๆงาน</span><span class="sxs-lookup"><span data-stu-id="962f4-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="962f4-228">ดังนั้นในสถานการณ์เหล่านี้ ผู้จัดการโครงการจะต้องรับผิดชอบในการแยกวิเคราะห์การจองหลายครั้งและมอบหมายให้พวกเขาตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="962f4-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="962f4-229">ในการจัดสรรการจอง ผู้จัดการโครงการจะมอบหมายงานจากทรัพยากรทั่วไปไปยังทรัพยากรที่ระบุชื่อแล้วจากนั้นใช้มุมมอง **การกระทบยอด** เพื่อให้แน่ใจว่าการจัดสรรทำงานร่วมกับการจองได้</span><span class="sxs-lookup"><span data-stu-id="962f4-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="962f4-230">แก้ไขความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-230">Edit a resource requirement</span></span>

<span data-ttu-id="962f4-231">หลังจากที่ความต้องการทรัพยากรถูกสร้างขึ้น ผู้จัดการโครงการหรือผู้จัดการทรัพยากรอาจต้องการแก้ไขรายละเอียดเพื่อปรับปรุงเงื่อนไขการค้นหาเมื่อมีการใช้ตารางหมายกำหนดการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="962f4-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="962f4-232">หากต้องการแก้ไขความต้องการทรัพยากร ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="962f4-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="962f4-233">บนหน้า **โครงการ** บนแท็บ **Team** ให้เลือกลิงก์ไปยังความต้องการใดๆในทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="962f4-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="962f4-234">บนหน้า **ความต้องการทรัพยากร** ที่ปรากฏขึ้น คุณสามารถอัพเดตหลายแอตทริบิวต์ได้</span><span class="sxs-lookup"><span data-stu-id="962f4-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="962f4-235">นี่คือตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="962f4-235">Here are some examples:</span></span>

    - <span data-ttu-id="962f4-236">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="962f4-236">Name</span></span>
    - <span data-ttu-id="962f4-237">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="962f4-237">From Date</span></span>
    - <span data-ttu-id="962f4-238">จนถึงปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="962f4-238">To Date</span></span>
    - <span data-ttu-id="962f4-239">ระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="962f4-239">Duration</span></span>
    - <span data-ttu-id="962f4-240">ขริดของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-240">Resource Type</span></span>

<span data-ttu-id="962f4-241">บนเพจ **ความต้องการทรัพยากร** ผู้จัดการโครงการหรือผู้จัดการทรัพยากรยังสามารถกำหนดข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="962f4-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="962f4-242">ทักษะ</span><span class="sxs-lookup"><span data-stu-id="962f4-242">Skills</span></span>
- <span data-ttu-id="962f4-243">บทบาท</span><span class="sxs-lookup"><span data-stu-id="962f4-243">Roles</span></span>
- <span data-ttu-id="962f4-244">การกำหนดลักษณะทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-244">Resource preferences</span></span>
- <span data-ttu-id="962f4-245">หน่วยองค์กรที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="962f4-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="962f4-246">อัพเดตการจองทรัพยากรหลังจากที่จองไว้ในโครงการ</span><span class="sxs-lookup"><span data-stu-id="962f4-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="962f4-247">หลังจากที่คุณได้เพิ่มทรัพยากรทั่วไปหรือทรัพยากรที่ระบุชื่อไปยังทีมโครงการแล้ว คุณสามารถเปลี่ยนแปลงการจองของทรัพยากรได้</span><span class="sxs-lookup"><span data-stu-id="962f4-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="962f4-248">บนหน้า **โครงการ** บนแท็บ **ทีม** ให้เลือกสมาชิกทีม แล้วเลือก **ปรับปรุงการจอง**</span><span class="sxs-lookup"><span data-stu-id="962f4-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![ตารางหมายกำหนดการให้บริการที่เปิดสำหรับสมาชิกทีมที่เลือก](media/Resource-Management-image40.png)

    <span data-ttu-id="962f4-250">ตารางหมายกำหนดการให้บริการจะปรากฏขึ้นและแสดงการจองของสมาชิกทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="962f4-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="962f4-251">ขยายเรกคอร์ดของสมาชิกทีมเพื่อดูชั่วโมงที่มีการจองกับโครงการนี้และโครงการอื่นๆที่ใช้กำลังการผลิตของสมาชิกในทีม</span><span class="sxs-lookup"><span data-stu-id="962f4-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="962f4-252">เลือกและลากการจองเพื่อขยายหรือตัดทอน</span><span class="sxs-lookup"><span data-stu-id="962f4-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="962f4-253">กล่องโต้ตอบ **สร้างการจองทรัพยากร** ปรากฏขึ้นซึ่งช่วยให้คุณสามารถปรับการจองได้</span><span class="sxs-lookup"><span data-stu-id="962f4-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![สร้างกล่องโต้ตอบการจองทรัพยากร](media/Resource-Management-image41.png)

3. <span data-ttu-id="962f4-255">คลิกขวาที่การจอง</span><span class="sxs-lookup"><span data-stu-id="962f4-255">Right-click the booking.</span></span> <span data-ttu-id="962f4-256">จากนั้นคุณสามารถใช้เมนูทางลัดเพื่อทำการดำเนินการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="962f4-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="962f4-257">เปลี่ยนแปลงสถานะการจอง</span><span class="sxs-lookup"><span data-stu-id="962f4-257">Change the booking status.</span></span>
    - <span data-ttu-id="962f4-258">แก้ไขการจอง</span><span class="sxs-lookup"><span data-stu-id="962f4-258">Edit the booking.</span></span>
    - <span data-ttu-id="962f4-259">ทดแทนทรัพยากรในทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="962f4-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="962f4-260">เปลี่ยนแปลงสถานะการจอง</span><span class="sxs-lookup"><span data-stu-id="962f4-260">Change the booking status</span></span>

<span data-ttu-id="962f4-261">คุณสามารถเปลี่ยนสถานะการจองเริ่มต้นหรือที่กำหนดเองได้</span><span class="sxs-lookup"><span data-stu-id="962f4-261">You can change any default or custom booking status.</span></span>

![เปลี่ยนคำสั่งสถานะ](media/Resource-Management-image42.png)

<span data-ttu-id="962f4-263">สถานะต่อไปนี้จะอยู่ใน PSA:</span><span class="sxs-lookup"><span data-stu-id="962f4-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="962f4-264">**ยกเลิก** – สถานะนี้ได้ยกเลิกการจองทรัพยากรและเพิ่มกำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="962f4-265">**จองแบบตายตัว** – สถานะนี้จะใช้กำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="962f4-266">การจองโดยทั่วไปจะมีสถานะนี้เมื่อคุณเปิด **ปรับปรุงการจอง** จากกริด **สมาชิกทีมทั้งหมด** ในหน้า **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="962f4-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="962f4-267">**จองแบบไม่ตายตัว** – สถานะนี้จะเพิ่มทรัพยากรให้กับทีมแต่ไม่ได้ใช้กำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="962f4-268">บ่งชี้ว่าทรัพยากรมีการจองสำหรับงานที่มีศักยภาพแต่ยังคงมีกำลังการผลิตถ้าจำเป็นสำหรับงานอื่น</span><span class="sxs-lookup"><span data-stu-id="962f4-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="962f4-269">ในมุมมองของความพร้อมใช้งานของทรัพยากรโดยรวม การจองแบบไม่ตายตัวจะมีสถานะแตกต่างจากการจองแบบตายตัว</span><span class="sxs-lookup"><span data-stu-id="962f4-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="962f4-270">**เสนอ** – สถานะนี้แสดงถึงข้อเสนอของผู้จัดการทรัพยากรหรือผู้จัดการโครงการสำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="962f4-271">ข้อเสนอไม่ได้ใช้กำลังการผลิตของทรัพยากรและทรัพยากรไม่ได้ถูกเพิ่มลงในทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="962f4-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="962f4-272">เมื่อต้องการจองทรัพยากรแบบตายตัวบนทีม ผู้จัดการโครงการต้องยอมรับการประชุมข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="962f4-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="962f4-273">ส่งคำขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-273">Submit resource requests</span></span>

<span data-ttu-id="962f4-274">การร้องขอทรัพยากรจะใช้เพื่อดำเนินการตามความต้องการ (ความต้องการทรัพยากร) ที่ต้องปฏิบัติตามผู้จัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="962f4-275">สำหรับทรัพยากรทั่วไปที่มีอยู่แล้วในทีม คุณสามารถส่งคำขอทรัพยากรได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="962f4-275">For a generic resource thta is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="962f4-276">คำขอทรัพยากรสามารถเติมเต็มได้ในสองวิธี:</span><span class="sxs-lookup"><span data-stu-id="962f4-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="962f4-277">ผู้จัดการทรัพยากรตอบสนองการร้องขอโดยตรง</span><span class="sxs-lookup"><span data-stu-id="962f4-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="962f4-278">ในกรณีนี้ ทรัพยากรทั่วไปจะถูกแทนที่ด้วยการจองแบบตายตัวที่มีทรัพยากรที่ระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="962f4-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="962f4-279">ผู้จัดการทรัพยากรเสนอทรัพยากรให้กับผู้จัดการโครงการและผู้จัดการโครงการอนุมัติหรือปฏิเสธทรัพยากรที่นำเสนอ</span><span class="sxs-lookup"><span data-stu-id="962f4-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="962f4-280">ปฏิบัติตามคำขอทรัพยากรโดยตรง</span><span class="sxs-lookup"><span data-stu-id="962f4-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="962f4-281">เมื่อความต้องการทรัพยากรถูกสร้างขึ้น ผู้จัดการโครงการสามารถส่งการร้องขอทรัพยากรสำหรับทรัพยากรทั่วไปโดยการเลือกทรัพยากรและจากนั้นเลือก **ส่งคำขอ**</span><span class="sxs-lookup"><span data-stu-id="962f4-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![ปุ่มส่งคำขอ](media/Resource-Management-image45.png)

<span data-ttu-id="962f4-283">ข้อคิดเห็นเกี่ยวกับทรัพยากรสามารถให้กับผู้จัดการทรัพยากรที่จะตอบสนองการร้องขอ</span><span class="sxs-lookup"><span data-stu-id="962f4-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="962f4-284">หลังจากคำขอถูกส่งแล้ว ฟิลด์ **สถานะ** สำหรับสมาชิกในทีมจะถูกเปลี่ยนเป็น **ส่งแล้ว**</span><span class="sxs-lookup"><span data-stu-id="962f4-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![กำลังป้อนข้อคิดเห็นเพิ่มเติม](media/Resource-Management-image46.png)

<span data-ttu-id="962f4-286">เมื่อผู้จัดการทรัพยากรตอบสนองการร้องขอ สมาชิกในทีมทั่วไปจะถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อในกริด **สมาชิกทีมทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="962f4-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![สมาชิกในทีมทั่วไปจะถูกแทนที่โดยทรัพยากรที่ระบุชื่อในกริดสมาชิกทีมทั้งหมด](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="962f4-288">ใช้การประชุมข้อเสนอทางทรัพยากรสำหรับคำขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="962f4-289">แทนที่จะจองทรัพยากรโดยตรงในการร้องขอทรัพยากร ผู้จัดการทรัพยากรสามารถนำเสนอทรัพยากรไปยังผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="962f4-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="962f4-290">ผู้จัดการทรัพยากรอาจใช้ตัวเลือกนี้เมื่อการจับคู่ที่แน่นอนสำหรับความต้องการไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="962f4-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="962f4-291">เมื่อผู้จัดการทรัพยากรเสนอทรัพยากร ผู้จัดการโครงการเห็นว่าฟิล์ด **สถานะ** สำหรับสมาชิกในทีมทั่วไปมีการเปลี่ยนแปลงไป **เพื่อความต้องการการตรวจทาน**</span><span class="sxs-lookup"><span data-stu-id="962f4-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![สถานะของสมาชิกทีมทั่วไปเปลี่ยนเป็นความต้องการการตรวจทาน](media/Resource-Management-image48.png)

<span data-ttu-id="962f4-293">เมื่อต้องการดูทรัพยากรที่นำเสนอพร้อมกับการแสดงภาพของผลจากการจองของการประชุมข้อเสนอ ให้คลิกสองครั้งที่สมาชิกในทีมที่มีสถานะของ **ความต้องการตรวจทาน**</span><span class="sxs-lookup"><span data-stu-id="962f4-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="962f4-294">จากนั้นเลือกแท็บ **ทรัพยากรที่นำเสนอ** </span><span class="sxs-lookup"><span data-stu-id="962f4-294">Then select the **Proposed Resources** tab.</span></span>

![แท็บทรัพยากรที่นำเสนอ](media/Resource-Management-image49.png)

<span data-ttu-id="962f4-296">เลือก **ยอมรับการประชุมข้อเสนอทั้งหมด** เพื่อยอมรับทรัพยากรที่นำเสนอทั้งหมด หรือ **ปฏิเสธการประชุมข้อเสนอทั้งหมด** เพื่อที่จะปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="962f4-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="962f4-297">ถ้าคุณยอมรับทรัพยากรที่นำเสนอ พวกเขาจะถูกจองแบบตายตัวในโครงการเป็นสมาชิกในทีมและแทนที่ทรัพยากรทั่วไป</span><span class="sxs-lookup"><span data-stu-id="962f4-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="962f4-298">คุณต้องยอมรับหรือปฏิเสธทรัพยากรที่นำเสนอทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="962f4-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="962f4-299">คุณไม่สามารถยอมรับหรือปฏิเสธบางส่วนได้</span><span class="sxs-lookup"><span data-stu-id="962f4-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="962f4-300">ทดแทนทรัพยากรในทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="962f4-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="962f4-301">บางครั้งผู้จัดการโครงการต้องแทนที่สมาชิกในทีมที่จองไว้ในโครงการ</span><span class="sxs-lookup"><span data-stu-id="962f4-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="962f4-302">บนหน้า **โครงการ** บนแท็บ **ทีม** ให้เลือกทรัพยากรที่ต้องการแทนที่ แล้วให้เลือก **ปรับปรุงการจอง**</span><span class="sxs-lookup"><span data-stu-id="962f4-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="962f4-303">ขยายทรัพยากรเพื่อดูโครงการที่มอบหมายให้</span><span class="sxs-lookup"><span data-stu-id="962f4-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![การขยายทรัพยากรเพื่อแสดงโครงการที่มอบหมาย](media/Resource-Management-image50.png)

3. <span data-ttu-id="962f4-305">คลิกขวาที่โครงการและจากนั้นเลือก **ทดแทนทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="962f4-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="962f4-306">ถ้าคุณทราบทรัพยากรที่คุณต้องการจะทดแทนสำหรับทรัพยากรปัจจุบัน เลือกหรือพิมพ์ชื่อแล้วเลือก **มอบหมายใหม่**</span><span class="sxs-lookup"><span data-stu-id="962f4-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![การระบุทรัพยากรทดแทน](media/Resource-Management-image51.png)

    <span data-ttu-id="962f4-308">หรือให้ทำตามขั้นตอนเหล่านี้เพื่อค้นหาทรัพยากร:</span><span class="sxs-lookup"><span data-stu-id="962f4-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="962f4-309">เลือก **ค้นหาการแทนที่**</span><span class="sxs-lookup"><span data-stu-id="962f4-309">Select **Find Substitution**.</span></span>

        ![การค้นหาสำหรับทรัพยากรทดแทน](media/Resource-Management-image52.png)

        <span data-ttu-id="962f4-311">ตัวช่วยจัดหมายกำหนดการให้บริการส่งกลับรายการของการทดแทนที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="962f4-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="962f4-312">ในตัวช่วยจัดหมายกำหนดการให้บริการ คุณสามารถกรองทรัพยากรที่พร้อมใช้งานเพิ่มเติมเพื่อค้นหาสิ่งทดแทนที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="962f4-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![รายการของทดแทนที่พร้อมใช้งาน](media/Resource-Management-image53.png)

    2. <span data-ttu-id="962f4-314">เพื่อทดแทนทรัพยากร เลือกที่คุณต้องการและจากนั้นให้เลือก **ทดแทน**</span><span class="sxs-lookup"><span data-stu-id="962f4-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![ทดแทดทรัพยากรที่เลือก](media/Resource-Management-image54.png)

    <span data-ttu-id="962f4-316">การจองและการมอบหมายจะถูกแทนที่ด้วยทรัพยากรใหม่</span><span class="sxs-lookup"><span data-stu-id="962f4-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![การจองและการมอบหมายถูกแทนที่ด้วยทรัพยากรใหม่](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="962f4-318">กระทบยอดการจองและงานมอบหมายสมาชิกทีม</span><span class="sxs-lookup"><span data-stu-id="962f4-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="962f4-319">สำหรับสมาชิกในทีมการจองและการมอบหมายถูกจับเป็นคู่กันอย่างหลวมๆ</span><span class="sxs-lookup"><span data-stu-id="962f4-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="962f4-320">กล่าวอีกนัยหนึ่ง ทรัพยากรสามารถมีการมอบหมายได้แต่ไม่มีการจอง หรือทรัพยากรสามารถมีการจองได้แต่ไม่มีการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="962f4-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="962f4-321">ตามหลักการแล้ว การจองและการมอบหมายควรจะถูกจัดตำแหน่งเพื่อให้ทรัพยากรมีความมุ่งมั่นในกำลังการผลิตเพื่อที่จะปฏิบัติงานที่ได้รับมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="962f4-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="962f4-322">อย่างไรก็ตามการจองอาจจะขึ้นอยู่กับความพร้อมใช้งานและการกำหนดเวลาที่อาจจะเปลี่ยนแปลงในขณะที่โครงการยังคงดำเนินต่อไป</span><span class="sxs-lookup"><span data-stu-id="962f4-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="962f4-323">ดังนั้นการจับเป็นคู่กันอย่างหลวมๆของการจองและงานมอบหมายทำให้มีความยืดหยุ่น</span><span class="sxs-lookup"><span data-stu-id="962f4-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="962f4-324">PSA มีแท็บ **การกระทบยอด** ที่ให้ผู้จัดการโครงการกระทบยอดการจองของสมาชิกในทีมและงานมอบหมายสำหรับทีมโครงการ</span><span class="sxs-lookup"><span data-stu-id="962f4-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![แท็บการกระทบยอด](media/Resource-Management-image56.png)

<span data-ttu-id="962f4-326">แท็บ **การกระทบยอด** แสดงการจองและการมอบหมายไปจนถึงระดับของการมอบหมายงานสำหรับสมาชิกในทีมแต่ละคน</span><span class="sxs-lookup"><span data-stu-id="962f4-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="962f4-327">จะแสดงชั่วโมงในเซลล์ที่แสดงช่วงเวลาตั้งแต่เดือนไปจนถึงวัน</span><span class="sxs-lookup"><span data-stu-id="962f4-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="962f4-328">แท็บยังแสดงภาพรวมผลรวมสุทธิสำหรับโครงการพร้อมกับคอลัมน์ผลรวม</span><span class="sxs-lookup"><span data-stu-id="962f4-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="962f4-329">สำหรับทุกทรัพยากร แท็บจะคำนวณความแตกต่างระหว่างการจองของสมาชิกในทีมและค่าสะสมของการกำหนดงานที่มอบหมายของสมาชิกในทีม</span><span class="sxs-lookup"><span data-stu-id="962f4-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="962f4-330">ตามหลักการแล้ว ความแตกต่างนี้ควรเป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="962f4-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="962f4-331">กล่าวอีกนัยหนึ่งคือไม่ควรจะมีความแตกต่างระหว่างการจองและงานมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="962f4-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="962f4-332">ความแตกต่างของสีและแรเงาเพื่อดึงดูดให้ความสนใจกับสองเงื่อนไข:</span><span class="sxs-lookup"><span data-stu-id="962f4-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="962f4-333">**ความขาดแคลนการจอง** – ความขาดแคลนการจองเกิดขึ้นเมื่อทรัพยากรมีการมอบหมายมากกว่าการจอง</span><span class="sxs-lookup"><span data-stu-id="962f4-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="962f4-334">เนื่องจากกำลังการผลิตนี้ไม่ได้รับการสงวนสิทธิ์ ผู้จัดการโครงการอาจต้องการแก้ไขเงื่อนไขนี้โดยการขยายการจองของทรัพยากรเพื่อครอบคลุมการขาดดุล</span><span class="sxs-lookup"><span data-stu-id="962f4-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="962f4-335">**การจองเกินจำนวน** การจองเกินจำนวนจะเกิดขึ้นเมื่อมีการจองทรัพยากรไปยังโครงการ แต่ยังไม่ได้กำหนดให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="962f4-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="962f4-336">เงื่อนไขนี้อาจเป็นที่ยอมรับในกรณีที่ทรัพยากรถูกจองไปยังโครงการก่อนที่จะมีการมอบหมายงาน</span><span class="sxs-lookup"><span data-stu-id="962f4-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="962f4-337">อย่างไรก็ตามในกรณีอื่นๆ ทรัพยากรไม่ได้วางแผนเพื่อจะมอบหมายให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="962f4-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="962f4-338">ในกรณีเหล่านี้ ผู้จัดการโครงการควรพิจารณายกเลิกการจองของทรัพยากร เพื่อให้สามารถใช้กำลังการผลิตสำหรับโครงการอื่น</span><span class="sxs-lookup"><span data-stu-id="962f4-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="962f4-339">ในบางกรณีเมื่อคุณดูเวลาในระดับที่สูงกว่าระดับวัน (ตัวอย่างเช่นระดับเดือน) คุณอาจเห็นความแตกต่างสุทธิของศูนย์สำหรับทรัพยากร (กล่าวอีกนัยหนึ่ง การจอง = การมอบหมาย)</span><span class="sxs-lookup"><span data-stu-id="962f4-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="962f4-340">อย่างไรก็ตามถ้าคุณดูเวลาในระดับสัปดาห์ คุณอาจเห็นว่ามีการมอบหมายของชั่วโมงเป็นศูนย์และการจองของ 40 ชั่วโมงในสัปดาห์แรกแต่การมอบหมายงานของ 40 ชั่วโมงและการจองเป็นศูนย์ชั่วโมงในสัปดาห์ที่สอง</span><span class="sxs-lookup"><span data-stu-id="962f4-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="962f4-341">โดยรวมแล้วการจองและการมอบหมายงานจะกระทบยอดแต่จะแตกต่างจากหนึ่งสัปดาห์ต่อไป</span><span class="sxs-lookup"><span data-stu-id="962f4-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="962f4-342">เมื่อคุณดูเวลาในระดับที่สูงกว่า เซลล์ในแท็บ **การกระทบยอด** มีตัวบ่งชี้เพื่อแจ้งให้คุณทราบว่ามีความแตกต่างในระดับที่ต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="962f4-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="962f4-343">เมื่อคลิกสองครั้งในเซลล์ คุณสามารถขยายเพื่อดูความแตกต่างได้</span><span class="sxs-lookup"><span data-stu-id="962f4-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="962f4-344">จากนั้นคุณสามารถคลิกขวาเพื่อซูมออก โดยการเลือกทรัพยากรแล้วใช้ตัวควบคุม **ความแตกต่างถัดไป** บนแถบเครื่องมือกริด คุณสามารถไปที่ความแตกต่างถัดไประหว่างการจองและการมอบหมายงานสำหรับทรัพยากรนั้น</span><span class="sxs-lookup"><span data-stu-id="962f4-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="962f4-345">จากนั้นคุณสามารถใช้ตัวควบคุม **ความแตกต่างก่อนหน้านี้** เพื่อกลับไป</span><span class="sxs-lookup"><span data-stu-id="962f4-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="962f4-346">นอกจากนี้คุณยังสามารถปิดตัวบ่งชี้ความแตกต่างและแถบนำทางภายใต้ **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="962f4-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![ตัวบ่งชี้ความแตกต่าง](media/Resource-Management-image57.png)

<span data-ttu-id="962f4-348">ถ้าคุณมีการมอบหมายงานสำหรับทรัพยากรแต่ไม่มีการจองบนหน้า **โครงการ** บนแท็บ **การกระทบยอด** ให้เลือกการขาดแคลนการจองแล้วเลือก **ขยายการจอง**</span><span class="sxs-lookup"><span data-stu-id="962f4-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="962f4-349">กล่องโต้ตอบ **การขยายการจอง** ปรากฏขึ้นและแสดงการจองที่จำเป็นเพื่อจัดการการขาดแคลนของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="962f4-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="962f4-350">นอกจากนี้ยังแสดงการจองที่มีอยู่ของทรัพยากรในโครงการทั้งหมดหรือเอนทิตีที่จัดกำหนดการอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="962f4-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="962f4-351">ถ้าคุณเลือก **ตกลง** เพื่อสร้างการจองสำหรับทรัพยากรโดยไม่คำนึงถึงความพร้อมใช้งานของทรัพยากรนั้น คุณอาจทำให้เกิดการจองเกิน</span><span class="sxs-lookup"><span data-stu-id="962f4-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![กล่องโต้ตอบการขยายการจอง](media/Resource-Management-image58.png)

<span data-ttu-id="962f4-353">ผู้จัดการโครงการหรือผู้จัดการทรัพยากรสามารถใช้ตารางหมายกำหนดการให้บริการเพื่อจัดการกับสถานการณ์ใดๆที่ทรัพยากรถูกจองเกินกว่ากำลังการผลิต</span><span class="sxs-lookup"><span data-stu-id="962f4-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
