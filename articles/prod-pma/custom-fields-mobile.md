---
title: ใช้ฟิลด์ที่กำหนดเองสำหรับแอปบนมือถือ Microsoft Dynamics 365 Project Timesheet บน iOS และ Android
description: หัวข้อนี้มีรูปแบบทั่วไปสำหรับการใช้ส่วนขยายเพื่อใช้ฟิลด์ที่กำหนดเอง
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 79ef62d6911b393248536e4cc73475f6c35a22e2
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2022
ms.locfileid: "8682779"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>ใช้ฟิลด์ที่กำหนดเองสำหรับแอปบนมือถือ Microsoft Dynamics 365 Project Timesheet บน iOS และ Android

[!include [banner](../includes/banner.md)]

หัวข้อนี้มีรูปแบบทั่วไปสำหรับการใช้ส่วนขยายเพื่อใช้ฟิลด์ที่กำหนดเอง หัวข้อต่อไปนี้ครอบคลุม:

- ชนิดข้อมูลต่างๆ ที่กรอบฟิลด์ข้อมูลที่กำหนดเองสนับสนุน
- วิธีแสดงฟิลด์แบบอ่านอย่างเดียวหรือแก้ไขได้ในรายการแผ่นเวลาและบันทึกค่าที่ผู้ใช้ระบุกลับไปยังฐานข้อมูล
- วิธีแสดงฟิลด์แบบอ่านอย่างเดียวบนส่วนหัวของแผ่นเวลา
- วิธีการรวมตรรกะทางธุรกิจที่กำหนดเองอื่นๆ เพื่อป้อนค่าเริ่มต้นในฟิลด์และทำการตรวจสอบความถูกต้องเพิ่มเติม

## <a name="audience"></a>ผู้ชม

หัวข้อนี้มีไว้สำหรับนักพัฒนาที่กำลังรวมฟิลด์ที่กำหนดเองไว้ในแอปพลิเคชันมือถือ Microsoft Dynamics 365 Project Timesheet ที่พร้อมใช้งานสำหรับ Apple iOS และ Google Android สมมติฐานคือผู้อ่านคุ้นเคยกับการพัฒนา X++ และฟังก์ชันการทำงานของแผ่นเวลาโครงการ

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>สัญญาข้อมูล - คลาส TSTimesheetCustomField X++

คลาส **TSTimesheetCustomField** คือคลาสสัญญาข้อมูล X++ ที่แสดงข้อมูลเกี่ยวกับฟิลด์ที่กำหนดเองสำหรับฟังก์ชันการทำงานของแผ่นเวลา รายการของออบเจ็กต์ฟิลด์ที่กำหนดเองจะถูกส่งผ่านทั้งสัญญาข้อมูล TSTimesheetDetails และสัญญาข้อมูล TSTimesheetEntry เพื่อแสดงฟิลด์ที่กำหนดเองในแอปมือถือ

- **TSTimesheetDetails** - สัญญาส่วนหัวของแผ่นเวลา
- **TSTimesheetEntry** - สัญญาการทำธุรกรรมแผ่นเวลา กลุ่มของวัตถุเหล่านี้ที่มีข้อมูลโครงการเดียวกันและค่า **timesheetLineRecId** เป็นเส้น

### <a name="fieldbasetype-types"></a>fieldBaseType (ประเภท)

คุณสมบัติ **FieldBaseType** บนออบเจ็กต์ **TsTimesheetCustom** กำหนดประเภทของฟิลด์ที่ปรากฏในแอป ค่า **ประเภท** ดังต่อไปนี้ได้รับการรองรับ

