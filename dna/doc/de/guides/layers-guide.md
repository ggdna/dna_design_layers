<!--
@license
Copyright (c) dnaCopyrightHolder

Use of this source code is governed by terms that can be
found in the LICENSE file in the root of this package.
-->

# Leitfaden zu den Ebenen

## @layer Das Ebenensystem kennen <a id="know-the-layer-system"></a>

- „Layers of Product Design“ teilt Designarbeit in sieben Ebenen in drei
  Zonen auf; diese Leitfäden folgen
  [layers-skills](https://github.com/jamiemill/layers-skills) von Jamie
  Mill (MIT)
- Untere Ebenen sind das Fundament der oberen; eine schwache untere Ebene
  erzeugt Schulden in jeder Ebene darüber
- Auf jeder Ebene einsteigen, aber vor dem Aufbauen die Ebenen darunter
  prüfen

Problemraum — Wissen, das aus der Realität gewonnen wird:

- 1 [Beobachtetes Verhalten](layers/observed-behaviour-guide.md) — was
  Nutzer tatsächlich tun
- 2 [Domäne](layers/domain-guide.md) — was vor unserem Produkt existiert
- 3 [Nutzerbedürfnisse](layers/user-needs-guide.md) — was Nutzer erreichen
  wollen, und warum

Lösungsraum — bewusste Entscheidungen darüber, was gebaut wird:

- 4 [Produktstrategie](layers/product-strategy-guide.md) — welche
  Bedürfnisse wir bedienen, für welches Ergebnis
- 5 [Konzeptmodell](layers/conceptual-model-guide.md) — welche Objekte,
  Beziehungen und Begriffe
- 6 [Interaktionsablauf](layers/interaction-flow-guide.md) — welche Orte,
  Aktionen und Wege
- 7 [Oberfläche](layers/surface-guide.md) — was Nutzer sehen, lesen und
  hören

## @design Design als Entscheiden verstehen <a id="treat-design-as-decision-making"></a>

- Jede Ebene trifft Entscheidungen; Artefakte halten sie nur fest
- Vier Arten von Fortschritt: eine Entscheidung treffen, eine noch
  ungetroffene aufdecken, eine riskante bewerten, priorisieren
- Immer an einer Ebene arbeiten; Problemraum und Lösungsraum nicht mischen
- Schlechte Entscheidungen markieren, nicht nur fehlende
- Entscheidungen festhalten, keine Mitschriften; die Aufzeichnung kurz
  halten

## @skills Die Skills nutzen <a id="use-the-skills"></a>

- `/layers-intro` zu Beginn jeder Design-Sitzung laden
- `/layers-orient` ausführen, wenn unklar ist, welche Ebene Aufmerksamkeit
  braucht, siehe den [Orientierungs-Leitfaden](layers/orient-guide.md)
- Den Skill der Ebene ausführen, an der gearbeitet wird:
  `/layers-observed-behaviour`, `/layers-domain`, `/layers-user-needs`,
  `/layers-product-strategy`, `/layers-conceptual-model`,
  `/layers-interaction-flow`, `/layers-surface`
- Jeder Skill liest seinen Leitfaden; ein Leitfaden ist eine Bibliothek von
  Techniken, kein Drehbuch: eine Technik für die anstehende Entscheidung
  wählen, sie durcharbeiten, das Ergebnis festhalten

## @record Die Ergebnisse festhalten <a id="record-the-results"></a>

- Das Ergebnis einer Sitzung ins Projektmanagement-Repo schreiben, siehe
  den [PM-Repo-Leitfaden](pm-repo-guide.md#use-the-design-layers) der
  Ebene `dna_plan`, falls das Repo sie hat
- Eine Entscheidung pro Datei in `concepts/decisions`; alles andere in die
  Topic-, UX-, Ziel- oder Requirements-Datei, zu der es gehört
