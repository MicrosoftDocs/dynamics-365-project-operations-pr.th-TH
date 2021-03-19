---
title: การเติมเต็มความต้องการทรัพยากร
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการเติมเต็มความต้องการทรัพยากร
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
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
ms.openlocfilehash: 5df7431aa0385381a13927db6ae757f87f1832f1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283121"
---
# <a name="fulfilling-resource-requests"></a><span data-ttu-id="8bbe6-103">คำขอการเติมเต็มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8bbe6-103">Fulfilling resource requests</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8bbe6-104">ความต้องการทรัพยากรสามารถส่งเป็นคำขอทรัพยากรไปยังผู้จัดการทรัพยากรที่รับผิดชอบในการเติมเต็มคำขอเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="8bbe6-104">Resource requirements can be sent as resource requests to the resource manager who is responsible for fulfilling those requests.</span></span>

<span data-ttu-id="8bbe6-105">คำขอทรัพยากรจะแสดงเป็นรายการในมุมมอง **คำขอทรัพยากรที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="8bbe6-105">Resource requests are shown as a list in the **Active Resource Requests** view.</span></span>

> ![รายการของคำขอทรัพยากร](media/Resource-Management-image59.png)

<span data-ttu-id="8bbe6-107">เพื่อเติมเต็มคำขอ โปรดเลือกในรายการแล้วจากนั้นเลือก **ค้นหาทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="8bbe6-107">To fulfill a request, select it in the list, and then select **Find Resources**.</span></span> <span data-ttu-id="8bbe6-108">อีกวิธีหนึ่ง คลิกสองครั้งที่แถวเพื่อเปิดคำขอ</span><span class="sxs-lookup"><span data-stu-id="8bbe6-108">Alternatively, double-click a row to open the request.</span></span> <span data-ttu-id="8bbe6-109">จากนั้นคุณสามารถเลือกแท็บ **ความต้องการทรัพยากร** เพื่อดูความต้องการสำหรับคำขอนั้น</span><span class="sxs-lookup"><span data-stu-id="8bbe6-109">You can then select the **Resource Requirement** tab to view the requirements for that request.</span></span> <span data-ttu-id="8bbe6-110">หากต้องการเริ่มเติมเต็มคำขอ โปรดเลือก **ค้นหาทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="8bbe6-110">To start to fulfill the request, select **Find Resources**.</span></span>

> ![รายละเอียดความต้องการทรัพยากร](media/Resource-Management-image60.png)

<span data-ttu-id="8bbe6-112">ผู้ช่วยของหมายกำหนดการให้บริการจะปรากฏขึ้นและถูกกรองตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="8bbe6-112">The Schedule Assistant appears and is filtered by the requirements.</span></span> <span data-ttu-id="8bbe6-113">โปรดเลือกทรัพยากร และจากนั้นโปรดเลือก **จอง**</span><span class="sxs-lookup"><span data-stu-id="8bbe6-113">Select the resource, and then select **Book**.</span></span>

> ![ทรัพยากรที่เลือก](media/Resource-Management-image61.png)

<span data-ttu-id="8bbe6-115">สมาชิกในทีมทั่วไปจะถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อซึ่งจองแบบตายตัวในทีมโครงการและการมอบหมายงานในหมายกำหนดการให้บริการของโครงการ</span><span class="sxs-lookup"><span data-stu-id="8bbe6-115">The generic team member is replaced with the hard-booked named resource on the project team and task assignments in the project schedule.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]