---
title: จัดการทรัพยากร
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับวิธีที่คุณสามารถจัดการกับทรัพยากร
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 5b34ad66750dba9459d551a2527c13111196511e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086133"
---
# <a name="manage-resources"></a>จัดการทรัพยากร

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation รวมแดชบอร์ดผู้จัดการทรัพยากรที่ให้ภาพรวมที่เห็นได้ของความต้องการของทรัพยากรและการใช้ประโยชน์ทั่วทั้งองค์กร คุณสามารถใช้แผนภูมิบนแดชบอร์ดนี้เพื่อช่วยแสดงภาพของของข้อมูลดังต่อไปนี้:

- **ความต้องการของทรัพยากร** – แผนภูมิ **Active Resource Request** แสดงทรัพยากรที่ถูกส่ง ทรัพยากรถูกรวมเข้าด้วยกันโดยบทบาทหรือโครงการ
- **ความต้องการของทรัพยากรที่ไม่ได้ส่งมา** – แผนภูมิ **Unassigned Resource Demand** จะแสดงข้อกำหนดของทรัพยากรทั้งหมดที่ไม่ได้ถูกส่ง ยังช่วยผู้จัดการทรัพยากรดูความต้องการที่ยังไม่ได้รับการยืนยันหรือที่อาจจะส่งผ่านการร้องขอทรัพยากร
- **การใช้ประโยชน์ที่เรียกเก็บได้สำหรับสัปดาห์ที่ผ่านมา** – แผนภูมิ **การใช้ประโยชน์ตามบทบาท** แสดงเปอร์เซ็นต์ของการใช้ประโยชน์ที่เรียกเก็บได้จริงขององค์กรตามบทบาทเทียบกับการใช้ประโยชน์ที่เรียกเก็บเงินได้ตามเป้าหมายตามบทบาท

    > [!NOTE]
    > เพื่อทำให้แผนภูมิ **การใช้ประโยชน์ตามบทบาท** พร้อมใช้งาน สร้างงานที่รันเวิร์กโฟลว์ UpdateRoleUtilization งานที่เกิดซ้ำนี้รันทุกๆเจ็ดเพื่อคำนวณการใช้ประโยชน์ที่เรียกเก็บได้สำหรับเจ็ดวันก่อนหน้า ผลลัพธ์ถูกรวมเข้าด้วยกันโดยบทบาท

## <a name="manage-project-team-members"></a>จัดการสมาชิกในทีมโครงการ

ผู้จัดการโครงการสามารถใช้แดชบอร์ดผู้จัดการทรัพยากรเพื่อจัดการทรัพยากรในโครงการ ตัวอย่างเช่น พวกเขาสามารถเพิ่มสมาชิกทีมไปที่โครงการและจองสมาชิกในทีมเพื่อตอบสนองความต้องการทรัพยากรที่ถูกบันทึกโดยทรัพยากรทั่วไปได้โดยตรง

### <a name="add-a-team-member-directly-to-a-project"></a>เพิ่มสมาชิกในกลุ่มไปยังโครงการได้โดยตรง

เพื่อเพิ่มสมาชิกในกลุ่มไปยังโครงการได้โดยตรง บนเพจ **โครงการ** บนแท็บ **ทีม** เลือก **สร้าง** **สร้างด่วน: สมาชิกในทีมโครงการ** กล่องโต้ตอบปรากฏขึ้น ในกล่องโต้ตอบนี้ คุณสามารถทำงานเหล่านี้ได้:

- **จองทรัพยากรที่ระบุชื่อ** – ในฟิล์ด **Bookable Resource** แล้วเลือกชื่อของทรัพยากร จากนั้นเลือกบทบาท กำหนดระยะเวลา และเลือกวิธีการจัดสรร ทรัพยากรที่ระบุชื่อที่คุณเลือกได้ถูกเพิ่มไปในโครงการโดยการใช้วิธีการจัดสรรและปฏิทินทรัพยากรที่เลือกมา
- **เพิ่มทรัพยากรทั่วไป** – เว้นฟิล์ด **ทรัพยากรที่สามารถจองได้** ว่างไว้ จากนั้นเลือกบทบาท กำหนดระยะเวลา เลือกวิธีการจัดสรรที่ต้องการ ทรัพยากรทั่วไปถูกเพิ่มไปยังทีมเป็นตัวยึดตำแหน่งเพื่อถือรูปแบบความต้องการที่ถูกใช้ในการจองทรัพยากรที่ระบุชื่อในทีม ความต้องการเกิดขึ้นตามปฏิทินโครงการ
- **เพิ่มทรัพยากรที่ระบุชื่อในทีมโดยไม่ต้องใช้กำลังการผลิตของทรัพยากร** – ในฟิล์ด **Bookable Resource** แล้วเลือกทรัพยากร จากนั้นเลือกระยะเวลา และเลือก **ไม่มี** เป็นวิธีการจัดสรร ทรัพยากรที่ถูกเพิ่มไปยังทีมแต่กำลังการผลิตของทรัพยากรยังไม่ถูกใช้ผ่านการจอง

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>จองสมาชิกในทีมเพื่อทำตามความต้อองการทรัพยากรสำหรับทรัพยากรทั่วไป

