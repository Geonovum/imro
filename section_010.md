# Attribuutwaarden {#090B956C}

## Attribuutwaarden en datatypen {#454FBC1A}

Voor de waarden van de attributen zijn verschillende datatypen te onderscheiden. De volgende indeling geeft de gebruikte datatypen weer.

<table style='width: 100%;'><caption>Tabel 3 Indeling datatypen</caption>
<colgroup><col id='col1' style='width: 28.48101265822785%;'>
<col id='col2' style='width: 71.51898734177216%;'>
</colgroup>
<thead valign='top'><tr><th align='left'><span style='color: #auto;'>Datatype</span><br/>
</th>
<th align='left'><span style='color: #auto;'>Omschrijving</span><br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>Standaard</td>
<td align='left'>Characterstring, Integer, etc.</td>
</tr>
<tr><td align='left'>ScopedName</td>
<td align='left'></td>
</tr>
<tr><td align='left' colspan='2'>Geometrie</td>
</tr>
<tr><td align='left'>GM_Point</td>
<td align='left'>Punt object</td>
</tr>
<tr><td align='left'>GM_Curve</td>
<td align='left'>Lijn object</td>
</tr>
<tr><td align='left'>GM_Surface</td>
<td align='left'>Vlak object</td>
</tr>
<tr><td align='left'>GM_MultiPoint</td>
<td align='left'>Meerdere punten in één geometrie</td>
</tr>
<tr><td align='left'>GM_MultiCurve</td>
<td align='left'>Meerdere lijnen in één geometrie</td>
</tr>
<tr><td align='left'>GM_MultiSurface</td>
<td align='left'>Meerdere vlakken in één geometrie</td>
</tr>
<tr><td align='left' colspan='2'>Domeinlijsten</td>
</tr>
<tr><td align='left'>&lt;&lt;enumeration&gt;&gt;</td>
<td align='left'>Opsommend limitatief.</td>
</tr>
<tr><td align='left'>&lt;&lt;CodeList&gt;&gt;</td>
<td align='left'>Opsommend uitbreidbaar.</td>
</tr>
<tr><td align='left' colspan='2'>Stereotypen</td>
</tr>
<tr><td align='left'>&lt;&lt;featureType&gt;&gt;</td>
<td align='left'>geo-object [NEN-EN-ISO 19136]. Objecttype gebruikt voor het

representeren van geo-informatie</td>
</tr>
<tr><td align='left'>&lt;&lt;dataType&gt;&gt;</td>
<td align='left'>gestructureerd datatype zonder identiteit<br/>
[ISO/TS 19103:2005]<br/>
</td>
</tr>
<tr><td align='left'>&lt;&lt;union&gt;&gt;</td>
<td align='left'>gestructureerd datatype zonder identiteit waarvan precies één van de<br/>
eigenschappen aanwezig is in elke instantie

[ISO/TS 19103:2005]</td>
</tr>
<tr><td align='left'>&lt;&lt;identificatie&gt;&gt; </td>
<td align='left'>attribuut voor unieke identificatie volgens NEN 3610</td>
</tr>
<tr><td align='left'></td>
<td align='left'></td>
</tr>
</tbody>
</table>

<b>ScopedName</b>: Een attribuut met het type ScopedName is vergelijkbaar met een CharacterString attribuut. Alleen is er ook de mogelijkheid om bij de tekst optioneel een scope op te nemen waarbinnen die naam is gedefinieerd. Deze scope bevat dan een verwijzing naar de instantie die de naam heeft afgegeven.<br/>
Voorbeeld: De officiële straatnaam krijgt als scope een verwijzing naar de gemeente die de straatnaam heeft afgegeven. Eventuele onofficiële namen krijgen dan geen scope.<br/>
Bij de IMRO coderingen wordt de scope niet ingevuld.  
<br/>

<b>Enumeraties</b>: In IMRO is een groot aantal voor-gedefinieerde datatypen als enumeratielijst opgenomen. Dit zijn lijsten van toegestane waarden die een attribuut binnen IMRO kan aannemen. Een enumeratielijst is limitatief en binnen het model niet uitbreidbaar. Niet voor elke attribuut kan een lijst met mogelijke waarden gedefinieerd worden. Dit komt voor omdat het (nu) niet mogelijk of zinvol is om een lijst te maken die binnen de Ruimtelijke Ordening geldt.  
<br/>

<b>CodeList</b>: Bij de opgenomen enumeratielijsten is aangegeven of ze van het type CodeList zijn. Als dit het geval is kunnen de lijsten uitgebreid worden met attribuutwaarden die nog niet in het model gedefinieerd zijn. Bij de uitwisseling worden deze waarden voorafgegaan door het woord ‘other’. Zie voorbeeld.  
<br/>

Een waarde uit de enumeratielijst OmvangWaarde:<br/>
&lt;imro2012:OmvangWaarde&gt;<span style='color: #00B050;'>aantal parkeerplaatsen</span>&lt;/imro2012:OmvangWaarde&gt;

Een waarde die aan de enumeratielijst OmvangWaardeBestemmingsplan is toegevoegd:<br/>
&lt;imro2012:OmvangWaarde&gt;<span style='color: #00B050;'>other: aantal parkeermeters</span>&lt;/imro2012:OmvangWaarde&gt;  
<br/>

<b>Nieuw datatype. Samengesteld attribuut</b>: Wanneer attributen gecombineerd dienen te worden, wordt dit aangegeven door de creatie van een nieuw datatype. Het nieuwe datatype is een klasse van het stereotype &lt;&lt;dataType&gt;&gt; waarvan de attributen gevormd worden door de te combineren attributen. Deze attributen hebben weer hun eigen specifieke datatype. Een voorbeeld is het datatype ‘TekstReferentie’ dat samengesteld is uit een attribuut voor een link naar een tekst een een attribuut om het soort tekst aan te geven.

## Domeinwaarden {#1AF2DC22}

In de volgende paragrafen zijn alle in IMRO voorkomende domeinen van attribuutwaarden opgenomen. Het bijbehorende stereotype, enumeratie of CodeList wordt aangegeven. Bij de naamgeving is in een aantal gevallen rekening gehouden met het type instrument of planobject waarin het domein wordt gebruikt. Dit is alleen gedaan indien voor eenzelfde attribuut bij verschillende planobjecten een andere domeinlijst gebruikt wordt. Bijvoorbeeld Illustratie_BP en Illustratie_GSV.

Voor codelijsten geldt standaard dat ze uitgebreid kunnen worden conform het standaard format ‘other:…….’. Indien een ander format voorgeschreven is, is dat in of bij de lijsten opgenomen.  
<br/>

