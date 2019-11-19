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

**Добавление ssh rsa ключа из github.com**

Для добавления ssh rsa ключа из github.com выполните следующие комманды:

	mkdir /root/.ssh
	chmod 700 /root/.ssh
	curl https://github.com/your-username.keys -o  /root/.ssh/authorized_keys
	chmod 600 .ssh/authorized_keys

**Запускаем и останавливаем cjdns**

	sudo ./cjdroute < cjdroute.conf

Если вы хотите записывать логи в файл, то:

	sudo ./cjdroute < cjdroute.conf > cjdroute.log

Остановка cjdns осуществляется следующим образом:

	sudo killall cjdroute

Если вы испытываете проблемы при использовании killall cjdroute. Используйте pgrep cjdroute или top для определения, запущен ли он.

**Выводим на виртуальной машине лог узла робономики на субстрате**

	journalctl -f -u robonomics.service 


