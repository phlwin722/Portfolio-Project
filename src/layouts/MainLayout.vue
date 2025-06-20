<template>
  <q-layout view="hHh lpR fFf">
    <q-header class="header-bg">
      <q-toolbar>
        <q-toolbar-title>
          <div class="row q-pl-md q-pt-md  q-pr-md q-pb-sm">
            <div class="col-6 row items-center justify-start">
              <label class="cursor-pointer"
              @click="githubAcct">@Phlwin722</label>
            </div>
            <div class="col-6 row items-center justify-end">
              <input
                type="checkbox"
                id="darkmode-toogle"
                :checked="isDarkMode"
                @change="toggleDarkMode"
              />
              <label class="label" for="darkmode-toogle">
                <svg
                  viewBox="0 0 24 24"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                  class="sun"
                >
                  <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                  <g
                    id="SVGRepo_tracerCarrier"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  ></g>
                  <g id="SVGRepo_iconCarrier">
                    <path
                      d="M11 1C11 0.447715 11.4477 0 12 0C12.5523 0 13 0.447715 13 1V3C13 3.55228 12.5523 4 12 4C11.4477 4 11 3.55228 11 3V1Z"
                      fill="#ffffff"
                    ></path>
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M18 12C18 15.3137 15.3137 18 12 18C8.68629 18 6 15.3137 6 12C6 8.68629 8.68629 6 12 6C15.3137 6 18 8.68629 18 12ZM8.06167 12C8.06167 14.1751 9.82492 15.9383 12 15.9383C14.1751 15.9383 15.9383 14.1751 15.9383 12C15.9383 9.82492 14.1751 8.06167 12 8.06167C9.82492 8.06167 8.06167 9.82492 8.06167 12Z"
                      fill="#ffffff"
                    ></path>
                    <path
                      d="M20.4853 3.51472C20.0947 3.12419 19.4616 3.12419 19.0711 3.51472L17.6568 4.92893C17.2663 5.31946 17.2663 5.95262 17.6568 6.34315C18.0474 6.73367 18.6805 6.73367 19.0711 6.34315L20.4853 4.92893C20.8758 4.53841 20.8758 3.90524 20.4853 3.51472Z"
                      fill="#ffffff"
                    ></path>
                    <path
                      d="M1 13C0.447715 13 0 12.5523 0 12C0 11.4477 0.447715 11 1 11H3C3.55228 11 4 11.4477 4 12C4 12.5523 3.55228 13 3 13H1Z"
                      fill="#ffffff"
                    ></path>
                    <path
                      d="M3.51472 3.51472C3.1242 3.90524 3.1242 4.53841 3.51472 4.92893L4.92894 6.34315C5.31946 6.73367 5.95263 6.73367 6.34315 6.34315C6.73368 5.95262 6.73368 5.31946 6.34315 4.92893L4.92894 3.51472C4.53841 3.12419 3.90525 3.12419 3.51472 3.51472Z"
                      fill="#ffffff"
                    ></path>
                    <path
                      d="M11 21C11 20.4477 11.4477 20 12 20C12.5523 20 13 20.4477 13 21V23C13 23.5523 12.5523 24 12 24C11.4477 24 11 23.5523 11 23V21Z"
                      fill="#ffffff"
                    ></path>
                    <path
                      d="M6.34315 17.6569C5.95263 17.2663 5.31946 17.2663 4.92894 17.6569L3.51473 19.0711C3.1242 19.4616 3.1242 20.0948 3.51473 20.4853C3.90525 20.8758 4.53842 20.8758 4.92894 20.4853L6.34315 19.0711C6.73368 18.6805 6.73368 18.0474 6.34315 17.6569Z"
                      fill="#ffffff"
                    ></path>
                    <path
                      d="M21 13C20.4477 13 20 12.5523 20 12C20 11.4477 20.4477 11 21 11H23C23.5523 11 24 11.4477 24 12C24 12.5523 23.5523 13 23 13H21Z"
                      fill="#ffffff"
                    ></path>
                    <path
                      d="M17.6568 17.6569C17.2663 18.0474 17.2663 18.6805 17.6568 19.0711L19.0711 20.4853C19.4616 20.8758 20.0947 20.8758 20.4853 20.4853C20.8758 20.0948 20.8758 19.4616 20.4853 19.0711L19.0711 17.6569C18.6805 17.2663 18.0474 17.2663 17.6568 17.6569Z"
                      fill="#ffffff"
                    ></path>
                  </g>
                </svg>
                
                <svg
                  viewBox="0 0 24 24"
                  class="moon"
                  version="1.1"
                  xmlns="http://www.w3.org/2000/svg"
                  xmlns:xlink="http://www.w3.org/1999/xlink"
                  fill="#000000"
                >
                  <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                  <g
                    id="SVGRepo_tracerCarrier"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  ></g>
                  <g id="SVGRepo_iconCarrier">
                    <title>moon_stars_line</title>
                    <g
                      id="页面-1"
                      stroke="none"
                      stroke-width="1"
                      fill="none"
                      fill-rule="evenodd"
                    >
                      <g
                        id="Weather"
                        transform="translate(-528.000000, 0.000000)"
                      >
                        <g
                          id="moon_stars_line"
                          transform="translate(528.000000, 0.000000)"
                        >
                          <path
                            d="M24,0 L24,24 L0,24 L0,0 L24,0 Z M12.5934901,23.257841 L12.5819402,23.2595131 L12.5108777,23.2950439 L12.4918791,23.2987469 L12.4918791,23.2987469 L12.4767152,23.2950439 L12.4056548,23.2595131 C12.3958229,23.2563662 12.3870493,23.2590235 12.3821421,23.2649074 L12.3780323,23.275831 L12.360941,23.7031097 L12.3658947,23.7234994 L12.3769048,23.7357139 L12.4804777,23.8096931 L12.4953491,23.8136134 L12.4953491,23.8136134 L12.5071152,23.8096931 L12.6106902,23.7357139 L12.6232938,23.7196733 L12.6232938,23.7196733 L12.6266527,23.7031097 L12.609561,23.275831 C12.6075724,23.2657013 12.6010112,23.2592993 12.5934901,23.257841 L12.5934901,23.257841 Z M12.8583906,23.1452862 L12.8445485,23.1473072 L12.6598443,23.2396597 L12.6498822,23.2499052 L12.6498822,23.2499052 L12.6471943,23.2611114 L12.6650943,23.6906389 L12.6699349,23.7034178 L12.6699349,23.7034178 L12.678386,23.7104931 L12.8793402,23.8032389 C12.8914285,23.8068999 12.9022333,23.8029875 12.9078286,23.7952264 L12.9118235,23.7811639 L12.8776777,23.1665331 C12.8752882,23.1545897 12.8674102,23.1470016 12.8583906,23.1452862 L12.8583906,23.1452862 Z M12.1430473,23.1473072 C12.1332178,23.1423925 12.1221763,23.1452606 12.1156365,23.1525954 L12.1099173,23.1665331 L12.0757714,23.7811639 C12.0751323,23.7926639 12.0828099,23.8018602 12.0926481,23.8045676 L12.108256,23.8032389 L12.3092106,23.7104931 L12.3186497,23.7024347 L12.3186497,23.7024347 L12.3225043,23.6906389 L12.340401,23.2611114 L12.337245,23.2485176 L12.337245,23.2485176 L12.3277531,23.2396597 L12.1430473,23.1473072 Z"
                            id="MingCute"
                            fill-rule="nonzero"
                          ></path>
                          <path
                            d="M12.4769,4.54573 C12.1415,3.79872 12.7837,2.99796 13.5739,3.13745 C17.7941,3.88241 21,7.56587 21,12.0001 C21,16.9707 16.9705,21.0001 12,21.0001 C7.5657,21.0001 3.88225,17.7943 3.13729,13.5741 C2.99778,12.7838 3.79861,12.1417 4.54557,12.4771 C5.29352,12.8128 6.12352,13.0001 6.99996,13.0001 C10.3137,13.0001 13,10.3138 13,7.00012 C13,6.12369 12.8127,5.29368 12.4769,4.54573 Z M14.8809,5.61825 C14.9592,6.06746 15,6.52925 15,7.00012 C15,11.4184 11.4182,15.0001 6.99996,15.0001 C6.52909,15.0001 6.0673,14.9593 5.61809,14.8811 C6.71634,17.31 9.16146,19.0001 12,19.0001 C15.8659,19.0001 19,15.8661 19,12.0001 C19,9.16162 17.3098,6.7165 14.8809,5.61825 Z M5.56482,7.71573 L5.62857,7.85506 L5.62857,7.85506 C5.90134,8.41936 6.33105,8.89305 6.86601,9.21934 L6.96534,9.27755 C7.0115,9.30351 7.0115,9.36997 6.96534,9.39593 L6.86601,9.45414 C6.33105,9.78043 5.90134,10.2541 5.62857,10.8184 L5.56482,10.9577 L5.56482,10.9577 C5.53984,11.0139 5.46007,11.0139 5.4351,10.9577 L5.37134,10.8184 L5.37134,10.8184 C5.09857,10.2541 4.66887,9.78043 4.13391,9.45414 L4.03457,9.39593 L4.03457,9.39593 C3.98842,9.36997 3.98842,9.30351 4.03457,9.27755 L4.13391,9.21934 L4.13391,9.21934 C4.66887,8.89305 5.09857,8.41936 5.37134,7.85506 L5.4351,7.71573 L5.4351,7.71573 C5.46007,7.65953 5.53984,7.65953 5.56482,7.71573 Z M8.39662,2.85738 C8.43638,2.76792 8.56335,2.76792 8.6031,2.85738 L8.70458,3.07914 L8.70458,3.07914 C9.13876,3.97736 9.82274,4.73135 10.6743,5.25072 L10.8324,5.34337 L10.8324,5.34337 C10.9058,5.38469 10.9058,5.49048 10.8324,5.5318 L10.6743,5.62445 L10.6743,5.62445 C9.82274,6.14382 9.13876,6.89781 8.70458,7.79603 C8.66919,7.86924 8.63613,7.94349 8.6031,8.0178 C8.56335,8.10725 8.43638,8.10725 8.39662,8.0178 L8.29515,7.79603 L8.29515,7.79603 C7.86097,6.89781 7.17699,6.14382 6.32548,5.62445 L6.16736,5.5318 L6.16736,5.5318 C6.09389,5.49048 6.09389,5.38469 6.16736,5.34337 L6.32548,5.25072 L6.32548,5.25072 C7.17699,4.73135 7.86097,3.97736 8.29515,3.07914 L8.39662,2.85738 L8.39662,2.85738 Z"
                            id="形状"
                            fill="#0F0F0F"
                          ></path>
                        </g>
                      </g>
                    </g>
                  </g>
                </svg>
              </label>
            </div>
          </div>
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref, watch } from "vue";
import { useQuasar } from "quasar";

