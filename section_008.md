# OCL Model Constraints {#1B9B615D}

## Waarom constraints? {#7F7DA0E5}

De toepassing van IMRO2012 voor omgevingsinstrumenten is vastgelegd in de praktijkrichtlijnen.<br/>
Bijna alle regels voor het toepassen van IMRO2012 zijn vertaald in het UML-klassediagram IMRO2012 (en vice versa).<br/>
Een aantal regels die expliciet dan wel impliciet in de praktijkrichtlijn staan zijn niet te vertalen naar het UML-klassediagram. Voor het vastleggen van deze regels wordt gebruik gemaakt van ‘constraints’ (beperkingen op het model). De formele taal die daarvoor gebruikt wordt is OCL (Object Constraint Language). Het UML-klassediagram in combinatie met de constraints beschrijft het totaal van de modelinformatie.

## Validatie {#7F7DA0EA}

Een IMRO2012 gecodeerd bestand kan worden gevalideerd op een correcte toepassing van het IMRO2012 model. Het valideren bestaat uit een validatie van het GML bestand (het IMRO2012 uitwisselingsbestand) tegen een XML Schema (IMRO2012 XSD bestand) en een set aan Constraints (Schematron definities).<br/>
Voor de validatie zijn dus drie bestanden van belang:<br/>
<ul><li>GML bestand dat gevalideerd dient te worden;</li>
<li>IMRO2012.XSD bestand (XML Schema Definition bestand);</li>
<li>Schematron definities (business rules).</li>
</ul>

## Format {#7F7DA0F1}

De in dit hoofdstuk opgenomen constraints horen bij het conceptuele niveau van het UML-klassediagram. Voor toepassing op het implementatie niveau van GML (XML) moeten ze vertaald worden naar Schematron.<br/>
Elke constraintregel wordt eerst in woorden beschreven en daarna in OCL (versie 2.0).

De constraints worden toegepast op objectklassen in het UML diagram van IMRO2012. De constraints zijn hierdoor onderdeel van IMRO2012. De overervingsregels uit de objectoriëntatie zijn van toepassing op constraints.

## Constraints {#7F7DA0F7}

De constraints zijn uitgewerkt bij de objectklasse waarop ze van toepassing zijn. Ruimtelijkplan algemeen, bestemmingsplan, structuurvisie, en gebiedsgerichte besluiten.<br/>
De volgende constraints zijn bepaald.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 9.202523090786213%;'
<col id='col2' style='width: 90.7974769092138%;'
</colgroup>
<thead valign='top'><tr><th align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: #000000;' colspan='2'>Ruimtelijk Plan Algemeen

</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>a1</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Minimaal en maximaal 1 object plangebied per bestand</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Plangebied<br/>
inv PlangebiedMax1: Plangebied::allInstances()  size() = 1

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>a2</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Minimaal en maximaal 1 object MetadataImroBestand</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012:: MetadataIMRObestand<br/>
inv MetadataMax1: MetadataIMRObestand::allInstances()  size() = 1

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>a3</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Het attribuut namespace heeft altijd de waarde NL.IMRO</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::NEN3610ID<br/>
inv ObjectNamespace: self.namespace = ‘NL.IMRO’

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>a4</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Maximale lengte van de lokaalID van een plangebied is 23 tekens.</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Plangebied<br/>
inv PlangebiedLokaalIDMaxChar: self.identificatie.NEN3610ID.lokaalID -&gt; size() &lt; 24

toelichting: format = [0-9]{4}\.[A-Za-z0-9]{1,18}

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>a5</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Attribuut versie bestaat verplicht uit 4 alfanumerieke tekens.</b><br/>
<span style='background-color: yellow;'> </span><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Plangebied<br/>
inv PlangebiedVersieAantalEnTypeChar:let allowedChar: Set = Set{'A'..'Z', 'a'..'z', '0'..'9'}<br/>
in self.identificatie.NEN3610ID.versie-&gt;forAll (char | allowedChar-&gt;exists( char ))and

self.identificatie.NEN3610ID.versie -&gt; size() = 4

toelichting: format = [A-Za-z0-9]{4}<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>a7</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Maximale lengte van de lokaalID van een planobject is 32 tekens en toegestane tekens.</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Planobject<br/>
inv PlanobjectLokaalIDMaxCharEnTypeTekens:

let allowedChar: Set = Set{'A'..'Z', 'a'..'z', '0'..'9', '_', '-' '.', ','}<br/>
in self.lokaalID.element-&gt;forAll (char | allowedChar-&gt;exists( char ))

and

self.identificatie.NEN3610ID.lokaalID -&gt; size() &lt; 33

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>a8</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Plangebieden hebben verplicht het attribuut versie in de NEN3610ID</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Plangebied<br/>
inv PlangebiedVersieVerplicht: self.identificatie.NEN3610ID.versie -&gt; notEmpty()

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>a9</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Planobjecten hebben geen versie attribuut in de NEN3610ID</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Planobject<br/>
inv PlanobjectGeenVersie: self.identificatie.NEN3610ID.versie -&gt; isEmpty()

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>a10</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>CBS-code bronhouder verwerkt in identificatiecode.</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Plangebied<br/>
inv PlangebiedIdnCBSCode: self.identificatie.NEN3610ID.lokaalID.substring(1,4) = self.overheidsCode

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>a11</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Coordinaatreferentiesysteem is verplicht Rijksdriehoeksstelsel</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::MetadataIMROBestand<br/>
inv EPSGCode: self.codeReferentiesysteem = ‘28992’

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;' colspan='2'><b>Bestemmingsplan</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Bestemmingsplangebied</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b1</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing naar tekst</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Inv TypeTekstEnBestandsnaamPG_BP:

Context: IMRO2012::Bestemmingsplangebied

def: namespace : String = self.identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = self.identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = self.identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
def: objectgerichteTest: Boolean = self.verwijzingNorm = IMROPT2012<br/>
def: tekstTypeBijlage: Boolean = (self.verwijzingNaarTekstInfo.TekstReferentiePG_BP.typeTekst = TeksttypePG_BP::’bijlage bij toelichting’ or self.verwijzingNaarTekstInfo.TekstReferentiePG_BP.typeTekst = TeksttypePG_BP::’bijlage bij regels’)

and

/* tekst niet objectgericht */<br/>
/* regels */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentiePG_BP.typeTekst = TeksttypePG_BP::regels) and not(objectgerichteTekst) implies

self.verwijzingNaarTekstInfo.TekstReferentiePG_BP.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'r_' + planID

and<br/>
/*toelichting*/<br/>
(self.verwijzingNaarTekstInfo.TekstReferentiePG_BP.typeTekst = TeksttypePG_BP::toelichting) and not(objectgerichteTekst) implies

self.verwijzingNaarTekstInfo.TekstReferentiePG_BP.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 't_' + planID

and<br/>
/* bijlage bij regels */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentiePG_BP.typeTekst = TeksttypePG_BP::'bijlage bij regels') and not(objectgerichteTekst) implies

self.verwijzingNaarTekstInfo.TekstReferentiePG_BP.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* bijlage bij toelichting */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentiePG_BP.typeTekst = TeksttypePG_BP::'bijlage bij toelichting') and not(objectgerichteTekst) implies

self.verwijzingNaarTekstInfo.TekstReferentiePG_BP.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* tekst objectgericht*/<br/>
/* niet tekstTypeBijlage */

(objectgerichteTekst and not(tekstTypeBijlage))<br/>
implies

self.verwijzingNaarTekstInfo.TekstReferentiePG_BP.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID

and<br/>
/* tekst objectgericht*/<br/>
/* tekstTypeBijlage */

