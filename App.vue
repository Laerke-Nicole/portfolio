<script setup>
import { RouterLink, RouterView } from 'vue-router'

function myFunction() {
   var x = document.getElementById("myLinks");
   if (x.style.display === "block") {
     x.style.display = "none";
   } else {
     x.style.display = "block";
   }
} 
</script>


<template>
  <!-- my navigation -->
  
  <header> 
    <div>
      <!-- my logo -->
      <RouterLink to="/"><img src="./assets/logo-light.svg" height="45" alt="" class="logo"></RouterLink>
  
      <!-- links -->
      <!-- Load an icon library to show a hamburger menu (bars) on small screens -->
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
  
        <!-- nav on bigger screens -->
        <!-- "Hamburger menu" / "Bar icon" to toggle the navigation links -->
        <a href="javascript:void(0);" class="icon" @click="myFunction">
          <i class="fa fa-bars"></i>
        </a>
      </div>
      <nav id="myLinks"  @click="myFunction">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/contact">Kontakt</RouterLink>
        <RouterLink to="/portfolio">Portfolio</RouterLink>  
        <a href="https://firebasestorage.googleapis.com/v0/b/portfolio-5a046.appspot.com/o/cv.pdf?alt=media&token=179e9337-fe02-4611-8c69-f0914fbd36bb" target="_blank"><li>CV &nearr;</li></a>
        <RouterLink to="/about">Om mig</RouterLink>

        
      </nav>
  </header>


  <!-- Load an icon library to show a hamburger menu (bars) on small screens -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">



  <RouterView />
  
  <!-- footer -->
  <footer>
    <h1>Lad os arbejde sammen!</h1>
    <RouterLink to="/contact">
        <button id="button1" class="button">Kontakt mig</button>
    </RouterLink>

    <!-- links in footer -->
    <div class="footerContent">
      <div class="footerMyName">
        <h2>Lærke Nicole Nielsen</h2>
        <h2>Lærke Nicole Nielsen</h2>
        <h2>Lærke Nicole Nielsen</h2>
      </div>

        <ul>          
          <RouterLink to="//www.linkedin.com/in/laerke-nicole-nielsen/" target="_blank"><li>LinkedIn</li></RouterLink>
          <RouterLink to="//github.com/Laerke-Nicole" target="_blank"><li>Github</li></RouterLink>
        </ul>

        <ul>
          <RouterLink to="/contact"><li>Kontakt</li></RouterLink>
          <RouterLink to="/portfolio"><li>Portfolio</li></RouterLink>
          <a href="https://firebasestorage.googleapis.com/v0/b/portfolio-5a046.appspot.com/o/cv.pdf?alt=media&token=179e9337-fe02-4611-8c69-f0914fbd36bb" target="_blank"><li>CV &nearr;</li></a>
          <RouterLink to="/about"><li>Om mig</li></RouterLink>
        </ul>
    </div>

    <!-- my mail in footer -->
    <div class="mail">
      <h4>laenie01@easv365.dk</h4>
      <hr>
    </div>
  </footer>
</template>


<style scoped>
a.icon {
  display: none;
  color: var(--white-headline);
}

a.icon:hover {
  color: var(--primary-hover);
  background-color: var(--black-text);
}

.v-enter-active,
.v-leave-active {
  transition: opacity 1.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}

/*
  Enter and leave animations can use different
  durations and timing functions.
*/
.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateX(20px);
  opacity: 0;
}


.bounce-enter-active {
  animation: bounce-in 0.5s;
}
.bounce-leave-active {
  animation: bounce-in 0.5s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.25);
  }
  100% {
    transform: scale(1);
  }
}


/* navigationbar */
header {
  line-height: 1.5;
  min-height: 10vh;
  padding: 7px 2rem 0;
  position: fixed;
  z-index: 1000;
  background-color: var(--black-text);
  /* display: flex; */
  flex-direction: row;
  flex-wrap: nowrap;
  place-items: center; 
  /* padding-right: calc(var(--section-gap) / 2); */ /* changed */
  width: 100%;
  align-items: center;
}

header > div{
  width: 100%;
  position: relative;
}

.logo {
  display: flex;
  align-items: center;
  justify-content: center;
}

nav {
  display: flex;
  justify-content: center;
  width: 100%;
  text-align: center;
  text-align: left;
}

nav a.router-link-exact-active {
  color: var(--primary-hover);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  color: var(--white-headline);
  font-weight: 600;
  transition: 0.3s;
  color: var(--white-headline);
  line-height: 1.6;
  font-family: rift, sans-serif;
  font-style: normal !important;
  list-style-type: none;
}

nav a:first-of-type {
  border: 0;
}

nav a:hover {
  color: var(--primary-hover);
}

header .wrapper {
  display: flex;
  place-items: flex-start;
  flex-wrap: wrap;
  width: 100%;  /* changed */
} 

/* Style the hamburger menu */
.icon {
  display: block;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  right: 0;
  padding-right: 32px;
  align-items: center;
}
/* navigationbar end */


/* footer */
footer {
  background-color: var(--primary-color);
  padding-bottom: 45px;
}

footer h1 {
  color: var(--white-headline);
  font-family: condor, sans-serif;
  font-style: normal;
  font-weight: 200;
  font-size: 40px;
  text-align: center;
  padding-top: 45px;
  padding-bottom: 16px;
}

.footerContent {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}

footer .footerMyName h2 {
  color: var(--white-headline);
  font-family: rift, sans-serif;
  font-style: normal;
  font-weight: bold; 
  font-size: 30px;
  display: flex;
  flex-direction: column;
}

footer .button {
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 30px auto;
}

footer ul {
  padding: 0;
}

footer li {
  display: flex;
  flex-direction: column;
  color: var(--white-headline);
  font-family: rift, sans-serif;
  font-style: normal;
  font-weight: bold; 
  font-size: 30px;
  display: flex;
  flex-direction: column;
  transition: 0.3s;
}

footer li:hover {
  color: var(--primary-hover);
}

.mail {
  display: flex;
  color: var(--white-headline);
  font-family: condor, sans-serif;
  font-style: normal;
  font-weight: 200;
  font-size: 18px;
  gap: 18px;
  justify-content: center;
  padding: 18px 0 60px 0;
}

.mail hr {
  display: block;
  border-width: 0;
  height: 2px;
  width: 62%;
  background-color: var(--white-headline);
  align-self: center;
}
/* footer end */


/* responsive */

@media only screen and (min-width: 800px) {
  nav {
    display: block;
    display: flex;
    position: absolute;
    top: 30%;
    left: 30px;
  }
}


@media only screen and (max-width: 800px) {
  nav {
  display: none;
  }

  nav a {
    display: flex;
    flex-direction: column;
    text-align: center;
    padding: 16px 0;
  }

  a.icon {
  display: block !important;
  }
}

@media only screen and (max-width: 780px) {
  footer h1 {
    font-size: 35px;
  }

  footer .footerMyName h2 {
    font-size: 24px;
  }

  footer li {
    font-size: 24px;
  }

  .mail hr {
    width: 55%;
  }
}

@media only screen and (max-width: 600px) {
  .footerContent {
    flex-direction: column;
    text-align: center;
  }

  footer ul {
    padding: 12px 0;
  }

  .mail {
    font-size: 16px;
  }

  .mail hr {
    width: 52%;
  }
}

@media only screen and (max-width: 500px) {
  footer h1 {
    font-size: 24px;
  }

  .mail hr {
    width: 48%;
  }
}
/* responsive end */


</style>
