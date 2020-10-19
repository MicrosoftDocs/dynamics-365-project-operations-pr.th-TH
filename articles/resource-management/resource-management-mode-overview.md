---
title: ภาพรวมโหมดการจัดการทรัพยากร
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันการจัดการทรัพยากรใน Dynamics 365 Project Operations
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930114"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="2ee7d-103">ภาพรวมโหมดการจัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="2ee7d-103">Resource management modes overview</span></span>

<span data-ttu-id="2ee7d-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="2ee7d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="2ee7d-105">Dynamics 365 Project Operations รองรับสองโหมดเพื่อให้คุณดำเนินการตามขั้นตอนการจองโดยรวม</span><span class="sxs-lookup"><span data-stu-id="2ee7d-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="2ee7d-106">โหมดการจัดการมีการกำหนดเป็นพารามิเตอร์โครงการและสามารถแก้ไขได้หากธุรกิจของคุณต้องการการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="2ee7d-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="2ee7d-107">โหมดส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="2ee7d-107">Central mode</span></span>
<span data-ttu-id="2ee7d-108">สำหรับองค์กรที่รวมศูนย์การจัดสรรทรัพยากรให้กับโครงการ โหมดส่วนกลางจะกำหนดวิธีที่จะทำให้ผู้จัดการโครงการสามารถกำหนดความต้องการทรัพยากรในระดับโครงการได้</span><span class="sxs-lookup"><span data-stu-id="2ee7d-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="2ee7d-109">การปฏิบัติตามความต้องการทรัพยากรถูกมอบหมายให้กับผู้จัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="2ee7d-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="2ee7d-110">ผู้จัดการโครงการสามารถยอมรับหรือปฏิเสธทรัพยากรที่เสนอโดยผู้จัดการทรัพยากรได้</span><span class="sxs-lookup"><span data-stu-id="2ee7d-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![โหมดส่วนกลาง](./media/resource-management-central.png)

<span data-ttu-id="2ee7d-112">หากต้องการจัดการทรัพยากรด้วยโหมดส่วนกลาง โปรดดู:</span><span class="sxs-lookup"><span data-stu-id="2ee7d-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="2ee7d-113">มอบหมายทรัพยากรทั่วไปที่จองได้ให้กับงานและสร้างความต้องการของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="2ee7d-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="2ee7d-114">จองทรัพยากรที่ระบุชื่อจากความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="2ee7d-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="2ee7d-115">ส่งคำขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="2ee7d-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="2ee7d-116">เติมเต็มคำขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="2ee7d-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="2ee7d-117">ยอมรับหรือปฏิเสธทรัพยากรโครงการที่นำเสนอจากคำขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="2ee7d-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="2ee7d-118">โหมดไฮบริด</span><span class="sxs-lookup"><span data-stu-id="2ee7d-118">Hybrid mode</span></span>
<span data-ttu-id="2ee7d-119">สำหรับองค์กรที่ต้องการความยืดหยุ่นในการจัดสรรทรัพยากร โหมดไฮบริดช่วยให้ทั้งผู้จัดการโครงการและผู้จัดการทรัพยากรสามารถจองทรัพยากรได้</span><span class="sxs-lookup"><span data-stu-id="2ee7d-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![โหมดไฮบริด](./media/resource-management-hybrid.png)

<span data-ttu-id="2ee7d-121">นอกเหนือจากกระบวนการของโหมดส่วนกลางที่รองรับแล้ว โปรดดูหัวข้อต่อไปนี้เพื่อจัดการขั้นตอนการจองที่รองรับอื่นๆ ทั้งหมดในโหมดไฮบริด:</span><span class="sxs-lookup"><span data-stu-id="2ee7d-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="2ee7d-122">จองทรัพยากรให้กับโครงการโดยตรง</span><span class="sxs-lookup"><span data-stu-id="2ee7d-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="2ee7d-123">จองทรัพยากรที่มีชื่อว่าสามารถจองได้ให้ทีมโครงการและมอบหมายงาน</span><span class="sxs-lookup"><span data-stu-id="2ee7d-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="2ee7d-124">จองทรัพยากรจากความต้องการทรัพยากร:</span><span class="sxs-lookup"><span data-stu-id="2ee7d-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="2ee7d-125">มอบหมายทรัพยากรทั่วไปที่จองได้ให้กับงานและสร้างความต้องการของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="2ee7d-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="2ee7d-126">จองทรัพยากรที่ระบุชื่อจากความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="2ee7d-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
