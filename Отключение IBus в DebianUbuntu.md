---
title: "Отключение IBus в Debian/Ubuntu"
source: "https://blog.tataranovich.com/2021/01/disable-ibus.html"
author:
published:
created: 2025-04-23
description: "Супруге приходится пользоваться Zoom и с ним в систему притянуло IBus  (Intelligent Input Bus). Это фреймворк для методов ввода и наверное т..."
tags:
  - "clippings"
---
## воскресенье, 10 января 2021 г.

### Отключение IBus в Debian/Ubuntu

Супруге приходится пользоваться Zoom и с ним в систему притянуло [IBus](https://ru.wikipedia.org/wiki/IBus) (Intelligent Input Bus). Это фреймворк для методов ввода и наверное тем кто использует иероглифы он полезен, но для меня он не решает никаких проблем, а лишь добавляет глюки с переключением языка ввода (используется переключение по Caps Lock).

Чтобы отключить IBus нужно добавить "отклонение" через dpkg-divert

```
sudo dpkg-divert --package im-config --rename /usr/bin/ibus-daemon
```

Включить обратно можно командой

```
sudo dpkg-divert --package im-config --rename --remove /usr/bin/ibus-daemon
```

После перезагрузки системы IBus больше не запускается.

Автор:[Andrey Tataranovich](https://www.blogger.com/profile/08081249568199801233 "author profile") на [13:56](https://blog.tataranovich.com/2021/01/disable-ibus.html "permanent link")

Ярлыки:[admin](https://blog.tataranovich.com/search/label/admin),[debian](https://blog.tataranovich.com/search/label/debian),[ubuntu](https://blog.tataranovich.com/search/label/ubuntu)

[Отправить по электронной почте](https://www.blogger.com/share-post.g?blogID=1327304432540056545&postID=8230429296840841312&target=email "Отправить по электронной почте") [Написать об этом в блоге](https://www.blogger.com/share-post.g?blogID=1327304432540056545&postID=8230429296840841312&target=blog "Написать об этом в блоге") [Поделиться в X](https://www.blogger.com/share-post.g?blogID=1327304432540056545&postID=8230429296840841312&target=twitter "Поделиться в X") [Опубликовать в Facebook](https://www.blogger.com/share-post.g?blogID=1327304432540056545&postID=8230429296840841312&target=facebook "Опубликовать в Facebook") [Поделиться в Pinterest](https://www.blogger.com/share-post.g?blogID=1327304432540056545&postID=8230429296840841312&target=pinterest "Поделиться в Pinterest")

[Следующее](https://blog.tataranovich.com/2021/02/kodi-nfs-51013.html "Следующее") [Предыдущее](https://blog.tataranovich.com/2021/01/diy-shunt.html "Предыдущее") [Главная страница](https://blog.tataranovich.com/)

Подписаться на:[Комментарии к сообщению (Atom)](https://blog.tataranovich.com/feeds/8230429296840841312/comments/default)

[[Проблема IBUS_UBUNTU]]