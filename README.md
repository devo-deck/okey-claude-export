# Okey Friends – Claude Handover

Stand: 6. November 2026. Dieses Paket enthält das vollständige Unity-Projekt **U2n2 einschließlich der werfbaren Tischobjekte**, nicht nur die APK.

## Für Claude

1. `OkeyUnity_Komplett_2026-11-06_U2n2.zip` vollständig entpacken.
2. In Unity Hub **exakt Unity 6000.0.85f1** zum Öffnen verwenden. Nicht auf 6000.3 aktualisieren, ohne vorher Probleme zu prüfen.
3. Unity erzeugt Cache- und Importdateien beim ersten Öffnen neu. `Library`, `Temp`, `obj`, `Logs`, `Builds` und `.git` fehlen bewusst.
4. Vor Änderungen die Ist-Dateien lesen. `PLAENE/PLAN.md` beschreibt einen früheren Stand und nennt Unity 6000.3.26f1; **maßgeblich sind die Projektdateien und tatsächlich 6000.0.85f1**.
5. Alle `.meta`-Dateien und GUIDs beibehalten. Keine GUIDs neu erzeugen oder Assets ohne Unity verschieben.
6. Nach Änderungen EditMode- und PlayMode-Tests laufen lassen und einen Android-Build prüfen. Keine visuelle Verschlechterung.

## Wichtige Dateien

- Tischobjekte: `Assets/_Project/Scripts/Game/TischObjekteSystem.cs`, `TischObjekt.cs`, `TischObjekteUI.cs`, `PropPhysik.cs`
- Modell und Tests: `Assets/_Project/Scripts/Okey.Core/TischObjekteModell.cs`, `Okey.Core.Tests/TischObjekteTests.cs`, `Okey.PlayMode.Tests/TischObjekteU2n2Tests.cs`
- U2n2-Assets: `Assets/_Project/Art/TableItems/V2/` und `Assets/_Project/Prefabs/TableItems/TObj_*`
- Historische technische Planung: `PLAENE/PLAN.md`
- Früheres Designregelwerk: `PLAENE/okey.md`; die folgenden neueren Entscheidungen überschreiben Widersprüche aus älteren Entwürfen.

## Verbindliche Richtung

- Mobile Premium-/AAA-Anmutung im Cartoon-Stil, elegant statt protzig. Keine Version darf schlechter aussehen als die vorherige.
- Zielgerät: Xiaomi Redmi 14. Flüssigkeit und sparsamer Speicher gehen vor Details. Speicherziel auf „Hoch“ etwa 320 MB PSS.
- Querformat, URP, IL2CPP ARM64, GLES3-Fallback; automatische Grafikqualität und stabile Bildrate auf schwachen Handys.
- Online-Multiplayer bewusst erst nach den Inhalten. Trotzdem alle neuen Interaktionen serverfähig/synchronisierbar halten: Ereignisse und Inventar hinter sauberen Schnittstellen, keine lokalen Einbahnstraßen.
- Zunächst private APK-Tests, keine Store-Veröffentlichung. Echtgeld erst später über Google Play/App Store; bis dahin Testwährung.

## Umsetzungsreihenfolge

1. **U2n2, im vorliegenden Projekt:** Tischobjekte Çay-Glas, Tesbih, Nazar, Zigarre, Feuerzeug und Ring; Objekt-Knopf mit Çay-Glas und Plus; Greifen und Werfen.
2. **U2o:** Café B „Laternenabend“ mit entspanntem Licht, größer, schöner und orientalisch. Charakter-Erstellung A: einfache weiche beige 3D-Cartoonfigur, matte runde Arme und Beine, keine detaillierten Hände; Augen, Frisur, Nase, Mund und Körperform anpassbar. Nasen bis groß und lustig übertrieben; Uhr, Kette und Hut separat.
3. **U2p:** Zug-Timer und schneller Modus; lustige Ereignisse, wenn jemand zu lange braucht (schlafend/schnarchend, räuspernder Onkel, langsamer Kellner mit Tee, Trommeln auf dem Tisch).
4. **U4 Shop:** Diamanten und Münzen, täglich 4–6 rotierende Artikel, Wochenhighlight, limitierte Angebote und Lootboxen.
5. **U3 zuletzt:** Online-Multiplayer auf Hetzner, Gastspiel ohne Registrierung, kurze Spieler-ID wie `#K7Q2`, Freunde über ID/Einladungslink. Konto nur für Käufe oder Gerätewechsel sichern, mit Erhalt des Fortschritts. Gelegentlicher Hinweis „Konto sichern“.

