# npm ls

<v-clicks>

## - `npm ls`
## - `npm ls *`
## - `npm ls * | grep lodash`
## - `npm ls lodash`
## - `npm ls --production`

</v-clicks>

---

# Dedupe

```zsh
$ npm ls lodash
```

```zsh {all|3|6,9|all}
test-project@0.0.1 /home/evgenii/test-project
├─┬ cypress@13.14.2
│ └── lodash@4.17.21
├─┬ eslint-plugin-vue@9.28.0
│ └─┬ vue-eslint-parser@9.4.3
│   └── lodash@4.17.21 deduped
└─┬ start-server-and-test@2.0.8
  └─┬ wait-on@8.0.1
    └── lodash@4.17.21 deduped
```
