# Оформление ВКР бакалавра

Направление подготовки:
- 09.03.03 Прикладная информатика

Профиль:
- Прикладная информатика в технике и технологиях

## Источники

Параметры оформления, а также общее представление о формировании документации в LaTeX подчерпнуто в работе [Амета Умерова](https://github.com/Amet13/) - [bachelor-diploma](https://github.com/Amet13/bachelor-diploma/).

Прочие источники и ссылки на них указаны в составе работы (`section/sources.tex`).

### Формирование pdf-документа:

```shell
xelatex main.tex
```

### Возможные ошибки и шаги к их решению (на примере ОС Ubuntu 22.04)

1. Установка xelatex:

    ```shell
    sudo apt install texlive-xetex
    ```

2. Добавление xelatex в PATH

    https://gist.github.com/nex3/c395b2f8fd4b02068be37c961301caa7

3. Установка шрифтов 

    https://askubuntu.com/questions/463754/how-to-make-ttf-mscorefonts-installer-package-download-fonts-after-it-says-it-i

    ```shell
    sudo apt-get install ttf-mscorefonts-installer
    ```

4. Ошибки *spawn latexmk enoent*

    https://stackoverflow.com/questions/68179318/recipe-terminated-with-fatal-error-spawn-latexmk-enoent

    ```shell
    sudo apt install latexmk
    ```

5. Ошибки *Fatal Package fontspec Error: The fontspec package requires either XeTeX or ...*

    Изменяется в настройках среды.

    Например, в VSCode у расширения `LaTeX Workshop` можно найти рабочий вариант способа сборки (recipe).
    Чтобы использовать его по умолчанию можно задать параметр в настройках расширения `LaTeX Workshop`:
    ```json
    "latex-workshop.latex.recipe.default": "lastUsed"
    ```
    и запустить нужный вариант сборки.

    Далее автоматически будет применяться выбранный способ формирования документа.

