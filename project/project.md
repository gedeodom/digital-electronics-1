# Morse code recevier

### Team members

**Polkorab Jaroslav**
- návrh morse code příjímače, vytvoření a zpracování kódu

**Sedlák Ondřej**
- zpracování schémat

**Gedeon Dominik**
- dokumentace projektu

**Gočiková Erika**

### Table of contents

* [Project objectives](#objectives)
* [Hardware description](#hardware)
* [VHDL modules description and simulations](#modules)
* [TOP module description and simulations](#top)
* [Video](#video)
* [References](#references)

<a name="objectives"></a>

## Project objectives

Využít desku Nexys-A7 na zadávání a zároveň vizualizaci morseova kódu. 

<a name="hardware"></a>

## Hardware description

Realizaci jsme provedli následovně. Pomocí switche, který v poloze nahoře zapisuje čárku a v poloze dole zapisuje tečku, se tvoří morseovka. Problém s rozpoznáním kdy končí znak a kdy končí slovo jsme vyřešili tím, že se počítají náběžné hrany, když je jich víc (tzn. déle času se nepřepne switch), tak program rozpozná, že končí slovo. 

<a name="modules"></a>

## VHDL modules description and simulations

Write your text here.

<a name="top"></a>

## TOP module description and simulations

Write your text here.

<a name="video"></a>

## Video

Write your text here

<a name="references"></a>

## References

1. Write your text here.
