## Плагины для Visual Studio Code
 - ***`Color Info (✔)`*** ― плагин, который даёт вам возможность получать краткую справку об используемых в CSS цветах.
 - ***`AutoFileName (✔)`*** ― плагин, который автоматически дополняет пути к файлам.
 - ***`Babel ES6/ES7`*** - плагин, преобразующий ES6 в ES5.
 - ***`Debugger for Chrome (✔)`*** ― плагин для отладки кода в Chrome.
 - ***`ESlint (✔)`*** ―  плагин, который интегрирует анализатор кода ESLint в VS code.
 - ***`Gitlens (✔)`*** ― плагин помогает представлять информацию о истории кода в Git, плавно перемещаться и исследовать историю файла или ветки.
 - ***`HTML Boilerplate (✔)`*** ― плагин, которое упрощает работу с HTML файлами, избавляя вас от необходимости прописывать теги head и body вручную.
 - ***`Javascript (ES6) code snippets (✔)`*** ― плагин в котором собраны сниппеты языка Javascript.
 - ***`Live Server (✔)`*** ― плагин, позволяющий просматривать написанный код в браузере в режиме  *`hot reload`*
 - ***`Markdown Preview Enhanced`*** ― плагин, позволяющий просматривать файлы с расширением *`.md`* 
 - ***`Npm Intellisense (✔)`*** ― плагин позволяет автоматически дополнять имена модулей из *`npm`*
 - ***`Path Intellisense (✔)`*** ― плагин позволяет автоматически дополнять имена файлов по мере ввода строки.
 - ***`Prettier (✔)`*** ― плагин, которое позволяет приводить код, написанный несколькими людьми, к единообразному виду.
 - ***`Quokka.js (✔)`*** ― плагин, дающая возможность предварительного просмотра результата выполнения того или иного куска кода.
 - ***`Simple React Snippets (✔)`*** ― плагин, содержащий множество сниппетов для React JS.
 - ***`SVG Viewer (✔)`*** ― плагин привносит в VS Code возможность работать с SVG файлами.
 - ***`Vue (✔) `*** ― плагин, содержащий множество сниппетов для Vue JS.
 - ***`TODO highlight`*** ― плагин позволяет проставлять метки всем недоделанным местам в коде, что упрощает дальнейшую работу над проектом.
 
## Лучшие темы для Visual Studio Code

*Atom One Dark Theme ( ✔  )*
*Dracula Official Theme ( ✔  )*
*Material Theme ( ✔  )*
*Monokai Pro ( ✔  )*
*Material Theme ( ✔  )*
*Ayu*
*Captain Sweetheart*
*Cobalt2 Theme*
*Firewatch Theme*
*Flatland Monokai Theme*
*Seti Theme*

## Шрифты для написания кода

*Fira Code Mono ( ✔  )*
*Inconsolata*
*Source Code Pro*
*Ubuntu Mono ( ✔  )*
*Hermit ( ✔  )*
*PT Mono*
*Consolas Mono*
*Monaco*

## Настраиваем рабочее окружение
Жмём <kbd>F1</kbd>, печатаем `workspace` и жмём <kbd>Enter</kbd>.
В появившимся окне настроек справа вставляем заготовленные настройки:
```json
{
	"gitlens.advanced.messages": {
		"suppressCommitHasNoPreviousCommitWarning": false,
		"suppressCommitNotFoundWarning": false,
		"suppressFileNotUnderSourceControlWarning": false,
		"suppressGitVersionWarning": false,
		"suppressLineUncommittedWarning": false,
		"suppressNoRepositoryWarning": false,
		"suppressResultsExplorerNotice": false,
		"suppressShowKeyBindingsNotice": true,
		"suppressUpdateNotice": true,
		"suppressWelcomeNotice": false
	},
	"liveServer.settings.donotShowInfoMsg": true,
	"editor.fontSize": 13,
	"editor.tabSize": 2,
	"editor.wordWrap": "on",
	"editor.formatOnSave": true,
	"prettier.printWidth": 80,
	"eslint.enable": true,
	"files.insertFinalNewline": true,
	"explorer.confirmDelete": false,
	"editor.lineHeight": 24,
	"explorer.decorations.badges": false,
	"emmet.syntaxProfiles": {
		"javascript": "jsx",
		"xml": {
			"attr_quotes": "single"
		}
	},
	"emmet.includeLanguages": {
		"javascript": "javascriptreact"
	},
	"emmet.triggerExpansionOnTab": true,
	"files.associations": {
		"*.vue": "vue"
	},
	"prettier.trailingComma": "none",
	"gitlens.keymap": "none",
	"vsicons.projectDetection.disableDetect": true,
	"vsicons.dontShowNewVersionMessage": true,
	"workbench.colorTheme": "Dracula Soft",
	"editor.fontFamily": "Fira Code Medium",
	"editor.fontLigatures": true,
	"winopacity.opacity": 245,
	"window.zoomLevel": 1,
	"editor.minimap.enabled": true,
}
```

## Разрешаем использование декораторов
Создаем конфигурационный файл с названием `jsconfig.json` и наполняем его следующим содержимым:
```json
{
  "compilerOptions": {
    "experimentalDecorators": true
  }
}
```