<b>Bestemmingshoofdgroep_E</b><br/>
Definitie: Hoofdgroepen waar specifieke bestemmingen in ingedeeld kunnen worden.<br/>
Bron: SVBP2012.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt;enumeration&gt;&gt;<br/>
Bestemmingshoofdgroep_E<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>agrarisch<br/>
</td>
</tr>
<tr><td align='left'>agrarisch met waarden<br/>
</td>
</tr>
<tr><td align='left'>bedrijf<br/>
</td>
</tr>
<tr><td align='left'>bedrijventerrein<br/>
</td>
</tr>
<tr><td align='left'>bos<br/>
</td>
</tr>
<tr><td align='left'>centrum<br/>
</td>
</tr>
<tr><td align='left'>cultuur en ontspanning<br/>
</td>
</tr>
<tr><td align='left'>detailhandel<br/>
</td>
</tr>
<tr><td align='left'>dienstverlening<br/>
</td>
</tr>
<tr><td align='left'>gemengd<br/>
</td>
</tr>
<tr><td align='left'>groen<br/>
</td>
</tr>
<tr><td align='left'>horeca<br/>
</td>
</tr>
<tr><td align='left'>kantoor<br/>
</td>
</tr>
<tr><td align='left'>maatschappelijk<br/>
</td>
</tr>
<tr><td align='left'>natuur<br/>
</td>
</tr>
<tr><td align='left'>overig<br/>
</td>
</tr>
<tr><td align='left'>recreatie<br/>
</td>
</tr>
<tr><td align='left'>sport<br/>
</td>
</tr>
<tr><td align='left'>tuin<br/>
</td>
</tr>
<tr><td align='left'>verkeer<br/>
</td>
</tr>
<tr><td align='left'>water<br/>
</td>
</tr>
<tr><td align='left'>wonen<br/>
</td>
</tr>
<tr><td align='left'>woongebied<br/>
</td>
</tr>
</tbody>
</table>

<b>Bestemmingshoofdgroep_D</b><br/>
Definitie: Hoofdgroepen waar specifieke dubbelbestemmingen in ingedeeld kunnen worden.<br/>
Bron: SVBP2012.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt;enumeration&gt;&gt;<br/>
Bestemmingshoofdgroep_D<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>leiding<br/>
</td>
</tr>
<tr><td align='left'>waarde<br/>
</td>
</tr>
<tr><td align='left'>waterstaat<br/>
</td>
</tr>
</tbody>
</table>

<b>Bestemmingshoofdgroep_ED</b><br/>
Definitie: Samenvoeging van Bestemmingshoofdgroep_E en Bestemmingshoofdgroep_D in één lijst.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt;enumeration&gt;&gt;<br/>
Bestemmingshoofdgroep_ED<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>Voor inhoud zie Bestemmingshoofdgroep_E en Bestemmingshoofdgroep_D<br/>
</td>
</tr>
</tbody>
</table>

<b>Bouwaanduidingen</b><br/>
Definitie: Naamgeving voor bouwaanduidingen in een bestemmingsplan.<br/>
Bron: SVBP2012.<br/>
Opmerking: Een aantal waarden zijn conform een bepaald format vrij intevullen. De vrij intevullen tekst is met .. aangegeven.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt;enumeration&gt;&gt;<br/>
&lt;&lt;CodeList&gt;&gt;<br/>
Bouwaanduidingen<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>aaneengebouwd<br/>
</td>
</tr>
<tr><td align='left'>antennemast<br/>
</td>
</tr>
<tr><td align='left'>bijgebouwen<br/>
</td>
</tr>
<tr><td align='left'>gestapeld<br/>
</td>
</tr>
<tr><td align='left'>kap<br/>
</td>
</tr>
<tr><td align='left'>karakteristiek<br/>
</td>
</tr>
<tr><td align='left'>nokrichting<br/>
</td>
</tr>
<tr><td align='left'>onderdoorgang<br/>
</td>
</tr>
<tr><td align='left'>plat dak<br/>
</td>
</tr>
<tr><td align='left'>twee-aaneen<br/>
</td>
</tr>
<tr><td align='left'>vrijstaand<br/>
</td>
</tr>
<tr><td align='left'><i>Bouwaanduidingen voor uitgesloten aspecten:</i><br/>
</td>
</tr>
<tr><td align='left'>aaneengebouwd uitgesloten<br/>
</td>
</tr>
<tr><td align='left'>antennemast uitgesloten<br/>
</td>
</tr>
<tr><td align='left'>bijgebouwen uitgesloten<br/>
</td>
</tr>
<tr><td align='left'>gestapeld uitgesloten<br/>
</td>
</tr>
<tr><td align='left'>kap uitgesloten<br/>
</td>
</tr>
<tr><td align='left'>karakteristiek uitgesloten<br/>
</td>
</tr>
<tr><td align='left'>nokrichting uitgesloten<br/>
</td>
</tr>
<tr><td align='left'>onderdoorgang uitgesloten<br/>
</td>
</tr>
<tr><td align='left'>plat dak uitgesloten<br/>
</td>
</tr>
<tr><td align='left'>twee-aaneen uitgesloten<br/>
</td>
</tr>
<tr><td align='left'>vrijstaand uitgesloten<br/>
</td>
</tr>
<tr><td align='left'><i>Bouwaanduidingen die aangevuld moeten worden in het waardeveld van het attribuut naam:</i><br/>
</td>
</tr>
<tr><td align='left'>specifieke bouwaanduiding - ..<br/>
</td>
</tr>
<tr><td align='left'>specifieke bouwaanduiding uitgesloten - ..<br/>
</td>
</tr>
</tbody>
</table>

<b>Figuren</b><br/>
Definitie: Naamgeving voor figuren in een bestemmingsplan.<br/>
Bron: SVBP2012.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt;enumeration&gt;&gt;<br/>
&lt;&lt;CodeList&gt;&gt;<br/>
Figuren<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>as van de weg<br/>
</td>
</tr>
<tr><td align='left'>dwarsprofiel<br/>
</td>
</tr>
<tr><td align='left'>gevellijn<br/>
</td>
</tr>
<tr><td align='left'>hartlijn leiding - brandstof<br/>
</td>
</tr>
<tr><td align='left'>hartlijn leiding - gas<br/>
</td>
</tr>
<tr><td align='left'>hartlijn leiding - hoogspanning<br/>
</td>
</tr>
<tr><td align='left'>hartlijn leiding - hoogspanningsverbinding<br/>
</td>
</tr>
<tr><td align='left'>hartlijn leiding - olie<br/>
</td>
</tr>
<tr><td align='left'>hartlijn leiding - riool <br/>
</td>
</tr>
<tr><td align='left'>hartlijn leiding - water <br/>
</td>
</tr>
<tr><td align='left'>relatie<br/>
</td>
</tr>
<tr><td align='left'><i>Figuur waarvan de naam aangevuld moeten worden in het waardeveld van het attribuut naam:</i><br/>
</td>
</tr>
<tr><td align='left'>hartlijn leiding - ..<br/>
</td>
</tr>
</tbody>
</table>

