---
title: เพิ่มสมาชิกทีมจากตารางสมาชิกทีม
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับวิธีที่คุณสามารถจัดการกับทรัพยากรสมาชิกทีม
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 0f975d295b4c0ccef9827767beabd32ffd761faa
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897744"
---
# <a name="add-team-members-from-the-team-member-grid"></a>เพิ่มสมาชิกทีมจากตารางสมาชิกทีม

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

Dynamics 365 Project Operations มีแดชบอร์ดผู้จัดการทรัพยากรที่ให้ภาพรวมที่เห็นได้ของความต้องการของทรัพยากรและการใช้ประโยชน์ทั่วทั้งองค์กร คุณสามารถใช้แผนภูมิบนแดชบอร์ดนี้เพื่อช่วยแสดงภาพของข้อมูลดังต่อไปนี้:

- **ความต้องการของทรัพยากร**: แผนภูมิ **คำขอทรัพยากรที่ใช้งานอยู่** แสดงทรัพยากรที่มีการส่ง ทรัพยากรถูกรวมเข้าด้วยกันโดยบทบาทหรือโครงการ
- **ความต้องการของทรัพยากรที่ไม่ได้ส่งมา**: แผนภูมิ **ความต้องการของทรัพยากรที่ยังไม่ได้มอบหมาย** จะแสดงข้อกำหนดของทรัพยากรทั้งหมดที่ไม่ได้ถูกส่ง ตารางนี้ช่วยผู้จัดการทรัพยากรดูความต้องการที่ยังไม่ได้รับการยืนยันหรือที่อาจจะส่งผ่านการร้องขอทรัพยากร
- **การใช้ประโยชน์ที่เรียกเก็บได้สำหรับสัปดาห์ที่ผ่านมา**: แผนภูมิ **การใช้ประโยชน์ตามบทบาท** แสดงเปอร์เซ็นต์ของการใช้ประโยชน์ที่เรียกเก็บได้จริงขององค์กรตามบทบาทเทียบกับการใช้ประโยชน์ที่เรียกเก็บเงินได้ตามเป้าหมายตามบทบาท

    > [!NOTE]
    > เพื่อทำให้แผนภูมิ **การใช้ประโยชน์ตามบทบาท** พร้อมใช้งาน สร้างงานที่รันเวิร์กโฟลว์ **UpdateRoleUtilization** งานที่เกิดซ้ำนี้รันทุกๆเจ็ดเพื่อคำนวณการใช้ประโยชน์ที่เรียกเก็บได้สำหรับเจ็ดวันก่อนหน้า ผลลัพธ์ถูกรวมเข้าด้วยกันโดยบทบาท

## <a name="manage-project-team-members"></a>จัดการสมาชิกในทีมโครงการ

ผู้จัดการโครงการสามารถใช้แดชบอร์ดผู้จัดการทรัพยากรเพื่อจัดการทรัพยากรในโครงการ ตัวอย่างเช่น พวกเขาสามารถเพิ่มสมาชิกทีมไปที่โครงการและจองสมาชิกในทีมเพื่อตอบสนองความต้องการทรัพยากรที่ถูกบันทึกโดยทรัพยากรทั่วไปได้โดยตรง

### <a name="add-a-team-member-directly-to-a-project"></a>เพิ่มสมาชิกในกลุ่มไปยังโครงการได้โดยตรง

เพื่อเพิ่มสมาชิกในกลุ่มไปยังโครงการได้โดยตรง บนฟอร์ม **โครงการ** บนแท็บ **ทีม** เลือก **สร้าง** **สร้างด่วน: สมาชิกในทีมโครงการ** กล่องโต้ตอบปรากฏขึ้น ในกล่องโต้ตอบนี้ คุณสามารถทำงานเหล่านี้ได้:

