<template>
    <div class="header-grid" >
        <div  class="mob-div" />
        <img src="./../assets/logo.png" />
        <a  v-for="(item, i) in items"
                :key="i" v-on:click="gotosite(item.link)"
       > {{ item.title }} </a>
        <div class="mobile-menu"> 
           <v-menu bottom left>
            <v-btn
              slot="activator"
              dark
              icon
            >
              <v-icon>more_vert</v-icon>
            </v-btn>

            <v-list>
              <v-list-tile
                v-for="(item, i) in items"
                :key="i"
                v-on:click="gotosite(item.link)"
              >
                <v-list-tile-title>{{ item.title }}</v-list-tile-title>
              </v-list-tile>
            </v-list>
          </v-menu>
        </div>
    </div>
</template>
<script>
export default {
    name:'Header',
    data: () => ({
      items: [
        { title: 'SOURCE',link:'https://github.com/poush/H2' },
        { title: 'COMMUNITY',link:'https://gitter.im/h2org/community#' }
      ]
    }),
     methods : {
        gotosite(producturl) {
          window.location.href = producturl
      }
    }
}
</script>
<style lang="css" scoped>

.mobile-menu,.mob-div{
    display: none;
}
.header-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr) 8fr;
  margin-left: 3rem;
  margin-top: 1rem;
}
.header-grid img {
  height: 5rem;
  grid-column-gap: 1em;
}
a {
  cursor: pointer;
}
.header-grid a {
  height: inherit;
  color: rgba(255, 255, 255, 0.58);
  font-size: 2.3rem;
  justify-self: center;
  -ms-flex-item-align: center;
      align-self: center;
}
.header-grid a:hover {
  color: white;
}
@media screen and (max-width: 1054px) {
.header-grid {
    grid-template-columns: 5fr 1fr;
}
a,.header-grid img  {
    display: none;
}
.mobile-menu,.mob-div {
    display: block;
}
}

</style>