ใน PSA คุณสามารถจองทรัพยากรทั่วไปในทีมโครงการและสามารถระบุบทบาท กำลังการผลิตที่ต้องการ และวิธีที่การผลิตนั้นกระจายออกไป ในความต้องการทรัพยากร คุณสามารถระบุแอตทริบิวต์ที่เกี่ยวข้องกับทรัพยากรทั่วไป แอตทริบิวต์เหล่านี้รวมไปถึงทักษะที่จำเป็น หน่อยองค์กรที่ต้องการ และทรัพยากรที่ต้องการ

ทำตามขั้นตอนต่อไปนี้เพื่อระบุทักษะที่จำเป็นในทรัพยากรทั่วไปสำหรับนักพัฒนา

1. ในหน้า **โครงการ** , ในแท็บ **ทีม** , เลือก **สร้าง** เพื่อจองทรัพยากรทั่วไป

    ![ทรัพยากรทั่วไปที่จองไว้ในทีม](media/Resource-Management-image9.png)

2. ในมุมมอง **สมาชิกในทีมทั้งหมด** ในคอลัมน์ **ความต้องการทรัพยากร** เลือกลิงก์เพื่อเพิ่มทักษะที่จำเป็นสำหรับทรัพยากรทั่วไป

    ![ลิงก์ความต้องการ](media/Resource-Management-image10.png)

3. บนหน้า **ความต้องการทรัพยากร** ที่ปรากฏในกริด **ทักษะ** เลือกจุดไข่ปลา ( **...** ) และจากนั้นเลือก **เพิ่มคุณสมบัติที่จำเป็นใหม่** เพื่อเพิ่มคุณลักษณะที่จำเป็นสำหรับนักพัฒนา

    ![เพิ่มคำสั่งคุณลักษณะที่จำเป็นใหม่](media/Resource-Management-image11.png)

4. ในกล่องโต้ตอบ **สร้างด่วน: คุณลักษณะที่จำเป็น** ที่ปรากฏในฟิล์ด **คุณลักษณะ** เลื่อกทักษะที่จำเป็น หลังจากนั้น ในฟิล์ด **ค่าการจัดอันดับ** เลือกเลือกระดับความเชี่ยวชาญสำหรับทักษะนั้น สุดท้ายนี้ในฟิล์ด **ความต้องการทรัพยากร** ให้กำหนดความต้องการให้กับแหล่งข้อมูลจากหน่วยองค์กรหรือแม้กระทั่งทรัพยากรที่ระบุชื่อ เมื่อคุณทำเสร็จแล้ว ให้เลือก **บันทึก**

    ![สร้างด่วน: กล่องโต้ตอบของคุณลักษณะที่จำเป็น](media/Resource-Management-image12.png)

5. ในหน้า **ความต้องการทรัพยากร** เลือก **จอง** เพื่อตอบสนองความต้องการทรัพยากร

    ![ปุ่มจองบนหน้าทรัพยากรที่จำเป็น](media/Resource-Management-image13.png)

    คุณยังสามารถเลือกทรัพยากรทั่วไปในกริด **All Team Members** และจากนั้นเลือก **จอง**

    ![ปุ่มจองที่อยู่บนกริดสมาชิกทีมทั้งหมด](media/Resource-Management-image14.png)

    > [!NOTE]
    > ในตัวอย่างนี้ มี 40 ชั่วโมงที่ต้องการแต่ไม่มีชั่วโมงที่จองจริงเนื่องจากทรัพยากรทั่วไปไม่มีการจอง นอกจากนั้น ไม่มีชั่วโมงที่มอบหมายเนื่องจากทรัพยากรทั่วไปถูกเพิ่มไปยังทีมโดยตรง ยังไม่ถูกเพิ่มโดยการใช้การมอบหมายงาน

    ในหน้า **ตัวช่วยจัดหมายกำหนดการให้บริการ** คุณสามารถกรองทรัพยากรที่มีอยู่ตามความต้องการที่ระบุไว้ในความต้องการทรัพยากร ทรัพยากรถูกเรียงลำดับตามพารามิเตอร์การเรียงลำดับที่ระบุไว้ในตารางหมายกำหนดการให้บริการ

    ![หน้าตัวช่วยจัดหมายกำหนดการให้บริการ](media/Resource-Management-image15.png)

    นี่คือตัวกรองบางตัวที่ใช้บ่อย:

    - **คุณลักษณะพร้อมกับการจัดอันดับ** กรองโดยทักษะ ประกาศนียบัตร และคุณภาพทรัพยากรอื่นๆพร้อมกับการจัดอันดับความเชี่ยวชาญ
    - **บทบาท** กรองตามบทบาทเริ่มต้นที่ถูกกำหนดให้กับทรัพยากรที่สามารถจองได้
    - **หน่วยองค์กร** กรองทรัพยากรที่สามารถจองได้โดยหน่วยองค์กรที่ได้รับมอบหมาย

