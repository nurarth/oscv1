git clone https://github.com/smartiqaorg/geometric_lib.git - Клонируем репозиторий
cd geometric_lib - Переходим в папку репозитория
git checkout develop
git checkout release
git log --all --pretty=oneline --graph
git checkout main - Возвращаемся на ветку main
git merge develop --no-ff - Вливаем ветку develop в ветку main в --no-ff режиме (мердж с дополнительным коммитом)
git log --all --pretty=oneline --graph 
git reset --hard HEAD^ - Удаляем коммит, полученный в предыдущем задании
git log --all --pretty=oneline --graph 
git merge develop --ff - Вливаем ветку develop в main в ff-режиме (перемотка без дополнительного коммита)
git log --all --pretty=oneline --graph 
git config merge.conflictstyle diff3 - Попросим Git выводить базу слияния при просмотре конфликта
git config --global merge.tool meld - Установим meld для разрешения конфликтов
git checkout release 
git rebase -i main - Выполняем интерактивный ребейз ветки release относительно main
git mergetool - Разрешаем конфликт  
git rebase --continue - Продолжаем ребейз
git mergetool - Снова конфликт. Разрешаем его.
git rebase --continue - Продолжаем ребейз 
git log --all --pretty=oneline --graph
git checkout main 
git merge release --ff - Выполняем fast-forward мердж ветки release в ветку main
git log --pretty=oneline --graph