<b>Gebiedsaanduidingen</b><br/>
Definitie: Naamgeving voor gebiedsaanduidingen in een bestemmingsplan.<br/>
Bron: SVBP2012.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt;enumeration&gt;&gt;<br/>
&lt;&lt;CodeList&gt;&gt;<br/>
Gebiedsaanduidingen<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>geluidzone<br/>
</td>
</tr>
<tr><td align='left'>geluidzone - ..<br/>
</td>
</tr>
<tr><td align='left'>geluidzone - industrie<br/>
</td>
</tr>
<tr><td align='left'>geluidzone - industrie ..<br/>
</td>
</tr>
<tr><td align='left'>geluidzone - spoor<br/>
</td>
</tr>
<tr><td align='left'>geluidzone - spoor ..<br/>
</td>
</tr>
<tr><td align='left'>geluidzone - weg<br/>
</td>
</tr>
<tr><td align='left'>geluidzone - weg ..<br/>
</td>
</tr>
<tr><td align='left'>luchtvaartverkeerzone<br/>
</td>
</tr>
<tr><td align='left'>luchtvaartverkeerzone - ..<br/>
</td>
</tr>
<tr><td align='left'>milieuzone<br/>
</td>
</tr>
<tr><td align='left'>milieuzone - ..<br/>
</td>
</tr>
<tr><td align='left'>milieuzone - bodembeschermingsgebied<br/>
</td>
</tr>
<tr><td align='left'>milieuzone - bodembeschermingsgebied ..<br/>
</td>
</tr>
<tr><td align='left'>milieuzone - geluidsgevoelige functie<br/>
</td>
</tr>
<tr><td align='left'>milieuzone - geluidsgevoelige functie ..<br/>
</td>
</tr>
<tr><td align='left'>milieuzone - geurzone<br/>
</td>
</tr>
<tr><td align='left'>milieuzone - geurzone ..<br/>
</td>
</tr>
<tr><td align='left'>milieuzone - grondwaterbeschermingsgebied<br/>
</td>
</tr>
<tr><td align='left'>milieuzone - grondwaterbeschermingsgebied ..<br/>
</td>
</tr>
<tr><td align='left'>milieuzone - stiltegebied<br/>
</td>
</tr>
<tr><td align='left'>milieuzone - stiltegebied ..<br/>
</td>
</tr>
<tr><td align='left'>milieuzone - waterwingebied<br/>
</td>
</tr>
<tr><td align='left'>milieuzone - waterwingebied ..<br/>
</td>
</tr>
<tr><td align='left'>milieuzone - zones wet milieubeheer<br/>
</td>
</tr>
<tr><td align='left'>milieuzone - zones wet milieubeheer ..<br/>
</td>
</tr>
<tr><td align='left'>overige zone<br/>
</td>
</tr>
<tr><td align='left'>overige zone - ..<br/>
</td>
</tr>
<tr><td align='left'>reconstructiewetzone<br/>
</td>
</tr>
<tr><td align='left'>reconstructiewetzone - ..<br/>
</td>
</tr>
<tr><td align='left'>reconstructiewetzone - extensiveringsgebied<br/>
</td>
</tr>
<tr><td align='left'>reconstructiewetzone - extensiveringsgebied ..<br/>
</td>
</tr>
<tr><td align='left'>reconstructiewetzone - landbouwontwikkelingsgebied<br/>
</td>
</tr>
<tr><td align='left'>reconstructiewetzone - landbouwontwikkelingsgebied ..<br/>
</td>
</tr>
<tr><td align='left'>reconstructiewetzone - verwevingsgebied<br/>
</td>
</tr>
<tr><td align='left'>reconstructiewetzone - verwevingsgebied ..<br/>
</td>
</tr>
<tr><td align='left'>veiligheidszone<br/>
</td>
</tr>
<tr><td align='left'>veiligheidszone - ..<br/>
</td>
</tr>
<tr><td align='left'>veiligheidszone - bevi<br/>
</td>
</tr>
<tr><td align='left'>veiligheidszone - bevi ..<br/>
</td>
</tr>
<tr><td align='left'>veiligheidszone - leiding<br/>
</td>
</tr>
<tr><td align='left'>veiligheidszone - leiding ..<br/>
</td>
</tr>
<tr><td align='left'>veiligheidszone - lpg<br/>
</td>
</tr>
<tr><td align='left'>veiligheidszone - lpg ..<br/>
</td>
</tr>
<tr><td align='left'>veiligheidszone - munitie<br/>
</td>
</tr>
<tr><td align='left'>veiligheidszone - munitie ..<br/>
</td>
</tr>
<tr><td align='left'>veiligheidszone - vervoer gevaarlijke stoffen<br/>
</td>
</tr>
<tr><td align='left'>veiligheidszone - vervoer gevaarlijke stoffen ..<br/>
</td>
</tr>
<tr><td align='left'>veiligheidszone - vuurwerk<br/>
</td>
</tr>
<tr><td align='left'>veiligheidszone - vuurwerk ..<br/>
</td>
</tr>
<tr><td align='left'>veiligheidszone - windturbine<br/>
</td>
</tr>
<tr><td align='left'>veiligheidszone - windturbine ..<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - ..<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - buisleidingenstraat<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - buisleidingenstraat ..<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - dijk<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - dijk ..<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - duin<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - duin ..<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - molenbiotoop<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - molenbiotoop ..<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - radar<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - radar ..<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - spoor<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - spoor ..<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - straalpad<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - straalpad ..<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - vaarweg<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - vaarweg ..<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone - weg<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone – weg ..<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone - ..<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone - moderniseringsgebied<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone - moderniseringsgebied ..<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone - afwijkingsgebied<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone - afwijkingsgebied ..<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone - verwezenlijking in de naaste toekomst<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone - verwezenlijking in de naaste toekomst ..<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone - wijzigingsgebied<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone - wijzigingsgebied ..<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone – wet geluidhinder<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone – wet geluidhinder ..<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone – natura 2000 <br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone – natura 2000 ..<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone – tracéwet<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone – tracéwet ..<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone – waterwet<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone – waterwet ..<br/>
</td>
</tr>
</tbody>
</table>

