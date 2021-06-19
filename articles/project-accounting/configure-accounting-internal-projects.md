---
title: กำหนดค่าการบัญชีสำหรับโครงการภายใน
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการตั้งค่าแนวทางปฏิบัติการลงบัญชีสำหรับโครงการภายในใน Project Operations
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad8b974ef75cb0a4e43af0aa254cec1bbcab154a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012879"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="68ae6-103">กำหนดค่าการบัญชีสำหรับโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="68ae6-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="68ae6-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="68ae6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="68ae6-105">โครงการภายในช่วยให้บริษัทต่างๆ สามารถติดตามต้นทุนที่เกี่ยวข้องกับกิจกรรมที่ไม่ได้ถูกเรียกเก็บเงินจากลูกค้า</span><span class="sxs-lookup"><span data-stu-id="68ae6-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="68ae6-106">ตัวอย่างโครงการภายใน ได้แก่:</span><span class="sxs-lookup"><span data-stu-id="68ae6-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="68ae6-107">การพัฒนาผลิตภัณฑ์ เช่น แอปบนมือถือ และการติดตามต้นทุนที่เกี่ยวข้องกับการพัฒนา</span><span class="sxs-lookup"><span data-stu-id="68ae6-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="68ae6-108">การจัดการเวลาและค่าใช้จ่ายก่อนการขาย</span><span class="sxs-lookup"><span data-stu-id="68ae6-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="68ae6-109">โครงการภายในที่ขายล่วงหน้านี้สามารถแปลงเป็นโครงการที่เรียกเก็บเงินได้ในภายหลังหากชนะใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="68ae6-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="68ae6-110">โครงการใดๆ ที่ไม่เกี่ยวข้องกับสัญญาใน Dynamics 365 Project Operations ถือว่าเป็นแบบภายใน</span><span class="sxs-lookup"><span data-stu-id="68ae6-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="68ae6-111">โปรไฟล์ต้นทุนและรายได้โครงการจะไม่ถูกใช้กำหนดกฎการบัญชีสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="68ae6-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="68ae6-112">ต้นทุนโครงการภายในจะลงรายการบัญชีโดยใช้หลักการกำไรและขาดทุนเสมอ</span><span class="sxs-lookup"><span data-stu-id="68ae6-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="68ae6-113">บัญชีแยกประเภทสำหรับการลงรายการบัญชีถูกกำหนดไว้ในหน้า **การตั้งค่าการลงบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="68ae6-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="68ae6-114">ธุรกรรมเวลาถูกลงรายการบัญชีโดยการให้เดบิตบัญชี **ต้นทุน** และการให้เครดิตบัญชี **การจัดสรรบัญชีเงินเดือน**</span><span class="sxs-lookup"><span data-stu-id="68ae6-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="68ae6-115">ธุรกรรมค่าใช้จ่ายถูกลงรายการบัญชีโดยการให้เดบิตบัญชี **ต้นทุน** และการให้เครดิต **บัญชีส่วนต่างเวลาสำหรับค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="68ae6-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="68ae6-116">ธุรกรรมสินค้ามีการลงรายการบัญชีโดยการเดบิตบัญชี **ต้นทุน** และเครดิตบัญชี **ต้นทุน - สินค้า**</span><span class="sxs-lookup"><span data-stu-id="68ae6-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="68ae6-117">หลังจากธุรกรรมถูกลงรายการบัญชีไปยังโครงการ หากโครงการเชื่อมโยงกับสัญญาโครงการ ระบบจะย้อนกลับธุรกรรมสะสมทั้งหมดและสร้างธุรกรรมที่เรียกเก็บเงินใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="68ae6-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="68ae6-118">ธุรกรรมที่เรียกเก็บเงินเป็นไปตามกฎการบัญชีที่กำหนดไว้ในต้นทุนโครงการและโปรไฟล์รายได้ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="68ae6-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
