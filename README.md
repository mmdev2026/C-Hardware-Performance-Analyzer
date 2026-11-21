# C Hardware Performance Analyzer

Kostenloser Benchmark für Windows x64 zum Vergleich einer CPU-Berechnung mit einem Thread, einer OpenMP-Berechnung mit mehreren Threads und einer OpenCL-GPU-Berechnung. Die SIMD-Ansicht veranschaulicht acht gewichtete Eingaben eines Beispielneurons.

## Voraussetzungen

- Windows x64.
- Für den GPU-Test ein passender OpenCL-Treiber.
- Die beiden EXE-Dateien und beide DLLs müssen nach dem Entpacken im selben Ordner liegen.

## Ausführen

1. Das vollständige ZIP in einen Ordner entpacken.
2. `hardware_gui.exe` starten.
3. Auf **Benchmark starten** klicken.

Für einen reinen CPU-Test PowerShell im entpackten Ordner öffnen und ` .\hardware_analyse.exe --cpu-only` ausführen (ohne das Leerzeichen direkt nach dem Backtick).

## Beispielmessung

Auf einem Intel Core i5-10310U wurden jeweils 100 Additionen auf 4.194.304 Werten ausgeführt; die angegebenen Zeiten sind Mediane aus drei Messungen:

- Ein CPU-Thread: 134,376 ms
- OpenMP: 111,010 ms
- Intel UHD Graphics über OpenCL, einschließlich Transfer: 119,710 ms
- Ergebnisfehler: 0

Die Ergebnisse hängen von Gerät, Treiber und Aufgabe ab. In diesem Beispiel war OpenMP etwa 8,7 ms schneller als die GPU einschließlich Transfer.

## Umfang und Einschränkungen

Dies ist ein spezifischer Benchmark für die beschriebenen Rechenpfade und keine vollständige Hardwarediagnose. Die Vorschau wurde auf Windows 11 Pro x64 mit Intel UHD Graphics getestet. Tests auf Windows 10, einer separaten sauberen Windows-Installation und Hardware ohne AVX stehen noch aus. Die EXE-Dateien sind unsigniert.

## Lizenz und Copyright

Kostenlos für private und gewerbliche Anwender. Anleitung und Lizenztexte liegen im ZIP-Paket bei.

Copyright © Manfred Mertens, 21.11.2026.
