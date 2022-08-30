---
title: ใช้ API กำหนดการโครงการเพื่อดำเนินการกับเอนทิตีการจัดกำหนดการ
description: บทความนี้ให้ข้อมูลและตัวอย่างสำหรับการใช้ API กำหนดการโครงการ
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3248a057b831d81fdc2bc198b4ed4da5e46462f2
ms.sourcegitcommit: 8edd24201cded2672cec16cd5dc84c6a3516b6c2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/06/2022
ms.locfileid: "9230339"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>ใช้ API กำหนดการโครงการเพื่อดำเนินการกับเอนทิตีการจัดกำหนดการ

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_



## <a name="scheduling-entities"></a>เอนทิตีการจัดกำหนดการ

API กำหนดการโครงการให้ความสามารถในการสร้าง อัปเดต และลบการดำเนินการด้วย **เอนทิตีการจัดกำหนดการ** เอนทิตีเหล่านี้ได้รับการจัดการผ่านกลไกการจัดกำหนดการในโครงการสำหรับเว็บ สร้าง ปรับปรุง และลบการดำเนินงานกับ **เอนทิตีการจัดกำหนดการ** มีการจำกัดใน Dynamics 365 Project Operations รุ่นก่อนหน้า

ตารางต่อไปนี้แสดงรายการเอนทิตีกำหนดการโครงการทั้งหมด

| ชื่อเอนทิตี  | ชื่อตรรกะของเอนทิตี |
| --- | --- |
| Project | msdyn_project |
| งานโครงการ  | msdyn_projecttask  |
| การขึ้นต่อกันของงานโครงการ  | msdyn_projecttaskdependency  |
| การมอบหมายทรัพยากร | msdyn_resourceassignment |
| บักเก็ตโครงการ  | msdyn_projectbucket |
| สมาชิกของทีมโครงการ | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet เป็นรูปแบบหน่วยการทำงานที่สามารถใช้เมื่อต้องดำเนินการตามกำหนดการหลายรายการที่ส่งผลกระทบต่อคำขอภายในธุรกรรม

## <a name="project-schedule-apis"></a>API กำหนดการโครงการ

ต่อไปนี้คือรายการ API กำหนดการโครงการปัจจุบัน

- **msdyn_CreateProjectV1**: API นี้สามารถใช้ในการสร้างโครงการ ระบบจะสร้างโครงการและบักเก็ตโปรเจ็กต์เริ่มต้นในทันที
- **msdyn_CreateTeamMemberV1**: API นี้สามารถใช้เพื่อสร้างสมาชิกทีมโครงการ โดยจะมีการสร้างสมาชิกทีมในทันที
- **msdyn_CreateOperationSetV1**: API นี้สามารถใช้เพื่อจัดกำหนดการคำขอต่างๆ ที่ต้องดำเนินการภายในธุรกรรม
- **msdyn_PssCreateV1**: API นี้สามารถใช้เพื่อสร้างเอนทิตี เอนทิตีสามารถเป็นเอนทิตีการจัดกำหนดการโครงการใดๆ ที่สนับสนุนการดำเนินการสร้าง
- **msdyn_PssUpdateV1**: API นี้สามารถใช้เพื่อปรับปรุงเอนทิตี เอนทิตีสามารถเป็นเอนทิตีการจัดกำหนดการโครงการใดๆ ที่สนับสนุนการดำเนินการอัปเดต
- **msdyn_PssDeleteV1**: API นี้สามารถใช้เพื่อลบเอนทิตี เอนทิตีสามารถเป็นเอนทิตีการจัดกำหนดการโครงการใดๆ ที่สนับสนุนการดำเนินการลบ
- **msdyn_ExecuteOperationSetV1**: API นี้ใช้เพื่อดำเนินงานทั้งหมดภายในชุดการดำเนินงานที่กำหนด

## <a name="using-project-schedule-apis-with-operationset"></a>การใช้ API กำหนดการโครงการกับ OperationSet

เนื่องจากเรกคอร์ด **CreateProjectV1** และ **CreateTeamMemberV1** ทั้งคู่มีการสร้างขึ้นในทันที API เหล่านี้จึงไม่สามารถใช้ใน **OperationSet** ได้โดยตรง อย่างไรก็ตาม คุณสามารถใช้ API ดังกล่าวเพื่อสร้างเรกคอร์ดที่จำเป็น สร้าง **OperationSet** จากนั้นใช้เรกคอร์ดที่สร้างไว้ล่วงหน้าเหล่านี้ใน **OperationSet**

