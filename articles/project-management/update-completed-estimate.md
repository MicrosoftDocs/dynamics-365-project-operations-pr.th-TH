---
title: อัปเดตการประมาณการเมื่อดำเนินงานเสร็จสมบูรณ์
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการปรับปรุงการคาดคะเนกำลังคนในโครงการ
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 16393133a5de17308caceb069d7bca670caa04c8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086115"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="92488-103">อัปเดตการประมาณการเมื่อดำเนินงานเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="92488-103">Update estimate at completion</span></span>

<span data-ttu-id="92488-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="92488-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="92488-105">เป็นปกติสำหรับผู้จัดการโครงการที่จะแก้ไขการประมาณการเดิมของงาน</span><span class="sxs-lookup"><span data-stu-id="92488-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="92488-106">การประมาณการโครงการใหม่เป็นการรับรู้ของผู้จัดการโครงการของการประมาณการ ที่กำหนดสถานะปัจจุบันของโครงการ</span><span class="sxs-lookup"><span data-stu-id="92488-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="92488-107">อย่างไรก็ตาม เราไม่แนะนำให้ผู้จัดการโครงการเปลี่ยนเลขเส้นฐาน เนื่องจากเส้นฐานของโครงการแสดงแหล่งที่มาของความจริงที่เชื่อมต่อ สำหรับหมายกำหนดการให้บริการรและการปประมาณการต้นทุนของโครงการ และผู้เกี่ยวข้องทั้งหมดในโครงการได้ตกลงกันแล้ว</span><span class="sxs-lookup"><span data-stu-id="92488-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="92488-108">มีสองวิธีที่ผู้จัดการโครงการสามารถประมาณการโครงการความพยายามในการทำงานใหม่:</span><span class="sxs-lookup"><span data-stu-id="92488-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="92488-109">แทนที่ประมาณการเริ่มต้นที่จะทำให้สมบูรณ์ (ETC) ด้วยการประมาณการใหม่ของกำลังคนที่เหลือจริงในงาน</span><span class="sxs-lookup"><span data-stu-id="92488-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="92488-110">แทนที่เปอร์เซ็นต์ความคืบหน้าค่าเริ่มต้นด้วยการประมาณการใหม่ของความคืบหน้าจริงในงาน</span><span class="sxs-lookup"><span data-stu-id="92488-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="92488-111">แต่ละวิธีเหล่านี้ทำให้เกิดการคำนวณใหม่ของ ETC, ประมาณการเมื่อดำเนินงานเสร็จสมบูรณ์ (EAC) ของงาน และเปอร์เซ็นต์ความคืบหน้า และผลต่างความพยายามที่คาดการณ์ไว้ในงาน</span><span class="sxs-lookup"><span data-stu-id="92488-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="92488-112">EAC, ETC และเปอร์เซ็นต์ความคืบหน้าในงานสรุปจะมีการคำนวณอีกครั้ง และสร้างการคาดการณ์ใหม่ของผลต่างของกำลังคน</span><span class="sxs-lookup"><span data-stu-id="92488-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
