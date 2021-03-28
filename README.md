# Vanliga Frågor


Mer **grundläggande tangentbordsinformation** finns på: <https://keyboard.university/> och <https://keyboardfinder.com/>

Som inledning vill jag bara säga att det mesta inom denna hobby är personlig preferens. Många av dessa frågor kan besvaras med: "prova det du är intresserad av och dra dina egna slutsatser". Med det sagt så finns det några mer specifika frågor som vi får ofta.

## Var köper man saker?

Det finns ett gäng butiker inom EU som specialiserar sig inom olika typer av försäljning.

### [MyKeyboard.eu](https://mykeyboard.eu)
 Belgien. Tangentbord/keycaps/kringutrustning. Säljer både in-stock och GB.

### [Candy Keys](https://candykeys.com)
 Tyskland. Tangentbord/keycaps/kringutrustning. Säljer både in-stock och GB.

### [KeyGem](https://keygem.store)
Tangentbord/keycaps/kringutrustning. Har större utbud in-stock.

### [MaxGaming](https://maxgaming.se)
Sverige. Lite smalare utbud, och mer åt retail-hållet, har bra Nordic-utbud. Säljer in-stock. Finns i discorden!

### [Oblotzky Industries](https://oblotzky.industries)
Säljer enbart GB, finns "pre-order" vilket är förhandsbokning av extras i GB.

### [SplitKB](https://splitkb.com)
Fokuserar på split-tangentbord och tillbehör.

### [](https://loob.no)
Norge. Stort utbud av smörj, utanför EU men tar betalt för moms så att beställningar går igenom tullen smärtfritt.

### [KBDFans](https://kbdfans.com)
Asien. Många instegsmodeller och bra utbud av delar. Kan ofta bli dyrt pga import och moms.

Utöver detta finns naturligtvis fler försäljare, många finns på servern med "Vendor"-tagg alternativt går de att hitta på: <https://keebmap.xyz/>. *(cred till @Snakeyh#3250)*

Det är också vanligt att köp görs på andrahandsmarknaden. Antingen i #köp och #sälj på <https://mekaniskatangentbord.se> eller på <https://mechmarket.reddit.com>.

## Vad är ett group buy/GB?

Ett GB är lite som en kickstarter. Någon designar något, de som är intresserade betalar i förväg, när köptiden är slut skickas beställning och saken produceras.
Detta leder naturligt till väldigt lång väntetid, då efterfrågan för GB-produkter har blivit så hög att det i många fall är kö till produktionen. 6 månaders väntetid är i de flesta fallen det absolut minsta man ska räkna med och det tar oftast längre tid.
Gruppköp sker på egen risk och de flesta har någon skräckhistoria där processen har tagit betydligt längre tid än väntat. Men å andra sidan producerar GB's de mest eftertraktade sakerna i hobbyn. Risken blir dessutom betydligt lägre när inköp görs via en vendor, vilket den stora majoriteten av GB's gör nu för tiden.

GB's kan vara lite svåra att hålla koll på, men till det finns ett flertal trackers som kan vara till hjälp:
<https://mechgroupbuys.com/>
<https://keycaplendar.firebaseapp.com/>

## Hur fungerar åäö på ANSI?

Ett tangentbord programmeras med keycodes som är språkneutrala och en tangents keycode översätts av operativsystemets inställda tangentbordsspråk till rätt symbol. Alltså behöver inget programmeras specifikt för att få "åäö" att fungera som det brukar.
Däremot har ISO ett par tangenter som är specifika. **<>** bredvid vänster shift samt att **' *** till vänster om ISO-enter istället hamnar ovanför ANSI-enter. Dessa måste programmeras någon annanstans om man vill köra ANSI, oftast på ett lager eller genom att använda split backspace om ditt PCB har stöd för det.

## Vilken xxx är bäst?

Svaret på denna fråga blir tråkigt nog: "Det finns inget bäst, allt är personlig preferens." varje gång den ställs. Om du är intresserad av något, så prova. Inget någon säger här kommer kunna översättas i hur du upplever något.
Med det sagt så kan det då och då vara värt att få input från andra, men då är det kanske bättre att ställa frågan "Vilken xxx tycker ni om?". Det är självklart fritt fram att fråga efter andras åsikter om du sitter fast med två alternativ, men generella frågor som: “Vilken taktil är bäst?” undanbedes.

## Hur rengör jag mina xxx?

Ljummet vatten och diskmedel för allt i plast, isopropanol till metall.
PBT keycaps klarar av diskmaskin på låg temperatur, annars är det för hand eller med ultraljudstvätt som gäller.
Deskmats/musmattor med sydda kanter klarar av tvättmaskin på låga temperaturer.

## Hur programmerar jag mitt tangentbord?

Först och främst behöver du veta om ditt tangentbord stödjer QMK. Detta gör du kanske enklast på produktsidan där du köpte ditt tangentbord eller din pcb. 

Om din pcb stödjer QMK är det bara att tuta och köra. För det absolut enklaste sättet att få till QMK är att surfa in på <https://config.qmk.fm>

