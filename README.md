___Hvis du afprøver dette sikkerhedshul, så brug din egen NemID bruger!___

Indledning
----------

NemID er sårbart over for et nemt angreb (en uges forberedelse, hvis man har erfaring med Javascript og Puppeteer).
Digitaliseringsstyrelsen er opmærksom på det, men synes ikke det vigtigt nok til at ændre på arkitekturen. Formentligt fordi de synes det vil gå ud over brugervenligheden.

Problemet blev beskrevet i [2011](https://www.version2.dk/artikel/overblik-her-er-kritikken-af-nemid-32893) af version2 med en manuel process fra angriberen.
Og er i [2018](https://www.version2.dk/artikel/digitaliseringsstyrelsen-efter-udvikler-angreb-ja-nemid-saarbar-phishing-1086131) blevet demonstreret på en automatiseret måde.

Tidligere lå der kode her, som demonstrerede, hvor nemt det er for sider med NemID login, at gøre noget andet end forventet med brugerens NemID uden at brugeren opdager det.

Men koden er fjernet, da Digitaliseringsstyrelsen har truet med at gå til politiet.

Hvordan beskytter jeg mig?
--------------------------
NemID appen beskytter delvist mod dette angreb, så indtil Digitaliseringsstyrelsen retter problemet, så brug altid NemID appen og tjek at der står det forventede inden du godkender i appen.

Hvis du er ved at logge på fx nemid.dk og NemID appen skriver fx din banks navn, og du ikke godkender, så har svindlerne allerede fået dit brugernavn og adgangskode. Sker det, så skal du ændre din kode på https://nemid.nu og kontakte NemID support.

Formålet med projektet
----------------------
Digitaliseringsstyrelsen skal erkende, at det er nødvendigt for sikkerheden, at de ændrer arkitekturen for NemID/MitID.
Der er adskillige gange gjort opmærksom på problemet uden at styrelsen har lukket hullet.
For at presse styrelsen til at reagere og beskytte os alle, gjorde koden her, det nemt for enhver at se, hvor nemt det er at lave et NemID phishing site.

Problemet
---------
NemID login boksen tillades på mange forskellige domæner. Som slutbruger kan du ikke vide, om du sender login oplysningerne til NemID eller til den hjemmeside, du er ved at logge ind på.
Hvis man fjerner den mulighed og informerer brugerne om hvilket domæne, der skal stå i adresselinjen, så har brugerne mulighed for at opdage snyd.

Løsningen
---------
Hvis man kun måtte logge ind gennem https://nemlog-in.dk og brugerne blev oplyst om det, så ville sikkerhedshullet være lukket.
Der kunne f.eks. stå på nøglekortet: Indtast kun disse nøgler på https://nemlog-in.dk og i NemID appen.

Det offentliges hjemmesider bruger en fælles NemID gateway til borger.dk, sundhed.dk osv. Man bliver altid omdirigeret til https://nemlog-in.dk, logger ind, og bliver så sendt tilbage til siden man kom fra.
Så løsningen kunne være at kræve, at de private sider også benytter sig af https://nemlog-in.dk.

Er det nødvendigt at offentliggøre koden?
-----------------------------------------
Mange spørger: "kan du ikke nøjes med at omtale problemet i artikler i medierne", hvortil jeg henviser at det allerede har været forsøgt.
Selve idéen til angrebet blev offentliggjort i 2011, så Digitaliseringsstyrelsen har haft mere end nok tid til at gøre noget ved problemet.
Tilsyneladende synes Digitaliseringsstyrelsen ikke at problemet er alvorligt.

Men nu er koden så alligevel fjernet, og andre metoder undersøges.

For dem der vil stjæle penge ved at udnytte dette hul, er det ikke en stor investering at bruge 1-2 uger på at forberede koden.

Trusselsbrevet
--------------
Hvis Digitaliseringsstyrelsen ikke synes at problemet er alvorligt, hvorfor truer de så med at anmelde dette projekt til politiet?

[2020-03-digst.dk-Brev fra Digitaliseringsstyrelsen.pdf](2020-03-digst.dk-Brev%20fra%20Digitaliseringsstyrelsen.pdf)

Der står intet i brevet om at problemet er alvorligt, ej heller at de har tænkt sig rette noget i NemID løsningen.
De påstår at dette projekt opfordrer andre til at udføre ulovlige handlinger i form af hacking.
Hvilket det ikke gør.

Tidligere var der her på siden en opfordring til at forbedre dette projekt. Den er nu fjernet.

Der var også en opfordring til at lave en video af, at det bliver brugt. Med det var der ment, at man brugte det med sin egen NemID bruger!

Videodemo
---------
Der er en dårlig video her i to versioner (det kommer an på din enhed hvilket format der virker).
http://philosof.dk/rune/nemid.ogv
http://philosof.dk/rune/nemid.mkv

Den er afsluttet inden demoen viser det interessante, fordi det er persondata.
Forhåbentligt bliver der laves en version med den sidste del sløret de rigtige steder.
