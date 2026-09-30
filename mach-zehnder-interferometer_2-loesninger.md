<!-- Løsninger til mach-zehnder-interferometer_2-opgaver.md.
     Til læreren. Bygges ikke ind i simuleringen og lægges ikke på GitHub.
     Formler er skrevet til VS Codes markdown-visning, derfor 1{,}52 og ikke 1,52. -->

# Mach-Zehnder-interferometer — løsninger

## Indledning

Løsningerne bruger samme regler som simuleringen:

$$\mathrm{BS}\,|0\rangle = \tfrac{1}{\sqrt{2}}\big(|0\rangle + |1\rangle\big), \qquad \mathrm{BS}\,|1\rangle = \tfrac{1}{\sqrt{2}}\big(|0\rangle - |1\rangle\big)$$

Faseskifteren sidder i arm 1 og ganger amplituden for arm 1 med $e^{i\phi}$. Uden hvilken-vej-markering giver det

$$P_0 = \cos^2\!\left(\tfrac{\phi}{2}\right), \qquad P_1 = \sin^2\!\left(\tfrac{\phi}{2}\right)$$

Med hvilken-vej-markering er $P_0 = P_1 = \tfrac12$ uanset $\phi$.

| $\phi$ | $P_0$ | $P_1$ |
|:--|:--|:--|
| 0° | 1 | 0 |
| 45° ($\pi/4$) | 0,854 | 0,146 |
| 90° ($\pi/2$) | 0,500 | 0,500 |
| 180° ($\pi$) | 0 | 1 |
| 270° ($3\pi/2$) | 0,500 | 0,500 |

**Afvigelser fra simuleringen:** Ingen. Opgave 5 bruger egne tal ($\lambda_0 = 532\ \mathrm{nm}$, $n = 1{,}52$), som ikke indgår i simuleringen.

**Tilfældige udfald:** Simuleringen trækker hver fotons detektor tilfældigt med sandsynlighederne ovenfor. Den målte andel spreder sig derfor om teorien med standardafvigelsen $\sigma = \sqrt{P(1-P)/N}$:

| $N$ | $P = 0{,}5$ | $P = 0{,}854$ |
|:--|:--|:--|
| 30 | $\pm 9$ procentpoint | $\pm 6$ procentpoint |
| 50 | $\pm 7$ procentpoint | $\pm 5$ procentpoint |
| 100 | $\pm 5$ procentpoint | $\pm 4$ procentpoint |

Ved $P = 0$ og $P = 1$ er der ingen spredning: alle klik havner i samme detektor.

---

## 1. Første observation

**a)** Alle klik havner i detektor 0. Med 30 fotoner bliver fordelingen præcis 30/0, fordi $P_0 = 1$.

**b)** Svaret er personligt. De fleste forventer 50/50, fordi fotonen "deles" ved den første beamsplitter.

**c)** Hvis fotonen valgte én bestemt vej ved BS1, ville den ankomme alene til BS2. Så er der intet at interferere med, og BS2 deler 50/50. Man ville altså forvente halvdelen af klikkene i hver detektor.

> **Til læreren:** Det er netop kontrasten mellem c) og det, eleverne ser, der er pointen. Resultatet kan kun forklares, hvis begge veje har bidraget.

## 2. Interferensen regnet i hånden

**a)** Efter BS1:

$$\mathrm{BS}\,|0\rangle = \tfrac{1}{\sqrt{2}}\big(|0\rangle + |1\rangle\big)$$

**b)** Ved BS2 bruges reglerne på hvert led:

- Fra arm 0: $\tfrac{1}{\sqrt2}\,\mathrm{BS}\,|0\rangle = \tfrac12|0\rangle + \tfrac12|1\rangle$
- Fra arm 1: $\tfrac{1}{\sqrt2}\,\mathrm{BS}\,|1\rangle = \tfrac12|0\rangle - \tfrac12|1\rangle$

| | Mod D0 | Mod D1 |
|:--|:--|:--|
| Fra arm 0 | $a_1 = \tfrac12$ | $b_1 = \tfrac12$ |
| Fra arm 1 | $a_2 = \tfrac12$ | $b_2 = -\tfrac12$ |

**c)**

