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
   <router-link id="navLink" to="/"> Local</router-link>
    <router-link id="navLink" to="/global">Global</router-link>
    </div>
  </nav>
</template>


<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 80px;
  /* background: greenyellow; */
}

.navlinks {
  display: flex;
  justify-content: space-around;
  width: 200px;
  height: fit-content;
}

.navlinks a {
  text-decoration: none;
}

.router-link-active{
  font-size: 20px;
}

/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  nav {
    background: red;
  }
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {
  nav {
    background: green;
  }
}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
  nav {
    background: blue;
  }
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  nav {
    background: orange;
  }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  nav {
    background: pink;
  }
}
</style>