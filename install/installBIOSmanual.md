# Manualna instalacja w systemach BIOS (legacy) za pomocą instalatora Calamares

Ostatnia opcja daje ci najwięcej kontroli. Będziesz mógł dokładnie dopasować schemat partycji twojego dysku, używając wbudowanego menadżera partycjonowania.

*Ustawienie wszystkiego w instlatorze Calamares*

1: W przeciwieństwie do poprzednich scenariuszów, wybranie manualnego partycjonowania nie zmieni informacji wyświetlanej na pasku na dole okna. Naciśnij **Dalej** żeby rozpocząć partycjonowanie.

*Zwolnij miejsce*

2: Następny ekran wyświetla edytowany dysk oraz jego stan zarówno w formie paska jak i listy partycji. Obie te rzeczy przedstawiają to samo tylko w inny sposób. Przycisk **Nowa tabela partycji** umożliwia stworzenie nowej tabeli partycji, albo MBR albo GPT. To skasuje wszystkie dane i usunie wszystkie partycje na dysku. Możesz też zatrzymać obecną tabelę partycji i tylko edytować partycje na niej.

Dla przypomnienia co to są partycje i tabele partycji, zajrzyj do rozdziału **Przydatne definicje**.

3: Kliknięcie na daną partycję czy to na pasku czy na liście ją zaznaczy. Opcja **Edycja** i **Kasuj** stanie się dostępna.

4: Kliknięcie na **Edycja** otworzy następne okno z informacjami o partycji, jej wielkości, zawartości, systemem plików i punktem montowania oraz flagami, jeśli chcesz jej użyć dla instalacji Manjaro. Porcja partycji, która posiada dane jest pokazana po lewej stronie paska i jest wyróżniona lekkim pogrubieniem 3D.

5: Kliknięcie i przeciąganie na krawędzie paska partycji umożliwia zmianę jej wielkości. Nie może ona być mniejsza niż wielkość wymagana do zachowania na niej danych. Klkiknięcie na **OK** zamknie okno i uaktualni diagram i listę partycji. **Zwróć uwagę, że na razie żadna zmiana nie jest wprowadzana i dopiero po zaakceptowaniu podsumowania instalator ją przeprowadzi.**

*Tworzenie partycji*

6: Możesz wybrać zwolnione miejsce i kliknąć na **Stwórz**, by utworzyć  nową partycję używając całego wolnego miejsca lub tylko jego części.

7: Pokaże się nowe okno z informacjami o partycji, którą chcesz stworzyć. Dopasuj jej wielkość do swoich życzeń i wybierz system plików. Dla Linuxa ext4 zazwyczaj jest dobrym wyborem. Dalej, wybierz punkt montowania partycji. Opcja ta decyduje pod jakim katalogiem będzie dostępna dana partycja. **Jedynym wymogiem jest, że musisz mieć partycję zamontowaną jako /, która jest najwyższym katalogiem drzewa katalogów w Linuksie.** Resztę możesz ustawić wg własnych potrzeb. Dla przypomnienia co to jest systemy plików, zajrzyj do rozdziału **Przydatne definicje**.

8: Na przykładzie obok wybrałem stworzenie odrębnej partycji dla katalogu **/home**, który jest używany do przechowywania danych użytkowników, takich jak muzyka, obrazy, video i inne. Kiedy wszystko jest zrobione, weź moment by zweryfikować czy ustawienia zgadzają się z twoimi życzeniami. **Wszystkie partycje z wybranym punktem montowania będą użyte podczas instalacji Manjaro. Możesz porzucić wszystkie zmiany przez kliknięcie na **Cofnij wszystkie zmiany** po prawej, górnej stronie okna. Na dole masz opcję, która umożliwia decyzję czy i gdzie instalować program rozruchowy GRUB.

W tym wypadku partycja swap została już stworzona. Będzie ona użyta jeśli kiedykolwiek zabraknie wam RAMu, żeby zakończyć operacje, lub żeby hibernować komputer. Jeśli jej nie masz i chcesz stworzyć, utwórz nową partycję i wybierz **linuxswap** jako system plików. Nie musisz wybierać punktu montowania dla niej.

*Przejrzyj ustawienia i potwierdź*

9: Reszta procesu jest podobna do przedstawionego we wcześniejszym podrozdziale **Wyczyść cały dysk i pozwól instalatorowi Calamares ustawić partycje.** Tak jak poprzednio, będziesz musiał uzupełnić informacje o użytkowników oraz zobaczysz podsumowanie swoich wyborów. To twoja ostatnia szansa na wprowadzenie zmian. Po kliknięciu na **Dalej** instalacja się rozpocznie.

