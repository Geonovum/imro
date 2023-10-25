# GML specificaties {#7F7DAEBA}

## GML versie en profiel {#181304A8}

IMRO2012 maakt als uitwisselingsformaat gebruik van gml versie 3.2.1, simple features profile 2. Dit is de versie en het profiel op GML dat door Nederland wordt gevolgd als standaard voor GML implementatie. IMRO2012 is geïmplementeerd in een GML schema dat refereert aan gml 3.2.1 conform het simple features profile 2. Het volgende XML schema is daarvoor van belang:<br/>
<ul><li>IMRO2012.XSD: XML schema van het IMRO2012 model.</li>
</ul>

## Nadere implementatie specificaties {#2E971161}

Voor het genereren van IMRO2012 gml bestanden zijn er nog een aantal aanvullende afspraken.  
<br/>

<b>Encoding, tekenset, van het GML bestand</b><br/>
Voor de encoding van het GML bestand wordt UTF-8 voorgeschreven. Van UTF-8 wordt de tekenset ISO-8859-1 ondersteunt en binnen deze tekenset wordt gebruikt: unicode [32 – 128] en [160 – 255]. Opgemerkt wordt dat (U+8216), (U+8217), (U+8220), (U+8221) ook als tekens op een kaart weer te geven moeten zijn.  
<br/>

<b>FeatureCollection</b><br/>
Voor het gml bestand is er een eigen FeatureCollection gemaakt. De benaming is FeatureCollectionIMRO.  
<br/>

<b>gml:featureMember - gml:featureMembers</b><br/>
Alleen gml:featureMember wordt in IMRO2012 ondersteund.  
<br/>

<b><i>gml: id</i></b><br/>
Elk object in het GML bestand krijgt een &lt;gml:id&gt;. Dit gml:id heeft geen informatiewaarde maar is nodig om interne en externe referenties te realiseren. Er zijn in een IMRO bestand drie verschillende situaties met betreking tot het gml:id:<br/>
<b>Object Plangebied: </b>De waarde voor gml:id is opgebouwd uit de waarden van het samengestelde attribuut &lt;imro:identificatie&gt; volgens het format gml:id = &lt;namespace&gt;’.’&lt;lokaalID&gt;’-’&lt;versie&gt;.<br/>
<b>Object Planobject:</b> De waarde voor gml:id is opgebouwd uit de waarden van het samengestelde attribuut &lt;imro:identificatie&gt; volgens het format gml:id= &lt;namespace&gt;’.’&lt;lokaalID&gt;.<br/>
<b>Objecten die een gml geometrie</b> representeren: Geen afgesproken format anders dan dat het met een alfanumeriek teken moet beginnen en uniek moet zijn binnen een bestand. Voor geometrieën hoeft het gml:id niet persistent te zijn en mag elke keer opnieuw worden gegenereerd.  
<br/>

<b>Geometrietypen en interpolatie</b><br/>
In het IMRO2012 UML en het afgeleide XML schema zijn de geometrietypen gespecificeerd.<br/>
Naast gml:LineString mag ook gml:Arc en gml:Circle gebruikt worden.<br/>
gml:Arc is gedefinieerd door drie punten.<br/>
Niet ondersteund worden:<br/>
gml:ArcByCenterPoint<br/>
gml:ArcByBulge<br/>
gml:CircleByCenterPoint  
<br/>

<b>Draairichting van polygonen</b><br/>
Hiervoor gelden de regels van ISO19107: Geographic information – Spatial Schema.<br/>
Voor een polygoon die je van de bovenkant bekijkt: exterior ring tegen de klok in, interior ring met de klok mee. In 2d GIS bekijk je polygonen altijd van de bovenkant.  
<br/>

<b>Nauwkeurigheid coördinaten</b><br/>
Nauwkeurigheid van coördinaten is 3 decimalen. Alles wat nauwkeuriger is wordt afgerond op deze nauwkeurigheid (3 decimalen). 0.0015 -&gt; 0.002; 0.0014 -&gt; 0.001.  
<br/>

