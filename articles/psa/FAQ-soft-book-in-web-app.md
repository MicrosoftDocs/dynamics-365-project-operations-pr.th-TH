---
title: ฉันจะทำการจองทรัพยากร "แบบไม่ตายตัว" ในรุ่นแอพ 2.x ได้อย่างไร?
description: บทความนี้อธิบายถึงวิธีการจองสมาชิกในกลุ่มคนของโครงการแบบไม่ตายด้วยบ Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 9e5d1c91f8ea98117583996552c2f2834be9c537
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085955"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>ฉันจะทำการจองทรัพยากร "แบบไม่ตายตัว" ในแอพเว็บได้อย่างไร (แอพ Project Service v2.x)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

คุณสามารถจัดกำหนดการอย่างไม่แน่นอน หรือ "จองแบบไม่ตายตัว" ทรัพยากรลงในกลุ่มคนของโครงการ เพื่อแสดงแผนเพื่อให้คุณกำหนดทรัพยากรให้กับโครงการ การจองแบบไม่ตายตัวไม่ใช้กำลังการผลิตที่พร้อมใช้งานของทรัพยากร ไม่สามารถกำหนดสมาชิกของกลุ่มคนที่มีการจองแบบไม่ตายตัวไปที่งานโครงการได้ ทรัพยากรที่มีสถานะจองแบบตายตัวและยอมรับชนิดที่ยอมรับ สามารถกำหนดให้กับงาน (โดยใช้สมมติฐานว่ามีชั่วโมงจองแบบตายตัวเพียงพอเพื่อครอบคลุมความพยายามในการกำหนด)

สมาชิกในกลุ่มคนของโครงการแบบไม่ตายตัวแสดงขึ้นในกริดสมาชิกในกลุ่มคน ที่มีชั่วโมงที่มีการจองแบบไม่ตายตัวของพวกเขาที่แสดงในคอลัมน์แบบไม่ตายตัว จะแสดงขึ้นบนบอร์ดกำหนดการด้วย อีกครั้ง จะไม่แสดงปริมาณการใช้ใดๆ ของกำลังการผลิตเป็นการจองแบบไม่ตายตัว ไม่ใช้กำลังการผลิตของทรัพยากร

มีวิธีสามวิธีในการจองแบบไม่ตายตัวสมาชิกในกลุ่มคนบนโครงการที่มี Project Service รุ่น 2.x คุณสามารถจองแบบไม่ตายตัวด้วยบอร์ดกำหนดการ ใช้คุณลักษณะการรักษาการจอง หรือด้วยการสร้างทรัพยากรทั่วไป วิธีการเหล่านี้ถูกอธิบายอยู่ด้านล่างนี้

## <a name="soft-book-with-the-schedule-board"></a>จองแบบไม่ตายตัวด้วยบอร์ดกำหนดการ

เพื่อจองแบบไม่ตายตัวด้วยบอร์ดกำหนดการ ให้ทำตามกระบวนงานนี้: 
1. เปิดบอร์ดกำหนดการ
2. เลือกแท็บโครงการที่แผงความต้องการการจองด้านล่างของบอร์ดกำหนดการ
3. ค้นหาโครงการคุณต้องการจองแบบไม่ตายตัวทรัพยากรในนั้น ถ้าคุณมีโครงการหลายโครงการ คลิกบนส่วนหัวของคอลัมน์โครงการ และจากนั้น ใช้ตัวกรองเพื่อค้นหาโครงการของคุณ
4. คลิกบนโครงการ จากนั้นลากแล้วปล่อยไว้บนกริดเวลาของทรัพยากร
5. นี่จะเปิดแผงการสร้างการจองทรัพยากรทางด้านขวา ปรับปรุงวันที่เริ่มต้นและสิ้นสุด เลือกสถานะการจองเป็นแบบชั่วคราว และตั้งค่าชั่วโมง 
6. คลิกจอง
7. กลับไปในโครงการ ขณะนี้ ทรัพยากรจะแสดงเป็นสมาชิกในทีมที่มีชั่วโมงที่จองแบบไม่ตายตัวในคอลัมน์การจองแบบไม่ตายตัว

หมายเหตุว่า คุณไม่สามารถกำหนดรายการเหล่านั้นให้กับงานในโครงสร้างการแบ่งงาน (WBS) ได้ เนื่องจากทรัพยากรต้องถูกจองแบบตายตัวในกลุ่มคนที่จะถูกกำหนด

## <a name="soft-book-using-the-maintain-bookings-feature"></a>จองแบบไม่ตายตัวโดยใช้คุณลักษณะรักษาการจอง