- **จองทรัพยากรที่ระบุชื่อ**: ในฟิลด์ **ทรัพยากรที่สามารถจองได้** แล้วเลือกชื่อของทรัพยากร จากนั้นเลือกบทบาท กำหนดระยะเวลา และเลือกวิธีการจัดสรร ทรัพยากรที่ระบุชื่อที่คุณเลือกได้ถูกเพิ่มไปในโครงการโดยการใช้วิธีการจัดสรรและปฏิทินทรัพยากรที่เลือกมา
- **เพิ่มทรัพยากรทั่วไป**: เว้นฟิลด์ **ทรัพยากรที่สามารถจองได้** ว่างไว้ จากนั้นเลือกบทบาท กำหนดระยะเวลา เลือกวิธีการจัดสรรที่ต้องการ วิธีนี้จะมีการเพิ่มทรัพยากรทั่วไปให้กับทีมเป็นตัวแทน ตัวแทนจะเก็บรูปแบบความต้องการที่ใช้ในการจองทรัพยากรที่ระบุชื่อในทีม ความต้องการเกิดขึ้นตามปฏิทินโครงการ
- **เพิ่มทรัพยากรที่ระบุชื่อในทีมโดยไม่ต้องใช้ความสามารถรองรับของทรัพยากร**: ในฟิลด์ **ทรัพยากรที่สามารถจองได้** แล้วเลือกทรัพยากร เลือกระยะเวลา และเลือก **ไม่มี** เป็นวิธีการจัดสรร ทรัพยากรที่ถูกเพิ่มไปยังทีมแต่ความสามารถรองรับของทรัพยากรยังไม่ถูกใช้ผ่านการจอง

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>จองสมาชิกในทีมเพื่อทำตามความต้อองการทรัพยากรสำหรับทรัพยากรทั่วไป

ใน Project Operations คุณสามารถจองทรัพยากรทั่วไปในทีมโครงการได้ นอกจากนี้ คุณยังสามารถระบุบทบาท ความสามารถรองรับที่ต้องการ และวิธีการกระจายความสามารถรองรับนั้น สำหรับความต้องการทรัพยากร คุณสามารถระบุแอตทริบิวต์ที่เกี่ยวข้องกับทรัพยากรทั่วไป แอตทริบิวต์เหล่านี้รวมไปถึงทักษะที่จำเป็น หน่อยองค์กรที่ต้องการ และทรัพยากรที่ต้องการ

ทำตามขั้นตอนต่อไปนี้เพื่อระบุทักษะที่จำเป็นในทรัพยากรทั่วไปสำหรับนักพัฒนา

1. ในฟอร์ม **โครงการ** , ในแท็บ **ทีม** , เลือก **สร้าง** เพื่อจองทรัพยากรทั่วไป
2. ในมุมมอง **สมาชิกในทีมทั้งหมด** ในคอลัมน์ **ความต้องการทรัพยากร** เลือกลิงก์เพื่อเพิ่มทักษะที่จำเป็นสำหรับทรัพยากรทั่วไป
3. บนฟอร์ม **ความต้องการทรัพยากร** ในตาราง **ทักษะ** เลือกจุดไข่ปลา (**...**) และจากนั้นเลือก **เพิ่มคุณสมบัติที่จำเป็นใหม่** เพื่อเพิ่มคุณลักษณะที่จำเป็นสำหรับนักพัฒนา
4. ในฟอร์มของกล่องโต้ตอบ **สร้างด่วน: คุณลักษณะที่ต้องการ** ในฟิลด์ **คุณลักษณะ** เลือกทักษะที่ต้องการ
5. ในฟิลด์ **ค่าการจัดอันดับ** เลือกระดับความเชี่ยวชาญสำหรับทักษะนั้น 
6. ในฟิลด์ **ความต้องการทรัพยากร** ให้กำหนดความต้องการให้กับแหล่งข้อมูลจากหน่วยองค์กรหรือแม้กระทั่งทรัพยากรที่ระบุชื่อ เมื่อคุณทำเสร็จแล้ว ให้เลือก **บันทึก**
7. ในฟอร์ม **ความต้องการทรัพยากร** เลือก **จอง** เพื่อตอบสนองความต้องการทรัพยากร คุณยังสามารถเลือกทรัพยากรทั่วไปในกริด **All Team Members** และจากนั้นเลือก **จอง**

    > [!NOTE]
    > ในตัวอย่างนี้ มี 40 ชั่วโมงที่ต้องการแต่ไม่มีชั่วโมงที่จองจริงเนื่องจากทรัพยากรทั่วไปไม่มีการจอง นอกจากนั้น ไม่มีชั่วโมงที่มอบหมายเนื่องจากทรัพยากรทั่วไปถูกเพิ่มไปยังทีมโดยตรงแทนการเพิ่มโดยใช้การมอบหมายงาน

    ในฟอร์ม **ตัวช่วยจัดหมายกำหนดการให้บริการ** คุณสามารถกรองทรัพยากรที่มีอยู่ตามความต้องการที่ระบุไว้ในความต้องการทรัพยากร ทรัพยากรถูกเรียงลำดับตามพารามิเตอร์การเรียงลำดับที่ระบุไว้ในตารางหมายกำหนดการให้บริการ

   ตัวกรองที่ใช้บ่อยที่สุดบางส่วนได้แก่:

    - **คุณลักษณะพร้อมกับการจัดอันดับ**: กรองโดยทักษะ ประกาศนียบัตร และคุณภาพทรัพยากรอื่นๆพร้อมกับการจัดอันดับความเชี่ยวชาญ
    - **บทบาท**: กรองตามบทบาทเริ่มต้นที่ถูกกำหนดให้กับทรัพยากรที่สามารถจองได้
    - **หน่วยองค์กร**: กรองทรัพยากรที่สามารถจองได้โดยหน่วยองค์กรที่ได้รับมอบหมาย

