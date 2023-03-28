<script setup lang="ts"></script>

<template>
  <div class="navbar">

    <div class="logo"></div>

    <div class="buttongroup">
      <button class="navigationButton">Home</button>
      <button class="navigationButton">Our Vision</button>
      <button class="navigationButton">Test</button>
    </div>

    <div></div>
  </div>
</template>

<style scoped>

.navbar {
  background: #159957; /* fallback for old browsers */
  background: -webkit-linear-gradient(to right, #159957, #155799); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to right, #159957, #155799); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */


  display: flex;
  align-items: center;
  justify-content: space-between;

  position: absolute;
  left: 0;
  right: 0;
  top: 0;

  width: 100%;
  height: 10%;
}

.buttongroup {
  justify-content: center;
}

.navigationButton {
  transition-duration: 0.2s;
  margin: 12px;
  font-size: 20px;


  position: relative;

  border: none;
  display: inline-block;
  color: white;
  text-decoration: none;
  background: rgba(255, 122, 89, 0%);

}
.navigationButton:hover::after {
  /*
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
  */
  transform-origin: bottom left;
  transform: scale(1);
}

.navigationButton::after {
  content: "";
  position: absolute;
  width: 100%;
  transform: scale(0);
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: white;
  transition: transform 0.25s ease-out;
  -webkit-transform-origin: bottom right;
}


</style>