(objectgerichteTekst and tekstTypeBijlage)

implies

(self.verwijzingNaarTekstInfo.TekstReferentiePG_BP.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID) or<br/>
(self.verwijzingNaarTekstInfo.TekstReferentiePG_BP.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'b_' + planID)

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b2</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing vaststellingsbesluit</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Inv FormatVerwijzingBesluit:

Context: IMRO2012::Bestemmingsplangebied

def: namespace : String = self.identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = self.identificatie.NEN3610ID.lokaalID<br/>
def: planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
and

self.verwijzingNaarVaststellingsbesluit.substring(1,aantalKarakters + 3) = 'vb_' + planID<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b4</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Attribuut besluitnummer en verwijzingNaarVaststellingsbesluit alleen toegestaan en verplicht indien planstatus vastgesteld </b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Bestemmingsplangebied<br/>
Inv BesluitnummerVerplichtBP:<br/>
if self.planstatusInfo.planstatus = Planstatus::vastgesteld<br/>
 then self.besluitnummer -&gt; notEmpty()and self.verwijzingNaarVaststellingsbesluit -&gt; notEmpty()<br/>
 else self.besluitnummer -&gt; isEmpty()and self.verwijzingNaarVaststellingsbesluit -&gt; isEmpty()<br/>
endif

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>bb1</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Relatie tussen attribuut beleidsmatigVerantwoordelijkeOverheid en attributen naamOverheid en locatieNaam.</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Bestemmingsplangebied<br/>
Inv locatieNaamVerplicht_naamOverheid:

*/gemeente/*<br/>
*/ naamOverheid 1 maal/*<br/>
self. beleidsmatigVerantwoordelijkeOverheid = Overheden_BP:: gemeentelijke overheid implies<br/>
self.naamOverheid -&gt; size() = 1

and<br/>
*/deelgemeente/*<br/>
*/naamOverheid 1 maal*/<br/>
self. beleidsmatigVerantwoordelijkeOverheid = Overheden_BP:: deelgemeente/stadsdeel implies<br/>
self.naamOverheid -&gt; size() = 1

*/provinciale overheid/*<br/>
*/naamOverheid 1 maal, locatieNaam verplicht*/

self. beleidsmatigVerantwoordelijkeOverheid = Overheden_BP:: provinciale overheid implies<br/>
self.naamOverheid -&gt; size() = 1 and self.locatieNaam -&gt; notEmpty()

and<br/>
*/nationale overheid/*<br/>
*/naamOverheid 1 of meer, locatieNaam verplicht*/

self. beleidsmatigVerantwoordelijkeOverheid = Overheden_BP:: nationale overheid<br/>
implies<br/>
self.locatieNaam -&gt; notEmpty()

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>bb2</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Attribuut verwijzingNaarExternPlanInfo verplicht bij uitwerkingsplan, wijzigingsplan.</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Bestemmingsplangebied<br/>
inv ExternPlanInfoVerplicht:<br/>
self.typePlan = RuimtelijkPlanOfBesluit_BP::uitwerkingsplan or<br/>
self.typePlan = RuimtelijkPlanOfBesluit_BP::wijzigingsplan<br/>
implies<br/>
self.verwijzingNaarExternPlanInfo -&gt; notEmpty()

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>bb3</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Indien verwijzingNorm een waarde PRABPK2012 heeft dan is bij maatvoering opname van de symboolcode verplicht en is de symboolcodelijst gesloten.</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Maatvoering<br/>
inv GebruikPRABPK2012:<br/>
def: normen : set = self.plangebied.Bestemmingsplangebied -&gt;collect (verwijzingNorm)<br/>
and

normen -&gt; includes(PRABPK2012)implies<br/>
self.MaatvoeringInfo.symboolcode -&gt; notEmpty()

and<br/>
/* gesloten lijst: de prefix other: mag niet worden gebruikt */<br/>
self.MaatvoeringInfo.symboolcode.substring(1,7) &lt;&gt; ‘other:_’<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Bestemmingsvlak</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b7</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing naar tekst</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Bestemmingsvlak

Inv TypeTekstEnBestandsnaamBP:<br/>
def: namespace : String = self.identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = self.identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = self.identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
def: objectgerichteTekst: Boolean = self.plangebied.BestemmingsplanGebied.verwijzingNorm = IMROPT2012

and<br/>
/* niet objectgerichte tekst*/

/* regels html*/<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_BP.typeTekst = Teksttype_BP::regels) and not(objectgerichteTekst) implies

self.verwijzingNaarTekstInfo.TekstReferentie_BP.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'r_' + planID

and<br/>
/*objectgericht*/<br/>
objectgerichteTekst implies

self.verwijzingNaarTekstInfo.TekstReferentie_BP.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = ‘pt_’ + planID

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b9</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Een Enkelbestemming kent andere hoofdgroepen dan een Dubbelbestemming</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Enkelbestemming<br/>
inv EnkelHoofdgroep: self.bestemmingshoofdgroep &lt;&gt; Bestemminghoofdgroep_ED::leiding and<br/>
self.bestemmingshoofdgroep &lt;&gt; Bestemminghoofdgroep_ED::waarde and<br/>
self.bestemmingshoofdgroep &lt;&gt; Bestemminghoofdgroep_ED::waterstaat

context IMRO2012::Dubbelbestemming<br/>
inv DubbelHoofdgroep: self.bestemmingshoofdgroep = Bestemminghoofdgroep_ED::leiding or<br/>
self.bestemmingshoofdgroep = Bestemminghoofdgroep_ED::waarde or<br/>
self.bestemmingshoofdgroep = Bestemminghoofdgroep_ED::waterstaat

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b10</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Bestemmingsvlak verwijst naar een bestaand plangebied id</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Geen OCL constraint

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b11</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Aanduiding verwijst naar een bestaand plangebied id</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Geen OCL constraint

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b12</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Aanduiding verwijst naar een bestaand bestemmingsvlak id</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Geen OCL constraint

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b13</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Bouwvlak verwijst altijd naar een bestemmingsvlak maar is optioneel</b><b> bij plantype wijzigingsplan, inpassingsplan of indien het dient ter vervanging van een extern plan.</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Bouwvlak

inv AssociatieBouwvlakBestvlak:<br/>
def: terVervangingExternPlanInfo: Boolean = (self.plangebied.BestemmingsplanGebied. verwijzingNaarExternPlanInfo.rolExternPlan_BP = RolExternPlan_BP::ter vervanging van extern plan)

