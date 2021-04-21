---
title: ปิดการใช้งานรายการราคา
description: หัวข้อนี้จะอธิบายวิธีการปิดใช้การงานหรือเอารายการราคาที่ไม่ได้ใช้งานหรือของเก่าออก
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701980"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="3f124-103">ปิดการใช้งานรายการราคา</span><span class="sxs-lookup"><span data-stu-id="3f124-103">Deactivate price lists</span></span> 

<span data-ttu-id="3f124-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="3f124-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3f124-105">การเอารายการราคาของเก่าหรือที่ไม่ได้ใช้งานออกจาก Dynamics 365 Project Operations มีสองขั้นตอนที่คุณต้องทำ</span><span class="sxs-lookup"><span data-stu-id="3f124-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="3f124-106">ลบหรือเอารายการราคาออกจากเพจเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="3f124-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="3f124-107">ปิดการใช้งานหรือลบรายการราคาออกจากรายการราคาที่ใช้งานอยู่ในเพจ **รายการราคา**</span><span class="sxs-lookup"><span data-stu-id="3f124-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="3f124-108">คุณต้องทำทั้งสองขั้นตอนเพื่อเอารายการราคาออกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3f124-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="3f124-109">การดำเนินการเฉพาะขั้นตอนที่ 2 ซึ่งเป็นการลบหรือปิดการใช้งานรายการราคาโดยตรงจากมุมมองรายการราคาที่ใช้งานอยู่นั้นไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="3f124-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="3f124-110">นอกจากนี้ คุณต้องลบการเชื่อมโยงของรายการราคานี้ออกจากตำแหน่งทั้งหมดที่กล่าวถึงในขั้นตอนที่ 1</span><span class="sxs-lookup"><span data-stu-id="3f124-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="3f124-111">ลบรายการราคาออกจากเพจเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="3f124-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="3f124-112">หากต้องการลบรายการราคาออกจาก Project Operations ให้ไปที่เพจต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3f124-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="3f124-113">เพจ **พารามิเตอร์โครงการ** > แท็บ **รายการราคา**</span><span class="sxs-lookup"><span data-stu-id="3f124-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="3f124-114">เพจ **หน่วยองค์กร** > ตาราง **รายการราคา**</span><span class="sxs-lookup"><span data-stu-id="3f124-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="3f124-115">เพจ **ลูกค้าองค์กร** ตาราง > **รายการราคาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="3f124-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="3f124-116">เพจ **ใบเสนอราคาโครงการ** > ตาราง **รายการราคาโครงการ**: ใช้กับใบเสนอราคาโครงการที่ใช้งานอยู่ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3f124-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="3f124-117">เพจ **สัญญาโครงการ** > ตาราง **รายการราคาโครงการ**: ใช้กับสัญญาโครงการที่ใช้งานอยู่ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3f124-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="3f124-118">สำหรับแต่ละเพจ คุณต้องเลือกรายการราคาที่คุณต้องการลบ จากนั้นเลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="3f124-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="3f124-119">ลบหรือปิดการใช้งานรายการราคาออกจากเพจรายการราคา</span><span class="sxs-lookup"><span data-stu-id="3f124-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="3f124-120">หากต้องการลบรายการราคาออกจากรายการราคาที่ใช้งานอยู่ ให้ไปที่ **การขาย** > **ลูกค้า** > **รายการราคา**</span><span class="sxs-lookup"><span data-stu-id="3f124-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="3f124-121">เลือกรายการราคาที่คุณต้องการลบ จากนั้นเลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="3f124-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="3f124-122">หากรายการราคาอ้างอิงกับธุรกรรมที่มีอยู่ คุณจะไม่สามารถลบออกได้</span><span class="sxs-lookup"><span data-stu-id="3f124-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="3f124-123">หากเกิดกรณีนี้ คุณสามารถปิดการใช้งานรายการราคาเพื่อไม่ให้ปรากฏในมุมมองใดๆ</span><span class="sxs-lookup"><span data-stu-id="3f124-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="3f124-124">การปิดการใช้งานรายการราคา ให้เลือกรายการราคาอีกครั้ง จากนั้นเลือก **ปิดการใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="3f124-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
