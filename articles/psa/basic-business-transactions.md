---
title: ธุรกรรมทางธุรกิจ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับธุรกรรมทางธุรกิจ
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d82f5d75de69b32b39c9a55d77287c0719930eb4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086054"
---
# <a name="business-transactions"></a>ธุรกรรมทางธุรกิจ

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

ใน Dynamics 365 Project Service Automation *ธุรกรรมทางธุรกิจ* เป็นแนวคิดที่เป็นนามธรรมซึ่งไม่ได้แสดงโดยเอนทิตีใดๆ อย่างไรก็ตามบางฟิลด์และกระบวนการทั่วไปบนเอนทิตีได้รับการออกแบบมาเพื่อใช้แนวคิดของธุรกรรมทางธุรกิจ เอนทิตีต่อไปนี้ใช้สำหรับสิ่งที่เป็นนามธรรม:

- รายละเอียดบรรทัดใบเสนอราคา
- รายละเอียดที่เป็นรายละเอียดการให้บริการตามสัญญา
- บรรทัดการประมาณการ
- บรรทัดสมุดรายวัน
- ตามจริง

ของเอนทิตี, รายละเอียดบรรทัดใบเสนอราคา รายละเอียดการให้บริการตามสัญญา และบรรทัดการประเมินจะการเหล่านี้ถูกแม็ปกับระยะการประเมินในวงจรชีวิตของโครงการ บรรทัดสมุดรายวันและเอนทิตีที่เกิดขึ้นจริงได้รับการแม็ปกับขั้นตอนการดำเนินการในวงจรชีวิตของโครงการ

PSA ให้เรกคอร์ดในทั้งห้าเอนทิตีนี้เป็นธุรกรรมทางธุรกิจ ความแตกต่างเพียงอย่างเดียวคือเรกคอร์ดในเอนทิตีที่มีการแม็ปกับระยะการประเมินจะถือว่าเป็นการคาดการณ์ทางการเงิน ในขณะที่เรกคอร์ดในเอนทิตีที่ถูกแมปไปยังระยะการดำเนินการจะถือว่าเป็นข้อเท็จจริงทางการเงินที่เกิดขึ้นแล้ว

สำหรับข้อมูลเพิ่มเติม ดูที่ [การประเมินการ](estimates.md) และ [ข้อมูลจริง](actuals.md)

## <a name="concepts-that-are-unique-to-business-transactions"></a>แนวคิดที่ไม่ซ้ำกับธุรกรรมทางธุรกิจ
แนวคิดต่อไปนี้ไม่ซ้ำกับแนวคิดของธุรกรรมทางธุรกิจ:

- ชนิดธุรกรรม
- คลาสธุรกรรม
- ที่มาของธุรกรรม
- การเชื่อมต่อธุรกรรม

### <a name="transaction-type"></a>ชนิดธุรกรรม

ชนิดของธุรกรรมแสดงถึงระยะเวลาและบริบทของผลกระทบทางการเงินในโครงการ แสดงโดยชุดตัวเลือกที่มีค่าที่สนับสนุนใน PSA ดังต่อไปนี้:
- ต้นทุน
- สัญญาโครงการ
- ยอดขายที่ยังไม่ได้เรียกเก็บเงิน
- ยอดขายที่เรียกเก็บเงินแล้ว
- การขายระหว่างองค์กร
- ต้นทุนต่อหน่วยการจัดเตรียมทรัพยากร

### <a name="transaction-class"></a>คลาสธุรกรรม

คลาสของธุรกรรมแสดงถึงชนิดต่างๆ ของต้นทุนที่เกิดขึ้นในโครงการ แสดงโดยชุดตัวเลือกที่มีค่าที่สนับสนุนใน PSA ดังต่อไปนี้:

- Time
- ค่าใช้จ่าย
- วัสดุ
- ค่าธรรมเนียม
- เหตุการณ์สำคัญ
- ภาษี

ค่า **เหตุการณ์สำคัญ** มักถูกใช้โดยตรรกะทางธุรกิจสำหรับการเรียกเก็บเงินที่มีราคาคงที่ใน PSA

### <a name="transaction-origin"></a>ที่มาของธุรกรรม

แหล่งกำเนิดของธุรกรรมเป็นเอนทิตีที่เก็บต้นกำเนิดของธุรกรรมทางธุรกิจแต่ละรายการ เมื่อการดำเนินโครงการเริ่มดำเนินการ ธุรกรรมทางธุรกิจแต่ละรายการจะก่อให้เกิดธุรกรรมทางธุรกิจอื่น ซึ่งจะสร้างอีกรายการหนึ่ง และรายการอื่นๆ เอนทิตีต้นกำเนิดธุรกรรมถูกออกแบบมาเพื่อเก็บข้อมูลเกี่ยวกับต้นกำเนิดของธุรกรรมแต่ละรายการ เพื่อช่วยในการรายงานและการตรวจสอบย้อนกลับ 

