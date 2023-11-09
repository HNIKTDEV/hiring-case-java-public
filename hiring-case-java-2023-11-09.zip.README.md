# Komme i gang med hiring-case-java-2023-11-09.zip

## Last ned hiring-case-java-2023-11-09.zip(.sha256sum)

Gå til [hiring-case-java-public](https://github.com/HNIKTDEV/hiring-case-java-public), om du ikke allerede leser dette der.

Du må laste ned:

1. [hiring-case-java-2023-11-09.zip](https://github.com/HNIKTDEV/hiring-case-java-public/raw/main/hiring-case-java-2023-11-09.zip)

2. [hiring-case-java-2023-11-09.zip.sha256sum](https://github.com/HNIKTDEV/hiring-case-java-public/raw/main/hiring-case-java-2023-11-09.zip.sha256sum)

Du behøver en Github-konto for å følge instruksjonene under, dersom du ikke har dette kan du [opprette en konto her](https://github.com/signup). Om du ønsker å sette opp utviklingsmiljøet på annen måte så kommer det noen tips på slutten av denne filen.

## Sett opp utviklingsmiljø i Github Codespaces

### Lag *repository*

Logg inn på [Github](https://github.com) dersom du ikke er logget inn allerede.

Gå til [github.com/new](https://github.com/new) for opprette ett nytt privat *repository*.

Velg ditt brukernavn på Github i nedtrekksmenyen ved *Owner*.

På *Repository name* skriv inn hiring-case-java-\<kandidatens navn>. For eksempel `hiring-case-java-kari-nordmann`.

Trykk på knappen med teksten *Create repository*.

### Last opp filer til *repository*

I forrige steg opprettet du ett tomt *repository* på github. Gå til det nye *repositoriet*. I ruten *Quick setup ..* kan du velge *uploading an existing file*. Trykk på lenken.

Merk og trekk følgende filer fra lokal PC og inn i nettleservinduet for å laste opp filene til Github.

- `hiring-case-java-2023-11-09.zip`
- `hiring-case-java-2023-11-09.zip.sha256sum` 

Legg til en *commit* melding og trykk på knappen *Commit changes*. Du skal nå ha lastet opp det du trenger til Github.

### Sett opp utviklingsmiljø

I forrige steg ble nødvendige filer lagret i *repositoriet*. Fra *repositoriet* sin hovedside, trykk på knappen *\<> Code*. I menyen velg tab med tittel *Codespaces*. Du vil se en knapp som sier *Create codespace on main*.

Når Github Codespaces er startet opp, valider oppgavefilene i terminalvinduet som kommer til synet.

```sh
sha256sum -c hiring-case-java-2023-11-09.zip.sha256sum # Forventet svar er hiring-case-java-2023-11-09.zip: OK
```

Pakk ut zip fil.

```sh
unzip hiring-case-java-2023-11-09.zip # Du vil bli spurt om å skrive inn passord
```

Etter at filene er pakket ut, legg til de nye filene til git repoet.

```sh
git add -A
git commit -m "Pakket ut hiring-case-java-2023-11-09.zip."
git push origin
```

Github Codespaces kontainer vil behøve en gjenoppbygging ettersom `.devcontainer/devcontainer.json` inneholder oppsett for utviklingsmiljøet.

Trykk *F1*-tasten og ett kommandovindu vil dukke opp i VSCode. Skriv *Codespaces: Rebuild Container*, velg denne. Trykk *Rebuild* på dialogvinduet som dukker opp.

Neste steg er å lese [README.md](README.md) som du har pakket ut av `hiring-case-java-2023-11-09.zip`.

## Alternative måter å sette opp utviklingsmiljøet på

### Devcontainers

Utviklingsmiljø i Devcontainers vil være veldig likt Github Codespaces, og du vil ikke behøver en Github konto. Oppsettet er testet i lokal Devcontainers i tillegg og bør i teorien fungere ok. Sjekk ut [installasjonveiledning på code.visualstudio.com](https://code.visualstudio.com/docs/devcontainers/containers#_installation) for å komme i gang.

### Nix og NixOS

Zip-filen inneholder grunnleggende konfigurasjon for å komme i gang med Java-utvikling i [Nix og NixOS](https://nixos.org/). Det kan du gjerne tilpasse videre.

* Oppsett av Nix java miljø: `echo "use flake" >> .envrc`
* Kjør: `direnv allow` og java er installert.

### Manuelt oppsett

Utenom en IDE/editor så vil du normalt behøve følgende verktøy.

* JDK 17 eller nyere.
* Docker
* Node
* Maven
* Git

Opprettelse av lokalt Git *repository* foregår gjerne med følgende steg. Du kan legge inn *ditt* navn og epost dersom du ikke har satt opp dette globalt tidligere.

```sh
$ git init
$ git config user.name "Ditt navn her"
$ git config user.email epost@eksempel.no
$ git add .
$ git commit -am "Initial commit"
```