---
layout: default
title: Traducció de diceware.com
author: Arnold Reinhold
translated: Toni Homedes i Saun
lang: ca
source: http://world.std.com/~reinhold
---

<div  class="alert alert-info" role="alert" id="legal-notice">
<button type="button" class="close" data-dismiss="alert" aria-label="Close">
<span aria-hidden="true">&times;</span></button>
Traducció al Català de la <a href="http://www.diceware.com/"
hreflang="en">pàgina original</a> d'<a href="http://world.std.com/~reinhold/" hreflang="en">Arnold Reinhold</a><br />
<span lang="en">Translation to Catalan of <a href="http://world.std.com/~reinhold/"
hreflang="en">Arnold Reinhold</a>'s <a href="http://www.diceware.com/"
hreflang="en">original page</a></span>
</div>

---------------------------------------

Pàgina d'inici de Diceware
==========================

<IMG SRC="{{ page.source }}/dice5.gif" NAME="graphics1" ALIGN=LEFT
WIDTH=111 HEIGHT=37 BORDER=0>

Aquesta pàgina ofereix una manera millor de crear frases d'accés fortes però
fàcils de recordar per utilitzar amb programes d'encriptació i seguretat. Les
contrasenyes i frases d'accés febles són un dels defectes més comuns en la
seguretat informàtica. Preneu-vos uns minuts i aprengueu a fer-ho bé. La
informació que es presenta aquí pot ser utilitzat per qualsevol persona. No cal
cap coneixement previ sobre criptografia o matemàtiques. Només cal seguir els
passos senzills que és descriuen a continuació. Si voleu saber encara més sobre
les frases d'accés consulteu les
[Preguntes Freqüents (FAQ) de Diceware][faq] i, si us plau,
comproveu el Bloc  de Seguretat Diceware
per comentaris sobre les últimes evolucions de la seguretat informàtica i
l'autentificació de secret compartit.

