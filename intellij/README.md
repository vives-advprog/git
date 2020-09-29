# Werken met git in Intellij

## Enable version control

Bestaat er nog geen remote repository, maar je hebt wel al lokaal sourcecode staan. Maak dan eerst een lokale repository aan.

Intellij menu: **VCS | Enable Version Control integration**

![Enable Version Control integration](https://github.com/vives-advprog/werken-met-git/blob/master/intellij/images/enableVersionControlIntegration.png 'Enable Version Control integration')

Kies `git` als Version Control system

![Version Control git](https://github.com/vives-advprog/werken-met-git/blob/master/intellij/images/versionControlGit.png 'Version Control git')

Het project waarin je dit hebt uitgevoerd is nu een lokale git repository. Een `.git` folder wordt toegevoegd aan die map

## Check out a project from a remote host (clone)﻿

Bestaat er reeds een remote repository (bv. op GitHub) dan kan je deze repository clonen (= downloaden van het project met volledige versie geschiedenis)

Open Intellij (zonder project). Je ziet het Welcom screen

![Intellij splash](https://github.com/vives-advprog/werken-met-git/blob/master/intellij/images/IntellijSplash.png 'Intellij splash')

Kies voor `Get from Version Control`

Of via Intellij menu: **VCS | Get from Version Control**

Geef de url van de remote repository op in het veld URL en bepaal in welke directory je het project wil clonen.

![git clone](https://github.com/vives-advprog/werken-met-git/blob/master/intellij/images/gitClone.png 'git clone')

Klik op clone

Merk langs de linkerkant van bovenstaand scherm onder "Repository URL" ook een mogelijkheid op om repositories gekoppeld aan je GitHub account te clonen. Hiervoor dien je je GitHub account toe te voegen in Intellij (zie verder in dit document voor meer info).

## Exclude files from version control (ignore)

Niet alle bestanden in het project wil je opnemen in version control.

Voeg een `.gitignore` bestand toe aan de root van je project.

Intellij menu: **New | File** met de naam `.gitignore`

Inhoud van de file: https://github.com/vives-advprog/fop-gitignore/blob/master/.gitignore

## Check project status﻿

In Intellij is het mogelijk om de status van je lokale directory te vergelijken met de repository versie van je project.

Intellij menu: **View | Tool Windows | Git**

![git status](https://github.com/vives-advprog/werken-met-git/blob/master/intellij/images/gitStatus.png 'git status')

* De **Default** lijst toont alle bestanden die zijn gewijzigd sinds de laatste keer dat je gesynchroniseerd hebt met de remote repository (blauw) en alle nieuwe bestanden die aan git zijn toegevoegd maar nog niet zijn gecommit (groen)

* De **Unversioned Files** lijst bevat alle bestanden die zijn toegevoegd aan het project, maar nog niet werden toegevoegd aan git (`git add <naam van het bestand>`)

## Add a remote repository﻿

Wanneer je een Git project hebt gecloned van een remote repository, dan is de link tussen je local repository en de remote repository meteen ingesteld.

Als je echter start vanaf een lokaal git project, een local repository, die je ook wil delen met andere via een remote git repository dan moet je de link naar de remote repository nog configureren in je git project.

Voorwaarde: Er bestaat reeds een lege remote repository (bv. op GitHub)
![leeg remote](https://github.com/vives-advprog/werken-met-git/blob/master/intellij/images/leegRemote.png 'leeg remote')

Intellij menu: **VCS | git | Remotes...**

Klik op de +

Name: origin

URL: <de url van de lege remote repository> (deze vind je terug in de blauwe balk op GitHub)

![Add remote](https://github.com/vives-advprog/werken-met-git/blob/master/intellij/images/addRemote.png 'add remote')

Ok

![Add remote ok](https://github.com/vives-advprog/werken-met-git/blob/master/intellij/images/addRemoteOk.png 'add remote ok')
