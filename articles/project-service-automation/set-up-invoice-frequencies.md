---
title: ตั้งค่าความถี่ของใบแจ้งหนี้
description: วิธีการตั้งค่าความถี่ของใบแจ้งหนี้ใน Project Service
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 49498392-6780-4cd6-a57f-da9aeaecd287
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: be60f81c46baa1fe293a7e0617cd92ffb923f76f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756397"
---
# <a name="set-up-invoice-frequencies-project-service"></a><span data-ttu-id="1f3c5-103">ตั้งค่าความถี่ของใบแจ้งหนี้ (Project Service)</span><span class="sxs-lookup"><span data-stu-id="1f3c5-103">Set up invoice frequencies (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="1f3c5-104">ความถี่ของใบแจ้งหนี้ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ระบุว่าคุณเรียกเก็บเงินไคลเอนต์ของคุณบ่อยเพียงใด และวันไหนในช่วงเวลาที่คุณระบุ</span><span class="sxs-lookup"><span data-stu-id="1f3c5-104">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] invoice frequencies determine how often you bill your clients, and on which day of the time period you specify.</span></span> <span data-ttu-id="1f3c5-105">ตั้งค่าความถี่ของใบแจ้งหนี้สำหรับแต่ละรอบระยะเวลาที่คุณวางแผนที่จะใช้สำหรับการเรียกเก็บเงิน ไคลเอนต์ของคุณเช่นรายเดือน สอง หรือสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="1f3c5-105">Set up an invoice frequency for each time period you plan to use for billing your clients, such as monthly, biweekly, or weekly.</span></span>  
  
1.  <span data-ttu-id="1f3c5-106">ไปที่ **Project Service > ความถี่ของใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="1f3c5-106">Go to **Project Service > Invoice Frequencies**.</span></span>  
  
2.  <span data-ttu-id="1f3c5-107">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="1f3c5-107">Click **New**.</span></span>  
  
3.  <span data-ttu-id="1f3c5-108">ในพื้นที่ **ทั่วไป** ป้อนชื่อสำหรับความถี่ของใบแจ้งหนี้ใน **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="1f3c5-108">In the **General** area, enter a name for the invoice frequency in **Name**.</span></span>  
  
4.  <span data-ttu-id="1f3c5-109">ใน **รอบระยะเวลา** เลือก **รายเดือน**, **อาทิตย์** หรือ **รายสัปดาห์**</span><span class="sxs-lookup"><span data-stu-id="1f3c5-109">In **Period**, select **Monthly**, **Biweekly**, or **Weekly**.</span></span>  
  
5.  <span data-ttu-id="1f3c5-110">ถ้าคุณระบุรอบระยะเวลารายเดือนหรือทุกสองสัปดาห์ ใน **จำนวนวันที่เรียกใช้** เลือก **วันของช่วงเวลา** เพื่อออกใบแจ้งหนี้ในวันที่ระบุระยะเวลา (ว่าเป็นวันทำการหรือวันหยุดสุดสัปดาห์), หรือเลือก **วันในสัปดาห์ของช่วงเวลา** เพื่อออกอินวอยซ์ในวันทำการที่ระบุระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="1f3c5-110">If you specified a period of monthly or biweekly, in **Days of run**, select **Day of period** to invoice on the specified day of the period (whether weekday or weekend), or select **Weekday of period** to invoice on the specified weekday of the period.</span></span>  
  
6.  <span data-ttu-id="1f3c5-111">ถ้าคุณกำหนดระยะเวลาของรายเดือน **รันต่อเดือน** เลือกจำนวนครั้งต่อเดือนที่คุณต้องการเรียกใช้ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="1f3c5-111">If you specified a period of monthly, in **Runs per month**, select the number of times per month you want to run the invoice.</span></span>  
  
7.  <span data-ttu-id="1f3c5-112">ในพื้นที่ **รายละเอียดความถี่ของใบแจ้งหนี้** เปลี่ยนแปลงรายละเอียดวันหรือวันทำการตามความจำเป็นเพื่อให้แน่ใจว่าใบแจ้งหนี้ถูกเรียกใช้ในวันหรือวันทำการที่ถูกต้องของระยะเวลาที่คุณระบุไว้</span><span class="sxs-lookup"><span data-stu-id="1f3c5-112">In the **Invoice Frequency Details** area, change the day or weekday details as necessary to make sure the invoice runs on the correct day or weekday of the period you specified.</span></span>  
  
8.  <span data-ttu-id="1f3c5-113">เมื่อคุณทำเสร็จแล้ว คลิก **บันทึก** ที่มุมล่างขวาของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="1f3c5-113">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="1f3c5-114">ดูเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1f3c5-114">See Also</span></span>  
 [<span data-ttu-id="1f3c5-115">ตั้งค่าคอนฟิก Project Service</span><span class="sxs-lookup"><span data-stu-id="1f3c5-115">Configure Project Service</span></span>](../project-service/configure.md)
