---
title: การจองและการมอบหมาย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับความแตกต่างระหว่างการจองทรัพยากรและการมอบหมายทรัพยากร
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085781"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="f1a7b-103">การจองและการมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="f1a7b-103">Bookings vs assignments</span></span>

<span data-ttu-id="f1a7b-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="f1a7b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f1a7b-105">การจองคือการจัดสรรที่ตายตัวและไม่ตายตัวของทรัพยากรให้กับโครงการ</span><span class="sxs-lookup"><span data-stu-id="f1a7b-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="f1a7b-106">การจองแบบตายตัวใช้ความสามารถรองรับของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="f1a7b-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="f1a7b-107">การมอบหมายคือการมอบหมายของทรัพยากรให้กับงานโครงการในหมายกำหนดการให้บริการโครงการ</span><span class="sxs-lookup"><span data-stu-id="f1a7b-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="f1a7b-108">ทรัพยากรสามารถเป็นได้ทั้งทรัพยากรจริงหรือทั่วไป</span><span class="sxs-lookup"><span data-stu-id="f1a7b-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="f1a7b-109">ตามหลักการแล้วสำหรับทรัพยากรจริง การจองและการมอบหมายควรยอมรับเพราะพวกเขาไม่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="f1a7b-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="f1a7b-110">อย่างไรก็ตาม Microsoft Dynamics Project Operations ไม่บังคับใช้ข้อตกลงนี้</span><span class="sxs-lookup"><span data-stu-id="f1a7b-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="f1a7b-111">มุมมอง **การกระทบยอด** แสดงตำแหน่งผู้จัดการโครงการที่การจองและการมอบหมายทรัพยากรไม่เห็นด้วย</span><span class="sxs-lookup"><span data-stu-id="f1a7b-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
