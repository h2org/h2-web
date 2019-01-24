<template>
    <div class="header-grid" >
        <img src="./../assets/logo.png" />
        <a> HOME </a>
        <a> DOWNLOAD </a>
        <a> ABOUT </a>
        <a> FORUMS </a>
    </div>
</template>
<script>
export default {
    name:'Header',
}
</script>
<style lang="css" scoped>
.header-grid {
    display: grid;
    grid-template-columns: repeat(5,1fr) 8fr;
    margin-left: 3rem;
    margin-top: 1rem;
}
.header-grid img {
    height: 5rem;
    grid-column-gap: 1em;
}
.header-grid a {
   height: inherit;
   color: rgba(255,255,255,.58);
   font-size: 2.3rem;
   justify-self: center;
   align-self: center;
}
.header-grid a:hover {
    color: white;
}
</style>


