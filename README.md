# Растровые карты Подмосковья для ММБ ("карты Славы Завьялова")

## Неофициальная сборка карт для загрузки в навигационные программы телефонов и планшетов

Карты соответствуют исходникам лета 2024 года.
По сравнению со сборкой 2023 года обозначения стали мельче в полтора раза для лучшего соответствия печатным картам.

Формат sqlitedb предназначен для программы OSMAnd.
Для большинства других программ нужно использовать стандартный формат mbtiles.

Файлы с суффиксом light отрисованы в обычном режиме, с суффиксом dark -- инвертированной освещённости для тёмного времени суток.

Файлы с суффиксом hq (повышенной чёткости) содержат в себе плитки с диапазоном параметра Z от 1 до 15, без суффикса -- с диапазоном от 1 до 14.

[Карты mbtiles повышенной чёткости](https://github.com/kazantsev-a-s/slazav-tiles/releases/download/2024.06/slazav-light-hq.mbtiles)

[Карты sqlitedb повышенной чёткости](https://github.com/kazantsev-a-s/slazav-tiles/releases/download/2024.06/slazav-light-hq.sqlitedb)

[Карты mbtiles](https://github.com/kazantsev-a-s/slazav-tiles/releases/download/2024.06/slazav-light.mbtiles)

[Карты sqlitedb](https://github.com/kazantsev-a-s/slazav-tiles/releases/download/2024.06/slazav-light.sqlitedb)

[Ночные карты mbtiles повышенной чёткости](https://github.com/kazantsev-a-s/slazav-tiles/releases/download/2024.06/slazav-dark-hq.mbtiles)

[Ночные карты sqlitedb повышенной чёткости](https://github.com/kazantsev-a-s/slazav-tiles/releases/download/2024.06/slazav-dark-hq.sqlitedb)

[Ночные карты mbtiles](https://github.com/kazantsev-a-s/slazav-tiles/releases/download/2024.06/slazav-dark.mbtiles)

[Ночные карты sqlitedb](https://github.com/kazantsev-a-s/slazav-tiles/releases/download/2024.06/slazav-dark.sqlitedb)

Предыдущие неофициальные сборки [тут.](https://github.com/kazantsev-a-s/slazav-tiles/releases)

Официальные сборки плиток можно найти [здесь.](https://slazav.xyz/maps/podm.htm)

## Исходники карт для самостоятельной сборки в UNIX и инструкции

Скачайте программу [mapsoft2.](https://github.com/slazav/mapsoft2)

Скачайте репозиторий [карт Подмосковья.](https://github.com/slazav/map_podm)

Соберите исходники mapsoft2, скопируйте программы ms2render и ms2nom в одну из папок, куда указывает переменная среды PATH. Скопируйте из mapsoft2 файлы render.cfg и types.cfg, а также папку pics в папку репозитория map_podm.

Для создания файлов формата SQLiteDB и MBTiles используйте скрипт [make_tiles_db](https://github.com/kazantsev-a-s/slazav-tiles/raw/master/make_tiles_db), который надо скачать и поместить в папку репозитория map_podm.
В самом пакете mapsoft2 есть свои скрипты для сборки плиток, а make_tiles_db это альтернативная реализация с рядом доработок.

Запустите скрипт make_tiles_db из папки map_podm.

## Загрузка в программу OSMAnd

Заливка карт в программу OSMAnd+, которую для Android можно скачать в магазине свободных приложений [FDroid:](https://f-droid.org/)

Самый просто вариант, это положить файл sqlitedb на телефон в произвольное место и открыть его в любом файловом менеджере, после чего выбрать приложение OSMAnd.

Более продвинутый:

1) Включить пункт "Онлайн-карты", до которого можно добраться так: кнопка глобус -> Источник карты.. -> "Онлайн-карты" -> Включить.

2) Положить выбранные файлы типа SQLiteDB во внутреннюю папку с плитками приложения OSMAnd. Скорее всего это будет /sdcard/Android/data/net.osmand.plus/files/tiles.

3) Выбрать нужную карту в меню глобус -> "Карта наложения" или "глобус -> Карта подложки". Если выбраны обе, то можно быстро переключаться между ними после небольшой настройки в этих же пунктах меню с помощью ползунка на основном экране.

<!-- Yandex.Metrika counter -->
<script type="text/javascript" >
    (function (d, w, c) {
        (w[c] = w[c] || []).push(function() {
            try {
                w.yaCounter50082013 = new Ya.Metrika2({
                    id:50082013,
                    clickmap:true,
                    trackLinks:true,
                    accurateTrackBounce:true
                });
            } catch(e) { }
        });

        var n = d.getElementsByTagName("script")[0],
            s = d.createElement("script"),
            f = function () { n.parentNode.insertBefore(s, n); };
        s.type = "text/javascript";
        s.async = true;
        s.src = "https://mc.yandex.ru/metrika/tag.js";

        if (w.opera == "[object Opera]") {
            d.addEventListener("DOMContentLoaded", f, false);
        } else { f(); }
    })(document, window, "yandex_metrika_callbacks2");
</script>
<noscript><div><img src="https://mc.yandex.ru/watch/50082013" style="position:absolute; left:-9999px;" alt="" /></div></noscript>
<!-- /Yandex.Metrika counter -->