8. หากคุณไม่พอใจกับผลลัพธ์ของการค้นหาความต้องการเริ่มต้น คุณสามารถเปลี่ยนเกณฑ์ตัวกรองได้ ขยายบานหน้าต่าง **มุมมองตัวกรอง** ที่อยู่ทางด้านซ้ายและจากนั้นเลือก **ค้นหา** เพื่อหาทรัพยากรเพิ่มเติม เพื่อเปลี่ยนวิธีที่ผลลัพธ์ถูกเรียงลำดับ เลือก **เรียงลำดับ**
9. เลือกทรัพยากรตามความต้องการที่ระบุไว้ในความต้องการตามที่ระบุไว้ที่ด้านบนของกริด คุณสามารถล้างการเลือกของเซลล์ในกริดและปล่อยให้ทรัพยากรเปิดความสามารถรองรับ สามารถเลือกได้เพียงหนึ่งทรัพยากรเท่านั้นในแต่ละครั้งที่จองไว้
10. เลือก **สมุด** เพื่อจองทรัพยากรที่เลือกและปล่อยให้ตารางหมายกำหนดการให้บริการเปิดไว้เพื่อให้คุณสามารถเลือกทรัพยากรเพิ่มเติมได้ หรือเลือก **จอง & ออก** เพื่อจองทรัพยากรที่เลือกและปิดตารางหมายกำหนดการให้บริการ
11. กลับไปที่มุมมอง **สมาชิกในทีมทั้งหมด**  ในกริดให้สังเกตว่าทรัพยากรทั่วไปถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อและมี 40 ชั่วโมงที่ถูกแสดงว่าจองสำหรับทรัพยากรนั้น

    > [!NOTE]
    > ไม่มีชั่วโมงที่กำหนดไว้แสดงขึ้นเนื่องจากมีการจองโดยตรงกับทีม พวกเขาไม่ได้จองโดยใช้การมอบหมายงาน

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>มอบหมายทรัพยากรทั่วไปให้กับงานและสร้างความต้องการทรัพยากร

ใน Project Operations คุณสามารถสร้างงานและจากนั้นมอบหมายทรัพยากรทั่วไปให้กับพวกเขา ความต้องการทรัพยากรสามารถแสดงด้วยตัวยึดตำแหน่งในขณะที่คุณประเมินหมายกำหนดการให้บริการและหมายเลขทางการเงินของคุณ จากนั้นคุณสามารถสร้างความต้องการทรัพยากรสำหรับทรัพยากรทั่วไปและเติมความต้องการเหล่านั้น

