---
title: แก้ไขการจอง
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีอัปเดตและทำการเปลี่ยนแปลงไปยังการจอง
author: ruhercul
manager: Annbe
ms.date: 11/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3980df0608c387d47ad68bbf2e816d408f1c2cf0
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841411"
---
# <a name="edit-bookings"></a><span data-ttu-id="798f9-103">แก้ไขการจอง</span><span class="sxs-lookup"><span data-stu-id="798f9-103">Edit Bookings</span></span>

<span data-ttu-id="798f9-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="798f9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="798f9-105">เมื่อมีการเปลี่ยนแปลงเกิดขึ้นในโครงการที่คุณต้องอัปเดตการจองที่มีอยู่ คุณสามารถทำการเปลี่ยนแปลงได้หลายวิธี</span><span class="sxs-lookup"><span data-stu-id="798f9-105">When changes occur on a project that require you to update existing bookings, there are several ways to make the changes.</span></span> <span data-ttu-id="798f9-106">หัวข้อนี้ระบุวิธีการอัปเดตและทำการเปลี่ยนแปลงไปยังการจอง</span><span class="sxs-lookup"><span data-stu-id="798f9-106">This topic outlines how to update and make changes to bookings.</span></span>

## <a name="resource-reconciliation"></a><span data-ttu-id="798f9-107">การกระทบยอดทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="798f9-107">Resource reconciliation</span></span>

<span data-ttu-id="798f9-108">จากมุมมอง **การกระทบยอดทรัพยากร** คุณสามารถดูความแตกต่างระหว่างงานที่มอบหมายให้กับทรัพยากรกับการจองที่จัดสรรให้กับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="798f9-108">From the **Resource reconciliation** view, you can view the differences between the work assigned to a resource against the bookings allocated to the resource.</span></span> <span data-ttu-id="798f9-109">ในอินสแตนซ์ที่มีการมอบหมายมากกว่าการจอง คุณสามารถใช้กริด **การกระทบยอดทรัพยากร** เพื่อขยายการจอง</span><span class="sxs-lookup"><span data-stu-id="798f9-109">In instances where there are more assignments than bookings, you can use the **Resource reconciliation** grid to extend the bookings.</span></span> <span data-ttu-id="798f9-110">การดำเนินการนี้ช่วยให้คุณสามารถสร้างการจองใหม่เพื่อให้ครอบคลุมการขาดแคลนใดๆ ที่เน้นในมุมมอง</span><span class="sxs-lookup"><span data-stu-id="798f9-110">This action lets you create new bookings to cover any shortage that is highlighted in the view.</span></span>

## <a name="maintain-bookings"></a><span data-ttu-id="798f9-111">รักษาการจอง</span><span class="sxs-lookup"><span data-stu-id="798f9-111">Maintain bookings</span></span>

<span data-ttu-id="798f9-112">จากกริด **สมาชิกในกลุ่มคน** ผู้จัดการโครงการสามารถเน้นทรัพยากรเฉพาะ และเลือก **รักษาการจอง** เพื่อเปิดมุมมองที่กรองแล้วของบอร์ดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="798f9-112">From the **Team Member** grid, a Project manager can highlight a specific resource and select **Maintain Bookings** to open a filtered view of the Schedule Board.</span></span> <span data-ttu-id="798f9-113">มุมมองมุ่งเน้นไปที่การจองที่จัดสรรสำหรับทรัพยากรที่ระบุในโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="798f9-113">The view focuses on the bookings allocated for the specified resource on the relevant project.</span></span> <span data-ttu-id="798f9-114">จากมุมมองนี้ ผู้จัดการโครงการสามารถขยาย ย่อ หรือย้ายการจอง โดยมีรายละเอียดที่เพิ่มขึ้นเมื่อเทียบกับตัวเลือก **ขยายการจอง**</span><span class="sxs-lookup"><span data-stu-id="798f9-114">From this view, the Project manager can extend, shorten, or move the bookings with increased granularity compared to the **Extend Bookings** option.</span></span> <span data-ttu-id="798f9-115">นอกจากนี้ ผู้จัดการโครงการยังสามารถทดแทนทรัพยากรได้</span><span class="sxs-lookup"><span data-stu-id="798f9-115">The Project manager can also substitute resources.</span></span>

## <a name="schedule-board"></a><span data-ttu-id="798f9-116">กระดานตารางเวลา</span><span class="sxs-lookup"><span data-stu-id="798f9-116">Schedule Board</span></span>

<span data-ttu-id="798f9-117">จาก **บอร์ดกำหนดการ** ผู้จัดการทรัพยากรมีมุมมองผลงานของการจองทั้งหมดในองค์กร</span><span class="sxs-lookup"><span data-stu-id="798f9-117">From the **Schedule Board**, the Resource manager has a portfolio view of all bookings across an organization.</span></span> <span data-ttu-id="798f9-118">จากมุมมองนี้ ผู้จัดการทรัพยากรสามารถขยาย ย่อ หรือย้ายการจองที่มีอยู่ที่คล้ายกับความสามารถที่มีให้ใน **รักษาการจอง**</span><span class="sxs-lookup"><span data-stu-id="798f9-118">From this view, the Resource manager can extend, shorten, or move existing bookings similar to the capabilities offered in **Maintain Bookings**.</span></span> <span data-ttu-id="798f9-119">นอกจากนี้ ผู้จัดการทรัพยากรยังสามารถทดแทนทรัพยากรที่มีอยู่ที่จัดสรรให้กับการจองเฉพาะได้ โดยคลิกขวาที่การจองและเลือก **ทดแทนทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="798f9-119">The Resource manager can also substitute existing resources allocated to a specific booking by right-clicking the booking, and selecting **Substitute Resource**.</span></span> <span data-ttu-id="798f9-120">นอกจากนี้ ผู้จัดการทรัพยากรยังสามารถแก้ไขเส้นชั้นของการจองที่มีอยู่ได้ โดยการคลิกขวาที่การจองและเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="798f9-120">Resource managers can also edit the contours of existing bookings by right-clicking the booking and selecting **Edit**.</span></span>
