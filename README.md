# Square-game
JS game - click the square

ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ГОРОДА МОСКВЫ ДОПОЛНИТЕЛЬНОГО ПРОФЕССИОНАЛЬНОГО ОБРАЗОВАНИЯ ЦЕНТР ПРОФЕССИОНАЛЬНЫХ КВАЛИФИКАЦИЙ И СОДЕЙСТВИЯ ТРУДОУСТРОЙСТВУ «ПРОФЕССИОНАЛ»
 
 
ПОЯСНИТЕЛЬНАЯ ЗАПИСКА
к итоговой аттестационной работе на тему
«Разработка web-ресурса с использованием технологий HTML, CSS, JavaScript»
(на примере web-ресурса: http://tatum.p-host.in/diploma.html )

 
Петрова Марина Вадимовна группы №: 0540
программы профессиональной переподготовки
«Frontend разработка»
 
 
 
Москва, 2022
 
Оглавление
 
Постановка задачи и план работы……………………………………….3
ОСНОВНАЯ ЧАСТЬ………………………………………………………...4
Назначение веб-ресурса…………………………………………………..4
Описание этапов разработки, описание функционала с приложением листингов исходного программного кода основной функции, структурных модулей, пример кода-разметки……………..4
Список литературы………………………………………………11
 
 
ПОСТАНОВКА ЗАДАЧИ И ПЛАН РАБОТЫ.
 
Задачей является создание онлайн игры на внимание. При начале работы над проектом, необходимо определиться, как будет работать и выглядеть проект. После чего необходимо определиться какими инструментами создавать внешний вид сайта, и саму архитектуру игры.
План работ:
1. Создание основы HTML.
2. Написать конструктор игры, переменные и функции в JS.
3. Добавление CSS кода.
4. Адаптировать для мобильных устройств.
 

ОСНОВНАЯ ЧАСТЬ.
Назначение веб-ресурса.
 
Веб-ресурс предназначен для онлайн игры. Суть игры: различные геометрические фигуры (квадраты, круги и треугольники) хаотично летают по игровой зоне, необходимо кликать по квадратам, чтобы зарабатывать очки, в случае промаха расходуются жизни. В дальнейшем можно дописать уровни сложности, такие как изменяющаяся скорость движения объектов, “клики” по определенным цветам, “клики” по другим объектам. Также игру можно дополнить модальным окном, в котором будет выводиться результат и игровой уровень.
 
Описание этапов разработки, описание функционала с приложением листингов исходного программного кода основной функции, структурных модулей, пример кода-разметки
 
Этап разработки начинался с создания проекта и написания основ HTML.  Веб ресурс создавался с использованием grid системы, для этого в html были прописаны 2 зоны: 
для кнопки начала игры и очков,
для самого экрана игры 

В проект веб ресурса входят 1 страница в формате html, в которой прописан код CSS, HTML, и JavaScript. Страница веб проекта адаптивна и может открываться на разных устройствах  с разным разрешением экрана.
При переходе по адресу http://tatum.p-host.in/diploma.html пользователь попадает на страницу сайта, на которой есть кнопка начала игры, также в верхнюю консоль выводится количество набранных очков и оставшихся жизней. Далее создается массив из вида геометрических фигур, а также цветовых вариантов. В игре будет участвовать не более 20 фигур, и у игрока будет 3 жизни. После чего создаем переменную игры.
         
Далее необходимо написать функцию для создания рандомных объектов, в которой мы прописываем рандом движения по экрану (направление и скорость),рандом из игровых объектов,рандом из цвета,переменные с префиксом для использования по всему документу. Здесь же добавляем возможность удаления объекта по клику (для этого создаем новый массив со всеми элементами, прошедшими проверку, кроме нажатого ранее объекта). Затем проверяем игру на наличие квадратов, и если их нет, то обновляем поле и получаем опять 20 рандомных объектов различных цветов. Также здесь прописываем увеличение очков в случае “клика” по квадрату, если же пользователь ошибается и “кликает” по другому объекту, то у него уменьшаются “жизни”. В случае если “жизни” равны нулю, выводится сообщение, что пользователь проиграл и тогда игра останавливается.

И не менее важная часть игры - это анимация, в которой мы прописываем точку старта движения фигур (для каждой фигуры свою), а также скорость движения объекта. Также в случае, если наш объект выходит за рамки игрового поля (слева, справа, сверху или снизу), то мы разворачиваем его движение в другую сторону.
 
После того как основная идея игры прописана, необходимо добавить несколько функций, таких как:
- Функция начала игры, которая проверяет все условия и возвращает необходимые значения (очки=0, жизни=3, и свойство игры - в игре, сбрасывает объекты, и запускает саму игру).
- Функция проверки на наличие квадратов через DOM элемент.
- Функция обновления игрового поля (очистка игровой зоны, создание нового массива из элементов и проверка, что на поле есть квадратные фигуры).
- Функция остановки игры (выключаем анимацию, обновляем очки/жизни)
- Функция обновления счета и жизней
- Переключение кнопки включения-выключения игры
 

Исходные файлы проекта можно просмотреть на GitHub по ссылке https://github.com/username/Job_Title.
Тестирование работоспособности веб ресурса проводилось не в автоматическом режиме, т.е. без написания тестов.

 
СПИСОК ЛИТЕРАТУРЫ
 
1. Электронные ресурсы.
1.  Сайт
Официальная документация Mozilla [Электронный ресурс]: офиц. сайт. URL: https://developer.mozilla.org/ru/ (Дата обращения: 30.07.2022).
2. Сайт
Официальная документация ресурса “Современный учебник JavaScript” [Электронный ресурс]: офиц. сайт. URL: https://learn.javascript.ru/ (Дата обращения: 01.08.2022).
3.  Сайт
Электронный учебник по HTML и CSS [Электронный ресурс]: офиц. сайт. http://htmlbook.ru/html5 (Дата обращения: 29.07.2022).
4. Сайт
Онлайн урок от платформы skillbox [Электронный ресурс]: офиц. сайт.https://skillbox.ru/media/code/kak_napisat_igru_na_javascript/ (Дата обращения: 29.07.2022).

 
 
 

