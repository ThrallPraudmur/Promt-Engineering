## Что такое промпт (prompt)?
Промты начинаются с команды /imagine и могут включать текст, ссылки на изображение и параметры.
* **текст** описывает, какое изображение вы хотите сгенерировать
* **ссылки на иозбражения** могут быть добавлены в промт, чтобы задать стиль генерируемой картинки. Ссылки всегда идут в начале промта
* **параметры** задают версию Midjourney, стиль, размер изобажения. Параметры указываются в конце через два дефиса `--`

Также Midjourney умеет объединять два разных изображения в одно:
1. Загрузите исходное изображение (или два) на сервисы [Imgur](https://img.doerig.dev/) или [Postimages](https://postimages.org/ru/) и получите ссылки на них в формате .png, .jpg или .webp;
2. Вставьте ссылку в начало промта, а затем добавьте текстовое описание;
3. Чтобы объединить два изображения в одно, вставьте две ссылки на них подряд через запятую (торт + замок, цветочки + Александр)

```python
/imagine https://i.imgur.com/Z5UIh53.jpg торт на день рождения
```

## Использование параметров
Параметры всегда добавляются в конец промта, важно писать их правильно, через два дефиса `--` и с пробелом перед цифрами: </br>
`--v 6` для генерации изображения будет использоваться самая новая модель Midjourney V6. По умолчанию используется версия Midjourney 5.2 </br>
`--v 5` или **--v 4** для генерации изображения будет использоваться предыдущая версия Midjourney </br>
`--niji` изображение будет генерироваться в стиле аниме </br>
`--aspect` или `--ar` изменение соотношения сторон генерируемого изображения </br>
`--style raw` позволяет получить более натуриальные и реалистичные изображения, уменьшая влияние эстетической обработки Midjourney </br>
`--stylize` или `--s` также влияет на художественную обработку изображения. Низкие значения создают более естественные картинки, высокие - более обработанные. По умолчанию 100, параметры варьируются от 0 до 1000 </br>
