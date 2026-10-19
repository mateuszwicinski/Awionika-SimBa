Awionika-SimBa - Modułowy komputer pokładowy rakiety (Altium Designer)

Projekt modułowego systemu elektroniki rakietowej wykonany w środowisku Altium Designer. Całość została zaprojektowana w formie 3-poziomowego, okrągłego stosu płytek drukowanych, dostosowanego kształtem do montażu wewnątrz kadłuba rakiety.

Poszczególne płytki łączą się ze sobą za pomocą złącz szpilkowych (goldpin), które przekazują linie zasilania oraz sygnały sterujące między poziomami.

Opis modułów systemu

Płytka dolna (Zasilanie i układy wykonawcze)
Odpowiada za zasilanie całego stosu oraz załączanie elementów wykonawczych:

Zasilanie: przetwornica step-down D30V30F5 dostarczająca główną linię 5V oraz stabilizator liniowy AMS1117 dla linii 3.3V. Wejście zasilania ze złącza XT30 lub ARK z diodą zabezpieczającą przed odwrotną polaryzacją.

Obwód zapalnika odzysku: wyjście śrubowe ARK sterowane tranzystorem N-MOSFET (AO3400A) z rezystorem ściągającym bramkę do masy. W gałąź zapalnika wpięty jest szeregowo bezpiecznik polimerowy 2.6A (0ZCG0260BF2B), którego zadaniem jest odcięcie dopływu prądu do zapalnika po zadziałaniu ładunku w razie zwarcia lub stopienia drutu oporowego, co chroni akumulator przed przeciążeniem i zapobiega wyłączeniu reszty elektroniki.

Obwód buzzera: tranzystor N-MOSFET (AO3400A) z diodą gaszącą impulsy indukcyjne (SS14) do załączania buzzera akustycznego po wylądowaniu.

Wyjścia serwomechanizmów: złącza JST-XH wyprowadzające linie zasilania 5V, masę oraz sygnały sterujące PWM.

Płytka środkowa (Logika i pamięć)
Główny moduł sterujący:

Mikrokontroler: płytka deweloperska ESP32-C3-Zero, połączona z magistralą między płytkami.

Karta pamięci: gniazdo modułu czytnika kart MicroSD (Waveshare) połączone przez interfejs SPI do zapisu parametrów lotu w czasie rzeczywistym.

Płytka górna (Sensory i łączność radiowa)
Moduł pomiarowy i komunikacyjny:

Moduł radiowy: LoRa z wyprowadzeniem pinu antenowego bezpośrednio do złącza antenowego J6.

Czujniki: pola pod moduł barometru oraz moduł czujnika IMU podłączone pod magistralę I2C/SPI.

Zawartość repozytorium

Dokumenty:

Schematy ideowe w formacie PDF dla każdego z trzech modułów.

Zestawienia komponentów (BOM) w formacie CSV.

Zrzuty i rendery 3D płytek drukowanych.

Fabryka:

Spakowane archiwa (ZIP) z plikami Gerber (warstwy miedzi, soldermaski, opisów i obrysu) oraz plikami wierceń maszynowych (NC Drill).

Projekty:

Pliki projektowe Altium Designer (.PrjPcb, .SchDoc, .PcbDoc).

Biblioteki symboli (.SchLib) oraz footprintów (.PcbLib) utworzone na potrzeby projektu.


<img width="3982" height="2461" alt="Plytka_srodkowa_ESP_SD(bok1)" src="https://github.com/user-attachments/assets/1f6b9a6e-c8ed-4c57-b403-96c427d23071" />