1. บนฟอร์ม **โครงการ** บนแท็บ **หมายกำหนดการให้บริการ** ให้เลือก **เพิ่ม** เพื่อสร้างงาน
2. ในฟิลด์ **ทรัพยากร** ให้เลือกสัญลักษณ์ **ตัวเลือกทรัพยากร** ตัวเลือกทรัพยากรปรากฏขึ้นและแสดงสมาชิกในทีมที่มีอยู่สำหรับโครงการ
3. ป้อนชื่อของทรัพยากรทั่วไปใหม่แล้วเลือก **สร้าง**
4. ในกล่องโต้ตอบ **สร้างด่วน: สมาชิกทีมโครงการ** ที่ปรากฏขึ้นในฟิลด์ **บทบาท** ให้เลือกบทบาทสำหรับทรัพยากรทั่วไป 
5. ในฟิลด์ **หน่วยทรัพยากร** ให้เลือกหน่วยองค์กรสำหรับทรัพยากรทั่วไป จากนั้นเลือก **บันทึก** ขณะนี้สมาชิกทีมทั่วไปได้รับการมอบหมายให้กับงาน

   บนแท็บ **ทีม** คุณจะเห็นสมาชิกในทีมทั่วไปใหม่ ขอให้สังเกตว่ามีเพียงชั่วโมงที่ได้รับมอบหมายเท่านั้น ชั่วโมงเหล่านี้คือผลรวมของงานทั้งหมดที่ได้มอบหมายให้กับสมาชิกในทีมทั่วไป สมาชิกในทีมทั่วไปยังไม่มีชั่วโมงที่ต้องการหรือความต้องการทรัพยากร

6. ขณะนี้คุณสามารถมอบหมายสมาชิกในทีมทั่วไปให้กับงานอื่นๆโดยใช้ตัวเลือกทรัพยากร

   เมื่อคุณมอบหมายทรัพยากรทั่วไปให้กับงานเสร็จสิ้นแล้วคุณสามารถสร้างความต้องการทรัพยากรสำหรับทรัพยากรทั่วไปได้

7. บนแท็บ **ทีม** ให้เลือกทรัพยากรทั่วไปและจากนั้นให้เลือก **สร้างความต้องการ** เมื่อความต้องการถูกสร้างขึ้น สมาชิกในทีมทั่วไปจะมีชั่วโมงที่ต้องการและลิงก์สำหรับความต้องการทรัพยากร

  หลังจากที่คุณจองทรัพยากรที่ระบุชื่อเสร็จสมบูรณ์ ทรัพยากรทั่วไปจะถูกลบออกจากทีมและถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อ บนแท็บ **หมายกำหนดการให้บริการ** การมอบหมายงานของทรัพยากรทั่วไปจะถูกเอาออกและแทนที่ด้วยทรัพยากรที่ระบุชื่อ

  > [!NOTE]
  > ลักษณะการทำงานนี้เกิดขึ้นเฉพาะเมื่อทรัพยากรที่ระบุชื่อมีการจองจนเต็มสำหรับความต้องการทรัพยากรทั่วไป เมื่อทรัพยากรที่ระบุชื่อบางส่วนแทนที่ความต้องการทรัพยากรทั่วไปหรือทรัพยากรที่ระบุชื่อจำนวนมากแทนที่ความต้องการทรัพยากรทั่วไปอย่างใดอย่างหนึ่ง ทรัพยากรทั่วไปยังคงได้รับมอบหมายให้กับงาน

Project Operations ไม่ได้มอบหมายทรัพยากรทั้งสองให้กับงาน เนื่องจากลักษณะการทำงานนั้นจะสร้างหมายกำหนดการให้บริการที่คาดการณ์ได้น้อยลง ในตัวอย่างง่ายๆนี้ เป็นเรื่องง่ายที่จะแบ่งชั่วโมงเท่าๆกันระหว่างสองทรัพยากร อย่างไรก็ตาม ในสถานการณ์ที่ซับซ้อนมากขึ้นที่เกี่ยวข้องกับงานหลายและทรัพยากรต่างๆ PSA จะต้องทำสมมติฐานเกี่ยวกับวิธีการจัดสรรการจองที่ได้รับสำหรับหลายๆทรัพยากรในหลายๆงาน

ดังนั้นในสถานการณ์เหล่านี้ ผู้จัดการโครงการจะต้องรับผิดชอบในการแยกวิเคราะห์การจองหลายครั้งและมอบหมายให้พวกเขาตามความจำเป็น ในการจัดสรรการจอง ผู้จัดการโครงการจะมอบหมายงานจากทรัพยากรทั่วไปไปยังทรัพยากรที่ระบุชื่อแล้วจากนั้นใช้มุมมอง **การกระทบยอด** เพื่อให้แน่ใจว่าการจัดสรรทำงานร่วมกับการจองได้

