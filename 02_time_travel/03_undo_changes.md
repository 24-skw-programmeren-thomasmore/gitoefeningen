# Undo changes 

## Undo unstaged change: git checkout 

* Dus: je hebt een aanpassing gedaan die je niet meer wil. 
* Je wil terug naar de situatie van de laatste commit.


### In Git Bash 
* doe een checkout van de laatste commit: 

```
    cd gittest
    git status
    <pas de file aan>
    git status
    <we willen nu de aanpassingen rollbacken:> 
    git checkout <aangepaste file>
    git status
```

### In IntelliJ 
* open het commit-window (klik op Commit in de linker marge)
* rechts-klik op "default change list"
* kies "Rollback" 

## Undo staged change: git reset HEAD 

* Dus: je hebt een aanpassing gedaan en deze gestaged (git add .)
* Je wil terug naar de situatie van de laatste commit.

### In Git Bash
```
    cd gittest
    git status
    <pas de file aan>
    git add . 
    git status
    <we willen nu de aanpassingen rollbacken:> 
    git reset HEAD
    git status
```

### In IntelliJ
* in IntelliJ zie je niet echt het verschil tussen staged en niet-staged (dat gebeurt achter de schermen door in het commit window de files te selecteren)
* open het commit-window (klik op Commit in de linker marge)
* rechts-klik op "default change list"
* kies "Rollback"


## Undo last commit

### In Git Bash

### In IntelliJ


---
[prev](02_go_back_in_time.md)
[next]()
