---
title: นำเข้าและรักษาธุรกรรมบัตรเครดิต
description: หัวข้อนี้อธิบายวิธีการนำเข้าและรักษาธุรกรรมบัตรเครดิตที่เกี่ยวข้องกับค่าใช้จ่าย ธุรกรรมเหล่านี้สามารถตั้งค่าเพื่อให้นำเข้าโดยอัตโนมัติตามกำหนดเวลาที่เกิดขึ้นประจำหรือสามารถนำเข้าด้วยตนเองได้ตามต้องการ
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: df5c6bce8a534f4f8b1872e2bd5cc8a58ef11189
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271601"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="456c0-104">นำเข้าและรักษาธุรกรรมบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="456c0-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="456c0-105">คุณสามารถตั้งค่าธุรกรรมบัตรเครดิตที่เกี่ยวข้องกับค่าใช้จ่ายเพื่อให้มีการนำเข้าโดยอัตโนมัติตามกำหนดการที่เป็นกิจวัตร</span><span class="sxs-lookup"><span data-stu-id="456c0-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="456c0-106">หรือสามารถนำเข้าธุรกรรมได้ด้วยตนเองตามที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="456c0-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="456c0-107">ธุรกรรมบัตรเครดิตมีการนำเข้าผ่านเอนทิตีข้อมูลธุรกรรมบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="456c0-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="456c0-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับเอนทิตีข้อมูล ดูที่ [เอนทิตีข้อมูล](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities)</span><span class="sxs-lookup"><span data-stu-id="456c0-108">For more information about data entities, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="456c0-109">นำเข้าธุรกรรมบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="456c0-109">Import credit card transactions</span></span>

1. <span data-ttu-id="456c0-110">บนเพจ **ธุรกรรมบัตรเครดิต** ให้เลือก **นำเข้าธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="456c0-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="456c0-111">หากคุณเปิดการจัดการข้อมูลเป็นครั้งแรก ระบบต้องปรับปรุงรายการเอนทิตีข้อมูลก่อนจึงจะดำเนินการต่อได้</span><span class="sxs-lookup"><span data-stu-id="456c0-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="456c0-112">ในฟิลด์ **ชื่อ** ให้ป้อนคำอธิบายเฉพาะของงานนำเข้า</span><span class="sxs-lookup"><span data-stu-id="456c0-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="456c0-113">ในฟิลด์ **รูปแบบข้อมูลต้นทาง** เลือกรูปแบบของไฟล์ที่มีธุรกรรมบัตรเครดิตที่จะนำเข้า</span><span class="sxs-lookup"><span data-stu-id="456c0-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="456c0-114">เลือก **อัปโหลด** จากนั้นค้นหาและเลือกไฟล์ที่จะนำเข้า</span><span class="sxs-lookup"><span data-stu-id="456c0-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="456c0-115">หลังจากอัปโหลดไฟล์แล้ว ให้ตรวจสอบการแม็ปของไฟล์ธุรกรรมบัตรเครดิตและคอลัมน์ของเอนทิตีข้อมูลธุรกรรมบัตรเครดิตโดยการเลือกลิงก์ **ดูแผนผัง** บนไทล์</span><span class="sxs-lookup"><span data-stu-id="456c0-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="456c0-116">หากมีข้อผิดพลาดในการแม็ป หรือหากคุณต้องเปลี่ยนการแม็ป ให้ทำการเปลี่ยนแปลงการแม็ปจากแท็บ **การจัดรูปแบบการแสดงการแม็ป** หรือแท็บ **รายละเอียดการแม็ป**</span><span class="sxs-lookup"><span data-stu-id="456c0-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="456c0-117">ในการทำธุรกรรมบัตรเครดิตให้เป็นแบบอัตโนมัติ ให้เลือก **สร้างงานข้อมูลที่เป็นกิจวัตร**</span><span class="sxs-lookup"><span data-stu-id="456c0-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="456c0-118">จากนั้นคุณสามารถตั้งค่าการเกิดขึ้นประจำที่กำหนดความถี่ในการนำเข้าธุรกรรมบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="456c0-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="456c0-119">เมื่อคุณทำเสร็จแล้ว ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="456c0-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="456c0-120">หากต้องการนำเข้าไฟล์ที่เลือกตอนนี้ ให้เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="456c0-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="456c0-121">หากเกิดข้อผิดพลาดระหว่างการนำเข้า คุณสามารถดูบันทึกการดำเนินการหรือข้อมูลการจัดเตรียมเพื่อดูข้อผิดพลาดที่คุณต้องแก้ไขเพื่อช่วยรับประกันว่าการนำเข้าจะประสบความสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="456c0-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="456c0-122">หากคุณต้องนำเข้ารูปแบบไฟล์มากกว่าหนึ่งรูปแบบ คุณต้องสร้างงานนำเข้าแยกกันสำหรับรูปแบบแต่ละชนิด</span><span class="sxs-lookup"><span data-stu-id="456c0-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="456c0-123">กำหนดธุรกรรมบัตรเครดิตใหม่สำหรับพนักงานที่ถูกเลิกจ้าง</span><span class="sxs-lookup"><span data-stu-id="456c0-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="456c0-124">หลังจากเรกคอร์ดพนักงานสิ้นสุดลง บัญชี Active Directory Domain Services (AD DS) ของพนักงานจะถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="456c0-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="456c0-125">อย่างไรก็ตาม อาจมีธุรกรรมบัตรเครดิตที่ยังคงต้องใช้ค่าใช้จ่ายและชำระเงินคืน</span><span class="sxs-lookup"><span data-stu-id="456c0-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="456c0-126">จากเพจ **ธุรกรรมบัตรเครดิต** คุณสามารถกำหนดพนักงานใหม่สำหรับธุรกรรมบัตรเครดิตใดๆ ที่พนักงานที่เกี่ยวข้องได้รับการเลิกจ้าง</span><span class="sxs-lookup"><span data-stu-id="456c0-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="456c0-127">เลือกธุรกรรมบัตรเครดิตอย่างน้อยหนึ่งรายการ จากนั้นเลือก **กำหนดธุรกรรมใหม่**</span><span class="sxs-lookup"><span data-stu-id="456c0-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="456c0-128">จากนั้นคุณสามารถเลือกพนักงานคนอื่นเพื่อกำหนดธุรกรรมบัตรเครดิตให้ได้</span><span class="sxs-lookup"><span data-stu-id="456c0-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="456c0-129">หลังจากกำหนดธุรกรรมบัตรเครดิตใหม่แล้ว ธุรกรรมสามารถถูกเลือกสำหรับรายงานค่าใช้จ่ายและชำระเงินผ่านกระบวนการปกติสำหรับการชำระเงินคืนในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="456c0-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]