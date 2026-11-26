<!--
@license
Copyright (c) dnaCopyrightHolder

Use of this source code is governed by terms that can be
found in the LICENSE file in the root of this package.
-->

# Leitfaden zum Konzeptmodell

Ebene 5 von 7, Lösungsraum. Skill: `/layers-conceptual-model`.

## @layer Wissen, was diese Ebene ist <a id="know-what-this-layer-is"></a>

- Die Objekte, die das Produkt kennt, ihre Beziehungen, Zustände und
  Begriffe — unabhängig von jeder Oberfläche
- Die am meisten vernachlässigte tragende Ebene; ihr mehr Aufmerksamkeit
  geben, als sich bequem anfühlt
- Nicht das mentale Modell der Nutzer, kein Datenbankschema

## @decide Entscheiden <a id="decide"></a>

- Welche Objekte es gibt und wo ihre Grenzen liegen
- Wie Objekte zusammenhängen: Kardinalität und benannte Rollen
- Was ein Nutzer mit jedem Objekt tun kann
- Welche Zustände und Übergänge zählen
- Ein Name pro Konzept, ein Konzept pro Name

## @honest Ehrlich bleiben <a id="keep-it-honest"></a>

- Nur echte Objekte: instanziierbar, strukturiert, nützlich; „CAC“ ist eine
  Instanz von Metric
- Ein Attribut, das ein anderes Objekt benennt, als Beziehung modellieren
- Keine spekulativen Ergänzungen; jedes Element geht auf ein benanntes
  Bedürfnis zurück
- Kann-ein-Objekt-sein heißt nicht Soll-eigenständig-sein; Persistenz mit
  einem konkreten Ablauf begründen, Wetten als vorläufig markieren
- Allgemeine Verben aufteilen, die unterschiedliche Folgen verbergen: eine
  Adresse korrigieren vs. einen Umzug melden
- Gespräche über Implementierung auf das lenken, was der Nutzer tun kann

## @technique Eine Technik wählen <a id="pick-a-technique"></a>

| Situation                            | Technik                                     |
| ------------------------------------ | ------------------------------------------- |
| Material zum Auswerten               | Noun Foraging, OOUX                         |
| Ein Objekt unklar                    | Objektdefinition                            |
| Objekthaftigkeit unsicher            | Zuerst den Ablauf skizzieren, dann formalisieren |
| Beziehungen zu prüfen                | Relationale Objektkarte (`erDiagram`)       |
| Status ändert, was erlaubt ist       | Zustandsdiagramm (`stateDiagram-v2`)        |
| Verben uneinheitlich                 | Aktionsinventar über alle Objekte           |
| Benennung umstritten                 | Liste der Ubiquitous Language               |
| Redesign                             | Das bestehende Produkt durchgehen           |

Die zeitlichen Entscheidungen abklopfen: Zwischenzustände, Leseverzögerung,
Beziehung über die Zeit, Semantik des Löschens, Historie.

## @capture Festhalten <a id="capture"></a>

- Feststehende Objektdefinitionen, vorläufige markiert
- Diagramme, die eine echte Beziehung oder einen Lebenszyklus abbilden
- Begriffsentscheidungen mit verworfenen Alternativen
- Offene Fragen an die Entwicklung

## @continue Weitermachen <a id="continue"></a>

Wenn Objekte und Aktionen stabil sind, gestalten, wie Nutzer sich durch sie
bewegen: [Interaktionsablauf](interaction-flow-guide.md).
