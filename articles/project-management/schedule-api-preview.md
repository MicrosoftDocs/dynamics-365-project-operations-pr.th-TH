---
title: ใช้ API กำหนดการเพื่อดำเนินงานกับเอนทิตีการจัดกำหนดการ
description: หัวข้อนี้ให้ข้อมูลและตัวอย่างสำหรับการใช้ API กำหนดการ
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116820"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>ใช้ API กำหนดการเพื่อดำเนินงานกับเอนทิตีการจัดกำหนดการ

_**นำไปใช้กับ:** Project Operations สำหรับสถานการณ์ตามทรัพยากร/วัสดุที่ไม่ได้เก็บในคลัง การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

> [!IMPORTANT] 
> ฟังก์ชันการทำงานบางส่วนหรือทั้งหมดที่ระบุไว้ในหัวข้อนี้มีให้โดยเป็นส่วนหนึ่งของรุ่นพรีวิว เนื้อหาและฟังก์ชันการทำงานอาจเปลี่ยนแปลงได้ 

## <a name="scheduling-entities"></a>เอนทิตีการจัดกำหนดการ

API กำหนดการ ให้ความสามารถในการสร้าง ปรับปรุง และลบการดำเนินงานกับ **เอนทิตีการจัดกำหนดการ** เอนทิตีเหล่านี้ได้รับการจัดการผ่านกลไกการจัดกำหนดการในโครงการสำหรับเว็บ สร้าง ปรับปรุง และลบการดำเนินงานกับ **เอนทิตีการจัดกำหนดการ** มีการจำกัดใน Dynamics 365 Project Operations รุ่นก่อนหน้า

ตารางต่อไปนี้แสดงรายการของ **เอนทิตีการจัดกำหนดการ**

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

## <a name="schedule-apis"></a>API กำหนดการ

ต่อไปนี้เป็นรายการของ API กำหนดการปัจจุบัน

- **msdyn_CreateProjectV1**: API นี้สามารถใช้ในการสร้างโครงการ โครงการและบักเก็ตโครงการเริ่มต้นจะมีการสร้างในทันที
- **msdyn_CreateTeamMemberV1**: API นี้สามารถใช้เพื่อสร้างสมาชิกทีมโครงการ โดยจะมีการสร้างสมาชิกทีมในทันที
- **msdyn_CreateOperationSetV1**: API นี้สามารถใช้เพื่อจัดกำหนดการคำขอต่างๆ ที่ต้องดำเนินการภายในธุรกรรม
- **msdyn_PSSCreateV1**: API นี้สามารถใช้เพื่อสร้างเอนทิตี เอนทิตีสามารถเป็นเอนทิตีการจัดกำหนดการใดๆ ที่สนับสนุนการดำเนินการสร้าง
- **msdyn_PSSUpdateV1**: API นี้สามารถใช้เพื่อปรับปรุงเอนทิตี เอนทิตีสามารถเป็นเอนทิตีการจัดกำหนดการใดๆ ที่สนับสนุนการดำเนินการปรับปรุง
- **msdyn_PSSDeleteV1**: API นี้สามารถใช้เพื่อลบเอนทิตี เอนทิตีสามารถเป็นเอนทิตีการจัดกำหนดการใดๆ ที่สนับสนุนการดำเนินการลบ
- **msdyn_ExecuteOperationSetV1**: API นี้ใช้เพื่อดำเนินงานทั้งหมดภายในชุดการดำเนินงานที่กำหนด

## <a name="using-schedule-apis-with-operationset"></a>การใช้API กำหนดการกับ OperationSet

เนื่องจากเรกคอร์ด **CreateProjectV1** และ **CreateTeamMemberV1** ทั้งคู่มีการสร้างขึ้นในทันที API เหล่านี้จึงไม่สามารถใช้ใน **OperationSet** ได้โดยตรง อย่างไรก็ตาม คุณสามารถใช้ API ดังกล่าวเพื่อสร้างเรกคอร์ดที่จำเป็น สร้าง **OperationSet** จากนั้นใช้เรกคอร์ดที่สร้างไว้ล่วงหน้าเหล่านี้ใน **OperationSet**

## <a name="supported-operations"></a>การดำเนินการที่รองรับ

