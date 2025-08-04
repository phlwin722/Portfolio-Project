<template>
    <button class="button" @click="cv">
        Download CV
        <svg fill="currentColor" viewBox="0 0 24 24" class="icon" xmlns="http://www.w3.org/2000/svg">
        <path 
            d="M12 16.5l4.5-4.5h-3v-6h-3v6h-3l4.5 4.5zM5 18v1.5h14V18H5z"
        />
        </svg>
    </button>

</template>

<style scoped>
/* From Uiverse.io by adeladel522 */ 
.button {
  position: relative;
  transition: all 0.3s ease-in-out;
  box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.2);
  padding-block: 0.5rem;
  padding-inline: 1.25rem;
  background-color: #006bb3;
  border-radius: 9999px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  color: #ffff;
  gap: 10px;
  font-weight: bold;
  border: 3px solid #ffffff4d;
  outline: none;
  overflow: hidden;
  font-size: 15px;
}
.icon {
  width: 24px;
  height: 24px;
  transition: all 0.3s ease-in-out;
}
.button:hover {
  transform: scale(1.05);
  border-color: #fff9;
}
.button:hover .icon {
  transform: translate(4px);
}
.button:hover::before {
  animation: shine 1.5s ease-out infinite;
}
.button::before {
  content: "";
  position: absolute;
  width: 100px;
  height: 100%;
  background-image: linear-gradient(
    120deg,
    rgba(255, 255, 255, 0) 30%,
    rgba(255, 255, 255, 0.8),
    rgba(255, 255, 255, 0) 70%
  );
  top: 0;
  left: -100px;
  opacity: 0.6;
}
@keyframes shine {
  0% {
    left: -100px;
  }
  60% {
    left: 100%;
  }
  to {
    left: 100%;
  }
}
</style>