and<br/>
(self.plangebied.Bestemmingsplangebied.typePlan &lt;&gt; RuimtelijkPlanOfBesluit_BP::wijzigingsplan and<br/>
self.plangebied.Bestemmingsplangebied.typePlan &lt;&gt; RuimtelijkPlanOfBesluit_BP::inpassingsplan and not terVervangingExternPlanInfo) implies self.bestemmingsvlak -&gt; notEmpty()

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b14</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Naam bouwvlak is altijd bouwvlak</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2013::Bouwvlak<br/>
inv Bouwvlaknaam: self.naam = ‘bouwvlak’

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b15</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Functieaanduiding kan niet verwijzen naar aanduiding van het type bouwvlak, functieaanduiding, bouwaanduiding, maatvoering, figuur.</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Functieaanduiding<br/>
inv AssociatieFunctieaanduidingNiet:<br/>
not(self.aanduiding.oclIsTypeOf(Bouwvlak))<br/>
and<br/>
not(self.aanduiding.oclIsTypeOf(Functieaanduiding))<br/>
and<br/>
not(self.aanduiding.oclIsTypeOf(Bouwaanduiding))<br/>
and<br/>
not(self.aanduiding.oclIsTypeOf(Maatvoering))<br/>
and<br/>
not(self.aanduiding.oclIsTypeOf(Figuur)

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b16</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Bouwaanduiding kan niet verwijzen naar aanduiding van het type functieaanduiding, bouwaanduiding, maatvoering, figuur</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Bouwaanduiding<br/>
inv AssociatieBouwaanduidingNiet:<br/>
not(self.aanduiding.oclIsTypeOf(Functieaanduiding))<br/>
and<br/>
not(self.aanduiding.oclIsTypeOf(Bouwaanduiding))<br/>
and<br/>
not(self.aanduiding.oclIsTypeOf(Maatvoering))<br/>
and<br/>
not(self.aanduiding.oclIsTypeOf(Figuur)

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b17</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Maatvoering kan niet verwijzen naar aanduiding van het type functieaanduiding, bouwaanduiding, maatvoering, figuur</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Maatvoering<br/>
inv AssociatieMaatvoeringNiet:<br/>
not(self.aanduiding.oclIsTypeOf(Functieaanduiding))<br/>
and<br/>
not(self.aanduiding.oclIsTypeOf(Bouwaanduiding))<br/>
and<br/>
not(self.aanduiding.oclIsTypeOf(Maatvoering))<br/>
and<br/>
not(self.aanduiding.oclIsTypeOf(Figuur)

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b18</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Figuur kan niet verwijzen naar aanduiding van het type functieaanduiding, bouwaanduiding, maatvoering, figuur</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Figuur<br/>
inv AssociatieFiguurNiet:<br/>
not(self.aanduiding.oclIsTypeOf(Functieaanduiding))<br/>
and<br/>
not(self.aanduiding.oclIsTypeOf(Bouwaanduiding))<br/>
and<br/>
not(self.aanduiding.oclIsTypeOf(Maatvoering))<br/>
and<br/>
not(self.aanduiding.oclIsTypeOf(Figuur)

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b19</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Functieaanduiding verwijst altijd naar een bestemmingsvlak of een gebiedsaanduiding maar is optioneel</b><b> bij plantype wijzigingsplan en inpassingsplan of indien het dient ter vervanging van een extern plan.</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Functieaanduiding<br/>
inv FunctieaanduidingVoorBestOfAanduiding:<br/>
def: terVervangingExternPlanInfo: Boolean = (self.plangebied.BestemmingsplanGebied. verwijzingNaarExternPlanInfo.rolExternPlan_BP = RolExternPlan_BP::ter vervanging van extern plan)

and

if<br/>
(self.plangebied.Bestemmingsplangebied.typePlan &lt;&gt; RuimtelijkPlanOfBesluit_BP::wijzigingsplan and<br/>
self.plangebied.Bestemmingsplangebied.typePlan &lt;&gt; RuimtelijkPlanOfBesluit_BP::inpassingsplan and not terVervangingExternPlanInfo) then

not (self.aanduiding.oclIsTypeOf(Gebiedsaanduiding) and self.bestemmingsvlak -&gt; notEmpty())<br/>
and<br/>
not (self.aanduiding -&gt; isEmpty() and self.bestemmingsvlak -&gt; isEmpty())<br/>
else<br/>
not (self.aanduiding.oclIsTypeOf(Gebiedsaanduiding) and self.bestemmingsvlak -&gt; notEmpty())

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b20</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Bouwaanduiding verwijst altijd naar een bestemmingsvlak, bouwvlak of een gebiedsaanduiding maar is optioneel</b><b> bij plantype wijzigingsplan en inpassingsplan of indien het dient ter vervanging van een extern plan .</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Bouwaanduiding<br/>
inv BouwaanduidingVoorBestOfAanduiding:<br/>
def: terVervangingExternPlanInfo: Boolean = (self.plangebied.BestemmingsplanGebied. verwijzingNaarExternPlanInfo.rolExternPlan_BP = RolExternPlan_BP::ter vervanging van extern plan)

and

if<br/>
(self.plangebied.Bestemmingsplangebied.typePlan &lt;&gt; RuimtelijkPlanOfBesluit_BP::wijzigingsplan and<br/>
self.plangebied.Bestemmingsplangebied.typePlan &lt;&gt; RuimtelijkPlanOfBesluit_BP::inpassingsplan and not terVervangingExternPlanInfo) then

not (((self.aanduiding.oclIsTypeOf(Bouwvlak) or self.aanduiding.oclIsTypeOf(Gebiedsaanduiding)) and self.bestemmingsvlak -&gt; notEmpty()))<br/>
and<br/>
not (self.aanduiding -&gt; isEmpty() and self.bestemmingsvlak -&gt; isEmpty())<br/>
else<br/>
not (((self.aanduiding.oclIsTypeOf(Bouwvlak) or self.aanduiding.oclIsTypeOf(Gebiedsaanduiding)) and self.bestemmingsvlak -&gt; notEmpty()))

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b21</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Maatvoering verwijst altijd naar een bestemmingsvlak , een bouwvlak of een gebiedsaanduiding maar is optioneel</b><b> bij plantype wijzigingsplan en inpassingsplan of indien het dient ter vervanging van een extern plan..</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Maatvoering<br/>
inv MaatvoeringVoorBestOfAanduiding:<br/>
def: terVervangingExternPlanInfo: Boolean = (self.plangebied.BestemmingsplanGebied. verwijzingNaarExternPlanInfo.rolExternPlan_BP = RolExternPlan_BP::ter vervanging van extern plan)

and

if<br/>
(self.plangebied.Bestemmingsplangebied.typePlan &lt;&gt; RuimtelijkPlanOfBesluit_BP::wijzigingsplan and<br/>
self.plangebied.Bestemmingsplangebied.typePlan &lt;&gt; RuimtelijkPlanOfBesluit_BP::inpassingsplan and not terVervangingExternPlanInfo) then

not (((self.aanduiding.oclIsTypeOf(Bouwvlak) or self.aanduiding.oclIsTypeOf(Gebiedsaanduiding)) and self.bestemmingsvlak -&gt; notEmpty()))<br/>
and<br/>
not (self.aanduiding -&gt; isEmpty() and self.bestemmingsvlak -&gt; isEmpty())<br/>
else<br/>
not (((self.aanduiding.oclIsTypeOf(Bouwvlak) or self.aanduiding.oclIsTypeOf(Gebiedsaanduiding)) and self.bestemmingsvlak -&gt; notEmpty()))

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b22</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Figuur verwijst altijd naar een bestemmingsvlak of een bouwvlak of een gebiedsaanduiding maar is optioneel</b><b> bij plantype wijzigingsplan en inpassingsplan of indien het dient ter vervanging van een extern plan.</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Figuur<br/>
inv FiguurVoorBestOfAanduiding:<br/>
def: terVervangingExternPlanInfo: Boolean = (self.plangebied.BestemmingsplanGebied. verwijzingNaarExternPlanInfo.rolExternPlan_BP = RolExternPlan_BP::ter vervanging van extern plan)

and

if<br/>
(self.plangebied.Bestemmingsplangebied.typePlan &lt;&gt; RuimtelijkPlanOfBesluit_BP::wijzigingsplan and<br/>
self.plangebied.Bestemmingsplangebied.typePlan &lt;&gt; RuimtelijkPlanOfBesluit_BP::inpassingsplan and not terVervangingExternPlanInfo) then

(not (self.aanduiding -&gt; notEmpty() and self.bestemmingsvlak -&gt; notEmpty()))<br/>
and<br/>
(not (self.aanduiding -&gt; isEmpty() and self.bestemmingsvlak -&gt; isEmpty()))<br/>
and<br/>
(self.aanduiding.oclIsTypeOf(Bouwvlak) or self.aanduiding.oclIsTypeOf(Gebiedsaanduiding) or self.aanduiding -&gt; isEmpty())<br/>
else<br/>
(self.aanduiding.oclIsTypeOf(Bouwvlak) or self.aanduiding.oclIsTypeOf(Gebiedsaanduiding) or self.aanduiding -&gt; isEmpty())

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b23</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format illustratie verwijzing</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Figuur<br/>
Inv Illustratieverwijzing:

def: namespace : String = self.identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = self.identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = self.identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
and

/* illustratie */

self.verwijzingNaarTekstInfo.IllustratieReferentie_BP.verwijzingNaarIllustratie.substring(1,aantalKarakters + 2) = 'i_' + planID<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b24</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Alle aanduidingen, behalve het object Figuur, kunnen maximaal naar 1 bestemmingsvlak verwijzen.</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Aanduiding<br/>
inv verwijzingNaarBestemming:<br/>
not(self.oclIsTypeOf(Figuur)) implies<br/>
self.bestemmingsvlak-&gt;size()&lt; 2

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Gebiedsaanduiding</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>b26</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing naar tekst bij, functieaanduiding, bouwaanduiding, maatvoering, figuur en gebiedsaanduiding.</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Functieaanduiding<br/>
context IMRO2012::Bouwaanduiding<br/>
context IMRO2012::Maatvoering<br/>
context IMRO2012::Figuur<br/>
context IMRO2012::Gebiedsaanduiding

Inv TypeTekstEnBestandsnaamGebiedsaanduiding:<br/>
def: namespace : String = self.identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = self.identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = self.identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
def: objectgerichteTekst: Boolean = self.plangebied.BestemmingsplanGebied.verwijzingNorm = IMROPT2012

and

/* regels */

not(objectgerichteTekst) implies<br/>
self.verwijzingNaarTekstInfo.TekstReferentie_BP.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'r_' + planID

and<br/>
objectgerichteTekst implies<br/>
self.verwijzingNaarTekstInfo.TekstReferentie_BP.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = ‘pt_’ + planID

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;' colspan='2'><b>Structuurvisie</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Structuurvisieplangebied</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>c2</b>

</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing naar tekst</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>voor _G _ P en _R gelijk.</b>

Context: IMRO2012::Structuurvisieplangebied_G<br/>
Context: IMRO2012::Structuurvisieplangebied_P<br/>
Context: IMRO2012::Structuurvisieplangebied_R

Inv TypeTekstEnBestandsnaamPG_SV:

def: namespace : String = identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
def: objectgerichteTekst: Boolean = self.verwijzingNorm = IMROPT2012<br/>
def: tekstTypeBijlage: Boolean = self.verwijzingNaarTekstInfo.TekstReferentiePG_SV.typeTekst = TeksttypePG_SV::bijlage

and<br/>
/* tekst niet objectgericht */<br/>
/* document */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentiePG_SV.typeTekst = TeksttypePG_SV::document and not(objectgerichteTekst) implies

self.verwijzingNaarTekstInfo.TekstReferentiePG_SV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'd_' + planID

and<br/>
/* bijlages */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentiePG_SV.typeTekst = TeksttypePG_SV::bijlage and not(objectgerichteTekst) implies

self.verwijzingNaarTekstInfo.TekstReferentiePG_SV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* toelichting */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentiePG_SV.typeTekst = TeksttypePG_SV::toelichting and not(objectgerichteTekst) implies

self.verwijzingNaarTekstInfo.TekstReferentiePG_SV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* tekst objectgericht*/<br/>
/* niet tekstTypeBijlage */<br/>
(objectgerichteTekst and not(tekstTypeBijlage))<br/>
implies

self.verwijzingNaarTekstInfo.TekstReferentiePG_SV.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID

/* tekst objectgericht*/<br/>
/*bijlage*/<br/>
(objectgerichteTekst and tekstTypeBijlage) implies

(self.verwijzingNaarTekstInfo.TekstReferentiePG_SV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID) or

(self.verwijzingNaarTekstInfo.TekstReferentiePG_SV.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID)

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>c3</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing vaststellingsbesluit</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>voor _G _ P en _R gelijk.</b>

Context: IMRO2012::Structuurvisieplangebied_G<br/>
Context: IMRO2012::Structuurvisieplangebied_P<br/>
Context: IMRO2012::Structuurvisieplangebied_R

<b>rest is gelijk aan bestemmingsplangebied</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>c4</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing naar illustratie</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>voor _G _ P en _R gelijk.</b>

Context: IMRO2012::Structuurvisieplangebied_G<br/>
Context: IMRO2012::Structuurvisieplangebied_P<br/>
Context: IMRO2012::Structuurvisieplangebied_R

Inv Illustratieverwijzing:

def: namespace : String = self.identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = self.identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = self.identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
and

/* illustratie */<br/>
self.verwijzingNaarTekstInfo.IllustratieReferentiePG.verwijzingNaarIllustratie.substring(1,aantalKarakters + 2) = 'i_' + planID<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>c5</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Attribuut besluitnummer en verwijzingNaarVaststellingsbesluit alleen toegestaan en verplicht indien planstatus = vastgesteld</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Structuurvisieplangebied_G<br/>
Inv BesluitnummerVerplichtGSV:<br/>
if self.PlanstatusEnDatum.planstatus = Planstatus::vastgesteld<br/>
 then self.besluitnummer -&gt; notEmpty()and self.verwijzingNaarVaststellingsbesluit -&gt; notEmpty()<br/>
 else self.besluitnummer -&gt; isEmpty()and self.verwijzingNaarVaststellingsbesluit -&gt; isEmpty()<br/>
endif

Context: IMRO2012::Structuurvisieplangebied_P<br/>
Inv BesluitnummerVerplichtPSV:<br/>
if self.planstatusInfo.planstatus = Planstatus::vastgesteld<br/>
 then self.besluitnummer -&gt; notEmpty()and self.verwijzingNaarVaststellingsbesluit -&gt; notEmpty()<br/>
 else self.besluitnummer -&gt; isEmpty()and self.verwijzingNaarVaststellingsbesluit -&gt; isEmpty()<br/>
endif

Context: IMRO2012::Structuurvisieplangebied_R<br/>
Inv BesluitnummerVerplichtRSV:<br/>
if self.planstatusInfo.planstatus = Planstatus::vastgesteld<br/>
 then self.besluitnummer -&gt; notEmpty()and self.verwijzingNaarVaststellingsbesluit -&gt; notEmpty()<br/>
 else self.besluitnummer -&gt; isEmpty()and self.verwijzingNaarVaststellingsbesluit -&gt; isEmpty()<br/>
endif

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Structuurvisiegebieden en complexen</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>c7</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing naar tekst</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>verschillend voor _G _P en _R</b>

<b>_G</b><br/>
<b>gebied_G, complex_G</b><br/>
Context: IMRO2012::Structuurvisiegebied_G<br/>
Context: IMRO2012::Structuurvisiecomplex_G

Inv TypeTekstEnBestandsnaam_SV:

def: namespace : String = identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
def: objectgerichteTest: Boolean = self.verwijzingNorm = IMROPT2012

and<br/>
/* tekst niet objectgericht */<br/>
/* beleid */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_SV.typeTekst = Teksttype_SV::document and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_SV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'd_' + planID

and<br/>
/* toelichting */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_SV.typeTekst = Teksttype_SV::toelichting and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_SV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 't_' + planID

and<br/>
/* tekst objectgericht*/<br/>
objectgerichteTekst implies

self.verwijzingNaarTekstInfo.TekstReferentie_SV.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID

<b>_P</b><br/>
<b>gebied_P en complex_P</b><br/>
Context: IMRO2012:: Structuurvisiegebied_P<br/>
Context: IMRO2012:: Structuurvisiecomplex_P

Inv TypeTekstEnBestandsnaam_PSV:

def: namespace : String = identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
def: objectgerichteTest: Boolean = self.verwijzingNorm = IMROPT2012

and<br/>
/* tekst niet objectgericht */<br/>
/* beleid */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_PSV.typeTekst = Teksttype_PSV::document and not(objectgerichteTekst))implies

self.verwijzingNaarTekstInfo.TekstReferentie_PSV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'd_' + planID

and<br/>
/* toelichting */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_PSV.typeTekst = Teksttype_PSV::toelichting and not(objectgerichteTekst))implies

self.verwijzingNaarTekstInfo.TekstReferentie_PSV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 't_' + planID

and<br/>
/* beleid gemandateerd aan GS */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_PSV.typeTekst = Teksttype_PSV::'beleid gemandateerd aan GS' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_PSV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'd_' + planID

and<br/>
/* tekst objectgericht*/<br/>
objectgerichteTekst implies

self.verwijzingNaarTekstInfo.TekstReferentie_PSV.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID

<b>verklaring_P</b><br/>
Context: IMRO2012::Structuurvisieverklaring_P<br/>
Inv TypeTekstEnBestandsnaamV_PSV:

def: namespace : String = identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
def: objectgerichteTest: Boolean = self.verwijzingNorm = IMROPT2012

and<br/>
/* tekst niet objectgericht */<br/>
/* toelichting */

not(objectgerichteTekst) implies<br/>
self.verwijzingNaarTekstInfo.TekstReferentieV_PSV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 't_' + planID

and<br/>
/* tekst objectgericht*/<br/>
objectgerichteTekst implies

self.verwijzingNaarTekstInfo.TekstReferentieV_PSV.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID

<b>_R</b><br/>
Context: IMRO2012:: Structuurvisiegebied_R<br/>
Context: IMRO2012:: Structuurvisiecomplex_R

<b>gebied_R gelijk aan complex_R gelijk aan gebied_G</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>c8</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing naar illustratie</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>voor _G en _R gelijk.</b>

gebied_G, complex_G, gebied_R, complex_R

context IMRO2012::Structuurvisiegebied_G<br/>
context IMRO2012::Structuurvisiecomplex_G<br/>
context IMRO2012::Structuurvisiegebied_R<br/>
context IMRO2012::Structuurvisiecompex_R

Inv Illustratieverwijzing:

def: namespace : String = self.identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = self.identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = self.identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
and

/* illustratie */<br/>
self.verwijzingNaarTekstInfo.IllustratieReferentie.verwijzingNaarIllustratie.substring(1,aantalKarakters + 2) = 'i_' + planID

Voor _P<br/>
gebied_P, complex_P, verklaring_P<br/>
context IMRO2012::Structuurvisiegebied_P<br/>
context IMRO2012::Structuurvisiecomplex_P<br/>
context IMRO2012::Structuurvisieverklaring_P

Inv Illustratieverwijzing:

def: namespace : String = self.identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = self.identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = self.identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
and

/* illustratie */<br/>
self.verwijzingNaarTekstInfo.IllustratieReferentie_PSV.verwijzingNaarIllustratie.substring(1,aantalKarakters + 2) = 'i_' + planID

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Algemene test regels voor verwijzingen</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>c9</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Structuurvisiegebied verwijst naar een bestaand plangebied id</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Geen OCL constraint

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>c10</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Structuurvisiecomplex verwijst naar een bestaand plangebied id</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Geen OCL constraint

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>c11</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Structuurvisieverklaring verwijst naar een bestaand plangebied id</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Geen OCL constraint

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>c12</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Structuurvisiecomplex verwijst naar een bestaand planobject id</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Geen OCL constraint

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>c13</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Structuurvisiegebied_R en Structuurvisiecomplex_R</b><br/>
<b>Het object heeft verplicht een geometrie indien het object naar een kaart illustratie verwijst.</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Structuurvisiegebied_R<br/>
Context: IMRO2012::Structuurvisiecomplex_R<br/>
Inv GeometrieVerplichtGebiedRSV:<br/>
self.verwijzingNaarIllustratieInfo.IllustratieReferentie.typeIllustratie = Illustratie::kaart implies<br/>
self.begrenzing -&gt; notEmpty()

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>c14</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>CartografieInfo, indien gebruikt is er altijd een kaart met nummer 1. Nummer 0 mag niet voorkomen. Het nummer is altijd een positief, geheel getal.</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>/* geldt voor het datatype CartografieInfo. Wordt gebruikt bij:<br/>
Structuurvisiegebied_G,<br/>
Structuurvisiecomplex_G,<br/>
Structuurvisiegebied_P,<br/>
Structuurvisiecomplex_P,<br/>
Structuurvisieverklaring_P,<br/>
Structuurvisiegebied_R,<br/>
Structuurvisiecomplex_R,<br/>
Besluitvlak_P,<br/>
Belsluitsubvlak_P,<br/>
Besluitvlak_A,<br/>
Besluitsubvlak_A. */

context CartografieInfo

Inv altijdEenKaartnummer1:<br/>
def: kaartnummers : set = self-&gt;collect (kaartnummer)<br/>
and<br/>
(kaartnummers -&gt; includes(1) and not(kaartnummers -&gt; includes(0))<br/>
and<br/>
self.kaartnummer.oclIsTypeOf(Integer)<br/>
and<br/>
/* niet negatief */<br/>
self.kaartnummer = self.kaartnummer.abs()

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;' colspan='2'><b>Gebiedsgerichte besluiten</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Provinciale Verordening</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e2</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing naar tekst</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Besluitgebied_P

Inv TypeTekstEnBestandsnaamBG_PV:

def: namespace : String = identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
def: objectgerichteTest: Boolean = self.verwijzingNorm = IMROPT2012<br/>
def: tekstTypeBijlage: Boolean = (self.verwijzingNaarTekstInfo.TekstReferentieBG_PV.typeTekst = TeksttypeBG_PV::'bijlage bij regels' or<br/>
verwijzingNaarTekstInfo.TekstReferentieBG_PV.typeTekst = TeksttypeBG_PV::'bijlage bij toelichting' or<br/>
self.verwijzingNaarTekstInfo.TekstReferentieBG_PV.typeTekst = TeksttypeBG_PV::'bijlage bij besluitdocument')

and<br/>
/* tekst niet objectgericht */<br/>
/* besluitdocument */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_PV.typeTekst = TeksttypeBG_PV::besluitdocument and not(objectgerichteTekst))implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_PV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'd_' + planID

and<br/>
/* regels */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_PV.typeTekst = TeksttypeBG_PV::regels and not(objectgerichteTekst))implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_PV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'r_' + planID

and<br/>
/*toelichting */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_PV.typeTekst = TeksttypeBG_PV::toelichting and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_PV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 't_' + planID

and<br/>
/* bijlage bij regels */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_PV.typeTekst = TeksttypeBG_PV::'bijlage bij regels' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_PV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* bijlage bij toelichting */<br/>
(verwijzingNaarTekstInfo.TekstReferentieBG_PV.typeTekst = TeksttypeBG_PV::'bijlage bij toelichting' and not(objectgerichteTekst))implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_PV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* bijlage bij besluitdocument */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_PV.typeTekst = TeksttypeBG_PV::'bijlage bij besluitdocument' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_PV. verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* tekst objectgericht*/<br/>
/* niet tekstTypeBijlage */<br/>
(objectgerichteTekst and not(tekstTypeBijlage)) implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_PV.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID

/* tekst objectgericht */<br/>
/* tekstTypeBijlage */<br/>
(objectgerichteTekst and tekstTypeBijlage) implies

(self.verwijzingNaarTekstInfo.TekstReferentieBG_PV.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'b_' + planID) or<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_PV.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID)

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e3</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing vaststellingsbesluit</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Besluitgebied_P<br/>
Context: IMRO2012::Besluitgebied_A<br/>
Context: IMRO2012::Besluitgebied_X

