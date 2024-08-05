# TTT4203

### 
1. [*GRUNNLEGGENDE ELEKTRONIKK*](#del1)
2. [*KRETSTEORI*](#del2)
3. [*ENGERGI OG EFFEKT*](#del3)
4. [*DIODER*](#del4)
5. [*KRETSDIAGRAM*](#del5)
6. [*SYSTEMPERSPEKTIV*](#del6)
7. [*ANALOGT OG DIGITALT*](#del7)
8. [*TRANSISTORER*](#del8)
9. [*LOGISKE BYGGEKLOSSER*](#del9)
10. [*RESISTIVE KRETSAR*](#del10)
11. [*SUPERPOSISJONSPRINSIPPET*](#del11)
12. [*THÉVENINS TEOREM*](#del12)
13. [*ENERGIKILDER*](#del13)
14. [*MINNE OG REGISTER*](#del14)
15. [*REAKTIVE ELEMENT*](#del15)

<a name="del1"></a>
## GRUNNNLEGGENDE ELEKTRONIKK

### Oppklaring av begreper

**Ladning** er en grunnleggende egenskap ved partikler som protoner og elektroner. Elektrisk ladning kan være positiv eller negativ, og like ladninger frastøter hverandre mens ulike ladninger tiltrekker hverandre. Mengden ladning måles i enheter kalt coulomb (C). Ladning er som biler på en vei. Akkurat som biler kan bevege seg fra ett sted til et annet, kan ladninger bevege seg gjennom en leder. 

**Strøm** er bevegelsen av elektrisk ladning gjennom en leder, som vanligvis er en ledning. Strøm måles i ampere (A) og beskriver mengden ladning som passerer gjennom et punkt i kretsen per tidsenhet. Strøm er som bilens fart, det vil si hvor raskt ladningene (bilene) beveger seg gjennom kretsen (veien). Jo større strømmen er, desto flere "biler" passerer et gitt punkt per tidsenhet. 

**Spenning** er energien per ladningsenhet som driver strømmen gjennom en krets, det kan sammenlignes med hvor mye du trykker på gasspedalen. Spenning måles i volt (V) og kan sees på som "trykket" som skyver ladningene (bilene) gjennom kretsen. Jo mer du trykker på gasspedalen, desto mer energi gir du til bilen, og jo raskere kan den kjøre. 

**Motstand** er en egenskap i materialer som begrenser strømmen av elektrisk ladning. Den måles i ohm ($\Omega$). Høy motstand tilsvarer en humpete vei, trafikkork eller sterk motvind som bremser bilene, mens lav motstand tilsvarer en jevn, klar vei med lite vind hvor bilene kan kjøre raskt.

Elektroniske kretser trenger energikilder for å fungere, og disse kan være enten spenningskilder eller strømkilder. 

En **spenningskilde**, som et batteri, gir konstant spenning til kretsen. Den "skyver" ladning gjennom kretsen, og ladningen kommer ut med høyere energi enn den hadde da den gikk inn. Dette er som om du trykker gaasspedalen i bilen til en bestemt posisjon og holder den der. Bilen får konstant energi fra gasspedalen uavhengig av hastigheten. Hastigheten vil avhenge av veiforholdene. Hvis du kjører opp en motbakke, vil bilen gå saktere fordi den konstante posisjonen ikke gir nok kraft til å opprettholde samme hastighet.

En **strømkilde** leverer konstant strøm til kretsen, uavhengig av spenningen. Den "presser" ladningen med en konstant hastighet, og sammmenlignes med en cruise control som setter bilens hastighet til en bestemt verdi, og justerer gasspedalen for å oppprettholde denne hastigheten. Strømkilden sørger for at strømmen er konstant, uansett hvilken motstand som oppstår i kretsen.

I en **seriekobling** kobler man sammen elektriske komponenter etter hverandre slik at strømmen går gjennom alle komponentene uten å dele seg i forskjellige grener. 

I en **parallellkobling** kan man koble på andre elementer slik at de blir en «egen» krets, og strømmen får flere veier å gå. 

### Måling av strøm og spenning

- Måling av strøm skjer med et ampermeter. Strøm i en krets går alltid gjennom en eller annen gren. For å måle strømmen gjennom en gren, kobler vi ampermeteret i serie med grenen. Ampermeteret er ikke eit symmetrisk kretselement, og vi må koble det opp deretter. Dersom strømmen går fra pluss til minus på ampermeteret, viser det et positivt tall. Dersom strømmen går andre veien, blir verdien vist som et negativt tall. 
- Måling av spenning skjer med et voltmeter. For å måle spenningen over en gren, kobler vi voltmeteret i parallell med den aktuelle greina. Dersom pluss-enden er kobla til den enden av greina der ladninga har størst energi, viser spenninga eit positivt tall. I motsatt tilfelle, vises et negativt tall. Når vi måler spenningen, måler vi altså energiforskjellen over komponenten.

<a name="del2"></a>
## KRETSTEORI

### Kirchhoffs strømlov

Kirchhoffs strømlov (KCL) er basert på prinsippet om ladningsbevaring: ladning kan verken oppstå eller forsvinne. Dette prinsippet innebærer at den totale mengden ladning som går inn i et kretselement må være lik den totale mengden ladning som går ut. Tenk på dette som en tunnel: antall biler (ladninger) som går inn i tunnelen, må være det samme som antall biler som kommer ut.

Når vi bruker KCL på en seriekobling, ser vi at strømmen gjennom alle elementene i serien må være den samme. Dette er fordi det ikke finnes noen steder i en seriekobling hvor ladning kan samles opp eller forsvinne. 

KCL blir mer kompleks når vi har flere noder, men prinsippet er det samme. For en node i en krets er Kirchhoffs strømlov formulert som: *Den algebraiske summen av strømmer inn til en node vil alltid være lik den algebraiske summen av strømmer ut fra noden.* Dette betyr at summen av alle strømmer som går inn i en node minus summen av alle strømmer som går ut fra noden, skal være null.

Med andre ord, hvis vi vet retningen på strømmene i en node, kan vi bruke denne informasjonen til å beregne strømmer i kretsen ved å sette opp og løse ligninger basert på KCL.


### Kirchhoffs strømlov

Kirchhoffs spenningslov (KVL) er basert på prinsippet om energibevaring i en elektrisk krets. Denne loven sier at den totale spenningen rundt en lukket sløyfe i en krets alltid vil være null. Dette kan sammenlignes med et energibudsjett: summen av energien som tilføres og energien som brukes opp i en sløyfe må være balansert.

For å forstå KVL, tenk deg at du går rundt i en sløyfe som representerer en elektrisk krets. Når du beveger deg gjennom en komponent som en motstand eller et batteri, endres spenningen. En motstand, for eksempel, fører til et spenningsfall (energi som blir brukt opp), mens et batteri gir et spenningsløft (energi som tilføres).

KVL sier at hvis du legger sammen alle spenningene du opplever når du går rundt hele sløyfen og inkludere både spenningsfall og spenningsløft, vil den totale summen alltid være null. Med andre ord, *den algebraiske summen av spenninger i en lukket sløyfe i en krets er null*. Dette kan skrives som $\sum_{i=1}^{n}$ $V_i = 0$ hvor $V_{i}$ er spenningen over hver komponent i sløyfen.

Denne loven gjør det mulig å analysere elektriske kretser ved å sette opp og løse ligninger som beskriver hvordan spenningene fordeler seg i en krets. Ved å bruke KVL kan man beregne ukjente spenninger og strømmer i en krets, basert på kjente verdier og kretsens konfigurasjon.


### Ideelle kretselement
Elektronikk handler om å sette sammen fysiske komponenter til funksjonelle systemer, mens kretsteori gir matematiske modeller for hvordan strøm og spenninger oppfører seg i disse kretsene. Kretsteori er et verktøy for å modellere, forstå, analysere, dimensjonere og diskutere både eksisterende og hypotetiske elektroniske systemer.

En **ideell motstand** er et kretselement som oppfyller Ohms lov. Det vil si at elementloven, som uttrykker relasjonen mellom spenning *v* over og strøm *i* gjennom elementet er gitt ved $v = Ri$, der konstanten *R* er *resistansen* eller *motstandsverdien* til motstanden. Grafen er en rett linje med stigningstall 1/R. 

En **ideell spenningskilde** har en spenning over seg som er uavhengig av strømmen som går gjennom. 

En **ideell strømkilde** er et kretselement som har en strøm *i* gjennom seg som er uavhengig av spenningen *v* over elementet. 


### Potensial

**Potensiale** i et punkt er energinivået per ladningsenhet på et bestemt punkt i en krets. Det er ofte referert til som spenningen i et punkt relativt til et referansepunkt. Dette referansepunktet er vanligvis kalt jord (engelsk: "ground"), og potensialet der er definert som 0V.

**Spenningen** over en komponent er forskjellen i potensiale mellom to punkter, typisk før og etter ladningen har passert komponenten. Denne forskjellen i potensiale gir et mål på hvor mye energi per ladningsenhet som har blitt overført til eller fra ladningen når den beveger seg gjennom komponenten.


<a name="del3"></a>
## ENERGI OG EFFEKT

### Grunnleggende størrelser
Hvordan kan vi vite om en ladning leverer eller tar i mot energi? Dersom ladningen går ut fra + på kretselementet og inn igjen på -, leverer den energi. Dersom tilfellet er motsatt, tar den i mot energi. Derfor er det viktig å ha kontroll på + og - når vi kobler kretser.

Generelt har vi at energimengden levert til et kretselement når det går strømmen *I* gjennom og spenninga *V* over kretselementet i tiden *T* er gitt ved $E = IVT$.

Som regel er vi ikke interesserte i totalenergi. Den totale energien er alltid avhengig av tiden, og den kan være vanskelig å holde styr på. Derfor er det mye lettere for oss å se på energi levert/mottatt per tidsenhet. Dette kaller vi effekt og er gitt ved $P = E/T = IV$. Ved hjelp av Ohms lov kan dette omskrives til $P = IV = \frac{V^{2}}{R} = RI^{2}$.


<a name="del4"></a>
## DIODER

En **diode** er en halvlederkomponent som bare leder strøm i én retning. Leder strøm når anoden er positiv i forhold til katoden (fremoverbias), sperrer strøm når anoden er negativ (reversbias).

En **ideell diode** leder strøm uten spenningsfall i fremoverbias, sperrer helt i reversbias.
En **reell diode** har et typisk spenningsfall på 0.7V for silisiumdioder i fremoverbias, og en liten lekkasjestrøm i reversbias.

<a name="del5"></a>
## KRETSDIAGRAM

Kretsdiagrammer brukes til å representere elektriske kretser på en forståelig og systematisk måte. Dette hjelper med å kommunisere hvordan komponentene er koblet sammen og hvordan kretsen fungerer. Kretsens topologi refererer til hvordan komponentene er koblet sammen. Dette er avgjørende for å forstå kretsens funksjon. Det viser forbindelsene mellom komponentene, men ikke nødvendigvis den fysiske plasseringen av komponentene. Diagrammene følger visse standardkonvensjoner for å sikre klarhet og konsistens. Dette inkluderer symboler for ulike komponenter som motstander, kondensatorer, dioder, og transistorer. Brytere og vendere er viktige komponenter i mange kretser. De kontrollerer strømflyten ved å åpne eller lukke en krets.



<a name="del6"></a>
## SYSTEMPERSPEKTIV

For å representere komplekse modeller bruker vi blokkdiagram. Det er grafiske representasjoner som viser hvordan forskjellige deler av et system er koblet sammen og samhandler. Et eksempel er et høyttaleranlegg for konsertbruk, som består av en mikrofon, en forsterker, og en høyttaler. Mikrofonen kan betraktes som en spenningskilde som leverer energi til forsterkeren. Spenningen fra mikrofonen er tidsvarierende fordi den representerer lyd fra sangeren. Dette signalet forsterkes og sendes til høyttaleren som omdanner det til lyd.

Forsyningsspenningen til et elektronisk system er vanligvis en likespenning, noe som gjør systemet mer forutsigbart.
Forskjellige typer spenninger i elektroniske systemer inkluderer:
- Likespenning: En konstant spenning som ikke varierer over tid.
- Periodiske spenninger: Spenninger som gjentar seg etter en viss tidsperiode TT.
- Transiente spenninger: Spenninger som varer i en begrenset tidsperiode.
- Informasjonsbærende signaler: Signaler som hele tiden endrer seg og ikke kan forutsies nøyaktig.

Vekselspenning (AC) varierer over tid, i motsetning til likespenning (DC) som er konstant. Et eksempel på vekselspenning er sinusformet spenning, som er viktig i signalteori og brukes i stikkontakter (230V, 50Hz i Norge).


<a name="del7"></a>
## ANALOGT OG DIGITALT

Teknologien i informasjonssamfunnet baserer seg på at noe kan representeres som noe annet, ofte ved hjelp av elektronikk. Elektriske signaler brukes til å representere informasjon, hvor **analoge** signaler varierer kontinuerlig og kan ha uendelig mange verdier, mens **digitale** signaler er diskrete og representerer spesifikke tilstander, som "på" eller "av".

Digitale systemer bruker binære signaler (0 og 1) for å formidle informasjon. De er mindre følsomme for støy og forstyrrelser enn analoge systemer, siden de kun trenger å skille mellom et begrenset antall tilstander. Dette gjør digitale signaler mer robuste og enklere å behandle og lagre.

I digitale kretser representerer høy spenning (for eksempel 5V) en "1", mens lav spenning (0V) representerer en "0". Denne binære representasjonen forenkler implementeringen av logiske operasjoner og databehandling.


<a name="del8"></a>
## TRANSISTORER

<a name="del9"></a>
## LOGISKE BYGGEKLOSSER

<a name="del10"></a>
## RESISTIVE KRETSER

<a name="del11"></a>
## SUPERPOSISJONSPRINSIPPET

<a name="del12"></a>
## THÉVENINS TEOREM

<a name="del13"></a>
## ENERGIKILDER

<a name="del14"></a>
## MINNE OG REGISTER

<a name="del15"></a>
## REAKTIVE ELEMENT



