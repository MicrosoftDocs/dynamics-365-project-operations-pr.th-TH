---
title: ไปยัง Project Operations
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีเข้าถึง Project Operations จาก Lifecycle Services
author: sigitac
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 50b44b014fcbb730b273322390227ae82cbdcefc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290022"
---
# <a name="navigate-project-operations"></a><span data-ttu-id="b0444-103">ไปยัง Project Operations</span><span class="sxs-lookup"><span data-stu-id="b0444-103">Navigate Project Operations</span></span>

<span data-ttu-id="b0444-104">_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง_</span><span class="sxs-lookup"><span data-stu-id="b0444-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b0444-105">Dynamics 365 Project Operations สำหรับสถานการณ์ทรัพยากร/วัสดุที่ไม่ได้เก็บในคลังประกอบด้วยสององค์ประกอบ:</span><span class="sxs-lookup"><span data-stu-id="b0444-105">Dynamics 365 Project Operations for resource/non-stocked scenarios consists of two components:</span></span> 

 - <span data-ttu-id="b0444-106">**Project Operations บนสภาพแวดล้อม Common Data Service (CDS)**: ส่วนประกอบนี้ครอบคลุมถึงความสามารถและกระบวนการต่าง ๆ ตั้งแต่โอกาสทางการขายไปจนถึงการออกใบแจ้งหนี้ชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="b0444-106">**Project Operations on Common Data Service (CDS) environment**: This component covers capabilities and processes from opportunity to proforma invoicing.</span></span> 
 - <span data-ttu-id="b0444-107">**การจัดการโครงการและการบัญชีในสภาพแวดล้อม Dynamics 365 Finance**: ส่วนประกอบนี้ครอบคลุมถึงความสามารถในการจัดการค่าใช้จ่าย การบัญชีโครงการ และการรับรู้รายได้</span><span class="sxs-lookup"><span data-stu-id="b0444-107">**Project management and accounting on Dynamics 365 Finance environment**: This component covers expense management capabilities, project accounting, and revenue recognition.</span></span> 

<span data-ttu-id="b0444-108">หลังจากที่คุณจัดเตรียม Project Operations ตามที่อธิบายไว้ในหัวข้อนี้ หน้า **รายละเอียดสภาพแวดล้อม** ของ Lifecycle Services (LCS) ช่วยให้เข้าถึงทั้งสององค์ประกอบของ Project Operations ได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="b0444-108">After you provision Project Operations as described in this topic, the Lifecycle Services (LCS) **Environment details** page provides easy access to both components of Project Operations.</span></span>  

<span data-ttu-id="b0444-109">ใช้ชื่อสภาพแวดล้อมในส่วน **ชื่อสภาพแวดล้อม Common Data Service** เพื่อนำไปยัง Project Operations บนสภาพแวดล้อม CDS</span><span class="sxs-lookup"><span data-stu-id="b0444-109">Use the environment name in the section, **Common Data Service Environment Name** to navigate to Project Operations on a CDS environment.</span></span> 

  ![ชื่อสภาพแวดล้อม Common Data Service](./media/environment-name.PNG)

<span data-ttu-id="b0444-111">เลือก **เข้าสู่ระบบ** > **เข้าสู่ระบบสภาพแวดล้อม** เพื่อไปที่โมดูล **การจัดการโครงการและการบัญชี** ใน Finance</span><span class="sxs-lookup"><span data-stu-id="b0444-111">Select **Login** > **Log on to environment** to navigate to the **Project management and accounting** module in Finance.</span></span>  

   ![เข้าสู่ระบบ Finance](./media/environment-login.PNG)

> [!NOTE]
> <span data-ttu-id="b0444-113">คุณสามารถเข้าถึง Project Operations ในโมดูล Common Data Service และ **การจัดการโครงการและการบัญชี** โดยตรงโดยใช้ URL ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="b0444-113">You can access Project Operations in the Common Data Service and the **Project management and accounting** module directly by using their respective URLs.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]