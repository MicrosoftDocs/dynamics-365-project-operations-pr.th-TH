---
title: ปรับใช้งาน Project Operations - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการติดตั้งการปรับใช้งาน Project Operations Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0633585fcef91d9218d6140764addb7cf96ab31d
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175689"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="437f5-103">ปรับใช้งาน Project Operations - Lite</span><span class="sxs-lookup"><span data-stu-id="437f5-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="437f5-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="437f5-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="437f5-105">Project Operations รองรับรูปแบบการปรับใช้งานหลายแบบ</span><span class="sxs-lookup"><span data-stu-id="437f5-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="437f5-106">หากต้องการกำหนดรูปแบบการปรับใช้งานที่ดีที่สุด โปรดดู [ชนิดการปรับใช้งาน](determine-deployment-type.md)</span><span class="sxs-lookup"><span data-stu-id="437f5-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="437f5-107">การปรับใช้งานนี้ การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราวส่งผลในการปรับใช้งานเฉพาะ **Common Data Service ของ Project Operations**</span><span class="sxs-lookup"><span data-stu-id="437f5-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="437f5-108">ติดตั้ง Project Operations ในสภาพแวดล้อม CDS ใหม่</span><span class="sxs-lookup"><span data-stu-id="437f5-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="437f5-109">ติดตั้งในสภาพแวดล้อม CDS ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="437f5-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="437f5-110">ติดตั้ง Project Operations ในสภาพแวดล้อม CDS ใหม่</span><span class="sxs-lookup"><span data-stu-id="437f5-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="437f5-111">ในฐานะ [ผู้ดูแลระบบส่วนกลางหรือผู้ดูแลระบบ Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) ที่มีสิทธิ์การใช้งาน Project Operations ให้สร้างสภาพแวดล้อม CDS ใหม่ใน [ศูนย์จัดการ Power Platform](https://admin.powerplatform.com)</span><span class="sxs-lookup"><span data-stu-id="437f5-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="437f5-112">ทำให้แน่ใจว่า **ฐานข้อมูล CDS** และ **แอป Dynamics 365** ถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="437f5-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="437f5-113">สำหรับข้อมูลเพิ่มเติม ดูที่ [สร้างและจัดการสภาพแวดล้อมในศูนย์จัดการ Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center)</span><span class="sxs-lookup"><span data-stu-id="437f5-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="437f5-114">เลือก **Microsoft Dynamics 365 Project Operations** จากรายการปรับใช้งานแอป Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="437f5-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="437f5-115">ติดตั้ง Project Operations ในสภาพแวดล้อม CDS ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="437f5-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="437f5-116">ในฐานะ [ผู้ดูแลระบบส่วนกลางหรือผู้ดูแลระบบ Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) ที่มีสิทธิ์การใช้งาน Project Operations ให้ค้นหาสภาพแวดล้อมใน [ศูนย์จัดการ Power Platform](https://admin.powerplatform.com) ที่คุณต้องการติดตั้ง Project Operations</span><span class="sxs-lookup"><span data-stu-id="437f5-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="437f5-117">ติดตั้ง **Microsoft Dynamics 365 Project Operations** จากรายการปรับใช้งานแอป Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="437f5-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="437f5-118">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [จัดการแอป Dynamics Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps)</span><span class="sxs-lookup"><span data-stu-id="437f5-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


