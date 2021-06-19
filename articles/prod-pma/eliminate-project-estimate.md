---
title: ตัดการประมาณการโครงการออก
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการตัดการประมาณการโครงการออกหลังจากเสร็จสิ้น
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a4ad06bef7ed66a626c6d2ad7ef01ba5b99d1c0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006939"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="eaba7-103">ตัดการประมาณการโครงการออก</span><span class="sxs-lookup"><span data-stu-id="eaba7-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eaba7-104">การประเมินโครงการแสดงมุมมองทางการเงินสำหรับงานที่ถูกประเมินและวางกำหนดการสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="eaba7-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="eaba7-105">ในการทำงานกับการประมาณการสำหรับโครงการ คุณต้องแนบโครงการกับโครงการประมาณการ</span><span class="sxs-lookup"><span data-stu-id="eaba7-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="eaba7-106">โครงการประมาณการจะขึ้นอยู่กับโครงการที่มีอยู่เสมอ อย่างไรก็ตามหลายโครงการสามารถอ้างถึงโครงการประมาณการเดียวได้</span><span class="sxs-lookup"><span data-stu-id="eaba7-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="eaba7-107">สามารถแนบได้เฉพาะโครงการราคาคงที่และโครงการการลงทุนในโครงการประมาณการ และโครงการเหล่านั้นต้องอยู่ในกลุ่มโครงการเดียวกันกับโครงการประมาณการ</span><span class="sxs-lookup"><span data-stu-id="eaba7-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="eaba7-108">ในการตัดโครงการประมาณการออก จะต้องเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="eaba7-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="eaba7-109">ขั้นตอนต่อไปนี้อธิบายวิธีตัดการประมาณการออก</span><span class="sxs-lookup"><span data-stu-id="eaba7-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="eaba7-110">ไปที่ **การจัดการโครงการและการบัญชี** > **โครงการทั้งหมด** และเปิดโครงการ</span><span class="sxs-lookup"><span data-stu-id="eaba7-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="eaba7-111">บนแท็บ **จัดการ** เลือกแท็บ **การประมาณการ** และบนหน้า **การประมาณการ** เลือก **ตัดออก**</span><span class="sxs-lookup"><span data-stu-id="eaba7-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="eaba7-112">บนหน้า **ตัดการประมาณการ** บนแท็บ **ทั่วไป** ตั้งค่าตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="eaba7-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="eaba7-113">**รหัสรอบระยะเวลา**: เลือกรหัสรอบระยะเวลาเพื่อเลือกโครงการประมาณการที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="eaba7-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="eaba7-114">**วันที่การประมาณการ**: เลือกวันที่การประมาณการที่เหมาะสมสำหรับการตัดออก</span><span class="sxs-lookup"><span data-stu-id="eaba7-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="eaba7-115">**ตัดออกด้วยคำเตือน WIP**: เปิดใช้งานตัวเลือกนี้เพื่อแจ้งเตือนเมื่อการประมาณการที่เกี่ยวข้องกับงานที่กำลังดำเนินการ (WIP) จะถูกตัดออก</span><span class="sxs-lookup"><span data-stu-id="eaba7-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="eaba7-116">เมื่อไม่ได้เปิดใช้งานตัวเลือกนี้ การกำจัดจะไม่สามารถดำเนินต่อไปได้หากมีธุรกรรมที่ไม่ได้ประมาณไว้</span><span class="sxs-lookup"><span data-stu-id="eaba7-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="eaba7-117">ตัวเลือกนี้จะใช้ได้เฉพาะเมื่อมีการใช้การตัดออกกับโครงการประมาณการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="eaba7-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="eaba7-118">ไม่สามารถใช้ได้หากคุณใช้การลงบัญชีเป็นระยะ</span><span class="sxs-lookup"><span data-stu-id="eaba7-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="eaba7-119">การตั้งค่านี้ใช้ได้กับการตั้งค่าบนแท็บ **การประมาณการ** บนหน้า **พารามิเตอร์โครงการ** ในกลุ่มฟิลด์ **อนุญาตให้ตัดออกเมื่อมีธุรกรรมที่ไม่ได้ประมาณไว้**</span><span class="sxs-lookup"><span data-stu-id="eaba7-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="eaba7-120">**ตั้งค่าขั้นตอนเป็นเสร็จสิ้น**: เปิดใช้งานตัวเลือกนี้เพื่อตั้งค่าระยะของโครงการประมาณการเป็น **เสร็จแล้ว** หลังจากที่คุณเรียกใช้การตัดออก</span><span class="sxs-lookup"><span data-stu-id="eaba7-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="eaba7-121">**พิมพ์รายการประมาณการ**: เลือกข้อมูลที่จะรวมเมื่อพิมพ์รายการประมาณการ</span><span class="sxs-lookup"><span data-stu-id="eaba7-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="eaba7-122">**แสดง Infolog**: เปิดใช้งานตัวเลือกนี้เพื่อแสดง Infolog</span><span class="sxs-lookup"><span data-stu-id="eaba7-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="eaba7-123">**วันที่ลงบัญชี**: เลือกวันที่ลงรายการบัญชีแยกประเภทของการประมาณการ</span><span class="sxs-lookup"><span data-stu-id="eaba7-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="eaba7-124">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="eaba7-124">Select **OK**.</span></span>
5. <span data-ttu-id="eaba7-125">หลังจากกระบวนการตัดออกเสร็จสมบูรณ์ โครงการประมาณการที่ถูกตัดออกจะแสดงด้วยค่าลบ</span><span class="sxs-lookup"><span data-stu-id="eaba7-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="eaba7-126">หากคุณไม่ได้ตั้งใจที่จะกำจัดการประมาณการ คุณสามารถเลือกการประมาณการที่ตัดออกแล้วเลือก **ย้อนกลับการตัดออก**</span><span class="sxs-lookup"><span data-stu-id="eaba7-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]