<b>Gebiedsaanduidinggroep</b><br/>
Definitie: Rangschikking voor gebiedsaanduidingen in een bestemmingsplan. De rangschikking is gekoppeld aan de digitale verbeelding van de gebiedsaanduiding<br/>
Bron: SVBP2012.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt;enumeration&gt;&gt;<br/>
Gebiedsaanduidinggroep<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>geluidzone<br/>
</td>
</tr>
<tr><td align='left'>luchtvaartverkeerzone<br/>
</td>
</tr>
<tr><td align='left'>milieuzone<br/>
</td>
</tr>
<tr><td align='left'>reconstructiewetzone<br/>
</td>
</tr>
<tr><td align='left'>veiligheidszone<br/>
</td>
</tr>
<tr><td align='left'>vrijwaringszone<br/>
</td>
</tr>
<tr><td align='left'>wetgevingzone<br/>
</td>
</tr>
<tr><td align='left'>overige zone<br/>
</td>
</tr>
</tbody>
</table>

<b>Idealisatie_1</b><br/>
Definitie: Manier waarop de geometrie ruimtelijk geïnterpreteerd moet worden.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt; enumeration&gt;&gt;<br/>
Idealisatie_1<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>exact<br/>
</td>
</tr>
</tbody>
</table>

<b>Idealisatie_2</b><br/>
Definitie: Manier waarop de geometrie ruimtelijk geïnterpreteerd moet worden.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
Idealisatie_2<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>exact<br/>
</td>
</tr>
<tr><td align='left'>indicatief<br/>
</td>
</tr>
</tbody>
</table>

<b>Idealisatie_3</b><br/>
Definitie: Manier waarop de geometrie ruimtelijk geïnterpreteerd moet worden.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt; enumeration&gt;&gt;<br/>
Idealisatie_3<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>exact<br/>
</td>
</tr>
<tr><td align='left'>indicatief<br/>
</td>
</tr>
<tr><td align='left'>cartografisch figuur<br/>
</td>
</tr>
</tbody>
</table>

<b>Illustratie</b><br/>
Definitie: Verbeelding.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
Illustratie<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>afbeelding<br/>
</td>
</tr>
<tr><td align='left'>kaart<br/>
</td>
</tr>
</tbody>
</table>

<b>Illustratie_BP</b><br/>
Definitie: Verbeelding.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt;enumeration&gt;&gt;<br/>
Illustratie_BP<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>afbeelding<br/>
</td>
</tr>
</tbody>
</table>

<b>Illustratie_XGB</b><br/>
Definitie: Verbeelding.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
Illustratie_XGB<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>kaart<br/>
</td>
</tr>
</tbody>
</table>

<b>Instrument_GSV</b><br/>
Definitie: Juridisch instrument binnen de Wro, Wabo en Chw.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
&lt;&lt;CodeList&gt;&gt;<br/>
Instrument_GSV<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>beheersverordening<br/>
</td>
</tr>
<tr><td align='left'>bestemmingsplan<br/>
</td>
</tr>
<tr><td align='left'>coördinatieregeling<br/>
</td>
</tr>
<tr><td align='left'>inpassingsplan<br/>
</td>
</tr>
<tr><td align='left'>omgevingsvergunning <br/>
</td>
</tr>
<tr><td align='left'>proactieve aanwijzing<br/>
</td>
</tr>
<tr><td align='left'>reactieve aanwijzing<br/>
</td>
</tr>
<tr><td align='left'>verordening<br/>
</td>
</tr>
<tr><td align='left'>voorbereidingsbesluit<br/>
</td>
</tr>
<tr><td align='left'>zienswijze<br/>
</td>
</tr>
</tbody>
</table>

<b>Instrument_PSV</b><br/>
Definitie: Juridisch instrument binnen de Wro.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
&lt;&lt;CodeList&gt;&gt;<br/>
Instrument_PSV<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>bestuurlijke afspraken (convenanten)<br/>
</td>
</tr>
<tr><td align='left'>coördinatieregeling<br/>
</td>
</tr>
<tr><td align='left'>inpassingsplan<br/>
</td>
</tr>
<tr><td align='left'>omgevingsvergunning <br/>
</td>
</tr>
<tr><td align='left'>proactieve aanwijzing<br/>
</td>
</tr>
<tr><td align='left'>reactieve aanwijzing<br/>
</td>
</tr>
<tr><td align='left'>verordening<br/>
</td>
</tr>
<tr><td align='left'>vooroverleg<br/>
</td>
</tr>
<tr><td align='left'>zienswijze<br/>
</td>
</tr>
</tbody>
</table>

<b>Instrument_RSV</b><br/>
Definitie: Juridisch instrument binnen de Wro.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
&lt;&lt;CodeList&gt;&gt;<br/>
Instrument_RSV<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>amvb<br/>
</td>
</tr>
<tr><td align='left'>beheersverordening<br/>
</td>
</tr>
<tr><td align='left'>bestemmingsplan<br/>
</td>
</tr>
<tr><td align='left'>bestuurlijke afspraken<br/>
</td>
</tr>
<tr><td align='left'>coördinatieregeling<br/>
</td>
</tr>
<tr><td align='left'>inpassingsplan<br/>
</td>
</tr>
<tr><td align='left'>omgevingsvergunning <br/>
</td>
</tr>
<tr><td align='left'>proactieve aanwijzing<br/>
</td>
</tr>
<tr><td align='left'>reactieve aanwijzing<br/>
</td>
</tr>
<tr><td align='left'>verordening<br/>
</td>
</tr>
<tr><td align='left'>voorbereidingsbesluit<br/>
</td>
</tr>
<tr><td align='left'>vooroverleg<br/>
</td>
</tr>
<tr><td align='left'>zienswijze<br/>
</td>
</tr>
</tbody>
</table>

<b>Normadressant_AMB</b><br/>
Definitie: Instantie, overheid of maatschappelijke partij tot welke het in de beleidstekst beschreven aspect zich richt.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
Normadressant_AMB<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>bevoegd gezag<br/>
</td>
</tr>
<tr><td align='left'>burgemeester en wethouders<br/>
</td>
</tr>
<tr><td align='left'>burgers<br/>
</td>
</tr>
<tr><td align='left'>gedeputeerde staten<br/>
</td>
</tr>
<tr><td align='left'>gemeentelijke bestuursorganen<br/>
</td>
</tr>
<tr><td align='left'>gemeenteraad<br/>
</td>
</tr>
<tr><td align='left'>provinciale bestuursorganen<br/>
</td>
</tr>
<tr><td align='left'>provinciale staten<br/>
</td>
</tr>
<tr><td align='left'>regionale bestuursorganen<br/>
</td>
</tr>
<tr><td align='left'>onze Minister<br/>
</td>
</tr>
<tr><td align='left'>onze Minister die het mede aangaat<br/>
</td>
</tr>
<tr><td align='left'>rijksbestuursorganen<br/>
</td>
</tr>
<tr><td align='left'>waterschappen<br/>
</td>
</tr>
<tr><td align='left'>niet nader aangeduid<br/>
</td>
</tr>
</tbody>
</table>

