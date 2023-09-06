# Git

Git is een gratis en opensource gedistribueerd versiebeheersysteem om je (software)broncode te managen.

In het vak Advanced Programming zullen we zo veel mogelijk git gebruiken voor het beheren van projecten, opdrachten, oplossingen, ...

* [Werken met git via de command line](https://github.com/vives-advprog/werken-met-git/tree/master/commandline)
* [Werken met git in Intellij](https://github.com/vives-advprog/werken-met-git/tree/master/intellij)

![Git Workflow](https://github.com/vives-advprog/werken-met-git/blob/master/images/workflow.png "Git Workflow")

## .gitignore
Voeg in de root van je git repository een hidden text file toe: _.gitignore_ (schrijfwijze is van belang).

In dit bestand kan je een opsomming geven van bestanden of mappen uit je project die je liever niet in je git repository wenst.

Dit kunnen bijvoorbeeld zijn:
* gebruikersspecifieke bestanden met de settings van je IDE bv.
* Bestanden en mappen die gegeneerd worden. Bv: target folder nu het builden van een project
* logfiles van je applicatie
* dependencies die via maven beheerd worden
* ...

Inhoud .gitignore bestand voor Java projecten in Intellij
```
### Intellij ###

# .idea folder
.idea/

# File-based project format
*.iws
*.iml
*.ipr

# IntelliJ
out/
target/

# mpeltonen/sbt-idea plugin
.idea_modules/

### Mac OS ###
.DS_Store
```
