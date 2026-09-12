# Məsafəyə əsaslanan avtobus gediş haqqı sistemi

**Business Analysis Case Study**

Layihə mövcud sabit tarif modelindən məsafəyə əsaslanan dinamik gediş haqqı modelinə keçidi təhlil edən konseptual biznes analizi işidir. Layihədə cari vəziyyət, təklif olunan həll, maraqlı tərəflər, tələblər, risklər, xüsusi hallar və gözlənilən biznes nəticələri təqdim olunur.

> Əsas sual: 2 km və 18 km səfər edən sərnişinlər eyni gediş haqqını ödəməlidirlərmi?

## Layihənin məqsədləri

- Gediş haqqını faktiki səfər məsafəsinə əsasən hesablamaq
- Qısa və uzun məsafəli səfərlər üçün daha ədalətli tarif modeli qurmaq
- Güzəştli sərnişin qrupları üçün endirimlər tətbiq etmək
- Transfer qaydalarını avtomatlaşdırmaq
- Elektron ödəniş imkanlarını genişləndirmək
- Marşrutlar üzrə gəlir və sərnişin axınını izləmək
- Şübhəli əməliyyatları müəyyənləşdirmək
- Gəliri 15-20%, sərnişin məmnuniyyətini isə 25–30% artırmaq

## Biznes problemi

### Cari vəziyyət - AS-IS

Mövcud modeldə səfərin məsafəsindən asılı olmayaraq bütün sərnişinlər eyni məbləği ödəyirlər.

| Səfər məsafəsi | Gediş haqqı |
| --- | ---: |
| 2 km | 0,50 AZN |
| 8 km | 0,50 AZN |
| 18 km | 0,50 AZN |

Bu model aşağıdakı problemlərə səbəb olur:

| Problem | Təsir |
| --- | --- |
| Qiymət uyğunsuzluğu | Qısa və uzun məsafəli səfərlər üçün eyni tarif tətbiq olunur |
| Məlumat çatışmazlığı | Minmə və enmə nöqtələri qeydə alınmadığı üçün faktiki səfər məsafəsi bilinmir |
| Sərnişin axınının görünməməsi | Pik və qeyri-pik saatlardakı tələbi dəqiq ölçmək mümkün deyil |
| Marşrut gəlirliliyinin ölçülməməsi | Marşrutlar üzrə gəlir və xərc müqayisəsi aparılmır |
| Gəlir itkisi | Uzun məsafəli səfərlər üzrə potensial gəlir əldə edilmir |
| Məhdud sosial tariflər | Güzəştli qruplar üçün çevik qiymət mexanizmi yoxdur |

### Problemin təxmini ölçüsü

| Maliyyə göstəricisi | Dəyər |
| --- | ---: |
| Cari illik gəlir | 50 milyon AZN |
| Potensial illik gəlir itkisi | 10 milyon AZN |
| Əlavə əməliyyat xərci | 2 milyon AZN |
| **Təxmini ümumi illik itki** | **12 milyon AZN** |

| Sərnişin göstəricisi | Dəyər |
| --- | ---: |
| Cari gündəlik sərnişin sayı | 200 000 |
| Potensial gündəlik azalma | 60 000 |
| Potensial azalma faizi | 30% |

> Rəqəmlər konseptual biznes modeli üçün istifadə olunan ilkin fərziyyələrdir.

## Təklif olunan həll - TO-BE

Məsafəyə əsaslanan dinamik tarif sistemi sərnişinin minmə və enmə nöqtələrini qeydə alır, qət edilən məsafəni hesablayır və uyğun gediş haqqını avtomatik tətbiq edir.

### Səfər prosesi

1. Sərnişin NFC kartı, bank kartı və ya mobil tətbiq vasitəsilə minmə əməliyyatını qeyd edir.
2. Sistem minmə nöqtəsini və vaxtını qeydə alır.
3. Səfər müddətində marşrut və məsafə məlumatları izlənilir.
4. Sərnişin enərkən çıxış əməliyyatını qeyd edir.
5. Sistem məsafəni, tarif növünü, güzəşti və vaxt əmsalını nəzərə alaraq yekun məbləği hesablayır.
6. Məbləğ balansdan çıxılır və sərnişinə elektron qəbz təqdim olunur.

### Hesablama nümunəsi

7,5 km səfər üçün baza tarifi 0,40 AZN, hər əlavə kilometr üzrə tarif 0,05 AZN və pik saat əmsalı 1,2 olduqda:

