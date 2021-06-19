---
title: สร้างแบบจำลองการคาดการณ์สำหรับงบประมาณโครงการ
description: หัวข้อนี้อธิบายวิธีสร้างแบบจำลองการคาดการณ์สำหรับงบประมาณที่เหลือ
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3549b41fce72b44230ab27de081dade15a912266
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006325"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="2a071-103">สร้างแบบจำลองการคาดการณ์สำหรับงบประมาณโครงการ</span><span class="sxs-lookup"><span data-stu-id="2a071-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a071-104">หัวข้อนี้อธิบายวิธีสร้างแบบจำลองการคาดการณ์สำหรับงบประมาณที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="2a071-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="2a071-105">โครงการที่อยู่ภายใต้การควบคุมงบประมาณจะใช้งบประมาณสองประเภท: เดิมและที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="2a071-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="2a071-106">เมื่อคุณสร้างงบประมาณโครงการ คุณต้องระบุแบบจำลองการคาดการณ์งบประมาณเดิมและงบประมาณคงเหลือที่สร้างขึ้นในหน้า **แบบจำลองการคาดการณ์**</span><span class="sxs-lookup"><span data-stu-id="2a071-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="2a071-107">งบประมาณโครงการตามแบบจำลองที่ระบุถูกสร้างขึ้นเมื่อคุณยอมรับงบประมาณโครงการ</span><span class="sxs-lookup"><span data-stu-id="2a071-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="2a071-108">แบบจำลองการคาดการณ์ที่ใช้สำหรับการควบคุมงบประมาณไม่สามารถมีแบบจำลองย่อยหรือใช้เป็นแบบจำลองย่อยได้</span><span class="sxs-lookup"><span data-stu-id="2a071-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="2a071-109">เลือก **การจัดการโครงการและการบัญชี** > **การตั้งค่า** > **การคาดการณ์**  > **แบบจำลองการคาดการณ์**</span><span class="sxs-lookup"><span data-stu-id="2a071-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="2a071-110">เลือก **ใหม่** เพื่อสร้างแบบจำลองการคาดการณ์ใหม่ จากนั้นป้อนหมายเลขรหัสแบบจำลองและชื่อสำหรับแบบจำลองใหม่</span><span class="sxs-lookup"><span data-stu-id="2a071-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="2a071-111">ตั้งค่าตัวเลือก **หยุดแล้ว** เป็น **ใช่** เพื่อป้องกันการเปลี่ยนแปลงใดๆ ในรายการการคาดการณ์สำหรับแบบจำลองการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="2a071-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="2a071-112">ถ้ารายการการคาดการณ์ที่เชื่อมโยงกับแบบจำลองควรสร้างการคาดการณ์กระแสเงินสดในบัญชีแยกประเภททั่วไป ให้ตั้งค่า **รวมไว้ในการคาดการณ์กระแสเงินสด** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="2a071-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="2a071-113">หากต้องการใช้วันที่โครงการเป็นวันที่ในใบแจ้งหนี้ ให้ตั้งค่า **คาดการณ์วันที่ใบแจ้งหนี้** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="2a071-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="2a071-114">ในฟิลด์ **ประเภทงบประมาณ** เลือกประเภทแบบจำลองประเภทใดประเภทหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2a071-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="2a071-115">**งบประมาณเดิม**: ใช้จำนวนงบประมาณเดิมที่มีการผูกมัดเมื่อมีการสร้างและอนุมัติงบประมาณเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="2a071-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="2a071-116">**งบประมาณที่เหลือ**: ใช้จำนวนงบประมาณที่เหลือในช่วงอายุของโครงการ</span><span class="sxs-lookup"><span data-stu-id="2a071-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="2a071-117">ยอดคงเหลือในแบบจำลองการคาดการณ์นี้จะลดลงตามธุรกรรมจริงและเพิ่มขึ้นหรือลดลงโดยการแก้ไขงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="2a071-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="2a071-118">**ดำเนินการส่งต่อ**: ใช้จำนวนงบประมาณยกยอดสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="2a071-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="2a071-119">ยกยอดไปเป็นกระบวนการทางเลือกที่สามารถเรียกใช้เพื่อโอนจำนวนงบประมาณที่ไม่ได้ใช้จากปีบัญชีหนึ่งไปยังอีกปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="2a071-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="2a071-120">ตั้งค่าตัวเลือกดังต่อไปนี้ตามกำหนด:</span><span class="sxs-lookup"><span data-stu-id="2a071-120">Set the following options as required:</span></span>

   - <span data-ttu-id="2a071-121">เปิดใช้งาน **คาดการณ์วันที่ใบแจ้งหนี้** เพื่อใช้วันที่โครงการเป็นวันที่ในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="2a071-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="2a071-122">เปิดใช้งาน **คาดการณ์ด้วย WIP** เพื่อคาดการณ์ตามงานที่กำลังดำเนินการ (WIP) จากนั้นเลือกประเภทของ WIP</span><span class="sxs-lookup"><span data-stu-id="2a071-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="2a071-123">คุณสามารถใช้ค่าเริ่มต้นของ **ประเภทงบประมาณ** เป็น **ไม่มี** หรือป้อนประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="2a071-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="2a071-124">ไม่สามารถเปลี่ยนแปลงประเภทงบประมาณได้หลังจากที่คุณเปลี่ยนแปลงเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="2a071-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="2a071-125">หากคุณเปลี่ยนประเภทงบประมาณเริ่มต้น ตัวเลือกอื่นๆ ทั้งหมดจะไม่พร้อมใช้งานสำหรับการอัปเดต และคุณไม่สามารถใช้แบบจำลองการคาดการณ์นี้ซ้ำได้</span><span class="sxs-lookup"><span data-stu-id="2a071-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]