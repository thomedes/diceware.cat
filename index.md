---
title: Pàgina d'inici
layout: default
page: home
---

<div class="jumbotron">
  <h1>{{ site.name }}</h1>

  <p>Les <strong>contrasenyes</strong> més <strong>segures</strong> i
  <strong>fàcils de recordar</strong><p>
</div>

<a id="quees"></a> Què és el Diceware
-------------------------------------

Mireu un moment aquesta contrasenya:

    ZwDr03nm

Serieu capaços de repetir-la sense mirar?

Ara mireu aquesta:

    format dient rebia cobrava

Us costaria recordar-la? De ben segur que seria més fàcil que l'anterior.

En canvi, la segona contrasenya *és més segura* que la primera.

-------------------------------------------------------------------------------

Diceware és un sistema per crear contrasenyes ideat per [A. G.
Reinhold](http://world.std.com/~reinhold/) que dona contrasenyes molt fàcils de
recordar i, al mateix temps, molt segures.

Les contrasenyes estan formades per diverses paraules curtes. Això és el que fa
que sigui fàcil de recordar. L'únic inconvenient és que haurem d'escriure una
mica més per posar la contrasenya.

Així, el Diceware esta format per una [llista de
paraules](https://github.com/thomedes/diceware.cat/raw/master/num-daus-i-paraules.txt)
que seleccionem tirant uns daus. Podem escollir la quantitat de paraules que
vulguem, però quantes més agafem més segura serà la contrasenya.

Així, a mode de exemple, les llongituds aconsellades són:

 -  **baixa seguretat**: 4 ó 5 paraules
 -  **mitja seguretat**: 6 ó 7 paraules
 -  **alta seguretat**: 7 ó més paraules

<a id="comutilitzo"></a> Com utilitzar el Diceware
--------------------------------------------------

Bàsicament la idea del Diceware es tenir una llista de paraules que anem
seleccionant al atzar. Per fer-ho fàcil la llista està feta per funcionar amb
tirades de daus, i, si us hi fixeu, al costat de cada paraula hi han 5 números
del 1 al 6 que corresponen a cinc resultats de daus:

    45542   ones
    45543   ONU
    45544   onze
    45545   opac
    45546   opaca
    45551   opalina

Aleshores, el que heu de fer és tirar un dau cinc cops (o cinc daus un cop, o
qualsevol combinació intermitja) i anotar els resultats. És busca la paraula
a la llista i ja en tenim una. Repetir tants cops com paraules necessitem.

Per una explicació més detallada pas a pas us recomano mirar la [traducció de
la pàgina de Diceware](diceware.com.ca.html) o, si llegiu l'anglès,
[la original](http://world.std.com/~reinhold/diceware.html).

Properament podreu descarregar la llista de paraules en format PDF de fàcil
impressió per poder fer això sense usar l'ordinador, que, de fet, es la manera
recomanada.

Com està feta la llista (només per als més tècnics)
---------------------------------------------------

Encara que no ho creieu porto molts anys pensant en com fer la llista. Les
llistes normals que s'usen per Diceware porten moltes "falses paraules" com
números, barreja de lletres i números i similar que estalvien feina a l'hora de
fer la llista però que, al meu entendre, *trenquen el principi fonamental* de
Diceware: *que sigui fàcil recordar la contrasenya*.

El mètode que he emprat és:

 -  Preparar (a ma) una llista manual amb totes les paraules que m'han vingut
al cap fàcils de recordar: Noms propis, Noms de pobles, rius, països, parts del
cos, objectes d'us quotidià, etc. Això m'ha dona a la vora de 700 paraules.

 -  He recopilat tants escrits en català contemporani com he pogut. N'he separat
 les paraules i he comptat la freqüència amb que apareixia cada una d'elles.
 També les he filtrat amb un diccionari català per eliminar les que estaven
 mal escrites.

 -  A la meva llista original he afegit la segona llista ordenada per mida de la
 paraula i freqüència d'us, de manera que en les més abundants (les de 7
 lletres) només quedin les més conegudes.

 -  He filtrat les paraules que tenen accents, dièresi, l·l o qualsevol altre
 caràcter estrany[[1](#filtre)].

 -  Finalment he agafat les 7776 primeres de la llista restant.

### <a id="filtre"></a>Perquè suprimir les paraules amb accents, dièresi i altres

Per dos motius:

#### La entropia no augmenta

Tot i la sensació de seguretat que proporciona
pensar que hi han "més caràcters diferents" *és erroni*, seguim
tenint 7776 paraules, i, per tant, *la entropia no augmenta*.

#### Teclats no catalans

Per als que tingueu la sort de viatjar... heu tingut mai que escriure una
contrasenya en un teclat estranger? Heu tingut mai que preguntar com és pot
escriure à o ü en aquell teclat? Terrible! Els estàs dient mitja contrasenya
abans de començar! Limitant-se a lletres i número ascii és molt fàcil escriure
la contrasenya en qualsevol teclat.

<a id="tecnics"></a>Perquè és segur Diceware? (només per als més tècnics)
-------------------------------------------------------------------------

La seguretat d'una contrasenya es mesura per la seva
[entropia](http://ca.wikipedia.org/wiki/Entropia#En_la_teoria_de_la_informaci.C3.B3).
Aquesta entropia, en el camp de la informàtica, es sol donar en bits i dona una
idea de l'esforç que caldrà per trobar la nostra contrasenya.

Per al Diceware la llista mesura 7776 (6^5) paraules, així que cada
paraula ens dona log2(7776) => 12,9 bits d'aleatorietat. En comparació, cada lletra
d'una contrasenya clàssica (A-Z, a-z i 0-9) ens dona log2(64) => 6 bits
d'aleatorietat.

Per això afirmava que la seguretat de

    ZwDr03nm                     => 8 lletres i números => 8 * 6    =   48 bits

és inferior a la de

    format dient rebia cobrava   => 4 paraules          => 4 * 12,9 = 51,7 bits
