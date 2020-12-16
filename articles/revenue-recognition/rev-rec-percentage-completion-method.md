---
title: โครงการประมาณการรายได้ราคาคงที่
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับรายได้ที่มีราคาคงที่ในโครงการ
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531576"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="3d6a0-103">โครงการประมาณการรายได้ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="3d6a0-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="3d6a0-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="3d6a0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3d6a0-105">เมื่อคุณสร้างรายละเอียดการให้บริการตามสัญญาโครงการที่มีแอตทริบิวต์ต่อไปนี้ใน Dynamics 365 Project Operations บน Microsoft Dataverse ระบบจะสร้างโครงการประมาณการรายได้ราคาคงที่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3d6a0-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="3d6a0-106">ข้อมูลในโครงการนี้อ้างอิงจากสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3d6a0-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="3d6a0-107">วิธีการเรียกเก็บเงินแบบราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="3d6a0-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="3d6a0-108">โครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3d6a0-108">An associated project.</span></span>
  - <span data-ttu-id="3d6a0-109">อย่างน้อยหนึ่งเหตุการณ์สําคัญที่กำหนดไว้ในแท็บ **กำหนดการใบแจ้งหนี้** บนหน้า **รายละเอียดการให้บริการตามสัญญาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="3d6a0-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="3d6a0-110">ตรวจทานโครงการประมาณการรายได้ราคาคงที่</span><span class="sxs-lookup"><span data-stu-id="3d6a0-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="3d6a0-111">หากต้องการตรวจทานโครงการประมาณการรายได้ราคาคงที่ ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3d6a0-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="3d6a0-112">ในสภาพแวดล้อม Dynamics 365 Finance ไปที่ **การจัดการโครงการและการบัญชี** > **โครงการ** > **โครงการประมาณการรายได้ราคาคงที่**</span><span class="sxs-lookup"><span data-stu-id="3d6a0-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="3d6a0-113">เลือกโครงการที่คุณต้องการดูและดับเบิลคลิกที่ **ประมาณรหัสโครงการ** เพื่อเปิดเรกคอร์ดและตรวจทานรายละเอียดของโครงการ</span><span class="sxs-lookup"><span data-stu-id="3d6a0-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="3d6a0-114">ขยายแท็บ **โครงการ** คุณจะเห็นโครงการหนึ่งในกริด **โครงการที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="3d6a0-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="3d6a0-115">ระบบใช้สิ่งนี้เป็นโครงการเริ่มต้นเนื่องจากเป็นโครงการที่เกี่ยวข้องกับรายละเอียดการให้บริการตามสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="3d6a0-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="3d6a0-116">หากต้องการเปลี่ยนการเชื่อมโยง ให้เลือกโครงการเพิ่มเติมและเพิ่มลงในกริด **โครงการที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="3d6a0-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="3d6a0-117">หากเลือกหลายโครงการในกริดนี้ เปอร์เซ็นต์ความสำเร็จของโครงการและประมาณการรายได้จะถูกคำนวณร่วมกันสำหรับโครงการที่เลือกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3d6a0-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="3d6a0-118">ต้นทุนโครงการ โปรไฟล์รายได้ แม่แบบต้นทุน และรหัสรอบระยะเวลาสามารถตั้งค่าได้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="3d6a0-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="3d6a0-119">หากไม่ได้ตั้งค่าด้วยตนเอง ค่าจะเริ่มต้นในระหว่างการคำนวณโดยประมาณครั้งแรกสำหรับโครงการโดยใช้กฎที่กำหนดค่าสำหรับต้นทุนโครงการและโปรไฟล์รายได้</span><span class="sxs-lookup"><span data-stu-id="3d6a0-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>

