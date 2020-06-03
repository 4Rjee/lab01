## Laboratory work I

<a href="https://yandex.ru/efir/?stream_id=vsVJzkz4i9-s"><img src="https://raw.githubusercontent.com/tp-labs/lab01/master/preview.png" width="640"/></a>

Данная лабораторная работа посвещена изучению утилит для разработки проектов

## Tasks

- [x] 1. Ознакомиться со ссылками учебного материала
- [x] 2. Выполнить инструкцию учебного материала
- [x] 3. Составить отчет и отправить ссылку личным сообщением в **Slack**

## Tutorial

```bash
$ export GITHUB_USERNAME=4Rjee
$ export GIST_TOKEN=*******************************
$ alias edit=atom
```

```sh
$ mkdir -p ${GITHUB_USERNAME}/workspace
$ cd ${GITHUB_USERNAME}/workspace
$ pwd
/home/mint/4Rjee/workspace
$ cd ..
$ pwd
/home/mint
```

```sh
$ mkdir -p workspace/tasks/
$ mkdir -p workspace/projects/
$ mkdir -p workspace/reports/
$ cd workspace
```

```sh
# Debian
$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
--2020-06-03 14:38:32--  https://nodejs.org/dist/v12.16.1/node-v12.16.1-darwin-x64.tar.gz
Resolving nodejs.org (nodejs.org)... 104.20.23.46, 104.20.22.46, 2606:4700:10::6814:172e, ...
Connecting to nodejs.org (nodejs.org)|104.20.23.46|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 19689364 (19M) [application/gzip]
Saving to: ‘node-v12.16.1-darwin-x64.tar.gz’

node-v12.16.1-darwi 100%[===================>]  18.78M  5.51MB/s    in 3.4s    

2020-06-03 14:38:36 (5.51 MB/s) - ‘node-v12.16.1-darwin-x64.tar.gz’ saved [19689364/19689364]
$ tar -xf node-v6.11.5-linux-x64.tar.xz
$ rm -rf node-v6.11.5-linux-x64.tar.xz
$ mv node-v6.11.5-linux-x64 node
```

```sh
$ ls node/bin
node  npm  npx
$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games
$ export PATH=${PATH}:`pwd`/node/bin
$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/home/mint/workspace/node/bin
$ mkdir scripts
$ cat > scripts/activate<<EOF
export PATH=\${PATH}:`pwd`/node/bin
EOF
$ source scripts/activate
```

```sh
$ brew install gist
Warning: gist 5.1.0 is already installed and up-to-date
To reinstall 5.1.0, run `brew reinstall gist`
```

```sh
$ (umask 0077 && echo ${GIST_TOKEN} > ~/.gist)
```

## Report

```sh
$ export LAB_NUMBER=01
$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
Cloning into 'tasks/lab01'...
remote: Enumerating objects: 71, done.
remote: Total 71 (delta 0), reused 0 (delta 0), pack-reused 71
Unpacking objects: 100% (71/71), done.
$ mkdir reports/lab${LAB_NUMBER}
$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
$ cd reports/lab${LAB_NUMBER}
$ edit REPORT.md
$ gist REPORT.md
```

## Links

### Unix commands