## <a name="supported-operations"></a>การดำเนินการที่รองรับ

| เอนทิตีการจัดกำหนดการ | สร้าง | ปรับปรุง | Delete | ข้อควรพิจารณาที่สำคัญ |
| --- | --- | --- | --- | --- |
งานโครงการ | ตกลง | ตกลง | ตกลง | ฟิลด์ **ความคืบหน้า**, **EffortCompleted** และ **EffortRemaining** สามารถแก้ไขได้ใน Project for the Web แต่ไม่สามารถแก้ไขใน Project Operations  |
| การขึ้นต่อกันของงานโครงการ | ตกลง |  | ตกลง | ไม่ปรับปรุงเรกคอร์ดการขึ้นต่อกันของงานโครงการ แต่สามารถลบเรกคอร์ดเก่าและสร้างเรกคอร์ดใหม่ได้ |
| การกำหนดทรัพยากร | ตกลง | ตกลง | | ไม่รองรับการดำเนินการกับฟิลด์ต่อไปนี้: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** และ **PlannedWork** ไม่ปรับปรุงเรกคอร์ดการกำหนดทรัพยากร แต่สามารถลบเรกคอร์ดเก่าและสร้างเรกคอร์ดใหม่ได้ |
| บักเก็ตโครงการ | ตกลง | ตกลง | ตกลง | มีการสร้างบักเก็ตเริ่มต้นโดยใช้ **CreateProjectV1** API มีการเพิ่มการสนับสนุนสำหรับการสร้างและการลบบักเก็ตโครงการในการปรับปรุงรุ่น 16 |
| สมาชิกของทีมโครงการ | ตกลง | ตกลง | ตกลง | สำหรับการดำเนินการสร้าง ให้ใช้ **CreateTeamMemberV1** API |
| Project | ตกลง | ตกลง |  | ไม่รองรับการดำเนินการกับฟิลด์ต่อไปนี้: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** และ **Duration** |

API เหล่านี้สามารถเรียกใช้กับเอนทิตีอ็อบเจ็กต์ที่มีฟิลด์แบบกำหนดเอง

รหัสคุณสมบัติเป็นแบบระบุหรือไม่ก็ได้ หากระบุ ระบบจะพยายามใช้และแสดงข้อยกเว้นหากไม่สามารถใช้งานได้ หากไม่ระบบ ระบบจะสร้างขึ้นเอง

## <a name="restricted-fields"></a>ฟิลด์ที่ถูกจำกัด

ตารางต่อไปนี้กำหนดฟิลด์ที่ถูกจำกัดจาก **สร้าง** และ **แก้ไข**

### <a name="project-task"></a>งานโครงการ

