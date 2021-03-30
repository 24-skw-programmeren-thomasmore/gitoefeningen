# GitIgnore file

| .gitignore file: welke files en directories mogen nooit aan deze repo mogen toegevoegd worden |
| ---| 
 

* Sommige files mogen nooit gecommit worden!
* Namelijk files die altijd automatisch aangepast worden 
  * bvb: IDE config - die verandert als je look&feel of een setting aanpast in je IDE
  * bvb: files die gebuild worden vanuit de code - verandert altijd als je iets in je code aanpast
  * bvb: files die je programma aanmaakt - verandert altijd als je programma start
* Waarom is dit?
  * Deze files veranderen elke keer als je je project build/runt. Of elke keer als
je collega het project build/runt. Als je deze files toevoegt in git dan zal iedereen ze elke keer
moeten committen.
* Maak altijd een .gitignore file 
  * Maak een nieuwe file met de naam .gitignore. In deze file zet je alles wat je niet wil
committen.
  * deze moet in de root van je project staan
  * voor verschillende programmeertalen kan je .gitignore files downloaden (of laten genereren door github)  
  * Add en commit de .gitignore file in je repository
* Example gitignore files: https://github.com/github/gitignore
* Bvb een typische .gitignore file voor een java project voor een developer die met Jetbrains
Intellij werkt:
    ```
    .idea
    *.iml 
    *.class
    *.log
    *.jar
    *.war
    *.nar
    *.ear
    *.zip
    *.tar.gz
    *.rar
    hs_err_pid*
    ```

| elk project moet een .gitignore file hebben |
| ---| 


---
[prev](/06_git_init_met_intellij.md)
[next](../02_time_travel/01_history.md)

