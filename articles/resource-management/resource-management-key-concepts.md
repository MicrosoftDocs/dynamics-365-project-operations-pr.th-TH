---
title: แนวคิดหลักในการจัดการทรัพยากร
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับความสามารถในการจัดการทรัพยากรใน Microsoft Dynamics Project Operations
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a14f0ec328049d1b199201955c384df9fac61e39
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123896"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="62a49-103">แนวคิดหลักในการจัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="62a49-103">Resource management key concepts</span></span>

<span data-ttu-id="62a49-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="62a49-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="62a49-105">ทรัพยากรเป็นสินทรัพย์ที่สำคัญที่สุดขององค์กรที่ใช้การบริการ</span><span class="sxs-lookup"><span data-stu-id="62a49-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="62a49-106">ความสามารถในการค้นหาทรัพยากรที่ถูกต้องในเวลาที่เหมาะสม จองทรัพยากรเหล่านั้นในโครงการ และใช้ทรัพยากร และช่วยให้องค์กรบรรลุเป้าหมายรายได้ และเป้าหมายความพึงพอใจของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="62a49-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="62a49-107">คุณสามารถใช้ฟังก์ชันการจัดเตรียมทรัพยากรโครงการใน Dynamics 365 Project Operations เพื่อดำเนินงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="62a49-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="62a49-108">สร้างทีมโครงการโดยการจองที่มีพร้อมใช้งานและทรัพยากรที่มีคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="62a49-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="62a49-109">สร้างเรกคอร์ดสมาชิกในทีมทั่วไปและกำหนดบทบาทและหน่วยองค์กรทรัพยากรของตน</span><span class="sxs-lookup"><span data-stu-id="62a49-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="62a49-110">สร้างความต้องการทรัพยากรสำหรับสมาชิกในทีมทั่วไปจากการมอบหมายงานของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="62a49-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="62a49-111">จับคู่ทักษะโดยการระบุทักษะที่กำหนดไว้ในความต้องการทรัพยากรกับทักษะของทรัพยากรที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="62a49-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="62a49-112">ทรัพยากรทดแทน</span><span class="sxs-lookup"><span data-stu-id="62a49-112">Substitute resources.</span></span>
- <span data-ttu-id="62a49-113">จัดการมอบหมายกำหนดการให้บริการโครงการและการจองทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="62a49-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="62a49-114">กระทบยอดแตกต่างในการจองและงานมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="62a49-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="62a49-115">เปลี่ยนการจองทรัพยากรในการตอบสนองต่อสถานะที่ไม่อยู่ที่สำนักงาน</span><span class="sxs-lookup"><span data-stu-id="62a49-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="62a49-116">ทำงานร่วมกันระหว่างผู้จัดการโครงการและผู้จัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="62a49-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="62a49-117">ดูประวัติของการใช้ทรัพยากรกับเป้าหมายรวมถึงการแบ่งการใช้เวลาของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="62a49-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="62a49-118">เก็บรักษาทักษะและข้อมูลความชำนาญ</span><span class="sxs-lookup"><span data-stu-id="62a49-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="62a49-119">คุณสามารถสรรหาโครงการของคุณกับทีมงานของทรัพยากรทั่วไปหรือทรัพยากรที่ระบุชื่อใน Project Operations</span><span class="sxs-lookup"><span data-stu-id="62a49-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="62a49-120">คุณสามารถใช้วิธีการต่างๆเพื่อเพิ่มและมอบหมายสมาชิกในทีมและจัดการการจองและงานมอบหมายของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="62a49-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 
