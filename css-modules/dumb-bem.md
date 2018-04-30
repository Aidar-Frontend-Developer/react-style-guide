


## Использование библиотеки dumb-bem

`dumb-bem` — это библиотека, предназначенная для создания атомарных React-компонентов с BEM/SMACSS правилами по наименованию классов.

Передавая имя блока в функцию `dumbBem`, мы получаем функцию-декоратор, которая меняет свойства у React-элемента.
Для изменения свойств будем использовать библиотеку `transform-props-with`.
Для начала установим зависимости `dumbBem` и `transform-props-with`
```json
yarn add dumb-bem transform-props-with
```

Добавим их в наш проект

```javascript
import dumbBem from 'dumb-bem'
import tx from 'transform-props-with'

// здесь header — название BEM блока
const dumbHeader = dumbBem('header')

const Header = tx(dumbHeader)('header')
const Title = tx([dumbHeader,  { element: 'title' }])('h1')
const Subtitle = tx([dumbHeader, { element: 'subtitle' }])('h2')

const DumbComponent = ({ title = 'Title', subtitle = 'Subtitle' }) => (
    <Header>
        <Title>{ title }</Title>
        <Subtitle hidden={!subtitle}>{ subtitle }</Subtitle>
    </Header>
)

export default DumbComponent
```

И на выходе наш компонент `DumbComponent` будет выглядеть следующим образом:

```html
<div class="header">
  <h1 class="header__title">Title</h1>
  <h2 class="header__subtitle">Subtitle</h2>
</div>
```
