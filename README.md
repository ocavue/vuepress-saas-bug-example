reproduction repo for https://github.com/vuejs/vuepress/issues/353

step1:

    $ cd vuepress-theme-project
    $ yarn link
    success Registered "vuepress-theme-project".
    info You can now run `yarn link "vuepress-theme-project"` in the projects where you want to use this module and it will be used instead.
    $ cd ../vuepress-project
    $ yarn link vuepress-theme-project
    success Using linked module for "vuepress-theme-project".
    $ yarn install

step2:

    $ cd vuepress-project
    $ yarn run dev

error:

    ERROR in ../vuepress-theme-project/enhanceApp.js
    Module not found: Error: Can't resolve 'sass-loader' in '/tmp/vuepress-saas-bug-example/vuepress-project'
    @ ../vuepress-theme-project/enhanceApp.js 1:0-22
    @ ./node_modules/vuepress/lib/app/.temp/themeEnhanceApp.js
    @ ./node_modules/vuepress/lib/app/app.js
    @ ./node_modules/vuepress/lib/app/clientEntry.js
    @ multi ./node_modules/vuepress/lib/app/clientEntry.js

If you remove `import "./theme.scss";` in vuepress-theme-project/enhanceApp.js, everything is ok.