### <a name="transaction-connection"></a>การเชื่อมต่อธุรกรรม

การเชื่อมต่อธุรกรรมเป็นเอนทิตีที่จัดเก็บความสัมพันธ์ระหว่างสองธุรกรรมทางธุรกิจที่คล้ายกัน เช่น ต้นทุนและการขายที่เกี่ยวข้องจริง หรือการกลับรายการธุรกรรมที่ถูกทริกเกอร์โดยกิจกรรมการเรียกเก็บเงิน เช่น การยืนยันใบแจ้งหนี้หรือการแก้ไขใบแจ้งหนี้

ที่มาของธุรกรรมและเอนทิตีการเชื่อมต่อธุรกรรมจะร่วมกันช่วยให้คุณรักษาการติดตามความสัมพันธ์ระหว่างธุรกรรมธุรกิจและการดำเนินการที่มีผลลัพธ์เป็นการสร้างธุรกรรมทางธุรกิจที่เฉพาะเจาะจง

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>ตัวอย่าง: วิธีที่ที่มาของธุรกรรมทำงานกับการเชื่อมต่อธุรกรรม

ตัวอย่างต่อไปนี้แสดงการประมวลผลรายการเวลาโดยทั่วไปในวงจรชีวิตของโครงการ PSA

> ![การประมวลผลรายการเวลาในวัฏจักร Project Service](media/basic-guide-17.png)
 
1. การส่งรายการเวลาทำให้เกิดการสร้างบรรทัดสมุดรายวันสองรายการ: รายการหนึ่งสำหรับต้นทุนและรายการหนึ่งสำหรับการขายที่ยังไม่ได้เรียกเก็บเงิน
2. การส่งการอนุมัติของรายการเวลาทำให้เกิดการสร้างข้อมูลจริงสองรายการ: รายการหนึ่งสำหรับต้นทุนและรายการหนึ่งสำหรับการขายที่ยังไม่ได้เรียกเก็บเงิน
3. เมื่อผู้ใช้สร้างใบแจ้งหนี้โครงการ ธุรกรรมบรรทัดใบแจ้งหนี้จะถูกสร้างขึ้นโดยใช้ข้อมูลจากการขายจริงที่ยังไม่ได้เรียกเก็บเงิน 
4. เมื่อใบแจ้งหนี้ได้รับการยืนยันจะมีการสร้างข้อมูลจริงใหม่สองรายการ: การกลับการขายที่ยังไม่ได้เรียกเก็บเงินและการขายที่เรียกเก็บเงินจริง

แต่ละเหตุการณ์เหล่านี้จะทริกเกอร์การสร้างเรกคอร์ดในเอนทิตีที่มาของธุรกรรมและการเชื่อมต่อธุรกรรมเพื่อช่วยสร้างการติดตามของความสัมพันธ์ระหว่างเรกคอร์ดทั้งหมดที่สร้างขึ้นในรายละเอียดรายการเวลา บรรทัดสมุดรายวัน ข้อมูลจริง และบรรทัดใบแจ้งหนี้

ตารางต่อไปนี้แสดงเรกคอร์ดในเอนทิตี้ที่มาของธุรกรรมสำหรับโฟลว์งานก่อนหน้านี้

