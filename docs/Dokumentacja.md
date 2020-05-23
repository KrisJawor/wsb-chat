# DOKUMENTACJA APLIKACJI „CZAT"

Aplikację przygotowali:

1. Chołyk Bogusław
2. Paweł Włodarski
3. Michał Sikorski
4. Krzysztof Jaworski
5.


## 1. Cel projektu.

Stworzenie aplikacji polegającej na możliwości wymiany informacji z wybranym z dostępnych użytkowników.

## 2. Organizacja projektu

**Czas realizacji projektu: 23.02.2020 do 25.05.2020.**

Osoby odpowiedzialne za poszczególne części projektu:

* Chołyk Bogusław – dokumentacja, komunikacja w zespole oraz z managerem projektu. 23.02.2020 – 24.05.2020
* Krzysztof Jaworski – wygląd aplikacji (CSS) 23.02.2020 – 11.05.2020
* Włodarski Paweł – Backend aplikacji 23.02.2020 – 11.05.2020
* …………………. – testowanie aplikacji 22.03.2020 – 24.05.2020
* Michał Sikorski – rozwój i skalowanie aplikacji 26.03.2020 – 24.05.2020

## 3.Architektura aplikacji 
Prostota oraz ogólnodostępność aplikacji sprawiły, iż najkorzystniejszym do jej stworzenia było użycie kombinacji języka PHP (Backend) i JavaScript (Frontend).

W celu zapewnienia interakcji (dwukierunkowej, swobodnej wymianie komunikatów) między serwerem a aplikacją, użyta została technologia WebSocket. Umożliwia ona serwerowi wysyłanie danych do przeglądarki, nawet wtedy, jeżeli przeglądarka o te dane nie zapyta. Wystarczy, że wcześniej zostanie zestawiony odpowiedni kanał komunikacyjny.

Ograniczona ilość użytkowników uzależniona jest od zasobów serwera.

## 4. Testowanie Aplikacji
TUTAJ WPISZ TEKST 😊 i z 1-2 screeny	

## 5. Skalowanie Aplikacji
W aplikacji użyto automatycznego skalowania pionowego. Zwiększającego dostępne zasoby sprzętowe, w zależności od wykorzystania.
Przykładowa konfiguracja na platformie Azure, sprowadza się do określenia reguł, kiedy skalowanie ma być uruchomione. 

Przechodzimy do sekcji autoskalowania zasobu. 
![1](https://user-images.githubusercontent.com/57036751/82708547-ce596980-9c7e-11ea-95fa-f2a595114b78.png)

Dodajemy regułę z ustawieniami domyślnymi, a następnie regułę z ustawieniami operatora na wartości "mniejsze niż" i próg metryki na "20", wartość parametru operacja, na "zmniejsz liczbę o"
![2](https://user-images.githubusercontent.com/57036751/82708564-d7e2d180-9c7e-11ea-8d9a-f0655bc7dd93.png)

W efekcie otrzymujemy takie reguły.
![3](https://user-images.githubusercontent.com/57036751/82708571-d9ac9500-9c7e-11ea-9bfd-8bd1c082c4c5.png)