6. หากคุณไม่พอใจกับผลลัพธ์ของการค้นหาความต้องการเริ่มต้น คุณสามารถเปลี่ยนเกณฑ์ตัวกรองได้ ขยายบานหน้าต่าง **มุมมองตัวกรอง** ที่อยู่ทางด้านซ้ายและจากนั้นเลือก **ค้นหา** เพื่อหาทรัพยากรเพิ่มเติม

    ![หน้าต่างมุมมองตัวกรอง](media/Resource-Management-image16.png)

7. เพื่อเปลี่ยนวิธีที่ผลลัพธ์ถูกเรียงลำดับ เลือก **เรียงลำดับ**

    ![คำสั่งให้เรียงลำดับ](media/Resource-Management-image17.png)

8. เลือกทรัพยากรตามความต้องการที่ระบุไว้ในความต้องการตามที่ระบุไว้ที่ด้านบนของกริด คุณสามารถล้างการเลือกของเซลล์ในกริดและปล่อยให้ทรัพยากรเปิดความสามารถรองรับ สามารถเลือกได้เพียงหนึ่งทรัพยากรเท่านั้นในแต่ละครั้งที่จองไว้

9. เลือก **สมุด** เพื่อจองทรัพยากรที่เลือกและปล่อยให้ตารางหมายกำหนดการให้บริการเปิดไว้เพื่อให้คุณสามารถเลือกทรัพยากรเพิ่มเติมได้ หรือเลือก **จอง & ออก** เพื่อจองทรัพยากรที่เลือกและปิดตารางหมายกำหนดการให้บริการ

    ![ทรัพยากรสำหรับจอง](media/Resource-Management-image19.png)

    คุณจะได้รับการแจ้งเตือนเกี่ยวกับชั่วโมงที่จองไว้ ตัวชี้วัดความต้องการแสดงจำนวนความต้องการในการจองที่มีความพึงพอใจและจำนวนที่ยังคงอยู่ นอกจากนี้คุณยังสามารถดูว่ากำลังการผลิตของทรัพยากรที่เลือกมีการใช้มากน้อยเพียงใด เลือก **ขยาย** เพื่อดูรายละเอียดเพิ่มเติมเกี่ยวกับการจองทรัพยากร

9. กลับไปที่มุมมอง **สมาชิกในทีมทั้งหมด**  ในกริดให้สังเกตว่าทรัพยากรทั่วไปถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อและมี 40 ชั่วโมงที่ถูกแสดงว่าจองสำหรับทรัพยากรนั้น

    ![อัปเดตกริดสมาชิกทีมทั้งหมดแล้ว](media/Resource-Management-image20.png)

    > [!NOTE]
    > ไม่มีชั่วโมงที่กำหนดไว้แสดงขึ้นเนื่องจากมีการจองโดยตรงกับทีม พวกเขาไม่ได้จองโดยใช้การมอบหมายงาน

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>มอบหมายทรัพยากรทั่วไปให้กับงานและสร้างความต้องการทรัพยากร

ใน PSA คุณสามารถสร้างงานและจากนั้นมอบหมายทรัพยากรทั่วไปให้กับพวกเขา ด้วยวิธีนี้ ความต้องการทรัพยากรสามารถแสดงด้วยตัวยึดตำแหน่งในขณะที่คุณประเมินหมายกำหนดการให้บริการและหมายเลขทางการเงินของคุณ จากนั้นคุณสามารถสร้างความต้องการทรัพยากรสำหรับทรัพยากรทั่วไปและเติมความต้องการเหล่านั้น

1. บนหน้า **โครงการ** บนแท็บ **หมายกำหนดการให้บริการ** ให้เลือก **เพิ่ม** เพื่อสร้างงาน

    ![สร้างงานใหม่](media/Resource-Management-image21.png)

2. ในฟิลด์ **ทรัพยากร** ให้เลือกสัญลักษณ์ **ตัวเลือกทรัพยากร** ตัวเลือกทรัพยากรปรากฏขึ้นและแสดงสมาชิกในทีมที่มีอยู่สำหรับโครงการ

    ![ตัวเลือกทรัพยากร](media/Resource-Management-image22.png)

3. ป้อนชื่อของทรัพยากรทั่วไปใหม่แล้วเลือก **สร้าง**

    ![ชื่อของทรัพยากรทั่วไปใหม่ได้ป้อนแล้ว](media/Resource-Management-image23.png)

