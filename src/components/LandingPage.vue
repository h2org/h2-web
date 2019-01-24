<template>
    <div class="landing-page-grid" > 
        <div class="quick-download-grid" >
            <p>H2 is a minimalist browser to watch embeded videos and more in picture-in-picture mode.</p>
           <button class="download-button">DOWNLOAD FOR MAC</button>
        </div>
        <div class="poster-h2" >
            <img src="../assets/dsh2.png" alt="">
        </div>
    </div>

</template>
<script>
export default {
    name:'Landing Page',
}
</script>
<style lang="css" scoped>

button {
  width: 60%;
  background: none;
  border: 0;
  box-sizing: border-box;
  font-family: 'TypoPRO Bebas Neue',sans-serif;
  padding:1rem;
  box-shadow: inset 0 0 0 5px white;
  color: white;
  font-size: inherit;
  position: relative;
  vertical-align: middle;
}
button::before, button::after {
  box-sizing: inherit;
  content: '';
  position: absolute;
  width: 100%;
  height: 100%;
}

.download-button {
  transition: color 0.25s;
}
.download-button::before, .download-button::after {
  border: 5px solid transparent;
  width: 0;
  height: 0;
}
.download-button::before {
  top: 0;
  left: 0;
}
.download-button::after {
  bottom: 0;
  right: 0;
}
.download-button:hover {
  color: #60daaa;
}
.download-button:hover::before, .download-button:hover::after {
  width: 100%;
  height: 100%;
}
.download-button:hover::before {
  border-top-color: #60daaa;
  border-right-color: #60daaa;
  transition: width 0.25s ease-out, height 0.25s ease-out 0.25s;
}
.download-button:hover::after {
  border-bottom-color: #60ccda;
  border-left-color: #60ccda;
  transition: border-color 0s ease-out 0.5s, width 0.25s ease-out 0.5s, height 0.25s ease-out 0.75s;
}



.landing-page-grid {
    margin-left: 4rem;
    width: 100vw;
    display: grid;
    grid-template-columns: 1fr 1fr;
    font-size: 2.5rem;
    text-align: justify;
}
.quick-download-grid p {
    margin-top: 20vh;
    color: rgba(255,255,255,.58);
    max-width: 60%;
}
.button-download {
    color: white;
    max-width: 55%;
    text-align: center;
    border: 5px solid white;
    padding: 0.7rem;
}
.poster-h2 img {
    width: 80%;
}

</style>