### <a name="edit-a-resource-requirement"></a>แก้ไขความต้องการทรัพยากร

หลังจากที่ความต้องการทรัพยากรถูกสร้างขึ้น ผู้จัดการโครงการหรือผู้จัดการทรัพยากรอาจต้องการแก้ไขรายละเอียดเพื่อปรับปรุงเงื่อนไขการค้นหาเมื่อมีการใช้ตารางหมายกำหนดการให้บริการ หากต้องการแก้ไขความต้องการทรัพยากร ทำตามขั้นตอนเหล่านี้

1. บนฟอร์ม **โครงการ** บนแท็บ **ทีม** ให้เลือกลิงก์ไปยังความต้องการใดๆ ในทรัพยากรทั่วไป
2. บนฟอร์ม **ความต้องการทรัพยากร** ที่ปรากฏขึ้น ให้ป้อนข้อมูลฟิลด์ที่จำเป็น

   บนฟอร์ม **ความต้องการทรัพยากร** ผู้จัดการโครงการหรือผู้จัดการทรัพยากรยังสามารถกำหนดทักษะ บทบาท การกำหนดลักษณะทรัพยากร และหน่วยขององค์กรที่ต้องการได้

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>อัพเดตการจองทรัพยากรหลังจากที่จองไว้ในโครงการ

หลังจากที่คุณได้เพิ่มทรัพยากรทั่วไปหรือทรัพยากรที่ระบุชื่อไปยังทีมโครงการแล้ว คุณสามารถเปลี่ยนแปลงการจองของทรัพยากรได้

1. บนฟอร์ม **โครงการ** บนแท็บ **ทีม** ให้เลือกสมาชิกทีม แล้วเลือก **ปรับปรุงการจอง**
 
   ตารางหมายกำหนดการให้บริการจะปรากฏขึ้นและแสดงการจองของสมาชิกทีมโครงการ ขยายเรกคอร์ดของสมาชิกทีมเพื่อดูชั่วโมงที่มีการจองกับโครงการนี้และโครงการอื่นๆที่ใช้ความสามารถรองรับของสมาชิกในทีม

2. เลือกและลากการจองเพื่อขยายหรือตัดทอน กล่องโต้ตอบ **สร้างการจองทรัพยากร** ปรากฏขึ้นซึ่งช่วยให้คุณสามารถปรับการจองได้
3. คลิกขวาที่การจอง จากนั้นคุณสามารถใช้เมนูทางลัดเพื่อทำการดำเนินการต่อไปนี้:

    - เปลี่ยนแปลงสถานะการจอง
    - แก้ไขการจอง
    - ทดแทนทรัพยากรในทีมโครงการ

### <a name="change-the-booking-status"></a>เปลี่ยนแปลงสถานะการจอง

คุณสามารถเปลี่ยนสถานะการจองเริ่มต้นหรือที่กำหนดเองได้

สถานะต่อไปนี้จะอยู่ใน Project Operations:

- **ถูกยกเลิก**: ยกเลิกการจองทรัพยากรและเพิ่มความสามารถรองรับของทรัพยากร
- **จองแบบตายตัว**: ใช้ความสามารถรองรับของทรัพยากร การจองโดยทั่วไปจะมีสถานะนี้เมื่อคุณเปิด **ปรับปรุงการจอง** จากกริด **สมาชิกทีมทั้งหมด** ในฟอร์ม **โครงการ**
- **จองแบบไม่ตายตัว**: เพิ่มทรัพยากรให้กับทีมแต่ไม่ได้ใช้ความสามารถรองรับของทรัพยากร สถานะนี้บ่งชี้ว่าทรัพยากรมีการจองสำหรับงานที่มีศักยภาพแต่ยังคงมีความสามารถรองรับถ้าจำเป็นสำหรับงานอื่น ในมุมมองของความพร้อมใช้งานของทรัพยากรโดยรวม การจองแบบไม่ตายตัวจะมีสถานะแตกต่างจากการจองแบบตายตัว
- **ที่เสนอ**: แสดงถึงข้อเสนอของผู้จัดการทรัพยากรหรือผู้จัดการโครงการสำหรับทรัพยากร ข้อเสนอไม่ได้ใช้ความสามารถรองรับของทรัพยากรและทรัพยากรไม่ได้ถูกเพิ่มลงในทีมโครงการ เมื่อต้องการจองทรัพยากรแบบตายตัวในทีม ผู้จัดการโครงการต้องยอมรับข้อเสนอ