*Użycie GParted, żeby stworzyć, skasować i zmodyfikować partycje*

GParted jest programem graficznym używanym do modyfikacji partycji na dyskach. To potężne narzędzie i ma przyjazny interfejs. GParted pozwala na tworzenie, kasowanie jak i zmiane atrybutów partycji jak rozmiar, miejsce na dysku, system plików. Program potrafi też tworzyć tabele partycji różnego typu, między innymi najczęściej używane typu MBR (msdos) i GPT. Dla odświeżenia informacji o partycjach i tabelach partycji, sprawdź rozdział **Przydatne definicje**.
W tej sekcji zademonstrujemy jak zredukować rozmiar istniejącej partycji i użyć wolnego miejsca, żeby stworzyć dwie nowe partycje, które potem będą użyte do instalacji Manharo!

1: Zacznijmy od początku! Znajdziesz GParted w menu wersji Manjro live. Program może też być znaleziony w repozytoriach większości dystrybucji. Edycja Manjaro KDE domyślnie ma dostępny program **zarządzanie partycjami**, który spełnia podobne funkcje jak GParted jednak jego interfejs graficzny (GUI) może się nieco różnić.

*Zmniejsz istniejącą partycję*

2: Po uwierzytelnieniu hasłem, pojawi się okno podobne do tego przedstawionego obok. Pasek pokazuje graficzną reprezentacje struktury dysku, który jest zaznaczony na przycisku po prawej, górnej stronie okna. Jeśli masz więcej dysków, to jest miejsce, gdzie możesz przełączać na ten, który chcesz edytować. Każda partycja jest zaznaczona prostokątem na pasku. Zakolorowana część reprezentuje dane. Wszystkie partycje są też przedstawione w postaci listy z informacjami na ich temat.

3: Kliknięcie na na wybraną partycję na liście lub na pasku dysku wybierze ją i podświetli, co udostępni opcje, które mogą być zastosowane.

4: W górnym panelu mamy parę przycisków reprezentujących różne akcje. Pierwszy jest nieaktywny w tym momencie, ponieważ tworzy on partycję na pustej przestrzeni. Drugi kasuje partycję, a trzeci pozwala na edycję i to jest opcja, o którą ci w tej chwili chodzi.

5: Kliknięcie na nią otworzy nowe okno pokazujące wybraną partycję w postaci paska jak i opcjami poniżej. Żeby zredukować wielkość partycji kliknij i przeciągnij jej granicę na pasku albo wpisz rozmiar ręcznie. Po uzyskaniu wolnego miejsca, możesz także przeciągnąć partycję zmieniając jej pozycję i miejsce, które ma zapełnić. Kliknij na **Zmień rozmiar** kiedy skończysz. **Powinieneś zrobić wcześniej kopię zapasową wszystkich danych z partycji, której rozmiar zamierzasz zmienić.**

*Tworzenie nowej partycji*

6: Po uzyskaniu wolnego miejsca możesz stworzyć nową partycję! Wybierz i kliknij na pierwszą opcję w górnym panelu.

7: W oknie, które się pojawi, będziesz mógł ustawić wielkość nowej partycji. Domyślnie zajmuje ona całą wolą przestrzeń, ale możesz to zmienić w taki sam sposób jak przy zmianie wielkości istniejącej partycji wcześniej. Możesz też między innymi wybrać system plików używany na partycji. Dla Linuksa **ext4** zazwyczaj jest najlepszą opcją, chociaż inne formaty jak xfs czy btrfs są również dostępne. Możesz też nadać etykietę partycji, czyli nazwę jaka pokaże się w wielu menadżerach plików, przez co będziesz mógł ją łatwiej zidentyfikować. Kliknięcie na **Dodaj** zamknie okno. Dla przypomnienia o systemach plików, zajrzyj do rozdziału **Przydatne definicje**.

Jeśli twoja nowa partycja nie zajmuje całej wolnej przestrzeni, możesz powtórzyć te kroki, żeby stworzyć kolejną partycję.

*Zastosuj zmiany*

8: Klikanie na wszystkie te opcje ciągle jeszcze nie zmieniło nic na wybranym dysku. Zostały one jednak zapisane w postaci listy widocznej na dole okna. Żeby zastosować zmiany, kliknij na przycisk **Zastosuj**. **Po tym wszystkie zmiany zostaną przeprowadzone na wybranym dysku.**

9: Pokaże się nowe okno wskazujące na proces przeprowadzania zmian...

10: ... a na koniec informacje czy zmiany zostały zastosowane.

11: Gratulacje. Udało ci się stworzyć nowe partycje, na które będziesz mógł zainstalować Manjaro!
