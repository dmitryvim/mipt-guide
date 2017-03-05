# Гид по работе с github.com для студентов МФТИ (1, 2 курс)

1. Завести аккаунт github.com
2. Установка git на локальный компьютер
3. Сделать fork репозитория с домашним заданием (обновить fork)
4. Клонировать свой репозиторий на домашний компьютер
5. Создать ветку, под выполняемое задание
6. Выполнить работу на локальном комьютере, деля коммиты
7. Запушить ветку в свой репозиторий
8. Создать pull-request в master, подключив к нему преподавателя
9. Выполнить рекомендации преподавателя и сдать задание

## Завести аккаунт github.com

Современные сайты делают всё, чтобы на них было просто зарегистрироваться. Заходите на [https://github.com/](https://github.com/) и sign up for GitHub.

> Будьте внимательны при выборе username. Возможно, Вам придётся его показать будущему работодателю. Пусть Вам не будет стыдно за выбранное по-глупости имя ;) 

## Установка git на локальный компьютер

В зависимости от того, какая операционная система у Вас установлена на домашнем компьютере, Ваши действия могут слегка отличаться. По разным причинам, как разработчик, я сторонник unix систем (ubuntu, linux mint, debian, macOs), в них существует устоявшаяся традиция работы через командную строку. Говорят, что начиная с windows 10 и установки bash в систему от microsoft, жизнь стала проще, увы, не знаю, на момент написания этого текста windows для меня почти потерян (или я для windows).

