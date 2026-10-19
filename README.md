<h1>Awionika-SimBa - Modułowy komputer pokładowy rakiety (Altium Designer)</h1>

Projekt modułowego systemu elektroniki rakietowej wykonany w środowisku Altium Designer. Całość została zaprojektowana w formie 3-poziomowego, okrągłego stosu płytek drukowanych, dostosowanego kształtem do montażu wewnątrz kadłuba rakiety.

Poszczególne płytki łączą się ze sobą za pomocą złącz szpilkowych (goldpin), które przekazują linie zasilania oraz sygnały sterujące między poziomami.

<h2>Opis modułów systemu</h2>

<h3>Płytka dolna (Zasilanie i układy wykonawcze)</h3>

Odpowiada za zasilanie całego stosu oraz załączanie elementów wykonawczych:

Zasilanie: przetwornica step-down D30V30F5 dostarczająca główną linię 5V oraz stabilizator liniowy AMS1117 dla linii 3.3V. Wejście zasilania ze złącza XT30 lub ARK z diodą zabezpieczającą przed odwrotną polaryzacją.

Obwód zapalnika odzysku: wyjście śrubowe ARK sterowane tranzystorem N-MOSFET (AO3400A) z rezystorem ściągającym bramkę do masy. W gałąź zapalnika wpięty jest szeregowo bezpiecznik polimerowy 2.6A (0ZCG0260BF2B), którego zadaniem jest odcięcie dopływu prądu do zapalnika po zadziałaniu ładunku w razie zwarcia lub stopienia drutu oporowego, co chroni akumulator przed przeciążeniem i zapobiega wyłączeniu reszty elektroniki.

Obwód buzzera: tranzystor N-MOSFET (AO3400A) z diodą gaszącą impulsy indukcyjne (SS14) do załączania buzzera akustycznego po wylądowaniu.

Wyjścia serwomechanizmów: złącza JST-XH wyprowadzające linie zasilania 5V, masę oraz sygnały sterujące PWM.

<h3>Płytka środkowa (Logika i pamięć)</h3>

Główny moduł sterujący:

Mikrokontroler: płytka deweloperska ESP32-C3-Zero, połączona z magistralą między płytkami.

Karta pamięci: gniazdo modułu czytnika kart MicroSD (Waveshare) połączone przez interfejs SPI do zapisu parametrów lotu w czasie rzeczywistym.

<h3>Płytka górna (Sensory i łączność radiowa)</h3>

Moduł pomiarowy i komunikacyjny:

Moduł radiowy: LoRa z wyprowadzeniem pinu antenowego bezpośrednio do złącza antenowego J6.

Czujniki: pola pod moduł barometru oraz moduł czujnika IMU podłączone pod magistralę I2C/SPI.

Zawartość repozytorium

<h2>Dokumenty:</h2>

Schematy ideowe w formacie PDF dla każdego z trzech modułów.

Zestawienia komponentów (BOM) w formacie CSV.

Zrzuty i rendery 3D płytek drukowanych.

<h2>Fabryka:</h2>

Spakowane archiwa (ZIP) z plikami Gerber (warstwy miedzi, soldermaski, opisów i obrysu) oraz plikami wierceń maszynowych (NC Drill).

<h2>Projekty:</h2>

Pliki projektowe Altium Designer (.PrjPcb, .SchDoc, .PcbDoc).

Biblioteki symboli (.SchLib) oraz footprintów (.PcbLib) utworzone na potrzeby projektu.

<h2>Płytka logiki</h2>

<img width="3982" height="2461" alt="Plytka_srodkowa_ESP_SD(bok1)" src="https://github.com/user-attachments/assets/1f6b9a6e-c8ed-4c57-b403-96c427d23071" />

<img width="3982" height="2461" alt="Plytka_srodkowa_ESP_SD(bok2)" src="https://github.com/user-attachments/assets/125a35fe-7c15-48ad-833a-087032ccef5e" />

<img width="3982" height="2461" alt="Plytka_srodkowa_ESP_SD(tył)" src="https://github.com/user-attachments/assets/d0959f9e-c7fb-4f7d-b3fa-7f4cbc0040f1" />

<img width="3982" height="2461" alt="Plytka_srodkowa_ESP_SD" src="https://github.com/user-attachments/assets/33aeb9eb-18b7-4ea2-9034-3a88fd78278e" />

<h2>Płytka LORA</h2>

<img width="3982" height="2461" alt="Plytka_gorna_lora_czujniki(bok1)" src="https://github.com/user-attachments/assets/a76c9de1-7708-4984-93a6-030a0a9a492f" />

<img width="3982" height="2461" alt="Plytka_gorna_lora_czujniki(bok2)" src="https://github.com/user-attachments/assets/c5f02e94-2aff-4869-a8be-9189449f1510" />

<img width="3982" height="2461" alt="Plytka_gorna_lora_czujniki(tyl)" src="https://github.com/user-attachments/assets/c4254731-a5d8-4119-9353-cdb35252ee30" />

<img width="3982" height="2461" alt="Plytka_gorna_lora_czujniki" src="https://github.com/user-attachments/assets/ff22ace0-d0c1-4b7e-9fbf-999012a77f90" />

<h2>Płytka power</h2>

<img width="3982" height="2461" alt="Plytka_dolna_power(bok1)" src="https://github.com/user-attachments/assets/b3d35b0c-4c71-4312-a0b3-bf81e3ad789f" />

<img width="3982" height="2461" alt="Plytka_dolna_power(bok2)" src="https://github.com/user-attachments/assets/471ad78f-37bb-4ca6-9dd8-cdc98a040fa9" />

<img width="3982" height="2461" alt="Plytka_dolna_power(tyl)" src="https://github.com/user-attachments/assets/1596a212-a05c-4da2-ad44-ccc7cc8136f6" />

<img width="3982" height="2461" alt="Plytka_dolna_power" src="https://github.com/user-attachments/assets/ed1bfd8c-6fd4-427a-be18-64804e0fa673" />