## Finishers und Emotes

Finishers sind große, stimmige, tischweite Momente. Freigegebene neue Finishers:

- **Polizei-Razzia:** Marke, Blaulicht, Polizisten stürmen das Café und führen die anderen ab; Sieger war Zivilbulle.
- **Pantoffel:** Sieger wirft den Pantoffel in Zeitlupe an den Kopf des Letzten; Comic-BONK.
- **Explosion:** Dynamit unterm Tisch, anschließend alle verrußt mit Afro.
- **Hubschrauber:** Sieger fliegt am Seil mit dem Geld davon; der Wind fegt alle weg, **niemand fällt am Ende um**.
- **Pistole:** zuerst zwei Schüsse in die Luft, danach fallen alle in übertriebenem Comic-Stil um; keine realistische Gewalt, kein Blut.
- Weitere bereits vereinbarte große Finishers: Tisch seitlich kippen, Geldregen, lauter Stein-Slam.
- **Gestrichen:** Schockwelle, Bulldozer, Çay-Tsunami und Mutter-mit-Pantoffel.

Emotes statt Finishers: Zigarre (größer, lustig, realistischer Rauch), Tee-Toast, Tesbih, Tavla-Würfel, Zaubertrick, Saz, Sonnenbrille, Wackeln und Weinen. Ein alter Onkel beobachtet und kommentiert im Hintergrund. Emotes dürfen von jedem am Tisch ausgelöst werden.

## Shop und Währungen

- Diamanten nur gegen Echtgeld: Starter 1,99 €, Pakete 4,99 € und 9,99 € mit Bonus.
- Münzen durch Spielen oder Umtausch/Kauf mit Diamanten.
- Etwa 80 % der Kosmetik auch für Münzen, etwa 20 % auffälligste Artikel nur für Diamanten.
- Normale Artikel ungefähr 2–5 €, wenige Topartikel etwa 10 €.
- Lootboxen mit Münzen oder Diamanten, sichtbare Chancen, Münzausgleich für Duplikate, rein kosmetisch, hochwertige Öffnungsanimation.
- Echtgeldwährung bleibt der einfache grüne Smaragd mit ganz subtiler heller Kontur; Münze unverändert, wenig Detail.
- Logo nur „Okey Friends“, ohne Krone. Knöpfe B „Iznik-Facette“, Hauptmenü-Kontrast V2 ohne Krone. Freundesliste größer, Ladebildschirm nachreichen.

## Später, nicht jetzt priorisieren

Eigenes Café, das Geld erwirtschaftet und Minispiele enthält. Dritte Währung „Chips“ für Glücksrad, Greifautomat und Lotto nach Server und Shop. Vor echten Käufen/Start rechtliche Prüfung von Lootboxen, Minispielen und Jugendschutz.

## Arbeitsauftrag an Claude

Erst den Ist-Stand verstehen, verbessern und bestehende Funktionen nicht brechen. Vor größeren Änderungen einen konkreten Plan liefern, betroffene Dateien nennen und Test/Build ausführen. Neue Features ins Projekt integrieren, nicht nur als Mockup oder unverbundenen Code anlegen. Keine Behauptung von Tests, die nicht tatsächlich gelaufen sind.