<b>rest is gelijk aan bestemmingsplangebied</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e4</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing naar illustratie</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Besluitgebied_P <br/>
Inv Illustratieverwijzing:

def: namespace : String = self.identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = self.identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = self.identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
and

/* illustratie */<br/>
self.verwijzingNaarTekstInfo.IllustratieReferentiePG.verwijzingNaarIllustratie.substring(1,aantalKarakters + 2) = 'i_' + planID

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e5</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Attribuut besluitnummer en verwijzingNaarVaststellingsbesluit alleen toegestaan en verplicht indien planstatus = vastgesteld</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Besluitgebied_P<br/>
Inv BesluitnummerVerplichtPV:<br/>
if self.planstatusInfo.planstatus = Planstatus::vastgesteld<br/>
 then self.besluitnummer -&gt; notEmpty()and self.verwijzingNaarVaststellingsbesluit -&gt; notEmpty()<br/>
 else self.besluitnummer -&gt; isEmpty()and self.verwijzingNaarVaststellingsbesluit -&gt; isEmpty()<br/>
endif

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e6</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Attribuut locatieNaam is verplicht indien attribuut beleidsmatigVerantwoordelijkeOverheid = proviciale - of nationale overheid</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Besluitgebied_P<br/>
Inv LocatienaamVerplichtP:<br/>
self.beleidsmatigVerantwoordelijkeOverheid = Overheden_P::provinciale overheid or<br/>
self.beleidsmatigVerantwoordelijkeOverheid = Overheden_P::nationale overheid<br/>
implies