- baza tarifi: 0,40 AZN;
- əlavə məsafə: 6,5 × 0,05 = 0,325 AZN;
- pik saatdan əvvəlki məbləğ: 0,725 AZN;
- yekun məbləğ: 0,725 × 1,2 = 0,87 AZN;
- 5 AZN balansdan sonra qalan məbləğ: 4,13 AZN.

## Tarif modeli

### Məsafəyə əsaslanan tariflər

| Xətt növü | Baza tarifi | Əlavə kilometr | Pik saat əmsalı | Gecə əmsalı |
| --- | ---: | ---: | ---: | ---: |
| Qısa şəhərdaxili | 0,40 AZN | 0,05 AZN | 1,2 | 0,7 |
| Şəhərdaxili | 0,50 AZN | 0,06 AZN | 1,3 | 0,8 |
| Şəhərlərarası | 1,00 AZN | 0,10 AZN | 1,1 | 0,9 |

| Məsafə | Təxmini tarif aralığı |
| --- | ---: |
| 0–2 km | 0,40–0,50 AZN |
| 2–5 km | 0,55–0,70 AZN |
| 5–10 km | 0,75–1,00 AZN |
| 10–15 km | 1,10–1,40 AZN |
| 15 km-dən çox | 1,50–2,00 AZN |

### Güzəştli tariflər

| Kateqoriya | Endirim | Aylıq paket nümunəsi |
| --- | ---: | ---: |
| Tələbələr | 50% | 20 AZN / 100 səfər |
| Pensiyaçılar | 40% | 25 AZN / 120 səfər |
| Sosial güzəşt hüququ olan digər şəxslər | 30% | 30 AZN / 100 səfər |
| Əlilliyi olan şəxslər | 35% | 22 AZN / 120 səfər |
| 6–16 yaşlı uşaqlar | 60% | 15 AZN / 150 səfər |
| 6 yaşdan kiçik uşaqlar | Pulsuz | — |

Güzəştlər uyğun sərnişin profilinə bağlanır və ödəniş zamanı avtomatik tətbiq olunur.

### Transfer qaydaları

| Transfer növü | Vaxt pəncərəsi | Güzəşt | Əlavə şərt |
| --- | --- | ---: | --- |
| Eyni marşrut üzrə transfer | 60 dəqiqə | 50% | Təkrar səfər ayrıca yoxlanılır |
| Fərqli marşrutlar üzrə transfer | 90 dəqiqə | 25% | Ən çox 3 transfer |
| Eyni gün geri dönüş | Eyni gün | 50% | Eyni istiqamət və məsafə meyarları tətbiq olunur |

### Vaxta əsaslanan əmsallar

| Vaxt aralığı | Əmsal | Tətbiq səbəbi |
| --- | ---: | --- |
| 07:00–09:00 | 1,3 | Səhər pik saatı |
| 10:00–16:00 | 1,0 | Standart tarif |
| 16:00–19:00 | 1,4 | Axşam pik saatı |
| 19:00–23:00 | 1,1 | Axşam tarifi |
| 23:00–06:00 | 0,7 | Gecə güzəşti |
| Həftəsonu | 0,9 | Qeyri-pik səfərlərin təşviqi |

Əmsalların məqsədi sərnişin axınını gün ərzində daha balanslı bölmək və marşrut tutumundan səmərəli istifadə etməkdir.

## Ödəniş üsulları

| Ödəniş üsulu | Əsas imkanlar |
| --- | --- |
| NFC nəqliyyat kartı | Balansın artırılması, avtomatik yükləmə, bonus sistemi və məhdud oflayn əməliyyat |
| Mobil tətbiq | QR kodla minmə və enmə, balans, səfər tarixçəsi, elektron qəbz və bildirişlər |
| Kontaktsız bank kartı | Birbaşa ödəniş və ayrıca nəqliyyat kartına ehtiyac olmadan istifadə |

## Monitorinq və şübhəli əməliyyatların aşkarlanması

Sistem aşağıdakı halları izləməlidir:

- beş saniyə ərzində təkrarlanan minmə əməliyyatları;
- real olmayan məsafə və sürət məlumatları;
- üç saatdan artıq açıq qalan səfərlər;
- bir gün ərzində qeyri-adi sayda əməliyyat;
- eyni kart və ya cihaz məlumatının təkrarlanması.

Şübhəli hal aşkarlandıqda sistem xəbərdarlıq yaradır, kartı müvəqqəti məhdudlaşdıra və əməliyyatı araşdırma üçün aidiyyəti komandaya göndərə bilər.

## AS-IS və TO-BE müqayisəsi

