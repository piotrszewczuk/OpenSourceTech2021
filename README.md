# OpenSourceTech2021

## Instrukcja uruchomienia środowiska laboratoryjnego

1. **Wymagane komponenty**

Komputer PC z systemem operacyjnym MS Windows 10, Apple macOS lub Linux o następujących minimalnych parametrach:
- procesor min. 4 rdzeniowy lub 2 rdzeniowy z technologią Hyper-Threading i włączoną opcją wirtualizacji w BIOS
- min. 8 GB pamięci RAM
- min. 40 GB wolnej przestrzeni dyskowej

Dodatkowo w systemie operacyjnym powinno zostać zainstalowane następujące oprogramowanie:

- Vagrant - narzędzie do automatyzacji uruchamiania środowisk wirtualnych https://www.vagrantup.com/downloads
- VirtualBox - środowisko wirtualizacyjne https://www.virtualbox.org/wiki/Downloads
- Git - narzędzie do kontroli wersji plików https://git-scm.com/downloads

> Instalacja powyższych komponentów wymaga posiadania uprawnień Administratora systemu operacyjnego. 

2. **Uruchomienie środowiska laoratoryjnego**

Po instalacji wymaganego oprogramowania należy pobrać plik z definicją laboratoryjnego środowiska Ansible i zapisać go w lokalnym katalogu np. 'OpenSourceTech' na dysku C: (w sytemach MS Windows) lub w katalogu domowym użytkownika (w systemach Apple macOS i Linux):
- https://github.com/piotrszewczuk/OpenSourceTech2021/raw/main/Vagrantfile

> Przy pobieraniu pliku Vagrantfile ważne jest, aby go zapisać w takiej postaci w jakiej jest udostępniony na stronie GitHub, bez żadnych rozszerzeń, zmian itp 

Po pobraniu pliku Vagrantfile należy uruchomić terminal i wykonać następujące polecenia: 
- w systemie MS Windows
```bash
cd c:\OpenSourceTech
vagrant up
```
- w systemach Apple macOS i Linux
```bash
cd ~/OpenSourceTech
vagrant up
```

