<template>
  <nav>
    <div class="logo">
      <img
        alt="Vue logo"
        src="../assets/mobileLogo_dailynews.svg"
        height="50"
      />
    </div>
    <div class="navlinks">
      <router-link to="/">Local</router-link>
      <router-link to="/global">Global</router-link>
    </div>
  </nav>
</template>


<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 80px;
  background: greenyellow;
}

.navlinks{
  display: flex;
  justify-content: space-around;
  width: 200px;
  height: fit-content;
 
}
</style>