| เหตุการณ์                        | ที่มา                   | ชนิดที่มา                       | ธุรกรรม                       | ชนิดธุรกรรม         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| การส่งรายการเวลา        | GUID เรกคอร์ดรายการเวลา   | รายการเวลา                        | GUID (ต้นทุน) เรกคอร์ดบรรทัดสมุดรายวัน    | บรรทัดสมุดรายวัน             |
| GUID เรกคอร์ดรายการเวลา       | รายการเวลา               | GUID เรกคอร์ดบรรทัดสมุดรายวัน (การขาย)   | บรรทัดสมุดรายวัน                      |                          |
| การอนุมัติเวลา                | GUID เรกคอร์ดบรรทัดสมุดรายวัน | บรรทัดสมุดรายวัน                      | GUID เรกคอร์ดการขายที่ยังไม่ได้เรียกเก็บเงิน        | ตามจริง                   |
| GUID เรกคอร์ดรายการเวลา       | รายการเวลา               | GUID เรกคอร์ดการขายที่ยังไม่ได้เรียกเก็บเงิน        | ตามจริง                            |                          |
| GUID เรกคอร์ดบรรทัดสมุดรายวัน     | บรรทัดสมุดรายวัน             | GUID เรกคอร์ดต้นทุนตามจริง           | ตามจริง                            |                          |
| GUID เรกคอร์ดรายการเวลา       | รายการเวลา               | GUID เรกคอร์ดต้นทุนตามจริง           | ตามจริง                            |                          |
| การสร้างใบแจ้งหนี้             | GUID เรกคอร์ดรายการเวลา   | รายการเวลา                        | GUID ธุรกรรมของบรรทัดใบแจ้งหนี้     | ธุรกรรมของบรรทัดใบแจ้งหนี้ |
| GUID เรกคอร์ดบรรทัดสมุดรายวัน     | บรรทัดสมุดรายวัน             | GUID ธุรกรรมของบรรทัดใบแจ้งหนี้     | ธุรกรรมของบรรทัดใบแจ้งหนี้          |                          |
| การยืนยันใบแจ้งหนี้         | GUID รายการใบแจ้งหนี้        | รายการใบแจ้งหนี้                      | GUID เรกคอร์ดการขายที่เรียกเก็บเงินแล้ว          | ตามจริง                   |
| GUID ใบแจ้งหนี้                 | ใบแจ้งหนี้                  | GUID เรกคอร์ดการขายที่เรียกเก็บเงินแล้ว          | ตามจริง                            |                          |
| GUID รายละเอียดบรรทัดใบแจ้งหนี้     | รายละเอียดรายการใบแจ้งหนี้      | GUID เรกคอร์ดการขายที่เรียกเก็บเงินแล้ว          | ตามจริง                            |                          |
| GUID เรกคอร์ดรายการเวลา       | รายการเวลา               | GUID เรกคอร์ดการขายที่เรียกเก็บเงินแล้ว          | ตามจริง                            |                          |
| GUID เรกคอร์ดบรรทัดสมุดรายวัน     | บรรทัดสมุดรายวัน             | GUID เรกคอร์ดการขายที่เรียกเก็บเงินแล้ว          | ตามจริง                            |                          |
| GUID เรกคอร์ดรายการเวลา       | รายการเวลา               | GUID การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน      | ตามจริง                            |                          |
| GUID เรกคอร์ดบรรทัดสมุดรายวัน     | บรรทัดสมุดรายวัน             | GUID การกลับการขายที่ยังไม่ได้เรียกเก็บเงิน      | ตามจริง                            |                          |
| การแก้ไขใบแจ้งหนี้แบบร่าง     | ILD GUID เก่า             | ธุรกรรมของบรรทัดใบแจ้งหนี้          | ILD GUID การแก้ไข               | ธุรกรรมของบรรทัดใบแจ้งหนี้ |
| IL GUID เก่า                  | รายการใบแจ้งหนี้             | ILD GUID การแก้ไข               | ธุรกรรมของบรรทัดใบแจ้งหนี้          |                          |
| GUID ใบแจ้งหนี้ที่ชำระแล้วเก่า             | ใบแจ้งหนี้                  | ILD GUID การแก้ไข               | ธุรกรรมของบรรทัดใบแจ้งหนี้          |                          |
| GUID เรกคอร์ดรายการเวลา       | รายการเวลา               | ILD GUID การแก้ไข               | ธุรกรรมของบรรทัดใบแจ้งหนี้          |                          |
| GUID เรกคอร์ดบรรทัดสมุดรายวัน     | บรรทัดสมุดรายวัน             | ILD GUID การแก้ไข               | ธุรกรรมของบรรทัดใบแจ้งหนี้          |                          |
| การแก้ไขใบแจ้งหนี้ที่ยืนยันแล้ว | ILD GUID เก่า             | ธุรกรรมของบรรทัดใบแจ้งหนี้          | GUID การขายตามจริงที่เรียกเก็บเงินแล้วที่กลับรายการ | ตามจริง                   |
| IL GUID เก่า                  | รายการใบแจ้งหนี้             | GUID การขายตามจริงที่เรียกเก็บเงินแล้วที่กลับรายการ | ตามจริง                            |                          |
| GUID ใบแจ้งหนี้ที่ชำระแล้วเก่า             | ใบแจ้งหนี้                  | GUID การขายตามจริงที่เรียกเก็บเงินแล้วที่กลับรายการ | ตามจริง                            |                          |
| GUID เรกคอร์ดรายการเวลา       | รายการเวลา               | GUID การขายตามจริงที่เรียกเก็บเงินแล้วที่กลับรายการ | ตามจริง                            |                          |
| GUID เรกคอร์ดบรรทัดสมุดรายวัน     | บรรทัดสมุดรายวัน             | GUID การขายตามจริงที่เรียกเก็บเงินแล้วที่กลับรายการ | ตามจริง                            |                          |
| ILD GUID เก่า                 | ธุรกรรมของบรรทัดใบแจ้งหนี้ | GUID การขายตามจริงใหม่ที่ยังไม่ได้เรียกเก็บเงิน    | ตามจริง                            |                          |
| IL GUID เก่า                  | รายการใบแจ้งหนี้             | GUID การขายตามจริงใหม่ที่ยังไม่ได้เรียกเก็บเงิน    | ตามจริง                            |                          |
| GUID ใบแจ้งหนี้ที่ชำระแล้วเก่า             | ใบแจ้งหนี้                  | GUID การขายตามจริงใหม่ที่ยังไม่ได้เรียกเก็บเงิน    | ตามจริง                            |                          |
| GUID เรกคอร์ดรายการเวลา       | รายการเวลา               | GUID การขายตามจริงใหม่ที่ยังไม่ได้เรียกเก็บเงิน    | ตามจริง                            |                          |
| GUID เรกคอร์ดบรรทัดสมุดรายวัน     | บรรทัดสมุดรายวัน             | GUID การขายตามจริงใหม่ที่ยังไม่ได้เรียกเก็บเงิน    | ตามจริง                            |                          |
| ILD GUID การแก้ไข          | ธุรกรรมของบรรทัดใบแจ้งหนี้ | GUID การขายตามจริงใหม่ที่ยังไม่ได้เรียกเก็บเงิน    | ตามจริง                            |                          |
| IL GUID การแก้ไข           | รายการใบแจ้งหนี้             | GUID การขายตามจริงใหม่ที่ยังไม่ได้เรียกเก็บเงิน    | ตามจริง                            |                          |
| GUID ใบแจ้งหนี้การแก้ไข      | ใบแจ้งหนี้                  | GUID การขายตามจริงใหม่ที่ยังไม่ได้เรียกเก็บเงิน    | ตามจริง                            |                          |

