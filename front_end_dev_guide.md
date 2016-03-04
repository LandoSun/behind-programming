前端小队开发指引
===================

前端生态了解
-------------------

> TODO：待寻觅合适的slides

暂时请参考：

* [2015前端生态发展回顾](https://github.com/kuitos/kuitos.github.io/issues/32)
* [前端组件库](https://github.com/JingwenTian/awesome-frontend)
* [Frontend Development](https://github.com/dypsilon/frontend-dev-bookmarks)
* [Awesome JavaScript](https://github.com/sorrycc/awesome-javascript)
* [awesome之Front-end Development](https://github.com/sindresorhus/awesome#front-end-development)

前端工作流选型
---------------

* 使用[Webpack](https://webpack.github.io/)，而非[Browserify](http://browserify.org/)
* 如果够用，使用`npm`自己的[极简工作流支持](http://blog.keithcirkel.co.uk/how-to-use-npm-as-a-build-tool/)，原因参考：
  - [Why we should stop using Grunt & Gulp](http://blog.keithcirkel.co.uk/why-we-should-stop-using-grunt/)
  - [Choose: Grunt, Gulp, or npm?](https://ponyfoo.com/articles/choose-grunt-gulp-or-npm)
* 如果不够，则使用[Gulp](https://github.com/alferov/awesome-gulp)加以补充
* 不使用[GruntJS](http://gruntjs.com/)

前端技术选型
----------------

* 不支持IE等古代浏览器
* [HTML5]((https://developer.mozilla.org/zh-CN/docs/Web/Guide/HTML/HTML5))
* [CSS3](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS3)
  - 使用 [SCSS](http://sass-lang.com/guide)语法 来写
  - 不使用SASS、[Less](http://lesscss.org/)
* JS
  - 使用 [ES6](http://es6-features.org/)（又称之为ES2015） 来写
  - 英文资料参考[Overview of ECMAScript 6 features](https://github.com/lukehoban/es6features)
  - 中文资料参考[《ECMAScript 6入门》](http://es6.ruanyifeng.com/)
  - 不使用：
    + ES4：大部分的IE只支持到这个程度，即很多人理解里的古代JS，语言/库特性缺失太严重
    + [ES5](http://yanhaijing.com/es5/)：大部分现代浏览器只支持到这个程度。ES5为JS打下来扎实的语言/库基础。
    + [TypeScript](http://www.typescriptlang.org/)：微软倒腾出来的ES5的超集，增加了类型支持。
    + [CoffeeScript](http://coffeescript.org/)：Rails社区很火过
    + 想要对比这些语言，请见[TypeScript vs. CoffeeScript vs. ES6](http://www.slideshare.net/NeilGreen1/type-script-vs-coffeescript-vs-es6)
  - 使用[Babel](https://babeljs.io/)将ES6预编译成ES5来在浏览器中运行
* CSS框架选用众所周知的[Bootstrap](http://v4-alpha.getbootstrap.com/)
  - 直接选择其[版本4](http://blog.getbootstrap.com/2015/08/19/bootstrap-4-alpha/)
  - 不选择目前受众最广的[版本3](http://getbootstrap.com/)，主要考虑到前端发展一日千里，版本3很快会失去支持，而且版本4提供了很多新的组件和特性。
* JS框架选用类似[React](https://github.com/enaqx/awesome-react)但更轻的[Vue.js](http://vuejs.org/) ：
  - Vue.js的丰富资料，见[Awesome Vue.js](https://github.com/vuejs/awesome-vue)
  - Vue.js和其他前端框架的比较，请见[Comparison with Other Frameworks](http://vuejs.org/guide/comparison.html)
  - 使用官方的[脚手架vue-cli](https://github.com/vuejs/vue-cli)中的[webpack模版](https://github.com/vuejs-templates/webpack)来生成项目结构，包含：
    + [Webpack](https://webpack.github.io/) + [vue-loader](http://vuejs.github.io/vue-loader) 支持 `.vue`单文件组件
    + [Babel](https://babeljs.io/)来将ES6转换为ES5
    + [Karma](https://karma-runner.github.io)+[Jasmine](http://jasmine.github.io/)来做单元测试  
    + [inject-loader](https://github.com/plasticine/inject-loader)来做[Mock](http://vuejs.github.io/vue-loader/workflow/testing-with-mocks.html)
    + [eslint](http://eslint.org/) 做JS静态代码检查
    + [EditorConfig](http://editorconfig.org/) 来配置代码编辑器
  - 额外选择[Building Large-Scale Apps(Using Vue.js)](http://vuejs.org/guide/application.html)中推荐的：
    + [vue-router](https://github.com/vuejs/vue-router) 解决路由问题
    + [vue-resource](https://github.com/vuejs/vue-resource) 解决和后端[RESTful服务](https://github.com/marmelab/awesome-rest)通讯的问题
    + [Vuex](https://github.com/vuejs/vuex/) 实现 [Flux](https://facebook.github.io/flux/) ，或者采用兼容 React 和 Vue.js 的 [Redux](https://github.com/rackt/redux/)
  - 额外选择：`TODO: 待将上述选择生成为1个模版`

前端开发规范参考
------------------

> 当你难以确定最佳实践的时候，看看业界是怎么做的

* [前端开发规范手册](https://github.com/Aaaaaashu/Front-End-Style-Guide)
* [前端代码规范 及 最佳实践](http://coderlmn.github.io/code-standards/)
* [豆瓣Javascript代码风格规范](https://docs.google.com/document/pub?id=17ICSeE4Qd04-1U-pphmKCAmfgJGEVjqDellbu4oAiqU)
* [豆瓣CSS开发规范](https://docs.google.com/document/pub?id=17dKkWwdaKyNnkwswihHje2cfoMGqbSJLydTIxqFwlQU)
* [网易HTML规范](http://nec.netease.com/standard/html-structure.html)
* [网易CSS开发规范](http://nec.netease.com/standard/css-sort.html)
* [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript/tree/master/es5)
* [Isobar Front-end Code Standards](http://isobar-idev.github.io/code-standards/)
* [PUP Front end standards](http://www.yellowshoe.com.au/standards/)
* [TMWtech Front-End Dev guidelines](http://tech.tmw.co.uk/code/TMW-frontend-guidelines/)
* [Frontend Guidelines](https://github.com/bendc/frontend-guidelines)
* [Front End Development Guidelines](http://taitems.github.io/Front-End-Development-Guidelines/)
* [Front-end Style Guides](https://24ways.org/2011/front-end-style-guides/)
* [20 Useful Docs and Guides for Front-End Developers](http://www.sitepoint.com/20-docs-guides-front-end-developers/)