---
title: ส่งคำขอทรัพยากร
description: คุณสามารถส่งคำขอทรัพยากรที่สร้างขึ้นเป็นคำขอทรัพยากรได้ จากนั้นคำขอจะถูกส่งไปยังผู้จัดการทรัพยากรเพื่อทำตามคำขอ
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085826"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="3ab0c-104">ส่งคำขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="3ab0c-104">Submit a resource request</span></span>

<span data-ttu-id="3ab0c-105">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="3ab0c-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3ab0c-106">คุณสามารถส่งคำขอทรัพยากรที่สร้างขึ้นเป็นคำขอทรัพยากรได้</span><span class="sxs-lookup"><span data-stu-id="3ab0c-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="3ab0c-107">จากนั้นคำขอจะถูกส่งไปยังผู้จัดการทรัพยากรเพื่อทำตามคำขอ</span><span class="sxs-lookup"><span data-stu-id="3ab0c-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="3ab0c-108">ใน Dynamics 365 Project Operations บนเพจ **โครงการ** เลือกแท็บ **ทีม** เพื่อดูรายการทรัพยากรที่สามารถจองได้</span><span class="sxs-lookup"><span data-stu-id="3ab0c-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="3ab0c-109">เลือกทรัพยากรทั่วไปที่มีความจำเป็นจากในรายการ จากนั้นคลิก **ส่งคำขอ**</span><span class="sxs-lookup"><span data-stu-id="3ab0c-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="3ab0c-110">สถานะของคำขอของสมาชิกทีมทั่วไปจะถูกเปลี่ยนเป็น **ส่งแล้ว**</span><span class="sxs-lookup"><span data-stu-id="3ab0c-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="3ab0c-111">หลังจากคำขอได้รับการทำตาม ทรัพยากรทั่วไปจะถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อ หากผู้จัดการทรัพยากรทำตามคำขอด้วยการจองของทรัพยากรที่ระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="3ab0c-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="3ab0c-112">มิฉะนั้น หากผู้จัดการทรัพยากรได้เสนอทรัพยากรที่ระบุชื่อ ทรัพยากรทั่วไปจะยังคงอยู่ในทีมและสถานะคำขอจะถูกเปลี่ยนเป็น **ต้องมีการตรวจทาน**</span><span class="sxs-lookup"><span data-stu-id="3ab0c-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