| เอนทิตีการจัดกำหนดการ | สร้าง | อัปเดต | Delete | ข้อควรพิจารณาที่สำคัญ |
| --- | --- | --- | --- | --- |
งานโครงการ | ใช่ | ใช่ | ใช่ | ไม่มี |
| การขึ้นต่อกันของงานโครงการ | ใช่ | ใช่ | | ไม่ปรับปรุงเรกคอร์ดการขึ้นต่อกันของงานโครงการ แต่สามารถลบเรกคอร์ดเก่าและสร้างเรกคอร์ดใหม่ได้ |
| การกำหนดทรัพยากร | ใช่ | ใช่ | | ไม่รองรับการดำเนินการกับฟิลด์ต่อไปนี้: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** และ **PlannedWork** ไม่ปรับปรุงเรกคอร์ดการกำหนดทรัพยากร แต่สามารถลบเรกคอร์ดเก่าและสร้างเรกคอร์ดใหม่ได้ |
| บักเก็ตโครงการ | ไม่พร้อมใช้งาน | ไม่พร้อมใช้งาน | ไม่พร้อมใช้งาน | มีการสร้างบักเก็ตโครงการเริ่มต้นโดยใช้ **CreateProjectV1** API |
| สมาชิกของทีมโครงการ | ใช่ | ใช่ | ใช่ | สำหรับการดำเนินการสร้าง ให้ใช้ **CreateTeamMemberV1** API |
| Project | ใช่ | ใช่ | ไม่พร้อมใช้งาน | ไม่รองรับการดำเนินการกับฟิลด์ต่อไปนี้: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** และ **Duration** |

API เหล่านี้สามารถเรียกใช้กับเอนทิตีอ็อบเจ็กต์ที่มีฟิลด์แบบกำหนดเอง

รหัสคุณสมบัติเป็นแบบระบุหรือไม่ก็ได้ หากระบุ ระบบจะพยายามใช้และแสดงข้อยกเว้นหากไม่สามารถใช้งานได้ หากไม่ระบบ ระบบจะสร้างขึ้นเอง

## <a name="restricted-fields"></a>ฟิลด์ที่ถูกจำกัด

ตารางต่อไปนี้กำหนดฟิลด์ที่ถูกจำกัดจาก **สร้าง** และ **แก้ไข**

### <a name="project-task"></a>งานโครงการ

