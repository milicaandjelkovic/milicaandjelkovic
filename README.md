# CRISP-DM 
## Mетодологија примене машинског учења (CRISP-DM)
### 1.	Анализа и разумевање пословног проблема

CRISP-DM aметодологија је описана као модел хијерархијског процеса, који се састоји од скупова задатака описаних на четири нивоа апстракције (од општег до специфичног): фаза, генерички задатак, специјализовани задатак и инстанца процеса. Сама методологија обухвата шест фаза које су приказане на Графику 1.

(![image](https://user-images.githubusercontent.com/106746983/174995686-557bd622-8f7a-4b6b-a751-7fcea58582ff.png))

Прва фаза обухвата анализу и разумевање проблема. Ова почетна фаза се фокусира на разумевање циљева и захтева пројекта из пословне перспективе, затим претварање овог знања у дефиницију проблема рударења података и прелиминарни план дизајниран за постизање циљева.
Први циљ аналитичара података је да темељно разуме, из пословне перспективе, шта клијент заиста жели да постигне. Клијент често има много супротстављених циљева и ограничења која морају бити правилно избалансирана. Циљ аналитичара је да на почетку открије важне факторе који могу утицати на иход пројекта. Могућа последица занемаривања овог корака је улагање великог труда у стварање тачних одговора на погрешна питања.

### 2.	Aнализа података

Друга фаза – Разумевање података почиње почетним прикупљањем података и наставља се активностима које омогућавају аналитичару да се упозна са подацима, идентификује проблеме са квалитетом података, стекне прве увиде у податке и/или открије занимљиве подскупове за формирање хипотеза у вези са скривеним информацијама.
У овом кораку анализирамо изворе података за пројекат, при чему постоје три основна извора података: интерни подаци, отворени подаци и подаци треће стране. Међутим, без обзира на то одакле подаци потичу, за све податке важи исто правило – смеће унутра, смеће ван (GIGO – Garbage In, Garbage Out). Да бисмо проценили податке треба да одговоримо на неколико питања: 

- Да ли су подаци комплетни? Шта би могло недостајати?
- Одакле потичу подаци?
- Која су била места прикупљања?
- Ко је прикупљао и обрађивао податке?
- Какве су биле измене у подацима?
- Који су проблеми са квалитетом?
Уколико радимо са структурираним подацима, онда је ова фаза лакша. Међутим, када су у питању неструктурирани и полуструктурирани подаци, они морају прво да буду означени што може бити дуготрајан и напоран процес.
Постоје четири кључна задатка у овом кораку:
1.	Прикупљање података: у оквиру овог задатка неопходно је прикупити податке или бар потврдити да им имамо приступ, тестирати поступак приступа подацима и верификовати податке који тамо постоје. Уколико се испостави да неки од података за које смо првенствено проценили да су нам неопходни, а они нису доступни, можемо их заменити неким алтернативним извором података, изменити циљеве пројекта или прикупити нове податке. Такође је неопходно учитати податке у апликацију којом ће бити обрађени како би се утврдило да ли су компатибилни (можда су подаци превише обимни и сложени за инфраструктуру са којом располажемо или не могу бити учитани због специфичног формата).
2.	Опис података: у оквиру овог задатка потребно је описати извор и формате података, број случајева, број и описе поља и било које друге опште информације које могу бити важне. Такође треба извршити кратку процену погодности података за циљеве пројекта. 
3.	Истраживање података: у овом задатку пажљивије испитујемо податке. За сваку променљиву испитујемо опсег вредности и њихову расподелу (при чему користимо основне статистичке технике). Сврха овог истраживања јесте да се детаљније упознамо са подацима и евентуално уочимо неке знаке проблема са квалитетом података и поставимо основу за кораке припреме података.
4.	Провера квалитета података: након што смо податке прикупили и прегледали, време је да се провери да ли су довољно добри да подрже наше циљеве. Често ћемо имати проблем са квалитетом који треба решити. Неки од најгорих проблема са подацима би били: подаци који су нам потребни не постоје; подаци постоје, али не можемо да их добијемо; постоје огромни проблеми са квалитетом података (пуно недостајућиј или нетачних вредности које се не могу исправити).

### 3.	Припрема података

Фаза припреме података обухвата све активности потребне за конструисање коначног скупа података (подаци који ће бити унети у алат(е) за моделирање) из почетних необрађених података. Задаци припреме података ће се вероватно понављати више пута, а не било који прописаним редоследом. Задаци укључују избор атрибута, трансформацију и чишћење података за алате за моделирање.
Радње које су обухваћене задатком чишћења и сређивања података су следеће:
-	Елиминисање дупликата: поставимо тестове за идентификовање и елиминисање дупликата и обришемо сувишне податке.
-	Постојање есктремних вредности: ово су подаци чија вредност знатно одступа од вредности осталих података (било позитивно, било негативно). Постојање екстремних вредности може бити последица погрешног мерења или једноставно неког специфичног и ретког случаја. Иако у већини случајева ово подаци нису битни за анализу, постоје ситуације када се анализирају искључиво екстремне вредности, нпр. код утбрђивања превара са кредитним картицама.
-	Доследност података: уверимо се да имамо јасно дефинисане променљиве (нпр. изрази као што су „приход“ или „купац“ могу имати више значења).
-	Правила за валидацију: док гледамо податке покушавамо да пронађемо инхерентна ограничења. На пример, можемо имати индикатор упозорења за колону „старост“ и ако је у многим случајевима преко 120, тада имамо озбиљан проблем са подацима (немогуће је да многи имају 120 година).
-	Груписање података: одређени подаци можда неће бити потребни, јер да ли је важно да ли неко има 34 или 36 година? Највероватније не, али поређење оних који имају од 30 до 40 година и оних који имају од 41 до 50 година сигурано јесте важно.
-	Спајање података: у неким случајевима колоне података имају врло сличне информације. Можда се у једној налази растојање у метрима а у другој у километрима, па тако можемо користити податке из само једне од те две колоне.
-	Застарелост података: морамо проверити да ли су подаци релевантни и правовремени.
-	One-Hot Encoding: ово је начин да се категорички подаци замене бројевима. На пример: рецимо да имамо базу података са колоном која има три могуће вредности: запослен, незапослен и пензионер. Можемо представити „запослен“ као , „незапослен“ као 2 и „пензионер“ као 3. Иако ово на први поглед делује логично проблем је што алгоритам мисли да је „пензионер“ важнији од „запосленог“. Али применом One-Hot Encoding – а могуће је избећи овај проблем. Потребно је креирати три нове колоне „јесте_запослен“, „јесте_незапослен“ и “јесте_пензионер“. За сваки ред података ставићемо 1 тамо где је тачна одређена категорија, а 0 за све остало.
-	Табеле конверзије: ово можемо користити приликом превођења података из једног стандарда у други. То је нпр. случај ако имамо подакте у једном метричком систему (милиметри, метри) и желимо да их пребацимо у други метрички систем (инчи, стопе).
-	Изведени атрибути: можда ћемо морати да креирамо нека нова поља – атрибуте (на пример, користећи датум испоруке и датум када је купац издао налог да би израчунали колико је купац дуго чекао да прими поруџбину).
-	Спајање података из више различитих извора: на пример из интерне базе података са купцима и базе података курирске службе о испорукама.
-	Форматирање података: подаци нам често долазе у форматима који нису погодни за моделирање, па је у овом кораку потребно довести све податке у одговарајући формат.

### 4.	Избор модела

У овој фази се бирају и премењују различите технике моделирања, а њихови параметри се калибришу на оптималне вредности. Обично постоји неколико техника за исти тип проблема. Неке технике имају посебне захтеве у погледу облика података. Конкретно, многе технике моделирања захтевају испуњавање специфичних претпоставки о подацима – на пример, да сви атрибути имају униформну дистрибуцију, није дозвољено постојање недостајућих вредности, класни атрибут мора бити симболичан, итд.

### 5.	Евалуација модела

У овој фази пројекта, изградили смо модел (или моделе) који на први поглед има висок квалитет из перспективе анализе података. Пре него што пређемо на коначну имплементацију модела, важно је да га темељно проценимо и прегледамо кораке који су предузети да бисмо били сигурни да модел правилно постиже пословне циљеве. Кључни циљ је да се утврди да ли постоји неко важно пословно питање које није довољно размотрено. На крају ове фазе треба донети одлуку о коришћењу резултата.

### 6.	Имплементација модела

Креирање модела генерално није крај пројекта. Чак и ако је сврха модела да повећа знање о подацима, стечено знање ће морати да буде организовано и представљено на начин да га корисник може користити. Често укључује примену „живих“ модела у оквиру процеса доношења одлука у организацији – на пример, персонализацију веб страница у реалном времену или поновљено бодовање маркентишких база података. У зависности од захтева, газа примене може бити једноставна као генерисање извештаја или сложена као имплементација поновљивог процеса рударења података у целом предузећу. У многим случајевим, корисник, а не аналитичар података, спроводи кораке примене. Међутим, чак и ако ће аналитичар спровести напоре за имплементацију, важно је да корисник унапред разуме које радње треба да спроведе да би стварно користио креиране моделе.
![image](https://user-images.githubusercontent.com/106746983/174996487-4a196ed0-cfd6-4bde-b415-d08cf48fcea8.png)

### Разумевање пословног проблема
**Да ли ће клијент напустити банку?**
1)	Ког је пола клијент (ако је у питању физичко лице)?
2)	Колико година има клијент-ако је физичко лице, односно колико дуго послује-ако је правно лице?
3)	Који је радни статус клијента? (ако је физичко лице)
4)	Колико дуго је клијент банке?
5)	Да ли су повезана лица клијента такође клијенти банке?
6)	Да ли привредни субјекат код којег је клијент запослен има рачун у банци клијента (ако је клијент физичко лице)?
7)	Да ли клијент има депозитни рачун код банке?
8)	Да ли је клијент узимао кредит од банке?
9)	Да ли клијент има кредитну картицу банке?
10)	Висина накнаде одржавања рачуна.
11)	Доступност банке (мисли се на мрежу филијала у граду у ком клијент живи).
12)	Висина каматне стопе на зајмове.
13)	Да ли је клијент био одбијен приликом тражења кредита?
14)	Да ли је рачун клијента био блокиран?
15)	Да ли је клијент користио неке нестандардне производе банке (нпр. осигурање)?
16)	Да ли клијент поседује мобилну апликацију банке?
17)	Да ли клијент користи неки од посебних пакета рачуна банке?

