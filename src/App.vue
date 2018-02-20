<template>
  <div id="app">
    <div id="menu">
      <a><router-link :to="'/'">Home</router-link></a>
      /
      <a><router-link :to="'/about'">About</router-link></a>
      /
      <a><router-link :to="'/projects'">Projects</router-link></a>
    </div>
    <transition name="slide" mode="in-out">
      <keep-alive>
        <router-view />
      </keep-alive>
    </transition>
  </div>
</template>

<script>

export default {
  name: 'App'
}
</script>

<style>
@import 'https://fonts.googleapis.com/css?family=Abril+Fatface|Lato|Oswald|Quando|Teko';
@import 'https://dl.dropbox.com/s/50g6fbds3rh4m0j/saturnicons.css';
@import 'https://raw.githubusercontent.com/daneden/animate.css/master/animate.css';

:root {
  /* --color-orange: #f7c282; */
  --color-orange: #7E52A0;
}

body {
  overflow-x: hidden;
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  word-wrap: break-word;
  color: #888888;
  font-family: Helvetica, Arial, sans-serif;
  font-size: 11px;
  line-height: calc(11px + 5px);
  background-color: #f6f6f6;
  background-image: url(https://assets.tumblr.com/images/x.gif?v=1);
  background-attachment: fixed;
  background-repeat: repeat;
}

input, textarea, select, a {
    outline: none;
}

a {
    color: #444444;
    text-decoration: none;
    -webkit-transition: all 0.6s ease;
    -moz-transition: all 0.6s ease;
    -o-transition: all 0.6s ease;
    transition: all 0.6s ease;
}

.page-enter-active, .page-leave-active {
  transition: 1s, transform 1s;
}
.page-enter, .page-leave-to {
  opacity: 0;
  transform: translateX(-30%);
}

.slide-leave-active,
.slide-enter-active {
  transition: 1s;
}
.slide-enter {
  transform: translate(100%, 0);
}
.slide-leave-to {
  transform: translate(-100%, 0);
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

#menu {
    position: fixed;
    top: 0px;
    left: 0px;
    width: 100%;
    height: 50px;
    text-align: center;
    z-index: 1000;
    padding: 0;
}

#menu a {
    margin: 0px 10px;
    color: #333333;
    min-height: 30px;
    line-height: 55px;
    font-size: 12px;
    padding: 5px 15px;
    letter-spacing: 2px;
    cursor: pointer;
    text-transform: uppercase;
}

.close {
  position: absolute;
  bottom: 20px;
  right: 20px;
  width: 40px;
  height: 40px;
  padding: 5px;
  line-height: 50px;
  text-align: center;
  border: 1px solid #dddddd;
  background: #dddddd;
  cursor: pointer;
  z-index: 10000;
}

.close:hover, .close span:hover {
  color: #D295BF;
}
</style>