1. Sök upp ditt tangenbord i dropplistan
2. Välj en layout så att bilden matchar den faktiska layout du har på ditt tangentbord
3. Sätt KEYMAP NAME till något coolt t.ex. *Cheezis_coolaste_keymap_finalversion_final_fix_latest_final_beta*
4. Klicka på en knapp och välj sedan i menyn längst ner vad du vill att den ska göra. T.ex. markera där du vill ha *1* och klicka sedan på *1* i menyn.
5. När du känner dig nöjd och tycker att allt ser bra ut tryck på COMPILE i övre högra hörnet.
6. Titta på en snurrande potatis tills den bakat klart.
7. Tryck på FIRMWARE rakt nedanför COMPILE.
8. Om du inte har QMK toolbox installerat är det nu dags att skaffa det, så klicka på den blå *get qmk toolbox* precis under FIRMWARE knappen.
9. Installera QMK Toolbox och öppna det.
10. Klicka på *open* och leta reda på den fil som laddades ner när du klickade på FIRMWARE.
11. Anslut ditt tangentbord till datorn.
12. Kontrollera hur du sätter ditt tangentbord i resetläge/dfu-läge, vanligtvis finns det en *reset-knapp* på baksidan av pcbn, det kan också funka att samtidigt som du kopplar in usb-kabeln att hålla nere *mellanslag* och *B* eller hålla ner *escape*. Om du lyckas ska det dyka upp gul text som säger *connected* i QMK toolbox.
13. Klicka på *flash* och allting borde fungera som det ska.

*Cred till @Cheezï#8998 för denna guide.*

## Jag vågar/kan/vill inte löda, var får jag tag på hotswap?

Hotswap är ett smidigt val som första bräda om man inte riktigt vet vilken sorts brytare man vill använda, däremot kommer det med några nackdelar.
Dessa “nackdelar” är bl.a. att ISO-utbudet är väldigt lågt, att inte alla layoutstorlekar har bra utbud samt att både ljud och brytarstabilitet kan bli något sämre än med fastlödda brytare.
Hotswap brukar finnas på samma ställen som Tofu-kits säljs, hos keygem, kbdfans osv.
 
Att löda tangentbord är mycket enklare än man kan tro, och i 99% av fallen klarar sig de flesta med en billig lödstation från Kjell. Ett annat, lite dyrare alternativ är TS100 eller TS80P. Det finns gott om guides på tangentbordslödning på Youtube och hjälp går alltid att få i #do-it-yoursjälv.

## "WTB (asdyr bräda), helst under 1k"

Nej. Även om vi alla skulle uppskatta lägre priser så är detta en relativt dyr hobby. T.o.m. instegs-kit som NK65 Entry och KBD67mkII brukar ligga över 1000kr. Det går absolut att få tag på kits under 1000kr, men det kommer ofta med nackdelar som tråkig mounting eller billigare material.

## Hur får jag tag på ISO Nordic?

Lite svår fråga att svara på då det finns flera lösningar i olika prisklasser. Detta svar är också enbart för cherry-profil.

Billigt - ett keyset från maxgaming/aliexpress, täcker ISO Nordic men kompatibilitet kanske inte finns där för mer udda layouts.
Medium - valfritt ePBT-set med tillhörande international-kit, har större baskit och kommer enbart i PBT.
Dyrt - ett GMK-set köpt i group buy eller på andrahandsmarknaden, kräver tillhörande NorDe-kit. Kommer enbart i doubleshot ABS.

ePBT och GMK brukar (trots priset) vara en vettig investering då de håller hög kvalitet och kan säljas för nära inköpspris på andrahandsmarknaden.

## Vilket material ska jag ha på xxx?

Detta är högst subjektivt, och har därför inget definitivt svar.
För plates kan man säga att mässing och kolfiber är åt det styvare hållet och ger ett "pingigare" ljud, medan plast (POM, PC) är mjukare och ger ett dovare ljud.
För brytare så är det definitivt skillnad på material, men det maskeras ofta så fort man använder smörj. Här är det enklast att prova sig fram.
Tangentbordsmaterial är omöjligt att ge ett svar på då brädans design spelar in minst lika mycket som dess material. I slutändan handlar detta om preferens ändå.

## Vilket smörj ska jag använda?

Generellt så kan man säga att olja används till fjädrar och fett används till brytare/stabs. Däremot finns det inget som hindrar dig från att experimentera.
Den mest populära smörjserien är tillverkad av Krytox där produktnamnen ser ut så här:
*GPL 205g0*
Ju högre tal namnet består av desto tjockare är smörjet. Den första siffran anger typ av smörj, *1* är olja och *2* är fett.*g0* indikerar smörjets konsistens som en grad, där "grad 0" är relativt mjuk och lättapplicerad.
Utöver Krytox så finns Tribosys (som i stort sett är en direkt kopia, namnen ser ut så här: *3204* och följer samma princip som för Krytox där högre tal = tjockare), Glorious Lube och Super Lube vilket är lite mindre premium men funkar utmärkt till stabs.

## Hur designar jag min egen PCB?

Kolla in [guiden för PCB-desig](PCB-design.md)
