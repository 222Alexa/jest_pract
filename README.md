# AJS-4.1.jest
# Домашнее задание к лекции «Unit-тестирование»

**Важно**: каждая задача выполняется в виде отдельного проекта с собственным GitHub репозиторием.

**Важно**: ESLint не должен выдавать ошибок.

**Важно**: Jest должен обеспечивать 100% покрытие по строкам для тестируемых вами функций.

**Важно**: Ко всем задачам должен быть подключен Appveyor и выставлен бейджик статуса.

**Важно**: используйте `import`/`export` а не `require`.

В качестве шаблона вы можете использовать [готовый проект](/ci-template).

В личном кабинете на сайте [netology.ru](http://netology.ru/) в поле комментария к домашней работе вставьте ссылки на ваш GitHub-проекты.

## Описание установки

```shell
npm init
# При инициалиализации в качестве тестовой команды указать:
# test command: jest --coverage
npm install --save-dev jest babel-jest @babel/core @babel/cli @babel/preset-env
npm install core-js@3
```

Не забудьте про `.babelrc` и `.browserslistrc`.

В `.babelrc`:
```json
{
  "presets": [["@babel/preset-env", {
    "useBuiltIns": "usage",
    "corejs": 3
  }]]
}
```

Запуск тестов:
```shell
npm test
```

---

## Чистые функции

### Легенда

Во время игры вам необходимо будет отображать полоску жизни над игровым персонажем. Для сигнализации пользователю вы решили ввести цветовую индикацию:
1. Здоровье более 50 - зелёный;
1. Здоровье от 50 и до 15 - жёлтый;
1. Менее 15 - красный.

### Описание

Реализуйте функцию, которая на вход принимает объект вида:
```javascript
{name: 'Маг', health: 90}
```
И возвращает ответ в виде одной из строк: `healthy`, `wounded`, `critical`

Сгенерируйте проект на базе `npm`. Подключите туда `jest` и напишите авто-тесты, которые обеспечивают 100% покрытие вашей функции по строкам.

Убедитесь, что вы обеспечили 100% покрытие тестами.
[![Build status](https://ci.appveyor.com/api/projects/status/98flq37oaiw3qes0/branch/master?svg=true)](https://ci.appveyor.com/project/222Alexa44925/jest-pract/branch/master)
