## Демо инъекции dylib в ipa для non-jailbroken устройств

### Инструкции
1. Создать / получить отвязанный IPA файл. Пример файлов, а также инструкцию по экспорту с Jailbroken устройств можно найти на 4pda.
2. Xcode -> New project -> Framework (Dynamic). Target: iPhoneOS
    * [Пример](https://github.com/GN-OS/Bloard) open-source твика (формат deb), созданного в Theos.
3. Скопируй полученный dylib в папку dylib.
    * Здесь также могут понадобиться стандартные swift либы: ```/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/lib/swift```
4. Запусти inject.sh  ```sh ./inject.sh original.ipa ./dylib```
5. Подпиши полученный ```original-patch.ipa``` с помощью [Cydia Impactor](http://www.cydiaimpactor.com).

### Лицензии
* [optool](https://github.com/alexzielenski/optool)
* inject.sh — Forked from [patchapp.sh](https://github.com/bamtan/PokemonGoAnywhere/blob/master/patchapp.sh)
* [Остальное](..)