เพื่อจองแบบไม่ตายตัวด้วยการรักษาการจอง ให้ทำตามกระบวนงานนี้:
1. จากกริดสมาชิกในกลุ่มคน คลิก สร้าง
2. เลือกทรัพยากรที่สามารถจองได้ บทบาท เริ่มต้น/สิ้นสุด
3. เลือกวิธีการปันส่วนอื่นที่ไม่ใช่ ไม่มี:
- กำลังการผลิตแบบเต็ม
- กำลังการผลิตเป็นเปอร์เซ็นต์
- ตามชั่วโมง กระจายแบบเท่าๆ กัน
- ตามชั่วโมง เน้นช่วงต้น
4. คลิก บันทึก คุณจะเห็นทรัพยากรบนกริดของกลุ่มคนและชั่วโมงของพวกเขาที่ถูกระบุเป็นตายตัว
5. รักษาการจองของทรัพยากร โดยการคลิกที่รักษาการจอง
6. เมื่อบอร์ดกำหนดการเปิดขึ้น ขยายทรัพยากรเพื่อแสดงการจองของพวกเขา คุณจะเห็นการจองที่ระบุเป็นตายตัว
7. คลิกขวาที่การจอง ภายใต้สถานะการเปลี่ยน เลือกการจองแบบไม่ตายตัว และจากนั้น ไม่ตายตัว ขณะนี้ สถานะการจองเป็น ไม่ตายตัว
8. หลังจากปิดบอร์ดกำหนดการ คุณจะเห็นว่า ชั่วโมงสำหรับทรัพยากรมีการเปลี่ยนแปลงจากแบบตายตัวเป็นแบบไม่ตายตัวบนกริดสมาชิกในกลุ่มคน
หมายเหตุว่า ถ้าคุณจองทรัพยากรแบบตายตัวลงในกลุ่มคน และจากนั้น กำหนดงานให้พวกเขาใน WBS เมื่อคุณใช้รักษาการจองเพื่อเปลี่ยนสถานะของแบบตายตัวเป็นแบบไม่ตายตัว จะเอาการกำหนดจากงานสำหรับทรัพยากรนั้น เมื่อคุณสามารถกำหนดทรัพยากรที่จองแบบตายตัวเท่ากับงานเท่านั้น

## <a name="soft-book-by-creating-a-generic-resource"></a>จองแบบไม่ตายตัวโดยการสร้างทรัพยากรทั่วไป

คุณสามารถสร้างการจองแบบไม่ตายตัวได้โดยการสร้างสมาชิกในกลุ่มคนของทรัพยากรทั่วไป ดำเนินการตามกับบอร์ดกำหนดการหรือการร้องขอทรัพยากร และเปลี่ยนแปลงชนิดในระหว่างการจอง
เพื่อทำสิ่งนี้ ใช้กระบวนงานต่อไปนี้:

1. ในโครงการ WBS กำหนดบทบาทให้กับงานคุณต้องการสร้างสมาชิกในกลุ่มคนทั่วไปให้
2. คลิกสร้างกลุ่มคนในโครงการ
3. กริดสมาชิกในกลุ่มคนของโครงการ เลือกทรัพยากรทั่วไป แล้วคลิกจอง
4. บนบอร์ดกำหนดการ เลือกทรัพยากรที่คุณต้องการจอง
5. บนแผงสร้างการจองทรัพยากรของบอร์ดกำหนดการ เปลี่ยนสถานะจองเป็นแบบไม่ตายตัว
6. คลิกจอง หรือจองและจบการทำงาน

หลังจากปิดบอร์ดกำหนดการ คุณจะเห็นทรัพยากรที่เลือกถูกเพิ่มลงในกลุ่มคนที่มีชั่วโมงที่แบบไม่ตายตัว ตลอดจนชั่วโมงที่กำหนด นอกจากนี้ คุณจะเห็นว่า ทรัพยากรทั่วไปยังคงอยู่ในกลุ่มคนเป็นตัวบ่งชี้ที่งานกำหนดให้กับสมาชิกในกลุ่มคนที่จองแบบไม่ตายตัว

เมื่อคุณพร้อมที่จะเปลี่ยนแปลงทรัพยากรสมาชิกในกลุ่มคนที่จองแบบไม่ตายตัว เป็นในกลุ่มคนที่จองแบบตายตัว เพื่อให้คุณสามารถกำหนดรายการเหล่านั้นให้กับงานได้ ดำเนินการรายการต่อไปนี้:

1. เลือกทรัพยากร และคลิกรักษาการจอง
2. เมื่อบอร์ดกำหนดการเปิดขึ้น ขยายทรัพยากรเพื่อแสดงการจองของพวกเขา คุณจะเห็นการจองถูกทำเครื่องหมายเป็นแบบไม่ตายตัว
3. คลิกขวาที่การจอง ภายใต้สถานะการเปลี่ยน เลือกการจองแบบตายตัว และจากนั้น ตายตัว ขณะนี้ สถานะการจองเป็น ตายตัว
4. หลังจากปิดบอร์ดกำหนดการ คุณจะเห็นว่า ชั่วโมงสำหรับทรัพยากรมีการเปลี่ยนแปลงจากแบบไม่ตายตัวเป็นแบบตายตัวบนกริดสมาชิกในกลุ่มคน ตอนนี้ คุณอาจกำหนดทรัพยากรไปที่งาน (โดยมีการจัดตำแหน่งระหว่างชั่วโมงที่จองแบบตายตัวและจำนวนชั่วโมงความพยายามของงานสำหรับการมอบหมาย) หมายเหตุว่า ถ้าคุณตามขั้นตอนการบรรลุทรัพยากรทั่วไปในรายการ #3 ข้างต้น เมื่อคุณเปลี่ยนสถานะของทรัพยากรที่สามารถจองได้ซึ่งจองแบบไม่ตายตัวเป็นแบบตายตัว สมาชิกในกลุ่มคนทั่วไปจะถูกเอาออกจากกลุ่มคน