| ค่าของประเภท | ประเภท              | หมายเหตุ |
|-------------|-------------------|-------|
| 0           | String (และ Enum) | ฟิลด์จะปรากฏเป็นฟิลด์ข้อความ |
| 1           | Integer           | ค่าจะแสดงเป็นตัวเลขโดยไม่มีตำแหน่งทศนิยม |
| 2           | จริง              | ค่าจะแสดงเป็นตัวเลขที่มีตำแหน่งทศนิยม<p>หากต้องการแสดงมูลค่าที่แท้จริงเป็นสกุลเงินในแอป ให้ใช้คุณสมบัติ **fieldExtenededType** คุณสามารถใช้คุณสมบัติ **numberOfDecimals** เพื่อกำหนดจำนวนตำแหน่งทศนิยมที่จะแสดง</p> |
| 3           | Date              | รูปแบบวันที่กำหนดโดยการตั้งค่า **รูปแบบวันที่ เวลา และตัวเลข** ของผู้ใช้ที่ระบุไว้ภายใต้ **การกำหนดภาษาและประเทศ/ภูมิภาค** ใน **ตัวเลือกผู้ใช้** |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- ถ้าคุณสมบัติ **stringOptions** ไม่ได้ระบุบนออบเจ็กต์ **TSTimesheetCustomField** ฟิลด์ข้อความอิสระจะถูกจัดเตรียมไว้ให้กับผู้ใช้

    คุณสมบัติ **stringLength** สามารถใช้เพื่อตั้งค่าความยาวสตริงสูงสุดที่ผู้ใช้ป้อนได้

- ถ้าคุณสมบัติ **stringOptions** มีให้ในออบเจ็กต์ **TSTimesheetCustomField** องค์ประกอบรายการเหล่านั้นเป็นค่าเดียวที่ผู้ใช้สามารถเลือกได้โดยใช้ปุ่มตัวเลือก (ปุ่มตัวเลือก)

    ในกรณีนี้ฟิลด์สตริงสามารถทำหน้าที่เป็นค่า enum สำหรับวัตถุประสงค์ในการป้อนข้อมูลของผู้ใช้ ในการบันทึกค่าลงในฐานข้อมูลเป็น enum ให้แม็ปค่าสตริงกลับไปเป็นค่า enum ด้วยตนเองก่อนที่คุณจะบันทึกลงในฐานข้อมูลโดยใช้ชุดของคำสั่ง (ดูที่ส่วน "ใช้ชุดของคำสั่งบนคลาส TSTimesheetEntryService เพื่อบันทึกรายการแผ่นเวลาจากแอปกลับไปที่ฐานข้อมูล" ต่อไปในหัวข้อนี้เป็นตัวอย่าง)

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

คุณสามารถใช้คุณสมบัตินี้เพื่อจัดรูปแบบค่าจริงเป็นสกุลเงิน แนวทางนี้ใช้ได้เฉพาะเมื่อค่า **fieldBaseType** คือ **จริง**

- **TSCustomFieldExtendedType:ไม่มี** - ไม่มีการใช้การจัดรูปแบบ
- **TSCustomFieldExtendedType::สกุลเงิน** - จัดรูปแบบค่าเป็นสกุลเงิน

    เมื่อการจัดรูปแบบสกุลเงินใช้งานอยู่ ฟิลด์ **stringValue** อาจถูกใช้ส่งรหัสสกุลเงินที่ควรจะแสดงในแอป ค่านี้เป็นค่าอ่านอย่างเดียว

    ฟิลด์ **realValue** มีจำนวนเงินที่ควรบันทึกลงในฐานข้อมูล

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

คุณสามารถใช้คุณสมบัตินี้ระบุตำแหน่งที่ฟิลด์ที่กำหนดเองควรปรากฏในแอป

- **TSCustomFieldSection::หัวข้อ** - ฟิลด์จะปรากฏในส่วน **ดูรายละเอียดเพิ่มเติม** ในแอป ฟิลด์เหล่านี้เป็นแบบอ่านอย่างเดียวเสมอ
- **TSCustomFieldSection::รายการ** - ฟิลด์นี้จะปรากฏขึ้นหลังฟิลด์รายการสำเร็จรูปทั้งหมดในรายการแผ่นเวลา ฟิลด์เหล่านี้สามารถแก้ไขได้หรือเป็นแบบอ่านอย่างเดียว

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

คุณสมบัตินี้ระบุฟิลด์เมื่อค่าที่แอปให้ไว้จะถูกบันทึกกลับไปที่ฐานข้อมูล

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

คุณสมบัตินี้ระบุฟิลด์เมื่อค่าที่แอปให้ไว้จะถูกบันทึกกลับไปที่ฐานข้อมูล

