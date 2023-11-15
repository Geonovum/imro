# Bijlage 1: UML-schema presentatie voor klassediagram {#7F7DAF04}

Voor het beschrijven van het model wordt gebruik gemaakt van de grafische modelleertaal UML (Unified Modelling Language). UML vindt zijn oorsprong in de objectoriëntatie en is door de Object management Groep (OMG) ontwikkeld als een standaard voor het beschrijven van objectgeoriënteerde modellen. Het UML klassediagram is één van de mogelijkheden die UML biedt. Dit onderdeel wordt in dit document gebruikt voor het beschrijven van IMRO. Hieronder volgt een beknopte samenvatting van de belangrijkste begrippen en notaties die gebruikt worden in een UML klassediagram.

<table style='width: 100%;'><caption></caption>
<colgroup><col id='col1' style='width: 40.05955107650023%;'>
<col id='col2' style='width: 59.940448923499765%;'>
</colgroup>
<thead valign='top'><tr><th align='left'>Begrip Nederlands (Engels)<br/>
</th>
<th align='left'>UML-notatie<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left'>Klasse (Class) = verzameling objecten met overeenkomstige eigenschappen (‘kenmerken, associaties en gedrag’).

Abstracte klasse (abstract class) = klasse zonder objecten.<br/>
Concrete klasse = klasse met objecten.<br/>
</td>
<td align='left'><img src='media/image16.png' alt='Afbeelding met tekst, schermopname, Lettertype, lijn' style='width: 46.433675633877826%;'></img>
Rechthoek met drie compartimenten:<br/>
Naam van de klasse<br/>
Attributen ( kenmerken)<br/>
Operaties ( gedrag)<br/>
</td>
</tr>
<tr><td align='left'>Instantie (instance) = een object uit een klasse<br/>
</td>
<td align='left'></td>
</tr>
<tr><td align='left'>Associatie (association) = relatie tussen twee klassen<br/>
</td>
<td align='left'>Een relatie tussen twee of meer klassen. Om weer te geven hoeveel objecten met elkaar gekoppeld zijn gebruiken we de multipliciteit.<br/>
<img src='media/image17.png' alt='Afbeelding met tekst, schermopname, Lettertype, lijn' style='width: 32.10230503762498%;'></img>
Eén object (instantie) van klasse A heeft een relatie met nul of meer objecten (instanties) van klasse B<br/>
</td>
</tr>
<tr><td align='left'>Multipliciteit (multiplicity) = het aantal betrokken objecten in een associatie

</td>
<td align='left'>Opname van een expliciet aantal (1, 2 enz)<br/>
Of een reeks:<br/>
0.. = nul of meer<br/>
1..  = één of meer<br/>
2..5 = twee tot vijf<br/>
</td>
</tr>
<tr><td align='left'>Specialisatie (specialization) = het verfijnen van een klasse (de zgn. superklasse) in onder- of subklassen

</td>
<td align='left'><figure><img src='media/image18.png' alt='Afbeelding met tekst, lijn, Rechthoek, schermopname' style='width: 78.53598067150281%;'></img>
<figcaption></figcaption></figure>

</td>
</tr>
<tr><td align='left'>Overerving (inheritance) = iedere subklasse erft alle eigenschappen (kenmerken, associaties en gedrag) van zijn superklasse<br/>
</td>
<td align='left'></td>
</tr>
<tr><td align='left'>Aggregatie (aggregation) = een associatie tussen een samengestelde klasse en een component klasse (maakt deel uit van). Objecten van de deelklasse kunnen worden toegevoegd of verwijderd zonder dat de geheelklasse ophoudt te bestaan.<br/>
</td>
<td align='left'><figure><img src='media/image19.png' alt='Afbeelding met tekst, schermopname, lijn, Rechthoek' style='width: 32.38892282140697%;'></img>
<figcaption></figcaption></figure>

</td>
</tr>
<tr><td align='left'>Compositie (composition) = een associatie die aangeeft dat een of meer klassen (componenten) onderdeel zijn van een andere klasse (compositieklasse), met als restrictie dat een component niet zelfstandig verder leeft als de compositieklasse verdwijnt<br/>
</td>
<td align='left'><figure><img src='media/image20.png' alt='Afbeelding met tekst, schermopname, lijn, Rechthoek' style='width: 88.85458194301945%;'></img>
<figcaption></figcaption></figure>

</td>
</tr>
<tr><td align='left'>Enumeratie (enumeration) = Een klasse die een lijst van waardes weergeeft. Deze kan gebruikt worden op plaatsen waar voor een bepaalde waarde uit een beperkt aantal vooraf bekende mogelijkheiden gekozen moet worden. Een enumeratie is een klasse met als stereotype ‘&lt;&lt;Enumeration&gt;&gt;’.<br/>
</td>
<td align='left'><figure><img src='media/image21.png' alt='Afbeelding met tekst, Lettertype, schermopname' style='width: 40.127873775044456%;'></img>
<figcaption></figcaption></figure>

</td>
</tr>
<tr><td align='left'>CodeList= Wanneer vooraf niet bekend is welke waardes een bepaald attribuut kan krijgen, maar als er wel een lijst waarschijnlijke waardes is, wordt in plaats van een Enumeratie een CodeList gebruikt. Een CodeList is een klasse met als stereotype ‘&lt;&lt;CodeList&gt;&gt;’.<br/>
</td>
<td align='left'></td>
</tr>
</tbody>
</table>

