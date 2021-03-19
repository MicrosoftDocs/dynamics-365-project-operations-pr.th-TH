---
title: ใช้ Add-in ของ Project Service เพื่อวางแผนการทำงานของคุณใน Microsoft Project | MicrosoftDocs
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการเพิ่ม การตั้งค่าคอนฟิก และการใช้ add-in ของ Microsoft Project สำหรับ Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 20436393aca6c16e337e06ae646b2857ef925e74
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285506"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>ใช้ Add-in Project Service Automation เพื่อวางแผนการทำงานของคุณใน Microsoft Project

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ทำให้การวางแผนโครงการของคุณ รวมถึงการประเมินง่ายขึ้นสำหรับคุณ คุณสามารถกำหนดงาน เพื่อให้ต้นทุน ความพยายาม และมูลค่าขายนั้นชัดเจน เมื่อข้อเสนอขั้นสุดท้ายถูกส่ง  

 ขณะนี้ คุณสามารถติดตั้ง [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] และทำงานด้านการวางแผนของคุณในสภาพแวดล้อมที่คุ้นเคยของ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ใช้ความสามารถในการวางแผนและการจัดการที่สมบูรณ์ของ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] แล้วอัพเดตแผนโครงการของคุณใน Project Service Automation  

> [!IMPORTANT]
> - ในการใช้คุณลักษณะการจัดการเอกสารของ SharePoint เพื่อจัดเก็บไฟล์ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ของคุณ สำหรับโครงการ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ผู้ดูแลระบบ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ของคุณ จำเป็นต้องเปิดใช้งานการจัดการเอกสาร 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] จะเข้ากันได้กับ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition เท่านั้น  

## <a name="download-and-install-the-add-in"></a>ดาวน์โหลดและติดตั้ง add-in  
 เตรียมข้อมูลการลงชื่อเข้าใช้ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ของคุณให้พร้อม คุณจะต้องใช้ข้อมูลนี้ในการเชื่อมต่อจาก [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]  

1.  จากศูนย์ดาวน์โหลด ดาวน์โหลด Add-in สำหรับรุ่นที่ได้รับการสนับสนุนของ Project Service ของคุณ ทั้ง [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) หรือ [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956)  

2.  คลิกการเชื่อมโยงดาวน์โหลด  

3.  เมื่อการดาวน์โหลดเสร็จสมบูรณ์ คลิก **ใช่** เพื่อติดตั้ง add-in  

## <a name="configure-the-add-in"></a>ตั้งค่าคอนฟิก add-in  

1. เปิดโครงการ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] และคลิกแท็บ **Project Service**  

2. คลิก **เชื่อมต่อ**  

3. ป้อนข้อมูลการเข้าสู่ระบบของคุณ และจากนั้นคลิก **ลงชื่อเข้าใช้**  

   ตอนนี้ คุณสามารถเริ่มการใช้ add-in ได้  

## <a name="read-from-a-template"></a>อ่านจากเท็มเพลต  
 อ่านจากเท็มเพลตที่คุณได้สร้างขึ้นใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] และได้คัดลอกลงใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] เพื่อเริ่มการวางแผนโครงการของคุณ [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [สร้างเท็มเพลตโครงการ (Project Service Automation)](../psa/create-project-template.md)  

1.  จากแท็บ **Project Service** คลิก **อ่าน** > **เท็มเพลต Project Service Automation**  

2.  เลือกเท็มเพลตโครงการจากรายการ และจากนั้นคลิก **เปิด**  

    > [!NOTE]
    >  โดยค่าเริ่มต้น งานที่จะถูกคัดลอกจากเท็มเพลตลงในโครงการจะถูกตั้งค่าเป็น จัดกำหนดการแล้วด้วยตนเอง  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>มอบหมายบทบาท [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ให้กับทรัพยากรโครงการ  

1.  เปิดโครงการและคลิกที่ ribbon ของ **งาน**  

2.  คลิกเมนู **แผนภูมิ Gantt** แล้วเลือก **แผ่นงานทรัพยากร**  

3.  บนแผ่นงานทรัพยากร คลิกเมนูแบบหล่นลงของ **บทบาททรัพยากรของ Project Service** และเลือกบทบาท Project Service Automation  

## <a name="staff-your-project-with-resources"></a>หาพนักงานให้กับโครงการของคุณพร้อมกับทรัพยากร  

1.  จากแท็บ Project Service ทั้งหมด ให้เลือกแถว และคลิก **ค้นหาทรัพยากร**  

2.  บนหน้าจอ **จองทรัพยากร** เลือกทรัพยากรที่คุณต้องการใช้สำหรับโครงการ  

3.  คลิก **จอง** แล้วคลิก **ถัดไป**  

## <a name="publish-your-project"></a>เผยแพร่โครงการของคุณ  
เมื่อการวางแผนโครงการของคุณเสร็จสมบูรณ์แล้ว ขั้นตอนถัดไปคือการนำเข้าและการเผยแพร่โครงการใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]  

โครงการจะนำเข้าไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] กระบวนการการกำหนดราคาและการสร้างทีมงานจะถูกนำไปใช้ เปิดโครงการใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] เพื่อดูว่ากลุ่มคน การประเมินโครงการ และโครงสร้างการแบ่งงาน ได้ถูกสร้างขึ้น ตารางต่อไปนี้แสดงตำแหน่งที่จะพบผลลัพธ์:


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **แผนภูมิแกนต์**   | นำเข้าลงในหน้าจอ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **โครงสร้างการแบ่งงาน** |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **รีเฟรชแผ่นงานทรัพยากร** |   นำเข้าลงในหน้าจอ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]**สมาชิกทีมโครงการ**   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **ใช้การใช้งาน**    |    นำเข้าลงในหน้าจอ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **การประเมินโครงการ**     |

