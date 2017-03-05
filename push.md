# Отправка выполненного задания в личный репозиторий

[Главная](./README.md)
| [Непосредственное выполнение задания](./work.md)
| [Демонстрация выполненного задания преподавателю](./pull-request.md)

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