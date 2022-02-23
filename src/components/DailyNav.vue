<template>
  <nav>
    <div class="logo">
      <img alt="Vue logo" src="../assets/DailyNewLogowtxt.svg" height="70" />
    </div>
    <div class="navlinks">
      <router-link id="navLink" to="/"> Local</router-link>
      <router-link id="navLink" to="/global">Global</router-link>
    </div>
  </nav>
</template>


<style scoped>
nav {
  grid-area: nav;
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  height: 80px;
  font-family: "Inter", sans-serif;
 
  /* background: greenyellow; */
}


.logo {
  margin-left: 15px;
}

.navlinks {
  display: flex;
  justify-content: space-around;
  width: 200px;
  height: fit-content;
}

.navlinks a {
  color: black;
  text-decoration: none;
}

.router-link-active {
  text-decoration: none;
  border-bottom: black 4px solid;
}



/* Responsivnes________  */

/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  nav{
    /* background: greenyellow; */
  }
   
  .navlinks {
    width: 120px;
    justify-content: space-between;
    margin-right: 30px;
  }
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  nav {
    /* background: orange; */
    /* margin: 0 2% 0 2%; */
  }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  nav {
    /* background: pink; */
    /* margin: 0 5% 0 5%; */
  }
}
</style>