4. ในกล่องโต้ตอบ **สร้างด่วน: สมาชิกทีมโครงการ** ที่ปรากฏขึ้นในฟิล์ด **บทบาท** ให้เลือกบทบาทสำหรับทรัพยากรทั่วไป ในฟิลด์ **หน่วยทรัพยากร** ให้เลือกหน่วยองค์กรสำหรับทรัพยากรทั่วไป จากนั้นเลือก **บันทึก**

    ![สร้างด่วน: กล่องโต้ตอบสมาชิกทีมโครงการ](media/Resource-Management-image24.png)

    ขณะนี้สมาชิกทีมทั่วไปได้รับการมอบหมายให้กับงาน

    ![สมาชิกทีมทั่วไปได้รับการมอบหมายให้กับงาน](media/Resource-Management-image25.png)

    บนแท็บ **ทีม** คุณจะเห็นสมาชิกในทีมทั่วไปใหม่ ขอให้สังเกตว่ามีเพียงชั่วโมงที่ได้รับมอบหมายเท่านั้น ชั่วโมงเหล่านี้คือผลรวมของงานทั้งหมดที่ได้มอบหมายให้กับสมาชิกในทีมทั่วไป สมาชิกในทีมทั่วไปยังไม่มีชั่วโมงที่ต้องการหรือความต้องการทรัพยากร

    ![สมาชิกในทีมทั่วไปบนแท็บทีม](media/Resource-Management-image26.png)

5. ขณะนี้คุณสามารถมอบหมายสมาชิกในทีมทั่วไปให้กับงานอื่นๆโดยใช้ตัวเลือกทรัพยากร

    ![สมาชิกในทีมทั่วไปในตัวใช้เลือกทรัพยากร](media/Resource-Management-image27.png)

    เมื่อคุณมอบหมายทรัพยากรทั่วไปให้กับงานเสร็จสิ้นแล้วคุณสามารถสร้างความต้องการทรัพยากรสำหรับทรัพยากรทั่วไปได้

5. บนแท็บ **ทีม** ให้เลือกทรัพยากรทั่วไปและจากนั้นให้เลือก **สร้างความต้องการ**

    ![คำสั่งสร้างความต้องการ](media/Resource-Management-image28.png)

    เมื่อความต้องการถูกสร้างขึ้น สมาชิกในทีมทั่วไปจะมีชั่วโมงที่ต้องการและลิงก์สำหรับความต้องการทรัพยากร

    ![ลิงก์สำหรับความต้องการทรัพยากร](media/Resource-Management-image29.png)

    หลังจากที่คุณจองทรัพยากรที่ระบุชื่อเสร็จสมบูรณ์ ทรัพยากรทั่วไปจะถูกลบออกจากทีมและถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อ

    ![ทรัพยากรทั่วไปถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อ](media/Resource-Management-image30.png)

    บนแท็บ **หมายกำหนดการให้บริการ** การมอบหมายงานของทรัพยากรทั่วไปจะถูกเอาออกและแทนที่ด้วยทรัพยากรที่ระบุชื่อ

    ![การมอบหมายทรัพยากรทั่วไปจะถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อบนแท็บหมายกำหนดการให้บริการ ](media/Resource-Management-image31.png)

    > [!NOTE]
    > ลักษณะการทำงานนี้เกิดขึ้นเฉพาะเมื่อทรัพยากรที่ระบุชื่อมีการจองจนเต็มสำหรับความต้องการทรัพยากรทั่วไป เมื่อทรัพยากรที่ระบุชื่อบางส่วนแทนที่ความต้องการทรัพยากรทั่วไปหรือทรัพยากรที่ระบุชื่อจำนวนมากแทนที่ความต้องการทรัพยากรทั่วไปอย่างใดอย่างหนึ่ง ทรัพยากรทั่วไปยังคงได้รับมอบหมายให้กับงาน

    ในภาพประกอบต่อไปนี้ แผนงาน 80 ชั่วโมงได้รับการวางแผนสำหรับระยะเวลาห้าวัน (16 ชั่วโมงต่อวันมากกว่าห้าวัน) และได้มอบหมายให้กับทรัพยากรทั่วไปที่มีชื่อว่า **ฟังก์ชัน**

    ![80-ชั่วโมง, งาน 5 วันที่ได้มอบหมายให้กับทรัพยากรทั่วไปที่ทำงานได้](media/Resource-Management-image32.png)

    เมื่อคุณสร้างความต้องการ ใช้เวลา 80 ชั่วโมงมากกว่า 5 วัน

    ![ความต้องการที่สร้างขึ้นสำหรับ 80 ชั่วโมงมากกว่า 5 วัน](media/Resource-Management-image33.png)

    เนื่องจากทรัพยากรที่มีอยู่ทำงานได้เพียง 8 ชั่วโมงต่อวัน ต้องใช้ทรัพยากรสองตัวเพื่อตอบสนองความต้องการได้

    ![ทรัพยากรที่สอง](media/Resource-Management-image35.png)

    บนแท็บ **ทีม** ขณะนี้คุณสามารถดูว่าทรัพยากรทั่วไปไม่มีชั่วโมงที่ต้องการ แต่ชั่วโมงที่มอบหมายยังคงปรากฏพร้อมกับทรัพยากรที่ระบุชื่อทั้งสองที่ประกอบกันเป็นการบรรลุเป้าหมาย

    ![ทรัพยากรที่ระบุชื่อทั้งสองบนแท็บทีม](media/Resource-Management-image36.png)

    บนแท็บ **หมายกำหนดการให้บริการ** ทรัพยากรทั่วไปยังคงได้รับมอบหมายให้กับงาน

    ![ทรัพยากรทั่วไปบนแท็บหมายกำหนดการให้บริการ](media/Resource-Management-image37.png)

