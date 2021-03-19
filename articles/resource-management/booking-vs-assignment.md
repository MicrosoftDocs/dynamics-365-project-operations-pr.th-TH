---
title: การจองและการมอบหมาย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับความแตกต่างระหว่างการจองทรัพยากรและการมอบหมายทรัพยากร
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279926"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="471c9-103">การจองและการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="471c9-103">Bookings vs assignments</span></span>

<span data-ttu-id="471c9-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="471c9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="471c9-105">การจองคือการจัดสรรที่ตายตัวและไม่ตายตัวของทรัพยากรให้กับโครงการ</span><span class="sxs-lookup"><span data-stu-id="471c9-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="471c9-106">การจองแบบตายตัวใช้ความสามารถรองรับของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="471c9-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="471c9-107">การจองแสดงถึงแนวคิดขององค์กรสำหรับทีม เพื่อให้พวกเขาเข้าใจว่าจะมีการใช้ทรัพยากรอย่างไรในโครงการต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="471c9-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="471c9-108">Dynamics 365 Project Operations พิจารณาการจองแนวคิดระดับโครงการ</span><span class="sxs-lookup"><span data-stu-id="471c9-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="471c9-109">ซึ่งแตกต่างจากการจอง การมอบหมายคือการยืนยันของทรัพยากรให้กับงานโครงการในหมายกำหนดการให้บริการโครงการ</span><span class="sxs-lookup"><span data-stu-id="471c9-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="471c9-110">ทรัพยากรสามารถตั้งชื่อได้หรือทั่วไป</span><span class="sxs-lookup"><span data-stu-id="471c9-110">The resources can be named or generic.</span></span>  <span data-ttu-id="471c9-111">เมื่อความต้องการทรัพยากรได้มาจากการมอบหมายงานโครงการ Project Operations จะใช้เส้นชั้นความพยงการมอบหมายทรัพยากรเพื่อสร้างเส้นชั้นของรายละเอียดความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="471c9-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="471c9-112">อย่างไรก็ตาม จะไม่มีการรักษาการมอบหมายทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="471c9-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="471c9-113">การอัปเดตการจองที่มาจากความต้องการทรัพยากร จะไม่อัปเดตการมอบหมายทรัพยากรใดๆ</span><span class="sxs-lookup"><span data-stu-id="471c9-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="471c9-114">โดยปกติ ผลรวมของการจองทรัพยากรจะเท่ากับผลรวมของการมอบหมายทรัพยากรสำหรับงานหนึ่งหรือหลายงาน</span><span class="sxs-lookup"><span data-stu-id="471c9-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="471c9-115">อย่างไรก็ตาม Project Operations ไม่บังคับใช้ข้อตกลงนี้</span><span class="sxs-lookup"><span data-stu-id="471c9-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="471c9-116">มุมมอง **การกระทบยอด** แสดงตำแหน่งผู้จัดการโครงการที่การจองและการมอบหมายทรัพยากรไม่เห็นด้วย</span><span class="sxs-lookup"><span data-stu-id="471c9-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]