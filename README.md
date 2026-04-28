# Alarm System with PIN Disarming and Dashboard

## Project Description
This project implements an alarm system with motion detection. It is built on the **Raspberry Pi 4b+** platform using **Python** and a **Flask** server.
The server communicates with a web dashboard created in **HTML, JavaScript, and CSS** using the **Bootstrap** framework.
The system is controlled manually—setting, arming, and disarming via a PIN code—while detailed information is accessible through the web dashboard. The project utilizes asynchronous programming.

Developed as a student project - 2nd year - Applied Computer Science.

---

## Technologies
- **Libraries:**
  - `RPi.GPIO` – Pin handling and component control
  - `threading` – Asynchronous operations and communication between key functions
  - `Flask` – Server for the web dashboard
  - `tm1637` – Controlling the 7-segment display for PIN configuration
  - `mailer` – Sending email alerts regarding potential intrusions
- **Bootstrap 5** – Frontend framework for the dashboard

---

## Functionalities
- **RCWL-0516** – Microwave Doppler sensor for motion detection
- **HCSR-04** – Doppler sensor range regulation and measuring distance to a moving object
- **4x3 Membrane Keypad:**
   - Setting the PIN
   - Arming and disarming the detector
   - Aborting alarms and countdowns
- **TM1637 + LEDs:**
   - Displaying PIN changes on the panel
   - Simple animations signaling system events
- **Flask Server:**
   - Dashboard hosting
   - Logging PIN entry attempts
   - Log file (`log.txt`) download functionality
   - Real-time system status
- **Bootstrap Dashboard:**
   - Visual interface for the web app
   - Light and dark mode support
   - Visit counter
   - Color-coded button backlighting
- **Security Features:**
   - Alarm triggers after 3 incorrect PIN attempts or timeout
   - Audible signaling (buzzer)

---

## Asynchronous Programming Aspects
The `Thread`, `Event`, and `Lock` objects from the threading library were used to optimize parallel operations and manage component access:
- **Thread** – Enables simultaneous tasks, such as running an alarm countdown while validating PIN entries to abort it.
- **Event** – Binary flags used for communication and thread control.
- **Lock** – Manages access to the TM1632 screen to prevent overlapping data from different functions.

---

## Hardware
- Raspberry Pi 4b+
- TM1637 (7-segment display)
- 2x LEDs
- 4x3 Membrane Keypad
- RCWL-0516 (Motion sensor)
- HC-SR04 (Ultrasonic sensor)
- KY-006 Passive Buzzer

---

## File Structure Schema
<img width="499" height="472" alt="schema" src="https://github.com/user-attachments/assets/390527c1-da0d-4bed-a294-3b7e889a981a" />

## Wiring Diagram
![e0dd9675-cee9-4b02-9b4f-687b96b7323b](https://github.com/user-attachments/assets/5d30b374-6c1a-40c8-960a-a7334515ed83)

---

## Authors:
- Jakub Sosna ([2gub4]https://github.com/2gub4)) – Python code, hardware
- Kamil Skorupski ([K3mYk](https://github.com/K3mYk)) – Flask server, dashboard, hardware
  
---

<br>
<br>
<br>
<br>

## Opis projektu
Projekt realizuje działanie systemu alarmowego z detekcją ruchu. Zdudowany jest na platformie Raspberry Pi 4b+ w języku Python z serwerem Flask. 
Serwer służy do komunikacji z dashboardem będącym aplikacją web'ową stworzoną w HTML, JavaScript i CSS przy pomocy narzędzia Bootsrap.
Sterowanie odbywa się poprzez ręczne ustawianie, uzbrajanie i rozbrajanie kodem PIN, a szczegółowe informacje dostępne są przez wspomniany dashboard po połączeniu z serwerem. Korzysta z programowania asynchronicznego.

Realizowany na potrzeby projektu studenckiego - 2 rok - Informatyka Stosowana

---

## Technologie
- Biblioteki:
  - RPi.GPIO - obsługa Pinów, sterowanie komponentami
  - threading - asynchroniczne działanie i komunikacja kluczowych funkcji
  - Flask - serwer obsługujący dashboard
  - tm1637 - sterowanie komponentem o tożsamej nazwie - wyświetlanie aktualnej konfiguracji pinu
  - mailer - wysyłanie monitu o potencjalnym włamaniu na maila
- Bootstap 5 - frontend dashboard'u

---

## Funkcjonalności
- **RCWL-0516** - mikrofalowy czujnik Dopplera, odpowiedzialny za detekcję ruchu
- **HCSR-04** - regulacja zasięgu czujnika Dopplera, mierzenie odległości do ruchomego obiektu
- klawiatura membranowa 4x3:
   - ustawianie pinu
   - uzbrajanie i rozbrajanie detektora
   - przerywanie alarmu i odliczania
- **TM1637** + diody LED:
   - wyświetlanie zmian przy PINie na panelu
   - proste animacje sygnalizujące zdarzenia
- Flask:
   - obsługa dashboardu
   - tworzenie logów o próbach wprowadznia PINu
   - pobieranie pliku log.txt
   - status systemu
- Bootstrap:
   - wizualny aspekt aplikacji webowej   
   - obsługa ciemnego i jansnego motywu
   - wyświetlanie ilości odwiedzeń
   - różnokolorowe podświetlenie przycisków
- alarm w przypadku 3-krotnego wprowadzenia błędnego PINu lub upływu czasu
- sygnalizacja dźwiękowa

---

## Aspekty programowania asynchronicznego
Z biblioteki zaimportowano obiekty Thread, Event i Lock, by usprawnić równoległe funkcjonowanie kluczowych funkcji oraz zapewnić komunikację i dostęp do komponentów.
- Thread - tworzenie wątków czerpiących z funkcji by umożliwić np. jednoczesne odliczanie do alarmu i walidację PINu, mającą na celu jego przerwanie
-  Event - tworzenie dwustanowych flag służących do komunikacji i sterowania wątkami
-  Lock - zarządanie dostępem do ekranu tm1632, tak by wyświetlane z różnych funkcji informacje nie nachodziły na siebie

---

## Sprzęt
- Raspberry Pi 4b+
- TM1632
- diody LED 2x
- klawiatura membranowa 4x3
- RCWL-0516
- HC-SR04
- buzzer pasywny KY-006

---

## Schemat struktury plików
<img width="499" height="472" alt="schemat" src="https://github.com/user-attachments/assets/390527c1-da0d-4bed-a294-3b7e889a981a" />

## Schemat połączeń

![e0dd9675-cee9-4b02-9b4f-687b96b7323b](https://github.com/user-attachments/assets/5d30b374-6c1a-40c8-960a-a7334515ed83)

---

## Autorzy:
- Jakub Sosna (2gub4) - kod Python, hardware
- Kamil Skorupski ([K3mYk](https://github.com/K3mYk)) - serwer Flask, dashboard, hardware

  
