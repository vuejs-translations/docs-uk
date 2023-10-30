---
footer: false
---

# Вступ {#introduction}

:::info Ви переглядаєте документацію для Vue 3!

- Підтримка Vue 2 припиниться 31 грудня 2023 р. Докладніше про [Vue 2 Extended LTS](https://v2.vuejs.org/lts/).
- Документацію по Vue 2 було переміщено за адресою [v2.vuejs.org.ua](https://v2.vuejs.org.ua/).
- Оновлюєтесь з Vue 2? Перегляньте [Гід по міграції](https://v3-migration.vuejs.org/uk/).
  :::

<style src="@theme/styles/vue-mastery.css"></style>
<div class="vue-mastery-link">
  <a href="https://www.vuemastery.com/courses/" target="_blank">
    <div class="banner-wrapper">
      <img class="banner" alt="Vue Mastery banner" width="96px" height="56px" src="https://storage.googleapis.com/vue-mastery.appspot.com/flamelink/media/vuemastery-graphical-link-96x56.png" />
    </div>
    <p class="description">Вивчайте Vue з відео курсами на <span>VueMastery.com</span></p>
    <div class="logo-wrapper">
        <img alt="Vue Mastery Logo" width="25px" src="https://storage.googleapis.com/vue-mastery.appspot.com/flamelink/media/vue-mastery-logo.png" />
    </div>
  </a>
</div>

## Що таке Vue? {#what-is-vue}

Vue (вимовляється як (англ.) /vjuː/, (укр) /в'ю/) — це фреймворк, який працює на JavaScript, створений для розробки користувацьких інтерфейсів. Він працює на базі звичайного HTML, CSS та JavaScript, з можливостями декларативно програмувати користувацькі інтерфейси будь-якої складності на основі компонентів.

Найпростіший приклад:

<div class="options-api">

```js
import { createApp } from 'vue'

createApp({
  data() {
    return {
      count: 0
    }
  }
}).mount('#app')
```

</div>
<div class="composition-api">

```js
import { createApp, ref } from 'vue'

createApp({
  setup() {
    return {
      count: ref(0)
    }
  }
}).mount('#app')
```

</div>

```vue-html
<div id="app">
  <button @click="count++">
    Рахунок: {{ count }}
  </button>
</div>
```

**Результат**

<script setup>
import { ref } from 'vue'
const count = ref(0)
</script>

<div class="demo">
  <button @click="count++">
    Рахунок: {{ count }}
  </button>
</div>

Наведений вище приклад демонструє дві основні функції Vue:

- **Декларативний рендеринг**: Vue розширює стандартний HTML шаблонним синтаксисом, який дозволяє нам декларативно задавати структуру HTML на основі стану описаного у JavaScript.

- **Реактивність**: Vue автоматично відстежує зміни стану описаного у JavaScript і з максимальною ефективністю оновлює DOM, коли відбуваються зміни.

Можливо, у вас вже є запитання – не хвилюйтеся. Ми розглянемо кожну деталь в наступних розділах документації. Наразі, будь ласка, прочитайте розділ повністю, щоб ви могли мати високорівневе розуміння того, що пропонує Vue.

:::tip Передумови
Решта документації передбачає базове знання HTML, CSS і JavaScript. Якщо ви зовсім новачок у розробці користувацьких інтерфейсів, можливо, це не найкраща ідея одразу переходити безпосередньо до вивчення фреймворку, можливо, краще спочатку осягнути основи, а потім повернутися! Ви можете перевірити свій рівень знань JavaScript використовуючи [посібник MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/A_re-introduction_to_JavaScript). Попередній досвід роботи з іншими фреймворками допомагає у вивчені Vue, але не обов’язковий.
:::

## Прогресивний фреймворк {#the-progressive-framework}

Vue — це фреймворк та екосистема, яка охоплює більшість функцій, необхідних для розробки інтерфейсу. Але веб додатки надзвичайно різноманітні – речі, які ми створюємо в рамках веб додатків, можуть кардинально відрізнятися за формою та масштабом. Зважаючи на це, Vue розроблено таким чином, щоб бути гнучким і адаптивним. Залежно від вашого випадку та задач, Vue можна використовувати різними способами:

- Розширення статичного HTML
- Вбудовування як веб компонента на будь-яку сторінку
- Створення одно-сторінкового додатку (SPA)
- Фулстек / Додаток з рендерингом на стороні серверу (SSR)
- Jamstack / Генерація статичного додатку (SSG)
- Створення десктопних, мобільних, WebGL додатків і навіть додатків для термінала

Якщо ви вважаєте ці концепції важкими для розуміння, не хвилюйтеся! Гід і посібник вимагають лише базових знань HTML і JavaScript, і ви повинні бути в змозі зрозуміти їх, не бувши експертом з HTML чи JavaScript.

Якщо ви досвідчений розробник, зацікавлений у тому, як найкраще інтегрувати Vue у свій стек, або вам цікаво, що означають ці терміни, ми докладніше обговоримо їх у [Способах використання Vue](/guide/extras/ways-of-using-vue).

Не дивлячись на гнучкість фреймворку, основні знання про те, як працює Vue, можуть бути застосовані спільно для всіх цих варіантів використання Vue. Навіть якщо ви зараз лише новачок, знання, отримані на цьому шляху, залишаться корисними, коли ви зростатимете, щоб вирішувати амбітніші цілі в майбутньому. Якщо ви досвідчений розробник, ви можете обрати оптимальний спосіб використання Vue на основі проблем, які ви намагаєтеся вирішити, зберігаючи ту саму продуктивність. Ось чому ми називаємо Vue «Прогресивним фреймворком»: це фреймворк, який може рости разом з вами та адаптуватися до ваших потреб.

## Однофайлові компоненти {#single-file-components}

У більшості проєктів Vue, що використовують інструменти збірки та потребують етапу збірки, ми створюємо компоненти Vue, використовуючи HTML-подібний формат файлу під назвою **Single-File Component** (також відомий як файли `*.vue`, скорочено **SFC**). Vue SFC, як випливає з назви, інкапсулює логіку компонента (JavaScript), шаблон (HTML) і стилі (CSS) в одному файлі. Ось попередній приклад, написаний у форматі SFC:

<div class="options-api">

```vue
<script>
export default {
  data() {
    return {
      count: 0
    }
  }
}
</script>

<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<style scoped>
button {
  font-weight: bold;
}
</style>
```

</div>
<div class="composition-api">

```vue
<script setup>
import { ref } from 'vue'
const count = ref(0)
</script>

<template>
  <button @click="count++">Лічильник: {{ count }}</button>
</template>

<style scoped>
button {
  font-weight: bold;
}
</style>
```

</div>

SFC є однією з основних функцій Vue і рекомендованим способом створення компонентів Vue, **якщо** ваша задача вимагає використання інструментів збірки. Ви можете дізнатися більше [як і навіщо використовувати SFC](/guide/scaling-up/sfc) у спеціальному розділі, але наразі знайте, що Vue впорається з усіма налаштуваннями інструментів збірки за вас автоматично.

## Стилі API {#api-styles}

Компоненти Vue можна створювати в двох різних стилях API: **Опційному АРІ** і **Композиційному API**.

### Опційний API {#options-api}

За допомогою Опційного API ми визначаємо логіку компонента за допомогою об'єкта параметрів таких як `data`, `methods` і `mounted`. Властивості, визначені параметрами, виділяються у внутрішні функції `this`, що своєю чергою вказує на екземпляр компонента:

```vue
<script>
export default {
  // Властивості, повернуті з data(), переходять у реактивний стан
  // та виділяються у `this`.
  data() {
    return {
      count: 0
    }
  },

  // Методи — це функції, які змінюють стан і ініціюють оновлення.
  // Їх можна прив'язати як обробники подій у шаблонах.
  methods: {
    increment() {
      this.count++
    }
  },

  // Хуки життєвого циклу викликаються на різних етапах
  // життєвого циклу компонента.
  // Ця функція буде викликана під час монтування компонента.
  mounted() {
    console.log(`Початковий рахунок: ${this.count}.`)
  }
}
</script>

<template>
  <button @click="increment">Рахунок: {{ count }}</button>
</template>
```

[Спробуйте у Пісочниці](https://play.vuejs.org/#eNp9VE1v00AQ/SsjCwmqRglSb1Go+FAPcAAEHH1IcLapW8e27HWJFEUKKW05ICKhKlyQ4ALntPQjJHX6F3b/Ar+EN+vaaSVaKXJ2583OvPdm7a71KAzL24mwqlYtdiI3lKu2LzphEElqivVG4knq2j5RpULqi5qpsX6vB2qijtScV3pUInWh5tif6L5K9Q7HSJ1RsyEb95YMysiJ3kXWsR4C/0R6hzimxmp6WS3F8w+Z4mOVXnbkDQGc4OBIzXD4Mx9H1pBL1OWGG9fLnJx1y6gSRUImkZ/viJwg8WWV7mf7Hv/1Sraf6/oGdgNmpyb0t39Aek+dkP6gd8Bqqvf0SH8tkR5izcrUObikYGK4FJQJoAFG5kQOo2xq7JlBbgp4aPhy2329S+oc4CkA6LyAJbDiLjqdwWf4YppyiUNAeBqXpogby9kTWAYrP4LAITpwr7HeNR3aQm4Ezbiau+D6TiTawpcLm4jYwLJxZ3n5BnN+wgbT8lRNoGigD3j26reas09MZwYKZkhYmuf4ypiMNN0H1TNmz5LZ7DEUgGne5PbaU8TOjeSUTeTjhYm/+CpcHRVaHmJ7jBFeJ5WbPFLHpPf5Imfuox7yj0wCxnNzuzb7JJoL/5zAjwNPlL2gda+uvuON4LIDU4BbYzh9VmnYzdW0Sne6C8d75fqSMdv28atVitcPGynaodeQAjui2ttEysCnh47nOlsPbKsYpW2tqh/XO3S72W2nXq9WyQ6iSK1SVLRKlozBfN1tlTfjwMebb+TYlhO0Q9cT0YtQulBmW8Xdsa2G5wXvnpmYjBKB+5HFnQ3hbP0nvhl3OGZbLyMRi2hb2FaByUbUEuDO8Nrr56KDdQG2g2biIfsW8JWA6wlzzNIeJ34TtK/kGbZP2/wVc/3Wm3itI4Uf56KYaH7LORufvye3SF/QXSmv5AOzev8AXpWS5w==)

### Композиційний API {#composition-api}

За допомогою Композиційного API ми визначаємо логіку компонента за допомогою імпортованих функцій API. У SFC Композиційного API зазвичай використовується з [`<script setup>`](/api/sfc-script-setup). Атрибут `setup` — це підказка, яка змушує Vue виконувати перетворення під час компіляції, що дозволяє нам використовувати Композиційний API з меншою кількістю повторюваного шаблонного коду. Наприклад, імпортовані функції та змінні/функції верхнього рівня, оголошені в `<script setup>`, можна безпосередньо використовувати в шаблоні SFC.

Ось той самий компонент із тим самим шаблоном, але з використанням Композиційного API та `<script setup>`:

```vue
<script setup>
import { ref, onMounted } from 'vue'

// реактивний стан
const count = ref(0)

// функції, що змінюють стан і запускають оновлення
function increment() {
  count.value++
}

// хуки життєвого циклу
onMounted(() => {
  console.log(`Початковий рахунок: ${count.value}.`)
})
</script>

<template>
  <button @click="increment">Рахунок: {{ count }}</button>
</template>
```

[Спробуйте у Пісочниці](https://play.vuejs.org/#eNp9VE1v00AQ/SsjCwmqRglSb1Go+FAPcAAEHH1IcLapW8e27HWJFEUKKW05ICKhKlyQ4ALntPQjJHX6F3b/Ar+EN+vaaSVaKXJ2583OvPdm7a71KAzL24mwqlYtdiI3lKu2LzphEElqivVG4knq2j5RpULqi5qpsX6vB2qijtScV3pUInWh5tif6L5K9Q7HSJ1RsyEb95YMysiJ3kXWsR4C/0R6hzimxmp6WS3F8w+Z4mOVXnbkDQGc4OBIzXD4Mx9H1pBL1OWGG9fLnJx1y6gSRUImkZ/viJwg8WWV7mf7Hv/1Sraf6/oGdgNmpyb0t39Aek+dkP6gd8Bqqvf0SH8tkR5izcrUObikYGK4FJQJoAFG5kQOo2xq7JlBbgp4aPhy2329S+oc4CkA6LyAJbDiLjqdwWf4YppyiUNAeBqXpogby9kTWAYrP4LAITpwr7HeNR3aQm4Ezbiau+D6TiTawpcLm4jYwLJxZ3n5BnN+wgbT8lRNoGigD3j26reas09MZwYKZkhYmuf4ypiMNN0H1TNmz5LZ7DEUgGne5PbaU8TOjeSUTeTjhYm/+CpcHRVaHmJ7jBFeJ5WbPFLHpPf5Imfuox7yj0wCxnNzuzb7JJoL/5zAjwNPlL2gda+uvuON4LIDU4BbYzh9VmnYzdW0Sne6C8d75fqSMdv28atVitcPGynaodeQAjui2ttEysCnh47nOlsPbKsYpW2tqh/XO3S72W2nXq9WyQ6iSK1SVLRKlozBfN1tlTfjwMebb+TYlhO0Q9cT0YtQulBmW8Xdsa2G5wXvnpmYjBKB+5HFnQ3hbP0nvhl3OGZbLyMRi2hb2FaByUbUEuDO8Nrr56KDdQG2g2biIfsW8JWA6wlzzNIeJ34TtK/kGbZP2/wVc/3Wm3itI4Uf56KYaH7LORufvye3SF/QXSmv5AOzev8AXpWS5w==)

### Що вибрати? {#which-to-choose}

Обидва стилі API цілком здатні охопити стандартні випадки використання. Це різні інтерфейси, які працюють від однієї й тієї ж основної системи. Фактично, Опційний API реалізовано поверх Композиційного API! Основні концепції та знання про Vue спільні для обох стилів.

Опційний API побудовано навколо концепції «екземпляра компонента» (`this`, як показано в прикладі), який зазвичай краще узгоджується з розробкою на основі класу для користувачів, які мають досвід ООП. Він також більш зручний для початківців, оскільки абстрагується від деталей реактивності та забезпечує організацію коду через групи параметрів.

Композиційний API, своєю чергою, побудовано навколо концепції оголошення реактивних змінних безпосередньо в області функції та компонуванні єдиного реактивного стану з множини функцій, що підійде для складніших компонентів/випадків. Цей стиль має менше обмежень та потребує розуміння того, як реактивність працює у Vue, щоб ефективно використовувати її. Своєю чергою, гнучкість цього стилю забезпечує більш потужні можливості повторного використання та організації логіки.

Ви можете ознайомитись з більш детальним порівнянням двох стилів та потенційними перевагами Композиційного API у [FAQ щодо Композиційного API](/guide/extras/composition-api-faq).

Якщо ви тільки знайомитесь з Vue, ось наша загальна рекомендація:

- З метою навчання використовуйте стиль, який вам здається легшим для розуміння. Знову ж таки, більшість основних концепцій спільні для двох стилів. Ви завжди можете обрати інший стиль пізніше.

- Для комерційних проєктів:

  - Використовуйте Опційний API, якщо ви не користуєтеся інструментами збірки або плануєте використовувати Vue переважно в додатках низької складності.

  - Використовуйте Композиційний API + Single-File Components, якщо плануєте створювати повноцінні програми за допомогою Vue.

На етапі навчання вам не потрібно дотримуватися лише одного стилю. Решта документації містить зразки коду в обох стилях, де це можливо, і ви можете будь-коли перемикатися між ними за допомогою **перемикача параметрів API** у верхній частині лівої бічної панелі.

## Все ще є запитання? {#still-got-questions}

Перегляньте наші [FAQ](/about/faq).

## Виберіть свій стиль навчання {#pick-your-learning-path}

Різні розробники мають різні стилі навчання. Не соромтеся вибрати стиль навчання, який відповідає вашим уподобанням, хоча ми рекомендуємо переглянути всю документацію, якщо це можливо!

<div class="vt-box-container next-steps">
  <a class="vt-box" href="/tutorial/">
    <p class="next-steps-link">Спробуйте Посібник</p>
    <p class="next-steps-caption">Для тих, хто надає перевагу навчанню на практиці.</p>
  </a>
  <a class="vt-box" href="/guide/quick-start.html">
    <p class="next-steps-link">Прочитайте <br>Гід</p>
    <p class="next-steps-caption">Гід детально ознайомить вас з усіма аспектами фреймворку.</p>
  </a>
  <a class="vt-box" href="/examples/">
    <p class="next-steps-link">Перегляньте приклади</p>
    <p class="next-steps-caption">Ознайомтеся з прикладами основних функцій і типових завдань при розробці інтерфейсу користувача.</p>
  </a>
</div>
