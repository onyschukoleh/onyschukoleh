======================================================================= 
Горияие клавиши в VSCode:
- одноврименный выбор нескольких одинаковых елементов  Ctrl+D
- переход в браузер Alt+L+O


=======================================================================
В VSCode:

+ ESLint		//https://eslint.org/docs/user-guide/integrations
+ LiveServer  		
+ ES7 React/Redux/GraphQL/React-Native snippes  // алиасы prop-typs под REACT
+ Prettier-Code		https://prettier.io/docs/en/editors.html

=======================================================================
Настройки VSCode
{
  "files.autoSave": "onFocusChange",
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
}

=======================================================================
В терминале (https://github.com/goitacademy/react-lint-config)

$ npm install --save-dev prettier husky lint-staged
$ vi .prettierrc.json
		{
		"printWidth": 80,
 		"tabWidth": 2,
		"useTabs": false,
		"semi": true,
		"singleQuote": true,
		"trailingComma": "all",
		"bracketSpacing": true,
		"jsxBracketSameLine": false,
		"arrowParens": "avoid",
		"proseWrap": "always" 
		}
$vi .huskyrc
		{
		  "hooks": {
		  "pre-commit": "lint-staged"
			   }
		}
$vi .lintstagedrc
		{
  		"src/**/*.{json,css,scss,md}": ["prettier --write"],
  		"src/**/*.{js,jsx,ts,tsx}": ["prettier --write", "eslint --fix"]
		}



	.gitignore
		# dependencies
		/node_modules
		/.pnp
		/pnp/js

		# testing
		/coverage

		# production
		/build

		# misc
		.DS_Store
		.env.local
		.evn.development.local
		.evn.test.local
		.evn.production.local
		npm-debug.log*
		yarn-debug.log*
		yarn-error.log*