**เมื่อต้องการนำเข้าและเผยแพร่โครงการของคุณ**  
1. จากแท็บ **Project Service** คลิก **เผยแพร่** > **Project Service Automation ใหม่**  

2. ในกล่องโต้ตอบ **เผยแพร่ไปยังโครงการใหม่ใน Project Service** ป้อน **ชื่อโครงการ** และเลือก **ลูกค้า**  

3. สามารถเลือกที่จะตรวจสอบ **เชื่อมโยงแผนงานโครงการกับ Project Service Automation** เพื่อเชื่อมโยงแฟ้มโครงการของแผนไปยัง Project Service Automation  

4. คลิก **เผยแพร่**  

   การเชื่อมโยงแฟ้มโครงการไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ทำให้แฟ้มโครงการเป็นต้นแบบ และตั้งค่าโครงสร้างการแบ่งงานใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ให้เป็นแบบอ่านอย่างเดียว  เมื่อต้องการทำการเปลี่ยนแปลงไปยังรายการแผนการของโครงการ คุณต้องดำเนินการใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] และเผยแพร่เป็นการปรับปรุงไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]  

## <a name="edit-a-project-thats-been-imported"></a>แก้ไขโครงการที่ได้มีการนำเข้า  
 เมื่อต้องการทำการเปลี่ยนแปลงไปยังการวางแผนโครงการ ที่ได้ถูกนำเข้าลงใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] คุณมีสองตัวเลือก:  

- เปิดแฟ้มหลัก และแก้ไขใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

- ยกเลิกการเชื่อมโยงแฟ้ม และแก้ไขใน Project Service โดยตรง โดยค่าเริ่มต้น โครงการที่ได้ถูกอัพโหลดจากโครงการของ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ถูกล็อก และสามารถแก้ไขได้ในโครงการเท่านั้น เมื่อต้องการแก้ไขแฟ้มใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] แฟ้มต้องถูกยกเลิกการเชื่อมโยง  

### <a name="edit-in-pn_microsoft_project"></a>แก้ไขใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. จากเมนูหลัก คลิก **Project Service** > **โครงการ**  

2. จากรายการของโครงการ เปิดรายการที่คุณสร้างขึ้นใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

3. คลิก **เปิดในโครงการ MS** จาก ribbon นี่จะเปิดแฟ้มหลักที่เชื่อมโยงในโครงการของ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>ยกเลิกการเชื่อมโยงแฟ้ม และแก้ไขใน Project Service ของ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. จากเมนูหลัก คลิก **Project Service** > **โครงการ**  

2. จากรายการของโครงการ เปิดรายการที่คุณสร้างขึ้นใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

