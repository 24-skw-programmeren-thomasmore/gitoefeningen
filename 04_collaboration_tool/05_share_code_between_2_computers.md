# Hoe code sharen tussen 2 computers 

## Situatie 
* Op school werk je op je laptop.
* Thuis werk je op een desktop. 
* Je wil wel verderwerken aan dezelfde oefeningen/codebase. 

## Gebruik Git en GitHub
* zet altijd de laatste versie van de code op GitHub voor je op je andere machine begint te werken (commit en push). 
* Op je andere machine doe je altijd eerst een fetch en een update
* check of je echt de laatste versie van de code voor je hebt! 
* pas daarna begin je te werken aan je code
* **op deze manier vermijd je merges en conflicten**

## Voorbeeld 
* je start een project op je laptop op school met IntelliJ  
  * [maak een git repo](../01_getting_started/06_git_basis_met_intellij.md) van dit project
  * commit al je aanpassingen 
  * connecteer je project met een [repo op GitHub](../03_github/04_connect_existing_local_repo.md)
  * push alle commits zodat ze zichtbaar zijn op GitHub
  * laatste versie van de code staat dus op GitHub 
* thuis 
  * op je desktop thuis open je IntelliJ 
  * File > New > Project from Version Control -- gebruik de url van de repo op GitHub 
  * je hebt nu de laatste versie van het project op je desktop
  * werk verder op je desktop 
  * commit en push als je klaar bent zodat de laatste versie op GitHub staat 
* naar school 
  * voor je naar school vertrekt open je het project op je laptop 
  * doe een [fetch all remotes en een pull/update](../03_github/05_push_and_pull) (van de branches waar je aan gewerkt hebt)
  * de laatste versie van je code staat nu op je laptop
  * op school werk je verder op je laptop 
  * als je klaar bent: commit en push zodat de laatste versie weer op GitHub staat 
* thuis
  * als je wil verderwerken op je desktop: 
  * open het project
  * doe een [fetch all remotes en een pull/update](../03_github/05_push_and_pull) (van de branches waar je aan gewerkt hebt)
  * de laatste versie van je code staat nu op je desktop
  * etc 
  

## Gebruik NOOIT een shared drive 
* **Je mag nooit een codeer-project op een shared drive zetten!!!!** 
* Vroeg of laat kom je in de problemen als je dat doet.
* shared drive = bvb oneDrive, googleDrive, dropbox, ... 
* Waarom mag dit niet? 
  * een shared drive doet heel frequent een syncronisatie tussen de folder op de lokale pc en de folder in de cloud 
  * dwz: elke keer als een file lokaal op de laptop verandert zal de shared drive proberen om de folder in de cloud aan te passen 
  * MAAR: als een java-file verandert en je IDE (IntelliJ) staat open, dan zal er automatisch vanalles achter de schermen gebeuren wat ook weer een aantal aanpassingen op de folder veroorzaakt, en dat veroorzaakt dus ook weer een sync van de shared drive
  * Hierdoor zal de sync op een gegeven moment in de problemen komen
  * Het effect is dan typisch: je runt je programma en je ziet een heel ander resultaat dan wat je zou verwachten met de code die je voor ziet staan
  * dit geldt ook voor andere programmeertalen uiteraard 

---
[prev](../04_collaboration_tool/04_conflicten_best_practices.md)
[next](../05_branches/01_branches.md)