PSA ไม่ได้มอบหมายทรัพยากรทั้งสองให้กับงาน เนื่องจากลักษณะการทำงานนั้นจะสร้างหมายกำหนดการให้บริการที่คาดการณ์ได้น้อยลง ในตัวอย่างง่ายๆนี้ เป็นเรื่องง่ายที่จะแบ่งชั่วโมงเท่าๆกันระหว่างสองทรัพยากร อย่างไรก็ตาม ในสถานการณ์ที่ซับซ้อนมากขึ้นที่เกี่ยวข้องกับงานหลายและทรัพยากรต่างๆ PSA จะต้องทำสมมติฐานเกี่ยวกับวิธีการจัดสรรการจองที่ได้รับสำหรับหลายๆทรัพยากรในหลายๆงาน

ดังนั้นในสถานการณ์เหล่านี้ ผู้จัดการโครงการจะต้องรับผิดชอบในการแยกวิเคราะห์การจองหลายครั้งและมอบหมายให้พวกเขาตามความจำเป็น ในการจัดสรรการจอง ผู้จัดการโครงการจะมอบหมายงานจากทรัพยากรทั่วไปไปยังทรัพยากรที่ระบุชื่อแล้วจากนั้นใช้มุมมอง **การกระทบยอด** เพื่อให้แน่ใจว่าการจัดสรรทำงานร่วมกับการจองได้

### <a name="edit-a-resource-requirement"></a>แก้ไขความต้องการทรัพยากร

หลังจากที่ความต้องการทรัพยากรถูกสร้างขึ้น ผู้จัดการโครงการหรือผู้จัดการทรัพยากรอาจต้องการแก้ไขรายละเอียดเพื่อปรับปรุงเงื่อนไขการค้นหาเมื่อมีการใช้ตารางหมายกำหนดการให้บริการ หากต้องการแก้ไขความต้องการทรัพยากร ทำตามขั้นตอนเหล่านี้

1. บนหน้า **โครงการ** บนแท็บ **Team** ให้เลือกลิงก์ไปยังความต้องการใดๆในทรัพยากรทั่วไป
2. บนหน้า **ความต้องการทรัพยากร** ที่ปรากฏขึ้น คุณสามารถอัพเดตหลายแอตทริบิวต์ได้ นี่คือตัวอย่าง:

    - ชื่อ
    - วันที่เริ่มต้น
    - จนถึงปัจจุบัน
    - ระยะเวลา
    - ขริดของทรัพยากร

บนเพจ **ความต้องการทรัพยากร** ผู้จัดการโครงการหรือผู้จัดการทรัพยากรยังสามารถกำหนดข้อมูลต่อไปนี้:

- ทักษะ
- บทบาท
- การกำหนดลักษณะทรัพยากร
- หน่วยองค์กรที่ต้องการ

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>อัพเดตการจองทรัพยากรหลังจากที่จองไว้ในโครงการ

หลังจากที่คุณได้เพิ่มทรัพยากรทั่วไปหรือทรัพยากรที่ระบุชื่อไปยังทีมโครงการแล้ว คุณสามารถเปลี่ยนแปลงการจองของทรัพยากรได้

1. บนหน้า **โครงการ** บนแท็บ **ทีม** ให้เลือกสมาชิกทีม แล้วเลือก **ปรับปรุงการจอง**

    ![ตารางหมายกำหนดการให้บริการที่เปิดสำหรับสมาชิกทีมที่เลือก](media/Resource-Management-image40.png)

    ตารางหมายกำหนดการให้บริการจะปรากฏขึ้นและแสดงการจองของสมาชิกทีมโครงการ ขยายเรกคอร์ดของสมาชิกทีมเพื่อดูชั่วโมงที่มีการจองกับโครงการนี้และโครงการอื่นๆที่ใช้ความสามารถรองรับของสมาชิกในทีม

2. เลือกและลากการจองเพื่อขยายหรือตัดทอน กล่องโต้ตอบ **สร้างการจองทรัพยากร** ปรากฏขึ้นซึ่งช่วยให้คุณสามารถปรับการจองได้

    ![สร้างกล่องโต้ตอบการจองทรัพยากร](media/Resource-Management-image41.png)

3. คลิกขวาที่การจอง จากนั้นคุณสามารถใช้เมนูทางลัดเพื่อทำการดำเนินการต่อไปนี้:

    - เปลี่ยนแปลงสถานะการจอง
    - แก้ไขการจอง
    - ทดแทนทรัพยากรในทีมโครงการ

### <a name="change-the-booking-status"></a>เปลี่ยนแปลงสถานะการจอง

คุณสามารถเปลี่ยนสถานะการจองเริ่มต้นหรือที่กำหนดเองได้

![เปลี่ยนคำสั่งสถานะ](media/Resource-Management-image42.png)

สถานะต่อไปนี้จะอยู่ใน PSA:

