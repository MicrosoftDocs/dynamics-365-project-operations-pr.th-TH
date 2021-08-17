---
title: จัดการโครงการและการจองในปฏิทิน Office 365 ของคุณ
description: วิธีการจัดการโครงการและการจองในปฏิทิน Office 365 ของคุณ
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b38affbfc8d339ac1a2093391286ea4c095207be8de2e8eeca558e6fcc5bcc07
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985457"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>จัดการโครงการและการจองในปฏิทิน (Project Service) ของคุณ

> [!Note]
> ที่ไม่สนับสนุน: คุณลักษณะนี้ได้รับการตัดออกแล้ว และไม่สามารถใช้ได้อีกต่อไป

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

ดูการนัดหมายส่วนบุคคล การจองงานโครงการ และการนัดหมายใบสั่งงานของ Field Service โดยใช้ปฏิทิน [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]  
  
 ด้วยทุกอย่างในสถานที่เดียว จึงง่ายต่อการจัดการวันของคุณ การประชุม การนัดหมาย การจอง และงานของคุณทั้งหมดสามารถใช้งานได้ในปฏิทิน [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] ของคุณ  
  
 ถ้าคุณกำลังใช้ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]คุณยังสามารถป้อนการนัดหมายส่วนบุคคลของคุณในมุมมองรายการเวลาของ Project Service ได้ด้วย นี่ทำให้ผู้จัดการโครงการและทรัพยากร ทราบความพร้อมใช้งานสำหรับโครงการของคุณ ยังประหยัดเวลาของคุณอีกด้วย เนื่องจากคุณไม่จำเป็นต้องป้อนรายละเอียดเกี่ยวกับการนัดหมายส่วนบุคคลของคุณสองครั้ง คุณสามารถนำเข้าการนัดหมายส่วนบุคคลของคุณได้โดยง่าย จากปฏิทินของคุณไปยังมุมมองรายการของเวลาของ Project Service  
  
 ปฏิทินของคุณจะซิงค์โครงการและการจองใบสั่งงาน จากวันนี้เป็นระยะเวลา 4 สัปดาห์ที่จะมาถึง การตั้งค่านี้ไม่สามารถเปลี่ยนแปลงได้  
  
 การซิงค์ได้รับการสนับสนุนแบบทางเดียวเท่านั้นจาก PSA ไปยังปฏิทิน [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] ของคุณ คุณสามารถซิงค์ในลำดับย้อนกลับ 
  
 เมื่อต้องการเรียนรู้วิธีการใช้ปฏิทิน [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] ของคุณ โปรดดู [ปฏิทินใน Outlook บนเว็บสำหรับธุรกิจ](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936)  
  
## <a name="setup"></a>ตั้งค่า  
 ก่อนที่คุณจะสามารถดูและจัดการการจองของคุณบนปฏิทิน [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] ของคุณได้ คุณจำเป็นต้องติดตั้งบางสิ่ง  
  
- คุณจะต้องมีผู้ดูแลระบบส่วนกลางของ [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] หรือข้อมูลประจำตัวของผู้ดูแลระบบ  
  
- ผู้ดูแลระบบของคุณจำเป็นต้องกำหนดค่าโปรไฟล์เซิร์ฟเวอร์อีเมล และผู้ใช้แต่ละรายจะต้องกำหนดค่ากล่องจดหมายของพวกเขา [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [ตั้งค่าการประมวลผลอีเมลผ่านการทำข้อมูลให้ตรงกันทางฝั่งเซิร์ฟเวอร์](/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>เปิดใช้งานการทำข้อมูลให้ตรงกันสำหรับองค์กรของคุณ (งานผู้ดูแลระบบ)  
  
1.  จากเมนูหลัก ให้คลิก **การตั้งค่า** > **การจัดการ**  
  
2.  คลิก **การตั้งค่าระบบ**  
  
3.  คลิกที่แท็บ **การทำข้อมูลให้ตรงกัน**  
  
4.  ภายใต้ **เลือกว่าจะเปิดใช้งานการทำข้อมูลการจองทรัพยากรให้ตรงกับ หรือไม่** ตรวจสอบ **ทำข้อมูลการจองทรัพยากรให้ตรงกันกับ Outlook**  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>เปิดใช้งานการทำข้อมูลให้ตรงกันสำหรับโพรไฟล์ผู้ใช้ของคุณ (งานผู้ใช้)  
  
1.  คลิกปุ่ม **การตั้งค่า** ในมุมบนขวาของหน้าจอ  
  
2.  คลิก **ตัวเลือก**  
  
3.  คลิกที่แท็บ **การทำข้อมูลให้ตรงกัน**  
  
4.  ภายใต้ **ทำข้อมูลการจองทรัพยากรให้ตรงกันกับ Outlook** ตรวจสอบ **การทำข้อมูลการจองทรัพยากรให้ตรงกันกับ Outlook**  
  
## <a name="import-your-personal-appointments-user-task"></a>นำเข้าการนัดหมายส่วนบุคคลของคุณ (งานผู้ใช้)  
 คุณสามารถนำเข้าการนัดหมายส่วนบุคคลของคุณได้จากปฏิทินของคุณ ไปยังมุมมองรายการของเวลาของ Project Service Automation  
  
1. เปิดปฏิทินของ [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] และคลิก **นำเข้าข้อมูล**  
  
2. บนหน้าจอตัวกรอง เลือก **การนัดหมายจาก Exchange** แล้วคลิก **นำไปใช้**  
  
3. ระบบจะดึงการนัดหมายลงในมุมมองรายการเวลา ให้เป็นรายการที่แนะนำจากสัปดาห์ปัจจุบัน เมื่อต้องการเพิ่มรายการสำหรับสัปดาห์อื่น คลิก **ก่อนหน้านี้** หรือ **ถัดไป**  
  
4. เลือกการนัดหมายที่คุณต้องการเพิ่มลงใน มุมมองรายการของเวลาของ Project Service Automation  
  
5. ในกล่องป็อปอัพ **รายการเวลา** เลือกตัวเลือกที่เหมาะสม เพื่อแปลงการนัดหมายเป็นมุมมองรายการของเวลาของ Project Service Automation  
  
6. คลิก **บันทึก**  
  
### <a name="see-also"></a>ดูเพิ่มเติม  
 [เวลา ค่าใช้จ่าย และคำแนะนำในการทำงานร่วมกัน](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]