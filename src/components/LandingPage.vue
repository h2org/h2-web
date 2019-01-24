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
  -webkit-box-sizing: border-box;
          box-sizing: border-box;
  font-family: "TypoPRO Bebas Neue", sans-serif;
  padding: 1rem;
  -webkit-box-shadow: inset 0 0 0 5px white;
          box-shadow: inset 0 0 0 5px white;
  color: white;
  font-size: inherit;
  position: relative;
  vertical-align: middle;
  margin-top: 6rem;
  margin-bottom: 5rem;
}
button::before,
button::after {
  -webkit-box-sizing: inherit;
          box-sizing: inherit;
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
}
.download-button {
  -webkit-transition: color 0.25s;
  transition: color 0.25s;
}
.download-button::before,
.download-button::after {
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
.download-button:hover::before,
.download-button:hover::after {
  width: 100%;
  height: 100%;
}
.download-button:hover::before {
  border-top-color: #60daaa;
  border-right-color: #60daaa;
  -webkit-transition: width 0.25s ease-out, height 0.25s ease-out 0.25s;
  transition: width 0.25s ease-out, height 0.25s ease-out 0.25s;
}
.download-button:hover::after {
  border-bottom-color: #60ccda;
  border-left-color: #60ccda;
  -webkit-transition: border-color 0s ease-out 0.5s, width 0.25s ease-out 0.5s,
    height 0.25s ease-out 0.75s;
  transition: border-color 0s ease-out 0.5s, width 0.25s ease-out 0.5s,
    height 0.25s ease-out 0.75s;
}
.landing-page-grid {
  max-width: 100vw;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-areas: "download poster";
  font-size: 2.5rem;
  text-align: justify;
  padding-left: 4rem;
}
.poster-h2 {
  grid-area: poster;
}
.quick-download-grid {
  grid-area: download;
  max-width: 700px;
}
.quick-download-grid p {
  margin-top: 20vh;
  color: rgba(255, 255, 255, 0.58);
  max-width: 60%;
}
.button-download {
  padding-top: 0.1em;
  color: white;
  max-width: 55%;
  text-align: center;
  border: 5px solid white;
  padding: 0.7rem;
}
.poster-h2 img {
  width: 80%;
}
@media screen and (max-width: 1054px) {
.landing-page-grid {
    grid-template-columns: 1fr;
    grid-template-areas: "poster" "download";
    padding-left: 0rem;
    width: 90vw;
}
.quick-download-grid p {
    margin-top: 10vh;
    max-width: 80%;
}
.button-download {
    max-width: 80%;
}
button {
    width: 100%;
}
.download-button-wrap {
    width: 80%;
    -ms-flex-item-align: center;
        align-self: center;
    justify-self: center;
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
.poster-h2,.quick-download-grid {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-orient: vertical;
  -webkit-box-direction: normal;
      -ms-flex-direction: column;
          flex-direction: column;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
  -webkit-box-pack: center;
      -ms-flex-pack: center;
          justify-content: center;
}
}

</style>