### <a name="submit-resource-requests"></a>ส่งคำขอทรัพยากร

การร้องขอทรัพยากรจะใช้เพื่อดำเนินการตามความต้องการ หรือความต้องการทรัพยากร ที่ต้องปฏิบัติตามผู้จัดการทรัพยากร สำหรับทรัพยากรทั่วไปที่มีอยู่แล้วในทีม คุณสามารถส่งคำขอทรัพยากรได้โดยตรง คำขอทรัพยากรสามารถเติมเต็มได้ในสองวิธี:

- ผู้จัดการทรัพยากรตอบสนองการร้องขอโดยตรง ในกรณีนี้ ทรัพยากรทั่วไปจะถูกแทนที่ด้วยการจองแบบตายตัวที่มีทรัพยากรที่ระบุชื่อ
- ผู้จัดการทรัพยากรเสนอทรัพยากรให้กับผู้จัดการโครงการและผู้จัดการโครงการอนุมัติหรือปฏิเสธทรัพยากรที่นำเสนอ

#### <a name="direct-fulfillment-of-resource-requests"></a>ปฏิบัติตามคำขอทรัพยากรโดยตรง

เมื่อความต้องการทรัพยากรถูกสร้างขึ้น ผู้จัดการโครงการสามารถส่งการร้องขอทรัพยากรสำหรับทรัพยากรทั่วไปโดยการเลือกทรัพยากรและจากนั้นเลือก **ส่งคำขอ** ข้อคิดเห็นเกี่ยวกับทรัพยากรสามารถให้กับผู้จัดการทรัพยากรที่จะตอบสนองการร้องขอ หลังจากคำขอถูกส่งแล้ว ฟิลด์ **สถานะ** สำหรับสมาชิกในทีมจะถูกเปลี่ยนเป็น **ส่งแล้ว** เมื่อผู้จัดการทรัพยากรตอบสนองการร้องขอ สมาชิกในทีมทั่วไปจะถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อในกริด **สมาชิกทีมทั้งหมด**

#### <a name="use-a-resource-proposal-for-resource-requests"></a>ใช้การประชุมข้อเสนอทางทรัพยากรสำหรับคำขอทรัพยากร

แทนที่จะจองทรัพยากรโดยตรงในการร้องขอทรัพยากร ผู้จัดการทรัพยากรสามารถนำเสนอทรัพยากรไปยังผู้จัดการโครงการ ผู้จัดการทรัพยากรอาจใช้ตัวเลือกนี้เมื่อการจับคู่ที่แน่นอนสำหรับความต้องการไม่พร้อมใช้งาน เมื่อผู้จัดการทรัพยากรเสนอทรัพยากร ผู้จัดการโครงการเห็นว่าฟิลด์ **สถานะ** สำหรับสมาชิกในทีมทั่วไปมีการเปลี่ยนแปลงไป **เพื่อความต้องการการตรวจทาน**

คุณสามารถดูทรัพยากรที่เสนอพร้อมกับการจัดรูปแบบการแสดงสำหรับผลของการจองข้อเสนอได้ 

1. ดับเบิลคลิกที่สมาชิกทีมที่มีสถานะเป็น **ต้องมีการตรวจสอบ** 
2. เลือกแท็บ **ทรัพยากรที่เสนอ**
3. เลือก **ยอมรับการประชุมข้อเสนอทั้งหมด** เพื่อยอมรับทรัพยากรที่นำเสนอทั้งหมด หรือ **ปฏิเสธการประชุมข้อเสนอทั้งหมด** เพื่อที่จะปฏิเสธ ถ้าคุณยอมรับทรัพยากรที่นำเสนอ พวกเขาจะถูกจองแบบตายตัวในโครงการเป็นสมาชิกในทีมและแทนที่ทรัพยากรทั่วไป

> [!NOTE]
> คุณต้องยอมรับหรือปฏิเสธทรัพยากรที่นำเสนอทั้งหมด คุณไม่สามารถยอมรับหรือปฏิเสธบางส่วนได้