const $q = useQuasar();
const isDarkMode = ref($q.dark.isActive);

// Function to toggle dark mode
const toggleDarkMode = () => {
  $q.dark.set(!isDarkMode.value);
  isDarkMode.value = $q.dark.isActive;
};

watch(isDarkMode, (enabled) => {
  document.body.classList.toggle("dark-mode", enabled);
  
  console.log("Dark mode enabled:", enabled);
});

const githubAcct = async() => {
  window.open('https://github.com/phlwin722', '_blank' )
}

</script>

<style scoped>
* {
  font-family: "Lexend Deca", sans-serif;
}

.label {
  width: 70px;
  height: 35px;
  background: #ebebeb;
  display: block;
  border-radius: 200px;
  position: relative;
  cursor: pointer;
  box-shadow: inset 0px 5px 15px rgba(0, 0, 0, 0.4),
    inset 0px -5px 15px rgba(255, 255, 255, 0.4);
  transition: 0.3s;
}

.label:after {
  content: "";
  width: 25px;
  height: 25px;
  position: absolute;
  top: 5px;
  left: 5px;
  background: linear-gradient(180deg, #ffcc89, #d8860b);
  border-radius: 50%;
  box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.2);
  transition: 0.3s;
}

input {
  width: 0;
  height: 0;
  visibility: hidden;
}

input:checked + .label {
  background-color: #242424;
}

input:checked + .label:after {
  left: 65px;
  transform: translateX(-100%);
  background: linear-gradient(180deg, #777, #3a3a3a);
}

.label:active:after {
  width: 33px;
}

.label svg {
  position: absolute;
  width: 18px;
  z-index: 100px;
  top: 8px;
}

.label svg.sun {
  left: 10px;
  fill: #fff;
  transition: 0.3s;
}

.label svg.moon {
  left: 42px;
  fill: #7e7e7e;
  transition: 0.3s;
}

input:checked + .label svg.sun {
  fill: #7e7e7e;
}

input:checked + .label svg.sun {
  fill: #fff;
}

/* Header styles */
.header-bg {
  background: #fff;
  transition: 0.3s;
  color: black;
}

/* Dark mode styles applied to body */
body.dark-mode .header-bg {  
  color: white;
  background: linear-gradient(to right, #000000, #212627);
}

.q-toolbar{
  margin: 0;
  padding: 0;
}


</style>
