# PC-Builder (WIP)
Small website I made to try out **Vuetify** and test my frontend development skills. Inspired by LTT's secret shopper series. **It is functional, but it is not actually meant to be used as it is right now**.

## Installation
1. Clone the repo.
2. `npm install`
3. `npm run serve` for development, `npm run build` for production.

## Known issues
On the production build, some files will return 404. Remove the initial `/` in the `index.html`. 

eg:

`<script src="/js/app.000000.js"></script>` to `<script src="js/app.000000.js"></script>`


## License
Licensed under the [MIT License](https://github.com/RelatedTitle/PC-Builder/blob/main/LICENSE).