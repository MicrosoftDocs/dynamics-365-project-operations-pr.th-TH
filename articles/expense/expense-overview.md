---
title: ภาพรวมค่าใช้จ่าย
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันค่าใช้จ่ายใน Project Operations
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6c5ef2a45e8141bda38baf3eaf0a403d6db95e48
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122861"
---
# <a name="expense-home-page"></a><span data-ttu-id="4daa6-103">โฮมเพจค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="4daa6-103">Expense home page</span></span>

<span data-ttu-id="4daa6-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="4daa6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="4daa6-105">Dynamics 365 Project Operations รองรับความสามารถในการประมวลผลค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="4daa6-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="4daa6-106">การประมวลผลค่าใช้จ่ายเกิดขึ้นโดยมีหรือไม่มีโครงการโดยใช้เวิร์กโฟลว์ที่ปรับแต่งได้ของนโยบาย ประเภทธุรกรรม และการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="4daa6-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="4daa6-107">ใน Project Operations มีรูปแบบการปรับใช้งานที่รองรับสองแบบสำหรับค่าใช้จ่าย:</span><span class="sxs-lookup"><span data-stu-id="4daa6-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="4daa6-108">**เต็มรูปแบบ**: การปรับใช้งานเต็มรูปแบบสามารถใช้ได้สำหรับ **Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง** หรือ **Project Operations สำหรับสถานการณ์ของใบสั่งผลิต**</span><span class="sxs-lookup"><span data-stu-id="4daa6-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="4daa6-109">**ขั้นพื้นฐาน**: การปรับใช้งานขั้นพื้นฐานสามารถใช้ได้สำหรับ **Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง** และ **การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว**</span><span class="sxs-lookup"><span data-stu-id="4daa6-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="4daa6-110">เต็ม</span><span class="sxs-lookup"><span data-stu-id="4daa6-110">Full</span></span> 
<span data-ttu-id="4daa6-111">การปรับใช้งานค่าใช้จ่ายเต็มรูปแบบให้การบังคับใช้นโยบายที่สมบูรณ์ซึ่งรวมถึงความสามารถในการสร้างนโยบาย เช่น:</span><span class="sxs-lookup"><span data-stu-id="4daa6-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="4daa6-112">ค่าจำกัดประเภทค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="4daa6-112">Expense category limits</span></span>
  - <span data-ttu-id="4daa6-113">การเดินทาง</span><span class="sxs-lookup"><span data-stu-id="4daa6-113">Travel</span></span>
  - <span data-ttu-id="4daa6-114">เบี้ยเลี้ยง</span><span class="sxs-lookup"><span data-stu-id="4daa6-114">Per diem</span></span>
  - <span data-ttu-id="4daa6-115">การนำเข้าบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="4daa6-115">Credit card imports</span></span>
  - <span data-ttu-id="4daa6-116">การรู้จำอักขระด้วยแสงของใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="4daa6-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="4daa6-117">พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="4daa6-117">Basic</span></span> 
<span data-ttu-id="4daa6-118">สถานการณ์การปรับใช้งานค่าใช้จ่ายขั้นพื้นฐานให้คุณสามารถบันทึกค่าใช้จ่ายพื้นฐานสำหรับโครงการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4daa6-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="4daa6-119">สำหรับข้อมูลเพิ่มเติม โปรดดู [รายการค่าใช้จ่าย (ใช้งานง่าย)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="4daa6-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="4daa6-120">กำหนดการปรับใช้งานค่าใช้จ่ายของคุณ</span><span class="sxs-lookup"><span data-stu-id="4daa6-120">Determine your Expense deployment</span></span>
<span data-ttu-id="4daa6-121">หากต้องการตรวจสอบว่าคุณกำลังเรียกใช้การปรับใช้งานการจัดการค่าใช้จ่ายขั้นพื้นฐานหรือไม่ ให้ตรวจสอบว่า URL ที่อยู่ลงท้ายด้วย **.crm.dynamics.com**</span><span class="sxs-lookup"><span data-stu-id="4daa6-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
