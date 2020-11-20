---
title: ตั้งค่าการรวมบัตรเครดิต
description: หัวข้อนี้อธิบายวิธีการนำเข้าและรักษาธุรกรรมบัตรเครดิตที่เกี่ยวข้องกับค่าใช้จ่าย
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
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
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120881"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="8cf28-103">ตั้งค่าการรวมบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="8cf28-103">Set up credit card integration</span></span>

<span data-ttu-id="8cf28-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ที่อิงตามทรัพยากร/ที่ไม่ได้เก็บในสต็อก การปรับใช้ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="8cf28-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8cf28-105">คุณสามารถตั้งค่าธุรกรรมบัตรเครดิตที่เกี่ยวข้องกับค่าใช้จ่ายเพื่อให้มีการนำเข้าโดยอัตโนมัติตามกำหนดการที่เป็นกิจวัตร</span><span class="sxs-lookup"><span data-stu-id="8cf28-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="8cf28-106">หรือสามารถนำเข้าธุรกรรมได้ด้วยตนเองตามที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="8cf28-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="8cf28-107">ธุรกรรมบัตรเครดิตมีการนำเข้าผ่านเอนทิตีข้อมูลธุรกรรมบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="8cf28-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="8cf28-108">นำเข้าธุรกรรมบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="8cf28-108">Import credit card transactions</span></span>

1. <span data-ttu-id="8cf28-109">บนเพจ **ธุรกรรมบัตรเครดิต** ให้เลือก **นำเข้าธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="8cf28-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="8cf28-110">หากคุณเปิดการจัดการข้อมูลเป็นครั้งแรก ระบบต้องปรับปรุงรายการเอนทิตีข้อมูลก่อนจึงจะดำเนินการต่อได้</span><span class="sxs-lookup"><span data-stu-id="8cf28-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="8cf28-111">ในฟิลด์ **ชื่อ** ให้ป้อนคำอธิบายเฉพาะของงานนำเข้า</span><span class="sxs-lookup"><span data-stu-id="8cf28-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="8cf28-112">ในฟิลด์ **รูปแบบข้อมูลต้นทาง** เลือกรูปแบบของไฟล์ที่มีธุรกรรมบัตรเครดิตที่จะนำเข้า</span><span class="sxs-lookup"><span data-stu-id="8cf28-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="8cf28-113">เลือก **อัปโหลด** จากนั้นค้นหาและเลือกไฟล์ที่จะนำเข้า</span><span class="sxs-lookup"><span data-stu-id="8cf28-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="8cf28-114">หลังจากอัปโหลดไฟล์แล้ว ให้ตรวจสอบการแม็ปของไฟล์ธุรกรรมบัตรเครดิตและคอลัมน์ของเอนทิตีข้อมูลธุรกรรมบัตรเครดิตโดยการเลือกลิงก์ **ดูแผนผัง** บนไทล์</span><span class="sxs-lookup"><span data-stu-id="8cf28-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="8cf28-115">หากมีข้อผิดพลาดในการแม็ป หรือหากคุณต้องเปลี่ยนการแม็ป ให้ทำการเปลี่ยนแปลงการแม็ปจากแท็บ **การจัดรูปแบบการแสดงการแม็ป** หรือแท็บ **รายละเอียดการแม็ป**</span><span class="sxs-lookup"><span data-stu-id="8cf28-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="8cf28-116">ในการทำธุรกรรมบัตรเครดิตให้เป็นแบบอัตโนมัติ ให้เลือก **สร้างงานข้อมูลที่เป็นกิจวัตร**</span><span class="sxs-lookup"><span data-stu-id="8cf28-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="8cf28-117">จากนั้นคุณสามารถตั้งค่าการเกิดขึ้นประจำที่กำหนดความถี่ในการนำเข้าธุรกรรมบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="8cf28-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="8cf28-118">เมื่อคุณทำเสร็จแล้ว ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8cf28-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="8cf28-119">หากต้องการนำเข้าไฟล์ที่เลือกตอนนี้ ให้เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="8cf28-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="8cf28-120">หากเกิดข้อผิดพลาดระหว่างการนำเข้า คุณสามารถดูบันทึกการดำเนินการหรือข้อมูลการจัดเตรียมเพื่อดูข้อผิดพลาดที่คุณต้องแก้ไขเพื่อช่วยรับประกันว่าการนำเข้าจะประสบความสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="8cf28-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="8cf28-121">หากคุณต้องนำเข้ารูปแบบไฟล์มากกว่าหนึ่งรูปแบบ คุณต้องสร้างงานนำเข้าแยกกันสำหรับรูปแบบแต่ละชนิด</span><span class="sxs-lookup"><span data-stu-id="8cf28-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="8cf28-122">กำหนดธุรกรรมบัตรเครดิตใหม่สำหรับพนักงานที่ถูกเลิกจ้าง</span><span class="sxs-lookup"><span data-stu-id="8cf28-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="8cf28-123">หลังจากเรกคอร์ดพนักงานสิ้นสุดลง บัญชี Active Directory Domain Services (AD DS) ของพนักงานจะถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8cf28-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="8cf28-124">อย่างไรก็ตาม อาจมีธุรกรรมบัตรเครดิตที่ยังคงต้องใช้ค่าใช้จ่ายและชำระเงินคืน</span><span class="sxs-lookup"><span data-stu-id="8cf28-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="8cf28-125">จากเพจ **ธุรกรรมบัตรเครดิต** คุณสามารถกำหนดพนักงานใหม่สำหรับธุรกรรมบัตรเครดิตใดๆ ที่พนักงานที่เกี่ยวข้องได้รับการเลิกจ้าง</span><span class="sxs-lookup"><span data-stu-id="8cf28-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="8cf28-126">เลือกธุรกรรมบัตรเครดิตอย่างน้อยหนึ่งรายการ จากนั้นเลือก **กำหนดธุรกรรมใหม่**</span><span class="sxs-lookup"><span data-stu-id="8cf28-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="8cf28-127">จากนั้นคุณสามารถเลือกพนักงานคนอื่นเพื่อกำหนดธุรกรรมบัตรเครดิตให้ได้</span><span class="sxs-lookup"><span data-stu-id="8cf28-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="8cf28-128">หลังจากกำหนดธุรกรรมบัตรเครดิตใหม่แล้ว ธุรกรรมสามารถถูกเลือกสำหรับรายงานค่าใช้จ่ายและชำระเงินผ่านกระบวนการปกติสำหรับการชำระเงินคืนในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="8cf28-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
