<template>
  <div id="app">
    <Header/>
    <transition  name="slide-fade">
        <router-view></router-view> 
    </transition>
  </div>
</template>

<script>
  import Header from './components/Header'
export default {
  name: 'App',
  components: {
    Header
  }
}
</script>

<style>
@font-face{
     font-family: 'FuturaStd'; 
     src: url('assets/font/FuturaStd.otf');
}
html, body{
  height: 100%;
  margin: 0;
  font-family: 'FuturaStd'
}
#app {
  height: 100%;
  width: 100%;
  /*background-color: black;*/
}
/* 可以设置不同的进入和离开动画 */
/* 设置持续时间和动画函数 */
.slide-fade-enter-active {
  transition: all .3s ease;
}
.slide-fade-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active for below version 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}
</style>