self.locatieNaam -&gt; notEmpty()

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Besluitvlak_P</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e7</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing naar tekst</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Besluitvlak_P

Inv TypeTekstEnBestandsnaam_PV:

def: namespace : String = identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
def: objectgerichteTekst: Boolean = self.verwijzingNorm = IMROPT2012<br/>
def: tekstTypeBijlage: Boolean = (self.verwijzingNaarTekstInfo.TekstReferentie_PV.typeTekst = Teksttype_PV::'bijlage bij regel met voorbereidingsbescherming' or self.verwijzingNaarTekstInfo.TekstReferentie_PV.typeTekst = Teksttype_PV::'bijlage bij regel zonder voorbereidingsbescherming' or<br/>
self.verwijzingNaarTekstInfo.TekstReferentie_PV.typeTekst = Teksttype_PV::'bijlage bij toelichting’)

and<br/>
/* tekst niet objectgericht */

/* regel zonder voorbereidingsbescherming */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_PV.typeTekst = Teksttype_PV::'regel zonder voorbereidingsbescherming' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_PV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'r_' + planID

and<br/>
/* regel met voorbereidingsbescherming */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_PV.typeTekst = Teksttype_PV::'regel met voorbereidingsbescherming' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_PV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'r_' + planID

and<br/>
/*toelichting */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_PV.typeTekst = Teksttype_PV::toelichting and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_PV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 't_' + planID

and<br/>
/* bijlage bij regel zonder voorbereidingsbescherming */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_PV.typeTekst = Teksttype_PV::'bijlage bij regel zonder voorbereidingsbescherming' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_PV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* bijlage regel met voorbereidingsbescherming */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_PV.typeTekst = Teksttype_PV::'bijlage bij regel met voorbereidingsbescherming' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_PV.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* bijlage bij toelichting */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_PV.typeTekst = Teksttype_PV::'bijlage bij toelichting' and not(objectgerichteTekst)) implies

