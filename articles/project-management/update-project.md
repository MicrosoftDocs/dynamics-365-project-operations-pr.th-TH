---
title: อัปเดตโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการปรับปรุงโครงการใน Project Operations
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897835"
---
# <a name="update-a-project"></a><span data-ttu-id="75408-103">อัปเดตโครงการ</span><span class="sxs-lookup"><span data-stu-id="75408-103">Update a project</span></span>

<span data-ttu-id="75408-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="75408-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="75408-105">ด้านล่างนี้คือข้อมูลสรุปของฟิลด์ที่สามารถปรับปรุงในโครงการได้หลังจากที่สร้างและผลกระทบใดๆ ที่เกี่ยวข้องของการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="75408-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="75408-106">ฟิลด์รายละเอียดโครงการ</span><span class="sxs-lookup"><span data-stu-id="75408-106">Project detail fields</span></span>

- <span data-ttu-id="75408-107">**ชื่อ**: ชื่อของโครงการ</span><span class="sxs-lookup"><span data-stu-id="75408-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="75408-108">**คำอธิบาย**: ภาพรวมของโครงการ</span><span class="sxs-lookup"><span data-stu-id="75408-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="75408-109">**ลูกค้า**: บริษัทที่จะมีการส่งมอบโครงการให้</span><span class="sxs-lookup"><span data-stu-id="75408-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="75408-110">**แม่แบบปฏิทิน**: ชั่วโมงการทำงานของโครงการ</span><span class="sxs-lookup"><span data-stu-id="75408-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="75408-111">เมื่อฟิลด์มีการเปลี่ยนแปลง กำหนดการทั้งหมดจะถูกคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="75408-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="75408-112">**สกุลเงิน**: สกุลเงินสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="75408-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="75408-113">ฟิลด์นี้เป็นเริ่มต้นตามสกุลเงินที่กำหนดไว้ในหน่วยที่ทำสัญญา</span><span class="sxs-lookup"><span data-stu-id="75408-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="75408-114">เมื่อมีการปรับปรุงหน่วยที่ทำสัญญา ฟิลด์นี้จะได้รับการปรับปรุงด้วย</span><span class="sxs-lookup"><span data-stu-id="75408-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="75408-115">**หน่วยที่ทำสัญญา**: หน่วยองค์กรที่แสดงถึงกลุ่มหรือฝ่ายของบริษัท ที่มีหน้าที่รับผิดชอบหลักในการขายที่ชนะ และการจัดการการส่งมอบงานและบริการให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="75408-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="75408-116">**ผู้จัดการโครงการ**: สมาชิกทีมโครงการที่มีอำนาจในการตรวจสอบและอนุมัติรายการเวลาและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="75408-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="75408-117">ฟิลด์ประมาณการ</span><span class="sxs-lookup"><span data-stu-id="75408-117">Estimate fields</span></span>

- <span data-ttu-id="75408-118">**วันที่เริ่มต้นโดยประมาณ**: วันที่โครงการจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="75408-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="75408-119">เมื่อมีการปรับปรุงฟิลด์นี้ งานใดๆ ในโครงการจะย้ายโดยเป็นไปตามสัดส่วนกับวันที่เริ่มต้นใหม่</span><span class="sxs-lookup"><span data-stu-id="75408-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="75408-120">**วันที่สิ้นสุด** : วันที่โครงการสิ้นสุดลง</span><span class="sxs-lookup"><span data-stu-id="75408-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="75408-121">**กำลังคน**: กำลังคนโดยประมาณของโครงการ</span><span class="sxs-lookup"><span data-stu-id="75408-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="75408-122">เมื่อเพิ่มงานลงในโครงการแล้ว ฟิลด์นี้จะไม่สามารถแก้ไขได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="75408-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="75408-123">**ค่าแรงงานโดยประมาณ**: ค่าแรงโดยประมาณของโครงการ</span><span class="sxs-lookup"><span data-stu-id="75408-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="75408-124">เมื่อเพิ่มค่าแรงลงในโครงการแล้ว ฟิลด์นี้จะไม่สามารถแก้ไขได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="75408-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="75408-125">**ค่าใช้จ่ายโดยประมาณ**: ค่าใช้จ่ายโดยประมาณของโครงการ</span><span class="sxs-lookup"><span data-stu-id="75408-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="75408-126">เมื่อเพิ่มค่าใช้จ่ายลงในโครงการแล้ว ฟิลด์นี้จะไม่สามารถแก้ไขได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="75408-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="75408-127">ฟิลด์ข้อมูลจริงของโครงการ</span><span class="sxs-lookup"><span data-stu-id="75408-127">Project actual fields</span></span>
- <span data-ttu-id="75408-128">**การเริ่มต้นจริง** : วันที่โครงการเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="75408-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="75408-129">**การเสร็จสิ้นจริง** : จะได้รับการปรับปรุงเมื่อโครงการเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="75408-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="75408-130">ฟิลด์สถานะโครงการ</span><span class="sxs-lookup"><span data-stu-id="75408-130">Project status fields</span></span>

- <span data-ttu-id="75408-131">**สถานะโครงการโดยรวม**: สถานภาพโครงการโดยรวมที่ระบุโดยผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="75408-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="75408-132">**ข้อคิดเห็น**: การบรรยายเกี่ยวกับสถานภาพปัจจุบันของโครงการที่ระบุโดยผู้จัดการโครงการ</span><span class="sxs-lookup"><span data-stu-id="75408-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>