| Göstərici | AS-IS | TO-BE | Gözlənilən dəyişiklik |
| --- | ---: | ---: | ---: |
| Tranzaksiya müddəti | 30 saniyə | 2–3 saniyə | Təxminən 90% azalma |
| Məlumatların tamlığı | 40% | 99% | 59 faiz bəndi artım |
| Səhv nisbəti | 5–8% | 0,5%-dən az | Təxminən 90% azalma |
| Sərnişin üzrə orta gəlir | 0,50 AZN | 0,72 AZN | 44% artım |
| İstifadəçi məmnuniyyəti | 68% | 92% | 24 faiz bəndi artım |
| Real vaxt məlumatlarının mövcudluğu | 0% | 100% | Tam görünürlük |
| Təxmini illik gəlir | 50 milyon AZN | 62 milyon AZN | 24% artım |

## Maraqlı tərəflərin təhlili

| Maraqlı tərəf | Rolu | Əsas gözləntisi | Əsas narahatlığı |
| --- | --- | --- | --- |
| Şəhər nəqliyyat qurumu | Sponsor və siyasət sahibi | Daha ədalətli və ölçülə bilən tarif sistemi | İctimai qəbul və tənzimləyici uyğunluq |
| Nəqliyyat şirkətinin rəhbərliyi | Biznes sahibi | Gəlir və əməliyyat səmərəliliyinin artması | İlkin investisiya və istifadəçi qəbulu |
| Maliyyə direktoru | Büdcə sahibi | İnvestisiyanın əsaslandırılması | Xərc artımı və gəlirlilik riski |
| Sərnişinlər | Son istifadəçilər | Ədalətli qiymət və rahat ödəniş | Texniki nasazlıq və məlumat məxfiliyi |
| Avtobus sürücüləri | Əməliyyat istifadəçiləri | Sadə və etibarlı proses | Əlavə əməliyyat yükü və təlim ehtiyacı |
| İT komandası | Texniki icraçı | Miqyaslana bilən və idarə olunan həll | İnteqrasiya və dəstək yükü |
| Bank və ödəniş tərəfdaşı | Ödəniş təminatçısı | Tranzaksiya sayının artması | Yüksək yük və fırıldaqçılıq riski |
| Audit və uyğunluq komandası | Nəzarət tərəfi | Tam audit izi və hüquqi uyğunluq | Məlumatların qorunması |

## Tələblər

### Biznes tələbləri

| ID | Tələb | Prioritet | Qəbul meyarı |
| --- | --- | --- | --- |
| BR-001 | Gediş haqqı faktiki məsafəyə əsasən avtomatik hesablanmalıdır | Kritik | Hesablanan məsafə üzrə xəta 2%-dən azdır |
| BR-002 | Güzəştli sərnişin kateqoriyalarına endirim avtomatik tətbiq olunmalıdır | Yüksək | Endirim sərnişin profilinə və tarif qaydasına uyğun hesablanır |
| BR-003 | Şəxsi məlumatlar qüvvədə olan məlumatların qorunması tələblərinə uyğun saxlanılmalıdır | Kritik | Məlumatlar şifrələnir, girişlər qeydə alınır və saxlanma müddəti idarə olunur |
| BR-004 | Yeni tarif modeli gəlirin ən azı 20% artmasına imkan verməlidir | Yüksək | Orta gediş haqqı və ümumi gəlir hədəfləri hesabatda izlənilir |
| BR-005 | Sərnişin məmnuniyyəti artırılmalıdır | Yüksək | CSAT, NPS, tətbiqdən istifadə və dəstək müraciətləri izlənilir |

### Funksional tələblər

| ID | Funksiya | Əsas qəbul meyarı |
| --- | --- | --- |
| FR-001 | Minmə və enmə qeydiyyatı | NFC və QR əməliyyatı 2 saniyədən az müddətdə qeydə alınır |
| FR-002 | GPS əsasında məsafənin hesablanması | Ölçülən məsafə faktiki məsafədən ən çox 5% fərqlənir |
| FR-003 | Dinamik vaxt əmsalının tətbiqi | Əmsal vaxt və gün qaydasına uyğun avtomatik yenilənir |
| FR-004 | Nəqliyyat kartlarının idarə edilməsi | Balans, avtomatik yükləmə, bloklama və kartın dəyişdirilməsi dəstəklənir |
| FR-005 | Real vaxt idarəetmə paneli | Sərnişin sayı, gəlir, sistem vəziyyəti və xəbərdarlıqlar 5 saniyədən gec olmayaraq yenilənir |
| FR-006 | Mobil tətbiq | Balans, səfər tarixçəsi, QR ödəniş, müraciət və bildiriş funksiyaları təqdim olunur |

