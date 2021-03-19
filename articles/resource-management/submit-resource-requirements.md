---
title: ส่งคำขอทรัพยากร
description: คุณสามารถส่งคำขอทรัพยากรที่สร้างขึ้นเป็นคำขอทรัพยากรได้ จากนั้นคำขอจะถูกส่งไปยังผู้จัดการทรัพยากรเพื่อทำตามคำขอ
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279161"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="35f9d-104">ส่งคำขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="35f9d-104">Submit a resource request</span></span>

<span data-ttu-id="35f9d-105">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="35f9d-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="35f9d-106">คุณสามารถส่งคำขอทรัพยากรที่สร้างขึ้นเป็นคำขอทรัพยากรได้</span><span class="sxs-lookup"><span data-stu-id="35f9d-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="35f9d-107">จากนั้นคำขอจะถูกส่งไปยังผู้จัดการทรัพยากรเพื่อทำตามคำขอ</span><span class="sxs-lookup"><span data-stu-id="35f9d-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="35f9d-108">ใน Dynamics 365 Project Operations บนเพจ **โครงการ** ให้เลือกแท็บ **ทีม** เพื่อดูรายการทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="35f9d-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="35f9d-109">เลือกทรัพยากรทั่วไปที่มีความจำเป็นจากในรายการ จากนั้นคลิก **ส่งคำขอ**</span><span class="sxs-lookup"><span data-stu-id="35f9d-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="35f9d-110">สถานะของคำขอของสมาชิกทีมทั่วไปจะถูกเปลี่ยนเป็น **ส่งแล้ว**</span><span class="sxs-lookup"><span data-stu-id="35f9d-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="35f9d-111">หลังจากคำขอได้รับการทำตาม ทรัพยากรทั่วไปจะถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อ หากผู้จัดการทรัพยากรทำตามคำขอด้วยการจองของทรัพยากรที่ระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="35f9d-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="35f9d-112">มิฉะนั้น หากผู้จัดการทรัพยากรได้เสนอทรัพยากรที่ระบุชื่อ ทรัพยากรทั่วไปจะยังคงอยู่ในทีมและสถานะคำขอจะถูกเปลี่ยนเป็น **ต้องมีการตรวจทาน**</span><span class="sxs-lookup"><span data-stu-id="35f9d-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]