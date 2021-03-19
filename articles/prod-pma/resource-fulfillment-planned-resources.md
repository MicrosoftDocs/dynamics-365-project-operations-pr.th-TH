---
title: การเติมเต็มทรัพยากรสำหรับทรัพยากรที่วางแผนไว้
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับทรัพยากรที่วางแผนสำหรับโครงการ
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4200d74a18c706a492ebd0e5383d5957ce6ab6c8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288807"
---
# <a name="resource-fulfillment-for-planned-resources"></a><span data-ttu-id="60ed3-103">การเติมเต็มทรัพยากรสำหรับทรัพยากรที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="60ed3-103">Resource fulfillment for planned resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60ed3-104">ผู้จัดการโครงการสามารถวางแผนบทบาททรัพยากรที่จำเป็นสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="60ed3-104">A project manager can plan required resource roles for a project.</span></span> <span data-ttu-id="60ed3-105">Resource Manager จะเห็นทรัพยากรที่วางแผนไว้เหล่านี้ตามคำขอในหน้า **การเติมเต็มทรัพยากร** และสามารถมอบหมายทรัพยากรจริงได้</span><span class="sxs-lookup"><span data-stu-id="60ed3-105">The resource manager will see these planned resources as requests on the **Resource fulfillment** page and can assign actual resources.</span></span>

1. <span data-ttu-id="60ed3-106">บนหน้า **โครงการทั้งหมด** เลือกโครงการ **การอัพเกรด XYZ ระยะที่ 2**</span><span class="sxs-lookup"><span data-stu-id="60ed3-106">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="60ed3-107">เลือก **โครงการ** และจากนั้น เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="60ed3-107">Select **Project**, and then select **Edit**.</span></span>
3. <span data-ttu-id="60ed3-108">บนแท็บ **กลุ่มคนของโครงการและการจัดกำหนดการ** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="60ed3-108">On the **Project team and scheduling** tab, select **Add**.</span></span>
4. <span data-ttu-id="60ed3-109">ในกล่องโต้ตอบ **เพิ่มบทบาท** เลือกบทบาท **นักพัฒนาซอฟต์แวร์**</span><span class="sxs-lookup"><span data-stu-id="60ed3-109">In the **Add roles** dialog box, select the **Software developer** role.</span></span>
5. <span data-ttu-id="60ed3-110">เลือก **สร้าง** แล้วจากนั้น ปิดหน้าโครงการ</span><span class="sxs-lookup"><span data-stu-id="60ed3-110">Select **Create**, and then close the project page.</span></span>
6. <span data-ttu-id="60ed3-111">บนหน้า **การเติมเต็มทรัพยากร** ให้เลือก **นักพัฒนาซอฟต์แวร์ 1** สำหรับโครงการ **โครงการอัพเกรด XYZ ระยะที่ 2**</span><span class="sxs-lookup"><span data-stu-id="60ed3-111">On the **Resource fulfillment** page, select **Software developer 1** for the **XYZ Upgrade project Phase 2** project.</span></span>
7. <span data-ttu-id="60ed3-112">เลือกผู้ปฏิบัติงาน และจากนั้น เลือก **มอบหมาย**</span><span class="sxs-lookup"><span data-stu-id="60ed3-112">Select a worker, and then select **Assign**.</span></span>
8. <span data-ttu-id="60ed3-113">ตรวจสอบว่าบรรทัดสำหรับ **นักพัฒนาซอฟต์แวร์ 1** ถูกลบออกสำหรับโครงการ **โครงการอัพเกรด XYZ ระยะที่ 2**</span><span class="sxs-lookup"><span data-stu-id="60ed3-113">Verify that the line for **Software developer 1** has been removed for the **XYZ Upgrade project Phase 2** project.</span></span>
9. <span data-ttu-id="60ed3-114">บนแท็บ **กลุ่มคนในโครงการและการจัดกำหนดการ** สำหรับ **การอัพเกรด XYZ ระยะที่ 2** ตรวจสอบว่ามีการเพิ่มผู้ปฏิบัติงานที่คุณเลือกในขั้นตอนก่อนหน้าเป็น **นักพัฒนาซอฟต์แวร์**</span><span class="sxs-lookup"><span data-stu-id="60ed3-114">On the **Project team and scheduling** tab, for the **XYZ Upgrade Phase 2** project, verify that the worker that you selected in the previous step has been added as **Software developer**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]