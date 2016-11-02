# Automatyczna instalacja w systemach BIOS (legacy) za pomocą instalatora Calamares


Graficznym instalatorem w Manjaro jest Calamares. Za jego pomocą mamy możliwość wyboru trzech zautomatyzowanych opcji instalacji, które poniżej omówimy w szczegółach. Manualna instalacja jest przedstawiona w rozdziale Manualna instalacja w systemach BIOS (legacy) za pomocą instalatora Calamares.

Wyczyść cały dysk i pozwól instalatorowi Calamares ustawić partycje.

Najprostszą wersją instalacji jest nadpisanie całego dysku i pozwolenie instalatorowi na utworzenie domyślnych partycji dla waszego nowego systemu operacyjnego. To odpowiednia metoda jeśli chcesz zacząć od początku, gdyż wszystkie informacje na dysku zostaną skasowane. Jeśli checesz je zachować, możesz skopiować dane na dysk zewnętrzny i przywrócić po instalacji.

Wybierz swój język

1.Pierwszym ekranem po uruchomieniu instalatora jest wybór języka z menu. Dodatkowo jeśli nie jesteście podłączeni do Internetu pojawi się na tym ekranie ostrzeżenie.

Wybierz swoją lokację

2. Możesz wybrać swoją strefę czasową albo klikając na pobliski rejon na mapie, albo wybierając region i strefę z menu.

3. Jeśli klikniesz na przycisk "Zmień..." pojawi się menu, które pozwala na wybranie systemowych ustawień lokalnych, które wpływają na ustawienia języka i znaków w niektórych elementach wiersza poleceń interfejsu użytkownika. Dla języka polskiego poprawnym jest domyślne ustawienie pl_PL.UTF-8 UTF-8.

Wybierz ustawienia klawiatury

4. Następnie będziesz mogli wybrać ustawienia klawiatury. Wybierz swój język z listy po lewej stronie a potem podkategorię na liście po prawej stronie. Dzięki temu litery na klawiaturze będą odpowiadać literom na ekranie. Po ustawieniu języka polskiego i wybrania "Domyślnie" będziesz miał do dyspozycji wszystkie polskie znaki i standardowy polski układ klawiszy. Możesz to przetestować w polu na samym dole wpisując kombinacje klawiszy dla polskich znaków (alt+a, alt+s itd.).

5. Możesz też wybrać model klawiatury z menu. Lista jest dość długa, więc twoja klawiatura najprawdopodobniej będzie na liście. W większości wypadków wystarcza jednak zostawienie domyślnej wartości.

Wybierz metodę partycjonowania

6. W tym kroku będziesz musiał wybrać metodę partycjonowania. Wybrany dysk jest pokazany na górze okna. Na lewo jest zaznaczenie, które pokazuje czy instalacja odbywa się w trybie BIOS czy UEFI. Ten rozdział opisuje instalację BIOS. Instalacja UEFI jest opisana w rozdziale Automatyczna instalacja w systemach UEFI za pomocą instalatora Calamares. Typ tablicy partycji GTP lub MBR jest pokazany po prawej stronie. Obecny stan wybranego dysku jest pokazany na dole okna. Instalator posiada parę opcji partycjonowania. Ta sekcja skupia się na opcji, która wymazuje cały dysk i automatycznie tworzy partycje, które będą pasować Manjaro. Liczba opcji może się różnić w zależności od ilości i występowaniu partycji oraz systemów na dysku (na zupełnie czystym dysku z jedną partycją będą widoczne tylko dwie opcje: czyszczenie dysku i manualna instalacja, natomiast na dyskach z systemem, będą cztery opcje).

Pierwsza opcja zainstaluje system Manjaro obok istniejącego systemu poprzez zmniejszenie jego partycji i przeznaczenie uzyskanego miejsca na Manjaro. Druga opcja zainstaluje Manjaro na wybranej partycji wymazując wszystkie jej dane, ale nie ruszy innych co pozwoli zachować ich dane. Trzecia – omawiana w tym rozdziale – kasuje wszystkie partycje i pozwala instalatorowi Calamares stworzyć własne. Ostatnia opcja pozwala na manualne stworzenie, modyfikację i kasowanie partycji, przez co możecie ustawić system według własnych potrzeb. Opcja ta będzie omawiana w rozdziale Manualna instalacja w systemach BIOS (legacy) za pomocą instalatora Calamares.

