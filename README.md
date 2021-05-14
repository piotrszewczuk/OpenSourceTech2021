# OpenSourceTech2021

## Instrukcja uruchomienia środowiska laboratoryjnego

**Wymagane komponenty**

Komputer PC z systemem operacyjnym MS Windows 10, Apple macOS lub Linux
- procesor min. 4 rdzeniowy lub 2 rdzeniowy z technologią Hyper-Threading i włączoną opcją wirtualizacji w BIOS
- min. 8 GB pamięci RAM
- min. 40 GB wolnej przestrzeni dyskowej

Dodatkowo w systemie operacyjnym powinno zostać zainstalowane następujące oprogramowanie:

- Vagrant - narzędzie do automatyzacji uruchamiania środowisk wirtualnych https://www.vagrantup.com/downloads
- VirtualBox - środowisko wirtualizacyjne https://www.virtualbox.org/wiki/Downloads
- Git - narzędzie do kontroli wersji plików https://git-scm.com/downloads

> Instalacja powyższych komponentów wymaga posiadania uprawnień Administratora systemu operacyjnego. 

**Uruchomienie środowiska laoratoryjnego**

Po instalacji wymaganego oprogramowania należy pobrać plik z definicją laboratoryjnego środowiska Ansible:
- https://github.com/piotrszewczuk/OpenSourceTech2021/raw/main/Vagrantfile

> Przy pobieraniu pliku Vagrantfile ważne jest aby go zapisać w takiej postaci w jakiej jest udostępniony na stronie GitHub, bez żadnych rozszerzeń, zmian itp 

- 

```bash
mkdir c:\OpenSourceTech
cd c:\OpenSourceTech
vagrant up
```
- w systemach Apple macOS i Linux
```bash
mkdir ~/OpenSourceTech
cd ~/OpenSourceTech
vagrant up
```

