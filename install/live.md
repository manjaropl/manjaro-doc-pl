# Uruchamianie wersji Live

Uruchomienie systemu w wersji Live, czy to z CD/DVD czy z pamięci USB, daje możliwość obejrzenia i sprawdzenia systemu Manjaro Linux jak działa na twojej maszynie. To bardzo ważny krok przed decyzją instalacji systemu.
W celu uzyskania najlepszych rezultatów powinieneś być podłączony do Internetu. Jeśli używasz kabla i podłączysz go przed uruchomieniem Manjaro Live, system automatycznie nawiąże połączenie. Jeśli masz bezprzewodowe połączenie Wi-Fi, możesz go wybrać i ustawić po uruchomieniu pulpitu Manjaro.

Po przygotowaniu bootowalnego USB/CD/DVD kolejnym krokiem jest ustawienie kolejności i wybranie pierwszego urządzenia bootowalnego w BIOSie. Wejście do BIOSu może różnić się w zależności od maszyny, np. może być wymagane naciśnięcie lub przytrzymanie "Esc", "Del" lub "F10", czasem "F12". Jeśli nie jesteś pewny co zrobić, zajrzyj do dokumentacji twojego komputera lub poszukaj odpowiedzi w sieci.

**Menu bootowania**

Kiedy uruchomisz nośnik instalacyjny (CD/DVD lub pamięć USB) w trybie BIOS (legacy) powinieneś zobaczyć ekran bootowania Manjaro, który oferuje parę opcji, których ustawienie pozwoli na najlepsze doświadczenie środowiska Live.
Jest możliwe ustawienie preferowanego języka i klawiatury, co oznacza, że Manjaro będzie używać twojego języka od samego początku.

**Ustawienie języka i klawiatury**

Ustaw język naciskając F2, a następnie używając strzałek na klawiaturze przesuń zaznaczenie na polski, jak na przykładzie obok. Naciśnij Enter, żeby potwierdzić wybór i powrócić do menu bootowania.
Wybierając dany język, zostanie też ustawiony domyślny układ klawiatury dla niego, w twoim wypadku będzie to QUWERTY z polskimi znakami. Jeśli masz inną klawiaturę lub woliasz pisać w innym języku, naciśnij F2 ponownie i strzałkami wybierz Klawiaturę (na końcu listy) i po znalezieniu odpowiedniej opcji naciśnij Enter, by potwierdzić i powrócić do menu bootowania.

**Wybór sterowników**

Są dwa główne zestawy sterowników, które mogą być użyte w Manjaro: Otwarte (otwartoźródłowe) i Zamknięte (własnościowe). Różnice między nimi są znaczne i twój wybór może zależeć od sprzętu na twoim komputerze.

Otwarte sterowniki (ang. **free** lub *open source*), tak jak samo Manjaro, są napisane i uaktualniane przez dużą społeczność. Dla starszego sprzętu i tego z wbudowaną grafiką Intela lub kartami graficznymi AMD to jest najlepszy wybór.-> skonsultować!

Zamknięte sterowniki (ang. **non-free** lub *proprietary*) są napisane i uaktualniane tylko przez producentów sprzętu. To generalnie najlepszy wybór dla nowszych komputerów z dedykowanymi kartami Nvidia. W tej chwili zamknięte sterowniki są polecane dla kart Nvidia nowszych niż seria 8000. Dla starszych kart Nvidii otwarto-źródłowe sterowniki mogą lepiej działać.

Aby uruchomić i/lub zainstalować Manjaro z otwartymi sterownikami, wybierz **Start Manjaro Linux**.
Aby uruchomić i/lub zainstalować Manjaro z zamkniętymi sterownikami, wybierz **Start (none-free drivers)**.

**Witaj w Manjaro**

Po wybraniu Start, Manjaro się załaduje. Możesz zobaczyć dużo tekstu przewijającego się przez ekran -nie martw się tym, to oznacza że system działa! Po chwili, zakładając że twój sprzęt jest kompatybilny, otworzy się pulpit Manjaro i zobaczysz ekran powitalny.
Ekran powitalny w wersji live zawiera linki do uruchomienia instalatorów, dokumentację (jak tak, którą teraz właśnie czytacie!) i kanały wsparcia (forum, kanał IRC). Nie martw się jeśli zamkniesz ten ekran: można go uruchomić ponownie wyszukując go w menu systemowym.
