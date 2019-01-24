<template>
  <div id="app">
    <Header />
    <div class="center-flex" >
    <LandingPage />
    </div>
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
.center-flex {
  width:100vw;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: center;
      -ms-flex-pack: center;
          justify-content: center;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
}

</style>
