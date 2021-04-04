# Pull Before Push

## Keep the main branch stable!  

* Als de features klaar zijn en getest, dan willen we uiteindelijk alle changes op de default branch main (of master)  
* We werken op feature branches om ervoor te zorgen dat **main altijd stabiel blijft** 
* Je mag dus nooit met een conflict mergen naar main!  

## Solve Conflict

* Hiervoor gebruiken we hetzelfde principe als [pull before push](../04_collaboration_tool/04_conflicten_best_practices.md)
* Dit principe gebruik je steeds als je van een "meer lokale" branch naar een "meer algemene" branch gaat
  * meer lokale branch = waarop je developt -- bvb feature branch  
  * meer algemene branch = waar je de code opzet als development klaar is -- bvb main (of dev)  
* Dus: 
  * checkout "feature branch" 
  * merge "main" into current (dus into feature branch)
  * solve conflicts
  * test 
  * checkout "main" 
  * merge "feature branch" into current 
  * dit is normaal gezien zonder conflicten 
    
    
## Oefening   
* checkout main 
* merge the_first_branch into main 
* resultaat: 
  * alle aanpassingen van the_first_branch zitten nu ook op main
  * main en the_first_branch zijn nu gelijk   

## Oefening
* feature 1
  * checkout main 
  * maak nieuwe branch feature_1, checkout  
  * pas een aantal files aan  
  * commit en push   
* feature 2 
  * checkout main
  * maak nieuwe branch feature_2, checkout
  * pas een aantal files aan (zonder conflicten met feature 1)
  * commit en push
* **merge feature 1 in main** 
  * feature 1 is klaar en getest dus moet gemerged worden naar main 
  * checkout feature_1 
  * merge main into feature_1 
  * noot: er is niks veranderd in main dus dit doet niks, maar het is een best practice om om dit uit gewoonte altijd te doen  
  * test
  * push   
  * checkout main 
  * merge feature_1 into main
  * noot: deze stap is normaal gezien zonder conflicten   
  * test 
  * push   
* **merge feature 2 in main**
    * feature 2 is ook klaar en getest dus moet gemerged worden naar main
    * checkout feature_2
    * merge main into feature_2
    * noot: **de code van feature_1 komt binnen in feature_2** !!!
    * **fix conflicts** indien nodig
    * test
    * push
    * checkout main
    * merge feature_2 into main
    * noot: deze stap is normaal gezien zonder conflicten
    * test
    * push

## Oefening
* doe nu hetzelfde als in de vorige oefening maar **met conflicten**   



---
[prev](06_merge_with_conflicts.md)

