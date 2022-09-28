# Растровые карты Подмосковья Славы Завьялова

## Неофициальная сборка карт для загрузки в навигационные программы

Карты соответствуют исходникам лета 2022 года.

Карты в формате sqlitedb предназначены для программы OSMAnd.
Для большинства других программ нужно использовать стандартный формат mbtiles.

Файлы с суффиксом light отрисованы в обычном режиме, с суффиксом dark -- инвертированной освещённости для тёмного времени суток.

Файлы с суффиксом hq (повышенной чёткости) содержат в себе плитки с диапазоном параметра Z от 1 до 15, без суффикса -- с диапазоном от 1 до 14.

[Карты mbtiles повышенной чёткости](https://github.com/kazantsev-a-s/slazav-tiles/releases/download/2022.08/slazav-light-hq.mbtiles)

[Карты sqlitedb повышенной чёткости](https://github.com/kazantsev-a-s/slazav-tiles/releases/download/2022.08/slazav-light-hq.sqlitedb)

[Ночные карты mbtiles повышенной чёткости](https://github.com/kazantsev-a-s/slazav-tiles/releases/download/2022.08/slazav-dark-hq.mbtiles)

[Ночные карты sqlitedb повышенной чёткости](https://github.com/kazantsev-a-s/slazav-tiles/releases/download/2022.08/slazav-dark-hq.sqlitedb)

[Карты mbtiles](https://github.com/kazantsev-a-s/slazav-tiles/releases/download/2022.08/slazav-light.mbtiles)

[Карты sqlitedb](https://github.com/kazantsev-a-s/slazav-tiles/releases/download/2022.08/slazav-light.sqlitedb)

[Ночные карты mbtiles](https://github.com/kazantsev-a-s/slazav-tiles/releases/download/2022.08/slazav-dark.mbtiles)

[Ночные карты sqlitedb](https://github.com/kazantsev-a-s/slazav-tiles/releases/download/2022.08/slazav-dark.sqlitedb)

## Исходники карт для самостоятельной сборки

Программа [Mapsoft2](https://github.com/slazav/mapsoft2) для сборки карт.

Репозиторий [карт Подмосковья.](https://github.com/slazav/map_podm)

Для создания файлов формата SQLiteDB и MBTiles запустите скрипт make_tiles_db.

## Загрузка в программу OSMAnd

Заливка карт в программу OSMAnd+, которую для Android можно скачать в магазине свободных приложений [FDroid](https://f-droid.org/) :

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
