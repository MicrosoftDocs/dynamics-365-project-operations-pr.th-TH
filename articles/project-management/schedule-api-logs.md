---
title: บันทึกการจัดกำหนดการโครงการ
description: บทความนี้ให้ข้อมูลและตัวอย่างที่จะช่วยให้คุณใช้บันทึกการจัดกำหนดการโครงการเพื่อติดตามความล้มเหลวที่เกี่ยวข้องกับบริการจัดกำหนดการโครงการและ API การจัดกำหนดการโครงการ
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923718"
---
# <a name="project-scheduling-logs"></a>บันทึกการจัดกำหนดการโครงการ

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_, _Project for the Web_

Microsoft Dynamics 365 Project Operations ใช้ [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) เป็นเครื่องมือการจัดกำหนดการโครงการหลัก แทนการใช้ Application Programming Interface (API) ของเว็ปแอปพลิเคชัน Microsoft Dataverse Project Operations ใช้ API การจัดกำหนดการโครงการใหม่เพื่อสร้าง ปรับปรุง และลบงานโครงการ การกำหนดทรัพยากร การขึ้นต่อกันของงาน บักเก็ตโครงการ และสมาชิกทีมโครงการ อย่างไรก็ตาม เมื่อสร้าง ปรับปรุง หรือลบการดำเนินการโดยทางโปรแกรมกับเอนทิตีโครงสร้างการแบ่งงาน (WBS) อาจเกิดข้อผิดพลาดขึ้นได้ เพื่อติดตามข้อผิดพลาดและประวัติการดำเนินงานเหล่านี้ มีการนำบันทึกการดูแลระบบใหม่มาใช้สองรายการ: **ชุดการดำเนินงาน** และ **บริการจัดกำหนดการโครงการ (PSS)** หากต้องการเข้าถึงบันทึกเหล่านี้ ให้ไปที่ **การตั้งค่า** \> **การรวมกำหนดการ**

แผนภาพต่อไปนี้แสดงแบบจำลองข้อมูลสำหรับบันทึกการจัดกำหนดการโครงการ

