## Preact Poi starter

So whats the deal here?

Poi justs works. Of course Poi will try to look up a `.babelrc`. Since Preact has a different __jsx pragma__ you must have __transform-react-jsx__ plugin with `{ pragma: "h" }` opt at least to work with.

```json
{
  "sourceMaps": true,
  "presets": [
    ["es2015", { "loose":true }],
    "stage-0"
  ],
  "plugins": [
    ["transform-decorators-legacy"],
    ["transform-react-jsx", { "pragma": "h" }]
  ]
}
```

For this example I added `transform-decorators-legacy` as well.

#### run development server

`npm run dev` aka `$ poi [root file]`

#### run production build

`npm run build` aka `$ poi build [root file]`
