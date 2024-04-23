{
  "env": {
    "browser": true,
    "es2021": true
  },
  "extends": [
    "plugin:react/recommended",
    "prettier"
  ],
  "parserOptions": {
    "ecmaFeatures": {
      "jsx": true
    },
    "ecmaVersion": 12,
    "sourceType": "module"
  },
  "plugins": [
    "react-hooks",
    "import",
    "prettier"
  ],
  "rules": {
    "react/jsx-filename-extension": [1, { "extensions": [".js", ".jsx", ".tsx", ".ts"] }],
    "react/require-default-props": "off",
    "no-param-reassign": "off",
    "jsx-a11y/alt-text": "off",
    "react/react-in-jsx-scope": "off",
    "react/display-name": "off",
    "prettier/prettier": "error",
    "no-unused-vars": "off"
  },
  "settings": {
    "react": {
      "version": "detect"
    },
    "import/resolver": {
      "node": {
        "moduleDirectory": [
          "node_modules",
          "src/"
        ]
      }
    }
  },
  "globals": {
    "JSX": true
  }
}
