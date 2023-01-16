# Vite + Typescript + Storybook + pnpm

## Install

```
git clone https://github.com/Luk-z/vite_ts_sb_pnpm.git

cd vite_ts_sb_npm

nvm use
# or nvm i

## use --force to bypass npm Conflicting peer dependency
npm install --force

npm run storybook
```

Should throw an error like

```
@storybook/cli v7.0.0-beta.28

info => Starting manager..
✘ [ERROR] Could not resolve "vue/dist/vue"

    node_modules/@zeplin/storybook-inspector/dist/index.js:1:20422:
      1 │ ...react-element-to-jsx-string")},921:e=>{e.exports=require("vue/dist/vue")}},t={};return function n(o){var r=t[o];if(void 0!==r)re...
        ╵                                                             ~~~~~~~~~~~~~~

  The module "./dist/vue" was not found on the file system:

    node_modules/vue/package.json:32:16:
      32 │     "./dist/*": "./dist/*",
         ╵                 ~~~~~~~~~~

  Import from "vue/dist/vue.js" to get the file "node_modules/vue/dist/vue.js":

    node_modules/@zeplin/storybook-inspector/dist/index.js:1:20435:
      1 │ ...element-to-jsx-string")},921:e=>{e.exports=require("vue/dist/vue")}},t={};return function n(o){var r=t[o];if(void 0!==r)return r...
        │                                                                    ^
        ╵                                                                    .js
```
