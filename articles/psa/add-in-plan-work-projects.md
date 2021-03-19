---
title: วางแผนงานของคุณใน Microsoft Project ด้วย Add-in ของ Project Service
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการใช้ add-in ของ Microsoft Project สำหรับ Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
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
ms.openlocfilehash: 471d3c421cd9dc39a5864e37ef762b5d08e59762
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285551"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>วางแผนงานของคุณใน Microsoft Project ด้วย Add-in ของ Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ทำให้การวางแผนโครงการของคุณ รวมถึงการประเมินง่ายขึ้นสำหรับคุณ คุณสามารถกำหนดงาน เพื่อให้ต้นทุน ความพยายาม และมูลค่าขายนั้นชัดเจน เมื่อข้อเสนอขั้นสุดท้ายถูกส่ง  

คุณสามารถติดตั้ง [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] และทำงานด้านการวางแผนของคุณในสภาพแวดล้อมที่คุ้นเคยของ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ใช้ความสามารถในการวางแผนและการจัดการที่สมบูรณ์ของ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] แล้วอัพเดตแผนโครงการของคุณใน Project Service Automation  

> [!IMPORTANT]
> - ในการใช้คุณลักษณะการจัดการเอกสารของ SharePoint เพื่อจัดเก็บไฟล์ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ของคุณ สำหรับโครงการ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ผู้ดูแลระบบ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ของคุณ จำเป็นต้องเปิดใช้งานการจัดการเอกสาร 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] จะเข้ากันได้กับ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition เท่านั้น  

## <a name="download-and-install-the-add-in"></a>ดาวน์โหลดและติดตั้ง add-in  
 เตรียมข้อมูลการลงชื่อเข้าใช้ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ของคุณให้พร้อม คุณจะต้องใช้ข้อมูลนี้ในการเชื่อมต่อจาก [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]  

1.  จากศูนย์ดาวน์โหลด ดาวน์โหลด Add-in สำหรับรุ่นที่ได้รับการสนับสนุนของ Project Service ของคุณ ทั้ง [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) หรือ [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956)  

2.  เลือกการเชื่อมโยงการดาวน์โหลด  

3.  เมื่อการดาวน์โหลดเสร็จสมบูรณ์ เลือก **ใช่** เพื่อติดตั้ง add-in  

## <a name="configure-the-add-in"></a>ตั้งค่าคอนฟิก add-in  

1. เปิด [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] และเลือกแท็บ **Project Service**  

2. เลือก **เชื่อมต่อ**  

3. ป้อนข้อมูลการลงชื่อเข้าใช้ของคุณ และจากนั้น เลือก **ลงชื่อเข้าใช้**  

   ตอนนี้ คุณสามารถเริ่มการใช้ add-in ได้  

## <a name="read-from-a-template"></a>อ่านจากเท็มเพลต  
 อ่านจากเท็มเพลตที่คุณได้สร้างขึ้นใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] และได้คัดลอกลงใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] เพื่อเริ่มการวางแผนโครงการของคุณ [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [สร้างเท็มเพลตโครงการ (Project Service Automation)](../psa/create-project-template.md)  

1.  จากแท็บ **Project Service** เลือก **อ่าน** > **เทมเพลตโครงการ Project Service Automation**  

2.  เลือกเทมเพลตโครงการจากรายการ และจากนั้น เลือก **เปิด**  

    > [!NOTE]
    >  โดยค่าเริ่มต้น งานที่จะถูกคัดลอกจากเท็มเพลตลงในโครงการจะถูกตั้งค่าเป็น จัดกำหนดการแล้วด้วยตนเอง  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>มอบหมายบทบาท [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ให้กับทรัพยากรโครงการ  

1.  เปิดโครงการ และเลือก ribbon ของ **งาน**  

2. เลือกเมนู **แผนภูมิ Gantt** แล้วจากนั้น เลือก **แผ่นงานทรัพยากร**  

3. บนแผ่นงานทรัพยากร เลือกเมนูแบบหล่นลงของ **บทบาททรัพยากรของ Project Service** และเลือกบทบาท Project Service Automation  

## <a name="staff-your-project-with-resources"></a>หาพนักงานให้กับโครงการของคุณพร้อมกับทรัพยากร  

1.  จากแท็บ Project Service ให้เลือกแถว และเลือก **ค้นหาทรัพยากร**  

2.  บนหน้าจอ **จองทรัพยากร** เลือกทรัพยากรที่คุณต้องการใช้สำหรับโครงการ  

3.  เลือก **จอง** และจากนั้น เลือก **ตกลง**  

## <a name="publish-your-project"></a>เผยแพร่โครงการของคุณ  
เมื่อการวางแผนโครงการของคุณเสร็จสมบูรณ์แล้ว ขั้นตอนถัดไปคือการนำเข้าและการเผยแพร่โครงการใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]  

โครงการจะนำเข้าไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] กระบวนการการกำหนดราคาและการสร้างทีมงานจะถูกนำไปใช้ เปิดโครงการใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] เพื่อดูว่ากลุ่มคน การประเมินโครงการ และโครงสร้างการแบ่งงาน ได้ถูกสร้างขึ้น ตารางต่อไปนี้แสดงตำแหน่งที่จะค้นหาผลลัพธ์


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **แผนภูมิแกนต์**   | นำเข้าลงในหน้าจอ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **โครงสร้างการแบ่งงาน** |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **รีเฟรชแผ่นงานทรัพยากร** |   นำเข้าลงในหน้าจอ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]**สมาชิกทีมโครงการ**   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **ใช้การใช้งาน**    |    นำเข้าลงในหน้าจอ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **การประเมินโครงการ**     |

