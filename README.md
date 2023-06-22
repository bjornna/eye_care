# ArenaEyeCare

Dette er repo for utvikling av klinisk applikasjon for oppfølging av pasienter
med øyesykdommer.

Foreløpig har vi i alle fall følgende variabler på blokka:

- Visus

  - måle på høyre og venstre
  - et desimaltall
  - vanlig og uvanlig måte (Snell eller Logmar)
  - +/- er en standardisert tavle med 5 bokstaver per linje - med alle
    bokstavene på en linje får du 1.0 , men klarer du bare 4 får du minus, 3
    minus/minus
  - 0.2 fratrekk eller tillegg per bokstav
  - Noen maskiner gir ut tall på f.eks. 0.63 (Logmar) som ikke passer helt.

- Øye trykk
sta
  - Et tall
  - Metodeavhengig - to vanlige, instrumentet, GAT (Goldman/gullstandard) eller
    EyeCare (som er enklere å gjennomføre)

- Refraksjon

  - BrillestyrkeW
  - Tre verdier per øye; sfærisk, sylinder (skjeve hornhinner) og akser

- Akselengde

  - Hvor langt øyet er, f.eks. ved grå stær operasjon
  - Relativt stabilt

  Akselengdemåling er måling av øyets akselengde, det vil si lengden fra sentrum av hornhinnen til netthinnens skarpsynområde (macula). Undersøkelsen er nødvendig for å kunne beregne riktig styrke på den kunstige linsen som settes inn i øyet til erstatning for den syke linsen ved operasjon for grå stær.

- Hornhinnetykkelse

  - Relatvit stabilt - kan være viktig for sykdommen eller for å tolke
    resultateet av andre målinger

- CCT (hornhinnetykkelse)

- Lysvei (grad 0-4)

  - Sun klassifisering, angir standard lysspalte og eller antalle
    betennelsesceller
  - F.eks. pasienter med barneleddgikt følger opp dette flere ganger i året.

  - Er det denne graderingen som skal benyttes?
    https://www.helsebiblioteket.no/innhold/retningslinjer/oftalmologi-nasjonal-kvalitetshandbok-for-oftalmologi/uveitt

- Diabetes retinopati grad (0-5)

  - Beskrevet i nasjonal retnlingslinjer - internasjonal klassifisering

- Diabetes makulopati grad (0-2)
  - Maya Gran Bjerke på Ullevål har meldt inn noe der
  - Litt mer ullent definert i fagmiljøet
  - To modaliteter (foto eller OCT)
  - Ulik klassifisering: Foto (ingen, tilstede, klinisk signifikant), OCT
    (ingen, tilstede, center invovolving)
  - Kan gjøre begge deler, dvs. Foto og OCT
  - Foto for diabetesscreening (bildene blir gradert til makulopati som utløser
    OCT)
  - OCT er gullstandard - og foto for screening/siling

Mulige skjema:

- Diabetes retinopati screening
- Injeksjonsbehandling
- Glaukom kontroll
- Katarakt forundersøkelse-operasjon-etterktr
- Uveitt kontroll

```code
no.dips.arena.eyecare::RET::Diabetes retinopati screening
no.dips.arena.eyecare::INJ::Injeksjonsbehandling
no.dips.arena.eyecare::GLA::Glaukom kontroll
no.dips.arena.eyecare::KAT::Katarakt forundersøkelse-operasjon-etterktr
no.dips.arena.eyecare::UVE::Uveitt kontroll
```

## UNN

Ønsker å gjøre det enklere og bedre.

Arbeidsflyt

Ønsket: Bilder tas av sykepleier og graderes først av sykepleier. Flertallet
graderes ferdig av spl, og noen til øyelege.

Glaukomontroll: Visus og trykk hos sykepleier. Noen ganger av lege.

I dag (glaukom):

- Sykepleier dokumenterer i sitt notat (forundersøkelse)
- Lege gjentar det samme med copy-paste fra spl. dokumentet.

Ønsker oppsummering for gjengangspasienter: Benytter kursiv dokument.

Epikrise:

- legenotatet går ut som epikrise

Søkt midler sammen med Ullevål: HBNC (langtids blodsukker) - ønsker data fra
primærlegene som følger opp pasientene fra dag til dag. Praksisnett - (Snowboks)
som henter data fra fastlegenes system til DIPS. Kobler på Retina Risk
Applikasjonen fra Island.

Involverte:

- Leger
- Sykepleiere
- Optikere
- Helsefagarbeidere som kan gjøre visus og øyetrykk

### Diabetes Retinarisk screening

Diabetes retinopati (0-5) - gjentatte kontroller og ønsker å få presentert
resultatene på en bedre måte.

Nasjonalt register for diabetes. Ønsker å få levert ut opplysninger fra
screening til registeret. Benytter FastTrak i dag.

Spm: Fungerer FastTrak etter hensikten med tanke på variablene? Ja - tror den er
dekkende.

### Poliklinisk

Andre problemer enn diabetes , f.eks. injeksjon. Kontroller med 4-16 ukers
intervaller.

### En gangs opplysninger