- **ยกเลิก** – สถานะนี้ได้ยกเลิกการจองทรัพยากรและเพิ่มกำลังการผลิตของทรัพยากร
- **จองแบบตายตัว** – สถานะนี้จะใช้กำลังการผลิตของทรัพยากร การจองโดยทั่วไปจะมีสถานะนี้เมื่อคุณเปิด **ปรับปรุงการจอง** จากกริด **สมาชิกทีมทั้งหมด** ในหน้า **โครงการ**
- **จองแบบไม่ตายตัว** – สถานะนี้จะเพิ่มทรัพยากรให้กับทีมแต่ไม่ได้ใช้กำลังการผลิตของทรัพยากร บ่งชี้ว่าทรัพยากรมีการจองสำหรับงานที่มีศักยภาพแต่ยังคงมีกำลังการผลิตถ้าจำเป็นสำหรับงานอื่น ในมุมมองของความพร้อมใช้งานของทรัพยากรโดยรวม การจองแบบไม่ตายตัวจะมีสถานะแตกต่างจากการจองแบบตายตัว
- **เสนอ** – สถานะนี้แสดงถึงข้อเสนอของผู้จัดการทรัพยากรหรือผู้จัดการโครงการสำหรับทรัพยากร ข้อเสนอไม่ได้ใช้กำลังการผลิตของทรัพยากรและทรัพยากรไม่ได้ถูกเพิ่มลงในทีมโครงการ เมื่อต้องการจองทรัพยากรแบบตายตัวบนทีม ผู้จัดการโครงการต้องยอมรับการประชุมข้อเสนอ

### <a name="submit-resource-requests"></a>ส่งคำขอทรัพยากร

การร้องขอทรัพยากรจะใช้เพื่อดำเนินการตามความต้องการ (ความต้องการทรัพยากร) ที่ต้องปฏิบัติตามผู้จัดการทรัพยากร สำหรับทรัพยากรทั่วไปที่มีอยู่แล้วในทีม คุณสามารถส่งคำขอทรัพยากรได้โดยตรง คำขอทรัพยากรสามารถเติมเต็มได้ในสองวิธี:

- ผู้จัดการทรัพยากรตอบสนองการร้องขอโดยตรง ในกรณีนี้ ทรัพยากรทั่วไปจะถูกแทนที่ด้วยการจองแบบตายตัวที่มีทรัพยากรที่ระบุชื่อ
- ผู้จัดการทรัพยากรเสนอทรัพยากรให้กับผู้จัดการโครงการและผู้จัดการโครงการอนุมัติหรือปฏิเสธทรัพยากรที่นำเสนอ

#### <a name="direct-fulfillment-of-resource-requests"></a>ปฏิบัติตามคำขอทรัพยากรโดยตรง

เมื่อความต้องการทรัพยากรถูกสร้างขึ้น ผู้จัดการโครงการสามารถส่งการร้องขอทรัพยากรสำหรับทรัพยากรทั่วไปโดยการเลือกทรัพยากรและจากนั้นเลือก **ส่งคำขอ**

![ปุ่มส่งคำขอ](media/Resource-Management-image45.png)

ข้อคิดเห็นเกี่ยวกับทรัพยากรสามารถให้กับผู้จัดการทรัพยากรที่จะตอบสนองการร้องขอ หลังจากคำขอถูกส่งแล้ว ฟิลด์ **สถานะ** สำหรับสมาชิกในทีมจะถูกเปลี่ยนเป็น **ส่งแล้ว**

![กำลังป้อนข้อคิดเห็นเพิ่มเติม](media/Resource-Management-image46.png)

เมื่อผู้จัดการทรัพยากรตอบสนองการร้องขอ สมาชิกในทีมทั่วไปจะถูกแทนที่ด้วยทรัพยากรที่ระบุชื่อในกริด **สมาชิกทีมทั้งหมด**

