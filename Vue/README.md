# Vue
Learning progress

1.install Node

    https://nodejs.org/en/download/

  i recommend you to install the LTS(stable version) msi package
  after installing, node -v & npm -v to check the result
  considering we use the msi package, "Path" of environment do not need modification

    npm config set registry https://registry.npm.taobao.org
  
  in order to download more quick, please change the local mirror of taobao.
2.install vue

    npm install vue -g
    g means node_global


3.install vue-cli

    npm install vue-cli -g
    vue-cli could help us create the template file (vue + webpack)


4.create vue project

    cd D:\vue_workspace
    vue init webpack vueDemo  it will help us to create and initial the project

5.run the project

    npm install
    npm run dev
    tips: if you are developing the front and backgroud in one PC, remember to change the port iin the index.js file, should be different from the backgroud project (default is 8080).

6.install bootstrap-vue

    currently is the begin of the vue project, i choose the bootstrap-vue for UI
    bootstrap-vue is much more close to original html
    npm i bootstrap-vue
    https://bootstrap-vue.org/
    we could find most of the controls usage from this site

7.id will be mount by Vue -- el

8.template means the content in the el -- template

9.instance is the combine of the el and template

10.v-text will not be transfered by vue, but v-html will

11.v-show and v-if

    v-if will clean the html, remove from DOM
    v-show will just act as display: none

12.v-for
    better to add :key="item", it will improve the performance
    key should be unique