$$P_0 = (a_1 + a_2)^2 = \left(\tfrac12 + \tfrac12\right)^2 = 1, \qquad P_1 = (b_1 + b_2)^2 = \left(\tfrac12 - \tfrac12\right)^2 = 0$$

Interferensen er konstruktiv mod D0 og destruktiv mod D1.

**d)** Ja. Alle fotoner ender i D0, som i opgave 1.

## 3. Forskellige faser

| $\phi$ | Forventet andel D0 | Forventet andel D1 | Teori $P_0$ |
|:--|:--|:--|:--|
| 0° | 100 % | 0 % | 1 |
| 90° ($\pi/2$) | ca. 50 % | ca. 50 % | 0,5 |
| 180° ($\pi$) | 0 % | 100 % | 0 |
| 270° ($3\pi/2$) | ca. 50 % | ca. 50 % | 0,5 |

Med 50 fotoner ved 90° og 270° er andele mellem ca. 36 % og 64 % helt normale ($\pm 2\sigma$).

**a)** Sandsynligheden flytter sig gradvist fra D0 til D1 og tilbage igen, når fasen øges. Mønstret gentager sig for hver 360°.

**b)** D0 falder fra 100 % ved 0 over ca. 50 % ved $\pi/2$ til 0 % ved $\pi$.

**c)** D1 stiger tilsvarende fra 0 % over ca. 50 % til 100 %. Summen er hele tiden 100 %.

**d)** Målingerne bør passe med modellen inden for den statistiske spredning. $P_0 = P_1$ når $\cos^2(\phi/2) = \tfrac12$, dvs. ved $\phi = 90°$ ($\pi/2$) og $\phi = 270°$ ($3\pi/2$).

## 4. Hvilken-vej og interferens

**a)** Uden markering havner alle klik i D0. Med markering bliver fordelingen ca. 50/50. Med 50 fotoner er andele mellem ca. 36 % og 64 % normale.

**b)** Nej. Med markering er fordelingen 50/50 for alle værdier af $\phi$. Grafen viser en vandret stiplet linje.

**c)** Med tallene fra opgave 2 ($a_1 = a_2 = \tfrac12$):

$$\text{Amplituder lagt sammen: } P_0 = (a_1 + a_2)^2 = 1$$

$$\text{Sandsynligheder lagt sammen: } P_0 = a_1^2 + a_2^2 = \tfrac14 + \tfrac14 = \tfrac12$$

Det første passer med målingen uden markering, det andet med målingen med markering. For D1 får man tilsvarende $(b_1 + b_2)^2 = 0$ og $b_1^2 + b_2^2 = \tfrac12$.

**d)** Uden markering findes der ingen information om vejen. Så lægges amplituderne sammen, og den relative fase afgør, om de forstærker eller ophæver hinanden. Det er interferens. Med markering findes informationen i princippet. Så lægges sandsynlighederne sammen, interferensleddet $2a_1a_2$ forsvinder, og fasen har ingen betydning.

## 5. Udledning af $P_0$ og $P_1$

**a)** Pilen fra arm 0 har koordinaterne $\left(\tfrac12,\ 0\right)$. Pilen fra arm 1 har samme længde, men er drejet vinklen $\phi$:

$$\left(\tfrac12\cos\phi,\ \tfrac12\sin\phi\right)$$

**b)** Summen har koordinaterne $\left(\tfrac12(1 + \cos\phi),\ \tfrac12\sin\phi\right)$. Kvadratet på længden er

$$P_0 = \tfrac14\left((1 + \cos\phi)^2 + \sin^2\phi\right) = \tfrac14\left(1 + 2\cos\phi + \cos^2\phi + \sin^2\phi\right) = \tfrac14\left(2 + 2\cos\phi\right) = \tfrac12(1 + \cos\phi)$$

hvor $\cos^2\phi + \sin^2\phi = 1$ er brugt.

**c)** Formlen $\cos(2v) = 2\cos^2(v) - 1$ bruges med $v = \tfrac{\phi}{2}$:

$$\cos(\phi) = 2\cos^2\!\left(\tfrac{\phi}{2}\right) - 1 \quad\Rightarrow\quad \cos^2\!\left(\tfrac{\phi}{2}\right) = \tfrac12\big(1 + \cos(\phi)\big)$$

Højresiden er netop $P_0$ fra b), så $P_0 = \cos^2\!\left(\tfrac{\phi}{2}\right)$.

