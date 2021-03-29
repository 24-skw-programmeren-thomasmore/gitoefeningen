# Installeer Git 

## Download en installeer 
* Windows: 
  * https://git-scm.com/downloads 
  * In de wizard:
    * Select Components >  Selecteer Windows Explorer integration:  
    ![img.png](images/git_setup.png)
      
    * Default editor: kies bvb notepad++ (of notepad)
    * Laat verder alle defaults staan
* Mac: 
  * Best via de Homebrew package manager 
  * Installeer xcode command line tools - in terminal:    
    ```xcode-select –install```    
  * en volg de instructies 
  * Installeer homebrew - in terminal (op 1 lijn): 
    ```/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"```
  * Installeer git -- in terminal: 
    ```brew install git```
    
## Configureer git 
* In Git Bash (Windows) of terminal (Mac) typ je:
```
git config --global user.name "<jouw naam>"
git config --global user.email <jouw e-mailadres>
```
* user.name is de naam die je zal zien als je code commit.
* noot: Values met een spatie of een ander special character zet je altijd tussen dubbele quotes
* Check dit:
    ```git config –global -l```
* Als je iets fout gezet hebt:
    ```git config –global -replace-all user.name "<new Name>"```

---
[prev](01_wat_is_git.md)
[next]()