# Werken met git

Git is een gratis en opensource gedistribueerd versiebeheersysteem om je (software)broncode te managen.

## Commando's
### Nieuwe repository
Bestaat er reeds een remote repository (bv. op GitHub) dan moet je deze repository clonen
``
git clone https://github.com/vivesfop2/fop-gitignore.git
``

Bestaat er nog geen remote repository, maar je hebt wel al lokaal files (code) staan. Maak dan een lokale repository aan
``
git init
``
De map waarin je dit command hebt uitgevoerd is nu een lokale git repository. Een .git folder wordt toegevoegd aan die map

### Lokale aanpassingen
Welke files zijn er gewijzigd in mijn working directory? Op welke branch werk ik
``
git status
``

Bestanden van working directory toevoegen aan staging directory. Of maw: voeg de wijzigingen aan bestand `Persoon.java` toe aan de volgende commit
```
git add Persoon.java
```
Working directory > staging directory

Commit alle bestanden die je hebt toegevoegd aan de staging directory
```
git commit -m "een duidelijke omschrijving van je wijzigigen"
```
Staging directory > lokale repository

### Geschiedenis opvragen
Toon alle commits, starten met de nieuwste
```
git log
```

### Publiceren naar remote repository
Heb je in een eerste fase een ```git clone https://...``` uitgevoerd, dan bestaat er reeds een link tussen je lokale repository (op je laptop) en je remote repository (bv op GitHub)

Je code doorsturen naar de remote repository kan nu heel makkelijk door:
```git push```
Alle commits in je lokale repository zullen nu worden doorgevoerd op je remote repository

Ben je echter gestart met eerst een lokale repository op te zetten door ```git init``` uit te voeren, dan moet je nog een link lekken tussen je okale repository (op je laptop) en je remote repository (bv op GitHub)
Hoe ga je te werk:
* Maak een nieuwe **lege** remote repository aan op GitHub (of je krijgt die van de docenten)
* Leg connectie met je remote repository: ```git remote add origin <URL remote repo>```
* Push je lokale repository naar je remote repository: ```git push -u origin master```

Vanaf nu kan je ook heel makkelijk door enkel ```git push``` uit te voeren je code naar de remote repository sturen