**d)** Mod D1 er bidragene $b_1 = \tfrac12$ og $b_2 = -\tfrac12$. Pilen fra arm 0 er stadig $\left(\tfrac12,\ 0\right)$, mens pilen fra arm 1 nu peger modsat:

$$\left(-\tfrac12\cos\phi,\ -\tfrac12\sin\phi\right)$$

Summen er $\left(\tfrac12(1 - \cos\phi),\ -\tfrac12\sin\phi\right)$, og

$$P_1 = \tfrac14\left((1 - \cos\phi)^2 + \sin^2\phi\right) = \tfrac14\left(2 - 2\cos\phi\right) = \tfrac12(1 - \cos\phi)$$

Formlen $\cos(2v) = 1 - 2\sin^2(v)$ med $v = \tfrac{\phi}{2}$ giver $\sin^2\!\left(\tfrac{\phi}{2}\right) = \tfrac12\big(1 - \cos(\phi)\big)$, så $P_1 = \sin^2\!\left(\tfrac{\phi}{2}\right)$.

**e)**

$$P_0 + P_1 = \tfrac12(1 + \cos\phi) + \tfrac12(1 - \cos\phi) = 1$$

Fotonen ender altid i én af de to detektorer. Interferensen flytter sandsynlighed mellem detektorerne, men skaber eller fjerner den ikke. Interferensleddene $+\tfrac12\cos\phi$ og $-\tfrac12\cos\phi$ går ud med hinanden.

**f)** Pilene mod D0:

| $\phi$ | Pilene | Sum | $P_0$ | Interferens |
|:--|:--|:--|:--|:--|
| 0 | samme retning | længde 1 | 1 | fuldt konstruktiv |
| $\pi/2$ | vinkelrette | længde $\tfrac{1}{\sqrt2}$ | $\tfrac12$ | delvis |
| $\pi$ | modsat retning | længde 0 | 0 | fuldt destruktiv |

> **Til læreren:** Pilene er komplekse tal i forklædning: pilen fra arm 1 er $\tfrac12 e^{i\phi}$. Opgaven giver samme udledning uden komplekse tal. Elever, der kender cosinusrelationen, kan også finde summens længde direkte: $\tfrac14 + \tfrac14 + 2\cdot\tfrac14\cos\phi = \tfrac12(1 + \cos\phi)$. Bemærk fortegnet: vinklen mellem pilene er $\phi$, så cosinusrelationen bruges med $+2ab\cos\phi$ (summen af to vektorer), ikke med $-2ab\cos$ som for en trekantsside.

## 6. En glasplade som faseskifter

*Givet:* $\lambda_0 = 532\ \mathrm{nm}$, $n = 1{,}52$, $P_0 = 0{,}75$.

**a)**

$$\cos^2\!\left(\tfrac{\phi}{2}\right) = 0{,}75 \;\Rightarrow\; \cos\!\left(\tfrac{\phi}{2}\right) = 0{,}866 \;\Rightarrow\; \tfrac{\phi}{2} = 30° \;\Rightarrow\; \phi = 60° = \tfrac{\pi}{3}$$

**b)** Formlen løses for $d$:

$$d = \frac{\phi\,\lambda_0}{2\pi\,(n-1)} = \frac{\tfrac{\pi}{3}\cdot 532\ \mathrm{nm}}{2\pi\cdot 0{,}52} \approx 171\ \mathrm{nm}$$

**c)** Med $d = 10\ \mu\mathrm{m}$:

$$\phi = 2\pi\cdot\frac{10\,000\ \mathrm{nm}}{532\ \mathrm{nm}}\cdot 0{,}52 = 2\pi\cdot 9{,}774 \approx 61{,}4\ \mathrm{rad}$$

Resten efter 9 hele omgange er $0{,}774\cdot 2\pi \approx 4{,}87\ \mathrm{rad} \approx 279°$. Det giver

$$P_0 = \cos^2\!\left(\tfrac{279°}{2}\right) = \cos^2(139{,}4°) \approx 0{,}58$$

**d)** Et fasefejl på $0{,}5\ \mathrm{rad}$ svarer til en tykkelsesfejl på

