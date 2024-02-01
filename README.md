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
`--v 5` или `--v 4` для генерации изображения будет использоваться предыдущая версия Midjourney </br>
`--niji` изображение будет генерироваться в стиле аниме </br>
`--aspect` или `--ar` изменение соотношения сторон генерируемого изображения </br>
`--style raw` позволяет получить более натуриальные и реалистичные изображения, уменьшая влияние эстетической обработки Midjourney </br>
`--stylize` или `--s` также влияет на художественную обработку изображения. Низкие значения создают более естественные картинки, высокие - более обработанные. По умолчанию 100, параметр варьируется от 0 до 1000 </br>
`--chaos` более высокие значения создают более разнообразные и не похожие друг на друга начальные варианты изображения, варьируется от 0 до 100 </br>
`--weird` используется для добавления необычных и эксцентричных качеств к изображениям, что приводит к уникальным и неожиданным результатам. Параметры варьируются от 0 до 3000, где 0 - отсутствие странности </br>
`--no` указывает на то, чего в изображение быть не должно: `--no цветы` </br>
`sameseed` </br>
`uplight` </br>
`hd`

**Сосредоточьтесь на основной концепции. </br>
Сокращайте, когда это возможно. </br>
Меньше слов означает, что каждое из них будет иметь больший вес. </br>
Думайте о том, что важно.**

## Команды-подсказки для подготовки промпта
`/describe` + загрузка изображения: Midjourney пришлёт несколько вариантов промпта для этого изображения </br>
`/shorten` + текстовый промпт: Midjourney проанализирует промпт и даст рекомендации по его улучшению: какие слова лишние и не участвуют в генерации изображения, а какие ключевые 

Эти команды не расходуют генерации и позволяют взглянуть на промпты глазами Midjourney, чтобы лучше понять принципы их составления.

После отправки команды `/imagine` с вашим промптом начинается генерация 4 начальных изображений, она обычно занимает 1-3 минуты. </br>
Вместе с картинками появляется два ряда кнопок:
* `U` увеличивает выбранное изображение и добавляет детализацию
* `V` создаёт 4 новые вариации выбранного изображения
* Повтор генерирует изображения заново с тем же промптом
* Конвертик позволяет получить `--seed` изображения, зная который можно незначительно менять результаты генерации

После увеличения `U` изображения появляются новые кнопки:
* `Vary` создаёт 4 новые вариации с большими Strong или меньшими Subtle изменениями
* `Zoom out` отдаляет изображение и дорисовывает новые детали (1.5х или 2х)
* `Pan` дорисовывает изображение в выбранную сторону

## Как разместить текст на изображении?
Midjourney V6 умеет генерировать небольшой объём текста на изображениях:
* Добавьте параметр `--v 6` в конце промпта;
* Пишите текст на английском языке и в "кавычках"

```python
/imagine a photo of text "Hello World" written with a marker on a sticky note --v 6
```


