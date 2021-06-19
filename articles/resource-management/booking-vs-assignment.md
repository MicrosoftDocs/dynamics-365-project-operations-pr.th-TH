---
title: การจองและการมอบหมาย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับความแตกต่างระหว่างการจองทรัพยากรและการมอบหมายทรัพยากร
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012789"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="b385e-103">การจองและการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="b385e-103">Bookings vs assignments</span></span>

<span data-ttu-id="b385e-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="b385e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b385e-105">การจองคือการจัดสรรที่ตายตัวและไม่ตายตัวของทรัพยากรให้กับโครงการ</span><span class="sxs-lookup"><span data-stu-id="b385e-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="b385e-106">การจองแบบตายตัวใช้ความสามารถรองรับของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="b385e-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="b385e-107">การจองแสดงถึงแนวคิดขององค์กรสำหรับทีม เพื่อให้พวกเขาเข้าใจว่าจะมีการใช้ทรัพยากรอย่างไรในโครงการต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="b385e-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="b385e-108">Dynamics 365 Project Operations พิจารณาการจองแนวคิดระดับโครงการ</span><span class="sxs-lookup"><span data-stu-id="b385e-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="b385e-109">ซึ่งแตกต่างจากการจอง การมอบหมายคือการยืนยันของทรัพยากรให้กับงานโครงการในหมายกำหนดการให้บริการโครงการ</span><span class="sxs-lookup"><span data-stu-id="b385e-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="b385e-110">ทรัพยากรสามารถตั้งชื่อได้หรือทั่วไป</span><span class="sxs-lookup"><span data-stu-id="b385e-110">The resources can be named or generic.</span></span>  <span data-ttu-id="b385e-111">เมื่อความต้องการทรัพยากรได้มาจากการมอบหมายงานโครงการ Project Operations จะใช้เส้นชั้นความพยงการมอบหมายทรัพยากรเพื่อสร้างเส้นชั้นของรายละเอียดความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="b385e-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="b385e-112">อย่างไรก็ตาม จะไม่มีการรักษาการมอบหมายทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="b385e-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="b385e-113">การอัปเดตการจองที่มาจากความต้องการทรัพยากร จะไม่อัปเดตการมอบหมายทรัพยากรใดๆ</span><span class="sxs-lookup"><span data-stu-id="b385e-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="b385e-114">โดยปกติ ผลรวมของการจองทรัพยากรจะเท่ากับผลรวมของการมอบหมายทรัพยากรสำหรับงานหนึ่งหรือหลายงาน</span><span class="sxs-lookup"><span data-stu-id="b385e-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="b385e-115">อย่างไรก็ตาม Project Operations ไม่บังคับใช้ข้อตกลงนี้</span><span class="sxs-lookup"><span data-stu-id="b385e-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="b385e-116">มุมมอง **การกระทบยอด** แสดงตำแหน่งผู้จัดการโครงการที่การจองและการมอบหมายทรัพยากรไม่เห็นด้วย</span><span class="sxs-lookup"><span data-stu-id="b385e-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]