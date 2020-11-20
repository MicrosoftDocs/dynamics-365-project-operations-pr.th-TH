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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483971"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="e4b07-103">หมายเหตุสำหรับนักพัฒนาสำหรับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="e4b07-103">Developer notes for Approvals</span></span>

<span data-ttu-id="e4b07-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="e4b07-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e4b07-105">Dynamics 365 Project Operations มีตรรกะการตรวจสอบความถูกต้องที่ช่วยให้แน่ใจว่าการเปลี่ยนแปลงเรกคอร์ดที่ถูกต้องผ่านขั้นตอนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="e4b07-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="e4b07-106">การเปลี่ยนเรกคอร์ดที่ถูกต้องทำให้แน่ใจว่า:</span><span class="sxs-lookup"><span data-stu-id="e4b07-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="e4b07-107">แถวที่สนับสนุนทั้งหมดถูกสร้างขึ้นในตารางที่เกี่ยวข้อง เช่น สมุดรายวัน และข้อมูลจริง</span><span class="sxs-lookup"><span data-stu-id="e4b07-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="e4b07-108">ผู้อนุมัติถูกทำเครื่องหมายเป็น **ผู้อนุมัติโครงการ** ในโครงการก่อนดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="e4b07-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