![รูปแบบข้อมูลสำหรับบันทึกการจัดกำหนดการโครงการ](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>บันทึกชุดการดำเนินงาน

บันทึกชุดการดำเนินงานจะติดตามการดำเนินการของชุดการดำเนินงานที่ใช้ในการเรียกใช้การดำเนินการสร้าง ปรับปรุง หรือลบหนึ่งรายการหรือจำนวนมากในชุดงานของโครงการ งานโครงการ การกำหนดทรัพยากร การขึ้นต่อกันของงาน บักเก็ตโครงการ หรือสมาชิกทีมโครงการ ฟิลด์ **สถานะของการดำเนินงาน** แสดงสถานะโดยรวมของชุดการดำเนินงาน รายละเอียดของส่วนข้อมูลชุดการดำเนินงานจะบันทึกไว้ในเรกคอร์ดรายละเอียดชุดการดำเนินงานที่เกี่ยวข้อง

### <a name="operation-set"></a>ชุดการดำเนินงาน

ตารางต่อไปนี้แสดงฟิลด์ที่เกี่ยวข้องกับเอนทิตี **ชุดการดำเนินงาน**

| ชื่อ Schema            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | วันที่/เวลาที่ชุดการดำเนินงานเสร็จสิ้นหรือล้มเหลว                                                | CompletedOn            |
| msdyn_correlationid   | ค่า **correlationId** ของคำขอ                                                                  | CorrelationId          |
| msdyn_description     | คำอธิบายของชุดการดำเนินงาน                                                                        | Description            |
| msdyn_executedon      | วันที่/เวลาที่มีการเรียกใช้เรกคอร์ด                                                                       | ดำเนินการเมื่อ            |
| msdyn_operationsetId  | รหัสเฉพาะของอินสแตนซ์เอนทิตี                                                                   | OperationSet           |
| msdyn_Project         | โครงการที่เกี่ยวข้องกับชุดการดำเนินงาน                                                            | Project                |
| msdyn_projectid       | ค่า **projectId** ของคำขอ                                                                      | ProjectId (ไม่สนับสนุน) |
| msdyn_projectName     | ไม่สามารถใช้งานได้                                                                                              | ไม่สามารถใช้งานได้         |
| msdyn_PSSErrorLog     | รหัสเฉพาะของบันทึกข้อพลาดของการจัดกำหนดการโครงการที่เกี่ยวข้องกับชุดการดำเนินงาน | บันทึกข้อผิดพลาด PSS          |
| msdyn_PSSErrorLogName | ไม่สามารถใช้งานได้                                                                                              | ไม่สามารถใช้งานได้         |
| msdyn_status          | สถานะของชุดการดำเนินงาน                                                                             | Status                 |
| msdyn_statusName      | ไม่สามารถใช้งานได้                                                                                              | ไม่สามารถใช้งานได้         |
| msdyn_useraadid       | รหัสออบเจ็กต์ Azure Active Directory (Azure AD) ของผู้ใช้ที่มีคำขออยู่                     | UserAADID              |

### <a name="operation-set-detail"></a>รายละเอียดชุดการดำเนินงาน

ตารางต่อไปนี้แสดงฟิลด์ที่เกี่ยวข้องกับเอนทิตี **รายละเอียดชุดการดำเนินงาน**

| ชื่อ Schema                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | ฟิลด์ Dataverse ที่ซีเรียลไลซ์สำหรับคำขอ                                            | CdsPayload            |
| msdyn_entityname           | ชื่อของเอนทิตีสำหรับคำขอ                                                     | EntityName            |
| msdyn_httpverb             | วิธีการร้องขอ                                                                         | คำสั่งการกระทำของ HTTP (ไม่สนับสนุน) |
| msdyn_httpverbName         | ไม่สามารถใช้งานได้                                                                             | ไม่สามารถใช้งานได้        |
| msdyn_operationset         | รหัสเฉพาะของชุดการดำเนินงานที่มีเรกคอร์ดอยู่                      | OperationSet          |
| msdyn_operationsetdetailId | รหัสเฉพาะของอินสแตนซ์เอนทิตี                                                  | รายละเอียด OperationSet   |
| msdyn_operationsetName     | ไม่สามารถใช้งานได้                                                                             | ไม่สามารถใช้งานได้        |
| msdyn_operationtype        | ชนิดการดำเนินงานของรายละเอียดชุดการดำเนินงาน                                             | ชนิดของการดำเนินการ         |
| msdyn_operationtypeName    | ไม่สามารถใช้งานได้                                                                             | ไม่สามารถใช้งานได้        |
| msdyn_psspayload           | ฟิลด์ของบริการจัดกำหนดการโครงการที่ซีเรียลไลซ์สำหรับคำขอ                           | PssPayload            |
| msdyn_recordid             | ตัวระบุของเรกคอร์ดคำขอ                                                       | รหัสเรกคอร์ด             |
| msdyn_requestnumber        | หมายเลขที่สร้างขึ้นโดยอัตโนมัติที่ใช้เพื่อระบุลำดับของคำขอที่ได้รับ | หมายเลขคำขอ        |

## <a name="project-scheduling-service-error-logs"></a>บันทึกข้อผิดพลาดของบริการจัดกำหนดการโครงการ

บันทึกข้อผิดพลาดของบริการจัดกำหนดการโครงการจะบันทึกความล้มเหลวที่เกิดขึ้นเมื่อบริการจัดกำหนดการโครงการ พยายามดำเนินงาน **บันทึก** หรือ **เปิด** เมื่อมีการสร้างบันทึกเหล่านี้ มีสามสถานการณ์ที่รองรับ:

- การดำเนินการที่เริ่มต้นโดยผู้ใช้ล้มเหลวอย่างมาก (เช่น สร้างการมอบหมายไม่ได้เนื่องจากไม่มีสิทธิ์)
- บริการจัดกำหนดการโครงการไม่สามารถสร้าง ปรับปรุง ลบ หรือดำเนินงานตามขั้นตอนอื่นๆ ในเอนทิตีโดยทางโปรแกรม
- ผู้ใช้พบข้อผิดพลาดเมื่อเรกคอร์ดไม่สามารถเปิดได้ (ตัวอย่างเช่น เมื่อเปิดโครงการหรือมีการปรับปรุงข้อมูลของสมาชิกทีม)

### <a name="project-scheduling-service-log"></a>บันทึกของบริการจัดกำหนดการโครงการ

ตารางต่อไปนี้แสดงฟิลด์ที่มีอยู่ในบันทึกของบริการจัดกำหนดการโครงการ

| ชื่อ Schema          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | สแตกการเรียกของข้อยกเว้น                                               | สแตกการเรียก     |
| msdyn_correlationid | รหัสความสัมพันธ์ของข้อผิดพลาด                                               | CorrelationId  |
| msdyn_errorcode     | ฟิลด์ที่ใช้จัดเก็บหัสข้อผิดพลาดหรือรหัสข้อผิดพลาด HTTP ของ Dataverse | รหัสข้อผิดพลาด     |
| msdyn_HelpLink      | ลิงก์ไปยังคู่มือวิธีใช้สำหรับบุคคลทั่วไป                                       | ลิงก์ความช่วยเหลือ      |
| msdyn_log           | บันทึกจากบริการจัดกำหนดการโครงการ                                   | แฟ้มบันทึก            |
| msdyn_project       | โครงการที่เชื่อมโยงกับบันทึกข้อผิดพลาด                             | Project        |
| msdyn_projectName   | ชื่อของโครงการถ้าส่วนข้อมูลของชุดการดำเนินงานจะคงอยู่ | ไม่สามารถใช้งานได้ |
| msdyn_psserrorlogId | รหัสเฉพาะของอินสแตนซ์เอนทิตี                                     | บันทึกข้อผิดพลาด PSS  |
| msdyn_SessionId     | รหัสเซสชันของโครงการ                                                        | รหัสเซสชัน     |

## <a name="error-log-cleanup"></a>การล้างข้อมูลบันทึกข้อผิดพลาด

โดยค่าเริ่มต้น ทั้งบันทึกข้อผิดพลาดของบริการจัดกำหนดการโครงการและบันทึกชุดการดำเนินงานสามารถล้างข้อมูลได้ทุกๆ 90 วัน เรกคอร์ดใดๆ ที่เก่ากว่า 90 วันจะถูกลบออก อย่างไรก็ตาม การเปลี่ยนค่าของฟิลด์ **msdyn_StateOperationSetAge** ในเพจ **พารามิเตอร์โครงการ** ผู้ดูแลระบบสามารถปรับช่วงเวลาการล้างข้อมูลให้อยู่ระหว่าง 1 ถึง 120 วันได้ การเปลี่ยนค่านี้มีหลายวิธี:

- ปรับแต่งเอนทิตี **พารามิเตอร์โครงการ** โดยการสร้างเพจแบบกำหนดเองและเพิ่มฟิลด์ **อายุชุดการดำเนินงานของเก่า**
- ใช้รหัสไคลเอ็นต์ที่ใช้ [ชุดพัฒนาซอฟต์แวร์ WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord)
- ใช้โค้ด Service SDK ที่ใช้วิธีการ Xrm SDK **updateRecord** (การอ้างอิง API ของไคลเอ็นต์) ในแอปแบบจำลอง Power Apps มีคำอธิบายและพารามิเตอร์ที่รองรับสำหรับวิธีการ **updateRecord**

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
