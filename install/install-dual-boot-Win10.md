#Dual-boot z Microsoft Windows 10

Windows używa innego schematu partycji niż stosowanego zwykle w Linuksie. Ten rozdział skupia się na różnicach między instalacją Manjaro jako jedynego systemu a instalacją obok systemu Microsoft Windows 10.

*Ściągnij plik instalacyjny*

Musisz upewnić się, że ściągnąłeś wersję 64-bit Manjaro. Nie ma znaczenia jaką edycję wybrałeś, ale nazwa pliku instalacyjnego musi kończyć się na **x86_64.iso**.
Następnie stwórz nośnik instalacyjny, nagrywając plik iso na DVD lub pamięć USB. Dla użytkowników Windows polecamy program Rufus, który powinien mieć poniższe ustawienia:

*Urządzenie*: "wybierz swoje urządzenie USB" (Uwaga: koniecznie wybierz poprawne urządzenie, bo zostanie ono sformatowane!)

*Schemat partycjonowania:* Schemat partycjonowania GPT dla UEFI

*System plików:* FAT32 (Domyślne)

*Rozmiar jednostki alokacji:* 4096 bajtów (Domyślne)

*Nowa nazwa Woluminu:* Manjaro64x (lub inna rozpoznawalna, krótka nazwa, która będzie wyświetlana w menedżerze plików po podłączeniu USB)

*Opcje formatowania:* Szybkie formatowanie. Utwórz bootowalny dysk używając Obraz ISO (wybierz plik instalacyjny Manjaro). Utwórz rozszerzoną nazwę i pliki ikon.

Kliknij na **Start** i to wszystko (proces może trwać od 2-5 min.)!

Kiedy skończysz, zrestartuj komputer i uruchom system z USB jak to było wcześniej wyjaśnione w rozdziale automatycznej instalacji w trybie UEFI.

1: Rufus z polecanymi ustawieniami.

*Automatyczna instalacja

Jeśli nie chcesz zawracać sobie głowy ustawianiem wszystkiego manualnie, możesz pozwolić Calamares wykonać całą brudną robotę za ciebie!

2: Używając automatycznej instalacji Manjaro obok Windows, wybierz partycję używaną jako dysk C: przez Windows. Zwykle to ta największa. Przesuń pasek wielkości partycji tak jak jest to przedstawione w rozdziale instalacji obok istniejącego systemu, żeby zwiększyć lub zmniejszyć wielkość partycji, która będzie stworzona na potrzeby Manjaro. Partycja Windows EFI jest wykrywana automatycznie. Dla przypomnienia informacji o partycjach i tablicach partycji przeczytaj rozdział **Przydatne definicje**.

*Instalacja manualna*
 
 Można też użyć manualnego partycjonowania. Kroki przedstawione poniżej są bardzo podobne do tych zaprezentowanych w rozdziale **Manualna instalacja w systemach BIOS** i **Tworzenie nowej partycji**.
 
 *Wybierz partycję EFI*
 
 3: Partycja EFI stworzona przez Windows może być użyta dla Manjaro. Wybierz windowsową partycję EFI i naciśnij **Edycja**. Partycja EFI powinna być tą jedyną używającą systemu plików fat32 z flagą esp i boot. Dla odświeżenia informacji o systemach plików przeczytaj rozdział **Przydatne definicje**.
 
 4: Koniecznie wybierz **Zachowaj**, żeby nie ruszać zawartości partycji. Wybranie opcji formatowania skasuje pliki startowe Windowsa i stracisz możliwość uruchomienia tego systemu! Następnie wybierz **/boot/efi** jako punkt montowania i upewnij się, że są zaznaczone flagi **boot** i **esp**. Punkt montowania wskazuje, z którego katalogu ta partycja będzie dostępna po instalacji Manjaro.
 
 *Zmniejszenie partycji C:*
 
 5: Tak jak w poprzedniej sekcji tylko, że tym razem będziesz musiał sam znaleźć, zaznaczyć i **edytować** tą partycję (zwykle jest to największa ze wszystkich).
 
 6: Możesz użyć paska na górze okna, które reprezentuje edytowaną partycję. Lewa część z efektem 3D reprezentuje dane na partycji. Nie możesz skurczyć jej poniżej tego poziomu a czasem i nawet będziesz musiał zostawić więcej (partycja Windows może mieć nieprzenośne pliki na pustym dysku, do wirtualnej pamięci i przywracania systemu, których nie da się ruszyć, dopóki nie wyłączysz tych opcji). Tak samo jak przy edycji partycji EFI, musimy zaznaczyć **Zachowaj**, inaczej stracimy całą zawartość partycji z Windowsem!

 7: Następnie wybierz wolne miejsce i kliknij na **Utwórz**.
 
 8: Teraz utworzymy partycję **swap**, używaną, kiedy systemowi zabraknie pamięci RAM lub będziesz chciał użyć opcji hibernacji systemu. Zwykle ta partycja powinna mieć parę GB (jeśli masz 4 GB RAM lub mniej, ustaw 4-8GB, jeśli masz 8 GB RAM, ustaw 8GB, jeśli masz 12-16GB RAM, zwykle 8GB też powinno wystarczyć). Partycja ta używa systemu plików linuxswap. Nie musisz jej montować.
 
 *Utwórz nową partycję*
 
 9: Teraz możesz stworzyć partycje dla Manjaro! W tym przykładnie wybrana jest tylko pojedyncza partycja systemowa z systemem plików ext4 zamontowana jako root czyli /. Możesz utworzyć też dodatkowe partycje dla /home (w razie reinstalacji zachowają się na niej pliki użytkownika)  i innych. Niezależnie od wybranego schematu partycji co najmniej jedna z nich musi mieć punkt montowania /.
 
 *Przejrzyj ustawienia i potwierdź*
 
 10: Przechodząc przez instalator dojdziesz do podsumowania, gdzie będziesz miał okazję przejrzeć wszystkie swoje wybory i ewentualnie wrócić by je zmienić. Jeśli jesteś zadowolony z nich, możesz kliknąć na **Dalej** i zacząć następny etap instalacji. Po tym momencie nie będzie już możliwości zmiany!

 *Aktualizacja GRUB, gdzie się podział Windows?*
 
 Czasami zdarza się, że program bootujący Grub2 nie wykryje istniejącej instalacji systemu Microsoft Windows. To oznacza, że tylko Manjaro Linux pojawi się na liście systemów operacyjnych podczas startu komputera.
 
 Żeby rozwiązać ten problem, uruchom Manjaro, zaloguj się do systemu, otwórz terminal i użyj komendy:
 
 sudo update-grub
 
Wymagane jest podanie hasła użytkownika (jego wpisywanie nie będzie się pojawiać w terminalu, to normalne). Po restarcie systemu GRUB powinien mieć opcję wybrania Windows w menu.
 
 To samo można osiągnąć używając programu graficznego grub-customizer, który jest dostępny w AUR (można go zainstalować przez program pamac po włączeniu AUR lub przez octopi po kliknięciu na ikonę obcego i wyszukaniu wspomnianego pakietu, albo przez komendę yaourt w terminalu).
