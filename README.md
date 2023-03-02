# Forberedelser

## Last ned og installer følgende

* IDE of choice, men vi kan foreslå [IntelliJ Community Edition](https://www.jetbrains.com/idea/download/), og/eller [VSCode](https://code.visualstudio.com/).
* [Thunder Client](https://marketplace.visualstudio.com/items?itemName=rangav.vscode-thunder-client) plugin i [VSCode](https://code.visualstudio.com/), evntuelt `curl` fra kommandolinjen.
* [Java 17 JDK](https://www.oracle.com/java/technologies/downloads/#jdk17-windows) eller nyere, eventuelt [OpenJDK](https://openjdk.org/install/).
  * [Link til oppsett](https://javatutorial.net/set-java-home-windows-10) på Windows.
* [Git](https://git-scm.com/downloads).
* [Maven](https://maven.apache.org/download.cgi).
  * [Link til oppsett](https://www.mkyong.com/maven/how-to-install-maven-in-windows/) på Windows.
* [Docker Desktop](https://docs.docker.com/compose/install/)/docker-compose.

# Gjennomføring

Last ned [hiring-case-java.zip](./hiring-case-java.zip) og pakk den ut til ett passende sted. Du skal ha mottatt ett passord for å åpne innholdet i en epost fra oss. I den utpakkede mappen vil du finne en `README.md` fil som veileder deg videre.

# Levering

Når du er ferdig med oppgavene, lag en ny ZIP fil med din besvarelse og gi denne ett passende navn ala `hiring-case-java-kandidatens-navn.zip`. Pass på at du får med `.git` mappen. Legg gjerne ved en hash av filen slik at vi kan sjekke integriteten til filen vi mottar. I "Git Bash" eller kommandolinje på Mac/Linux kan du kjøre kommandoen `sha256sum hiring-case-java-kandidatens-navn.zip` for å generere hash.

Besvarelsen sendes som ett vedlegg i epost. Hvilken epost-adresse besvarelsen skal sendes til, samt tidsfrist, står beskrevet i epost fra oss.

Lykke til.

## Feil i oppgavetekst

 * Oppgave 4: `Lever en liste over alle - f.eks listAllMaleFirstNames()` skulle nok vært `Lever en liste over alle - f.eks listAll()`.
