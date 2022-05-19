# javahw10
Домашнее задание к занятию "Объекты с внутренним состоянием, управление состоянием при тестировании"
# Задание 1. Радиоман (обязательное к выполнению)

Проект "Умный дом" развивается и было решено улучшить часть, отвечающую за Радио.

Что нужно сделать: внедрить изменения в сам класс и тесты.

Как это сделать:

* Создайте в Git в том же репозитории новую ветку: flexible (возьмите проект к ДЗ про радио, в который уже подключен CI и нужные плагины)
* Модифицируете класс `Radio` под новые требования
* Делаете тест-дизайн новой версии класса, модифицируете или добавляете новые тесты
* Пушите всё на Github и делаете Pull Request (мёржить его НЕ НУЖНО!)
* Удостоверьтесь, что все тесты в CI запускаются на Pull Request и проходят
* Ссылку на Pull Request пришлите в качестве результата ДЗ.

Требования к работе с радиостанциями:

1. Можно задавать **количество радиостанций** при создании объекта (по умолчанию - 10).
1. Номер текущей радиостанции изменяется в пределах от 0 до количества радиостанций невключительно (т.е. если станций 10, то номер последней - 9).
1. Если текущая радиостанция - максимальная, и клиент нажал на кнопку next (следующая) на пульте, то текущей должна стать 0-ая.
1. Если текущая радиостанция - 0, и клиент нажал на кнопку prev (предыдущая) на пульте, то текущей должна стать максимальная.
1. Всё также должен присутствовать сеттер текущей станции.

Теперь объекты радио в своём поле будут хранить и количество станций, заданное при создание объекта радио (для чего вам понадобится создать свой конструктор для класса `Radio`, принимающий параметром желаемое количество радиостанций и сохраняющего это значение у себя в поле). Ещё один конструктор потребуется без параметров, чтобы если пользователь нашего класса не захотел бы указывать количество радиостанций, мы бы выставили их количество в 10 штук (см. в требованиях "по умолчанию - 10").

ВНИМАНИЕ: конструктором с параметром задаётся именно количество радиостанций, а не номер максимальной, это разные вещи - если станций, например, 30 (количество), то последней будет 29 (номер максимальной), тк нумеруем с нуля.

Требования к работе с уровнем громкости звука:

Клиент должен иметь возможность увеличивать и уменьшать уровень громкости звука (в пределах от 0 до 100)
Если уровень громкости звука достиг максимального значения, то дальнейшее нажатие на + не должно ни к чему приводить
Если уровень громкости звука достиг минимального значения, то дальнейшее нажатие на - не должно ни к чему приводить

Итого: отправьте ссылку на Pull Request пришлите в качестве результата ДЗ.
