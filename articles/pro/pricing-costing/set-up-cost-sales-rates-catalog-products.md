---
title: ตั้งค่าอัตราต้นทุนและการขายสำหรับผลิตภัณฑ์ในแค็ตตาล็อก - Lite
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีตั้งค่าต้นทุนและอัตราการขายสำหรับสินค้าในแค็ตตาล็อกผลิตภัณฑ์
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764587"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="a21e3-103">ตั้งค่าอัตราต้นทุนและการขายสำหรับผลิตภัณฑ์ในแค็ตตาล็อก - Lite</span><span class="sxs-lookup"><span data-stu-id="a21e3-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="a21e3-104">_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_</span><span class="sxs-lookup"><span data-stu-id="a21e3-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a21e3-105">การตั้งราคาสำหรับรายการแค็ตตาล็อกสินค้าใน Dynamics 365 Project Operations เหมือนกับใน Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="a21e3-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="a21e3-106">ใน Project Operations ไม่สามารถประมาณหรือใช้ผลิตภัณฑ์ในโครงการได้ ดังนั้นจึงไม่จำเป็นต้องกำหนดราคาแค็ตตาล็อกผลิตภัณฑ์ในรายการราคาโครงการสำหรับใบเสนอราคาและสัญญา</span><span class="sxs-lookup"><span data-stu-id="a21e3-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="a21e3-107">ใช้ฟิลด์ **ราคาผลิตภัณฑ์** ของใบเสนอราคา สัญญา หรือบัญชีเพื่อกำหนดราคาแค็ตตาล็อกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a21e3-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="a21e3-108">อย่าตั้งราคาแค็ตตาล็อกผลิตภัณฑ์ในรายการราคาโครงการ</span><span class="sxs-lookup"><span data-stu-id="a21e3-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="a21e3-109">ราคาตลาดของโครงการเป็นเอกสิทธิ์ของ Project Operations</span><span class="sxs-lookup"><span data-stu-id="a21e3-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="a21e3-110">ตรรกะทางธุรกิจเฉพาะโปรแกรมประยุกต์คัดลอกรายการราคาจากใบเสนอราคาเป็นสัญญา</span><span class="sxs-lookup"><span data-stu-id="a21e3-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="a21e3-111">ผลลัพธ์เป็นราคาตลาดของโครงการแบบเฉพาะสัญญา</span><span class="sxs-lookup"><span data-stu-id="a21e3-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="a21e3-112">การดำเนินการคัดลอกอาจทำให้กระบวนการชนะของใบเสนอราคาล่าช้า หากราคาตลาดของโครงการในใบเสนอราคามีขนาดใหญ่เกินไป</span><span class="sxs-lookup"><span data-stu-id="a21e3-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="a21e3-113">ไม่ได้คัดลอกราคาตลาดของผลิตภัณฑ์เพื่อสร้างราคาตลาดที่กำหนดเองในสัญญา</span><span class="sxs-lookup"><span data-stu-id="a21e3-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="a21e3-114">เนื่องจากไม่มีการคัดลอกที่เกี่ยวข้อง ประสิทธิภาพของกระบวนการเสนอราคาจึงไม่ได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="a21e3-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>
