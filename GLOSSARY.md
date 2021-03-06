# Słowniczek

## Partycja
Partycja to część dysku twardego, która przechowuje dane (pliki), używając pewnego formatu zwanego *systemem plików*. Partycja może być przeznaczona dla systemu operacyjnego lub do przechowywania plików. Dysk twardy może być podzielony na wiele partycji, a każda z nich będzie działać jako osobny byt z własnym systemem plików. Wszystkie dyski, czy to twarde lub SSD, jak np. pamięć USB, zawierają jedną lub więcej partycji. Przykładem partycji jest dysk C używany przez Microsoft Windows.

## System plików
System plików jest formatem zapisu plików na partycji. Niektóre popularne systemy plików to **ntfs** (używany przez Microsoft Windows), **ext4** (używany przez Linuksa), fat32, btrfs i xfs. Każdy z nich jest używany w innych sytuacjach i ma swoje mocne i słabe strony. Na przykład, fat32 może być czytany przez każdy system operacyjny, jednak każdy plik na nim musi być mniejszy niż 4GB.

## Tablica partycji
Tablica partycji jest listą wszystkich partycji istniejących na dysku. Dwa główne typy to Master Boot Record (MBR) i GUID Partition Table (GPT). Różne tablice partycji pozwalają na różne typy partycji, jak np. partycja podstawowa czy rozszerzona. Tablica MBR jest stosowana w starszych systemach BIOS i może zawierać ograniczoną liczbę partycji podstawowych, podczas gdy GPT jest używana na nowszych systemach UEFI i nie ma takich ograniczeń. Jednak nie zawsze tak jest.

## Katalog
Katalog w Linuksie (ang. directory) to mniej więcej to samo co folder w Windowsie (ang. folder) i możesz je traktować jako jedno i to samo.

## Punkt montowania
Punkt montowania reprezentuje katalog, z którego jest dostępna dana partycja. Tak jak klikanie na C w menedżerze plików Windows dawało dostęp do zawartości partycji, klikanie na dany katalog w Linuksie daje dostęp do zamontowanej partycji.

Parę programów jest używanych do bootowania (startu) systemu na twoim komputerze: od uruchomienia sprzętu (ang. hardware) do logowania się na systemie operacyjnym.

## BIOS
(ang. Basic Input/Output System) to oprogramowanie firmowe używane podczas bootowania (startu systemu) do inicjalizacji sprzętu (ang. hardware). Oferuje różne ustawienia w menu po naciśnięciu specyficznego klawisza podczas bootowania. Systemy używające BIOS mają najczęściej tablicę partycji MBR.

## UEFI
(ang. Unified Extensible Firmare Interface) jest następcą BIOSu i jest używany najczęściej na nowszych komputerach. Ciągle posiada menu podobne do BIOSu i oferuje tzw. legacy mode, który używa BIOS. System partycji używany przez systemy i komputery UEFI jest nieco inny od tego używanego przez BIOS. Na przykład, mała partycja fat32 jest potrzebna, żeby przechowywać pliki potrzebne do rozruchu komputera. Systemy UEFI mają tablicę partycji GPT.

## Program rozruchowy
 (ang. boot loader) jest programem, który umożliwia ci wybranie systemu operacyjnego po włączeniu komputera. Podczas startu jest wyświetlana lista wszystkich wykrytych systemów operacyjnych. Jednym z najczęściej używanych programów rozruchowych w Linuksie jest **GRUB** i jest on instalowany przez Calamares - instalator używany przez Manjaro.