<b>Normadressant_PV</b><br/>
Definitie: Instantie, overheid of maatschappelijke partij tot welke het in de beleidstekst beschreven aspect zich richt.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
Normadressant_PV<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>bevoegd gezag<br/>
</td>
</tr>
<tr><td align='left'>burgemeester en wethouders<br/>
</td>
</tr>
<tr><td align='left'>gedeputeerde staten<br/>
</td>
</tr>
<tr><td align='left'>gemeentelijke bestuursorganen<br/>
</td>
</tr>
<tr><td align='left'>gemeenteraad<br/>
</td>
</tr>
<tr><td align='left'>regionale bestuursorganen<br/>
</td>
</tr>
<tr><td align='left'>niet nader aangeduid<br/>
</td>
</tr>
</tbody>
</table>

<b>Normadressant_XGB</b><br/>
Definitie: Instantie, overheid of maatschappelijke partij tot welke het in de beleidstekst beschreven aspect zich richt.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
Normadressant_XGB<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>bevoegd gezag<br/>
</td>
</tr>
<tr><td align='left'>burgemeester en wethouders<br/>
</td>
</tr>
<tr><td align='left'>burgers<br/>
</td>
</tr>
<tr><td align='left'>gedeputeerde staten<br/>
</td>
</tr>
<tr><td align='left'>gemeentelijke bestuursorganen<br/>
</td>
</tr>
<tr><td align='left'>gemeenteraad<br/>
</td>
</tr>
<tr><td align='left'>provinciale bestuursorganen<br/>
</td>
</tr>
<tr><td align='left'>provinciale staten<br/>
</td>
</tr>
<tr><td align='left'>regionale bestuursorganen <br/>
</td>
</tr>
<tr><td align='left'>rijksbestuursorganen<br/>
</td>
</tr>
<tr><td align='left'>niet nader aangeduid<br/>
</td>
</tr>
</tbody>
</table>

<b>OmvangWaarde</b><br/>
Definitie: Meetbare parameter.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt;enumeration&gt;&gt;<br/>
&lt;&lt;CodeList&gt;&gt;<br/>
OmvangWaarde<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>aantal<br/>
</td>
</tr>
<tr><td align='left'>aantal bedrijven<br/>
</td>
</tr>
<tr><td align='left'>maximum aantal bedrijven<br/>
</td>
</tr>
<tr><td align='left'>minimum aantal bedrijven<br/>
</td>
</tr>
<tr><td align='left'>aantal bezoekers <br/>
</td>
</tr>
<tr><td align='left'>maximum aantal bezoekers<br/>
</td>
</tr>
<tr><td align='left'>minimum aantal bezoekers<br/>
</td>
</tr>
<tr><td align='left'>aantal bouwlagen<br/>
</td>
</tr>
<tr><td align='left'>maximum aantal bouwlagen<br/>
</td>
</tr>
<tr><td align='left'>minimum aantal bouwlagen<br/>
</td>
</tr>
<tr><td align='left'>aantal gebouwen<br/>
</td>
</tr>
<tr><td align='left'>maximum aantal gebouwen<br/>
</td>
</tr>
<tr><td align='left'>minimum aantal gebouwen<br/>
</td>
</tr>
<tr><td align='left'>aantal parkeerplaatsen<br/>
</td>
</tr>
<tr><td align='left'>maximum aantal parkeerplaatsen<br/>
</td>
</tr>
<tr><td align='left'>minimum aantal parkeerplaatsen<br/>
</td>
</tr>
<tr><td align='left'>aantal rijstroken<br/>
</td>
</tr>
<tr><td align='left'>maximum aantal rijstroken<br/>
</td>
</tr>
<tr><td align='left'>minimum aantal rijstroken<br/>
</td>
</tr>
<tr><td align='left'>aantal sporen<br/>
</td>
</tr>
<tr><td align='left'>maximum aantal sporen<br/>
</td>
</tr>
<tr><td align='left'>minimum aantal sporen<br/>
</td>
</tr>
<tr><td align='left'>aantal winkels<br/>
</td>
</tr>
<tr><td align='left'>maximum aantal winkels<br/>
</td>
</tr>
<tr><td align='left'>minimum aantal winkels<br/>
</td>
</tr>
<tr><td align='left'>aantal wooneenheden<br/>
</td>
</tr>
<tr><td align='left'>maximum aantal wooneenheden<br/>
</td>
</tr>
<tr><td align='left'>minimum aantal wooneenheden<br/>
</td>
</tr>
<tr><td align='left'>maatvoering<br/>
</td>
</tr>
<tr><td align='left'>bebouwd oppervlak (m2)<br/>
</td>
</tr>
<tr><td align='left'>maximum bebouwd oppervlak (m2)<br/>
</td>
</tr>
<tr><td align='left'>minimum bebouwd oppervlak (m2)<br/>
</td>
</tr>
<tr><td align='left'>breedte (m)<br/>
</td>
</tr>
<tr><td align='left'>maximum breedte (m)<br/>
</td>
</tr>
<tr><td align='left'>minimum breedte (m)<br/>
</td>
</tr>
<tr><td align='left'>dakhelling (graden)<br/>
</td>
</tr>
<tr><td align='left'>maximum dakhelling (graden)<br/>
</td>
</tr>
<tr><td align='left'>minimum dakhelling (graden)<br/>
</td>
</tr>
<tr><td align='left'>diepte (m)<br/>
</td>
</tr>
<tr><td align='left'>maximum diepte (m)<br/>
</td>
</tr>
<tr><td align='left'>minimum diepte (m)<br/>
</td>
</tr>
<tr><td align='left'>hoogte (m)<br/>
</td>
</tr>
<tr><td align='left'>maximum hoogte (m)<br/>
</td>
</tr>
<tr><td align='left'>minimum hoogte (m)<br/>
</td>
</tr>
<tr><td align='left'>bouwhoogte (m)<br/>
</td>
</tr>
<tr><td align='left'>maximum bouwhoogte (m)<br/>
</td>
</tr>
<tr><td align='left'>minimum bouwhoogte (m)<br/>
</td>
</tr>
<tr><td align='left'>goothoogte (m)<br/>
</td>
</tr>
<tr><td align='left'>maximum goothoogte (m)<br/>
</td>
</tr>
<tr><td align='left'>minimum goothoogte (m)<br/>
</td>
</tr>
<tr><td align='left'>hoogteligging vlak (m)<br/>
</td>
</tr>
<tr><td align='left'>maximum hoogteligging vlak (m)<br/>
</td>
</tr>
<tr><td align='left'>minimum hoogteligging vlak (m)<br/>
</td>
</tr>
<tr><td align='left'>lengte (m)<br/>
</td>
</tr>
<tr><td align='left'>maximum lengte (m)<br/>
</td>
</tr>
<tr><td align='left'>minimum lengte (m)<br/>
</td>
</tr>
<tr><td align='left'>oppervlakte (m2)<br/>
</td>
</tr>
<tr><td align='left'>maximum oppervlakte (m2)<br/>
</td>
</tr>
<tr><td align='left'>minimum oppervlakte (m2)<br/>
</td>
</tr>
<tr><td align='left'>vloeroppervlakte (m2)<br/>
</td>
</tr>
<tr><td align='left'>vloeroppervlakte, bruto (m2)<br/>
</td>
</tr>
<tr><td align='left'>vloeroppervlakte, netto (m2)<br/>
</td>
</tr>
<tr><td align='left'>vloeroppervlakte; bvo (m2)<br/>
</td>
</tr>
<tr><td align='left'>vloeroppervlakte; vvo (m2)<br/>
</td>
</tr>
<tr><td align='left'>maximum vloeroppervlakte (m2)<br/>
</td>
</tr>
<tr><td align='left'>maximum vloeroppervlakte; bruto (m2)<br/>
</td>
</tr>
<tr><td align='left'>maximum vloeroppervlakte; netto (m2)<br/>
</td>
</tr>
<tr><td align='left'>maximum vloeroppervlakte; bvo (m2)<br/>
</td>
</tr>
<tr><td align='left'>maximum vloeroppervlakte; vvo (m2)<br/>
</td>
</tr>
<tr><td align='left'>minimum vloeroppervlakte (m2)<br/>
</td>
</tr>
<tr><td align='left'>minimum vloeroppervlakte; bruto (m2)<br/>
</td>
</tr>
<tr><td align='left'>minimum vloeroppervlakte; netto (m2)<br/>
</td>
</tr>
<tr><td align='left'>minimum vloeroppervlakte; bvo (m2)<br/>
</td>
</tr>
<tr><td align='left'>minimum vloeroppervlakte; vvo (m2)<br/>
</td>
</tr>
<tr><td align='left'>volume (m3)<br/>
</td>
</tr>
<tr><td align='left'>maximum volume (m3)<br/>
</td>
</tr>
<tr><td align='left'>minimum volume (m3)<br/>
</td>
</tr>
<tr><td align='left'>bebouwingspercentage (%)<br/>
</td>
</tr>
<tr><td align='left'>maximum bebouwingspercentage (%)<br/>
</td>
</tr>
<tr><td align='left'>minimum bebouwingspercentage (%)<br/>
</td>
</tr>
<tr><td align='left'>aantal aaneen te bouwen wooneenheden<br/>
</td>
</tr>
<tr><td align='left'>maximum aantal aaneen te bouwen wooneenheden<br/>
</td>
</tr>
<tr><td align='left'>minimum aantal aaneen te bouwen wooneenheden<br/>
</td>
</tr>
<tr><td align='left'>verticale bouwdiepte (m)<br/>
</td>
</tr>
<tr><td align='left'>maximum verticale bouwdiepte (m)<br/>
</td>
</tr>
<tr><td align='left'>minimum verticale bouwdiepte (m)<br/>
</td>
</tr>
</tbody>
</table>