| ชื่อตรรกะ                           | สามารถสร้าง     | สามารถแก้ไข         |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | ไม่             | ไม่               |
| msdyn_actualcost_base                  | ไม่             | ไม่               |
| msdyn_actualend                        | ไม่             | ไม่               |
| msdyn_actualend                      | ไม่             | ไม่               |
| msdyn_actualsales_base                 | ไม่             | ไม่               |
| msdyn_actualstart                      | ไม่             | ไม่               |
| msdyn_costatcompleteestimate           | ไม่             | ไม่               |
| msdyn_costatcompleteestimate_base      | ไม่             | ไม่               |
| msdyn_costconsumptionpercentage        | ไม่             | ไม่               |
| msdyn_effortcompleted                  | ไม่ (ใช่สำหรับโครงการ)             | ไม่ (ใช่สำหรับโครงการ)               |
| msdyn_effortremaining                  | ไม่ (ใช่สำหรับโครงการ)              | ไม่ (ใช่สำหรับโครงการ)                |
| msdyn_effortestimateatcomplete         | ไม่             | ไม่               |
| msdyn_iscritical                       | ไม่             | ไม่               |
| msdyn_iscriticalname                   | ไม่             | ไม่               |
| msdyn_ismanual                         | ไม่             | ไม่               |
| msdyn_ismanualname                     | ไม่             | ไม่               |
| msdyn_ismilestone                      | ไม่             | ไม่               |
| msdyn_ismilestonename                  | ไม่             | ไม่               |
| msdyn_LinkStatus                       | ไม่             | ไม่               |
| msdyn_linkstatusname                   | ไม่             | ไม่               |
| msdyn_msprojectclientid                | ไม่             | ไม่               |
| msdyn_plannedcost                      | ไม่             | ไม่               |
| msdyn_plannedcost_base                 | ไม่             | ไม่               |
| msdyn_plannedsales                     | ไม่             | ไม่               |
| msdyn_plannedsales_base                | ไม่             | ไม่               |
| msdyn_pluginprocessingdata             | ไม่             | ไม่               |
| msdyn_progress                         | ไม่ (ใช่สำหรับโครงการ)             | ไม่ (ใช่สำหรับโครงการ) |
| msdyn_remainingcost                    | ไม่             | ไม่               |
| msdyn_remainingcost_base               | ไม่             | ไม่               |
| msdyn_remainingsales                   | ไม่             | ไม่               |
| msdyn_remainingsales_base              | ไม่             | ไม่               |
| msdyn_requestedhours                   | ไม่             | ไม่               |
| msdyn_resourcecategory                 | ไม่             | ไม่               |
| msdyn_resourcecategoryname             | ไม่             | ไม่               |
| msdyn_resourceorganizationalunitid     | ไม่             | ไม่               |
| msdyn_resourceorganizationalunitidname | ไม่             | ไม่               |
| msdyn_salesconsumptionpercentage       | ไม่             | ไม่               |
| msdyn_salesestimateatcomplete          | ไม่             | ไม่               |
| msdyn_salesestimateatcomplete_base     | ไม่             | ไม่               |
| msdyn_salesvariance                    | ไม่             | ไม่               |
| msdyn_salesvariance_base               | ไม่             | ไม่               |
| msdyn_scheduleddurationminutes         | ไม่             | ไม่               |
| msdyn_scheduledend                     | ไม่             | ไม่               |
| msdyn_scheduledstart                   | ไม่             | ไม่               |
| msdyn_schedulevariance                 | ไม่             | ไม่               |
| msdyn_skipupdateestimateline           | ไม่             | ไม่               |
| msdyn_skipupdateestimatelinename       | ไม่             | ไม่               |
| msdyn_summary                          | ไม่             | ไม่               |
| msdyn_varianceofcost                   | ไม่             | ไม่               |
| msdyn_varianceofcost_base              | ไม่             | ไม่               |

### <a name="project-task-dependency"></a>การขึ้นต่อกันของงานโครงการ

| ชื่อตรรกะ                  | สามารถสร้าง     | สามารถแก้ไข     |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | ไม่             | ไม่           |
| msdyn_linktypename            | ไม่             | ไม่           |
| msdyn_predecessortask         | ตกลง            | ไม่           |
| msdyn_predecessortaskname     | ตกลง            | ไม่           |
| msdyn_project                 | ตกลง            | ไม่           |
| msdyn_projectname             | ตกลง            | ไม่           |
| msdyn_projecttaskdependencyid | ตกลง            | ไม่           |
| msdyn_successortask           | ตกลง            | ไม่           |
| msdyn_successortaskname       | ตกลง            | ไม่           |

### <a name="resource-assignment"></a>การกำหนดทรัพยากร

| ชื่อตรรกะ                 | สามารถสร้าง     | สามารถแก้ไข     |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | ตกลง            | ไม่           |
| msdyn_bookableresourceidname | ตกลง            | ไม่           |
| msdyn_bookingstatusid        | ไม่             | ไม่           |
| msdyn_bookingstatusidname    | ไม่             | ไม่           |
| msdyn_committype             | ไม่             | ไม่           |
| msdyn_committypename         | ไม่             | ไม่           |
| msdyn_effort                 | ไม่             | ไม่           |
| msdyn_effortcompleted        | ไม่             | ไม่           |
| msdyn_effortremaining        | ไม่             | ไม่           |
| msdyn_finish                 | ไม่             | ไม่           |
| msdyn_plannedcost            | ไม่             | ไม่           |
| msdyn_plannedcost_base       | ไม่             | ไม่           |
| msdyn_plannedcostcontour     | ไม่             | ไม่           |
| msdyn_plannedsales           | ไม่             | ไม่           |
| msdyn_plannedsales_base      | ไม่             | ไม่           |
| msdyn_plannedsalescontour    | ไม่             | ไม่           |
| msdyn_plannedwork            | ไม่             | ไม่           |
| msdyn_projectid              | ตกลง            | ไม่           |
| msdyn_projectidname          | ไม่             | ไม่           |
| msdyn_projectteamid          | ไม่             | ไม่           |
| msdyn_projectteamidname      | ไม่             | ไม่           |
| msdyn_start                  | ไม่             | ไม่           |
| msdyn_taskid                 | ไม่             | ไม่           |
| msdyn_taskidname             | ไม่             | ไม่           |
| msdyn_userresourceid         | ไม่             | ไม่           |