$$\Delta d = \frac{0{,}5\cdot\lambda_0}{2\pi\,(n-1)} = \frac{0{,}5\cdot 532\ \mathrm{nm}}{2\pi\cdot 0{,}52} \approx 81\ \mathrm{nm}$$

For pladen på $10\ \mu\mathrm{m}$ er det under 1 % af tykkelsen. Omkring $\phi \approx 279°$ ændrer $P_0$ sig med ca. $0{,}5$ pr. radian, så $0{,}5\ \mathrm{rad}$ giver en usikkerhed på $P_0$ på ca. $\pm 0{,}25$. Man kan altså næsten ikke forudsige $P_0$ ud fra en målt tykkelse, medmindre tykkelsen kendes på få titals nanometer.

**e)** To grunde:

- Kun $\phi$ modulo $2\pi$ påvirker detektorerne. En ekstra tykkelse på $\lambda_0/(n-1) \approx 1023\ \mathrm{nm}$ giver præcis én omgang mere og samme fordeling.
- $\cos^2$ er en lige funktion, så $\phi$ og $2\pi - \phi$ giver samme fordeling.

For $P_0 = 0{,}75$ passer fx $d \approx 171\ \mathrm{nm}$, $853\ \mathrm{nm}$, $1194\ \mathrm{nm}$, $1876\ \mathrm{nm}$ osv.

> **Til læreren:** Delspørgsmål d) og e) er pointen bag interferometriske sensorer: De er ekstremt følsomme for små ændringer af fasen, men kan ikke alene fortælle, hvor mange hele omgange der er. I praksis måler man derfor ændringer, fx mens pladen hældes eller temperaturen skifter.

## 7. Hvad betyder faseskifteren?

**a)** Eksempler:

- en tynd glasplade eller et andet gennemsigtigt stof i den ene arm
- en lille forskel i armlængde, fx ved at flytte et spejl
- en gas med andet tryk eller en anden sammensætning i den ene arm
- en temperaturændring i den ene arm
- en faseskifter med flydende krystal, styret med en spænding
- i atominterferometre: en forskel i tyngdefeltet mellem armene

**b)** Uden markering lægges amplituderne fra de to arme sammen ved BS2. Den relative fase bestemmer, om de forstærker eller ophæver hinanden mod hver detektor. Ændres $\phi$, flyttes sandsynligheden mellem D0 og D1.

**c)** Med markering lægges sandsynlighederne sammen i stedet for amplituderne. Fasen indgår kun i interferensleddet, og det forsvinder. Derfor er fordelingen 50/50 uanset $\phi$.

## 8. Fortegnskonventionen og fase

Med reglerne uden minus giver begge indgange samme udgangstilstand $\tfrac{1}{\sqrt2}\big(|0\rangle + |1\rangle\big)$.

**a)** Efter BS1:

$$\mathrm{BS}\,|0\rangle = \tfrac{1}{\sqrt2}\big(|0\rangle + |1\rangle\big)$$

Efter BS2:

$$\tfrac{1}{\sqrt2}\big(\mathrm{BS}\,|0\rangle + \mathrm{BS}\,|1\rangle\big) = \Big(\tfrac12|0\rangle + \tfrac12|1\rangle\Big) + \Big(\tfrac12|0\rangle + \tfrac12|1\rangle\Big) = |0\rangle + |1\rangle$$

**b)** $P_0 = 1^2 = 1$ og $P_1 = 1^2 = 1$, så $P_0 + P_1 = 2$. Fotonen skulle altså med sikkerhed ende i D0 *og* med sikkerhed ende i D1. Det er umuligt: der kommer dobbelt så meget lys ud, som der blev sendt ind.

**c)** Faseskifteren giver $\tfrac{1}{\sqrt2}\big(|0\rangle - |1\rangle\big)$ lige før BS2. Efter BS2:

$$\tfrac{1}{\sqrt2}\big(\mathrm{BS}\,|0\rangle - \mathrm{BS}\,|1\rangle\big) = \Big(\tfrac12|0\rangle + \tfrac12|1\rangle\Big) - \Big(\tfrac12|0\rangle + \tfrac12|1\rangle\Big) = 0$$

Nu er $P_0 = P_1 = 0$, så $P_0 + P_1 = 0$. Fotonen forsvinder, selv om beamsplitterne ikke absorberer lys.

**d)** Med de rigtige regler:

