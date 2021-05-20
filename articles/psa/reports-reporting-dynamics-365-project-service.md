---
title: โฮมเพจการรายงาน
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการรายงานใน Dynamics 365 Project Service Automation
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 32b504a862f98dac4b1d9b54289476026d988c13
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951502"
---
# <a name="reporting-home-page"></a><span data-ttu-id="e50c9-103">โฮมเพจการรายงาน</span><span class="sxs-lookup"><span data-stu-id="e50c9-103">Reporting home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e50c9-104">Microsoft Dynamics 365 Project Service Automation ให้องค์กรตามโครงการจัดการการดำเนินธุรกิจของตนได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="e50c9-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="e50c9-105">ในโครงการใดๆสมาชิกในทีมต้องจัดการโอกาสทางการขาย ใบเสนอราคาและการวางแผนงาน ทรัพยากรโครงการ จัดการงานตามแผน การเรียกเก็บเงินสำหรับงาน และจากนั้นทำงานเพื่อทำให้โครงการเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e50c9-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="e50c9-106">ความสามารถในการรายงานการดำเนินงานเป็นกุญแจสำคัญในการกำหนดสุขภาพขององค์กรและการดำเนินการแก้ไขใดๆที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="e50c9-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="e50c9-107">PSA ใช้ Microsoft Dynamics 365 ในการรายงานวิธีการและเทคโนโลยีสำหรับการรายงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e50c9-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="e50c9-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวเลือกสำหรับการรายงาน โปรดดูที่ [คู่มือการเขียนรายงานสำหรับ Dynamics 365 Customer Engagement (on-premises)รุ่น 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365)</span><span class="sxs-lookup"><span data-stu-id="e50c9-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="e50c9-109">ตัวช่วยสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="e50c9-109">Report Wizard</span></span>

<span data-ttu-id="e50c9-110">ตัวช่วยสร้างรายงานช่วยให้บุคคลที่ไม่ใช่นักพัฒนาสร้างรายงานอย่างง่ายได้</span><span class="sxs-lookup"><span data-stu-id="e50c9-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="e50c9-111">เนื่องจากแอปถูกสร้างขึ้นบนแพลตฟอร์มที่มีอยู่แล้ว ประสบการณ์จะเหมือนกับประสบการณ์ที่มีการจัดทำเอกสารใน [สร้างหรือแก้ไขรายงานโดยใช้ตัวช่วยสร้างรายงาน](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard)</span><span class="sxs-lookup"><span data-stu-id="e50c9-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="e50c9-112">อย่างไรก็ตามคุณจะใช้เอนทิตีเฉพาะ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e50c9-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="e50c9-113">Custom SQL Server Reporting Services รายงาน</span><span class="sxs-lookup"><span data-stu-id="e50c9-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="e50c9-114">ถ้าธุรกิจของคุณต้องการรายงานเฉพาะที่ไม่สามารถสร้างได้โดยใช้ตัวช่วยสร้างรายงาน คุณสามารถสร้างรายงานที่กำหนดเองได้</span><span class="sxs-lookup"><span data-stu-id="e50c9-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="e50c9-115">คุณต้องติดตั้ง Microsoft Visual Studio ร่วมกับ Microsoft SQL Server Data Tools ที่หมาะสมและ Report Authoring Extensions</span><span class="sxs-lookup"><span data-stu-id="e50c9-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="e50c9-116">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับเครื่องมือและรุ่น โปรดดูที่ [รายงานสภาพแวดล้อมการเขียนโดยใช้ SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools)</span><span class="sxs-lookup"><span data-stu-id="e50c9-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="e50c9-117">สำหรับข้อมูลเกี่ยวกับวิธีการสร้างรายงานที่กำหนดเอง โปรดดูที่ [การสร้างรายงานใหม่โดยใช้ SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools)</span><span class="sxs-lookup"><span data-stu-id="e50c9-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="e50c9-118">แอปข้อมูลเชิงลึก Power BI</span><span class="sxs-lookup"><span data-stu-id="e50c9-118">Power BI insights apps</span></span>

<span data-ttu-id="e50c9-119">Microsoft Power BI และ Dynamics 365 ทั้งสองให้คุณมีวิธีที่มีประสิทธิภาพในการทำงานกับข้อมูลของคุณในรูปแบบของแอปพลิเคชันข้อมูลเชิงลึก</span><span class="sxs-lookup"><span data-stu-id="e50c9-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="e50c9-120">สำหรับข้อมูลเกี่ยวกับความพร้อมใช้งานของแอปข้อมูลเชิงลึก โปรดดูที่ [หน้าแอปข้อมูลเชิงลึก Power BI](https://powerbi.microsoft.com/power-bi-insights-apps/)</span><span class="sxs-lookup"><span data-stu-id="e50c9-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="e50c9-121">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e50c9-121">Additional resources</span></span>
<span data-ttu-id="e50c9-122">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการรายงานใน PSA โปรดดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e50c9-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="e50c9-123">การทำงานกับแบบจำลองข้อมูล Project Service</span><span class="sxs-lookup"><span data-stu-id="e50c9-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="e50c9-124">แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="e50c9-124">Dashboards</span></span>](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]