### <a name="iseditable-noyes"></a>isEditable (NoYes)

ตั้งค่าคุณสมบัตินี้เป็น **ใช่** เพื่อระบุว่าผู้ใช้ควรแก้ไขฟิลด์ในส่วนรายการแผ่นเวลา ตั้งค่าคุณสมบัติเป็น **ไม่** เพื่อทำให้ฟิลด์เป็นแบบอ่านอย่างเดียว

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

ตั้งค่าคุณสมบัตินี้เป็น **ใช่** เพื่อระบุว่าผู้ใช้ควรบังคับใช้ฟิลด์ในส่วนรายการแผ่นเวลา

### <a name="label-str"></a>ป้ายกำกับ (str)

คุณสมบัตินี้ระบุป้ายกำกับที่แสดงถัดจากฟิลด์ในแอป

### <a name="stringoptions-list-of-strings"></a>stringOptions (รายการสตริง)

คุณสมบัตินี้จะใช้ได้ก็ต่อเมื่อ **fieldBaseType** ถูกตั้งค่าเป็น **สตริง** ถ้า **stringOptions** ถูกตั้งค่าสตริงที่พร้อมใช้งานสำหรับการเลือกผ่านปุ่มตัวเลือก (ปุ่มตัวเลือก) จะถูกระบุโดยสตริงในรายการ หากไม่มีการระบุสตริง จะอนุญาตให้ป้อนข้อความอิสระในฟิลด์สตริงได้ (โปรดดูที่ส่วน "ใช้ชุดคำสั่งบนคลาส TSTimesheetEntryService เพื่อบันทึกรายการแผ่นเวลาจากแอปกลับไปที่ฐานข้อมูล" ในหัวข้อนี้เป็นตัวอย่าง)

### <a name="stringlength-int"></a>stringLength (int)

คุณสมบัตินี้ระบุความยาวสูงสุดสำหรับฟิลด์สตริง คุณสมบัตินี้จะใช้ได้ก็ต่อเมื่อ **fieldBaseType** ถูกตั้งค่าเป็น **สตริง**

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

คุณสมบัตินี้ระบุจำนวนตำแหน่งทศนิยมที่แสดงสำหรับฟิลด์จริง คุณสมบัตินี้จะใช้ได้ก็ต่อเมื่อ **fieldBaseType** ถูกตั้งค่าเป็น **จริง**

### <a name="ordersequence-int"></a>orderSequence (int)

คุณสมบัตินี้ควบคุมลำดับการแสดงฟิลด์แบบกำหนดเองในแอปเมื่อระบุฟิลด์แบบกำหนดเองมากกว่าหนึ่งฟิลด์ ฟิลด์ที่มีตัวเลขต่ำกว่าจะแสดงก่อน

### <a name="booleanvalue-boolean"></a>booleanValue (บูลีน)

สำหรับฟิลด์ของประเภท **บูลีน** คุณสมบัตินี้ส่งผ่านค่าบูลีนของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป

### <a name="guidvalue-guid"></a>guidValue (guid)

สำหรับฟิลด์ของประเภท **GUID** คุณสมบัตินี้ส่งผ่านตัวระบุที่ไม่ซ้ำแบบส่วนกลาง (GUID) ของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป

### <a name="int64value-int64"></a>int64Value (int64)

สำหรับฟิลด์ของประเภท **Int64** คุณสมบัตินี้ส่งผ่านค่า Int64 ของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป

### <a name="intvalue-int"></a>intValue (int)

สำหรับฟิลด์ของประเภท **Int** คุณสมบัตินี้ส่งผ่านค่า Int ของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป

### <a name="realvalue-real"></a>realValue (จริง)

สำหรับฟิลด์ของประเภท **จริง** คุณสมบัตินี้ส่งผ่านค่าจริงของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป

### <a name="stringvalue-str"></a>stringValue (str)

สำหรับฟิลด์ของประเภท **สตริง** คุณสมบัตินี้ส่งผ่านค่าสตริงของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป นอกจากนี้ยังใช้สำหรับฟิลด์ของประเภท **จริง** ที่จัดรูปแบบเป็นสกุลเงิน สำหรับช่องเหล่านั้น คุณสมบัติจะใช้เพื่อส่งรหัสสกุลเงินไปยังแอป

