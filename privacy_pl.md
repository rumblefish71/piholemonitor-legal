# Polityka Prywatności dla PiHoleMonitor

Ostatnia aktualizacja: 16 kwietnia 2026 r.

## 1. Informacje Ogólne
Niniejsza polityka prywatności informuje o rodzaju, zakresie i celu gromadzenia oraz wykorzystywania danych osobowych podczas korzystania z aplikacji „PiHoleMonitor”.

Administrator:
Christian Jurtz
Haubachstr. 48
16540 Hohen Neuendorf
Niemcy
mountainfields@jurtz.de

## 2. Podstawowa Zasada
Aplikacja służy do monitorowania **własnej** instancji Pi-hole®.
**Nie mamy dostępu do Twoich danych w Pi-hole.**
Komunikacja odbywa się wyłącznie i bezpośrednio między Twoim urządzeniem (smartfonem) a Twoim serwerem Pi-hole. Twoje dane uwierzytelniające (tokeny API, hasła) są przechowywane w formie zaszyfrowanej na Twoim urządzeniu i nie opuszczają go.

## 3. Uprawnienia i Przetwarzanie Danych

### 3.1 Dostęp do Sieci (INTERNET)
Aplikacja wymaga dostępu do sieci, aby połączyć się ze skonfigurowanym serwerem Pi-hole.
* **Dane:** Adres IP, nazwy hostów, token API.
* **Przetwarzanie:** Dane są przetwarzane wyłącznie lokalnie i nie są przesyłane do nas ani do osób trzecich.
* **Podstawa prawna:** Prawnie uzasadniony interes (Art. 6 ust. 1 lit. f RODO) w zakresie funkcjonalności aplikacji.

### 3.2 Blokada Aplikacji i Biometria (USE_BIOMETRIC)
Opcjonalnie możesz zabezpieczyć dostęp do aplikacji. Wykorzystuje to metody zabezpieczeń skonfigurowane na Twoim urządzeniu (np. odcisk palca, rozpoznawanie twarzy lub PIN/wzór).
* **Przetwarzanie:** Weryfikacja odbywa się wyłącznie lokalnie przez system operacyjny Android (Android Biometric API).
* **Prywatność danych:** Aplikacja nigdy nie ma dostępu do surowych danych biometrycznych ani do kodu PIN. Otrzymujemy jedynie potwierdzenie („Sukces” lub „Błąd”) z systemu. Dane biometryczne nigdy nie opuszczają bezpiecznej pamięci sprzętowej urządzenia (Art. 9 RODO).

### 3.3 Raportowanie Awarii (Crash Reporting)
Aby poprawić stabilność aplikacji, możesz wyrazić zgodę na wysyłanie raportu o błędach w przypadku awarii.
* **Typ:** Opt-In (domyślnie wyłączone). Musisz wyrazić wyraźną zgodę w ustawieniach („Crash Reporting Consent”).
* **Odbiorca:** Dane są wysyłane na nasz własny serwer (`https://www.mountainfields.de/crash`). **Brak** udostępniania podmiotom trzecim.
* **Gromadzone dane:**
    * Typ urządzenia, model, producent, wersja systemu Android.
    * Zużycie pamięci (RAM) w momencie awarii.
    * Techniczny raport o błędzie (Stacktrace).
    * Fragment logu systemowego (Logcat, maks. 200 linii).
* **Przechowywanie:** Raporty są przechowywane na naszym serwerze do 30 dni w celu analizy, a następnie usuwane. Na urządzeniu są usuwane natychmiast po wysłaniu.
* **Podstawa prawna:** Twoja zgoda (Art. 6 ust. 1 lit. a RODO). Możesz ją wycofać w dowolnym momencie.

### 3.4 Zaawansowane Debugowanie (Session Recording)
Możesz ręcznie uruchomić szczegółowe nagrywanie błędów („Session Recording”).
* **Typ:** Ręczny (Opt-In).
* **Przetwarzanie:** Plik (`debug_reports`) jest generowany **wyłącznie lokalnie**. **Brak automatycznego przesyłania.** Ty decydujesz o udostępnieniu tego pliku.
* **Przechowywanie:**
    * **Surowe dane** są **usuwane natychmiast** po wygenerowaniu raportu.
    * Wygenerowany raport jest **tymczasowo buforowany** i **automatycznie usuwany z urządzenia po maksymalnie 1 godzinie**.
* **Zawartość raportu:**
    * Wersja aplikacji, typ kompilacji, hash Git.
    * Informacje o sieci (status WiFi/GSM/VPN).
    * **Dane zamaskowane:** Skonfigurowana domena Pi-hole, **ukryte adresy IP** (np. `192.168.xxx.xxx`), adresy MAC oraz identyfikatory sesji (SID).
    * Status certyfikatu SSL.
    * Log aktywności aplikacji podczas sesji.
* **Uwaga:** Mimo maskowania raport może zawierać **metadane techniczne**. **Udostępniaj go tylko zaufanym osobom.**

## 4. Przechowywanie Wrażliwych Danych
Tokeny API i hasła są przechowywane w systemie **Android Keystore** oraz w `SharedPreferences` (zaszyfrowane AES-256 GCM).

## 5. Twoje Prawa
Masz prawo do dostępu do danych, ich sprostowania, usunięcia, ograniczenia przetwarzania oraz przenoszenia danych (Art. 15–20 RODO).
* **Kontakt:** Aby skorzystać ze swoich praw, skontaktuj się z adresem e-mail podanym powyżej.
* **Prawo do skargi:** Masz prawo wnieść skargę do organu nadzorczego.

## 6. Bezpieczeństwo Danych
Stosujemy środki techniczne i organizacyjne (np. szyfrowanie), aby chronić Twoje dane (Art. 32 RODO).

## 7. Zmiany w Polityce Prywatności
Zastrzegamy sobie prawo do aktualizacji niniejszej polityki. Zmiany będą publikowane tutaj.