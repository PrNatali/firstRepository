# Моё руководство по работе с Git
## Основные команды
 * команда __git init__ - служит для инициализации репозитория. Для дальнейшего отслеживаия происходящий изменений в папке.
 * команда __git add__ (название файла) - дабавляет указанный файл в отслеживание.
 
 *Прежде чем задать команду git add, мы должны сохранить редактируемый файл. Для этого воспользуемся командой Ctrl+S.*
 * команда __git commit -m "text"__ позволяет создать контрольную точку. Версию сохранения и добавить пояснительный комментарий. 
 * команда __git status__ - помогает отследить какие файлы присутствуют, в каком они состоянии, есть ли изменения, требующие сохранения. 
 * команда __git help__ - выведет в терминал список команд и их обозначения. 
 * команда __git log__ - журнал изменений. История сохранений. Отобразятся разные версии. 
* команда __git checkout + первые 4 цифры кода комита__ - позволят нам переходить в различные версии.

___Вывод:___ 
Работая с большими объемами информации и множеством строчек кода, достаточно трудно найти тот участок, на котором нужно внести правки. Для этого мы создаем различные контрольные точки с комментариями, чтобы мобильно перемещаться между версиями и продолжать работу. 

## Работа с изображениями.

Чтобы вставить изображение в текст, переместите его в рабочую папку, затем введите:
![](), где в квадратных скобках прописываем текст, который будет отображаться, если файл не загрузится. В круглых скобках - название файла с его расширением. 

## Работа с различными ветками.


* команда __git branch__ - выводит список веток. Звездочкой указывается текущая. 
* команда __git checkout name__ позволяет перейти на другую ветку. 
Чтобы вернуться на основную, вводим команду __git checkout master__. 
* чтобы отобразить все коммиты и на каких ветках они находятся, вводим команду __git log --graph__.

При вводе команды *git log*, находясь в сторонней ветке, отобразятся коммиты как с этой ветки, так и основной в хронологическом порядке с конца изменений. Остальные сторонние отображаться не будут.

* Когда мы отработали в ветке и перенесли её в основную, то мы можем её удалить. Чтобы удалить ветку, используем команду __git branch -d name__ 

## Варианты слияния.

### *Fast-forward*
когда у побочной ветки коммиты есть, а у первоисточника нет. Слияние происходит как добавление информации. 

### *Auto-merging* 
когда коммиты есть и на побочной и на основной ветке, но при этом изменения касаются разных участков и конфликт отсутствует. 

### *Conflict*
когда на разных ветках записаны одни и те же участки. Редактируем конечный результат, сохраняем, добавляем к отслеживанию, создаем commit. 

## Работа с удаленным реозиторием 
### Создание удаленного реозитория. 
* На портале GitHub В ЛК добавляем новый репозиторий
* выбираем условия, на базе чего он будет создан.
* Например,связываем локальный с удаленным.
* команда __git remote add origin ссылка__ 
* задаем имя основной ветки удаленного репозитория __git brauch -M master__
* команда __git push -u origin master__ - отравка текущего сотояния на удаленный реозиторий. Настраивает основную ветку локального репозитория, делая её достуной к отправке.