### <a name="datevalue-date"></a>dateValue (วันที่)

สำหรับฟิลด์ของประเภท **วันที่** คุณสมบัตินี้ส่งผ่านค่าวันที่ของฟิลด์ระหว่างเซิร์ฟเวอร์และแอป

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>แสดงและบันทึกฟิลด์ที่กำหนดเองในส่วนรายการแผ่นเวลา

ด้านล่างนี้เป็นภาพหน้าจอจากแอปบนมือถือของการสร้างรายการแผ่นเวลา โดยจะแสดงฟิลด์แบบสำเร็จรูปและฟิลด์ที่กำหนดเองในส่วน "รายการเวลา" ที่เรียกว่า "สตริงการทดสอบ" พร้อมด้วยค่า enum ของ "ตัวเลือกที่สอง" ที่กำหนดไว้แล้ว

![ฟิลด์ที่กำหนดเองของสตริงการทดสอบในแอป](media/timesheet-entry.jpg)



ด้านล่างนี้คือภาพหน้าจอจากแอปบนมือถือของผู้ใช้ที่เลือกหนึ่งในตัวเลือก enum ที่มีให้สำหรับฟิลด์ "สตริงทดสอบ" ที่กำหนดเอง  สองตัวเลือกคือ "ตัวเลือกแรก" และ "ตัวเลือกที่สอง" แสดงเป็นปุ่มตัวเลือก ขณะนี้ตัวเลือกที่สองถูกเลือก

