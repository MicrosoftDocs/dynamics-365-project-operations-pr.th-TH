---
title: แก้ไขราคาต้นทุนในประมาณการและข้อมูลจริง - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการแก้ไขราคาต้นทุนสำหรับการประมาณการและตามจริง
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2afaa2231f4044dbcbfa24b91aec39289275a91
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764617"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a><span data-ttu-id="b5b52-103">แก้ไขราคาต้นทุนในประมาณการและข้อมูลจริง - Lite</span><span class="sxs-lookup"><span data-stu-id="b5b52-103">Resolve cost prices on estimates and actuals - lite</span></span>

<span data-ttu-id="b5b52-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="b5b52-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b5b52-105">ในการแก้ไขราคาต้นทุนและราคาตลาดต้นทุนสำหรับการประมาณการและตามจริง ระบบจะใช้ข้อมูลในฟิลด์ **วันที่** **สกุลเงิน** และ **หน่วยที่ทำสัญญา** ของโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="b5b52-105">To resolve cost prices and the cost price list for estimates and actuals, the system uses the information in the **Date**, **Currency**, and **Contracting Unit** fields of the related project.</span></span> <span data-ttu-id="b5b52-106">หลังจากแก้ไขราคาตลาดต้นทุนแล้ว แอปพลิเคชันจะแก้ไขอัตราต้นทุน</span><span class="sxs-lookup"><span data-stu-id="b5b52-106">After the cost price list is resolved, the application resolves the cost rate.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="b5b52-107">การแก้ไขอัตราต้นทุนตามจริงและรายการประมาณการสำหรับเวลา</span><span class="sxs-lookup"><span data-stu-id="b5b52-107">Resolving cost rates on actual and estimate lines for Time</span></span>

<span data-ttu-id="b5b52-108">บรรทัดประมาณการสำหรับเวลาอ้างถึงใบเสนอราคาและรายละเอียดการให้บริการตามสัญญาสำหรับการกำหนดเวลาและทรัพยากรในโครงการ</span><span class="sxs-lookup"><span data-stu-id="b5b52-108">Estimate lines for Time refer to the quote and contract line details for time and resource assignments on a project.</span></span>

<span data-ttu-id="b5b52-109">หลังจากแก้ไขราคาต้นทุนแล้ว ฟิลด์ **บทบาท** และฟิลด์ **หน่วยการจัดเตรียมทรัพยากร** ในบรรทัดประมาณการสำหรับเวลา จะถูกจับคู่กับรายการราคาตามบทบาทในราคาตลาด</span><span class="sxs-lookup"><span data-stu-id="b5b52-109">After a cost price list is resolved, the **Role** and **Resourcing Unit** fields on the estimate line for Time are matched against the role price lines in the price list.</span></span> <span data-ttu-id="b5b52-110">การจับคู่นี้จะถือว่าคุณใช้มิติการกำหนดราคามาตรฐานสำหรับต้นทุนแรงงาน</span><span class="sxs-lookup"><span data-stu-id="b5b52-110">This match assumes that you're using the standard pricing dimensions for labor cost.</span></span> <span data-ttu-id="b5b52-111">หากคุณกำหนดค่าระบบให้ตรงกับฟิลด์แทนหรือนอกเหนือจาก **บทบาท** และ **หน่วยจัดหาทรัพยากร** จะใช้ชุดค่าผสมที่แตกต่างกันเพื่อดึงบรรทัดราคาตามบทบาทที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="b5b52-111">If you configured the system to match fields instead of, or in addition to **Role** and **Resourcing Unit**, then a different combination will be used to retrieve a matching role price line.</span></span> <span data-ttu-id="b5b52-112">หากแอปพลิเคชันพบบรรทัดราคาตามบทบาทที่มีอัตราต้นทุนสำหรับการรวม **บทบาท** และ **หน่วยจัดหาทรัพยากร** นั่นคืออัตราต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b5b52-112">If the application finds a role price line that has a cost rate for the **Role** and **Resourcing Unit** combination, that is the default cost rate.</span></span> <span data-ttu-id="b5b52-113">หากแอปพลิเคชันไม่สามารถจับคู่ค่า **บทบาท** และ **หน่วยจัดหาทรัพยากร** จะมีการดึงข้อมูลบรรทัดราคาตามบทบาทด้วยบทบาทที่ตรงกัน แต่เป็นค่าว่างของ **หน่วยจัดหาทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="b5b52-113">If the application can't match the **Role** and **Resourcing Unit** values, then it retrieves role price lines with a matching role, but null values of the **Resourcing Unit**.</span></span> <span data-ttu-id="b5b52-114">หลังจากมีเรกคอร์ดราคาตามบทบาทที่ตรงกันแล้ว อัตราต้นทุนจะเริ่มต้นจากเรกคอร์ดนั้น</span><span class="sxs-lookup"><span data-stu-id="b5b52-114">After it has a matching role price record, the cost rate defaults from that record.</span></span> 

