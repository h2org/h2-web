<template>
  <div id="app">
    <Header />
    <LandingPage />
  </div>
</template>

<script>
import Header from './components/Header'
import LandingPage from './components/LandingPage'
export default {
  name: 'app',
  components:{
    Header,
    LandingPage,
  }
}
</script>

<style>


body {
  margin: 0;
  padding: 0;
  background: #00010b;
  overflow-x: hidden;
  font-family: 'TypoPRO Bebas Neue',sans-serif;
}
</style>