### <a name="substitute-a-resource-on-the-project-team"></a>ทดแทนทรัพยากรในทีมโครงการ

บางครั้งผู้จัดการโครงการต้องแทนที่สมาชิกในทีมที่จองไว้ในโครงการ

1. บนฟอร์ม **โครงการ** บนแท็บ **ทีม** ให้เลือกทรัพยากรที่ต้องการแทนที่ แล้วให้เลือก **ปรับปรุงการจอง**
2. ขยายทรัพยากรเพื่อดูโครงการที่มอบหมายให้
3. คลิกขวาที่โครงการและจากนั้นเลือก **ทดแทนทรัพยากร**
4. ถ้าคุณทราบทรัพยากรที่คุณต้องการจะทดแทนสำหรับทรัพยากรปัจจุบัน เลือกหรือพิมพ์ชื่อแล้วเลือก **มอบหมายใหม่**

หรือ หากคุณต้องการค้นหาทรัพยากร ให้ทำตามขั้นตอนต่อไปนี้

1. เลือก **ค้นหาการแทนที่**

   ตัวช่วยจัดหมายกำหนดการให้บริการส่งกลับรายการของการทดแทนที่พร้อมใช้งาน ในตัวช่วยจัดหมายกำหนดการให้บริการ คุณสามารถกรองทรัพยากรที่พร้อมใช้งานเพิ่มเติมเพื่อค้นหาสิ่งทดแทนที่เหมาะสม

2. เพื่อทดแทนทรัพยากร เลือกที่คุณต้องการและจากนั้นให้เลือก **ทดแทน**   

   การจองและการมอบหมายจะถูกแทนที่ด้วยทรัพยากรใหม่

## <a name="reconcile-team-member-bookings-and-assignments"></a>กระทบยอดการจองและงานมอบหมายสมาชิกทีม

สำหรับสมาชิกในทีมการจองและการมอบหมายถูกจับเป็นคู่กันอย่างหลวมๆ กล่าวอีกนัยหนึ่ง ทรัพยากรสามารถมีการมอบหมายได้แต่ไม่มีการจอง หรือทรัพยากรสามารถมีการจองได้แต่ไม่มีการมอบหมาย ตามหลักการแล้ว การจองและการมอบหมายควรจะถูกจัดตำแหน่งเพื่อให้ทรัพยากรมีความมุ่งมั่นในความสามารถรองรับเพื่อที่จะปฏิบัติงานที่ได้รับมอบหมาย อย่างไรก็ตามการจองอาจจะขึ้นอยู่กับความพร้อมใช้งานและการกำหนดเวลาที่อาจจะเปลี่ยนแปลงในขณะที่โครงการยังคงดำเนินต่อไป ดังนั้นการจับเป็นคู่กันอย่างหลวมๆของการจองและงานมอบหมายทำให้มีความยืดหยุ่น

Project Operations มีแท็บ **การกระทบยอด** ที่ให้ผู้จัดการโครงการกระทบยอดการจองของสมาชิกในทีมและงานมอบหมายสำหรับทีมโครงการ

แท็บ **การกระทบยอด** แสดงการจองและการมอบหมายไปจนถึงระดับของการมอบหมายงานสำหรับสมาชิกในทีมแต่ละคน จะแสดงชั่วโมงในเซลล์ที่แสดงช่วงเวลาตั้งแต่เดือนไปจนถึงวัน

แท็บยังแสดงภาพรวมผลรวมสุทธิสำหรับโครงการพร้อมกับคอลัมน์ผลรวม

สำหรับทุกทรัพยากร แท็บจะคำนวณความแตกต่างระหว่างการจองของสมาชิกในทีมและค่าสะสมของการกำหนดงานที่มอบหมายของสมาชิกในทีม ตามหลักการแล้ว ความแตกต่างนี้ควรเป็น 0 (ศูนย์) กล่าวอีกนัยหนึ่งคือไม่ควรจะมีความแตกต่างระหว่างการจองและงานมอบหมาย ความแตกต่างของสีและแรเงาเพื่อดึงดูดให้ความสนใจกับสองเงื่อนไข:

