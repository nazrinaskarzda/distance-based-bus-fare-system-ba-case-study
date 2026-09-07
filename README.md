# Məsafəyə Əsaslanan Avtobus Gediş Haqqı Sistemi

## Layihə haqqında

2 km və 18 km yol gedən sərnişin eyni gediş haqqını ödəməlidirmi?

Bu Business Analysis case study-si mövcud sabit tarif modelini təhlil edir və gediş haqqının faktiki məsafəyə əsasən hesablandığı alternativ sistem təklif edir.

## Problem

Sabit tarif modeli:

* Qısa və uzun səfərlər arasında qiymət uyğunsuzluğu yaradır.
* Sərnişinlərin minmə və enmə nöqtələrini qeydə almır.
* Marşrut gəlirliliyinin ölçülməsini çətinləşdirir.
* Resurs və marşrut planlamasını real məlumatlarla dəstəkləmir.

## Təklif olunan həll

Sərnişin avtobusa minərkən `tap-in`, enərkən isə `tap-out` edir. Sistem GPS vasitəsilə qət edilən məsafəni müəyyənləşdirir və gediş haqqını avtomatik hesablayır.

Həllə həmçinin balans yoxlanılması, güzəştli tariflər, transfer qaydaları, elektron qəbz, offline rejim və fraud monitorinqi daxildir.

## Mənim rolum

IT Biznes Analitik kimi:

* AS-IS və TO-BE proseslərini modelləşdirdim.
* Stakeholder analizi və RACI Matrix hazırladım.
* Stakeholder müsahibə suallarını müəyyənləşdirdim.
* Biznes, funksional və qeyri-funksional tələbləri sənədləşdirdim.
* Requirements Traceability Matrix qurdum.
* Edge case, risk və fərziyyələri təhlil etdim.

## Proses modeli

![AS-IS və TO-BE prosesləri](04_AsIs_ToBe_Process.png)

## Layihə sənədləri

* [Mövcud prosesin analizi](01_Current_Process_Analysis.docx)
* [Stakeholder analizi və RACI Matrix](02_Stakeholder_Analysis.xlsx)
* [Stakeholder sualları](03_Stakeholder_Questions.docx)
* [Requirements Traceability Matrix](05_Requirements_Traceability_Matrix.xlsx)
* [Edge Case Analysis](06_Edge_Cases.xlsx)
* [Risk və Assumption Log](07_Risk_Assumptions_Log.xlsx)

## İstifadə edilən bacarıqlar

`Business Analysis` · `BPMN` · `AS-IS / TO-BE` · `Stakeholder Analysis` · `RACI` · `Requirements Engineering` · `Traceability` · `Risk Analysis`

---

**Hazırlayan:** Nazrin Askarzada
**Rol:** IT Business Analyst

> Bu, şəxsi portfolio üçün hazırlanmış konseptual case study-dir və real qurumun rəsmi layihəsini təmsil etmir.