verwijzingNaarTekstInfo.TekstReferentie_PV.verwijzingTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* tekst objectgericht*/<br/>
/* niet tekstTypeBijlage */<br/>
(objectgerichteTekst and (bijlage))<br/>
implies

self.verwijzingNaarTekstInfo.TekstReferentie_PV.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID

and<br/>
/* tekst objectgericht*/<br/>
/* tekstTypeBijlage */<br/>
(objectgerichteTekst and tekstTypeBijlage) implies<br/>
verwijzingNaarTekstInfo.TekstReferentie_PV.verwijzingTekst.substring(1,aantalKarakters + 2) = 'b_' + planID) or

(self.verwijzingNaarTekstInfo.TekstReferentie_PV.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID)

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e8</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format illustratieverwijzing</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>gelijk aan structuurvisiegebied_G

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Besluitsubvlak_P</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e9</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing naar tekst</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Besluitsubvlak_P

<b>rest is gelijk aan Besluitvlak_P</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e10</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format illustratieverwijzing</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Besluitsubvlak_P

<b>rest is gelijk aan aan structuurvisiegebied_G</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>AMvB</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e11</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing naar tekst</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context: Besluitgebied_A<br/>
Inv TypeTekstEnBestandsnaamBG_AMB:

def: namespace : String = identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
def: objectgerichteTest: Boolean = self.verwijzingNorm = IMROPT2012<br/>
def: tekstTypeBijlage: Boolean = (self.verwijzingNaarTekstInfo.TekstReferentieBG_AMB.typeTekst = TeksttypeBG_AMB::'bijlage bij regels' or verwijzingNaarTekstInfo.TekstReferentieBG_AMB.typeTekst = TeksttypeBG_AMB::'bijlage bij toelichting' or<br/>
self.verwijzingNaarTekstInfo.TekstReferentieBG_AMB.typeTekst = TeksttypeBG_AMB::'bijlage bij besluitdocument')

and<br/>
/* tekst niet objectgericht */

/* besluitdocument */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_AMB.typeTekst = TeksttypeBG_AMB::besluitdocument and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'd_' + planID

and<br/>
/* regels */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_AMB.typeTekst = TeksttypeBG_AMB::regels and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'r_' + planID

and<br/>
/*toelichting */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_AMB.typeTekst = TeksttypeBG_AMB_BP::toelichting and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 't_' + planID

and<br/>
/* bijlage bij regels */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_AMB.typeTekst = TeksttypeBG_AMB::'bijlage bij regels' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* bijlage bij toelichting */<br/>
(verwijzingNaarTekstInfo.TekstReferentieBG_AMB.typeTekst = TeksttypeBG_AMB::'bijlage bij toelichting' and not(objectgerichteTekst)) implies

verwijzingNaarTekstInfo.TekstReferentieBG_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* bijlage bij besluitdocument */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_AMB.typeTekst = TeksttypeBG_AMB::'bijlage bij besluitdocument' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* tekst objectgericht*/<br/>
/* niet tekstTypeBijlage */<br/>
(objectgerichteTekst and not(tekstTypeBijlage)) implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID

/* tekst objectgericht*/<br/>
/* tekstTypeBijlage */<br/>
(objectgerichteTekst and tekstTypeBijlage) implies

(self.verwijzingNaarTekstInfo.TekstReferentieBG_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID)

or

(self.verwijzingNaarTekstInfo.TekstReferentieBG_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID)

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e12</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing naar illustratie</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Besluitgebied_A