> [!NOTE]
> <span data-ttu-id="b5b52-115">หากคุณกำหนดค่าลำดับความสำคัญอื่นของ **บทบาท** และ **หน่วยจัดหาทรัพยากร** หรือหากคุณมีมิติข้อมูลอื่นที่มีลำดับความสำคัญสูงกว่า ลักษณะการทำงานนี้ก็จะเปลี่ยนไปตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="b5b52-115">If you configure a different prioritization of **Role** and **Resourcing Unit**, or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="b5b52-116">ระบบจะดึงเรกคอร์ดราคาตามบทบาทที่มีค่าที่ตรงกับค่ามิติการกำหนดราคาแต่ละค่าตามลำดับความสำคัญ โดยมีแถวที่มีค่าว่างสำหรับมิติเหล่านั้นที่มาล่าสุด</span><span class="sxs-lookup"><span data-stu-id="b5b52-116">The system retrieves role price records with values that match each of the pricing dimension values in order of priority with rows that have null values for those dimensions coming last.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="b5b52-117">การแก้ไขอัตราต้นทุนตามจริงและรายการประมาณการสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="b5b52-117">Resolving cost rates on actual and estimate lines for Expense</span></span>

<span data-ttu-id="b5b52-118">บรรทัดการประมาณการสำหรับค่าใช้จ่ายหมายถึงใบเสนอราคาและรายละเอียดการให้บริการตามสัญญาสำหรับค่าใช้จ่าย และบรรทัดการประมาณการค่าใช้จ่ายของโครงการ</span><span class="sxs-lookup"><span data-stu-id="b5b52-118">Estimate lines for Expense refer to the quote and contract line details for expenses and the expense estimate lines on a project.</span></span>

<span data-ttu-id="b5b52-119">หลังจากแก้ไขรายการราคาต้นทุนแล้ว ระบบจะใช้ชุดข้อมูลของ **ประเภท** และ **หน่วย** ในรายการประมาณการค่าใช้จ่ายที่ตรงกับรายการ **ราคาของประเภท** บนราคาตลาดที่แก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="b5b52-119">After a cost price list is resolved, the system uses a combination of the **Category** and **Unit** fields on the expense estimate line to match against the **Category Price** lines on the resolved price list.</span></span> <span data-ttu-id="b5b52-120">หากระบบพบบรรทัดราคาประเภทที่มีอัตราต้นทุนสำหรับการรวมฟิลด์ **ประเภท** และ **หน่วย** อัตราต้นทุนจะเป็นค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b5b52-120">If the system finds a category price line that has a cost rate for the **Category** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="b5b52-121">หากระบบไม่สามารถจับคู่ค่า **ประเภท** และ **หน่วย** หรือหากสามารถค้นหารายการราคาประเภทที่ตรงกัน แต่วิธีการกำหนดราคาไม่ใช่ **ราคาต่อหน่วย** อัตราต้นทุนเริ่มต้นเป็นศูนย์ (0)</span><span class="sxs-lookup"><span data-stu-id="b5b52-121">If the system can't match the **Category** and **Unit** values, or if it's able to find a matching category price line but the pricing method isn't **Price Per Unit**, the cost rate defaults to zero(0).</span></span>
