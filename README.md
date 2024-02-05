# Strategibanken

## 1. Installation

### 1.1 Ruby

#### 1.1.1 Windows

Om du har [Chocolatey](https://chocolatey.org/): `choco install ruby`

Annars : [RubyInstaller for Windows](https://rubyinstaller.org/)

#### 1.1.2 MacOs

1. Installera [Homebrew](https://brew.sh/) 
2. `brew install ruby`

### 1.2 Asciidoctor

I strategibankens rotmapp: `bundle install`

## 2. Bygga boken lokalt

I strategibankens rotmapp: `asciidoctor -r asciidoctor-kroki -r asciidoctor-tabs docs/index.adoc`

Den färdigbyggda boken finns i `docs/index.html`

Öppna gärna `docs/index.html` med VS Code Live Server

### 2.1 Bygga boken lokalt automagiskt vid filändring

#### 2.1.1 Windows

Vet ej

#### 2.1.1 MacOs

`brew install fswatch`
`fswatch -o ./docs -e "index.html" | xargs -n1 -I{} asciidoctor -r asciidoctor-kroki -r asciidoctor-tabs docs/index.adoc`


## 3. Bygga boken till GH Pages.

Boken byggs automagiskt vid push till main-branchen på GitHub (kan ta några minuter).