<b>gelijk aan structuurvisiegebied_G</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e13</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Attribuut besluitnummer en verwijzingNaarVaststellingsbesluit alleen toegestaan en verplicht planstatus = vastgesteld</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Besluitgebied_A<br/>
Inv BesluitnummerVerplicht:<br/>
if self.planstatusInfo.planstatus = Planstatus::vastgesteld<br/>
 then self.besluitnummer -&gt; notEmpty()and self.verwijzingNaarVaststellingsbesluit -&gt; notEmpty()<br/>
 else self.besluitnummer -&gt; isEmpty()and self.verwijzingNaarVaststellingsbesluit -&gt; isEmpty()<br/>
endif

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Besluitvlak_A</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e14</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format verwijzing naar tekst</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Inv TypeTekstEnBestandsnaam_AMB:

def: namespace : String = identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
def: objectgerichteTest: Boolean = self.verwijzingNorm = IMROPT2012<br/>
def: tekstTypeBijlage: Boolean = (self.verwijzingNaarTekstInfo.TekstReferentie_AMB.typeTekst = Teksttype_AMB::'bijlage bij regels' or<br/>
self.verwijzingNaarTekstInfo.TekstReferentie_AMB.typeTekst = Teksttype_AMB::'bijlage bij toelichting' or<br/>
self.verwijzingNaarTekstInfo.TekstReferentie_AMB.typeTekst = Teksttype_AMB::'bijlage bij besluittekst')

and

/* tekst niet objectgericht */

/*besluittekst*/<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_AMB.typeTekst = Teksttype_AMB::besluittekst and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'd_' + planID

and<br/>
/* regels */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_AMB.typeTekst = Teksttype_AMB::regels and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'r_' + planID

and<br/>
/*toelichting */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_AMB.typeTekst = Teksttype_AMB::toelichting and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 't_' + planID

and<br/>
/* bijlage bij regels */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_AMB.typeTekst = Teksttype_AMB::'bijlage bij regels' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* bijlage bij toelichting */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_AMB.typeTekst = Teksttype_AMB::'bijlage bij toelichting' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* bijlage bij besluittekst */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_AMB.typeTekst = Teksttype_AMB::'bijlage bij besluittekst' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* tekst objectgericht*/<br/>
/* niet tekstTypeBijlage */<br/>
(objectgerichteTekst and not(tekstTypeBijlage)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID

/* tekst objectgericht*/<br/>
/* tekstTypeBijlage */

(objectgerichteTekst and tekstTypeBijlage) implies

(self.verwijzingNaarTekstInfo.TekstReferentie_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID)

or<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_AMB.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID)

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e15</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format verwijzing illustratie</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Besluitvlak_A

idem aan structuurvisieplangebied_G

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Besluitsubvlak_A</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e16</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format verwijzing naar tekst</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Besluitsubvlak_A

gelijk aan Besluitvlak_A

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format verwijzing naar illustratie</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Besluitsubvlak_A<br/>
gelijk aan Besluitvlak_A

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Overige gebiedsgerichte besluiten</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e17</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing naar tekst</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Besluitgebied_X<br/>
Inv TypeTekstEnBestandsnaamBG_XGB:

def: namespace : String = identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
def: objectgerichteTest: Boolean = self.verwijzingNorm = IMROPT2012<br/>
def: tekstTypeBijlage: Boolean = (self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.typeTekst = TeksttypeBG_XGB::'bijlage bij besluitdocument' or<br/>
self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.typeTekst = TeksttypeBG_XGB::'bijlage voorschriften regels' or<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.typeTekst = TeksttypeBG_XGB::'bijlage bij toelichting')

and<br/>
/* tekst niet objectgericht */<br/>
/* besluitdocument */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.typeTekst = TeksttypeBG_XGB::besluitdocument and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'd_' + planID

and<br/>
/* voorschriften/regels */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.typeTekst = TeksttypeBG_XGB::voorschriften/regels and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'r_' + planID

and<br/>
/*toelichting */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.typeTekst = TeksttypeBG_XGB::toelichting and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 't_' + planID

and<br/>
/* bijlage bij besluitdocument */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.typeTekst = TeksttypeBG_XGB::'bijlage bij besluitdocument' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* bijlage bij toelichting */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.typeTekst = TeksttypeBG_XGB::'bijlage bij toelichting' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* bijlage bij voorschriften/regels */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.typeTekst = TeksttypeBG_XGB::'bijlage bij besluitdocument' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.verwijzingNaarTekst. substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* tekst objectgericht*/<br/>
/* niet tekstTypeBijlage */<br/>
(objectgerichteTekst and not(tekstTypeBijlage)) implies

self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID

and

/* tekst objectgericht*/<br/>
/* tekstTypeBijlage */<br/>
(objectgerichteTekst and tekstTypeBijlage) implies

(self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.verwijzingNaarTekst. substring(1,aantalKarakters + 2) = 'b_' + planID)<br/>
or<br/>
(self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID)

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>ee1</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Relatie tussen besluittype en teksttype</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Besluitgebied_X

Inv RelatieBesluitEnTeksttype:<br/>
def: Teksttypen: Bag = self.verwijzingNaarTekstInfo.TekstReferentieBG_XGB -&gt; collect (typeTekst)<br/>
and

/* aanwijzingsbesluit, gerechtelijke uitspraak, omgevingsvergunning en reactieve aanwijzing */

(self.typePlan = RuimtelijkPlanOfBesluit_XGB::aanwijzingsbesluit or<br/>
self.typePlan = RuimtelijkPlanOfBesluit_XGB::’gerechtelijke uitspraak’ or<br/>
self.typePlan = RuimtelijkPlanOfBesluit_XGB::omgevingsvergunning or<br/>
 self.typePlan = RuimtelijkPlanOfBesluit_XGB::'reactieve aanwijzing') implies

Teksttypen-&gt;Count( 'besluitdocument' ) = 1<br/>
and<br/>
Teksttypen-&gt;Count( 'voorschriften/regels' ) = 0<br/>
and<br/>
Teksttypen-&gt;Count( 'toelichting' ) &lt;= 1<br/>
and<br/>
Teksttypen-&gt;Count( 'bijlage bij besluitdocument' ) &lt;= 1<br/>
and<br/>
Teksttypen-&gt;Count( 'bijlage bij voorschriften/regels’ ) = 0<br/>
and<br/>
Teksttypen-&gt;Count( ‘bijlage bij toelichting’ ) &lt;= 1)

and<br/>
/* beheersverordening, exploitatieplan */<br/>
(self.typePlan = RuimtelijkPlanOfBesluit_XGB:: beheersverordening or self.typePlan = RuimtelijkPlanOfBesluit_XGB:: exploitatieplan) implies

Teksttypen-&gt;Count( ‘besluitdocument’ ) = 0<br/>
and<br/>
Teksttypen-&gt;Count( ‘voorschriften/regels’ ) = 1<br/>
and<br/>
Teksttypen-&gt;Count( ‘toelichting’ ) &lt;= 1<br/>
and<br/>
Teksttypen-&gt;Count( ‘bijlage bij besluitdocument’ ) = 0<br/>
and<br/>
Teksttypen-&gt;Count( ‘bijlage bij voorschriften/regels’ ) &lt;= 1<br/>
and<br/>
Teksttypen-&gt;Count( ‘bijlage bij toelichting’ ) &lt;= 1)

and<br/>
/* voorbereidngsbesluit */<br/>
self.typePlan = RuimtelijkPlanOfBesluit_XGB:: voorbereidingsbesluit implies

