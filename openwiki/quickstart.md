---
type: repository-guide
title: Repository-Leitfaden
description: Dieser Leitfaden ordnet den derzeit bewusst minimalen Repository-Stand ein und trennt das Produkt-Repository von seinem generierten OpenWiki. Er verweist auf die Dokumentationsautomation und die passenden Einstiegspunkte für Beiträge.
tags: [repository, openwiki, contributor-guide]
sources:
  - id: openwiki-source-6d4b4e707b8d60b6ccfa3425
    resource: repo://.github/workflows/openwiki-update.yml
  - id: openwiki-source-8037e2358a2c4f9b2c722a11
    resource: repo://AGENTS.md
  - id: openwiki-source-23775c3de52f3ab95a13cb8b
    resource: repo://README.md
generated: { by: "openwiki/0.7.2", at: "2026-10-28T08:13:22.574Z" }
verified:
  - by: openwiki/0.7.2
    at: 2026-10-28T08:13:22.574Z
---

# Repository-Leitfaden

## Aktueller Stand und Grenze des Repositories

`README.md` enthält derzeit ausschließlich die Überschrift `paperclip`. Im Repository sind keine Anwendungsimplementierung und keine Testsuite vorhanden. Deshalb lässt sich weder ein Produktlauf noch ein Testkommando dokumentieren: Produktverhalten, Schnittstellen und Konfiguration sind in diesem Stand nicht belegt.

Das Verzeichnis `openwiki/` ist davon getrennt zu betrachten. Es ist ein generierter Evidenzindex zur bedarfsgesteuerten Orientierung, nicht die Produktimplementierung. Die in diesem Wiki beschriebenen Abläufe betreffen daher seine Pflege und nicht die Ausführung von `paperclip`.

## Orientierung für Beiträge

- **Produktumfang klären:** Bei Fragen zum derzeitigen Projektstand ist [`README.md`](../README.md) die einzige Produktdokumentation. Fehlen dort oder im Repository Implementierung und Tests, keine Eigenschaften des Produkts ableiten.
- **OpenWiki als Kontext nutzen:** Die Arbeitsanweisungen in [`AGENTS.md`](../AGENTS.md) verlangen, Wiki-Kontext nur bei Bedarf abzurufen. Sind die OpenWiki-Abrufwerkzeuge nicht verfügbar, dient diese Seite als Einstieg und verweist auf die passende Fachseite. Quellcode und Tests bleiben stets maßgeblich, sobald sie vorhanden sind.
- **Wiki-Automatisierung betreiben oder ändern:** [OpenWiki-Aktualisierungsautomatisierung](operations/openwiki-automation.md) erläutert den geplanten bzw. manuell startbaren GitHub-Actions-Workflow, den Aktualisierungs-PR und den Umgang mit Teilerfolgen und Fehlern. Die zugrunde liegende Konfiguration steht in [`.github/workflows/openwiki-update.yml`](../.github/workflows/openwiki-update.yml).

## Pflegegrenze

OpenWiki-Seiten werden durch die geplante GitHub-Actions-Aktualisierung erneuert. `AGENTS.md` weist deshalb an, generierte OpenWiki-Seiten nicht ohne ausdrücklichen Auftrag von Hand zu bearbeiten: Änderungen an Produktcode oder dessen Dokumentation gehören in die jeweiligen Quelldateien; die Automation erzeugt anschließend den Wiki-Stand. Änderungen an der Automation selbst sollten gegen die Betriebsanleitung geprüft werden, insbesondere wenn sie Aktualisierung, PR-Staging oder Fehlerweitergabe beeinflussen.
