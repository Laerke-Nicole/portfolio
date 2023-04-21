<template>
  <main>

    <!-- about container -->
    <div class="aboutBorder1">
      <div class="about">

        <!-- content about me -->
        <div class="aboutMe">
          <video controls poster="../assets/img/thumbnail.png">
            <source src="../assets/vid/video-cv.mp4"
              type="video/mp4">
          </video>
          <div class="aboutText">
            <h1>Hvem er jeg</h1>
            <p>Jeg er lige nu i gang med min multimediedesigneruddannelse på Erhvervsakademiet Sydvest i Esbjerg. Jeg er passioneret for både foto- og videoredigering, samt design og web-udvikling, men har også interesse for grafisk- og UI/UX design. Jeg elsker at lærer nyt og nørde med mit arbejde, ligegyldig hvilken opgave jeg får. Og min detajleorienteret- og samarbejdssans hjælper mig med at give det bedste resultat.</p>
          </div>
          <div class="aboutSpecialties">
              <p>Design & development</p>
              <p>Videoredigering</p>
              <p>Fotografering</p>
            </div>
        </div>
        
        <!-- bottom with button -->
        <div class="aboutBottom">
          <p>Lærke Nicole Nielsen</p>
          <hr>
          <a href="//youtube.com/watch?v=Z7Z1Q48Qe3o" target="_blank"><button id="button1">Se på Youtube</button></a>
        </div>
      </div>
    </div>

  </main>
</template>

<style>
main {
  padding-top: 10vh;
}

/* border for container */
.aboutBorder1 {
  padding: 15px 15px 15px 15px;
  background-color: var(--white-headline);
}

/* text about me */
.about {
  background-color: var(--white-headline);
  padding: 0 8%;
  padding-top: 100px;
  height: 85vh;
  border: var(--dark-border);
}

.aboutMe {
  display: flex;
}

.aboutMe video {
  width: 50%;
  height: 50%;
  cursor: pointer;
}

.aboutText {
  display: flex;
  flex-direction: column;
  padding: 0 24px;
}

.aboutText h1 {
  color: var(--secondary-color);
  font-size: 50px;
  line-height: 0.7;
}

.aboutText p {
  margin-top: 12px;
  max-width: 350px;
  padding-right: 50px;
}
/* text about me end */


/* vertical specialties */
.aboutSpecialties {
  writing-mode: vertical-rl;
  display: flex;
  align-items: center;
  position: absolute;
  right: 0;
  gap: 22px;
}

.aboutSpecialties p {
  font-size: 17px;
}
/* vertical specialties end */


/* bottom part of about */
.aboutBottom {
  display: flex;
  gap: 18px;
  padding-top: 8px !important;
}

.aboutBottom p {
  padding-top: 10px !important;
}

.aboutBottom hr {
  margin-top: 5px;
  display: block;
  border-width: 0;
  height: 2px;
  width: 175px;
  background-color: var(--secondary-color);
  align-self: center;
}
/* bottom part of about end */


/* responsive */
@media only screen and (max-width: 1030px) {
  .about {
    padding-right: 30px;
  }

  .aboutBottom {
    padding-top: 18px;
  }

  .aboutBottom p {
    font-size: 15px;
  }

  .aboutBottom hr {
  max-width: 100px;
  }
}

@media only screen and (max-width: 980px) {
  .about {
    padding-top: 72.365px;
  }

  .aboutSpecialties {
    display: none;
  }
}

@media only screen and (max-width: 970px) {
  .about {
    height: 150vh;
  }

  .aboutMe {
    display: flex;
    flex-direction: column;
  }

  .aboutMe video {
    width: 80%;
    height: 80%;
    margin: 0 auto;
  }

  .aboutText {
    padding-top: 45px;
    padding-left: 10%;
  }

  .aboutText p {
    padding-right: 0;
  }

  .aboutBottom {
    padding-left: 10%;
    padding-top: 30px !important;
  }
}

@media only screen and (max-width: 850px) {
  .about {
    height: 140vh;
  }
}

@media only screen and (max-width: 700px) {
  .about {
    height: 125vh;
  }
}

@media only screen and (max-width: 600px) {
  .aboutBottom {
  gap: 12px;
  }
}

@media only screen and (max-width: 550px) {
  .aboutBottom hr {
  max-width: 50px;
  }
}

@media only screen and (max-width: 496px) {
  .aboutBottom p {
    display: none;
  }

  .aboutBottom hr {
    display: none;
  }

}

@media only screen and (max-width: 380px) {
  .aboutText h1 {
    font-size: 35px;
  }
}



/* responsive end */


</style>