| **ชื่อตรรกะ**                       | **สามารถสร้าง** | **สามารถแก้ไข**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | ไม่ใช่             | ไม่ใช่               |
| msdyn_actualcost_base                  | ไม่ใช่             | ไม่ใช่               |
| msdyn_actualend                        | ไม่ใช่             | ไม่ใช่               |
| msdyn_actualend                      | ไม่ใช่             | ไม่ใช่               |
| msdyn_actualsales_base                 | ไม่ใช่             | ไม่ใช่               |
| msdyn_actualstart                      | ไม่ใช่             | ไม่ใช่               |
| msdyn_costatcompleteestimate           | ไม่ใช่             | ไม่ใช่               |
| msdyn_costatcompleteestimate_base      | ไม่ใช่             | ไม่ใช่               |
| msdyn_costconsumptionpercentage        | ไม่ใช่             | ไม่ใช่               |
| msdyn_effortcompleted                  | ไม่ใช่             | ไม่ใช่               |
| msdyn_effortestimateatcomplete         | ไม่ใช่             | ไม่ใช่               |
| msdyn_iscritical                       | ไม่ใช่             | ไม่ใช่               |
| msdyn_iscriticalname                   | ไม่ใช่             | ไม่ใช่               |
| msdyn_ismanual                         | ไม่ใช่             | ไม่ใช่               |
| msdyn_ismanualname                     | ไม่ใช่             | ไม่ใช่               |
| msdyn_ismilestone                      | ไม่ใช่             | ไม่ใช่               |
| msdyn_ismilestonename                  | ไม่ใช่             | ไม่ใช่               |
| msdyn_LinkStatus                       | ไม่ใช่             | ไม่ใช่               |
| msdyn_linkstatusname                   | ไม่ใช่             | ไม่ใช่               |
| msdyn_msprojectclientid                | ไม่ใช่             | ไม่ใช่               |
| msdyn_plannedcost                      | ไม่ใช่             | ไม่ใช่               |
| msdyn_plannedcost_base                 | ไม่ใช่             | ไม่ใช่               |
| msdyn_plannedsales                     | ไม่ใช่             | ไม่ใช่               |
| msdyn_plannedsales_base                | ไม่ใช่             | ไม่ใช่               |
| msdyn_pluginprocessingdata             | ไม่ใช่             | ไม่ใช่               |
| msdyn_progress                         | ไม่ใช่             | ไม่ (ใช่ สำหรับ P4W) |
| msdyn_remainingcost                    | ไม่ใช่             | ไม่ใช่               |
| msdyn_remainingcost_base               | ไม่ใช่             | ไม่ใช่               |
| msdyn_remainingsales                   | ไม่ใช่             | ไม่ใช่               |
| msdyn_remainingsales_base              | ไม่ใช่             | ไม่ใช่               |
| msdyn_requestedhours                   | ไม่ใช่             | ไม่ใช่               |
| msdyn_resourcecategory                 | ไม่ใช่             | ไม่ใช่               |
| msdyn_resourcecategoryname             | ไม่ใช่             | ไม่ใช่               |
| msdyn_resourceorganizationalunitid     | ไม่ใช่             | ไม่ใช่               |
| msdyn_resourceorganizationalunitidname | ไม่ใช่             | ไม่ใช่               |
| msdyn_salesconsumptionpercentage       | ไม่ใช่             | ไม่ใช่               |
| msdyn_salesestimateatcomplete          | ไม่ใช่             | ไม่ใช่               |
| msdyn_salesestimateatcomplete_base     | ไม่ใช่             | ไม่ใช่               |
| msdyn_salesvariance                    | ไม่ใช่             | ไม่ใช่               |
| msdyn_salesvariance_base               | ไม่ใช่             | ไม่ใช่               |
| msdyn_scheduleddurationminutes         | ไม่ใช่             | ไม่ใช่               |
| msdyn_scheduledend                     | ไม่ใช่             | ไม่ใช่               |
| msdyn_scheduledstart                   | ไม่ใช่             | ไม่ใช่               |
| msdyn_schedulevariance                 | ไม่ใช่             | ไม่ใช่               |
| msdyn_skipupdateestimateline           | ไม่ใช่             | ไม่ใช่               |
| msdyn_skipupdateestimatelinename       | ไม่ใช่             | ไม่ใช่               |
| msdyn_summary                          | ไม่ใช่             | ไม่ใช่               |
| msdyn_varianceofcost                   | ไม่ใช่             | ไม่ใช่               |
| msdyn_varianceofcost_base              | ไม่ใช่             | ไม่ใช่               |

### <a name="project-task-dependency"></a>การขึ้นต่อกันของงานโครงการ

| **ชื่อตรรกะ**              | **สามารถสร้าง** | **สามารถแก้ไข** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | ไม่ใช่             | ไม่ใช่           |
| msdyn_linktypename            | ไม่ใช่             | ไม่ใช่           |
| msdyn_predecessortask         | ใช่            | ไม่ใช่           |
| msdyn_predecessortaskname     | ใช่            | ไม่ใช่           |
| msdyn_project                 | ใช่            | ไม่ใช่           |
| msdyn_projectname             | ใช่            | ไม่ใช่           |
| msdyn_projecttaskdependencyid | ใช่            | ไม่ใช่           |
| msdyn_successortask           | ใช่            | ไม่ใช่           |
| msdyn_successortaskname       | ใช่            | ไม่ใช่           |

### <a name="resource-assignment"></a>การกำหนดทรัพยากร