**เมื่อต้องการนำเข้าและเผยแพร่โครงการของคุณ**  
1. บนแท็บ **Project Service** ไปที่ **เผยแพร่** > **โครงการ Project Service Automation ใหม่**  

2. ในกล่องโต้ตอบ **เผยแพร่ไปยังโครงการใหม่ใน Project Service** ป้อน **ชื่อโครงการ** และเลือก **ลูกค้า**  

3. อีกทางหนึ่งคือ เลือก **เชื่อมโยงแผนโครงการกับ Project Service Automation** เพื่อเชื่อมโยงไฟล์โครงการของแผนไปยัง Project Service Automation  

4. เลือก **เผยแพร่**  

   การเชื่อมโยงแฟ้มโครงการไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ทำให้แฟ้มโครงการเป็นต้นแบบ และตั้งค่าโครงสร้างการแบ่งงานใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ให้เป็นแบบอ่านอย่างเดียว  เมื่อต้องการทำการเปลี่ยนแปลงไปยังรายการแผนการของโครงการ คุณต้องดำเนินการใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] และเผยแพร่เป็นการปรับปรุงไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]  

## <a name="edit-a-project-thats-been-imported"></a>แก้ไขโครงการที่ได้มีการนำเข้า  
 เมื่อต้องการทำการเปลี่ยนแปลงไปยังการวางแผนโครงการ ที่ได้ถูกนำเข้าลงใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] คุณมีสองตัวเลือก:  

- เปิดแฟ้มหลัก และแก้ไขใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

- ยกเลิกการเชื่อมโยงแฟ้ม และแก้ไขใน Project Service โดยตรง โดยค่าเริ่มต้น โครงการที่ได้ถูกอัพโหลดจากโครงการของ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ถูกล็อก และสามารถแก้ไขได้ในโครงการเท่านั้น เมื่อต้องการแก้ไขแฟ้มใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] แฟ้มต้องถูกยกเลิกการเชื่อมโยง  

### <a name="edit-in-pn_microsoft_project"></a>แก้ไขใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. บนเมนูหลัก ไปที่ **Project Service** > **โครงการ**  

2. จากรายการของโครงการ เปิดรายการที่คุณสร้างขึ้นใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

3. เลือก **เปิดในโครงการ MS** จาก ribbon นี่จะเปิดแฟ้มหลักที่เชื่อมโยงในโครงการของ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>ยกเลิกการเชื่อมโยงแฟ้ม และแก้ไขใน Project Service ของ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. บนเมนูหลัก ไปที่ **Project Service** > **โครงการ**  

2. จากรายการของโครงการ เปิดรายการที่คุณสร้างขึ้นใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

3. เลือก **ยกเลิกการเชื่อมโยงจากโครงการ MS** จาก ribbon  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>อัพโหลดแฟ้มโครงการไปยัง SharePoint หรือกลุ่ม Office  
 คุณสามารถอัพโหลดแฟ้มโครงการของคุณไปยัง SharePoint และค้นหาภายใต้เอกสารที่เกี่ยวข้องสำหรับโครงการ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ของคุณ  คุณจำเป็นต้องให้ผู้ดูแลของคุณตั้งค่าคอนฟิกการจัดการเอกสารของ SharePoint และเปิดใช้งานสำหรับเอนทิตีของโครงการ 

 นอกจากนี้ คุณยังสามารถอัพโหลดแฟ้มโครงการของคุณไปยัง [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] ได้ ถ้าคุณได้ตั้งค่ากลุ่มของ Office

