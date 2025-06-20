<template>
  <q-page 
    class="q-pa-md" 
    :class="{ 'dark-gradient-bg': $q.dark.isActive }"
  >

    <!-- Intro Section -->
    <div class="card q-pl-lg q-mb-md card-intro">
      <div class="row" style="margin-top: -110px;">
        <div class="col">
          <h4 class="q-mb-sm">Hi, I'm Dexter Jamero</h4>
          <p class="q-mt-xl">
            I'm a passionate IT student focused on mobile and web development. I love solving real-world problems through technology.
            I'm eager to learn new technologies, expand my knowledge, and make valuable contributions to your company.
          </p>
          </div>
        <div class="col disapeard"></div>
      </div>
    </div>

    <!-- About Me Section -->
    <div class="card q-pa-md card-intro">
      <div class="text-center block q-mt-lg">
        <h4 class=''>About Me</h4>
      </div>
        <div class="row">
          <div class="col disapeard">

          </div>
          <div class="col">
            <div class=" block-right-project">
              <p class="text-gray-800 ">
                My main goal is to create intuitive and scalable applications that help solve real-world problems.
                I'm always curious about how technology can improve everyday life, and I'm committed to continuous learning and growth.
              </p>
              <CvButton
                class="q-mt-lg"
                @click="cv"
              />
            </div>
          </div>
        </div>
    </div>

    <!-- Projects Section -->
    <div class="card q-pa-md q-mb-md">
      <q-card-section>
        <div class="text-center ">
          <h4 class="q-mb-sm block-left">Projects</h4>
          <p class="text-subtitle1 text-grey block-right-project">Academic Projects</p>
        </div>
        <q-separator spaced />

        <div class="q-mt-md text-center block-right-project">
        
        <Splide 
          :options="options" 
        >
          <SplideSlide 
            data-splide-hash="slide1"
          >
            <q-card class="project-card relative-position ">
              <q-card-section>
                <q-img
                  class="project-img"
                  src="src/assets/mobile.png"
                  width="400px"
                />
                <h6 class="q-mt-lg">Pet Safety Through Real-Time GPS Tracking</h6>
                <div class="text-subtitle1 text-grey" style="margin-top: -50px;">Capstone Project (2024)</div>
                <p class="q-mt-lg">
                  A mobile app using Firebase and Mapbox for real-time pet tracking, with geofencing alert features.
                </p>
              </q-card-section>
              <q-card-actions>
                <SourceCodeBtn 
                  class="project-button project-btn"
                  @click="mobile"
                />
              </q-card-actions>
            </q-card>
          </SplideSlide>
          <SplideSlide data-splide-hash="slide2">
            <q-card class="project-card relative-position">
              <q-card-section>
                <q-img
                    class="project-img"
                    src="src/assets/ecommercee.png"
                    width="400px"
                />
                <h6 style="margin-top: 33px;">E-Commerce Website</h6>
                <div class="text-subtitle1 text-grey" style="margin-top: -50px;">Semester Project (2024)</div>
                <p class="q-mt-lg">
                  A full-stack e-commerce platform using PHP, MySQL, and PayPal API for online transactions.
                </p>
              </q-card-section>
              <q-card-actions>
                <SourceCodeBtn
                  class="project-btn"
                  @click="ecommerce"
                />
              </q-card-actions>
            </q-card>
          </SplideSlide>
        </Splide>

        </div>
      </q-card-section>
    </div>

    <!-- Skills Section -->
    <div class="card q-pa-md text-center">
      <div>
        <div class="">
          <div class="text-center ">
            <h4 class="q-mb-sm block-left">
              Skills & Technologies
            </h4>
            <p class="text-subtitle1 block-right-project">
              Experience during college day
            </p>
          </div>
        </div>
        
        <q-separator spaced />

        <div 
          class="row q-mt-md q-mr-md justify-center"
        >
          <!-- Web Development -->
          <q-card class="col-xs-12 col-sm-4 q-ma-md q-pa-md skills-col block-left">
            <h6 class="text-subtitle1">Web Development</h6>
            <p class="text-subtitle1 text-left">Frontend Developer</p>
            <div class="row">       
              <div class="col skills-container">
                <div>
                  <q-img
                    src="src/assets/html.png"
                    width="50px"
                  />
                </div>
                <span>HTML</span>
              </div>
              <div class="col skills-container">
                <div>
                  <q-img
                    src="src/assets/css.png"
                    width="50px"
                  />
                </div>
                <span>CSS</span>
              </div>
              <div class="col skills-container">
                <div>
                  <q-img
                    src="src/assets/JavaScript-logo.png"
                    width="49px"
                  />
                </div>
                <span>JavaScript</span>
              </div>
            </div>   

            <div class="row q-mt-md">       
              <div class="col skills-container">
                <div>
                  <q-img
                    src="src/assets/bootstrap.png"
                    width="50px"
                  />
                </div>
                <span>Bootstrap</span>
              </div>
              <div class="col skills-container">
                <div>
                  <q-img
                    src="src/assets/Quasar_Framework.png"
                    width="50px"
                  />
                </div>
                <span>Quasar Framework</span>
              </div>
              <div class="col skills-container">
                <div>
                  <q-img
                    src="src/assets/Vuejs.png"
                    width="50px"
                  />
                </div>
                <span>Vue js</span>
              </div>
            </div>   
            <p class="text-subtitle1 text-left q-mt-md">Backend Developer</p>
            <div class="row q-mt-md">       
              <div class="col skills-container">
                <div class="q-mt-md">
                  <q-img
                    src="src/assets/ph.png"
                    width="50px"
                  />
                </div>
                <span>PHP</span>
              </div>
              <div class="col skills-container">
                <div>
                  <q-img
                    src="src/assets/laravel.png"
                    width="45px"
                  />
                </div>
                <span>laravel</span>
              </div>
              <div class="col skills-container">
                <div>
                  <q-img
                    src="src/assets/MySqL.png"
                    width="50px"
                  />
                </div>
                <span>MySQL</span>
              </div>
            </div>
          </q-card>

          <!-- Mobile Development -->
          <q-card class="col-xs-12 col-sm-4 q-ma-md q-pa-md block-center skills-col">
            <h6 class="text-subtitle1">Mobile Development</h6>
            <div class="row q-mt-md">
              <div class="col skills-container">
                <div>
                  <q-img
                    src="src/assets/Java.png"
                    width="50px"
                  />
                </div>
                <span>JAVA</span>
              </div>
              <div class="col skills-container">
                <div>
                  <q-img
                    src="src/assets/Firebases.png"
                    width="50px"
                  />
                </div>
                <span>Firebase</span>
              </div>
              <div class="col"></div>
            </div>
          </q-card>

          <!-- Others -->
          <q-card class="col-xs-12 col-sm-4 q-ma-md q-pa-md skills-col block-right ">
            <h6 class="text-subtitle1">Others</h6>
            <div class="row q-mt-md">
              <div class="col skills-container">
                <div>
                  <q-img
                    src="src/assets/git.jpg"
                    width="55px"
                  />
                </div>
                <span>Git</span>
              </div>
              <div class="col skills-container">
                <div class="q-mt-sm">
                  <q-img
                    src="src/assets/wsl.png"
                    width="65px"
                  />
                </div>
                <span>Ubuntu WSL</span>
              </div>
              <div class="col skills-container">
                <div>
                  <q-img
                    src="src/assets/Csharp_Logo.png"
                    width="55px"
                  />
                </div>
                <span>C#</span>
              </div>
            </div>
            <div class="row q-mt-md">
              <div class="col skills-container">
                <div>
                  <q-img
                    src="src/assets/Python.png"
                    width="50px"
                  />
                </div>
                <span>Python</span>
              </div>
              <div class="col skills-container">
                <div>
                  <q-img
                    src="src/assets/Postman.png"
                    width="50px"
                  />
                </div>
                <span>Postman</span>
              </div>
              <div class="col"></div>       
            </div>
          </q-card>

        </div>
      </div>
    </div>

      <!-- Education Section -->
    <div class="education card card-intro q-pa-md q-mt-md q-mb-md">
      <div class="text-center">
        <h4 class="text-center block-left">Education</h4>
        <p class="q-mt-lg block-left"><strong>Bulacan State University - Sarmiento Campus</strong></p>
        <p class="block-left">Bachelor of Science in Information Technology</p>
        <p class="block-left">Major in Web & Mobile Development</p>
        <p class="text-primary block-left">CUM LAUDE – GWA: 1.53 / 1.00</p>
        <p class="text-caption text-grey block-left">2021 – 2025</p>
        <div class="q-mt-xl">
          <p class="text-grey cursor-pointer block-left" @click="portfolio">Designed & Developed by Dexter Jamero</p>
        </div>
      
      </div>
    </div>
  </q-page>
