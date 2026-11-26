<!--
@license
Copyright (c) ggdna

Use of this source code is governed by terms that can be
found in the LICENSE file in the root of this package.
-->

# Leitfaden zur Domäne

Ebene 2 von 7, Problemraum. Skill: `/layers-domain`.

## Wissen, was diese Ebene ist <a id="know-what-this-layer-is"></a>

- Was in der realen Welt vor jedem Produkt existiert: Konzepte, Begriffe,
  Prozesse, mentale Modelle
- Beobachtung, nicht Design

## Entscheiden <a id="decide"></a>

- Welche zentralen Konzepte es gibt und wie sie zusammenhängen
- Welche Wörter Menschen verwenden, und wo sie sich widersprechen
- Wo die Nahtstellen sind: Gruppen, die dasselbe Wort unterschiedlich
  verwenden
- Welche Ereignisse und Prozesse die Domäne über die Zeit strukturieren

## Ehrlich bleiben <a id="keep-it-honest"></a>

- Widersprüche festhalten, nicht auflösen; die Auflösung gehört ins
  Konzeptmodell
- In der realen Welt bleiben; Gespräche über Produkt oder Oberfläche
  zurückweisen
- Nomen als Objekt / Attribut / Instanz / unklar markieren, wenig filtern
- Sagen, wenn Überzeugungen des Teams statt erforschter Fakten abgebildet
  werden

## Eine Technik wählen <a id="pick-a-technique"></a>

| Situation                            | Technik                              |
| ------------------------------------ | ------------------------------------ |
| Beziehungen unklar                   | Concept Map (`graph TD`)             |
| Sprache umstritten                   | Begriffs-Audit                       |
| Gruppen gehen auseinander            | Bounded-Context-Mapping              |
| Prozesslastige Domäne                | Domain Event Storming                |
| Wissen steckt in Menschen            | Experteninterviews, Shadowing        |
| Domäne erzeugt Formulare, Rechnungen | Analyse von Dokumenten und Artefakten |
| Etablierter Markt                    | Wettbewerbsanalyse                   |

## Festhalten <a id="capture"></a>

- Concept Map, falls sie sich ihren Platz verdient hat
- Begriffskonflikte und Bounded Contexts
- Zentrale Ereignisse
- Nomen-Ernte

## Weitermachen <a id="continue"></a>

Die Nomen-Ernte ist das Rohmaterial des
[Konzeptmodells](conceptual-model-guide.md).
