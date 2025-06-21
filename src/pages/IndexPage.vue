<template>
  <q-page class="q-pa-md q-pl-xl q-pr-xl" :class="{ 'dark-gradient-bg': $q.dark.isActive }">
    <!-- Intro Section -->
    <div class="q-mb-md card-intro" style="height: 75vh">
      <div class="row">
        <div class="col">
          <h4 class="q-mb-sm">Hi, I'm Dexter Jamero</h4>
          <p class="q-mt-xl">
            I'm a passionate IT Graduate focused on mobile and web development.
            I love solving real-world problems through technology. I'm eager to
            learn new technologies, expand my knowledge, and make valuable
            contributions to your company.
          </p>
        </div>
        <div class="col disapeard"></div>
      </div>
    </div>

    <!-- About Me Section -->
    <div class="card q-pa-md card-intro">
      <div class="text-center block q-mt-lg">
        <h4 class="">About Me</h4>
      </div>
      <div class="row">
        <div class="col disapeard"></div>
        <div class="col">
          <div class="block-right-project">
            <p class="text-gray-800">
              My main goal is to create intuitive and scalable applications that
              help solve real-world problems. I'm always curious about how
              technology can improve everyday life, and I'm committed to
              continuous learning and growth.
            </p>
            <CvButton class="q-mt-lg" @click="cv" />
          </div>
        </div>
      </div>
    </div>

    <!-- Projects Section -->
    <div class="card q-pa-md q-mb-md">
      <div class="text-center">
        <h4 class="q-mb-sm block-left">Projects</h4>
        <p class="text-subtitle1 block-right-project">Academic Projects</p>
      </div>
      <q-separator spaced />

      <div class="q-mt-md text-center block-right-project">
        <Splide :options="options">
          <SplideSlide data-splide-hash="slide1">
            <q-card class="project-card relative-position">
              <q-card-section>
                <img class="project-img" width="400px" src="/mobile.png" />

                <h6 class="q-mt-lg">
                  Pet Safety Through Real-Time GPS Tracking
                </h6>
                <div class="text-subtitle1 text-grey" style="margin-top: -50px">
                  Capstone Project (2024)
                </div>
                <p class="q-mt-lg">
                  Designed and developed a real-time multi-pet tracking mobile
                  app using Firebase for GPS data and Mapbox for interactive map
                  visualization. Included geofencing alerts when pets exit
                  user-defined safe zones, enhancing safety and user awareness.
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
                <img class="project-img" width="400px" src="/ecommercee.png" />
                <h6 style="margin-top: 33px">E-Commerce Website</h6>
                <div class="text-subtitle1 text-grey" style="margin-top: -50px">
                  Semester Project (2024)
                </div>
                <p class="q-mt-lg">
                  A scalable shopping cart solution for an eCommerce platform,
                  incorporating dynamic product displays, real-time inventory
                  control, streamlined order processing, and integration with
                  payment gateways.
                </p>
              </q-card-section>
              <q-card-actions>
                <SourceCodeBtn class="project-btn" @click="ecommerce" />
              </q-card-actions>
            </q-card>
          </SplideSlide>
          <SplideSlide data-splide-hash="slide2">
            <q-card class="project-card relative-position">
              <q-card-section>
                <img
                  class="project-img"
                  width="100px"
                  height="100px"
                  src="/multi-business.png"
                />
                <h6 style="margin-top: 30px">Multi Business System</h6>
                <div class="text-subtitle1 text-grey" style="margin-top: -50px">
                  Semester Project (2023)
                </div>
                <p class="q-mt-lg project-info">
                  Developed a centralized sales monitoring system that enables
                  business owners to track all transactions through a single
                  account. The system enhances operational oversight by
                  providing real-time visibility into sales performance,
                  improving decision-making and efficiency.
                </p>
              </q-card-section>
              <q-card-actions>
                <SourceCodeBtn class="project-btn" @click="multi_business" />
              </q-card-actions>
            </q-card>
          </SplideSlide>
        </Splide>
      </div>
    </div>

    <!-- Skills Section -->
    <div class="card q-pa-md text-center">
      <div class="text-center">
        <h4 class="q-mb-sm block-left">Skills & Technologies</h4>
        <p class="text-subtitle1 block-right-project">
          Experience during college day
        </p>
      </div>

      <q-separator spaced />

      <div class="row q-mt-md q-mr-md justify-center">
        <!-- Web Development -->
        <q-card
          class="col-xs-12 col-sm-4 q-ma-md q-pa-md skills-col block-left"
        >
          <div class="flex justify-center">
            <svg
              class="svg q-mr-sm"
              fill="#fff"
              version="1.1"
              id="Capa_1"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink"
              viewBox="0 0 419.931 419.931"
              xml:space="preserve"
            >
              <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
              <g
                id="SVGRepo_tracerCarrier"
                stroke-linecap="round"
                stroke-linejoin="round"
              ></g>
              <g id="SVGRepo_iconCarrier">
                <g>
                  <g>
                    <g>
                      <path
                        d="M282.895,352.367c-2.176-1.324-4.072-3.099-5.579-5.25c-0.696-0.992-1.284-2.041-1.771-3.125H28.282V100.276h335.624 v159.138c7.165,0.647,13.177,5.353,15.701,11.797c2.235-1.225,4.726-1.982,7.344-2.213c1.771-0.154,3.53-0.044,5.236,0.293 V39.561c0-12.996-10.571-23.569-23.566-23.569H23.568C10.573,15.992,0,26.565,0,39.561v309.146 c0,12.996,10.573,23.568,23.568,23.568h257.179c-2.007-4.064-2.483-8.652-1.302-13.066 C280.126,356.67,281.304,354.354,282.895,352.367z M338.025,55.569c0-4.806,3.896-8.703,8.702-8.703h8.702 c4.807,0,8.702,3.896,8.702,8.703v9.863c0,4.806-3.896,8.702-8.702,8.702h-8.702c-4.807,0-8.702-3.896-8.702-8.702V55.569z M297.56,55.569c0-4.806,3.896-8.703,8.702-8.703h8.703c4.807,0,8.702,3.896,8.702,8.703v9.863c0,4.806-3.896,8.702-8.702,8.702 h-8.703c-4.806,0-8.702-3.896-8.702-8.702V55.569z M257.094,55.569c0-4.806,3.897-8.703,8.702-8.703h8.702 c4.807,0,8.703,3.896,8.703,8.703v9.863c0,4.806-3.896,8.702-8.703,8.702h-8.702c-4.805,0-8.702-3.896-8.702-8.702V55.569z"
                      ></path>
                      <path
                        d="M419.875,335.77l-2.615-14.83c-0.353-1.997-2.256-3.331-4.255-2.979l-13.188,2.324c-1.583-3.715-3.605-7.195-6.005-10.38 l8.614-10.268c0.626-0.744,0.931-1.709,0.847-2.68c-0.086-0.971-0.554-1.867-1.3-2.494l-11.534-9.68 c-0.746-0.626-1.713-0.93-2.683-0.845c-0.971,0.085-1.867,0.552-2.493,1.298l-8.606,10.26c-3.533-1.8-7.312-3.188-11.271-4.104 v-13.392c0-2.028-1.645-3.674-3.673-3.674h-15.06c-2.027,0-3.673,1.646-3.673,3.674v13.392 c-3.961,0.915-7.736,2.304-11.271,4.104l-8.608-10.259c-1.304-1.554-3.62-1.756-5.175-0.453l-11.535,9.679 c-0.746,0.627-1.213,1.523-1.299,2.494c-0.084,0.971,0.22,1.937,0.846,2.683l8.615,10.266c-2.396,3.184-4.422,6.666-6.005,10.38 l-13.188-2.325c-1.994-0.351-3.901,0.982-4.255,2.979l-2.614,14.83c-0.169,0.959,0.05,1.945,0.607,2.744 c0.561,0.799,1.41,1.342,2.37,1.511l13.198,2.326c0.215,4.089,0.927,8.045,2.073,11.812l-11.6,6.695 c-0.844,0.485-1.459,1.289-1.712,2.229c-0.252,0.941-0.119,1.943,0.367,2.787l7.529,13.041c0.485,0.844,1.289,1.459,2.229,1.711 c0.313,0.084,0.632,0.125,0.951,0.125c0.639,0,1.272-0.166,1.836-0.492l11.609-6.703c2.73,2.925,5.812,5.517,9.18,7.709 l-4.584,12.593c-0.332,0.916-0.289,1.926,0.123,2.809s1.157,1.566,2.072,1.898l14.148,5.149c0.406,0.148,0.832,0.224,1.257,0.224 c0.53,0,1.063-0.115,1.554-0.345c0.883-0.411,1.564-1.157,1.897-2.073l4.583-12.593c1.965,0.238,3.965,0.361,5.994,0.361 s4.029-0.125,5.994-0.361l4.584,12.593c0.332,0.916,1.016,1.662,1.897,2.073c0.49,0.229,1.021,0.345,1.554,0.345 c0.424,0,0.85-0.074,1.256-0.224l14.15-5.149c0.913-0.332,1.659-1.017,2.07-1.898c0.412-0.883,0.456-1.893,0.123-2.809 l-4.584-12.591c3.365-2.192,6.447-4.786,9.18-7.709l11.609,6.703c0.563,0.324,1.197,0.492,1.836,0.492 c0.318,0,0.64-0.043,0.951-0.125c0.941-0.252,1.743-0.869,2.229-1.711l7.529-13.043c0.486-0.842,0.619-1.846,0.367-2.787 c-0.253-0.938-0.868-1.742-1.712-2.229l-11.598-6.693c1.146-3.768,1.856-7.724,2.071-11.812l13.198-2.327 c0.96-0.169,1.812-0.712,2.37-1.511C419.825,337.715,420.044,336.729,419.875,335.77z M354.184,359.336 c-11.155,0-20.2-9.045-20.2-20.201s9.046-20.2,20.2-20.2c11.156,0,20.201,9.044,20.201,20.2S365.34,359.336,354.184,359.336z"
                      ></path>
                      <g>
                        <path
                          d="M164.695,235.373c0-4.752-2.785-9.117-7.096-11.119l-39.455-18.332l39.456-18.334c4.31-2.004,7.095-6.368,7.095-11.118 v-0.319c0-4.21-2.119-8.075-5.665-10.334c-1.962-1.253-4.247-1.916-6.606-1.916c-1.778,0-3.563,0.391-5.16,1.133l-63.078,29.333 c-4.309,2.004-7.092,6.368-7.092,11.117v0.877c0,4.743,2.782,9.104,7.093,11.118l63.084,29.336 c1.631,0.755,3.368,1.138,5.162,1.138c2.338,0,4.616-0.664,6.597-1.924c3.548-2.268,5.666-6.13,5.666-10.335L164.695,235.373 L164.695,235.373z"
                        ></path>
                        <path
                          d="M226.932,134.012c-2.301-3.15-6.002-5.03-9.901-5.03h-0.314c-5.354,0-10.048,3.425-11.679,8.516L163.478,266.27 c-1.183,3.718-0.517,7.813,1.781,10.962c2.301,3.148,6.002,5.029,9.901,5.029h0.315c5.352,0,10.043-3.426,11.672-8.516 l41.555-128.762C229.896,141.268,229.234,137.167,226.932,134.012z"
                        ></path>
                        <path
                          d="M308.001,194.366l-63.079-29.333c-1.592-0.74-3.374-1.131-5.152-1.131c-2.358,0-4.644,0.661-6.605,1.912 c-3.552,2.263-5.671,6.127-5.671,10.337v0.319c0,4.746,2.783,9.111,7.097,11.123l39.454,18.33l-39.455,18.331 c-4.311,2.002-7.096,6.367-7.096,11.119v0.321c0,4.205,2.119,8.066,5.669,10.336c1.974,1.258,4.254,1.923,6.595,1.923 c1.792,0,3.527-0.383,5.169-1.141l63.082-29.336c4.307-2.009,7.088-6.371,7.088-11.114v-0.877 C315.094,200.735,312.311,196.371,308.001,194.366z"
                        ></path>
                      </g>
                    </g>
                  </g>
                </g>
              </g>
            </svg>
            <h6 class="text-subtitle1">Web Development</h6>
          </div>
          <p class="text-subtitle1 text-left">Frontend Developer</p>
          <div class="row">
            <div class="col skills-container">
              <div>
                <img width="50px" src="/html.png" />
              </div>
              <span>HTML</span>
            </div>
            <div class="col skills-container">
              <div>
                <img width="50px" src="/css.png" />
              </div>
              <span>CSS</span>
            </div>
            <div class="col skills-container">
              <div>
                <img width="47px" src="/JavaScript-logo.png" />
              </div>
              <span>JavaScript</span>
            </div>
          </div>

          <div class="row q-mt-md">
            <div class="col skills-container">
              <div>
                <img width="50px" src="/bootstrap.png" />
              </div>
              <span>Bootstrap</span>
            </div>
            <div class="col skills-container">
              <div>
                <img width="50px" src="/Quasar_Framework.png" />
              </div>
              <span>Quasar Framework</span>
            </div>
            <div class="col skills-container">
              <div>
                <img width="50px" src="/Vuejs.png" />
              </div>
              <span>Vue js</span>
            </div>
          </div>
          <p class="text-subtitle1 text-left q-mt-md">Backend Developer</p>
          <div class="row q-mt-md">
            <div class="col skills-container">
              <div class="q-mt-md">
                <img width="50px" src="/ph.png" />
              </div>
              <span>PHP</span>
            </div>
            <div class="col skills-container">
              <div>
                <img width="50px" src="/laravel.png" />
              </div>
              <span>laravel</span>
            </div>
            <div class="col skills-container">
              <div>
                <img width="50px" src="/MySqL.png" />
              </div>
              <span>MySQL</span>
            </div>
          </div>
        </q-card>

        <!-- Mobile Development -->
        <q-card
          class="col-xs-12 col-sm-4 q-ma-md q-pa-md block-center skills-col"
        >
          <div class="flex justify-center">
            <svg
              class="svg q-mr-sm"
              version="1.1"
              id="Icons"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink"
              viewBox="0 0 32 32"
              xml:space="preserve"
              fill="none"
            >
              <g id="SVGRepo_iconCarrier">
                <path
                  d="M19,23v4c0,1.1-0.9,2-2,2H7c-1.1,0-2-0.9-2-2V5c0-1.1,0.9-2,2-2h10c1.1,0,2,0.9,2,2v2"
                  style="
                    fill: none;
                    stroke: #ffffff;
                    stroke-width: 2;
                    stroke-linecap: round;
                    stroke-linejoin: round;
                    stroke-miterlimit: 10;
                  "
                />
                <line
                  x1="5"
                  y1="7"
                  x2="19"
                  y2="7"
                  style="
                    stroke: #ffffff;
                    stroke-width: 2;
                    stroke-linecap: round;
                    stroke-linejoin: round;
                    stroke-miterlimit: 10;
                  "
                />
                <line
                  x1="5"
                  y1="23"
                  x2="19"
                  y2="23"
                  style="
                    stroke: #ffffff;
                    stroke-width: 2;
                    stroke-linecap: round;
                    stroke-linejoin: round;
                    stroke-miterlimit: 10;
                  "
                />
                <line
                  x1="11"
                  y1="26"
                  x2="13"
                  y2="26"
                  style="
                    stroke: #ffffff;
                    stroke-width: 2;
                    stroke-linecap: round;
                    stroke-linejoin: round;
                    stroke-miterlimit: 10;
                  "
                />
                <polyline
                  points="14,12 11,15 14,18"
                  style="
                    fill: none;
                    stroke: #ffffff;
                    stroke-width: 2;
                    stroke-linecap: round;
                    stroke-linejoin: round;
                    stroke-miterlimit: 10;
                  "
                />
                <polyline
                  points="24,12 27,15 24,18"
                  style="
                    fill: none;
                    stroke: #ffffff;
                    stroke-width: 2;
                    stroke-linecap: round;
                    stroke-linejoin: round;
                    stroke-miterlimit: 10;
                  "
                />
                <line
                  x1="21"
                  y1="11"
                  x2="17"
                  y2="19"
                  style="
                    stroke: #ffffff;
                    stroke-width: 2;
                    stroke-linecap: round;
                    stroke-linejoin: round;
                    stroke-miterlimit: 10;
                  "
                />
              </g>
            </svg>

            <h6 class="text-subtitle1">Mobile Development</h6>
          </div>
          <div class="row q-mt-md">
            <div class="col skills-container">
              <div>
                <img width="50px" src="/Java.png" />
              </div>
              <span>JAVA</span>
            </div>
            <div class="col skills-container">
              <div>
                <img width="50px" src="/Firebases.png" />
              </div>
              <span>Firebase</span>
            </div>
            <div class="col"></div>
          </div>
        </q-card>

        <!-- Others -->
        <q-card
          class="col-xs-12 col-sm-4 q-ma-md q-pa-md skills-col block-right"
        >
          <div class="flex justify-center">
            <svg
              class="svg q-mr-sm"
              viewBox="0 0 24 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
              <g
                id="SVGRepo_tracerCarrier"
                stroke-linecap="round"
                stroke-linejoin="round"
              ></g>
              <g id="SVGRepo_iconCarrier">
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M11.7086 1.53214C10.9786 1.05676 10.078 0.917375 9.27255 1.04467C8.46803 1.17183 7.62325 1.5904 7.12591 2.39445C6.9332 2.70601 6.81024 3.04646 6.7559 3.40767C5.97312 3.35525 5.18086 3.59264 4.58547 4.08919C3.98255 4.59201 3.59741 5.34432 3.59741 6.25684C3.59741 6.55614 3.63851 6.86315 3.72008 7.17654C3.42298 7.23942 3.13697 7.34918 2.86932 7.50027C1.98542 7.99927 1.36438 8.90663 1.11913 9.88841C0.869371 10.8882 0.989124 12.0467 1.70052 13.0391C2.0609 13.5419 2.54903 13.9691 3.1623 14.305C3.01053 14.5081 2.88229 14.7271 2.77811 14.9565C2.35249 15.8935 2.32044 17.0038 2.64559 17.98C2.97535 18.9701 3.69756 19.8871 4.83624 20.3254C5.57833 20.6111 6.42615 20.6665 7.35551 20.4749C7.39798 20.9494 7.52745 21.3806 7.74983 21.7577C8.22598 22.5651 9.0236 22.9458 9.80541 22.9947C10.5523 23.0414 11.3758 22.778 12 22.2458C12.6242 22.778 13.4477 23.0414 14.1946 22.9947C14.9764 22.9458 15.774 22.5651 16.2502 21.7577C16.4725 21.3806 16.602 20.9494 16.6445 20.4749C17.5738 20.6665 18.4217 20.6111 19.1638 20.3254C20.3024 19.8871 21.0246 18.9701 21.3544 17.98C21.6796 17.0038 21.6475 15.8935 21.2219 14.9565C21.1177 14.7271 20.9895 14.5081 20.8377 14.305C21.451 13.9691 21.9391 13.5419 22.2995 13.0391C23.0109 12.0467 23.1306 10.8882 22.8809 9.88841C22.6356 8.90663 22.0146 7.99927 21.1307 7.50027C20.863 7.34918 20.577 7.23942 20.2799 7.17654C20.3615 6.86315 20.4026 6.55614 20.4026 6.25684C20.4026 5.34432 20.0175 4.59201 19.4145 4.08919C18.8191 3.59264 18.0269 3.35525 17.2441 3.40767C17.1898 3.04646 17.0668 2.70601 16.8741 2.39445C16.3767 1.5904 15.532 1.17183 14.7274 1.04467C13.922 0.917375 13.0214 1.05676 12.2914 1.53214C11.9861 1.73097 12.0139 1.73097 11.7086 1.53214ZM13.0033 20.0518L13.0033 17.5288C13.0045 17.0494 13.1133 16.3457 13.3939 15.7998C13.6573 15.2872 13.9946 15.0268 14.5082 15.0268C15.0623 15.0268 15.5115 14.5773 15.5115 14.0227C15.5115 13.4682 15.0623 13.0186 14.5082 13.0186C13.9202 13.0186 13.4216 13.16 13.0033 13.3894V12.5084C13.0045 12.029 13.1133 11.3254 13.3939 10.7794C13.6573 10.2668 13.9946 10.0064 14.5082 10.0064C15.0623 10.0064 15.5115 9.55688 15.5115 9.00234C15.5115 8.4478 15.0623 7.99826 14.5082 7.99826C13.9202 7.99826 13.4216 8.13957 13.0033 8.36902L13.0033 3.97532C13.005 3.57853 13.1671 3.35779 13.3859 3.21528C13.6436 3.04746 14.0284 2.96723 14.4144 3.02824C14.8013 3.08939 15.0539 3.26704 15.1679 3.45142C15.2603 3.60078 15.3726 3.9329 15.091 4.59054C14.9015 5.03294 15.0524 5.54766 15.4507 5.8175C15.849 6.08734 16.3825 6.03639 16.7226 5.69604C17.0903 5.32811 17.7563 5.32032 18.1299 5.63189C18.2795 5.75662 18.396 5.94564 18.396 6.25684C18.396 6.59422 18.2548 7.14633 17.705 7.91672C17.4235 8.31116 17.4637 8.85055 17.8006 9.19878C18.1375 9.54701 18.6749 9.60465 19.0779 9.33577C19.5101 9.04741 19.8566 9.08664 20.1448 9.24934C20.4837 9.44063 20.8032 9.85112 20.9342 10.3755C21.0607 10.8818 20.9923 11.4176 20.669 11.8686C20.3466 12.3184 19.6765 12.8121 18.3565 13.0323C17.8683 13.1137 17.5124 13.5392 17.5182 14.0344C17.5239 14.5296 17.8896 14.9467 18.3795 15.0167C18.8812 15.0884 19.207 15.3732 19.3952 15.7874C19.5966 16.231 19.6273 16.8151 19.4508 17.345C19.2789 17.861 18.9351 18.2619 18.4434 18.4511C17.9498 18.6411 17.1399 18.6809 15.9267 18.129C15.5761 17.9695 15.1653 18.025 14.8694 18.2716C14.5735 18.5183 14.4448 18.9127 14.5382 19.2866C14.6621 19.7827 14.8668 20.9406 14.0694 20.9905C13.5184 21.0249 13.0062 20.6055 13.0033 20.0518ZM10.9967 3.97532C10.995 3.57853 10.8329 3.35779 10.6141 3.21528C10.3564 3.04746 9.97157 2.96723 9.58558 3.02824C9.19869 3.08939 8.94611 3.26704 8.83207 3.45142C8.73968 3.60078 8.62739 3.9329 8.90901 4.59054C9.09846 5.03294 8.94757 5.54766 8.54931 5.8175C8.15105 6.08734 7.61747 6.03639 7.27739 5.69604C6.90975 5.32811 6.24365 5.32032 5.87006 5.63189C5.72051 5.75662 5.604 5.94564 5.604 6.25684C5.604 6.59422 5.74515 7.14633 6.29501 7.91672C6.57653 8.31116 6.53629 8.85055 6.19937 9.19878C5.86246 9.54701 5.32505 9.60465 4.92206 9.33577C4.48987 9.04741 4.1434 9.08664 3.8552 9.24934C3.51634 9.44063 3.19679 9.85112 3.06581 10.3755C2.93933 10.8818 3.0077 11.4176 3.33095 11.8686C3.65342 12.3184 4.32349 12.8121 5.64353 13.0323C6.13166 13.1137 6.48757 13.5392 6.48182 14.0344C6.47607 14.5296 6.11037 14.9467 5.62048 15.0167C5.1188 15.0884 4.793 15.3732 4.60484 15.7874C4.40339 16.231 4.37273 16.8151 4.54922 17.345C4.7211 17.861 5.06489 18.2619 5.55656 18.4511C6.05021 18.6411 6.86015 18.6809 8.0733 18.129C8.42388 17.9695 8.83474 18.025 9.13063 18.2716C9.42652 18.5183 9.5552 18.9127 9.4618 19.2866C9.33788 19.7827 9.13324 20.9406 9.93058 20.9905C10.4816 21.0249 10.9938 20.6055 10.9967 20.0518L10.9967 20.0472V17.5292C10.9955 17.0498 10.8868 16.3459 10.6061 15.7998C10.3427 15.2872 10.0054 15.0268 9.49176 15.0268C8.93765 15.0268 8.48846 14.5773 8.48846 14.0227C8.48846 13.4682 8.93765 13.0186 9.49176 13.0186C10.0798 13.0186 10.5784 13.16 10.9967 13.3894V12.5088C10.9955 12.0294 10.8868 11.3255 10.6061 10.7794C10.3427 10.2668 10.0054 10.0064 9.49176 10.0064C8.93765 10.0064 8.48846 9.55688 8.48846 9.00234C8.48846 8.4478 8.93765 7.99826 9.49176 7.99826C10.0798 7.99826 10.5784 8.13957 10.9967 8.36902L10.9967 3.97532Z"
                  fill="#ffffff"
                ></path>
              </g>
            </svg>
            <h6 class="text-subtitle1">Others</h6>
          </div>
          <div class="row q-mt-md">
            <div class="col skills-container">
              <div>
                <img width="55" src="/git.jpg" />
              </div>
              <span>Git</span>
            </div>
            <div class="col skills-container">
              <div class="q-mt-xs q-mb-xs">
                <img width="65" src="/wsl.png" />
              </div>
              <span>Ubuntu WSL</span>
            </div>
            <div class="col skills-container">
              <div>
                <img width="55" src="/Csharp_Logo.png" />
              </div>
              <span>C#</span>
            </div>
          </div>
          <div class="row q-mt-md">
            <div class="col skills-container">
              <div>
                <img width="55" src="/Python.png" />
              </div>
              <span>Python</span>
            </div>
            <div class="col skills-container">
              <div>
                <img width="55" src="/Postman.png" />
              </div>
              <span>Postman</span>
            </div>
            <div class="col"></div>
          </div>
        </q-card>
      </div>
    </div>

    <!-- Education Section -->
    <div class="education card card-intro q-pa-md q-mt-md q-mb-md">
      <div class="text-center">
        <h4 class="text-center block-left">Education</h4>
        <p class="q-mt-lg block-left">
          <strong>Bulacan State University - Sarmiento Campus</strong>
        </p>
        <p class="block-left">Bachelor of Science in Information Technology</p>
        <p class="block-left">Major in Web & Mobile Development</p>
        <p class="text-primary block-left">CUM LAUDE – GWA: 1.53 / 1.00</p>
        <p class="text-caption text-grey block-left">2021 – 2025</p>
        <div class="q-mt-xl">
          <p class="text-grey cursor-pointer block-left" @click="portfolio">
            Designed & Developed by Dexter Jamero
          </p>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script setup>
