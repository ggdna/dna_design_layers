# dna_design_layers

[English](README.md) | Deutsch

Gibt einem Repo die Guides und Skills, um die sieben Schichten des
Produktdesigns durchzuarbeiten, vom beobachteten Verhalten bis zur
Oberfläche.

## Motivation

Produktentscheidungen bauen aufeinander auf: Was Nutzer tun und was die
Domäne vorgibt, kommt vor den Bedürfnissen, die Bedürfnisse vor der
Strategie, die Strategie vor dem konzeptuellen Modell, dem Ablauf und der
Oberfläche. Eine schwache untere Schicht belastet jede darüber. Die
Schicht gibt einem Repo eine Methode, diese Entscheidungen Schicht für
Schicht zu treffen, mit einem Skill pro Schicht, den ein Agent in einer
Design-Session ausführen kann, und Entscheidungen statt Mitschriften
festzuhalten. Die Guides und Skills entstanden in dna_plan und sind als
eigene Schicht hierher umgezogen.

## Verwendung

Als Dev-Dependency eintragen und einmal initialisieren:

```bash
pnpm add -D @ggdna/dna-design-layers   # TypeScript projects
dart pub add dev:dna_design_layers     # Dart projects
gg dna init
```

`gg dna init` legt einen Test ab, der die DNA bei jedem Testlauf
instanziiert und prüft. Er legt die Guides in `doc/guides/` und
`doc/guides/layers/` ab und die Skills in `.claude/skills/layers-*/`.

Tippe zu Beginn einer Design-Session `/layers-intro` in Claude Code.
Starte `/layers-orient`, wenn unklar ist, welche Schicht Aufmerksamkeit
braucht: Der Skill prüft alle sieben Schichten und empfiehlt eine. Danach
startest du den Skill der Schicht, an der du arbeitest.

## Guides

- `dna/doc/guides/layers-guide.md` — das Schichtensystem, Design als
  Entscheiden, wie man die Skills nutzt, wo die Ergebnisse festgehalten
  werden
- `dna/doc/guides/layers/` — ein kurzer Guide pro Schicht, jeweils eine
  Sammlung von Techniken für die Entscheidungen dieser Schicht:
  `observed-behaviour-guide.md`, `domain-guide.md`,
  `user-needs-guide.md`, `product-strategy-guide.md`,
  `conceptual-model-guide.md`, `interaction-flow-guide.md`,
  `surface-guide.md`, dazu `orient-guide.md` für die Prüfung über alle
  Schichten

## Skills

- `/layers-intro` — die Einführung in das Schichtensystem; zuerst laden,
  die anderen Skills bauen darauf auf
- `/layers-orient` — prüft alle sieben Schichten, nennt die
  Engpass-Schicht und empfiehlt, worauf man sich konzentriert
- `/layers-observed-behaviour` — plant Nutzerforschung und macht daraus
  Befunde mit Konfidenz dazu, was Nutzer tatsächlich tun
- `/layers-domain` — kartiert die Begriffe, widersprüchlichen Bezeichnungen
  und Bounded Contexts einer Domäne
- `/layers-user-needs` — erhebt und priorisiert Bedürfnisse, Schmerzpunkte
  und Wünsche, die in die Produktstrategie einfließen
- `/layers-product-strategy` — verbindet Chancen bei den Nutzern mit
  Geschäftszielen und Lösungswetten und prüft die riskantesten Annahmen
  mit wenig Aufwand
- `/layers-conceptual-model` — legt die Objekte, Beziehungen, Zustände und
  das Vokabular des Produkts fest, unabhängig von jeder Oberfläche
- `/layers-interaction-flow` — kartiert die Orte, Handlungsmöglichkeiten,
  Randfälle und Fehlerpfade eines Ablaufs, ohne sich auf eine visuelle
  Form festzulegen
- `/layers-surface` — prüft die Oberfläche gegen die Schichten darunter:
  Vokabular, Konsistenz, Feedback, Hierarchie, Barrierefreiheit

Jeder Skill liest den Guide seiner Schicht.

## Umfang

Die Schicht liefert die Methode, nicht die Ergebnisse. Wo die Ergebnisse
einer Design-Session landen — eine Entscheidung pro Datei in einem
Projektmanagement-Repo —, regelt
[dna_plan](https://github.com/ggdna/dna_plan); der Layers-Guide verweist
auf dessen PM-Repo-Guide, wenn das Repo ihn hat. Die Guides folgen
[layers-skills](https://github.com/jamiemill/layers-skills) von Jamie
Mill (MIT).

## Schichten

Die Schicht ist orthogonal: `dna/_dna.json` nennt keine Eltern-Schichten,
und sie bleibt bewusst ohne — eine Eltern-Schicht würde jeden Nutzer
dieses Themas erreichen, ob das Repo sie wollte oder nicht, und ein
Umbrella hier einzubinden würde einen Zyklus schließen, sobald dieses
Umbrella die Schicht listet.

Noch listet keine Umbrella-Schicht sie, auch `dna_ggdna` nicht: Ein Repo,
das das Thema will, trägt `dna_design_layers` in seine eigene
`dna/_dna.json` ein.

## Variablen

- `dnaCopyrightHolder` — der Name im Lizenzkopf jeder Datei;
  `dna/_dna.json` deklariert kein `mustOverride`, ein nutzendes Repo muss
  ihn also nicht setzen, und eines, das ihn nicht in seiner eigenen
  `dna/_vars.json` setzt, bekommt den Standardwert `ggdna`

## Entwicklung

Der Ordner `dna/` ist handgeschriebene Quelle und wird nie generiert. Das
Repo instanziiert seine eigene DNA — nach Änderungen `dart test` laufen
lassen; vorher committen, denn eine Datei, die die DNA überschreiben
würde, darf keine uncommittete Arbeit enthalten.

Bearbeite die Dateien unter `dna/`, nicht ihre Kopien in `doc/` und
`.claude/`, die der Test überschreibt.

## Lizenz

MIT — siehe [LICENSE](LICENSE).
