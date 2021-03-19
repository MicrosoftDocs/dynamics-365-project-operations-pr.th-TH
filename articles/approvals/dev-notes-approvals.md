---
title: หมายเหตุสำหรับนักพัฒนาสำหรับการอนุมัติ
description: หัวข้อนี้ให้ข้อมูลนักพัฒนาเพิ่มเติมเกี่ยวกับการทำงานกับการอนุมัติ
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290292"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="8f36f-103">หมายเหตุสำหรับนักพัฒนาสำหรับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="8f36f-103">Developer notes for Approvals</span></span>

<span data-ttu-id="8f36f-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="8f36f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8f36f-105">Dynamics 365 Project Operations มีตรรกะการตรวจสอบความถูกต้องที่ช่วยให้แน่ใจว่าการเปลี่ยนแปลงเรกคอร์ดที่ถูกต้องผ่านขั้นตอนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="8f36f-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="8f36f-106">การเปลี่ยนเรกคอร์ดที่ถูกต้องทำให้แน่ใจว่า:</span><span class="sxs-lookup"><span data-stu-id="8f36f-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="8f36f-107">แถวที่สนับสนุนทั้งหมดถูกสร้างขึ้นในตารางที่เกี่ยวข้อง เช่น สมุดรายวัน และข้อมูลจริง</span><span class="sxs-lookup"><span data-stu-id="8f36f-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="8f36f-108">ผู้อนุมัติถูกทำเครื่องหมายเป็น **ผู้อนุมัติโครงการ** ในโครงการก่อนดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="8f36f-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]