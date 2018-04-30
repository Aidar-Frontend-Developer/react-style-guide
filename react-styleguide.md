
## Styleguide for react components

- Использовать *`lodash`* только при работе c коллекциями

> import _ from 'lodash'

------------
- Использовать глобальные зависимости *`React, Redux, PropTypes и.т.д`*

> import React, { Component } from 'react'

> import PropTypes from 'prop-types'

* ***Примечание***: Отделяйте локально импортируемые зависимости от других. Повышает читаемость кода

------------
- Использовать общие компоненты *`ca-common`*

> import { CATable, CARow, CACell } from 'ca-common/ui-lib/components/TableElements'

------------
- Использовать *`fetcher`*

> import {fetchWrapper} from 'ca-common/redux/modules/common'

------------
- Использовать стили для компонента *`scss`*

> import './AccountActivity.cscc'

------------
- Использовать константы

> import { arrayValue } from './array'

------------
### Создание компонента через class

- Создание компонента через *`class`*

> class AccountActivity extends Component

------------
- Все статичное выводим тут в следующем порядке:

	- Статические методы и переменные:

		> 		static ARRAY = [1,2,4,5]
		> 		static METHOD() {}

	- Статичные свойства *`propTypes`* и *`defaultProps`*:

        > 		static propTypes = {
        > 			option: PropTypes.string,
        > 			age: PropTypes.number.isRequired
        > 		}

        > 		static defaultProps = {
        > 			option: 'Я принимаю строку поскольку я не isRequired'
        > 		}

	* ***Примечание***: описываем props типа объект в propTypes

        > 		static propTypes = {
        > 			letter: PropTypes.shape({
        > 				number: PropTypes.number
        > 			}).isRequired
        > 		}

------------
- Использовать *`constructor`*, если он необходим

* ***Примечание***: Необходимость возникает только при использовании (state)
	> 		constructor(props) {
	> 			super(props);
	> 			this.state = {
	> 				checkValue: this.props.checking
	> 			}
	>		 }

* ***Примечание***: props в конструктор не пробрасываем, если мы не используем его через this.props

	> 		constructor() {
	> 			super();
	> 			this.state = {
	> 				checkValue: 'I am state'
	> 			}
	>		 }

* ***Примечание***: state можно объявлять и без конструктора
	> 		state = {
	> 			checkValue: 'I am state'
	>		 }
------------
- Использование *`Lifecycle methods`* , если он необходим.

	> 		componentDidMount() {
	> 			this.timerId = setInterval( ()=> this.tick(), 1000 )
	> 		}

------------
- Использование методов

	> 		handleChechoxShowStatus = () => {
	> 			this.setState(prevState => ({ expanded: !prevState.expanded }))
	> 		}

* ***Примечание***: Желательно использовать стрелочные функции `arrow function` и называть методы с суфиксом "*handle*"
* ***Примечание к this.setState***: Чтобы получить измененный state, передайте функцию setState, с предыдущим состоянием в качестве аргумента

------------
-  Использование метода *`render`*

* ***Примечание***: В методе *`render`* используйте деструктуризацию пропросов и стейтов

	>		const {checkboxStatus, accout} = this.props
	> 		const {checkValue} = this.state

------------
- Использование метода *`return`*

* ***Примечание***: Стараемся избегать анонимных функций в методе render. Выносите их в отдельные функции.
Каждый раз, когда родительский компонент перерендеривается, создается новая функция что и приводит к повторному рендерингу
  >       return (
	> 			<input type=text onChange={(e) => { model.name = e.target.value } />
	> 		)

* ***Примечание***: Используйте это вариант

	> 		return (
	> 			<input type=text onChange={this.handleCheckboxStatus} />
	> 		)

------------
- Использование метода *`mapStateToProps`*

* ***Примечание***: Если нам необходимо вытянуть данные из (store) используем mapStateToProps

	> 		function mapStateToProps (state) {
	>			return {
	> 				user: state.user
	>			}
	>		 }

------------
- Использование метода *`mapDispatchToProps`*

* ***Примечание***: Чтобы сохранить некоторые сообщения, Redux предоставляет bindActionCreators(), который позволяет вам это сделать

	> 		function mapDispatchToProps(dispatch) {
	> 			return bindActionCreators({ increment, decrement }, dispatch);
	>		 }

------------
- Использование метода *`connect`*

* ***Примечание***: Функция *`connect`* позволяет нам получить в качестве props для компонента данные из store. *`mapStateToProps`* и *`mapDispatchToProps`* передаем по мере необходимости

	> connect(mapStateToProps, mapDispatchToProps)(AccountActivity)

------------

### Stateless functional components

* ***Примечание***: У этих компонентов нету состояния (stateless). Они чисты и понятны, используйте их как можно чаще.

	> 		const Square = ({ value, onClick }) => {
	> 			<button className="square" onClick={onClick}>{value}<button/>
	>		 )}

### Чем они отличаются от statefull компонентов ?

- propTypes
* ***Примечание***: Объявление proptypes вынесены из компонента

	> 		Stateless.propTypes = {
	> 			title: PropTypes.string
	>		 }
- Деструктуризация *`props`* и *`defaultProps`*

	> 		const Stateless = ({ title = 'React' }) => {
	> 			return ( <div>{title}</div> )
	>		 }
* ***Примечание***: defalutProps можно объявлять в самих props *`title = 'React'`*
------------

* ***Примечание*** Написать Best practise для следующих разделов
- ~~VSCode configuration~~
- ~~Eslint~~
	- ~~Auto-fix~~
	- ~~Eslintrc configuration~~
- CSS Modules (in progress)
	- Post-Processing CSS
	- Classnames
	- Dumb-bem
	- Styled-components
- Immutable.js
- Reselect
- Git (precommit)
- Flexbox

- Webpack
- React-Router
- Redux
	- Middleware
- ReduxForm
- Jest, Enzyme testing
- Redux Saga
- Recompose
- Typescipt
- Flow
- Deploy
- UI library
- Often used npm modules
- JS Patterns
- REST API
	- GraphQL
	-	Websocket
		- Socket.io
- Backend
	- Ruby
