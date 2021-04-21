---
title: ตั้งค่าการรวมบัตรเครดิต
description: หัวข้อนี้อธิบายวิธีการทำงานกับธุรกรรมบัตรเครดิตที่เกี่ยวข้องกับค่าใช้จ่าย
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866706"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="3fc59-103">ตั้งค่าการรวมบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="3fc59-103">Set up credit card integration</span></span>

<span data-ttu-id="3fc59-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="3fc59-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3fc59-105">คุณสามารถตั้งค่าธุรกรรมบัตรเครดิตที่เกี่ยวข้องกับค่าใช้จ่ายเพื่อให้มีการนำเข้าโดยอัตโนมัติตามกำหนดการที่เป็นกิจวัตร</span><span class="sxs-lookup"><span data-stu-id="3fc59-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="3fc59-106">หรือสามารถนำเข้าธุรกรรมได้ด้วยตนเองตามที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="3fc59-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="3fc59-107">ธุรกรรมบัตรเครดิตมีการนำเข้าผ่านเอนทิตีข้อมูลธุรกรรมบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="3fc59-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="3fc59-108">นำเข้าธุรกรรมบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="3fc59-108">Import credit card transactions</span></span>

<span data-ttu-id="3fc59-109">การนำเข้าธุรกรรมบัตรเครดิต ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="3fc59-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="3fc59-110">บนเพจ **ธุรกรรมบัตรเครดิต** ให้เลือก **นำเข้าธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="3fc59-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="3fc59-111">หากคุณเปิดการจัดการข้อมูลเป็นครั้งแรก ระบบต้องปรับปรุงรายการเอนทิตีข้อมูลก่อนจึงจะดำเนินการต่อได้</span><span class="sxs-lookup"><span data-stu-id="3fc59-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="3fc59-112">ในฟิลด์ **ชื่อ** ให้ป้อนคำอธิบายเฉพาะสำหรับงานนำเข้า</span><span class="sxs-lookup"><span data-stu-id="3fc59-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="3fc59-113">ในฟิลด์ **รูปแบบข้อมูลต้นทาง** เลือกรูปแบบของไฟล์ที่มีธุรกรรมบัตรเครดิตที่จะนำเข้า</span><span class="sxs-lookup"><span data-stu-id="3fc59-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="3fc59-114">เลือก **อัปโหลด** จากนั้นค้นหาและเลือกไฟล์ที่จะนำเข้า</span><span class="sxs-lookup"><span data-stu-id="3fc59-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="3fc59-115">หลังจากอัปโหลดไฟล์แล้ว ให้ตรวจสอบการแม็ปของไฟล์ธุรกรรมบัตรเครดิตและคอลัมน์ของเอนทิตีข้อมูลธุรกรรมบัตรเครดิตโดยการเลือกลิงก์ **ดูแผนผัง** บนไทล์</span><span class="sxs-lookup"><span data-stu-id="3fc59-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="3fc59-116">หากมีข้อผิดพลาดในการแม็ป หรือหากคุณต้องเปลี่ยนการแม็ป ให้ทำการเปลี่ยนแปลงการแม็ปจากแท็บ **การจัดรูปแบบการแสดงการแม็ป** หรือแท็บ **รายละเอียดการแม็ป**</span><span class="sxs-lookup"><span data-stu-id="3fc59-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="3fc59-117">ในการทำธุรกรรมบัตรเครดิตให้เป็นแบบอัตโนมัติ ให้เลือก **สร้างงานข้อมูลที่เป็นกิจวัตร**</span><span class="sxs-lookup"><span data-stu-id="3fc59-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="3fc59-118">จากนั้นคุณสามารถตั้งค่าการเกิดขึ้นประจำที่กำหนดความถี่ในการนำเข้าธุรกรรมบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="3fc59-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="3fc59-119">เมื่อคุณทำเสร็จแล้ว ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3fc59-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="3fc59-120">หากต้องการนำเข้าไฟล์ที่เลือกตอนนี้ ให้เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="3fc59-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="3fc59-121">หากเกิดข้อผิดพลาดระหว่างการนำเข้า คุณสามารถดูบันทึกการดำเนินการหรือข้อมูลการจัดเตรียมเพื่อดูข้อผิดพลาดที่คุณต้องแก้ไข เพื่อช่วยให้การนำเข้าประสบความสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="3fc59-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="3fc59-122">หากคุณต้องการนำเข้ามากกว่าหนึ่งรูปแบบไฟล์ คุณต้องสร้างงานนำเข้าแยกกันสำหรับรูปแบบแต่ละประเภท</span><span class="sxs-lookup"><span data-stu-id="3fc59-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="3fc59-123">กำหนดธุรกรรมบัตรเครดิตใหม่สำหรับพนักงานที่ถูกเลิกจ้าง</span><span class="sxs-lookup"><span data-stu-id="3fc59-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="3fc59-124">หลังจากเรกคอร์ดพนักงานสิ้นสุดลง บัญชี Active Directory Domain Services (AD DS) ของพนักงานจะถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3fc59-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="3fc59-125">อย่างไรก็ตาม อาจมีธุรกรรมบัตรเครดิตที่ยังคงต้องใช้ค่าใช้จ่ายและชำระเงินคืน</span><span class="sxs-lookup"><span data-stu-id="3fc59-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="3fc59-126">ในเพจ **ธุรกรรมบัตรเครดิต** คุณสามารถมอบหมายธุรกรรมบัตรเครดิตใดๆ ให้พนักงานได้ใหม่เมื่อพนักงานที่เกี่ยวข้องลาออกไป</span><span class="sxs-lookup"><span data-stu-id="3fc59-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="3fc59-127">เลือกธุรกรรมบัตรเครดิตอย่างน้อยหนึ่งรายการ จากนั้นเลือก **กำหนดธุรกรรมใหม่**</span><span class="sxs-lookup"><span data-stu-id="3fc59-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="3fc59-128">จากนั้นคุณสามารถเลือกพนักงานคนอื่นเพื่อกำหนดธุรกรรมบัตรเครดิตให้ได้</span><span class="sxs-lookup"><span data-stu-id="3fc59-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="3fc59-129">หลังจากกำหนดธุรกรรมบัตรเครดิตใหม่แล้ว ธุรกรรมสามารถถูกเลือกสำหรับรายงานค่าใช้จ่ายและชำระเงินผ่านกระบวนการปกติสำหรับการชำระเงินคืนในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="3fc59-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="3fc59-130">ลบธุรกรรมบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="3fc59-130">Delete credit card transactions</span></span> 

<span data-ttu-id="3fc59-131">บางครั้ง หลังจากนำเข้าธุรกรรมบัตรเครดิตแล้ว ธุรกรรมบางอย่างอาจต้องถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="3fc59-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="3fc59-132">อาจเพราะธุรกรรมซ้ำกันหรือเนื่องจากข้อมูลอาจไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="3fc59-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="3fc59-133">ผู้ดูแลระบบสามารถใช้คุณลักษณะ **"ลบธุรกรรมบัตรเครดิต"** เพื่อเลือกและลบธุรกรรมบัตรเครดิตที่ **ไม่ได้แนบ** กับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="3fc59-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="3fc59-134">ไปที่ **งานประจำงวด** > **ลบธุรกรรมบัตรเครดิต**</span><span class="sxs-lookup"><span data-stu-id="3fc59-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="3fc59-135">เลือก **กรอง** และให้ข้อมูลเพื่อระบุเรกคอร์ดที่จะรวมไว้ด้วย</span><span class="sxs-lookup"><span data-stu-id="3fc59-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="3fc59-136">เลือก **ตกลง** เพื่อลบเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="3fc59-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
