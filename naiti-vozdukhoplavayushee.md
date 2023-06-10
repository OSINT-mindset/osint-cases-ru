---
description: '@osint_mindset Статья - X, редактор - Akvagon | February 01, 2023'
---

# Найти воздухоплавающее

Приветствуем, наши любимые осинтеры! Сегодня вновь отложим GEOINT и попробуем решить задачку по старому доброму OSINT-у. Что же мы придумали на этот раз? [Котосинт](https://osint-mindset.gitbook.io/cases/kotosint-ili-slabo-naiti-kota-v-turcii) прошли, [контейнеры](https://osint-mindset.gitbook.io/cases/o-more-more...) тоже, сегодня же представляем для вас следующее:

**Задание**

> На одном личном блоге плавает такое существо. Найдите электронную почту автора блога.

<figure><img src="https://telegra.ph/file/7e84cfb8c6672f41ca072.jpg" alt=""><figcaption><p>Изображение к заданию</p></figcaption></figure>

В чате пошли догадки, что же за существо изображено на картинке. Также смущало слово "плавает", не намёк ли это случаем? В любом раскладе, самым популярным по началу запросом стала обыкновенная крыса. Один из участников даже сгенерировал недостающую голову с помощью [искусственного интеллекта](https://openai.com/dall-e-2/), другие же просто нашли фото крыс и мышей для сравнения.

<figure><img src="https://telegra.ph/file/c00ec5418bea24cd97121.jpg" alt=""><figcaption><p>Сгенерированное изображение и изображение найденное в интернете</p></figcaption></figure>

Внимательно изучив грызунов, на форуме возникли обоснованные мысли, что это не крыса и не мышь, так как количество пальцев, длина хвоста и шерсть указывают на то, что это животное, больше похожее на опоссума. Сравнив реального и мультяшного зверька, версия была принята.

\


<figure><img src="https://telegra.ph/file/1aa7f6cc30047306d01ec.jpg" alt=""><figcaption><p>Изображение опоссума</p></figcaption></figure>

> Интересный факт. Используя "выделение фрагмента", Яндекс сам подсказывает, что это за животное.

<figure><img src="https://telegra.ph/file/1c03ae7f83e6310fe8058.png" alt=""><figcaption><p>Система определяет животное всего по нескольким фрагментам изображения</p></figcaption></figure>

Но нам не давала покоя одна мысль, которую озвучили на форуме:

> Пожалуйста, обратите внимание на формулировку задания.

> \- На одном личном блоге плавает следующее существо

> Имеется в виду, что изображение передвигается по сайту как анимация.

> То есть просто сайты, где это существо статично, не подходят.

Получается нам нужно найти не просто картинку, а анимацию. Естественно, мы полезли подбирать новые запросы по поисковикам. И через некоторое время [BLACK](https://t.me/blacktiesz) дал верный ответ!

\


**Решение**

> Поиск изображения по [линзе](https://images.google.ru/) не даст результатов, так что воспользуемся нейросетью [DALLE-E 2](https://openai.com/dall-e-2/), чтобы дополнить изображение, а именно дорисовать голову животного.

> Идем в DALLE-E 2 (Для этого понадобится аккаунт OpenAI)

\


<figure><img src="https://telegra.ph/file/3955998235da5da10f0d9.jpg" alt=""><figcaption><p>Нейросеть DALLE-E 2</p></figcaption></figure>

> Нажимаем на кнопку **upload an image**.

> 2\. Выбираем наше изображение и нажимаем на **skip cropping**.

<figure><img src="https://telegra.ph/file/7fb1a001897b06806d1ef.jpg" alt=""><figcaption><p>Работа с изображением</p></figcaption></figure>

> 3\. Растягиваем изображение (Я растянул до 642x1200)

<figure><img src="https://telegra.ph/file/c251d994d37e0420a48bc.jpg" alt=""><figcaption><p>Редактирование изображения</p></figcaption></figure>

> 4\. Нажимаем на галочку и стираем область, где мы хотим дорисовать голову ластиком. В поле для промта пишем **rat**.

> Дальше выбираете понравившийся результат и скачиваете картинку.

<figure><img src="https://telegra.ph/file/da34dae729895bfb35cbd.png" alt=""><figcaption><p>Результат генерации при помощи нейросети</p></figcaption></figure>

> 4\. Загружаем результат в [Google Lense](https://images.google.ru/) и выделяем полностью изображение.

<figure><img src="https://telegra.ph/file/e2459f7f2edf8753e18a6.jpg" alt=""><figcaption><p>Результаты поиска с использованием Google Lense</p></figcaption></figure>

> В похожих изображениях видим наше животное! Переходим на сайт.

<figure><img src="https://telegra.ph/file/92f9df0d8e596f4324fb6.jpg" alt=""><figcaption><p>Похожее изображение</p></figcaption></figure>

> На этом блоге нет анимаций с этим животным, соответственно сайт не подходит.

> Этот опоссум является логотипом компании [11ty](https://www.11ty.dev/blog/logo-homage/). Под изображением есть ссылка на оригинальный сайт, а значит переходим.

> На главной странице хоть и "плавает" это существо, но его изменили и это не является личным блогом.

<figure><img src="https://telegra.ph/file/5cd4509d9c428afd5bb98.gif" alt=""><figcaption><p>Вид сайта 11ty</p></figcaption></figure>

> 5\. Поэтому переходим в историю этого логотипа [https://www.11ty.dev/blog/logo-homage/](https://www.11ty.dev/blog/logo-homage/) и скачиваем нужный.

<figure><img src="https://telegra.ph/file/4e20b7e8de92e226b7e1c.png" alt=""><figcaption><p>Находим нужный логотип и сохраняем</p></figcaption></figure>

> 6\. Это лого мы загружаем в Google Lense и нажимаем **Find image source**.

<figure><img src="https://telegra.ph/file/575121813d489c0bb3472.jpg" alt=""><figcaption><p>Поиск с использованием Google Lense</p></figcaption></figure>

> 7\. В адресной строке пишем **blog**.

<figure><img src="https://telegra.ph/file/d074a1feb6ed4604d8a3e.png" alt=""><figcaption><p>Используем дополнительное описание в строке поиска Google</p></figcaption></figure>

> На первой странице выдачи ничего полезного не нашел, поэтому переходим на вторую страницу и видим сайт, подходящий под наше описание. Главное, чтобы там был опоссум на шарике **с анимацией**.

<figure><img src="https://telegra.ph/file/de34b883a481983b123c4.jpg" alt=""><figcaption><p>Находим нужную страницу</p></figcaption></figure>

> 8\. Переходим на сайт и находим то, что искали.

<figure><img src="https://telegra.ph/file/95072663c2d281385363b.gif" alt=""><figcaption></figcaption></figure>

> Этот сайт полностью подходит под наше описание! Осталось найти почту автора этого блога.

> 9\. Нажимаем на кнопку **home**.

<figure><img src="https://telegra.ph/file/a756c2f2a24414bd50b29.png" alt=""><figcaption><p>Искомый блог</p></figcaption></figure>

> 10\. Наводим на кнопку **email me** и в левом нижнем углу видим почту.

<figure><img src="https://telegra.ph/file/ede57ecb54952c902b908.jpg" alt=""><figcaption><p>Ответ</p></figcaption></figure>

**Ответ: jg@justus.ws.**

Вот так совместная работа искусственного интеллекта и человека приносит грандиозные плоды. А что вы думаете про внедрение ИИ в нашу жизнь? Пишите в комментариях на [нашем канале](https://t.me/osint\_mindset)! Пока же, до новых встреч в интересных решениях, друзья.

> [@osint\_mindset](https://t.me/osint\_mindset) Канал, где вы можете узнать основные события в сообществе[\
> @forum\_rassledovaniy](https://t.me/+GMxoDCvLO0k0MWRi) Форум, где вы можете поучиться решать таски
