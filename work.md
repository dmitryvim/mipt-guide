# Домашнее задание

[Главная](./README.md)
| [Создание отдельной ветки для выполнение доманего задания](./branch.md)
| [Создание отдельной ветки для выполнение доманего задания](./push.md)

Для разных сред разработки данная инструкция может различаться
1. [CLion](./import-clion.md)
2. [CodeBlocks](./import-codeblocks.md)
3. [MS Visual Studio](./import-visual-studio.md)

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
