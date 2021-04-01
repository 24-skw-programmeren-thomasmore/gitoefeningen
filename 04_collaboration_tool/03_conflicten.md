# Conflicten

## Wat is een conflict?
* Bij een merge van 2 versies krijg je een conflict als in de 2 versies een aanpassing gedaan is in dezelfde file en op dezelfde lijn. 
* git kan dan niet zelf beslissen wat er moet gebeuren 
* je moet zelf nakijken en **kiezen**:
  * wil je jouw aanpassingen
  * of de aanpasingen van de andere persoon
  * of allebei de aanpassingen
  ***** of moet je nog extra code aanpassingen doen om dit te laten werken
* noot: merge van 2 versies kan zijn: 
  * pull 
  * merge van branches 
* Voor wat volgt raad ik wel aan om IntelliJ te gebruiken, of een andere tool waarmee je visuele merges kan doen.


## Hoe zie je dat er een conflict is? 
* Als je in IntelliJ een pull doet die een conflict veroorzaakt krijg je een duidelijke boodschap: 
![img.png](images/pull_with_conflict.png)
  
## Wat doe je bij een conflict 
* Dit moet je doen voor elke file waarin een conflict zit. 
* Kies zeker **Merge**! 
* Als je "Accept Yours" kiest gooi je de changes die je collega gepushed heeft weg! 
* Als je "Accept Theirs" kiest gooi je je eigen changes weg! 
* IntelliJ opent het **Merge venster**. 

## Wat zien we in het Merge venster?  
![img.png](images/merge_window.png)
* Links zie je je eigen versie
* Rechts zie je de versie die je collega gepusht had
* In het midden zie het resultaat
* Een conflict wordt in het rood gemarkeerd
* Een change die geen conflict is wordt in het groen gemarkeerd
* Rechts bovenaan zie je dat er 1 conflict is in dit geval   
* Je kan de up/down pijltjes links bovenaan gebruiken om naar de vorige/volgende change te gaan (als er meerdere changes zijn) 
* Het is meestal wel een goed idee om "Apply non-conflicting changes te kiezen (All)" (als er ook non-conflicting changes zijn)

## Wat doe je in het Merge venster? 
* Ga naar het eerste conflict 
* Je moet nu kiezen welke versie je wil houden: de linkse versie (jouw versie) of de rechtse versie (van je collega's) 
* In het IntelliJ merge tool moet je voor allebei de versies (links en rechts) zeggen of je dit wil houden of niet  
* In dit geval kies ik om ze allebei te houden
* Ik kies eerst de linkse versie 
![img.png](images/conflict_resolve_choose_left.png)


* Deze change wordt dan toegepast in het middelste stuk (Result)
![img.png](images/conflict_resolve_accept_left.png)


* Ik kies dus ook de rechtse versie
![img.png](images/conflict_resolve_choose_right.png)


* Deze change wordt ook toegepast in het middelste stuk (Result)
![img.png](images/conflict_resolve_accept_right.png)
  
* If check nog even het resultaat: 
![img.png](images/conflict_resolve_check_result.png)
  

* **Ik pas de tekst in het middelste venster nog aan tot ik het resultaat goed vind** 
* Dan duw ik op de **Apply** knop rechts onderaan 
* IntelliJ zal onmiddellijk deze merge committen (als alle conflicten geresolved zijn)
* In git log zie ik de nieuwe commit. De message is "Merge remote-tracking branch 'origin/main'"
* Je ziet ook dat er vanaf mijn nieuwe commit nu 2 paden naar beneden lopen die de aparte gemergde commits bevatten 

![img.png](images/conflict_log.png)

* Test steeds of alles nog werkt na een merge 

## Wat gebeurt er als het het conflict negeert 
* Dan zie je deze popup:

![img.png](images/ignore_conflict.png)

* als je die ook negeert:

![img.png](images/keep_ignoring_conflict.png)

* Je kan nu niet meer committen tot je het conflict oplost!  


## Hoe voorkom je conflict problemen 
****
### Pull often
* als je dikwijls pullt dan zijn de changes die je binnenkrijgt klein
* er kunnen wel conflicten zijn, maar deze zullen ook **klein** zijn en dus **gemakkelijk** te fixen 
* de changes die je pullt zijn nog "**vers**" en degene die deze change gedaan heeft zal nog weten wat/waarom/hoe

| pull often | 
|---|

## Push often 
* als je dikwijls pusht dan zijn de changes die je pusht klein 
* als ze conflicten veroorzaken voor je collega's dan zijn die conflicten **klein** en **gemakkelijk** te fixen  

| push often | 
|---|

## Test before you push 
* leer in kleine stappen te werken! 
* test! 

## Oefening 
* spreek af met 1 of meer mensen uit je klas en clone dezelfde repo op github
* bekijk welke problemen je tegenkomt en los samen op
* changes in dezelfde file op dezelfde lijn 
  * persoon 1: maak een local change en commit
  * persoon 2: maak een local change _in dezelfde file en op dezelfde lijn_ en commit
  * persoon 1: pull en push
  * persoon 2: pull en push - **los het conflict op** 
  * persoon 1: pull
  * bekijk het resultaat in github en op je local repo
  
## Oefening op je eentje 
* je kan dit eventueel ook op je eentje doen (maar dat is niet simpeler)
* clone dezelfde Github-repo 2 keer op je lokale machine 
* Je kan in elke clone files aanpassen en committen
* pull en push werkt dan op dezelfde manier als in een team 

---
[prev](01_simpele_workflow.md)
[next]()