7. Klikając na "Wyczyść dysk" na dole okna zobaczysz podgląd struktury dysku przed i po wybranej operacji. Zmiana zostanie zastosowana w późniejszym etapie instalacji. Upewnij się, że wybrane opcje są tymi, które chcesz, bo pomyłka na tym etapie może nieodwracalnie skasować dane, które pragniesz zachować (np. poprzez wybranie złego dysku). Jeśli jednak wszystko jest w porządku, możesz potwierdzić ustawienia klikając na przycisk "Dalej".

Jest też opcja szyfrowania partycji Manjaro. Dzięki temu każdy, kto będzie chciał dostać się do danych na tym dysku, będzie musiał podać wybrane przez ciebie hasło.
Opcja "Położenie programu rozruchowego" na samym dole strony umożliwia wybranie czy i gdzie instalować program rozruchowy GRUB, który umożliwia wybranie startu systemu/ów. Jeśli nie jesteś pewny, najlepiej zostawić opcję domyślną.

8. Następnie zostaniesz zapytany o imię, którym będą cię witać niektóre programy, nazwę użytkownika, którą będziesz używać do logowania się do systemu, imię twojego komputera, jak będzie widziany w tej samej sieci, hasło, które musi być wpisane dwa razy, żeby się upewnić, że nie ma żadnych literówek. Na końcu możesz ustawić czy chcesz by system pytał cię o hasło podczas logowania oraz czy chcesz używać tego samego hasła dla konta administratora. Zalecane opcje są już zaznaczone i jeśli nie chcesz ich ustawić inaczej, sugerujemy zostawienie ich tak jak są.

Przejrzyj wszystkie swoje wybory i potwierdź

9. Podczas tego ostatniego etapu przed instalacją zostanie  zaprezentowany ekran z podsumowaniem wszystkich dokonanych wcześniej wyborów. Jeśli jednak zmieniłeś zdanie, możesz się cofnąć do tyłu parę razy, żeby zmienić wybraną opcję. Informacje wcześniej wybrane będą zapamiętane, żeby nie trzeba było ich ponownie uzupełniać przy powrocie do tego etapu. Upewnij się, że partycjonowanie jest zgodne z twoim życzeniem, ponieważ po zatwierdzeniu na tym etapie nie będzie możliwa już żadna zmiana. Wszystkie dane na wybranym dysku zostaną skasowane. Jeśli jesteście usatysfakcjonowani wyborem kliknijcie na "Dalej".

Instalacja...

10. Teraz możesz się zrelaksować i pozwolić instalatorowi działać. Podczas instalacji zostanie pokazany przegląd slajdów przedstawiający kluczowe cechy systemu operacyjnego Manjaro. Proces potrwa co najmniej parę minut, w zależności od sprzętu, na którym instalujesz oraz rodzaju nośnika i portu USB (polecamy pamięci USB 3 i porty USB 3). W przypadku instalacji na innym dysku USB i/lub posiadając już inny zainstalowany system, na którymkolwiek dysku, proces instalacji może się znaczenie przedłużyć i mieć pewne momenty przestoju (na tym samym procencie paska postępu). Zaleca się uzbroić w cierpliwość i pozwolić by proces się dokończył. W najgorszych warunkach instalacja może trwać nawet do godziny lub więcej (z USB 2 lub z CD na USB 2 przy innym systemie na HDD), jednak zazwyczaj trwa tylko ok. 10-15 min.

... zakończone!

11. Instalacja się zakończyła! Żeby zrestartować system od razu i przejść do nowego systemu, zaznacz "Zrestartuj teraz" i naciśnij "Zakończ". -> sprawdzić! Podczas restartu, musisz przywrócić poprzednią kolejność bootowania lub ustawić jako pierwszy nośnik startowy ten, na którym właśnie zainstalowałeś Manjaro.

Jeśli nadpisanie całego dysku ci jednak nie odpowiada, możecie wybrać inną opcję instalatora.