- [ar](https://en.wikipedia.org/wiki/Ar_(Unix))
- [cat](https://en.wikipedia.org/wiki/Cat_(Unix))
- [cd](https://en.wikipedia.org/wiki/Cd_(command))
- [cp](https://en.wikipedia.org/wiki/Cp_(Unix))
- [cut](https://en.wikipedia.org/wiki/Cut_(Unix))
- [echo](https://en.wikipedia.org/wiki/Echo_(command))
- [env](https://en.wikipedia.org/wiki/Env_(shell))
- [ex](https://en.wikipedia.org/wiki/Ex_(editor))
- [file](https://en.wikipedia.org/wiki/File_(command))
- [find](https://en.wikipedia.org/wiki/Find)
- [ls](https://en.wikipedia.org/wiki/Ls)
- [man](https://en.wikipedia.org/wiki/Man_page)
- [mkdir](https://en.wikipedia.org/wiki/Mkdir)
- [mv](https://en.wikipedia.org/wiki/Mv)
- [nm](https://en.wikipedia.org/wiki/Nm_(Unix))
- [ps](https://en.wikipedia.org/wiki/Ps_(Unix))
- [pwd](https://en.wikipedia.org/wiki/Pwd)
- [rm](https://en.wikipedia.org/wiki/Rm_(Unix))
- [sed](https://en.wikipedia.org/wiki/Sed)
- [touch](https://en.wikipedia.org/wiki/Touch_(Unix))

### Package Managers

- [apt](http://help.ubuntu.ru/wiki/apt) | [dnf](https://en.wikipedia.org/wiki/DNF_(software)) | [yum](https://fedoraproject.org/wiki/Yum/ru)
- [brew](https://brew.sh) | [linuxbrew](http://linuxbrew.sh)
- [npm](https://docs.npmjs.com)

### Software

- [curl](https://www.gitbook.com/book/bagder/everything-curl/details)
- [wget](https://www.gnu.org/software/wget/manual/wget.pdf)
- [clang](https://clang.llvm.org)
- [g++](https://gcc.gnu.org/onlinedocs/gcc-4.0.2/gcc/G_002b_002b-and-GCC.html)
- [make](https://en.wikipedia.org/wiki/Make_(software))
- [open](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/open.1.html)
- [openssl](https://www.openssl.org)
- [nano](https://www.nano-editor.org)
- [tree](https://linux.die.net/man/1/tree)
- [vim](http://www.vim.org)

## Homework

1. Скачайте библиотеку *boost* с помощью утилиты **wget**. Адрес для скачивания `https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz`.

~$  wget https://sourceforge.net/projects/boost/files/boost/1.72.0/boost_1_72_0.tar.gz

--2020-06-03 15:00:36--  https://sourceforge.net/projects/boost/files/boost/1.72.0/boost_1_72_0.tar.gz

boost_1_72_0.tar.gz 100%[===================>] 120.72M   182KB/s    in 3m 22s 

2020-06-03 15:04:04 (612 KB/s) - ‘boost_1_72_0.tar.gz’ saved [126580835/126580835]

2. Разархивируйте скаченный файл в директорию `~/boost_1_69_0`

$ tar -xf boost_1_72_0.tar.gz

$ rm -rf boost_1_72_0.tar.gz

$ mv boost_1_72_0 ~/boost_1_72_0

3. Подсчитайте количество файлов в директории `~/boost_1_69_0` **не включая** вложенные директории.

~$find . -type f  -maxdepth 1 | wc -l

13

4. Подсчитайте количество файлов в директории `~/boost_1_69_0` **включая** вложенные директории.

~$find . -type f | wc -l

75698

5. Подсчитайте количество заголовочных файлов, файлов с расширением `.cpp`, сколько остальных файлов (не заголовочных и не `.cpp`).

~$find . -type f -name "*.hpp" -o -name "*.h" | wc -l

16771

~$ find . -type f -name "*.cpp" | wc -l

14708

$ find . -type f -not -name '*.hpp' -not -name '*.h' -not -name "*.cpp" | wc -l

44219

6. Найдите полный пусть до файла `any.hpp` внутри библиотеки *boost*.

~$ find `pwd` | grep 'boost/any.hpp'

/home/mint/boost_1_72_0/boost/any.hpp

7. Выведите в консоль все файлы, где упоминается последовательность `boost::asio`.
~$ grep -rwl . -e "boost::asio"

./boost_1_72_0/boost/process/spawn.hpp

./boost_1_72_0/boost/process/io.hpp

....

./boost_1_72_0/doc/html/boost_asio/overview/networking/other_protocols.html

./boost_1_72_0/doc/html/boost_asio/overview/networking/protocols.html

8. Скомпилирутйе *boost*. Можно воспользоваться [инструкцией](https://www.boost.org/doc/libs/1_61_0/more/getting_started/unix-variants.html#or-build-custom-binaries) или [ссылкой](https://codeyarns.com/2017/01/24/how-to-build-boost-on-linux/).

./bootstrap.sh

./b2

The Boost C++ Libraries were successfully built!

9. Перенесите все скомпилированные на предыдущем шаге статические библиотеки в директорию `~/boost-libs`.

mv stage/lib ~/boost-libs

10. Подсчитайте сколько занимает дискового пространства каждый файл в этой директории.

find . -type f -exec du -h {} '+'

8,0K	./libboost_stacktrace_basic.a

...

36K	./libboost_context.dylib

11. Найдите *топ10* самых "тяжёлых".

find . -type f -exec du -h {} '+' | sort -rn | head

1134K	./libboost_log.dylib

868K	./libboost_program_options.a

754K	./libboost_regex.dylib

730K	./libboost_graph.a

708K	./libboost_unit_test_framework.dylib

671K	./libboost_serialization.a

592K	./libboost_locale.dylib

485K	./libboost_graph.dylib

450K	./libboost_python27.a

448K	./libboost_program_options.dylib


```
Copyright (c) 2015-2020 The ISC Authors
```
