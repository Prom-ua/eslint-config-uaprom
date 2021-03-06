# eslint-config-uaprom
Репозиторий c инструкцией подключения к другим проектам и 
готовым конфигом на базе [airbnb](https://github.com/airbnb/javascript)

## Установка

### Шаг 1. (ставим eslint config и peer deps):

```bash
npm info "eslint-config-airbnb@14.1" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev "@evo/eslint-config-uaprom@latest"
```

### Шаг 2. (Добавляем в eslintrc)
```bash
echo '{"extends": "@evo/eslint-config-uaprom"}' > .eslintrc
```

## Настройка для webpack для нового проекта
1. npm install --save-dev eslint-loader
2. Добавляем eslint-loader как показано на инструкции [https://github.com/MoOx/eslint-loader](https://github.com/MoOx/eslint-loader)

## Разработка
Если вы хотите внести изменение в существующий конфиг это можно сделать так:

1. Создать PR c изменениями (дождаться review).
2. После подтверждения изменений сделать merge в мастер.
3. Опубликовать пакет на npm (для этого вы должны быть добавлены в организацию evo на npm - [https://www.npmjs.com/org/evo](https://www.npmjs.com/org/evo))

