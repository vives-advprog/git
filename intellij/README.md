# Werken met git in Intellij

## Nieuwe repository

Bestaat er reeds een remote repository (bv. op GitHub) dan kan je deze repository clonen (= downloaden van het project met volledige versie geschiedenis)

Open Intellij (zonder project). Je ziet het start/splash screen
![Intellij splash](https://github.com/vives-advprog/werken-met-git/intellij/images/blob/master/images/IntellijSplash.png 'Intellij splash')

Kies voor `get from version control`

Geef de url van de remote repository op in het veld URL en bepaal in welke directory je het project wil clonen.
![git clone](https://github.com/vives-advprog/werken-met-git/intellij/images/blob/master/images/gitClone.png 'git clone')

Bestaat er nog geen remote repository, maar je hebt wel al lokaal files (code) staan. Maak dan een lokale repository aan

```
git init
```

De map waarin je dit command hebt uitgevoerd is nu een lokale git repository. Een .git folder wordt toegevoegd aan die map
