# Заметки
* [Исходники документации по работе с Aira](https://github.com/airalab/aira/tree/master/docs)
* [Сборка документации по работе с Aira](https://aira.readthedocs.io/en/latest/getting_started.html)
* Канал обновлений Aira под Nix: [https://aira.life/channels/aira-unstable/](https://aira.life/channels/aira-unstable/)
* Последняя версия образа aira для rpi4: [https://aira.life/channels/aira-unstable/](https://aira.life/channels/aira-unstable/)

## Подсказки

**Перейти на канал Airapkgs в Nix:**

Для подключения к unstable каналу репозитория выполните:

    nix-channel --remove nixos
    nix-channel --add https://aira.life/channels/aira-unstable/ nixos

Для просмотра списка подключенных каналов выполните:

    nix-channel --list

Обновление кеша канала:

    nix-channel --update

Обновление конфигурации ОС. Для применения изменений необходио выполнить:

    nixos-rebuild switch