![ปุ่มตัวเลือก (ปุ่มตัวเลือก) สำหรับฟิลด์แบบกำหนดเองของสตริงการทดสอบ](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>ขยายตาราง TSTimesheetLine เพื่อให้มีฟิลด์ที่กำหนดเอง

ในสถานการณ์ทั่วไปมีแนวโน้มว่าข้อมูลสำหรับฟิลด์ที่กำหนดเองในส่วนรายการแผ่นเวลาจะถูกบันทึกลงในตาราง TSTimesheetLine อย่างไรก็ตามสามารถใช้ตารางอื่นๆ ได้หากสามารถดึงข้อมูลโดยยึดตามเรกคอร์ด TSTimesheetTrans ที่มีให้หรือถ้าไม่มีบริบทของเรกคอร์ดที่เฉพาะเจาะจง (ตัวอย่างเช่น หากฟิลด์ถูกตั้งค่าเป็นแบบอ่านอย่างเดียวในพารามิเตอร์โครงการ)

โปรดทราบว่าช่องที่กำหนดเองไม่จำเป็นต้องมีเรกคอร์ดฐานข้อมูลสำรอง สามารถสร้างแบบไดนามิกตามตรรกะ X++ แนวทางนี้มีประโยชน์ในสถานการณ์แบบอ่านอย่างเดียว (ดูหัวข้อ "ใช้ชุดคำสั่งบนคลาส TSTimesheetDetails โดยวิธี buildCustomFieldListForHeader เพื่อกรอกรายละเอียดแผ่นเวลา" สำหรับตัวอย่างของค่าฟิลด์แบบกำหนดเองที่สร้างขึ้นแบบไดนามิก)

ด้านล่างนี้คือภาพหน้าจอจาก Visual Studio ของ Application Object Tree แสดงส่วนขยายของตาราง TSTimesheetLine พร้อมกับฟิลด์ TestLineString ที่เพิ่มเป็นฟิลด์แบบกำหนดเอง

![สตริงรายการ](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>ใช้ชุดคำสั่งบนวิธี buildCustomFieldList ของคลาส TSTimesheetSettings เพื่อแสดงฟิลด์ในส่วนรายการแผ่นเวลา

รหัสนี้ควบคุมการตั้งค่าการแสดงผลสำหรับฟิลด์ในแอป ตัวอย่างเช่น จะควบคุมประเภทของฟิลด์ ป้ายกำกับว่าฟิลด์บังคับหรือไม่ และส่วนใดที่ฟิลด์ปรากฏ

ตัวอย่างต่อไปนี้แสดงฟิลด์สตริงในรายการเวลา ฟิลด์นี้มีสองตัวเลือก **ตัวเลือกแรก** และ **ตัวเลือกที่สอง** ซึ่งมีให้ใช้งานผ่านปุ่มตัวเลือก (ปุ่มตัวเลือก) ฟิลด์ในแอปเชื่อมโยงกับฟิลด์ **TestLineString** ที่เพิ่มลงในตาราง TSTimesheetLine

หมายเหตุการใช้วิธี **TSTimesheetCustomField::newFromMetatdata()** เพื่อลดความซับซ้อนของการเริ่มต้นคุณสมบัติฟิลด์ที่กำหนดเอง: **fieldBaseType** **tableName** **ชื่อฟิลด์** **label** **isEditable** **isMandatory** **stringLength** และ **numberOfDecimals** คุณยังสามารถตั้งค่าพารามิเตอร์เหล่านี้ด้วยตนเองได้ตามต้องการ

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>ใช้ชุดคำสั่งบนวิธี buildCustomFieldListForEntry ของคลาส TSTimesheetEntry เพื่อป้อนค่าในรายการแผ่นเวลา

วิธี **buildCustomFieldListForEntry** ถูกใช้เพื่อป้อนค่าในบรรทัดแผ่นเวลาที่บันทึกไว้ในแอปมือถือ ใช้เรกคอร์ด TSTimesheetTrans เป็นพารามิเตอร์ คุณสามารถใช้ฟิลด์จากเรกคอร์ดนั้นเพื่อกรอกค่าฟิลด์ที่กำหนดเองในแอป

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>ใช้ชุดคำสั่งบนคลาส TSTimesheetEntryService เพื่อบันทึกรายการแผ่นเวลาจากแอปกลับไปที่ฐานข้อมูล

ในการบันทึกฟิลด์ที่กำหนดเองกลับไปที่ฐานข้อมูลในการใช้งานทั่วไป คุณต้องขยายหลายวิธี:

- วิธี **timesheetLineNeedsUpdating** ใช้เพื่อตรวจสอบว่าผู้ใช้ในแอปเปลี่ยนแปลงเรกคอร์ดรายการหรือไม่และต้องบันทึกลงในฐานข้อมูล หากประสิทธิภาพไม่น่ากังวล วิธีนี้สามารถทำให้ง่ายขึ้นเพื่อให้กลับมา **จริง** เสมอ
- วิธี **populateTimesheetLineFromEntryDuringCreate** และ **populateTimesheetLineFromEntryDuringUpdate** สามารถขยายวิธีการเพื่อให้ป้อนค่าในเรกคอร์ดฐานข้อมูล TSTimesheetLine จากเรกคอร์ดสัญญาข้อมูล TSTimesheetEntry ที่มีให้ ในตัวอย่างต่อไปนี้ ให้สังเกตว่าการแม็ประหว่างฟิลด์ฐานข้อมูลและฟิลด์รายการทำได้ด้วยตนเองผ่านรหัส X++ อย่างไร
- วิธี **populateTimesheetWeekFromEntry** ยังสามารถขยายได้หากฟิลด์แบบกำหนดเองที่แม็ปกับออบเจ็กต์ **TSTimesheetEntry** ต้องเขียนกลับไปที่ตารางฐานข้อมูล TSTimesheetLineweek

> [!NOTE]
> ตัวอย่างต่อไปนี้บันทึกค่า **firstOption** หรือ **secondOption** ที่ผู้ใช้เลือกไปยังฐานข้อมูลเป็นค่าสตริงดิบ หากฟิลด์ฐานข้อมูลเป็นฟิลด์ของประเภท **Enum** ค่าเหล่านั้นสามารถแม็ปกับค่า enum ด้วยตนเองจากนั้นบันทึกลงในฟิลด์ enum บนตารางฐานข้อมูล

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>แสดงฟิลด์ที่กำหนดเองในส่วนหัวของแผ่นเวลา

ด้านล่างนี้เป็นภาพหน้าจอจากแอปบนมือถือของผู้ใช้ที่กำลังดูแผ่นเวลา ปุ่ม "ข้อมูลเพิ่มเติม" ถูกเลือกไว้ที่มุมขวาบนเพื่อแสดงตัวเลือก "ดูรายละเอียดเพิ่มเติม"  

![คำสั่งดูรายละเอียดเพิ่มเติม](media/show-more.png)

ด้านล่างนี้เป็นภาพหน้าจอจากแอปบนมือถือที่แสดงส่วน "เพิ่มเติม" ของแผ่นเวลา มีการเพิ่มฟิลด์ที่กำหนดเองที่เรียกว่า "อัตราการใช้งานของแผ่นเวลานี้ (ฟิลด์ที่กำหนดเองจากการคำนวณ)" ในส่วนหัวของแผ่นเวลา ค่าแบบอ่านอย่างเดียวคือ "0.667" ถูกตั้งค่าในฟิลด์ที่กำหนดเอง

![ส่วนเพิ่มเติม](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>ขยายตาราง TSTimesheetTable เพื่อให้มีฟิลด์ที่กำหนดเอง

ในสถานการณ์ทั่วไป มีแนวโน้มว่าข้อมูลสำหรับฟิลด์ที่กำหนดเองในส่วนหัวจะถูกดึงจากตาราง TSTimesheetHeader อย่างไรก็ตามสามารถใช้ตารางอื่นๆ ได้หากสามารถดึงข้อมูลโดยยึดตามเรกคอร์ด TSTimesheetTable ที่มีให้หรือถ้าไม่มีบริบทของเรกคอร์ดที่เฉพาะเจาะจง (ตัวอย่างเช่น หากฟิลด์ถูกตั้งค่าเป็นแบบอ่านอย่างเดียวในพารามิเตอร์โครงการ)

โปรดทราบว่าช่องที่กำหนดเองไม่จำเป็นต้องมีเรกคอร์ดฐานข้อมูลสำรอง สามารถสร้างแบบไดนามิกตามตรรกะ X++ ตัวอย่างต่อไปนี้แสดงให้เห็นถึงแนวทางนี้

ฟิลด์ในส่วนส่วนหัวมักเป็นแบบอ่านอย่างเดียวในแอป

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>ใช้ชุดคำสั่งบนวิธี buildCustomFieldList ของคลาส TSTimesheetSettings เพื่อแสดงฟิลด์ในส่วนหัว

รหัสนี้ควบคุมการตั้งค่าการแสดงผลสำหรับฟิลด์ในแอป ตัวอย่างเช่น จะควบคุมประเภทของฟิลด์ ป้ายกำกับว่าฟิลด์บังคับหรือไม่ และส่วนใดที่ฟิลด์ปรากฏ

ตัวอย่างต่อไปนี้แสดงค่าที่คำนวณในส่วนส่วนหัวในแอป

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>ใช้ชุดคำสั่งบนวิธี buildCustomFieldListForHeader ของคลาส TSTimesheetDetails เพื่อป้อนรายละเอียดแผ่นเวลา

วิธี **buildCustomFieldListForHeader** ถูกใช้กรอกรายละเอียดในส่วนหัวของแผ่นเวลาในแอปมือถือ ใช้เรกคอร์ด TSTimesheetTable เป็นพารามิเตอร์ คุณสามารถใช้ฟิลด์จากเรกคอร์ดนั้นเพื่อกรอกค่าฟิลด์ที่กำหนดเองในแอป ตัวอย่างต่อไปนี้ไม่อ่านค่าใดๆ จากฐานข้อมูล แต่จะใช้ตรรกะ X++ เพื่อสร้างค่าที่คำนวณแล้วซึ่งจะแสดงในแอป


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>โอกาสในการกำหนดค่า/ความสามารถในการขยายอื่นๆ

### <a name="adding-additional-validation-for-the-app"></a>การเพิ่มการตรวจสอบความถูกต้องเพิ่มเติมสำหรับแอป

ตรรกะที่มีอยู่สำหรับการทำงานของแผ่นเวลาในระดับฐานข้อมูลจะยังคงทำงานได้ตามที่คาดไว้ หากต้องการขัดจังหวะการดำเนินการบันทึกหรือส่งให้เสร็จสิ้นและแสดงข้อความแสดงข้อผิดพลาด คุณสามารถเพิ่ม **แสดงข้อผิดพลาด ("ข้อความถึงผู้ใช้")** ไปยังรหัสผ่านส่วนขยายของชุดคำสั่ง นี่คือสามตัวอย่างของวิธีการขยายที่มีประโยชน์:

- ถ้า **validateWrite** ในตาราง TSTimesheetLine ส่งกลับ **เท็จ** ในระหว่างการดำเนินการบันทึกสำหรับรายการแผ่นเวลา ข้อความแสดงข้อผิดพลาดจะปรากฏในแอปมือถือ
- ถ้า **validateSubmit** ในตาราง TSTimesheetTable ส่งกลับ **เท็จ** ในระหว่างการส่งรายการแผ่นเวลา ข้อความแสดงข้อผิดพลาดจะปรากฏกับผู้ใช้
- ตรรกะที่เติมในฟิลด์ (ตัวอย่างเช่น **คุณสมบัติรายการ**) ในระหว่างวิธี **แทรก** บนตาราง TSTimesheetLine จะยังคงทำงานอยู่

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>การซ่อนและทำเครื่องหมายฟิลด์สำเร็จรูปเป็นแบบอ่านอย่างเดียวผ่านการกำหนดค่า

จากพารามิเตอร์โครงการ คุณสามารถสร้างฟิลด์สำเร็จรูปแบบอ่านอย่างเดียวหรือซ่อนไว้ในแอปมือถือ ตั้งค่าตัวเลือกในส่วน **แผ่นเวลามือถือ** ในส่วนแท็บ **แผ่นเวลา** ของหน้า **พารามิเตอร์การจัดการโครงการและการบัญชี**

![พารามิเตอร์โครงการ](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>การเปลี่ยนกิจกรรมที่มีให้เลือกผ่านส่วนขยาย

กิจกรรมที่มีให้เลือกสำหรับโครงการกรอกผ่านวิธี **getActivitiesForProject()** และ **getActivityQuery()** ในคลาส **TsTimesheetProjectService** คุณสามารถใช้ชุดคำสั่งเพื่อเปลี่ยนลักษณะการทำงานนี้เพื่อให้เข้ากับสถานการณ์ทางธุรกิจของคุณสำหรับกิจกรรมที่พร้อมให้เลือกสำหรับโครงการเฉพาะ

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>การป้อนประเภทโครงการเริ่มต้นในรายการแผ่นเวลา

รายการประเภทโครงการเริ่มต้นในรายการแผ่นเวลาเกิดขึ้นในสามระดับ คุณสามารถใช้ชุดคำสั่งเพื่อขยายลักษณะการทำงานในระดับใดระดับหนึ่งหรือทั้งหมดเพื่อให้บรรลุลักษณะการทำงานที่ต้องการ ใช้ลำดับชั้นต่อไปนี้:

1. แอปพยายามใส่หมวดหมู่เริ่มต้นจากทรัพยากรโครงการ ประเภทเริ่มต้นนี้ถูกตั้งค่าในวิธี **getCurrentUserResource** และ **getDelegatedResourcesForCurrentUser** ในคลาส **TSTimesheetSettingsService**
2. หากไม่ได้ระบุหมวดหมู่เริ่มต้นที่ระดับทรัพยากรโครงการ แอปจะพยายามดึงออกจากกิจกรรมโครงการ ประเภทเริ่มต้นนี้ถูกตั้งค่าในวิธี **getActivitiesForProject** ในคลาส **TSTimesheetProjectService**
3. หากไม่ได้ระบุหมวดหมู่เริ่มต้นที่ระดับกิจกรรมโครงการ ประเภทเริ่มต้นจะถูกดึงออกจากพารามิเตอร์โครงการ ประเภทเริ่มต้นนี้ถูกตั้งค่าในวิธี **getProjectDetailsbyRule** ในคลาส **TSTimesheetProjectService**


[!INCLUDE[footer-include](../includes/footer-banner.md)]