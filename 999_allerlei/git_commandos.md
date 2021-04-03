# Meest gebruikte git commando's


| Git commando|wat doet het |
|---|---| 
| git help  | toon mogelijke commando's | 
| git init  | maak deze directory bruikbaar voor git | 
| git status  | is working folder clean of dirty - wat is de actieve branch   | 
| git add <filename>  |  voeg de changes in deze file toe aan de changelist (voor volgende commit) | 
| git add .  |  voeg de changes in alle files in dir en subdirs toe aan de changelist (voor volgende commit) | 
| git add *  |   voeg de changes in alle files in dir toe aan de changelist (voor volgende commit)  (geen subdirs) | 
| git commit -m <message>  | vergeet message niet!!! | 
|    |  | 
| git log  |  toon de history (alle commits in actieve branch) | 
| git checkout main  |  maak de default branch main actief | 
| git checkout \<commithash>  |  ga naar deze commit - je bent dan in detached head en kan niet meer committen | 
| git checkout \<modified-file>  | rollback deze file  | 
| git reset HEAD  |  rollback van git add: voordat je gecommit hebt | 
| git reset HEAD~  | rollback na een commit | 
|    |  | 
| git clone  |  maak een lokale repo die een copy is van een bestaande repo | 
| git push  |  stuur commits in local repo naar de remote repo (voor actieve branch) | 
| git pull  |  stuur commits van remote repo naar local repo (voor actieve branch) | 
|   |  | 
| git status  |  welke branch is actief| 
| git branch  |  welke branches bestaan in local repo | 
| git branch -r |  welke branches bestaan in remote repo | 
| git branch -a | alle branches (local en remote) | 
| git checkout \<NAAM VAN DE BRANCH> | checkout: maak een branch actief | 

