<!--
@license
Copyright (c) dnaCopyrightHolder

Use of this source code is governed by terms that can be
found in the LICENSE file in the root of this package.
-->

# Leitfaden zum Interaktionsablauf

Ebene 6 von 7, Lösungsraum. Skill: `/layers-interaction-flow`.

## @layer Wissen, was diese Ebene ist <a id="know-what-this-layer-is"></a>

- Die Orte, durch die sich ein Nutzer bewegt, die Affordanzen an jedem, der
  gezeigte Inhalt, der Ablauf zwischen Zuständen
- Über dem Modell (was existiert), unter der Oberfläche (wie es aussieht)
- Immer für einen Nutzer in einer Situation, der einen Job erledigt

## @decide Entscheiden <a id="decide"></a>

- Durch welche Orte der Ablauf führt
- Was der Nutzer an jedem Ort tun kann, und wohin es führt
- Welchen Inhalt jeder Ort zeigt
- Was bei Fehlern, leeren Zuständen und Randfällen passiert
- Ob der Ablauf so einfach ist, wie er sein kann

## @honest Ehrlich bleiben <a id="keep-it-honest"></a>

- Jede Affordanz hat ein benanntes Ziel
- Randfälle sind Pflichtschritte: Validierung, Serverfehler,
  Verbindungsabbruch, Timeout, gleichzeitige Bearbeitung, leer, Laden, nach
  der Aktion, Abbrechen
- Keine zerrissenen Objekte: Attribute und Aktionen eines Objekts bleiben
  zusammen
- Keine isolierten Objekte: Jede Beziehung ist navigierbar oder bewusst
  nicht
- Das Vokabular stimmt mit der Ubiquitous Language überein
- Orte für Nutzer benennen; mehr als 5–6 Orte pro Job sind ein Signal

## @technique Eine Technik wählen <a id="pick-a-technique"></a>

| Situation                          | Technik                          |
| ---------------------------------- | -------------------------------- |
| Standard                           | Breadboarding                    |
| Ungetroffene Entscheidungen finden | Den Ablauf als Nutzer durchgehen |
| Viel zu planen, viele Nutzer       | User Story Mapping               |
| Redesign                           | Aufgabenanalyse                  |
| Kanäle und Backstage               | Service Blueprinting             |
| Nur zur Orientierung               | Ablaufdiagramm (`graph LR`)      |

Breadboard-Notation:

```text
Place name
- affordance → destination place
[ content shown in this place ]
```

## @capture Festhalten <a id="capture"></a>

- Das Breadboard: Orte, Affordanzen, Ziele, Inhalt, Bedingungen
- Ein Ablaufdiagramm, falls es der Orientierung dient
- Offene Entscheidungen und ungelöste Randfälle
- Risiken, die von ungeklärten unteren Ebenen abhängen

## @continue Weitermachen <a id="continue"></a>

Prüfen, ob das [Konzeptmodell](conceptual-model-guide.md) stabil ist, dann
zur [Oberfläche](surface-guide.md) übergehen.
