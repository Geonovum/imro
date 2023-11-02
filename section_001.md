# Inleiding {#7F7D92A9}

## Informatiemodel {#7F7D92AA}

In dit rapport wordt het Informatiemodel voor de Ruimtelijke Ordening, IMRO2012, beschreven. De verschillende omgevingsinstrumenten (plannen, visies, besluiten e.d.) worden gepresenteerd, de planobjecten die nodig zijn om de ruimtelijke component van de beleidsinformatie te beschrijven worden gedefinieerd, de relaties tussen de planobjecten en de attributen met bijbehorende domeinwaarden zijn opgenomen.<br/>

Dit rapport is onderdeel van set RO Standaarden 2012 en is normstellend voor de codering van omgevingsinstrumenten. Het is van belang voor applicatiebouwers en als referentie voor andere IMRO gerelateerde documenten. IMRO2012 wordt beschreven zonder uit te weiden over de praktische toepassing van het model voor het coderen van digitale omgevingsinstrumenten. Bijvoorbeeld voor bestemmingsplannen of structuurvisies. Alle voor dit toepassingsdoel benodigde informatie vindt u in zogenaamde praktijkrichtlijnen:<br/>
<ul><li><a href='https://docs.geostandaarden.nl/ro/bp2012/' target='_blank'>Praktijkrichtlijn Bestemmingsplannen (PRBP2012)</a>;</li>
<li><a href='https://docs.geostandaarden.nl/ro/sv2012/' target='_blank'>Praktijkrichtlijn Structuurvisies (PRSV2012)</a>;</li>
<li><a href='https://docs.geostandaarden.nl/ro/gb2012/' target='_blank'>Praktijkrichtlijn Gebiedsgerichte Besluiten (PRGB2012)</a>;</li>
<li><a href='https://docs.geostandaarden.nl/ro/pv2012/' target='_blank'>Praktijkrichtlijn Provinciale Verordening (PRPV2012)</a>;</li>
<li><a href='https://docs.geostandaarden.nl/ro/amvb2012/' target='_blank'>Praktijkrichtlijn Algemene Maatregel van Bestuur (PRAMvB2012)</a>;</li>
<li><a href='https://docs.geostandaarden.nl/ro/pt2012/' target='_blank'>Praktijkrichtlijn voor Planteksten (PRPT2012)</a>.</li>
</ul><br/>

Naast de praktijkrichtlijnen zijn er nog drie standaarden van toepassing voor de ontsluiting en verbeelding van omgevingsinstrumenten:<br/>
<ul><li><a href='https://docs.geostandaarden.nl/ro/svbp' target='_blank'>Standaard Vergelijkbare Bestemmingsplannen (SVBP2012)</a> met bijbehorende <a href='https://docs.geostandaarden.nl/ro/bp2012/' target='_blank'>praktijkrichtlijn</a>;</li>
<li><a href='https://docs.geostandaarden.nl/ro/stri' target='_blank'>Standaard Toegankelijkheid Ruimtelijke Instrumenten (STRI2012)</a> met bijbehorende <a href='https://docs.geostandaarden.nl/ro/tri2012' target='_blank'>praktijkrichtlijn</a>;</li>
<li><a href='https://docs.geostandaarden.nl/ro/imropt' target='_blank'> Informatiemodel Ruimtelijke Ordening Planteksten (IMROPT2012)</a> met bijbehorende <a href='https://docs.geostandaarden.nl/ro/pt2012/' target='_blank'>praktijkrichtlijn</a>.</li>
</ul>
<br/>

Het informatiemodel voor de ruimtelijke ordening is in 2000 in een eerste versie verschenen. Sinds die datum is IMRO in verhoogde mate toegepast in de praktijk. Om een correcte digitale uitwisseling van een ruimtelijk instrument kunnen garanderen is een eenduidige beschrijving van de inhoud noodzakelijk. IMRO2012 is het informatiemodel dat deze eenduidige beschrijving mogelijk maakt.  
<br/>

In juli 2008 is de nieuwe Wet op de ruimtelijke ordening (Wro) in werking getreden. Onderdeel van deze wet is dat planologische visies, plannen, besluiten, verordeningen en algemene maatregelen van bestuur digitaal vervaardigd en op elektronische wijze beschikbaar worden gesteld. Daarnaast is ook in de Wet algemene bepalingen omgevingsrecht (Wabo) en in de Crisis- en herstelwet (Chw) een verplichte elektronische beschikbaarstelling opgenomen voor sommige gevallen. Om dit mogelijk te maken zijn de RO standaarden ontwikkeld. IMRO is één van de standaarden uit dit samenhangende pakket.

Het gebruik van de RO Standaarden 2008 heeft ervaringen en inzichten opgeleverd die de standaard kunnen verbeteren. Daarnaast is ook de RO praktijk en wetgeving in beweging wat een effect heeft op de eisen die aan de standaard gesteld worden. Beide processen hebben geleid tot een nieuwe IMRO versie. IMRO2012 is de opvolger van IMRO2008.  
<br/>

Voor de toepassing van IMRO in de verschillende instrumenten zijn de eerder genoemde praktijkrichtlijnen opgesteld. Dit zijn aparte documenten die per instrumenttype uitvoerig en volledig toelichten hoe een digitaal instrument conform IMRO gecodeerd dient te worden.

## Leeswijzer {#7F7D92C5}

Dit document bestaat uit twee delen. In <a href='#7F7D92A9'>Hoofdstuk 1</a> tot en met <a href='#48DDA048'>Hoofdstuk 5</a> wordt de context van IMRO2012 beschreven en de relaties die er zijn met het Basismodel Geo-informatie. Het tweede deel behandelt de inhoudelijke beschrijving van IMRO2012: in <a href='#06474D64'>Hoofdstuk 6</a> wordt aan de hand van UML-klassediagrammen en bijbehorende objectcatalogus de verschillende omgevingsinstrumenten beschreven. <a href='#1139BF9A'>Hoofdstuk 7</a> handelt over de geometrie van planobjecten. <a href='#1B9B615D'>Hoofdstuk 8</a> beschrijft extra modelregels die niet in de klassediagrammen vastgelegd zijn doormiddel van tekst en OCL constraints. Metadata van een IMRO2012 GML bestand worden in <a href='#5B919E61'>Hoofdstuk 9</a> beschreven. Een belangrijk onderdeel van het model zijn de domeinlijsten die de waarden voor de gebruikte attributen beschrijven. In <a href='#090B956C'>Hoofdstuk 10</a> zijn deze lijsten opgenomen. Ten slotte zijn in <a href='#7F7DAEBA'>Hoofdstuk 11</a> regels opgenomen voor de toepassing van het gml uitwisselingsformaat.<br/>
In <a href='#7F7DAF04'>Bijlage 1</a> is het UML-schema presentatie voor klassediagram opgenomen. Het overzicht Basismodel Geo-informatie: UML klassediagram is in <a href='#7F7DAF40'>Bijlage 2</a> opgenomen.