Teksttypen-&gt;Count( ‘besluitdocument’ ) = 1<br/>
and<br/>
Teksttypen-&gt;Count(‘voorschriften/regels’ ) &lt;= 1<br/>
and<br/>
Teksttypen-&gt;Count( ‘toelichting’ ) &lt;= 1<br/>
and<br/>
Teksttypen-&gt;Count( ‘bijlage bij besluitdocument’ ) &lt;= 1<br/>
and<br/>
Teksttypen-&gt;Count( ‘bijlage bij voorschriften/regels’ ) &lt;= 1<br/>
and<br/>
Teksttypen-&gt;Count( ‘bijlage bij toelichting’ ) &lt;= 1)

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e18</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format verwijzing naar illustratie</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2012::Besluitgebied_X <br/>
Inv Illustratieverwijzing:

def: namespace : String = self.identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = self.identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = self.identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
and

/* illustratie */<br/>
self.verwijzingNaarTekstInfo.IllustratieReferentie_XGB.verwijzingNaarIllustratie.substring(1,aantalKarakters + 2) = 'i_' + planID

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e19</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Attribuut besluitnummer en verwijzingNaarVaststellingsbesluit alleen toegestaan en verplicht planstatus = vastgesteld</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Besluitgebied_X<br/>
Inv BesluitnummerVerplichtXGB:<br/>
if self.planstatusInfo.planstatus = Planstatus::vastgesteld<br/>
 then self.besluitnummer -&gt; notEmpty()and self.verwijzingNaarVaststellingsbesluit -&gt; notEmpty()<br/>
 else self.besluitnummer -&gt; isEmpty()and self.verwijzingNaarVaststellingsbesluit -&gt; isEmpty()<br/>
endif

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e20</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Relatie tussen attribuut beleidsmatigVerantwoordelijkeOverheid en attributen naamOverheid en locatieNaam.</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Inv locatieNaamVerplicht_naamOverheid:

*/gemeente/*<br/>
*/naamOverheid 1 maal/*<br/>
self. beleidsmatigVerantwoordelijkeOverheid = Overheden_XGB:: gemeentelijke overheid implies<br/>
self.naamOverheid -&gt; size() = 1<br/>
and<br/>
*/deelgemeente/*<br/>
*/naamOverheid 1 maal/*<br/>
self. beleidsmatigVerantwoordelijkeOverheid = Overheden_XGB:: deelgemeente/stadsdeel implies<br/>
self.naamOverheid -&gt; size() = 1

*/provinciale overheid/*<br/>
*/naamOverheid 1 maal, locatieNaam verplicht/*<br/>
self. beleidsmatigVerantwoordelijkeOverheid = Overheden_XGB:: provinciale overheid implies<br/>
self.naamOverheid -&gt; size() = 1 and self.locatieNaam -&gt; notEmpty()

and<br/>
*/nationale overheid/*<br/>
*/naamOverheid 1 of meer, locatieNaam verplicht/*<br/>
self. beleidsmatigVerantwoordelijkeOverheid = Overheden_XGB:: nationale overheid<br/>
implies<br/>
self.locatieNaam -&gt; notEmpty()

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Besluitvlak_X</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e21</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing naar tekst</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Besluitvlak_X

Inv TypeTekstEnBestandsnaam_XGB:

def: namespace : String = identificatie.NEN3610ID.namespace<br/>
def: lokaalID : String = identificatie.NEN3610ID.lokaalID<br/>
def: versie : String = identificatie.NEN3610ID.versie<br/>
def : planID : String = namespace + '.' + lokaalID + '-' + versie<br/>
def: aantalKarakters : Integer = planID -&gt; size()<br/>
def: objectgerichteTest: Boolean = self.verwijzingNorm = IMROPT2012<br/>
def: tekstTypeBijlage: Boolean = (self.verwijzingNaarTekstInfo.TekstReferentie_XGB.typeTekst = Teksttype_XGB::'bijlage bij besluittekst' or<br/>
self.verwijzingNaarTekstInfo.TekstReferentie_XGB.typeTekst = Teksttype_XGB::'bijlage bij toelichting' or<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_XGB.typeTekst = Teksttype_XGB:: ‘bijlage bij voorschriften/regels’

and

/* tekst niet objectgericht */<br/>
/* besluittekst */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_XGB.typeTekst = Teksttype_XGB::besluittekst and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_XGB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'd_' + planID

and<br/>
/* voorschriften/regels */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_XGB.typeTekst = self.Teksttype_XGB::voorschriften/regels and not(objectgerichteTekst)) implies

verwijzingNaarTekstInfo.TekstReferentie_XGB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'r_' + planID

and<br/>
/* toelichting */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_XGB.typeTekst = Teksttype_XGB::toelichting and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_XGB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 't_' + planID

and<br/>
/* bijlage bij besluittekst */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_XGB.typeTekst = Teksttype_XGB::'bijlage bij besluittekst' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_XGB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* bijlage bij toelichting */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_XGB.typeTekst = Teksttype_XGB::'bijlage bij toelichting' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_XGB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* bijlage bij voorschriften/regels */<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_XGB.typeTekst = Teksttype_XGB::'bijlage bij voorschriften/regels' and not(objectgerichteTekst)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_XGB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID

and<br/>
/* tekst objectgericht*/<br/>
/* geen tekstTypeBijlage */<br/>
(objectgerichteTekst and not(tekstTypeBijlage)) implies

self.verwijzingNaarTekstInfo.TekstReferentie_XGB.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID

/* tekst objectgericht*/<br/>
/* tekstTypeBijlage */<br/>
(objectgerichteTekst and tekstTypeBijlage)implies

(self.verwijzingNaarTekstInfo.TekstReferentie_XGB.verwijzingNaarTekst.substring(1,aantalKarakters + 2) = 'b_' + planID)

or<br/>
(self.verwijzingNaarTekstInfo.TekstReferentie_XGB.verwijzingNaarTekst.substring(1,aantalKarakters + 3) = 'pt_' + planID)

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Besluitsubvlak_X</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e22</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Format voor verwijzing naar tekst</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Besluitsubvlak_X

rest gelijk aan Besluitvlak_X

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Algemene test regels voor verwijzingen</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e23</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Besluitgebied </b><b>verwijst naar een bestaand plangebied id</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Geen OCL constraint

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e24</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Besluitvlak verwijst naar een bestaand plangebied id</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Geen OCL constraint

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e25</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Besluitsubvlak verwijst naar een bestaand plangebied id</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Geen OCL constraint

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e26</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Besluitsubvlak verwijst naar een bestaand Besluitvlak id</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Geen OCL constraint

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e27</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Besluitsubvlak verwijst naar een bestaand Besluitsubvlak id</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Geen OCL constraint

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>e28</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Besluitsubvlak verwijst naar besluitvlak of Besluitsubvlak</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Context: IMRO2012::Besluitsubvlak_P<br/>
Context: IMRO2012::Besluitsubvlak_A<br/>
Context: IMRO2012::Besluitsubvlak_X

Inv subvlakHoortBijAnderVlak:<br/>
not(self.besluitvlak -&gt; isEmpty() and self.besluitsubvlak -&gt; isEmpty())

and

not(self.besluitvlak -&gt; notEmpty() and self.besluitsubvlak -&gt; notEmpty())

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;' colspan='2'><b>MetadataIMRObestand</b>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>f1</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Attribuut codeReferentiesysteem heeft altijd waarde 28992 (Rijksdriehoekstelsel)</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>context IMRO2013:: MetadataIMRObestand

inv Rijksdriehoekstelsel: self.codeReferentiesysteem = ‘28992’

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'></td>
</tr>
</tbody>
</table>