| **ชื่อตรรกะ**             | **สามารถสร้าง** | **สามารถแก้ไข** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | ใช่            | ไม่ใช่           |
| msdyn_bookableresourceidname | ใช่            | ไม่ใช่           |
| msdyn_bookingstatusid        | ไม่ใช่             | ไม่ใช่           |
| msdyn_bookingstatusidname    | ไม่ใช่             | ไม่ใช่           |
| msdyn_committype             | ไม่ใช่             | ไม่ใช่           |
| msdyn_committypename         | ไม่ใช่             | ไม่ใช่           |
| msdyn_effort                 | ไม่ใช่             | ไม่ใช่           |
| msdyn_effortcompleted        | ไม่ใช่             | ไม่ใช่           |
| msdyn_effortremaining        | ไม่ใช่             | ไม่ใช่           |
| msdyn_finish                 | ไม่ใช่             | ไม่ใช่           |
| msdyn_plannedcost            | ไม่ใช่             | ไม่ใช่           |
| msdyn_plannedcost_base       | ไม่ใช่             | ไม่ใช่           |
| msdyn_plannedcostcontour     | ไม่ใช่             | ไม่ใช่           |
| msdyn_plannedsales           | ไม่ใช่             | ไม่ใช่           |
| msdyn_plannedsales_base      | ไม่ใช่             | ไม่ใช่           |
| msdyn_plannedsalescontour    | ไม่ใช่             | ไม่ใช่           |
| msdyn_plannedwork            | ไม่ใช่             | ไม่ใช่           |
| msdyn_projectid              | ใช่            | ไม่ใช่           |
| msdyn_projectidname          | ไม่ใช่             | ไม่ใช่           |
| msdyn_projectteamid          | ไม่ใช่             | ไม่ใช่           |
| msdyn_projectteamidname      | ไม่ใช่             | ไม่ใช่           |
| msdyn_start                  | ไม่ใช่             | ไม่ใช่           |
| msdyn_taskid                 | ไม่ใช่             | ไม่ใช่           |
| msdyn_taskidname             | ไม่ใช่             | ไม่ใช่           |
| msdyn_userresourceid         | ไม่ใช่             | ไม่ใช่           |

### <a name="project-team-member"></a>สมาชิกของทีมโครงการ

| **ชื่อตรรกะ**                                 | **สามารถสร้าง** | **สามารถแก้ไข** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | ไม่ใช่             | ไม่ใช่           |
| msdyn_creategenericteammemberwithrequirementname | ไม่ใช่             | ไม่ใช่           |
| msdyn_deletestatus                               | ไม่ใช่             | ไม่ใช่           |
| msdyn_deletestatusname                           | ไม่ใช่             | ไม่ใช่           |
| msdyn_effort                                     | ไม่ใช่             | ไม่ใช่           |
| msdyn_effortcompleted                            | ไม่ใช่             | ไม่ใช่           |
| msdyn_effortremaining                            | ไม่ใช่             | ไม่ใช่           |
| msdyn_finish                                     | ไม่ใช่             | ไม่ใช่           |
| msdyn_hardbookedhours                            | ไม่ใช่             | ไม่ใช่           |
| msdyn_hours                                      | ไม่ใช่             | ไม่ใช่           |
| msdyn_markedfordeletiontimer                     | ไม่ใช่             | ไม่ใช่           |
| msdyn_markedfordeletiontimestamp                 | ไม่ใช่             | ไม่ใช่           |
| msdyn_msprojectclientid                          | ไม่ใช่             | ไม่ใช่           |
| msdyn_percentage                                 | ไม่ใช่             | ไม่ใช่           |
| msdyn_requiredhours                              | ไม่ใช่             | ไม่ใช่           |
| msdyn_softbookedhours                            | ไม่ใช่             | ไม่ใช่           |
| msdyn_start                                      | ไม่ใช่             | ไม่ใช่           |

### <a name="project"></a>Project

