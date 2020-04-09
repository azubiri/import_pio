# import_pio

## Introduction
This repository is created to learn how to import a project from Github, and use it in PlatformIO.
This will be useful for mbed and Arduino projects because they can be at the same platform.

## Tested
### Boards
- [x] STm32 Nucleo
- [ ] Arduino

### OS
- [x] Windows
- [ ] Linux

### Framework
- [x] Mbed
- [ ] Arduino

### IDE or Text editor
- [x] Visual Studio Code
- [ ] Text editor

---
## Steps
For example with this simple mbed project:
1) Clone this repository
```sh
git clone https://github.com/azubiri/import_pio
```
2) Go to your bash terminal, and change your current directory by the repository folder
```sh
cd ~/Documents/PlatformIO/Projects/import_pio
```
Go to your text editor, or your favourite IDE. Then, create "platformio.ini" file with the following content inside.
```
[env:nucleo_f303re]
platform = ststm32
board = nucleo_f303re
framework = mbed
```
As you can see in the example above, we will use a Nucleo F303RE board from ST Microelectronics on mbed framework.

After that, we can build this code. So, type in a bash terminal the :
```sh
platformio run
```
If you want to test what happens if we program our board, type:
```sh
platformio run --target upload
```
Finally, to show the message from the board, and confirm all steps are done well type the following:
```sh
platformio device monitor --port COM[3]
```
In this case, PC and board are connected through COM3 port, but be careful and check it.

---
## References
[PlatformIO Documentation](https://docs.platformio.org/en/latest/)