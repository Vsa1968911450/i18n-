<template>
  <div id="app">
    <div id="nav">
      <p @click="zhongwen">中文</p> |
      <p  @click="yinwen">英文</p>
      <div>{{ $t('main.logo') }}</div>
    </div>
    <router-view/>
  </div>
</template>
<script>
export default {
  data () {
    return {

    }
  },
  methods: {
    zhongwen () {
      localStorage.setItem('lang', 'cn')
      this.$i18n.locale = 'cn'
    },
    yinwen () {
      localStorage.setItem('lang', 'en')
      this.$i18n.locale = 'en'
    }
  }
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
