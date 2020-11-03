---
title: ซิงโครไนซ์กำลังการผลิตของทรัพยากร
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการซิงโครไนซ์กำลังการผลิตของทรัพยากรในปฏิทินและโครงการ
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085910"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="4435d-103">ซิงโครไนซ์กำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4435d-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4435d-104">กระบวนการสำหรับการซิงโครไนซ์ทรัพยากรช่วยรับประกันว่า ข้อมูลสำหรับปฏิทินและปฏิทินฐานจะไหลลงสู่การจัดกำหนดการทรัพยากรของโครงการ</span><span class="sxs-lookup"><span data-stu-id="4435d-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="4435d-105">หากปฏิทินมีการเปลี่ยนแปลง กระบวนการจะทำการปรับปรุงที่จำเป็นไปยังการจัดกำหนดการทรัพยากรโครงการ</span><span class="sxs-lookup"><span data-stu-id="4435d-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="4435d-106">นอกจากนี้ กระบวนการยังช่วยปรับปรุงประสิทธิภาพ เนื่องจากข้อมูลทรัพยากรของปฏิทินจะถูกซิงโครไนซ์ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="4435d-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="4435d-107">ดังนั้น การปรับปรุงไปยังข้อมูลการจัดกำหนดการทรัพยากรจึงเกิดขึ้นได้เร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="4435d-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="4435d-108">เราขอแนะนำให้คุณจัดกำหนดการกระบวนการเป็นกลุ่ม แทนที่จะทำทีละรายการ</span><span class="sxs-lookup"><span data-stu-id="4435d-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="4435d-109">มิฉะนั้น จะมีความเสี่ยงที่ใครบางคนจะลืมวันที่รวม เมื่อข้อมูลถูกซิงโครไนซ์ครั้งล่าสุด</span><span class="sxs-lookup"><span data-stu-id="4435d-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="4435d-110">หากไม่ใช้วันที่รวม ช่องว่างอาจเกิดขึ้นระหว่างการซิงโครไนซ์วันที่</span><span class="sxs-lookup"><span data-stu-id="4435d-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![การซิงโครไนซ์ปฏิทิน](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="4435d-112">ซิงโครไนซ์ค่าสะสมของกำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4435d-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="4435d-113">กระบวนการซิงโครไนซ์ถูกออกแบบมาเพื่อซิงโครไนซ์ข้อมูลปฏิทินทรัพยากรทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4435d-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="4435d-114">ข้อมูลนี้รวมถึงข้อมูลปฏิทินฐานเกี่ยวกับการเปลี่ยนแปลงใดๆ ในตารางกำลังการผลิตของปฏิทินทรัพยากรของโครงการ</span><span class="sxs-lookup"><span data-stu-id="4435d-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="4435d-115">หากมีการเพิ่มทรัพยากรใหม่ในโครงการ การซิงโครไนซ์จะช่วยรับประกันว่าข้อมูลปฏิทินที่ปรับปรุงพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4435d-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="4435d-116">การซิงโครไนซ์นี้สามารถทำได้ทุกเมื่อ</span><span class="sxs-lookup"><span data-stu-id="4435d-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="4435d-117">เราขอแนะนำให้คุณใช้ชุดงาน</span><span class="sxs-lookup"><span data-stu-id="4435d-117">We recommend that you use a batch.</span></span> <span data-ttu-id="4435d-118">ตัวเลือกจะพร้อมใช้งานในระหว่างการซิงโครไนซ์ของการสำรองกำลังการผลิต</span><span class="sxs-lookup"><span data-stu-id="4435d-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="4435d-119">เลือก **การจัดการโครงการและการบัญชี** &gt; **เป็นระยะ** &gt; **การซิงโครไนซ์กำลังการผลิต** &gt; **ซิงโครไนซ์ค่าสะสมของกำลังการผลิตของทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="4435d-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="4435d-120">ตั้งค่าตัวเลือกในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4435d-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="4435d-121">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="4435d-121">Option</span></span>      | <span data-ttu-id="4435d-122">รายละเอียด</span><span class="sxs-lookup"><span data-stu-id="4435d-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="4435d-123">รหัสรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="4435d-123">Period code</span></span> | <span data-ttu-id="4435d-124">หรือเลือกรหัสช่วงวันที่ของบัญชีแยกประเภททั่วไป เพื่อกำหนดวันที่เริ่มต้นและวันที่สิ้นสุดสำหรับกระบวนการซิงโครไนซ์สำหรับค่าสะสมของกำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4435d-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="4435d-125">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="4435d-125">Start date</span></span>  | <span data-ttu-id="4435d-126">ป้อนวันที่เริ่มต้นของกระบวนการซิงโครไนซ์สำหรับค่าสะสมของกำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4435d-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="4435d-127">วันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="4435d-127">End date</span></span>    | <span data-ttu-id="4435d-128">ป้อนวันที่สิ้นสุดของกระบวนการซิงโครไนซ์สำหรับค่าสะสมของกำลังการผลิตของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4435d-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="4435d-129">[![กระบวนการซิงโครไนซ์](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="4435d-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
