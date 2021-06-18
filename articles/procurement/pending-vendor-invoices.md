---
title: ซื้อวัสดุที่ไม่เก็บในคลังโดยใช้ใบแจ้งหนี้ของผู้จัดจำหน่ายที่รอดำเนินการ
description: หัวข้อนี้อธิบายวิธีการบันทึกใบแจ้งหนี้ของผู้จัดจำหน่ายที่รอดำเนินการ
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993839"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="e08b5-103">ซื้อวัสดุที่ไม่เก็บในคลังโดยใช้ใบแจ้งหนี้ของผู้จัดจำหน่ายที่รอดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="e08b5-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="e08b5-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="e08b5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e08b5-105">เนื่องจากบริษัทจัดหาวัสดุที่ไม่เก็บในคลังสำหรับโครงการ สามารถบันทึกต้นทุนได้ทันทีกับโครงการ</span><span class="sxs-lookup"><span data-stu-id="e08b5-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="e08b5-106">ตัวอย่างเช่น Contoso Robotics US กำลังดำเนินโครงการต่ออายุอุปกรณ์ และต้องการสิทธิ์การใช้งานซอฟต์แวร์</span><span class="sxs-lookup"><span data-stu-id="e08b5-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="e08b5-107">สิทธิ์การใช้งานเหล่านี้ถูกจัดหาจากผู้จัดจำหน่ายบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="e08b5-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="e08b5-108">โดยใช้ Dynamics 365 Finance เสมียนบัญชีเจ้าหนี้จะบันทึกเอกสารใบแจ้งหนี้ของผู้จัดจำหน่ายที่รอดำเนินการและระบุต้นทุนสิทธิ์การใช้งานโดยตรงกับโครงการต่ออายุอุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="e08b5-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="e08b5-109">ก่อนที่คุณจะใช้ฟังก์ชันที่อธิบายไว้ในหัวข้อนี้ โปรดตรวจสอบและใช้การตั้งค่าคอนฟิกที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="e08b5-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="e08b5-110">สำหรับข้อมูลเพิ่มเติม โปรดดู [เปิดใช้งานวัสดุที่ไม่เก็บในคลังและใบแจ้งหนี้ของผู้จัดจำหน่ายที่รอดำเนินการ](configure-materials-nonstocked.md)</span><span class="sxs-lookup"><span data-stu-id="e08b5-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="e08b5-111">ลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่ายที่รอดำเนินการที่เกี่ยวข้องกับโครงการ</span><span class="sxs-lookup"><span data-stu-id="e08b5-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="e08b5-112">สามารถบันทึกใบแจ้งหนี้ของผู้จัดจำหน่ายที่รอดำเนินการได้ในหน้า **ใบแจ้งหนี้ของผู้จัดจำหน่ายที่รอดำเนินการ** (**บัญชีเจ้าหนี้** > **ใบแจ้งหนี้** > **ใบแจ้งหนี้ของผู้จัดจำหน่ายที่รอดำเนินการ**)</span><span class="sxs-lookup"><span data-stu-id="e08b5-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="e08b5-113">ทำตามขั้นตอนต่อไปนี้เพื่อลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่ายที่รอดำเนินการที่เกี่ยวข้องกับโครงการ:</span><span class="sxs-lookup"><span data-stu-id="e08b5-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="e08b5-114">ไปที่ **บัญชีเจ้าหนี้** > **ใบแจ้งหนี้** และเลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="e08b5-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="e08b5-115">ในฟิลด์ **บัญชีใบแจ้งหนี้** เลือกผู้จัดจำหน่าย และในฟิลด์ **หมายเลข** ป้อนการระบุใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e08b5-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="e08b5-116">เพิ่มบรรทัดในใบแจ้งหนี้ของผู้จัดจำหน่าย และในฟิลด์ **หมายเลขสินค้า** เลือกสินค้าที่ไม่เก็บในคลังที่ซื้อจากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e08b5-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="e08b5-117">ไม่สามารถบันทึกรายการใบแจ้งหนี้ของผู้จัดจำหน่ายที่ยึดตามประเภทการจัดซื้อเทียบกับโครงการได้</span><span class="sxs-lookup"><span data-stu-id="e08b5-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="e08b5-118">เพิ่มปริมาณที่ซื้อ</span><span class="sxs-lookup"><span data-stu-id="e08b5-118">Add the quantity purchased.</span></span> <span data-ttu-id="e08b5-119">ระบบจะเติมราคาต่อหน่วยตามการตั้งค่าคอนฟิกราคาสินค้าที่ไม่เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="e08b5-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="e08b5-120">ตรวจสอบจำนวนเงินทั้งหมดและรายละเอียดอื่นๆ ที่จำเป็นในรายการ</span><span class="sxs-lookup"><span data-stu-id="e08b5-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="e08b5-121">ในรายละเอียดรายการ บนแท็บ **โครงการ** เลือก ID ของโครงการที่จะมีการบันทึกรายการนี้</span><span class="sxs-lookup"><span data-stu-id="e08b5-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="e08b5-122">อีกทางหนึ่งคือ เลือกหมายเลขกิจกรรม และอัปเดตประเภทโครงการและคุณสมบัติรายการ</span><span class="sxs-lookup"><span data-stu-id="e08b5-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="e08b5-123">ลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่ายที่รอดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="e08b5-123">Post pending vendor invoice.</span></span> <span data-ttu-id="e08b5-124">เมื่อมีการลงรายการบัญชีใบแจ้งหนี้ ระบบจะบันทึก:</span><span class="sxs-lookup"><span data-stu-id="e08b5-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="e08b5-125">จำนวนยอดดุลของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e08b5-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="e08b5-126">จำนวนเงินภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="e08b5-126">The sales tax amount.</span></span>
    - <span data-ttu-id="e08b5-127">ต้นทุนเทียบกับโครงการจะถูกบันทึกลงในบัญชีการรวมการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="e08b5-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="e08b5-128">ธุรกรรมจริงของโครงการใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="e08b5-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="e08b5-129">ธุรกรรมนี้ได้รับการประมวลผลเพิ่มเติมโดยใช้ [สมุดรายวันการรวมของ Project Operations](../project-accounting/project-operations-integration-journal.md)</span><span class="sxs-lookup"><span data-stu-id="e08b5-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="e08b5-130">การลงรายการบัญชีสมุดรายวันนี้จะย้ายยอดเงินจากบัญชีการรวมการจัดซื้อไปยังบัญชีต้นทุนโครงการ</span><span class="sxs-lookup"><span data-stu-id="e08b5-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
