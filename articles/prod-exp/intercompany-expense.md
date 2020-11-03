---
title: ค่าใช้จ่ายระหว่างบริษัท
description: พนักงานที่ถูกว่าจ้างโดยนิติบุคคลหนึ่งในองค์กรอาจทำงานให้กับนิติบุคคลอื่นในองค์กรเดียวกัน ในสถานการณ์นี้ คุณสามารถใช้คุณลักษณะค่าใช้จ่ายระหว่างบริษัท เพื่อกำหนดค่าใช้จ่ายของพนักงานให้กับนิติบุคคลที่ดำเนินงาน
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086083"
---
# <a name="intercompany-expenses"></a>ค่าใช้จ่ายระหว่างบริษัท

[!include [banner](../includes/banner.md)]

พนักงานที่ถูกว่าจ้างโดยนิติบุคคลหนึ่งในองค์กรอาจทำงานให้กับนิติบุคคลอื่นในองค์กรเดียวกัน ในสถานการณ์นี้ คุณสามารถใช้คุณลักษณะค่าใช้จ่ายระหว่างบริษัท เพื่อกำหนดค่าใช้จ่ายของพนักงานให้กับนิติบุคคลที่ดำเนินงาน นิติบุคคลที่จ้างพนักงานเรียกว่า นิติบุคคลให้กู้ยืม นิติบุคคลที่พนักงานต้องเสียค่าใช้จ่าย เรียกว่า นิติบุคคลที่กู้ยืมเงิน 

ก่อนที่พนักงานจะสามารถสร้างและส่งค่าใช้จ่ายสำหรับงานที่ดำเนินการให้กับนิติบุคคลอื่น ในนิติบุคคลที่ให้กู้ยืมเงินบนหน้า **พารามิเตอร์การจัดการค่าใช้จ่าย** เลือกตัวเลือก **อนุญาตรายการค่าใช้จ่ายระหว่างบริษัท** 

## <a name="tax-posting-for-intercompany-expenses"></a>การลงรายการบัญชีภาษีสำหรับค่าใช้จ่ายระหว่างบริษัท

[!include [banner](../includes/banner.md)]

หากคุณต้องการใช้กลุ่มภาษีที่เชื่อมโยงกับนิติบุคคลที่ให้กู้ยืม (ต้นทาง) แทนนิติบุคคลที่กู้ยืมเงิน (ปลายทาง) ในรายงานค่าใช้จ่ายของคุณ คุณจะต้องกำหนดค่านี้ในการตั้งค่าภาษีการขายบัญชีแยกประเภททั่วไป เมื่อพารามิเตอร์บัญชีแยกประเภททั่วไป **นิติบุคคลสำหรับการลงรายการบัญชีภาษีระหว่างบริษัท** ถูกตั้งค่าเป็น **ที่มา** และ **ใช้กฎการจัดเก็บภาษีการขาย** ถูกตั้งค่าเป็น **ไม่** การรวมภาษีจะใช้สำหรับนิติบุคคลที่ให้กู้ยืมเงิน เมื่อพารามิเตอร์เดียวกันถูกตั้งค่าเป็น **ปลายทาง** การรวมภาษีจะใช้สำหรับนิติบุคคลที่กู้ยืมเงิน สำหรับนิติบุคคลในสหรัฐอเมริกา เมื่อพารามิเตอร์ถูกตั้งค่าเป็น **ที่มา** ฟิลด์ **ลูกหนี้ภาษีขาย** ต้องกำหนดค่าใหม่บนหน้า **กลุ่มการลงรายการบัญชีแยกประเภท** กลไกจัดการบัญชีจะใช้ข้อมูลจากฟิลด์นี้สำหรับรายการบัญชีที่เกี่ยวข้องกับภาษี   
ลักษณะการทำงานสอดคล้องกันสำหรับรายการค่าใช้จ่ายที่ลงรายการบัญชีโดยมีหรือไม่มีโครงการ  