<b>Ondergronden</b><br/>
Definitie: naamgeving van de gebruikte ondergrond bij het instrument.

Opmerking: wanneer niet gebruik is gemaakt van een ondergrond uit het domein dient de naam van de ondergrond ingevuld te worden als vrije tekst.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
&lt;&lt;CodeList&gt;&gt;<br/>
Ondergronden<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>grootschalige basiskaart (GBK)<br/>
</td>
</tr>
<tr><td align='left'>basisregistratie grootschalige topografie (BGT)<br/>
</td>
</tr>
<tr><td align='left'>basisregistratie topografie (BRT)<br/>
</td>
</tr>
<tr><td align='left'>basisregistratie kadaster (BRK)<br/>
</td>
</tr>
</tbody>
</table>

<b>Overheden_BP</b><br/>
Definitie: Administratieve overheid.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt;enumeration&gt;&gt;<br/>
Overheden_BP<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>gemeentelijke overheid<br/>
</td>
</tr>
<tr><td align='left'>deelgemeente/stadsdeel<br/>
</td>
</tr>
<tr><td align='left'>provinciale overheid<br/>
</td>
</tr>
<tr><td align='left'>nationale overheid<br/>
</td>
</tr>
</tbody>
</table>

<b>Overheden_G</b><br/>
Definitie: Administratieve overheid.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
Overheden_G<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>gemeentelijke overheid<br/>
</td>
</tr>
<tr><td align='left'>deelgemeente/stadsdeel<br/>
</td>
</tr>
</tbody>
</table>

<b>Overheden_P</b><br/>
Definitie: Administratieve overheid.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
Overheden_P<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>provinciale overheid<br/>
</td>
</tr>
</tbody>
</table>

<b>Overheden_R</b><br/>
Definitie: Administratieve overheid.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
Overheden_R<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>nationale overheid<br/>
</td>
</tr>
</tbody>
</table>

<b>Overheden_XGB</b><br/>
Definitie: Administratieve overheid.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
Overheden_XGB<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>gemeentelijke overheid<br/>
</td>
</tr>
<tr><td align='left'>deelgemeente/stadsdeel<br/>
</td>
</tr>
<tr><td align='left'>provinciale overheid<br/>
</td>
</tr>
<tr><td align='left'>nationale overheid<br/>
</td>
</tr>
</tbody>
</table>

<b>Planstatus</b><br/>
Definitie: Status van een ruimtelijk plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
Planstatus<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>concept<br/>
</td>
</tr>
<tr><td align='left'>voorontwerp<br/>
</td>
</tr>
<tr><td align='left'>ontwerp<br/>
</td>
</tr>
<tr><td align='left'>vastgesteld<br/>
</td>
</tr>
<tr><td align='left'>geconsolideerd<br/>
</td>
</tr>
</tbody>
</table>

