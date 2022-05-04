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

- využít desku Nexys-A7 na zadávání morseova kódu pomocí switche
- převedení teček a čárek do textu
- zobrazení textu na 7 segmentovém displeji

<a name="hardware"></a>

## Hardware description

Realizaci jsme provedli následovně. Pomocí switche, který v poloze nahoře zapisuje čárku a v poloze dole zapisuje tečku, se tvoří morseovka. Problém s rozpoznáním kdy končí znak a kdy končí slovo jsme vyřešili tím, že se počítají náběžné hrany, když je jich víc (tzn. déle času se nepřepne switch), tak program rozpozná, že končí slovo. Následně program zobrazí text na 7mi segmentovém displeji.

<a name="modules"></a>

## VHDL modules description and simulations



<a name="top"></a>

## TOP module description and simulations

Top umožňuje propojit jednotlivé moduly a následně vše nahrát do desky Nexys-A7.

<a name="video"></a>

## Video

Write your text here

<a name="references"></a>

## References

1. Nexys-A7 reference manuál (https://digilent.com/reference/programmable-logic/nexys-a7/reference-manual?redirect=1)
2. 
