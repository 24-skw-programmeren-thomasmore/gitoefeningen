# Branches 

| Zorg ervoor dat je eerst de [basisbegrippen](../01_getting_started/01_wat_is_git.md) begrijpt| 
|---|

## Wat is een branch? 
* Tot nu toe hebben we op 1 branch gewerkt: de default branch main (of master) 
* Dat wil zeggen: een commit wordt toegevoegd bovenop deze default branch
* Als je een nieuwe branch maakt en activeert (checkout)
  * dan worden commits toegevoegd bovenop deze nieuwe branch
  * je ziet deze commits dus niet meer in de default branch   

## Hoe werken we met branches? 
* typisch werk je elke feature af op een branch.
  * als je de branch van **feature1** actief maakt (checkout)
      * dan zie je enkel de code die gecommit is voor feature1 (en ouder) 
      * in git log zie je enkel de commits van feature1 (en de oudere commits)  
  * als je de branch van **feature2** actief maakt (checkout)
      * dan zie je enkel de code die gecommit is voor feature2 (en ouder)
      * in git log zie je enkel de commits van feature2 (en de oudere commits)
* als de feature klaar is (bvb feature1)
  * dwz getest!!! 
  * dan **merge** je de feature1 branch naar de default branch (main of master)  
  * als je nu de default branch (main of master) actief maakt (checkout)
      * dan zie je ook hier de code die gecommit is voor feature1 (en ouder)
      * in git log zie je nu ook de commits van feature1   
* dezelfde merge-principes gelden als bij [pull-push](../04_collaboration_tool/02_merges.md)
* let op: maak een branch per feature, niet per persoon

| branch features, not persons |
|---|

## Waarom werken we met branches?
* werken met verschillende branches is iets complexer, maar geeft wel meer **flexibiliteit**
* je houdt de default branch stabiel: 
  * hierop komen alleen de features die helemaal klaar zijn (en getest). 
  * op de default branch staat dus steeds code die de werkt en die recent is  
  * bvb als je een last-minute demo moet geven voor een klant heb je hier steeds een recente versie die werkt
* een feature die niet op tijd klaar geraakt kan je uitstellen tot de volgende release    
* let op: laat een branch niet te lang openstaan om grote conflicten te vermijden 
* noot: in de realiteit ga je nog extra tussenstappen inbouwen (dev-branch, test-branch) voor je gaat mergen naar je main (of master) branch. Dat is buiten de scope van deze cursus.   



---
[prev](../04_collaboration_tool/05_share_code_between_2_computers.md)
[next](02_branches_voorbeelden.md)