| $\phi$ | Tilstand efter BS2 | $P_0$ | $P_1$ | $P_0 + P_1$ |
|:--|:--|:--|:--|:--|
| 0 | $\vert 0\rangle$ | 1 | 0 | 1 |
| $\pi$ | $\vert 1\rangle$ | 0 | 1 | 1 |

(Udregningerne er dem fra opgave 2 og forklaringen.) Summen er 1 i begge tilfælde.

**e)** Uden minus kan beamsplitteren ikke skelne de to indgange: de giver nøjagtig samme udgangstilstand. Så lægges bidragene fra de to arme altid sammen på samme måde mod begge detektorer. Enten forstærker de hinanden begge steder (for meget lys), eller også ophæver de hinanden begge steder (fotonen forsvinder). Med et minus i den ene regel forstærker bidragene hinanden mod den ene detektor og ophæver hinanden mod den anden. Så flyttes sandsynligheden kun mellem detektorerne, og summen forbliver 1. Minusset handler altså ikke om, hvad der sker med den enkelte foton ved transmission, men om at beamsplitteren ikke må skabe eller fjerne lys.

**f)** En beamsplitter kan fx laves, så refleksion fra den ene side giver et faseskift på $\pi$, mens refleksion fra den anden side og transmission ikke giver noget. Med to ens orienterede beamsplittere af den type får amplituden for fotonen i arm 1 et faseskift på $\pi$ ved refleksion i begge beamsplittere. Regner man vejene igennem, får hver af de fire veje nøjagtig samme fortegn som med simuleringens regler. Simuleringen flytter blot fortegnet i arm 1 over på én transmission.

> **Til læreren:** Opgaven viser, at et minus er nødvendigt, men ikke hvor det skal sidde. Stærke elever kan undersøge, at det også virker at sætte minusset et andet sted, fx $\mathrm{BS}\,|0\rangle = \tfrac{1}{\sqrt2}(|0\rangle - |1\rangle)$ og $\mathrm{BS}\,|1\rangle = \tfrac{1}{\sqrt2}(|0\rangle + |1\rangle)$: summen er stadig 1, men den lyse detektor ved $\phi = 0$ kan skifte. Generelt giver en indgangstilstand $a|0\rangle + b|1\rangle$ sandsynlighederne $\tfrac12(a+b)^2$ og $\tfrac12(a-b)^2$, som altid summer til $a^2 + b^2 = 1$.

## 9. Betyder et klik i D0, at fotonen tog arm 0?

**a)** Nej. Man kunne fristes til at tro, at alle fotonerne har taget arm 0, men havde fotonen kun taget arm 0, ville den ankomme alene til BS2 og ende 50/50 i de to detektorer. At alle klik ender i D0, er netop et resultat af, at bidragene fra begge arme interfererer.

**b)** Uden BS2 fortsætter en foton fra arm 0 lige op i D0, og en foton fra arm 1 fortsætter lige ud til højre i D1.

**c)** Navnene er valgt, så detektor $k$ ville registrere en foton fra arm $k$, hvis BS2 ikke var der. Med BS2 på plads modtager hver detektor bidrag fra begge arme, og klikket er et måleresultat for hele superpositionen, ikke for vejen.

> **Til læreren:** Opgaven er lavet til at forebygge en misforståelse, som navnene "detektor 0" og "detektor 1" let fører til. Den hænger tæt sammen med komplementaritet: Uden BS2 måler detektorerne vejen, med BS2 måler de interferensen.

---

## Til læreren: simuleringens forenklinger

- **Animationen med markering:** Når hvilken-vej-markeringen er slået til, viser simuleringen fotonen lokaliseret i den ene arm, som om vejen bliver aflæst. Fysisk er det nok, at vejen *kan* aflæses. Fordelingen er den samme.
- **Faste fasebidrag:** Spejlene og beamsplitternes glas giver i virkeligheden også faser. De er ens i begge arme eller lagt ind i nulpunktet for $\phi$, så $\phi = 0$ er defineret som den indstilling, hvor D0 er lys.
- **Skyderen:** Fasen kan kun sættes i trin på 5°. Opgaverne bruger kun værdier, der kan indstilles.
- **Statistikken nulstilles**, når fasen ændres, eller markeringen slås til eller fra. Eleverne skal derfor aflæse andelene, før de ændrer indstilling.
