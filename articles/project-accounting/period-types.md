---
title: ชนิดของรอบระยะเวลา
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีตั้งค่าชนิดของรอบระยะเวลาสำหรับการประมาณรายได้
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287306"
---
# <a name="period-types"></a><span data-ttu-id="eb711-103">ชนิดของรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="eb711-103">Period types</span></span>

<span data-ttu-id="eb711-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="eb711-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="eb711-105">ชนิดของรอบระยะเวลาเป็นตัวกำหนดความถี่ในการประมาณรายได้ในโครงการ</span><span class="sxs-lookup"><span data-stu-id="eb711-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="eb711-106">หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีตั้งค่าชนิดของรอบระยะเวลาสำหรับการประมาณรายได้</span><span class="sxs-lookup"><span data-stu-id="eb711-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="eb711-107">การสร้างและทำงานกับชนิดของรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="eb711-107">Create and work with period types</span></span>
<span data-ttu-id="eb711-108">ในการสร้างและทำงานกับชนิดของรอบระยะเวลา ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="eb711-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="eb711-109">ในสภาพแวดล้อม Dynamics 365 Finance ไปที่ **การจัดการโครงการและการบัญชี** > **ติดตั้ง** > **ประมาณการ** > **ชนิดของรอบระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="eb711-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="eb711-110">เลือก **สร้าง** เพื่อสร้างชนิดของรอบระยะเวลาใหม่</span><span class="sxs-lookup"><span data-stu-id="eb711-110">Select **New** to create new period type.</span></span> <span data-ttu-id="eb711-111">ป้อนชื่อและคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="eb711-111">Enter a name and description.</span></span>
3. <span data-ttu-id="eb711-112">ในฟิลด์ **ความถี่** เลือกค่า:</span><span class="sxs-lookup"><span data-stu-id="eb711-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="eb711-113">หากคุณเลือก **รายสัปดาห์** **ทุกสองสัปดาห์** **ทุกครึ่งเดือน** **เดือน** **วัน** **ไตรมาส** หรือ **ปี** ปฏิทินจะถูกใช้เพื่อสร้างระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="eb711-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="eb711-114">หากคุณเลือก **รอบระยะเวลาบัญชีแยกประเภท** รอบระยะเวลาบัญชีแยกประเภทจากการกำหนดค่าบัญชีแยกประเภททั่วไปจะถูกใช้เพื่อสร้างรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="eb711-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="eb711-115">หากคุณเลือก **ไม่จำกัด** คุณสามารถระบุรอบระยะเวลาที่กำหนดเองได้</span><span class="sxs-lookup"><span data-stu-id="eb711-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="eb711-116">เลือกเรกคอร์ดชนิดของรอบระยะเวลา แล้วเลือก **สร้างรอบระยะเวลา** เพื่อสร้างรอบระยะเวลาสำหรับชนิดของรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="eb711-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="eb711-117">ตามความถี่ของรอบระยะเวลาที่คุณเลือก คุณอาจมีตัวเลือกในการระบุวันที่เริ่มต้นหรือจำนวนรอบระยะเวลาที่จะสร้าง</span><span class="sxs-lookup"><span data-stu-id="eb711-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="eb711-118">เลือก **รอบระยะเวลา** เพื่อตรวจสอบรอบระยะเวลาที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="eb711-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]