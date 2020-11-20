---
title: การจองและการมอบหมาย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับความแตกต่างระหว่างการจองทรัพยากรและการมอบหมายทรัพยากร
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130241"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="1d271-103">การจองและการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="1d271-103">Bookings vs assignments</span></span>

<span data-ttu-id="1d271-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="1d271-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1d271-105">การจองคือการจัดสรรที่ตายตัวและไม่ตายตัวของทรัพยากรให้กับโครงการ</span><span class="sxs-lookup"><span data-stu-id="1d271-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="1d271-106">การจองแบบตายตัวใช้ความสามารถรองรับของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="1d271-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="1d271-107">การจองแสดงถึงแนวคิดขององค์กรสำหรับทีม เพื่อให้พวกเขาเข้าใจว่าจะมีการใช้ทรัพยากรอย่างไรในโครงการต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="1d271-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="1d271-108">Dynamics 365 Project Operations ถือว่าการจองเป็นแนวคิดระดับโครงการ</span><span class="sxs-lookup"><span data-stu-id="1d271-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="1d271-109">ซึ่งแตกต่างจากการจอง การมอบหมายคือการยืนยันของทรัพยากรให้กับงานโครงการในหมายกำหนดการให้บริการโครงการ</span><span class="sxs-lookup"><span data-stu-id="1d271-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="1d271-110">ทรัพยากรสามารถตั้งชื่อได้หรือทั่วไป</span><span class="sxs-lookup"><span data-stu-id="1d271-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="1d271-111">โดยปกติ ผลรวมของการจองทรัพยากรจะเท่ากับผลรวมของการมอบหมายทรัพยากรสำหรับงานหนึ่งหรือหลายงาน</span><span class="sxs-lookup"><span data-stu-id="1d271-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="1d271-112">อย่างไรก็ตาม Project Operations ไม่บังคับใช้ข้อตกลงนี้</span><span class="sxs-lookup"><span data-stu-id="1d271-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="1d271-113">มุมมอง **การกระทบยอด** แสดงตำแหน่งผู้จัดการโครงการที่การจองและการมอบหมายทรัพยากรไม่เห็นด้วย</span><span class="sxs-lookup"><span data-stu-id="1d271-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