<b>RolExternPlan_AMB</b><br/>
Definitie: Benaming van rol van en relatie met een extern plan of besluit.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
RolExternPlan_AMB<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>als mutatie opgenomen<br/>
</td>
</tr>
<tr><td align='left'>ter vervanging van extern plan/besluit<br/>
</td>
</tr>
<tr><td align='left'>in extern plan/besluit uit te werken<br/>
</td>
</tr>
<tr><td align='left'>informatie in extern plan/besluit<br/>
</td>
</tr>
<tr><td align='left'>ten gevolge van extern plan/besluit<br/>
</td>
</tr>
</tbody>
</table>

<b>RolExternPlan_BP</b><br/>
Definitie: Benaming van rol van en relatie met een extern plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt;enumeration&gt;&gt;<br/>
RolExternPlan_BP<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>als mutatie opgenomen<br/>
</td>
</tr>
<tr><td align='left'>ter vervanging van extern plan<br/>
</td>
</tr>
<tr><td align='left'>ten gevolge van extern plan/besluit<br/>
</td>
</tr>
</tbody>
</table>

<b>RolExternPlanPG_SV</b><br/>
Definitie: Benaming van rol van en relatie met een extern plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
RolExternPlanPG_SV<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>als mutatie opgenomen<br/>
</td>
</tr>
<tr><td align='left'>ter vervanging van extern plan<br/>
</td>
</tr>
<tr><td align='left'>in extern plan/besluit uit te werken<br/>
</td>
</tr>
<tr><td align='left'>in extern plan/besluit uitgewerkt<br/>
</td>
</tr>
<tr><td align='left'>informatie in extern plan/besluit<br/>
</td>
</tr>
<tr><td align='left'>ten gevolge van extern plan/besluit<br/>
</td>
</tr>
</tbody>
</table>

<b>RolExternPlan_PV</b><br/>
Definitie: Benaming van rol van en relatie met een extern plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
RolExternPlan_PV<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>als mutatie opgenomen<br/>
</td>
</tr>
<tr><td align='left'>ter vervanging van extern plan/besluit<br/>
</td>
</tr>
<tr><td align='left'>ten gevolge van extern plan/besluit<br/>
</td>
</tr>
</tbody>
</table>

<b>RolExternPlan_SV</b><br/>
Definitie: Benaming van rol van en relatie met een extern plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
RolExternPlan_SV<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>in extern plan/besluit uit te werken <br/>
</td>
</tr>
<tr><td align='left'>in extern plan/besluit uitgewerkt<br/>
</td>
</tr>
<tr><td align='left'>informatie in extern plan/besluit<br/>
</td>
</tr>
<tr><td align='left'>ten gevolge van extern plan/besluit<br/>
</td>
</tr>
</tbody>
</table>

<b>RolExternPlan_XGB</b><br/>
Definitie: Benaming van rol van en relatie met een extern plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
RolExternPlan_XGB<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>als mutatie opgenomen<br/>
</td>
</tr>
<tr><td align='left'>ter vervanging van extern plan/besluit<br/>
</td>
</tr>
<tr><td align='left'>informatie in extern plan/besluit<br/>
</td>
</tr>
<tr><td align='left'>in extern plan/besluit uit te werken<br/>
</td>
</tr>
<tr><td align='left'>ten gevolge van extern plan/besluit<br/>
</td>
</tr>
</tbody>
</table>

<b>RuimtelijkPlanOfBesluit_AMB</b><br/>
Definitie: Ruimtelijk plan of besluit conform de Wro.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt; enumeration&gt;&gt;<br/>
<b>RuimtelijkPlanOfBesluit_AMB</b><br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>amvb<br/>
</td>
</tr>
<tr><td align='left'>regeling<br/>
</td>
</tr>
</tbody>
</table>

<b>RuimtelijkPlanOfBesluit_BP</b><br/>
Definitie: Ruimtelijk plan of besluit conform de Wro.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt;enumeration&gt;&gt;<br/>
RuimtelijkPlanOfBesluit_BP<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>bestemmingsplan<br/>
</td>
</tr>
<tr><td align='left'>inpassingsplan<br/>
</td>
</tr>
<tr><td align='left'>rijksbestemmingsplan<br/>
</td>
</tr>
<tr><td align='left'>uitwerkingsplan <br/>
</td>
</tr>
<tr><td align='left'>wijzigingsplan <br/>
</td>
</tr>
</tbody>
</table>

<b>RuimtelijkPlanOfBesluit_PV</b><br/>
Definitie: Ruimtelijk plan of besluit conform de Wro.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt; enumeration&gt;&gt;<br/>
RuimtelijkPlanOfBesluit_PV<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>provinciale verordening<br/>
</td>
</tr>
</tbody>
</table>

<b>RuimtelijkPlanOfBesluit_SV</b><br/>
Definitie: Ruimtelijk plan of besluit conform de Wro.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt; enumeration&gt;&gt;<br/>
RuimtelijkPlanOfBesluit_SV<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>structuurvisie<br/>
</td>
</tr>
</tbody>
</table>

<b>RuimtelijkPlanOfBesluit_XGB</b><br/>
Definitie: Ruimtelijk plan of besluit conform de Wro.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt; enumeration&gt;&gt;<br/>
RuimtelijkPlanOfBesluit_XGB<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>aanwijzingsbesluit<br/>
</td>
</tr>
<tr><td align='left'>beheersverordening <br/>
</td>
</tr>
<tr><td align='left'>exploitatieplan<br/>
</td>
</tr>
<tr><td align='left'>gerechtelijke uitspraak<br/>
</td>
</tr>
<tr><td align='left'>omgevingsvergunning<span style='background-color: yellow;'> </span><br/>
</td>
</tr>
<tr><td align='left'>reactieve aanwijzing<br/>
</td>
</tr>
<tr><td align='left'>voorbereidingsbesluit<br/>
</td>
</tr>
</tbody>
</table>