### <a name="project-team-member"></a>สมาชิกของทีมโครงการ

| ชื่อตรรกะ                                     | สามารถสร้าง     | สามารถแก้ไข     |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | ไม่             | ไม่           |
| msdyn_creategenericteammemberwithrequirementname | ไม่             | ไม่           |
| msdyn_deletestatus                               | ไม่             | ไม่           |
| msdyn_deletestatusname                           | ไม่             | ไม่           |
| msdyn_effort                                     | ไม่             | ไม่           |
| msdyn_effortcompleted                            | ไม่             | ไม่           |
| msdyn_effortremaining                            | ไม่             | ไม่           |
| msdyn_finish                                     | ไม่             | ไม่           |
| msdyn_hardbookedhours                            | ไม่             | ไม่           |
| msdyn_hours                                      | ไม่             | ไม่           |
| msdyn_markedfordeletiontimer                     | ไม่             | ไม่           |
| msdyn_markedfordeletiontimestamp                 | ไม่             | ไม่           |
| msdyn_msprojectclientid                          | ไม่             | ไม่           |
| msdyn_percentage                                 | ไม่             | ไม่           |
| msdyn_requiredhours                              | ไม่             | ไม่           |
| msdyn_softbookedhours                            | ไม่             | ไม่           |
| msdyn_start                                      | ไม่             | ไม่           |

### <a name="project"></a>Project

| ชื่อตรรกะ                           | สามารถสร้าง     | สามารถแก้ไข     |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | ไม่             | ไม่           |
| msdyn_actualexpensecost_base           | ไม่             | ไม่           |
| msdyn_actuallaborcost                  | ไม่             | ไม่           |
| msdyn_actuallaborcost_base             | ไม่             | ไม่           |
| msdyn_actualend                      | ไม่             | ไม่           |
| msdyn_actualsales_base                 | ไม่             | ไม่           |
| msdyn_contractlineproject              | ตกลง            | ไม่           |
| msdyn_contractorganizationalunitid     | ตกลง            | ไม่           |
| msdyn_contractorganizationalunitidname | ตกลง            | ไม่           |
| msdyn_costconsumption                  | ไม่             | ไม่           |
| msdyn_costestimateatcomplete           | ไม่             | ไม่           |
| msdyn_costestimateatcomplete_base      | ไม่             | ไม่           |
| msdyn_costvariance                     | ไม่             | ไม่           |
| msdyn_costvariance_base                | ไม่             | ไม่           |
| msdyn_duration                         | ไม่             | ไม่           |
| msdyn_effort                           | ไม่             | ไม่           |
| msdyn_effortcompleted                  | ไม่             | ไม่           |
| msdyn_effortestimateatcompleteeac      | ไม่             | ไม่           |
| msdyn_effortremaining                  | ไม่             | ไม่           |
| msdyn_finish                           | ตกลง            | ตกลง          |
| msdyn_globalrevisiontoken              | ไม่             | ไม่           |
| msdyn_islinkedtomsprojectclient        | ไม่             | ไม่           |
| msdyn_islinkedtomsprojectclientname    | ไม่             | ไม่           |
| msdyn_linkeddocumenturl                | ไม่             | ไม่           |
| msdyn_msprojectdocument                | ไม่             | ไม่           |
| msdyn_msprojectdocumentname            | ไม่             | ไม่           |
| msdyn_plannedexpensecost               | ไม่             | ไม่           |
| msdyn_plannedexpensecost_base          | ไม่             | ไม่           |
| msdyn_plannedlaborcost                 | ไม่             | ไม่           |
| msdyn_plannedlaborcost_base            | ไม่             | ไม่           |
| msdyn_plannedsales                     | ไม่             | ไม่           |
| msdyn_plannedsales_base                | ไม่             | ไม่           |
| msdyn_progress                         | ไม่             | ไม่           |
| msdyn_remainingcost                    | ไม่             | ไม่           |
| msdyn_remainingcost_base               | ไม่             | ไม่           |
| msdyn_remainingsales                   | ไม่             | ไม่           |
| msdyn_remainingsales_base              | ไม่             | ไม่           |
| msdyn_replaylogheader                  | ไม่             | ไม่           |
| msdyn_salesconsumption                 | ไม่             | ไม่           |
| msdyn_salesestimateatcompleteeac       | ไม่             | ไม่           |
| msdyn_salesestimateatcompleteeac_base  | ไม่             | ไม่           |
| msdyn_salesvariance                    | ไม่             | ไม่           |
| msdyn_salesvariance_base               | ไม่             | ไม่           |
| msdyn_scheduleperformance              | ไม่             | ไม่           |
| msdyn_scheduleperformancename          | ไม่             | ไม่           |
| msdyn_schedulevariance                 | ไม่             | ไม่           |
| msdyn_taskearlieststart                | ไม่             | ไม่           |
| msdyn_teamsize                         | ไม่             | ไม่           |
| msdyn_teamsize_date                    | ไม่             | ไม่           |
| msdyn_teamsize_state                   | ไม่             | ไม่           |
| msdyn_totalactualcost                  | ไม่             | ไม่           |
| msdyn_totalactualcost_base             | ไม่             | ไม่           |
| msdyn_totalplannedcost                 | ไม่             | ไม่           |
| msdyn_totalplannedcost_base            | ไม่             | ไม่           |

