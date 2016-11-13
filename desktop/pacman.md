# Instalacja oprogramowania - pacman
Menedżerem pakietów w Manjaro jest **pacman** - nazwa wywodzi się od **pac** kage **man** ager. Pacman jest narzędziem konsolowym, stworzonym przez Judda twórcę dystrybucji Arch Linux i rozwijanym przez deweloperów Archa. Za jego pomocą możesz instalować, aktualizować, konfigurować, przeszukiwać lub usuwać pakiety. Poniżej kilka przykładów użycia pacmana.
### Aktualizacja systemu
W celu aktualizacji systemu, wydaj następującą komendę:
```sudo pacman -Syu```

### Synchronizacja lokalnej bazy pakietów z repozytoriami Manjaro
System Manjaro posiada bazę danych ze wszystkimi pakietami oprogramowania, które są dostępne w oficjalnych repozytoriach. Baza ta jest niezbędna, aby menedżer pakietów pacman mógł zlokalizować oraz pobrać pakiety do ich instalacji. Kiedy aktualizujesz system ta baza jest również automatycznie odświeżana. Za pomocą poniższej komendy możesz kompletnie przebudować bazę danych pacmana, a nie tylko ją odświeżyć i zaktualizować.

```sudo pacman -Syy```

Aby za pomocą jednej komendy zarówno zsynchronizować bazę danych pakietów oraz zaktualizować system wpisz:

```sudo pacman -Syyu```

### Wyszukiwanie pakietów
Za pomocą pacmana możemy także wyszukiwać pakiety, zarówno te zainstalowane jak i dostępne w repozytoriach Manjaro.
#### Przeszukiwanie repozytoriów Manjaro
Aby wyszukać pakiet:
```pacman -Ss [nazwa pakietu]```

Przykładowo aby sprawdzić czy w repozytorich dostępny jest menedżer plików krusader:

```pacman -Ss krusader```
#### Wyszukiwanie wśród zainstalowanych pakietów
Aby uzyskać informacje o pakiecie, który mamy już zainstalowany w systemie wydajemy polecenie:
```pacman -Q [nazwa pakietu]```
Więcej informacji o pakiecie wyświetli nam polecenie:
```pacman -Qi [nazwa pakietu]```
Aby wyświetlić listę wszystkich zainstalowanych pakietów:
```pacman -Qq```
### Pobieranie i instalowanie pakietów
Pakiety mogą być pobierane oraz instalowane z wielu źródeł, nie tylko z oficjalnych repozytoriów Manjaro. **Pamiętaj jednak, że gdy instalujesz pakiety spoza oficjalnych repozytoriów robisz to na własne ryzyko.**
#### Pakiety z oficjalnych repozytoriów
Instalacja pakietu:
```sudo pacman -S [nazwa pakietu]```
Przykładowo aby zainstalować menedżer plików krusader:
```sudo pacman -S krusader```
#### Pakiety z dysku lub z Internetu
Aby zainstalować pakiet, który mamy pobrany na dysku (nazwa pliku powinna się kończyć na **pkg.tar.xz**):
```sudo pacman -U [/ścieżka/][nazwa pakietu.pkg.tar.xz]```
Aby zainstalować pakiet za pomocą URL (znajdujący się gdzieś w Internecie):
```sudo pacman -U http://manjaro.pl/repo/pakiet.pkg.tar.xz```
### Usuwanie programów
Aby odinstalować pakiet z systemu:
```sudo pacman -R [nazwa pakietu]```
Więcej informacji na temat pacman można znaleźć na wiki lub w manualu:
```man pacman```
