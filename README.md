# Werken met git

Git is een gratis en opensource gedistribueerd versiebeheersysteem om je (software)broncode te managen.

In het vak Advanced Programming zullen we zo veel mogelijk git gebruiken voor het beheren van projecten, opdrachten, oplossingen, ...

![Three tree architecture](https://github.com/vives-advprog/werken-met-git/blob/master/images/threetree.png "Three tree architecture")

![Git Workflow](https://github.com/vives-advprog/werken-met-git/blob/master/images/workflow.png "Git Workflow")

* [Werken met git via de command line](#enable-version-control)
* [Werken met git in Intellij](#check-out-a-project-from-a-remote-host--clone-)

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

[Een voorbeeld die voldoende is voor tijdens het vak Advanced Programming vind je hier](https://github.com/vives-advprog/fop-gitignore/blob/master/.gitignore)

> Voeg dit .gitignore bestand toe aan ieder project dat je wil bijhouden in een git-repository. Voeg dit bestand toe nog voor je een eerste commit doet!