ตารางต่อไปนี้แสดงเรกคอร์ดในเอนทิตีการเชื่อมต่อของธุรกรรมสำหรับโฟลว์งานก่อนหน้านี้

| เหตุการณ์                          | ธุรกรรม 1                 | บทบาทธุรกรรม 1 | ชนิดธุรกรรม 1           | ธุรกรรม 2                | บทบาทธุรกรรม 2 | ชนิดธุรกรรม 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| การส่งรายการเวลา          | GUID เรกคอร์ดบรรทัดสมุดรายวัน (การขาย)      | การขายที่ยังไม่ได้เรียกเก็บเงิน     | msdyn_journalline            | GUID เรกคอร์ดบรรทัดสมุดรายวัน (ต้นทุน)     | ต้นทุน               | msdyn_journalline  |
| การอนุมัติเวลา                  | GUID (การขาย) ตามจริงที่ยังไม่ได้เรียกเก็บเงิน  | การขายที่ยังไม่ได้เรียกเก็บเงิน     | msdyn_actual                 | GUID ต้นทุนตามจริง (ต้นทุน)       | ต้นทุน               | msdyn_actual       |
| การสร้างใบแจ้งหนี้               | GUID รายละเอียดบรรทัดใบแจ้งหนี้      | การขายที่เรียกเก็บเงินแล้ว       | msdyn_invoicelinetransaction | GUID การขายตามจริงที่ยังไม่ได้เรียกเก็บเงิน   | การขายที่ยังไม่ได้เรียกเก็บเงิน     | msdyn_actual       |
| การยืนยันใบแจ้งหนี้           | GUID การกลับรายการตามจริง         | การกลับ          | msdyn_actual                 | GUID การขายที่ยังไม่ได้เรียกเก็บเงินเดิม | ดั้งเดิม           | msdyn_actual       |
| GUID การขายที่เรียกเก็บเงินแล้ว              | การขายที่เรียกเก็บเงินแล้ว                  | msdyn_actual       | GUID การขายตามจริงที่ยังไม่ได้เรียกเก็บเงิน   | การขายที่ยังไม่ได้เรียกเก็บเงิน               | msdyn_actual       |                    |
| การแก้ไขใบแจ้งหนี้แบบร่าง       | GUID ธุรกรรมของบรรทัดใบแจ้งหนี้ | แทน          | msdyn_invoicelinetransaction | GUID การขายที่เรียกเก็บเงินแล้ว            | ดั้งเดิม           | msdyn_actual       |
| ยืนยันการแก้ไขใบแจ้งหนี้     | GUID การกลับการขายที่เรียกเก็บเงินแล้ว    | การกลับ          | msdyn_actual                 | GUID การขายที่เรียกเก็บเงินแล้ว            | ดั้งเดิม           | msdyn_actual       |
| GUID การขายตามจริงใหม่ที่ยังไม่ได้เรียกเก็บเงิน | แทน                     | msdyn_actual       | GUID การขายที่เรียกเก็บเงินแล้ว            | ดั้งเดิม                     | msdyn_actual       |                    |