# Завдання

Напишіть програму, яка приймає два аргументи командної строки, які
містять хост і порт. Використайте `http.request` та відправте POST-запит на

```js
url + '/users/create'
```
з тілом, яке містить `JSON.stringify` об'єкт:

```js
{"user_id": 1}
```

Зробіть це п'ять разів, щоразу збільшуючи властивість `user_id`, починаючи з 1.

Коли запити будуть завершені, відправте GET-запит на:

```js
url + '/users'
```

використайте `console.log` на тіло відповіді від GET-запиту.

## Поради

В цьому завданні, вам буде необхідно координувати декілька асинхронних операцій.

Використайте `async.series` для цього і передайте в `Object`. В одній з функцій
потрібно використати `async.times`, щоб відправити POST-request використовуючи `http.request`.
Інша буде робити GET-запит.

Ви можете прочитать більше про `async.times` тут:

  https://github.com/caolan/async#times
