---
title: กำลังส่งคำขอทรัพยากร
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการส่งคำขอสำหรับทรัพยากรโครงการ
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086025"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="b9d21-103">กำลังส่งคำขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="b9d21-103">Submitting a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b9d21-104">คุณสามารถส่งคำขอทรัพยากรที่สร้างขึ้นเป็นคำขอทรัพยากรได้</span><span class="sxs-lookup"><span data-stu-id="b9d21-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="b9d21-105">จากนั้นคำขอจะถูกส่งไปยังผู้จัดการทรัพยากรเพื่อทำตามคำขอ</span><span class="sxs-lookup"><span data-stu-id="b9d21-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="b9d21-106">ใน Project Service Automation (PSA) ในเพจ **โครงการ** ให้คลิกแท็บ **ทีม** เพื่อดูรายการทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="b9d21-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="b9d21-107">เลือกทรัพยากรทั่วไปที่มีความจำเป็นจากในรายการ จากนั้นคลิก **ส่งคำขอ**</span><span class="sxs-lookup"><span data-stu-id="b9d21-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![กำลังส่งคำขอทรัพยากร](media/RM-how-to-18.png)

<span data-ttu-id="b9d21-109">สถานะของคำขอของสมาชิกทีมทั่วไปจะถูกเปลี่ยนเป็น **ส่งแล้ว**</span><span class="sxs-lookup"><span data-stu-id="b9d21-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="b9d21-110">หลังจากคำขอได้รับการทำตามโดยผู้จัดการทรัพยากร ทรัพยากรทั่วไปจะถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อ หากผู้จัดการทรัพยากรทำตามคำขอด้วยการจองของทรัพยากรที่ระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="b9d21-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="b9d21-111">มิฉะนั้น ทรัพยากรทั่วไปจะยังคงอยู่ในทีมและสถานะคำขอจะถูกเปลี่ยนเป็น **ตามมีการตรวจทาน** หากผู้จัดการทรัพยากรได้เสนอทรัพยากรที่ระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="b9d21-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review** , if the resource manager has proposed a named resource.</span></span>
