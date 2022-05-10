#misimovic_obs

#SSH ключ

Введите в терминале команду:
```
$ ssh-keygen -t ed25519 -C "example_email@domen.com"
```

> Generating public/private ed 25519 key pair
Затем введите название файла, в котором будет сохранён SSH ключ (или можно ввести Enter, в результате чего расположение файла будет стандартным).
> Enter a file in which to save the key (/Users/you/.ssh/id_ed25519)
Также появится возможность добавить пароль (лучше это не делать).
> Enter passphrase (empty for no passphrase): [Press enter]
> Enter same passphrase again: [Press enter]
Запустите ssh-агента командой:
```
$ eval "$(ssh-agent -s)"
```
В терминале появится сообщение:
```
> Agent pid 59566
```
Добавьте приватный ключ в ssh-агент с помощью команды:
```
$ ssh-add ~/.ssh/id_ed25519
```
Если при создании ключа ему было дано другое имя, нужно указать его.


Откройте файл SSH ключа и скопировать содержимое в буффер обмена.

В GitHub в разделе Settings выберете подраздел SSH and GPG keys.

Нажмите на New SSH key или Add SSH key.

В поле Key вставьте ключ из буффера обмена.


Для завершения нужно нажать зелёную кнопку Add SSH key.

Клонирование репозитория

Перейдите на страницу интересующего вас репозитория на GitHub.

Нажмите на зелёную кнопку Code.

Выберете раздел SSH.

Скопируйте ссылку с буффер обмена
```
https://github.com/mi12q
```
В терминале выполните команду:
```
$ git clone https://github.com/mi12q
```
