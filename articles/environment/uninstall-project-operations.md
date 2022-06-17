---
title: ถอนการติดตั้ง Dynamics 365 Project Operations
description: บทความนี้ให้ข้อมูลเกี่ยวกับวิธีถอนการติดตั้ง Dynamics 365 Project Operations
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 33a505594d6db47b4f8a0c8a630a0836f424e7d5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911987"
---
# <a name="uninstall-dynamics-365-project-operations"></a>ถอนการติดตั้ง Dynamics 365 Project Operations 

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ทรัพยากร/ไม่ได้เก็บในคลัง_

หากต้องการถอนการติดตั้ง Dynamics 365 Project Operations คุณต้องได้รับการกำหนดบทบาทเป็นผู้ดูแลระบบ

1. ไปที่ **การตั้งค่า** > **โซลูชัน**

    ![เพจการตั้งค่า](./media/uninstall-proj-ops-solutions.png)
  
2. นำโซลูชันออกในลำดับที่แน่นอนตามที่แสดงไว้ในตารางต่อไปนี้ 

    | ขั้น | ชื่อโซลูชัน                                    | หมายเหตุ                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 2 | ProjectOperations_Anchor                           | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 5 | ProjectService                                     | ไม่มีหมายเหตุเพิ่มเติม                                                                         |
    | 6 | ProjectServiceCore_Patch                           | ไม่มีหมายเหตุเพิ่มเติม                                                                         |
    | 7 | ProjectServiceCore                                 | ไม่มีหมายเหตุเพิ่มเติม                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 9 | FieldServiceCommon                                 | จำเป็นสำหรับการรวมแบบสองทิศทางกับ Dynamics 365 Finance หรือ Dynamics 365 Supply Chain Management   |
    | 10 | msdyn_AssetCommon                                  | จำเป็นสำหรับการรวมแบบสองทิศทางกับ Dynamics 365 Finance หรือ Dynamics 365 Supply Chain Management   |
    | 11 | msdyn_TESA_Anchor                                  | จำเป็นสำหรับ Dynamics 365 Field Service                                                     |
    | 12 | msdyn_TESA_Patch                                   | จำเป็นสำหรับ Dynamics 365 Field Service                                                     |
    | 13 | msdyn_TESA                                         | จำเป็นสำหรับ Dynamics 365 Field Service                                                     |
    | 14 | ResourceSchedulingControls                         | จำเป็นสำหรับ Dynamics 365 Field Service                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | จำเป็นสำหรับ Dynamics 365 Field Service                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | จำเป็นสำหรับ Dynamics 365 Field Service                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | จำเป็นสำหรับ Dynamics 365 Field Service                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 19 | Dynamics365Notes                                   | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 21 | DualWriteCore                                      | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 22 | Dynamics365AssetManagementApp                      | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 23 | Dynamics365AssetManagement                         | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 25 | Dynamics365FinanceExtended                         | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 26 | HCMCommon                                          | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 28 | ผู้เข้าร่วม                                              | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 29 | Dynamics365Company                                 | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 30 | CurrencyExchangeRates                              | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
    | 31 | AssetCommon                                        | หากไม่พบ ให้ข้ามโซลูชันนี้                                                            |