</template>

<script setup>
import SourceCodeBtn from 'src/components/ViewSourceCode.vue'
import CvButton from 'src/components/DownloadCv.vue'
import { Splide, SplideSlide } from '@splidejs/vue-splide';
// Default theme
import '@splidejs/vue-splide/css';

const options = {
  perPage: 2,
  perMove: 1,
  height: 'auto',
  focus: 'center',
  trimSpace: false,
  breakpoints: {
    700: {
      perPage: 1,
      height: 'auto',
    },
    1024: {
      perPage: 2,
    },

    1280: {
      perPage: 3,
    },
  },
}

const mobile = async() => {
  window.open("https://github.com/phlwin722/Capstone_Project_Gps_Pet_Tracker", "_blank")
}

const ecommerce = async() => {
  window.open("https://github.com/phlwin722/Shopping-cart-oche", "_blank")
}

const cv = async() => {
  window.open("https://drive.google.com/file/d/19NEuor_RckXjE94REUKo574GLoxilgbt/view?usp=sharing", "_blank")
}

const portfolio = async() => {
  window.open("https://github.com/phlwin722/Portfolio-Project", "_blank")
}
</script>

<style scoped>
.dark-gradient-bg {
  background: linear-gradient(to right, #000000, #212627);
  min-height: 100vh;
  transition: background 0.3s ease;
  color: white;
}

p {
  font-size: 17px;
}

.skills-col {
  max-width: 350px;
  height: 520px;
}

.card {
  height: 100vh ;
}

span {
  font-size: 13px;
}

.q-card {
  border-radius: 20px;
  color: white;
  background-color: rgb(30, 34, 43);
}

.skills-container:hover { 
  transition: all 0.4s;
  cursor: pointer;
  transform: scale(1.1);
}

.skills-container {
  padding-top: 5px;
}

.card-intro {
  display:flex;
  flex-direction: column;
  justify-content: center; /* vertical center */
  align-items: flex-center; /* align left */
}

.project-card {
  height: 430px;
  margin: 50px;
}

.project-img {
  max-width: 100%;
  height: auto;
}

.project-btn {
  position: absolute;
  bottom: 30px;
  left: 50%;
  transform: translate(-50%);
}

@keyframes appear {
  from {
    opacity: 0;
    scale: 0.5;
  }
  to {
    opacity: 1;
    scale: 1;
  }
}

.block {
  animation: appear  1s ease-out both;
  animation-timeline: view();
  animation-range: entry 0% cover 40% ;
}

.block-center {
  animation: appear  1s ease-out both;
  animation-timeline: view();
  animation-range: entry 0% cover 40% ;
}

.block-left {
  animation: appearFromLeft 1s ease-out both;
  animation-timeline: view();
  animation-range: entry 0% cover 40%;
}



@keyframes appearFromLeft {
  from {
    opacity: 0;
    transform: translateX(-50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

.block-right {
  animation: appearFromRight 1s ease-out both;
  animation-timeline: view();
  animation-range: entry 0% cover 40%;
}

.block-right-project {
  animation: appearFromRight 1s ease-out both;
  animation-timeline: view();
  animation-range: entry 0% cover 40%;
}

@keyframes appearFromRight {
  from {
    opacity: 0;
    transform: translateX(50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@media (max-width: 1279px) { /* < xl */
  .project-card {
    height: 430px;
    margin: 40px;
  }

  p {
    font-size: 16px;
  }

  .block-center {
    animation: appearFromRight 1s ease-out both;
    animation-timeline: view();
    animation-range: entry 0% cover 40%;
  }

  .block-right {
    animation: appear 1s ease-out both;
    animation-timeline: view();
    animation-range: entry 0% cover 40%;
  }
}

@media (max-width: 1225px) {
  .education {
    margin-top: 290px;
  }
}

@media (max-width: 1023px) { /* < lg */
  .project-card {
    height: 460px;
    margin: 30px;
  }

  p {
    font-size: 16px;
  }

  .block-center {
    animation: appearFromRight  1s ease-out both;
    animation-timeline: view();
    animation-range: entry 0% cover 40% ;
  }

  .block-right {
    animation: appear 1s ease-out both;
    animation-timeline: view();
    animation-range: entry 0% cover 40%;
  }

}

@media (max-width: 767px) { /* < md */
  .project-card {
    height: 490px;
    margin: 20px;
  }
}

@media (max-width: 639px) { /* < sm */
  .project-card {
    height: 520px;
    margin: 10px;
  }
}

@media (max-width: 480px) {
  .project-card {
    height: 500px;
    margin: 5px;
  }

  .disapeard {
    display: none;
  }
  
  span {
    font-size: 10px;
  }

  .education {
    margin-top: 800px;
  }
  
  .project-card {
    padding: 18px;
  }

  p {
    font-size: 14px;
  }
}

</style>
y