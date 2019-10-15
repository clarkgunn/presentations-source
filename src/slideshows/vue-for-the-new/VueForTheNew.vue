
<template>
  <div id="MyFirstSlideshow">
    <div class="eg-slideshow">
      <slide enter="animated fadeInDown">
        <h1>Vue for the New</h1>
        <img src="./assets/vue-logo.png" alt="Vue.js logo">
      </slide>
      <slide enter="animated fadeUp">
        <img style="border-radius: 100%" src="./assets/Clark.png" alt="a photo of me">
        <h1>Clark Mitchell</h1>
        <div style="display:flex; align-items: center">
          <ul style="list-style:none;">
            <li><span class="grey">https://</span>ClarkMitchell.dev</li>
            <li>
              <img class="icon" src="./assets/twitter-xxl.png" alt="twitter icon">
              <span class="grey">@</span>TheVikingDev
            </li>
            <li>
              <img class="icon" src="./assets/github-11-xxl.png" alt="twitter icon">
              ClarkMitchell
            </li>
          </ul>
        </div>
      </slide>
      <slide :steps=4 enter="bounceInRight" leave="bounceOutDown">
        <h3>The Progressive Javascript Framework</h3>
        <div class="center">
          <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
            <h4 v-if="step >= 2">Reactivity</h4>
          </eg-transition>
          <eg-transition enter="bounceInRight" leave="bounceOutRight">
            <h4 v-if="step >= 3">Composability</h4>
          </eg-transition>
          <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
            <h4 v-if="step >= 4">Ecosystem</h4>
          </eg-transition>
        </div>
      </slide>
      <slide enter="animated fadeInDown">
        <h1>Evan You</h1>
        <img class="fullimage" src="./assets/evan-you.jpg" alt="Vue.js logo">
      </slide>
      <slide :steps=3 enter="bounceInRight" leave="bounceOutDown">
        <h4>What Came Before...</h4>
        <eg-transition enter="bounceInLeft" leave="bounceOutRight">
          <img v-if="step == 2" src="./assets/iconfinder_JQuery_logo_282806.png" alt="Vue.js logo">
        </eg-transition>
        <eg-transition enter="fadeInUp" leave="bounceOutRight">
          <img class="fullimage" v-if="step == 3" src="./assets/jquery-soup.png" alt="Vue.js logo">
        </eg-transition>
      </slide>
      <slide :steps=2 enter="bounceInRight" leave="bounceOutDown">
        <h3>The Enterprise Alternative</h3>
        <div class="center">
          <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
            <img v-if="step >= 2" src="./assets/angular.png" alt="Vue.js logo">
          </eg-transition>
          <eg-transition enter="bounceInRight" leave="bounceOutRight">
            <img v-if="step >= 3" src="./assets/react-logo.png" alt="Vue.js logo">
          </eg-transition>
        </div>
      </slide>
      <slide :steps=2 enter="bounceInRight" leave="bounceOutDown">
        <h3>The Facebook Frontrunner</h3>
        <div class="center">
          <eg-transition enter="bounceInRight" leave="bounceOutRight">
            <img v-if="step >= 2" src="./assets/react-logo.png" alt="Vue.js logo">
          </eg-transition>
        </div>
      </slide>
      <slide enter="animated fadeInDown">
        <h1>Vue<span class="grey">.js</span></h1>
        <img src="./assets/vue-logo.png" alt="Vue.js logo">
      </slide>
      <slide enter="animated fadeInDown">
        <h4>new Vue();</h4>
        <img src="./assets/declarative.png" alt="simple vue example">
      </slide>
      <slide :steps=4 enter="bounceInRight" leave="bounceOutDown">
        <h3>Declarative Rendering</h3>
        <div class="center">
          <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
            <h4 v-if="step >= 2">"Mustache" Template syntax</h4>
          </eg-transition>
          <eg-transition enter="bounceInRight" leave="bounceOutRight">
            <h4 v-if="step >= 3">Data Binding</h4>
          </eg-transition>
          <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
            <h4 v-if="step >= 4">Reactivity</h4>
          </eg-transition>
        </div>
      </slide>
      <slide enter="animated fadeInDown">
        <input type="text" placeholder="enter text" v-model="binding">
        <h1>{{ binding }}</h1>
        <img src="./assets/new-vue.png" alt="simple vue example">
      </slide>
      <slide enter="fade in">
        <h1 v-if="visible">Conditionals</h1>
        <input type="checkbox" v-model="visible" name="visible">
        <label for="visible">Show the title?</label>
        <img class="fullimage" src="./assets/v-if.png" alt="conditional code example">
      </slide>
      <slide id="loops" :steps=3 enter="bounceInRight" leave="bounceOutDown">
        <h1>Loops</h1>
        <eg-transition enter="bounceInLeft" leave="none">
          <img v-if="step == 2" src="./assets/v-for.png" alt="Vue.js logo">
        </eg-transition>
        <eg-transition enter="bounceInLeft" leave="none">
          <div v-if="step == 3">
          <ol>
            <li v-bind:key="todo" v-for="todo in todos">
              {{ todo }}
            </li>
          </ol>
          </div>
        </eg-transition>
      </slide>
      <slide enter="fade in">
        <h3>{{ onTitle }}</h3>
        <button v-on:click="reverseTitle">Reverse Title</button>
        <img class="fullimage"  src="./assets/v-on.png" alt="v-on code example">
      </slide>
      <slide enter="animated fadeInUp">
        <h2>Vue Lifecycle</h2>
        <img class="fullimage" src="./assets/vue-lifecycle-hooks.png" alt="vue lifecycle flowchart">
      </slide>
      <slide enter="animated fadeInUp">
        <h2>Lifecycle hooks</h2>
        <img class="fullimage" src="./assets/created.png" alt="vue lifecycle flowchart">
      </slide>
      <slide enter="animated fadeInUp">
        <h2>Components</h2>
        <img class="fullimage" src="./assets/components.png" alt="vue lifecycle flowchart">
      </slide>
      <slide enter="animated fadeInUp">
        <h3>Components and Props</h3>
        <img class="fullimage" src="./assets/component.png" alt="vue lifecycle flowchart">
      </slide>
      <slide enter="animated fadeInUp">
        <h3>Slots</h3>
        <img src="./assets/slots.png" alt="an example of slots">
      </slide>
      <slide enter="animated fadeInUp">
        <h3>Single File Components</h3>
        <img class="fullimage" src="./assets/sfc.png" alt="vue lifecycle flowchart">
      </slide>
      <slide :steps=5 enter="bounceInRight" leave="bounceOutDown">
        <h3>But wait, there's more...</h3>
        <div class="center">
          <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
            <h4 v-if="step >= 2">Event Handlers and Event Modifiers</h4>
          </eg-transition>
          <eg-transition enter="bounceInRight" leave="bounceOutRight">
            <h4 v-if="step >= 3">Custom Events and Named Slots</h4>
          </eg-transition>
          <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
            <h4 v-if="step >= 4">Async Components and Transitions</h4>
          </eg-transition>
          <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
            <h4 v-if="step >= 5">Plugins and more...</h4>
          </eg-transition>
        </div>
      </slide>
      <slide enter="animated fadeInUp">
        <h1>Ecosystem</h1>
      </slide>
      <slide enter="animated fadeInUp">
        <h2>Vue Router</h2>
        <img class="fullimage" src="./assets/router.png" alt="vue lifecycle flowchart">
      </slide>
      <slide enter="animated fadeInUp">
        <h2>Vuex</h2>
        <img class="fullimage" src="./assets/vuex-graph.png" alt="vuex chart">
      </slide>
      <slide enter="animated fadeInUp">
        <h2>Vuepress</h2>
        <img class="fullimage" src="./assets/vuepress.png" alt="vue lifecycle flowchart">
      </slide>
      <slide enter="animated fadeInUp">
        <h2>Nuxt</h2>
        <img class="fullimage" src="./assets/nuxt.png" alt="vue lifecycle flowchart">
      </slide>
      <slide enter="animated fadeInUp">
        <h2>Gridsome</h2>
        <img class="fullimage" src="./assets/gridsome.png" alt="vue lifecycle flowchart">
      </slide>
      <slide enter="animated fadeInUp">
        <h2>Nativescript Vue</h2>
        <img class="fullimage" src="./assets/nativescript-vue.png" alt="vue lifecycle flowchart">
      </slide>
      <slide enter="animated fadeInUp">
        <h2>Slideshows</h2>
        <img class="fullimage" src="./assets/eagle.jpg" alt="eagle js slideshows">
      </slide>
      <slide enter="animated fadeInUp">
        <h1>Questions?</h1>
      </slide>
    </div>
  </div>
</template>

<script>
import eagle from 'eagle.js'

export default {
  mixins: [eagle.slideshow],
  infos: {
    title: 'Vue for the New',
    description: 'Vue.js and its ecosystem',
    path: 'vue-for-the-new'
  },
  data () {
    return {
      binding: '',
      todos: ['Make Slideshow', 'Present on Vue.js'],
      onTitle: 'V-on and Methods',
      visible: true
    }
  },
  methods: {
    reverseTitle () {
      this.onTitle = this.onTitle.split('').reverse().join('')
    }
  }
}
</script>

<style lang='scss'>
  @import url(https://fonts.googleapis.com/css?family=Patrick+Hand+SC);
  .grey {
    color: grey;
  }

  img.fullimage {
    max-width: 100% !important;
    width: 100%
  }

  button {
    padding: 2vh 5vw;
    margin-bottom: 5vh;
    font-size: 1.2em;
  }

  .icon {
    width: 1em;
    height: 1em;
  }

  #MyFirstSlideshow {
    .eg-slideshow {
      font-family: 'Patrick Hand SC';
      background-color: #f8f8f2;

      .eg-slide-content {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
      }
    }
  }
</style>