3. คลิก **ยกเลิกการเชื่อมโยงจากโครงการ MS** จาก ribbon  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>อัพโหลดแฟ้มโครงการไปยัง SharePoint หรือกลุ่ม Office  
 คุณสามารถอัพโหลดแฟ้มโครงการของคุณไปยัง SharePoint และค้นหาภายใต้เอกสารที่เกี่ยวข้องสำหรับโครงการ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ของคุณ  คุณจำเป็นต้องให้ผู้ดูแลของคุณตั้งค่าคอนฟิกการจัดการเอกสารของ SharePoint และเปิดใช้งานสำหรับเอนทิตีของโครงการ 

 นอกจากนี้ คุณยังสามารถอัพโหลดแฟ้มโครงการของคุณไปยัง [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] ได้ ถ้าคุณได้ตั้งค่ากลุ่มของ Office

### <a name="upload-a-file-for-sharepoint"></a>อัปโหลดไฟล์ สำหรับ SharePoint  

1. จากเมนูหลัก คลิก **Project Service** > **อัพโหลด**  

2. เลือก **ไปยังเอกสารโครงการของ Project Service Automation**  

3. ในกล่องโต้ตอบ **เปิดใช้งานการเปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** เลือก **ใช่** หรือ **ไม่ใช่**  

   - เมื่อคุณคลิก **ใช่** คุณจะสามารถเลือกปุ่ม **เปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ใน Project Service Automation เปิดใช้งาน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] และโหลดแฟ้มโครงการจากไลบรารีเอกสาร SharePoint  

   - หากคุณคลิก **ไม่ใช่** การเชื่อมโยงสำหรับปุ่ม **เปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** จะไม่ทำงาน  

4. แฟ้ม [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] สามารถถูกพบได้ใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ภายใต้ **เอกสาร** สำหรับโครงการ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] เฉพาะได้  

### <a name="upload-a-file-for-office-groups"></a>อัพโหลดแฟ้มสำหรับกลุ่ม Office  

1. จากเมนูหลัก คลิก **Project Service** > **อัพโหลด**  

2. เลือก **ไปยังเอกสารโครงการของ Project Service Automation**  

3. ในกล่องโต้ตอบ **เปิดใช้งานการเปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** เลือก **ใช่** หรือ **ไม่ใช่**  

   - เมื่อคุณคลิก **ใช่** คุณจะสามารถเลือกปุ่ม **เปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ใน Project Service Automation เปิดใช้งาน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] และโหลดแฟ้มโครงการจากไลบรารีเอกสาร SharePoint  

   - หากคุณคลิก **ไม่ใช่** การเชื่อมโยงสำหรับปุ่ม **เปิดใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** จะไม่ทำงาน  

4. แฟ้ม [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] สามารถถูกพบได้ใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ภายใต้ **เอกสาร** สำหรับโครงการ [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] เฉพาะได้  

## <a name="publish--your-project-as-a-template"></a>เผยแพร่โครงการของคุณเป็นเท็มเพลต  
 คุณสามารถบันทึกโครงการของคุณ และนำมาใช้ใหม่ได้โดยการบันทึกเป็นเท็มเพลตโครงการใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]  เท็มเพลตโครงการเป็นแผนโครงการที่สามารถนำมาใช้ใหม่ได้ใน [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [สร้างเท็มเพลตโครงการ (Project Service Automation)](../psa/create-project-template.md)  

1. จากแท็บ **Project Service** คลิก **เผยแพร่** > **เท็มเพลตโครงการ Project Service Automation ใหม่**  

2. ในกล่องโต้ตอบ **เผยแพร่ไปยังโครงการใหม่ในเท็มเพลต Project Service** ป้อน **ชื่อเท็มเพลตโครงการ**  

3. หรือสามารถเลือกตรวจสอบ **เชื่อมโยงแผนงานโครงการกับ Project Service Automation** เพื่อเชื่อมโยงแฟ้มโครงการไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]  

4. คลิก **เผยแพร่**  

