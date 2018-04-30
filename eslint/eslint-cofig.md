// .eslintrc | Common eslint rules
module.exports = {
  "env": {
    "es6": true,
    "node": true,
    "browser": true
  },
  "parser": "babel-eslint",
  "parserOptions": {
    "ecmaVersion": 6,
    "sourceType": "module"
  },
  "globals": {
    "console": false,
    "navigator": true,
    "window": true,
  },
  "extends": [
    "eslint:recommended",
    "plugin:react/recommended",
    "plugin:jsx-a11y/recommended",
    "plugin:css-modules/recommended"
  ],
  "plugins": [
    "react",
    "jsx-a11y",
    "css-modules"
  ],
  "rules": {
    "css-modules/no-unused-class": [2, { "camelCase": true }],
    "css-modules/no-undef-class": [2, { "camelCase": true }],
    "for-direction": "error",
    "getter-return": "error",
    "no-await-in-loop": "error",
    "no-extra-parens": ["off", "all", {
      "conditionalAssign": true,
      "nestedBinaryExpressions": false,
      "returnAssign": false,
      "ignoreJSX": "all",
      "enforceForArrowConditionals": false,
    }],
    "no-prototype-builtins": "error",
    "no-template-curly-in-string": "error",
    "valid-jsdoc": "error",
    "accessor-pairs": "error",
    "array-callback-return": "error",
    "block-scoped-var": "error",
    "class-methods-use-this": "error",
    "complexity": [
      "off",
      11
    ],
    "consistent-return": "error",
    "curly": "error",
    "default-case": "error",
    "dot-location": [
      "error",
      "property"
    ],
    "dot-notation": "error",
    "eqeqeq": "error",
    "guard-for-in": "error",
    "no-alert": "error",
    "no-caller": "error",
    "no-div-regex": "error",
    "no-else-return": "error",
    "no-empty-function": "error",
    "no-eq-null": "error",
    "no-eval": "error",
    "no-extend-native": "error",
    "no-extra-bind": "error",
    "no-extra-label": "error",
    "no-floating-decimal": "error",
    "no-global-assign": "error",
    "no-implicit-coercion": "error",
    "no-implicit-globals": "off",
    "no-implied-eval": "error",
    "no-invalid-this": "off",
    "no-iterator": "error",
    "no-labels": "error",
    "no-lone-blocks": "error",
    "no-loop-func": "error",
    "no-magic-numbers": ["error", { "ignoreArrayIndexes": true, "ignore": [-1, 0, 1] }],
    "no-multi-spaces": "error",
    "no-multi-str": "error",
    "no-new": "error",
    "no-new-func": "error",
    "no-new-wrappers": "error",
    "no-octal-escape": "error",
    "no-param-reassign": "error",
    "no-proto": "error",
    "no-restricted-properties": "error",
    "no-return-assign": "error",
    "no-return-await": "error",
    "no-script-url": "error",
    "no-self-compare": "error",
    "no-sequences": "error",
    "no-throw-literal": "error",
    "no-unmodified-loop-condition": "error",
    "no-unused-expressions": "error",
    "no-useless-call": "error",
    "no-useless-concat": "error",
    "no-useless-return": "error",
    "no-void": "error",
    "no-warning-comments": "warn",
    "no-with": "error",
    "prefer-promise-reject-errors": "error",
    "radix": "error",
    "require-await": "error",
    "vars-on-top": "error",
    "wrap-iife": "error",
    "yoda": "error",
    "strict": "off",
    "init-declarations": [
      "error",
      "always"
    ],
    "no-catch-shadow": "error",
    "no-label-var": "error",
    "no-restricted-globals": "error",
    "no-shadow": "error",
    "no-shadow-restricted-names": "error",
    "no-undef-init": "error",
    "no-undefined": "error",
    "no-use-before-define": "error",
    "array-bracket-newline": [
      "error",
      {
        "multiline": true,
        "minItems": 3
      }
    ],
    "array-bracket-spacing": [
      "error",
      "never"
    ],
    "array-element-newline": [
      "error",
      {
        "minItems": 3
      }
    ],
    "block-spacing": "error",
    "brace-style": "error",
    "camelcase": [
      "error",
      {
        "properties": "never"
      }
    ],
    "capitalized-comments": "error",
    "comma-dangle": [
      "error",
      "only-multiline"
    ],
    "comma-spacing": [
      "error",
      {
        "before": false,
        "after": true
      }
    ],
    "comma-style": [
      "error",
      "last"
    ],
    "computed-property-spacing": [
      "error",
      "never"
    ],
    "consistent-this": [
      "error",
      "self"
    ],
    "eol-last": [
      "error",
      "always"
    ],
    "func-call-spacing": [
      "error",
      "never"
    ],
    "func-name-matching": "error",
    "func-names": [
      "error",
      "never"
    ],
    "func-style": [
      "error",
      "declaration",
      {
        "allowArrowFunctions": true
      }
    ],
    "function-paren-newline": ['error', 'multiline'],
    "id-blacklist": [
      "error",
      "data",
      "err",
      "e",
      "cb",
      "callback"
    ],
    "id-length": [
      "error",
      {
        "properties": "never",
        "exceptions": [
          "_"
        ]
      }
    ],
    "indent": [
      "error",
      2
    ],
    "jsx-quotes": [
      "error",
      "prefer-double"
    ],
    "key-spacing": [
      "error",
      {
        "afterColon": true
      }
    ],
    "keyword-spacing": "error",
    "line-comment-position": [
      "error",
      {
        "position": "above"
      }
    ],
    "max-depth": [
      "error",
      4
    ],
    "max-len": [
      "error",
      120
    ],
    "max-lines": [
      "error",
      250
    ],
    "max-nested-callbacks": [
      "error",
      2
    ],
    "max-params": [
      "error",
      3
    ],
    "max-statements": [
      "off",
      10
    ],
    "max-statements-per-line": [
      "error",
      {
        "max": 1
      }
    ],
    "multiline-ternary": [
      "error",
      "always-multiline"
    ],
    "new-cap": ["error", { "properties": false }],
    "new-parens": "error",
    "newline-per-chained-call": [
      "error",
      {
        "ignoreChainWithDepth": 2
      }
    ],
    "no-array-constructor": "error",
    "no-bitwise": "error",
    "no-continue": "error",
    "no-inline-comments": "off",
    "no-lonely-if": "error",
    "no-mixed-operators": "error",
    "no-multi-assign": "error",
    "no-multiple-empty-lines": "error",
    "no-negated-condition": "error",
    "no-nested-ternary": "error",
    "no-new-object": "error",
    "no-plusplus": [
      "error",
      {
        "allowForLoopAfterthoughts": true
      }
    ],
    "no-trailing-spaces": "error",
    "no-underscore-dangle": "error",
    "no-unneeded-ternary": "error",
    "no-whitespace-before-property": "error",
    "nonblock-statement-body-position": [
      "error",
      "below"
    ],
    "object-curly-newline": ["error", {
      "ObjectExpression": { "minProperties": 4, "multiline": true, "consistent": true },
      "ObjectPattern": { "minProperties": 4, "multiline": true, "consistent": true }
    }],
    "object-curly-spacing": [
      "error",
      "always"
    ],
    "object-property-newline": [
      "error",
      {
        "allowMultiplePropertiesPerLine": true
      }
    ],
    "one-var": [
      "error",
      "never"
    ],
    "one-var-declaration-per-line": [
      "error",
      "initializations"
    ],
    "operator-assignment": [
      "error",
      "always"
    ],
    "operator-linebreak": [
      "error",
      "after"
    ],
    "padded-blocks": [
      "error",
      "never"
    ],
    "quote-props": [
      "error",
      "as-needed"
    ],
    "quotes": [
      "error",
      "single"
    ],
    "require-jsdoc": "off",
    "semi": "error",
    "semi-spacing": "error",
    "semi-style": [
      "error",
      "last"
    ],
    "sort-keys": "off",
    "sort-vars": "off",
    "space-before-blocks": "error",
    "space-before-function-paren": [
      "error",
      "never"
    ],
    "space-in-parens": [
      "error",
      "never"
    ],
    "space-infix-ops": "error",
    "space-unary-ops": "error",
    "spaced-comment": [
      "error",
      "always"
    ],
    "switch-colon-spacing": "error",
    "template-tag-spacing": "error",
    "unicode-bom": [
      "error",
      "never"
    ],
    "wrap-regex": "off",
    "padding-line-between-statements": [
      "error",
      {
        "blankLine": "always",
        "prev": [
          "const",
          "let",
          "var"
        ],
        "next": "*"
      },
      {
        "blankLine": "any",
        "prev": [
          "const",
          "let",
          "var"
        ],
        "next": [
          "const",
          "let",
          "var"
        ]
      }
    ],
    "arrow-body-style": [
      "error",
      "as-needed"
    ],
    "arrow-parens": [
      "error",
      "as-needed",
      {
        "requireForBlockBody": true
      }
    ],
    "arrow-spacing": "error",
    "generator-star-spacing": [
      "error",
      {
        "before": false,
        "after": true
      }
    ],
    "no-confusing-arrow": [
      "error",
      {
        "allowParens": true
      }
    ],
    "no-duplicate-imports": "error",
    "no-useless-computed-key": "error",
    "no-useless-constructor": "error",
    "no-useless-rename": "error",
    "no-var": "error",
    "object-shorthand": [
      "error",
      "always",
      {
        "avoidExplicitReturnArrows": true
      }
    ],
    "prefer-arrow-callback": "error",
    "prefer-const": "error",
    "prefer-destructuring": [
      "error",
      {
        "VariableDeclarator": {
          "object": true,
          "array": true
        }
      }
    ],
    "prefer-numeric-literals": "error",
    "prefer-rest-params": "error",
    "prefer-spread": "error",
    "prefer-template": "error",
    "rest-spread-spacing": [
      "error",
      "never"
    ],
    "sort-imports": ["off", {
      "ignoreCase": false,
      "ignoreMemberSort": false,
      "memberSyntaxSortOrder": ["none", "all", "multiple", "single"],
    }],
    "symbol-description": "error",
    "template-curly-spacing": "error",
    "yield-star-spacing": [
      "error",
      "after"
    ],
    "react/boolean-prop-naming": [
      "error",
      {
        "rule": "(^(is|has)[A-Z]([A-Za-z0-9]?)+)|(^[A-Za-z0-9]+(ed|able|ing)$)"
      }
    ],
    "react/default-props-match-prop-types": [
      "error",
      {
        "allowRequiredDefaults": true
      }
    ],
    "react/forbid-component-props": "off",
    "react/forbid-elements": [
      "off",
      {
        "forbid": [
          {
            "element": "button",
            "message": "use <Button /> instead"
          }
        ]
      }
    ],
    "react/forbid-prop-types": "error",
    "react/forbid-foreign-prop-types": "error",
    "react/no-array-index-key": "warn",
    "react/no-did-mount-set-state": "error",
    "react/no-did-update-set-state": "error",
    "react/no-multi-comp": "warn",
    "react/no-redundant-should-component-update": "error",
    "react/no-set-state": "off",
    "react/no-unused-prop-types": "error",
    "react/no-will-update-set-state": "error",
    "react/prefer-es6-class": [
      "error",
      "always"
    ],
    "react/prefer-stateless-function": "error",
    "react/require-default-props": "error",
    "react/self-closing-comp": "error",
    "react/sort-comp": "error",
    "react/sort-prop-types": ["error", {
      "callbacksLast": false,
      "ignoreCase": true,
      "requiredFirst": true,
    }],
    "react/style-prop-object": "error",
    "react/void-dom-elements-no-children": "error",
    "react/jsx-boolean-value": [
      "error",
      "never"
    ],
    "react/prop-types": ["error", {
      "ignore": [ "children" ]
    }],
    "react/jsx-closing-bracket-location": ["error", "line-aligned"],
    "react/jsx-closing-tag-location": "error",
    "react/jsx-curly-spacing": "error",
    "react/jsx-equals-spacing": "error",
    "react/jsx-filename-extension": "error",
    "react/jsx-first-prop-new-line": "error",
    "react/jsx-handler-names": "error",
    "react/jsx-indent": [
      "error",
      2
    ],
    "react/jsx-indent-props": [
      "error",
      2
    ],
    "react/jsx-max-props-per-line": [
      "error",
      {
        "maximum": 3
      }
    ],
    "react/jsx-no-bind": "error",
    "react/jsx-pascal-case": "error",
    "react/jsx-sort-props": "error",
    "react/jsx-space-before-closing": "error",
    "react/jsx-tag-spacing": ["error", { "beforeSelfClosing": "always" }],
    "react/jsx-wrap-multilines": [
      "error",
      {
        "declaration": false,
        "assignment": false,
        "return": false,
        "arrow": false
      }
    ],
    "jsx-a11y/click-events-have-key-events": "off"
  },
  "overrides": [
    {
      "files": [
        "assets/javascripts/**/*.js",
        "assets/javascripts/**/*.jsx"
      ],
      "excludedFiles": "*.test.js",
      "plugins": [
        "react"
      ],
      "env": {
        "es6": true,
        "node": true
      }
    },
    {
      "files": [
        "gemini/**/*.js",
      ],
      "plugins": [
        "react"
      ],
      "globals": {
        "geminiReact": true
      },
      "env": {
        "es6": true,
        "node": true
      },
      "rules": {
        "react/jsx-filename-extension": "off",
        "prefer-arrow-callback": "off",
        "max-nested-callbacks": [
          "error",
          6
        ],
        "no-empty-function": "off",
        "max-lines": "off",
        "no-magic-numbers": "off",
      }
    },
    {
      "files": [
        "*.test.js"
      ],
      "env": {
        "es6": true,
        "node": true,
        "jest": true
      },
      "globals": {
        "context": true,
        "set": true,
      },
      "plugins": [
        "jest"
      ],
      "rules": {
        "jest/no-disabled-tests": "warn",
        "jest/no-focused-tests": "error",
        "jest/no-identical-title": "error",
        "jest/valid-expect": "error",
        "no-unused-expressions": "off",

        "max-nested-callbacks": [
          "error",
          6
        ],
        "react/jsx-filename-extension": "off",
        "no-magic-numbers": "off"
      },
      "settings": {
        "import/resolver": ["jest", { "babel-module": {} }]
      }
    }
  ]
};