### Qeyri-funksional tələblər

| Kateqoriya | Tələb |
| --- | --- |
| Performans | Minmə və enmə əməliyyatı 2 saniyədən, ödəniş emalı 3 saniyədən az çəkməlidir |
| Əlçatanlıq | Sistem üzrə illik əlçatanlıq ən azı 99,9% olmalıdır |
| Bərpa | RTO 15 dəqiqədən, RPO isə 1 dəqiqədən az olmalıdır |
| Təhlükəsizlik | Məlumatlar saxlanarkən və ötürülərkən şifrələnməli, rol əsaslı giriş və audit qeydləri tətbiq edilməlidir |
| İstifadə rahatlığı | İnterfeys Azərbaycan, rus və ingilis dillərini, həmçinin WCAG 2.1 AA əlçatanlıq tələblərini dəstəkləməlidir |
| Miqyaslanma | Sistem ən azı 100 000 eyni vaxtlı istifadəçini və saniyədə 1 000 əməliyyatı dəstəkləməlidir |
| Texniki xidmət | API sənədləşdirilməsi, avtomatlaşdırılmış test və yerləşdirmə prosesi təmin edilməlidir |

## Risklər və fərziyyələr

### Əsas risklər

| Risk | Ehtimal | Təsir | Qarşı tədbir |
| --- | --- | --- | --- |
| GPS məlumatlarının qeyri-dəqiq olması | Yüksək | Orta | GPS, BLE və əvvəlcədən hesablanmış marşrut məlumatlarının birlikdə istifadəsi |
| Sərnişinlərin yeni sistemi qəbul etməməsi | Orta | Yüksək | Pilot proqram, keçid dövrü, maarifləndirmə və təşviq kampaniyası |
| Kart klonlanması və saxta əməliyyatlar | Orta | Yüksək | Real vaxt monitorinqi, təhlükəsiz kart texnologiyası və audit |
| Mövcud sistemlə inteqrasiyanın mürəkkəbliyi | Orta | Yüksək | Texniki uyğunluq yoxlaması, pilot marşrut və mərhələli tətbiq |
| Sürücülərin dəyişikliklərə müqaviməti | Yüksək | Orta | Təlim, aydın prosedurlar və davamlı əməliyyat dəstəyi |
| Maliyyə modelinin gözlənilən nəticəni verməməsi | Aşağı | Yüksək | Ssenari analizi, pilot nəticələrinin ölçülməsi və tariflərin yenidən tənzimlənməsi |

### Əsas fərziyyələr

| Fərziyyə | Əhəmiyyət | Yoxlama üsulu |
| --- | --- | --- |
| Şəhər idarəsi layihəyə lazımi dəstəyi verəcək | Kritik | Rəsmi təsdiq və müntəzəm rəhbərlik görüşləri |
| GPS, NFC və mobil internet infrastrukturu əlçatandır | Yüksək | Texniki uyğunluq araşdırması |
| Sərnişinlər keçid dövründən sonra sistemi qəbul edəcəklər | Kritik | Pilot proqram və istifadəçi rəyləri |
| Məsafəyə əsaslanan tarif ictimai baxımdan qəbul olunacaq | Yüksək | Sorğular və məlumatlandırma kampaniyası |
| 5 milyon AZN ilkin büdcə təsdiqlənəcək | Kritik | Maliyyə təsdiqi və büdcə sənədləri |
| 20 nəfərlik texniki komanda əlçatan olacaq | Yüksək | Resurs planı və işə qəbul planı |

## Xüsusi hallar

| Hal | Sistem davranışı |
| --- | --- |
| Təkrarlanan minmə əməliyyatı | Beş saniyə ərzində eyni kartla edilən ikinci əməliyyat nəzərə alınmır |
| Tuneldə GPS siqnalının itməsi | Son etibarlı nöqtə və əvvəlcədən hesablanmış marşrut məlumatı istifadə olunur |
| Enmə əməliyyatının qeydə alınmaması | Üç saatdan sonra səfər avtomatik bağlanır və əvvəlcədən müəyyən edilmiş maksimum tarif tətbiq olunur |
| Güzəşt müddətində transfer | Sistem 90 dəqiqəlik pəncərəni yoxlayır və uyğun endirimi avtomatik tətbiq edir |
| İnternet bağlantısının olmaması | Əməliyyat cihazda müvəqqəti saxlanılır və bağlantı bərpa olunduqda sinxronlaşdırılır |
| Balansın kifayət etməməsi | Müəyyən edilmiş limit daxilində mənfi balansa icazə verilir və balans artırma bildirişi göstərilir |
| Ailə hesabında bir neçə kart | Əlavə kartlar əsas hesaba bağlanır və əməliyyatlar vahid hesabatda göstərilir |
| Tarif dəyişikliyi sərhədində səfər | Səfərin əvvəlində qüvvədə olan tarif qaydası tətbiq olunur |

