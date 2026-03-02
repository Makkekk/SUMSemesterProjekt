

[git_guide_toc.md](https://github.com/user-attachments/files/25679919/git_guide_toc.md)
# Git & GitHub Arbejdsproces Guide

*Standard for projektgruppen*

------------------------------------------------------------------------

## Indholdsfortegnelse

1.  [Formål](#1-formål)
2.  [Grundprincipper](#2-grundprincipper)
3.  [Workflow](#3-workflow)
4.  [Pull Request proces](#4-pull-request-proces)
5.  [Commit standard](#5-commit-standard)
6.  [Recovery guide](#6-recovery-guide)
7.  [.gitignore standard](#7-gitignore-standard)
8.  [Kommando reference](#8-kommando-reference)
9.  [Ressourcer](#9-ressourcer)

------------------------------------------------------------------------

## 1. Formål

Dette dokument definerer den fælles Git‑standard for projektgruppen.\
Målet er:

-   Stabil kodebase
-   Ensartet workflow
-   Gennemsigtig historik
-   Minimal risiko for fejl

------------------------------------------------------------------------

## 2. Grundprincipper

**Main = stabil version**

Regler:

-   Rediger aldrig direkte i main
-   Brug altid branches
-   Brug Pull Requests
-   Minimum én godkendelse før merge
-   GitHub håndterer merge

------------------------------------------------------------------------

## 3. Workflow

### 3.1 Start arbejde

``` bash
git switch main
git pull
git switch -c feature/navn
```

### 3.2 Under arbejde

``` bash
git add .
git commit -m "beskrivelse"
```

Commit ofte.

------------------------------------------------------------------------

### 3.3 Upload branch

``` bash
git push origin feature/navn
```

------------------------------------------------------------------------

## 4. Pull Request proces

1.  Opret PR på GitHub\
2.  Skriv formål\
3.  Tilføj reviewers\
4.  Afvent review

**Review svar**

  Status            Betydning
  ----------------- ----------------
  Approve           Klar til merge
  Request changes   Ret fejl
  Comment           Kommentar

------------------------------------------------------------------------

## 5. Commit standard

**Format**

    Handling + objekt

**Gode** - Tilføjer login validation - Fikser routing bug - Refactorer
service layer

**Dårlige** - fix - ting - update

------------------------------------------------------------------------

## 6. Recovery guide

Hvis lokal kode skal nulstilles:

``` bash
git fetch origin
git reset --hard origin/main
```

⚠️ Sletter ALLE lokale ændringer.

------------------------------------------------------------------------

## 7. .gitignore standard

    bin/
    obj/
    .idea/
    *.user

------------------------------------------------------------------------

## 8. Kommando reference

  Kommando                   Funktion
  -------------------------- -----------------
  git clone `<url>`{=html}   Download repo
  git pull                   Opdater lokal
  git status                 Status
  git add .                  Stage
  git commit -m              Commit
  git push                   Upload
  git switch                 Skift branch
  git branch                 Liste
  git fetch                  Sync uden merge
  git reset --hard           Reset
  git log --oneline          Historik

------------------------------------------------------------------------

## 9. Ressourcer

-   GitHub Hello World\
-   Learn Git Branching\
-   GitHub Pull Request Docs

------------------------------------------------------------------------

## Versionshistorik

  Version   Dato   Ændring
  --------- ------ ---------------
  1.0       2026   Første udgave
