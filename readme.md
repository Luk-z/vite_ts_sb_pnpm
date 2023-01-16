# Vite + Typescript + Storybook + pnpm

## Install

```shell
git clone https://github.com/Luk-z/vite_ts_sb_pnpm.git

cd vite_ts_sb_pnpm

nvm use
# or `nvm i` and maybe `npm install -g pnpm`

pnpm install

pnpm storybook
```

Should throw an error like

```shell
$ pnpm storybook

> vite_ts_sb_pnpm@0.0.0 storybook /Users/luca.ziliani/code/my/test_storybook/vite_ts_sb_pnpm
> storybook dev -p 6006

@storybook/cli v7.0.0-beta.28

info => Starting manager..
✘ [ERROR] Could not resolve "vue/dist/vue"

    node_modules/.pnpm/@zeplin+storybook-inspector@0.1.3_react-dom@18.2.0/node_modules/@zeplin/storybook-inspector/dist/index.js:1:20422:
      1 │ ...react-element-to-jsx-string")},921:e=>{e.exports=require("vue/dist/vue")}},t={};return function n(o){var r=t[o];if(void 0!==r)re...
        ╵                                                             ~~~~~~~~~~~~~~

  The module "./dist/vue" was not found on the file system:

    node_modules/.pnpm/@zeplin+storybook-inspector@0.1.3_react-dom@18.2.0/node_modules/vue/package.json:32:16:
      32 │     "./dist/*": "./dist/*",
         ╵                 ~~~~~~~~~~

  Import from "vue/dist/vue.js" to get the file
  "node_modules/.pnpm/@zeplin+storybook-inspector@0.1.3_react-dom@18.2.0/node_modules/vue/dist/vue.js":

    node_modules/.pnpm/@zeplin+storybook-inspector@0.1.3_react-dom@18.2.0/node_modules/@zeplin/storybook-inspector/dist/index.js:1:20435:
      1 │ ...element-to-jsx-string")},921:e=>{e.exports=require("vue/dist/vue")}},t={};return function n(o){var r=t[o];if(void 0!==r)return r...
        │                                                                    ^
        ╵
```

## Steps to create the project

```shell
pnpm create vite vite_ts_sb_pnpm --template react-ts

pnpm dlx storybook@7.0.0-beta.28 init

pnpm  add -D storybook-zeplin

# add "storybook-zeplin/register" to addons in main.cjs

```
