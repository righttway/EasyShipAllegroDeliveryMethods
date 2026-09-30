# EasyShipAllegroDeliveryMethods
Adding Allegro delivery methods to 4Values TA system (EasyShip)

# Integracja aplikacji z Allegro – opis do rejestracji

## 1. Informacje ogólne
Aplikacja integruje system ERP z usługami Allegro w zakresie obsługi przesyłek. Integracja automatyzuje proces tworzenia przesyłek, pobierania etykiet oraz monitorowania statusów operacji transportowych.

## 2. Cel integracji
Celem integracji jest:
- automatyczne tworzenie przesyłek na podstawie danych zamówień,
- pobieranie numerów listów przewozowych,
- pobieranie etykiet przewozowych,
- obsługa zleceń odbioru (pickup),
- synchronizacja statusów operacji logistycznych.

## 3. Zakres API Allegro wykorzystywany przez aplikację
Aplikacja korzysta z API Allegro w obszarach:
- autoryzacja OAuth2 (odświeżanie tokena dostępowego),
- Shipment Management (tworzenie i odczyt przesyłek),
- Label (generowanie etykiet),
- Pickup (propozycje i tworzenie odbioru).

## 4. Sposób autoryzacji
Autoryzacja realizowana jest przez OAuth2 z użyciem:
- `client_id`,
- `client_secret`,
- `refresh_token`.

Aplikacja przechowuje token dostępu lokalnie i odnawia go po wygaśnięciu.

## 5. Przetwarzane dane
W ramach integracji przetwarzane są dane niezbędne do obsługi przesyłek, w szczególności:
- dane nadawcy i odbiorcy,
- adres dostawy,
- numer telefonu i e-mail odbiorcy,
- parametry przesyłki (masa, gabaryt, usługa),
- dane wymagane do wygenerowania etykiety i numeru śledzenia.

## 6. Bezpieczeństwo
- Komunikacja z API Allegro odbywa się przez HTTPS.
- Dostęp do API jest zabezpieczony tokenami OAuth2.
- Przetwarzane są wyłącznie dane wymagane do realizacji usług logistycznych.

## 7. Środowisko i utrzymanie
Integracja działa jako część wewnętrznego systemu obsługi wysyłek ERP i jest utrzymywana przez właściciela aplikacji.

## 8. Kontakt
W sprawach dotyczących integracji prosimy o kontakt:
- e-mail: pawel@4values.pl
- firma/administrator: 4Values Global Solutions Sp. z o.o./ Paweł Bednarz

---

## Wersja dokumentu
Data aktualizacji: 2026-09-30