![สมาชิกในทีมทั่วไปจะถูกแทนที่โดยทรัพยากรที่ระบุชื่อในกริดสมาชิกทีมทั้งหมด](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>ใช้การประชุมข้อเสนอทางทรัพยากรสำหรับคำขอทรัพยากร

แทนที่จะจองทรัพยากรโดยตรงในการร้องขอทรัพยากร ผู้จัดการทรัพยากรสามารถนำเสนอทรัพยากรไปยังผู้จัดการโครงการ ผู้จัดการทรัพยากรอาจใช้ตัวเลือกนี้เมื่อการจับคู่ที่แน่นอนสำหรับความต้องการไม่พร้อมใช้งาน เมื่อผู้จัดการทรัพยากรเสนอทรัพยากร ผู้จัดการโครงการเห็นว่าฟิล์ด **สถานะ** สำหรับสมาชิกในทีมทั่วไปมีการเปลี่ยนแปลงไป **เพื่อความต้องการการตรวจทาน**

![สถานะของสมาชิกทีมทั่วไปเปลี่ยนเป็นความต้องการการตรวจทาน](media/Resource-Management-image48.png)

เมื่อต้องการดูทรัพยากรที่นำเสนอพร้อมกับการแสดงภาพของผลจากการจองของการประชุมข้อเสนอ ให้คลิกสองครั้งที่สมาชิกในทีมที่มีสถานะของ **ความต้องการตรวจทาน** จากนั้นเลือกแท็บ **ทรัพยากรที่นำเสนอ** 

![แท็บทรัพยากรที่นำเสนอ](media/Resource-Management-image49.png)

เลือก **ยอมรับการประชุมข้อเสนอทั้งหมด** เพื่อยอมรับทรัพยากรที่นำเสนอทั้งหมด หรือ **ปฏิเสธการประชุมข้อเสนอทั้งหมด** เพื่อที่จะปฏิเสธ ถ้าคุณยอมรับทรัพยากรที่นำเสนอ พวกเขาจะถูกจองแบบตายตัวในโครงการเป็นสมาชิกในทีมและแทนที่ทรัพยากรทั่วไป

> [!NOTE]
> คุณต้องยอมรับหรือปฏิเสธทรัพยากรที่นำเสนอทั้งหมด คุณไม่สามารถยอมรับหรือปฏิเสธบางส่วนได้

### <a name="substitute-a-resource-on-the-project-team"></a>ทดแทนทรัพยากรในทีมโครงการ

บางครั้งผู้จัดการโครงการต้องแทนที่สมาชิกในทีมที่จองไว้ในโครงการ

1. บนหน้า **โครงการ** บนแท็บ **ทีม** ให้เลือกทรัพยากรที่ต้องการแทนที่ แล้วให้เลือก **ปรับปรุงการจอง**
2. ขยายทรัพยากรเพื่อดูโครงการที่มอบหมายให้

    ![การขยายทรัพยากรเพื่อแสดงโครงการที่มอบหมาย](media/Resource-Management-image50.png)

3. คลิกขวาที่โครงการและจากนั้นเลือก **ทดแทนทรัพยากร**
4. ถ้าคุณทราบทรัพยากรที่คุณต้องการจะทดแทนสำหรับทรัพยากรปัจจุบัน เลือกหรือพิมพ์ชื่อแล้วเลือก **มอบหมายใหม่**

    ![การระบุทรัพยากรทดแทน](media/Resource-Management-image51.png)

    หรือให้ทำตามขั้นตอนเหล่านี้เพื่อค้นหาทรัพยากร:

    1. เลือก **ค้นหาการแทนที่**

        ![การค้นหาสำหรับทรัพยากรทดแทน](media/Resource-Management-image52.png)

        ตัวช่วยจัดหมายกำหนดการให้บริการส่งกลับรายการของการทดแทนที่พร้อมใช้งาน ในตัวช่วยจัดหมายกำหนดการให้บริการ คุณสามารถกรองทรัพยากรที่พร้อมใช้งานเพิ่มเติมเพื่อค้นหาสิ่งทดแทนที่เหมาะสม

        ![รายการของทดแทนที่พร้อมใช้งาน](media/Resource-Management-image53.png)

    2. เพื่อทดแทนทรัพยากร เลือกที่คุณต้องการและจากนั้นให้เลือก **ทดแทน**

        ![ทดแทดทรัพยากรที่เลือก](media/Resource-Management-image54.png)

    การจองและการมอบหมายจะถูกแทนที่ด้วยทรัพยากรใหม่

    ![การจองและการมอบหมายถูกแทนที่ด้วยทรัพยากรใหม่](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>กระทบยอดการจองและงานมอบหมายสมาชิกทีม

สำหรับสมาชิกในทีมการจองและการมอบหมายถูกจับเป็นคู่กันอย่างหลวมๆ กล่าวอีกนัยหนึ่ง ทรัพยากรสามารถมีการมอบหมายได้แต่ไม่มีการจอง หรือทรัพยากรสามารถมีการจองได้แต่ไม่มีการมอบหมาย ตามหลักการแล้ว การจองและการมอบหมายควรจะถูกจัดตำแหน่งเพื่อให้ทรัพยากรมีความมุ่งมั่นในความสามารถรองรับเพื่อที่จะปฏิบัติงานที่ได้รับมอบหมาย อย่างไรก็ตามการจองอาจจะขึ้นอยู่กับความพร้อมใช้งานและการกำหนดเวลาที่อาจจะเปลี่ยนแปลงในขณะที่โครงการยังคงดำเนินต่อไป ดังนั้นการจับเป็นคู่กันอย่างหลวมๆของการจองและงานมอบหมายทำให้มีความยืดหยุ่น

PSA มีแท็บ **การกระทบยอด** ที่ให้ผู้จัดการโครงการกระทบยอดการจองของสมาชิกในทีมและงานมอบหมายสำหรับทีมโครงการ

![แท็บการกระทบยอด](media/Resource-Management-image56.png)

แท็บ **การกระทบยอด** แสดงการจองและการมอบหมายไปจนถึงระดับของการมอบหมายงานสำหรับสมาชิกในทีมแต่ละคน จะแสดงชั่วโมงในเซลล์ที่แสดงช่วงเวลาตั้งแต่เดือนไปจนถึงวัน

แท็บยังแสดงภาพรวมผลรวมสุทธิสำหรับโครงการพร้อมกับคอลัมน์ผลรวม

สำหรับทุกทรัพยากร แท็บจะคำนวณความแตกต่างระหว่างการจองของสมาชิกในทีมและค่าสะสมของการกำหนดงานที่มอบหมายของสมาชิกในทีม ตามหลักการแล้ว ความแตกต่างนี้ควรเป็น 0 (ศูนย์) กล่าวอีกนัยหนึ่งคือไม่ควรจะมีความแตกต่างระหว่างการจองและงานมอบหมาย ความแตกต่างของสีและแรเงาเพื่อดึงดูดให้ความสนใจกับสองเงื่อนไข:

- **ความขาดแคลนการจอง** – ความขาดแคลนการจองเกิดขึ้นเมื่อทรัพยากรมีการมอบหมายมากกว่าการจอง เนื่องจากกำลังการผลิตนี้ไม่ได้รับการสงวนสิทธิ์ ผู้จัดการโครงการอาจต้องการแก้ไขเงื่อนไขนี้โดยการขยายการจองของทรัพยากรเพื่อครอบคลุมการขาดดุล
- **การจองเกินจำนวน** การจองเกินจำนวนจะเกิดขึ้นเมื่อมีการจองทรัพยากรไปยังโครงการ แต่ยังไม่ได้กำหนดให้กับงาน เงื่อนไขนี้อาจเป็นที่ยอมรับในกรณีที่ทรัพยากรถูกจองไปยังโครงการก่อนที่จะมีการมอบหมายงาน อย่างไรก็ตามในกรณีอื่นๆ ทรัพยากรไม่ได้วางแผนเพื่อจะมอบหมายให้กับงาน ในกรณีเหล่านี้ ผู้จัดการโครงการควรพิจารณายกเลิกการจองของทรัพยากร เพื่อให้สามารถใช้กำลังการผลิตสำหรับโครงการอื่น

ในบางกรณีเมื่อคุณดูเวลาในระดับที่สูงกว่าระดับวัน (ตัวอย่างเช่นระดับเดือน) คุณอาจเห็นความแตกต่างสุทธิของศูนย์สำหรับทรัพยากร (กล่าวอีกนัยหนึ่ง การจอง = การมอบหมาย) อย่างไรก็ตามถ้าคุณดูเวลาในระดับสัปดาห์ คุณอาจเห็นว่ามีการมอบหมายของชั่วโมงเป็นศูนย์และการจองของ 40 ชั่วโมงในสัปดาห์แรกแต่การมอบหมายงานของ 40 ชั่วโมงและการจองเป็นศูนย์ชั่วโมงในสัปดาห์ที่สอง โดยรวมแล้วการจองและการมอบหมายงานจะกระทบยอดแต่จะแตกต่างจากหนึ่งสัปดาห์ต่อไป

เมื่อคุณดูเวลาในระดับที่สูงกว่า เซลล์ในแท็บ **การกระทบยอด** มีตัวบ่งชี้เพื่อแจ้งให้คุณทราบว่ามีความแตกต่างในระดับที่ต่ำกว่า เมื่อคลิกสองครั้งในเซลล์ คุณสามารถขยายเพื่อดูความแตกต่างได้ จากนั้นคุณสามารถคลิกขวาเพื่อซูมออก โดยการเลือกทรัพยากรแล้วใช้ตัวควบคุม **ความแตกต่างถัดไป** บนแถบเครื่องมือกริด คุณสามารถไปที่ความแตกต่างถัดไประหว่างการจองและการมอบหมายงานสำหรับทรัพยากรนั้น จากนั้นคุณสามารถใช้ตัวควบคุม **ความแตกต่างก่อนหน้านี้** เพื่อกลับไป นอกจากนี้คุณยังสามารถปิดตัวบ่งชี้ความแตกต่างและแถบนำทางภายใต้ **การตั้งค่า**

![ตัวบ่งชี้ความแตกต่าง](media/Resource-Management-image57.png)

ถ้าคุณมีการมอบหมายงานสำหรับทรัพยากรแต่ไม่มีการจองบนหน้า **โครงการ** บนแท็บ **การกระทบยอด** ให้เลือกการขาดแคลนการจองแล้วเลือก **ขยายการจอง** กล่องโต้ตอบ **การขยายการจอง** ปรากฏขึ้นและแสดงการจองที่จำเป็นเพื่อจัดการการขาดแคลนของทรัพยากร นอกจากนี้ยังแสดงการจองที่มีอยู่ของทรัพยากรในโครงการทั้งหมดหรือเอนทิตีที่จัดกำหนดการอื่นๆ ถ้าคุณเลือก **ตกลง** เพื่อสร้างการจองสำหรับทรัพยากรโดยไม่คำนึงถึงความพร้อมใช้งานของทรัพยากรนั้น คุณอาจทำให้เกิดการจองเกิน

![กล่องโต้ตอบการขยายการจอง](media/Resource-Management-image58.png)

ผู้จัดการโครงการหรือผู้จัดการทรัพยากรสามารถใช้ตารางหมายกำหนดการให้บริการเพื่อจัดการกับสถานการณ์ใดๆที่ทรัพยากรถูกจองเกินกว่ากำลังการผลิต