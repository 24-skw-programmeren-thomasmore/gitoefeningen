# Go back in time 

## Git checkout 
Met het git commando "**git checkout**" kan je rondspringen in je commit history.
Je gaat dan terug naar de status van je working directory zoals die was op het moment van die commit. 

### In Git Bash: 
  ```
  cd gittest
  git status
  git log
  git checkout <commithash>
  git log
  ```

* Bekijk de inhoud van je working directory (de files) 
* In de “git log” zie je alleen de commits tot en met de gekozen commit.
* Met het volgende commando zie jse weer alle commits: 
```
git log --all --graph --decorate
```

### In Intellij: 
* selecteer een commit 
* rechts-klik en selecteer "checkout Revision <commit hash>" 
* Bekijk de inhoud van je working directory (de files)

## Wat is HEAD? 

* De **HEAD** is je huidige gezichtspunt op je repository (point of view).
* Je kan naar een ander viewpoint springen met “git checkout”, de HEAD revision zal dan naar
een andere commit wijzen. 
* We zullen later ook zien dat we met “git checkout” ook naar een andere branch kunnen springen.
* Je kan zien waar je HEAD staat met “git status”.
* In IntelliJ is de HEAD aangeduid met een geel labeltje

![checkout_head.png](images/checkout_head.png)

* Als je een **commit** doet, dan gaat HEAD naar deze nieuwe commit (want dat is je nieuwe
“point of view” na je commit).

![checkout_head_na_commit.png](images/checkout_head_na_commit.png)

* Na de “git checkout \<commithash>” zie je in git bash deze boodschap:

```
You are in 'detached HEAD' state. You can look around, make experimental changes
and commit them, and you can discard any commits you make in this state without
impacting any branches by performing another checkout.
```
* Als je het command "git status" nu gebruikt zie je : 
```
HEAD detached at 001961a
```

* Dit betekent dat je geen commits kan doen.
* Want een commit wordt altijd toegevoegd na HEAD, maar… daar staat nu al iets… (the place
of the “next commit” is “already taken”).

![checkout_head_detached.png](images/checkout_head_detached.png)

## Hoe geraak je uit een detached head state? 
* Doe een checkout van een branch (dus niet van een commit): bvb van de default branch main (of master)
```
git checkout main
```

* Als je dit doet dan zal HEAD terug naar de laatste commit van branch master wijzen. En kan je terug committen.
  
![checkout_head_na_commit.png](images/checkout_head_na_commit.png)


* Check altijd welke branch actief is  
  * Git Bash: gebruik "git status" 
  * IntelliJ: rechts onderaan in de marge  


---
[prev](01_history.md)
[next](03_undo_changes.md)