<b>srsName</b><br/>
srsName invullen bij elk planobject op hoogste geometrie niveau.<br/>
Voor IMRO2012 is het coördinaat referentiesysteem Rijksdriehoekstelsel, epsg code 28992, verplicht en wordt dit als volgt ingevuld:<br/>
<span style='color: #FF0000;'>srsName</span>="urn:ogc:def:crs:EPSG::28992"<br/>
<i>Toelichting: srsName is de specificatie van het coördinaat referentiesysteem. Voor iedere geometrie moet een srsName te vinden zijn. In feite betekent dit dat iedere geometrie een srsName moet hebben. In geval van een multigeometrie hoeft de srsName alleen aan de multigeometrie te hangen en niet aan ieder los onderdeeltje ervan.</i>  
<br/>

<b>srsDimension</b><br/>
srsDimension wordt niet opgenomen.<br/>
<i>Toelichting: De srsDimension geeft aan uit hoeveel elementen een coördinaat bestaat. In het geval van twee dimensies (x,y) is dat 2. Omdat GML-SF2 drie dimensies niet toestaat is dat in dit geval niet nodig.</i>  
<br/>

<b>Xlink:href</b><br/>
Het format voor de href is dat een # altijd voorafgaat aan een gml:id.<br/>
<i>Voorbeeld:</i><br/>
Verwijzing naar een plangebied:<br/>
<pre class="text">&lt;imro:plangebied <span style='color: #FF0000;'>xlink:href</span>="#NL.IMRO.0012.0000SA7680-0003"/&gt;<br/>
</pre>

Verwijzing naar een planobject:<br/>
<pre class="text">&lt;imro:bestemmingsvlak <span style='color: #FF0000;'>xlink:href</span>="#NL.IMRO.1233556"/&gt;<br/>
</pre>

<i>Toelichting: Het # is om aan te geven dat binnen een href het volgende fragment een locatie betreft binnen het voorafgaande 'document'. Als er geen voorafgaand document is, is de locatie intern (lokaal). Kortom als de href begint met een # wordt er verwezen naar een lokaal gml:id. Dat klopt ook met de bedoeling van de links tussen planobjecten. Als er verwezen wordt naar een extern object, dan begint de href niet met het # maar komt het # voorafgaand aan de locatie (meestal een gml:id) binnen het externe document.</i>  
<br/>

<b>Uitbreidbare codelijsten</b><br/>
Het format voor waarden die aan uitbreidbare codelijsten worden toegevoegd is:<br/>
<pre class="text">&lt;pattern <span style='color: #FF0000;'>value</span>="other: .*"/&gt;<br/>
</pre>

Dit staat alle verzamelingen van tekens toe maar moet wel beginnen met ‘other:’ + ‘spatie’<br/>
Een waarde als: other: maatvoering; oppervlakte; relatief vloeroppervlak (%), is hiermee op te nemen.  
<br/>

Naast deze open toevoeging bij codelijsten zijn er ook codelijsten die een strikter format hebben voor toe te voegen waarden. Voorbeeld hiervan is de codelijst Functieaanduidingen. Voor de toe te voegen waarden is een begintekst voorgeschreven. Een voorbeeld hiervan is:<br/>
<pre class="text"><span style='color: #000000;'>    </span><span style='color: #0000FF;'>&lt;</span><span style='color: #800000;'>simpleType</span><span style='color: #FF0000;'> name</span><span style='color: #0000FF;'>="</span><span style='color: #000000;'>GebiedsaanduidingenOtherType</span><span style='color: #0000FF;'>"&gt;</span><br/>
<span style='color: #000000;'>        </span><span style='color: #0000FF;'>&lt;</span><span style='color: #800000;'>restriction</span><span style='color: #FF0000;'> base</span><span style='color: #0000FF;'>="</span><span style='color: #000000;'>string</span><span style='color: #0000FF;'>"&gt;</span><br/>
<span style='color: #000000;'>            </span><span style='color: #0000FF;'>&lt;</span><span style='color: #800000;'>pattern</span><span style='color: #FF0000;'> value</span><span style='color: #0000FF;'>="</span><span style='color: #000000;'>geluidzone - .*</span><span style='color: #0000FF;'>"/</span><br/>
</pre>

Dit betekent dat bijvoorbeeld een waarde ‘geluidzone – schietbaan’ is toegestaan.

