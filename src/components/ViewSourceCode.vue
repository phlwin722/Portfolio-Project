<template>
  <button class="custom-button" type="button">
    <div class="button-icon-container">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 1024 1024"
        height="25px"
        width="25px"
      >
        <g transform="scale(-1,1) translate(-1024,0)">
          <path
            d="M224 480h640a32 32 0 1 1 0 64H224a32 32 0 0 1 0-64z"
            fill="#ffffff"
          ></path>
          <path
            d="m237.248 512 265.408 265.344a32 32 0 0 1-45.312 45.312l-288-288a32 32 0 0 1 0-45.312l288-288a32 32 0 1 1 45.312 45.312L237.248 512z"
            fill="#ffffff"
          ></path>
        </g>
      </svg>
    </div>
    <p class="button-text">View Source Code</p>
  </button>
</template>

<style scoped>
.custom-button {
  background-color: #0488e0;
  text-align: center;
  width: 15rem; /* 60 x 0.25rem */
  height: 3.3rem; /* 12 x 0.25rem */
  border-radius: 1rem; /* 2xl */
  position: relative;
  cursor: pointer;
  color: black;
  font-weight: bold;
  display: inline-block;
}

.button-icon-container {
  background-color: #006bb3;
  border-radius: 0.75rem; /* xl */
  height: 2.5rem; /* 10 x 0.25rem */
  width: 25%;
  position: absolute;
  top: 4px;
  left: 0.25rem; /* 1 */
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 10;
  transition: width 0.5s ease;
}

.custom-button:hover .button-icon-container {
  width: 14.2rem; /* ~232px */
}

.button-text {
  color: white;
  font-weight: bold;
  font-size: 1rem; /* base */
  transform: translateX(1.25rem); /* translate-x-5 */
  margin-top: 0.4rem; /* q-mt-sm */
  padding-top: 0.25rem; /* q-pt-xs */
  margin-left: 0.5rem; /* q-ml-sm */
}

@media (max-width: 375px) {
  .button-text {
    font-size: 13px;
  }

  .custom-button:hover .button-icon-container {
    width: 13rem; /* ~232px */
  }
}
@media (max-width: 320px) {
  .button-text {
    font-size: 13px;
  }

  .custom-button:hover .button-icon-container {
    width: 11.2rem; /* ~232px */
  }
}
</style>
