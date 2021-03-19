---
title: กำหนดค่าการบัญชีสำหรับโครงการภายใน
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการตั้งค่าแนวทางปฏิบัติการลงบัญชีสำหรับโครงการภายในใน Project Operations
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287621"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="8fa0a-103">กำหนดค่าการบัญชีสำหรับโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="8fa0a-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="8fa0a-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="8fa0a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8fa0a-105">โครงการภายในช่วยให้บริษัทต่างๆ สามารถติดตามต้นทุนที่เกี่ยวข้องกับกิจกรรมที่ไม่ได้ถูกเรียกเก็บเงินจากลูกค้า</span><span class="sxs-lookup"><span data-stu-id="8fa0a-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="8fa0a-106">ตัวอย่างโครงการภายใน ได้แก่:</span><span class="sxs-lookup"><span data-stu-id="8fa0a-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="8fa0a-107">การพัฒนาผลิตภัณฑ์ เช่น แอปบนมือถือ และการติดตามต้นทุนที่เกี่ยวข้องกับการพัฒนา</span><span class="sxs-lookup"><span data-stu-id="8fa0a-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="8fa0a-108">การจัดการเวลาและค่าใช้จ่ายก่อนการขาย</span><span class="sxs-lookup"><span data-stu-id="8fa0a-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="8fa0a-109">โครงการภายในที่ขายล่วงหน้านี้สามารถแปลงเป็นโครงการที่เรียกเก็บเงินได้ในภายหลังหากชนะใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="8fa0a-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="8fa0a-110">โครงการใดๆ ที่ไม่เกี่ยวข้องกับสัญญาใน Dynamics 365 Project Operations ถือว่าเป็นแบบภายใน</span><span class="sxs-lookup"><span data-stu-id="8fa0a-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="8fa0a-111">โปรไฟล์ต้นทุนและรายได้โครงการจะไม่ถูกใช้กำหนดกฎการบัญชีสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="8fa0a-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="8fa0a-112">ต้นทุนโครงการภายในจะลงรายการบัญชีโดยใช้หลักการกำไรและขาดทุนเสมอ</span><span class="sxs-lookup"><span data-stu-id="8fa0a-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="8fa0a-113">บัญชีแยกประเภทสำหรับการลงรายการบัญชีถูกกำหนดไว้ในหน้า **การตั้งค่าการลงบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="8fa0a-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="8fa0a-114">ธุรกรรมเวลาถูกลงรายการบัญชีโดยการให้เดบิตบัญชี **ต้นทุน** และการให้เครดิตบัญชี **การจัดสรรบัญชีเงินเดือน**</span><span class="sxs-lookup"><span data-stu-id="8fa0a-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="8fa0a-115">ธุรกรรมค่าใช้จ่ายถูกลงรายการบัญชีโดยการให้เดบิตบัญชี **ต้นทุน** และการให้เครดิต **บัญชีส่วนต่างเวลาสำหรับค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="8fa0a-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="8fa0a-116">หลังจากธุรกรรมถูกลงรายการบัญชีไปยังโครงการ หากโครงการเชื่อมโยงกับสัญญาโครงการ ระบบจะย้อนกลับธุรกรรมสะสมทั้งหมดและสร้างธุรกรรมที่เรียกเก็บเงินใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="8fa0a-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="8fa0a-117">ธุรกรรมที่เรียกเก็บเงินเป็นไปตามกฎการบัญชีที่กำหนดไว้ในต้นทุนโครงการและโปรไฟล์รายได้ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="8fa0a-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]