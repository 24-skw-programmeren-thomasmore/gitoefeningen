# Bestaand locaal project op Github zetten

* Je hebt een **lokaal project waar al files inzitten** en je wil dit op Github zetten

## maak local repo

* maak eerst een local repo van je project met "git init" 
  in [Git Bash](../01_getting_started/05_git_init.md) 
  of in [IntelliJ](../01_getting_started/06_git_init_met_intellij.md) 
* check de [.gitignore file](../01_getting_started/08_gitignore.md) 

| check de .gitignore file voor je commit en pusht! | 
|---|

* commit de files in je local repo  

## maak een lege repo op Github 
* Maak je eigen repository op Github:
* Ga naar Repositories
* Klik de New button
* Geef een repository name en description
* public or private ‐> kies best private
* je wil **geen** .ignore file en **geen** readme.md file
* Noot: als de repo op Github al files bevat kan het moeilijker zijn om die te connecteren met je bestaande local repo    
* Klik de “Create repository” button

## connecteer  
* connecteer je local repo met de nieuwe repo op Github
* check eerst de [.gitignore file](../01_getting_started/08_gitignore.md) op je local repo!

### in Git Bash: 
```
git remote -v
git remote add origin <URL-VAN-GITHUB-REPO>
git remote -v
```

* Het commando "git remote -v" toont welke remote repo geconnecteerd is met deze local repo
* Het 2e commando connecteert je local repo met deze github. De "alias" die we gebruiken voor deze remote is "origin"
* Noot: het is mogelijk om meerdere remote repo's te connecteren met een repo. Maar dat is buiten de scope van deze oefeningen. 
* Noot:**origin** is de naam die per conventie gebruikt wordt voor de eerste remote die je connecteert 

### in IntelliJ: 
* Menu > VCS > Share Project on Github... 


## Oefening
* maak een project op je computer en connecteer dit met een nieuwe repo op github 

---
[prev](03_connect_with_existing_github_repo.md)
[next](05_push.md)
