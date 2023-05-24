### Домашнее задание к занятию 2. «Применение принципов IaaC в работе с виртуальными машинами» Баранов Сергей


---


### Задача 1

###### Опишите основные преимущества применения на практике IaaC-паттернов.

IaaC - качественно новый подход к ведению дел в Ops. Это одномоментно и техническая реализация поставленной задачи, и документирование действий, настроек. Кодинг для описания инфраструктуры приводит нас к тому, что нужно разбираться в программировании с точки зрения получения финального продукта - программы. Остается знать опыт разработки IaaC, понимать когда и что использовать и осознанно, с ответственностью, применять то или иное в работе, всегда остается место для творчества и реализации, но применение паттернов IaaC оправдано оптимизационно и функционально.

- Ускорение производства и вывода продукта на рынок;
- Стабильность среды, устранение дрейфа конфигураций;
- Более быстрая и эффективная разработка;
- Ускоряет процесс развертывания необходимой инфраструктуры;
- Позволяет избежать ситуаций недокументированных изменений, быстрый откат изменений и деплой новых;
- Дает возможность быстро производить доставку кода для непрерывной его интеграции в продукте, а также провести тестирование.


###### Какой из принципов IaaC является основополагающим?

Идемпотентность - это свойство объекта или операции, при повторном выполнении которой мы получаем результат идентичный предыдущему и всем  последующим выполнениям.


---


### Задача 2 

###### Чем Ansible выгодно отличается от других систем управление конфигурациями?

- разработкой занимается крупная компания - RedHat;
- не требует агентов на управляемых хостах - доступ по ssh.


###### Какой, на ваш взгляд, метод работы систем конфигурации более надёжный — push или pull?

Pull, т.к. отсутствует единая точка отказа и хранения данных для доступа.


---


### Задача 3

###### Установите на личный компьютер:

VirtualBox,
Vagrant,
Terraform,
Ansible.

###### Приложите вывод команд установленных версий каждой из программ, оформленный в Markdown.

root@baranovsa:/home/baranovsa# vboxmanage --version

6.1.42r155177

root@baranovsa:/home/baranovsa# vagrant --version

Vagrant 2.3.4

root@baranovsa:/home/baranovsa# ansible --version
ansible 2.10.8

  config file = None
  
  configured module search path = ['/root/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  
  ansible python module location = /usr/lib/python3/dist-packages/ansible
  
  executable location = /usr/bin/ansible
  
  python version = 3.9.2 (default, Feb 28 2021, 17:03:44) [GCC 10.2.1 20210110]
  
root@baranovsa:/home/baranovsa#


---


### Задача 4


###### Воспроизведите практическую часть лекции самостоятельно.

Создайте виртуальную машину. Зайдите внутрь ВМ, убедитесь, что Docker установлен с помощью команды docker ps,

>Vagrantfile из лекции и код ansible находятся в папке.
>Примечание. Если Vagrant выдаёт ошибку:
>URL: ["https://vagrantcloud.com/bento/ubuntu-20.04"] 
>Error: The requested URL returned error: 404:

>выполните следующие действия:
>Скачайте с сайта файл-образ "bento/ubuntu-20.04".
>Добавьте его в список образов Vagrant: "vagrant box add bento/ubuntu-20.04 <путь к файлу>".

![monitoring](https://github.com/12sergey12/IaaC/blob/main/images/%D0%BE%D1%82%D0%B2%D0%B5%D1%824%20%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5.png)
