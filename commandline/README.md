# Werken met git via de command line

  * [git configureren](#git-configureren)
  * [Nieuwe repository](#nieuwe-repository)
  * [Lokale aanpassingen](#lokale-aanpassingen)
  * [Geschiedenis opvragen](#geschiedenis-opvragen)
  * [Synchroniseren van aanpassingen](#synchroniseren-van-aanpassingen)
    + [Local naar remote repository](#local-naar-remote-repository)
    + [Remote naar local repository](#remote-naar-local-repository)
  * [Een goeie git workflow](#een-goeie-git-workflow)
  * [.gitignore](#gitignore)

## git configureren
Je username instellen die zichtbaar zal zijn bij iedere commit
```
git config --global user.name "[name]"
```

Je emailadres instellen dat zichtbaar zal zijn bij iedere commit
```
git config --global user.email "[voornaam.familienaam@student.vives.be]"
```

## Nieuwe repository
Bestaat er reeds een remote repository (bv. op GitHub) dan kan je deze repository clonen (= downloaden van het project met volledige versie geschiedenis)
```
git clone https://github.com/vives-advprog/eenrepository.git
```

Bestaat er nog geen remote repository, maar je hebt wel al lokaal files (code) staan. Maak dan een lokale repository aan
```
git init
```
De map waarin je dit command hebt uitgevoerd is nu een lokale git repository. Een .git folder (hidden folder) wordt toegevoegd aan die map

## Lokale aanpassingen
Welke files zijn er nieuw en/of gewijzigd in mijn working directory sinds m'n laatste commit? Op welke branch werk ik?
```
git status
```

Bestanden van working directory toevoegen aan staging directory. (= klaar maken voor _versioning_)
Of maw: voeg de wijzigingen aan bestand ``Persoon.java`` toe aan de volgende commit
>Working directory > staging directory
```
git add Persoon.java
```

Commit alle bestanden die je hebt toegevoegd aan de staging directory.
>Staging directory > local repository
```
git commit -m "een duidelijke omschrijving van je wijzigigen"
```

![Three tree architecture](https://github.com/vives-advprog/werken-met-git/blob/master/images/threetree.png "Three tree architecture")

## Geschiedenis opvragen
Toon alle commits, starten met de nieuwste
```
git log
```

## Synchroniseren van aanpassingen
### Local naar remote repository
Heb je in een eerste fase een `git clone https://...` uitgevoerd, dan bestaat er reeds een link tussen je lokale repository (op je laptop) en je remote repository (bv op GitHub)

Je code doorsturen naar de remote repository kan nu heel makkelijk door:
```
git push
```
Alle commits in je lokale repository zullen nu worden doorgevoerd/geupload in je remote repository

___
Ben je echter gestart met eerst een lokale repository op te zetten door `git init` uit te voeren, dan moet je nog een link leggen tussen je lokale repository (op je laptop) en je remote repository (bv op GitHub)

Hoe ga je te werk:
* Maak een nieuwe **lege** remote repository aan op GitHub (of je krijgt die van de docenten)
* Leg connectie met je remote repository: ``git remote add origin <URL remote repo>``
* Push je lokale repository naar je remote repository: ``git push -u origin master``

vb:
```
git remote add origin https://github.com/githubusername/myremoterepository.git
git push -u origin master
```

Vanaf nu kan je ook heel makkelijk door enkel ```git push``` uit te voeren je code naar de remote repository sturen

___

``git push`` commando neemt 2 argumenten
```
git push <RemoteName> <BranchName>
```

### Remote naar local repository
Je werkt met meerdere aan hetzelfde project en je versie op je lokale repository loopt achter met de versie op je remote repository. Je medestudent(en) hebben dus reeds wijzigen doorgevoerd op de remote repository die jij nog niet staan hebt. Uiteraard wil je deze ook

Deze kan je ophalen als volgt:
```
git pull
```

## Een goeie git workflow
Eenmaal je remote repository er staat en deze gesyncht is met je lokale repository is volgende workflow aan te raden om met git te werken
```
git add <file>
git commit -m "message"
git pull
git push
```

## .gitignore
Voeg in de root van je git repository een hidden text file toe: _.gitignore_ (schrijfwijze is van belang).

De hidden file .gitignore staat dus naast de hidden map /.git in je projectmap

In dit bestand kan je een opsomming geven van bestanden of mappen uit je project die je liever niet in je git repository wenst.

Dit kunnen bijvoorbeeld zijn:
* gebruikersspecifieke bestanden met de settings van je IDE bv.
* Bestanden en mappen die gegeneerd worden. Bv: target folder nu het builden van een project
* logfiles van je applicatie
* dependencies die via maven beheerd worden
* ...

> Voeg een .gitignore bestand toe aan ieder project dat je wil bijhouden in een git-repository. Voeg dit bestand toe nog voor je een eerste commit doet!

Volgende inhoud neem je minstens op in ieder `.gitignore` bestand binnen een Java project in Intellij
```
### IntelliJ IDEA ###
/.idea/
*.iws
*.iml
*.ipr
target/
out/

### Mac OS ###
.DS_Store
```
