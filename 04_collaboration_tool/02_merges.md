# Merges

## Wat is een merge? 
* Wat gebeurt er bij een pull van een change?
  * noot: in je local repo is alles gecommit
* Bij een pull is er een **merge van de changes**: jouw aanpassingen en de aanpassingen van je collega's komen samen.  
* Git heeft goede merging capaciteiten. In de meeste gevallen lukt dit zonder problemen.
* Maar minstens moet je na een merge steeds alles opnieuw testen!

| Pull on a clean directory! |
|---|

## Changes in verschillende files: 
* git zal de nieuwe versies van die files in je local repo pullen
* je ziet geen extra commit in de git log 

## Changes in dezelfde file op verschillende lijnen: 
* bvb: lijnen toevoegen, lijnen deleten, lijnen aanpassen
* de changes die de andere persoon gedaan heeft worden in jouw file toegepast.
* zolang jouw changes en de andere changes op verschillende lijnen zijn is er geen probleem 
* we zeggen dat deze ***file gemerged** is: **git heeft een extra aanpasssing gedaan in jouw file**, tussen jouw aanpassingen  
* git doet automatisch een commit voor dit soort merge. De message is iets als:
```
Merge branch 'master' of https://github.com/verapeeters-thomasmore/test
```
* Je krijgt de mogelijkheid om deze message aan te passen in de default editor ([zie installatie Git](../01_getting_started/02_installeer_git.md)).

## Changes in dezelfde file op dezelfde lijnen:
* in dit geval kan git zelf niet beslissen wat het resultaat moet zijn
* we noemen dit een [**conflict**](03_conflicten.md) 
* je moet zelf nakijken op welke lijnen er een conflict is en voor elke lijn **kiezen**:  
  * wil je jouw aanpassingen
  * of de aanpasingen van de andere persoon
  * of allebei de aanpassingen  
  * of moet je nog extra code aanpassingen doen om dit te laten werken    
* Hierover meer in de [volgende sectie](03_conflicten.md)

## Oefening 
* spreek af met 1 of meer mensen uit je klas en clone dezelfde repo op github
* bekijk welke problemen je tegenkomt en los samen op
* changes in verschillende files  
  * persoon 1: maak local changes en commit 
  * persoon 2: maak local changes _in een andere file_ en commit 
  * persoon 1: pull en push   
  * persoon 2: pull en push  
  * persoon 1: pull 
  * bekijk het resultaat in github en op je local repo 
* changes in dezelfde file op verschillende lijnen 
  * persoon 1: maak local changes en commit
  * persoon 2: maak local changes _in dezelfde file_ en commit
  * persoon 1: pull en push
  * persoon 2: pull en push
  * persoon 1: pull
  * bekijk het resultaat in github en op je local repo
  
## Oefening op je eentje 
* je kan dit eventueel ook op je eentje doen (maar dat is niet simpeler)
* clone dezelfde Github-repo 2 keer op je lokale machine 
* Je kan in elke clone files aanpassen en committen
* pull en push werkt dan op dezelfde manier als in een team 

---
[prev](01_simpele_workflow.md)
[next](03_conflicten.md)

