Notatka w MarkDown na GitHub opisująca wykonane ćwiczenia (środowisko pracy, linux - podstawowe polecenia, git, GitHub, gcc, pierwsze programy)

Inicjowanie GITa w folderze lokalnym
Instalacja GITa w systemie Linux

    Instalacji programu GIT dokonuje się poprzez polecenie w konsoli: sudo apt install git

Jak stworzyc Pierwszy folder

    W terminalu należy przejść do wybranej lokalizacji i wpisać polecenie mkdir repo1 a kolejnie cd repo1

    Lista dostępnych komend  będzie pod poleceniem git help

Jak stworzyc Pierwszy plik

    Aby utworzyć plik testowy w konsoli wpisz komendę touch test.txt lub > test.txt

Inicjowanie GITa

    Wykonaj polecenie git init
    Przy użyciu polecenia ls -la dokonaj sprawdzenia czy został utworzony katalog .git

Konfigurowanie GITa
Konfigurowanie połączenia z github.com
Za pierwszym razem wymagane jest podanie danych do zdalnego repozytorium Git'a.

    W tym celu użyj komendy:git config --global user.email "adres@email.com" podając adres email do konta na github.com
    Następnie podaj nazwę użytkownika z github.com: git config --global user.name "nazwa_użytkownika"

Praca z wykorzystaniem GITa
Sprawdzanie zmodyfikowanych plików

Aby sprawdzić zmodyfikowane pliki użyj polecenia: git status
Dodawanie plików do zdalnego repozytorium

    Dodanie pliku do repozytorium odbywa się za pomocą polecenia: git add "nazwa_pliku" lub aby dodać wszystkie zmodyfikowanie pliki git add .
    Następnie dodaj komentarz do wprowadzonych zmian: git commit -m "Komentarz"
    Historię wprowadzonych zmian wyświetlisz dzięki poleceniu: git log

Wysyłanie plików na serwer

Wysłanie pliku(ów) następuje po poleceniu: git push -u origin master. Należy zauważyć, że po wskazaniu gałęzi origin-master kolejne komendy mogą ograniczyć się do git push do czasu zmiany gałęzi na inną.
Pierwszy program w C

Aby utworzyć plik zawierający kod programu należy wykonać polecenie

touch <nazwa_pliku.c>

a następnie otworzyć plik w edytorze tekstowym np. Nano:

nano <nazwa_pliku.c

W edytorze należy napisać program zgodnie ze standardem języka C. Np.:

#include <stdio.h>
int main (void)
{
puts ("Hello World!");
return 0;
}

Kompilowanie programu za pomocą GCC

Aby dokonać kompilacji napisanego programu należy zainstalować program GCC. W Linuksie należy użyć komendy

sudo apt install gcc

Następnie w celu kompilowania używamy:

gcc <nazwa_pliku.c> -o <nazwa_pliku.o>

Można dodatkowo zastosować parametr -Wall w celu szczegółowego sprawdzenia kodu.
Uruchamianie programu

W terminalu wpisujemy>

/.<nazwa_pliku.o>