## Layihə sənədləri

| Mərhələ | Sənəd |
| --- | --- |
| Cari vəziyyətin təhlili | [Cari prosesin təhlili](./Current_Process_Analysis.pdf) |
| Proses modelləşdirilməsi | [AS-IS və TO-BE prosesləri](./AsIs_ToBe_Process.png) |
| Xüsusi halların təhlili | [Xüsusi hallar](./Edge_Cases.pdf) |
| Maraqlı tərəflərin təhlili | [Maraqlı tərəflərin təhlili](./Stakeholder_Analysis.xlsx.pdf) |
| Tələblərin toplanması | [Maraqlı tərəflər üçün müsahibə sualları](./Stakeholder_Questions.pdf) |
| Tələblərin sənədləşdirilməsi | [Biznes tələbləri](./Business_Requirements.docx) |
| Tələblərin sənədləşdirilməsi | [Funksional tələblər](./Functional_Requirements.xlsx) |
| Tələblərin izlənilməsi | [Tələblərin izlənilməsi matrisi](./Requirements_Traceability_Matrix.xlsx.pdf) |
| Risklərin idarə edilməsi | [Risk və fərziyyələr jurnalı](./Risk_Assumptions_Log.xlsx.pdf) |
| İcra planı | [Tətbiq yol xəritəsi](./Implementation_Roadmap.xlsx) |

## Gözlənilən faydalar

### Maliyyə təsiri

| Göstərici | İlkin qiymətləndirmə |
| --- | ---: |
| Cari illik gəlir | 50 milyon AZN |
| Birinci il üçün proqnozlaşdırılan gəlir | 62 milyon AZN |
| Birinci il üzrə tətbiq xərci | 5 milyon AZN |
| Birinci il üzrə xalis əlavə fayda | 7 milyon AZN |
| Üç il üzrə ümumi əlavə gəlir | 20,5 milyon AZN |
| Üç il üzrə əməliyyat qənaəti | 6 milyon AZN |
| Üç il üzrə ümumi investisiya | 12 milyon AZN |
| Üç il üzrə xalis fayda | 14,5 milyon AZN |
| Üç illik ROI | 121% |
| İnvestisiyanın geri dönüş müddəti | 9 ay |
| NPV - 10% diskont dərəcəsi ilə | 8,2 milyon AZN |
| IRR | 45% |

> Maliyyə göstəriciləri real məlumatlar deyil; konseptual ssenari əsasında hazırlanmış ilkin hesablamalardır.

### Əməliyyat və istifadəçi faydaları

| Sahə | Cari vəziyyət | Hədəf vəziyyət |
| --- | ---: | ---: |
| Tranzaksiya müddəti | 30 saniyə | 2 saniyə |
| Səhv nisbəti | 5–8% | 0,5%-dən az |
| Əl ilə müdaxilə | 20% | 5% |
| Real vaxt sərnişin məlumatları | Mövcud deyil | 100% görünürlük |
| Ödəniş rahatlığı | 40% | 95% |
| Tarif şəffaflığı | 30% | 99% |
| Dəstək müraciətinə cavab müddəti | 24 saat | 1 saatdan az |
| Sərnişin məmnuniyyəti | 68% | 92% |
| Audit tarixçəsi | Mövcud deyil | 100% qeydiyyat |

## İcra planı

| Mərhələ | Müddət | Əsas fəaliyyətlər |
| --- | --- | --- |
| Əsas dizayn | 1–4-cü həftələr | Maraqlı tərəflərlə başlanğıc görüşü, sistem dizaynı, texnologiya seçimi, büdcə və risk planı |
| Mərhələli tətbiq | 5–20-ci həftələr | Tarif və GPS modulunun hazırlanması, mobil tətbiq, kart inteqrasiyası, pilot sınaq və təlim |
| İstismara verilmə | 21–24-cü həftələr | Tam yerləşdirmə, marşrutların aktivləşdirilməsi, monitorinq, dəstək və ilkin qiymətləndirmə |

> Bu layihə tədris və portfel məqsədilə hazırlanmış konseptual case study-dir. Real qurumun rəsmi layihəsini təmsil etmir.
