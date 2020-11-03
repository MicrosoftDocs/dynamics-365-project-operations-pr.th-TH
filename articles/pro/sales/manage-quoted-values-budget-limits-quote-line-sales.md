---
title: รายการใบเสนอราคาตามโครงการ (Pro)
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการใช้รายการใบเสนอราคาตามโครงการสำหรับงานโครงการ (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085862"
---
# <a name="project-based-quote-lines-pro"></a>รายการใบเสนอราคาตามโครงการ (Pro)

_**นำไปใช้กับ:** การปรับใช้งานแบบ Lite - จัดการกับการออกใบแจ้งหนี้ชั่วคราว_

รายการใบเสนอราคาตามโครงการได้รับการออกแบบมาเพื่อช่วยในการประเมินงานโครงการสำหรับการมีส่วนร่วม โครงสร้างของรายการใบเสนอราคาตามโครงการมีการขยายสำหรับการประมาณการโครงการด้วยแนวคิดต่อไปนี้:

- วิธีการเรียกเก็บเงิน
- การแม็ปโครงการและงาน
- คลาสธุรกรรมที่รวมไว้
- วงเงินที่ต้องไม่เกิน
- การตั้งค่าการคิดค่าธรรมเนียม
- การประมาณการโดยใช้รายละเอียดรายการใบเสนอราคา
- ลูกค้าในรายการใบเสนอราคา

ตารางต่อไปนี้ให้ข้อมูลเกี่ยวกับฟิลด์บนแท็บ **ทั่วไป** ของรายการใบเสนอราคาตามโครงการ ฟิลด์เหล่านี้ช่วยตั้งค่าพื้นฐานสำหรับการประมาณการค่าเบื้องต้นอย่างละเอียดสำหรับงานโครงการ

| **ฟิลด์** | **ความเกี่ยวข้อง วัตถุประสงค์ และคำแนะนำ** | **ผลกระทบขั้นปลาย** |
| --- | --- | --- |
| ชื่อ | ชื่อของรายการใบเสนอราคาที่จะช่วยคุณระบุส่วนประกอบที่ไม่ต่อเนื่องของใบเสนอราคาที่กำลังประมาณการ | คัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา |
| วิธีการเรียกเก็บเงิน | ในใบเสนอราคาที่สร้างขึ้นจากโอกาสทางการขาย ค่านี้จะมีการคัดลอกจากฟิลด์ที่เกี่ยวข้องในรายการโอกาสทางการขาย ฟิลด์นี้ประกอบด้วยรูปแบบการทำสัญญาหลักสองแบบที่สนับสนุนโดย Dynamics 365 Project Operations:</br>- ราคาคงที่</br>- เวลาและวัสดุ| ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา |
| Project | ใช้ฟิลด์ที่ไม่บังคับนี้เพื่อระบุโครงการที่จะใช้เพื่อส่งมอบงานในการมีส่วนร่วมนี้ เมื่อโครงการถูกแม็ปกับรายการใบเสนอราคา จะช่วยในการตั้งค่างานที่คิดค่าธรมเนียมและยังนำการประมาณราคาตามโครงการไปใช้กับรายการใบเสนอราคาเป็นรายละเอียดรายการใบเสนอราคา เมื่อไม่ได้แม็ปโครงการกับรายการใบเสนอราคาตามโครงการ ควรสร้างการประมาณด้วยตนเองโดยการสร้างรายละเอียดรายการใบเสนอราคาแต่ละรายการ | ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา|
| งานที่รวมไว้ | ระบุว่ารายการใบเสนอราคานี้มีการใช้สำหรับงานโครงการทั้งหมดหรือบางส่วนสำหรับโครงการที่เลือก ฟิลด์นี้มีค่าที่เป็นไปได้ต่อไปนี้:</br>- งานโครงการทั้งหมด</br>- งานโครงการที่เลือกเท่านั้น</br>ค่าว่างในฟิลด์นี้เทียบเท่ากับตัวเลือก **งานโครงการทั้งหมด** | เมื่อมีการเลือก **งานโครงการที่เลือกเท่านั้น** จากนั้นในเพจโครงการ แท็บ **การตั้งค่าการเรียกเก็บเงินงาน** ช่วยให้คุณสามารถเลือกงานเฉพาะเพื่อเชื่อมโยงกับรายการใบเสนอราคานี้ ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา |
| รวมเวลา | ค่าสถานะ **ใช่**/**ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานในโครงการที่เลือกจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้หรือไม่ ค่า **ไม่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้ ค่า **ใช่** ระบุว่าธุรกรรมเวลาหรือต้นทุนแรงงานจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้ | ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา |
| รวมค่าใช้จ่าย | ค่าสถานะ **ใช่**/**ไม่** ระบุว่าต้นทุนค่าใช้จ่ายในโครงการที่เลือกจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้หรือไม่ ค่า **ไม่** ระบุว่าต้นทุนค่าใช้จ่ายจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้ ค่า **ใช่** ระบุว่าต้นทุนค่าใช้จ่ายจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้ | ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา |
| รวมค่าธรรมเนียม | ค่าสถานะ **ใช่**/**ไม่** ระบุว่าค่าธรรมเนียมในโครงการที่เลือกจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้หรือไม่ ค่า **ไม่** ระบุว่าต้นทุนค่าธรรมเนียมจะไม่รวมอยู่ในประมาณการในรายการใบเสนอราคานี้ ค่า **ใช่** ระบุว่าต้นทุนค่าธรรมเนียมจะรวมอยู่ในประมาณการในรายการใบเสนอราคานี้ | ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา |
| จำนวนเงินตามใบเสนอราคา | นี่คือจำนวนเงินที่จะเสนอให้กับลูกค้าสำหรับงานทั้งหมดที่คาดการณ์ไว้ในรายการใบเสนอราคาตามโครงการนี้ ในใบเสนอราคาที่สร้างขึ้นจากโอกาสทางการขาย ค่านี้จะมีการคัดลอกจากฟิลด์ **งบประมาณของลูกค้า** ในรายการโอกาสทางการขาย เมื่อรายการใบเสนอราคาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและมีการสรุปจากจำนวนเงินในรายละเอียดรายการใบเสนอราคา | ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา |
| ภาษีที่ประเมิน | นี่คือฟิลด์ที่แก้ไขได้สำหรับผู้ใช้ในการเพิ่มจำนวนภาษีโดยประมาณในรายการใบเสนอราคา เมื่อรายการใบเสนอราคาตามโครงการมีรายละเอียดรายการ ฟิลด์นี้จะถูกล็อกสำหรับการแก้ไขและมีการสรุปจากจำนวนเงินภาษีในรายละเอียดรายการใบเสนอราคา | ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา |
| จำนวนเงินตามใบเสนอราคาหลังหักภาษี | ฟิลด์นี้คือจำนวนเงินของรายการใบเสนอราคาหลังหักภาษีและเป็นแบบอ่านอย่างเดียว จำนวนเงินในฟิลด์นี้มีการคำนวณเป็น *จำนวนเงินที่เสนอราคา + ภาษี* | ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา |
| วงเงินที่ต้องไม่เกิน | ฟิลด์นี้สามารถแก้ไขได้และพร้อมใช้งานในรายการใบเสนอราคาตามโครงการที่มีวิธีการเรียกเก็บเงินสำหรับ **เวลาและวัสดุ** | ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา |
| งบประมาณของลูกค้า | ฟิลด์นี้สามารถแก้ไขได้และมีการคัดลอกจากฟิลด์ที่สัมพันธ์กันในรายการโอกาสทางการขายหากมีการสร้างใบเสนอราคาจากโอกาสทางการขาย | ค่าฟิลด์นี้จะมีการคัดลอกไปยังรายละเอียดการให้บริการตามสัญญาโครงการที่สร้างขึ้นจากรายการใบเสนอราคานี้เมื่อชนะการเสนอราคา |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>กฎการตรวจสอบความถูกต้องสำหรับฟิลด์บนแท็บ ทั่วไป ของรายการใบเสนอราคาตามโครงการ

**กฎข้อที่ 1** : ถ้าฟิลด์ **งานที่รวมไว้** ว่างเปล่าหรือหากตั้งค่าเป็น **งานโครงการทั้งหมด** โครงการจะรวมอยู่ในรายการใบเสนอราคา

**กฎข้อที่ 2** : ถ้าฟิลด์ **งานที่รวมไว้** ว่างเปล่าหรือหากตั้งค่าเป็น **งานโครงการทั้งหมด** โครงการและคลาสธุรกรรมบางรายการสามารถรวมอยู่ในรายการใบเสนอราคาตามโครงการของใบเสนอราคาเดียวเท่านั้น

**กฎข้อที่ 3** : ถ้าฟิลด์ **งานที่รวมไว้** ตั้งค่าเป็น **งานโครงการที่เลือกเท่านั้น** โครงการและคลาสธุรกรรมบางรายการสามารถรวมอยู่ในรายการใบเสนอราคาตามโครงการของใบเสนอราคาหลายรายการ

**กฎข้อที่ 4** : หากโอกาสทางการขายมีใบเสนอราคาหลายใบ สามารถมีรายการใบเสนอราคาจากใบเสนอราคาที่ต่างกันซึ่งการอ้างอิงโครงการเดียวกันทั้งหมดและมีคลาสธุรกรรมเดียวกัน

**กฎข้อที่ 5** : หากใบเสนอราคาไม่ได้อยู่ในโอกาสทางการขายเดียวกัน ก็จะไม่สามารถรวมโครงการและคลาสธุรกรรมเดียวกันได้

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>โอกาสทางการขาย</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>ใบเสนอราคา</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>รายการใบเสนอราคา</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="90" valign="top">
                <p>
                    <strong>งานที่รวมไว้</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>รวมเวลา</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>รวมค่าใช้จ่าย</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>รวม</strong>
                </p>
                <p>
                    <strong>ค่าธรรมเนียม</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>ถูกต้อง/ไม่ถูกต้อง</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>เหตุผล</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ร1 </p>
            </td>
            <td width="90" valign="top">
                <p>
ว่างเปล่า </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="42" valign="top">
                <p>
มี </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
ไม่ถูกต้อง </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
การละเมิดกฎ #2 เวลา ค่าใช้จ่าย และค่าธรรมเนียมของโครงการ P1 รวมอยู่ในรายการใบเสนอราคา QL1 และ QL2
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
ร1 </p>
            </td>
            <td width="90" valign="top">
                <p>
ว่างเปล่า </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="42" valign="top">
                <p>
มี </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ร1 </p>
            </td>
            <td width="90" valign="top">
                <p>
ว่างเปล่า </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
มี </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
ไม่ถูกต้อง </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
การละเมิดกฎ #2 เวลาและค่าธรรมเนียมของโครงการ P1 รวมอยู่ในรายการใบเสนอราคา QL1 และ QL2
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
ร1 </p>
            </td>
            <td width="90" valign="top">
                <p>
ว่างเปล่า </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="42" valign="top">
                <p>
มี </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ร1 </p>
            </td>
            <td width="90" valign="top">
                <p>
ว่างเปล่า </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
มี </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
ถูกต้อง </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
เวลาและค่าธรรมเนียมของโครงการ P1 รวมอยู่ใน QL1
ค่าใช้จ่ายในโครงการ P1 รวมอยู่ใน QL2
ไม่มีการทับซ้อนกันในสิ่งที่รวมอยู่ในแต่ละรายการใบเสนอราคา และจะถูกต้อง
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
ร1 </p>
            </td>
            <td width="90" valign="top">
                <p>
ว่างเปล่า </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ร1 </p>
            </td>
            <td width="90" valign="top">
                <p>
งานที่เลือกเท่านั้น </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="42" valign="top">
                <p>
มี </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
ไม่ถูกต้อง </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
การละเมิดกฎ #2 ข้างต้น </p>
                <p>
Q1 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับงานย่อยในโครงการ P1
                </p>
                <p>
QL2 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับโครงการ P1 ทั้งหมดและทับซ้อนกับสิ่งที่รวมอยู่ใน Q1
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
ร1 </p>
            </td>
            <td width="90" valign="top">
                <p>
ว่างเปล่า </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="42" valign="top">
                <p>
มี </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ร1 </p>
            </td>
            <td width="90" valign="top">
                <p>
งานที่เลือกเท่านั้น </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="42" valign="top">
                <p>
มี </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
ถูกต้อง </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
ตามกฎ #3 ข้างต้น </p>
                <p>
Q1 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับงานย่อยในโครงการ P1
                </p>
                <p>
QL2 ประกอบด้วยเวลา ค่าใช้จ่าย และค่าธรรมเนียมสำหรับงานย่อยในโครงการ P1
                </p>
                <p>
การตรวจสอบความถูกต้องเพิ่มเติมเพียงอย่างเดียวคือชุดย่อยของงานบน QL1 ซึ่งแตกต่างจากชุดย่อยของงานบน QL2 เพื่อให้แน่ใจว่าไม่มีการทับซ้อนกัน ระบบดำเนินการนี้ทำได้เมื่อเกี่ยวข้องกับงาน
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
ร1 </p>
            </td>
            <td width="90" valign="top">
                <p>
งานที่เลือกเท่านั้น </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="42" valign="top">
                <p>
มี </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ร1 </p>
            </td>
            <td width="90" valign="top">
                <p>
งานโครงการทั้งหมดหรือว่างเปล่า </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="42" valign="top">
                <p>
มี </p>
            </td>
            <td width="54" valign="top">
                <p>
ถูกต้อง </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
ตามกฎ #5, Q1 และ Q2 เป็นใบเสนอราคาสองรายการในโอกาสทางการขายเดียวกัน ดังนั้นทั้งคู่จึงสามารถประมาณการสำหรับส่วนประกอบเดียวกันของโครงการได้
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ร1 </p>
            </td>
            <td width="90" valign="top">
                <p>
งานโครงการทั้งหมดหรือว่างเปล่า </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="42" valign="top">
                <p>
มี </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ร1 </p>
            </td>
            <td width="90" valign="top">
                <p>
งานโครงการทั้งหมดหรือว่างเปล่า </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="42" valign="top">
                <p>
มี </p>
            </td>
            <td width="54" valign="top">
                <p>
ถูกต้อง </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
ตามกฎ #4, Q1 และ Q2 เป็นใบเสนอราคาสองรายการในโอกาสทางการขายที่ต่างกัน ดังนั้นทั้งคู่จึงสามารถประมาณการสำหรับส่วนประกอบเดียวกันของโครงการเดียวกันได้
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ร1 </p>
            </td>
            <td width="90" valign="top">
                <p>
งานโครงการทั้งหมดหรือว่างเปล่า </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="48" valign="top">
                <p>
มี </p>
            </td>
            <td width="42" valign="top">
                <p>
มี </p>
            </td>
            <td width="54" valign="top">
                <p>
ไม่ถูกต้อง </p>
            </td>
        </tr>
    </tbody>
</table>
