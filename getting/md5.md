# Sprawdzenie sum kontrolnych MD5

Zanim wypalimy pobrany obraz dysku (lub użyjemy go jako wirtualnego dysku w VirtualBox) należy sprawdzić czy został on poprawnie pobrany. Naprawdę zalecamy sprawdzić integralność obrazu przed jego użyciem, ponieważ skutki użycia uszkodzonego dysku mogą być fatalne. W najlepszym przypadku instalacja nie powiedzie się. Może też się zdarzyć, że uszkodzony obraz iso spowoduje, że zainstalowany system będzie uszkodzony.

Aby zweryfikować integralność pobranego obrazu musimy pobrać pliki zawierające jego sumy kontrolne. Są one dostępne na serwerze z którego pobieramy obrazy iso. Przykładowo plik **manjaro-xfce-15.12-x86_64-sha1sum.txt** zawiera sumy kontrolną obrazu iso Manjaro XFCE 15.12. Jego zawartość powinna być podobna do listingu:

```
ba3322bcd7a34855582913b581abecc6b81e256e  manjaro-xfce-15.12-x86_64.iso
```

### MD5 oraz SHA-1
Są dwa rodzaje plików zawierających sumy kontrolne. Pierwszy kończy się na **-sha1sum.txt**, drugi na **-md5sum.txt**. MD5 oraz SHA to dwa typy kryptograficznych funkcji skrótu; cząstka **sha** w nazwie pliku pochodzi od **Secure Hash Algorithm**. Algorytmy te są używane do generowania unikalnego skrótu (hash code) dla każdego pliku iso z obrazem dysku. Sam plik z sumami kontrolnymi to plik tekstowy zawierający hashkody (skróty), które powinny odpowiadać kodom wygenerowanym przez algorytm MD5 lub SHA-1. Pobrane pliki mogą być sprawdzone czy są identyczne z tymi na serwerze - jeśli plik uległ zmianie, np. z powodu błędów podczas pobierania wygenerowany kod będzie inny.

### Sprawdzanie sum kontrolnych na Linuksie

Przykładowo jeśli pobraliśmy obraz iso do katalogu `ISO`, musimy do niego wejść:

```
cd ISO
```
oraz wygenerować sumę kontrolną obrazu iso poleceniem:

Dla sumy sha1:

```
[daniel@manjaro ISO]$ sha1sum manjaro-xfce-15.12-x86_64.iso
ba3322bcd7a34855582913b581abecc6b81e256e  manjaro-xfce-15.12-x86_64.iso


```
Dla sumy md5:

```
[daniel@manjaro ISO]$ md5sum manjaro-xfce-15.12-x86_64.iso
37402f11a79ee7091987f6026901027d  manjaro-xfce-15.12-x86_64.iso

```

Polecenia wygenerują sumy kontrolne dla 64 bitowego obrazu iso Manjaro XFCE 15.12. Należy je porównać z tymi zawartymi w pliku z sumami kontrolnymi.

### Sprawdzanie sum kontrolnych na Windows

System Windows domyślnie nie udostępnia narzędzi do sprawdzania sum kontrolnych, dlatego też musimy pobrać i zainstalować odpowiednią aplikację.

Jednym z takich programów posiadających pozytywne recenzje jest **Raymond's MD5 & SHA Checksum Utility**. Programik można pobrać ze strony Download.com http://download.cnet.com/MD5-SHA-Checksum-Utility/3000-2092_4-10911445.html

![Dupa](../images/win_checksum.png)

Weryfikacja sumy kontrolnej za pomocą tego programu jest bardzo łatwa. Klikamy **Browse**, odnajdujemy pobrany obraz iso i klikamy **Open**. Program obliczy sumy kontrolne dla naszego obrazu iso. Aby sprawdzić czy sumy kontrolne się zgadzają otwieramy plik **manjaro-0.8.12-sha1sum.txt** w Notatniku, kopiujemy z niego sume kontrolną dla pliku iso ktory pobraliśmy i wklejamy do pola **Hash**. Klikamy **Verify**. Jeśli sumy się zgadzają program poinformuje nas o tym komunikatem: **Hash matched**.