- **การจองไม่เพียงพอ**: เกิดขึ้นเมื่อทรัพยากรมีการมอบหมายมากกว่าการจอง เนื่องจากความสามารถรองรับนี้ไม่ได้รับการสงวนสิทธิ์ ผู้จัดการโครงการอาจต้องการแก้ไขเงื่อนไขนี้โดยการขยายการจองของทรัพยากรเพื่อครอบคลุมการขาดดุล
- **การจองเกินจำนวน**: เกิดขึ้นเมื่อมีการจองทรัพยากรไปยังโครงการ แต่ยังไม่ได้กำหนดให้กับงาน เงื่อนไขนี้อาจเป็นที่ยอมรับในกรณีที่ทรัพยากรถูกจองไปยังโครงการก่อนที่จะมีการมอบหมายงาน อย่างไรก็ตามในกรณีอื่นๆ ทรัพยากรไม่ได้วางแผนเพื่อจะมอบหมายให้กับงาน ในกรณีเหล่านี้ ผู้จัดการโครงการควรพิจารณายกเลิกการจองของทรัพยากร เพื่อให้สามารถใช้ความสามารถรองรับสำหรับโครงการอื่น

ในบางกรณีเมื่อคุณดูเวลาในระดับที่สูงกว่าระดับวัน (ตัวอย่างเช่นระดับเดือน) คุณอาจเห็นความแตกต่างสุทธิของศูนย์สำหรับทรัพยากร กล่าวอีกนัยหนึ่งคือ การจอง = การมอบหมาย อย่างไรก็ตามถ้าคุณดูเวลาในระดับสัปดาห์ คุณอาจเห็นว่ามีการมอบหมายของชั่วโมงเป็นศูนย์และการจองของ 40 ชั่วโมงในสัปดาห์แรกแต่การมอบหมายงานของ 40 ชั่วโมงและการจองเป็นศูนย์ชั่วโมงในสัปดาห์ที่สอง โดยรวมแล้วการจองและการมอบหมายงานจะกระทบยอดแต่จะแตกต่างจากหนึ่งสัปดาห์ต่อไป

เมื่อคุณดูเวลาในระดับที่สูงกว่า เซลล์ในแท็บ **การกระทบยอด** มีตัวบ่งชี้เพื่อแจ้งให้คุณทราบว่ามีความแตกต่างในระดับที่ต่ำกว่า ดับเบิลคลิกในเซลล์ที่จะขยายเพื่อดูความแตกต่าง จากนั้นคุณสามารถคลิกขวาเพื่อซูมออก โดยการเลือกทรัพยากรแล้วเลือก **ความแตกต่างถัดไป** บนแถบเครื่องมือตาราง คุณสามารถไปที่ความแตกต่างถัดไประหว่างการจองและการมอบหมายงานสำหรับทรัพยากรนั้น เลือก **ความแตกต่างก่อนหน้า** เพื่อย้อนกลับ นอกจากนี้คุณยังสามารถปิดตัวบ่งชี้ความแตกต่างและแถบนำทางภายใต้ **การตั้งค่า**

ถ้าคุณมีการมอบหมายงานสำหรับทรัพยากรแต่ไม่มีการจองบนฟอร์ม **โครงการ** บนแท็บ **การกระทบยอด** ให้เลือกการจองไม่เพียงพอ แล้วเลือก **ขยายการจอง** กล่องโต้ตอบ **การขยายการจอง** ปรากฏขึ้นและแสดงการจองที่จำเป็นเพื่อจัดการการขาดแคลนของทรัพยากร กล่องโต้ตอบนี้ยังแสดงการจองที่มีอยู่ของทรัพยากรในโครงการทั้งหมดหรือเอนทิตีที่จัดกำหนดการอื่นๆ ถ้าคุณเลือก **ตกลง** เพื่อสร้างการจองสำหรับทรัพยากรโดยไม่คำนึงถึงความพร้อมใช้งานของทรัพยากรนั้น คุณอาจทำให้เกิดการจองเกิน

ผู้จัดการโครงการหรือผู้จัดการทรัพยากรสามารถใช้ตารางหมายกำหนดการให้บริการเพื่อจัดการกับสถานการณ์ใดๆที่ทรัพยากรถูกจองเกินกว่าความสามารถรองรับ