### <a name="upload-a-file-for-sharepoint"></a>อัปโหลดไฟล์ สำหรับ SharePoint  

1. บนเมนูหลัก ไปที่ **Project Service** > **อัปโหลด**  

2. เลือก **ไปยังเอกสารโครงการของ Project Service Automation**  

3. ในกล่องโต้ตอบ **เปิดใช้งานการเปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** เลือก **ใช่** หรือ **ไม่ใช่**  

   - ถ้าคุณเลือก **ใช่** คุณก็จะสามารถเลือก **เปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ใน Project Service Automation และเปิดใช้งาน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] และโหลดไฟล์โครงการจากไลบรารีเอกสาร SharePoint ได้  

   - หากคุณเลือก **ไม่** ลิงค์สำหรับ **เปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** จะไม่ทำงาน  

4. แฟ้ม [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] สามารถถูกพบได้ใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ภายใต้ **เอกสาร** สำหรับโครงการ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] เฉพาะได้  

### <a name="upload-a-file-for-office-groups"></a>อัพโหลดแฟ้มสำหรับกลุ่ม Office  

1. บนเมนูหลัก ไปที่ **Project Service** > **อัปโหลด**  

2. เลือก **ไปยังเอกสารโครงการของ Project Service Automation**  

3. ในกล่องโต้ตอบ **เปิดใช้งานการเปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** เลือก **ใช่** หรือ **ไม่ใช่**  

   - ถ้าคุณเลือก **ใช่** คุณก็จะสามารถเลือก **เปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ใน Project Service Automation และเปิดใช้งาน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] และโหลดไฟล์โครงการจากไลบรารีเอกสาร SharePoint ได้  

   - หากคุณเลือก **ไม่** ลิงค์สำหรับ **เปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** จะไม่ทำงาน  

4. แฟ้ม [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] สามารถถูกพบได้ใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ภายใต้ **เอกสาร** สำหรับโครงการ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] เฉพาะได้  

## <a name="publish--your-project-as-a-template"></a>เผยแพร่โครงการของคุณเป็นเท็มเพลต  
 คุณสามารถบันทึกโครงการของคุณ และนำมาใช้ใหม่ได้โดยการบันทึกเป็นเท็มเพลตโครงการใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] เท็มเพลตโครงการเป็นแผนโครงการที่สามารถนำมาใช้ใหม่ได้ใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างเทมเพลตโครงการ (Project Service Automation)](../psa/create-project-template.md) 

1. บนแท็บ **Project Service** ไปที่ **เผยแพร่** > **เทมเพลตโครงการ Project Service Automation ใหม่**  

2. ในกล่องโต้ตอบ **เผยแพร่ไปยังโครงการใหม่ในเทมเพลต Project Service** ป้อน **ชื่อเทมเพลตโครงการ**  

3. อีกทางหนึ่งคือ เลือก **เชื่อมโยงแผนโครงการกับ Project Service Automation** เพื่อเชื่อมโยงไฟล์โครงการไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]  

4. เลือก **เผยแพร่**  

การเชื่อมโยงแฟ้มโครงการไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ทำให้แฟ้มโครงการเป็นต้นแบบ และตั้งค่าโครงสร้างการแบ่งงานในเท็มเพลต [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ให้เป็นแบบอ่านอย่างเดียว  เมื่อต้องการทำการเปลี่ยนแปลงไปยังรายการแผนการของโครงการ คุณต้องดำเนินการใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] และเผยแพร่เป็นการปรับปรุงไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]

## <a name="read-a-resource-loaded-schedule"></a>อ่านกำหนดการที่โหลดทรัพยากร

เมื่ออ่านโครงการจาก Project Service Automation ปฏิทินของทรัพยากรจะไม่ถูกซิงโครไนซ์กับไคลเอ็นต์เดสก์ท็อป หากระยะเวลางาน ความพยายาม หรือจุดสิ้นสุด มีความแตกต่างกัน อาจเป็นเพราะทรัพยากรและไคลเอ็นต์เดสก์ท็อปไม่มีปฏิทินแม่แบบชั่วโมงการทำงานเดียวกันที่ใช้กับโครงการ


## <a name="data-synchronization"></a>การซิงโครไนซ์ข้อมูล
ตารางในส่วนนี้ให้ข้อมูลเกี่ยวกับการซิงโครไนซ์ข้อมูลเอนทิตีระหว่าง Project Service Automation และ add-in ของ Microsoft Project desktop