### <a name="project-bucket"></a>บักเก็ตโครงการ

| ชื่อตรรกะ          | สามารถสร้าง      | สามารถแก้ไข     |
|-----------------------|-----------------|--------------|
| msdyn_displayorder    | ตกลง             | ไม่           |
| msdyn_name            | ตกลง             | ตกลง          |
| msdyn_project         | ตกลง             | ไม่           |
| msdyn_projectbucketid | ตกลง             | ไม่           |

## <a name="limitations-and-known-issues"></a>ข้อจำกัดและปัญหาที่ทราบ
ต่อไปนี้เป็นรายการข้อจำกัดและปัญหาที่ทราบ:

- API กำหนดการโครงการสามารถใช้ได้โดย **ผู้ใช้ที่มีใบอนุญาต Microsoft Project** เท่านั้น แต่ไม่สามารถใช้โดย:

    - ผู้ใช้แอปพลิเคชัน
    - ผู้ใช้ของระบบ
    - ผู้ใช้การบูรณาการ
    - ผู้ใช้รายอื่นที่ไม่มีสิทธิ์การใช้งานที่จำเป็น

- **OperationSet** แต่ละรายการสามารถดำเนินงานได้สูงสุด 100 รายการ
- ผู้ใช้แต่ละรายสามารถมี **OperationSet** ที่เปิดอยู่ได้สูงสุด 10 รายการ
- ปัจจุบัน Project Operations รองรับงานทั้งหมดสูงสุด 500 งานในโครงการ
- ขณะนี้สถานะความล้มเหลวและบันทึกความล้มเหลวของ **OperationSet** ยังไม่พร้อมใช้งาน
- [ข้อจำกัดและขอบเขตในโครงการและงาน](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>การจัดการข้อผิดพลาด

- หากต้องการตรวจสอบข้อผิดพลาดที่เกิดจาก Operation Sets ไปที่ **การตั้งค่า** \> **การรวมกำหนดการ** \> **Operation Sets**
- หากต้องการตรวจสอบข้อผิดพลาดที่เกิดจากบริการกำหนดการโครางการ ให้ไปที่ **การตั้งค่า** \> **การรวมกำหนดการ** \> **บันทึกข้อผิดพลาด PSS**

## <a name="sample-scenario"></a>สถานการณ์ตัวอย่าง

ในสถานการณ์นี้ คุณจะสร้างโครงการ สมาชิกทีม งานสี่งาน และการกำหนดทรัพยากรสองรายการ จากนั้น คุณจะปรับปรุงหนึ่งงาน ปรับปรุงโครงการ ลบหนึ่งงาน ลบการกำหนดทรัพยากรหนึ่งรายการ และสร้างการขึ้นต่อกันของงาน

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>ตัวอย่างเพิ่มเติม

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
   
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