การเชื่อมโยงแฟ้มโครงการไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ทำให้แฟ้มโครงการเป็นต้นแบบ และตั้งค่าโครงสร้างการแบ่งงานในเท็มเพลต [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ให้เป็นแบบอ่านอย่างเดียว  เมื่อต้องการทำการเปลี่ยนแปลงไปยังรายการแผนการของโครงการ คุณต้องดำเนินการใน [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] และเผยแพร่เป็นการปรับปรุงไปยัง [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]

## <a name="read-a-resource-loaded-schedule"></a>อ่านกำหนดการที่โหลดทรัพยากร

เมื่ออ่านโครงการจาก Project Service Automation ปฏิทินของทรัพยากรจะไม่ถูกซิงโครไนซ์กับไคลเอ็นต์เดสก์ท็อป หากระยะเวลางาน ความพยายาม หรือจุดสิ้นสุด มีความแตกต่างกัน อาจเป็นเพราะทรัพยากรและไคลเอ็นต์เดสก์ท็อปไม่มีปฏิทินแม่แบบชั่วโมงการทำงานเดียวกันที่ใช้กับโครงการ


## <a name="data-synchronization"></a>การซิงโครไนซ์ข้อมูล

ตารางต่อไปนี้แสดงวิธีการซิงโครไนซ์ข้อมูลระหว่าง Project Service Automation และ Microsoft Project desktop add-in

| **เอนทิตี** | **ฟิลด์** | **Microsoft Project ไปยัง Project Service Automation** | **Project Service Automation ไปยัง Microsoft Project** |
| --- | --- | --- | --- |
| งานโครงการ | วันครบกำหนด | ● | - |
| งานโครงการ | ความพยายามโดยประมาณ | ● | - |
| งานโครงการ | รหัสไคลเอ็นต์ MS Project | ● | - |
| งานโครงการ | งานหลัก | ● | - |
| งานโครงการ | Project | ● | - |
| งานโครงการ | งานโครงการ | ● | - |
| งานโครงการ | ชื่องานโครงการ | ● | - |
| งานโครงการ | หน่วยการจัดเตรียมทรัพยากร (ถูกตัดออกใน v3.0) | ● | - |
| งานโครงการ | ระยะเวลาตามกำหนดการ | ● | - |
| งานโครงการ | วันที่เริ่ม | ● | - |
| งานโครงการ | รหัส WBS | ● | - |

| **เอนทิตี** | **ฟิลด์** | **Microsoft Project ไปยัง Project Service Automation** | **Project Service Automation ไปยัง Microsoft Project** |
| --- | --- | --- | --- |
| สมาชิกของทีม | รหัสไคลเอ็นต์ MS Project | ● | - |
| สมาชิกของทีม | ชื่อตำแหน่ง | ● | - |
| สมาชิกของทีม | โครงการ | ● | ● |
| สมาชิกของทีม | ทีมโครงการ | ● | ● |
| สมาชิกของทีม | หน่วยการจัดเตรียมทรัพยากร | - | ● |
| สมาชิกของทีม | บทบาท | - | ● |
| สมาชิกของทีม | ชั่วโมงทำงาน | ไม่ได้ซิงค์ | ไม่ได้ซิงค์ |

| **เอนทิตี** | **ฟิลด์** | **Microsoft Project ไปยัง Project Service Automation** | **Project Service Automation ไปยัง Microsoft Project** |
| --- | --- | --- | --- |
| การมอบหมายทรัพยากร | วันที่เริ่มต้น | ● | - |
| การมอบหมายทรัพยากร | จำนวนชั่วโมง | ● | - |
| การมอบหมายทรัพยากร | รหัสไคลเอ็นต์ MS Project | ● | - |
| การมอบหมายทรัพยากร | งานตามแผน | ● | - |
| การมอบหมายทรัพยากร | Project | ● | - |
| การมอบหมายทรัพยากร | ทีมโครงการ | ● | - |
| การมอบหมายทรัพยากร | การมอบหมายทรัพยากร | ● | - |
| การมอบหมายทรัพยากร | งาน | ● | - |
| การมอบหมายทรัพยากร | จนถึงปัจจุบัน | ● | - |

| **เอนทิตี** | **ฟิลด์** | **Microsoft Project ไปยัง Project Service Automation** | **Project Service Automation ไปยัง Microsoft Project** |
| --- | --- | --- | --- |
| การขึ้นต่อกันของงานโครงการ | การขึ้นต่อกันของงานโครงการ | ● | - |
| การขึ้นต่อกันของงานโครงการ | ชนิดลิงก์ | ● | - |
| การขึ้นต่อกันของงานโครงการ | งานที่ต้องทำก่อน | ● | - |
| การขึ้นต่อกันของงานโครงการ | Project | ● | - |
| การขึ้นต่อกันของงานโครงการ | งานที่ตามมา | ● | - |

### <a name="see-also"></a>ดูเพิ่มเติม  
 [คำแนะนำของผู้จัดการโครงการ](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]