| **ชื่อตรรกะ**                       | **สามารถสร้าง** | **สามารถแก้ไข** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | ไม่ใช่             | ไม่ใช่           |
| msdyn_actualexpensecost_base           | ไม่ใช่             | ไม่ใช่           |
| msdyn_actuallaborcost                  | ไม่ใช่             | ไม่ใช่           |
| msdyn_actuallaborcost_base             | ไม่ใช่             | ไม่ใช่           |
| msdyn_actualsales                      | ไม่ใช่             | ไม่ใช่           |
| msdyn_actualsales_base                 | ไม่ใช่             | ไม่ใช่           |
| msdyn_contractlineproject              | ใช่            | ไม่ใช่           |
| msdyn_contractorganizationalunitid     | ใช่            | ไม่ใช่           |
| msdyn_contractorganizationalunitidname | ใช่            | ไม่ใช่           |
| msdyn_costconsumption                  | ไม่ใช่             | ไม่ใช่           |
| msdyn_costestimateatcomplete           | ไม่ใช่             | ไม่ใช่           |
| msdyn_costestimateatcomplete_base      | ไม่ใช่             | ไม่ใช่           |
| msdyn_costvariance                     | ไม่ใช่             | ไม่ใช่           |
| msdyn_costvariance_base                | ไม่ใช่             | ไม่ใช่           |
| msdyn_duration                         | ไม่ใช่             | ไม่ใช่           |
| msdyn_effort                           | ไม่ใช่             | ไม่ใช่           |
| msdyn_effortcompleted                  | ไม่ใช่             | ไม่ใช่           |
| msdyn_effortestimateatcompleteeac      | ไม่ใช่             | ไม่ใช่           |
| msdyn_effortremaining                  | ไม่ใช่             | ไม่ใช่           |
| msdyn_finish                           | ใช่            | ใช่          |
| msdyn_globalrevisiontoken              | ไม่ใช่             | ไม่ใช่           |
| msdyn_islinkedtomsprojectclient        | ไม่ใช่             | ไม่ใช่           |
| msdyn_islinkedtomsprojectclientname    | ไม่ใช่             | ไม่ใช่           |
| msdyn_linkeddocumenturl                | ไม่ใช่             | ไม่ใช่           |
| msdyn_msprojectdocument                | ไม่ใช่             | ไม่ใช่           |
| msdyn_msprojectdocumentname            | ไม่ใช่             | ไม่ใช่           |
| msdyn_plannedexpensecost               | ไม่ใช่             | ไม่ใช่           |
| msdyn_plannedexpensecost_base          | ไม่ใช่             | ไม่ใช่           |
| msdyn_plannedlaborcost                 | ไม่ใช่             | ไม่ใช่           |
| msdyn_plannedlaborcost_base            | ไม่ใช่             | ไม่ใช่           |
| msdyn_plannedsales                     | ไม่ใช่             | ไม่ใช่           |
| msdyn_plannedsales_base                | ไม่ใช่             | ไม่ใช่           |
| msdyn_progress                         | ไม่ใช่             | ไม่ใช่           |
| msdyn_remainingcost                    | ไม่ใช่             | ไม่ใช่           |
| msdyn_remainingcost_base               | ไม่ใช่             | ไม่ใช่           |
| msdyn_remainingsales                   | ไม่ใช่             | ไม่ใช่           |
| msdyn_remainingsales_base              | ไม่ใช่             | ไม่ใช่           |
| msdyn_replaylogheader                  | ไม่ใช่             | ไม่ใช่           |
| msdyn_salesconsumption                 | ไม่ใช่             | ไม่ใช่           |
| msdyn_salesestimateatcompleteeac       | ไม่ใช่             | ไม่ใช่           |
| msdyn_salesestimateatcompleteeac_base  | ไม่ใช่             | ไม่ใช่           |
| msdyn_salesvariance                    | ไม่ใช่             | ไม่ใช่           |
| msdyn_salesvariance_base               | ไม่ใช่             | ไม่ใช่           |
| msdyn_scheduleperformance              | ไม่ใช่             | ไม่ใช่           |
| msdyn_scheduleperformancename          | ไม่ใช่             | ไม่ใช่           |
| msdyn_schedulevariance                 | ไม่ใช่             | ไม่ใช่           |
| msdyn_taskearlieststart                | ไม่ใช่             | ไม่ใช่           |
| msdyn_teamsize                         | ไม่ใช่             | ไม่ใช่           |
| msdyn_teamsize_date                    | ไม่ใช่             | ไม่ใช่           |
| msdyn_teamsize_state                   | ไม่ใช่             | ไม่ใช่           |
| msdyn_totalactualcost                  | ไม่ใช่             | ไม่ใช่           |
| msdyn_totalactualcost_base             | ไม่ใช่             | ไม่ใช่           |
| msdyn_totalplannedcost                 | ไม่ใช่             | ไม่ใช่           |
| msdyn_totalplannedcost_base            | ไม่ใช่             | ไม่ใช่           |


## <a name="limitations-and-known-issues"></a>ข้อจำกัดและปัญหาที่ทราบ
ต่อไปนี้เป็นรายการข้อจำกัดและปัญหาที่ทราบ:

- API กำหนดการ สามารถใช้ได้โดย **ผู้ใช้ที่มีสิทธิ์การใช้งาน Microsoft Project** แต่ไม่สามารถใช้โดย:
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
   - หากต้องการตรวจสอบข้อผิดพลาดที่เกิดจาก Project Scheduling Service ไปที่ **การตั้งค่า** \> **การรวมกำหนดการ** \> **บันทึกข้อผิดพลาด PSS**

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
    task["msdyn_progress"] = 0.34m;
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
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

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