**Да ли клијент може да добије кредит?**

*Ако је клијент физичко лице:*
1)	Да ли је клијент у радном односу?
2)	Да ли је у питању стални радни однос?
3)	Колико дуго је у радном односу?
4)	Висина месечне зараде
5)	Да ли клијент поседује кредитну картицу банке код које тражи кредит?
6)	Да ли клијент има закључен уговор о кредиту са банком од које тражи кредит?
7)	Да ли клијент има закључен уговор о кредиту са неком другом банком која није предметна банка?
8)	Која је намена употребе кредитних средстава?
9)	Да ли клијент поседује неко средство обезбеђења?
10)	Ако поседује средство обезбеђења, која је његова вредност?
11)	Оцена кредитне способности клијента.

*Ако је клијент правно лице:*
1)	Да ли је привредни субјекат регистрован за обављање легалне привредне делатности у регистру Агенције за привредне регистре Републике Србије?
2)	Колико дуго привредни субјекат послује на територији Републике Србије?
3)	Да ли је привредни субјекат претходну пословну годину завршио са позитивним нето резултатаом?
4)	Да ли је привредни субјекат последњих 5 година имао позитиван нето резултат?
5)	Да ли је привредни субјекат клијент банке од које тражи кредит?
6)	Да ли привредни субјекат има кредитну обавезу према банци зајмодавцу?
7)	Да ли привредни субјекат има више од једне кредитне обавезе према банци зајмодавцу?
8)	Да ли привредни субјекат има кредитну обавезу према банци која није предметна банка зајмодавац?
9)	Да ли је рачун привредног субјекта у блокади?
10)	Колики је ниво финансијског левериџа?
11)	Намена кредитних средствава.
12)	Висина кредитних средстава.
13)	Оцена кредитне способности клијента.

**Да ли ће клијент променити телефонског оператера?**
1)	Колико година има клијент?
2)	Колико дуго је корисник предметног оператера?
3)	Да ли је postpaid или prepaid корисник?
4)	Да ли користи неки од пакета оператера?
5)	Да ли је клијенту битнији брз и квалитетан проток интернета или количина бесплатних минута и порука?
6)	Каква је покривеност мреже у месту где клијент живи?
7)	Да ли клијент користи мобилне услуге другог оператера а од посматраног проваједера користи интернет пакете?
8)	Да ли су чланови домаћинства клијента такође корисници услуга истог телефонског оператера? Ако јесу да ли су им бројеви телефона умрежени?
9)	Да ли клијент редовно извршава обавезе према свом оператеру?
10)	Да ли оператер има мобилну апликацију?
11)	Да ли оператер обезбеђује наградне игре за postpaid кориснике (греб-греб игрица са наградама у виду бесплатног интернета за наредних 5 дана, одређени износ кредита за нарених 7 дана, итд.)?
12)	Да ли је корисник услуга телефонског оператера куповао мобилни телефон код мобилног оператера?