Самый правильный способ установки git локально начинается с [соответствующего запроса в google](https://www.google.ru/?q=git+install#newwindow=1&q=git+install). Сразу вываливается много полезной и бесполезной информации. Скорее всего, вам подойдёт первая из 3-4 ссылок на [git-scm.com](https://git-scm.com/) или [github.com](https://github.com). Я предлагаю воспользоваться следующей [https://git-scm.com/book/ru/v2/Введение-Установка-Git](https://git-scm.com/book/ru/v2/%D0%92%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5-%D0%A3%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0-Git).

После установки git запустите git-bash в windows или обычный терминал в unix. Выполните команду

    $ git --version
    git version 2.7.4

Рекомендую убедиться, что версия git не ниже второй (у меня, как вы могли заметить, 2.7.4).

## Сделать fork репозитория с домашним заданием (обновить fork)

Итак, подготовительная работа завершена. Настало время разбираться с домашним заданием. Если таковое есть, то преподаватель, скорее всего, выслал ссылку на свой репозиторий, где он выкладывает черновики и/или формулировки домашнего задания. 

Например, вы получили вот такую ссылку [https://github.com/dmitryvim/mipt-hw-sample](https://github.com/dmitryvim/mipt-hw-sample). Открываете, не стесняетесь. Мне лень делать картинки, поэтому я верю в Вас: справа наверху, под Вашей аватаркой вы можете увидеть кнопочку *Fork* (сделать себе копию репозитория).

Если Вы всё сделали правильно, то отобразится красивая анимация и через некоторое время вы увидете крайне похожий репозиторий, но уже другой. Допустим, Ваш логин на github *dmitry-student*, тогда новая ссылка должна выглядеть вот так: [https://github.com/dmitry-student/mipt-hw-sample](https://github.com/dmitry-student/mipt-hw-sample). Это Ваша копия и Вы вольны делать с ней, что хотите, но если у Вас есть желание сдать задание, то настойчиво рекомендую следовать следующим инструкциям.


## Клонировать свой репозиторий на домашний компьютер

Ура, у каждого студента теперь есть собственный репозиторий, где он сможет выполнять домашнюю работу. Настало время сохранить его локально, чтобы можно было работать.

Открываете git bash и перемещаетесь в нужную вам директорию, туда, где будут лежать Ваши рабочие файлы. Например:

    $ cd study


> Обратите внимание, что в указанных примерах работы с командной строкой "$" ставится напротив выполняемых Вами команд (т.е. написать надо непосредственно команду "cd study", если "$" отсутствует, то это вариант ответа системы на Вашу команду)

Теперь необходимо склонировать (скопировать) репозиторий на локальную машину

    $ git clone https://github.com/dmitry-student/mipt-hw-sample
    Cloning into 'mipt-hw-sample'...
    remote: Counting objects: 11, done.
    remote: Compressing objects: 100% (6/6), done.
    remote: Total 11 (delta 0), reused 11 (delta 0), pack-reused 0
    Unpacking objects: 100% (11/11), done.
    Checking connectivity... done.

> Ещё одно замечание, Вы могли заметить (кроме пользователей macOs), что привычные ctrl+c и ctrl+v не работают. При использовании linux, помогут сочетания shift+ctrl+c и shift+ctrl+v, в windows остаётся довольствоваться командами от правой кнопки мыши. 

Обратите внимание на ссылку, в моём случае стоит username dmitry-student. В Вашем случае будет Ваше имя, например 

    $ git clone https://github.com/ivan-ivanov/mipt-hw-sample
    $ git clone https://github.com/mister-student/mipt-hw-sample
    $ git clone https://github.com/sergey-mipt/mipt-hw-sample

Теперь можете убедиться с помощью командной строки и/или стандартных средств системы (например, проводник). Что у Вас появилась новая папочка *mipt-sw-sample*. Внутри этой папки уже расположены какие-то рабочие файлы.

Дальнейшая работа будет проходить из папки проекта (в нашем случае mipt-sw-sample), зайдите внутрь этой папки с помощью команды

    $ cd mipt-sw-sample

Вы можете убедиться, что внутри рабочей папки находится скрытая директория *.git*, внутри неё вся история коммитов. 

## Создать ветку, под выполняемое задание

> см [подробнее](https://git-scm.com/book/ru/v1/%D0%92%D0%B5%D1%82%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B2-Git-%D0%9E%D1%81%D0%BD%D0%BE%D0%B2%D1%8B-%D0%B2%D0%B5%D1%82%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F-%D0%B8-%D1%81%D0%BB%D0%B8%D1%8F%D0%BD%D0%B8%D1%8F)

Есть определённые правила предосторожности, которые настойчиво рекомендуется использовать. Спросите преподавателя или google, "Почему нельзя коммитить в мастер?". Может даже новые обороты русского языка встретите. Мы будем делать вид, что соблюдаем эти предосторожности и создадим локальную ветку.

Наберите команду

    $ git branch
    * master

Если вы только начали работать, то у вас должен быть master и ничего более. Это один путь, от которого мы сейчас будет отвлетвляться

    $  git checkout -b task1
    Switched to a new branch 'task1'
    $ git branch
      master
    * task1

Теперь у вас стало две ветки master, чистая (в дальнейшем в ней будет лежать завершённое задание) и task1, ветка для выполнения задания 1.

Теперь вы можете открыть папку в Вашей среде разработки (я предпочитаю использовать CLion для c++, во время подготовки инструкции использовал sublime 2, ну а Вы опять свободны выбирать любую среду под себя).

## Выполнить работу на локальном комьютере, деля коммиты

Теперь задание получено, ветка создана, большая часть административных вопросов позади, надо приступать непосредственно к заданию.

В README.md написана формулировка задания. В нашем примере в src/cpp/sample лежит файл *sample.cpp*, который нам предстоит менять.
Откроем файл, в моём случае можно сделать так. В Вашем случае надо разобраться, как открыть и запускать файл с помощью visual studio, codeblocks или xcode (Надо найти кнопку, похожую на открыть директорию иди открыть CMake project).

    $ subl src/cpp/sample/sample.cpp

Файл откроет в текстовом редакторе

    #include <iostream>
    
    int factorial(int n);
    
    int main() {
        int n;
        std::cin >> n;
        std::cout << factorial(n);
    }

Дополним файл описанием метода factorial

    #include <iostream>
    
    int factorial(int n);
    
    int main() {
        int n;
        std::cin >> n;
        std::cout << factorial(n);
    }

    int factorial(int n)
    {
    	int result = 1;
    	for(int i = 1; i <= n; i++)
    	{
    		result *= i;
    	}
    	return result;
    }

Сохраним файл, запустите (в среде или из командной строки), проверьте, что всё работает. 

## Зафиксировать изменения 

> см [подробнее](https://git-scm.com/book/ru/v1/%D0%9E%D1%81%D0%BD%D0%BE%D0%B2%D1%8B-Git-%D0%97%D0%B0%D0%BF%D0%B8%D1%81%D1%8C-%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D0%B9-%D0%B2-%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%B9)

Теперь вернём в git bash.

Наберите команду 

    $ git status    
    On branch task1    
    Changes not staged for commit:    
      (use "git add <file>..." to update what will be committed)
      (use "git checkout -- <file>..." to discard changes in working directory)
    
    	modified:   src/cpp/sample/sample.cpp
    
    no changes added to commit (use "git add" and/or "git commit -a")

Вам подсвечивается красным, что был изменён файл sample.cpp. Если вы использовали для работы какую-то среду (особенно visual studio), то git status может подсветить ещё набор файлов, которые не важны в рамках выполняемого задания, но очень нужны для studio.

Нам надо добавить в git выполненную работу, для этого выполните следующую команду

    $ git add src/cpp/sample/sample.cpp

 Теперь проверьте git status

     $ git status
    On branch task1
    Changes to be committed:
      (use "git reset HEAD <file>..." to unstage)
    
    	modified:   src/cpp/sample/sample.cpp
    
Файл подсвечивается зелёным, это значит, что git принял изменения. Теперь их надо закоммитить, зафиксировав сделанный шаг, сопроводим commit описанием, что было сделано.

    $ git commit -m "Я выполнил задание 1"
    $ git status
    On branch task1
    nothing to commit, working directory clean

Теперь изменения сохранены, современная среда позволяет посмотреть историю изменений. Или Вы можете разобраться подробнее с [работой в командной строке](https://git-scm.com/book/ru/v1/%D0%9E%D1%81%D0%BD%D0%BE%D0%B2%D1%8B-Git-%D0%9F%D1%80%D0%BE%D1%81%D0%BC%D0%BE%D1%82%D1%80-%D0%B8%D1%81%D1%82%D0%BE%D1%80%D0%B8%D0%B8-%D0%BA%D0%BE%D0%BC%D0%BC%D0%B8%D1%82%D0%BE%D0%B2)


## Запушить ветку в свой репозиторий

Когда локально всё сохранено, надо выложить результат работы на сервер (в github)

    $ git push origin task1
    Username for 'https://github.com': dmitry-student
    Password for 'https://dmitry-student@github.com': 
    Counting objects: 6, done.
    Delta compression using up to 4 threads.
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (6/6), 540 bytes | 0 bytes/s, done.
    Total 6 (delta 1), reused 0 (delta 0)
    remote: Resolving deltas: 100% (1/1), completed with 1 local objects.
    To https://github.com/dmitry-student/mipt-hw-sample
    * [new branch]      task1 -> task1


В зависимости от настроек, которые [Вы можете поправить](https://git-scm.com/book/ru/v1/%D0%9D%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-Git-%D0%9A%D0%BE%D0%BD%D1%84%D0%B8%D0%B3%D1%83%D1%80%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-Git), система запросит login и password от сайта github.com. 

Не забываем про username, опять пройдём на страницу репозитория [https://github.com/dmitry-student/mipt-hw-sample](https://github.com/dmitry-student/mipt-hw-sample).

Примерно по центру, Вы сможете заметить надпись "2 branches". Кликните по надписи. У Вас должно отобразиться две ветки: master и task1.

## Создать pull-request в master, подключив к нему преподавателя

Ура, Вы уже загрузили сделанное задание в интернет, теперь его можно показать преподавателю или нельзя дать списать соседу. Чтобы задание считалось по-честному выполненным, его надо поместить в master через pull-request. Для этого, на экране branches напротив task1 нажимаете "New pull request". На вновь появившейся форме можно дополнить/изменить описание сделанного, чуть ниже можно увидеть изменения в коде.

Нажимайте клавишу "Create pull request". Теперь наверху отобразится ссылка похожая на [https://github.com/dmitryvim/mipt-hw-sample/pull/1](https://github.com/dmitryvim/mipt-hw-sample/pull/1), именно эту ссылку (только Вашу, с Вашим username и именем проекта) надо отправить преподавателю.

Ждём, что скажет преподаватель.

## Выполнить рекомендации преподавателя и сдать задание

Итак, отправили задание и получили комментарий. Все комментарии будут отображаться на сайте, и могут приходить на почту. Можно отправить ссылку друзьям, пусть они тоже подскажут, как можно улучшить Ваш код. 

Получив комментарий, Вам необходимо приняться за исправления. Всё по уже опробованной схеме.

1. Локально меняете файл
2. git add src/cpp/sample/sample.cpp
3. git commit -m "поправил отступы"
4. git push origin task1

Когда Вы сделаете push, pull-request будет обновляться и все увидят изменения. Так повторяем всё до тех пор, пока не получите approve. Должна отобразиться подобная запись "dmitryvim approved these changes 40 seconds ago". 

Ура, теперь можно нажимать merge и считать задание выполненным.

## итого

Нашли неточность, создавайте PR, пишите мне на почту - постараемся поправить.