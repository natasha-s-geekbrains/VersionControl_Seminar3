## _Инструкция для **Git**_

git --version - команда для проверки версии git

git init - инициализация локального репозитория

git status - получить информацию от git о его текущем состоянии

git add - добавить файл или файлы к следующему коммиту

git commit -m "massage" - создание коммита

git log - вывод на экран истории всех коммитов с их хеш-кодами

git checkout - переход от одного коммита к другому

git checkout master - вернуться к актуальному состоянию и продолжить работу

git diff - увидеть разницу между текущим файлом и закоммиченным файлом

git branch -посмотреть список веток репозитории

git branch <название ветки> - создать новую ветку

git checkout <название ветки> - переход на другую ветку 

git branch -d <название ветки> - удаление ветки

git push - Отправление репозитория на удаленый репозиторий

git pull - Выкачивание актуальной версии репозитория с удаленного и сливание с локальной версией

git clone ссылка - клонирование репозитория с интернета

## Порядок работы с удаленным репозиторием для Pull Request

1. Найти на Github нужный репозиторий. Это в нашем случае чужой репозиторий, куда вы планируется сделать Push своих изменений со своего локального репозитория и где после этого должен будет остаться ваш Pull Request.
2. На страничке этого чужого репозитория с помощью кнопочки Fork скопировать его в свой аккаунт на Github.
3. На страничке скопированного репозитория в своем аккаунте с помощью кнопочки Code на закладке HTTPS скопировать ссылку на этот репозиторий.
4. Перейти в VS code и открыть там папку, куда можно будет клонировать репозиторий со своего аккаунта в Github.
5. Выполнить команду __*git clone <ссылка на репозиторий>*__.
6. С помощью команды __*cd <название папки склонированного репозитория>*__ перейти в папку репозитория и выполнить команду __*git log*__, чтобы увидеть коммиты клонированной ветки и убедиться, что клонирование прошло удачно.
7. В своем локальном репозитории создать новую ветку, куда уже можно будет вносить изменения и не забыть перейти на эту ветку.
8. Теперь можно вносить изменения. Когда изменения будут завершены и вы будете готовы поделиться ими с коллегами, изменения нужно не забыть закоммитить и сделать команду __*git push*__.
9. Git поймет, что в вашем удаленном репозитории в Github еще не была создана ветка c таким же именем, на которой вы коммитили изменения в локальной версии. Git не выполнит вашу команду, а предложит вам сначала другую команду, с помощью которой вы сможете создать ветку с таим же именем на удаленном репозитории в Github. __*git push --set-upstream origin <название ветки>*__.
10. Теперь нужно перейти в свой аккаунт на Girhub и обновить страничку с удаленным репозитарием. На страничке появятся переправленные вами изменения и большая зеленая кнопочка __*Compare and pull request*__. Нужно нажать на эту кнопочку, чтобы переправить изменения из своего аккаунта в связанный финальный репозиторий, куда вы изначально и планировали отправить свои наработки.
11. Github в промежуточной форме автоматически предложит имя запроса (его можно поменять) и поле для сопроводительных комментариев. После этого нужно нажать большую зеленую кнопочку __*Create pull request*__.
12. Girhub переправит тебя на страничку финального репозитория, где можно будет увидеть свой Pull request и, например, проверить, содержит ли он все нужные последние изменения.
13. После этого останется только дождаться, когда ваш Pull request прйдет контроль и вы получите ответ.

## Дополнительная информация о работе с удаленными репозитариями

1. **git pull** - скачать изменения из удаленного репозитария в свой (при условии, что он уже до этого "подружился" с вашим локальным репозиторием)
2. Если вы создаете на Github новый пустой репозиторий, то Github предложит вам разные наборы команд для ваших разных возможных целей. Например, чтобы "подружить" ваш уже имеющийся репозиторий со вновь созданным на Github, будут предложены следующие команды для выполнения на локальном терминале: 
     *  **git branch -M main** - для переименования основной ветки локального репозиория в ветку main (в случаях, если она имеет другое название. Например, в VS Code основная ветка называется master).
     * __*git remote add origin <ссылка на ваш новый репозитарий на Github>*__ - подключение удаленного репозитария к локальному
     * __*git push -u origin main*__ - для корректного переноса информации из локального репозитория в удаленный.