### <a name="project-task-entity-table"></a>ตารางเอนทิตีงานโครงการ
ตารางต่อไปนี้แสดงวิธีการซิงโครไนซ์เอนทิตีงานโครงการระหว่าง Project Service Automation และ add-in ของ Microsoft Project desktop

| **เอนทิตี** | **ฟิลด์** | **Microsoft Project ไปยัง Project Service Automation** | **Project Service Automation ไปยัง Microsoft Project** |
| --- | --- | --- | --- |
| งานโครงการ | วันครบกำหนด | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| งานโครงการ | ความพยายามโดยประมาณ | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| งานโครงการ | รหัสไคลเอ็นต์ MS Project | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| งานโครงการ | งานหลัก | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| งานโครงการ | Project | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| งานโครงการ | งานโครงการ | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| งานโครงการ | ชื่องานโครงการ | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| งานโครงการ | หน่วยการจัดเตรียมทรัพยากร (ถูกตัดออกใน v3.0) | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| งานโครงการ | ระยะเวลาตามกำหนดการ | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| งานโครงการ | วันที่เริ่มต้น | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| งานโครงการ | รหัส WBS | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |

### <a name="team-member-entity-table"></a>ตารางเอนทิตีสมาชิกของทีม
ตารางต่อไปนี้แสดงวิธีการซิงโครไนซ์ข้อมูลเอนทิตีสมาชิกของทีมระหว่าง Project Service Automation และ Micros

| **เอนทิตี** | **ฟิลด์** | **Microsoft Project ไปยัง Project Service Automation** | **Project Service Automation ไปยัง Microsoft Project** |
| --- | --- | --- | --- |
| สมาชิกของทีม | รหัสไคลเอ็นต์ MS Project | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| สมาชิกของทีม | ชื่อตำแหน่ง | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| สมาชิกของทีม | โครงการ | Synchronized | Synchronized |
| สมาชิกของทีม | ทีมโครงการ | Synchronized | Synchronized |
| สมาชิกของทีม | หน่วยการจัดเตรียมทรัพยากร | ไม่มีการทำข้อมูลให้ตรงกัน | Synchronized |
| สมาชิกของทีม | บทบาท | ไม่มีการทำข้อมูลให้ตรงกัน | Synchronized |
| สมาชิกของทีม | ชั่วโมงทำงาน | ไม่มีการทำข้อมูลให้ตรงกัน | ไม่มีการทำข้อมูลให้ตรงกัน |

### <a name="resource-assignment-entity-table"></a>ตารางเอนทิตีการมอบหมายทรัพยากร
ตารางต่อไปนี้แสดงวิธีการซิงโครไนซ์ข้อมูลเอนทิตีการมอบหมายทรัพยากรระหว่าง Project Service Automation และ Micros

| **เอนทิตี** | **ฟิลด์** | **Microsoft Project ไปยัง Project Service Automation** | **Project Service Automation ไปยัง Microsoft Project** |
| --- | --- | --- | --- |
| การมอบหมายทรัพยากร | วันที่เริ่มต้น | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| การมอบหมายทรัพยากร | จำนวนชั่วโมง | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| การมอบหมายทรัพยากร | รหัสไคลเอ็นต์ MS Project | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| การมอบหมายทรัพยากร | งานตามแผน | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| การมอบหมายทรัพยากร | Project | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| การมอบหมายทรัพยากร | ทีมโครงการ | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| การมอบหมายทรัพยากร | การมอบหมายทรัพยากร | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| การมอบหมายทรัพยากร | งาน | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| การมอบหมายทรัพยากร | จนถึงปัจจุบัน | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |

### <a name="project-task-dependencies-entity-table"></a>ตารางเอนทิตีการขึ้นต่อกันของงานโครงการ
ตารางต่อไปนี้แสดงวิธีการซิงโครไนซ์ข้อมูลเอนทิตีการขึ้นต่อกันของงานโครงการระหว่าง Project Service Automation และ Micros

| **เอนทิตี** | **ฟิลด์** | **Microsoft Project ไปยัง Project Service Automation** | **Project Service Automation ไปยัง Microsoft Project** |
| --- | --- | --- | --- |
| การขึ้นต่อกันของงานโครงการ | การขึ้นต่อกันของงานโครงการ | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| การขึ้นต่อกันของงานโครงการ | ชนิดลิงก์ | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| การขึ้นต่อกันของงานโครงการ | งานที่ต้องทำก่อน | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| การขึ้นต่อกันของงานโครงการ | Project | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |
| การขึ้นต่อกันของงานโครงการ | งานที่ตามมา | Synchronized | ไม่มีการทำข้อมูลให้ตรงกัน |

### <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม
 [คำแนะนำของผู้จัดการโครงการ](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]