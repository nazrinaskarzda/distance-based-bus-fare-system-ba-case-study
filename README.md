# Məsafəyə Əsaslanan Avtobus Gediş Haqqı Sistemi

## Layihə haqqında

Bu layihə Bakı şəhərində tətbiq olunan sabit avtobus tarif modelinin təhlilinə və məsafəyə əsaslanan alternativ ödəniş sisteminin hazırlanmasına həsr olunmuş Business Analysis case study-sidir.

Mövcud sistemdə sərnişin qət etdiyi məsafədən asılı olmayaraq eyni gediş haqqını ödəyir. Təklif olunan modeldə isə ödəniş sərnişinin faktiki qət etdiyi məsafəyə əsasən hesablanır.

## Biznes problemi

Sabit tarif modeli bir sıra maliyyə və əməliyyat problemləri yaradır:

* Qısa və uzun məsafəli səfərlər üçün eyni məbləğin tutulması
* İstifadə həcmi ilə ödəniş arasında uyğunsuzluq
* Marşrutlar üzrə gəlirliliyin dəqiq ölçülə bilməməsi
* Sərnişinlərin minmə və enmə nöqtələri haqqında məlumatın olmaması
* Sərnişin axını və pik saatların effektiv izlənilməməsi
* Marşrut və resurs planlamasının real məlumatlar əvəzinə təxminlərə əsaslanması

## Təklif olunan həll

Yeni sistem `tap-in` və `tap-out` prinsipi əsasında işləyir:

* Sərnişin avtobusa minərkən kartını və ya mobil cihazını validatora yaxınlaşdırır.
* Sistem minmə nöqtəsini və vaxtını qeydə alır.
* Sərnişin avtobusdan enərkən yenidən validatora toxunur.
* GPS məlumatları əsasında qət edilən məsafə müəyyənləşdirilir.
* Gediş haqqı minimum tarif və məsafəyə əsaslanan tarif dərəcəsi üzrə avtomatik hesablanır.

## Sistemin əsas imkanları

* GPS əsaslı minmə və enmə qeydiyyatı
* Məsafəyə əsaslanan avtomatik tarif hesablanması
* Kart balansının real vaxtda yoxlanılması
* Güzəştli sərnişin qruplarına endirimlərin avtomatik tətbiqi
* Transfer qaydalarının idarə olunması
* SMS və mobil tətbiq vasitəsilə qəbz göndərilməsi
* Şübhəli əməliyyatların və fraud hallarının aşkarlanması
* Marşrutlar üzrə gəlir və sərnişin axınının izlənilməsi
* Real-time əməliyyat analitikası və hesabatlılıq

## Aparılmış Business Analysis işləri

Layihə çərçivəsində aşağıdakı fəaliyyətlər yerinə yetirilib:

* Mövcud prosesin və əsas biznes problemlərinin təhlili
* AS-IS və TO-BE proseslərinin modelləşdirilməsi
* Stakeholder-lərin müəyyənləşdirilməsi və qiymətləndirilməsi
* Influence, Interest və Impact analizi
* RACI Matrix hazırlanması
* Stakeholder müsahibə suallarının hazırlanması
* Biznes və stakeholder tələblərinin müəyyənləşdirilməsi
* Funksional və qeyri-funksional tələblərin sənədləşdirilməsi
* Requirements Traceability Matrix hazırlanması
* Edge case-lərin müəyyənləşdirilməsi
* Risk və fərziyyələrin qiymətləndirilməsi
* Risk və fərziyyələr arasında traceability-nin qurulması

## AS-IS və TO-BE prosesləri

Aşağıdakı diaqram mövcud sabit tarif prosesini və təklif olunan məsafəyə əsaslanan tarif prosesini müqayisə edir.

![AS-IS və TO-BE prosesləri](04_AsIs_ToBe_Process.png)

## Əsas sistem tələbləri

| Tələb                                   | İzah                                                                                                                   |
| --------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| **Gündəlik 500,000+ əməliyyat**         | Sistem gündəlik yüksək sayda tap-in, tap-out və ödəniş əməliyyatını idarə etməlidir.                                   |
| **3 saniyə ərzində tarif hesablanması** | Tap-out əməliyyatından sonra gediş haqqı maksimum 3 saniyə ərzində hesablanmalıdır.                                    |
| **99.5%-dən yüksək əlçatanlıq**         | Sistem gün ərzində stabil işləməli və xidmət kəsintiləri minimum səviyyədə saxlanılmalıdır.                            |
| **10 metr GPS dəqiqliyi**               | Tarif hesablamasında istifadə olunan GPS məlumatının xəta payı 10 metrdən çox olmamalıdır.                             |
| **Məlumat təhlükəsizliyi**              | Sərnişin və ödəniş məlumatları şifrələnməli və yalnız səlahiyyətli tərəflər üçün əlçatan olmalıdır.                    |
| **Üç dil dəstəyi**                      | İstifadəçi interfeysi Azərbaycan, rus və ingilis dillərini dəstəkləməlidir.                                            |
| **Offline iş rejimi**                   | İnternet bağlantısı kəsildikdə əməliyyatlar lokal saxlanılmalı və əlaqə bərpa olunduqdan sonra sinxronlaşdırılmalıdır. |

## Hazırlanmış sənədlər

1. [Mövcud prosesin analizi](01_Current_Process_Analysis.docx)
2. [Stakeholder analizi və RACI Matrix](02_Stakeholder_Analysis.xlsx)
3. [Stakeholder müsahibə sualları](03_Stakeholder_Questions.docx)
4. [AS-IS və TO-BE proses diaqramı](04_AsIs_ToBe_Process.png)
5. [Requirements Traceability Matrix](05_Requirements_Traceability_Matrix.xlsx)
6. [Edge Case Analysis](06_Edge_Cases.xlsx)
7. [Risk və Assumption Log](07_Risk_Assumptions_Log.xlsx)

## Nümayiş etdirilən bacarıqlar

* Business Process Analysis
* Requirements Elicitation
* Stakeholder Analysis
* RACI Matrix
* AS-IS / TO-BE Process Modelling
* Business, Functional və Non-Functional Requirements
* Requirements Traceability
* Edge Case Analysis
* Risk və Assumption Management
* BPMN
* IT Business Analysis

---

**Hazırlayan:** Nazrin Askarzada
**Rol:** IT Business Analyst

> **Qeyd:** Bu layihə şəxsi portfolio üçün hazırlanmış konseptual və tədris məqsədli case study-dir. Real qurum tərəfindən sifariş edilməyib və hər hansı təşkilatın rəsmi layihəsini təmsil etmir.
