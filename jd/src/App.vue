<template>
  <div id="app">
    <Shortcut />
    <Header />
    <FS />
    <Floors />
  </div>
</template>

<script>
import Shortcut from './components/Shortcut.vue';
import Header from './components/Header.vue';
import FS from './components/FS.vue';
import Floors from './components/Floors.vue';

export default {
  name: 'app',
  components: {
    Shortcut,
    Header,
    FS,
    Floors,
  }
}
</script>

<style lang="scss">
body{
  margin:0;
  -webkit-font-smoothing: antialiased;
  background-color: #fff;
  font: 12px/1.5 Microsoft YaHei,tahoma,arial,Hiragino Sans GB,\\5b8b\4f53,sans-serif;
  color: #666;
}
@font-face {
    font-family: iconfont;
    src: url("/fonts/iconfont.woff");
}
a{
  color:#999;
}
</style>
