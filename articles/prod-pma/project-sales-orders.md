---
title: ใบสั่งขายของโครงการสำหรับโครงการเวลาและวัสดุ
description: หัวข้อนี้อธิบายวิธีสร้างใบสั่งขายตามโครงการสำหรับโครงการเวลาและวัสดุ
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085917"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="c1443-103">ใบสั่งขายของโครงการสำหรับโครงการเวลาและวัสดุ</span><span class="sxs-lookup"><span data-stu-id="c1443-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c1443-104">หัวข้อนี้อธิบายวิธีสร้างใบสั่งขายสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="c1443-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="c1443-105">สามารถสร้างใบสั่งขายสำหรับโครงการชนิด **เวลาและวัสดุ** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c1443-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="c1443-106">หากโครงการเวลาและวัสดุมีแหล่งเงินทุนหลายแห่งในสัญญาโครงการ คุณต้องเปิดใช้งานพารามิเตอร์ **อนุญาตใบสั่งขายสำหรับโครงการที่มีแหล่งเงินทุนหลายแห่ง** บนหน้า **พารามิเตอร์การจัดการโครงการและการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="c1443-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="c1443-107">การสนับสนุนสำหรับใบสั่งขายของโครงการที่มีแหล่งเงินทุนหลายแห่ง พร้อมใช้งานตั้งแต่รุ่นแอปพลิเคชัน 10.0.2 ขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="c1443-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="c1443-108">พารามิเตอร์เพื่อเปิดใช้งานการสนับสนุนสำหรับใบสั่งขายของโครงการที่มีแหล่งเงินทุนหลายแห่ง จะถูกลบออกในเวฟรุ่นเมษายน 2020 หลังจากนั้นฟังก์ชันจะถูกเปิดใช้งานเสมอ</span><span class="sxs-lookup"><span data-stu-id="c1443-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="c1443-109">คุณสามารถสร้างใบสั่งขายตามโครงการได้สองวิธี:</span><span class="sxs-lookup"><span data-stu-id="c1443-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="c1443-110">ไปที่ตัวโครงการเอง</span><span class="sxs-lookup"><span data-stu-id="c1443-110">Go to the project itself.</span></span> <span data-ttu-id="c1443-111">ในบานหน้าต่างการดำเนินการ เลือก **จัดการ > งานของสินค้า > ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="c1443-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="c1443-112">ข้อมูลโครงการจะเริ่มต้นเป็นใบสั่งขายจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="c1443-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="c1443-113">หากสัญญาโครงการมีแหล่งเงินทุนมากกว่าหนึ่งแห่ง คุณจะต้องเลือกแหล่งเงินทุนเพื่อตั้งค่าลูกค้าสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="c1443-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="c1443-114">หากมีแหล่งเงินทุนเพียงแห่งเดียวสำหรับโครงการ ลูกค้าจะได้รับการตั้งค่าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c1443-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="c1443-115">ไปที่หน้ารายการ **ใบสั่งขายทั้งหมด** และสร้างใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="c1443-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="c1443-116">คุณจะต้องเลือกโครงการสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="c1443-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="c1443-117">หลังจากเลือกโครงการแล้ว ลูกค้าจะได้รับการตั้งค่าจากแหล่งเงินทุน หรือคุณจะต้องเลือกแหล่งเงินทุน หากสัญญาโครงการมีแหล่งเงินทุนหลายแห่ง</span><span class="sxs-lookup"><span data-stu-id="c1443-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

