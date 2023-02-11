# Решение OSINT #25

_Izumzudnoe Chudovische, January 31, 2023_

Есть сайт govn.uk. Необходимо найти радиолюбительский позывной создателя и его последнюю передачу местоположения по радио.

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

Не кидайтесь камнями, я просто неграмотный)

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

\


Решение:

Имея доменное имя мы конечно же попробуем найти информацию о нем:

Идем на [https://who.is/](https://who.is/) и в поисковой строке вбиваем интересующий нас ресурс и жмем на линзу

<figure><img src="https://telegra.ph/file/ba3b5b0c00b6a3153785d.png" alt=""><figcaption></figcaption></figure>

В ответ получаем выборку регистрационных данных

<figure><img src="https://telegra.ph/file/87fd46099729a4e179b87.png" alt=""><figcaption></figcaption></figure>

Тут я зацепился за нестандартный name-сервер cyanidehouse.ru.

Попробовав поискать в гугле мы получаем такую поисковую выдачу:

<figure><img src="https://telegra.ph/file/39e4e598514c1de88ddeb.png" alt=""><figcaption></figcaption></figure>

DSTAR.SU который является сайтом/форуме по радиолюбительскому стандарту D-STAR, что подводит нас ближе к искомому результату:

<figure><img src="https://telegra.ph/file/7e14a32a2ba19a0805a60.png" alt=""><figcaption></figcaption></figure>

\


Далее я решил зайти на dnslytics.com, который оказался третьим в поисковой выдаче и обнаружил, что на этом ip-адресе хостятся еще несколько web-ресурсов:

<figure><img src="https://telegra.ph/file/a76de229f14db561a0d93.png" alt=""><figcaption></figcaption></figure>

Сразу цепляюсь за prilutsskiy.ru и за сайт представленный в punycode (xn--h1aadcewh0a1a.xn--p1ai)

Пытаемся на него постучаться:

<figure><img src="https://telegra.ph/file/4b1776c340b383a300b54.png" alt=""><figcaption></figcaption></figure>

Не получилось, но у нас есть предполагаемая фамилия радиолюбителя. Пробуем найти в гугле "Прилуцкий радиолюбитель"

<figure><img src="https://telegra.ph/file/9a437c599d22147b850e9.png" alt=""><figcaption></figcaption></figure>

Вот мы и нашли старый и новый позывной: старый UB3ABM и новый R3ABM.

Далее нам требуется найти последние координаты по которым R3ABM выходил на связь.

Снова идем в гугл и ищем исключительно информацию по позывному

<figure><img src="https://telegra.ph/file/ac2699b1b7b4b8ad7246e.png" alt=""><figcaption></figcaption></figure>

На qrz.ru нас встречает неприветливое сообщение о том, что для просмотра детальной информации нужна регистрация

<figure><img src="https://telegra.ph/file/2c843ebfc0d527df8bf60.png" alt=""><figcaption></figcaption></figure>

Возвращаемся к поисковой выдаче и смотрим что нам выдаст [https://www.qrzcq.com/](https://www.qrzcq.com/)

<figure><img src="https://telegra.ph/file/86e6117650312ed58fd3b.png" alt=""><figcaption></figcaption></figure>

У нас есть координаты, но непонятно как давно они были получены.

Я решил перейти на APRS Info и посмотреть что это такое

<figure><img src="https://telegra.ph/file/1e325be047c283309205a.png" alt=""><figcaption></figcaption></figure>

В новой вкладке открывается ресур aprs.fi с поиском по позывному R3ABM\*

<figure><img src="https://telegra.ph/file/bc057cb79b0c5e2f3848a.png" alt=""><figcaption></figcaption></figure>

У нас 2 кандидата R3ABM-7 и R3ABM-9. Поискав немного информации об обозначениях что значит -7 и -9 стало понятно, что это все один и тот же человек, просто APRS SSID может отличаться в зависимости от настройки устройства передающего информацию, либо его типа.

<figure><img src="https://telegra.ph/file/234f270b0614f6b350c7a.png" alt=""><figcaption></figcaption></figure>

Переходим на метку которая имеет меньший возраст, а точнее 36 дней

<figure><img src="https://telegra.ph/file/c4f4e0cf71fe9c3de9d96.png" alt=""><figcaption></figcaption></figure>

Получаем координаты 52°31'02.4"N 13°20'15.6"E / 52.517333, 13.337667

\


<figure><img src="https://telegra.ph/file/d8c17a0c7d9d6eddd47b8.png" alt=""><figcaption></figcaption></figure>

Верны ли полученные координаты?

Возвращаемся к поисковой выдаче по позывному

<figure><img src="https://telegra.ph/file/b8e78f88fd9bcceec28e1.png" alt=""><figcaption></figcaption></figure>

Третья ссылка ведет нас на некий BrandMeister wiki.

[https://wiki.brandmeister.network/index.php/R3ABM](https://wiki.brandmeister.network/index.php/R3ABM)

\


<figure><img src="https://telegra.ph/file/cfd2834af86d478a7898f.png" alt=""><figcaption></figcaption></figure>

Очень информативно, но ничего непонятно. Переходим по гиперссылке [BrandMeister Dev Team](https://brandmeister.network/?page=team) где видим что R3ABM так же является ведущим разработчиком в BrandMeister, проживает в Берлине, Германия и еще один его позывной DL5ABM.

<figure><img src="https://telegra.ph/file/77e8012666eefc117b75d.png" alt=""><figcaption></figcaption></figure>

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

Ответ: 1) R3ABM 2) 52.517333, 13.337667
