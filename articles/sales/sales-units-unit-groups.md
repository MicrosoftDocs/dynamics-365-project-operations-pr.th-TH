---
title: หน่วยนับและกลุ่มของหน่วยนับ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีสร้างหน่วยนับและกลุ่มของหน่วยนับใน Dynamics 365 Project Operations
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 162366f4b7aa678b4e39d9745a657037bf36cbe0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277361"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="bd686-103">หน่วยนับและกลุ่มของหน่วยนับ</span><span class="sxs-lookup"><span data-stu-id="bd686-103">Units and unit groups</span></span>

<span data-ttu-id="bd686-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="bd686-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bd686-105">หน่วยคือปริมาณหรือการวัดที่คุณขายผลิตภัณฑ์หรือการบริการของคุณ</span><span class="sxs-lookup"><span data-stu-id="bd686-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="bd686-106">ตัวอย่างเช่น ถ้าคุณขายวัสดุอุปกรณ์ทำสวน คุณอาจขายเมล็ดพืชในหน่วยของห่อ กล่อง และแท่นวางสินค้า</span><span class="sxs-lookup"><span data-stu-id="bd686-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="bd686-107">กลุ่มของหน่วยนับคือคอลเลกชันของหน่วยต่างๆ</span><span class="sxs-lookup"><span data-stu-id="bd686-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="bd686-108">การทำตามขั้นตอนในหัวข้อนี้ ตรวจสอบให้แน่ใจว่าคุณได้รับมอบหมายบบทบาท System Administrator หรือ Sales Professional Manager หรือมีสิทธิ์เทียบเท่า</span><span class="sxs-lookup"><span data-stu-id="bd686-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="bd686-109">การสร้างกลุ่มของหน่วยนับ</span><span class="sxs-lookup"><span data-stu-id="bd686-109">Create a unit group</span></span>

1. <span data-ttu-id="bd686-110">ในแผนผังเว็บไซต์ เลือก **หน่วยนับ**</span><span class="sxs-lookup"><span data-stu-id="bd686-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="bd686-111">เลือก **ใหม่** และในกล่องโต้ตอบ **สร้างกลุ่มของหน่วยนับ** ให้ป้อนชื่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="bd686-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="bd686-112">ในฟิลด์ **หน่วยหลัก** ให้ป้อนหน่วยวัดทั่วไปที่ต่ำที่สุดที่ผลิตภัณฑ์จะถูกขายในหน่วยนี้</span><span class="sxs-lookup"><span data-stu-id="bd686-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="bd686-113">ตัวอย่างเช่น คุณอาจป้อน "ชิ้น" หรือ "ออนซ์"</span><span class="sxs-lookup"><span data-stu-id="bd686-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="bd686-114">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bd686-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="bd686-115">เพิ่มหน่วยหรือกลุ่มของหน่วยนับ</span><span class="sxs-lookup"><span data-stu-id="bd686-115">Add units to a unit group</span></span>

1. <span data-ttu-id="bd686-116">เปิดกลุ่มของหน่วยนับ และบนแท็บ **ที่เกี่ยวข้อง** เลือก **หน่วย**</span><span class="sxs-lookup"><span data-stu-id="bd686-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="bd686-117">คุณจะเห็นว่าได้มีการเพิ่มหน่วยหลักแล้ว</span><span class="sxs-lookup"><span data-stu-id="bd686-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="bd686-118">เลือก **เพิ่มหน่วยใหม่** และบนเพจ **สร้างด่วน: หน่วย** ในฟิลด์ **ชื่อ** ให้ป้อนชื่อของหน่วย</span><span class="sxs-lookup"><span data-stu-id="bd686-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="bd686-119">ในฟิลด์ **ปริมาณ** ให้ป้อนปริมาณที่หน่วยจะมี</span><span class="sxs-lookup"><span data-stu-id="bd686-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="bd686-120">ตัวอย่างเช่น ถ้ากล่องประกอบด้วยสองชิ้นส่วน ให้ป้อน "2"</span><span class="sxs-lookup"><span data-stu-id="bd686-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="bd686-121">ในฟิลด์ **หน่วยฐาน** ให้เลือกหน่วยฐานเพื่อสร้างหน่วยวัดต่ำสุดสำหรับหน่วย</span><span class="sxs-lookup"><span data-stu-id="bd686-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="bd686-122">ตัวอย่างเช่น คุณอาจเลือก "ชิ้น"</span><span class="sxs-lookup"><span data-stu-id="bd686-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="bd686-123">เลือก **บันทึก**:</span><span class="sxs-lookup"><span data-stu-id="bd686-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]