<b>RuimtelijkPlanObject</b><br/>
Definitie: <span style='color: #000000;'>Objecten waar een plangebied uit is samengesteld.</span>

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt; enumeration&gt;&gt;<br/>
RuimtelijkPlanObject<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>bouwaanduiding<br/>
</td>
</tr>
<tr><td align='left'>bouwvlak<br/>
</td>
</tr>
<tr><td align='left'>figuur<br/>
</td>
</tr>
<tr><td align='left'>functieaanduiding<br/>
</td>
</tr>
<tr><td align='left'>gebiedsaanduiding<br/>
</td>
</tr>
<tr><td align='left'>maatvoering<br/>
</td>
</tr>
<tr><td align='left'>besluitsubvlak_A<br/>
</td>
</tr>
<tr><td align='left'>besluitsubvlak_P<br/>
</td>
</tr>
<tr><td align='left'>besluitsubvlak_X<br/>
</td>
</tr>
<tr><td align='left'>besluitvlak_A<br/>
</td>
</tr>
<tr><td align='left'>besluitvlak_P<br/>
</td>
</tr>
<tr><td align='left'>besluitvlak_X<br/>
</td>
</tr>
<tr><td align='left'>dubbelbestemming<br/>
</td>
</tr>
<tr><td align='left'>enkelbestemming<br/>
</td>
</tr>
<tr><td align='left'>structuurvisiecomplex_G<br/>
</td>
</tr>
<tr><td align='left'>structuurvisiecomplex_P<br/>
</td>
</tr>
<tr><td align='left'>structuurvisiecomplex_R<br/>
</td>
</tr>
<tr><td align='left'>structuurvisiegebied_G<br/>
</td>
</tr>
<tr><td align='left'>structuurvisiegebied_P<br/>
</td>
</tr>
<tr><td align='left'>structuurvisiegebied_R<br/>
</td>
</tr>
<tr><td align='left'>structuurvisieverklaring_P<br/>
</td>
</tr>
</tbody>
</table>

<b>TeksttypeBG_AMB</b><br/>
Definitie: Soort tekst of tekstdocument in de context van het ruimtelijke plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt; enumeration&gt;&gt;<br/>
TeksttypeBG_AMB<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>besluitdocument<br/>
</td>
</tr>
<tr><td align='left'>regels<br/>
</td>
</tr>
<tr><td align='left'>toelichting<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij besluitdocument<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij regels<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij toelichting<br/>
</td>
</tr>
</tbody>
</table>

<b>Teksttype_AMB</b><br/>
Definitie: Soort tekst of tekstdocument in de context van het ruimtelijke plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt; enumeration&gt;&gt;<br/>
Teksttype_AMB<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>besluittekst<br/>
</td>
</tr>
<tr><td align='left'>regels<br/>
</td>
</tr>
<tr><td align='left'>toelichting<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij besluittekst<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij regels<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij toelichting<br/>
</td>
</tr>
</tbody>
</table>

<b>TeksttypeBG_PV</b><br/>
Definitie: Soort tekst of tekstdocument in de context van het ruimtelijke plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt; enumeration&gt;&gt;<br/>
TeksttypeBG_PV<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>besluitdocument<br/>
</td>
</tr>
<tr><td align='left'>regels<br/>
</td>
</tr>
<tr><td align='left'>toelichting<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij besluitdocument<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij regels<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij toelichting<br/>
</td>
</tr>
</tbody>
</table>

<b>Teksttype_PV</b><br/>
Definitie: Soort tekst of tekstdocument in de context van het ruimtelijke plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt; enumeration&gt;&gt;<br/>
Teksttype_PV<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>regel zonder voorbereidingsbescherming<br/>
</td>
</tr>
<tr><td align='left'>regel met voorbereidingsbescherming<br/>
</td>
</tr>
<tr><td align='left'>toelichting<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij regel zonder voorbereidingsbescherming<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij regel met voorbereidingsbescherming<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij toelichting<br/>
</td>
</tr>
</tbody>
</table>

<b>TeksttypeBG_XGB</b><br/>
Definitie: Soort tekst of tekstdocument in de context van het ruimtelijke plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt; enumeration&gt;&gt;<br/>
TeksttypeBG_XGB<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>besluitdocument<br/>
</td>
</tr>
<tr><td align='left'>voorschriften/regels<br/>
</td>
</tr>
<tr><td align='left'>toelichting<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij besluitdocument<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij voorschriften/regels<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij toelichting<br/>
</td>
</tr>
</tbody>
</table>

<b>Teksttype_XGB</b><br/>
Definitie: Soort tekst of tekstdocument in de context van het ruimtelijke plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt; enumeration&gt;&gt;<br/>
Teksttype_XGB<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>besluittekst<br/>
</td>
</tr>
<tr><td align='left'>voorschriften/regels<br/>
</td>
</tr>
<tr><td align='left'>toelichting<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij besluittekst<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij voorschriften/regels<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij toelichting<br/>
</td>
</tr>
</tbody>
</table>

<b>TeksttypePG_BP</b><br/>
Definitie: Soort tekst of tekstdocument in de context van het ruimtelijke plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt;enumeration&gt;&gt;<br/>
TeksttypePG_BP<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>regels<br/>
</td>
</tr>
<tr><td align='left'>toelichting<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij regels<br/>
</td>
</tr>
<tr><td align='left'>bijlage bij toelichting<br/>
</td>
</tr>
</tbody>
</table>

<b>Teksttype_BP</b><br/>
Definitie: Soort tekst of tekstdocument in de context van het ruimtelijke plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'>&lt;&lt;enumeration&gt;&gt;<br/>
Teksttype_BP<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>regels<br/>
</td>
</tr>
</tbody>
</table>

<b>TeksttypePG_SV</b><br/>
Definitie: Soort tekst of tekstdocument in de context van het ruimtelijke plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
TeksttypePG_SV<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>document<br/>
</td>
</tr>
<tr><td align='left'>bijlage<br/>
</td>
</tr>
<tr><td align='left'>toelichting<br/>
</td>
</tr>
</tbody>
</table>

<b>Teksttype_SV</b><br/>
Definitie: Soort tekst of tekstdocument in de context van het ruimtelijke plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
Teksttype_SV<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>beleid<br/>
</td>
</tr>
<tr><td align='left'>toelichting<br/>
</td>
</tr>
</tbody>
</table>

<b>Teksttype_PSV</b><br/>
Definitie: Soort tekst of tekstdocument in de context van het ruimtelijke plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
Teksttype_PSV<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>beleid<br/>
</td>
</tr>
<tr><td align='left'>beleid gemandateerd aan GS<br/>
</td>
</tr>
<tr><td align='left'>toelichting<br/>
</td>
</tr>
</tbody>
</table>

<b>TeksttypeV_PSV</b><br/>
Definitie: Soort tekst of tekstdocument in de context van het ruimtelijke plan.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 100%;'>
</colgroup>
<thead valign='top'><tr><th align='center'> &lt;&lt; enumeration&gt;&gt;<br/>
TeksttypeV_PSV<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>toelichting<br/>
</td>
</tr>
</tbody>
</table>