Aquesta pàgina també està disponible en [Xinès, Esperanto, Finès, Francès,
Italià, Japonès, Polonès i Espanyol](#idiomes). També hi han llistes de
paraules en [Català, Holandès, Esperanto, Finlandès, Francès, Alemany, Italià,
Japonès, Polonès, Rus, Espanyol, Suec i Turc](#idiomes).

---------------------------------------
---------------------------------------

**Proveu el nostre applet Java [Calculadora de Grans
Nombres]({{ page.source }}/BigNumCalc.html)**. Us permetrà realitzar molts dels
càlculs utilitzats en
criptografia de clau pública. Hauria de funcionar en la majoria dels navegadors
moderns en els equips que suporti Java (que no inclou iOS d'Apple, ho sento)

---------------------------------------

Què és una frasse de pas?
-------------------------

Una frase de pas és un munt de paraules i caràcters que escriviu en el vostre
ordinador perquè aquest sàpiga del cert que la persona que escriu sou vos. La
majoria de programes de seguretat permeten introduir una frase de pas en lloc
de només una contrasenya curta per a una major protecció contra els atacants.
Alguns programes també utilitzen la vostra frase de pas per formar una clau
criptogràfica per xifrar les seves dades:

 *  Les frases de pas s'utilitzen amb els [sistemes de seguretat de xarxa sense
fils]({{ page.source }}/airport.html) Wi-Fi com WPA i WPA2, quan s'utilitza en
mode de clau compartida personal (PSK). La seguretat d'ambdós sistemes depèn de
la força de la contrasenya que trieu.

 *  El popular programa de xifrat de Phil Zimmermann [PGP](#PGPInfo), per
exemple, requereix que feu frase de pas que cal introduir cada vegada que cal
signar o desxifrar missatges. El mateix succeeix amb la versió de codi
obert [GnuPG](http://www.gnupg.org/).

 *  Els programes populars de manegament de contrasenyes requereixen una
contrasenya mestra o frase de pas per protegir les dades que emmagatzemen.

 *  Les frases de pas s'utilitzen en el programari de xifrat de discos com PGPdisk
o FileVault d'Apple. Moltes organitzacions requereixen que el xifrat dels discos
dels ordinadors portàtils compleixin els requeriments legals per protegir
informació sensible.

 *  Les últimes versions dels sistemes operatius més populars, incloent
Windows XP i Mac OS-X, permeten utilitzar frases de pas més llargues per
la identificació dels usuaris, enlloc de només acceptar contrasenyes curtes.

 *  Les noves monedes digitals com el BitCoin utilitzen frases de pas per
protegir les "monedes" d'una apropiació indeguda.

 * Utilitzar una frase de pas curta com a resposta a una "pregunta de seguretat"
(com "A quina ciutat va néixer?") us protegeix front a intents de descobrir la
vostra resposta a base de buscar informació en línia sobre vos.

Hauríeu de seguir les instruccions de Diceware aquí presents *abans*
d'instal·lar un router Wi-Fi, crear la vostre clau PGP o GPG, obrir un nou
compte segur o preparar un disc xifrat.

Les frases de pas difereixen de les contrasenyes només en la longitud.
Les *contrasenyes* solen ser curtes, de sis a deu caràcters. Les contrasenyes
curtes son acceptables per entrar en sistemes informàtics programats per
detectar múltiples intents fallits de entrada i protegir les contrasenyes
desades apropiadament, però no són segures per usar-les en sistemes de xifrat.
Les frases de pas acostumen a ser molt més llargues -- típicament de 20 a 40
caràcters, de vegades inclús més. La seva major longitud les fa més segures.
Les frases de pas modernes van ser inventades per [Sigmund N. Porter](#Porter)
el 1982. [Si tot el que necessiteu és una contrasenya de entrada feu clic aquí](
{{ page.source }}/dicewarefaq.html#login). En cas contrari seguiu llegint.

Escollir una bona frase de pas és una de les coses més importants que podeu fer
per preservar la privacitat del vostre ordinador i missatges de correu electrònic.
Una frase de pas hauria d'esser:

 *  Coneguda només per vos

 *  Prou llarga com per ser segura

 *  Difícil d'endevinar -- inclús per algú que us coneix bé

 *  Fàcil de recordar

 *  Fàcil d'escriure sense errors

## <IMG SRC="{{ page.source }}/die236.gif" NAME="graphics2" ALIGN=LEFT WIDTH=32 HEIGHT=32 BORDER=0> Què és Diceware?

Diceware és un mètode per escollir frases de pas que utilitza daus (n. del t.
Dice => daus) per escollir paraules al atzar d'una llista especial anomenada
Llista de Paraules de Diceware. Cada paraula de la llista està precedida per un
número de 5 xifres. Totes les xifres estan entre el 1 i el 6, permetent usar
el resultat de cinc tirades de dau per seleccionar una paraula de la llista.

Aquest és un petit extracte de la llista de paraules de Diceware:

    16655 clause
    16656 claw
    16661 clay
    16662 clean
    16663 clear
    16664 cleat
    16665 cleft
    16666 clerk
    21111 cliche
    21112 click
    21113 cliff
    21114 climb
    21115 clime
    21116 cling
    21121 clink
    21122 clint
    21123 clio
    21124 clip
    21125 clive
    21126 cloak
    21131 clock

La [llista complerta][list] té 7776 paraules curtes, abreviacions i cadenes de
caràcters fàcils de recordar. La longitud mitjana de cada paraula és de 4.2
caràcters. Les paraules més llargues fan sis caràcters. La llista anglesa està
basada en una llista més llarga publicada en el grup de Usenet *sci.crypt* per
Peter Kwangjun Suk. La [llista alternativa][beale], editada per Alan Beale, té
menys americanismes i paraules obscures. També hi han [llistes per diversos
altres idiomes](#japanese). Pot descarregar la [llista de paraules Diceware en
format PDF][pdf] o en [format PostScript][ps].

## <IMG SRC="{{ page.source }}/die236.gif" NAME="graphics3" ALIGN=LEFT WIDTH=32 HEIGHT=32 BORDER=0> Ús de Diceware

Per usar Diceware necessitareu un o més daus. Els daus venen amb molts jocs de
sobretaula i també es poden comprar solts en botigues de joguets, aficions i
màgia. [Toys'R'Us](http://www.toysrus.com/) ven un paquet de cinc daus per
aproximadament un dolar. També estan disponibles [daus
Braille](http://www.google.com/search?q=daus+Braille). Podeu comprar cinc [daus
de cualitat de casino]({{ page.source }}/dicewarefaq.html#casino) en línia de
[Casinocom.com](http://www.casinocom.com/Diceonly.html). *[No utilitzeu un
ordinador ni cap tipus de dau electrònic](
{{ page.source }}/dicewarefaq.html#electronic)*.

 1. Descarregueu la [llista Diceware][list] complerta o la [llista alternativa
Beale][beale] i deseu-la en el vostre ordinador. Si ho preferiu,
[imprimiu-la](#print). Desprès torneu a aquesta pàgina.

 1. Decidiu quantes paraules utilitzareu a la vostra frase de pas. Una frase
de pas de cinc paraules proporciona un nivell de seguretat molt més elevat
que les contrasenyes senzilles que utilitzen la majoria de persones. Nosaltres
recomanem un mínim de sis paraules per usar-les amb PGP, GPG, seguretat Wi-Fi
i programes de xifrat de fitxers. Per a grans valors, tipus BitCoin i similar
es recomana utilitzar set o vuit paraules. Per més informació veieu les
[Preguntes Freqüents (FAQ) de Diceware][faq].

 1. Ara tireu els daus i escrigueu els resultats en un tros de paper. Escrigueu
els números en grups de cinc. Feu tants grups de cinc com paraules necessiteu.
Podeu tirar un dau cinc cops o cinc daus un cop, o qualsevol altre combinació.
Si tireu diversos daus alhora llegiu-los d'esquerra a dreta.

 1. Consulteu cada número de cinc dígits a la llista de Diceware i preneu la
paraula que hi ha just al costat. Per exemple 21124 vol dir que la propera
paraula de la vostra frase de pas seria "clip" (veure el extracte de la llista
més amunt).

 1. Quan ho hageu fet les paraules que hagueu trobat són la vostra nova
frase de pas. Memoritzeu-les i destruïu el tros de paper o guardeu-lo en un
lloc realment segur. Això és tot!

### Exemple

Suposeu que voleu una llista de sis paraules, tal com recomanem per la majoria
d'usuaris. Necessitareu 6 vegades 5 tirades que són 30 tirades. Imagineu que
surten les següents:

    1, 6, 6, 6, 5, 1, 5, 6, 5, 3, 5, 6, 3, 2, 2, 3, 5, 6,
    1, 6, 6, 5, 2, 2, 4, 6, 4, 3, 2, i 6.

Escrigueu els resultats en un tros de paper en grups de cinc tirades:

    1 6 6 6 5
    1 5 6 5 3
    5 6 3 2 2
    3 5 6 1 6
    6 5 2 2 4
    6 4 3 2 6

Aleshores busqueu cada crup de cinc tirades la la llista Diceware tot buscant
el número a la llista i apuntant la paraula que hi ha al costat del número:

    1 6 6 6 5 cleft
    1 5 6 5 3 cam
    5 6 3 2 2 synod
    3 5 6 1 6 lacy
    6 5 2 2 4 yr
    6 4 3 2 6 wok

La vostra frase de pas seria:

    cleft cam synod lacy yr wok

### Consells

 *  Per a la màxima seguretat assegureu-vos d'estar sol/a i tanqueu les cortines.
Escrigueu en una superfície dura -- no en una llibreta de paper. Després de
memoritzar la frase de pas cremeu les vostres notes, esmicoleu les cendres i
tireu-les al lavabo.

 *  Si utilitzeu una frase de pas per xifrat de fitxers us recomanem que en
guardeu una copia escrita en un lloc segur. Si no ho feu i oblideu la frase de
pas els vostres fitxers estaran perduts per sempre.

 *  <A NAME="print"></A> Si voleu treballar amb una copia impresa de la llista,
descarregueu la [llista Diceware en format
PDF]({{ page.source }}/dicewarewordlist.pdf) o en [format
PostScript]({{ page.source }}/dicewarewordlist.ps). Aquests fitxers estan
formatats amb 4 columnes i 54 línies per pàgina. Obtindreu una impresió de 36
pàgines en que les dues primeres tirades de dau son les mateixes per a cada
pàgina. Això facilita molt la cerca. Si preferiu una impressió més compacta
[aquí hi ha una versió d'onze pàgines de Patrick
Feisthammel](http://www.rubin.ch/pgp/diceware.html). *Aneu amb compte de no
marcar la copia impresa de cap manera mentre seleccioneu les paraules.* També
podeu trobar la llista de paraules com a apèndix de [Internet
Secrets](#internetsecrets).

 *  Si necessiteu fer frases de pas de manera freqüent feu-vos amb una caixa de
sabates o similar. Poseu cinc daus a la caixa, agiteu-la vigorosament -- un
mínim de de cops forts -- i alsehores inclineu la caixa per fer que els daus
s'alineïn en una vora. Ara podeu obrir la caixa i llegir els daus d'esquerra a
dreta o del davant al darrera si n'hi ha d'apilats. Aleshores busqueu la entrada
corresponent de la llista de paraules. Repetiu aquest procés fins que tingueu
suficients paraules per la vostra frase de pas.

 *  Us recomanem utilitzar la frase de pas exactament com ha estat generada. Si
voleu una frase de pas més segura seleccioneu una paraula addicional amb el
mètode Diceware.

 *  Com que algunes paraules de la llista tenen dos o menys caràcters pot ser que
obtingueu una frase de pas molt curta. Si la vostra frase de pas, incloent els
espais entre les paraules, fa menys de 17 caràcters de llargada us recomanem
tornar a començar i crear una frase de pas nova. També hauríeu de tornar a
començar si la vostra frase de pas és una frase reconeixible (aquesta situació
és extremadament rara).

 *  Veieu les [Preguntes Freqüents (FAQ) de
Diceware]({{ page.source }}/dicewarefaq.html#memory) per suggerències sobre
com memoritzar la vostra frase de pas.

### Informació addicional que no necessiteu conèixer

 *  Per una seguretat addicional sense afegir un altre paraula inseriu un
caràcter especial o dígit escollit al atzar a la vostra frase de pas. Aquí hi ha
com fer-ho de manera segura: tireu un dau per escollir una paraula de la vostra
frase, tireu de nou per escollir una lletra d'aquesta paraula. Tireu un tercer
i quart cop per escollir un caràcter addicional de la següent taula:

           Tercera tirada
            1 2 3 4 5 6
        Q  1 ~ ! # $ % ^
        u  2 & * ( ) - =
        a  3 + [ ] \ { }
        r  4 : ; " ' < >
        t  5 ? / 0 1 2 3
        a  6 4 5 6 7 8 9

 *  Per als més tècnics, cada paraula de la vostra frase proporciona 12,9 bits
d'entropia, la manera en que es mesura la seguretat de les frases de pas. Una
frase de pas de 5 paraules te una entropia de al menys 64,6 bits; sis paraules
tenen 77,5 bits, set paraules 90,4 bits i vuit paraules 103,2 bits. Afegir una
lletra al atzar afegeix uns 10 bits d'entropia. Tot això assumint, naturalment,
que mantingueu la vostra frase de pas en secret.

 *  Trobareu molt més informació que realment no necessiteu conèixer a les
[Preguntes Freqüents (FAQ) de Diceware][faq]

## <IMG SRC="{{ page.source }}/die236.gif" NAME="graphics4" ALIGN=LEFT WIDTH=32 HEIGHT=32 BORDER=0> Perquè Diceware?

Hi han [moltes recomanacions diferents](#faqs) disponibles a Internet sobre
com escollir una frase de pas. Moltes són bones, unes poques són dolentes però
pràcticament totes requereixen que l'usuari jutgi quan difícil serà d'endevinar
per un altre persona. Algunes no donen cap guia de com fer-ho, altres
requereixen que feu complicats càlculs matemàtics. En contrast el métode
Diceware és:

 *  Fàcil d'aprendre i d'utilitzar

 *  Molt segur

 *  Totalment prescriptiu - us diem que cal fer en cada pas del procés

 *  Transparent - No hi han "confieu en mi"s

 *  Lliure - No cal cap ordinador, programari o maquinari, només la llista
Diceware i daus corrents.

La natura prescriptiva de Diceware és molt important per als nous usuaris de
xifrat. Aquñi hi ha la experiencia d'una persona tal com ho va publicar al
grup de noticies d'Internet *alt.security.pgp*:

> "Només volia relatar una història personal sobre el difícil que és convèncer
> un principiant de escollir una contrasenya segura i de fer-li entendre que
> és una contrasenya segura. So una persona experimentada amb Internet i amb
> temes de seguretat. La meva germana, en canvi, és una principiant absoluta
> que tot just acaba d'obrir-se un compte d'Internet. Ella viu a mig-oest
> mentre que jo visc a la costa oest. Com a conseqüència solem enviar-nos molts
> correus electrònics.
>
> Fa poc, ella va voler dona la contrasenya d'Internet al seu marit per que ell
> també pogués connectar-se. Tot i amb això ella volia mantenir la possibilitat
> d'intercanviar missatges privats amb mi que ell no pogués llegir. Jo,
> naturalment la vaig introduir en l'ús del PGP,
>
> Li vaig donar la lliçoneta habitual sobre quan important és seleccionar
> una contrasenya que ningú més pugui endevinar amb facilitat i que la
> contrasenya ideal seria una paraula obscura i sense sentit que només tingués
> significat per ella. Li vaig explicar tot el necessari sobre no seleccionar
> natalicis, aniversaris, noms i similar. No li vaig suggerir una combinació
> aleatòria de lletres i números perquè tampoc necessitàvem una seguretat
> excepcional, només volíem que el seu marit no pogués llegir els nostres
> correus electrònics. Així, després de que ella selecciones la seva contrasenya
> de PGP vaig decidir fer un intent de craquejar-la. La PRIMERA paraula que
> vaig provar fa funcionar! Ella es va sorprendre del fàcil que em va ser
> endevinar-la però era una paraula que qualsevol que la conegués bé hauria
> endevinat. Així que després de donar-li uns quants consells més sobre la
> selecció de contrasenyes segures ho va tornar a intentar. Aquest cop només
> em va costar 3 intents trobar la paraula adequada. Al final, ho va donar per
> impossible i em va deixar a mi seleccionar la seva contrasenya."

Si la germana de l'autor hagués utilitat el Diceware la primera frase de pas
hagués estat totalment segura i coneguda només per ella. Recordeu: a la
criptografia de clau pública la seguretat dels missatges depèn de la frase de
pas *del destinatari*. Doneu a conèixer el Diceware.

## <IMG SRC="{{ page.source }}/die236.gif" NAME="graphics5" ALIGN=LEFT WIDTH=32 HEIGHT=32 BORDER=0>Enllaços i Referències

Per més informació sobre frases de pas Diceware veieu el següent:

[Preguntes Freqüents (FAQ) de Diceware][faq] Preguntes i respostes per a qui
vulgui saber més sobre Diceware i la generació de frases de pas.

La [llista de paraules][list], la [llista en format PostScript][ps],
la [llista de paraules Beale][beale], [llista Diceware8k][dw8k] per generació
amb ordinador.

Un [estudi sobre l'us de frases de pas a PGP]({{ page.source }}/passphrase.survey.asc).
Una petita enquesta que vaig fer per esbrinar el fan realment els usuaris de
PHP per crear frases de pas, i algunes suggerències de millores.

[Diceware for Passphrase Generation and Other Cryptographic
Applications]({{ page.source }}/diceware.txt) Inclou informació sobre altres
usos de la seguretat Diceware.

[Protecting Passwords](http://www.ibm.com/developerworks/library/s-pass2/index.html)
per Gary McGraw and John Viega, un article a la IBM Developerworks Security
Library que parla de contrasenyes, paraules de pas i Diceware.

[Passgen: A Password Generator Java Applet]({{ page.source }}/passgen.html)
Utilitza la latència del teclat per generar contrasenyes aleatòries en un
format seleccionable. No és tan segur com el mètode Diceware però és adequat
per contrasenyes d'entrada i aplicacions similars. Inclou el codi font.

[Random Noise Sources]({{ page.source }}/truenoise.html) Una col·lecció
d'informació sobre fonts d'aleatorietat per usar amb ordinadors.

[CipherSaber Home Page](http://ciphersaber.com/) Apreneu a fer el vostre propi
programa de xifrat fort. És més fàcil del que penseu!

[Other Papers on Cryptography by Arnold Reinhold]({{ page.source }}/papers.html)
P=?NP -- A qui li importa? Anàlisis criptogràfic de la histocompatibilitat, etc.

<A NAME="Porter"></A>S. N. Porter,
*A Password Extension for Improved Human Factors*,<br />
Advances in Cryptology: A Report on CRYPTO 81, editor Allen Gersho, volum 0,
U.C. Santa Barbara Dept. of Elec. and Computer Eng., Santa Barbara,
1982. Pàgines 81--81. També a Computers &amp; Security, Vol. 1. No. 1,
1982, North Holland Press.

## <A NAME="Japanese"></A><A NAME="idiomes"></A> Diceware en altres idiomes

[**CA** -- Llista de paraules en Català](https://github.com/Jautenim/diceware-cat)
(ASCII and UTF-8) proporcionada per Marcel Hernandez sota el termes de la
[llicència CC-BY-4.0](http://creativecommons.org/licenses/by/4.0/). Exemple de
frase de pas en Català:

    radiar balca imaginar insula sinitizin dar

[**CN** -- Xinés]({{ page.source }}/diceware.chinese.html) Traduit per Lian.

[**DE** -- Llista de paraules en Alemany]({{ page.source }}/diceware_german.txt)
[versió PDF]({{ page.source }}/Diceware_German.pdf) proporcionada per Benjamin
Tenne sota els termes de la [GNU General Public
License](http://www.gnu.org/licenses/). Exemple de frase de pas en Alemany:

    distel ist landen kammer puffen

[**EO** -- Esperanto](http://esperantajxo.blogspot.com/2014/07/dajsvaro.html)
traduït per Makis Diras, incloent una [llista de paraules en
Esperanto](https://4d93035d-a-62cb3a1a-s-sites.googlegroups.com/site/esperantajxo/Dajsvara%20Vortlisto%20v20140626.pdf?attachauth=ANoY7cpC-hvS8hNwTN-plRl96xV2I6H9G3yJEhG8sDIqLE-40DecJp-uvJHSZAwfTwWmGhmdKZbUDPtFDFvHv6CEAF1wG4N9iUoQV3KtkW2WeFmQ_gLCMjn5W9xw2VWoHZ_xtYuoYPkiUiPISE9FHHgDXqybgy0Wb6NaFMTLS8PkC5bO3e79-9drfDHn0R0mVUDQgtF1mKgXh1sIKpg5-Pww5jfm4unep1-h8DjyGcZOZV3rmUdK-WM=&attredirects=0).
Exemple de frase de pas en Esperanto:

    hirt neŭtr livre etern krank esoter

[**ES** -- Espanyol]({{ page.source }}/diceware_en_espanolA.htm) Traduit per
Manuel Palao, incloent una [llista de paraules en
Espanyol]({{ page.source }}/DW-Espanol-1P.pdf).
Exemple de frase de pas en Espanyol:

    multa h64 quien enero tubo

[**FI** -- Finès](http://www.iki.fi/kaip/noppaware/) traduït per Kai Puolamaki,
incloent una
[lista de paraules en Finès](http://www.iki.fi/kaip/noppaware/noppaware.txt).
Exemple de frase de pas Noppaware ("noppa" significa daus en Finès):

    olli kukot hoveli hintaa airoja

[**FR** -- Francès](http://web.archive.org/web/20041012030451/www.gjldp.org/CHARENTAISES/article.php3?id_article=4)
traduït per Joachim Dubuquoy-Portois. Hi ha una [llista de paraules en
Francès](http://weber.fi.eu.org/index.shtml.en#projects) en diversos formats per
Matthieu Weber. Exemple:

    ileus humide diktat sbire peotte

[**IT** -- Italià](http://www.taringamberini.com/italiano/diceware_it_IT.shtml)
traduït per Tarin Gamberini amb una [llista de paraules en
Italià](http://www.taringamberini.com/download/diceware_it_IT/word_list_diceware_in_italiano.txt)
([en format PDF](http://www.taringamberini.com/download/diceware_it_IT/word_list_diceware_in_italiano.pdf))
Exemple de frase de pas en Italià:

    casi botole stadi maglia venivo

[**JP** -- Japponès](http://www.hyuki.com/diceware/) traduït per Hiroshi Yuki, amb
una [llista de paraules en Japonès](http://s3.amazonaws.com/dotclue.org/diceware_jp.txt)
en Romaji per J Greely. Exemple de frase de pas en Japonès:

    douse aho socchi bidou tosou ob

[**NL** -- Llista de paraules en Holandès](http://theworld.com/%7Ereinhold/DicewareDutch.txt)
proporcionada per Bart Van den Eynde sota els termes de la
[GNU Free Documentation License](http://www.gnu.org/licenses/).
Exemple de frase de pas en Holandès:

    ijler 100 leperd akolei kolkje

[**PL** -- Polonès](http://drfugazi.eu.org/pl/bezpieczenstwo/diceware)
traduït per Piotr (DrFugazi) Tarnowski, Computer Science Techniques
Centre, Universitat de Silesia, Katowice, PL, incloent una [llista de paraules
poloneses](http://drfugazi.eu.org/sites/drfugazi.eu.org/files/dicelist-pl.txt)
Exemple de frase de pas polonesa:

    plewka szpieg raban pruski ibi

[**RU** -- llista de paraules en Rus]({{ page.source }}/diceware.ru.zip)
proporcionada per "kitten". Exemple de frase de pas. Us cal una font ciríl·lica
per poder llegir-la.

    ÍËðýÒý Ò¸Ïãý âÂðÒÚý ÊÛõÎûÈ ÁÂâÓÚý

[**SV** -- llista de paraules en Suec](http://x42.com/diceware/) proporcionada
per Magnus Bodin. Exemple de frase de pas en Suec:

    ark altan rodel lamm kyot

<A HREF="http://dicewaretr.110mb.com/diceware_tr.txt"><FONT
SIZE=4><B>TR</B></FONT></A>
<A HREF="http://dicewaretr.110mb.com/diceware_tr.txt">-- Turkish word
list</A> provided by Mert Dirik. Here is a sample Turkish passphrase:

    derz permi turba um beniz

El [Kit Diceware]({{ page.source }}/dicewarekit.html) conté instruccions sobre
com crear una llista de paraules Diceware en altres idiomes.

*Moltes gràcies a tots els traductors!*

## <A NAME="PGPInfo"></A> Per més informació sobre PGP veieu:

[The GNU Privacy Guard](http://www.gnupg.org/) (GPG), una implementació de PGP
de codi obert.

[Pàgina internacional de PGP](http://www.pgpi.com/)

[Pàgina d'inici de PGP, que ara forma part de Symantec](http://www.pgp.com/)

[Grup de Yahoo! PGP-Basics](http://groups.yahoo.com/group/PGP-Basics/)

<A NAME="faqs"></A>Altres llocs amb recomanacions sobre com crear
la vostra frase de pas. No vull dir que la informació d'aquests llocs sigui
erronia, simplement que és massa complexa per la majoria de persones. Doneu-hi
una ullada i jutgeu vos mateix.

[*Preguntes Freqüents (FAQ) sobre frases de pas per Randall T.
Williams*](http://www.stack.nl/%7Egalactus/remailers/passphrase-faq.html)

[*Preguntes Freqüents (FAQ) sobre frases de pas per Grady
Ward*](http://www.unix-ag.uni-kl.de/%7Econrad/krypto/passphrase-faq.html)

<A HREF="http://ciphersaber.com/"><FONT COLOR="#000080"><IMG
SRC="{{ page.source }}/mylock.gif" NAME="graphics6" ALIGN=LEFT WIDTH=74 HEIGHT=37
BORDER=1><CENTER>
        <TABLE CELLPADDING=2 CELLSPACING=2>
                <TR>
                        <TD WIDTH=298 STYLE="border: none; padding: 0in">
                                <PRE STYLE="margin-left: 0.39in; margin-right:
0.39in; background: transparent; border: 2.30pt double #808080; padding: 0.02in;
text-align: center">Ascii key+  || 08d0a5d961603380e2949d682c
10 Byte IV  || bfe8da5c1dec3aba9725d4f689
Ron's No.4  || 40761763d4d38935e8bd8a44bf
All u need  ==== 4656a7bd7f9ae5d082a30cdfa7
<A HREF="http://ciphersaber.org/">CipherSaber</A> || f21a918d29c5917956d0468eaf</PRE>
                        </TD>
                </TR>
        </TABLE>
</CENTER>

http://ciphersaber.org/ <FONT COLOR="#000080">Apreneu a escriure programes de
xifrat simples però forts per vosaltres mateixos. Si teniu qualsevol coneixement
de programació -- ni que sigui en BASIC -- podeu fer-ho.</FONT>

--------------------------------------

#### <A NAME="internetsecrets"></A>
<FONT COLOR="#000080">Doneu suport a aquesta pàgina comprant llibres en que he
treballat. Són uns regals excelents!<BR>
[Switching to a Mac For Dummies,](http://www.amazon.com/exec/obidos/ASIN/111802446X/agreinhol)<BR>
Es fantàstic deixar de donar-se cops de cap contra la pared,<BR>
[Green IT for Dummies](http://www.amazon.com/exec/obidos/ASIN/0470386886/agreinhol),<BR>
un munt de informació útil que pot salvar el planeta,<BR>
i<BR>
[Internet Secrets](http://www.amazon.com/exec/obidos/ASIN/0764532391/agreinhol),
2a ed<BR>
amb capítols meus sobre criptografia i Diceware, incloent la llista de paraules
de Diceware.<BR>
Els podeu trobar a la vostra llibreria local o fent clic en els títols per
demanar-los directament, es associació amb Amazon.com.</FONT>

--------------------------------------

--------------------------------------

<ADDRESS STYLE="margin-bottom: 0.2in; background: transparent"><FONT
COLOR="#000080">[Arnold G. Reinhold]({{ page.source }}/)<BR>
e-mail: les meves inicials (3 lletres) a mac punt com<BR>
Petjada PGP:<BR>
FA C3 82 FB 05 5E 03 1A 34 04 79 EA 9E 76 7B 67</FONT></ADDRESS>

<FONT COLOR="#000080">Copyright
© 1995-2015, Arnold G. Reinhold, Cambridge, Massachusetts USA.<BR>
(n. del t. no és tradueix la llicencia per no tenir prou coneixements legals)<br />
The author hereby grants rights for free, non-commercial, electronic
distribution, with attribution, of this <I>entire</I> text. Linking
to this page or the word list, including for commercial use, is
permitted and encouraged. All other rights reserved. Reasonable
requests for other uses, such as translations, are encouraged and
will be carefully and promptly considered. This information is
distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of MERCHANTABILITY or
FITNESS FOR A PARTICULAR PURPOSE.</FONT>

<FONT COLOR="#000080">To
the extent that a word list is protected by copyright, A G Reinhold
licenses its rights to the English Diceware Wordlist under the
<A HREF="http://creativecommons.org/licenses/by/3.0/">Creative
Commons CC-BY 3.0</A> license.</FONT>

<FONT COLOR="#000080">Diceware és una marca registrada de A G Reinhold.</FONT>

<FONT COLOR="#000080">Els <A HREF="#ads">anuncis</A> d'aquesta pàgina són
sel·leccionats per Google i ajuden a cobrir-ne les despeses. No tenim cap manera
de saber quins productes és presenten i, en particular, no recomanem cap dels
productes que puguis ser anunciats.</FONT>

<FONT COLOR="#000080">Primera publicació a usenet's sci.crypt.research el
1-8-1995</FONT>

<FONT COLOR="#000080">Última actualització 28-3-2015</FONT>

[list]:  {{ page.source }}/diceware.wordlist.asc
[ps]:    {{ page.source }}/dicewarewordlist.ps
[pdf]:   {{ page.source }}/dicewarewordlist.pdf
[beale]: {{ page.source }}/beale.wordlist.asc
[faq]:   {{ page.source }}/dicewarefaq.html
[dw8k]:  {{ page.source }}/dicewarefaq.html#diceware8k