Som er gunstig å ha tilgjengelig. Som f.eks. øyetrykk som er gunstig å få over
flere år.

Faste/konstante variabler

- Hornhinnetykkelse

## Løsningsdesign

### Sak

Det opprettes en sak per registrering. Formålet med dette er å kunne bruke VAQM
for å hente ut data fra hver konsultasjon.

## Bakgrunnsmateriale

Se eksempel journaldokumenter fra Helse Nord:
https://365dips.sharepoint.com/:w:/s/ehrcraft_dev/EZy-Pug-aldHqUFANuU0fTABB_n420KMbYDqHritiwIZtg?e=T8I0ee

- Øye DIPS - inkubator arketyper.no:
  https://arketyper.no/ckm/incubators/1078.43.66
- Øye - inkubator arketyper.no : https://arketyper.no/ckm/incubators/1078.43.40
- Ophthalmology - apperta.org: https://ckm.apperta.org/ckm/projects/1051.61.53

## Arketyper

- CCT - Central Cornea Thickness Details
  https://ckm.openehr.org/ckm/archetypes/1013.1.2015
- Visus (Skarpsyn)/ Visual acuity test result
  https://arketyper.no/ckm/archetypes/1078.36.2467
- Fundoscopic examination of eyes
  https://ckm.openehr.org/ckm/archetypes/1013.1.208
- Diabetes retinopati ous dips https://arketyper.no/ckm/archetypes/1078.36.1827
- Refraksjonsdetaljer https://arketyper.no/ckm/archetypes/1078.36.2470

## Andre ressurser

- FastTrak om Retinopati:
  https://fasttrak.dips.no/CRFShowStudy.asp?StudyName=RETINOPATI

- Task planning eksempel:
  https://github.com/openEHR/TP-examples/blob/master/16-eye_outpatient/index.adoc

## Diabetes retinopati grade

Below is extract from a published paper about the International Clinical Disease
Severity Scale for diabetich retinopathy(DR). Source:
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3874488/#sec-3title

- 1: **no apparent retinopathy** The first is “no apparent retinopathy”. As the
  name implies there are no diabetic fundus changes.
- 2: **mild non-proliferative retinopathy** The second stage is “mild
  non-proliferative retinopathy” (NPDR). This stage is characterized by the
  presence of a few microaneurysms.
- 3: **moderate NPDR** The third stage is “moderate NPDR” which is characterized
  by the presence of microaneurysms, intraretinal hemorrhages or venous beading
  that do not reach the severity of the standard photographs 2A
- 4: **Severe NPDR** “Severe NPDR”, the fourth stage, is the key level to
  identify. Data from the ETDRS has shown that eyes in patients with DM type 2
  that reach the grade of severe NPDR have a 50% chance of developing high risk
  characteristics if laser treatment is not instituted.
- 5: **proliferative diabetic retinopathy (PDR)**. The final stage is
  “proliferative diabetic retinopathy” (PDR). PDR is characterized by
  neovascularization of the disc, neovascularization of the retina,
  neovascularization of the iris, neovascularization of the angle, vitreous
  hemorrhage or tractional retinal detachment. With regards to macular edema, it
  should be noted if macular edema is present or absent. If it is present then
  it can be further classified as mild, moderate and severe depending on the
  distance of the exudates and thickening from the center of the fovea

## Lysvei

### GRADING INFLAMMATION AND DOCUMENTING COMPLICATIONS

**SUN** = Standardization of uveitis nomenclature.

Reference: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8935739/, PMC 2022 Mar 21

The SUN\* Working Group Grading Scheme for Anterior Chamber Cells

| Grade | Cells in Field† |
| ----- | --------------- |
| 0     | <1              |
| 0.5+  | 1–5             |
| 1+    | 6–15            |
| 2+    | 16–25           |
| 3+    | 26–50           |
| 4+    | >50             |

†Field size is a 1 mm by 1 mm slit beam.

The SUN\* Working Group Grading Scheme for Anterior Chamber Flare

| Grade | Description                            |
| ----- | -------------------------------------- |
| 0     | None                                   |
| 1+    | Faint                                  |
| 2+    | Moderate (iris and lens details clear) |
| 3+    | Marked (iris and lens details hazy)    |
| 4+    | Intense (fibrin or plastic aqueous)    |

The SUN\* Working Group Activity of Uveitis Terminology

| Term               | Definition                                                                                                               |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| Inactive           | Grade 0 cells†                                                                                                           |
| Worsening activity | Two step increase in level of inflammation (e.g. anterior chamber cells, vitreous haze) or increase from grade 3+ to 4 + |
| Improved activity  | Two step decrease in level of inflammation (e.g. anterior chamber cells, vitreous haze) or decrease to grade 0           |
| Remission          | Inactive disease for ≥3 months after discontinuing all treatments for eye disease                                        |

## Visus - snellen / logmar

Column A: snellen numerator

Column B: snellen denominator

Column C: letters gained (+) or missed (−)

Column D: logMAR acuity

ENTER INTO FORMULA BAR FOR CELL: = ROUND(LOG(B2/A2),2)−(C2\*0.02)