import SourceCodeBtn from "src/components/ViewSourceCode.vue";
import CvButton from "src/components/DownloadCv.vue";
import { Splide, SplideSlide } from "@splidejs/vue-splide";
// Default theme
import "@splidejs/vue-splide/css";

const options = {
  perPage: 2,
  perMove: 1,
  height: "auto",
  focus: "center",
  trimSpace: false,
  breakpoints: {
    767: {
      perPage: 1,
      height: "auto",
    },
    768: {
      perPage: 2,
      height: "auto",
    },
  },
};

const mobile = async () => {
  window.open(
    "https://github.com/phlwin722/Capstone_Project_Gps_Pet_Tracker",
    "_blank"
  );
};

const ecommerce = async () => {
  window.open("https://github.com/phlwin722/shopping_cart_system", "_blank");
};

const multi_business = async () => {
  window.open("https://github.com/phlwin722/Multi_business_system", "_blank");
};

const cv = async () => {
  window.open(
    "https://drive.google.com/file/d/17FwUZamf46SrzlSTcM4RcN0vV6P1e0CC/view?usp=sharing",
    "_blank"
  );
};

const portfolio = async () => {
  window.open("https://github.com/phlwin722/Portfolio-Project", "_blank");
};
</script>

<style scoped>
.dark-gradient-bg {
  background: linear-gradient(to right, #000000, #212627);
  min-height: 100vh;
  transition: background 0.3s ease;
  color: white;
}

p {
  font-size: 15px;
}

.skills-col {
  max-width: 350px;
  height: 540px;
}

.card {
  min-height: 100vh;
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
  display: flex;
  flex-direction: column;
  justify-content: center; /* vertical center */
  align-items: flex-center; /* align left */
}

.project-card {
  height: 460px;
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

.svg {
  max-width: 30px;
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
  animation: appear 1s ease-out both;
  animation-timeline: view();
  animation-range: entry 0% cover 40%;
}

.block-center {
  animation: appear 1s ease-out both;
  animation-timeline: view();
  animation-range: entry 0% cover 40%;
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

@media (min-width: 1024px) and (max-width: 1439px) {
  /* < lg */
  .project-card {
    height: 460px;
    margin: 30px;
  }
}

@media (min-width: 768px) and (max-width: 1023px) {
  /* < lg */
  .project-card {
    height: 540px;
    margin: 30px;
    width: 310px;
  }

  p {
    font-size: 14px;
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

@media (min-width: 426px) and (max-width: 767px) {
  /* < md */
  .project-card {
    height: 530px;
    margin: 20px;
  }

  .disapeard {
    display: none;
  }

  p {
    font-size: 14px;
  }
}

@media (min-width: 376px) and (max-width: 425px) {
  .project-card {
    height: 580px;
    margin: 10px;
    padding: 18px;
  }

  .disapeard {
    display: none;
  }

  p {
    font-size: 13px;
  }

  .project-btn {
    width: 190px;
  }
}

@media (min-width: 321px) and (max-width: 375px) {
  .project-card {
    height: 550px;
    margin: 10px;
    padding: 18px;
  }

  .disapeard {
    display: none;
  }

  p {
    font-size: 13px;
  }

  .project-btn {
    width: 190px;
  }
}

@media (max-width: 320px) {
  .project-card {
    height: 680px;
    margin: 10px;
    padding: 18px;
  }

  .disapeard {
    display: none;
  }

  p {
    font-size: 13px;
  }

  .project-btn {
    width: 190px;
  }

  span {
    font-size: 11px;
  }
}
</style>
